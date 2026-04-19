# Bài Tập 1: Phân Tích Iron Triangle

## Mục Tiêu

Áp dụng kiến thức về Iron Triangle (Scope - Time - Cost) vào một dự án thực tế mà bạn từng tham gia với tư cách Developer. Mục tiêu không phải để "có đáp án đúng" — mà để bắt đầu suy nghĩ như một PM: nhìn thấy trade-off, không chỉ nhìn thấy vấn đề kỹ thuật.

---

## Nhắc Lại Nhanh: Iron Triangle

```
                    SCOPE
                   /\
                  /  \
                 /    \
                /      \
               /________\
            TIME          COST

Nguyên tắc: Thay đổi 1 cạnh → ít nhất 1 cạnh khác bị ảnh hưởng.
Không thể giữ nguyên cả 3 trong khi thay đổi 1 — trừ khi hy sinh QUALITY.
```

---

## Bài Tập Chính: Phân Tích Dự Án Đã Trải Qua

Nghĩ về một dự án bạn từng tham gia với tư cách Developer (thực hoặc gần nhất có thể). Điền vào 10 câu hỏi dưới đây. Không cần câu trả lời hoàn hảo — tập trung vào suy nghĩ và phân tích.

---

### Template Phân Tích Dự Án Thực Tế

**Thông tin cơ bản:**

| Mục                             | Thông tin của bạn            |
| ------------------------------- | ---------------------------- |
| Tên dự án (ẩn danh nếu muốn)    |                              |
| Timeline dự kiến ban đầu        |                              |
| Timeline thực tế                |                              |
| Team size                       |                              |
| Bạn đóng vai trò gì             |                              |
| Dự án giao hàng đúng hạn không? | Có / Không / Trễ \_\_\_ tuần |

---

**Câu 1: Scope ban đầu là gì?**

Mô tả ngắn gọn những tính năng/deliverable chính mà dự án phải deliver theo kế hoạch ban đầu.

```
[Ví dụ: "App mobile bán hàng gồm login, catalog sản phẩm, giỏ hàng, thanh toán VNPay, order tracking"]
```

Viết của bạn:

---

**Câu 2: Scope thực tế khi ship là gì?**

So sánh với câu 1 — có gì bị thêm vào, có gì bị cắt ra?

```
Thêm vào (scope creep):
- [...]

Bị cắt / defer sang phase sau:
- [...]
```

---

**Câu 3: Có bao nhiêu lần scope thay đổi trong dự án?**

Cố nhớ lại từng lần — ai yêu cầu, lý do gì, và tác động của nó.

| #   | Ai yêu cầu | Thay đổi gì | Tác động thực tế |
| --- | ---------- | ----------- | ---------------- |
| 1   |            |             |                  |
| 2   |            |             |                  |
| 3   |            |             |                  |

---

**Câu 4: Timeline bị ảnh hưởng như thế nào?**

- Deadline gốc: \_\_\_
- Deadline thực tế delivery: \_\_\_
- Lý do chính gây trễ (nếu có):
  - [ ] Scope thay đổi
  - [ ] Underestimate kỹ thuật
  - [ ] Resource thiếu hoặc thay đổi
  - [ ] Bug / technical issue lớn
  - [ ] External dependency (API bên thứ 3, approval từ đối tác, v.v.)
  - [ ] Khác: \_\_\_

---

**Câu 5: Budget có bị ảnh hưởng không?**

Dù bạn không quản lý budget trực tiếp, hãy nhớ lại những dấu hiệu gián tiếp:

- Có sprint nào bị cancel hoặc rút ngắn không?
- Có thuê thêm người không? Hay ngược lại, có người bị rút ra khỏi dự án?
- Có lúc nào PM nói "chúng ta cần làm nhanh hơn để tránh tốn thêm chi phí" không?
- Infra/tool bị downgrade vì budget không?

```
[Ghi nhận quan sát của bạn]
```

---

**Câu 6: Quality thực tế như thế nào khi ship?**

Quality là thứ bị sacrifice khi 3 cạnh kia không được điều chỉnh. Nhìn lại trung thực:

- Technical debt để lại bao nhiêu? (Ước tính số tickets "cần fix sau")
- Test coverage có đủ không?
- Có feature nào ship với known bugs không?
- Có code review bị bỏ qua không? Sprint nào?
- Sau go-live, có bao nhiêu critical bugs được report trong 2 tuần đầu?

---

