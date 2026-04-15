# Work Breakdown Structure (WBS)

> "Nếu bạn không thể vẽ WBS cho dự án trong 30 phút, bạn chưa hiểu rõ dự án đó."

---

## WBS Là Gì?

WBS (Work Breakdown Structure) là công cụ phân rã dự án từ một deliverable lớn thành các công việc nhỏ hơn, có thể thực hiện được, có thể assign cho người cụ thể, và có thể đo lường tiến độ rõ ràng.

WBS KHÔNG phải:
- Timeline hay Gantt chart (WBS là WHAT, Gantt là WHEN)
- Process flow hay workflow (WBS là deliverable-oriented, không phải task-oriented)
- Danh sách to-do random

WBS LÀ:
- Sơ đồ phân cấp (hierarchy) của tất cả deliverables và work packages
- Nền tảng để estimate, schedule, và assign resource
- Single source of truth: nếu không có trong WBS, không có trong scope

**Lợi ích cụ thể:**

| Lợi ích | Giải thích thực tế |
|---|---|
| Không bỏ sót công việc | Phân rã đến work package level buộc bạn phải nghĩ đến mọi thứ cần làm |
| Estimate chính xác hơn | Estimate cho 1 task nhỏ 8 giờ dễ hơn estimate cho "toàn bộ module" |
| Phân công rõ ràng | Mỗi work package có đúng 1 người chịu trách nhiệm — không có "ai cũng chịu" |
| Theo dõi tiến độ dễ | % complete của project = (work packages done / total work packages) × 100 |
| Kiểm soát scope | Mọi yêu cầu mới đều phải hỏi: "Nó thuộc work package nào trong WBS?" |

---

## 100% Rule: Nguyên Tắc Cốt Lõi

**100% Rule:** WBS phải bao gồm 100% công việc của dự án — không thiếu, không thừa.

Cụ thể:
- Tổng công việc ở các level con = công việc của level cha
- Không có công việc nào được làm mà không xuất hiện trong WBS
- Không có công việc nào trong WBS mà không thuộc scope của dự án

**Kiểm tra 100% Rule:**

```
Sau khi tạo WBS, hỏi:
1. Có công việc nào team đang làm mà không có trong WBS không? → Thêm vào
2. Có work package nào trong WBS mà không ai làm không? → Xóa hoặc investigate tại sao
3. Tổng effort của tất cả work packages có hợp lý không so với tổng budget?
```

---

## 4 Bước Tạo WBS

### Bước 1: Bắt Đầu Với Deliverable Lớn Nhất (Level 0)

Level 0 là tên dự án. Đây là "100% of work".

```
Level 0: [Tên Dự Án]
```

Ví dụ: "WMS Migration Project", "E-Commerce Website v2", "CRM Implementation"

---

### Bước 2: Phân Nhỏ Thành Phases/Deliverables Lớn (Level 1)

Thường là 3–6 phases chính. Có hai cách phân chia phổ biến:

**Cách A: Theo Phase (phổ biến với Waterfall):**

```
1. Analysis Phase
2. Design Phase
3. Development Phase
4. Testing Phase
5. Deployment Phase
```

**Cách B: Theo Deliverable/Module (phổ biến với product development):**

```
1. User Authentication Module
2. Product Catalog Module
3. Cart & Checkout Module
4. Admin Dashboard
5. Infrastructure & DevOps
```

---

### Bước 3: Phân Nhỏ Tiếp Thành Work Packages (Level 2–3)

**8-Hour Rule:** Mỗi work package nên có effort ≤ 8 giờ công (1 ngày làm việc). Nếu lớn hơn, phân nhỏ tiếp. Nếu nhỏ hơn 2 giờ, có thể gộp với task liên quan.

Tại sao 8 giờ?
- Dễ estimate chính xác hơn
- Dễ track daily progress
- Phát hiện blockers sớm hơn (nếu 1 task đã kéo 2 ngày vẫn chưa xong là có vấn đề)

