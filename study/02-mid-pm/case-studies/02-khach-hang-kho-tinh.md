# Case Study 2: Khách Hàng Khó Tính — Scope Dispute

**Cấp độ:** PM Chính Thức
**Kỹ năng:** Scope management, contract management, negotiation, escalation
**Độ phức tạp:** ⭐⭐⭐⭐ Cao
**Thời gian đọc:** ~25 phút

---

## Bối Cảnh

**Công ty:** TechBridge Solutions — công ty IT outsourcing 80 người tại TP.HCM
**Khách hàng:** LogiPro JSC — công ty logistics 3PL (third-party logistics), 350 nhân viên
**Dự án:** Xây dựng hệ thống ERP tích hợp cho LogiPro — gồm: quản lý kho, vận chuyển, tài chính, và báo cáo

**PM:** Minh Tuấn, 3 năm kinh nghiệm, đây là dự án lớn nhất anh từng lead

**Hợp đồng:**
- Giá trị: 2.4 tỷ VND (fixed-price contract)
- Timeline: 12 tháng
- Scope: Được định nghĩa trong Scope Document 20 trang (SD-LogiPro-v1.0)
- Payment: 30% upfront, 40% ở milestone 6 tháng, 30% khi go-live

**Team:**
- 1 PM (Minh Tuấn)
- 1 Business Analyst (Lan Anh)
- 4 Backend developers
- 2 Frontend developers
- 1 QA engineer
- Tổng: 9 người

---

## Vấn Đề

Bắt đầu từ tuần 4, bà Phương — Giám đốc Vận hành của LogiPro và là người đại diện chính từ phía khách hàng — bắt đầu gửi yêu cầu thêm vào hệ thống với tần suất ngày càng tăng.

**Pattern điển hình của bà Phương:**
- Gửi yêu cầu qua Zalo trực tiếp cho developer (bypass PM)
- Claim rằng "Cái này đương nhiên là requirement ban đầu rồi, anh PM đọc lại scope đi"
- Khi PM hỏi chi tiết, bà dẫn ra những câu mơ hồ trong scope document và interpret theo ý mình
- Không chịu ký Change Request Form với lý do "Đây không phải change, đây là requirement"
- Gọi điện cho Account Manager của TechBridge để phàn nàn mỗi khi PM push back

**Áp lực nội bộ:**
- Dev team bắt đầu implement yêu cầu của bà Phương mà không thông qua PM (vì "sợ khách hàng")
- Account Manager gọi cho Minh Tuấn và nói: "Cậu phải flexible hơn, đây là client quan trọng"
- Dev lead than thở rằng team đang overload, không thể nhận thêm việc

---

## Timeline Sự Kiện (Tuần 1 — Tuần 12)

```
Tuần 1-3:    Bình thường. Kick-off, requirements gathering, design review.
             Scope Document v1.0 đã được ký bởi CEO LogiPro và TechBridge CEO.

Tuần 4:      Bà Phương yêu cầu thêm "Tính năng tracking xe tải real-time".
             PM giải thích đây là ngoài scope, bà Phương phản đối.
             ⚠️ Dấu hiệu đầu tiên.

Tuần 5:      Bà Phương gửi Zalo cho dev trực tiếp, yêu cầu thêm báo cáo
             tùy chỉnh (custom report builder). Dev nhận và bắt đầu làm.
             PM phát hiện sau 2 ngày.
             ❌ Scope creep đầu tiên không được kiểm soát.

Tuần 6-7:    Minh Tuấn tổ chức meeting với bà Phương. Bà yêu cầu thêm 6
             tính năng, claim tất cả đều "trong scope". PM cần phân tích.
             ⏸️ Tạm dừng để kiểm tra.

Tuần 8:      PM hoàn thành scope analysis. Kết quả: 2/6 thực sự trong scope
             (bị hiểu nhầm), 3/6 ngoài scope, 1/6 ambiguous.
             Trình bày với Account Manager — bị áp lực "cứ làm đi".
             😤 Áp lực nội bộ leo thang.

Tuần 9:      PM leo thang lên Project Sponsor nội bộ (Technical Director).
             Tổ chức họp 3 bên: TechBridge, LogiPro, và luật sư hợp đồng.
             📋 Scope Review Meeting.

Tuần 10:     Sau meeting, đạt được agreement:
             - 2/6 tính năng trong scope → implement bình thường
             - 3/6 tính năng ngoài scope → tạo CR, LogiPro phải ký
             - 1/6 tính năng ambiguous → dùng mediation, agree on middle ground
             ✅ Turning point.

Tuần 11-12:  Dự án tiếp tục với quy trình Change Control nghiêm ngặt hơn.
             Bà Phương vẫn gửi yêu cầu nhưng đã quen với quy trình CR.
             Dev team được remind: mọi yêu cầu phải qua PM.
             ▶️ Ổn định trở lại.
```