**Câu 7: PM của dự án đó xử lý trade-off như thế nào?**

Nhìn lại qua con mắt của người học PM:

- PM có communicate rõ ràng với team về các quyết định không?
- Khi scope thêm vào, PM có giải thích tại sao không có thêm time/budget không?
- PM có bảo vệ team trước áp lực từ stakeholder không?
- Điều bạn thấy PM làm tốt là gì?
- Điều bạn nghĩ PM lẽ ra nên làm khác đi là gì?

---

**Câu 8: Nếu BẠN là PM của dự án đó, bạn sẽ làm gì khác?**

Đây là câu quan trọng nhất. Suy nghĩ cụ thể — không phải lý thuyết.

```
Tôi sẽ làm khác ở điểm [X] vì [lý do Y], với kết quả kỳ vọng là [Z].
```

Ví dụ:

> "Tôi sẽ document rõ scope baseline trong tuần đầu và yêu cầu mọi thay đổi đi qua formal change request. Khi scope tăng 3 lần trong tháng 2 mà không có thêm time/budget, tôi sẽ escalate sớm hơn thay vì để team làm overtime."

---

**Câu 9: Bài học Iron Triangle rõ nhất từ dự án này là gì?**

Tóm tắt thành 2–3 câu ngắn gọn, súc tích.

```
[Bài học 1]
[Bài học 2]
[Bài học 3]
```

---

**Câu 10: Điều gì bạn sẽ áp dụng ngay khi trở thành PM?**

Ghi ra 1–2 hành động cụ thể, có thể thực hiện ngay từ dự án đầu tiên.

```
Action 1: [...]
Action 2: [...]
```

---

## 3 Scenarios Giả Định Để Thực Hành

Nếu bạn chưa có kinh nghiệm PM thực tế, hoặc muốn luyện thêm tư duy, hãy phân tích 3 tình huống dưới đây. Mỗi scenario phản ánh một dạng áp lực Iron Triangle phổ biến trong thực tế Việt Nam.

---

### Scenario A: Startup Fintech — Developer Nghỉ Giữa Dự Án

**Bối cảnh đầy đủ:**

Bạn là PM của startup fintech nhỏ (10 người). Dự án: xây dựng app thanh toán ví điện tử MVP. Timeline: 3 tháng (tháng 10 → tháng 12), mục tiêu ra mắt trước Tết Nguyên Đán để kịp mùa shopping. Budget: 400 triệu (3 developer full-time + 1 designer + PM là bạn).

Ngày D+45 (giữa tháng 11), developer chính (người duy nhất biết code phần backend payment gateway) thông báo nghỉ việc vì nhận offer từ công ty Singapore với lương gấp đôi. Anh ấy đồng ý ở lại thêm 2 tuần để handover.

Tại thời điểm này, dự án đang ở 60% completion theo kế hoạch ban đầu. Còn 6 tuần đến Tết. Các tính năng chưa xong bao gồm: tích hợp ngân hàng (quan trọng nhất), push notification, lịch sử giao dịch (báo cáo), và referral program.

**Câu hỏi để tự phân tích (viết ra trước khi đọc đáp án mẫu):**

1. Ba cạnh Iron Triangle đang ở trạng thái nào? Cạnh nào đang bị đe dọa nhất?
2. Bạn có những option nào? Liệt kê tất cả, kể cả option tệ nhất.
3. Thông tin nào bạn cần thu thập trong 24 giờ đầu?
4. Ai là stakeholder quan trọng nhất cần communicate ngay?
5. Nếu phải chọn 1 option, bạn chọn gì và tại sao?

---

### Scenario B: Dự Án ERP — Khách Hàng Thêm Module Sau Khi Ký Hợp Đồng

**Bối cảnh đầy đủ:**

Bạn là PM của công ty phần mềm, phụ trách dự án triển khai ERP cho nhà máy sản xuất nhựa 500 nhân viên. Hợp đồng đã ký: 1.2 tỷ VND, timeline 6 tháng, scope gồm 4 module: quản lý sản xuất, quản lý kho, mua hàng, và bán hàng.

Tháng 2/6, sau khi dự án đã hoàn thành analysis và đang bắt đầu development, Giám đốc Tài chính của khách hàng gọi điện trực tiếp cho bạn:

> "Chúng tôi vừa họp board và quyết định cần tích hợp module kế toán (general ledger, accounts payable/receivable, báo cáo tài chính) vào dự án này. Tài chính quan trọng hơn tôi nghĩ lúc đầu. Budget không thay đổi. Deadline cũng không thay đổi."

