# Công Cụ Project Planning & Tracking

---

## Jira (Atlassian)

**Best for:** Agile software teams, dev-centric projects

| | Chi tiết |
|---|---|
| **Pricing** | Free ≤10 users; $7.75/user/month (Standard); $15.25 (Premium) |
| **Methodology** | Agile (Scrum + Kanban), có thể dùng cho Waterfall |
| **Learning curve** | Trung bình (3-7 ngày để quen) |

### Cấu trúc Jira
```
Portfolio → Program → Project → Epic → Story → Task → Sub-task
```

### Key Features
- **Scrum board:** Sprint planning, Sprint backlog, Burndown chart
- **Kanban board:** WIP limits, Cumulative flow diagram
- **Backlog:** Prioritize, estimate (story points hoặc hours)
- **Roadmap:** Timeline view cho Epics
- **Dashboards:** Custom widgets (Burndown, Velocity, Open Issues)
- **Automation:** Rules tự động (e.g., khi Story done → notify PM)

### Setup Dự Án Mới trong Jira (6 Bước)
1. Create Project → chọn Scrum hoặc Kanban template
2. Setup Board columns (To Do / In Progress / In Review / Done)
3. Create Epics (feature groups lớn)
4. Invite team members và assign roles
5. Configure Sprints (2 tuần recommended)
6. Create Issues (Stories/Tasks) và estimate

### Tips Sử Dụng Hiệu Quả
- Dùng **Labels** để phân loại issues (bug, enhancement, tech-debt)
- Setup **Automations** để giảm manual work
- **Velocity chart** để estimate future sprints
- **Component** để track theo module/team

**Khi nào chọn Jira:** Dev team, Agile project, cần deep integration với Git/CI-CD

---

## Microsoft Project

**Best for:** Enterprise Waterfall, resource management, Gantt-heavy clients

| | Chi tiết |
|---|---|
| **Pricing** | Project Plan 1: $10/user/month; Plan 3: $30; Plan 5: $55 |
| **Methodology** | Waterfall (primary), có Agile view |
| **Learning curve** | Cao (1-2 tuần để proficient) |

### Key Features
- **Gantt chart:** Industry standard, highly detailed
- **Resource management:** Resource leveling, allocation %, cost tracking
- **Critical Path:** Automatic critical path calculation
- **EVM:** Built-in Earned Value tracking
- **Baseline:** Save baseline và compare với actuals

### Khi Nào Dùng MS Project
- Khách hàng/sponsor yêu cầu Gantt chart format
- Dự án construction, infrastructure, compliance-heavy
- Cần resource leveling phức tạp (nhiều người, nhiều dự án)
- Government hoặc enterprise contracts

**Nhược điểm:** Đắt, khó share với team, không real-time collaboration tốt.

---

## Asana

**Best for:** Marketing, operations, non-dev teams

| | Chi tiết |
|---|---|
| **Pricing** | Free ≤15 users (Basic); Premium $10.99/user/month; Business $24.99 |
| **Methodology** | Flexible (Kanban, List, Timeline, Calendar) |
| **Learning curve** | Thấp (1-2 ngày) |

### Điểm Mạnh
- Multiple views: Board, List, Timeline (Gantt-like), Calendar, Workload
- **Goals** feature: Link tasks vào company OKRs
- **Workload view:** Xem ai đang bị overload
- Template library phong phú

**Khi nào chọn Asana vs Jira:**
- Asana: Non-tech team, marketing campaigns, operations, easier UX
- Jira: Dev team, Agile sprints, cần deep software-specific features

---

## Monday.com

**Best for:** Visual management, agencies, business teams

| | Chi tiết |
|---|---|
| **Pricing** | Free ≤2 seats; Basic $9/seat; Standard $12; Pro $19 |
| **Methodology** | Flexible |
| **Learning curve** | Thấp |

### Điểm Mạnh
- Highly visual, colorful boards
- Multiple views: Board, Gantt, Calendar, Form, Map, Workload
- Strong automation (trigger-based)
- Good for client-facing projects

---

## Notion

**Best for:** Documentation-heavy PM, early-stage startups, learning PM

| | Chi tiết |
|---|---|
| **Pricing** | Free (personal); $8/user/month (Team) |
| **Methodology** | Flexible |
| **Learning curve** | Trung bình |

### PM Workspace Template

```
📁 My PM Workspace
├── 📋 Projects Database
│   ├── Properties: Name, Status, PM, Deadline, Budget, Phase
│   └── Views: Kanban (by status), Table, Calendar (by deadline)
├── 📝 Meeting Notes (linked to Projects)
├── 🗂️ Templates
│   ├── Project Charter
│   ├── Risk Register
│   ├── Status Report
│   └── Meeting Minutes
├── 📚 Study Notes
└── 🏆 Portfolio
```

**Khi nào chọn Notion:** Small team, documentation culture, học PM, early-stage startup

---

## ClickUp

**Best for:** All-in-one solution, replace multiple tools

| | Chi tiết |
|---|---|
| **Pricing** | Free; Unlimited $5/user/month; Business $12 |
| **Methodology** | Agile, Waterfall, Hybrid |
| **Learning curve** | Cao (nhiều features) |

### Điểm Nổi Bật
- Docs, Sprints, Goals, Workload, Time tracking — tất cả trong 1 tool
- Highly customizable (có thể tạo custom views)

---

## Trello

**Best for:** Simple Kanban, personal projects, small teams

| | Chi tiết |
|---|---|
| **Pricing** | Free (unlimited cards, limited features); Standard $5/user/month |
| **Methodology** | Kanban |
| **Learning curve** | Rất thấp (< 1 ngày) |

**Khi nào dùng:** Dự án nhỏ, cá nhân, team <5 người, workflow đơn giản

---

## Bảng So Sánh Tổng Hợp

| Tool | Best For | Agile | Gantt | Free? | $/user/mo | Complexity |
|---|---|---|---|---|---|---|
| Jira | Dev teams | ⭐⭐⭐⭐⭐ | ⭐⭐ | ≤10 users | $7.75 | Medium |
| MS Project | Enterprise Waterfall | ⭐⭐ | ⭐⭐⭐⭐⭐ | ❌ | $10+ | High |
| Asana | Non-tech teams | ⭐⭐⭐ | ⭐⭐⭐⭐ | ≤15 users | $10.99 | Low |
| Monday | Visual/Agency | ⭐⭐⭐ | ⭐⭐⭐ | ≤2 seats | $9 | Low |
| Notion | Docs + light PM | ⭐⭐ | ❌ | Yes | $8 | Medium |
| ClickUp | All-in-one | ⭐⭐⭐⭐ | ⭐⭐⭐ | Yes | $5 | High |
| Trello | Simple Kanban | ⭐⭐⭐ | ❌ | Yes | $5 | Very Low |
