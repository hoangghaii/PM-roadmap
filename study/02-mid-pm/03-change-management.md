# Quản Lý Change Request

> **Giai đoạn:** PM Chính Thức (2–5 năm)
> **Độ quan trọng:** ⭐⭐⭐ Bắt buộc
> **Thời gian học:** 1 tuần lý thuyết + 2 tuần thực hành trên dự án thực

---

## Scope Creep — Kẻ Thù Số 1 Của PM

Scope creep là hiện tượng phạm vi dự án dần dần mở rộng mà không có sự kiểm soát chính thức, thường xảy ra vì "chỉ thêm một tính năng nhỏ thôi".

### Scope Creep Là Gì?

Scope creep không phải lúc nào cũng bắt đầu từ một yêu cầu lớn. Nó thường đến từ những thay đổi nhỏ, tưởng vô hại:

- "Anh ơi, thêm cho em cái nút export PDF nhé, 1 ngày thôi mà"
- "Hệ thống báo cáo mình đang làm, tiện thể add thêm dashboard real-time đi"
- "Khách hàng nói họ muốn tích hợp thêm với Zalo nữa, trong scope đó chứ?"

Mỗi yêu cầu đơn lẻ có vẻ nhỏ, nhưng cộng lại sau 3 tháng, dự án đã phình to 40% mà không có thêm một đồng ngân sách hay một ngày timeline nào.

### Tại Sao Nguy Hiểm?

```
Scope tăng 20% → Dev overload → Quality giảm → Bug tăng → Test kéo dài
     ↓
Timeline trễ → Khách hàng bất mãn → Mối quan hệ xấu đi
     ↓
Budget vượt → PM giải trình với sponsor → Uy tín bị ảnh hưởng
     ↓
Team burnout → Turnover → Dự án tương lai bị ảnh hưởng
```

### Ví Dụ Thực Tế Tại Việt Nam

**Dự án:** Phát triển hệ thống quản lý nhân sự (HRM) cho công ty sản xuất 500 nhân viên.

**Scope ban đầu (ký hợp đồng):** Quản lý hồ sơ nhân viên, chấm công, tính lương cơ bản. Budget: 800 triệu VND, timeline: 6 tháng.

**Sau 2 tháng:**
- Khách hàng yêu cầu thêm module đánh giá KPI — "Cái này nằm trong 'quản lý nhân sự' mà anh"
- Thêm tích hợp với hệ thống bảo hiểm xã hội
- Thêm báo cáo thuế tự động
- Thêm mobile app cho nhân viên check-in

**Kết quả:** Dự án kéo dài 10 tháng, budget vượt 60%, team dev làm overtime 3 tháng liên tiếp, 2 senior dev nghỉ việc.

**Nguyên nhân gốc rễ:** PM không có quy trình Change Control, không ai kiểm soát scope.

---

## Baseline và Change Control

### Project Baseline Là Gì?

Baseline là **trạng thái đã được phê duyệt** của dự án tại một thời điểm cụ thể — cái "gốc" để đo lường mọi thứ.

```
┌─────────────────────────────────────────────────────────────┐
│                    3 LOẠI BASELINE                          │
├─────────────────┬───────────────────────────────────────────┤
│ Scope Baseline  │ Scope Statement + WBS + WBS Dictionary    │
│ Schedule Baseline│ Project Schedule đã được phê duyệt       │
│ Cost Baseline   │ Budget đã được phê duyệt (Cost Performance│
│                 │ Baseline)                                  │
└─────────────────┴───────────────────────────────────────────┘
```

Khi có thay đổi, bạn **không tự ý sửa baseline**. Bạn phải đi qua quy trình Change Control, được phê duyệt, rồi mới cập nhật baseline mới (version mới).

### Tại Sao Cần Change Control?

| Không có Change Control | Có Change Control |
|---|---|
| Ai cũng có thể yêu cầu thay đổi bất kỳ lúc nào | Mọi thay đổi đều được kiểm soát |
| PM không biết tổng impact | PM biết chính xác impact trước khi quyết định |
| Khó giải trình khi dự án trễ/vượt budget | Có audit trail đầy đủ |
| Team bị overload vì yêu cầu bất ngờ | Team được bảo vệ khỏi yêu cầu không hợp lý |
| Dễ tranh chấp với khách hàng | Rõ ràng ai yêu cầu, ai phê duyệt |

