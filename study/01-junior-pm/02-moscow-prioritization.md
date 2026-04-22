# Quản Lý Thời Gian & Ưu Tiên Công Việc

> Kỹ năng quan trọng nhất của PM không phải là lập kế hoạch hoàn hảo — mà là biết **bỏ gì** khi không thể làm tất cả.

---

## MoSCoW Prioritization

MoSCoW là framework phân loại requirements/tasks theo mức độ ưu tiên, giúp PM và team **đồng thuận về scope** trước khi bắt đầu sprint hoặc release.

Tên "MoSCoW" là acronym từ 4 categories:

### M — Must Have (Bắt buộc)

**Định nghĩa:** Không có tính năng/task này thì release là **failure** — không thể go-live, vi phạm contract, hoặc system không chạy được.

**Test câu hỏi:** "Nếu không có cái này, release có ý nghĩa gì không?" — Nếu không → Must have.

**Lưu ý quan trọng:** Must have thường chỉ nên chiếm **60–70% capacity** của sprint/release. Nếu Must have đã 100% capacity thì bạn đang set up team để fail.

**Ví dụ:**

- Hệ thống đăng nhập/xác thực người dùng
- Tính năng thanh toán core của e-commerce
- Migrate dữ liệu khách hàng trước khi cutover
- Security patch cho lỗ hổng critical

---

### S — Should Have (Nên có)

**Định nghĩa:** Quan trọng, có giá trị cao, **nhưng release vẫn có thể diễn ra** nếu không có. Thường là những tính năng mà users mong đợi nhưng có workaround tạm thời.

**Test câu hỏi:** "Nếu không có cái này, release có bị ảnh hưởng nghiêm trọng không?" — Nếu có workaround → Should have.

**Ví dụ:**

- Email notification khi đơn hàng được giao
- Export báo cáo ra Excel (có thể xem online trước)
- Performance optimization (hệ thống chạy chậm hơn mong đợi nhưng vẫn chạy)
- Search và filter nâng cao

---

### C — Could Have (Có thể có)

**Định nghĩa:** Nice-to-have, tăng trải nghiệm người dùng nhưng **không ảnh hưởng core value**. Làm nếu còn thời gian.

**Test câu hỏi:** "Có bao nhiêu users sẽ thực sự dùng cái này trong 30 ngày đầu?" — Nếu ít → Could have.

**Ví dụ:**

- Dark mode
- Keyboard shortcuts
- Tùy chỉnh màu sắc dashboard
- Tooltip hướng dẫn lần đầu dùng

---

### W — Won't Have (Loại bỏ lần này)

**Định nghĩa:** **Chính thức đưa ra khỏi scope** của release/sprint này. Không phải "sẽ không làm bao giờ" — mà là "không làm lần này, có thể xem xét sau."

**Tại sao cần W?** Vì stakeholders hay "thêm" requirements mà không "bỏ" — W buộc cả hai phía đồng ý về những gì không nằm trong scope.

**Ví dụ:**

- Mobile app (giai đoạn này chỉ làm web)
- Integration với SAP (sau khi ổn định hệ thống mới)
- Multi-language support (phase 2)
- AI-powered recommendations (future roadmap)

---

## Ví Dụ Thực Tế 1: Migration Project (Delphi → Modern Stack)

**Bối cảnh:** Công ty TNHH Logistics ABC đang migrate hệ thống quản lý kho từ Delphi lên web-based (React + .NET Core). Deadline: Q4, 4 tháng.

```
MUST HAVE (phải xong trước go-live Q4)
├── Migrate module nhập/xuất kho (core business)
├── Migrate module tồn kho real-time
├── User authentication & authorization
├── In phiếu nhập/xuất kho (nghiệp vụ hàng ngày)
└── Data migration từ Delphi database

SHOULD HAVE (quan trọng, có thể delay sang Q1)
├── Module báo cáo tổng hợp (workaround: export Excel thủ công)
├── Email notification khi tồn kho dưới threshold
└── Integration với phần mềm kế toán (hiện tại nhập tay OK)

COULD HAVE (làm nếu còn thời gian)
├── Dashboard analytics với chart đẹp
├── Mobile app cho warehouse staff
└── Barcode scanner integration

WON'T HAVE (chính thức ngoài scope Q4)
├── AI demand forecasting
├── IoT integration với RFID
└── Multi-warehouse management (công ty chỉ có 1 kho)
```

