# Các Phương Pháp Quản Lý Dự Án

> Không có phương pháp nào là tốt nhất tuyệt đối — chỉ có phương pháp phù hợp nhất với ngữ cảnh cụ thể. PM giỏi biết chọn và kết hợp.

---

## Tổng Quan

| Phương pháp | Phù hợp nhất khi | Tránh dùng khi |
|---|---|---|
| Waterfall | Requirement rõ ràng, ít thay đổi, compliance cao | Requirement mơ hồ, user feedback quan trọng |
| Agile/Scrum | Requirement thay đổi nhiều, cần deliver nhanh | Team không kỷ luật, khách hàng không available |
| Kanban | Công việc liên tục, không có sprint cố định | Cần hard deadline cho feature set cụ thể |
| Hybrid | Có phần rõ ràng + phần không chắc chắn | Team không experienced với cả hai approach |
| Prince2 | Dự án lớn, formal governance, nhiều stakeholder | Startup, team nhỏ, cần move fast |

---

## 1. Waterfall

### Mô tả
Waterfall (thác nước) là phương pháp tuyến tính: từng phase được hoàn thành trước khi chuyển sang phase tiếp theo. Không quay lại phase trước.

```
Requirements → Design → Implementation → Verification → Maintenance
    ↓               ↓            ↓               ↓
  Freeze           Freeze      Freeze          Freeze
```

### Khi nào dùng
- Requirement **rõ ràng, ổn định, ít thay đổi** (dưới 10%)
- Dự án có **compliance cao** (regulatory, audit trail cần thiết)
- Deliverable **vật lý hoặc không thể rollback** (xây dựng, phần cứng)
- Client không có thời gian hoặc không muốn tham gia thường xuyên
- Scope được fix by contract (fixed-price, fixed-scope)

### Khi nào KHÔNG dùng
- User chưa biết rõ mình muốn gì
- Technology mới, nhiều ẩn số kỹ thuật
- Market thay đổi nhanh, cần pivot sớm
- Team cần feedback loop để cải tiến liên tục

### Pros / Cons

| Pros | Cons |
|---|---|
| Documentation rõ ràng, dễ audit | Phát hiện lỗi muộn (thường ở phase Verification) |
| Dễ estimate cost và timeline | Khó thay đổi khi đã lock requirements |
| Phù hợp contract cố định | Rủi ro cao nếu requirement sai từ đầu |
| Stakeholder ít bị interrupt | Delivery muộn — user thấy product lần đầu ở cuối |

### Ví dụ thực tế Việt Nam

**Dự án core banking cho ngân hàng thương mại:**
- Requirement: Quy trình nghiệp vụ tín dụng được quy định bởi Ngân hàng Nhà nước → rõ ràng, ít thay đổi
- Compliance: Phải có đầy đủ documentation cho thanh tra
- Waterfall phù hợp: Phase SRS → System Design → Development → UAT → Go-live được define rõ từ đầu

**Dự án xây dựng hệ thống điều phối xe buýt cho Sở GTVT:**
- Scope fix trong hợp đồng đấu thầu
- Phải có documentation để quyết toán ngân sách nhà nước
- Team phát triển và stakeholder nhà nước quen với formal process

---

## 2. Agile / Scrum

### Agile Manifesto — 4 Giá Trị Cốt Lõi

```
We value:
  Individuals and interactions     OVER  processes and tools
  Working software                 OVER  comprehensive documentation
  Customer collaboration           OVER  contract negotiation
  Responding to change             OVER  following a plan

That is, while there is value in items on the right,
we value the items on the left more.
```

### 12 Nguyên Tắc Agile (Tóm Tắt)

