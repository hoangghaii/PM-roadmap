Chào bạn. Với vai trò là một Quản lý Dự án cấp cao có chứng chỉ CAPM, PMP và kinh nghiệm hơn 5 năm, tôi xin tóm tắt chi tiết quy trình quản lý dự án theo phương pháp **Dự đoán (Predictive/Plan-based)** này.

Đây là hướng dẫn chi tiết về cách **tài liệu hóa quy trình kiểm soát dự án**, **nhận diện các tài liệu cốt lõi**, và **cách tính toán biến động chi phí/tiến độ** theo chuẩn PMI.

---

## Tóm tắt Quy trình Kiểm soát Dự án Dự đoán

Việc kiểm soát dự án theo phương pháp Dự đoán đòi hỏi sự quản lý dựa trên **hệ thống** thay vì cảm tính, thông qua việc tuân thủ nghiêm ngặt các **Đường cơ sở (Baselines)** và các **Tài liệu bàn giao (Artifacts)** đã được quy định.

### 1. Cách thức Tài liệu hóa Quy trình Kiểm soát Dự án (Project Controls Documentation)

Quy trình kiểm soát được tài liệu hóa qua ba bước cốt lõi sau:

- **Thiết lập Kế hoạch Đo lường Hiệu suất (Performance Measurement Baseline - PMB):** Đây là tài liệu tích hợp, đóng vai trò là "thước đo" gốc, bao gồm ba thành phần chính:
  - **Scope Baseline (Đường cơ sở Phạm vi)**
  - **Schedule Baseline (Đường cơ sở Tiến độ)**
  - **Cost Baseline (Đường cơ sở Chi phí)**
- **Ghi nhận Nhật ký Dự án (Project Logs & Registers):** Cần liên tục cập nhật dữ liệu vào các tài liệu động (**Living Documents**) bao gồm:
  - **_Issue Log (Nhật ký vấn đề):_** Ghi lại các sự cố đang xảy ra, chỉ định người chịu trách nhiệm và thời hạn xử lý.
  - **_Change Log (Nhật ký thay đổi):_** Ghi lại trạng thái của mọi yêu cầu thay đổi (ví dụ: Đang chờ duyệt, Đã duyệt, hoặc Bị bác bỏ).
- **Tài liệu hóa Báo cáo Hiệu suất (Performance Reporting):** Bao gồm việc chuyển đổi dữ liệu thô thành thông tin có ý nghĩa để hỗ trợ ra quyết định, bao gồm:
  - **_Work Performance Data (Dữ liệu hiệu suất công việc):_** Các số liệu thô thu thập từ thực tế (ví dụ: chi phí phát sinh, thời gian hoàn thành).
  - **_Work Performance Information (Thông tin hiệu suất công việc):_** Dữ liệu đã được tính toán và phân tích dựa trên các chỉ số **EVM (Earned Value Management)** để đánh giá dự án đang có xu hướng nhanh hay chậm, lỗ hay lãi.
  - **_Work Performance Reports (Báo cáo hiệu suất công việc):_** Các tài liệu hoàn chỉnh (Biểu đồ, Dashboard, Báo cáo tuần) được gửi đến các bên liên quan.

### 2. Các Tài liệu/Sản vật Đặc trưng trong Dự án Dự đoán (Predictive Project Artifacts)

PM cần quản lý các tài liệu quan trọng được phân loại theo mục đích sử dụng:

#### A. Nhóm Tài liệu Khởi tạo (Initiation Artifacts)

- **Project Charter (Điều lệ dự án):** Tài liệu chính thức khởi tạo dự án và cấp quyền cho Quản lý Dự án.
- **Stakeholder Register (Sổ đăng ký các bên liên quan):** Danh sách phân loại thông tin, mức độ ảnh hưởng và kỳ vọng của các bên liên quan.

#### B. Nhóm Tài liệu Hoạch định (Planning Artifacts)

- **Project Management Plan (Kế hoạch quản lý dự án):** Tài liệu tổng thể bao gồm các kế hoạch chi tiết cho các lĩnh vực như Rủi ro, Truyền thông và Chất lượng.
- **WBS (Cấu trúc phân rã công việc) & WBS Dictionary (Từ điển WBS):** Cung cấp định nghĩa chi tiết 100% về phạm vi công việc.
- **Activity List (Danh mục công việc):** Danh sách các task cụ thể được rã từ Work Package để phục vụ cho việc xếp tiến độ.

#### C. Nhóm Đường cơ sở (Baselines) - **Tuyệt đối không được tự ý thay đổi**