---

## Quy Trình Change Request (Flowchart)

```
Stakeholder yêu cầu thay đổi
           ↓
PM ghi nhận vào Change Log (ngay lập tức, không được quên)
           ↓
PM phân tích: Có thực sự ngoài scope không?
    ↓ Ngoài scope          ↓ Trong scope (bị hiểu nhầm)
    Tiếp tục CR            Giải thích và close CR
           ↓
Impact Analysis: Time? Cost? Scope? Quality? Risk?
(Làm việc với BA, Tech Lead, Architect để estimate)
           ↓
Chuẩn bị options cho sponsor (thường 2-3 options)
Option A: Approve → +X tuần, +Y triệu
Option B: Defer sang phase 2
Option C: Replace feature Z bằng feature này
           ↓
Trình bày cho Sponsor / Steering Committee
           ↓
          /   \
    Approve   Reject   Defer
       ↓         ↓       ↓
  Update     Document  Ghi vào
  Project    lý do +   backlog /
  Plan +     Notify    phase 2
  Communicate stakeholder  planning
  to team
```

**Lưu ý quan trọng:**
- Không bao giờ bắt đầu implement trước khi có approval bằng văn bản
- CR approval phải từ đúng người có authority (không phải middle manager nói OK là xong)
- Thời gian phân tích CR thường mất 2–5 ngày làm việc, đừng để bị áp lực "làm ngay đi"

---

## Change Request Form Template

```
═══════════════════════════════════════════════════════════════
CR-[XXX]: [Tên thay đổi]
═══════════════════════════════════════════════════════════════
Ngày yêu cầu: ____________  |  Ngày cần quyết định: __________
Người yêu cầu: __________   |  Project: ____________________
Priority: ☐ High  ☐ Medium  ☐ Low
Phase hiện tại: _____________

───────────────────────────────────────────────────────────────
MÔ TẢ THAY ĐỔI
───────────────────────────────────────────────────────────────
Hiện trạng (As-Is):
[Mô tả trạng thái hiện tại của feature/process]

Yêu cầu thay đổi (To-Be):
[Mô tả chi tiết thay đổi mong muốn]

Lý do / Business Justification:
[Tại sao cần thay đổi này? Business value là gì?]

───────────────────────────────────────────────────────────────
IMPACT ANALYSIS (do PM + Tech Lead thực hiện)
───────────────────────────────────────────────────────────────
Scope:    ☐ Tăng  ☐ Giảm  ☐ Không đổi
Chi tiết: [Mô tả cụ thể công việc thêm/bớt]

Timeline: ☐ Tăng +[X] ngày  ☐ Giảm -[X] ngày  ☐ Không đổi
Lý do: [Explain tại sao timeline bị ảnh hưởng]
New delivery date (nếu approve): __________

Budget:   ☐ Tăng +[X] triệu VND  ☐ Giảm  ☐ Không đổi
Chi tiết: [Breakdown: nhân công, license, infrastructure...]

Quality:  ☐ Tăng  ☐ Giảm  ☐ Không đổi
Ghi chú: [Ảnh hưởng đến chất lượng như thế nào]

Dependencies mới: [Có tạo ra dependency mới không?]

Risk mới: [Mô tả risk phát sinh nếu approve CR này]

───────────────────────────────────────────────────────────────
KHUYẾN NGHỊ CỦA PM
───────────────────────────────────────────────────────────────
☐ Approve — Lý do: [PM recommend approve vì...]
☐ Reject  — Lý do: [PM recommend reject vì...]
☐ Defer   — Đến phase/sprint: [...]

Options cho Sponsor:
  Option A: [Mô tả + impact]
  Option B: [Mô tả + impact]
  Option C: [Mô tả + impact]

───────────────────────────────────────────────────────────────
QUYẾT ĐỊNH CỦA SPONSOR / CAB
───────────────────────────────────────────────────────────────
☐ Approved
☐ Rejected — Lý do: ________________________________________
☐ Deferred đến: ____________________________________________

Điều kiện kèm theo (nếu có): _______________________________

Ký tên: __________________________ Ngày: __________________
Chức vụ: _________________________________________________
═══════════════════════════════════════════════════════════════
```

