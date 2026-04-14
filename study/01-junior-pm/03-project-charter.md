# Project Charter — Điều Lệ Dự Án

> "Một dự án không có Project Charter giống như lên đường mà không có bản đồ — mọi người có thể đi cùng xe nhưng đến những đích khác nhau."

---

## Project Charter Là Gì?

Project Charter là **tài liệu chính thức phê duyệt sự tồn tại của dự án** và trao quyền cho Project Manager sử dụng nguồn lực tổ chức để thực hiện dự án.

Charter KHÔNG phải:
- Kế hoạch dự án chi tiết (đó là Project Plan / Gantt chart)
- Đặc tả kỹ thuật (đó là Technical Specification)
- Hợp đồng thương mại (đó là SLA/Contract)

Charter LÀ:
- Sự đồng thuận chính thức: "Chúng ta đang làm gì và tại sao"
- Ranh giới rõ ràng về scope — ngăn scope creep
- Nguồn sự thật duy nhất (single source of truth) cho dự án
- Nền tảng để PM có authority ra quyết định

---

## Khi Nào Cần Project Charter?

**Luôn luôn cần khi:**
- Dự án kéo dài > 1 tháng
- Budget > 50 triệu VND
- Có nhiều hơn 2 bộ phận liên quan
- Cần cross-department resource allocation
- Dự án có ảnh hưởng đến business operations hiện tại

**Có thể bỏ qua khi:**
- Task nhỏ trong sprint (dùng Jira Story thay thế)
- Proof-of-concept / spike (1–2 tuần, team nội bộ)
- Bug fix / maintenance work

**Thực tế ở nhiều công ty Việt Nam:** Charter bị bỏ qua → dự án trễ, scope không rõ, ai cũng nghĩ "việc của người khác". Charter là protection cho cả PM lẫn team.

---

## Template Đầy Đủ Với Giải Thích

```markdown
# PROJECT CHARTER
## [Tên Dự Án]

---

### 1. THÔNG TIN DỰ ÁN

| Thông tin | Chi tiết |
|---|---|
| Tên dự án | [Tên ngắn gọn, rõ ràng] |
| Project Sponsor | [Người có quyền phê duyệt budget và priority] |
| Project Manager | [PM chịu trách nhiệm delivery] |
| Ngày bắt đầu | DD/MM/YYYY |
| Ngày kết thúc (dự kiến) | DD/MM/YYYY |
| Phiên bản charter | v1.0 |
| Ngày cập nhật | DD/MM/YYYY |
```

**Giải thích Project Sponsor:** Đây là người "chủ" thực sự của dự án — người có budget, người được hưởng lợi, người ra quyết định cuối khi có conflict. Không phải CTO hay CEO tự động — mà là người business owner của outcome. Ví dụ: dự án portal HR thì Sponsor = CHRO (Chief HR Officer).

```markdown
---

### 2. MỤC TIÊU DỰ ÁN (SMART Goals)
```

**SMART = Specific, Measurable, Achievable, Relevant, Time-bound**

Ví dụ BAD (mơ hồ):
> "Cải thiện hệ thống quản lý kho để hoạt động tốt hơn."

Ví dụ GOOD (SMART):
> "Migrate toàn bộ module quản lý kho từ Delphi sang web-based application, giảm thời gian xử lý nhập/xuất kho từ 5 phút/lần xuống dưới 2 phút/lần, hoàn thành và go-live trước ngày 31/12/2025."

```markdown
### 3. SCOPE IN (Nằm Trong Phạm Vi Dự Án)
```

Liệt kê rõ ràng những gì DỰ ÁN SẼ DELIVER. Càng cụ thể càng tốt. Tránh từ ngữ mơ hồ như "cải thiện", "tốt hơn".

Ví dụ tốt:
- Migrate 5 module: nhập kho, xuất kho, tồn kho, báo cáo, user management
- Chuyển toàn bộ dữ liệu lịch sử 5 năm từ Delphi DB sang PostgreSQL
- Training cho 20 người dùng cuối (2 buổi, mỗi buổi 3 giờ)
- Go-live support trong 4 tuần sau cutover (hypercare)

