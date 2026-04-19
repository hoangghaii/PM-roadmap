### Scenario A

> Công ty bạn có dự án rebuild website thương mại điện tử. Timeline: 4 tháng. Budget: 800 triệu. Team: 3 developers, 1 designer, 1 QA. Tuần 10/16, stakeholder yêu cầu tích hợp thêm payment gateway thứ ba (ban đầu chỉ có 2).

**Câu hỏi:** Phân tích impact và đề xuất 3 options.

**Trả lời:**

#### A. Phân tích

- Timeline tổng: 16 tuần (4 tháng)
- Thời điểm CR: Tuần 10/16
- Còn lại: 6 tuần
- Cost: 800 triệu
- Scope: Rebuild website

#### B. 3 options

- **Option 1:** Giữ nguyên TIME và COST, cắt SCOPE
  - Đưa yêu cầu tích hợp thêm payment gateway thứ 3 sang phase 2
  - Giữ nguyên COST và TIME
  - Risk: Thiếu feature mà stakeholder muốn thêm vào, stakeholder không hài lòng, mất cơ hội cạnh tranh

- **Option 2:** Thêm scope vào sprint hiện tại (không kéo TIME)
  - Reallocate 1 developer hiện tại tập trung làm payment gateway 7 ngày
  - Đẩy task thấp priority nhất của developer đó sang sprint sau
  - Giữ nguyên TIME, tăng COST nhẹ (overtime nếu cần)
  - Risk: Feature bị đẩy sang sau có thể ảnh hưởng stakeholder khác. Nếu dùng overtime → developer burnout

- **Option 3:** Giãn timeline 2 tuần
  - Giữ nguyên scope (có payment gateway thứ 3)
  - Deadline mới: +1 tuần
  - Cost TĂNG khoảng 70tr do trả lương team thêm 1 tuần (hoặc absorbed bởi vendor nếu là fixed-price contract — cần confirm)
  - Risk: Risk: Chậm release 1 tuần → nếu có đối thủ đang release cùng thời điểm,
    mất lợi thế cạnh tranh; delay có thể cascade sang marketing campaign

---

### Scenario B

> Dự án app mobile cho ngân hàng. Regulatory deadline không thể đổi: 30/09 (yêu cầu của Ngân hàng Nhà nước). Đến ngày 01/09, team báo cáo còn 40% features chưa xong.

**Câu hỏi:** Với deadline cứng không thể thay đổi, PM cần làm gì ngay lập tức?

**Trả lời:**

#### A. Phân tích

- Deadline không thể đổi: 30/09
- Thời điểm hiện tại: 01/09 (còn 30 ngày)
- Còn 40% features chưa xong
- Thêm developer về lý thuyết có thể giúp, nhưng với chỉ còn 30 ngày và trừ 10 ngày buffer, thực tế chỉ còn 20 ngày coding. Developer mới cần 3-5 ngày onboarding → thực chất chỉ contribute được ~15 ngày. Với banking app cần hiểu business logic phức tạp, risk onboarding cao hơn lợi ích. Khả thi hơn nếu thêm người đã quen domain.
- Không thể hoàn thành kịp 40% còn lại trong 30 ngày
- Cần trừ ít nhất 10 ngày để UAT, fix bug, test và đưa lên app store, ch play

#### B. Hành động

- Emergency meeting với Tech Lead trong 2-4 giờ đầu:
  - Breakdown 40% còn lại thành danh sách features cụ thể
  - Estimate effort từng feature (giờ công)
- Phân loại MoSCoW features: Chỉ giữ lại các features must-have, những features should-have/could-have sẽ được đẩy sang phase sau
- Raise sponsor + xác nhận ngân hàng nhà nước về scope
- Cắt scope officially (CR document)
- Ấn định ngày code done là 20/9, dành 10 ngày cuối cùng cho các công việc UAT, fix bugs, test và đưa lên app store, ch play
- Cho phép OT trong 2 tuần đầu (1-20/09), nhưng enforce code freeze trước 20/09 để toàn bộ team chuyển sang QA. Không để OT kéo sát ngày submit
- Tối đa hóa thời gian code bằng cách loại bỏ các cuộc họp không cần thiết, hỗ trợ các member các công việc làm ảnh hưởng đến thời gian code

