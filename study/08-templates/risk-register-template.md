# RISK REGISTER

| Field | Chi Tiết |
|---|---|
| **Dự án** | [Tên dự án] |
| **Project ID** | [PC-YYYYMM-XXX] |
| **PM** | [Tên PM] |
| **Phiên bản** | 1.0 |
| **Ngày tạo** | DD/MM/YYYY |
| **Cập nhật lần cuối** | DD/MM/YYYY |
| **Review Cycle** | Hàng tuần (mỗi thứ Hai) |

---

## RISK SCORING MATRIX (5×5)

```
         |  IMPACT
         |  1-Rất thấp  2-Thấp    3-Trung bình  4-Cao    5-Rất cao
---------|------------------------------------------------------------
P  5-Rất |    5(M)      10(H)       15(H)        20(H)     25(H)
R  cao   |
O  4-Cao |    4(L)       8(M)       12(H)        16(H)     20(H)
B        |
A  3-TB  |    3(L)       6(M)        9(M)        12(H)     15(H)
B        |
I  2-Thấp|    2(L)       4(L)        6(M)         8(M)     10(H)
L        |
I  1-Rất |    1(L)       2(L)        3(L)         4(L)      5(M)
T  thấp  |
Y        |
```

**Legend:**
- `H` (High) = Score 15-25 → Cần immediate action, escalate lên sponsor
- `M` (Medium) = Score 8-14 → Cần mitigation plan, theo dõi hàng tuần
- `L` (Low) = Score 1-7 → Monitor, check định kỳ 2 tuần/lần

**Cách tính Score:** `Score = Probability × Impact`

---

## RISK REGISTER

| ID | Mô tả rủi ro | Category | Probability (1-5) | Impact (1-5) | Score | Level | Chiến lược | Response Actions | Owner | Target Date | Status | Last Reviewed |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| R001 | API của bên thứ ba (payment gateway) thay đổi interface đột ngột, gây gián đoạn tích hợp | Technical | 3 | 4 | 12 | M | Mitigate | 1. Lock API version contract với vendor; 2. Xây dựng abstraction layer; 3. Setup monitoring alerts cho API changes | Dev Lead | 15/05/2026 | Open | 14/04/2026 |
| R002 | Key developer (senior fullstack) nghỉ việc giữa chừng do thị trường tuyển dụng cạnh tranh | Resource | 2 | 5 | 10 | M | Mitigate | 1. Document hóa toàn bộ code và decision rationale; 2. Cross-training cho 1 dev khác; 3. Identify backup resource với HR | PM | 30/04/2026 | Open | 14/04/2026 |
| R003 | Yêu cầu thay đổi lớn từ stakeholder sau khi đã lock requirements (scope creep) | Stakeholder | 4 | 3 | 12 | M | Avoid | 1. Strict change control process (Change Request Form bắt buộc); 2. Requirements sign-off document; 3. Weekly demo cho stakeholders để catch misalignment sớm | PM | Ongoing | Open | 14/04/2026 |
| R004 | Hệ thống load testing thất bại, performance dưới ngưỡng yêu cầu (<2s response time ở 1000 concurrent users) | Technical | 3 | 4 | 12 | H | Mitigate | 1. Load testing bắt đầu từ sprint 4 (không đợi đến cuối); 2. Architecture review với cloud team; 3. Budget contingency cho infrastructure upgrade | Tech Lead | 01/06/2026 | Open | 14/04/2026 |
| R005 | Vendor cung cấp infrastructure gặp sự cố (downtime, data center issue) ảnh hưởng đến go-live | External | 2 | 4 | 8 | M | Transfer | 1. Check SLA với vendor (uptime 99.9%); 2. Disaster recovery plan; 3. Backup deployment region đã sẵn sàng | Tech Lead | 15/05/2026 | Open | 14/04/2026 |

---

## RISK CATEGORIES

| Category | Mô tả | Ví dụ |
|---|---|---|
| **Technical** | Rủi ro liên quan đến công nghệ, architecture, code | Bugs nghiêm trọng, security vulnerability, performance issues |
| **Schedule** | Rủi ro gây trễ timeline | Estimation sai, dependencies bị chậm, holidays/sick leave |
| **Resource** | Rủi ro liên quan đến con người và capacity | Nhân sự nghỉ việc, conflict allocation, skill gap |
| **External** | Rủi ro từ bên ngoài tổ chức | Vendor delay, regulatory changes, market shifts |
| **Stakeholder** | Rủi ro từ dynamics giữa stakeholders | Scope creep, conflicting priorities, lack of engagement |
| **Quality** | Rủi ro ảnh hưởng đến chất lượng sản phẩm | Insufficient testing, unclear acceptance criteria, tech debt |

