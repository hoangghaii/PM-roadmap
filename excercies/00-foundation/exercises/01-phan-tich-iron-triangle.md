# Bài Tập 1: Phân Tích Iron Triangle

## Bài Tập Chính: Phân Tích Dự Án Đã Trải Qua

**Thông tin cơ bản:**

| Mục                             | Thông tin của bạn |
| ------------------------------- | ----------------- |
| Tên dự án (ẩn danh nếu muốn)    | Cypher Global     |
| Timeline dự kiến ban đầu        | 01/04/2026        |
| Timeline thực tế                | 01/06/2026        |
| Team size                       | 5                 |
| Bạn đóng vai trò gì             | Developer         |
| Dự án giao hàng đúng hạn không? | Trễ 8 tuần        |

---

**Câu 1: Scope ban đầu là gì?**

Mô tả ngắn gọn những tính năng/deliverable chính mà dự án phải deliver theo kế hoạch ban đầu.

```text
Maintain app/web app dance với 2 roles: Creator và Fan. Scope: Fix bugs tồn động có từ trước, thêm tính năng subtitle cho video (CRUD, view), thêm tính năng cổng thanh toán (đã có paypal từ trước), làm lại trang dashboard cho 2 roles creator và fan.
```

---

**Câu 2: Scope thực tế khi ship là gì?**

So sánh với câu 1 — có gì bị thêm vào, có gì bị cắt ra?

```text
Thêm vào (scope creep):
- Không có

Bị cắt / defer sang phase sau:
- Bị cắt: không có
- Defer sang phase sau: thêm tính năng cổng thanh toán, làm lại trang dashboard cho 2 roles creator và fan.
```

---

**Câu 3: Có bao nhiêu lần scope thay đổi trong dự án?**

Cố nhớ lại từng lần — ai yêu cầu, lý do gì, và tác động của nó.

| #   | Ai yêu cầu     | Thay đổi gì                                            | Tác động thực tế           |
| --- | -------------- | ------------------------------------------------------ | -------------------------- |
| 1   | Team developer | Defer scope cổng thanh toán và làm lại trang dashboard | Kéo dài TIME, dãn deadline |
| 2   |                |                                                        |                            |
| 3   |                |                                                        |                            |

---

**Câu 4: Timeline bị ảnh hưởng như thế nào?**

- Deadline gốc: 01/04/2026
- Deadline thực tế delivery: 01/06/2026
- Lý do chính gây trễ (nếu có):
  - [x] Scope thay đổi
  - [x] Underestimate kỹ thuật
  - [x] Resource thiếu hoặc thay đổi
  - [x] Bug / technical issue lớn
  - [x] External dependency (API bên thứ 3, approval từ đối tác, v.v.)
  - [ ] Khác: \_\_\_

---

**Câu 5: Budget có bị ảnh hưởng không?**

Dù bạn không quản lý budget trực tiếp, hãy nhớ lại những dấu hiệu gián tiếp:

- Có sprint nào bị cancel hoặc rút ngắn không?
- Có thuê thêm người không? Hay ngược lại, có người bị rút ra khỏi dự án?
- Có lúc nào PM nói "chúng ta cần làm nhanh hơn để tránh tốn thêm chi phí" không?
- Infra/tool bị downgrade vì budget không?

```text
- Không có sprint nào bị cancel hay rút ngắn
- Không thuê thêm người hay rút người
- Infra/tool không bị downgrade vì bugget
- Tuy nhiên deadline bị dãn ra, 2 scope được xác đinh done trong 2 tuần thì bị kéo dài thành 3,4 tuần
-> Bugget bị tăng
```

---

**Câu 6: Quality thực tế như thế nào khi ship?**

Quality là thứ bị sacrifice khi 3 cạnh kia không được điều chỉnh. Nhìn lại trung thực:

- Technical debt để lại bao nhiêu? (Ước tính số tickets "cần fix sau")
- Test coverage có đủ không?
- Có feature nào ship với known bugs không?
- Có code review bị bỏ qua không? Sprint nào?
- Sau go-live, có bao nhiêu critical bugs được report trong 2 tuần đầu?

```text
- Technical debt để lại bao nhiêu: 30 tickets
- Test coverage có đủ không: Không đủ
- Có features nào ship với know bugs không: Có (video subtitle)
- Sau go-live, có bao nhiêu critical bugs được report trong 2 tuần đầu: Khá nhiều
```

---

**Câu 7: PM của dự án đó xử lý trade-off như thế nào?**

Nhìn lại qua con mắt của người học PM:

- PM có communicate rõ ràng với team về các quyết định không?
- Khi scope thêm vào, PM có giải thích tại sao không có thêm time/budget không?
- PM có bảo vệ team trước áp lực từ stakeholder không?
- Điều bạn thấy PM làm tốt là gì?
- Điều bạn nghĩ PM lẽ ra nên làm khác đi là gì?

```text
- PM có communicate rõ ràng với team về các quyết định không: Có
- Khi scope thêm vào, PM có giải thích tại sao không có thêm time/budget không: Có
- PM có bảo vệ team trước áp lực từ stakeholder không?: Có
- Điều bạn thấy PM làm tốt là gì: roadmap rõ ràng, raise lên kịp thời cho stackholder và techlead, quản lý và bám sát task tốt.
- Điều bạn nghĩ PM lẽ ra nên làm khác đi là gì: Nên xác định rõ scope ngay từ đầu là gì, est task quá ít thời gian, chưa lường trước được DEADLINE sẽ kéo dài ra.
```

---

**Câu 8: Nếu BẠN là PM của dự án đó, bạn sẽ làm gì khác?**

Đây là câu quan trọng nhất. Suy nghĩ cụ thể — không phải lý thuyết.

> "Tôi sẽ document rõ scope baseline trong tuần đầu và yêu cầu mọi thay đổi đi qua formal change request. Khi scope tăng 3 lần trong tháng 2 mà không có thêm time/budget, tôi sẽ escalate sớm hơn thay vì để team làm overtime. Task sẽ được est thêm để tránh overload. Khi thấy team dev raise source code quá cũ tôi sẽ kiểm tra lại và nói với stackholder những vấn đề sẽ xảy ra khi source code quá cũ"

---

**Câu 9: Bài học Iron Triangle rõ nhất từ dự án này là gì?**

Tóm tắt thành 2–3 câu ngắn gọn, súc tích.

```text
- Khi SCOPE bị thay đổi, khả năng TIME cũng bị thay đổi và COST sẽ bị thay đổi theo
- Source code quá cũ hoặc năng lực team chưa đủ sẽ ảnh hưởng rất nhiều tới SCOPE, TIME và COST
```

---

**Câu 10: Điều gì bạn sẽ áp dụng ngay khi trở thành PM?**

Ghi ra 1–2 hành động cụ thể, có thể thực hiện ngay từ dự án đầu tiên.

```text
Action 1: Nếu là maintain, nhờ team kiểm tra source code, nếu source code quá cũ cần suy nghĩ tới khả năng trễ deadline hoặc giảm scope, họp với stackholder để nói trước những vấn đề có thể xảy ra nếu source code quá cũ.
Action 2: Audit team, scope, phân loại MoSoCW features, estimate để check TIME.
```

## 3 Scenarios Giả Định Để Thực Hành

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