---

## 4 Loại Tình Huống Khi Đối Chiếu Scope Document

### Tình Huống 1: Requirement Mới Rõ Ràng KHÔNG Trong Scope → Escalate

**Ví dụ:** Bà Phương yêu cầu tích hợp GPS tracking với xe tải của LogiPro.

**Scope document nói gì:** "Hệ thống quản lý vận chuyển bao gồm: tạo lịch trình, phân công tài xế, cập nhật trạng thái thủ công."

**Phân tích:** Không có từ nào đề cập đến GPS, real-time tracking, hay IoT integration. Đây rõ ràng là tính năng mới.

**Hướng xử lý:**
1. Document bằng văn bản: Trích dẫn chính xác điều khoản trong scope document
2. Trình bày impact: Tính năng này cần tích hợp với thiết bị GPS (phần cứng không thuộc scope), API bên thứ ba, và thay đổi kiến trúc đáng kể
3. Tạo CR chính thức: Estimate +6 tuần, +350 triệu VND
4. Escalate nếu khách hàng không đồng ý: Đưa lên Account Manager → Legal → Senior Management

**Script giao tiếp:**
> "Chúng tôi đã kiểm tra kỹ Scope Document tại mục 3.2 — Quản Lý Vận Chuyển. Tính năng GPS real-time tracking không được đề cập trong bất kỳ điều khoản nào. Đây là một tính năng có giá trị cao cho LogiPro, và chúng tôi hoàn toàn có thể implement. Tuy nhiên, để đảm bảo quyền lợi của cả hai bên, chúng tôi cần thực hiện qua Change Request Process theo điều khoản 7.3 trong hợp đồng."

---

### Tình Huống 2: Requirement Ambiguous, Có Thể Interpret Cả 2 Cách → Negotiate

**Ví dụ:** Scope document ghi "Hệ thống cung cấp báo cáo vận hành." Bà Phương yêu cầu 15 loại báo cáo. PM nghĩ là 5 báo cáo chuẩn.

**Phân tích:** Câu "báo cáo vận hành" không specify số lượng, loại, hay format. Cả hai cách interpret đều có cơ sở.

**Hướng xử lý:**
1. Không tuyên bố ai đúng ai sai — đây là lỗi của scope document
2. Ngồi lại cùng nhau với BA, yêu cầu khách hàng liệt kê 15 báo cáo họ cần
3. Prioritize: Trong 15 báo cáo đó, cái nào critical cho go-live?
4. Negotiate: Đề xuất 8 báo cáo trong scope hiện tại, 7 báo cáo còn lại vào phase 2

**Script giao tiếp:**
> "Chúng tôi đồng ý rằng câu 'báo cáo vận hành' trong scope document có thể được hiểu theo nhiều cách — và đây là điều chúng tôi nên định nghĩa rõ hơn từ đầu. Thay vì tranh luận về đúng/sai, chúng ta hãy tập trung vào business priority: trong 15 báo cáo anh/chị cần, cái nào quan trọng nhất để vận hành ngay ngày đầu go-live? Hãy cùng chọn ra top 8, và 7 cái còn lại chúng tôi cam kết deliver trong phase 2."

---

### Tình Huống 3: Requirement Thực Sự Đã Có Trong Scope Nhưng PM Bỏ Sót → Admit và Fix

**Ví dụ:** Scope document có ghi "Tích hợp với phần mềm kế toán hiện tại của khách hàng." PM và team không implement, nghĩ là ngoài scope.

**Phân tích:** Sau khi đọc lại scope document, Minh Tuấn nhận ra điều khoản này rõ ràng. Đây là lỗi của PM, không phải scope creep.

**Hướng xử lý:**
1. Admit ngay, không chần chừ — trì hoãn chỉ làm mọi thứ tệ hơn
2. Xin lỗi khách hàng một cách chuyên nghiệp
3. Tạo recovery plan: Cần bao nhiêu thời gian, ảnh hưởng đến timeline không?
4. Communicate nội bộ: Tại sao requirement này bị bỏ sót?

