# Xây Dựng PMO (Project Management Office)

## PMO Là Gì?

PMO là bộ phận hoặc nhóm chịu trách nhiệm **chuẩn hóa quy trình PM**, cung cấp hỗ trợ và governance cho toàn bộ dự án trong tổ chức.

PMO không phải "cảnh sát" của dự án — PMO tốt là **enabler**, giúp PM deliver tốt hơn.

---

## 3 Loại PMO

| Loại | Authority | Vai trò chính | Phù hợp với |
|---|---|---|---|
| **Supportive** | Thấp | Cung cấp templates, training, best practices — advisory | Tổ chức PM maturity thấp, muốn bắt đầu nhẹ nhàng |
| **Controlling** | Trung bình | Yêu cầu tuân thủ methodology, review dự án, audit | Tổ chức cần standardization nhưng PM vẫn độc lập |
| **Directive** | Cao | Trực tiếp quản lý tất cả dự án, PM báo cáo cho PMO | Enterprise lớn, nhiều dự án liên quan phức tạp |

**Progression:** Hầu hết PMO bắt đầu từ Supportive, tiến lên Controlling khi trust được xây dựng.

---

## Khi Nào Công Ty Cần PMO?

Dấu hiệu nhận biết:
- Có hơn 5 dự án song song mà không ai biết tổng thể
- Mỗi PM làm theo cách riêng, không có standard
- Dự án hay trễ, over budget mà không rõ lý do
- C-level không có visibility về portfolio health
- PM junior không có hướng dẫn, phải tự mò
- Lessons learned từ dự án này không được áp dụng cho dự án khác

**Rule of thumb:** Nếu công ty có >10 dự án/năm và >3 PM, PMO thường mang lại ROI dương.

---

## 7 Bước Xây Dựng PMO

### Bước 1: Assessment — Đánh Giá PM Maturity Hiện Tại

Trước khi build PMO, phải hiểu **điểm xuất phát**.

**PM Maturity Model (5 cấp):**
```
Level 1: Initial     — Ad hoc, chaotic, phụ thuộc vào cá nhân
Level 2: Managed     — Có quy trình cơ bản nhưng không nhất quán
Level 3: Defined     — Quy trình được document, training có
Level 4: Quantified  — Đo lường performance, data-driven
Level 5: Optimizing  — Continuous improvement, benchmark với industry
```

**Assessment activities:**
- Survey PM hiện tại về quy trình họ đang dùng
- Review 5-10 dự án gần đây: on time? on budget? what went wrong?
- Interview C-level về expectations từ PMO
- Benchmark với industry (PMI, Gartner reports)

### Bước 2: PMO Charter

PMO cũng cần Charter của nó:
- **Mission:** PMO tồn tại để làm gì?
- **Scope:** PMO covers loại dự án nào?
- **Authority:** PMO có quyền gì? Có thể stop/pause dự án không?
- **Resources:** Bao nhiêu FTE? Budget?
- **Success metrics:** PMO đo lường thành công bằng gì?

### Bước 3: Process Standardization

Không cần chuẩn hóa tất cả mọi thứ cùng lúc. Priority:

```
Phase 1 (tháng 1-3): Templates cơ bản
  - Project Charter
  - Risk Register
  - Status Report
  - Meeting Minutes

Phase 2 (tháng 4-6): Processes
  - Change Request process
  - Escalation path
  - Project lifecycle definition (stages và gates)

Phase 3 (tháng 7-12): Governance
  - Project intake process (ai decide dự án nào được làm?)
  - Portfolio review cadence
  - Benefits realization tracking
```

### Bước 4: Tool Selection

Không cần tool phức tạp ngay từ đầu.

| Stage | Tool Recommendation |
|---|---|
| PMO mới (< 10 projects) | Excel/Google Sheets + Notion/Confluence |
| PMO growing (10-30 projects) | Jira + Confluence + Google Sheets |
| PMO mature (30+ projects) | MS Project Online / Planview / ServiceNow |

**Anti-pattern:** Mua tool đắt tiền trước khi có quy trình → tool bị bỏ không.

### Bước 5: Training & Capability Building

PMO chỉ hiệu quả khi PM team có đủ năng lực:

- Onboarding program cho PM mới (1-2 ngày)
- Monthly knowledge sharing sessions
- Template library với hướng dẫn sử dụng
- Mentoring program: Senior PM guide Junior PM
- External training budget (certifications)

### Bước 6: Governance Setup