1. Deliver working software sớm và liên tục — đây là thước đo tiến độ
2. Welcome changing requirements, kể cả late in development
3. Deliver working software thường xuyên (2 tuần đến 2 tháng)
4. Business và developer phải làm việc cùng nhau mỗi ngày
5. Build projects around motivated individuals — trust them
6. Face-to-face conversation là hiệu quả nhất
7. Working software là primary measure of progress
8. Agile processes promote sustainable development
9. Technical excellence và good design tăng agility
10. Simplicity — maximize the amount of work NOT done
11. Self-organizing teams tạo ra architecture tốt nhất
12. Regularly reflect và adjust behavior accordingly

### Scrum Framework Chi Tiết

#### Roles trong Scrum

| Role | Trách nhiệm chính |
|---|---|
| **Product Owner (PO)** | Quản lý Product Backlog, define priority, đại diện business/user |
| **Scrum Master (SM)** | Facilitate ceremonies, remove impediments, coach team |
| **Development Team** | Self-organizing, cross-functional, deliver increment |

#### Sprint — Đơn Vị Làm Việc Cơ Bản

```
Sprint (1–4 tuần, thường là 2 tuần):
┌────────────────────────────────────────────┐
│                                            │
│  Sprint Planning → Daily Standup (mỗi ngày)│
│       ↓                                    │
│  Sprint Execution (development work)       │
│       ↓                                    │
│  Sprint Review → Sprint Retrospective      │
│                                            │
└────────────────────────────────────────────┘
```

#### Scrum Ceremonies

**Sprint Planning (2–4 giờ cho sprint 2 tuần)**
- Team review Product Backlog
- PO explain priority và acceptance criteria
- Team commit những story sẽ làm trong sprint
- Output: Sprint Backlog

**Daily Standup (15 phút, đứng)**
- Mỗi người trả lời 3 câu:
  1. Hôm qua tôi đã làm gì?
  2. Hôm nay tôi sẽ làm gì?
  3. Có blocker nào không?
- Không giải quyết vấn đề tại đây — schedule offline meeting sau

**Sprint Review (1–2 giờ)**
- Team demo working software cho stakeholders
- PO accept hoặc reject story
- Stakeholders cho feedback
- Cập nhật Product Backlog dựa trên feedback

**Sprint Retrospective (1.5 giờ)**
- Team riêng (không có stakeholder ngoài)
- Ba câu hỏi: Làm tốt gì? Cần cải thiện gì? Hành động cụ thể cho sprint tới?
- Output: 1–3 action items để improve process

#### Scrum Artifacts

| Artifact | Mô tả | Ai quản lý |
|---|---|---|
| **Product Backlog** | Danh sách tất cả feature, bug, cải tiến theo priority | Product Owner |
| **Sprint Backlog** | Subset của Product Backlog được chọn cho sprint này | Dev Team |
| **Increment** | Working software hoàn chỉnh sau mỗi sprint | Dev Team |

### Khi nào dùng Scrum
- Startup SaaS cần iterate nhanh theo feedback user
- Mobile app với uncertain requirements
- Team 5–9 người, full-time, cross-functional
- PO có thể available thường xuyên để feedback

### Khi nào KHÔNG dùng Scrum
- Team phân tán múi giờ khác nhau, khó daily standup
- Dự án có fixed-price, fixed-scope contract (conflict với "welcome change")
- Stakeholder không có thời gian tham gia sprint review
- Team quá lớn (>15 người) — cần scale với SAFe hoặc LeSS

### Ví dụ thực tế Việt Nam

**Startup EdTech (Hà Nội, 12 người):**
- MVP platform dạy học online
- Sprint 2 tuần, demo mỗi 2 tuần cho early users
- Requirement thay đổi liên tục theo phản hồi học sinh
- Scrum phù hợp: iterate nhanh, học từ feedback, pivot khi cần

**Công ty SaaS HR (TP.HCM, 40 người, 3 teams):**
- Dùng Scrum theo team (3 teams × 8 người)
- Quarterly OKR align các team
- Release mỗi 2 tháng (kết hợp nhiều sprint)

---

## 3. Kanban

### Nguyên Tắc Kanban

