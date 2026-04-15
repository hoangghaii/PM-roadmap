# CHANGE REQUEST FORM

| Field | Chi Tiết |
|---|---|
| **CR ID** | CR-[ProjectCode]-[XXX] |
| **Tên thay đổi** | [Tiêu đề ngắn gọn mô tả thay đổi] |
| **Ngày yêu cầu** | DD/MM/YYYY |
| **Người yêu cầu** | [Tên - Role - Email] |
| **Dự án** | [Tên dự án - Project ID] |
| **Priority** | ☐ Critical  ☐ High  ☐ Medium  ☐ Low |
| **Loại thay đổi** | ☐ Scope  ☐ Timeline  ☐ Budget  ☐ Resource  ☐ Technical |

---

## MÔ TẢ THAY ĐỔI

[Chi tiết thay đổi yêu cầu. Viết đủ để người không biết context cũng hiểu được.]

**Hướng dẫn điền:**
- Mô tả **hiện tại** (as-is) và **sau thay đổi** (to-be)
- Bao gồm cả technical và business aspects
- Đính kèm mockup/wireframe/spec nếu có

**Ví dụ tốt:**
> Hiện tại, màn hình checkout chỉ hỗ trợ thanh toán bằng thẻ tín dụng (Visa/Mastercard). Yêu cầu thêm phương thức thanh toán MoMo và ZaloPay vào luồng checkout, với UX tương tự như thanh toán thẻ hiện tại. Người dùng có thể chọn phương thức thanh toán trên trang cart và checkout.

---

## LÝ DO / BUSINESS JUSTIFICATION

[Tại sao cần thay đổi? Business value là gì? Cost of NOT making this change?]

**Hướng dẫn điền:**
- Lý do phải **business-driven**, không phải technical preference
- Quantify impact nếu có thể: "Ước tính tăng 15% conversion rate dựa trên research"
- Nếu là emergency change, explain urgency rõ ràng

**Ví dụ:**
> Competitor vừa launch tính năng MoMo payment. User research cho thấy 40% người dùng tại Việt Nam prefer mobile payment over thẻ tín dụng. Nếu không thêm tính năng này trước Q3, ước tính mất 200-300 orders/tháng. Business đã cam kết với partner MoMo trước 30/06.

---

## IMPACT ANALYSIS

| Dimension | Bị ảnh hưởng? | Chi tiết Impact |
|---|---|---|
| **Scope** | ☐ Tăng  ☐ Giảm  ☐ Không đổi | [Mô tả feature/deliverable nào bị thêm/bớt] |
| **Timeline** | ☐ +[X] ngày  ☐ Không đổi  ☐ Rút ngắn | [Milestone nào bị push? Ngày go-live mới?] |
| **Budget** | ☐ +[X] triệu  ☐ Không đổi  ☐ Giảm | [Chi tiết cost: nhân công, license, infra] |
| **Quality** | ☐ Tăng  ☐ Giảm  ☐ Không đổi | [Ảnh hưởng đến test coverage, tech debt?] |
| **Risk** | ☐ Risk mới: [Mô tả] | [Risk mới phát sinh nếu approve change này] |
| **Resources** | ☐ Cần thêm: [Mô tả] | [Thêm người? Thêm skills?] |
| **Dependencies** | ☐ Ảnh hưởng: [Mô tả] | [Dự án/team khác bị ảnh hưởng không?] |

**Impact tổng hợp:**
> [PM viết 2-3 câu tóm tắt impact tổng thể. Ví dụ: "Change này sẽ trễ go-live 2 tuần (từ 01/07 → 15/07) và tăng budget thêm 50 triệu cho 2 developer sprint thêm. Risk tăng nhẹ do cần integrate với 2 payment vendors mới trong thời gian ngắn."]

---

## OPTIONS

**Option A — Implement đầy đủ (Recommended)**

Mô tả: [Implement tất cả yêu cầu trong CR]

Impact:
- Timeline: +[X] ngày (Go-live: DD/MM/YYYY)
- Budget: +[X] triệu
- Risk: [Mức độ]
- Resources: [Cần gì thêm]

Pros:
- [Pro 1]
- [Pro 2]

Cons:
- [Con 1]

---

**Option B — Partial implementation (Phased approach)**

Mô tả: [Implement phần cốt lõi trước, defer phần còn lại sang phase 2]

Impact:
- Timeline: +[X] ngày (nhỏ hơn Option A)
- Budget: +[X] triệu (nhỏ hơn Option A)
- Risk: Thấp hơn

Pros:
- Deliver business value sớm hơn
- Giảm risk trong sprint hiện tại

Cons:
- Cần sprint thêm sau cho phần defer
- User experience có thể không nhất quán tạm thời

---

**Option C — Reject / Defer**

Mô tả: Không implement trong dự án hiện tại

Impact:
- Timeline: Không đổi
- Budget: Không đổi
- Business risk: [Mô tả hậu quả nếu không làm]

---

**Khuyến nghị PM:** Option [A/B/C] vì [lý do ngắn gọn, tập trung vào business value và risk trade-off]

