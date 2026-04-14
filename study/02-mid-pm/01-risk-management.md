# Quản Lý Rủi Ro (Risk Management)

> **Cấp độ:** Mid PM (2–5 năm)
> **Thời gian học:** 1–2 tuần + thực hành liên tục
> **Áp dụng ngay:** Xây dựng Risk Register cho dự án đang chạy

---

## 1. Tại Sao Risk Management Quan Trọng

Hầu hết dự án không thất bại vì thiếu tài năng — chúng thất bại vì **những điều mà PM biết có thể xảy ra, nhưng không chuẩn bị**.

Thực tế tại Việt Nam:
- **73%** dự án IT trễ deadline (khảo sát StandishGroup 2023)
- **52%** dự án vượt ngân sách ít nhất 20%
- Phần lớn nguyên nhân: **key person nghỉ đột ngột, vendor trễ, requirement thay đổi late** — đều là rủi ro có thể dự báo trước

Risk Management không phải là **ngăn chặn rủi ro** (không thể). Nó là:
1. **Nhận diện** những gì có thể sai
2. **Đánh giá** mức độ nghiêm trọng
3. **Chuẩn bị** trước để giảm thiểu tác động
4. **Phản ứng** nhanh và có kế hoạch khi rủi ro xảy ra

> **Nguyên tắc vàng:** Rủi ro được nhận diện và có kế hoạch = vấn đề có thể quản lý. Rủi ro không biết = khủng hoảng.

---

## 2. Risk Identification Methods

### 2.1 Brainstorming
Tập hợp team (dev, QA, BA, stakeholder) trong 60–90 phút. Dùng câu hỏi kích thích:
- "Điều gì có thể làm dự án này thất bại?"
- "Lần trước bạn gặp vấn đề gì tương tự?"
- "Điều gì chúng ta đang giả định là đúng nhưng có thể sai?"

**Kỹ thuật:** Dùng sticky notes, mỗi người viết riêng trước khi share (tránh groupthink).

### 2.2 Risk Checklists
Dùng checklist từ dự án trước hoặc ngành. Phù hợp khi team thiếu kinh nghiệm hoặc cần tốc độ.

Checklist mẫu cho dự án phần mềm:
```
□ Key developer nghỉ / chuyển công ty
□ Vendor/third-party API không deliver đúng hạn
□ Requirement chưa rõ ràng dẫn đến rework
□ Môi trường dev/test không ổn định
□ Khách hàng review chậm, approval bị delay
□ Security vulnerability phát hiện muộn
□ Data migration phức tạp hơn dự kiến
□ Integration với legacy system gặp vấn đề
□ Team thiếu kỹ năng cho technology mới
□ Budget bị cắt giữa dự án
```

### 2.3 Expert Interviews
Phỏng vấn riêng từng chuyên gia (tech lead, architect, business analyst). Câu hỏi gợi ý:
- "Theo kinh nghiệm của bạn, phần nào của dự án này khó nhất?"
- "Bạn có lo lắng gì về phần kỹ thuật không?"
- "Điều kiện nào có thể làm estimate của bạn sai?"

### 2.4 Historical Data (Lessons Learned)
Xem lại lessons learned từ dự án tương tự. Câu hỏi:
- Dự án nào trước đây có scope/tech tương tự?
- Rủi ro nào đã xảy ra?
- Rủi ro nào được nhận diện nhưng không xảy ra — tại sao?

---

## 3. Risk Categories

| Category | Mô tả | Ví dụ |
|---|---|---|
| **Technical** | Rủi ro liên quan đến công nghệ, kiến trúc | API bên thứ ba không ổn định, debt kỹ thuật |
| **Schedule** | Rủi ro ảnh hưởng đến timeline | Estimate sai, dependency bị trễ |
| **Cost** | Rủi ro vượt ngân sách | Scope creep, resource rate tăng |
| **Resource** | Rủi ro về con người | Key dev nghỉ, team thiếu kỹ năng |
| **External** | Rủi ro từ bên ngoài không kiểm soát được | Thay đổi luật, thiên tai, vendor phá sản |
| **Organizational** | Rủi ro từ nội bộ tổ chức | Thay đổi ưu tiên của lãnh đạo, budget bị cắt |