Kanban không có sprint, không có fixed roles. Công việc flow liên tục qua các cột trạng thái.

**4 Nguyên tắc cốt lõi:**
1. **Visualize the workflow** — mọi thứ phải visible trên board
2. **Limit Work In Progress (WIP)** — không nhận task mới khi đang quá tải
3. **Manage flow** — tối ưu tốc độ flow, giảm bottleneck
4. **Make process policies explicit** — mọi người biết definition of done
5. **Improve collaboratively** — cải tiến dựa trên data, không phải cảm tính

### WIP Limits — Chìa Khóa Của Kanban

WIP (Work In Progress) limit = số lượng tối đa task được phép ở một cột tại một thời điểm.

```
Kanban Board:
┌──────────┬──────────────┬───────────┬───────────┬──────────┐
│ BACKLOG  │  IN PROGRESS │  REVIEW   │  TESTING  │   DONE   │
│          │   WIP: 3     │  WIP: 2   │  WIP: 2   │          │
├──────────┼──────────────┼───────────┼───────────┼──────────┤
│ Task A   │ Task D [Dev] │ Task G    │ Task I    │ Task J   │
│ Task B   │ Task E [Dev] │ Task H    │ Task K    │ Task L   │
│ Task C   │ Task F [Dev] │ (FULL!)   │ (FULL!)   │ ...      │
│ ...      │              │           │           │          │
└──────────┴──────────────┴───────────┴───────────┴──────────┘

Nếu REVIEW đầy (WIP=2), developer KHÔNG được push task mới vào Review.
Developer phải giúp unblock task ở Review trước.
```

**Tại sao WIP limits quan trọng:**
- Buộc team giải quyết bottleneck thay vì chồng chất thêm
- Giảm context switching, tăng focus
- Làm visible vấn đề sớm hơn

### Kanban vs Scrum

| Tiêu chí | Kanban | Scrum |
|---|---|---|
| Timeboxing | Không có sprint | Sprint cố định 1–4 tuần |
| Roles | Không có mandatory roles | PO, SM, Dev Team |
| Ceremonies | Không bắt buộc | Sprint Planning, Daily, Review, Retro |
| Thay đổi | Anytime | Chỉ trong Sprint Planning |
| Metric | Lead time, Cycle time, Throughput | Velocity (story points/sprint) |
| Phù hợp nhất | Continuous flow, support, ops | Product development, features |

### Khi nào dùng Kanban
- Support ticket queue (inbound, unpredictable)
- Bug fixing team
- IT operations, infrastructure team
- Marketing content production pipeline
- Bất kỳ công việc nào có flow liên tục, không batch

### Ví dụ thực tế Việt Nam

**Team support của công ty phần mềm kế toán:**
- Hàng ngày nhận 50–100 ticket từ khách hàng
- Không thể sprint plan vì ticket đến bất kỳ lúc nào
- Kanban board: Incoming → Triaged → In Progress → Waiting Customer → Resolved
- WIP limit In Progress = 5 (mỗi support agent cùng lúc không handle quá 2 ticket)

**Team DevOps/Infrastructure:**
- Deployment requests, server provisioning, certificate renewal
- Không có sprint — công việc đến khi nào xử lý khi đó
- Kanban phù hợp hơn Scrum

---

## 4. Hybrid

### Khi nào dùng Hybrid
Hybrid là kết hợp Waterfall và Agile. Thường áp dụng khi:
- Dự án có một **phần requirements rõ ràng** (architecture, infrastructure setup) và một **phần uncertain** (user-facing features)
- Stakeholder quen với Waterfall nhưng team muốn Agile
- Contract yêu cầu milestone cố định nhưng trong đó cho phép iterative development

### Ví dụ: Migration Project

