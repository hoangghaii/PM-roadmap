# Case Study 4: Program Manager Xử Lý Dependencies

**Cấp độ:** Senior PM / Program Manager
**Kỹ năng:** Program management, dependency management, schedule recovery, cascade impact analysis

---

## Bối Cảnh

Bạn là **Program Manager** cho chương trình "Chuyển đổi số" của một công ty logistics 300 nhân viên tại Hà Nội. Chương trình gồm 3 dự án liên quan:

| Dự án | Mô tả | Duration | PM | Status |
|---|---|---|---|---|
| **A: Backend Migration** | Migrate monolith sang microservices + API gateway | 6 tháng | Minh | Đang chạy |
| **B: Mobile App** | App cho tài xế và dispatcher, consume API từ A | 4 tháng | Lan | Chưa bắt đầu |
| **C: User Training** | Training toàn bộ nhân viên dùng hệ thống mới | 1 tháng | Hoa | Chưa bắt đầu |

### Dependency Map

```
Tháng:  1    2    3    4    5    6    7    8    9    10   11
        
[A: Backend Migration ─────────────────────────]
                                  ↑ API stable (W10)
                                  └──────────[B: Mobile App ──────────]
                                                              ↑ App ready
                                                              └──[C: Training]

Go-live: Tháng 11
```

**Dependency chi tiết:**
- **B phụ thuộc A:** Mobile App cần API Gateway từ Backend stable (khoảng tuần 10 của A)
- **C phụ thuộc A và B:** Training cần cả hệ thống backend lẫn app hoàn chỉnh

---

## Vấn Đề

**Tuần 8 của Dự án A:** PM Minh báo cáo trong Program Status Meeting:

*"Team gặp khó khăn với data migration từ legacy Oracle sang PostgreSQL. Estimated: cần thêm 3 tuần. API Gateway sẽ stable vào tuần 13 thay vì tuần 10."*

---

## Câu Hỏi Phân Tích

1. Cascade impact đến B và C là gì?
2. Có cách nào giảm thiểu impact không?
3. Bạn communicate với sponsor như thế nào?

---

## Cascade Impact Analysis

```
A trễ 3 tuần (API ready: W13 thay vì W10)
          ↓
B bắt đầu muộn 3 tuần → B kết thúc muộn 3 tuần
          ↓
C bắt đầu muộn 3 tuần → C kết thúc muộn 3 tuần
          ↓
Program Go-live: Tháng 11+3 tuần = Tháng 11 cuối (thay vì đầu)
```

**Impact chi tiết:**

| Dự án | Original End | New End | Delay | Business Impact |
|---|---|---|---|---|
| A | Tháng 6 cuối | Tháng 7 W3 | +3 tuần | API ready trễ |
| B | Tháng 10 | Tháng 11 W1 | +3 tuần | App deploy trễ |
| C | Tháng 11 W1 | Tháng 11 cuối | +3 tuần | Training trễ |
| Go-live | Tháng 11 W1 | Tháng 11 cuối | +3 tuần | Revenue impact |

---

## Hướng Xử Lý

### Option 1: Fast-Tracking — Overlap Activities

**Câu hỏi:** Có phần nào của B không phụ thuộc API của A không?

**Phân tích:**
```
B: Mobile App — breakdown của 4 tháng:
├── M1: UI Design + Architecture (không cần API)     ← B có thể bắt đầu ngay!
├── M2: Frontend Development với mock API             ← B có thể dùng mock API
├── M3: Integration với real API từ A                 ← Cần API stable từ A
└── M4: Testing + Bug fixing

→ B có thể bắt đầu tháng 1 hoặc 2, không cần đợi API ready
→ Khi A có API (W13), B đã hoàn thành M1+M2, chỉ cần M3+M4
→ Total delay thực sự: 0-1 tuần thay vì 3 tuần
```

**Kết quả fast-tracking:**
- B bắt đầu ngay (tháng 2-3 với mock API)
- B integration phase bắt đầu W13 (khi A ready)
- B kết thúc: chỉ trễ 0-1 tuần so với kế hoạch gốc

### Option 2: Crashing Project A

**Câu hỏi:** Thêm resource có giúp A recover 3 tuần không?

**Phân tích:**
```
Vấn đề: Data migration Oracle → PostgreSQL
Nguyên nhân: Schema complexity, data quality issues

Crashing options:
- Thêm 1 DBA chuyên PostgreSQL: +80 triệu, recover 1-2 tuần
- Mua tool ETL chuyên dụng: +30 triệu, recover 1 tuần
- Outsource data migration task: +100 triệu, recover 2 tuần

Brooks' Law caveat: "Adding manpower to a late project makes it later"
→ Crashing chỉ hiệu quả với tasks có thể parallel hóa
→ Data migration có thể parallel (by module/table group)
→ Crashing khả thi cho A, recover 1.5-2 tuần
```

