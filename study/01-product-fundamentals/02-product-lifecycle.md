# Product Development Lifecycle

## Tổng Quan

Product development không phải là "viết spec → engineering build → ship". Đó là một quá trình lặp đi lặp lại, liên tục khám phá và validate trước khi đầu tư build.

---

## Double Diamond Model

```
    Discover        Define          Develop          Deliver
  ____________    ____________    ____________    ____________
 /            \  /            \  /            \  /            \
/   Explore    \/   Focus on   \/   Create     \/   Ship &    \
\   broadly   /\   right prob /\   solutions  /\   measure   /
 \____________/  \____________/  \____________/  \____________/

   DIVERGE →    ← CONVERGE       DIVERGE →    ← CONVERGE
```

**Diamond 1: Khám phá vấn đề đúng**
- Discover: Research rộng, open-ended, không assume
- Define: Synthesize insights, frame the problem clearly

**Diamond 2: Tạo ra giải pháp đúng**
- Develop: Ideate, prototype, test nhiều giải pháp
- Deliver: Build, ship, measure, iterate

---

## Product Development Lifecycle (6 Giai Đoạn)

### 1. Discovery (Khám Phá)
**Mục tiêu:** Hiểu problem, validate assumption
**PM làm gì:**
- User interviews, surveys
- Market research
- Competitive analysis
- Data analysis (existing product)
- Stakeholder interviews

**Output:** Insights document, problem statement

**Ví dụ - Tính năng "Track Shipment":**
> PM phỏng vấn 20 shipper và 20 người nhận hàng. Phát hiện: 73% người nhận hàng gọi điện cho shipper để hỏi vị trí vì không có thông tin. Đây là pain point rõ ràng.

### 2. Define (Định Nghĩa)
**Mục tiêu:** Frame problem rõ ràng, set goals
**PM làm gì:**
- Problem statement
- User personas
- Success metrics
- Scope decision (in/out)
- Prioritization

**Output:** PRD v1, one-pager

**Ví dụ - Track Shipment:**
> Problem: "Người nhận hàng không biết khi nào shipper đến, dẫn đến missed deliveries và frustration."
> Goal: Giảm "where is my order?" calls xuống 80%

### 3. Design (Thiết Kế)
**Mục tiêu:** Tạo giải pháp phù hợp
**PM làm gì:**
- Collaborate với Designer
- Review wireframes, give feedback
- User testing với prototypes
- Iterate dựa trên feedback
- Sign off design

**Output:** Final designs, user flow diagrams

**Ví dụ - Track Shipment:**
> PM và Designer test 3 concepts: SMS notifications, in-app map tracking, push notifications. User testing với 10 users → real-time map tracking được ưa thích nhất.

### 4. Develop (Phát Triển)
**Mục tiêu:** Build đúng cái đã design
**PM làm gì:**
- Clarify requirements với engineering
- Unblock team (quyết định nhanh)
- Review builds, QA
- Adjust scope nếu cần (scope creep management)
- Stakeholder updates

**Output:** Working software

**Ví dụ - Track Shipment:**
> Engineering estimate: 6 tuần. PM quyết định launch MVP với 3 phases: SMS only (2 tuần), Basic map (2 tuần), Real-time map (2 tuần).

### 5. Deploy (Triển Khai)
**Mục tiêu:** Ship an toàn, đúng người đúng thời điểm
**PM làm gì:**
- Launch plan
- Phased rollout (5% → 20% → 100%)
- Go-to-market coordination
- Internal training
- Documentation

**Output:** Feature live, launch announcement

### 6. Measure (Đo Lường)
**Mục tiêu:** Validate impact, learn, iterate
**PM làm gì:**
- Monitor metrics vs targets
- Analyze user feedback
- Bug triage
- Decide: iterate, pivot, or sunset
- Document learnings

**Output:** Post-launch review, iteration plan

---

## Agile/Scrum từ Góc Nhìn PM

### Sprint Ceremonies

**Sprint Planning (Mỗi 2 tuần, đầu sprint)**
- PM chuẩn bị: Prioritized backlog với stories đã refined
- PM trong meeting: Present stories, clarify requirements
- Output: Sprint goal + sprint backlog

**Daily Standup (Mỗi ngày, 15 phút)**
- PM không phải "run" standup, nhưng nên attend
- PM lắng nghe: blockers nào cần PM unblock?
- PM action: Quyết định nhanh, không để engineering chờ

**Sprint Review / Demo (Cuối sprint)**
- Engineering demo what's built
- PM gather feedback từ stakeholders
- PM accept/reject completed stories

**Retrospective (Cuối sprint, 1 tiếng)**
- Team discuss: What went well? What to improve?
- PM role: Facilitate, listen, act on feedback
- Output: Action items cho sprint tiếp theo

**Backlog Refinement / Grooming (Giữa sprint)**
- PM present upcoming stories
- Engineering estimate, ask questions
- PM refine based on engineering input

### Vai Trò PM trong Agile

```
Discovery (PM heavy)    →    Development (Engineering heavy)
User Research                Sprint Planning
Problem Definition           Daily Standups  
PRD Writing                  Unblocking Team
Roadmapping                  Scope Management
Stakeholder Alignment        Launch Planning
```

---

## Ví Dụ Thực Tế: Feature "Bulk Import Orders" tại Logistics Company

**Tháng 1 - Discovery:**
- PM phỏng vấn 15 merchants → 80% manually enter orders một cách thủ công
- Pain: "Tôi mất 2 tiếng mỗi sáng để nhập đơn hàng từ spreadsheet"
- Opportunity: Nếu giảm 90% thời gian nhập liệu, merchants happy hơn, churn giảm

**Tháng 1.5 - Define:**
- Problem: Merchants lớn (>50 orders/ngày) không thể scale vì manual data entry
- Solution: Bulk import via CSV/Excel
- Target users: Merchants >50 orders/ngày (~200 merchants)
- Success metric: 50% eligible merchants sử dụng bulk import trong 60 ngày

**Tháng 2 - Design:**
- Wireframes: Upload flow, validation errors, success state
- User testing: 5 merchants test prototype → confusion về error messages
- Iterate: Better error messages, preview before import

**Tháng 2.5-3 - Develop:**
- Engineering builds: CSV parser, validation engine, batch API
- PM clarifies: Làm sao xử lý duplicate orders? Character encoding?
- PM decisions: Skip duplicates (không block import), UTF-8 only for now

**Tháng 3 - Deploy:**
- Soft launch: 20 beta merchants
- Training: Video tutorial + in-app guide
- Go-to-market: Email campaign cho eligible merchants

**Tháng 3.5 - Measure:**
- 65% eligible merchants adopted trong 45 ngày (target: 50% trong 60 ngày)
- Average time saving: 90 minutes/ngày per merchant
- Bug: 3 edge cases với special characters → hot fix trong tuần 1
- Next: API import cho merchants với own systems