**Work Package cần có đủ thông tin:**
- Tên rõ ràng (động từ + danh từ)
- Deliverable cụ thể (sản phẩm đầu ra là gì)
- Người chịu trách nhiệm (1 người, không phải "team")
- Effort estimate (giờ hoặc ngày)
- Dependencies (phụ thuộc vào task nào)

---

### Bước 4: Assign Người Chịu Trách Nhiệm (RAA)

**RAA = Responsible + Accountable**

- **Responsible (R):** Người trực tiếp làm công việc
- **Accountable (A):** Người chịu trách nhiệm cuối cùng nếu work package thất bại (thường là PM hoặc team lead)

**Nguyên tắc:**
- Mỗi work package chỉ có **đúng 1 Accountable**
- Có thể có nhiều Responsible (nhiều người cùng làm)
- PM không Responsible cho mọi thứ — PM là Accountable

---

## Work Package vs Activity

Nhiều PM mới nhầm lẫn giữa hai khái niệm này:

| | Work Package | Activity |
|---|---|---|
| **Là gì** | Đơn vị công việc nhỏ nhất trong WBS, có deliverable rõ ràng | Bước cụ thể để hoàn thành work package |
| **Ví dụ** | "Implement login API" | "Viết unit test cho login API", "Code review", "Fix bug từ review" |
| **Tracking** | Track ở WBS level | Track ở task management tool (Jira) |
| **Duration** | ≤ 8 giờ (lý tưởng) | ≤ 2–4 giờ |
| **Output** | Deliverable cụ thể, có thể verify | Contribution đến deliverable |

**Khi nào xuống đến Activity level?**
- Trong Agile: Jira Sub-tasks
- Trong Waterfall: Activity List trong Project Schedule
- Không nhất thiết phải trong WBS — WBS dừng ở Work Package level là đủ

---

## WBS Numbering Convention

Dùng hệ thống số để track và reference dễ dàng:

```
1.0  Phase 1: Analysis
  1.1  Document current system
  1.2  Stakeholder interviews
    1.2.1  Interview warehouse manager (2h)
    1.2.2  Interview IT staff (2h)
    1.2.3  Consolidate findings (3h)
  1.3  Gap analysis report

2.0  Phase 2: Development
  2.1  Module A
    2.1.1  Frontend development (8h)
    2.1.2  Backend API (8h)
    2.1.3  Unit testing (4h)
  2.2  Module B
    ...
```

**Quy tắc:**
- Level 0: Project name (không đánh số)
- Level 1: 1.0, 2.0, 3.0... (Major phases)
- Level 2: 1.1, 1.2, 1.3... (Sub-deliverables)
- Level 3: 1.1.1, 1.1.2... (Work packages)
- Level 4: Hiếm khi cần, chỉ dùng cho dự án rất phức tạp

---

## Ví Dụ WBS Đầy Đủ 1: Migration Project (Delphi → Modern Stack)

