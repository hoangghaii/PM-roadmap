# Case Study 1: Dự Án Trễ Deadline

**Cấp độ:** Junior PM / Project Coordinator
**Kỹ năng:** Scope management, stakeholder communication, risk escalation, options analysis

---

## Bối Cảnh

Bạn là **Project Coordinator** cho dự án phát triển phần mềm quản lý kho hàng cho một công ty phân phối tại TP.HCM. Đây là dự án đầu tiên bạn được giao làm đầu mối chính.

| Thông tin dự án | Chi tiết |
|---|---|
| Tên dự án | Warehouse Management System (WMS) v2.0 |
| Timeline | 4 tháng (tháng 1 → tháng 4) |
| Budget | 800 triệu VND (cố định) |
| Dev team | 3 Backend + 2 Frontend + 1 QA |
| Khách hàng | Công ty phân phối Minh Phát, 500 nhân viên |
| Contract | Fixed-price, fixed-scope |

**Timeline sự kiện:**

```
Tháng 1    Tháng 2    Tháng 3    Tháng 4
[Analysis] [Dev M1──] [Dev M2──] [UAT──Go-live]
                ↑
           Tuần 8: Khủng hoảng xảy ra
```

**Ngày D+60 (cuối tháng 2):** Team lead báo cáo trong weekly standup: *"Chúng ta cần thêm 6 tuần mới có thể deliver đủ scope."*

---

## Thông Tin Chi Tiết

Sau khi hỏi sâu hơn, bạn phát hiện:

- **Scope thay đổi:** Trong tháng 2, Giám đốc kho của khách hàng (không phải người ký contract) đã trực tiếp yêu cầu developer thêm 3 tính năng mới (barcode scanning integration, real-time dashboard, auto-reorder alerts). Developer đã làm theo vì "khách hàng yêu cầu trực tiếp".
- **Dev team:** Hiện đang ở 110% capacity, 2 người đang làm overtime liên tục 3 tuần.
- **Tác động:** 3 tính năng mới này chiếm ~6 tuần công.
- **Khách hàng:** Phó Giám đốc (người ký contract) không biết về những yêu cầu này và không đồng ý tăng timeline.
- **Budget:** Không có contingency budget.

---

## Câu Hỏi Phân Tích

*Dừng lại và suy nghĩ trước khi đọc hướng giải quyết:*

1. Bạn sẽ làm gì trong **24 giờ đầu tiên**?
2. Bạn sẽ **present vấn đề này** với sponsor/khách hàng như thế nào?
3. Các **options** nào khả thi trong tình huống này?
4. Bạn sẽ **chọn option nào** và tại sao?

---

## Hướng Giải Quyết Từng Bước

### Bước 1: Thu Thập Dữ Liệu (Giờ 1–4)

Trước khi làm bất cứ điều gì, **đừng panic, hãy thu thập facts.**

```
Cần trả lời 5 câu hỏi:
1. Scope change nào đã được thêm vào?
2. Ai yêu cầu? Ai approve? Khi nào?
3. Developer đã làm được bao nhiêu % của scope mới?
4. Nếu dừng scope mới ngay, deliver đúng hạn được không?
5. Có thể cắt scope nào của original mà không ảnh hưởng MVP?
```

**Hành động cụ thể:**
- Họp 1-on-1 với team lead để hiểu chi tiết
- Pull git history, Jira tickets xem scope change khi nào
- Review original contract và scope document
- Đừng blame developer ngay — họ làm theo chỉ đạo trực tiếp từ khách hàng

### Bước 2: Phân Tích Options (Giờ 4–8)

| Option | Mô tả | Pros | Cons | Feasibility |
|---|---|---|---|---|
| **A — Cắt scope mới** | Loại 3 tính năng mới khỏi scope, deliver original scope đúng hạn | Giữ deadline, không tăng cost | 3 tính năng bị delay | Cao ✅ |
| **B — Tăng timeline** | Gia hạn 6 tuần để deliver đủ tất cả | Full delivery | Khách hàng không đồng ý ban đầu | Trung bình ⚠️ |
| **C — Tăng resource** | Thêm 2 dev trong 6 tuần (~60 triệu VND) | Có thể recover một phần | Ramping time 2 tuần, tốn tiền, ai trả? | Thấp ❌ |
| **D — Hybrid** | Deliver core + 1 tính năng mới đúng hạn, 2 tính năng còn lại Phase 2 | Compromise | Cần đàm phán kỹ | Cao ✅ |

