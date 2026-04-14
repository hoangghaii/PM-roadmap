# PM Frameworks — Quick Reference

> Compact reference. In ra được trên 2 trang A4. Dùng khi cần nhớ nhanh framework nào dùng cho việc gì.

---

## PRIORITIZATION FRAMEWORKS

### RICE Scoring
```
RICE = (Reach × Impact × Confidence) ÷ Effort

Reach     = số users bị ảnh hưởng trong 1 tháng
Impact    = 0.25 (minimal) | 0.5 (low) | 1 (medium) | 2 (high) | 3 (massive)
Confidence = % bạn tin vào estimates (100% = data-backed, 50% = gut feel)
Effort    = số person-months để build

Ví dụ:
Feature A: Reach=1000, Impact=2, Confidence=80%, Effort=2 months
RICE = (1000 × 2 × 0.8) ÷ 2 = 800

Dùng khi: Cần justify priority cho stakeholders với số liệu cụ thể
```

### ICE Scoring
```
ICE = Impact × Confidence × Ease (mỗi thứ 1–10)

Impact     = Nếu thành công, impact bao nhiêu?
Confidence = Bạn chắc chắn bao nhiêu % sẽ thành công?
Ease       = Dễ implement bao nhiêu? (10 = rất dễ)

Dùng khi: Prioritize growth experiments nhanh, không cần số liệu chính xác
```

### MoSCoW
```
Must Have    = Không có → product fail (launch blockers)
Should Have  = Quan trọng nhưng có workaround
Could Have   = Nice to have, cut nếu cần
Won't Have   = Không làm lần này (có thể future)

Dùng khi: Sprint planning, scope decisions, stakeholder alignment
```

### Kano Model
```
     Delighters (Wow!)          — Không expect nhưng thích khi có
     ────────────────────────
     Performance Features       — Càng nhiều càng tốt (linear satisfaction)
     ────────────────────────
     Basic/Must-have Features   — Expect mặc định, không có thì thất vọng
     ────────────────────────
     Indifferent                — Không ảnh hưởng satisfaction
     Reverse                    — Một số users không muốn

Dùng khi: Understand what truly delights users vs what's just expected
```

### Value vs Effort Matrix (2×2)
```
               LOW EFFORT    HIGH EFFORT
HIGH VALUE  |  Quick Wins  |  Major Projects  |
LOW VALUE   |  Fill-ins    |  Thankless Jobs  |

→ Prioritize Quick Wins FIRST
→ Schedule Major Projects carefully
→ Do Fill-ins only when capacity available
→ Avoid Thankless Jobs

Dùng khi: Team alignment, backlog grooming visual aid
```

---

## STRATEGY FRAMEWORKS

### SWOT Analysis
```
            HELPFUL         HARMFUL
INTERNAL  | Strengths    | Weaknesses  |
EXTERNAL  | Opportunities| Threats     |

Questions:
S: Lợi thế độc đáo của ta là gì? (tech, team, brand, data)
W: Chúng ta đang thiếu gì? (resources, skills, market access)
O: Trend nào có lợi cho ta? (market shifts, competitor weaknesses)
T: Điều gì có thể làm hại ta? (new entrants, regulation, tech change)
```

### Porter's 5 Forces
```
                    [Threat of New Entrants]
                            ↓
[Supplier Power] → [Industry Rivalry] ← [Buyer Power]
                            ↑
                  [Threat of Substitutes]

Dùng để: Đánh giá competitive landscape của một market
Mỗi force rate: Low / Medium / High
```

### TAM / SAM / SOM
```
TAM (Total Addressable Market)
└── SÃ€M (Serviceable Addressable Market)
    └── SOM (Serviceable Obtainable Market)

TAM = Tổng thị trường nếu 100% market share
SAM = Phần của TAM bạn có thể serve với model hiện tại
SOM = Phần bạn thực tế có thể đạt trong 3–5 năm

Ví dụ (Logistics startup VN):
TAM = Toàn bộ logistics market VN = $40B
SAM = SME B2B logistics = $5B (target segment)
SOM = 2% SAM trong năm 3 = $100M
```

### North Star Metric (NSM) + Input Metrics
```
North Star Metric: 1 metric capture long-term value cho users
    └── Input Metric 1: driver trực tiếp của NSM
    └── Input Metric 2: driver trực tiếp của NSM
    └── Input Metric 3: driver trực tiếp của NSM

Ví dụ (E-commerce):
NSM: Số orders hoàn thành thành công/tuần
    ├── # new users mua lần đầu
    ├── # returning users đặt thêm
    └── Average order completion rate

Ví dụ (SaaS):
NSM: Weekly Active Users doing core action
    ├── # users onboarded thành công
    ├── # users complete activation event
    └── 30-day retention rate

Lưu ý: NSM không phải revenue (revenue là outcome, không leading indicator)
```

