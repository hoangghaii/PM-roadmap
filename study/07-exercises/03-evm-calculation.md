# Bài Tập 3: Earned Value Management (EVM)

**Mục tiêu:** Tính toán và phân tích sức khỏe dự án bằng EVM
**Thời gian:** 1-2 giờ
**Cấp độ:** Giai đoạn 2

---

## Quick Reference: Công Thức EVM

```
3 Chỉ Số Đầu Vào:
PV  = Planned Value     = BAC × Planned % Complete
EV  = Earned Value      = BAC × Actual % Complete
AC  = Actual Cost       (nhập tay từ accounting)

4 Variance/Index:
CV  = EV - AC           Cost Variance     (> 0 = under budget ✅)
SV  = EV - PV           Schedule Variance (> 0 = ahead of schedule ✅)
CPI = EV / AC           Cost Performance Index     (> 1 = efficient ✅)
SPI = EV / PV           Schedule Performance Index (> 1 = fast ✅)

Forecast:
EAC  = BAC / CPI        Estimate at Completion (dự báo tổng chi phí cuối)
ETC  = EAC - AC         Estimate to Complete (còn phải chi bao nhiêu)
VAC  = BAC - EAC        Variance at Completion (over/under budget cuối dự án)
TCPI = (BAC - EV) / (BAC - AC)  To-Complete Performance Index
```

---

## Bài Tập Chính

**Scenario:**
- **Budget (BAC):** 500 triệu VND
- **Duration:** 20 tuần
- **Tuần 10 review:**
  - Kế hoạch đã xong 50% công việc
  - Thực tế mới xong 42% công việc
  - Đã chi 280 triệu VND

**Yêu cầu:**
1. Tính PV, EV, AC
2. Tính CV, SV
3. Tính CPI, SPI
4. Tính EAC
5. Nhận xét: dự án đang ở trạng thái nào? Khuyến nghị gì?

---

## Đáp Án Chi Tiết

### Bước 1: Tính PV, EV, AC

```
PV = BAC × Planned % Complete
   = 500 × 50%
   = 250 triệu VND

EV = BAC × Actual % Complete
   = 500 × 42%
   = 210 triệu VND

AC = 280 triệu VND (given)
```

### Bước 2: Tính CV và SV

```
CV = EV - AC = 210 - 280 = -70 triệu VND  ❌ OVER BUDGET
SV = EV - PV = 210 - 250 = -40 triệu VND  ❌ BEHIND SCHEDULE
```

**Giải thích:**
- CV = -70 triệu → Chúng ta đã chi thêm 70 triệu so với giá trị công việc đã hoàn thành
- SV = -40 triệu → Chúng ta chậm hơn kế hoạch tương đương 40 triệu giá trị công việc

### Bước 3: Tính CPI và SPI

```
CPI = EV / AC = 210 / 280 = 0.75  ❌
→ Mỗi 1 triệu bỏ ra chỉ thu về 0.75 triệu giá trị

SPI = EV / PV = 210 / 250 = 0.84  ❌
→ Tốc độ thực hiện chỉ bằng 84% kế hoạch
```

### Bước 4: Tính EAC

```
EAC = BAC / CPI = 500 / 0.75 = 667 triệu VND

ETC = EAC - AC = 667 - 280 = 387 triệu VND
VAC = BAC - EAC = 500 - 667 = -167 triệu VND (over budget)
```

### Bước 5: Nhận Xét và Khuyến Nghị

**Tình trạng:** Dự án đang ở trạng thái **xấu trên cả 2 chiều** — over budget VÀ behind schedule.

**Dự báo:** Nếu tiếp tục với CPI hiện tại (0.75), dự án sẽ tốn **667 triệu** thay vì 500 triệu — **vượt budget 33%**.

**Nguyên nhân cần điều tra:**
- Tại sao chỉ xong 42% khi kế hoạch 50%?
- Tại sao chi 280 triệu cho 42% công việc (trong khi kế hoạch chỉ 250 triệu cho 50%)?
- Có scope thay đổi không?
- Resource issue? Estimation sai?

**Khuyến nghị cho PM:**
1. **Ngay lập tức:** Tổ chức meeting với sponsor để escalate — "Dự án cần action"
2. **Root cause analysis:** Tìm nguyên nhân cả over budget lẫn behind schedule
3. **Recovery plan:** Present 3 options:
   - Option A: Crash schedule (thêm resource) để recover SPI
   - Option B: Cắt scope để recover trong budget
   - Option C: Re-baseline với timeline và budget mới
4. **Tần suất review tăng lên:** Từ monthly → weekly

**TCPI (nếu muốn recover về BAC):**
```
TCPI = (BAC - EV) / (BAC - AC)
     = (500 - 210) / (500 - 280)
     = 290 / 220
     = 1.32

→ Để hoàn thành trong budget 500 triệu,
  phần còn lại phải hiệu quả 1.32× so với hiện tại
→ Gần như không khả thi khi CPI hiện tại chỉ là 0.75
→ Recommend re-baseline
```

---

## Bài Tập 3B: Scenario On Track

**Scenario:**
- BAC: 200 triệu, Duration: 10 tuần
- Tuần 5: Kế hoạch 50%, thực tế 52%, đã chi 95 triệu

**Tự tính trước, sau đó kiểm tra:**

```
PV  = 200 × 50% = 100 triệu
EV  = 200 × 52% = 104 triệu
AC  = 95 triệu

CV  = 104 - 95 = +9 triệu   ✅ Under budget
SV  = 104 - 100 = +4 triệu  ✅ Ahead of schedule
CPI = 104 / 95 = 1.09        ✅ Efficient
SPI = 104 / 100 = 1.04       ✅ Fast

EAC = 200 / 1.09 = 183.5 triệu (dự án có thể hoàn thành sớm hơn ngân sách)
```

**Nhận xét:** Đây là **dự án lý tưởng** — ahead of schedule và under budget. Nhưng đừng complacent — tiếp tục monitor, không giảm cadence review.

---

## Bài Tập 3C: Over Budget nhưng Ahead of Schedule

**Scenario:**
- BAC: 300 triệu, Duration: 12 tuần
- Tuần 6: Kế hoạch 50%, thực tế 60%, đã chi 200 triệu

```
PV  = 300 × 50% = 150 triệu
EV  = 300 × 60% = 180 triệu
AC  = 200 triệu

CV  = 180 - 200 = -20 triệu  ❌ Over budget
SV  = 180 - 150 = +30 triệu  ✅ Ahead of schedule
CPI = 180 / 200 = 0.90        ❌ Slightly inefficient
SPI = 180 / 150 = 1.20        ✅ Fast

EAC = 300 / 0.90 = 333 triệu (over budget 11%)
```

**Câu hỏi thảo luận:**
- Scenario này có "tốt" không? Ahead of schedule nhưng over budget.
- Nếu early completion có value (e.g., client trả thưởng), thì có thể justify.
- PM cần quyết định: slow down để save budget, hay continue fast và accept over budget?
- **Key insight:** SPI > 1 và CPI < 1 thường xảy ra khi dùng nhiều overtime/extra resource để go fast → cost tăng.
