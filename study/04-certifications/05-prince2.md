# PRINCE2 — Projects IN Controlled Environments

## Tổng Quan

PRINCE2 là phương pháp PM được phát triển bởi chính phủ UK (CCTA, nay là Cabinet Office), hiện được quản lý bởi Axelos. Đây là phương pháp PM được sử dụng rộng rãi nhất ở **UK, EU, Úc** và phổ biến trong các công ty Nhật Bản.

---

## 7 Principles (Nguyên Tắc)

Principles là nền tảng — không thể bỏ bất kỳ principle nào mà vẫn gọi là PRINCE2:

| # | Principle | Ý nghĩa |
|---|---|---|
| 1 | **Continued Business Justification** | Dự án phải có lý do kinh doanh hợp lý trong suốt vòng đời |
| 2 | **Learn from Experience** | Lessons learned phải được capture và áp dụng liên tục |
| 3 | **Defined Roles and Responsibilities** | Mỗi người phải biết rõ vai trò của mình |
| 4 | **Manage by Stages** | Dự án được chia thành stages, có gate review giữa các stage |
| 5 | **Manage by Exception** | PM chỉ escalate khi vượt tolerance threshold đã định |
| 6 | **Focus on Products** | Định nghĩa rõ sản phẩm/deliverable trước khi làm |
| 7 | **Tailor to Suit the Project** | Adapt PRINCE2 theo size và complexity của dự án |

---

## 7 Themes (Chủ Đề)

Themes là các khía cạnh cần quản lý xuyên suốt dự án:

| Theme | Documents chính | Mục đích |
|---|---|---|
| **Business Case** | Business Case document | Why — Tại sao dự án tồn tại |
| **Organization** | Project Initiation Document | Who — Ai làm gì |
| **Quality** | Quality Register, Product Descriptions | What — Tiêu chuẩn chất lượng |
| **Plans** | Project Plan, Stage Plans | How & When — Kế hoạch |
| **Risk** | Risk Register | Upside & Downside risks |
| **Change** | Issue Register, Change Log | Change control |
| **Progress** | Checkpoint Reports, Highlight Reports | Status tracking |

---

## 7 Processes (Quy Trình)

```
[SU] Starting Up a Project
         ↓
[IP] Initiating a Project ←───────────────────────────────────┐
         ↓                                                      │
[DP] Directing a Project (Project Board, runs throughout)      │
         ↓                                                      │
[CS] Controlling a Stage → [MP] Managing Product Delivery      │
         ↓                                                      │
[SB] Managing a Stage Boundary ────────────────────────────────┘
         ↓
[CP] Closing a Project
```

| Process | Viết tắt | Ai thực hiện | Key output |
|---|---|---|---|
| Starting Up | SU | PM + Executive | Project Brief |
| Initiating | IP | PM | Project Initiation Document (PID) |
| Directing | DP | Project Board | Authorize/direct/close decisions |
| Controlling a Stage | CS | PM | Work packages, checkpoint reports |
| Managing Product Delivery | MP | Team Manager | Completed products |
| Managing Stage Boundary | SB | PM | End Stage Report, Next Stage Plan |
| Closing | CP | PM | End Project Report, Lessons Learned |

---

## PRINCE2 vs PMP: So Sánh

| | PRINCE2 | PMP |
|---|---|---|
| **Origin** | UK Government | USA (PMI) |
| **Phổ biến ở** | UK, EU, Úc, Japan | USA, Global |
| **Approach** | Prescriptive (có cấu trúc rõ) | Descriptive (best practices) |
| **Focus** | Process & governance | Knowledge areas |
| **Flexibility** | Tailoring là principle | Adaptive by nature |
| **Agile** | PRINCE2 Agile (riêng) | Tích hợp trong PMP ECO |
| **Experience req.** | Không (Foundation) | 36 tháng (PMP) |
| **Cost Foundation** | ~£280 | N/A |
| **Cost Mid-level** | ~£350 (Practitioner) | $405-555 (PMP) |

**Khi nào chọn PRINCE2:**
- Làm việc với công ty UK/EU/Nhật
- Outsourcing contract với công ty nước ngoài
- Dự án chính phủ hoặc tài chính ở EU
- Background muốn có structured governance framework

**Khi nào chọn PMP:**
- Làm việc global, đặc biệt US-based companies
- Muốn recognized globally nhất
- Môi trường Agile/Hybrid

---

## PRINCE2 Foundation

**Dành cho:** Ai muốn hiểu framework, chưa cần apply

| Thông tin | Chi tiết |
|---|---|
| Yêu cầu | Không cần kinh nghiệm PM |
| Chi phí | ~£280 (~$350) |
| Đề thi | 60 câu MCQ, 60 phút, pass ≥ 55% (33/60) |
| Format | Closed book |
| Study time | 4-6 tuần |

**Study Plan 4 tuần:**
- Tuần 1: 7 Principles + 7 Themes (Business Case, Organization, Quality)
- Tuần 2: Remaining 4 Themes (Plans, Risk, Change, Progress)
- Tuần 3: 7 Processes
- Tuần 4: Mock exams + revision

**Resources:**
- Official PRINCE2 manual (Managing Successful Projects with PRINCE2)
- Udemy: PRINCE2 Foundation by Frank Turley (~$15)
- Free mock exams: prince2.com/practice-exams

---

## PRINCE2 Practitioner

**Dành cho:** PM muốn apply PRINCE2 trong thực tế

| Thông tin | Chi tiết |
|---|---|
| Yêu cầu | Có PRINCE2 Foundation certificate |
| Chi phí | ~£350 (~$440) |
| Đề thi | 68 câu scenario-based, 150 phút |
| Format | **Open book** (official manual được phép dùng) |
| Pass score | ≥ 55% (38/68) |
| Study time | 6-8 tuần sau Foundation |

**Key difference:** Practitioner test khả năng **apply** principles vào scenarios thực tế, không phải recall.

---

## PRINCE2 Agile

Kết hợp PRINCE2 governance với Agile delivery methods (Scrum, Kanban).

**Phù hợp khi:**
- Tổ chức đã dùng PRINCE2 muốn chuyển sang Agile
- Cần governance chặt (PRINCE2) + flexibility (Agile)

---

## Key PRINCE2 Concepts cho Developer → PM

### Tolerance (Dung Sai)

PRINCE2 dùng khái niệm tolerance thay vì "phải báo cáo mọi thứ":

```
PM có tolerance:  Time: ±2 tuần, Cost: ±5%
Nếu vượt tolerance → Escalate lên Project Board
Nếu trong tolerance → PM tự xử lý
```

Đây là "Manage by Exception" — rất thực tế, giúp không overwhelm C-level với details.

### Project Board (≠ Scrum Board)

PRINCE2 có Project Board gồm 3 vai trò:
- **Executive:** Chịu trách nhiệm business case (thường là sponsor)
- **Senior User:** Đại diện người dùng cuối
- **Senior Supplier:** Đại diện bên cung cấp/development

### Stage Gate Reviews

Cuối mỗi stage, Project Board review và quyết định:
- Continue to next stage?
- Modify approach?
- Stop project?

---

## Câu Hỏi Reflection

1. Nếu bạn đang làm outsourcing cho khách hàng Nhật Bản, PRINCE2 hay PMP phù hợp hơn? Tại sao?
2. PRINCE2's "Manage by Exception" translate thế nào vào một dự án Agile Sprint?
3. Giả sử công ty bạn đang dùng Scrum, PRINCE2 Agile có thể bổ sung gì?
