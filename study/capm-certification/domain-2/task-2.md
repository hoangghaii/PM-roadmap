Chào bạn, với vai trò là một chuyên gia quản lý dự án giàu kinh nghiệm (đã có chứng chỉ CAPM, PMP, PMI-ACP...), tôi xin tóm tắt chi tiết và đầy đủ các kiến thức bạn cung cấp về việc **lập kế hoạch và kiểm soát dự án** theo chuẩn kiến thức của PMI.

Dưới đây là bản tóm tắt được tổ chức thành các mục chính như sau:

---

# TÓM TẮT QUẢN LÝ VÀ KIỂM SOÁT DỰ ÁN

Để làm chủ việc quản lý và kiểm soát một dự án, **Quản lý Dự án (PM)** cần phối hợp nhuần nhuyễn giữa việc lập tiến độ, quản lý cấu trúc công việc, kiểm soát chất lượng và tích hợp toàn diện.

## 1. Hiểu về Tiến độ Dự án & Phương pháp Đường găng (CPM)

### 1.1. Khái niệm Đường Găng (Critical Path)

- **Đường găng (Critical Path)** là chuỗi các công việc có **tổng thời gian dài nhất** từ lúc bắt đầu đến khi kết thúc dự án.
- Công việc nằm trên đường găng có **Float = 0** (không có thời gian dự phòng).
- Nếu một công việc trên đường găng bị trễ, **toàn bộ dự án sẽ bị trễ**.

### 1.2. Kỹ thuật Tính toán Đường Găng (Forward & Backward Pass)

Để xác định đường găng, PM sử dụng sơ đồ mạng lưới dự án và tính toán qua hai lượt:

- **Lượt Tiến (Forward Pass):** Tính toán ngày bắt đầu sớm nhất (**Early Start - ES**) và ngày kết thúc sớm nhất (**Early Finish - EF**) của từng công việc từ trái sang phải.
  - **Công thức:** $EF = ES + \text{Duration} - 1$
- **Lượt Lùi (Backward Pass):** Tính toán ngày kết thúc muộn nhất (**Late Finish - LF**) và ngày bắt đầu muộn nhất (**Late Start - LS**) từ phải sang trái (bắt đầu từ ngày kết thúc dự án).
  - **Công thức:** $LS = LF - \text{Duration} + 1$
- **Tính Thời gian Dự phòng (Total Float):** Xác định độ trễ bằng công thức:
  - $\text{Float} = LS - ES$ hoặc $\text{Float} = LF - EF$.
  - **Kết quả:** Công việc có $\text{Float} = 0$ chính là thành viên của **Đường Găng**.

## 2. Tính toán Biến động Tiến độ (Schedule Variance - SV)

Trong giai đoạn Giám sát & Kiểm soát, PM sử dụng **Quản lý giá trị thu được (Earned Value Management - EVM)** để đo lường hiệu suất thực tế so với kế hoạch.

### 2.1. Các Chỉ số Lõi của EVM

- **PV (Planned Value - Giá trị Kế hoạch):** Lượng ngân sách dự kiến phải chi cho phần công việc dự kiến hoàn thành đến thời điểm hiện tại.
- **EV (Earned Value - Giá trị Thu được):** Lượng ngân sách phân bổ cho phần công việc **thực tế đã hoàn thành** tính đến hiện tại.
  - **Công thức:** $EV = \% \text{ Hoàn thành thực tế} \times \text{Tổng ngân sách BAC}$
- **AC (Actual Cost - Chi phí Thực tế):** Số tiền thực tế đã chi ra để hoàn thành công việc.

### 2.2. Công thức Tính Biến động Tiến độ

- **Schedule Variance (SV):** Đo lường sự chênh lệch giữa tiến độ thực tế và kế hoạch.
  - **Công thức:** $\text{SV} = \text{EV} - \text{PV}$
- **Schedule Performance Index (SPI):** Đo lường hiệu suất tiến độ.
  - **Công thức:** $\text{SPI} = \frac{\text{EV}}{\text{PV}}$

### 2.3. Cách Đọc Kết quả

- **SV< 0 (hoặc SPI< 1):** Dự án đang **Chậm tiến độ** ($\text{Behind Schedule}$) - _Nguy hiểm._
- **SV = 0 (hoặc SPI = 1):** Dự án đang **Đúng tiến độ** ($\text{On Schedule}$).
- **SV > 0 (hoặc SPI > 1):** Dự án đang **Vượt tiến độ/Nhanh hơn kế hoạch** ($\text{Ahead of Schedule}$).

## 3. Giải thích WBS (Work Breakdown Structure) & Work Packages

### 3.1. Cấu trúc phân rã công việc (WBS)