**Kết quả áp dụng:** Team tập trung 100% vào 5 Must-have items. Go-live Q4 đúng hạn. 2 Should-have items hoàn thành trong Q1.

---

## Ví Dụ Thực Tế 2: Sprint Planning Cho SaaS Product

**Bối cảnh:** SaaS B2B quản lý nhân sự — Sprint 7 (2 tuần), team 4 dev, velocity 40 story points.

```
Sprint Goal: "Hoàn thiện module chấm công để demo cho 3 enterprise clients"

MUST HAVE (chiếm 26 SP — 65% capacity)
├── [8 SP] Check-in/check-out theo ca làm việc
├── [5 SP] Tính giờ tăng ca tự động
├── [8 SP] Báo cáo chấm công theo tuần
└── [5 SP] Export báo cáo PDF

SHOULD HAVE (chiếm 10 SP — 25% capacity)
├── [5 SP] Approval workflow cho giờ tăng ca
└── [5 SP] Notification nhắc check-in khi quên

COULD HAVE (chiếm 4 SP — 10% — làm nếu ahead of schedule)
└── [4 SP] Biểu đồ attendance trend

WON'T HAVE (sprint này)
├── Mobile app check-in (face recognition)
└── Integration với payroll system
```

**Lesson:** Khi sprint đang track well vào ngày 8, team pull Could-have item vào và hoàn thành. Sprint velocity thực tế: 40/40 SP.

---

## Ví Dụ Thực Tế 3: App Mobile Launch

**Bối cảnh:** Startup fintech ra mắt app MVP trong 6 tuần với 2 iOS dev + 1 backend.

```
MUST HAVE
├── Đăng ký tài khoản (phone number + OTP)
├── Đăng nhập biometric (Face ID / fingerprint)
├── Xem số dư tài khoản
├── Chuyển tiền nội bộ (cùng app)
└── Lịch sử giao dịch 30 ngày

SHOULD HAVE
├── Thông báo push khi nhận tiền
├── Chuyển tiền ngân hàng khác (Napas)
└── Tìm kiếm trong lịch sử giao dịch

COULD HAVE
├── Categorize giao dịch tự động
└── Ảnh đại diện profile

WON'T HAVE (version 1.0)
├── Đầu tư / tiết kiệm
├── Vay vốn
├── QR Pay
└── Split bill tính năng
```

**Kết quả:** App launch sau 6 tuần với 5 Must-have. App store rating 4.2/5. Should-have hoàn thành trong v1.1 sau 3 tuần.

---

## Eisenhower Matrix (Urgent/Important)

Trong khi MoSCoW dùng cho **requirements/features**, Eisenhower Matrix dùng cho **tasks hàng ngày** của PM bản thân.

```
                    QUAN TRỌNG
                         │
         Q2              │         Q1
    [Lên lịch làm]       │     [Làm ngay]
    - Viết project       │     - Server down production
      charter            │     - Sponsor cần báo cáo
    - 1:1 với team       │       khẩn trước board meeting
    - Risk review        │     - Bug critical block UAT
                         │
KHÔNG ─────────────────────────────────────── KHẨN CẤP
KHẨN                     │
CẤP    Q4               │        Q3
    [Loại bỏ]           │    [Delegate/Tự động hóa]
    - Đọc email CC       │    - Báo cáo status routine
    - Meeting không      │    - Forward email tới người
      có agenda rõ       │      phụ trách
    - "Có thể bạn        │    - Update task tracking
      giúp mình..."      │      hàng ngày
                         │
                    KHÔNG QUAN TRỌNG
```

### So Sánh MoSCoW vs Eisenhower