---

## USER RESEARCH FRAMEWORKS

### Jobs To Be Done (JTBD)
```
Template: "When I [situation], I want to [motivation], so I can [expected outcome]"

Ví dụ:
"When I need to send money urgently, I want to transfer instantly without going to bank, 
so I can handle emergencies without stress."

3 loại Jobs:
Functional  = Practical task cần làm
Social      = Muốn được nhìn nhận như thế nào
Emotional   = Muốn cảm thấy như thế nào

Dùng khi: Understand WHY users use product, không chỉ WHAT they do
```

### 5 Whys
```
Vấn đề: User bỏ cart 80% trong checkout flow

Why 1: Tại sao users bỏ? → Vì thấy unexpected shipping cost
Why 2: Tại sao shipping cost unexpected? → Vì chỉ show ở step cuối
Why 3: Tại sao chỉ show ở step cuối? → Vì shipping tính theo địa chỉ
Why 4: Tại sao không hỏi địa chỉ sớm hơn? → Vì UX flow cũ từ 2019
Why 5: Tại sao không update UX flow? → Không ai track cart abandonment metric

ROOT CAUSE: Thiếu metric tracking → không biết có vấn đề
```

### Empathy Map
```
┌─────────────────┬─────────────────┐
│    THINK & FEEL │    SEE          │
│  (Beliefs,      │  (Environment,  │
│   feelings,     │   media, peers) │
│   worries)      │                 │
├─────────────────┼─────────────────┤
│    SAY & DO     │    HEAR         │
│  (Behavior,     │  (Influencers,  │
│   actions,      │   friends,      │
│   attitude)     │   channels)     │
├─────────────────┴─────────────────┤
│  PAIN          │  GAIN           │
│  (Frustrations,│  (Goals, needs, │
│  obstacles)    │  measures of    │
│                │  success)       │
└─────────────────────────────────-─┘

Dùng khi: Team alignment trước user interviews, sau research synthesis
```

---

## METRICS FRAMEWORKS

### AARRR (Pirate Metrics)
```
ACQUISITION   → Làm thế nào users tìm thấy bạn?
                Metrics: CAC, CPC, traffic sources, conversion rate
                ↓
ACTIVATION    → Users có "Aha moment" không?
                Metrics: Onboarding completion, time-to-first-value
                ↓
RETENTION     → Users có quay lại không?
                Metrics: DAU/MAU, 30-day retention, churn rate
                ↓
REFERRAL      → Users có giới thiệu cho người khác không?
                Metrics: NPS, referral rate, viral coefficient
                ↓
REVENUE       → Bạn monetize như thế nào?
                Metrics: ARPU, MRR, LTV, LTV:CAC ratio

Nguyên tắc: Fix leaks TỪ TRÊN XUỐNG. Không có retention tốt = đổ nước vào xô thủng.
```

### HEART Framework (Google)
```
H — Happiness     : Satisfaction, NPS, app store rating
E — Engagement    : DAU, session length, actions per session  
A — Adoption      : New users, feature adoption rate
R — Retention     : 30/60/90 day retention, churn rate
T — Task Success  : Completion rate, error rate, time on task

Cách dùng:
1. Chọn 2–3 dimensions relevant nhất cho feature/product
2. Define Signal (hành vi quan sát được)
3. Define Metric (cách đo signal)
```

### Health Metrics vs North Star Metrics
```
North Star Metric → Tăng trưởng dài hạn
Health Metrics    → Không để mọi thứ đổ vỡ

Health metrics ví dụ:
- Uptime ≥ 99.9%
- p95 API response time < 500ms  
- Error rate < 0.1%
- Support ticket volume (không tăng đột biến)
- Refund rate (không tăng)

Nguyên tắc: Optimize NSM KHÔNG LÀM HẠI health metrics
```

---

## PRESENTATION FRAMEWORKS

### Pyramid Principle (Barbara Minto)
```
Kết luận / Khuyến nghị (TRƯỚC TIÊN)
├── Argument 1 (support kết luận)
│   ├── Evidence 1a
│   └── Evidence 1b
├── Argument 2 (support kết luận)
│   ├── Evidence 2a
│   └── Evidence 2b
└── Argument 3 (support kết luận)

Dùng khi: Exec presentations, written PRD recommendations
Không dùng: Khi audience cần được dẫn dắt qua vấn đề trước khi nghe solution
```

