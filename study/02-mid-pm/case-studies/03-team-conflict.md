# Case Study 3: Team Conflict — Frontend vs Backend

**Cấp độ:** PM Chính Thức
**Kỹ năng:** Conflict resolution, facilitation, decision-making
**Độ phức tạp:** ⭐⭐⭐ Trung bình — Cao
**Thời gian đọc:** ~20 phút

---

## Bối Cảnh

**Công ty:** Digital Flow — startup SaaS 40 người, đang develop platform quản lý chuỗi cung ứng
**Dự án:** Xây dựng Order Management Module — một trong các module cốt lõi của platform
**Timeline:** 8 tuần, đang ở tuần 4

**Team:**
- **Hùng** — Senior Backend Developer, 6 năm kinh nghiệm, kiến trúc API chính của platform
- **Trang** — Senior Frontend Developer, 4 năm kinh nghiệm, lead UI/UX implementation
- **PM:** Quốc Anh, PM 3 năm, nền tảng từ QA engineer

**Vấn đề:** Hùng và Trang xung đột về cách thiết kế API cho tính năng Order Filtering. Dự án bị block 3 ngày — frontend không thể tiếp tục vì backend chưa finalize API contract, backend từ chối thay đổi design vì "frontend không hiểu performance implications."

---

## Diễn Biến Xung Đột

**Ngày 1:** Trang gửi request cho Hùng: "Mình cần API trả về full order object với nested customer data để hiển thị trên bảng danh sách."

**Ngày 1 (chiều):** Hùng từ chối: "Full nested object quá heavy, mỗi request có thể lên đến 50KB. Mình sẽ làm API trả về flat structure với customer_id, FE tự gọi thêm API nếu cần."

**Ngày 2:** Trang phản đối: "Nếu vậy FE phải làm N+1 requests, user experience sẽ rất tệ khi load 100 orders là 101 API calls."

**Ngày 2 (chiều):** Hùng leo thang: "Trang không hiểu database architecture, nested data sẽ gây join hell ở database layer."

**Ngày 3 sáng:** Cả hai không nói chuyện với nhau. Trang mang vấn đề lên PM với thái độ "anh giải quyết đi." Hùng nói với PM "tôi không thể làm việc với người thiếu technical knowledge."

**3 ngày trôi qua, 0 dòng code được viết.**

---

## Nguyên Nhân Thực Sự Thường Gặp Trong Conflict Kỹ Thuật

Phần lớn conflict kỹ thuật không phải về kỹ thuật. Quốc Anh nhận ra sau khi 1-on-1 với từng người:

```
Vấn đề bề mặt:          API design: nested vs flat

Vấn đề thực sự:
  ├── Hùng: Ego + Ownership — Cảm thấy frontend đang "xâm phạm" 
  │         lãnh địa kỹ thuật của mình. Lo sợ bị blame nếu API
  │         performance xấu.
  │
  ├── Trang: Frustration + Deadline pressure — Đã bị block 2 ngày,
  │          cảm thấy không được respect khi expertise bị dismiss.
  │
  └── Structural: Không có "API Design Agreement" từ đầu dự án,
                  không ai define ai có authority gì.
```

---

## Thomas-Kilmann Conflict Model: 5 Phong Cách Xử Lý Conflict

```
High │  Competing         Collaborating
     │  (Win-Lose)        (Win-Win)
     │  Hùng dùng style   → PM nên hướng đến đây
A    │  này lúc đầu
s    │
s    │          Compromising
e    │          (Middle ground)
r    │
t    │  Avoiding          Accommodating
i    │  (Lose-Lose)       (Lose-Win)
v    │  Trang bắt đầu     Nguy hiểm nếu
e    │  dùng style này    dùng sai người
n    │
e    └──────────────────────────────────
ss        Low                    High
                 Cooperativeness
```

### 5 Phong Cách Và Khi Nào Dùng

| Style | Mô tả | Dùng khi nào | Không nên dùng khi |
|---|---|---|---|
| **Competing** | Tôi thắng, anh thua. Dùng authority hoặc argument mạnh. | Quyết định gấp, emergency, vấn đề ethics rõ ràng | Cần buy-in dài hạn từ team |
| **Collaborating** | Cùng tìm giải pháp mới tốt hơn cả hai phương án ban đầu | Có thời gian, relationship quan trọng, vấn đề phức tạp | Deadline gấp hoặc vấn đề không quan trọng |
| **Compromising** | Mỗi bên nhường một chút — nobody fully happy | Khi collaborating không đủ thời gian, balance of power ngang nhau | Khi một bên rõ ràng đúng hơn |
| **Avoiding** | Né tránh conflict, không quyết định | Cần thêm thông tin, conflict sẽ tự giải quyết, quá nhỏ để quan tâm | Vấn đề quan trọng, cần quyết định sớm |
| **Accommodating** | Tôi thua để anh thắng — preserve relationship | Vấn đề quan trọng hơn với phía kia, bạn biết mình sai | Routinely — mất credibility |

