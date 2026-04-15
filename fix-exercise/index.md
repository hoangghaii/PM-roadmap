Được rồi, để thầy review bài kỹ nhé. Nhìn chung cấu trúc bài làm tốt — có Change Request rõ ràng,
có 3 options. Nhưng có 4 lỗi cần sửa, từ nhỏ đến lớn.

---

Nhận Xét Tổng Quan

Làm Tốt ✅

- Change Request format đúng chuẩn, đủ các trường
- 3 options hợp lý về hướng xử lý
- Biết tính impact scope và timeline  

---

Lỗi Cần Sửa

Lỗi 1 (Nhỏ): "Time: 6 tuần" — Thiếu context

Bài làm viết:

▎ Time: 6 tuần

Vấn đề: 6 tuần là thời gian còn lại, không phải tổng timeline. Người đọc CR không biết dự án đang
ở đâu.

Sửa thành:  
 Timeline tổng: 16 tuần (4 tháng)  
 Thời điểm CR: Tuần 10/16  
 Còn lại: 6 tuần

---

Lỗi 2 (Nhỏ): Tính cost chưa rõ assumption

Bài làm viết:

▎ +7 ngày × rate developer = +21tr VND

Vấn đề: Rate 3tr/ngày lấy từ đâu? Là 1 developer hay 3? Người approve CR không biết basis tính  
 toán.

Sửa thành:  
 Impact đến Cost: +7 ngày công × 1 developer × 3tr/ngày = +21tr VND
(Giả định rate developer hiện tại: 3tr/ngày)

---

Lỗi 3 (Quan trọng): Option 2 — "Thuê thêm 1 dev" có vấn đề logic

Bài làm viết:

▎ Thuê thêm 1 dev để làm, tăng cost thêm 21tr, giữ nguyên timeline

Vấn đề: Đây là ứng dụng sai của Iron Triangle. Thuê dev mới không tự động giữ được timeline vì:

- Dev mới cần 2-5 ngày onboarding để hiểu codebase
- Dev hiện tại phải dừng lại để hỗ trợ người mới
- Fred Brooks đã nói: "Adding manpower to a late project makes it later"

Option đúng ở đây phải là reallocation nội bộ: giữ nguyên team, ưu tiên dev hiện tại làm gateway
trước, và đẩy task khác sang sau.

Sửa thành:  
 Option 2: Thêm scope vào sprint hiện tại (không kéo timeline)

- Reallocate 1 developer hiện tại tập trung làm payment gateway 7 ngày
- Đẩy task thấp priority nhất của developer đó sang sprint sau
- Giữ nguyên timeline, tăng cost nhẹ (overtime nếu cần)
- Risk: Feature bị đẩy sang sau có thể ảnh hưởng stakeholder khác  
   Nếu dùng overtime → developer burnout  

---

Lỗi 4 (Quan trọng nhất): Option 3 — "Giữ nguyên cost" là SAI về bản chất

Bài làm viết:

▎ Kéo dài timeline thêm tối thiểu 1 tuần, giữ nguyên cost

Vấn đề: Đây là hiểu nhầm Iron Triangle nghiêm trọng nhất.

Kéo dài timeline 1 tuần nghĩa là team làm việc thêm 1 tuần → lương phải trả thêm → cost TĂNG,  
 không giữ nguyên.

3 developers × 1 tuần × 5 ngày × 3tr/ngày = +45tr VND  
 1 designer × 1 tuần = +15tr VND
1 QA × 1 tuần = +10tr VND  
 = Tổng tăng ≈ +70tr VND (chưa kể PM)

Trừ một trường hợp duy nhất cost không tăng: hợp đồng fixed-price (client trả cố định, vendor  
 chịu chi phí phát sinh). Nhưng ngay cả khi đó, cost thực của vendor vẫn tăng.

Sửa thành:  
 Option 3: Kéo dài timeline thêm 1 tuần

- Giữ nguyên scope (có payment gateway thứ 3)
- Deadline mới: +1 tuần
- Cost TĂNG khoảng 70tr do trả lương team thêm 1 tuần  
  (hoặc absorbed bởi vendor nếu là fixed-price contract — cần confirm)
- Risk: Chậm release 1 tuần → nếu có đối thủ đang release cùng thời điểm,  
   mất lợi thế cạnh tranh; delay có thể cascade sang marketing campaign  

---

Bảng Tổng Hợp Sau Khi Sửa

┌────────────┬─────────────────────┬─────────────────┬──────────────┐
│ │ Option 1 │ Option 2 │ Option 3 │  
 ├────────────┼─────────────────────┼─────────────────┼──────────────┤
│ Scope │ Cắt (defer gateway) │ Giữ nguyên │ Giữ nguyên │  
 ├────────────┼─────────────────────┼─────────────────┼──────────────┤
│ Timeline │ Giữ nguyên │ Giữ nguyên │ +1 tuần │  
 ├────────────┼─────────────────────┼─────────────────┼──────────────┤  
 │ Cost │ Giữ nguyên │ +nhẹ (overtime) │ +~70tr │  
 ├────────────┼─────────────────────┼─────────────────┼──────────────┤  
 │ Risk chính │ Thiếu feature │ Dev burnout │ Late release │
└────────────┴─────────────────────┴─────────────────┴──────────────┘

---

Điểm Số: 7/10

Trừ điểm:

- -1 Option 2 logic sai (Brooks' Law)
- -2 Option 3 kết luận cost sai — đây là lỗi nghiêm trọng về Iron Triangle  

Bài học cốt lõi: Trong Iron Triangle, timeline và cost luôn liên quan. Muốn kéo dài thời gian mà
không tăng cost → chỉ có thể nếu giảm scope (bớt người) hoặc hợp đồng fixed-price absorbs phần  
 chênh lệch.