### Recommendation của Program Manager

**Kết hợp 2 options:**

```
1. B bắt đầu ngay (fast-track M1+M2 với mock API)
   → Impact: B bắt đầu tuần này, không đợi A

2. Crash A với ETL tool (30 triệu)
   → Impact: A trễ 1.5 tuần thay vì 3 tuần

3. Kết quả:
   → B delay: 0-1 tuần
   → Go-live delay: 1-1.5 tuần (vs 3 tuần nếu không làm gì)
   → Extra cost: 30 triệu (vs delay cost >>30 triệu)
```

---

## Communication với Sponsor

### Email Thông Báo (Template)

```
Subject: [Program Chuyển Đổi Số] Risk Alert + Recovery Plan — Action Required

Kính gửi Giám Đốc [Tên],

TÓM TẮT: Dự án Backend (A) gặp delay 3 tuần do data migration phức tạp. 
Chúng tôi đã phân tích impact và có recovery plan để minimize impact 
xuống còn 1-1.5 tuần.

SITUATION:
- Project A (Backend): Cần thêm 3 tuần → API ready W13 (vs W10 kế hoạch)
- Without action: Go-live delay 3 tuần

OUR RECOVERY PLAN:
1. Start Project B ngay với mock API (0 chi phí thêm)
2. Add ETL tool để accelerate data migration (+30 triệu VND)
→ Result: Go-live delay còn 1-1.5 tuần

DECISION NEEDED:
Phê duyệt ngân sách thêm 30 triệu VND cho ETL tool trong 48 giờ.

Tôi đã chuẩn bị 15-phút briefing nếu Giám Đốc muốn review chi tiết.
Availability hôm nay từ 2-5pm.

Trân trọng,
[Tên Program Manager]
```

---

## Dependency Types — Lý Thuyết

| Type | Ký hiệu | Mô tả | Ví dụ |
|---|---|---|---|
| **Finish-to-Start** | FS | B không bắt đầu được cho đến khi A xong | Code review xong mới deploy |
| **Start-to-Start** | SS | B không bắt đầu được cho đến khi A bắt đầu | Testing bắt đầu cùng development |
| **Finish-to-Finish** | FF | B không xong được cho đến khi A xong | Documentation xong cùng code |
| **Start-to-Finish** | SF | B không xong được cho đến khi A bắt đầu | Hiếm, legacy system support |

---

## Schedule Compression Techniques

### Crashing vs Fast-Tracking

| | Crashing | Fast-Tracking |
|---|---|---|
| **Phương pháp** | Thêm resource vào critical path | Overlap activities vốn tuần tự |
| **Cost** | Tăng (thêm người/tool) | Không tăng nhiều |
| **Risk** | Thấp (nếu task parallelizable) | Cao hơn (rework nếu A thay đổi) |
| **Khi dùng** | Task có thể chia nhỏ song song | Tasks không phụ thuộc hoàn toàn |
| **Ví dụ** | Thêm 2 dev cho module trễ | B bắt đầu UI trong khi A đang làm API |

---

## Dependency Matrix Template

Công cụ để track dependencies giữa các dự án trong program:

| | **Project A** | **Project B** | **Project C** |
|---|---|---|---|
| **Project A** | — | A → B (API, W10) | A → C (Backend stable) |
| **Project B** | — | — | B → C (App stable) |
| **Project C** | — | — | — |

**Legend:**
- `X → Y (deliverable, deadline)`: X phải deliver [deliverable] trước [deadline] để Y tiến hành

---

## Lessons Learned

1. **Buffer time trong program schedule** là bắt buộc, không phải nice-to-have. Rule: Add 20% buffer vào critical path.

2. **Fast-tracking cần mock API strategy:** Dự án B có thể bắt đầu sớm hơn nhiều nếu có mock API/contract first approach từ đầu.

3. **Identify dependencies TRƯỚC khi lập schedule**, không phải sau khi vấn đề xảy ra.

4. **Communication proactive** — không đợi sponsor hỏi mới báo, báo trước khi họ phát hiện.

5. **Program Manager phải hiểu technical** ở mức đủ để đánh giá "có thể fast-track không?" — đây là giá trị của Technical PM background.

---

## Câu Hỏi Reflection

1. Nếu sponsor từ chối thêm 30 triệu cho ETL tool, bạn có options nào khác?
2. Làm thế nào để setup dependency tracking trong Jira cho 3 dự án song song?
3. Nếu tất cả 3 options đều không work và phải delay 3 tuần — bạn communicate với khách hàng cuối như thế nào?