```
Phase 1 (Waterfall — 2 tháng):
  Requirements lock → Architecture design → Infrastructure setup
  (Rõ ràng, phụ thuộc nhau, khó thay đổi)

Phase 2 (Agile — 4 tháng):
  Sprint 1: Migrate module A → Sprint 2: Module B → Sprint 3: Module C...
  (Iterate, học từ mỗi sprint, adjust priority)

Phase 3 (Waterfall — 1 tháng):
  UAT → Performance testing → Go-live → Hypercare
  (Fixed process, compliance, không thể iterate)
```

### Ví dụ thực tế Việt Nam

**Dự án chuyển đổi số cho công ty sản xuất 500 nhân viên:**
- Phase 1 (Waterfall): BPR (Business Process Reengineering) — phân tích nghiệp vụ, thiết kế quy trình mới, mua ERP
- Phase 2 (Agile): Customize ERP theo từng module — mỗi sprint deliver 1 module hoàn chỉnh
- Phase 3 (Waterfall): Data migration, go-live, hypercare

---

## 5. Prince2

### Mô tả
Prince2 (PRojects IN Controlled Environments) là framework quản lý dự án formal, phổ biến ở UK, EU, và các tổ chức chính phủ. Tập trung vào business justification, defined roles, và controlled stages.

### 7 Principles của Prince2

1. Continued business justification (luôn phải justify tại sao tiếp tục)
2. Learn from experience
3. Defined roles and responsibilities
4. Manage by stages (milestone-driven)
5. Manage by exception (chỉ escalate khi vượt tolerance)
6. Focus on products (deliverable-centric)
7. Tailor to suit the project environment

### Khi nào dùng Prince2
- Dự án chính phủ, tài chính, năng lượng
- Môi trường UK/EU/Australia
- Cần governance và audit trail chặt chẽ
- Multiple stakeholders với formal accountability

### Khi nào KHÔNG dùng Prince2
- Startup, SME, team nhỏ — overhead quá lớn
- Dự án cần tốc độ, flexibility cao
- Team không có kinh nghiệm Prince2 và không có thời gian train

### Ví dụ thực tế
**Dự án chuyển đổi hệ thống thanh toán cho công ty tài chính lớn ở Việt Nam** (liên doanh với đối tác nước ngoài):
- Đối tác UK yêu cầu Prince2 framework
- Formal stage gates (Project Initiation Document, Stage Plans, End Stage Reports)
- Exception reports phải được approve bởi Project Board

---

## Bảng So Sánh Tổng Hợp

| Tiêu chí | Waterfall | Scrum | Kanban | Hybrid | Prince2 |
|---|---|---|---|---|---|
| **Flexibility** | Thấp | Cao | Rất cao | Trung bình | Thấp–Trung |
| **Visibility** | Thấp (thấy muộn) | Cao (mỗi sprint) | Cao (realtime) | Trung bình | Trung bình |
| **Documentation** | Nặng | Nhẹ | Rất nhẹ | Vừa | Rất nặng |
| **Phù hợp team size** | Bất kỳ | 5–9 | Bất kỳ | Bất kỳ | Trung–lớn |
| **Customer involvement** | Thấp | Cao | Thấp–Trung | Vừa | Trung bình |
| **Phổ biến ở VN** | Phổ biến | Rất phổ biến | Phổ biến | Phổ biến | Ít |
| **Learning curve** | Thấp | Trung bình | Thấp | Trung bình | Cao |

---

## Tóm Tắt

Khi bạn join một dự án, PM cần hỏi ngay:
1. **Requirement có stable không?** → Nếu yes: lean Waterfall; Nếu no: lean Agile
2. **Delivery có thể incremental không?** → Nếu yes: Scrum/Kanban; Nếu no: Waterfall
3. **Team làm batch hay continuous work?** → Batch: Scrum; Continuous: Kanban
4. **Governance level?** → Formal/audit: Prince2 hoặc Waterfall; Lean: Agile

**Tiếp theo:** Làm bài tập [exercises/01-phan-tich-iron-triangle.md](./exercises/01-phan-tich-iron-triangle.md)