**Project Intake Process:**
```
Business unit submit project request
         ↓
PMO review: strategic fit? resource availability? ROI?
         ↓
Portfolio Review Board approve/reject/defer
         ↓
Project initiated với assigned PM
         ↓
Stage Gate Reviews (at each milestone)
         ↓
Project closure & lessons learned
```

**Reporting Cadence:**
- Weekly: Individual project status (PM → PMO)
- Monthly: Portfolio health dashboard (PMO → Directors)
- Quarterly: Portfolio review với C-level (PMO → Board)

### Bước 7: Continuous Improvement

PMO không phải set-and-forget:
- Quarterly retrospective của PMO team
- Annual PM community survey
- Benchmark với industry data
- Update templates và processes dựa trên lessons learned

---

## PMO KPIs

| KPI | Definition | Target |
|---|---|---|
| On-time delivery rate | % projects delivered on/before deadline | >80% |
| Budget variance | Average % over/under budget | <10% |
| PM certification rate | % PM có ít nhất 1 certification | >60% |
| Template adoption | % projects dùng standard templates | >90% |
| Stakeholder satisfaction | Survey score (1-5) | >4.0 |
| Lessons learned capture | % projects có lessons learned documented | >95% |

---

## Change Management Khi Implement PMO

**Thực tế:** Nhiều PM và Manager **resist** PMO vì lo ngại mất autonomy.

### Resistance Patterns và Cách Xử Lý

| Resistance | Nguyên nhân | Cách xử lý |
|---|---|---|
| "Thêm bureaucracy" | Templates = overhead | Show value: template tiết kiệm thời gian, không tăng |
| "Không cần ai kiểm soát tôi" | Mất autonomy | Positioning PMO là support, không phải police |
| "Quy trình không phù hợp project của tôi" | One-size-fits-all | Cho phép tailoring trong boundary |
| "Lãnh đạo không ủng hộ thực sự" | C-level nói có nhưng không follow through | Secure visible sponsor support trước khi launch |

### Communication Plan cho PMO Launch

```
T-4 tuần: C-level announcement về PMO initiative
T-2 tuần: All-PM meeting: "PMO là gì, PMO không phải là gì"
T-1 tuần: 1-on-1 với resistant stakeholders
T=0: Soft launch với 2-3 pilot projects
T+1 tháng: First success story showcase
T+3 tháng: Full rollout
```

---

## Ví Dụ Thực Tế: Xây Dựng PMO cho Công Ty IT 200 Người tại VN

**Context:** Công ty phần mềm outsourcing, 200 nhân viên, 15-20 dự án cùng lúc, 8 PM với level khác nhau.

**Vấn đề:**
- 60% dự án trễ ít nhất 2 tuần
- Khách hàng complain về inconsistent reporting
- Junior PM không biết escalate khi nào và cóm cách nào
- Không có central view của resource utilization

**PMO Roadmap 6 Tháng:**

```
Tháng 1-2: Foundation
├── Hire/assign PMO Director (1 FTE)
├── Assessment: survey 8 PMs + review 10 projects
├── Define PMO type: Controlling PMO
└── Create PMO Charter, approved by CEO

Tháng 3-4: Standardization
├── Create template library (Charter, Risk, Status, Minutes)
├── Define project lifecycle (5 stages + gates)
├── Implement weekly status reporting cadence
└── Launch PM community of practice (monthly)

Tháng 5-6: Governance
├── Setup portfolio visibility dashboard (Google Sheets)
├── Implement project intake process
├── Monthly portfolio review với Directors
└── First quarterly review với CEO + Lessons Learned session
```

**Results sau 6 tháng:**
- On-time delivery tăng từ 40% lên 65%
- Khách hàng satisfaction score tăng 0.8 điểm
- Junior PM onboarding time giảm 50%
- Resource conflicts giảm 40% do visibility tốt hơn

---

## Common Pitfalls

1. **Quá bureaucratic ngay từ đầu** → Start simple, add complexity gradually
2. **Không có C-level champion** → PMO cần executive sponsorship rõ ràng
3. **PMO focus vào compliance thay vì value** → Measure outcomes, không chỉ process adherence
4. **Template quá phức tạp** → PM sẽ fill in bullshit để comply, không thực sự dùng
5. **Bỏ qua "WIIFM" (What's In It For Me?)** → Show PM cụ thể PMO giúp họ gì

---

## Câu Hỏi Reflection

1. Công ty bạn hiện tại có PMO không? Nếu có, thuộc loại nào? Hiệu quả không?
2. Nếu bạn được giao xây dựng PMO cho công ty IT 50 người, bạn bắt đầu từ đâu?
3. Làm thế nào để PMO avoid being perceived as "bureaucracy police"?