---

## Change Log Template

Change Log là sổ theo dõi tất cả Change Requests. PM phải cập nhật sau mỗi CR.

```
┌──────┬──────────────────────┬────────┬──────────┬────────┬──────────┬──────────┬────────┐
│ CR # │ Tên thay đổi         │ Ngày   │ Người YC │Priority│ Status   │ Impact   │ Ghi chú│
├──────┼──────────────────────┼────────┼──────────┼────────┼──────────┼──────────┼────────┤
│CR-001│ Thêm export PDF      │ 15/1   │ Anh Tuấn │ Med    │ Approved │+3d, +15M │Update  │
│      │                      │        │ (Client) │        │ 20/1     │          │baseline│
├──────┼──────────────────────┼────────┼──────────┼────────┼──────────┼──────────┼────────┤
│CR-002│ Tích hợp Zalo OA     │ 25/1   │ PM team  │ Low    │ Deferred │+10d,+40M │Phase 2 │
│      │                      │        │          │        │ 28/1     │          │backlog │
├──────┼──────────────────────┼────────┼──────────┼────────┼──────────┼──────────┼────────┤
│CR-003│ Thay đổi dashboard   │ 1/2    │ Chị Hoa  │ High   │ Rejected │N/A       │Không   │
│      │ layout               │        │ (CFO)    │        │ 3/2      │          │trong   │
│      │                      │        │          │        │          │          │budget  │
├──────┼──────────────────────┼────────┼──────────┼────────┼──────────┼──────────┼────────┤
│CR-004│ Multi-currency       │ 10/2   │ Anh Khoa │ High   │ Pending  │TBD       │Đang    │
│      │ support              │        │ (CEO)    │        │          │          │phân    │
│      │                      │        │          │        │          │          │tích    │
└──────┴──────────────────────┴────────┴──────────┴────────┴──────────┴──────────┴────────┘

TỔNG KẾT (cập nhật mỗi tuần):
Approved CRs: 1 | Tổng impact thêm: +3 ngày, +15 triệu VND
Rejected CRs: 1 | Pending: 1 | Deferred: 1
```

---

## Change Advisory Board (CAB)

### CAB Là Gì?

CAB (Change Advisory Board) là hội đồng xem xét và phê duyệt change requests. Thường dùng trong IT Service Management (ITIL) nhưng ngày càng phổ biến trong project management.

### Khi Nào Cần CAB?

Không phải dự án nào cũng cần CAB chính thức. Cần CAB khi:
- Dự án có nhiều stakeholder với authority ngang nhau (không ai chịu ra quyết định một mình)
- Thay đổi có impact lớn đến nhiều bộ phận
- Dự án critical — downtime hay lỗi sẽ gây hậu quả nghiêm trọng
- Tổ chức có nhiều dự án đang chạy song song, một CR có thể ảnh hưởng nhiều dự án

### Thành Viên CAB Điển Hình

```
┌─────────────────────────────────────────────────────────────┐
│                   CHANGE ADVISORY BOARD                     │
├─────────────────────────────────────────────────────────────┤
│ Project Sponsor          → Quyết định final (vote nặng)    │
│ PM (Chair)               → Trình bày CR, điều phối meeting │
│ Tech Lead / Architect    → Đánh giá technical feasibility  │
│ Business Analyst         → Đánh giá business impact        │
│ Representative from Ops  → Đánh giá operational impact     │
│ Key Stakeholder (client) → Xác nhận business need         │
└─────────────────────────────────────────────────────────────┘
```

### Tần Suất Họp

| Loại CR | Xử lý như thế nào |
|---|---|
| Emergency (Critical bug, security) | CAB emergency meeting trong 24h |
| High priority | CAB weekly meeting, hoặc email vote trong 48h |
| Medium/Low priority | CAB meeting 2 tuần/lần định kỳ |
| Minor (typo, UI tweak) | PM tự quyết, không cần CAB |