---

## 4 RESPONSE STRATEGIES

### 1. Avoid (Tránh)
**Khi nào dùng:** Rủi ro có score cao (High), và có cách loại bỏ hoàn toàn.

**Cách thực hiện:** Thay đổi project plan, scope, hoặc approach để rủi ro không còn áp dụng.

**Ví dụ:** Thay vì build custom payment integration (rủi ro cao), dùng off-the-shelf payment gateway đã proven. Rủi ro integration failures được avoid bằng cách không tự build.

---

### 2. Transfer (Chuyển giao)
**Khi nào dùng:** Rủi ro khó kiểm soát nội bộ, có thể shift sang bên thứ ba chuyên nghiệp hơn.

**Cách thực hiện:** Mua bảo hiểm, ký hợp đồng với SLA, outsource phần có rủi ro.

**Ví dụ:** Infrastructure downtime risk → Dùng AWS với SLA 99.99% và penalty clause. Rủi ro tài chính được transfer sang AWS. Lưu ý: Transfer rủi ro, không transfer trách nhiệm — PM vẫn phải theo dõi.

---

### 3. Mitigate (Giảm thiểu)
**Khi nào dùng:** Rủi ro không thể avoid hoặc transfer hoàn toàn, nhưng có thể giảm Probability hoặc Impact.

**Cách thực hiện:** Actions cụ thể để giảm P hoặc I xuống mức chấp nhận được.

**Ví dụ:** Key person risk (Dev nghỉ việc) → Giảm Impact bằng documentation + cross-training, giảm Probability bằng cách cải thiện work environment và recognition.

---

### 4. Accept (Chấp nhận)
**Khi nào dùng:** Rủi ro score thấp (Low), hoặc cost to mitigate > potential loss.

**Cách thực hiện:**
- **Passive Accept:** Ghi nhận, không làm gì thêm. Monitor định kỳ.
- **Active Accept:** Chuẩn bị contingency plan sẵn sàng khi rủi ro xảy ra.

**Ví dụ:** Rủi ro mưa bão ảnh hưởng đến team onsite → Low probability, backup remote work policy sẵn sàng (Active Accept).

---

## HƯỚNG DẪN SỬ DỤNG

### Setup Ban Đầu (Kickoff + 1 tuần)
1. **Brainstorm** với core team: "What can go wrong?" — 30-phút session, không judge, viết hết
2. **Prioritize** theo score: Tập trung vào High risks trước
3. **Assign owners** cho mỗi risk: Owner là người chịu trách nhiệm theo dõi và thực hiện mitigation, không nhất thiết là người có thể fix
4. **Review với sponsor**: Walk through top 3-5 High risks, đảm bảo sponsor aware

### Review Hàng Tuần
- Cập nhật Status: Open / In Progress / Closed / Realized (rủi ro đã xảy ra)
- Cập nhật Last Reviewed
- Nếu rủi ro realized → Chuyển sang Issue Log, thêm note vào Status Report

### Thêm Risk Mới
Rủi ro mới có thể xuất hiện bất cứ lúc nào. Team nên được khuyến khích báo cáo risk ngay khi phát hiện, không đợi đến meeting.

### Đóng Risk
Risk có thể close khi:
- Milestone/phase liên quan đã qua (risk không còn applicable)
- Mitigation actions đã thực hiện và P×I giảm xuống mức acceptable
- Risk đã realized và được xử lý (move to closed với note)

---

## RISK LOG (Lịch Sử Thay Đổi)

| Ngày | ID | Thay Đổi | Người thực hiện |
|---|---|---|---|
| DD/MM/YYYY | R001 | Cập nhật Response Actions sau vendor call | [Tên] |
| DD/MM/YYYY | R003 | Close — milestone requirements sign-off đạt | [Tên] |

---

*Risk Register là "living document" — phải được cập nhật, không phải chỉ được tạo ra.*
