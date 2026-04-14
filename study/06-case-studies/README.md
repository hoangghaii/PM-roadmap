# Case Studies — Học từ Thực Tế

> "Người thông minh học từ sai lầm của người khác. Người bình thường học từ sai lầm của chính mình. Kẻ ngốc không học từ cả hai." — Otto von Bismarck

---

## Tổng Quan

Phần Case Studies này tập hợp các dự án thực tế — thành công lẫn thất bại — để rút ra bài học PM cụ thể, ứng dụng được vào công việc hàng ngày. Mỗi case study không chỉ kể câu chuyện mà phân tích nguyên nhân gốc rễ và chỉ ra **bạn nên làm gì khác đi**.

---

## Tại Sao Phải Học Case Studies?

Phần lớn sách PM dạy lý thuyết: "bạn nên làm risk management", "bạn nên communicate với stakeholders". Case studies cho bạn thấy **điều gì xảy ra khi bạn KHÔNG làm** — và hậu quả thực sự là gì.

### Lợi ích cụ thể:

1. **Pattern recognition**: Nhận ra các dấu hiệu cảnh báo sớm trong dự án của mình
2. **Vicarious learning**: Học từ $500 triệu dollar sai lầm mà không cần tốn tiền
3. **Vocabulary for risk**: Có ngôn ngữ để mô tả rủi ro với stakeholders
4. **Credibility**: Dẫn chứng case studies thực tế khi thuyết phục cấp trên

---

## Cách Học Hiệu Quả

### Quy trình đọc một case study:

```
Bước 1: ĐỌC TỔNG QUAN (5 phút)
├── Dự án là gì?
├── Kết quả: thành công hay thất bại?
└── Bối cảnh: ngành, quy mô, thời gian

Bước 2: PHÂN TÍCH NGUYÊN NHÂN (15 phút)
├── Root cause là gì? (thường là con người, quy trình, hoặc kỹ thuật)
├── Dấu hiệu cảnh báo nào bị bỏ qua?
└── Ai chịu trách nhiệm và tại sao?

Bước 3: RÚT BÀI HỌC (10 phút)
├── Nếu bạn là PM, bạn đã làm gì khác?
├── Bài học nào áp dụng được ngay hôm nay?
└── Bài học nào phù hợp với bối cảnh Việt Nam?

Bước 4: LIÊN KẾT THỰC TẾ (5 phút)
├── Dự án bạn đang làm có rủi ro tương tự không?
└── Hành động cụ thể bạn sẽ thực hiện sau khi đọc?
```

### Template ghi chú khi đọc:

```
Case Study: _______________
Ngày đọc: _______________

3 điều tôi học được:
1.
2.
3.

1 hành động tôi sẽ thực hiện trong dự án hiện tại:
-

Câu hỏi tôi còn chưa hiểu:
-
```

---

## Mục Lục Case Studies

### Nhóm 1: Failure Cases (Học từ thất bại)

| # | Case Study | Ngành | Thiệt hại | Bài học chính |
|---|-----------|-------|-----------|---------------|
| CS-01 | NASA Mars Climate Orbiter (1999) | Vũ trụ | $327M | Interface agreements, unit mismatch |
| CS-04 | Denver Airport Baggage System (1994) | Hàng không | $500M | Scope complexity, pilot testing |
| CS-05 | HealthCare.gov Launch Failure (2013) | Y tế / Chính phủ | $500M+ | Integration testing, multi-vendor coordination |

### Nhóm 2: Success & Adaptation Cases (Học từ thành công)

| # | Case Study | Ngành | Kết quả | Bài học chính |
|---|-----------|-------|---------|---------------|
| CS-02 | Spotify Agile Model | Tech / Music | Tăng trưởng bền vững | Autonomous squads, culture over process |

### Nhóm 3: Vietnam Context Cases (Bối cảnh địa phương)

| # | Case Study | Ngành | Bối cảnh | Bài học chính |
|---|-----------|-------|---------|---------------|
| CS-03 | ERP cho SME Việt Nam | Sản xuất | 200 nhân viên, Hà Nội | Change management, user resistance |

---

## Các Chủ Đề Xuyên Suốt

Sau khi đọc tất cả case studies, bạn sẽ thấy một số pattern lặp lại:

### 1. Communication Gap
Hầu hết thất bại không phải vì kỹ thuật — mà vì con người không communicate rõ ràng. NASA mất $327M vì 2 nhóm dùng đơn vị đo lường khác nhau và không ai xác nhận lại.

### 2. Optimistic Planning
Ước lượng thời gian và ngân sách quá lạc quan là pattern phổ biến. Denver Airport nghĩ hệ thống baggage mất 2 tháng — thực tế mất 2 năm.

### 3. Political Pressure Overriding Technical Judgment
HealthCare.gov phải launch đúng ngày vì lý do chính trị, dù kỹ thuật chưa sẵn sàng. Hậu quả: crash toàn quốc ngay ngày đầu.

### 4. User Resistance (Vietnam-specific)
ERP implementation tại VN thường thất bại vì người dùng resist thay đổi — không phải vì system tệ.

### 5. Scope Creep
Mỗi phòng ban muốn thêm một tính năng. Một mình không đủ. Tất cả cộng lại = dự án chết.

---

## Kết Nối Với Các Module Khác

```
Module 03 (Risk Management) ←→ CS-01, CS-04, CS-05
Module 04 (Stakeholder Mgmt) ←→ CS-03, CS-05
Module 05 (Agile / Scrum) ←→ CS-02
Module 02 (Project Planning) ←→ CS-04
```

---

## Nguồn Tham Khảo Thêm

- **"The Standish Chaos Report"** — nghiên cứu hàng năm về tỷ lệ thất bại của dự án IT
- **"Why Software Fails" (IEEE Spectrum)** — phân tích các nguyên nhân phổ biến
- **PM Network Magazine** — case studies PM thực tế từ PMI
- **"Lessons Learned" database của NASA** — miễn phí tại llis.nasa.gov