**Trong case này:** PM cần hướng tới **Collaborating** nhưng có thể phải dùng **Compromising** nếu không đủ thời gian.

---

## Hướng Xử Lý PM Từng Bước

### Bước 1: Tổ Chức 1-on-1 Meeting Với Từng Bên

Quốc Anh gặp riêng từng người trong 30 phút — không có mặt người kia. Mục đích: understand perspective, defuse emotion, identify common ground.

**5 Câu Hỏi PM Hỏi Mỗi Bên:**

```
1. "Hãy mô tả cho tôi hiểu vấn đề kỹ thuật từ góc nhìn của bạn — 
   không phán xét, tôi chỉ muốn hiểu."
   → Để nghe perspective đầy đủ, không interrupt

2. "Điều gì quan trọng nhất với bạn trong cách giải quyết API design này?"
   → Identify underlying interests (performance? UX? timeline?)

3. "Nếu không có constraint nào, giải pháp lý tưởng của bạn là gì?"
   → Mở không gian sáng tạo, tránh positional bargaining

4. "Bạn nghĩ concern chính của [người kia] là gì?"
   → Kiểm tra empathy, identify misunderstanding

5. "Deadline tuần sau — nếu chúng ta không quyết định hôm nay, 
   điều gì sẽ xảy ra với delivery?"
   → Bring back to project reality, reduce ego factor
```

**Điều Quốc Anh Phát Hiện:**
- Hùng thực ra không phản đối nested data về mặt kỹ thuật — anh lo ngại về cách viết query và cần thêm thời gian optimize
- Trang không nhất thiết cần full nested object — cô chỉ cần đủ data để render list view mà không cần extra API call
- Cả hai đều muốn dự án thành công — conflict là về cách làm, không phải về mục tiêu

### Bước 2: Phân Tích — Vấn Đề Kỹ Thuật Hay Ego?

```
DIAGNOSIS CHECKLIST:

Dấu hiệu là vấn đề kỹ thuật thuần túy:
  ☐ Cả hai đều cite technical evidence (benchmarks, docs)
  ☐ Không có cá nhân hóa ("design này tệ" vs "anh/chị tệ")
  ☐ Cả hai sẵn sàng xem xét giải pháp thứ ba
  ☐ Conversation productive khi không có áp lực

Dấu hiệu có ego/interpersonal:
  ☑ Dùng ngôn ngữ dismissive ("không hiểu", "thiếu kiến thức")
  ☑ Từ chối nghe perspective của người kia
  ☑ Escalate lên PM thay vì tự giải quyết
  ☑ Không nói chuyện trực tiếp với nhau

Kết luận case này: 70% ego + interpersonal, 30% technical
```

### Bước 3: Tổ Chức Meeting Chung — Facilitation Guide

```
CONFLICT RESOLUTION MEETING
Thời gian: 60 phút
Participants: Hùng, Trang, PM (Quốc Anh)
Tech Lead được mời nếu cần technical tiebreak

───────────────────────────────────────────
AGENDA:

0:00–0:05 | Ground Rules (PM)
  "Mục tiêu hôm nay là tìm giải pháp technical tốt nhất cho user.
   Không phán xét cá nhân. Mọi ý kiến đều được nghe.
   Chúng ta sẽ ra khỏi đây với một quyết định."

0:05–0:15 | Trang trình bày (3 phút) + Q&A không tranh luận (7 phút)
  "Trang, hãy describe FE requirement: cần gì từ API để render
   Order List view đúng performance."
  Rule: Hùng chỉ hỏi clarifying questions, chưa argue

0:15–0:25 | Hùng trình bày (3 phút) + Q&A không tranh luận (7 phút)
  "Hùng, hãy describe BE constraint: performance concern cụ thể là gì,
   có số liệu hoặc ước tính không?"
  Rule: Trang chỉ hỏi clarifying questions, chưa argue

0:25–0:40 | Brainstorm giải pháp (PM facilitate)
  PM viết lên whiteboard: 3 options
    Option A: Full nested (Trang muốn) — đánh giá pros/cons
    Option B: Flat + extra calls (Hùng đề xuất) — đánh giá pros/cons
    Option C: Partial nested (fields-selection) — giải pháp mới
  Mỗi người rate từng option: Feasibility (1-5), UX (1-5), Performance (1-5)

0:40–0:55 | Quyết định
  Xem xét scoring, discuss trade-offs
  Nếu không đồng ý → Tech Lead hoặc Architect tiebreak
  Document decision + rationale

0:55–1:00 | Action Items
  Ai làm gì, deadline khi nào?
───────────────────────────────────────────
```

