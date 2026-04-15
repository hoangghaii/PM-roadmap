# Quản Lý Stakeholders

> "PM không quản lý dự án — PM quản lý con người. Dự án tự nó không gây ra vấn đề. Con người mới là nguồn gốc của mọi success và failure."

---

## Stakeholder Là Ai?

Stakeholder là bất kỳ ai có interest hoặc bị ảnh hưởng bởi dự án của bạn — dù họ có biết hay không.

**Định nghĩa mở rộng:** Bao gồm cả người bạn không thích, người không respond email, người không đến meeting, và người không bao giờ dùng sản phẩm của bạn nhưng có quyền kill dự án bất kỳ lúc nào.

Ví dụ không ngờ tới: Trưởng phòng IT security có thể là stakeholder quan trọng nhất trong dự án CRM — không phải vì anh ta dùng CRM, mà vì anh ta có quyền từ chối deployment lên production nếu không đáp ứng security requirements.

---

## Internal vs External Stakeholders

**Internal Stakeholders** (trong tổ chức):

| Loại | Ví dụ cụ thể | Quan tâm chính |
|---|---|---|
| Executive sponsor | COO, CTO, CPO | ROI, strategic alignment, budget |
| Project team | Dev, QA, Designer, BA | Clear requirements, unblocked work |
| Business owner | Product Owner, Department head | Business goals, user satisfaction |
| Support functions | IT, Legal, Finance, HR | Compliance, security, cost control |
| End users (internal) | Sales team dùng CRM, warehouse staff | Ease of use, minimal disruption |

**External Stakeholders** (ngoài tổ chức):

| Loại | Ví dụ cụ thể | Quan tâm chính |
|---|---|---|
| Khách hàng / Client | Doanh nghiệp thuê bạn build software | Delivery đúng hạn, đúng spec |
| End users (external) | Người dùng app bạn build | UX tốt, tính năng họ cần |
| Đối tác / Vendor | Payment gateway, cloud provider | Sử dụng đúng API/contract |
| Cơ quan quản lý | Ngân hàng Nhà nước, Bộ TT&TT | Compliance với quy định |
| Cổ đông | Investor của startup | ROI, burn rate, timeline to market |

---

## Primary vs Secondary Stakeholders

**Primary Stakeholders:** Trực tiếp bị ảnh hưởng bởi project outcome — thường là những người sử dụng hoặc trả tiền cho sản phẩm.

**Secondary Stakeholders:** Gián tiếp bị ảnh hưởng — có thể có influence lớn nhưng không phải người dùng trực tiếp.

Ví dụ dự án xây dựng portal nội bộ HR:
- Primary: HR team (người dùng), CEO (sponsor, người duyệt budget)
- Secondary: IT security (phải approve deployment), Finance (phải duyệt chi phí), Legal (phải review data privacy)

---

## Stakeholder Identification: Cách Tìm Đủ Stakeholders

Nhiều PM mới chỉ nghĩ đến stakeholder "rõ ràng" — và bị surprised khi ai đó xuất hiện vào phút cuối để block dự án.

### 3 Kỹ Thuật Identify Stakeholders

**1. Brainstorming với team:**

Hỏi cả team: "Ai có thể bị ảnh hưởng bởi dự án này? Ai cần biết về dự án này? Ai có thể block chúng ta?"

Gợi ý theo category: Ai phê duyệt? Ai sử dụng? Ai bị ảnh hưởng? Ai có thể phản đối? Ai có regulatory authority?

**2. Org Chart Review:**

Xem sơ đồ tổ chức và walk through từng bộ phận: "Department này có liên quan đến dự án không?" Đặc biệt chú ý: IT, Finance, Legal, Compliance — những bộ phận hay bị bỏ quên.

**3. Lessons Learned Từ Previous Projects:**

Hỏi PM của dự án trước: "Ai là stakeholder mà chúng ta không biết đến lúc đầu nhưng tạo ra vấn đề sau này?"

---

## Stakeholder Register

Tài liệu track tất cả stakeholders. Update liên tục trong suốt dự án.

| ID | Tên | Vai trò | Bộ phận | Contact | Interest | Influence | Engagement Level |
|---|---|---|---|---|---|---|---|
| S01 | Nguyễn Thị Lan | Project Sponsor | Executive | lan@abc.com | Budget/ROI | Cao | Supportive |
| S02 | Trần Văn Bình | End User Lead | Warehouse | binh@abc.com | Ease of use | TB | Neutral |
| S03 | Lê Thu Hà | IT Director | IT | ha@abc.com | Security | Cao | Resistant |
| S04 | Phạm Quang Minh | CFO | Finance | minh@abc.com | Cost control | TB | Unaware |
| S05 | Đoàn Thị Cẩm | Warehouse Staff | Operations | cam@abc.com | Daily workflow | Thấp | Resistant |

