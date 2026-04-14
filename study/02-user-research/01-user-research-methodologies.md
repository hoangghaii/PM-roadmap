# User Research Methodologies

## Tại Sao User Research Quan Trọng?

> "You are not the user." — Urs Hölzle

Assumption là kẻ thù số 1 của PM. Hầu hết sản phẩm fail không phải vì engineering kém — mà vì build sai thứ. User research giúp bạn **build the right thing**.

---

## Qualitative vs Quantitative Research

| | Qualitative | Quantitative |
|--|--|--|
| **Trả lời câu hỏi** | Why & How | What & How many |
| **Phương pháp** | Interviews, observations | Analytics, surveys, A/B tests |
| **Sample size** | 5-20 users | Hàng trăm đến hàng triệu |
| **Output** | Insights, themes | Numbers, percentages |
| **Khi nào dùng** | Discovery, understand behavior | Validation, measure impact |

**Quan trọng:** Dùng cả hai. Qualitative giải thích "why" đằng sau numbers.

---

## 1. User Interviews

**Tốt nhất cho:** Discovery phase, understanding behaviors and motivations

**Khi nào dùng:**
- Bắt đầu làm sản phẩm mới (validate problem)
- Feature không perform như expected (tìm why)
- User onboarding kém (find friction points)

**Cách conduct:**
1. Xác định câu hỏi cần trả lời (không phải feature muốn validate)
2. Recruit đúng users (không phải friends/family)
3. Open-ended questions, không leading
4. Listen 80%, nói 20%
5. Synthesize sau mỗi interview

**Rule of thumb:** 5 interviews thường đủ để tìm patterns chính (Nielsen Norman Group research)

---

## 2. Surveys

**Tốt nhất cho:** Quantify qualitative findings, large-scale preference data

**Khi nào dùng:**
- Sau interview để validate findings ở quy mô lớn
- NPS, CSAT measurement
- Feature prioritization với users

**Best practices:**
- Keep < 10 câu hỏi
- Single-choice cho quantitative, open-ended cho qualitative
- Test survey với 3 người trước khi send
- Incentivize participation (GrabFood voucher, gift card)
- Tránh: "Rate this feature 1-5" — thay bằng "How often do you use this?"

**Tools:** Google Forms (free), Typeform (đẹp hơn), SurveyMonkey

---

## 3. Usability Testing

**Tốt nhất cho:** Validate design, find UX problems

**5 loại:**
1. **Moderated in-person:** Bạn ngồi cạnh user, observe, probe
2. **Moderated remote:** Video call, user share screen
3. **Unmoderated:** User làm task tự mình, recorded
4. **Guerrilla:** Nhanh, informal — ra cafe, hỏi người lạ
5. **A/B testing:** Quantitative usability test

**Process:**
1. Define tasks (không phải "Hãy mua sản phẩm" — đó là outcome, không phải task)
2. Recruit 5 users (5 thường đủ để find major issues)
3. Observe, ghi chép, đừng giúp khi user confused
4. Note: "Ở đây user do hesitant vì X"
5. Sau test: Thảo luận với designer

---

## 4. Contextual Inquiry (Shadowing)

**Tốt nhất cho:** Understand real workflow trong môi trường thực

**Concept:** Đến chỗ user làm việc, quan sát họ làm việc thực sự.

**Ví dụ - Logistics:**
> PM đến kho hàng, quan sát nhân viên dùng app nhập orders trong 3 giờ. Phát hiện: Họ print order ra giấy để check off — app không show đủ thông tin trên 1 màn hình → missing critical workflow insight!

**Khó:** Tốn thời gian, khó scale. Nhưng insights rất deep.

---

## 5. Khi Nào Dùng Phương Pháp Nào

```
DISCOVERY PHASE (Problem unknown)
         ↓
    User Interviews
    Contextual Inquiry
         ↓
DEFINE PHASE (Problem understood, solution unclear)
         ↓
    User Interviews (validate problem statement)
    Surveys (quantify pain point severity)
         ↓
DESIGN PHASE (Solution hypothesis)
         ↓
    Usability Testing (early prototype)
    User Interviews (feedback on concept)
         ↓
DEVELOP PHASE (Build)
         ↓
    Usability Testing (working prototype)
         ↓
LAUNCH PHASE
         ↓
    Surveys (NPS, CSAT)
    Analytics (Quantitative)
    A/B Testing
```

---

## Synthesizing Research

Sau khi collect data, cần synthesize để tìm patterns:

### Affinity Mapping
1. Viết mỗi insight/quote lên sticky note (Miro, FigJam, hoặc giấy thật)
2. Group similar notes lại với nhau
3. Label mỗi nhóm
4. Identify top themes

### Insight vs Observation
- **Observation:** "User click vào back button 3 lần trong checkout flow"
- **Insight:** "Users confused về số bước trong checkout — họ không biết mình đang ở đâu trong process"

**Luôn đi từ observation → insight → implication**

---

## Ví Dụ Thực Tế: Research cho App Giao Nhận

**Vấn đề muốn tìm hiểu:** Tại sao merchants có retention thấp sau 3 tháng?

**Phương pháp chọn:** User interviews với 8 merchants đã churn + 5 merchants active

**Findings sau synthesis:**
- Theme 1 (5/8 churned): "Tôi không biết đơn hàng nào bị chậm trễ cho đến khi khách gọi than phiền"
- Theme 2 (6/8 churned): "Reporting quá phức tạp, tôi không hiểu revenue của mình"
- Theme 3 (4/8 churned): "Driver thường cancel orders — tôi không có control"

**Insights:**
1. Merchants cần proactive alerts, không phải reactive reports
2. Dashboard cần simplification — less data, more actionable insights
3. Driver reliability là pain point #1 cho retention

**Product implications:**
1. Build proactive delay notification system
2. Redesign merchant dashboard với "top 3 insights of the week"
3. Merchant SLA guarantee program với compensation
