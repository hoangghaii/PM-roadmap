# Prioritization Frameworks - Giới Thiệu

## Tại Sao Phải Prioritize?

Bạn sẽ luôn có nhiều việc hơn time/resources cho phép. Không có framework, bạn sẽ:
- Làm theo tiếng kêu to nhất (HiPPO - Highest Paid Person's Opinion)
- Bị overwhelm, không biết bắt đầu từ đâu
- Waste resources vào features low-impact

**Mục tiêu của prioritization:** Đảm bảo team làm những việc có **impact cao nhất** với **effort thấp nhất**.

---

## Framework 1: RICE Scoring

**Công thức:**
```
RICE Score = (Reach × Impact × Confidence) / Effort
```

| Yếu Tố | Ý Nghĩa | Cách Đo |
|---------|---------|---------|
| **Reach** | Số users bị ảnh hưởng trong 1 period | Users/month, orders/month |
| **Impact** | Mức độ ảnh hưởng lên mỗi user | Scale 0.25 - 3x |
| **Confidence** | Độ chắc chắn về estimates | % (100%, 80%, 50%) |
| **Effort** | Tổng công việc cần thiết | Person-months |

**Impact Scale:**
- 3x = Massive impact
- 2x = High
- 1x = Medium
- 0.5x = Low
- 0.25x = Minimal

**Ví dụ RICE cho Logistics App:**

| Feature | Reach | Impact | Confidence | Effort | RICE |
|---------|-------|--------|-----------|--------|------|
| Real-time tracking | 5,000 | 2x | 80% | 2 | **4,000** |
| Bulk CSV import | 200 | 3x | 90% | 1 | **540** |
| Dark mode | 10,000 | 0.25x | 70% | 0.5 | **3,500** |
| API webhooks | 50 | 3x | 80% | 3 | **40** |

→ Real-time tracking wins, dù Dark mode có Reach cao hơn.

---

## Framework 2: MoSCoW Method

Phân loại features vào 4 buckets:

**Must Have** — Sản phẩm fail nếu không có
- Core functionality, legal requirements, safety features
- Ví dụ: Login, order creation, payment processing

**Should Have** — Quan trọng nhưng không critical
- Có thể launch without, nhưng nên có sớm
- Ví dụ: Email notifications, basic reporting

**Could Have** — Nice to have nếu có time/resources
- Low impact, có thể postpone indefinitely
- Ví dụ: Themes, advanced filters, dark mode

**Won't Have** — Explicitly không làm lần này
- Scope management — giúp team focus
- Ví dụ: "Native mobile app sẽ không có trong V1"

**Khi nào dùng MoSCoW:** Sprint planning, MVP definition, khi cần đơn giản hơn RICE.

---

## Framework 3: Value vs Effort Matrix

Vẽ trên 2 trục:
```
HIGH VALUE
     │ Quick Wins      │ Major Projects  │
     │ (DO FIRST)      │ (PLAN)          │
─────┼─────────────────┼─────────────────┼──── EFFORT
     │ Fill-Ins        │ Thankless Tasks │
LOW  │ (DO IF TIME)    │ (AVOID)         │
VALUE│                 │                 │
     LOW EFFORT        HIGH EFFORT
```

**Ứng dụng:** Nhanh, visual, dễ align với stakeholders. Tốt cho workshops.

---

## Framework 4: ICE Score

```
ICE = Impact + Confidence + Ease
```

- Đơn giản hơn RICE
- Không có Reach factor
- Tốt cho growth experiments, không tốt cho product roadmap

**Impact:** 1-10 (10 là impact cao nhất)
**Confidence:** 1-10 (10 là chắc chắn nhất)
**Ease:** 1-10 (10 là dễ làm nhất)

---

## Framework 5: Kano Model

Phân loại features theo cách users phản ứng:

**Basic Needs (Expected):**
- Users **expect** có — nếu không có, họ bực bội
- Nếu có, họ không impressed
- Ví dụ: App load nhanh, không crash, basic search

**Performance Needs:**
- Càng nhiều càng tốt — linear relationship
- Ví dụ: Tracking accuracy, delivery speed, search results quality

**Delighters (Excitement):**
- Users không expect — nếu có, họ love it
- Nếu không có, họ không care
- Ví dụ: Proactive delay notification, "driver gần đến" push notification

**Indifferent:**
- Users không care có hay không

**Reverse:**
- Một số users muốn, một số không muốn
- Ví dụ: Tự động dark mode theo giờ

**Ứng dụng Kano:** Khi design new product/feature, đảm bảo Basic Needs trước, rồi mới đến Delighters.

---

## Khi Nào Dùng Framework Nào?

| Situation | Framework Tốt Nhất |
|-----------|-------------------|
| Prioritize quarterly roadmap | RICE |
| Define MVP scope | MoSCoW |
| Quick team alignment meeting | Value vs Effort Matrix |
| Growth experiment backlog | ICE |
| New product design | Kano Model |
| Stakeholder conflict về priorities | RICE (objective, data-driven) |

---

## Bài Tập: RICE Scoring Thực Tế

Áp dụng RICE cho 5 features của một logistics app:

| Feature | Reach | Impact | Confidence | Effort | RICE |
|---------|-------|--------|-----------|--------|------|
| Push notifications khi hàng đến | ??? | ??? | ??? | ??? | ??? |
| Tự động tính phí ship | ??? | ??? | ??? | ??? | ??? |
| Review/rating shipper | ??? | ??? | ??? | ??? | ??? |
| Multi-language support | ??? | ??? | ??? | ??? | ??? |
| Loyalty points program | ??? | ??? | ??? | ??? | ??? |

*Điền vào và so sánh với nhóm để thấy sự khác biệt trong judgment.*

**Note quan trọng:** RICE không phải công thức magic. Nó là tool để **structure conversation**, không để replace judgment.