**Cột Engagement Level theo thang đo:**
- **Unaware:** Chưa biết về dự án
- **Resistant:** Biết nhưng chống đối
- **Neutral:** Biết nhưng không có ý kiến
- **Supportive:** Ủng hộ và hợp tác
- **Leading:** Chủ động thúc đẩy dự án

---

## Power/Interest Grid — Ma Trận Phân Loại Stakeholders

```
         HIGH POWER
              │
              │    KEEP SATISFIED    │    MANAGE CLOSELY
              │  ──────────────────  │  ──────────────────
              │  Sponsor thụ động   │  Executive sponsor
              │  C-level không dùng │  Key client
              │  Cơ quan quản lý    │  Khách hàng chính
              │                     │  Tech Lead (nếu critical)
              │                     │
─────────────────────────────────────────────────────────
              │                     │
              │      MONITOR        │    KEEP INFORMED
              │  ──────────────────  │  ──────────────────
              │  General public     │  End users
              │  Vendor nhỏ         │  Dev team members
              │  Government agency  │  QA team
              │  (ít liên quan)     │  Secondary stakeholders
              │
         LOW POWER
              │
              └──────────────────────────────────────────────
                   LOW INTEREST              HIGH INTEREST
```

### Keep Satisfied (High Power, Low Interest)

Đây là những người có quyền lực — có thể kill dự án — nhưng không quan tâm đến chi tiết hàng ngày.

**Chiến lược:**
- Cập nhật định kỳ ngắn gọn (executive summary 1 trang, không phải báo cáo 20 trang)
- Escalate issues đến họ chỉ khi thực sự cần quyết định ở level đó
- Đừng surprise họ với bad news — họ ghét surprises hơn bad news
- Identify trigger points: điều gì có thể khiến họ suddenly quan tâm và can thiệp?

**Ví dụ thực tế:** CFO của công ty. Ông ấy approve budget nhưng không muốn biết sprint có bao nhiêu story points. Chỉ cần nhận monthly financial summary: spent vs. plan, forecast to completion, major risks.

### Manage Closely (High Power, High Interest)

Đây là những người quan trọng nhất — vừa có quyền lực vừa quan tâm sâu đến dự án. Invest nhiều thời gian nhất vào nhóm này.

**Chiến lược:**
- Regular 1:1 meetings (ít nhất bi-weekly)
- Involve họ vào key decisions sớm — trước khi quyết định, không phải sau
- Proactive communication: share bad news sớm, đừng để họ nghe từ nguồn khác
- Understand their personal success metrics: họ cần dự án này thành công vì lý do gì?

**Ví dụ thực tế:** COO là sponsor của dự án WMS migration. Bà ấy cần dự án go-live trước Q1 vì đó là KPI của bà trong năm. Hiểu điều này giúp PM biết khi nào có thể push back và khi nào phải prioritize.

### Monitor (Low Power, Low Interest)

Không cần invest nhiều thời gian, nhưng đừng bỏ qua hoàn toàn.

**Chiến lược:**
- Đưa vào distribution list cho monthly newsletter/update
- Không cần invite vào meetings trừ khi họ liên quan trực tiếp
- Nhưng: check định kỳ xem họ có "upgrade" lên quadrant khác không (ví dụ: government agency có thể suddenly trở nên High Power nếu có quy định mới)

### Keep Informed (Low Power, High Interest)

Đây thường là end users và team members — những người bị ảnh hưởng nhiều nhất bởi outcome nhưng không có authority lớn.

**Chiến lược:**
- Regular updates qua newsletter nội bộ, Slack channel, hoặc demo sessions
- Involve họ trong UAT — họ sẽ dùng sản phẩm hàng ngày
- Lắng nghe feedback sớm — chờ đến demo cuối mới nghe feedback thường quá muộn
- Đừng oversell: nếu tính năng họ muốn không vào scope, nói thẳng thay vì vague

---

## Communication Matrix Đầy Đủ

Đây là công cụ PM dùng để plan và track communication với tất cả stakeholders.

