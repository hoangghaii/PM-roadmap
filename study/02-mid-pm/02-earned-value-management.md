# Earned Value Management (EVM)

> **Cấp độ:** Mid PM (2–5 năm)
> **Thời gian học:** 1 tuần lý thuyết + 1 tuần thực hành
> **Áp dụng ngay:** Thêm EVM tracking vào dự án đang chạy

---

## 1. EVM Là Gì và Tại Sao Quan Trọng Hơn "% Complete"

### Vấn Đề Với "Percent Complete"

Cuộc họp status report điển hình:
> PM hỏi: "Task này xong bao nhiêu rồi?"
> Dev trả lời: "75% rồi anh ơi."

Câu hỏi: 75% đó có nghĩa là gì? Còn bao lâu nữa xong? Đang trên hay dưới budget?

**"Percent complete" không trả lời được:**
- Chúng ta đang on track hay behind schedule?
- Chúng ta đang over hay under budget?
- Cuối dự án sẽ tốn bao nhiêu?
- Nếu tiếp tục như hiện tại, có xong đúng hạn không?

### EVM Giải Quyết Vấn Đề Này

EVM (Earned Value Management) là phương pháp đo lường hiệu suất dự án bằng cách **tích hợp ba chiều đo**: Scope + Time + Cost vào một hệ thống thống nhất.

Thay vì hỏi "xong bao nhiêu %", EVM hỏi:
- **Chúng ta đã chi bao nhiêu?** (Actual Cost)
- **Chúng ta đáng lẽ chi bao nhiêu ở thời điểm này?** (Planned Value)
- **Chúng ta thực sự làm được bao nhiêu công việc?** (Earned Value)

---

## 2. Ba Chỉ Số Cốt Lõi

### PV — Planned Value (Giá Trị Kế Hoạch)
**Định nghĩa:** Ngân sách được phê duyệt cho công việc theo kế hoạch đến thời điểm đo.

**Công thức:** `PV = % Planned × BAC`

Ví dụ: Dự án 100 triệu VND, 10 tuần. Đến tuần 5 theo kế hoạch phải hoàn thành 50% → PV = 50 triệu.

### EV — Earned Value (Giá Trị Kiếm Được)
**Định nghĩa:** Ngân sách được phê duyệt cho công việc ĐÃ hoàn thành thực tế.

**Công thức:** `EV = % Actual Complete × BAC`

Ví dụ: Đến tuần 5, thực tế chỉ hoàn thành 40% → EV = 40 triệu.

### AC — Actual Cost (Chi Phí Thực Tế)
**Định nghĩa:** Tổng chi phí thực tế đã bỏ ra đến thời điểm đo.

Ví dụ: Đến tuần 5, thực tế đã chi 55 triệu → AC = 55 triệu.

---

## 3. Các Chỉ Số Tính Toán Đầy Đủ

### Variance (Độ Lệch)

**CV — Cost Variance (Độ Lệch Chi Phí)**
```
CV = EV - AC
```
- CV > 0: Under budget (tốt)
- CV < 0: Over budget (xấu)
- CV = 0: Đúng ngân sách

**SV — Schedule Variance (Độ Lệch Tiến Độ)**
```
SV = EV - PV
```
- SV > 0: Ahead of schedule (tốt)
- SV < 0: Behind schedule (xấu)
- SV = 0: Đúng tiến độ

### Performance Indexes (Chỉ Số Hiệu Suất)

**CPI — Cost Performance Index**
```
CPI = EV / AC
```
- CPI > 1.0: Hiệu quả — mỗi đồng chi ra tạo ra hơn 1 đồng giá trị
- CPI = 1.0: Đúng kế hoạch
- CPI < 1.0: Không hiệu quả — mỗi đồng chi ra tạo ra ít hơn 1 đồng giá trị
- **Cảnh báo:** CPI < 0.8 → cần escalate ngay

**SPI — Schedule Performance Index**
```
SPI = EV / PV
```
- SPI > 1.0: Ahead of schedule
- SPI = 1.0: Đúng tiến độ
- SPI < 1.0: Behind schedule
- **Cảnh báo:** SPI < 0.8 → cần action plan ngay

### Forecasting (Dự Báo)