```text
1. Ba cạnh Iron Triangle đang ở trạng thái nào? Cạnh nào đang bị đe dọa nhất?
  Trước sự kiện:
    SCOPE: App thanh toán MVP (100%)
    TIME: 6 tuần
    COST: 400 triệu (3 developer, 1 designer, 1 PM)

  Sau sự kiện:
    SCOPE: Không đổi (cần 40% còn lại)
    TIME: 6 tuần
    COST: Giảm 1 senior dev + cost 2 tuần handover + có thể thêm 1 senior dev để bù vào

  -> Cả 3 cạnh đều đang bị áp lực, cạnh TIME đang bị ảnh hưởng nhiều nhất
  -> Quality chắc chắn bị ảnh hưởng

2. Thông tin nào bạn cần thu thập trong 24 giờ đầu?
  Meeting khẩn với dev nghỉ:
    - Tình trạng code hiện tại (% hoàn thành)
    - Technical debt, edge case chưa handle
    - Những phần nào phức tạp nhất (payment gateway flow, error handling)
    - Có ai trong team có thể tiếp nhận không? Cần bao lâu để onboard
    - Có thể document architecture trong 2 tuần không

  Meeting với techlead:
    - Estimate lại: với team còn lại (2 developer và 1 designer), có thể complete bao nhiêu % số scope còn lại trong 6 tuần
    - Trong số scope còn lại, những feature nào là bắt buộc, những tính năng nào có thể defer
    - Option thuê developer: có ai có thể tin tưởng được, mất bao lâu để on-board

3. Bạn có những option nào? Liệt kê tất cả, kể cả option tệ nhất.
  Option 1: Thuê outsource developer thay thế ngay
  Props: Giữ được scope và timeline
  Cons: Thêm chi phí, có thể khó tìm người, on-board 2-3 ngày
  Khả thi: Khó

  Option 2: Cắt scope, chỉ ship core feature trước tết
  Props: Giữ được timeline và cost
  Cons: Một số features đã promise không có, user experience kém hơn
  Khả thi: khả thi nhất

  Option 3: Kéo dài deadline thêm 4-6 tuần
  Props: Giữ được scope
  Cons: Mất market timing
  Khả thi: tệ nhất về business

  Option 4: Cho team overtime để hoàn thành tất cả
  Props: Giữ được timeline và scope
  Cons: Team burnout, quanlity thấp, rủi ro bugs critical khi lauch
  Khả thi: không nên

4. Nếu phải chọn 1 option, bạn chọn gì và tại sao?
  Chọn option 2: cắt scope, chỉ ship core flow scope đồng thời yêu cầu dev nghỉ tập trung document hết architecture của payment gateway trong 2 tuần, assign 1 dev junior kèm 1-1 để transfer.

  Phân tích cụ thể:
  - **Must Have (ship trước Tết):** Đăng ký tài khoản, nạp tiền, thanh toán QR, lịch sử giao dịch cơ bản
  - **Should Have (ship sau Tết 2–3 tuần):** Push notification, referral program
  - **Defer sang v1.5:** Analytics dashboard, loyalty tiers

5. Ai là stakeholder quan trọng nhất cần communicate ngay?
  Message cho CEO/CTO trong ngày hôm nay

  > "Chúng ta có một rủi ro nghiêm trọng cần quyết định ngay. [Dev tên X] vừa thông báo nghỉ việc, sẽ ở lại 2 tuần để handover. Phần anh ấy phụ trách (payment gateway integration) là core nhất của app và chiếm ~25% còn lại.
  >
  > Tôi đã ngồi với tech lead để assess. Có 3 options:
  >
  > 1. Cắt scope về MVP tối thiểu, giữ deadline Tết — team khả thi, rủi ro thấp
  > 2. Thuê outsource ngay — khó tìm người đúng, ramp-up tốn 2–3 tuần, thêm ~60–80 triệu
  > 3. Push deadline 6 tuần — mất timing Tết
  >
  > Tôi recommend Option 1. Cần anh/chị quyết định trong hôm nay để chúng ta bắt đầu chuẩn bị."
```

---

### Scenario B: Dự Án ERP — Khách Hàng Thêm Module Sau Khi Ký Hợp Đồng

**Bối cảnh đầy đủ:**

Bạn là PM của công ty phần mềm, phụ trách dự án triển khai ERP cho nhà máy sản xuất nhựa 500 nhân viên.
Hợp đồng đã ký: 1.2 tỷ VND, timeline 6 tháng, scope gồm 4 module: quản lý sản xuất, quản lý kho,
mua hàng, và bán hàng.

Tháng 2/6, sau khi dự án đã hoàn thành analysis và đang bắt đầu development,
Giám đốc Tài chính của khách hàng gọi điện trực tiếp cho bạn:

> "Chúng tôi vừa họp board và quyết định cần tích hợp module kế toán
> (general ledger, accounts payable/receivable, báo cáo tài chính) vào dự án này.
> Tài chính quan trọng hơn tôi nghĩ lúc đầu. Budget không thay đổi. Deadline cũng không thay đổi."

Module kế toán ước tính thêm 8–10 tuần developer, trong khi dự án chỉ còn 4 tháng.
Đây là yêu cầu từ CFO — người không phải sponsor ban đầu (sponsor là COO).

**Câu hỏi để tự phân tích:**

1. Tại sao đây là tình huống đặc biệt nguy hiểm (gợi ý: liên quan đến ai gọi điện)?
2. Bước đầu tiên bạn làm NGAY sau cuộc gọi là gì?
3. Bạn present vấn đề này với sponsor (COO) như thế nào?
4. Có bao nhiêu option khả thi? Phân tích pros/cons mỗi option.
5. Hậu quả nếu bạn nói "OK" với CFO mà không escalate?

---

**_Phân tích bối cảnh_**

- Dự án ERP cho nhà máy 500 nhân viên
- Dự án đã hoàn thành analysis và đang bắt đầu development

- Trước sự kiện:
  - BUDGET: 1.2 tỷ VND
  - SCOPE: 4 modules: quản lý sản xuất, quản lý kho, mua hàng, bán hàng
  - DEADLINE: 6 tháng

- Sau khi **Gián đốc tài chính của khách hàng** gọi cho bạn:
  - BUDGET: không đổi (1.2 tỷ VND)
  - SCOPE: 4 modules ban đầu + modules kế toán (general ledger, accounts payable/receivable, báo cáo tài chính)
  - DEADLINE: Không đổi (theo yêu cầu của stakeholder — đây là vấn đề)