---

## 4. Risk Register Template

Risk Register là **tài liệu sống** — cập nhật thường xuyên, không phải viết một lần rồi bỏ.

### Cấu Trúc Risk Register

| ID | Mô tả rủi ro | Loại | Xác suất (1–5) | Impact (1–5) | Score | Chiến lược | Hành động cụ thể | Owner | Deadline | Trạng thái |
|---|---|---|---|---|---|---|---|---|---|---|
| R001 | Key developer Nguyễn Văn A nghỉ việc | Resource | 3 | 5 | 15 | Mitigate | Pair programming, tài liệu hóa knowledge | PM + Tech Lead | Tuần 2 | Active |
| R002 | Third-party payment API không ổn định | Technical | 3 | 4 | 12 | Mitigate | Setup sandbox test, có fallback provider | Dev Lead | Tuần 3 | Active |

### Thang Đo Xác Suất và Impact

**Xác suất (Probability):**
| Điểm | Mức | Ý nghĩa |
|---|---|---|
| 1 | Rất thấp | < 10% khả năng xảy ra |
| 2 | Thấp | 10–30% |
| 3 | Trung bình | 30–50% |
| 4 | Cao | 50–70% |
| 5 | Rất cao | > 70% |

**Impact:**
| Điểm | Mức | Ý nghĩa |
|---|---|---|
| 1 | Rất thấp | Ảnh hưởng không đáng kể |
| 2 | Thấp | Trễ < 1 tuần hoặc < 5% budget |
| 3 | Trung bình | Trễ 1–2 tuần hoặc 5–15% budget |
| 4 | Cao | Trễ 2–4 tuần hoặc 15–30% budget |
| 5 | Rất cao | Dự án có thể thất bại |

---

## 5. Risk Scoring Matrix (5×5)

```
        IMPACT →
         1      2      3      4      5
       ┌──────┬──────┬──────┬──────┬──────┐
    5  │  5   │  10  │  15  │  20  │  25  │
       │ LOW  │ MED  │ HIGH │ HIGH │ HIGH │
       ├──────┼──────┼──────┼──────┼──────┤
    4  │  4   │   8  │  12  │  16  │  20  │
P      │ LOW  │ MED  │ MED  │ HIGH │ HIGH │
R      ├──────┼──────┼──────┼──────┼──────┤
O   3  │  3   │   6  │   9  │  12  │  15  │
B      │ LOW  │ LOW  │ MED  │ MED  │ HIGH │
A      ├──────┼──────┼──────┼──────┼──────┤
B   2  │  2   │   4  │   6  │   8  │  10  │
I      │ LOW  │ LOW  │ LOW  │ MED  │ MED  │
L      ├──────┼──────┼──────┼──────┼──────┤
I   1  │  1   │   2  │   3  │   4  │   5  │
T      │ LOW  │ LOW  │ LOW  │ LOW  │ LOW  │
Y      └──────┴──────┴──────┴──────┴──────┘

HIGH (≥15):  Escalate ngay lên sponsor/management, cần action plan ngay
MED  (8–14): Monitor chặt, review hàng tuần, cần mitigation plan
LOW  (≤7):   Accept và log, review định kỳ
```

**Quy tắc áp dụng:**
- **Score ≥ 15 (HIGH):** PM phải escalate lên sponsor trong 24h. Không chờ đến weekly meeting.
- **Score 8–14 (MEDIUM):** Đưa vào agenda weekly risk review. Assigned owner phải báo cáo update.
- **Score ≤ 7 (LOW):** Log trong risk register, xem xét lại mỗi 2 tuần.

---

## 6. Bốn Chiến Lược Xử Lý Rủi Ro

### 6.1 Avoid (Tránh né)
**Khi nào dùng:** Rủi ro có score cao và có thể loại bỏ bằng cách thay đổi kế hoạch.

**Cách làm:** Thay đổi scope, timeline, hoặc phương pháp để loại bỏ rủi ro hoàn toàn.

**Ví dụ:** Team không có kinh nghiệm với blockchain. Thay vì cố học, quyết định dùng solution truyền thống. → Loại bỏ rủi ro kỹ thuật.