### Bước 3: Chuẩn Bị Communication (Giờ 8–24)

**Email thông báo rủi ro cho Sponsor (template):**

```
Subject: [WMS Project] Risk Alert — Scope Change Impact Analysis

Kính gửi Anh/Chị [Tên Sponsor],

Trong quá trình review tiến độ tuần này, tôi phát hiện một tình huống 
cần được escalate và quyết định ngay.

VẤN ĐỀ: Trong tháng 2, phía team kỹ thuật đã nhận một số yêu cầu thêm 
tính năng từ phía vận hành kho của quý công ty mà chưa qua change 
request process. Tổng effort ước tính: +6 tuần.

IMPACT: Nếu không xử lý, dự án sẽ trễ đến [ngày mới] hoặc vượt budget.

TÔI ĐỀ XUẤT: Họp khẩn trong 24h để review options và quyết định hướng đi.

Tôi đã chuẩn bị 3 options với pros/cons. Thời gian nào thuận tiện cho 
Anh/Chị?

Trân trọng,
[Tên PM]
```

### Bước 4: Meeting Với Sponsor (Ngày 2)

**Agenda 30 phút:**
1. Present facts (không blame ai) — 5 phút
2. Present 3 options với impact rõ ràng — 10 phút
3. Đề xuất recommendation của PM — 5 phút
4. Q&A và quyết định — 10 phút

**Nguyên tắc present:**
- Dùng **số liệu**, không dùng cảm tính
- Present options, không chỉ present vấn đề
- Có **recommendation rõ ràng** — sponsor trả tiền để PM quyết định, không chỉ liệt kê options

### Bước 5: Document Quyết Định

Dù chọn option nào, **phải document bằng văn bản:**

```
1. Change Request Form cho 3 tính năng mới
   - Nếu approve → project plan update
   - Nếu reject → formal rejection documented
   
2. Meeting minutes có chữ ký/email confirm

3. Thông báo cho toàn team về quyết định

4. Cập nhật Risk Register
```

---

## Bài Học Quan Trọng

### 1. Scope Baseline Là Bất Khả Xâm Phạm
Mọi thay đổi scope — dù nhỏ — phải qua change request process. **"Khách hàng yêu cầu trực tiếp"** không phải lý do hợp lệ để bypass process.

**Action cho PM:** Ngay từ kickoff, phải communicate rõ với cả team và khách hàng: *"Mọi yêu cầu thay đổi đều phải qua PM. Developer không được tự ý nhận thêm việc từ stakeholder."*

### 2. Early Warning Signs Bị Bỏ Qua

Nhìn lại, có những dấu hiệu đáng lẽ phải phát hiện sớm hơn:
- Developer overtime liên tục từ tuần 5
- Daily standup không có blockers gì (suspicious — thực ra có nhưng không báo)
- Velocity giảm dần trong tháng 2

**Action cho PM:** Review burndown chart hàng tuần, không chỉ nghe báo cáo lời.

### 3. PM Không Phải "Người Mang Tin Xấu"
Khi report vấn đề lên sponsor, PM phải **mang theo solutions**, không chỉ mang theo vấn đề. Đây là sự khác biệt giữa PM và coordinator.

### 4. Relationship với Khách Hàng Quan Trọng Hơn Khi "Đúng"
Kể cả khi rõ ràng là lỗi của phía khách hàng (họ bypass process), PM vẫn phải xử lý tình huống một cách collaborative. Đây không phải tòa án — đây là mối quan hệ dài hạn.

---

## Kỹ Năng PM Được Rèn Luyện

- **Stakeholder communication** khi có bad news
- **Options analysis** và recommendation
- **Scope management** và change control
- **Risk escalation** đúng thời điểm và cách thức

---

## Câu Hỏi Reflection

1. Nếu bạn là PM từ đầu dự án, bạn sẽ setup quy trình nào để tránh tình huống này xảy ra?
2. Trong cuộc họp với sponsor, nếu họ blame dev team trực tiếp, bạn xử lý thế nào?
3. Nếu khách hàng insist muốn cả 3 tính năng mới **và** giữ deadline **và** không tăng budget — bạn làm gì?
4. Làm thế nào để xây dựng trust với developer để họ báo cáo vấn đề sớm hơn?