- **Định nghĩa:** Là sự phân rã có tính cấp bậc, hướng theo **sản phẩm đầu ra (Deliverable-oriented)** về toàn bộ phạm vi công việc.
- **Quy tắc 100% (100% Rule):** WBS phải bao hàm **100%** công việc của dự án (không thiếu, không thừa). Tổng công việc của các nhánh con phải bằng 100% công việc của nhánh cha.
- **Định dạng:** WBS không phải là danh sách hành động, mà là danh sách các **danh từ/sản phẩm** được chia nhỏ dần.

### 3.2. Gói công việc (Work Package)

- **Định nghĩa:** Là **cấp độ thấp nhất của WBS**, nằm ở dưới cùng của mỗi nhánh phân rã.
- **Đặc điểm:** Đây là nơi chi phí và thời gian thực hiện công việc có thể được **ước lượng đáng tin cậy nhất** và có thể giao trách nhiệm quản lý cho một người cụ thể.
- **Kích thước chuẩn (Quy tắc 8/80):** Một Work Package lý tưởng nên có thời lượng thực hiện không ít hơn **8 giờ** và không quá **80 giờ làm việc** (tương đương từ 1 ngày đến 2 tuần).
- **Từ điển WBS (WBS Dictionary):** Tài liệu đi kèm để giải thích chi tiết nội dung, tiêu chí nghiệm thu, rủi ro và nhân sự chịu trách nhiệm cho từng Work Package.

## 4. Áp dụng Kế hoạch Quản lý Chất lượng (Quality Management Plan)

Quản lý chất lượng theo chuẩn PMI là một quy trình xuyên suốt gồm 3 bước:

1. **Lập kế hoạch Chất lượng (Plan Quality Management):** Xác định **tiêu chuẩn chất lượng** áp dụng cho dự án và các tiêu chí nghiệm thu sản phẩm (Ví dụ: yêu cầu về khả năng tương thích của tính năng).
2. **Đảm bảo Chất lượng (Manage Quality / Quality Assurance - QA):** Tập trung vào **Quy trình**. Đảm bảo team đang sử dụng đúng các quy trình và tiêu chuẩn kỹ thuật (Ví dụ: thực hiện kiểm toán quy trình, Code Review).
3. **Kiểm soát Chất lượng (Control Quality - QC):** Tập trung vào **Sản phẩm**. Trực tiếp kiểm tra sản phẩm đầu ra xem có đạt tiêu chuẩn hay không trước khi bàn giao (Ví dụ: thực hiện các ca kiểm thử như SIT để bắt lỗi).

## 5. Áp dụng Kế hoạch Quản lý Tích hợp (Integration Management Plan)

**Quản lý tích hợp** là **nhiệm vụ tối thượng** của Project Manager, có vai trò liên kết và thống nhất tất cả các quy trình quản trị lại với nhau thành một khối chỉnh thể.

### 5.1. Cách PM áp dụng Quản lý Tích hợp trong thực tế

- **Cân bằng các ràng buộc xung đột:** Khi có yêu cầu thay đổi về tiến độ, PM tích hợp phải đánh giá tác động toàn diện lên **Chi phí** (ví dụ: chi phí làm thêm giờ) và **Chất lượng** (ví dụ: cắt giảm thời gian kiểm thử).
- **Quản lý các điểm giao tiếp (Interfaces):** Đảm bảo thông tin và sản phẩm chuyển giao giữa các giai đoạn một cách **đồng bộ** và mượt mà (Ví dụ: truyền đạt thiết kế từ Designer sang Dev một cách chính xác).
- **Thực hiện Kiểm soát Thay đổi Tích hợp (Integrated Change Control):** Quy trình xử lý yêu cầu thay đổi bao gồm 4 bước chính:
  1. **Ghi nhận:** Ghi lại yêu cầu thay đổi vào **Change Log**.
  2. **Đánh giá Tác động:** Đánh giá tác động **toàn diện** lên mọi khía cạnh (Phạm vi, Thời gian, Chi phí, Chất lượng, Rủi ro).
  3. **Trình phương án:** Đưa ra phương án xử lý lên **Hội đồng phê duyệt thay đổi (CCB)**.
  4. **Cập nhật Kế hoạch:** Cập nhật lại **kế hoạch gốc (Baselines)** nếu được duyệt và thông báo cho toàn đội triển khai.

---

**Tóm lại:** Sự kết hợp chặt chẽ giữa việc chia nhỏ công việc (**WBS**), kiểm soát tiến độ qua **Đường Găng (CPM)** và **EVM**, cùng với việc kiểm soát chất lượng theo chu trình 3 bước, và khả năng **Tích hợp** các khía cạnh quản trị, sẽ tạo nên một nền tảng vững chắc cho dự án thành công.
