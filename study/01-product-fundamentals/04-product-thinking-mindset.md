# Product Thinking Mindset

## Chuyển Từ "How" Sang "Why"

Với Developer: "Làm sao để tôi build tính năng này?"
Với PM: "Tại sao users cần tính năng này? Và liệu đây có phải giải pháp đúng không?"

**Ví dụ:**

> **Stakeholder yêu cầu:** "Thêm nút 'Copy tracking number'"
>
> **Developer thinking:** OK, let me add a clipboard API call button.
>
> **PM thinking:** Why do users need to copy tracking number? → They paste it into other sites/apps. → What if we just let them track directly in our app? → Maybe the real problem is lack of cross-carrier tracking, not the copy button.

Đây là **problem/solution thinking** — đừng assume solution, hãy validate problem trước.

---

## Jobs To Be Done (JTBD)

Framework này giải thích tại sao users "hire" một sản phẩm.

**Concept:** Users không mua sản phẩm — họ "hire" sản phẩm để hoàn thành một "job" (công việc) trong cuộc sống của họ.

**Format chuẩn:**
```
When [situation], I want to [motivation], so I can [expected outcome].
```

**Ví dụ Logistics:**
- "When tôi chờ hàng quan trọng, tôi muốn biết hàng đến lúc nào, so I can plan my day properly."
- "When tôi cần gửi hàng gấp, tôi muốn biết shipper nào available ngay, so I can make sure hàng đến đúng hẹn."
- "When nhân viên kho xử lý 100 đơn/ngày, they want to process quickly without errors, so they can close orders on time."

**Tại sao JTBD quan trọng:**
- Giúp bạn hiểu deeper motivation, không chỉ surface behavior
- Tránh build features mà không ai dùng
- Tìm ra competitors thực sự (không phải chỉ direct competitors)

**Ví dụ Airbnb:**
> Job: "When tôi muốn travel somewhere new, I want to feel at home, not like a tourist, so I can experience the place authentically."
> Airbnb "hired" for: Không phải chỉ rẻ hơn hotel — mà là authentic local experience.

---

## 5 Whys - Root Cause Analysis

Kỹ thuật đơn giản để tìm root cause thay vì solve symptom.

**Ví dụ:**

> **Problem:** User churn tăng 15% tháng này
>
> **Why 1:** Tại sao user cancel? → Họ nói app "too slow"
> **Why 2:** Tại sao app slow? → Loading time > 5 giây trên 3G
> **Why 3:** Tại sao loading time cao? → Đang load toàn bộ order history không pagination
> **Why 4:** Tại sao không có pagination? → Dev estimate "low priority" 6 tháng trước
> **Why 5:** Tại sao estimate low priority? → PM không có data về users on 3G

**Root cause:** Không có data về network conditions của users → blind spot về performance
**Solution thực sự:** Thu thập network data, establish performance monitoring, coi performance là first-class metric

---

## First Principles Thinking

Thay vì "best practice" hay analogy, hãy break down vấn đề thành fundamental truths và reason up.

**Cách làm:**
1. Identify assumptions
2. Break down thành fundamental pieces
3. Create solutions từ ground up

**Ví dụ - Elon Musk và Battery:**
> Assumption: "Batteries are expensive ($600/kWh) because they always have been"
> First Principles: What are batteries made of? → Carbon, nickel, aluminum, etc.
> What's the commodity cost? → ~$80/kWh
> → Tesla made own batteries, disrupted the market

**Ví dụ cho PM tại Vietnam logistics:**
> Assumption: "Khách hàng B2B cần account manager để onboard"
> First Principles: What do they actually need during onboarding?
> → Integration setup, data migration, team training, first successful shipment
> → What if: Self-serve onboarding với smart defaults + video guides?
> → Giảm cost, scale faster, khách hàng onboard 24/7 không cần wait cho account manager

---

## Systems Thinking

Nhìn sản phẩm như một hệ thống, không phải tập hợp features độc lập.

**Các thành phần:**
- **Inputs** → **Process** → **Outputs** → **Feedback loops**

**Ví dụ - Grab Driver-Passenger Matching:**

```
More Drivers → Shorter wait → More passengers use Grab → More demand
     ↑                                                         │
     └─────────────── More earnings per driver ───────────────┘
```

**Virtuous cycle (positive feedback loop):** Một khi đủ drivers và passengers, hệ thống tự reinforcing.

**Implication cho PM:** Feature decisions phải xét đến system effects. Giảm giá để attract passengers có thể hurt driver earnings → drivers leave → longer wait → passengers leave.

---

## Bài Tập: Chuyển Đổi Tư Duy

Với mỗi request dưới đây, viết:
1. Developer response (solution-focused)
2. PM questions (problem-focused)
3. JTBD statement

**Request 1:** "Thêm filter ngày tháng trong order history"

Developer: Add date range picker component...

PM questions:
- Tại sao users cần filter? Họ đang tìm gì?
- Bao nhiêu users dùng order history? Với mục đích gì?
- Có cách nào better để solve need này không?

JTBD: "When tôi cần reconcile monthly expenses, tôi muốn quickly find all orders from last month, so I can export cho accounting."

**Request 2:** "App cần dark mode"

PM questions:
- Ai đang request tính năng này?
- Họ dùng app vào lúc nào? (ban đêm? outdoor?)
- Dark mode có phải là true need, hay underlying need là eye strain reduction?
- Có bao nhiêu user complaints về brightness/eye strain?

**Request 3:** "Thêm tính năng chat giữa shipper và người nhận"

PM questions:
- Họ đang communicate thế nào hiện tại? (phone calls?)
- Loại thông tin nào họ cần communicate?
- Pain points của phone calls là gì? (intrusive? expensive? tracked?)
- Là unidirectional hay bidirectional need?

---

## Key Takeaways

1. **Luôn hỏi "Why" trước "How"** — understand the problem before jumping to solution
2. **Users nói gì họ muốn ≠ Họ thực sự cần gì** — dig deeper
3. **Bạn không phải user** — đừng project personal preferences
4. **Data + Empathy** — cần cả hai, không chỉ một
5. **Build less, learn more** — validate fast, build only what's validated
