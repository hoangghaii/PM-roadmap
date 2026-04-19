Nhận Xét Bài Giải Scenario B

Bài làm của bạn có nền tảng tốt, đặc biệt ở phần phân tích bối cảnh và options. Dưới đây là nhận
xét chi tiết từng phần:

---

Phân Tích Bối Cảnh — Tốt

Mapping Iron Triangle trước/sau rõ ràng. Chỉ một điểm cần chỉnh: cột "Sau sự kiện" nên ghi:

- DEADLINE: Không đổi (theo yêu cầu của stakeholder — đây là vấn đề)
- Không phải "deadline ban đầu + 8-10 tuần" vì đó là nhu cầu thực tế, còn yêu cầu của CFO là giữ
  nguyên deadline  

---

Câu 1: Tại Sao Nguy Hiểm — Khá Tốt, Thiếu 2 Điểm Quan Trọng

Bạn đã xác định đúng 2 rủi ro lớn nhất. Tuy nhiên còn thiếu:

- Rủi ro hợp đồng: Module kế toán không nằm trong contract. Nếu bạn nói "OK" với CFO, công ty bạn
  có thể bị ép làm việc miễn phí hoặc bị kiện nếu không deliver đúng hạn
- Rủi ro nội bộ khách hàng: CFO và COO có thể đang có conflict nội bộ (CFO muốn kế toán, COO  
  không biết hoặc không đồng ý) — bạn bị kéo vào chính trị nội bộ của khách hàng nếu không escalate

---

Câu 2: Bước Đầu Tiên — Sai Thứ Tự Ưu Tiên

Đây là điểm cần điều chỉnh nhiều nhất.

Vấn đề: Bạn đặt "họp tech lead" trước "leo thang với sponsor". Trong thực tế, thứ tự đúng là:

Bước 0 (NGAY TRÊN ĐIỆN THOẠI): Không cam kết gì với CFO  
 → "Cảm ơn anh/chị, tôi cần đánh giá impact và sẽ phản hồi trong 24 giờ"

Bước 1 (Trong vài giờ đầu): Báo ngay cho management nội bộ của bạn  
 → PM không tự xử lý tình huống vượt scope contract một mình

Bước 2 (Song song): Họp nhanh với tech lead  
 → Chỉ cần estimate sơ bộ (~30 phút), không cần phân rã chi tiết ngay  
 → Mục đích: có số liệu khi gặp COO

Bước 3 (Trong ngày): Gặp COO + CFO cùng lúc  
 → Đừng gặp COO trước khi có data từ tech lead

Một điểm thêm hay của bạn (bottleneck API bên thứ 3) là đúng hướng nhưng nên để vào phase sau khi
đã được approve, không phải làm ngay trong 24 giờ đầu.

---

Câu 3: Present Với COO — Cần Cải Thiện Tone Và Structure

Vấn đề trong draft của bạn:

1. "chúng ta sẽ thêm module kế toán" — nghe như đã quyết định rồi, nên đổi thành "CFO đề xuất  
   thêm"
2. "không biết ngày COO đã biết..." — quá informal, có thể làm COO cảm thấy bị thiếu tôn trọng
3. Thiếu data — khi gặp COO, bạn cần đến với con số, không chỉ vấn đề  

Draft cải thiện:

▎ "Anh [COO], tôi nhận được cuộc gọi từ CFO sáng nay với đề xuất thêm module kế toán vào scope  
 ▎ hiện tại, giữ nguyên budget và deadline.
▎  
 ▎ Tôi đã làm việc với tech lead để đánh giá sơ bộ: module kế toán cần thêm 8–10 tuần effort,  
 ▎ trong khi dự án còn 4 tháng với team hiện tại đang full capacity.
▎  
 ▎ Đây là thay đổi lớn nằm ngoài contract ban đầu, tôi cần anh xác nhận: đây có phải quyết định  
 ▎ chính thức từ phía khách hàng không? Và chúng ta có muốn xử lý theo quy trình change request
▎ không?  
 ▎  
 ▎ Tôi có 3 options để trình bày..."

---

Câu 4: Options — Thiếu 1 Option Quan Trọng

Options 1–4 của bạn đúng hướng. Một số điểm cần sửa:

┌─────────────────┬──────────────────────────────────────────────────────────────────────────┐  
 │ Option │ Nhận xét │  
 ├─────────────────┼──────────────────────────────────────────────────────────────────────────┤  
 │ Option 1 (Cắt │ Cần specify rõ: ai quyết định cắt feature nào — đây không phải quyết │
│ scope) │ định của PM một mình │
├─────────────────┼──────────────────────────────────────────────────────────────────────────┤  
 │ Option 2 │ Lỗi logic: Module kế toán (GL, AP/AR) cần developer có domain knowledge │
│ (Outsource) │ kế toán, không thể dùng junior outsource. Cần senior specialist, cost │  
 │ │ thực tế cao hơn nhiều │
├─────────────────┼──────────────────────────────────────────────────────────────────────────┤  
 │ Option 3 (Kéo │ "Mất market timing" không phù hợp cho ERP factory — nên đổi thành: ảnh │
│ deadline) │ hưởng kế hoạch vận hành nhà máy, chi phí PM team kéo dài │  
 ├─────────────────┼──────────────────────────────────────────────────────────────────────────┤
│ Option 4 (OT) │ Nên ghi rõ: Không khuyến nghị │  
 └─────────────────┴──────────────────────────────────────────────────────────────────────────┘

Option bạn bỏ sót (quan trọng nhất):

▎ Option 5: Defer sang Phase 2 — ký hợp đồng mới  
 ▎ - Giữ nguyên 4 modules theo contract, deliver đúng hạn  
 ▎ - Module kế toán = dự án riêng, hợp đồng riêng, timeline riêng  
 ▎ - Pros: Bảo vệ contract hiện tại, không rủi ro pháp lý, tạo doanh thu mới  
 ▎ - Cons: CFO có thể không hài lòng trong ngắn hạn

Đây thường là option PM senior nhất sẽ chọn vì bảo vệ cả hai phía.

---

Câu 5: Hậu Quả — Tốt, Thiếu Khía Cạnh Pháp Lý

Bạn đã cover tốt phần team và relationship. Còn thiếu:

- Rủi ro pháp lý: Nếu bạn verbal commit với CFO → công ty bạn có thể bị ép deliver module không  
  có trong contract, hoặc bị kiện nếu trễ/không deliver
- Tạo precedent xấu: CFO (và các stakeholder khác) học được rằng có thể bypass process bằng cách
  gọi thẳng cho PM → những lần sau sẽ tiếp tục làm vậy

---

Tổng Kết

┌──────────┬───────────────────────────┬──────────────────────────────────────────────┐
│ Phần │ Điểm mạnh │ Cần cải thiện │  
 ├──────────┼───────────────────────────┼──────────────────────────────────────────────┤  
 │ Bối cảnh │ Mapping rõ ràng │ Sửa nhỏ cột "Sau sự kiện" │
├──────────┼───────────────────────────┼──────────────────────────────────────────────┤  
 │ Câu 1 │ Xác định 2 rủi ro chính │ Thêm rủi ro hợp đồng + nội bộ khách hàng │  
 ├──────────┼───────────────────────────┼──────────────────────────────────────────────┤  
 │ Câu 2 │ Có đủ các bên cần gặp │ Sai thứ tự — escalate trước, tech detail sau │  
 ├──────────┼───────────────────────────┼──────────────────────────────────────────────┤  
 │ Câu 3 │ Đúng người cần gặp │ Tone quá casual, thiếu data, thiếu options │  
 ├──────────┼───────────────────────────┼──────────────────────────────────────────────┤  
 │ Câu 4 │ 4 options đủ chiều │ Thiếu Option 5 (Phase 2), lỗi logic Option 2 │  
 ├──────────┼───────────────────────────┼──────────────────────────────────────────────┤  
 │ Câu 5 │ Cover team + relationship │ Thêm rủi ro pháp lý + precedent │  
 └──────────┴───────────────────────────┴──────────────────────────────────────────────┘

Điểm tự đánh giá theo checklist bài tập: ~10-11/15 — đang đúng hướng, cần luyện thêm về formal  
 change management process và thứ tự ưu tiên khi escalate.
