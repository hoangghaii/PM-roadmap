# PROJECT CHARTER

| Field | Chi Tiết |
|---|---|
| **Tên dự án** | [Tên đầy đủ] |
| **Project ID** | [PC-YYYYMM-XXX] |
| **Phiên bản** | 1.0 |
| **Ngày tạo** | DD/MM/YYYY |
| **Project Sponsor** | [Tên - Chức vụ - Email] |
| **Project Manager** | [Tên - Email - Phone] |
| **Start Date** | DD/MM/YYYY |
| **Target End Date** | DD/MM/YYYY |
| **Department / Business Unit** | [Phòng ban] |
| **Ngân sách ước tính** | [X triệu VND] |

---

## 1. BỐI CẢNH VÀ LÝ DO (Business Case)

[Tại sao dự án này cần thực hiện? Vấn đề nào cần giải quyết? Cơ hội nào cần nắm bắt?]

**Hướng dẫn điền:**
- Mô tả vấn đề/cơ hội hiện tại bằng **số liệu cụ thể**: "Tỷ lệ lỗi manual hiện tại là 15%, gây tổn thất X triệu/tháng"
- Giải thích **tại sao bây giờ** — nếu không làm thì sao? Cost of inaction là gì?
- Kết nối với **mục tiêu chiến lược công ty** (OKR, KPI công ty năm nay)
- Độ dài lý tưởng: 1-2 đoạn (100-200 từ)

**Ví dụ tốt:**
> Hiện tại quy trình onboarding nhân viên mới tốn trung bình 5 ngày làm việc do phải xử lý thủ công qua email và Google Forms rời rạc. Với tốc độ tuyển dụng 20 người/tháng, bộ phận HR mất ~100 ngày công/tháng chỉ cho onboarding. Dự án này sẽ xây dựng hệ thống onboarding tự động, giảm thời gian xuống còn 1 ngày, tiết kiệm ước tính 400 triệu VND/năm và cải thiện trải nghiệm nhân viên mới.

**Common mistakes:**
- Viết quá chung chung: "Dự án này quan trọng cho công ty" — không đủ để justify đầu tư
- Không có số liệu: Stakeholders cần data để approve ngân sách
- Quá kỹ thuật: Business case viết cho CFO đọc, không phải cho dev team

---

## 2. MỤC TIÊU DỰ ÁN (SMART)

**Mục tiêu:** [1-2 câu mô tả kết quả cụ thể, đo lường được]

**Thành công trông như thế nào (Definition of Done):**
- [ ] [Tiêu chí 1 — cụ thể, đo lường được]
- [ ] [Tiêu chí 2]
- [ ] [Tiêu chí 3]
- [ ] [Tiêu chí 4]
- [ ] [Tiêu chí 5]

**Hướng dẫn điền:**
Áp dụng khung SMART cho từng mục tiêu:
- **S**pecific: Cụ thể — "Hệ thống X", không phải "Cải thiện quy trình"
- **M**easurable: Đo được — "Giảm 80%", không phải "Giảm đáng kể"
- **A**chievable: Khả thi — Không cam kết những gì team chưa từng làm được
- **R**elevant: Liên quan đến business case ở Section 1
- **T**ime-bound: Có deadline — "Trước 30/06/2026"

**Ví dụ Definition of Done tốt:**
- [ ] Hệ thống xử lý 100% đơn hàng online không cần can thiệp thủ công
- [ ] Thời gian xử lý đơn giảm từ 24h xuống dưới 2h
- [ ] Tỷ lệ lỗi dưới 0.5% (hiện tại 5%)
- [ ] 95% end users đánh giá "Satisfied" hoặc "Very Satisfied" sau training
- [ ] Đi live trước 01/07/2026

**Common mistakes:**
- Mục tiêu kiểu "Deliver the project on time and on budget" — đây là constraint, không phải objective
- Quá nhiều mục tiêu (>5): Dilute focus, khó track
- Không có baseline: Để đo "giảm 80%" thì phải biết điểm xuất phát là bao nhiêu

---

## 3. PHẠM VI DỰ ÁN (Scope)

### 3.1 Trong phạm vi (In Scope)
- [Feature/deliverable 1]
- [Feature/deliverable 2]
- [Feature/deliverable 3]
- [Feature/deliverable 4]

### 3.2 Ngoài phạm vi (Out of Scope)
- [Explicitly excluded item 1 — để tránh scope creep]
- [Explicitly excluded item 2]
- [Explicitly excluded item 3]

### 3.3 Assumptions (Giả định)
- [Assumption 1 — điều chúng ta giả định là đúng nhưng chưa được confirm]
- [Assumption 2]
- [Assumption 3]