| Stakeholder | Quan tâm gì | Báo cáo gì | Tần suất | Kênh | Format | Owner |
|---|---|---|---|---|---|---|
| Sponsor (COO) | Budget / timeline / ROI / strategic risk | Executive summary: % complete, spend vs plan, top 3 risks, decisions needed | Bi-weekly | Email + Meeting 30 phút | 1 trang PDF | PM |
| Dev Team | Technical requirements / scope / blockers | Sprint planning, daily standup, sprint review | Daily + bi-weekly sprint | Slack + Jira + Meeting | Bullet points, Jira tickets | PM + Tech Lead |
| End Users (key reps) | Tính năng, UX, training | Demo per milestone, training schedule | Per milestone (mỗi 4-6 tuần) | Meeting + Email | Live demo + slide | PM |
| Khách hàng / Client | Deadline / cost / deliverable quality | Progress report: milestone status, issues, next steps | Weekly | Email + optional meeting | Dashboard / table | PM |
| IT Director | Security, architecture, deployment requirements | Technical review checkpoint | Per major technical decision | Meeting + Email | Technical doc | PM + Tech Lead |
| CFO / Finance | Budget burn rate, forecast | Monthly financial summary | Monthly | Email | 1-trang summary | PM |
| QA Team | Test requirements, bug priorities | Bug report, test coverage | Daily | Jira + Slack | Jira dashboard | QA Lead |

**Lưu ý khi dùng Communication Matrix:**

- Format phải phù hợp với người nhận: Executive đọc 1 trang; Developer cần technical detail
- "Owner" không phải lúc nào cũng là PM — Tech Lead báo cáo technical updates cho IT Director sẽ đáng tin hơn PM làm thay
- Update matrix khi stakeholder thay đổi (người mới join, người cũ rời đi)

---

## Kỹ Thuật Quản Lý Kỳ Vọng

### Under-Promise, Over-Deliver

Đừng promise deadline optimistic để "làm stakeholder happy" rồi miss. Một lần miss deadline làm mất trust rất khó lấy lại.

**Thực hành:** Khi estimate, thêm buffer 20% vào con số bạn confident. Nếu finish sớm hơn → bạn trông như hero. Nếu trúng đúng → bạn deliver như expected.

### Proactive Communication: Bad News First

Nguyên tắc: Stakeholder nên nghe bad news từ PM trước, không phải từ nguồn khác.

Nếu sponsor nghe từ CFO rằng project trễ trước khi PM báo cáo → PM mất trust nghiêm trọng. Dù tin tức không tốt, chủ động báo sớm luôn được đánh giá cao hơn là im lặng.

**Template "bad news proactive":**

> "Tôi muốn update anh/chị sớm về một rủi ro vừa phát sinh. [Mô tả ngắn gọn]. Đây là impact đánh giá: [X]. Chúng tôi đang làm [Y] để address. Cần anh/chị quyết định về [Z] trước [deadline]. Tôi sẽ update thêm vào [thời gian cụ thể]."

### Stakeholder Engagement Levels

Mục tiêu của PM: di chuyển stakeholder từ Unaware/Resistant → Supportive.

```
Unaware → Aware: Inform (share project overview, rationale)
Aware → Resistant: Listen first (hiểu tại sao họ resist), address concerns
Resistant → Neutral: Involve (invite họ vào input session, address feedback)
Neutral → Supportive: Demonstrate value (show early wins, address pain points)
Supportive → Leading: Empower (give them ownership of pieces they care about)
```

---

## Difficult Stakeholders: 5 Loại và Cách Xử Lý

### 1. The Micromanager

**Biểu hiện:** Yêu cầu update hàng ngày dù không cần thiết. Approve từng small decision. Attend tất cả meetings kể cả technical standup.

**Nguyên nhân thực sự:** Thiếu trust (do PM chưa build được), lo lắng về dự án, hoặc đơn giản là management style của họ.

**Cách xử lý:**
- Tăng frequency và quality của updates chủ động → giảm nhu cầu họ hỏi
- Explicit meeting: "Tôi sẽ gửi daily summary 5pm mỗi ngày để anh/chị luôn updated. Điều đó có đủ để anh/chị comfortable không?"
- Build trust qua small wins trước — deliver đúng promise nhiều lần liên tiếp
- Nếu là behavioral issue không thể thay đổi: adapt — tăng reporting detail, maintain composure

---

### 2. The Ghost (Không Respond)

**Biểu hiện:** Không reply email trong nhiều ngày. Không đến meetings dù đã đồng ý. Không review tài liệu dù cần sign-off.

**Hậu quả:** Decision bị blocked, dự án bị delay.

