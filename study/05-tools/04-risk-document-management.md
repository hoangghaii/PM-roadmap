# Công Cụ Risk & Document Management

---

## SharePoint

**Best for:** Enterprise document management, Microsoft ecosystem

### Project Folder Structure Gợi Ý

```
📁 Sites > Projects > [Project Name]
├── 📁 01-Initiation
│   ├── Project Charter v1.0.docx
│   ├── Stakeholder Register.xlsx
│   └── Business Case.docx
├── 📁 02-Planning
│   ├── Project Plan.mpp / .xlsx
│   ├── Risk Register.xlsx
│   ├── Communication Plan.docx
│   └── WBS.xlsx
├── 📁 03-Execution
│   ├── Meeting Minutes
│   │   ├── 20260101 Kickoff Meeting.docx
│   │   └── 20260108 Status Meeting.docx
│   ├── Status Reports
│   │   ├── W01 Status Report.docx
│   │   └── W02 Status Report.docx
│   └── Change Requests
│       ├── CR-001 Add Feature X.docx
│       └── CR-002 Extend Timeline.docx
├── 📁 04-Monitoring & Control
│   ├── Issue Log.xlsx
│   └── Progress Reports
└── 📁 05-Closing
    ├── Lessons Learned.docx
    ├── Project Closure Report.docx
    └── Archive (zip của toàn bộ project)
```

### Permission Management

| Nhóm | Permission |
|---|---|
| PM | Full control |
| Project Team | Contribute (read + write) |
| Stakeholders | Read (specific folders) |
| PMO | Read all |
| External (client) | Read (selected documents only) |

---

## Google Drive

**Best for:** Simple teams, Google Workspace users, collaboration-first

### Structure Gợi Ý

```
📁 Shared Drive: Projects
└── 📁 [Project Name]
    ├── 📁 0_Admin (Charter, Stakeholders, Meeting Notes)
    ├── 📁 1_Planning (Project Plan, Risk Register, WBS)
    ├── 📁 2_Execution (Weekly Reports, Change Requests)
    ├── 📁 3_Deliverables (Milestones, Handover docs)
    └── 📁 4_Archive (Closed items, Old versions)
```

### Google Drive Tips

- Dùng **Shared Drives** (không phải My Drive) cho project files — files không bị mất khi người tạo rời team
- **Google Docs Comments** cho review và feedback
- **Version History** (Ctrl+Alt+Shift+H) — không cần đặt tên v1, v2, v3
- **Suggesting mode** khi review documents của người khác

---

## Document Management Best Practices

### File Naming Convention

**Format:** `YYYYMMDD_ProjectCode_DocumentType_Version`

```
✅ Good:
20260115_WMS_ProjectCharter_v1.0.docx
20260201_WMS_RiskRegister_v2.3.xlsx
20260210_WMS_StatusReport_W06.docx

❌ Bad:
project charter.docx
risk register FINAL.xlsx
status report NEW (2).docx
status report NEW UPDATED FINAL FINAL.docx
```

### Version Control Convention

```
v0.1 — Initial draft (internal review)
v0.2 — Updated after internal feedback
v1.0 — First official release (sent to client/sponsor)
v1.1 — Minor updates (typos, small clarifications)
v2.0 — Major revision (significant scope/content change)
```

### Document Lifecycle

```
Draft → Internal Review → Revision → Approved → Active → Archived
  ↑_____________________|
  (iterate until approved)
```

**Approval rules:**
- Project Charter: cần chữ ký sponsor
- Risk Register: cần PM review + Sponsor aware
- Change Request: cần sponsor signature
- Meeting Minutes: gửi trong 24h, không yêu cầu formal sign-off (email response = accepted)

---

## Risk Management Tools

### Excel Risk Register (Recommended cho most projects)

Đây là tool đơn giản nhất nhưng đủ dùng cho 90% dự án:

**Columns cần có:**
```
ID | Description | Category | Probability | Impact | Score | Level | 
Strategy | Response Actions | Owner | Target Date | Status | Last Reviewed
```

**Conditional Formatting cho Score:**
- Score 1-7: Green background (Low)
- Score 8-14: Yellow background (Medium)
- Score 15-25: Red background (High)

### ADO / Jira Risk Tracking

Với team đang dùng Jira:
- Tạo Issue Type = "Risk"
- Custom fields: Probability, Impact, Score, Mitigation
- Label: risk-open, risk-accepted, risk-closed
- Dashboard widget: Open risks by severity

---

## Lessons Learned Database

**Mục đích:** Đảm bảo mistakes từ dự án này không lặp lại ở dự án tiếp theo.

### Structure của Lessons Learned Document

```markdown
# Lessons Learned — [Tên Dự Án]
**Date Captured:** | **PM:** | **Project Duration:**

## What Went Well ✅
| Lesson | Context | Recommendation |
|---|---|---|
| Daily standup giúp detect blockers sớm | Phát hiện API issue ở W3, fix trước khi impact schedule | Dùng daily standup cho mọi dự án >2 tháng |

## What Could Be Improved ⚠️
| Issue | Root Cause | Recommendation |
|---|---|---|
| Requirement change không qua CR process | Khách hàng contact dev trực tiếp | Setup communication protocol ngay từ kickoff |

## Key Recommendations cho Dự Án Tiếp Theo
1. [Recommendation 1]
2. [Recommendation 2]
```

### PMO Lessons Learned Repository

Nếu có PMO, tập trung lessons learned vào 1 nơi:
- Confluence space: "PMO Lessons Learned"
- Tags: project-type, team-size, methodology, issue-category
- Quarterly "knowledge sharing" session để review và apply

**Rule:** Lessons Learned không có giá trị nếu không được đọc và applied. PMO phải actively reference chúng khi plan dự án mới.
