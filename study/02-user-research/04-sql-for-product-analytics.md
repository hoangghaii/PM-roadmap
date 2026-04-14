# SQL cho Product Analytics

## Tại Sao PM Cần SQL?

Khi bạn cần trả lời "bao nhiêu users dùng feature X?", bạn không muốn chờ Data team 3 ngày. Với SQL, bạn tự trả lời trong 5 phút.

SQL giúp PM:
- Validate assumptions với data thực
- Identify trends và anomalies nhanh
- Prepare analysis cho meetings
- Build credibility với stakeholders

---

## Cú Pháp Cơ Bản

```sql
SELECT column1, column2
FROM table_name
WHERE condition
ORDER BY column1 DESC
LIMIT 100;
```

---

## Aggregations — Tóm Tắt Data

```sql
-- Đếm số orders theo ngày
SELECT
  DATE(created_at) AS order_date,
  COUNT(*) AS total_orders,
  COUNT(DISTINCT user_id) AS unique_users,
  SUM(order_value) AS total_revenue,
  AVG(order_value) AS avg_order_value
FROM orders
WHERE created_at >= '2024-01-01'
GROUP BY DATE(created_at)
ORDER BY order_date DESC;
```

---

## JOINs — Kết Hợp Nhiều Bảng

```sql
-- Lấy thông tin user kèm số orders
SELECT
  u.user_id,
  u.email,
  u.created_at AS signup_date,
  COUNT(o.order_id) AS total_orders,
  SUM(o.order_value) AS lifetime_value
FROM users u
LEFT JOIN orders o ON u.user_id = o.user_id
GROUP BY u.user_id, u.email, u.created_at
ORDER BY lifetime_value DESC;
```

**INNER JOIN:** Chỉ rows có match ở cả 2 bảng
**LEFT JOIN:** Tất cả rows từ bảng trái + match từ bảng phải (NULL nếu không có)

---

## DAU/MAU — Metric Cơ Bản Nhất

```sql
-- Daily Active Users (DAU)
SELECT
  DATE(event_time) AS date,
  COUNT(DISTINCT user_id) AS dau
FROM events
WHERE event_type = 'app_open'
  AND event_time >= CURRENT_DATE - INTERVAL '30 days'
GROUP BY DATE(event_time)
ORDER BY date;

-- Monthly Active Users (MAU)
SELECT
  DATE_TRUNC('month', event_time) AS month,
  COUNT(DISTINCT user_id) AS mau
FROM events
WHERE event_type = 'app_open'
GROUP BY DATE_TRUNC('month', event_time)
ORDER BY month;

-- DAU/MAU Ratio (Stickiness)
WITH daily AS (
  SELECT DATE(event_time) AS date, COUNT(DISTINCT user_id) AS dau
  FROM events WHERE event_type = 'app_open'
  GROUP BY DATE(event_time)
),
monthly AS (
  SELECT DATE_TRUNC('month', event_time) AS month, COUNT(DISTINCT user_id) AS mau
  FROM events WHERE event_type = 'app_open'
  GROUP BY DATE_TRUNC('month', event_time)
)
SELECT
  d.date,
  d.dau,
  m.mau,
  ROUND(d.dau::decimal / m.mau * 100, 1) AS stickiness_pct
FROM daily d
JOIN monthly m ON DATE_TRUNC('month', d.date) = m.month
ORDER BY d.date DESC;
```

---

## Cohort Retention Analysis

```sql
-- Retention: Trong users đăng ký tháng X, bao nhiêu % còn active sau N tháng?
WITH cohorts AS (
  SELECT
    user_id,
    DATE_TRUNC('month', signup_date) AS cohort_month
  FROM users
),
user_activity AS (
  SELECT
    user_id,
    DATE_TRUNC('month', event_time) AS activity_month
  FROM events
  WHERE event_type = 'app_open'
  GROUP BY user_id, DATE_TRUNC('month', event_time)
)
SELECT
  c.cohort_month,
  DATEDIFF('month', c.cohort_month, a.activity_month) AS months_since_signup,
  COUNT(DISTINCT c.user_id) AS cohort_size,
  COUNT(DISTINCT a.user_id) AS retained_users,
  ROUND(COUNT(DISTINCT a.user_id)::decimal / COUNT(DISTINCT c.user_id) * 100, 1) AS retention_rate
FROM cohorts c
LEFT JOIN user_activity a ON c.user_id = a.user_id
  AND a.activity_month >= c.cohort_month
GROUP BY c.cohort_month, months_since_signup
ORDER BY c.cohort_month, months_since_signup;
```

---

## Funnel Analysis

