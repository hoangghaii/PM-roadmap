# Công Cụ PM — Tổng Quan

## Nguyên Tắc Chọn Công Cụ

> "A fool with a tool is still a fool."

Công cụ phục vụ quy trình, không phải ngược lại. Trước khi chọn tool, hãy hỏi:

1. **Team cần làm gì?** (Track tasks? Communicate? Report?)
2. **Team size bao nhiêu?** (<10, 10-50, 50+?)
3. **Methodology là gì?** (Agile, Waterfall, Hybrid?)
4. **Budget?** (Free, $10/user, enterprise?)
5. **Technical savviness?** (Dev-heavy hay business-heavy?)

---

## 4 Nhóm Công Cụ Chính

| Nhóm | Mục đích | File chi tiết |
|---|---|---|
| **Project Planning & Tracking** | Manage tasks, sprint, timeline, backlog | [01-project-planning-tools.md](01-project-planning-tools.md) |
| **Communication & Collaboration** | Team chat, meetings, documentation | [02-communication-collaboration.md](02-communication-collaboration.md) |
| **Reporting & Analytics** | Budget tracking, dashboards, EVM | [03-reporting-analytics.md](03-reporting-analytics.md) |
| **Document & Risk Management** | File storage, version control, risk tracking | [04-risk-document-management.md](04-risk-document-management.md) |

---

## Tool Stack Gợi Ý Theo Tình Huống

### Startup / Small Team (<10 người)
```
Planning:      Trello hoặc Notion
Communication: Slack + Google Meet
Documentation: Notion
Reporting:     Google Sheets
Storage:       Google Drive
```

### Agile Software Team (10-50 người)
```
Planning:      Jira
Communication: Slack + Zoom
Documentation: Confluence
Reporting:     Jira Dashboards + Google Sheets
Storage:       Confluence + Google Drive
```

### Enterprise / Traditional PM (50+ người)
```
Planning:      MS Project hoặc Jira Portfolio
Communication: Microsoft Teams
Documentation: SharePoint + Confluence
Reporting:     Power BI
Storage:       SharePoint
```

---

## Bài Tập: Setup PM Workspace

Tạo workspace trên **Notion** (free) với cấu trúc sau để practice:

```
📁 My PM Workspace
├── 📋 Projects (Kanban board: Not Started / In Progress / Done)
│   └── Mỗi project card: Name, Status, PM, Deadline, Progress %
├── 📚 Study Notes
│   ├── 00-Foundation
│   ├── 01-Junior PM
│   └── ...
├── 🏆 Portfolio (case studies từ kinh nghiệm thực tế)
├── 📖 Book Notes (template: Key takeaways, Quotes, Actions)
└── 🗂️ Templates
    ├── Project Charter
    ├── Risk Register
    ├── Meeting Minutes
    └── Status Report
```

**Tại sao Notion?** Free, flexible, kết hợp được docs + database + kanban trong 1 tool. Phù hợp để học PM mà không cần trả tiền tool phức tạp.

---

## Quick Reference: Chọn Tool Theo Câu Hỏi

| Câu hỏi | Tool |
|---|---|
| "Team cần Scrum board?" | Jira |
| "Cần Gantt chart cho client?" | MS Project hoặc Asana Timeline |
| "Team nhỏ, budget thấp, đơn giản?" | Trello hoặc Notion |
| "Cần document wiki?" | Confluence hoặc Notion |
| "Cần dashboard cho C-level?" | Power BI hoặc Google Looker Studio |
| "Team remote, cần whiteboard?" | Miro hoặc FigJam |
| "Cần track budget và EVM?" | Excel/Google Sheets |