```
WMS MIGRATION PROJECT (2025)
│
├── 1.0  Analysis Phase                          [2 tuần]
│   ├── 1.1  Document current system              [3 ngày]
│   │   ├── 1.1.1  Map all Delphi modules          [1 ngày]
│   │   ├── 1.1.2  Document database schema        [1 ngày]
│   │   └── 1.1.3  Document business rules         [1 ngày]
│   ├── 1.2  Identify dependencies                [2 ngày]
│   │   ├── 1.2.1  Internal system dependencies   [1 ngày]
│   │   └── 1.2.2  External integrations          [1 ngày]
│   └── 1.3  Gap analysis report                  [2 ngày]
│       ├── 1.3.1  Draft report                   [1 ngày]
│       └── 1.3.2  Stakeholder review & sign-off  [1 ngày]
│
├── 2.0  Design Phase                             [1 tuần]
│   ├── 2.1  System architecture design           [2 ngày]
│   ├── 2.2  Database schema design               [2 ngày]
│   └── 2.3  UI/UX wireframes                     [1 ngày]
│
├── 3.0  Development Phase                        [6 tuần]
│   ├── 3.1  Module Nhập Kho (Goods Receipt)      [10 ngày]
│   │   ├── 3.1.1  Backend API                    [4 ngày]
│   │   ├── 3.1.2  Frontend UI                    [4 ngày]
│   │   └── 3.1.3  Unit tests                     [2 ngày]
│   ├── 3.2  Module Xuất Kho (Goods Issue)         [8 ngày]
│   │   ├── 3.2.1  Backend API                    [3 ngày]
│   │   ├── 3.2.2  Frontend UI                    [3 ngày]
│   │   └── 3.2.3  Unit tests                     [2 ngày]
│   ├── 3.3  Module Tồn Kho (Inventory)            [6 ngày]
│   │   ├── 3.3.1  Real-time inventory tracking   [3 ngày]
│   │   └── 3.3.2  Location management            [3 ngày]
│   ├── 3.4  Module Báo Cáo                        [5 ngày]
│   │   ├── 3.4.1  Standard reports (5 loại)      [3 ngày]
│   │   └── 3.4.2  Export PDF/Excel               [2 ngày]
│   └── 3.5  Integration Testing                  [5 ngày]
│       ├── 3.5.1  Integration test cases         [2 ngày]
│       └── 3.5.2  Execute & fix bugs             [3 ngày]
│
├── 4.0  UAT Phase                                [2 tuần]
│   ├── 4.1  Test case preparation                [3 ngày]
│   ├── 4.2  User acceptance testing              [5 ngày]
│   │   ├── 4.2.1  Train test users               [1 ngày]
│   │   ├── 4.2.2  Execute test scenarios         [3 ngày]
│   │   └── 4.2.3  Document defects               [1 ngày]
│   └── 4.3  Bug fixing (UAT issues)              [3 ngày]
│
├── 5.0  Data Migration                           [1 tuần]
│   ├── 5.1  Data mapping document                [1 ngày]
│   ├── 5.2  Migration scripts development        [2 ngày]
│   ├── 5.3  Dry run (test environment)           [1 ngày]
│   └── 5.4  Reconciliation & validation          [1 ngày]
│
└── 6.0  Go-Live & Hypercare                      [5 tuần]
    ├── 6.1  Production deployment                [1 ngày]
    ├── 6.2  Go-live cutover                      [1 ngày]
    ├── 6.3  User training (2 sessions)           [2 ngày]
    ├── 6.4  Hypercare support                    [4 tuần]
    └── 6.5  Project closure report               [2 ngày]
```

**Tổng effort ước tính:** ~67 ngày làm việc
**Với team 3 developers + 1 BA + 1 PM:** ~3.5–4 tháng calendar time

---

## Ví Dụ WBS Đầy Đủ 2: Website E-Commerce