| Tiêu chí            | MoSCoW                               | Eisenhower Matrix       |
| ------------------- | ------------------------------------ | ----------------------- |
| **Dùng cho**        | Requirements, features, deliverables | Tasks cá nhân hàng ngày |
| **Thời điểm dùng**  | Planning phase, sprint planning      | Daily/weekly planning   |
| **Participants**    | Cả team + stakeholders               | Cá nhân PM              |
| **Output**          | Scope agreement                      | Priority to-do list     |
| **Tần suất review** | Mỗi sprint/release                   | Hàng ngày/tuần          |

---

## Time Blocking Technique Cho PM

Time blocking là kỹ thuật **đặt trước thời gian** trong calendar cho các loại công việc khác nhau, tránh bị meetings và interruptions chiếm hết ngày.

### Mẫu Calendar 1 Tuần Cho Junior PM

```
          MON         TUE         WED         THU         FRI
08:00  [Review       [Deep       [Review     [Deep       [Weekly
08:30   emails &      Work:       emails &    Work:       Review &
09:00   plan day]     WBS/        plan day]   Docs]       Planning
09:30                 Planning]
10:00  [Team          ↓          [Team        ↓          [1:1 với
10:30   Standup]               Standup]               PM/Mentor]
11:00  [Admin:                  [Admin:
11:30   update                   stakeholder
12:00   tracker]                 emails]
12:00  ─────────── LUNCH ────────────────────────────────────────
13:00  [Project      [Meetings   [Project    [Meetings   [Retrospe-
13:30   meeting      slot: max   meetings    slot]        ctive/
14:00   / reviews]   2 meetings] / demos]               Lessons
14:30                                                    Learned]
15:00  [Buffer:      [Buffer]    [Buffer:    [Buffer]    [Buffer +
15:30   blockers,               risk log,               End-of-
16:00   follow-up]              docs]                    week
16:30                                                    report]
17:00  ──────────────────── END OF DAY ───────────────────────────
```

### Nguyên Tắc Time Blocking Cho PM

1. **Deep Work blocks**: 90–120 phút, tắt notification, không accept meetings. Dùng cho: viết project charter, tạo WBS, phân tích risks, chuẩn bị presentations.

2. **Meeting slots**: Gom meetings vào buổi chiều hoặc 1–2 ngày cố định. Tránh meetings buổi sáng sớm (cắt mất deep work time tốt nhất).

3. **Buffer time (20–30% ngày)**: Dành cho unexpected issues. PM không buffer đủ sẽ luôn chạy deadline.

4. **No-meeting Fridays** (hoặc Thứ 4): Ngày tập trung để hoàn thành công việc tồn đọng.

---

## Công Cụ Quản Lý Priority

### Jira — Cho Agile Teams

```
Cấu trúc Jira board cho Junior PM:

BACKLOG                 TODO              IN PROGRESS          DONE
─────────               ────              ───────────          ────
[MUST] Epic A           Task 1.1 →        Task 2.1 (Dev A) →   Task 3.1 ✓
[MUST] Epic B           Task 1.2 →        Task 2.2 (Dev B) →   Task 3.2 ✓
[SHOULD] Epic C         Task 1.3                               Task 3.3 ✓
[COULD] Epic D
[WON'T] Epic E
```

**Tips Jira cho Junior PM:**

- Dùng **Labels** để tag MoSCoW category: `must-have`, `should-have`, `could-have`
- Dùng **Fix Version** để group items theo release
- **Epic** = nhóm tính năng lớn; **Story** = yêu cầu người dùng; **Task** = công việc kỹ thuật
- **Story Points** không phải giờ — là relative effort (1, 2, 3, 5, 8, 13 theo Fibonacci)
- Tạo **Sprint Burndown Chart** để track tiến độ visual

### Trello — Cho Smaller Teams / Non-Engineering

```
Boards cơ bản:

[MUST HAVE]    [SHOULD HAVE]    [COULD HAVE]    [WON'T HAVE]
   Card 1          Card 3          Card 6          Card 9
   Card 2          Card 4          Card 7          Card 10
                   Card 5          Card 8
```

