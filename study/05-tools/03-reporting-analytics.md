# Công Cụ Reporting & Analytics

---

## Excel / Google Sheets

**Best for:** Budget tracking, EVM, custom reports, all team sizes

**Free:** Google Sheets hoàn toàn miễn phí. Excel cần Microsoft 365.

### EVM Spreadsheet Template

Cấu trúc cơ bản để track EVM hàng tuần:

```
Sheet 1: EVM Dashboard
Columns: Week | PV | EV | AC | CV | SV | CPI | SPI | EAC | ETC | Status

Công thức (ví dụ Week 10):
PV  = BAC × (Planned % Complete)
EV  = BAC × (Actual % Complete)
AC  = Actual costs entered manually
CV  = EV - AC                    → Positive = under budget
SV  = EV - PV                    → Positive = ahead of schedule
CPI = EV / AC                    → >1 = good
SPI = EV / PV                    → >1 = good
EAC = BAC / CPI                  → Forecast total cost
ETC = EAC - AC                   → Remaining estimated cost
```

### Budget Tracker Template

```
Sheet 2: Budget Tracker
Columns:
- WBS ID
- Work Package
- Planned Cost
- Actual Cost
- Variance (Amount)
- Variance (%)
- Status (🟢/🟡/🔴)
- Notes

Footer rows:
- Total Planned
- Total Actual
- Overall Variance
- Budget Utilization %
```

### RAG Status Dashboard

```
Sheet 3: Project Dashboard
┌─────────────────────────────────────┐
│ PROJECT: [Name]    Date: [Date]      │
│ Overall Status: 🟡 AT RISK           │
├──────────┬──────────────────────────┤
│ Schedule │ 🟢 On Track              │
│ Budget   │ 🟡 +5% over              │
│ Scope    │ 🟢 Stable                │
│ Quality  │ 🟢 On Track              │
│ Team     │ 🔴 2 people at risk      │
└──────────┴──────────────────────────┘
Top Risks | Upcoming Milestones | Action Items
```

### Gantt Chart Cơ Bản trong Google Sheets

Dùng conditional formatting để tô màu ô:
- Columns: Tasks (rows) × Weeks (columns)
- Nếu week nằm trong [Start, End] → tô màu xanh
- Công thức: `=AND(C$1>=Start_Week, C$1<=End_Week)`

---

## Power BI

**Best for:** C-level dashboards, multi-project portfolios, executive reporting

| | Power BI Desktop | Power BI Pro |
|---|---|---|
| **Cost** | Free | $9.99/user/month |
| **Share reports** | ❌ | ✅ |
| **Refresh data** | Manual | Scheduled (8×/day) |
| **Collaborate** | ❌ | ✅ |

### Khi Nào Đầu Tư Power BI
- 5+ projects cần consolidated reporting
- C-level muốn self-service dashboard
- Data từ nhiều sources (Jira, Excel, SQL)
- Cần interactive drill-down

### Key PM Metrics để Visualize

```
1. Portfolio Health (Overall RAG)
   → Bar chart: % Green / Yellow / Red projects

2. Budget Performance
   → Scatter plot: Budget Variance vs Schedule Variance
   → Quadrants: Over budget+behind / Under budget+ahead / etc.

3. Risk Heatmap
   → Matrix: Probability × Impact, colored by score

4. Resource Utilization
   → Bar chart: % allocation per person per project

5. Milestone Tracker
   → Gantt-like timeline with RAG status per milestone
```

---

## Google Looker Studio (Data Studio)

**Best for:** Free alternative to Power BI, Google ecosystem

**Điểm mạnh:**
- Hoàn toàn **free**
- Kết nối trực tiếp Google Sheets, BigQuery, Google Analytics
- Share và embed dễ dàng
- Real-time data refresh

**Hạn chế vs Power BI:**
- Ít connector hơn (không connect Jira trực tiếp)
- Less powerful DAX-equivalent
- UI less polished

### Quick Setup: PM Dashboard với Looker Studio

1. Google Sheets → Looker Studio connector
2. Create scorecard widgets cho: Schedule %, Budget %, Risks open
3. Line chart cho EVM (PV, EV, AC theo tuần)
4. Table cho Action Items (filter by status)
5. Share link với stakeholders

---

## Executive Dashboard Design Principles

### 5 Metrics Quan Trọng Nhất cho C-Level

```
1. Overall Project Status (🟢/🟡/🔴) — một nhìn là biết
2. Schedule Performance (SPI hoặc % behind)
3. Budget Performance (% over/under)
4. Top 3 Risks (với mitigation status)
5. Next Milestone (ngày, owner, readiness)
```

### One-Page Dashboard Rule

C-level không có thời gian đọc báo cáo 10 trang. **Mọi thứ cần fit trong 1 trang A4 hoặc 1 slide.**

```
┌────────────────────────────────────────┐
│ PROJECT STATUS — [Tháng/Năm]           │
│ Overall: 🟡 AT RISK                     │
├──────┬──────┬────────────────┬─────────┤
│ SCH  │ COST │ SCOPE          │ TEAM    │
│ 🟡-2w│ 🟢   │ 🟢 Stable      │ 🔴 -1  │
├──────┴──────┴────────────────┴─────────┤
│ RISKS: [R1 description | mitigation]   │
│        [R2 description | mitigation]   │
├────────────────────────────────────────┤
│ NEXT MILESTONE: UAT Complete — 15/5    │
│ DECISIONS NEEDED: [Action, By when]    │
└────────────────────────────────────────┘
```

### Reporting Automation

Thay vì copy-paste số thủ công mỗi tuần:
- Google Sheets formula pulls từ Jira API (Apps Script)
- Slack bot gửi tự động status mỗi sáng thứ Hai
- Looker Studio refresh tự động

**Tip:** 80% thời gian viết status report là để compile data. Automate data collection = focus vào analysis và communication.