**Kết quả thực tế của meeting:** Team discover Option C — API hỗ trợ GraphQL-style field selection. FE specify exactly những fields cần, BE query exactly những gì được yêu cầu. Cả hai side đều win.

### Bước 4: Focus Vào Deliverable, Không Phải Ego

PM Quốc Anh dùng câu hỏi này để redirect conversation bất cứ khi nào nó đi lạc:

> "Hãy quay lại với người dùng cuối — khi người dùng mở trang danh sách đơn hàng, điều họ cần là gì? Và cái gì sẽ cho họ trải nghiệm tốt nhất trong thực tế?"

Khi focus về user outcome thay vì "ai đúng," conversation trở nên collaborative hơn.

### Bước 5: Nếu Không Giải Quyết Được → Escalate Lên Tech Lead

PM không cần phải là người đưa ra quyết định kỹ thuật. Nếu sau 60 phút không có consensus, PM làm:

1. Document cả hai positions và reasoning
2. Request Tech Lead hoặc Architect review
3. Tech Lead đưa ra binding decision trong 24h
4. PM ensure decision được communicate và respected bởi cả hai bên

**Điều quan trọng:** PM không được phép để conflict kéo dài vô thời hạn. Nếu cần escalate, escalate — đó không phải failure của PM.

### Bước 6: Document Quyết Định — Architecture Decision Record (ADR)

```
═══════════════════════════════════════════════════════════════
ADR-007: Order Filtering API Design
Status: ACCEPTED
Date: [Ngày]
Deciders: Hùng (BE), Trang (FE), Quốc Anh (PM)
───────────────────────────────────────────────────────────────
CONTEXT:
Order List view cần hiển thị thông tin order kèm customer name,
status, và total amount. FE cần data này trong single API call
để avoid N+1 requests. BE có performance concern với full nested object.

DECISION:
Implement API với field selection support. Client specify fields
cần thiết trong request. BE chỉ query và return exactly those fields.

Example request:
GET /api/orders?fields=id,status,total,customer.name,customer.email

RATIONALE:
- Giải quyết N+1 problem của FE
- BE control query optimization
- Flexible cho các views khác nhau trong tương lai
- Industry-proven pattern (GraphQL, sparse fieldsets)

ALTERNATIVES CONSIDERED:
- Full nested object: Rejected — payload quá lớn cho list view
- Flat + extra calls: Rejected — N+1 performance issue

CONSEQUENCES:
- BE cần implement field parsing logic (~2 days extra effort)
- FE cần specify fields explicitly trong every request
- Cần documentation cho API consumers
═══════════════════════════════════════════════════════════════
```

---

## Nguyên Tắc: PM Không Cần Biết Đúng/Sai Kỹ Thuật

Đây là insight quan trọng nhất trong case study này.

Nhiều PM (đặc biệt là PM có nền tảng technical) mắc lỗi cố gắng judge xem ai đúng về kỹ thuật. Đây là sai lầm vì:

1. **PM thường không có đủ context kỹ thuật** để judge đúng
2. **Việc PM chọn bên sẽ tạo ra "loser"** — người không được chọn sẽ disengaged
3. **Technical landscape thay đổi** — hôm nay đúng, mai có thể sai
4. **PM's job là process, not solution**

Nhiệm vụ của PM trong technical conflict:
```
✓ Tạo không gian để cả hai bên được nghe
✓ Đảm bảo decision được đưa ra bởi đúng người (technical authority)
✓ Document decision và rationale để team có thể move on
✓ Ensure conflict không block project progress
✓ Address underlying interpersonal issues sau khi technical issue resolved
```

---

## 5 Kỹ Thuật Facilitation Meeting Để Giải Quyết Conflict

### 1. Silent Brainstorming (1-2-4-All)

Mỗi người viết ý kiến độc lập trước (1), sau đó share với 1 người (2), nhóm 4 người (4), rồi share all. Giảm ảnh hưởng của người nói to nhất.

### 2. Interests Behind Positions

Khi hai người đưa ra positions đối lập, PM hỏi: "Điều gì khiến bạn cần điều đó?" — thường interests có thể được thỏa mãn bởi nhiều giải pháp khác nhau.

### 3. Dot Voting

Khi có nhiều options, cho mỗi người 3-5 "dots" (điểm) để vote cho options họ thích. Visual, nhanh, không bị influence bởi người nói to nhất.

### 4. Trade-off Matrix

Vẽ bảng với options ở cột và criteria ở hàng. Score mỗi ô. Quyết định dựa trên data, không phải emotion.