```
E-COMMERCE WEBSITE v2.0
│
├── 1.0  Project Management                       [xuyên suốt]
│   ├── 1.1  Project planning & WBS               [3 ngày]
│   ├── 1.2  Weekly status reports                [0.5 ngày/tuần]
│   └── 1.3  Project closure                      [2 ngày]
│
├── 2.0  Discovery & Design                       [3 tuần]
│   ├── 2.1  Requirements gathering               [1 tuần]
│   │   ├── 2.1.1  Stakeholder interviews         [3 ngày]
│   │   └── 2.1.2  Requirements document          [2 ngày]
│   ├── 2.2  UX Research & Personas               [3 ngày]
│   └── 2.3  UI Design                            [2 tuần]
│       ├── 2.3.1  Wireframes (all pages)         [5 ngày]
│       ├── 2.3.2  Visual design mockups          [5 ngày]
│       └── 2.3.3  Design review & approval       [1 ngày]
│
├── 3.0  Frontend Development                     [6 tuần]
│   ├── 3.1  Core pages                           [2 tuần]
│   │   ├── 3.1.1  Homepage                       [3 ngày]
│   │   ├── 3.1.2  Category & listing page        [3 ngày]
│   │   ├── 3.1.3  Product detail page            [2 ngày]
│   │   └── 3.1.4  Search & filter                [2 ngày]
│   ├── 3.2  Cart & Checkout flow                 [2 tuần]
│   │   ├── 3.2.1  Cart page                      [2 ngày]
│   │   ├── 3.2.2  Checkout step 1 (address)      [2 ngày]
│   │   ├── 3.2.3  Checkout step 2 (payment)      [3 ngày]
│   │   └── 3.2.4  Order confirmation page        [1 ngày]
│   ├── 3.3  User account pages                   [1 tuần]
│   │   ├── 3.3.1  Login / Register               [2 ngày]
│   │   ├── 3.3.2  Order history                  [2 ngày]
│   │   └── 3.3.3  Profile management             [1 ngày]
│   └── 3.4  Admin panel (frontend)               [1 tuần]
│       ├── 3.4.1  Product management UI          [2 ngày]
│       ├── 3.4.2  Order management UI            [2 ngày]
│       └── 3.4.3  Basic analytics dashboard      [1 ngày]
│
├── 4.0  Backend Development                      [6 tuần]
│   ├── 4.1  Authentication & User Management     [1 tuần]
│   ├── 4.2  Product Catalog API                  [1 tuần]
│   ├── 4.3  Cart & Order Management API          [1.5 tuần]
│   ├── 4.4  Payment Integration                  [1.5 tuần]
│   │   ├── 4.4.1  VNPay integration              [3 ngày]
│   │   ├── 4.4.2  Momo integration               [3 ngày]
│   │   └── 4.4.3  Payment webhook & reconcile    [2 ngày]
│   └── 4.5  Admin APIs & reporting               [1 tuần]
│
├── 5.0  Infrastructure & DevOps                  [2 tuần]
│   ├── 5.1  Cloud infrastructure setup           [3 ngày]
│   ├── 5.2  CI/CD pipeline                       [2 ngày]
│   ├── 5.3  CDN & performance optimization       [2 ngày]
│   └── 5.4  Security hardening & SSL             [2 ngày]
│
├── 6.0  Testing                                  [2 tuần]
│   ├── 6.1  Test plan & test cases               [3 ngày]
│   ├── 6.2  Functional testing                   [4 ngày]
│   ├── 6.3  Performance testing                  [2 ngày]
│   ├── 6.4  Security testing                     [2 ngày]
│   └── 6.5  UAT với khách hàng                   [3 ngày]
│
└── 7.0  Launch                                   [1 tuần]
    ├── 7.1  Production deployment                [1 ngày]
    ├── 7.2  DNS cutover & monitoring             [1 ngày]
    ├── 7.3  Smoke testing post-launch            [1 ngày]
    └── 7.4  Handover documentation               [2 ngày]
```

---

## WBS Dictionary Template

WBS Dictionary là tài liệu bổ sung chi tiết cho từng work package. Đặc biệt quan trọng khi có nhiều người làm việc cùng nhau.