```markdown
### 4. SCOPE OUT (Ngoài Phạm Vi Dự Án)
```

**Đây là phần bị bỏ qua nhiều nhất — và gây scope creep nhiều nhất.**

Liệt kê rõ những gì KHÔNG thuộc dự án này:

Ví dụ:
- Không bao gồm module kế toán (dự án riêng, Q2/2026)
- Không phát triển mobile app
- Không thay đổi business process hiện tại (chỉ migrate, không redesign)
- Không tích hợp với hệ thống ERP của tập đoàn mẹ

```markdown
### 5. MILESTONES CHÍNH

| Milestone | Mô Tả | Deadline | Người Chịu Trách Nhiệm |
|---|---|---|---|
| M1: Project Kickoff | Charter approved, team assembled | DD/MM | PM |
| M2: Analysis Complete | Current system documented, gap analysis done | DD/MM | BA + PM |
| M3: Dev Complete | All modules developed and unit tested | DD/MM | Tech Lead |
| M4: UAT Complete | User acceptance testing passed, bugs fixed | DD/MM | QA + PM |
| M5: Go-Live | System deployed to production | DD/MM | PM + DevOps |
| M6: Hypercare End | Support period ended, project closed | DD/MM | PM |
```

```markdown
### 6. BUDGET ƯỚC TÍNH

| Hạng Mục | Chi Phí Ước Tính | Ghi Chú |
|---|---|---|
| Nhân lực internal | X triệu | Y người × Z tháng |
| Nhân lực contractor | X triệu | Nếu có |
| Infrastructure | X triệu | Server, cloud, licenses |
| Training | X triệu | |
| Contingency (10–20%) | X triệu | Risk buffer |
| **TỔNG** | **X triệu** | |

**Budget Approval Level:** [Ai phê duyệt nếu vượt budget — ví dụ: PM tự quyết đến 10%, Sponsor quyết từ 10–20%, Board trên 20%]
```

```markdown
### 7. RỦI RO CHÍNH

| # | Rủi Ro | Xác Suất | Impact | Score | Mitigation |
|---|---|---|---|---|---|
| R1 | [Mô tả] | Cao/TB/Thấp | Cao/TB/Thấp | H/M/L | [Kế hoạch giảm nhẹ] |
| R2 | | | | | |
| R3 | | | | | |

*Score = Xác suất × Impact: H×H=Critical, H×TB=High, TB×TB=Medium, Thấp×Thấp=Low*
```

```markdown
### 8. STAKEHOLDERS

| Tên / Vai Trò | Bộ Phận | Mức Độ Ảnh Hưởng | Kỳ Vọng Chính |
|---|---|---|---|
| [Tên] / Sponsor | [Bộ phận] | Rất cao | Dự án on-time, on-budget |
| [Tên] / End User Lead | [Bộ phận] | Cao | Hệ thống dễ dùng, training đầy đủ |
| [Tên] / IT Director | IT | Cao | Security, maintainability |
| [Tên] / Finance | Finance | TB | Budget không vượt |

---

### 9. CHỮ KÝ PHÊ DUYỆT

| Vai Trò | Họ Tên | Chữ Ký | Ngày |
|---|---|---|---|
| Project Sponsor | | | |
| Project Manager | | | |
| [Stakeholder quan trọng khác] | | | |
```

---

## Ví Dụ 1: Project Charter Hoàn Chỉnh — Migration Delphi → Modern Stack

