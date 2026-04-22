## Bài Tập: Áp Dụng MoSCoW Cho 1 Backlog Thực Tế

### Tình Huống

Bạn là Junior PM cho dự án **portal nội bộ HR** của một công ty 200 nhân viên. Deadline: 3 tháng. Team: 2 dev, 1 QA. Backlog hiện tại có 15 items sau — hãy phân loại MoSCoW:

```
Backlog items (chưa phân loại):
1. Nhân viên xem bảng lương của mình
2. HR upload file payslip hàng loạt
3. Nhân viên đăng ký nghỉ phép online
4. Manager approve/reject đơn nghỉ phép
5. Tự động tính số ngày phép còn lại
6. Báo cáo attendance tháng cho manager
7. Nhân viên xem sơ đồ tổ chức công ty
8. Chat nội bộ giữa nhân viên
9. Nhân viên cập nhật thông tin cá nhân
10. HR quản lý hợp đồng lao động (scan/upload)
11. Hệ thống đăng nhập SSO với Google Workspace
12. Push notification khi đơn được approve
13. Mobile app cho nhân viên
14. Báo cáo headcount theo phòng ban
15. Tích hợp với phần mềm kế toán (lương)
```

Trả lời

```
Phân loại MoSCoW features

Must have:
- 11. Hệ thống đăng nhập SSO với Google Workspace
- 3. Nhân viên đăng ký nghỉ phép online
- 5. Tự động tính số ngày phép còn lại
- 4. Manager approve/reject đơn nghỉ phép
- 1. Nhân viên xem bảng lương của mình


Should have:
- 9. Nhân viên cập nhật thông tin cá nhân
- 6. Báo cáo attendance tháng cho manager
- 10. HR quản lý hợp đồng lao động (scan/upload)
- 2. HR upload file payslip hàng loạt


Cound have:
- 12. Push notification khi đơn được approve
- 7. Nhân viên xem sơ đồ tổ chức công ty
- 14. Báo cáo headcount theo phòng ban


Won't have:
- 13. Mobile app cho nhân viên
- 8. Chat nội bộ giữa nhân viên
- 15. Tích hợp với phần mềm kế toán (lương)
```

---

### Câu Hỏi Reflection Sau Bài Tập

1. Bạn có đồng ý với gợi ý phân loại không? Có items nào bạn phân loại khác không? Tại sao?
2. Nếu sponsor yêu cầu thêm #13 Mobile app vào Must have, bạn xử lý thế nào?
3. Làm thế nào để lấy sự đồng thuận từ cả HR department, IT department, và CEO về MoSCoW này?
4. Sau 6 tuần dev, 3 Must-have items hoàn thành nhưng #5 (tính ngày phép) phức tạp hơn dự kiến, cần thêm 2 tuần — bạn làm gì?

Trả lời

1. Bạn có đồng ý với gợi ý phân loại không? Có items nào bạn phân loại khác không? Tại sao?
   - Tôi đồng ý với gợi ý phân loại, thật ra tôi cũng đã phân loại như vậy.

2. Nếu sponsor yêu cầu thêm #13 Mobile app vào Must have, bạn xử lý thế nào?
   - Việc đầu tiên: lấy thông tin của feature: họp nhanh 30p với techlead để lấy các thông tin sau: estimate thời gian làm, ai có đủ khả năng làm, có cần thuê outsource không? Hiện tại, với thời gian 3 tháng, cần phải hoàn thành tất cả 5 must-have features, thêm 1 should-have và 1 could-have, nếu làm thêm mobile app rất có khả năng sẽ trễ deadline, cho dù có OT thêm

   - Việc thứ 2: đưa ra các options lựa chọn:
     - Option 1: Cắt scope của features #13 mobile app
       - Phân lại #13 theo MoSCoW features, chỉ ship các core, must-have feature
       - Props: Vẫn có thể thêm mobile app
       - Cons: Vì vẫn phải là tất cả 7 features đồng thời thên #13 nên dù đã cắt scope thì vẫn phải kéo dài deadline, cost tăng không quá cao, tuy nhiên mobile app không đủ feature, team burnout,...
     - Option 2: Phân loại MoSCoW Cắt scope cho tất cả 5 features must-have, 1 should-have, 1 could-have và #13
       - Phân loại MoSCoW cho tất cả 5 features must-have, 1 should-have, 1 could-have và #13, chỉ ship các core, must-have features
       - Props: Keep deadline, keep cost
       - Cons: Tất cả các features chỉ có các tính năng core, must-have -> ảnh hưởng tới user experience
     - Option 3: Đẩy feature should-have và could-have sang phase sau, thay thế bằng feature #13
       - Ship 5 features must-have và #13
       - Props: Keep deadline, keep cost, đầy đủ 5 features must-have
       - Cons: 2 features should-have và could-have bị loại bỏ tạm thời có thể ảnh hưởng tới user experience
     - Option 4: Thuê thêm out-source
       - Thuê thêm 1-2 dev mobile để làm phần #13
       - Props: Keep deadline, keep scope
       - Cons: Cost tăng vì cần thuê thêm 1-2 dev mobile, mất 1-2 tuần tối thiểu on-board
     - Option 5: Giữ nguyên scope hiện tại, k thêm #13 vào must have
       - Giải thích chúng ta chưa cần tới mobile app hiện tại vì team dev FE sẽ thêm responsive màn hình cho mobile để web có thể dễ dàng sử dụng trên mobile browser với đầy đủ các tính năng và không lỗi.
       - Props: Keep deadline, keep scope, keep cost
       - Cons:
         - Responsive web ≠ native app: không có push notification native, không có app store distribution, offline mode hạn chế
         - Sponsor có thể có lý do cụ thể muốn native app (branding, app store visibility) — responsive web không đáp ứng được

   - Việc thứ 3: họp với sponsor, nêu ra các vấn đề nếu đưa #13 vào must-have, và đưa ra các options đẫ nêu ở trên cho sponsor lựa chọn, đồng thời đưa ra gợi ý chọn option 5, fallback option 3