---

## Cách Nói "Không" Chuyên Nghiệp Với Khách Hàng

PM không có nhiệm vụ làm hài lòng khách hàng **bằng mọi giá** — PM có nhiệm vụ deliver **đúng cam kết**. Nói "không" đúng cách là kỹ năng quan trọng nhất.

### Script Mẫu Theo Tình Huống

**Tình huống 1: Yêu cầu thêm tính năng ngoài scope**

> "Chúng tôi hoàn toàn hiểu tại sao tính năng [X] này quan trọng với business của anh/chị — thực ra đây là một ý tưởng rất hay. Tuy nhiên, tính năng này không nằm trong scope đã ký kết trong hợp đồng, cụ thể là [trích dẫn điều khoản]. Để thêm tính năng này, chúng tôi sẽ cần [+X tuần] và [+Y triệu VND]. Có hai hướng để chúng ta xem xét: một là approve CR này với budget và timeline tương ứng, hai là đưa vào kế hoạch phase 2. Anh/chị muốn chúng tôi chuẩn bị CR chi tiết để trình bày không?"

**Tình huống 2: Yêu cầu thay đổi khi dự án gần hoàn thành**

> "Chúng tôi có thể làm việc đó, nhưng sẽ ảnh hưởng đáng kể đến delivery date. Hiện tại team đang ở giai đoạn UAT, nếu thay đổi thiết kế database ở thời điểm này, chúng tôi cần quay lại dev ít nhất 2 tuần, reset testing từ đầu thêm 1 tuần. Tổng cộng delay 3 tuần so với ngày go-live đã cam kết. Tôi muốn chắc chắn anh/chị hiểu trade-off này trước khi quyết định."

**Tình huống 3: Yêu cầu "nhỏ" liên tục được gửi đến**

> "Nếu chúng ta thêm X, chúng ta sẽ cần bỏ Y hoặc kéo dài thêm Z tuần. Đây là lần thứ tư trong tháng này team nhận được yêu cầu thay đổi ngoài scope — tôi muốn đề xuất chúng ta có một buổi họp Scope Review với đầy đủ stakeholder để ưu tiên những gì thực sự quan trọng nhất. Điều này sẽ giúp cả hai bên tránh bị trễ hạn."

**Tình huống 4: Áp lực từ C-level của khách hàng**

> "Tôi hiểu áp lực từ phía CEO của anh/chị. Để đưa ra quyết định chính xác nhất, tôi cần 2 ngày làm việc để phân tích impact đầy đủ. Tôi sẽ chuẩn bị 3 options rõ ràng với trade-off cụ thể để anh/chị quyết định. Đồng thời tôi cũng cần [tên Sponsor] của phía chúng tôi xác nhận. Có thể chúng ta schedule một cuộc họp 3 bên vào thứ Sáu này không?"

---

## 3 Ví Dụ Change Request Thực Tế

### Ví Dụ 1: CR-001 — Thêm Tính Năng Gửi Email Tự Động

**Bối cảnh:** Dự án xây dựng hệ thống quản lý đặt hàng B2B. Tuần 8/16, khách hàng yêu cầu thêm email notification khi đơn hàng thay đổi trạng thái.

**Impact Analysis:**
- Scope: Cần thêm email template, SMTP integration, trigger logic (3 developer-days)
- Timeline: +3 ngày làm việc
- Budget: +12 triệu VND (nhân công + email service)
- Risk: Nếu email config sai có thể spam khách hàng của khách hàng

**Recommendation:** Approve — vì business value cao (giảm cuộc gọi manual), cost thấp, timeline tác động không đáng kể.

**Kết quả:** Approved. Baseline được cập nhật. Team thêm story vào sprint tiếp theo.

---

### Ví Dụ 2: CR-002 — Thay Đổi Database Architecture

**Bối cảnh:** Dự án migration hệ thống legacy sang microservices. Ở tuần 10/20, architect mới được hire phát hiện database design hiện tại không scale tốt và đề xuất chuyển từ relational sang document-based.