---

## QUYẾT ĐỊNH

☐ **Approved** — Thực hiện theo khuyến nghị của PM
☐ **Approved with modification** — [Mô tả thay đổi so với recommendation]
☐ **Rejected** — Lý do: [Mô tả lý do từ chối]
☐ **Deferred** — Xem xét lại vào: [Ngày / milestone]

**Điều kiện (nếu có):**
[Approval có điều kiện gì không? Ví dụ: "Approved với điều kiện không push go-live date."]

| Vai trò | Tên | Quyết định | Ký | Ngày |
|---|---|---|---|---|
| Project Sponsor | | | | |
| Project Manager | | | | |
| Technical Lead | | | | |

---

## IMPLEMENTATION PLAN (Điền sau khi Approved)

| Task | Owner | Start | End | Notes |
|---|---|---|---|---|
| [Task 1] | | DD/MM | DD/MM | |
| [Task 2] | | DD/MM | DD/MM | |

**Updated Project Schedule:**
- Milestone [X] mới: DD/MM/YYYY (cũ: DD/MM/YYYY)
- Go-live mới: DD/MM/YYYY (cũ: DD/MM/YYYY)

**Updated Budget:**
- Budget cũ: [X] triệu
- Thêm từ CR này: [X] triệu
- Budget mới: [X] triệu

---

## HƯỚNG DẪN SỬ DỤNG CHANGE REQUEST

### Khi Nào Cần Change Request?

Bắt buộc dùng CR khi:
- Thêm hoặc bớt bất kỳ feature nào trong scope
- Thay đổi timeline hơn 5 ngày làm việc
- Thay đổi budget hơn 5% tổng budget
- Thay đổi team composition (thêm/bỏ core team member)
- Thay đổi technology stack

Không cần CR (nhưng cần document trong meeting minutes):
- Bug fixes trong existing scope
- UX tweaks nhỏ không ảnh hưởng functionality
- Clarifications về requirements (không phải thay đổi)

### Change Control Process

```
Stakeholder yêu cầu thay đổi
        ↓
PM tiếp nhận, tạo CR Form
        ↓
PM phân tích impact (1-3 ngày tùy complexity)
        ↓
PM present cho Change Control Board hoặc Sponsor
        ↓
Decision: Approve / Modify / Reject / Defer
        ↓
Nếu Approved → Update Project Plan, Notify team
        ↓
Implement → Verify → Close CR
```

### Tips Cho PM

**Đừng biến Change Control thành rào cản:** Mục tiêu là visibility và informed decisions, không phải "nói không với tất cả thay đổi."

**Impact analysis trung thực:** Nếu change này thực sự cần thêm 3 tuần, đừng nói "sẽ cố gắng làm trong 1 tuần." Dưới-estimate để được approve là anti-pattern nguy hiểm.

**Document mọi verbal approval:** Nếu sponsor approve qua Slack/email/verbal, PM vẫn cần tạo formal CR và ghi lại quyết định. "Verbal agreement không phải agreement."

---

---

# CHANGE LOG — [Tên Dự Án]

**Project ID:** [PC-YYYYMM-XXX]
**PM:** [Tên PM]
**Cập nhật lần cuối:** DD/MM/YYYY

| CR ID | Tên thay đổi | Ngày yêu cầu | Requestor | Priority | Status | Ngày quyết định | Decision | Impact (Time/Budget) | Notes |
|---|---|---|---|---|---|---|---|---|---|
| CR-001 | [Tên thay đổi đầu tiên] | DD/MM/YYYY | [Tên - Role] | High | Pending | - | - | TBD | |
| CR-002 | [Tên thay đổi thứ hai] | DD/MM/YYYY | [Tên - Role] | Medium | Approved | DD/MM/YYYY | Approved | +5 ngày / +20M | Implement sprint 6 |
| CR-003 | [Tên thay đổi thứ ba] | DD/MM/YYYY | [Tên - Role] | Low | Rejected | DD/MM/YYYY | Rejected | N/A | Out of scope, defer to v2 |
| CR-004 | [Tên thay đổi thứ tư] | DD/MM/YYYY | [Tên - Role] | Critical | In Review | - | - | TBD | Đang phân tích impact |

**Status Codes:**
- `Pending` — Mới nhận, chưa phân tích
- `In Review` — PM đang phân tích impact
- `Pending Approval` — Đã analyze, đang chờ sponsor quyết định
- `Approved` — Được approve, đang implement
- `Rejected` — Bị từ chối
- `Deferred` — Lùi lại, xem xét sau
- `Closed` — Đã implement và verify xong

---

**Budget Impact Summary:**
| Tháng | CRs Approved | Tổng Impact Budget | Ghi chú |
|---|---|---|---|
| [Tháng 1] | [X CRs] | +[X triệu] | |
| [Tháng 2] | [X CRs] | +[X triệu] | |
| **Tổng** | | **+[X triệu]** | |

---

*Change Log là công cụ quản lý, không phải bureaucracy. Mục tiêu: mọi người biết tại sao dự án thay đổi.*