3. Làm thế nào để lấy sự đồng thuận từ cả HR department, IT department, và CEO về MoSCoW này?
   - Bước 1 — Trước meeting (24-48h trước):
     - Gửi draft MoSCoW kèm giải thích ngắn cho từng nhóm (HR, IT, CEO) qua email
     - Mục tiêu: stakeholder đến meeting đã có context, không phải lần đầu nhìn thấy

   - Bước 2 — Trong meeting:  
     Agenda 60 phút:
     1. (10 phút) Trình bày tiêu chí phân loại — "Must have = không có thì portal không  
        hoạt động được; Should have = quan trọng nhưng có workaround"
     2. (30 phút) Walk through từng category, hỏi từng nhóm:  
        "HR team có items nào thấy phân loại chưa đúng không?"
     3. (15 phút) Xử lý disagreement
     4. (5 phút) Confirm đồng thuận, next steps

   - Bước 3 — Sau meeting:
     - Gửi email summary: "Chúng ta đã đồng thuận MoSCoW như sau..." và yêu cầu reply confirm
     - Email này là "paper trail" — quan trọng khi sau này có người muốn thay đổi scope

   - Kỹ thuật xử lý khi có conflict:  
      Nếu HR muốn #8 Chat vào Must have nhưng IT và CEO không đồng ý → dùng câu hỏi: "Nếu không có  
      chat, quy trình nghỉ phép của HR bị ảnh hưởng thế nào cụ thể?" Thường khi phân tích kỹ,  
      stakeholder tự nhận ra đó không phải Must have.

4. Sau 6 tuần dev, 3 Must-have items hoàn thành nhưng #5 (tính ngày phép) phức tạp hơn dự kiến, cần thêm 2 tuần — bạn làm gì?
   - Họp với team lead để xác định:
     - Technical issue (estimate sai từ đầu)? Hay requirements thay đổi (HR thêm rules phức tạp)?
     - Phần nào phức tạp: tính toán ngày, edge cases (nghỉ bù, lễ, carryover), hay integration với dữ liệu cũ?
   - Nếu phức tạp vì requirements thay đổi → đây là scope creep, sponsor một phần chịu trách nhiệm. Nếu estimate sai từ đầu → đây là vấn đề của team, và PM cần owned nó.

   - Đưa ra các options:
     - Option 1: Kéo dài deadline
       - Kéo dài deadline thêm 2 tuần để hoàn thành feature #5 và feature thứ 6 (#1)
       - Props: Keep scope
       - Cons: Cost tăng vì deadline bị kéo dài, sponsor không thích
     - Option 2: Cắt giảm scope của feature thứ 6 (#1)
       - Phân loại MoSCoW của feature thứ 6 (#1), chỉ ship core, must-have feature thứ 6 (#1) và toàn bộ các feature khác
       - Props: Keep scope
       - Cons: Feature thứ 6 (#1) không hoàn thiện đầy đủ tính năng
     - Option 3: Cắt giảm scope của feature #5
       - Phân loại MoSCoW của feature #5, chỉ ship core, must-have, đưa các phần còn lại và phần phức tạp sang phase sau (Deliver phiên bản simplified của #5: chỉ tính ngày phép cơ bản (annual leave quota - used = remaining). Defer các edge cases (carryover, phép bù, multiple leave types) sang phase 2.)
       - Props: Keep deadline, cost
       - Cons: Feature #5 không hoàn thiện đầy đủ tính năng
     - Option 4: Team OT
       - Cho team OT có kiểm soát để hoàn thành đầy đủ feature #5
       - Props: Keep deadline, scope
       - Cons: Team burnout, có thể có critical bugs

   - Họp với sponsor: đưa ra các vấn đề phức tạp hơn so với dự kiến và lý do tại sao không nhìn thấy được trước, đồng thời đưa ra các options đã được nêu ở trên để sponsor lựa chọn.
