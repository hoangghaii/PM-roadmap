# Iron Triangle — Tam Giác Ràng Buộc

> Đây là mô hình tư duy quan trọng nhất trong quản lý dự án. Nếu bạn chỉ nhớ một thứ từ giai đoạn nền tảng, hãy nhớ cái này.

---

## Khái Niệm Cốt Lõi

Iron Triangle (Tam giác sắt) mô tả ba ràng buộc cơ bản của mọi dự án:

```
                    SCOPE
                   /\
                  /  \
                 /    \
                /      \
               /________\
            TIME          COST
```

**Nguyên tắc vàng:** Khi một trong ba cạnh thay đổi, ít nhất một cạnh khác PHẢI thay đổi theo. Không thể giữ nguyên cả ba trong khi thay đổi một cạnh — trừ khi chấp nhận hy sinh chất lượng.

---

## Giải Thích Từng Cạnh

### SCOPE — Phạm vi công việc
**Là gì:** Tổng số tính năng, deliverable, và yêu cầu mà dự án phải thực hiện.

**Ví dụ cụ thể:**
- Scope = "Xây dựng ứng dụng mobile gồm đăng nhập, dashboard, báo cáo, và push notification"
- Scope tăng = thêm tính năng chat nội bộ
- Scope giảm = bỏ push notification ra khỏi v1

**Scope creep** là hiện tượng scope tăng dần không kiểm soát — thường không có thêm time hay cost tương ứng. Đây là "kẻ thù số 1" của PM.

### TIME — Thời gian
**Là gì:** Deadline hoặc duration của dự án.

**Ví dụ cụ thể:**
- Time = "Ra mắt ngày 30/06"
- Time bị rút ngắn = khách hàng đổi deadline thành 15/06
- Time giãn = project bị push sang tháng 8 vì phụ thuộc API bên thứ ba

**Lưu ý:** Thêm người vào project không luôn luôn giải quyết được time. Fred Brooks đã nói: *"Adding manpower to a late software project makes it later"* (The Mythical Man-Month). Developer mới cần thời gian onboard, hỏi han, review — làm chậm người cũ.

### COST — Chi phí / Ngân sách
**Là gì:** Budget tổng thể, bao gồm nhân lực (lương, outsource), hạ tầng, license, và chi phí khác.

**Ví dụ cụ thể:**
- Cost = "Ngân sách dự án 500 triệu VND, team 5 người trong 3 tháng"
- Cost tăng = thêm 1 developer thuê ngoài = thêm 30 triệu/tháng
- Cost giảm = cắt 20% budget, phải giảm scope hoặc giãn timeline

---

## Quality — Yếu Tố Thứ 4: Diamond Model

Nhiều tài liệu hiện đại mở rộng Iron Triangle thành Diamond bằng cách thêm **Quality** vào giữa:

```
                    SCOPE
                   /\
                  /  \
                 / Q  \
                /      \
               /________\
            TIME          COST

Q = Quality (bên trong, bị ảnh hưởng bởi cả 3 cạnh)
```

Khi Time bị rút ngắn, Cost không tăng, Scope không giảm → Quality là thứ sẽ chịu đựng.

**Quality giảm biểu hiện như thế nào:**
- Code review bị bỏ qua
- Test coverage giảm
- Technical debt tích lũy
- Bug không được fix hết trước release
- Documentation thiếu

> **Tại sao developer cần hiểu điều này:** Khi PM nói "cần ship trước Tết dù sao đi nữa" — bạn đang ngầm chấp nhận giảm quality. Hãy document rõ ràng những gì bị bỏ qua và tạo tickets để fix sau.

---

## Ví Dụ Thực Tế 1: Khách Hàng Muốn Thêm Tính Năng

**Tình huống:** Bạn đang develop một hệ thống HRM cho doanh nghiệp 300 nhân viên. Dự án đang ở tuần 8/12, đúng kế hoạch.

Khách hàng gọi điện: *"Chúng tôi vừa quyết định thêm module tính lương tự động vào scope. Không thay đổi deadline và budget."*

**Phân tích Iron Triangle:**