**Lưu ý:** Đôi khi avoid = bỏ lỡ cơ hội. Cân nhắc kỹ trước khi quyết định.

### 6.2 Transfer (Chuyển giao)
**Khi nào dùng:** Khi có bên thứ ba có thể chịu rủi ro tốt hơn bạn.

**Cách làm:** Mua bảo hiểm, thuê vendor, ký SLA với penalty clause, time & materials contract thay vì fixed price.

**Ví dụ:** Dự án có rủi ro data breach cao. Mua cyber insurance. → Chuyển financial risk sang công ty bảo hiểm.

### 6.3 Mitigate (Giảm thiểu)
**Khi nào dùng:** Không thể tránh hoàn toàn, nhưng có thể giảm xác suất hoặc impact.

**Cách làm:** 
- Giảm xác suất: training, prototype, proof of concept, code review
- Giảm impact: contingency reserve, backup plan, redundancy

**Ví dụ:** R001 - Key dev có thể nghỉ → Pair programming + knowledge documentation → Giảm impact từ 5 xuống 3.

### 6.4 Accept (Chấp nhận)
**Khi nào dùng:** Risk score thấp, hoặc chi phí giảm thiểu > tác động rủi ro.

**Passive Accept:** Log và không làm gì thêm. Phù hợp cho LOW risks.

**Active Accept:** Có contingency plan sẵn sàng khi rủi ro xảy ra.

**Ví dụ:** Rủi ro mưa bão ảnh hưởng đến cuộc họp face-to-face. Accept vì có option online meeting.

---

## 7. Risk Response Planning Chi Tiết

Khi xác định chiến lược, PM cần document rõ:

```
Risk ID: R001
Mô tả: Key developer Nguyễn Văn A (80% task backend) có thể nghỉ việc
Trigger: A thông báo nghỉ hoặc có dấu hiệu muốn nghỉ
Chiến lược: Mitigate

Hành động TRƯỚC khi rủi ro xảy ra (Prevention):
  1. Pair programming: A làm chính, Nguyễn Văn B làm phụ trên 70% task quan trọng
  2. Wiki documentation: A phải document toàn bộ technical decision trong 2 tuần đầu
  3. Code review bắt buộc: B review 100% code của A (knowledge transfer)
  4. 1:1 với A mỗi 2 tuần để nắm tâm lý, nhu cầu

Contingency plan (khi rủi ro xảy ra):
  1. Ngay lập tức: B take over, PM thông báo sponsor
  2. Trong 48h: assess impact, update timeline
  3. Trong 1 tuần: quyết định có cần hire thêm không
  4. Backup: liên hệ staffing agency (đã research sẵn 2 agency)

Owner: Tech Lead Trần Thị C
Review date: Hàng tuần trong weekly risk meeting
```

---

## 8. Risk Monitoring và Review Cadence

| Tần suất | Hoạt động |
|---|---|
| **Hàng ngày** | Quan sát trigger conditions (không cần meeting) |
| **Hàng tuần** | Risk review 15–20 phút trong weekly team meeting |
| **Hàng tháng** | Đánh giá lại Risk Register đầy đủ, cập nhật score |
| **Mỗi milestone** | Full risk reassessment — thêm/xóa risk, thay đổi chiến lược |
| **Sau sự cố** | Post-incident review, cập nhật lessons learned |

**Risk Review Meeting Agenda (15 phút):**
1. Review các HIGH risks hiện tại (5 phút)
2. Update trạng thái từng risk có owner (5 phút)
3. Có risk mới không? (3 phút)
4. Action items (2 phút)

---

## 9. Ví Dụ Thực Tế: Risk Register Dự Án Migration Hệ Thống

**Bối cảnh:** Dự án migrate hệ thống kế toán legacy (Oracle 11g) lên SAP S/4 HANA cho công ty sản xuất 500 nhân viên, budget 2 tỷ VND, timeline 8 tháng.

