# OKRs và Strategic Alignment

## Tại Sao Senior PM Cần Hiểu OKRs?

Project Manager cấp thấp hỏi: *"Dự án có on track không?"*
Senior PM hỏi: *"Dự án này đang tạo ra business value gì? Liệu chúng ta có đang build đúng thứ không?"*

Đây là sự khác biệt cốt lõi. Ở cấp Senior, bạn không chỉ deliver dự án — bạn phải đảm bảo dự án **đóng góp vào mục tiêu chiến lược** của công ty.

---

## OKRs Framework

### Định Nghĩa

**OKR = Objectives + Key Results**

| | Objective | Key Results |
|---|---|---|
| **Bản chất** | Định tính, aspirational, inspiring | Định lượng, measurable, time-bound |
| **Câu hỏi** | "Chúng ta muốn đi đâu?" | "Chúng ta biết mình đã đến chưa?" |
| **Ví dụ** | "Trở thành lựa chọn hàng đầu của logistics SME tại VN" | "Onboard 5 khách hàng mới trong Q3" |

### OKRs vs KPIs

| | OKRs | KPIs |
|---|---|---|
| **Mục đích** | Định hướng đột phá, thay đổi | Đo lường vận hành thường ngày |
| **Tần suất** | Quarterly | Monthly/Weekly |
| **Score** | 0.7 = tốt (stretch goal) | 1.0 = đạt yêu cầu |
| **Ví dụ** | Tăng NPS từ 20 lên 40 | Uptime 99.9%, response time <2s |

**Rule of thumb:** Nếu bạn chắc chắn 100% đạt được, đó không phải OKR tốt — đó là KPI.

---

## Ví Dụ OKRs Thực Tế

```
Company Level:
Objective: Tăng market share ở mảng logistics phần mềm tại VN
  KR1: Onboard 5 khách hàng enterprise mới trong Q3
  KR2: Giảm churn rate từ 15% xuống 8%
  KR3: NPS score ≥ 40

Product Team OKRs (align với Company):
Objective: Cải thiện trải nghiệm người dùng để giữ chân khách hàng
  KR1: Giảm thời gian onboarding từ 3 ngày xuống 1 ngày
  KR2: Tăng DAU/MAU ratio từ 40% lên 60%
  KR3: Giảm support tickets liên quan đến UX xuống 30%

→ Dự án "Real-time Tracking Feature" PM đang manage:
   Liên kết với Company KR2 (giảm churn) và KR3 (tăng NPS)
   Liên kết với Product KR2 (tăng engagement)
```

**PM cần biết:** Đây là lý do dự án tồn tại — không phải chỉ deliver feature.

---

## Cách Link Dự Án vào OKRs

### Strategy Map (từ trên xuống)
```
Company Strategy
      ↓
Company OKRs (Board/C-level)
      ↓
Department OKRs (VP/Director)
      ↓
Team OKRs (Manager)
      ↓
Projects & Initiatives (PM)
      ↓
Features & Tasks (Developer)
```

### Template "Project-OKR Alignment"

| Project | Liên kết với OKR | KR cụ thể | Expected Contribution | Measurement |
|---|---|---|---|---|
| Real-time Tracking | Company KR2: Giảm churn | Giảm churn từ 15% → 8% | Tracking giúp khách hàng không bị surprise | Churn rate sau 3 tháng go-live |
| Self-service Portal | Company KR3: NPS ≥ 40 | NPS tăng 10 điểm | Giảm dependency vào support team | NPS survey Q4 |

---

## Business Case Writing

Khi Senior PM cần justify một dự án với Board/C-level, phải viết Business Case:

### Structure Business Case

```markdown
## 1. Executive Summary (1 trang)
   - Vấn đề/cơ hội
   - Solution đề xuất
   - Expected benefits và costs
   - Recommendation

## 2. Problem Statement
   - Situation hiện tại (với data)
   - Consequences nếu không làm gì
   
## 3. Options Analysis
   Option A: Do nothing (baseline)
   Option B: Minimal solution
   Option C: Recommended solution
   Option D: Maximal solution
   
## 4. Recommended Solution
   - Description
   - Implementation approach
   - Timeline
   - Resources needed

## 5. Financial Analysis
   - Costs (one-time + recurring)
   - Benefits (quantified)
   - ROI / Payback period
   - NPV nếu cần
   
## 6. Risks
   - Top 3-5 risks và mitigation

## 7. Recommendation & Next Steps
```