| Yếu tố | Trạng thái ban đầu | Yêu cầu mới |
|---|---|---|
| Scope | HRM cơ bản (nhân sự, chấm công, báo cáo) | + Module tính lương tự động (~4 tuần dev) |
| Time | Còn 4 tuần | Không thay đổi |
| Cost | 500 triệu đã approve | Không tăng |

**Điều PM phải làm:**

PM không thể chỉ nói "OK" và chờ team tự xử lý. PM phải present rõ các lựa chọn cho khách hàng:

```
Lựa chọn A: GIỮ deadline + GIỮ budget → CẮT scope khác
  → Bỏ module báo cáo nâng cao khỏi v1, thêm vào v2

Lựa chọn B: GIỮ scope đầy đủ + GIỮ budget → GIÃN timeline
  → Push deadline thêm 4–5 tuần, release vào tháng 7 thay vì tháng 6

Lựa chọn C: GIỮ scope đầy đủ + GIỮ deadline → TĂNG budget
  → Thuê thêm 1 developer outsource ~40 triệu, hoàn thành đúng hạn

Lựa chọn D (KHÔNG KHUYẾN NGHỊ): Giữ tất cả → GIẢM quality
  → Ship với nhiều bug, technical debt cao, team kiệt sức
```

**PM nói gì với khách hàng:**

> "Chúng tôi hoàn toàn có thể làm module tính lương. Để đảm bảo chất lượng, chúng tôi cần bạn chọn một trong ba phương án: giãn timeline 5 tuần, tăng ngân sách 40 triệu, hoặc defer module báo cáo nâng cao sang phase 2. Mỗi phương án có trade-off khác nhau — chúng ta cùng ngồi review để bạn quyết định."

---

## Ví Dụ Thực Tế 2: Deadline Bị Rút Ngắn

**Tình huống:** Dự án app giao đồ ăn cho chuỗi nhà hàng. Deadline ban đầu: 01/12. Ngày 15/10, CEO thông báo: *"Chúng ta phải demo cho investor ngày 01/11. Tất cả tính năng phải có."*

**Phân tích:**
- Time bị rút từ 6 tuần → 2.5 tuần (giảm 58%)
- Scope không thay đổi theo yêu cầu
- Budget không tăng

**Thực tế kỹ thuật:** Với team 4 developer, sprint 2 tuần, còn 3 sprint → chỉ còn 1 sprint cho demo.

**PM làm gì:**

Bước 1: Tổ chức Emergency Planning Meeting với tech lead ngay lập tức.

Bước 2: Phân loại features theo MoSCoW:
```
Must Have (demo được):
  ✅ Đăng nhập, chọn món, đặt hàng cơ bản
  ✅ Hiển thị trạng thái đơn hàng

Should Have (nice to have):
  🟡 Push notification
  🟡 Review & rating

Could Have (defer):
  ⭕ Loyalty points
  ⭕ Recommendation engine

Won't Have (cut hoàn toàn):
  ❌ Admin analytics dashboard
  ❌ Multi-restaurant management
```

Bước 3: PM trình bày với CEO:

> "Demo được vào 01/11 là khả thi nếu chúng ta giới hạn scope demo ở user journey cốt lõi: đặt hàng, thanh toán, theo dõi. Các tính năng admin và analytics sẽ ready vào 01/12 như kế hoạch. Investor sẽ thấy được product hoạt động thực tế — điều đó thuyết phục hơn một bản demo đầy đủ nhưng nhiều bug."

---

## Ví Dụ Thực Tế 3: Budget Bị Cắt

**Tình huống:** Dự án xây dựng platform quản lý chuỗi cung ứng cho công ty logistics. Budget ban đầu: 2 tỷ VND. Tháng 2/5, CFO thông báo cắt 30% → còn 1.4 tỷ.

**Phân tích tác động:**

| Hạng mục | Budget gốc | Sau cắt | Thiếu |
|---|---|---|---|
| Nhân lực (5 dev × 3 tháng) | 900tr | 630tr | 270tr |
| Hạ tầng & cloud | 200tr | 140tr | 60tr |
| QA & testing | 300tr | 210tr | 90tr |
| Contingency | 200tr | 140tr | 60tr |
| Quản lý (PM fee) | 400tr | 280tr | 120tr |

**Options PM đề xuất với management:**