**_1. Tại sao đây là tính huống đặc biệt nguy hiểm_**

- Người gọi điện là **GIÁM ĐỐC TÀI CHÍNH** của khách hàng, 1 chức vụ rất lớn,
  nhưng người này không phải là sponsor ban đầu (không loại trừ khả năng sponsor của bạn không biết thông tin có module mới này)
- Rủi ro hợp đồng: Module kế toán không nằm trong contract. Nếu bạn nói "OK" với CFO, công ty bạn có thể bị ép làm việc miễn phí hoặc bị kiện nếu không deliver đúng hạn
- Rủi ro nội bộ khách hàng: CFO và COO có thể đang có conflict nội bộ (CFO muốn kế toán, COO không biết hoặc không đồng ý) — bạn bị kéo vào chính trị nội bộ của khách hàng nếu không escalate
- Module mới quá lớn, để hoàn thành cần 8-10 tuần developer -> Nếu thêm vào scope hiện tại sẽ không kịp

**_2. Bước đầu tiên bạn làm NGAY sau cuộc gọi là gì_**

Bước 0 (NGAY TRÊN ĐIỆN THOẠI): Không cam kết gì với CFO  
 → "Cảm ơn anh/chị, tôi cần đánh giá impact và sẽ phản hồi trong 24 giờ"

Bước 1 (Trong vài giờ đầu): Báo ngay cho management nội bộ của bạn  
 → PM không tự xử lý tình huống vượt scope contract một mình

Bước 2 (Song song): Họp nhanh với tech lead  
 → Chỉ cần estimate sơ bộ (~30 phút) để đánh giá risk, effor. Không cần phân rã chi tiết ngay  
 → Mục đích: có số liệu khi gặp COO

Bước 3 (Trong ngày): Gặp COO + CFO cùng lúc  
 → Đừng gặp COO trước khi có data từ tech lead

**_3. Bạn present vấn đề này với sponsor (COO) như thế nào_**

- Mở cuộc họp với COO và CFO

> "Anh [COO], tôi nhận được cuộc gọi từ CFO sáng nay với đề xuất thêm module kế toán vào scope hiện tại, giữ nguyên budget và deadline.
>
> Tôi đã làm việc với tech lead để đánh giá sơ bộ: module kế toán cần thêm 8–10 tuần effort, trong khi dự án còn 4 tháng với team hiện tại đang full capacity.
>
> Đây là thay đổi lớn nằm ngoài contract ban đầu, tôi cần anh xác nhận: đây có phải quyết định chính thức từ phía khách hàng không? Và chúng ta có muốn xử lý theo quy trình change request không?
>
> Tôi có 3 options để trình bày..."

**_4. Có bao nhiêu option khả thi? Phân tích pros/cons mỗi option._**

- Option 1: Cắt giảm SCOPE
  - Thêm module kế toán vào scope hiện tại tuy nhiên cả 5 modules sẽ chỉ ship core, must-have features.
  - Props: Giữ được COST và DEADLINE
  - Cons: Khồng đầy đủ feature, ảnh hưởng tới user experience.

- Option 2: Thuê thêm outsource developer
  - Thuê thêm 1-2 developer có domain knowledge kế toán trong 1-2 tháng để hoàn thành module kế toán
  - Props: Giữ được SCOPE và DEADLINE
  - Cons: Cost để tăng vì thuê thêm developer (giả định thuê 2 developer trong 2 tháng, 35 triệu/developer/tháng -> cost tăng thêm 100 triệu)

- Option 3: Kéo dài deadline
  - Kéo dài deadline thêm 8-10 tuần để hoàn thành module kế toán
  - Props: Giữ được SCOPE
  - Cons: Ảnh hưởng kế hoạch vận hành nhà máy, chi phí PM team kéo dài, ảnh hưởng đến business, cost tăng vì time tăng

- Option 4: Cho team OT
  - Cho team OT để hoàn thành module kế toán
  - Props: Giữ được SCOPE, DEADLINE
  - Cons: team burnout, quality giảm, tiềm ẩn critical bugs khi launch -> Không khuyến nghị

- Option 5: Defer sang Phase 2 — ký hợp đồng mới
  - Giữ nguyên 4 modules theo contract, deliver đúng hạn
  - Module kế toán = dự án riêng, hợp đồng riêng, timeline riêng
  - Pros: Bảo vệ contract hiện tại, không rủi ro pháp lý, tạo doanh thu mới
  - Cons: CFO có thể không hài lòng trong ngắn hạn

**_5. Hậu quả nếu bạn nói "OK" với CFO mà không escalate_**

