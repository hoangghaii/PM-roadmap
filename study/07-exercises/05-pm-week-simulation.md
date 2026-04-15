# Bài Tập 5: Simulation — 1 Tuần Làm PM

**Mục tiêu:** Trải nghiệm daily rituals của PM trong 1 tuần thực tế
**Thời gian:** 15-30 phút/ngày × 5 ngày
**Cấp độ:** Giai đoạn 0-1

---

## Tổng Quan

Trong 5 ngày, bạn sẽ nhìn dự án đang tham gia (dù là developer) qua **lens của PM**. Mỗi ngày thực hành 1 ritual quan trọng.

**Điều kiện:** Bạn cần có 1 dự án đang tham gia để làm bài tập này. Nếu không, dùng một trong các scenarios giả định trong bài tập khác.

---

## Ngày 1: Weekly Status Report

**Objective:** Tổng hợp tình trạng dự án trong 1 tuần nhìn từ góc độ PM.

**Bước thực hiện:**
1. Thu thập thông tin (15 phút): hỏi developer, check Jira, review commits
2. Đánh giá RAG status cho: Schedule, Budget, Scope, Quality, Team
3. Điền template dưới đây
4. Reflection: Bạn thấy gì mà trước đây không để ý?

**Template:**

```
PROJECT STATUS REPORT
Project: [Tên] | Week: [W__] | Date: [DD/MM/YYYY]
PM (simulated): [Tên bạn]

OVERALL: 🟢/🟡/🔴 [Lý do ngắn]

| Dimension  | Status | Comment                    |
|------------|--------|----------------------------|
| Schedule   | 🟢/🟡/🔴 |                          |
| Budget     | 🟢/🟡/🔴 |                          |
| Scope      | 🟢/🟡/🔴 |                          |
| Team       | 🟢/🟡/🔴 |                          |

HIGHLIGHTS THIS WEEK:
•
•

UPCOMING NEXT WEEK:
•
•

BLOCKERS:
| Issue | Impact | Action | Owner |
|-------|--------|--------|-------|
|       |        |        |       |

REFLECTION:
- Điều tôi thấy mà developer thường không để ý:
- Thông tin nào khó thu thập nhất và tại sao:
```

---

## Ngày 2: Risk Identification

**Objective:** Identify và assess 3 risks trong tuần tới.

**Bước thực hiện:**
1. Nhìn công việc tuần tới (Jira backlog, upcoming meetings, dependencies)
2. Hỏi: "Điều gì có thể không đúng kế hoạch?"
3. Assess mỗi risk: Probability (1-5) × Impact (1-5) = Score
4. Plan 1 action để mitigate mỗi risk HIGH/MEDIUM

**Template:**

```
WEEKLY RISK IDENTIFICATION
Project: [Tên] | Date: [DD/MM/YYYY]

| ID | Risk Description | Probability | Impact | Score | Action | Owner |
|----|-----------------|-------------|--------|-------|--------|-------|
| W1 |                 |             |        |       |        |       |
| W2 |                 |             |        |       |        |       |
| W3 |                 |             |        |       |        |       |

Risks tôi thường bỏ sót khi là developer (nhìn lại):
•
•
```

---

## Ngày 3: Meeting Facilitation

**Objective:** Prepare agenda + facilitate 1 meeting + write minutes.

**Bước thực hiện:**
1. Chọn 1 meeting sẽ xảy ra trong tuần (standup, sprint planning, review...)
2. Viết agenda chi tiết **trước** meeting
3. Trong meeting: observe hoặc co-facilitate
4. Sau meeting: viết minutes trong 1 giờ

**Agenda Template:**

```
MEETING AGENDA
Meeting: [Tên] | Date: [Date] | Time: [Time] | Duration: [X min]
Facilitator: [Tên] | Note-taker: [Tên]
Goal: [Mục đích của meeting — 1 câu]

AGENDA:
1. [Topic 1] — [X min] — Facilitator: [Tên]
   Goal: [Decision? Update? Brainstorm?]
2. [Topic 2] — [X min]
3. Action items review — [5 min]
4. Next steps — [5 min]

Pre-read (nếu có): [Link]
```

**Minutes Template (điền trong 1 giờ sau meeting):**

```
MEETING MINUTES
Meeting: [Tên] | Date: | Attendees: [X people]

KEY DECISIONS:
• [Decision 1]

ACTION ITEMS:
| Action | Owner | Due |
|--------|-------|-----|
|        |       |     |

NEXT MEETING: [Date]
```