Module kế toán ước tính thêm 8–10 tuần developer, trong khi dự án chỉ còn 4 tháng. Đây là yêu cầu từ CFO — người không phải sponsor ban đầu (sponsor là COO).

**Câu hỏi để tự phân tích:**

1. Tại sao đây là tình huống đặc biệt nguy hiểm (gợi ý: liên quan đến ai gọi điện)?
2. Bước đầu tiên bạn làm NGAY sau cuộc gọi là gì?
3. Bạn present vấn đề này với sponsor (COO) như thế nào?
4. Có bao nhiêu option khả thi? Phân tích pros/cons mỗi option.
5. Hậu quả nếu bạn nói "OK" với CFO mà không escalate?

---

### Scenario C: App Mobile — Budget Bị Cắt 30% Sau 3 Tháng

**Bối cảnh đầy đủ:**

Bạn là PM cho dự án phát triển app mobile 6 tháng cho một retail chain (chuỗi siêu thị nhỏ). Budget: 800 triệu. Team: 2 iOS developer, 1 Android developer, 1 backend developer, 1 designer, 1 QA, và bạn là PM.

Tháng 3/6 (đúng nửa chừng), CFO thông báo qua email: do tình hình kinh tế khó khăn và doanh thu Q1 giảm 25%, toàn bộ project budget bị cắt 30%. Budget còn lại: 560 triệu, không thể thương lượng thêm.

Hiện tại (sau 3 tháng), dự án đã hoàn thành:

- iOS app: 70% (còn thiếu payment integration và loyalty program)
- Android app: 50% (còn thiếu offline mode, payment, loyalty program)
- Backend API: 80% (còn thiếu analytics engine và admin dashboard)

Các tính năng chưa làm nhưng đã được promise với ban lãnh đạo: loyalty points system, push notification campaign manager, và analytics dashboard cho store managers.

**Câu hỏi để tự phân tích:**

1. Map lại Iron Triangle: trước và sau khi budget bị cắt
2. Với 560 triệu còn lại, bạn có thể duy trì team trong bao lâu?
3. Tính năng nào là MVP "sống còn" phải có? Tính năng nào có thể defer?
4. Bạn communicate như thế nào với team để duy trì morale?
5. Nếu timeline vẫn giữ nguyên 6 tháng, bạn sẽ ship gì?

---

## Đáp Án Mẫu: Scenario A (Startup Fintech)

### Bước 1: Phân Tích Nhanh Iron Triangle

```
Trước sự kiện:
  Scope: MVP app thanh toán (100%)
  Time: 6 tuần đến Tết (cố định — deadline market)
  Cost: 400 triệu (3 dev + 1 designer)

Sau khi dev chính nghỉ:
  Scope: Không đổi (vẫn cần 40% còn lại)
  Time: Không đổi (6 tuần)
  Cost: Thực tế giảm 1 senior developer
         + tốn thêm 2 tuần handover cost
         + tiềm năng cần thuê người mới

→ Cả 3 cạnh đang bị áp lực cùng lúc.
→ Quality gần như chắc chắn bị ảnh hưởng.
```

### Bước 2: Thu Thập Dữ Liệu Ngay Trong 24 Giờ Đầu

**Meeting khẩn với dev nghỉ (trong hôm nay):**

Hỏi và document lại:

- Tình trạng hiện tại của phần code anh ấy đang làm (% hoàn thành)
- Technical debt, edge cases chưa handle
- Những phần nào phức tạp nhất (payment gateway flow, error handling)
- Có ai trong team có thể tiếp nhận không? Cần bao lâu để onboard?
- Anh ấy có thể document architecture trong 2 tuần không?

**Meeting với tech lead (cùng ngày):**

- Estimate lại: với team còn lại (2 dev + designer), có thể complete bao nhiêu % scope trong 6 tuần?
- Tính năng nào bắt buộc cho MVP launch? Tính năng nào có thể defer?
- Option thuê outsource: có ai tin tưởng không? Ramp-up time bao lâu?

### Bước 3: Phân Tích 4 Options