**Impact Analysis:**
- Scope: Thay đổi toàn bộ data model, rewrite data access layer, migration script
- Timeline: +6 tuần
- Budget: +200 triệu VND
- Risk: Rất cao — đây là thay đổi architectural, có thể trigger cascade changes khắp hệ thống
- Quality: Potentially tốt hơn long-term nhưng risky short-term

**Recommendation:** Defer — technical debt có thể address sau khi go-live lần đầu. Kiến trúc hiện tại đủ tốt cho 2 năm tới. Đưa vào roadmap phase 2.

**Kết quả:** Sponsor đồng ý defer. Document lý do và technical debt acceptance vào Risk Register.

---

### Ví Dụ 3: CR-003 — Giảm Scope (Positive CR)

**Bối cảnh:** Dự án CRM đang bị áp lực timeline. PM phát hiện module "Advanced Forecasting" trong scope ban đầu rất phức tạp nhưng khách hàng thực ra chỉ cần basic forecasting.

**Impact Analysis:**
- Scope: Giảm — loại bỏ ML-based forecasting, chỉ làm rule-based
- Timeline: -2 tuần (buffer thêm cho testing)
- Budget: -80 triệu VND
- Quality: Tính năng đơn giản hơn nhưng reliable hơn

**Recommendation:** Approve — khách hàng vẫn nhận được business value cần thiết, giảm risk, tạo buffer timeline.

**Kết quả:** Approved sau khi confirm với end users rằng basic forecasting đủ dùng. Tiết kiệm được 2 tuần và 80 triệu.

---

## Configuration Management Cơ Bản

### Document Versioning

Tất cả tài liệu quan trọng của dự án phải có version control:

```
Document Naming Convention:
[ProjectCode]-[DocumentType]-v[Major].[Minor]-[YYMMDD]

Ví dụ:
CRM2026-ScopeStatement-v1.0-260115 (baseline gốc)
CRM2026-ScopeStatement-v1.1-260210 (sau CR-001)
CRM2026-ScopeStatement-v2.0-260315 (sau major scope change)
```

**Version Numbering Rules:**
- v1.0 → v1.1: Minor change, không ảnh hưởng baseline
- v1.x → v2.0: Major change, baseline được cập nhật sau approved CR
- Draft: v0.x cho đến khi được phê duyệt lần đầu

**Configuration Management Repository:**
Lưu tất cả document trong shared folder có cấu trúc rõ ràng:

```
/ProjectName/
  /01-Charter-and-Scope/
  /02-Plans/
  /03-Change-Requests/
    /Approved/
    /Rejected/
    /Pending/
  /04-Status-Reports/
  /05-Meeting-Minutes/
  /06-Closure/
```

---

## Lessons Learned: Viết Scope Document Chuẩn

### Cách Viết Scope Document Để Phòng Ngừa Tranh Chấp

Phần lớn scope dispute đến từ scope document viết mơ hồ. Dưới đây là các nguyên tắc để tránh:

**1. Dùng ngôn ngữ cụ thể, đo được**

| Mơ hồ (dễ tranh chấp) | Rõ ràng (phòng ngừa dispute) |
|---|---|
| "Hệ thống phải nhanh" | "Response time < 2 giây với 100 concurrent users" |
| "Báo cáo đầy đủ" | "7 loại báo cáo: [liệt kê từng cái + format]" |
| "Tích hợp với hệ thống hiện có" | "Tích hợp với SAP ERP (version 6.0) qua REST API" |
| "User-friendly interface" | "Giao diện theo mockup đính kèm (Appendix A)" |

**2. Luôn có phần "Exclusions" (Những gì KHÔNG nằm trong scope)**

```
NGOÀI PHẠM VI DỰ ÁN (EXCLUSIONS):
- Không bao gồm mobile application (iOS/Android)
- Không bao gồm tích hợp với hệ thống kế toán của bên thứ ba
- Không bao gồm migration dữ liệu lịch sử quá 3 năm
- Không bao gồm training cho nhân viên văn phòng tại tỉnh
- Không bao gồm hosting và infrastructure cost (do khách hàng tự lo)
```