| ID | Mô tả rủi ro | Loại | P | I | Score | Chiến lược | Hành động | Owner |
|---|---|---|---|---|---|---|---|---|
| R001 | Key developer backend nghỉ việc giữa dự án | Resource | 3 | 5 | **15** | Mitigate | Pair programming, document knowledge, retention bonus | Tech Lead |
| R002 | API kết nối Oracle ↔ SAP không ổn định | Technical | 4 | 4 | **16** | Mitigate | POC 2 tuần trước khi commit, có fallback batch job | Architect |
| R003 | Data cũ bị dirty/corrupt sau 15 năm | Technical | 4 | 4 | **16** | Mitigate | Data audit tháng 1, data cleansing sprint riêng | DBA |
| R004 | Finance team từ chối dùng hệ thống mới | Organizational | 3 | 4 | **12** | Mitigate | Training sớm, champion user trong finance team | PM + CFO |
| R005 | Budget bị cắt do tình hình kinh tế | Cost | 2 | 5 | **10** | Transfer + Accept | Contract fixed price với vendor, scope MVP rõ ràng | PM |
| R006 | Vendor SAP không deliver đúng hạn | External | 3 | 4 | **12** | Transfer | SLA với penalty clause, milestone-based payment | PM + Legal |
| R007 | Luật kế toán VN thay đổi làm sai requirement | External | 2 | 4 | **8** | Accept (Active) | Monitor nghị định Bộ Tài Chính, có buffer 2 tuần | BA |
| R008 | Môi trường test không đủ simulate production | Technical | 3 | 3 | **9** | Mitigate | Yêu cầu production-like test env từ đầu | Infra Lead |
| R009 | Go-live trùng với kỳ quyết toán thuế Q4 | Schedule | 4 | 3 | **12** | Avoid | Dời go-live sang tháng 1 năm sau | PM |
| R010 | Nhân viên kho không được đào tạo kịp | Resource | 3 | 3 | **9** | Mitigate | Training plan 6 tuần trước go-live | PM + HR |

**Tóm tắt:** 3 HIGH risks (R001, R002, R003) cần escalate lên sponsor và có action plan ngay. 5 MEDIUM risks monitor hàng tuần.

---

## 10. Trigger Conditions và Early Warning Signs

**Trigger** là dấu hiệu cảnh báo rủi ro sắp xảy ra — giúp PM phản ứng TRƯỚC khi rủi ro trở thành sự cố.

| Risk | Early Warning Sign (Trigger) |
|---|---|
| Key dev nghỉ | Dev ít tham gia meeting, hay đến muộn, hỏi về chính sách thôi việc |
| Vendor trễ | Vendor chưa send milestone update đúng hạn, email response chậm hơn |
| Budget overrun | Actual cost tuần 3 đã bằng 35% total budget (phải là 30%) |
| Scope creep | Khách hàng hay dùng từ "nhỏ thôi", "thêm một chút thôi" |
| Technical issue | Dev meetings kéo dài bất thường, nhiều "need to discuss" |
| Stakeholder disengaged | Sponsor bỏ họp nhiều, email không được trả lời kịp thời |

---

## 11. Contingency Plans vs Fallback Plans

| | Contingency Plan | Fallback Plan |
|---|---|---|
| **Khi nào dùng** | Rủi ro xảy ra như dự kiến | Contingency plan thất bại |
| **Ví dụ** | Key dev nghỉ → backup dev take over | Backup dev cũng không đủ năng lực → hire contractor |
| **Tốn kém hơn** | Thấp (đã chuẩn bị sẵn) | Cao (plan B của plan B) |
| **Approval cần** | PM tự quyết | Thường cần sponsor approval |

**Quy tắc:** Luôn có cả hai cho HIGH risks. MEDIUM risks ít nhất phải có contingency plan.

---

## Bài Tập Thực Hành

1. Lấy một dự án bạn đang/sẽ làm, tổ chức brainstorming 60 phút để identify ít nhất 10 rủi ro.
2. Score từng rủi ro và điền vào Risk Register template ở trên.
3. Với 3 rủi ro có score cao nhất, viết chi tiết Response Plan (prevention + contingency).
4. Xác định trigger condition cho mỗi HIGH risk.

> **Reflection sau 2 tuần:** Có rủi ro nào xảy ra không? Nếu có, bạn đã kịp phản ứng không? Score ban đầu có chính xác không?