**Cách xử lý:**
- Đổi channel: nếu email không hiệu quả → Slack → điện thoại → gặp trực tiếp
- Rút ngắn request: thay vì "review 20-trang doc", hỏi "cần 5 phút để confirm 1 điểm"
- Add urgency với deadline rõ ràng: "Tôi cần confirm trước thứ Sáu 17:00 để không delay sprint tiếp theo"
- Escalate một cách khéo léo: cc manager của họ vào email nếu đã nhắc 3 lần không response — không phải để complain, mà để visibility
- Tactic "assumed approval": "Nếu tôi không nhận được phản hồi trước [ngày], tôi sẽ proceed với phương án A. Vui lòng chỉ báo nếu có phản đối."

---

### 3. The Scope Creeper

**Biểu hiện:** Liên tục thêm yêu cầu mới trong mỗi cuộc họp. "Thêm cái này không khó đâu, chỉ cần..." Không hiểu (hoặc không muốn hiểu) trade-offs.

**Cách xử lý:**
- Có Charter signed với Scope IN/OUT rõ ràng — document is your shield
- Quy trình change request formal: mọi yêu cầu mới đều phải đi qua "Change Request Form" với impact analysis
- Nói "yes, and": thay vì "No", nói "Yes, chúng ta có thể thêm. Để đánh giá impact và bổ sung vào plan. Change request sẽ mất khoảng [X] ngày và [Y] cost. Bạn muốn proceed không?"
- Protect team: PM không được để scope creep invisible với team. Nếu scope thêm mà không có thêm resource → PM phải fight cho team, không phải im lặng để "giữ hòa khí"

---

### 4. The Pessimist

**Biểu hiện:** "Cái này không làm được đâu", "Dự án kiểu này chắc chắn trễ", "Team không đủ năng lực". Thường là người từng bị tổn thương bởi project failures trong quá khứ.

**Cách xử lý:**
- Đừng argue về optimism/pessimism — thay vào đó, hỏi: "Theo bạn, risk lớn nhất là gì? Chúng ta có thể làm gì để address nó?"
- Convert pessimism thành valuable risk input: "Tôi appreciate bạn thấy những điều tôi có thể bỏ sót. Bạn có thể giúp tôi tạo risk mitigation plan không?"
- Show early wins: deliver small milestones đúng hẹn để dần dần rebuild trust
- Acknowledge khi họ đúng: nếu concern của họ trở thành vấn đề thực sự, credit họ đã raise nó sớm

---

### 5. The Political Player

**Biểu hiện:** Có agenda ẩn. Dự án này liên quan đến power struggles giữa departments. Thay đổi lập trường theo người có mặt trong phòng.

**Cách xử lý:**
- Understand the politics trước khi bắt đầu: hỏi sponsor "Ai có thể không muốn dự án này thành công và tại sao?"
- Document mọi decisions và agreements bằng văn bản: "Như đã thảo luận trong meeting ngày X, chúng ta đã đồng ý Y. Tôi cc anh/chị trong email này để confirm."
- Không chọn phe trong internal politics
- Leverage sponsor: nếu political player đang block dự án vì lý do internal politics, escalate cho sponsor để unblock

---

## Meeting Management

### 3 Loại Meeting Phổ Biến

**1. Daily Standup (15 phút)**

Format: Mỗi người nói:
- Hôm qua làm gì?
- Hôm nay làm gì?
- Có blocker gì không?

PM role: Facilitate, ghi lại blockers, follow-up ngay sau standup. Không để standup trở thành status report dài dòng.

**2. Status Update Meeting (30–45 phút)**

Với stakeholders, không phải với dev team.

Agenda template:
```
[5 phút]  Recap từ meeting trước — decisions đã made, actions đã done
[10 phút] Current status: milestones, % complete, burn rate
[10 phút] Risks & issues: mới phát sinh, đã resolve
[10 phút] Next steps: upcoming milestones, decisions needed
[5 phút]  Q&A
```

**3. Decision Meeting (60–90 phút)**

Dùng khi cần stakeholder quyết định về trade-off lớn.

Agenda template:
```
[10 phút] Context: tại sao cần quyết định này và tại sao bây giờ?
[20 phút] Analysis: 3 options với pros/cons/recommendation
[30 phút] Discussion
[10 phút] Decision & next steps
[10 phút] Document decision, assign action items
```

**Facilitation tips:**
- Gửi agenda trước ít nhất 24 giờ
- Có "parking lot" cho topics ngoài agenda
- End meeting với: "Decision made: [X]. Action items: [tên] sẽ làm [Y] trước [date]."
- Send meeting notes trong vòng 24 giờ sau meeting

---

## Escalation Path

**Khi nào cần escalate:**