**Reflection:**
- Meeting có productive không? Tại sao?
- Bao nhiêu % thời gian là value-add?
- Nếu bạn facilitated, bạn làm tốt điều gì? Cần cải thiện gì?

---

## Ngày 4: Retrospective

**Objective:** Facilitate retrospective 15 phút với team (hoặc tự mình nếu không có team).

**Format: Start / Stop / Continue**

```
START: Điều gì chúng ta nên bắt đầu làm?
STOP:  Điều gì chúng ta nên dừng làm (không hiệu quả)?
CONTINUE: Điều gì đang hoạt động tốt, cần giữ?
```

**Facilitation Guide (15 phút):**
```
Phút 1-2:   Explain format, rules (no blame, focus on process)
Phút 3-8:   Silent brainstorm — mỗi người viết sticky notes
Phút 9-12:  Group và discuss (dot voting nếu cần)
Phút 13-15: Chọn 1-2 action items, assign owner
```

**Output Template:**

```
RETROSPECTIVE — [Sprint/Week] — [Date]

START (nên bắt đầu làm):
•
•

STOP (nên dừng làm):
•
•

CONTINUE (đang tốt, giữ lại):
•
•

ACTION ITEMS:
| Action | Owner | Due |
|--------|-------|-----|
|        |       |     |
```

---

## Ngày 5: Lessons Learned

**Objective:** Document 1 việc không suôn sẻ trong tuần với full analysis.

**Format: Situation → Root Cause → Impact → Actions Taken → Lesson → Recommendation**

**Template:**

```
LESSONS LEARNED
Project: [Tên] | Date: [Date] | Author: [Tên]
Category: [Technical / Process / Communication / People]

SITUATION (What happened?):
[Mô tả khách quan, không blame]

ROOT CAUSE (Why did it happen?):
[Dùng "5 Whys" nếu cần]
Why 1: ...
Why 2: ...
Why 3: ...

IMPACT:
• Time impact: [X hours/days lost]
• Cost impact: [N/A or estimate]
• Quality impact: [Description]

ACTIONS TAKEN:
• [Hành động đã làm để xử lý]

LESSON LEARNED:
[1-2 câu tóm tắt bài học]

RECOMMENDATION (cho dự án tiếp theo):
• [Recommendation 1]
• [Recommendation 2]
```

**Ví dụ điền sẵn:**

```
SITUATION: API integration với payment gateway bị fail ngay ngày demo
vì dev team dùng sandbox credentials trong production config.

ROOT CAUSE:
Why 1: Credentials sai → Why 2: Không có checklist deployment
Why 3: Chưa có deployment runbook → Why 4: Không ai assigned task đó
Why 5: Không có "Definition of Done" cho deployment

IMPACT: Demo delay 45 phút, khách hàng disappointed.

ACTIONS TAKEN: Hot-fix credentials, re-demo trong 1 giờ.

LESSON LEARNED: Deployment runbook và credential verification 
phải là part of Definition of Done, không phải optional.

RECOMMENDATION:
• Tạo deployment checklist cho mọi dự án
• Environment configs phải được reviewed bởi 2 người trước deploy
```

---

## End-of-Week Reflection

Sau 5 ngày, dành 20 phút để trả lời:

1. **Điều bất ngờ nhất** khi nhìn dự án từ góc độ PM là gì?
2. **Thông tin nào khó thu thập nhất** và tại sao? (Điều này nói lên vấn đề gì trong team/process?)
3. **Kỹ năng PM nào** bạn thấy mình cần phát triển nhất?
4. **1 thay đổi cụ thể** bạn có thể làm ngay để cải thiện cách dự án đang vận hành?
5. Sau tuần này, bạn có **muốn trở thành PM chính thức** hơn hay ít hơn? Tại sao?

---

## Tips Tối Đa Hóa Learning

- **Đừng làm riêng lẻ:** Nếu có thể, share outputs với PM trong team bạn và xin feedback
- **Document mọi thứ:** Lưu 5 ngày outputs vào PM Portfolio
- **Tự nhận xét khách quan:** Mục tiêu là học, không phải làm đẹp cho CV
- **Lặp lại mỗi tháng:** Sau 3 lần, bạn sẽ thấy rõ sự tiến bộ
