Chào bạn, với vai trò là một chuyên gia quản lý dự án có chứng chỉ CAPM, PMP và PMI-ACP, tôi xin tóm tắt chi tiết nội dung về cách tài liệu hóa việc kiểm soát dự án trong các dự án **Thích ứng (Adaptive/Agile)**.

Dưới đây là bản tóm tắt chi tiết được trình bày dưới dạng các gạch đầu dòng có cấu trúc, giúp bạn nắm vững phương pháp kiểm soát theo chuẩn kiến thức PMI:

---

# TÓM TẮT: KIỂM SOÁT DỰ ÁN THÍCH ỨNG (ADAPTIVE/AGILE)

Trong môi trường phát triển **Thích ứng**, việc kiểm soát dự án không dựa vào các đường cơ sở cố định (Baselines) mà tập trung vào **Tính minh bạch (Transparency)**, **Sự thích ứng liên tục (Adaptability)** và **Giá trị thực tế được bàn giao (Value Delivered)**.

## 1. Cách Tài Liệu Hóa Quy Trình Kiểm Soát Dự Án Thích Ứng (Project Controls)

Quy trình kiểm soát trong dự án Agile vận hành dựa trên nguyên lý **Thực nghiệm (Empiricism)**, tức là quan sát dữ liệu thực tế để ra quyết định thay vì chỉ dựa vào dự báo dài hạn.

- **Đo lường Vận tốc của Team (Team Velocity Tracking):**
  - **Cách thực hiện:** Cuối mỗi chu kỳ (Iteration/Sprint), Quản lý Dự án (**PM**)/Scrum Master tổng hợp lại số lượng **Story Points** (hoặc User Stories) mà đội nhóm đã thực sự hoàn thành, đáp ứng tiêu chuẩn **Definition of Done (DoD)**.
  - **Mục đích:** Tài liệu hóa chỉ số này giúp **PM dự báo năng suất thực tế** của đội nhóm cho các chu kỳ tiếp theo mà không gây áp lực về thời gian một cách vô lý.

- **Tài liệu hóa qua các Công cụ Trực quan (Visual Controls):**
  - **Bảng Kanban/Scrum Board:** Dùng để tài liệu hóa trạng thái thời gian thực của mọi công việc (`To Do`, `In Progress`, `Testing`, `Done`). Việc theo dõi bảng giúp phát hiện **nút thắt cổ chai (Bottlenecks)** nếu có quá nhiều thẻ công việc tồn đọng trong một cột.
  - **Biểu đồ Tiến độ (Progress Charts):**
    - **Biểu đồ Burn-down:** Tài liệu hóa lượng công việc **còn lại** theo từng ngày trong một chu kỳ. Đường thực tế dốc xuống càng gần đường lý thuyết, chứng tỏ sự kiểm soát tiến độ càng tốt.
    - **Biểu đồ Burn-up:** Tài liệu hóa tổng lượng công việc **đã hoàn thành tích lũy** theo thời gian, đồng thời thể hiện sự thay đổi của **phạm vi dự án (Scope line)**.

## 2. Các Sản Vật/Tài Liệu Đặc Trưng trong Dự án Thích ứng (Adaptive Artifacts)

PMI chia các tài liệu cốt lõi của Agile thành ba nhóm chính để đảm bảo mọi bên liên quan có chung một góc nhìn.

### A. Product Backlog (Danh sách Sản phẩm Tồn đọng)

- **Bản chất:** Là tài liệu **động**, tổng hợp tất cả các tính năng, yêu cầu, sửa lỗi và yêu cầu kỹ thuật cần thiết cho sản phẩm. Nó được sắp xếp liên tục theo thứ tự ưu tiên dựa trên **Giá trị Kinh doanh (Business Value)**.
- **Người sở hữu:** **Product Owner (PO)** là người duy nhất có quyền quyết định thêm, sửa, xóa hoặc thay đổi thứ tự ưu tiên của các mục.
- **Sự tiến hóa (Refinement):** Khác với tài liệu cố định, Product Backlog được **"làm mịn" (Refinement)** định kỳ. Các yêu cầu ưu tiên cao luôn chi tiết, rõ ràng; các yêu cầu ở dưới có thể mơ hồ hơn.

### B. Iteration / Sprint Backlog (Danh sách Chu kỳ Tồn đọng)

- **Bản chất:** Là tập hợp các **User Stories** được chọn ra từ Product Backlog để phát triển trong chu kỳ hiện tại, kèm theo các **Task kỹ thuật chi tiết** do đội nhóm thực thi phân rã.
- **Người sở hữu:** **Project/Development Team**. Khi Sprint bắt đầu, phạm vi của Sprint Backlog được **khóa lại (fixed)** để đội nhóm tập trung tối đa và tránh bị xao nhãng bởi các yêu cầu thay đổi đột xuất.

### C. Product Increment (Phần Tăng trưởng Sản phẩm)

- **Bản chất:** Là **sản phẩm đầu ra thực tế**, có thể chạy được và có giá trị sử dụng sau khi kết thúc một chu kỳ. Nó là tổng hợp của tất cả các User Stories đã hoàn thành trong Sprint đó cộng với giá trị tích lũy từ các Sprint trước.
- **Điều kiện bắt buộc:** Mọi phần việc chỉ được tính vào Product Increment nếu nó vượt qua bộ tiêu chuẩn **Definition of Done (DoD)**.

## 3. Các Tài liệu Bổ Trợ Kiểm Soát Hành Vi (Social/Process Artifacts)

Để kiểm soát chất lượng quy trình và hành vi của đội nhóm, cần có các thỏa thuận được văn bản hóa:

| Tài liệu (Artifact)               | Mục đích & Nội dung                                                                                                                                                            |
| :-------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Team Charter / Team Agreement** | Quy định các **quy tắc ứng xử nội bộ** do chính đội nhóm tự đặt ra (ví dụ: quy tắc giao tiếp, tương tác).                                                                      |
| **Definition of Ready (DoR)**     | Bộ tiêu chí kiểm soát **đầu vào** của một User Story trước khi đưa vào lập kế hoạch chu kỳ. Đảm bảo yêu cầu đã đủ rõ ràng, có tiêu chí nghiệm thu và có thể ước lượng được.    |
| **Definition of Done (DoD)**      | Bộ tiêu chí kiểm soát **chất lượng đầu ra** của sản phẩm. Đóng vai trò là **chốt chặn chất lượng tối thượng** của dự án (ví dụ: yêu cầu về mã nguồn, kiểm thử, và độ ổn định). |

### Tóm Lược Tư Duy Kiểm Soát trong Agile

- **Dự án Dự đoán:** Kiểm soát bằng cách yêu cầu mọi người **tuân thủ kế hoạch trên giấy**.
- **Dự án Thích ứng:** Kiểm soát bằng cách **tài liệu hóa các chỉ số thực tế** (Vận tốc, biểu đồ Burn-down) và bám chặt vào **tiêu chuẩn chất lượng (DoD)** để đảm bảo cứ hết một chu kỳ lặp là dự án lại trao đi một phần **giá trị thực sự** cho người dùng.