**Option 1: Cắt scope 30%**
- Defer Phase 2 features (reporting dashboard, API integration với đối tác)
- Giữ core: inventory tracking, order management, basic dashboard
- Risk: Product kém cạnh tranh hơn tại launch

**Option 2: Giãn timeline 2 tháng**
- Giảm team từ 5 → 3 developer, extend duration
- Tổng cost tương đương nhưng runway dài hơn
- Risk: Time-to-market chậm, cạnh tranh có thể chiếm thị phần

**Option 3: Hybrid**
- Cắt 15% scope + giãn 1 tháng
- Cân bằng giữa scope và time
- Thường là lựa chọn tốt nhất trong thực tế

---

## Cách PM Dùng Iron Triangle Trong Thực Tế

### 1. Onboarding stakeholder ngay từ đầu
Trong kick-off meeting, PM cần explicit nói:

> "Dự án này có ba ràng buộc: scope, time, cost. Nếu một trong ba thay đổi, chúng ta cần thảo luận về điều chỉnh hai cái còn lại. Đây là điều tôi sẽ luôn transparent với mọi người."

### 2. Dùng làm framework khi nhận change request
Mỗi lần có change request, PM cần phân tích:
- Change này ảnh hưởng đến scope như thế nào? (+X ngày dev)
- Nếu timeline cố định, cần thêm bao nhiêu cost?
- Nếu cost cố định, phải cắt gì khỏi scope?

### 3. Tạo Change Request Document
```
CHANGE REQUEST #004
Ngày: 15/03/2026
Người yêu cầu: Nguyễn Văn A (Product Owner)
Mô tả thay đổi: Thêm tính năng export PDF cho báo cáo
Impact đến Scope: +5 ngày dev, +2 ngày QA
Impact đến Timeline: Cần push deadline từ 30/03 → 06/04
Impact đến Cost: +7 ngày × rate developer = +21tr VND
Alternatives: Export CSV (2 ngày dev, không cần push deadline)
Decision needed by: 17/03
```

### 4. Escalate kịp thời
Khi PM phát hiện Iron Triangle không cân bằng (ví dụ: scope tăng mà không có thêm time/cost), đây là tín hiệu cần escalate ngay — không đợi đến khi trễ hạn mới báo.

---

## Bài Tập: Phân Tích 3 Scenario Iron Triangle

### Scenario A
> Công ty bạn có dự án rebuild website thương mại điện tử. Timeline: 4 tháng. Budget: 800 triệu. Team: 3 developers, 1 designer, 1 QA. Tuần 10/16, stakeholder yêu cầu tích hợp thêm payment gateway thứ ba (ban đầu chỉ có 2).

**Câu hỏi:** Phân tích impact và đề xuất 3 options.

---

### Scenario B
> Dự án app mobile cho ngân hàng. Regulatory deadline không thể đổi: 30/09 (yêu cầu của Ngân hàng Nhà nước). Đến ngày 01/09, team báo cáo còn 40% features chưa xong.

**Câu hỏi:** Với deadline cứng không thể thay đổi, PM cần làm gì ngay lập tức?

---

### Scenario C
> Startup gọi vốn được vòng Seed, CEO quyết định dùng 30% số tiền đó để build MVP trong 2 tháng. PM bạn join ngày đầu và nhận thấy scope đã được promise với investor quá lớn cho 2 tháng.

**Câu hỏi:** Bạn là PM — bạn làm gì trong tuần đầu tiên?

---

*Xem gợi ý đáp án tại: [exercises/01-phan-tich-iron-triangle.md](./exercises/01-phan-tich-iron-triangle.md)*

---

## Tóm Tắt

| Nguyên tắc | Áp dụng thực tế |
|---|---|
| Ba cạnh liên kết chặt chẽ | Luôn phân tích impact đến cả ba khi có thay đổi |
| Không có bữa trưa miễn phí | Không thể tăng scope mà không tốn thêm time hoặc cost |
| Quality là nạn nhân mặc định | Nếu không manage tốt, quality sẽ tự động bị sacrifice |
| Transparency là vũ khí | Dùng Iron Triangle để educate stakeholder, không phải đối phó |

**Tiếp theo:** [03-methodologies.md](./03-methodologies.md) — Chọn đúng phương pháp cho đúng dự án