- **Scope Baseline (Đường cơ sở Phạm vi):** Bao gồm **Scope Statement**, **WBS**, và **WBS Dictionary**.
- **Schedule Baseline (Đường cơ sở Tiến độ):** Kế hoạch tiến độ gốc đã được phê duyệt (thường thể hiện qua biểu đồ Gantt).
- **Cost Baseline (Đường cơ sở Chi phí):** Ngân sách gốc được phân bổ theo thời gian (thể hiện qua **S-Curve**).

### 3. Tính toán Biến động Chi phí và Tiến độ (Cost & Schedule Variances)

Việc đo lường mức độ lệch so với kế hoạch được thực hiện thông qua **Quản lý Giá trị Thu được (EVM)**.

#### Ba Chỉ số Nền tảng (Inputs)

1. **PV (Planned Value - Giá trị Kế hoạch):** Lượng công việc **đáng lẽ phải hoàn thành** tính đến thời điểm hiện tại theo kế hoạch.
2. **EV (Earned Value - Giá trị Thu được):** Lượng công việc **thực tế đã hoàn thành** tính đến hiện tại, quy đổi theo ngân sách gốc.
3. **AC (Actual Cost - Chi phí Thực tế):** Số tiền **thực tế đã chi ra** để hoàn thành lượng công việc tính đến hiện tại.

#### A. Công thức Tính Biến động (Variances)

Biến động cho biết mức độ lệch bằng một **con số tuyệt đối** (đơn vị tiền tệ):

| Công thức                             | Tên Chỉ số                                | Ý nghĩa Kết quả                                                                                                                                             |
| :------------------------------------ | :---------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| $$\text{CV} = \text{EV} - \text{AC}$$ | **Cost Variance (Biến động Chi phí)**     | $\text{CV}< 0$: **Vượt ngân sách / Lỗ** (Over Budget); $\text{CV} = 0$: **Đúng ngân sách**; $\text{CV} > 0$: **Dưới ngân sách / Tiết kiệm** (Under Budget). |
| $$\text{SV} = \text{EV} - \text{PV}$$ | **Schedule Variance (Biến động Tiến độ)** | $\text{SV}< 0$: **Chậm tiến độ** (Behind Schedule); $\text{SV} = 0$: **Đúng tiến độ**; $\text{SV} > 0$: **Vượt tiến độ / Nhanh** (Ahead of Schedule).       |

#### B. Công thức Tính Chỉ số Hiệu suất (Indices)

Các chỉ số này đo lường tỷ lệ hiệu quả bằng một **con số tương đối** (hệ số), giúp dễ dàng so sánh giữa các dự án khác nhau:

| Công thức                                    | Tên Chỉ số                                                | Ý nghĩa Kết quả                                                                                                                                 |
| :------------------------------------------- | :-------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------- |
| $$\text{CPI} = \frac{\text{EV}}{\text{AC}}$$ | **Cost Performance Index (Chỉ số Hiệu suất Chi phí)**     | $\text{CPI}< 1$: **Chi tiêu không hiệu quả (Lỗ)**; $\text{CPI} = 1$: **Chi tiêu đúng kế hoạch**; $\text{CPI} > 1$: **Chi tiêu hiệu quả (Lời)**. |
| $$\text{SPI} = \frac{\text{EV}}{\text{PV}}$$ | **Schedule Performance Index (Chỉ số Hiệu suất Tiến độ)** | $\text{SPI}< 1$: **Tiến độ chậm**; $\text{SPI} = 1$: **Tiến độ đúng hạn**; $\text{SPI} > 1$: **Tiến độ nhanh**.                                 |

#### 🌟 Bài tập Tình huống Thực tế (Ví dụ)

Giả sử tại tuần thứ 5:

- $\text{PV} = \$10,000$ (Kế hoạch)
- $\text{EV} = \$8,000$ (Thực tế đã hoàn thành)
- $\text{AC} = \$9,000$ (Chi phí thực tế đã phát sinh)

**Tính toán:**

1. $\text{CV} = 8,000 - 9,000 = -1,000$ (Dự án đang **vượt ngân sách $1,000**).
2. $\text{SV} = 8,000 - 10,000 = -2,000$ (Dự án đang **chậm tiến độ** tương đương lượng công việc trị giá $2,000$).
3. $\text{CPI} = \frac{8,000}{9,000} \approx 0.89$ (Hiệu suất chi phí kém: mỗi đồng chi ra chỉ thu lại được 0.89 đồng giá trị).
4. $\text{SPI} = \frac{8,000}{10,000} = 0.80$ (Team chỉ đạt được 80% công suất so với tốc độ yêu cầu trong kế hoạch).

**Kết luận của PM:** Dự án đang rơi vào tình trạng **xấu** (Chậm tiến độ và Vượt ngân sách). Quản lý Dự án cần phải **rà soát lại Đường găng (Critical Path)** và đưa ra các **hành động khắc phục (Corrective Action)** kịp thời.