### 3.4 Constraints (Ràng buộc)
- Budget không vượt quá [X triệu VND]
- Deadline cứng: [ngày] vì [lý do — ví dụ: sự kiện ra mắt, regulatory deadline]
- Technology stack phải sử dụng [framework/platform hiện có]
- Team size tối đa [X người]

**Hướng dẫn điền:**

**In Scope vs Out of Scope** — Đây là section quan trọng nhất để tránh scope creep. Nguyên tắc: "If it's not explicitly in scope, it's out of scope." Nhưng đừng để stakeholder tự suy diễn — list rõ những gì bạn biết họ hay hỏi về.

**Ví dụ Out of Scope tốt:**
- Integration với hệ thống legacy ERP (dự kiến phase 2)
- Mobile app (web-responsive trước, native app sau)
- Training cho văn phòng miền Bắc (phase 1 chỉ HCM)
- Data migration cho lịch sử >5 năm

**Assumptions quan trọng cần document:**
- "API của bên thứ 3 (payment gateway) sẽ available và stable"
- "Business requirements sẽ không thay đổi lớn sau sign-off"
- "Team có ít nhất 1 senior dev với kinh nghiệm [framework]"
- "Tất cả licenses cần thiết đã được mua"

**Common mistakes:**
- Out of Scope trống rỗng: Không liệt kê những gì bị loại trừ = scope creep guaranteed
- Assumptions không được document: Khi assumption sai, không ai nhớ đã assume gì
- Constraints không rõ ràng: "Budget linh hoạt" không giúp ích gì cho team

---

## 4. MILESTONES CHÍNH

| # | Milestone | Deliverable | Deadline | Owner | Status |
|---|---|---|---|---|---|
| M1 | Kickoff hoàn thành | Kickoff minutes, Risk Register v1 | DD/MM/YYYY | PM | Pending |
| M2 | Requirements approved | BRD/PRD sign-off | DD/MM/YYYY | BA/PM | Pending |
| M3 | Design approved | UI/UX mockups, Architecture doc | DD/MM/YYYY | Tech Lead | Pending |
| M4 | Development complete | Code deployed to staging | DD/MM/YYYY | Dev Lead | Pending |
| M5 | UAT passed | UAT sign-off document | DD/MM/YYYY | QA/PM | Pending |
| M6 | Go-live | System live, hypercare started | DD/MM/YYYY | PM | Pending |
| M7 | Project closed | Lessons learned, handover complete | DD/MM/YYYY | PM | Pending |

**Hướng dẫn điền:**
- Milestone phải là **sự kiện**, không phải hoạt động: "Requirements approved" (sự kiện), không phải "Writing requirements" (hoạt động)
- Mỗi milestone phải có **deliverable cụ thể** để biết milestone đạt được khi nào
- **Owner** là người chịu trách nhiệm đảm bảo milestone đạt được, không nhất thiết là người làm
- Giữ milestone ở mức **high-level** (5-10 cái). Chi tiết hơn thì dùng WBS/Project Schedule

**Common mistakes:**
- Milestone quá nhiều: Nếu có 20 milestones thì thực ra là task list, không phải milestone
- Không có deliverable: Milestone "Phase 1 complete" không ai biết complete nghĩa là gì
- Không có buffer: Mỗi milestone nên có ít nhất 2-3 ngày buffer trước milestone tiếp theo

---

## 5. NGÂN SÁCH

| Hạng Mục | Estimate | Actual | Variance | Notes |
|---|---|---|---|---|
| Nhân công (X người × Y tháng) | [X triệu] | - | - | Rate: X triệu/người/tháng |
| License/Software | [X triệu] | - | - | Liệt kê cụ thể: Jira, AWS, etc. |
| Infrastructure (Cloud/Server) | [X triệu] | - | - | Monthly cost × duration |
| External Services/API | [X triệu] | - | - | Payment gateway, SMS, etc. |
| Training | [X triệu] | - | - | Bao gồm cả end-user training |
| Travel/Logistics | [X triệu] | - | - | Nếu có multi-site |
| Contingency (10-15%) | [X triệu] | - | - | Reserve cho rủi ro unforeseen |
| **TỔNG** | **[X triệu]** | **-** | **-** | |

**Hướng dẫn điền:**

**Nhân công** thường chiếm 60-70% tổng budget. Tính bằng: (số người) × (số tháng) × (rate/tháng). Nhớ tính cả PM time.

**Contingency** nên là 10% cho dự án well-defined, 15-20% cho dự án có nhiều unknowns. Đây là reserve hợp pháp, không phải "slush fund" — cần có approval process để dùng.

**Common mistakes:**
- Quên tính infrastructure cost ongoing (monthly AWS bill sau go-live)
- Không có contingency — sau đó phải xin thêm budget, mất uy tín với sponsor
- Estimate quá optimistic: Luôn nhân thêm 20-30% cho first estimate

---

## 6. STAKEHOLDERS