```
            Option A  Option B  Option C
Performance    3         5         4
UX             5         2         4
Dev Effort     4         4         2
Flexibility    2         2         5
TOTAL         14        13        15  ← Winner
```

### 5. Roman Vote

Sau khi trình bày solution, mọi người giơ ngón tay cái:
- Ngón cái lên: Tôi ủng hộ và sẽ execute
- Ngón cái ngang: Tôi có reservation nhưng có thể sống với quyết định này
- Ngón cái xuống: Tôi phản đối — cần được nghe lý do trước khi proceed

---

## Conflict Prevention: Tránh Từ Đầu

### API Design Document

Trước khi bắt đầu sprint, tạo "API Contract" được sign-off bởi cả FE và BE:

```
API Contract — Order Module v1.0
Sign-off: Hùng (BE), Trang (FE), PM

Endpoint: GET /api/orders
Response format: [định nghĩa cụ thể]
Performance target: < 200ms cho 1000 records
Payload size target: < 10KB per page
Versioning: /api/v1/orders
```

### Definition of Done (DoD) Cho API

```
API được coi là DONE khi:
☐ Endpoint hoạt động theo spec đã agree
☐ Response time < threshold đã define
☐ Documentation viết trên Swagger
☐ FE đã test và confirm usable
☐ Unit test coverage > 80%
```

### Team Charter

Trong kick-off, agree về decision-making process:

```
TEAM DECISION-MAKING AGREEMENT:

Technical decisions:
  - FE decisions (UI, UX, state management): Trang quyết định
  - BE decisions (DB, infra, deployment): Hùng quyết định
  - Cross-cutting (API design, data flow): Cần agreement của cả hai
    → Nếu không agree trong 1 ngày → escalate lên Tech Lead

Communication:
  - Technical dispute phải qua PM, không bypass
  - Mọi decision > 4 giờ effort phải document
```

---

## Khi Nào PM Tự Xử Lý vs Khi Nào Escalate

```
PM tự xử lý:
├── Conflict về process/communication (không phải technical)
├── Personality clash nhẹ
├── Misunderstanding có thể giải quyết bằng facilitation
└── Đã có solution option nhưng cần facilitation để reach agreement

Escalate lên Tech Lead/Architect:
├── Conflict về technical architecture decision
├── Cả hai bên có technical arguments valid, không rõ bên nào đúng
└── Risk về scalability/security cần expert opinion

Escalate lên HR/Management:
├── Conflict mang tính personal, hostile behavior
├── Một người từ chối tham gia conflict resolution process
└── Pattern lặp đi lặp lại sau khi đã address nhiều lần
```

---

## Ví Dụ Thực Tế Việt Nam: Tính Tập Thể vs Cá Nhân

Văn hóa làm việc Việt Nam có đặc điểm đáng chú ý trong conflict management:

**Tính tập thể (Collectivism):** Người Việt thường tránh conflict công khai để "giữ hòa khí" và "không mất mặt" trước đồng nghiệp. Điều này dẫn đến:
- Conflict được giấu bên trong, bùng phát muộn và mạnh hơn
- Người thua cuộc trong public thường hold grudge lâu hơn
- 1-on-1 conversations hiệu quả hơn group confrontations

**Implications cho PM Việt Nam:**
- Ưu tiên giải quyết 1-on-1 trước khi bring vào group
- Khi đưa ra quyết định, frame theo "vì project và team" thay vì "ai đúng"
- Sau conflict resolution, tạo cơ hội để cả hai bên "save face"

**Script phù hợp văn hóa Việt:**
> "Cả Hùng và Trang đều có những điểm rất valid và thể hiện sự quan tâm đến chất lượng dự án. Giải pháp chúng ta vừa tìm ra thực ra kết hợp insight của cả hai — đây là một ví dụ tốt về teamwork."

---

## Lessons Learned

1. **Conflict không được giải quyết sẽ tốn kém hơn bạn nghĩ** — 3 ngày block của 2 senior dev = ~15 triệu VND + team morale

2. **PM phải act sớm** — Quốc Anh chờ đến ngày 3 mới can thiệp. Ngày 1 hoặc 2 đã nên nhảy vào.

3. **Technical conflict thường là symptom của process gap** — không có API design process là root cause

4. **ADR (Architecture Decision Record) nên là standard** — sau case này, Digital Flow implement ADR cho mọi technical decision lớn

5. **1-on-1 trước, group sau** — always. Không bao giờ tổ chức group conflict resolution mà không biết trước perspective của từng bên.

---

*Xem tiếp: [../../03-senior-pm/README.md](../../03-senior-pm/README.md)*

*Xem lại: [Case Study 2 — Khách Hàng Khó Tính](./02-khach-hang-kho-tinh.md)*