### BLUF (Bottom Line Up Front)
```
[Kết luận/Action cần thiết]
[Context ngắn gọn — TẠI SAO bạn viết cái này]
[Details cho người muốn đọc thêm]

Ví dụ:
"Đề xuất: Delay feature X sang Q3 (2 tuần) để fix P0 bugs hiện tại.
Context: Chúng ta đang có 3 P0 bugs ảnh hưởng 15% users, được report trong 48 giờ qua.
Details: [link to bug report, impact analysis, proposed timeline]"

Dùng khi: Slack messages, email updates, executive summaries
```

### STAR Method (Behavioral Questions)
```
S — Situation  : Context là gì?
T — Task       : Nhiệm vụ/challenge của bạn là gì?
A — Action     : Bạn đã làm gì cụ thể? (đây là phần QUAN TRỌNG NHẤT)
R — Result     : Kết quả là gì? (PHẢI CÓ SỐ LIỆU nếu có thể)

Ví dụ answer:
S: "Team của tôi có disagreement về priority của 2 features lớn."
T: "Tôi cần align engineering, design, và business stakeholders trong 1 tuần."
A: "Tôi set up facilitated workshop, present data analysis về impact của mỗi option, 
    và dùng RICE scoring để make decision objective."
R: "Team agreed trong 2 giờ. Feature được chọn ship sau đó, tăng conversion 12%."
```

---

## MEETING FRAMEWORKS

### RACI Matrix
```
R — Responsible  : Người THỰC HIỆN công việc
A — Accountable  : Người chịu TRÁCH NHIỆM cuối cùng (chỉ 1 người)
C — Consulted    : Người cần THAM VẤN ý kiến (2-way communication)
I — Informed     : Người cần THÔNG BÁO kết quả (1-way communication)

Ví dụ (Launching new feature):
             | PM | Eng Lead | Designer | CEO |
Feature spec |  A |    C     |    C     |  I  |
Design       |  C |    I     |    R/A   |  I  |
Build        |  I |    R/A   |    C     |  I  |
Launch       |  A |    R     |    R     |  C  |
```

### DACI Matrix
```
D — Driver     : Ai DRIVE project tới đích? (PM thường là D)
A — Approver   : Ai có quyền SAY YES/NO cuối cùng?
C — Contributor: Ai ĐÓNG GÓP input và expertise?
I — Informed   : Ai cần được THÔNG BÁO về decisions?

Khác RACI: DACI dùng nhiều hơn cho decisions, RACI cho tasks
```

### Sprint Ceremonies (Scrum Quick Reference)
```
Sprint Planning  → Đầu sprint: chọn backlog items, estimate, commit
Daily Standup    → Mỗi ngày 15 phút: What did yesterday? Today? Blockers?
Sprint Review    → Cuối sprint: Demo cho stakeholders gì đã build
Sprint Retro     → Cuối sprint: What went well? What to improve? Action items
Backlog Grooming → Mid-sprint: Refine upcoming items, estimate, clarify

Sprint length: 1–2 tuần (2 tuần phổ biến nhất)
PM role trong ceremonies:
- Planning: Clarify requirements, answer questions
- Standup: Listen for blockers, không talk too much  
- Review: Present to stakeholders, collect feedback
- Retro: Facilitate (hoặc observe), action items
- Grooming: Write/refine user stories TRƯỚC meeting
```

---

## DISCOVERY FRAMEWORKS

### Continuous Discovery (Teresa Torres)
```
Opportunity Solution Tree:

[Desired Outcome — Target metric]
        |
        ├── Opportunity 1 (user pain point / unmet need)
        │   ├── Solution A → Assumption 1, Assumption 2
        │   └── Solution B → Assumption 3
        │
        └── Opportunity 2
            ├── Solution C → Assumption 4
            └── Solution D → Assumption 5, Assumption 6

Nguyên tắc:
1. Start từ outcome, không phải từ ideas
2. Identify opportunities (pain points) trước khi brainstorm solutions
3. Test RISKIEST assumptions trước, không test toàn bộ solution
```

### Product-Market Fit (PMF) Signal
```
The Sean Ellis Test:
"Nếu product này biến mất ngày mai, bạn sẽ cảm thấy như thế nào?"
  A) Rất thất vọng
  B) Hơi thất vọng
  C) Không thất vọng (có thể dùng cái khác thay)
  D) Không biết

PMF signal: ≥40% users chọn "Rất thất vọng"

Retention Curve test:
PMF khi retention curve FLATTENS (không về 0)
No PMF khi retention curve về 0 (mọi người đều churn)
```

---

*In trang này = có reference sheet trong túi khi cần.*