```
WBS DICTIONARY — Work Package #3.1.1

ID:               3.1.1
Tên:              Backend API cho Module Nhập Kho
Phase:            Development
Parent WBS:       3.1 (Module Nhập Kho)

DELIVERABLE:
  API endpoints hoàn chỉnh cho quy trình nhập kho:
  - POST /api/goods-receipt (tạo phiếu nhập)
  - GET /api/goods-receipt/{id}
  - PUT /api/goods-receipt/{id}/confirm
  - Validation logic đầy đủ
  - Error handling chuẩn
  - Unit tests coverage ≥ 80%

OWNER:
  Responsible: Nguyễn Văn A (Senior Backend Dev)
  Accountable: Trần Minh Khoa (PM)

EFFORT:
  Estimate: 32 giờ (4 ngày làm việc)
  Start: 15/10/2025
  End: 20/10/2025 (trừ weekend)

DEPENDENCIES:
  Phải hoàn thành trước:
    - 1.3 Gap analysis report (để hiểu business rules)
    - 2.2 Database schema design (để biết cấu trúc DB)
  Được block bởi: Database schema approved

ACCEPTANCE CRITERIA:
  [ ] Tất cả endpoints documented trong Postman collection
  [ ] Unit test coverage ≥ 80% (verify bằng coverage report)
  [ ] Performance: response time < 500ms với 50 concurrent users
  [ ] Code review passed (ít nhất 1 senior review)
  [ ] Integrated với module xác thực đã có

RISKS:
  - Business rule cho partial receipt phức tạp hơn dự kiến → buffer thêm 1 ngày
```

---

## Critical Path Method (CPM) Cơ Bản Từ WBS

Sau khi có WBS với effort estimate và dependencies, bạn có thể xác định Critical Path.

**Critical Path là gì:** Chuỗi các tasks dài nhất từ đầu đến cuối dự án. Bất kỳ task nào trên Critical Path bị trễ đều làm trễ toàn bộ dự án.

**Ví dụ đơn giản:**

```
Dự án: 3 modules (A, B, C) cần làm tuần tự vì phụ thuộc nhau.

Task        Duration    Dependencies
──────────────────────────────────
1.1 Design     5 ngày       —
2.1 Module A   8 ngày       1.1 done
2.2 Module B   6 ngày       2.1 done
2.3 Module C   4 ngày       2.2 done
3.1 UAT        5 ngày       2.3 done
4.1 Deploy     2 ngày       3.1 done

Critical Path: 1.1 → 2.1 → 2.2 → 2.3 → 3.1 → 4.1
Total duration: 5 + 8 + 6 + 4 + 5 + 2 = 30 ngày

Nếu Module A bị trễ 2 ngày → toàn bộ project trễ 2 ngày
Nếu task song song (không trên critical path) trễ → không ảnh hưởng project end date
```

**Cách xác định Critical Path:**

1. Vẽ network diagram từ WBS (mỗi task = một node, arrows = dependencies)
2. Forward pass: tính Early Start (ES) và Early Finish (EF) từ trái sang phải
3. Backward pass: tính Late Start (LS) và Late Finish (LF) từ phải sang trái
4. Float = LS − ES (hoặc LF − EF). Task có Float = 0 → trên Critical Path

---

## Gantt Chart Từ WBS

Sau khi có WBS + durations + dependencies, chuyển sang Gantt:

```
WBS ID  Task                      Tuần 1  Tuần 2  Tuần 3  Tuần 4  Tuần 5
──────────────────────────────────────────────────────────────────────────
1.0     Analysis Phase            ████
  1.1   Document current system   ███
  1.2   Identify dependencies         ██
  1.3   Gap analysis report               █
2.0     Development Phase                   ████████████████
  2.1   Module A migration                  ██████████
  2.2   Module B migration                            ████████
  2.3   Integration testing                                    █████
3.0     UAT Phase                                                    █████
```

**Tools để tạo Gantt từ WBS:**

| Tool | Phù hợp cho | Ưu điểm | Nhược điểm |
|---|---|---|---|
| MS Project | Dự án phức tạp, nhiều dependencies | Đầy đủ tính năng, CPM tự động | Phức tạp, tốn tiền |
| Excel / Google Sheets | Dự án nhỏ, team nhỏ | Miễn phí, flexible | Phải làm tay |
| Jira (Epic/Story) | Agile projects | Tích hợp với backlog | Gantt view cần plugin |
| Notion | Documentation-first teams | Flexible, đẹp | Gantt view hạn chế |
| draw.io | Vẽ WBS diagram | Miễn phí, nhiều template | Chỉ diagram, không schedule |

