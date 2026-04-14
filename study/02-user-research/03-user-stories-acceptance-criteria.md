# User Stories & Acceptance Criteria

## User Story là Gì?

User story là cách ngắn gọn để mô tả một requirement từ góc độ người dùng. Nó focus vào **value** mà user nhận được, không phải technical implementation.

---

## Format Chuẩn

```
As a [type of user],
I want [to do something],
So that [I can achieve some goal/benefit].
```

**Ví dụ tốt:**
> As a merchant selling online,
> I want to upload multiple orders at once via CSV file,
> So that I can save 2 hours of manual data entry every morning.

**Ví dụ xấu:**
> As a user, I want a button to upload CSV file.

*Tại sao xấu? Không nói "so that" — không rõ value, không giúp team hiểu priority.*

---

## INVEST Criteria

User story tốt phải satisfy INVEST:

| Chữ | Ý Nghĩa | Ví Dụ |
|-----|---------|-------|
| **I**ndependent | Có thể develop/deploy riêng lẻ | Story không phụ thuộc vào story khác |
| **N**egotiable | Không phải contract cứng nhắc | Scope có thể thương lượng |
| **V**aluable | Deliver value cho user/business | Rõ ràng benefit |
| **E**stimable | Team có thể estimate effort | Đủ clear để estimate |
| **S**mall | Fit trong 1 sprint | < 1 tuần để build |
| **T**estable | Có thể verify khi done | Acceptance criteria clear |

---

## Acceptance Criteria - BDD Format

BDD (Behavior-Driven Development) dùng **Given/When/Then**:

```
Given [context/precondition],
When [action],
Then [expected outcome].
```

**Ví dụ — CSV Upload Feature:**

```
Scenario 1: Successful upload
Given tôi là merchant đã đăng nhập
  And tôi có file CSV đúng format với 50 orders
When tôi click "Upload CSV" và chọn file
Then 50 orders được tạo trong hệ thống
  And tôi nhận confirmation "50 orders imported successfully"
  And orders xuất hiện trong dashboard ngay lập tức

Scenario 2: File format error
Given tôi upload file .xlsx thay vì .csv
When hệ thống kiểm tra file
Then hệ thống show error "Only CSV files are supported"
  And không có orders nào được tạo
  And file bị rejected

Scenario 3: Partial failure
Given CSV có 50 rows, nhưng 3 rows có địa chỉ thiếu
When upload được process
Then 47 orders được tạo thành công
  And tôi nhận warning "3 orders failed - see details"
  And có thể download error report với specific rows + reasons
```

---

## Epic → Feature → Story → Task

```
Epic: Merchant Order Management
  └── Feature: Bulk Order Import
        ├── Story 1: Upload CSV file
        │     ├── Task: Build CSV parser service
        │     ├── Task: Build validation engine
        │     └── Task: Build success/error UI
        ├── Story 2: Preview before import
        └── Story 3: Download error report
```

**Epic:** Lớn, có thể kéo dài nhiều sprints (1-3 tháng)
**Feature:** Medium, 1-4 sprints
**Story:** Small, fit trong 1 sprint (< 5 ngày)
**Task:** Technical, sub-parts của story

---

## Story Splitting Techniques

Khi story quá lớn, split theo:

1. **Workflow steps:** "Merchant can see preview" tách thành "View order list" + "View error list"
2. **User types:** "Admin và merchant can import" → tách thành 2 stories
3. **Happy path first:** Build core happy path trước, edge cases sau
4. **CRUD:** Create, Read, Update, Delete — mỗi cái là 1 story
5. **Data variations:** Simple data trước, complex data sau

---

## Definition of Done (DoD)

DoD là checklist mà tất cả stories phải meet trước khi đánh dấu "done":

```
✅ Code written và passes code review
✅ Unit tests written với >80% coverage
✅ Acceptance criteria verified
✅ QA sign-off
✅ No critical bugs
✅ Documentation updated (nếu cần)
✅ Feature flag configured (nếu phased rollout)
✅ Analytics events tracked
✅ PM acceptance
```

---

## 10 User Stories Cho Tính Năng "Track Shipment"

```
Story 1 (Core happy path):
As a recipient waiting for package,
I want to see my shipment's current location on a map,
So that I can estimate when it will arrive and plan my day.

Acceptance criteria:
- Given: Order đã được picked up
- When: Tôi mở tracking page
- Then: Thấy real-time map với driver location
- Then: ETA được hiển thị (±10 phút accuracy)
- Then: Map tự refresh mỗi 30 giây

Story 2 (Notifications):
As a recipient,
I want to receive a push notification when driver is 10 minutes away,
So that I can be ready to receive the package.

Story 3 (SMS fallback):
As a recipient without smartphone,
I want to receive SMS updates about my shipment status,
So that I can stay informed without needing the app.

Story 4 (No internet):
As a recipient in area with poor connectivity,
I want to see last known driver location even offline,
So that I still have some information about delivery status.

Story 5 (Delivery photo):
As a recipient who missed delivery,
I want to see photo proof of where package was left,
So that I can find my package.

Story 6 (Contact driver):
As a recipient,
I want to contact driver through the app (masked number),
So that I can communicate without revealing personal numbers.

Story 7 (Delivery instructions):
As a recipient living in complex/apartment,
I want to add delivery instructions to my order,
So that driver can find me easily.

Story 8 (Multiple packages):
As a recipient with multiple pending orders,
I want to track all packages in one view,
So that I don't have to check each order separately.

Story 9 (Delivery history):
As a recipient,
I want to see history of past deliveries,
So that I can verify what was delivered and when.

Story 10 (Rating driver):
As a recipient after successful delivery,
I want to rate my delivery experience,
So that good drivers are rewarded and service quality improves.
```