**EAC — Estimate at Completion (Ước Tính Tổng Chi Phí Khi Hoàn Thành)**

Có 3 công thức tùy tình huống:
```
EAC = BAC / CPI                    (nếu xu hướng hiện tại tiếp tục)
EAC = AC + (BAC - EV)              (nếu variance là one-time, sẽ không lặp lại)
EAC = AC + (BAC - EV) / CPI        (nếu cả cost và schedule đều ảnh hưởng)
```
Công thức phổ biến nhất trong thực tế: `EAC = BAC / CPI`

**ETC — Estimate to Complete (Ước Tính Chi Phí Còn Lại)**
```
ETC = EAC - AC
```

**VAC — Variance at Completion (Độ Lệch Khi Hoàn Thành)**
```
VAC = BAC - EAC
```
- VAC > 0: Sẽ under budget
- VAC < 0: Sẽ over budget → báo cáo ngay cho sponsor

**TCPI — To-Complete Performance Index**
```
TCPI = (BAC - EV) / (BAC - AC)
```
TCPI cho biết: **từ giờ trở đi**, mỗi đồng bỏ ra phải tạo ra bao nhiêu giá trị để hoàn thành đúng ngân sách.
- TCPI > 1.1: Gần như không thể đạt được — cần revise budget hoặc scope
- TCPI ≤ 1.0: Realistic

---

## 4. Ví Dụ Thực Tế 1: Dự Án 100 Triệu VND

**Bối cảnh:** Dự án xây dựng website e-commerce cho công ty bán lẻ.
- BAC = 100 triệu VND
- Duration = 10 tuần
- Review vào cuối tuần 5

**Dữ liệu đo tại tuần 5:**
- Theo kế hoạch, phải hoàn thành 50% → **PV = 50 triệu**
- Thực tế hoàn thành 40% → **EV = 40 triệu**
- Thực tế đã chi → **AC = 55 triệu**

**Tính toán:**

| Chỉ số | Công thức | Kết quả | Diễn giải |
|---|---|---|---|
| CV | EV - AC = 40 - 55 | **-15 triệu** | Over budget 15 triệu |
| SV | EV - PV = 40 - 50 | **-10 triệu** | Behind schedule tương đương 10 triệu |
| CPI | EV / AC = 40 / 55 | **0.73** | Mỗi 1 đồng chi ra chỉ tạo 0.73 đồng giá trị |
| SPI | EV / PV = 40 / 50 | **0.80** | Chỉ đạt 80% tốc độ kế hoạch |
| EAC | BAC / CPI = 100 / 0.73 | **137 triệu** | Dự báo sẽ tốn 137 triệu (vượt 37%) |
| ETC | EAC - AC = 137 - 55 | **82 triệu** | Cần thêm 82 triệu để hoàn thành |
| VAC | BAC - EAC = 100 - 137 | **-37 triệu** | Sẽ vượt ngân sách 37 triệu |
| TCPI | (100-40)/(100-55) = 60/45 | **1.33** | Cần hiệu suất 133% từ giờ — gần như bất khả thi |

**Kết luận PM phải làm:** Escalate ngay. Dự án đang nghiêm trọng — vừa behind schedule, vừa over budget. Cần họp với sponsor trong 24h để trình bày 3 options: (1) tăng budget, (2) cắt scope, (3) kéo dài deadline.

---

## 5. Ví Dụ Thực Tế 2: Dự Án 500 Triệu VND (Bài Tập 3)

**Bối cảnh:** Dự án triển khai phần mềm quản lý vận tải cho công ty logistics.
- BAC = 500 triệu VND
- Duration = 20 tuần
- Review vào cuối tuần 10

**Dữ liệu:**
- PV = 250 triệu (50% planned done)
- EV = 210 triệu (42% actual complete)
- AC = 280 triệu (đã chi)

**Tính toán đầy đủ:**

