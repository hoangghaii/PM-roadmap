# Công Cụ Communication & Collaboration

---

## Slack

**Best for:** Daily team communication, async-first teams

### Channel Structure cho Dự Án PM

```
#project-[name]-general      — Thông tin chung, announcements
#project-[name]-dev          — Technical discussions
#project-[name]-status       — Weekly status updates (PM posts)
#project-[name]-alerts       — Automated alerts từ Jira/CI-CD
#project-[name]-random       — Non-work, team bonding

#pm-team                     — All PMs internal discussions
#escalations                 — Issues cần attention nhanh
```

### Best Practices

**Notification Management:**
- Set Do Not Disturb giờ ngoài làm việc
- Dùng @here vs @channel có chọn lọc
- Mute channels không liên quan trực tiếp

**Thread Culture:**
- Luôn reply trong thread, không tạo message mới
- Giữ channels sạch, organized

**Status Updates:**
- PM post weekly status trong `#project-[name]-status`
- Format: 🟢/🟡/🔴 + 3 bullet points key updates

**Integrations hữu ích:**
- `/remind` — set reminders
- Jira app — get notifications khi issue thay đổi
- Google Calendar — meeting reminders
- GitHub — PR/commit notifications

---

## Microsoft Teams

**Best for:** Enterprise với Office 365, meeting-heavy culture

### Khi Nào Chọn Teams vs Slack

| | Slack | Microsoft Teams |
|---|---|---|
| **Tốt cho** | Async communication, startup, tech-first | Enterprise, Office 365 users |
| **Integration** | 2000+ apps | Office 365 ecosystem (SharePoint, Planner, Power BI) |
| **Meetings** | Zoom integration | Built-in video (tốt, competitive với Zoom) |
| **File storage** | Cloud links | SharePoint integration |
| **Cost** | Free tier (limited); $7.25/month | Thường đã có trong Microsoft 365 license |

### Teams Structure cho PM
```
Team: [Project Name]
├── Channel: General — Thông tin chung
├── Channel: Planning — Project docs, plans
├── Channel: Development — Tech discussions
├── Channel: Stakeholders — Updates cho sponsor/client
└── Channel: Issues — Blockers, escalations
```

### Tabs trong Channel
Mỗi channel có thể pin tabs:
- SharePoint document folder
- Planner (Kanban board)
- OneNote (meeting notes)
- Power BI dashboard

---

## Zoom / Google Meet

**Best for:** Video meetings, remote standup, client demos

### Meeting Best Practices

**Trước Meeting:**
- Gửi agenda ít nhất 24h trước
- Include dial-in info và materials link
- Set expected duration và objectives

**Trong Meeting:**
- Video on — builds trust, reduces multitasking
- Host mute participants khi cần
- Use Zoom breakout rooms cho group discussions
- Screen share document khi review

**Sau Meeting:**
- Send minutes trong 24h
- Action items với owner và deadline
- Recording link (nếu consent)

### Remote Standup Format (15 phút)
```
1. Mỗi người: Hôm qua làm gì? Hôm nay làm gì? Blockers?
   → Max 2 phút/người
2. PM: Updates từ stakeholders, priority changes
   → 3 phút
3. Parking lot items → schedule follow-up
   → 2 phút

Rule: "Take it offline" nếu topic cần >2 phút discuss
```

---

## Confluence (Atlassian)

**Best for:** Project documentation, knowledge base, team wiki

### Page Structure cho Dự Án

```
Space: [Project Name]
├── Home (overview, links đến key docs)
├── 📋 Project Management
│   ├── Project Charter
│   ├── Stakeholder Register
│   ├── Risk Register
│   └── Status Reports (archive theo tuần)
├── 📐 Architecture & Design
│   ├── System Architecture
│   ├── API Contracts
│   └── Technical Decisions (ADRs)
├── 📝 Meeting Notes
│   └── [YYYYMMDD] Meeting Name
├── 🧪 Testing
│   ├── Test Plan
│   └── UAT Sign-off
└── 📚 Lessons Learned
```

### Tips Confluence Hiệu Quả
- Dùng **Page Templates** cho consistency (Meeting Notes, Status Reports)
- **Labels** để search dễ hơn
- **@mention** trong page để notify người cần đọc
- **Macros:** Status indicator, Table of Contents, Expand sections
- Link Confluence pages với Jira issues

**Jira + Confluence combo:** Jira cho tasks/tracking, Confluence cho documentation — đây là "dream stack" cho software teams.

---

## Miro / FigJam

**Best for:** Remote brainstorming, visual planning, retrospectives

### PM Templates Hữu Ích trong Miro

| Template | Dùng khi nào |
|---|---|
| **Retrospective** (Start/Stop/Continue, 4Ls) | End of sprint hoặc project |
| **Risk Matrix** | Risk identification workshop |
| **Stakeholder Map** | Stakeholder analysis session |
| **WBS Mind Map** | WBS brainstorming với team |
| **User Journey Map** | Khi làm requirement gathering |
| **Impact/Effort Matrix** | Prioritization session |
| **Timeline** | Planning visual timeline |

### Tips Facilitation Online với Miro
- Assign màu sticky note cho từng người
- Use Timer (built-in) cho timeboxed activities
- Voting feature để prioritize ideas
- Export board thành image/PDF cho documentation

---

## Communication Charter Template

Tạo communication charter ngay từ đầu dự án:

```markdown
# Communication Charter — [Tên Dự Án]

## Channels và Mục Đích
| Channel | Mục đích | Audience | Tần suất |
|---|---|---|---|
| Slack #project-name-status | Quick updates | Team | Daily |
| Email | Formal communication | Stakeholders | As needed |
| Jira | Task updates, comments | Dev team | Real-time |
| Weekly Meeting | Status review | PM + Leads | Weekly |
| Monthly Report | Executive summary | Sponsor | Monthly |

## Meeting Norms
- Có agenda trước 24h
- Start và end đúng giờ
- Video on cho meetings <10 người
- Minutes trong 24h
- Action items có owner và deadline

## Escalation Path
Level 1: Team member → PM (Slack, <4h)
Level 2: PM → Sponsor (Email + Meeting, <24h)
Level 3: Sponsor → Board (as needed)

## Response Time SLA
- Slack: 4 giờ trong giờ làm việc
- Email: 24 giờ
- Emergency: Phone call
```

---

## Async vs Sync: Khi Nào Dùng Gì

| Situation | Async (Slack/Email) | Sync (Meeting) |
|---|---|---|
| Status update routine | ✅ | ❌ |
| Simple question có answer rõ | ✅ | ❌ |
| Complex discussion, nhiều opinions | ❌ | ✅ |
| Decision cần input nhiều người | ❌ | ✅ |
| Conflict resolution | ❌ | ✅ |
| Brainstorming | ❌ | ✅ |
| FYI announcement | ✅ | ❌ |

**Anti-pattern:** Tổ chức meeting cho mọi thứ → Meeting fatigue → People stop attending → Team communication breakdown.