**Script giao tiếp:**
> "Sau khi rà soát lại scope document, tôi xác nhận tính năng tích hợp kế toán này đã nằm trong scope từ đầu. Tôi xin lỗi vì sự nhầm lẫn này — đây là lỗi của phía chúng tôi trong quá trình planning. Tôi đã trao đổi với tech lead, và chúng tôi cần 5 ngày làm việc để hoàn thành integration này. Nó sẽ không ảnh hưởng đến delivery date tổng thể vì chúng tôi có thể làm song song."

---

### Tình Huống 4: Requirement Phụ Thuộc Vào Interpretation Khác Nhau → Mediation

**Ví dụ:** Scope ghi "Hệ thống hỗ trợ multi-user." Bà Phương hiểu là "unlimited concurrent users," PM hiểu là "multiple user accounts với roles."

**Hướng xử lý:**
1. Không tự giải quyết song phương — đây cần người thứ ba
2. Mời BA senior hoặc người từ Legal để làm mediator
3. Đọc nguyên văn hợp đồng và scope document trong context
4. Tham khảo industry standard definition nếu cần
5. Reach final agreement bằng văn bản

---

## Bước-Bước Phân Tích Scope Document

### Bước 1: Kéo Scope Document Ra Đối Chiếu Từng Điểm

```
SCOPE DOCUMENT ANALYSIS WORKSHEET

Dự án: LogiPro ERP          Analyst: Lan Anh (BA)
Ngày: 15/2/2026             Scope Doc Version: v1.0

┌──────┬─────────────────────┬─────────────────────┬──────────────┐
│ Req# │ Yêu cầu từ KH       │ Scope Doc Reference │ Classification│
├──────┼─────────────────────┼─────────────────────┼──────────────┤
│ R-01 │ GPS real-time       │ Không có mention    │ OUT OF SCOPE │
│      │ tracking            │                     │              │
├──────┼─────────────────────┼─────────────────────┼──────────────┤
│ R-02 │ 15 loại báo cáo    │ Mục 4.5: "Báo cáo  │ AMBIGUOUS    │
│      │ vận hành            │ vận hành" (vague)   │              │
├──────┼─────────────────────┼─────────────────────┼──────────────┤
│ R-03 │ Tích hợp kế toán   │ Mục 3.8: "Tích hợp │ IN SCOPE     │
│      │ MISA                │ phần mềm kế toán    │ (PM bỏ sót) │
│      │                     │ hiện tại"           │              │
├──────┼─────────────────────┼─────────────────────┼──────────────┤
│ R-04 │ Mobile app cho      │ Exclusion list:     │ OUT OF SCOPE │
│      │ tài xế              │ "Không bao gồm      │              │
│      │                     │ mobile application" │              │
└──────┴─────────────────────┴─────────────────────┴──────────────┘
```

### Bước 2: Mapping Requirement Mới Với Scope Document

Quy trình 3 bước:
1. **Highlight:** In scope document, highlight mọi câu có thể liên quan đến requirement
2. **Quote:** Trích dẫn chính xác từng câu (không paraphrase, không diễn giải)
3. **Gap Analysis:** So sánh requirement với quote — có match không?

### Bước 3: Phân Loại

```
IN SCOPE      → Implement bình thường, không cần CR
AMBIGUOUS     → Negotiate, document agreement, không tự quyết
OUT OF SCOPE  → CR bắt buộc trước khi implement
```

---

## Escalation Path

```
Vấn đề scope dispute không giải quyết được ở PM level
           ↓
Level 1: Account Manager / Client Success Manager
         (TechBridge bên trong) — thường giải quyết được 70% cases
           ↓ (nếu không được)
Level 2: Project Sponsor Meeting
         (Senior management cả 2 bên) — formal meeting, có minutes
           ↓ (nếu không được)
Level 3: Legal / Contract Review
         Luật sư đọc hợp đồng, interpret chính thức
           ↓ (trường hợp cực kỳ nghiêm trọng)
Level 4: Mediation / Arbitration
         Bên thứ ba độc lập (thường theo điều khoản trong hợp đồng)
```

**Khi Escalate, PM Cần Chuẩn Bị:**
- Scope document gốc (có chữ ký)
- Email/Zalo history về yêu cầu thay đổi
- Impact analysis của từng requirement tranh chấp
- Change Log với tất cả CRs
- Timeline sự kiện theo thứ tự thời gian

---

## Template: Scope Clarification Email Gửi Khách Hàng