| Chỉ số | Kết quả | Diễn giải |
|---|---|---|
| CV = EV - AC | **-70 triệu** | Over budget 70 triệu |
| SV = EV - PV | **-40 triệu** | Behind schedule tương đương 40 triệu |
| CPI = EV/AC | **0.75** | Rất đáng lo — mỗi đồng chỉ tạo 0.75 giá trị |
| SPI = EV/PV | **0.84** | Chỉ đạt 84% tốc độ |
| EAC = BAC/CPI | **667 triệu** | Dự báo tổng chi phí sẽ là 667 triệu |
| ETC = EAC-AC | **387 triệu** | Cần thêm 387 triệu để hoàn thành |
| VAC = BAC-EAC | **-167 triệu** | Sẽ over budget 167 triệu (33% vượt) |
| TCPI | (500-210)/(500-280) = 290/220 | **1.32** | Cần tăng hiệu suất 32% từ giờ |

**Dashboard tóm tắt:**
```
┌────────────────────────────────────────────────────────────┐
│  DỰ ÁN LOGISTICS TMS — EVM DASHBOARD — TUẦN 10/20         │
├───────────────┬────────────────────────────────────────────┤
│ Ngân sách gốc │ 500 triệu VND                              │
│ Đã chi (AC)   │ 280 triệu VND  ▓▓▓▓▓▓▓▓▓▓▓▓░░░░░░░  56%  │
│ Kế hoạch (PV) │ 250 triệu VND  ▓▓▓▓▓▓▓▓▓▓░░░░░░░░░  50%  │
│ Thực tế (EV)  │ 210 triệu VND  ▓▓▓▓▓▓▓▓░░░░░░░░░░░  42%  │
├───────────────┼────────────────────────────────────────────┤
│ CPI           │ 0.75  ⚠ CẢNH BÁO — Under 0.8              │
│ SPI           │ 0.84  ⚠ Cần chú ý                         │
│ EAC (dự báo)  │ 667 triệu VND — Vượt 167 triệu (+33%)     │
├───────────────┼────────────────────────────────────────────┤
│ TÌNH TRẠNG    │ 🔴 NGHIÊM TRỌNG — Cần escalate ngay       │
└───────────────┴────────────────────────────────────────────┘
```

---

## 6. Cách Đọc EVM Dashboard

### Nguyên Tắc Đọc Nhanh

```
Nếu đường EV nằm dưới PV  → Behind schedule
Nếu đường EV nằm dưới AC  → Over budget
Nếu EV nằm dưới cả PV và AC → Tình huống tệ nhất (vừa trễ vừa tốn)
```

### Biểu Đồ S-Curve (ASCII)
```
Triệu VND
  500 │                                        ╱ BAC
      │                              ╱────────╱
  400 │                    ╱────────╱  PV
      │          ╱────────╱
  300 │ ╱───────╱
      │╱       ← Đây là lý tưởng (EV ≈ PV)
  280 │·····AC (thực tế đã chi nhiều hơn)
  250 │─────PV (kế hoạch đến tuần 10)
  210 │·····EV (thực tế làm được đến tuần 10)
      │
    0 └────────────────────────────────────
      0    5    10   15   20    Tuần
           ↑
     Điểm đo hiện tại
```

**Đọc:** Tại tuần 10, AC > PV > EV = vừa chậm vừa tốn → Red flag.

---

## 7. EVM Trong Agile

Agile không dùng EVM theo nghĩa truyền thống, nhưng có các tương đương:

| EVM Truyền Thống | Agile Tương Đương |
|---|---|
| PV (Planned Value) | Story Points theo kế hoạch sprint |
| EV (Earned Value) | Story Points hoàn thành (Done = Demo) |
| AC (Actual Cost) | Actual hours / cost spent |
| CPI | Story Points done / Cost → Cost per story point |
| SPI | Velocity thực tế / Velocity kế hoạch |
| EAC | Remaining story points / velocity → estimate finish date |
| Burndown chart | Phiên bản đơn giản của SV tracking |

**Burnup Chart** tốt hơn Burndown vì hiển thị cả scope thay đổi:
```
Story Points
  100 │────────────── Total Scope (có thể tăng)
      │         ╱╱╱╱╱ Completed
   60 │    ╱╱╱╱╱
      │╱╱╱╱
    0 └─────────────────────────
      Sprint: 1  2  3  4  5  6
```

---

## 8. Reporting EVM Cho Stakeholders

**Nguyên tắc:** Stakeholders không muốn thấy số — họ muốn thấy **tình trạng và quyết định cần làm**.

### Template Executive Report (1 trang)