Escalate là khi PM không có authority hoặc resource để resolve issue một mình. Không phải sign of weakness — là sign of good judgment.

Escalate khi:
- Issue ảnh hưởng đến scope/timeline/budget vượt thẩm quyền của PM
- Conflict giữa stakeholders không tự giải quyết được
- Risk materializes mà mitigation plan không đủ
- Team bị blocked bởi external dependency mà PM không thể unblock

**Cách escalate không làm mất relationship:**

```
1. Chuẩn bị trước:
   - Có đủ data (không escalate bằng cảm giác)
   - Có ít nhất 2-3 options kèm recommendation
   - Đã thử resolve ở level thấp hơn

2. Framing đúng:
   KHÔNG: "Anh X đang block dự án của chúng ta"
   CÓ: "Tôi cần anh/chị hỗ trợ unblock một issue đang ảnh hưởng đến milestone M3"

3. Structure:
   - Tóm tắt vấn đề (2-3 câu)
   - Impact nếu không giải quyết
   - Options PM đã cân nhắc
   - Cần sự hỗ trợ gì cụ thể từ escalation target
   - Timeline cần quyết định

4. Follow-up:
   - Sau khi escalate, confirm lại trong email
   - Document outcome
   - Cảm ơn người hỗ trợ unblock (ngay cả khi đó là việc của họ)
```

---

## Ví Dụ Thực Tế: Communication Plan Hoàn Chỉnh — Dự Án ERP 6 Tháng

**Dự án:** Triển khai ERP cho nhà máy sản xuất, 6 tháng, 4 modules.

**Stakeholder Map:**

```
HIGH POWER
    │   [Keep Satisfied]          [Manage Closely]
    │   CFO: monthly budget        COO (Sponsor): bi-weekly
    │   IT Director: security      Factory Manager: weekly
    │   Board member: quarterly    Project steering committee: monthly
    │
    ├─────────────────────────────────────────────────────
    │   [Monitor]                 [Keep Informed]
    │   Government/compliance     20 end users (production staff)
    │   General IT staff          3rd party vendor (ERP supplier)
    │   Other department heads    QA team
LOW POWER
    │
    └──────────────────────────────────────────────
         LOW INTEREST              HIGH INTEREST
```

**Communication Calendar (ví dụ tháng 2/6):**

| Tuần | Hoạt động | Đối tượng | Format |
|---|---|---|---|
| Tuần 1, Thứ 3 | Bi-weekly sponsor meeting | COO | 30 phút meeting + 1-page summary |
| Tuần 1, Thứ 6 | Weekly progress report email | Factory Manager + IT Director | Email với dashboard screenshot |
| Tuần 2, Thứ 2 | Sprint planning | Dev team | 2 giờ meeting |
| Tuần 2, Thứ 6 | Weekly progress report email | Factory Manager + IT Director | Email |
| Tuần 3, Thứ 3 | Milestone demo (M2: Design complete) | Sponsor + Factory Manager + Key users | 1 giờ meeting + live demo |
| Tuần 3, Thứ 6 | Steering committee report | COO + CFO + IT Director | 15 phút, slide deck 5 trang |
| Mỗi ngày 9:00 | Daily standup | Dev team + QA + BA | 15 phút |
| Cuối tháng | Financial summary | CFO | Email, 1 trang |

**Template Email Weekly Status Report:**

```
Subject: [ERP Project] Weekly Update — Tuần X/24 (DD/MM - DD/MM)

Anh/Chị [Tên],

OVERALL STATUS: 🟢 On Track / 🟡 At Risk / 🔴 Off Track

MILESTONES:
✅ M1 (Analysis): Complete (03/09/2025)
🔄 M2 (Development Sprint 1): 65% complete, on track for 24/10
⏳ M3 (Development Sprint 2): Not started, scheduled 25/10

TUẦN NÀY:
- Hoàn thành: Module nhập kho backend API (đúng kế hoạch)
- Đang làm: Module xuất kho UI (60%)
- Blocker: Database migration script cần review từ IT Director (đã gửi ngày 14/10)

TUẦN TỚI:
- Complete module xuất kho UI + basic testing
- Begin integration testing giữa module A và B
- Cần: IT Director review + approve migration script trước 18/10

RISKS:
⚠️ IT Director review chưa confirm — nếu delay thêm 3 ngày có thể impact M3 deadline

Trân trọng,
[Tên PM]
```

---

*Tiếp theo: [case-studies/01-du-an-tre-deadline.md](./case-studies/01-du-an-tre-deadline.md) — Case study thực tế về xử lý dự án trễ deadline*