```markdown
# PROJECT CHARTER
## Dự Án: Migration Hệ Thống Quản Lý Kho — Delphi to WMS Web

---

### 1. THÔNG TIN DỰ ÁN

| Thông tin | Chi tiết |
|---|---|
| Tên dự án | WMS Migration 2025 |
| Project Sponsor | Bà Nguyễn Thị Lan — COO, Công ty Logistics ABC |
| Project Manager | Anh Trần Minh Khoa — IT PM |
| Ngày bắt đầu | 01/09/2025 |
| Ngày kết thúc (dự kiến) | 31/12/2025 |
| Phiên bản | v1.2 |
| Ngày cập nhật | 15/09/2025 |

---

### 2. MỤC TIÊU DỰ ÁN (SMART Goals)

1. **Migrate toàn bộ 5 module** của hệ thống WMS (Warehouse Management System) từ Delphi sang nền tảng web (React + .NET Core + PostgreSQL) trước ngày 31/12/2025.

2. **Giảm thời gian xử lý** nhập/xuất kho từ trung bình 5 phút/lần xuống dưới 2 phút/lần (đo lường sau 30 ngày go-live).

3. **Zero downtime** trong giờ cao điểm (7:00–9:00 và 16:00–18:00) trong quá trình cutover.

4. **100% data integrity** — toàn bộ dữ liệu lịch sử 5 năm (2020–2024) được migrate chính xác, xác nhận bằng reconciliation report.

---

### 3. SCOPE IN

- Migration module nhập kho (Goods Receipt)
- Migration module xuất kho (Goods Issue)
- Migration module tồn kho và vị trí lưu (Inventory & Location)
- Migration module báo cáo (tồn kho, movement history, aging)
- Migration module user management và phân quyền
- Data migration: 5 năm lịch sử giao dịch (~2 triệu records)
- Training: 25 users (3 buổi × 3 giờ, cả HCM và Hà Nội)
- Hypercare support: 4 tuần sau go-live
- Tài liệu: User manual, Admin guide, Runbook

---

### 4. SCOPE OUT

- Module kế toán và tích hợp với phần mềm kế toán (dự án riêng năm 2026)
- Mobile app cho warehouse staff (Phase 2, Q2/2026)
- Barcode scanner / RFID integration (Phase 2)
- Thay đổi quy trình nghiệp vụ (chỉ digitize quy trình hiện tại, không redesign)
- Training cho manager về advanced analytics (scope training riêng)
- SLA support sau hypercare period (sẽ thảo luận riêng)

---

### 5. MILESTONES CHÍNH

| Milestone | Mô Tả | Deadline | Responsible |
|---|---|---|---|
| M0: Kickoff | Charter signed, team onboarded, tools ready | 05/09/2025 | PM |
| M1: Analysis | Current system doc, data mapping, gap analysis | 26/09/2025 | BA + PM |
| M2: Dev Sprint 1 | Module nhập kho + xuất kho (unit tested) | 24/10/2025 | Tech Lead |
| M3: Dev Sprint 2 | Module tồn kho + báo cáo + user mgmt | 21/11/2025 | Tech Lead |
| M4: UAT | Acceptance testing, bug fixing (max 2 tuần) | 05/12/2025 | QA + PM |
| M5: Data Migration Dry Run | Test data migration, reconciliation | 12/12/2025 | DBA + PM |
| M6: Go-Live | Production cutover (thứ Bảy) | 20/12/2025 | PM + DevOps |
| M7: Hypercare End | 4-week support period ends | 17/01/2026 | PM |

---

### 6. BUDGET

| Hạng Mục | Chi Phí | Ghi Chú |
|---|---|---|
| Dev team (3 devs × 4 tháng) | 120 triệu | Internal cost |
| PM + BA (4 tháng) | 60 triệu | Internal cost |
| QA (2 tháng) | 20 triệu | Internal cost |
| Infrastructure (cloud, licenses) | 15 triệu | Azure hosting 1 năm |
| Training | 8 triệu | Venue + materials + travel HN |
| Contingency (15%) | 33 triệu | Risk buffer |
| **Tổng** | **256 triệu** | |

**Approval:** PM tự quyết ≤ 15%; Sponsor ≤ 30%; COO + CFO > 30%

---

### 7. RỦI RO CHÍNH

| # | Rủi Ro | XS | Impact | Score | Mitigation |
|---|---|---|---|---|---|
| R1 | Dữ liệu Delphi DB bị corrupt, không migrate được | TB | Cao | High | Backup daily từ D-30; dry run migration 2 lần trước go-live |
| R2 | Users kháng cự thay đổi hệ thống mới | Cao | TB | High | Change management plan; involve key users từ phase analysis |
| R3 | Team dev overloaded, delay development | TB | Cao | High | Buffer 2 tuần trong plan; identify backup developer ngay từ đầu |
| R4 | Go-live gặp sự cố, cần rollback sang Delphi | Thấp | Rất Cao | High | Giữ Delphi chạy song song 2 tuần sau go-live; runbook rollback ready |
| R5 | Scope creep từ business (thêm yêu cầu mới) | Cao | TB | High | Charter sign-off rõ ràng; mọi thay đổi qua formal change request |

---

### 8. STAKEHOLDERS

| Tên / Vai Trò | Bộ Phận | Ảnh Hưởng | Kỳ Vọng |
|---|---|---|---|
| Bà Nguyễn Thị Lan / COO | Executive | Rất Cao | On-time, zero business disruption |
| Anh Phạm Văn Hùng / Warehouse Manager | Operations | Cao | Hệ thống dễ dùng hơn Delphi, training đầy đủ |
| Chị Lê Thu Hà / IT Director | IT | Cao | Security, maintainability, proper documentation |
| Anh Đỗ Quang Minh / CFO | Finance | TB | On-budget, ROI rõ ràng |
| 22 Warehouse Staff | Operations | TB | Không mất dữ liệu, training tốt |

---

### 9. CHỮ KÝ PHÊ DUYỆT

| Vai Trò | Họ Tên | Chữ Ký | Ngày |
|---|---|---|---|
| Project Sponsor / COO | Nguyễn Thị Lan | ___________ | ___/___/2025 |
| Project Manager | Trần Minh Khoa | ___________ | ___/___/2025 |
| IT Director | Lê Thu Hà | ___________ | ___/___/2025 |
```

