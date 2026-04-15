# WBS Template

## Cách Sử Dụng

1. Bắt đầu từ Project Name (level 0)
2. Phân rã thành Deliverables lớn (level 1)
3. Phân rã thành Sub-deliverables (level 2)
4. Phân rã thành Work Packages (level 3) — mỗi package ≤ 8 giờ

---

## Template Blank

```markdown
# WBS: [Tên Dự Án]

**PM:** [Tên] | **Date:** DD/MM/YYYY | **Version:** 1.0

---

## 1. [Deliverable Chính 1]

### 1.1 [Sub-deliverable]
| ID | Work Package | Effort | Owner | Dependencies | Notes |
|---|---|---|---|---|---|
| 1.1.1 | [Tên work package] | [X ngày] | [Tên] | None | |
| 1.1.2 | [Tên work package] | [X ngày] | [Tên] | 1.1.1 | |

### 1.2 [Sub-deliverable]
| ID | Work Package | Effort | Owner | Dependencies | Notes |
|---|---|---|---|---|---|
| 1.2.1 | | | | | |

---

## 2. [Deliverable Chính 2]

### 2.1 [Sub-deliverable]
...

---

## Tổng Hợp Effort

| Deliverable | Total Effort | Owner | Start | End |
|---|---|---|---|---|
| 1. [Tên] | [X ngày] | | | |
| 2. [Tên] | [X ngày] | | | |
| **TOTAL** | **[X ngày]** | | | |
```

---

## Ví Dụ Hoàn Chỉnh: Web Application E-commerce

```
WBS: E-Commerce Platform Development
PM: Nguyễn Thị B | Date: 01/02/2026 | Duration: 4 tháng

1. Project Management
   1.1 Initiation
       1.1.1 Project Charter (1 ngày)
       1.1.2 Stakeholder Register (0.5 ngày)
   1.2 Planning
       1.2.1 Project Plan (2 ngày)
       1.2.2 Risk Register (1 ngày)
   1.3 Execution Management
       1.3.1 Weekly Status Reports (0.5 ngày/tuần × 16 tuần = 8 ngày)
       1.3.2 Sprint Reviews facilitation (1 ngày/sprint × 8 = 8 ngày)

2. Requirements & Design
   2.1 Business Analysis
       2.1.1 Stakeholder interviews (3 ngày)
       2.1.2 User Stories creation (3 ngày)
       2.1.3 Acceptance Criteria definition (2 ngày)
   2.2 UX/UI Design
       2.2.1 Wireframes (5 ngày)
       2.2.2 UI Design (hi-fi mockups) (7 ngày)
       2.2.3 Design review và sign-off (1 ngày)

3. Development
   3.1 Frontend
       3.1.1 Setup React project + CI/CD (1 ngày)
       3.1.2 Product catalog pages (5 ngày)
       3.1.3 Shopping cart (3 ngày)
       3.1.4 Checkout flow (4 ngày)
       3.1.5 User authentication (3 ngày)
       3.1.6 Admin dashboard (5 ngày)
   3.2 Backend
       3.2.1 Database design (2 ngày)
       3.2.2 API development (product, cart, order) (10 ngày)
       3.2.3 Payment integration (VNPay/Momo) (5 ngày)
       3.2.4 Notification service (email/SMS) (3 ngày)
   3.3 Infrastructure
       3.3.1 AWS setup (EC2, RDS, S3, CDN) (2 ngày)
       3.3.2 Docker + deployment pipeline (2 ngày)

4. Testing
   4.1 QA Testing
       4.1.1 Test plan creation (2 ngày)
       4.1.2 Functional testing (8 ngày)
       4.1.3 Performance testing (2 ngày)
       4.1.4 Security testing (2 ngày)
   4.2 User Acceptance Testing
       4.2.1 UAT preparation (1 ngày)
       4.2.2 UAT execution với client (5 ngày)
       4.2.3 Bug fixing (UAT round 1) (4 ngày)
       4.2.4 UAT sign-off (1 ngày)

5. Launch & Handover
   5.1 Go-Live
       5.1.1 Production deployment (1 ngày)
       5.1.2 DNS và SSL setup (0.5 ngày)
       5.1.3 Smoke testing (1 ngày)
   5.2 Hypercare (2 tuần sau go-live)
       5.2.1 Monitoring và bug fix (5 ngày)
   5.3 Handover
       5.3.1 Technical documentation (3 ngày)
       5.3.2 Operations runbook (2 ngày)
       5.3.3 Training cho client team (2 ngày)
       5.3.4 Project closure report (1 ngày)
```

---

## WBS Dictionary (cho mỗi work package quan trọng)

| Field | Chi Tiết |
|---|---|
| **WBS ID** | 3.2.3 |
| **Tên** | Payment Integration (VNPay/Momo) |
| **Mô tả** | Tích hợp payment gateway VNPay và MoMo vào checkout flow |
| **Deliverable** | Working payment flow với test transactions |
| **Owner** | Backend Developer (Tên) |
| **Effort** | 5 ngày |
| **Dependencies** | 3.2.2 (API development) phải xong trước |
| **Acceptance Criteria** | - Test transaction thành công với cả 2 gateways \| - Refund flow hoạt động \| - Error handling (timeout, insufficient funds) tested |
| **Resources** | 1 Backend Developer + VNPay sandbox account |
| **Risk** | VNPay API có thể thay đổi → Kiểm tra trước khi bắt đầu |