```
Subject: [LogiPro ERP] Scope Clarification — Yêu Cầu Ngày [XX/XX/XXXX]

Kính gửi bà Phương,

Cảm ơn bà đã chia sẻ yêu cầu bổ sung trong cuộc họp ngày [ngày]. Để đảm bảo
tiến độ dự án và quyền lợi của cả hai bên, tôi muốn làm rõ về phạm vi của
các yêu cầu này.

SAU KHI PHÂN TÍCH SCOPE DOCUMENT (SD-LogiPro-v1.0):

1. YÊU CẦU ĐÃ CÓ TRONG SCOPE (Chúng tôi sẽ implement):
   - [Liệt kê requirement, kèm reference số mục trong scope doc]

2. YÊU CẦU NGOÀI SCOPE (Cần Change Request):
   - [Tên requirement]: Không được đề cập tại scope document. Để implement,
     chúng tôi cần thực hiện qua Change Request Process theo điều khoản 7.3
     hợp đồng. Estimated impact: [X tuần], [Y triệu VND].

3. YÊU CẦU CẦN LÀM RÕ THÊM (Cần meeting):
   - [Tên requirement]: Mục [X.Y] trong scope document có thể được interpret
     theo nhiều cách. Tôi đề xuất chúng ta có một buổi họp 1 giờ để align.

TÔI ĐỀ XUẤT:
- Meeting ngày [ngày]: Làm rõ các điểm ambiguous
- Sau meeting: Tôi sẽ chuẩn bị Change Request Form cho các yêu cầu ngoài scope

Vui lòng confirm lịch hoặc đề xuất thời gian phù hợp.

Trân trọng,
Minh Tuấn
Project Manager — TechBridge Solutions
```

---

## Template: Scope Dispute Resolution Meeting Agenda

```
═══════════════════════════════════════════════════════════════
SCOPE DISPUTE RESOLUTION MEETING
Dự án: LogiPro ERP
Ngày: [XX/XX/XXXX] | Thời gian: 09:00–11:00
Địa điểm: [Văn phòng / Google Meet]
───────────────────────────────────────────────────────────────
Participants:
  TechBridge: Minh Tuấn (PM), Lan Anh (BA), [Technical Director]
  LogiPro: Bà Phương (Ops Director), [CEO hoặc đại diện có thẩm quyền]
───────────────────────────────────────────────────────────────

AGENDA:

09:00–09:10 | Opening (PM)
  - Mục tiêu của meeting: Reach agreement, không phải tranh luận
  - Ground rules: Tập trung vào hợp đồng và business value, không cá nhân

09:10–09:30 | Review Scope Document Cùng Nhau (BA)
  - Đọc lại các điều khoản liên quan đến yêu cầu đang tranh chấp
  - Không interpret, chỉ đọc nguyên văn

09:30–10:00 | Phân Loại Từng Requirement (PM + BA + Khách hàng)
  - Đi qua từng yêu cầu, phân loại: In / Ambiguous / Out
  - Document real-time trên màn hình chung

10:00–10:30 | Negotiation (Sponsor + Client Representative)
  - Với requirement ngoài scope: Agree on CR approach
  - Với requirement ambiguous: Agree on interpretation
  - Với requirement trong scope: Confirm implementation

10:30–10:50 | Action Items và Next Steps (PM)
  - CR nào cần chuẩn bị? Deadline?
  - Ai responsible cho từng action?

10:50–11:00 | Closing
  - Confirm minutes sẽ được gửi trong 24h
  - Next meeting nếu cần
───────────────────────────────────────────────────────────────
Pre-read materials: Scope Document v1.0, Requirement List từ khách hàng
Facilitator: [Neutral party hoặc Technical Director TechBridge]
═══════════════════════════════════════════════════════════════
```

---

## Cách Viết Scope Document Chuẩn Để Tránh Dispute

### 1. Dùng Acceptance Criteria Cụ Thể

Mỗi deliverable phải có acceptance criteria rõ ràng. Xem thêm tại [03-change-management.md](../03-change-management.md).

### 2. Đính Wireframe/Mockup

Trước khi ký hợp đồng, tất cả UI screens phải có wireframe (dù là low-fidelity) được khách hàng review và sign off. Đính kèm vào scope document như Appendix.

### 3. Liệt Kê Exclusions Rõ Ràng