---

## Ví Dụ 2: Project Charter — Phát Triển Tính Năng Mới Cho SaaS

```markdown
# PROJECT CHARTER
## Module Chấm Công Tự Động — HRM SaaS v3.5

### Thông Tin Dự Án
| | |
|---|---|
| Sponsor | Bà Trần Kim Anh — CPO (Chief Product Officer) |
| PM | Anh Lê Hoàng Nam — Product Manager |
| Bắt đầu | 01/10/2025 |
| Go-live target | 15/12/2025 (10 tuần) |

### Mục Tiêu
Phát triển module chấm công tự động để: (1) Giảm 80% thời gian HR xử lý dữ liệu chấm công thủ công; (2) Cho phép manager approve/reject overtime trong vòng 24 giờ; (3) Đạt 90% satisfaction score từ HR users trong survey 30 ngày sau launch.

### Scope IN
- Check-in/check-out theo ca làm việc (fixed + flexible shift)
- Tính toán tự động: giờ tăng ca, đi trễ, về sớm
- Approval workflow: employee submit → manager approve/reject
- Báo cáo chấm công: ngày, tuần, tháng
- Export PDF/Excel cho payroll
- Integration với module Leave Management (đã có)
- Email notification: reminder check-in, OT approval result

### Scope OUT
- Facial recognition / GPS check-in (Phase 2)
- Mobile app (web-responsive là đủ cho Phase 1)
- Integration với third-party payroll software
- Shift scheduling tự động (scope riêng)

### Budget
Dev: 80 triệu (4 devs × 2.5 tháng) | QA: 15 triệu | Design: 10 triệu | Contingency: 16 triệu | **Total: 121 triệu**

### Top Risks
1. Compliance với Luật Lao Động VN — cần legal review các quy tắc tính OT (Xác suất: TB, Impact: Cao → Solution: Legal consultant review vào sprint 1)
2. Client data privacy — attendance data sensitive (→ PDPA compliance review)
3. Scope từ sales team muốn thêm features vào demo (→ Charter sign-off cứng)
```

---

## Common Mistakes Khi Viết Project Charter

### Mistake 1: Mục tiêu mơ hồ

**Sai:** "Cải thiện hiệu suất hệ thống"
**Đúng:** "Giảm thời gian load trang dashboard từ 8 giây xuống dưới 2 giây (đo bằng Lighthouse score ≥ 90)"

### Mistake 2: Scope IN không đủ cụ thể