| Option | Mô tả                                               | Pros                                | Cons                                                                         | Khả thi?                                       |
| ------ | --------------------------------------------------- | ----------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------- |
| **A**  | Thuê outsource developer thay thế ngay              | Giữ scope + timeline                | Ramp-up 2–3 tuần, tìm người tin tưởng khó, tốn chi phí thêm ~50–80 triệu     | Khó — 2 tuần ramp-up ăn hết thời gian handover |
| **B**  | Cắt scope — chỉ ship core payment flow trước Tết    | Giữ deadline, ship được MVP thực sự | Một số feature đã promise không có, user experience kém hơn                  | Khả thi nhất                                   |
| **C**  | Push deadline thêm 4–6 tuần (sau Tết)               | Giữ full scope, quality tốt hơn     | Mất market timing — Tết là peak season, khó recover                          | Tệ nhất về business                            |
| **D**  | Để team hiện tại cố làm hết trong 6 tuần (overtime) | Giữ deadline và scope               | Team burnout, quality thấp, rủi ro bugs critical khi launch, mất team sau đó | Không nên — sustainable                        |

### Bước 4: Recommendation

**Khuyến nghị: Option B (cắt scope) kết hợp một phần Option A.**

Phân tích cụ thể:

- **Must Have (ship trước Tết):** Đăng ký tài khoản, nạp tiền, thanh toán QR, lịch sử giao dịch cơ bản
- **Should Have (ship sau Tết 2–3 tuần):** Push notification, referral program
- **Defer sang v1.5:** Analytics dashboard, loyalty tiers

Đồng thời: Yêu cầu dev nghỉ tập trung document hết architecture của payment gateway trong 2 tuần. Assign 1 dev junior kèm cặp anh ấy full-time để transfer knowledge.

### Bước 5: Communication Với Stakeholder

**Message cho CEO/CTO trong ngày hôm nay:**

> "Chúng ta có một rủi ro nghiêm trọng cần quyết định ngay. [Dev tên X] vừa thông báo nghỉ việc, sẽ ở lại 2 tuần để handover. Phần anh ấy phụ trách (payment gateway integration) là core nhất của app và chiếm ~25% còn lại.
>
> Tôi đã ngồi với tech lead để assess. Có 3 options:
>
> 1. Cắt scope về MVP tối thiểu, giữ deadline Tết — team khả thi, rủi ro thấp
> 2. Thuê outsource ngay — khó tìm người đúng, ramp-up tốn 2–3 tuần, thêm ~60–80 triệu
> 3. Push deadline 6 tuần — mất timing Tết
>
> Tôi recommend Option 1. Cần anh/chị quyết định trong hôm nay để chúng ta bắt đầu chuẩn bị."

---

## Checklist Tự Đánh Giá

Sau khi hoàn thành bài tập, tự chấm điểm:

```
PHÂN TÍCH VẤN ĐỀ
[ ] Tôi xác định được chính xác cạnh nào của Iron Triangle bị ảnh hưởng
[ ] Tôi phân tích được impact chain (thay đổi A → hậu quả B → cần quyết định C)
[ ] Tôi không bỏ qua yếu tố Quality

THU THẬP DỮ LIỆU
[ ] Tôi biết cần hỏi ai và hỏi gì trước khi đưa ra quyết định
[ ] Tôi phân biệt được "thông tin cần ngay" và "thông tin có thể chờ"

ĐỀ XUẤT GIẢI PHÁP
[ ] Tôi đề xuất ít nhất 3 options (không chỉ 1)
[ ] Mỗi option có phân tích pros/cons rõ ràng
[ ] Tôi có recommendation cụ thể (không chỉ liệt kê options)
[ ] Recommendation của tôi có lý do logic, không chỉ "cảm giác đúng"

COMMUNICATION
[ ] Tôi biết ai là stakeholder cần thông báo đầu tiên
[ ] Message của tôi concise, có data, có options, có recommendation
[ ] Tone không hoảng loạn, không né tránh vấn đề

TƯ DUY PM
[ ] Tôi nhìn vấn đề từ góc độ business, không chỉ technical
[ ] Tôi cân nhắc cả team morale và sustainability
[ ] Tôi document được quyết định và lý do (để reference sau này)
```

**Điểm:**

- 13–15 ✓ : Tư duy PM tốt, tiếp tục phát triển
- 9–12 ✓ : Đang đúng hướng, cần luyện thêm phân tích trade-off
- 5–8 ✓ : Cần đọc lại lý thuyết và thực hành thêm scenarios
- < 5 ✓ : Đừng nản lòng — đây là bài tập đầu tiên. Luyện lại từ Scenario A.

---

_Tiếp theo: [02-phong-van-pm.md](./02-phong-van-pm.md) — Học từ người đang làm PM thực tế_