---

## ROI Calculation cho Dự Án IT

### Simple ROI Formula

```
ROI = (Net Benefits / Total Costs) × 100%

Net Benefits = Total Benefits - Total Costs
Payback Period = Total Costs / Annual Benefits
```

### Ví Dụ: Dự Án Automation cho Quy Trình Kế Toán

**Costs:**
```
Development:     150 triệu VND (one-time)
Infrastructure:   20 triệu VND (one-time)
Training:         10 triệu VND (one-time)
Maintenance:      15 triệu VND/năm (recurring)
Total Year 1:    195 triệu VND
Total 3 năm:     240 triệu VND
```

**Benefits (quantified):**
```
Giảm 2 FTE kế toán:        300 triệu VND/năm
Giảm lỗi → giảm audit cost: 30 triệu VND/năm
Faster closing (3 ngày → 1 ngày):
  → 2 ngày × 5 người × 200 ngày/năm = 50 triệu VND/năm
Total Annual Benefits:      380 triệu VND/năm
```

**Analysis:**
```
Net Benefits (3 năm) = 380×3 - 240 = 900 triệu VND
ROI = 900/240 = 375%
Payback Period = 195/380 = 0.51 năm ≈ 6 tháng
```

### Intangible Benefits
Không phải lúc nào cũng quantify được — nhưng vẫn phải mention:
- Improved employee satisfaction (giảm manual work)
- Better compliance posture
- Scalability cho growth
- Competitive advantage

---

## Benefits Realization Plan

**Vấn đề thực tế:** Nhiều dự án deliver đúng scope, đúng hạn, đúng budget — nhưng không tạo ra business value đã hứa.

### Benefits Realization Framework

```
Project Charter     Go-live          3 months later    1 year later
[Define Benefits] → [Baseline] → [Track] → [Measure] → [Report ROI]
       ↑                                                      ↓
   Business Case                                      Lessons Learned
```

### Template Benefits Register

| Benefit | Metric | Baseline | Target | Measurement Method | Owner | Timeline |
|---|---|---|---|---|---|---|
| Giảm churn | Churn rate | 15% | 8% | CRM data | CSM team | Q4 |
| Tăng NPS | NPS score | 22 | 40 | NPS survey | Product | Q4 |
| Giảm support tickets | Ticket/user/month | 2.3 | 1.5 | Zendesk | Support | Q3 |

---

## Senior PM Presenting to Board

### Ngôn Ngữ Board vs Ngôn Ngữ PM

| PM nói | Board muốn nghe |
|---|---|
| "Dự án on track" | "Chúng ta sẽ đạt KR2 trong Q3" |
| "Scope thay đổi 3 lần" | "Chúng ta đã adjust để maximize value" |
| "Developer đang làm Feature X" | "Investment này sẽ giúp giảm churn 7%" |
| "Timeline bị delay 2 tuần" | "Business impact là [X], recovery plan là [Y]" |

### Structure Presentation cho Board (15 phút)

```
Slide 1: Context — Dự án này serve OKR nào? (2 phút)
Slide 2: Progress vs Plan — Traffic light + key metrics (3 phút)
Slide 3: Key Risks & Mitigation (2 phút)
Slide 4: Decisions Needed (từ Board) (5 phút)
Slide 5: Next Milestone & Timeline (2 phút)
Slide 6: Q&A (buffer)
```

---

## Strategic Alignment Checklist

Trước khi bắt đầu bất kỳ dự án nào ở level Senior PM:

- [ ] Tôi biết dự án này liên kết với OKR nào của công ty
- [ ] Tôi có thể giải thích tại sao dự án này quan trọng trong 30 giây
- [ ] Tôi biết ai là business owner chịu trách nhiệm về business outcome
- [ ] Tôi có Benefits Register với metrics và measurement plan
- [ ] Tôi sẽ track và report benefits sau go-live (không chỉ khi close project)
- [ ] Nếu OKR thay đổi, tôi sẽ re-evaluate project scope/priority

---

## Câu Hỏi Reflection

1. Dự án bạn đang làm hiện tại liên kết với OKR nào của công ty? Bạn có biết không?
2. Nếu công ty thay đổi strategy giữa chừng, dự án bạn đang làm có còn relevant không?
3. Làm thế nào để PM "nói chuyện business" với CFO thay vì "nói chuyện IT"?