**Sai:** "Phát triển tính năng báo cáo"
**Đúng:** "Phát triển 5 loại báo cáo: (1) tồn kho theo ngày, (2) nhập kho theo tháng, (3) xuất kho theo khách hàng, (4) aging report, (5) movement history — tất cả có filter và export Excel/PDF"

### Mistake 3: Quên viết Scope OUT

Đây là lỗi phổ biến nhất. Hậu quả: stakeholder sau này add thêm yêu cầu và nói "tôi nghĩ đây là trong scope".

### Mistake 4: Budget không có contingency

Mọi dự án đều có unexpected costs. Không có contingency = sẽ vượt budget.
**Rule of thumb:** 10–15% cho dự án quen thuộc, 20–30% cho dự án với nhiều unknowns.

### Mistake 5: Sponsor ký nhưng không đọc

Charter chưa được reviewed kỹ nhưng vẫn được ký vì "bận quá". Sau này conflict xảy ra, không ai nhớ đã đồng ý gì.

**Giải pháp:** Khi present charter, walk sponsor qua từng phần, hỏi câu hỏi cụ thể: "Anh/chị có đồng ý rằng mobile app KHÔNG thuộc scope lần này không?"

---

## Tips: Cách Get Sign-Off Từ Sponsor

### Vấn Đề Thực Tế

Sponsor bận, không muốn đọc tài liệu dài. Charter gửi qua email thường bị ignore 1–2 tuần.

### Chiến Lược Hiệu Quả

**1. Pre-sell trước khi present:**
Gặp 1:1 với sponsor trước, walk through draft, ghi nhận feedback. Khi present chính thức, không có surprises.

**2. Executive Summary 1 trang:**
Tóm tắt charter trong 1 trang: mục tiêu, scope (bullet IN/OUT), timeline, budget, top 3 risks. Đây là thứ sponsor thực sự đọc.

**3. Đặt deadline rõ ràng:**
"Tôi cần chữ ký trước thứ Sáu 17:00 để kickoff team vào thứ Hai tuần sau như kế hoạch."

**4. Xử lý "pending review":**
Nếu sau 5 ngày chưa có phản hồi: "Tôi giả định rằng silence = approval và sẽ proceed theo plan. Nếu có thay đổi, vui lòng báo tôi trước thứ Sáu."

**5. Meeting walk-through:**
Đừng gửi charter và chờ — schedule 30 phút với sponsor để walk through. Ký ngay tại meeting nếu có thể.

---

## Checklist Review Project Charter

Trước khi submit cho sponsor, tự review:

```
THÔNG TIN CƠ BẢN
[ ] Sponsor được xác định rõ (tên, chức vụ, bộ phận)
[ ] PM được xác định
[ ] Start date và target end date có trong charter
[ ] Version và ngày cập nhật ghi rõ

MỤC TIÊU
[ ] Mục tiêu SMART — có số đo cụ thể
[ ] Có thể đánh giá "thành công" hay không sau khi dự án xong
[ ] Business value rõ ràng — tại sao làm dự án này?

SCOPE
[ ] Scope IN: đủ cụ thể, không mơ hồ
[ ] Scope OUT: đã liệt kê ít nhất 3–5 items ngoài scope
[ ] Stakeholders đã review và đồng ý với scope

MILESTONES
[ ] Ít nhất 4–6 milestones chính
[ ] Mỗi milestone có deadline cụ thể
[ ] Mỗi milestone có người chịu trách nhiệm

BUDGET
[ ] Có contingency (≥ 10%)
[ ] Approval levels rõ ràng
[ ] Budget breakdown theo hạng mục

RỦI RO
[ ] Ít nhất 3–5 rủi ro được identify
[ ] Mỗi rủi ro có mitigation plan
[ ] Risk owner được assign

STAKEHOLDERS
[ ] Tất cả stakeholders chính được identify
[ ] Kỳ vọng của từng stakeholder được ghi nhận

KÝ DUYỆT
[ ] Sponsor đã ký
[ ] PM đã ký
[ ] Các stakeholder quan trọng khác đã ký (nếu cần)
```