- Khả năng rất cao không hoàn thành được dự án, team burnout, quanlity giảm, bugs critical tiềm ẩn, CFO và COO mất niềm tin vào bạn, ảnh hưởng tới cả team và bạn.
- Rủi ro pháp lý: Nếu bạn verbal commit với CFO → công ty bạn có thể bị ép deliver module không có trong contract, hoặc bị kiện nếu trễ/không deliver
- Tạo precedent xấu: CFO (và các stakeholder khác) học được rằng có thể bypass process bằng cách gọi thẳng cho PM → những lần sau sẽ tiếp tục làm vậy

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

**_Phân tích bối cảnh:_**

- Dự án phát triển app mobile
- Timeline tổng: 6 tháng
- Timeline hiện tại: tháng 3/6
- Timeline còn lại: 3 tháng
- Budget ban đầu: 800 triệu
- Budget sau sụ kiện: 560 triệu (giảm 30%, không thể thương lượng)
- Team size: 2 iOS developer, 1 Android developer, 1 backend developer, 1 designer, 1 QA, 1 PM -> 7 members

**_1. Map lại Iron Triangle: trước và sau khi budget bị cắt:_**

**Trước sụ kiện:**

- Scope: phát triển app mobile (100%)
- Time: 3 tháng còn lại
- Budget: 800 triệu

**Sau sự kiện:**

- Scope: BẮT BUỘC phải giảm — đây là cạnh duy nhất có thể điều chỉnh
  - iOS thiếu 30%: payment integration, loyalty program
  - Android thiếu 50%: offline mode, payment, loyalty program
  - Backend thiếu 20%: analytics engine, admin dashboard
- Time: giữ nguyên (3 tháng)
- Buget: 560 triệu

-> Quality: gần như chắc chắn bị ảnh hưởng nếu không cắt scope kịp thời

-> Nhìn vào tình hình hiện tại, với budget giảm 30% và không thể thương lượng, cả 3 cạnh đều đang bị áp lực, cạnh SCOPE đang bị ảnh hưởng nặng nhất

-> Những options liên quan đến thay đổi COST sẽ bị reject, tự động loại trừ

**_2. Với 560 triệu còn lại, bạn có thể duy trì team trong bao lâu:_**

Budget ban đầu: 800 triệu, với 800 triệu chia đều cho 6 tháng, mỗi tháng tiền duy trì team bao gồm cả cơ sở hạ tầng, công cụ và chi phí vận hành là xấp xỉ 133 triệu

Đã tiêu: 3 × 133M = 400M  
Budget mới tổng: 560M  
Còn lại thực tế: 560M - 400M = 160M  
160M ÷ 133M = ~1.2 tháng

-> Chúng ta vẫn có thể duy trì team trong 1.2 tháng

**_3. Tính năng nào là MVP "sống còn" phải có? Tính năng nào có thể defer?_**

- iOS: Auth + catalog + cart + payment
- Android: Auth + catalog + cart + payment
- Backend: Core API + push notification cơ bản

**_4. Bạn communicate như thế nào với team để duy trì morale?_**

- Họp với team để thông báo tình hình hiện tại

> "3 tháng vừa rồi team mình đã làm được rất nhiều — iOS 70%, Android 50%, Backend 80%. Đó là nền tảng thực sự tốt.
>
> Tôi muốn chia sẻ thẳng với các bạn: do doanh thu Q1 giảm, budget dự án bị cắt 30%. Tôi đã nhận thông tin này và đang làm việc với ban lãnh đạo về hướng xử lý.
>
> Kế hoạch ngay bây giờ: chúng ta sẽ họp technical review vào [ngày cụ thể] để quyết định scope ưu tiên cho 3 tháng còn lại. Tôi sẽ đảm bảo mọi quyết định cắt scope đều có lý do rõ ràng và được communicate với stakeholder — không ai phải làm việc trong mơ hồ.
>
> Câu hỏi hoặc lo lắng nào, hãy nói thẳng với tôi."

**_5. Nếu timeline vẫn giữ nguyên 6 tháng, bạn sẽ ship gì?_**

- SHIP tại tháng 6:
  - iOS: Auth, catalog, cart, payment, push notification cơ bản
  - Android: Auth, catalog, cart, payment (bỏ offline mode)
  - Backend: Core API, push notification service

- DEFER sang Phase 2:
  - Loyalty program (iOS + Android)
  - Offline mode (Android)
  - Analytics dashboard cho store managers - Push notification campaign manager - Admin dashboard

Communicate với ban lãnh đạo: các features defer trên là features đã được promise  
→ cần họp riêng để align expectation trước khi announce