---

## Tools Để Tạo WBS

**MS Project:** Standard cho large-scale projects. Tích hợp CPM, resource leveling, Gantt tự động. Overkill cho projects nhỏ.

**Jira Epic → Story → Sub-task:** Tương đương WBS trong Agile. Epic = Phase (Level 1), Story = Work Package (Level 2-3), Sub-task = Activity.

**draw.io (diagrams.net):** Miễn phí, online, có WBS templates. Tốt để present WBS cho stakeholder.

**WBS Chart Pro:** Plugin cho MS Project, tạo visual WBS chart đẹp để present.

**Miro / FigJam:** Tốt cho workshop collaborative khi cả team cùng build WBS.

---

## Common Mistakes

### Mistake 1: WBS Quá Chi Tiết

Phân rã đến từng dòng code hay từng bug fix. WBS không phải tech spec.

**Dấu hiệu:** Work packages dưới 1 giờ, WBS có hàng trăm items.

**Fix:** Dừng ở level "8-hour rule". Tasks nhỏ hơn → quản lý trong Jira/task tool.

### Mistake 2: WBS Quá Vĩ Mô

Chỉ có 3–4 items ở Level 1, không phân nhỏ tiếp.

**Dấu hiệu:** "2.0 Development (3 tháng)" — không có sub-items.

**Fix:** Phân rã đến khi estimate mỗi work package dưới 8 giờ là đáng tin.

### Mistake 3: Bỏ Sót Dependencies

Không nghĩ đến việc task A phải xong trước task B mới làm được.

**Hậu quả:** Developer làm xong task nhưng không deploy được vì infra chưa sẵn sàng.

**Fix:** Với mỗi work package, hỏi: "Cần gì xong trước thứ này mới làm được?"

### Mistake 4: Không Assign Owner

Nhiều work package không có người chịu trách nhiệm rõ ràng.

**Hậu quả:** "Tưởng là anh kia làm..." — task bị bỏ sót đến tuần cuối.

**Fix:** Mỗi work package phải có tên cụ thể — không được viết "team" hay "TBD".

### Mistake 5: WBS Không Được Update

WBS tạo ra một lần rồi quên. Scope thay đổi nhưng WBS vẫn là version cũ.

**Fix:** WBS là living document. Mỗi approved change request → update WBS ngay.

---

## Bài Tập: Tạo WBS Cho Dự Án Bạn Đang Tham Gia

Dùng template dưới đây để tạo WBS cho bất kỳ dự án nào bạn đang làm (dù là developer, không phải PM):

```
Bước 1: Đặt tên dự án (Level 0)
[Tên dự án của bạn]

Bước 2: Xác định 3–5 phases chính (Level 1)
1.0 [Phase 1 — ví dụ: Discovery]
2.0 [Phase 2 — ví dụ: Development]
3.0 [Phase 3 — ví dụ: Testing]
4.0 [Phase 4 — ví dụ: Launch]

Bước 3: Với mỗi phase, liệt kê deliverables (Level 2)
1.1 [Deliverable A]
1.2 [Deliverable B]
...

Bước 4: Phân nhỏ thành work packages (Level 3), mỗi cái ≤ 8 giờ
1.1.1 [Work package] — [X giờ] — Owner: [Tên]
1.1.2 [Work package] — [X giờ] — Owner: [Tên]
...

Bước 5: Kiểm tra 100% Rule
[ ] Tổng effort của tất cả work packages có hợp lý?
[ ] Có công việc nào team đang làm mà không có trong WBS?
[ ] Mỗi work package đã có owner?
[ ] Dependencies đã được identify?
```

**Sau khi tạo xong, estimate tổng effort và so sánh với actual duration của dự án. Sự chênh lệch cho bạn biết nhiều về estimation skills của mình.**

---

*Tiếp theo: [05-stakeholder-management.md](./05-stakeholder-management.md) — Quản lý các bên liên quan*