---

### Scenario C

> Startup gọi vốn được vòng Seed, CEO quyết định dùng 30% số tiền đó để build MVP trong 2 tháng. PM bạn join ngày đầu và nhận thấy scope đã được promise với investor quá lớn cho 2 tháng.

**Câu hỏi:** Bạn là PM — bạn làm gì trong tuần đầu tiên?

**Trả lời:**

#### A. Phân tích

- Scope build hoàn chỉnh 1 MVP trong 2 tháng là quá lớn
- Bạn sẽ làm gì trong 5 ngày đầu tiên

#### B. Hành động

- Ngày 1 + 2: thu thập thông tin: audit thực tế:
  - Chia nhỏ features có trong scope thành những user story/task và estimate effort
  - Phân loại MoSCoW features
  - Đánh giá năng lực của team
  - Xác định nghẽn cổ chai: Có phụ thuộc đến api bên thứ 3 hay không? Những bên thứ 3 này sẽ làm ảnh hưởng đến dự án thế nào khi những bên này gặp vấn đề
- Ngày 3: Đưa ra các options phương án:
  - Dựa vào phân loại MoSCoW để xác định những core/ must-have futures
  - Tạo ra 2-3 kịch bản:
    - Kịch bản 1: Căt giảm SCOPE, phân loại MoSoCW feature, chỉ là must-have
      - Chỉ thực hiện những features cores, must-have
      - TIME giữ nguyên
      - COST giữ nguyên
      - SCOPE bị cắt
      - Risk: Thiếu features, CEO lo lắng vì không đúng cam kết ban đầu với Investor. Bạn cần giúp CEO giải thích rằng: "Investor thích một sản phẩm thực tế hoạt động tốt hơn là một bản demo đầy lỗi".
    - Kịch bản 2: Ship core, must-have features trong 2 tháng đầu và các features trong 2 tháng tiếp theo.
      - Core, must-have features được hoàn thành trong 2 tháng đầu và có thể demo được cho investor
      - Các features còn lại sẽ được hoàn thành trong 2 tháng tiếp theo
      - Investor sẽ tháy được sản phẩm chạy thực thế + roadmap crediable
      - TIME bị kéo dài thêm 2 tháng
      - COST sẽ bị tăng theo
      - Risk: Investor có accept "roadmap" thay vì "full product" không? → Đây là câu hỏi CEO phải trả lời, không phải PM
    - Kịch bản 3: Thuê thêm Freelancer hoặc Outsource
      - Thuê thêm 2 freelaner hoặc outsource trong 2 tháng: 25triệu/tháng/người \* 2tháng = 100triệu
      - COST tăng từ X -> X + 100triệu
      - Vẫn giữ được TIME và SCOPE
      - Risk: COST tăng đáng kể.
- Ngày 4: Họp với CEO và investor:
  - Chuẩn bị trước danh sách must-have features và danh sách các feature cho thể đẩy sang phase sau
  - Trình bày bằng những con số: Với tình hình nhân sự hiện tại, chúng ta cần tối thiểu 4 tháng để hoàn thành toàn bộ scope. Để kịp trong 2 tháng, chúng ta cần chọn các features core, must-have
  - Đưa ra danh sách must-have feature đã được chuẩn bị.
  - Scope đã được trình bày với investor bao gồm những gì cụ thể? Nếu chúng ta cắt 50% features, ai sẽ communicate với investor và communicate như thế nào? Đây là quyết định của CEO, không phải của tôi — nhưng tôi cần biết để plan đúng.
- Ngày 5: Thiết lập nhịp độ:
  - Chuẩn bị materials cho kick-off (draft sprint plan, update Jira) và chờ xác nhận từ CEO. Kick-off diễn ra sau khi CEO đã quyết định và — nếu cần — đã communicate với investor.
  - Thiết lập quy trình làm việc