**Tips Trello:**

- Dùng **Color labels** cho MoSCoW (đỏ=Must, vàng=Should, xanh=Could, xám=Won't)
- **Checklist** trong card cho sub-tasks
- **Due dates** + Calendar Power-Up để xem deadline
- **Butler** (automation) để auto-move cards khi done

### Excel/Google Sheets — Khi Không Có Tools

Template đơn giản:

| ID      | Requirement | Category | Priority Score | Status       | Sprint   |
| ------- | ----------- | -------- | -------------- | ------------ | -------- |
| REQ-001 | User login  | Must     | 100            | Done         | Sprint 1 |
| REQ-002 | Export PDF  | Should   | 75             | In Progress  | Sprint 2 |
| REQ-003 | Dark mode   | Could    | 30             | Backlog      | TBD      |
| REQ-004 | AI features | Won't    | 0              | Out of scope | —        |

**Priority Score gợi ý:** Must=100, Should=75, Could=30, Won't=0

---

## Bài Tập: Áp Dụng MoSCoW Cho 1 Backlog Thực Tế

### Tình Huống

Bạn là Junior PM cho dự án **portal nội bộ HR** của một công ty 200 nhân viên. Deadline: 3 tháng. Team: 2 dev, 1 QA. Backlog hiện tại có 15 items sau — hãy phân loại MoSCoW:

```
Backlog items (chưa phân loại):
1. Nhân viên xem bảng lương của mình
2. HR upload file payslip hàng loạt
3. Nhân viên đăng ký nghỉ phép online
4. Manager approve/reject đơn nghỉ phép
5. Tự động tính số ngày phép còn lại
6. Báo cáo attendance tháng cho manager
7. Nhân viên xem sơ đồ tổ chức công ty
8. Chat nội bộ giữa nhân viên
9. Nhân viên cập nhật thông tin cá nhân
10. HR quản lý hợp đồng lao động (scan/upload)
11. Hệ thống đăng nhập SSO với Google Workspace
12. Push notification khi đơn được approve
13. Mobile app cho nhân viên
14. Báo cáo headcount theo phòng ban
15. Tích hợp với phần mềm kế toán (lương)
```

### Gợi Ý Phân Loại (Tham Khảo)

<details>
<summary>Xem đáp án gợi ý (thử tự làm trước!)</summary>

**MUST HAVE:**

- #11 SSO login (nền tảng cho mọi tính năng)
- #3 Đăng ký nghỉ phép (nghiệp vụ core nhất của HR portal)
- #4 Approve/reject nghỉ phép (phụ thuộc #3)
- #5 Tính ngày phép tự động (core functionality)
- #1 Xem bảng lương (lý do nhân viên dùng portal)

**SHOULD HAVE:**

- #2 Upload payslip hàng loạt (workflow cho HR)
- #6 Báo cáo attendance (cần nhưng export Excel tạm được)
- #9 Cập nhật thông tin cá nhân (self-service HR)
- #10 Quản lý hợp đồng (quan trọng nhưng workaround được)

**COULD HAVE:**

- #7 Sơ đồ tổ chức (nice to have)
- #12 Push notification (convenience)
- #14 Báo cáo headcount (managers tự extract được)

**WON'T HAVE:**

- #8 Chat nội bộ (đã có Slack/Teams)
- #13 Mobile app (phase 2 sau khi web ổn)
- #15 Tích hợp kế toán (phức tạp, scope riêng)

</details>

### Câu Hỏi Reflection Sau Bài Tập

1. Bạn có đồng ý với gợi ý phân loại không? Có items nào bạn phân loại khác không? Tại sao?
2. Nếu sponsor yêu cầu thêm #13 Mobile app vào Must have, bạn xử lý thế nào?
3. Làm thế nào để lấy sự đồng thuận từ cả HR department, IT department, và CEO về MoSCoW này?
4. Sau 6 tuần dev, 3 Must-have items hoàn thành nhưng #5 (tính ngày phép) phức tạp hơn dự kiến, cần thêm 2 tuần — bạn làm gì?