```
DỰ ÁN: [Tên] — BÁO CÁO THÁNG [X]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

TÌNH TRẠNG TỔNG THỂ: 🔴 AT RISK / 🟡 CAUTION / 🟢 ON TRACK

TIẾN ĐỘ: [X]% hoàn thành, kế hoạch [Y]%
NGÂN SÁCH: Đã dùng [X]M, dự báo khi hoàn thành [Y]M (ngân sách gốc [Z]M)

TÓM TẮT CHO SPONSOR (3 điểm):
1. [Vấn đề lớn nhất]
2. [Nguyên nhân]
3. [Đề xuất hành động và cần approval gì]

CHỈ SỐ CHÍNH:
  CPI: 0.75 (mỗi đồng chi chỉ tạo 0.75 đồng giá trị)
  SPI: 0.84 (chậm hơn kế hoạch 16%)
  EAC: 667M (dự báo over budget 167M)

QUYẾT ĐỊNH CẦN TRONG TUẦN NÀY:
  □ Approve tăng budget thêm [X]M
  □ Approve cắt scope [Y] feature
  □ Approve kéo dài timeline thêm [Z] tuần
```

---

## 9. Common Mistakes Khi Dùng EVM

| Sai lầm | Tác hại | Cách tránh |
|---|---|---|
| Dùng "% complete" chủ quan | EV không chính xác, toàn bộ EVM sai | Chỉ count task là Done khi có deliverable thực |
| Không cập nhật PV khi scope thay đổi | So sánh với baseline sai | Mỗi approved change request → update PMB |
| Tính EAC chỉ 1 lần rồi bỏ | Dự báo lỗi thời | Tính lại EAC mỗi sprint/tháng |
| Báo cáo EVM số thô cho CEO | CEO không hiểu, không trust | Dùng visual chart, tập trung vào hàm ý |
| Bỏ qua TCPI | Không biết kế hoạch recovery có realistic không | Luôn tính TCPI khi CPI < 0.9 |

---

## 10. Bài Tập EVM — 3 Scenarios

### Scenario A: Dự Án Tốt
BAC = 200M, Tuần 8/16
PV = 100M, EV = 110M, AC = 95M

Tính: CV, SV, CPI, SPI, EAC, VAC. Nhận xét tình trạng.

**Đáp án:**
- CV = 110-95 = **+15M** (under budget)
- SV = 110-100 = **+10M** (ahead of schedule)
- CPI = 110/95 = **1.16** (hiệu quả)
- SPI = 110/100 = **1.10** (nhanh hơn kế hoạch)
- EAC = 200/1.16 = **172M** (tiết kiệm 28M)
- VAC = 200-172 = **+28M** (dưới ngân sách)
- Nhận xét: Dự án đang tốt. PM có thể báo cáo positive news, xem xét dùng contingency reserve cho risk khác.

### Scenario B: Dự Án Trung Bình
BAC = 300M, Tuần 6/12
PV = 150M, EV = 135M, AC = 148M

Tính đầy đủ và đề xuất hành động.

**Đáp án:**
- CV = 135-148 = **-13M** (over budget nhẹ)
- SV = 135-150 = **-15M** (behind schedule)
- CPI = 135/148 = **0.91**
- SPI = 135/150 = **0.90**
- EAC = 300/0.91 = **330M** (+30M)
- VAC = 300-330 = **-30M**
- Đề xuất: Cảnh báo vàng. Root cause analysis ngay. Nếu không cải thiện trong 2 tuần → escalate.

### Scenario C: Dự Án Nguy Hiểm (giống Bài Tập 3 trong roadmap)
BAC = 500M, Tuần 10/20
PV = 250M, EV = 210M, AC = 280M

**Đáp án:** (Xem Ví dụ thực tế 2 ở trên — đây chính xác là scenario đó)
- CPI = 0.75, SPI = 0.84, EAC = 667M
- Đề xuất: Escalate ngay. Họp sponsor trong 24h. Present 3 options.

---

> **Ghi nhớ:** EVM không phải công cụ phạt team — nó là hệ thống cảnh báo sớm. Dùng để **phát hiện vấn đề sớm và có đủ thời gian hành động**, không phải để đổ lỗi sau khi dự án thất bại.