```
PHẠM VI NGOÀI DỰ ÁN (EXCLUSIONS) — Những gì KHÔNG được bao gồm:

1. Không bao gồm phát triển mobile application (iOS/Android)
2. Không bao gồm tích hợp với bất kỳ GPS hardware hay IoT device nào
3. Không bao gồm báo cáo tùy chỉnh theo yêu cầu (chỉ có 5 báo cáo chuẩn
   theo danh sách tại Appendix C)
4. Không bao gồm migration dữ liệu lịch sử (chỉ import dữ liệu master data)
5. Không bao gồm training cho nhân viên tại chi nhánh tỉnh
6. Không bao gồm SLA 24/7 support (chỉ hỗ trợ giờ hành chính)
```

### 4. Định Nghĩa Thuật Ngữ (Glossary)

Những từ mơ hồ như "real-time", "fast", "multi-user", "comprehensive" phải được định nghĩa cụ thể:

```
Glossary:
- "Real-time": Cập nhật dữ liệu trong vòng 60 giây
- "Multi-user": Tối đa 50 concurrent users đồng thời
- "Fast": Response time < 3 giây trong điều kiện bình thường
```

---

## Bài Học Rút Ra

**Bài học 1: Scope creep là rủi ro lớn nhất trong PM — không phải technical risk**

Dự án có thể recover từ bug, từ server crash, từ key person nghỉ việc. Rất khó recover từ scope creep không kiểm soát trong fixed-price contract.

**Bài học 2: Khách hàng không xấu, nhưng họ có incentive khác với bạn**

Bà Phương không phải là người xấu — bà chỉ đang cố gắng maximize value cho công ty bà. PM cần hiểu điều này để không cảm xúc hóa conflict.

**Bài học 3: Quy trình Change Control không phải để nói "không" — để nói "yes, with informed decision"**

Khách hàng có thể có yêu cầu hợp lý và quan trọng ngoài scope. Change Control không block việc đó — nó đảm bảo decision được đưa ra với đầy đủ thông tin về impact.

**Bài học 4: PM cần có Sponsor nội bộ mạnh**

Minh Tuấn may mắn có Technical Director ủng hộ. PM không nên chiến đấu một mình với áp lực từ Account Manager.

**Bài học 5: Đừng bao giờ ký hợp đồng fixed-price với scope document mơ hồ**

Đây là nguyên nhân gốc rễ của case study này. Nếu scope document được viết tốt hơn từ đầu, 80% tranh chấp sẽ không xảy ra.

---

## Lessons Learned Chi Tiết

| # | Vấn đề | Nguyên nhân gốc | Lesson Learned | Áp dụng cho dự án sau |
|---|---|---|---|---|
| 1 | Dev implement trực tiếp theo yêu cầu KH | Thiếu quy tắc "mọi yêu cầu qua PM" | Establish ground rules trong kick-off | Slide "Team Working Agreement" trong kick-off |
| 2 | Scope document mơ hồ | Không đủ time cho requirements gathering | Tối thiểu 4 tuần cho discovery phase | Discovery phase mandatory trong project charter |
| 3 | PM bị áp lực từ Account Manager | Thiếu alignment nội bộ | Brief Account Manager trước về scope risks | Pre-sales scope review với PM |
| 4 | Không có wireframe | Tiết kiệm thời gian lúc đầu | Wireframe là mandatory cho UI requirements | Wireframe sign-off trước khi ký hợp đồng |
| 5 | Scope ambiguous về báo cáo | Câu mơ hồ "báo cáo vận hành" | Liệt kê từng deliverable + acceptance criteria | Report list với format mẫu trong scope doc |

---

## Câu Hỏi Reflection

1. Trong tình huống của Minh Tuấn, bạn sẽ xử lý Account Manager như thế nào khi bị áp lực "cứ làm đi"?

2. Nếu bạn là PM, bạn sẽ xây dựng "Working Agreement" với team như thế nào để dev không nhận yêu cầu trực tiếp từ khách hàng?

3. Trong tình huống bà Phương có relationship tốt với CEO của TechBridge, escalation path của bạn sẽ thay đổi không?

4. Nếu scope document ban đầu là do BA phía khách hàng viết (không phải TechBridge), trách nhiệm về scope ambiguity thuộc về ai?

5. Khi nào PM nên đề xuất chuyển từ fixed-price sang T&M (Time and Materials) contract?

---

*Xem tiếp: [Case Study 3 — Team Conflict](./03-team-conflict.md)*

*Xem lại lý thuyết: [../03-change-management.md](../03-change-management.md)*