```sql
-- Conversion funnel: View → Add to Cart → Checkout → Purchase
WITH funnel AS (
  SELECT
    user_id,
    MAX(CASE WHEN event_type = 'product_view' THEN 1 ELSE 0 END) AS viewed,
    MAX(CASE WHEN event_type = 'add_to_cart' THEN 1 ELSE 0 END) AS added_to_cart,
    MAX(CASE WHEN event_type = 'checkout_started' THEN 1 ELSE 0 END) AS started_checkout,
    MAX(CASE WHEN event_type = 'order_completed' THEN 1 ELSE 0 END) AS purchased
  FROM events
  WHERE event_time >= CURRENT_DATE - INTERVAL '30 days'
  GROUP BY user_id
)
SELECT
  COUNT(*) AS total_users,
  SUM(viewed) AS viewed_product,
  SUM(added_to_cart) AS added_to_cart,
  SUM(started_checkout) AS started_checkout,
  SUM(purchased) AS purchased,
  ROUND(SUM(added_to_cart)::decimal / COUNT(*) * 100, 1) AS view_to_cart_rate,
  ROUND(SUM(started_checkout)::decimal / SUM(added_to_cart) * 100, 1) AS cart_to_checkout_rate,
  ROUND(SUM(purchased)::decimal / SUM(started_checkout) * 100, 1) AS checkout_to_purchase_rate
FROM funnel;
```

---

## Feature Adoption Rate

```sql
-- Bao nhiêu % users dùng feature X sau khi nó launch?
SELECT
  DATE_TRUNC('week', first_use.first_use_date) AS week,
  COUNT(DISTINCT first_use.user_id) AS new_feature_users,
  (SELECT COUNT(DISTINCT user_id) FROM active_users WHERE week = week) AS total_active,
  ROUND(COUNT(DISTINCT first_use.user_id)::decimal /
    (SELECT COUNT(DISTINCT user_id) FROM active_users) * 100, 1) AS adoption_rate
FROM (
  SELECT user_id, MIN(event_time) AS first_use_date
  FROM events
  WHERE event_type = 'bulk_import_used'  -- feature cụ thể
  GROUP BY user_id
) first_use
GROUP BY DATE_TRUNC('week', first_use.first_use_date)
ORDER BY week;
```

---

## Revenue Per User

```sql
-- ARPU và LTV estimates
SELECT
  DATE_TRUNC('month', signup_date) AS cohort,
  COUNT(DISTINCT u.user_id) AS cohort_size,
  SUM(o.order_value) AS total_revenue,
  ROUND(SUM(o.order_value) / COUNT(DISTINCT u.user_id), 0) AS arpu_vnd,
  -- LTV (simple: avg monthly revenue × avg months active)
  ROUND(SUM(o.order_value) / COUNT(DISTINCT u.user_id) *
    AVG(DATEDIFF('month', u.signup_date, CURRENT_DATE)), 0) AS estimated_ltv
FROM users u
LEFT JOIN orders o ON u.user_id = o.user_id
  AND o.status = 'completed'
GROUP BY DATE_TRUNC('month', signup_date)
ORDER BY cohort DESC;
```

---

## CTEs — Common Table Expressions

```sql
-- Dùng WITH để tổ chức query phức tạp
WITH active_merchants AS (
  SELECT merchant_id
  FROM merchants
  WHERE status = 'active'
    AND last_order_date >= CURRENT_DATE - INTERVAL '30 days'
),
merchant_metrics AS (
  SELECT
    m.merchant_id,
    COUNT(o.order_id) AS monthly_orders,
    SUM(o.gmv) AS monthly_gmv
  FROM active_merchants m
  JOIN orders o ON m.merchant_id = o.merchant_id
  WHERE o.created_at >= CURRENT_DATE - INTERVAL '30 days'
  GROUP BY m.merchant_id
)
SELECT
  CASE
    WHEN monthly_orders >= 100 THEN 'High volume (100+)'
    WHEN monthly_orders >= 30 THEN 'Medium volume (30-99)'
    ELSE 'Low volume (<30)'
  END AS merchant_segment,
  COUNT(*) AS merchant_count,
  AVG(monthly_gmv) AS avg_gmv
FROM merchant_metrics
GROUP BY merchant_segment
ORDER BY avg_gmv DESC;
```

---

## Nơi Thực Hành SQL

1. **Mode Analytics SQL Tutorial** — mode.com/sql-tutorial (free, PM-focused)
2. **LeetCode SQL** — Easy + Medium problems
3. **SQLZoo** — Interactive, free
4. **HackerRank SQL** — Good for practice

**Target: 20 queries/tháng** — focus vào: JOINs, GROUP BY, CTEs, Window Functions