**3. Đính kèm wireframe/mockup**

Một bức ảnh đáng giá ngàn lời nói. Mọi UI requirement phải có mockup đính kèm. "Dashboard hiển thị doanh thu" có thể được interpret 10 cách khác nhau — mockup chỉ có 1 cách.

**4. Acceptance Criteria rõ ràng**

```
Tính năng: Đăng nhập hệ thống

ACCEPTANCE CRITERIA:
☐ AC-1: User nhập đúng email + password → đăng nhập thành công trong < 3 giây
☐ AC-2: User nhập sai password 3 lần → tài khoản bị khóa 15 phút
☐ AC-3: User nhập sai password → hiện thông báo lỗi bằng tiếng Việt
☐ AC-4: Hỗ trợ SSO với Google Workspace (domain công ty)
☐ AC-5: Session timeout sau 8 giờ không hoạt động
☐ AC-6: Không hỗ trợ đăng nhập bằng Facebook/Zalo (ngoài scope)
```

**5. Sign-off Requirement**

Scope document phải được ký bởi **đúng người có thẩm quyền** — không phải PM phía khách hàng, không phải supervisor cấp trung — mà là người có quyền ký hợp đồng.

---

## Acceptance Criteria: Tránh "Interpretation Disputes"

### Bad Acceptance Criteria (dễ tranh chấp)

```
✗ "Hệ thống phải hoạt động tốt"
✗ "Giao diện phải đẹp và hiện đại"
✗ "Tất cả dữ liệu phải được lưu đúng"
✗ "Performance phải ổn"
```

### Good Acceptance Criteria (cụ thể, không tranh chấp được)

```
✓ "Hệ thống xử lý tối thiểu 500 transactions/giây không có error"
✓ "Giao diện tuân theo mockup Figma version 2.3 (link: ...)"
✓ "100% dữ liệu được validate theo business rules tại Appendix B"
✓ "Page load time < 3 giây trên mạng 4G (đo bằng Chrome DevTools)"
```

### Template Acceptance Criteria (INVEST Format)

Dùng cấu trúc Given-When-Then để viết AC không tranh chấp:

```
Given [điều kiện đầu vào]
When  [hành động của user/system]
Then  [kết quả mong đợi, đo được]

Ví dụ:
Given user đã đăng nhập và có quyền Accountant
When user click "Export Báo Cáo Doanh Thu" chọn tháng 1/2026
Then hệ thống tạo file Excel với:
  - Tên file: "BC_DoanhThu_012026.xlsx"
  - Dữ liệu từ 01/01/2026 đến 31/01/2026
  - Các cột: Ngày, Mã đơn, Khách hàng, Số tiền, Thuế, Tổng
  - Format tiền tệ: VND, dấu phẩy phân cách nghìn
  - Thời gian tạo: < 5 giây nếu dữ liệu < 10,000 dòng
```

---

## Tóm Tắt: Change Management Checklist Cho PM

```
TRƯỚC DỰ ÁN:
☐ Scope document chi tiết, có Exclusions rõ ràng
☐ Acceptance Criteria cụ thể cho mọi deliverable
☐ Wireframe/mockup đính kèm
☐ Change Control Process đã được agree với khách hàng
☐ CR Form template sẵn sàng
☐ Change Log setup (Excel hoặc Jira)

TRONG DỰ ÁN:
☐ Mọi yêu cầu thay đổi đều vào Change Log ngay lập tức
☐ Không implement CR trước khi có approval
☐ Impact Analysis trước mọi quyết định
☐ Update baseline sau mỗi approved CR
☐ Communicate change đến team + stakeholders liên quan
☐ Weekly Change Log review với sponsor

KHI KẾT THÚC DỰ ÁN:
☐ Final Change Log tổng kết
☐ Document lessons learned về scope management
☐ Input cho scope document template tốt hơn cho dự án sau
```

---

*Tiếp theo: [Case Study 2 — Khách Hàng Khó Tính](./case-studies/02-khach-hang-kho-tinh.md)*

*Xem lại: [02-earned-value-management.md](./02-earned-value-management.md)*