| Tên | Chức vụ | Vai trò trong DA | Mức ảnh hưởng | Mong đợi chính | Communication |
|---|---|---|---|---|---|
| [Tên] | [Title] | Sponsor | High | ROI, đúng hạn | Monthly report |
| [Tên] | [Title] | PM | High | Resources, decisions | Daily standup |
| [Tên] | [Title] | Core Team | Medium | Clear requirements | Daily standup |
| [Tên] | [Title] | End User | Medium | Ease of use, training | UAT + training |
| [Tên] | [Title] | IT/Infra | Medium | Security, maintainability | Technical reviews |
| [Tên] | [Title] | Finance | Low | Budget compliance | Monthly report |

**Hướng dẫn điền:**

**Mức ảnh hưởng** (Influence/Interest matrix):
- High influence + High interest = **Manage closely** (Sponsor, key stakeholders)
- High influence + Low interest = **Keep satisfied** (C-level executives)
- Low influence + High interest = **Keep informed** (End users, affected teams)
- Low influence + Low interest = **Monitor** (Compliance, audit)

**Common mistakes:**
- Quên end users — họ sẽ dùng sản phẩm hàng ngày, cần involve sớm
- Không map communication frequency — một stakeholder hay complain "tôi không biết gì cả" = communication gap
- Stakeholder list quá dài: Nếu >15 người, group lại theo role

---

## 7. RỦI RO CHÍNH (Top 5)

| # | Rủi ro | Category | P (1-5) | I (1-5) | Score | Level | Chiến lược | Owner |
|---|---|---|---|---|---|---|---|---|
| R1 | [Mô tả rủi ro] | Technical | | | | H/M/L | Mitigate/Accept/Avoid/Transfer | [Tên] |
| R2 | | Schedule | | | | | | |
| R3 | | Resource | | | | | | |
| R4 | | External | | | | | | |
| R5 | | Stakeholder | | | | | | |

*Score = P × I. Level: 15-25 = High, 8-14 = Medium, 1-7 = Low*

*Xem chi tiết tại Risk Register: `risk-register-template.md`*

**Hướng dẫn điền:**
Top 5 rủi ro cho Project Charter là đủ. Mục tiêu là để sponsor nhận thức về các rủi ro chính, không phải comprehensive risk analysis. Risk Register mới là nơi quản lý đầy đủ.

---

## 8. DEPENDENCIES

**Phụ thuộc vào (Input dependencies) — Dự án này cần cái gì từ nơi khác:**
- [Dự án/Team/Resource cần hoàn thành/cung cấp trước khi dự án này bắt đầu hoặc đạt milestone X]
- Ví dụ: "API design từ team Platform cần sẵn sàng trước 15/03"
- Ví dụ: "Legal approval cho data processing trước khi go-live"

**Được phụ thuộc bởi (Output dependencies) — Dự án/team nào đang chờ output của dự án này:**
- [Dự án/Team sẽ dùng output của dự án này]
- Ví dụ: "Team Mobile App đang chờ API của dự án này để tích hợp"
- Ví dụ: "Marketing campaign Q3 cần feature X go-live trước 01/07"

**Hướng dẫn điền:**
Dependencies là rủi ro ẩn. Khi map dependencies rõ ràng, bạn có thể:
1. Proactively theo dõi external teams
2. Escalate sớm khi có delay upstream
3. Justify deadline với leadership ("nếu trễ hơn X thì team Y bị ảnh hưởng")

---

## 9. PHÊ DUYỆT

| Vai trò | Tên | Chữ ký | Ngày |
|---|---|---|---|
| Project Sponsor | | | |
| Project Manager | | | |
| Key Stakeholder #1 | | | |
| Key Stakeholder #2 | | | |

**Hướng dẫn lấy sign-off:**
1. Gửi draft cho sponsor trước ít nhất 3 ngày
2. Schedule 30-phút review meeting (đừng để họ đọc một mình và im lặng)
3. Walk through từng section, clarify questions
4. Gửi lại version cuối kèm summary những thay đổi so với draft
5. Email confirmation cũng là acceptable nếu không có chữ ký vật lý

---

## Document History

| Version | Ngày | Tác giả | Thay đổi |
|---|---|---|---|
| 1.0 | DD/MM/YYYY | [Tên] | Initial creation |
| 1.1 | DD/MM/YYYY | [Tên] | [Mô tả thay đổi] |

---

## Checklist Trước Khi Submit

- [ ] Tất cả sections đã điền (không còn placeholder text)
- [ ] Số liệu trong Business Case đã được verify
- [ ] Out of Scope đã list ít nhất 3-5 items
- [ ] Budget đã có contingency
- [ ] Top 5 risks đã identify
- [ ] Dependencies đã map
- [ ] Sponsor đã review draft
- [ ] Ngày ký xác nhận là realistic

---

*Document history: v1.0 — Initial creation*
