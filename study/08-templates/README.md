# Thư Viện Templates PM

## Cách Sử Dụng

Templates là công cụ, không phải mục tiêu. Adapt chúng theo context dự án của bạn — một template 20% phù hợp với context còn tốt hơn template 100% đẹp nhưng không ai dùng.

**Ba nguyên tắc dùng template hiệu quả:**

1. **Bắt đầu từ "tại sao"** — Trước khi điền template, hỏi: stakeholder cần biết gì? Quyết định nào sẽ được đưa ra dựa trên document này?
2. **Lược bỏ những gì không cần** — Nếu dự án nhỏ 3 người, bỏ những section phức tạp không cần thiết. Template là khung, không phải xiềng xích.
3. **Version control mọi thứ** — Mỗi lần update document, ghi rõ ngày, version, và thay đổi gì. Tránh document "sống" không ai biết cái nào là mới nhất.

---

## Danh Sách Templates

### Khởi Động Dự Án (Project Initiation)

| Template | File | Dùng Khi Nào | Thời Gian Tạo |
|---|---|---|---|
| Project Charter | `project-charter-template.md` | Trước khi dự án chính thức bắt đầu, cần được sponsor approve | 2-4 giờ |
| Project Kickoff Checklist | `project-kickoff-checklist.md` | 1-2 tuần trước và ngay sau kickoff meeting | 30 phút setup |
| RACI Matrix | `raci-matrix-template.md` | Ngay sau khi team được hình thành, trước kickoff | 1-2 giờ |
| WBS (Work Breakdown Structure) | `wbs-template.md` | Sau khi scope đã được approve, trước khi lên schedule | 2-4 giờ |

### Quản Lý Rủi Ro & Thay Đổi (Risk & Change)

| Template | File | Dùng Khi Nào | Tần Suất Cập Nhật |
|---|---|---|---|
| Risk Register | `risk-register-template.md` | Ngay sau kickoff, cập nhật liên tục trong dự án | Mỗi tuần hoặc khi có risk mới |
| Change Request Form | `change-request-template.md` | Mỗi khi có yêu cầu thay đổi scope/timeline/budget | Theo sự kiện (event-driven) |

### Báo Cáo & Giao Tiếp (Reporting & Communication)

| Template | File | Dùng Khi Nào | Tần Suất |
|---|---|---|---|
| Weekly Status Report | `weekly-status-report-template.md` | Mỗi tuần gửi cho stakeholders | Hàng tuần |
| Meeting Minutes | `meeting-minutes-template.md` | Sau mỗi cuộc họp quan trọng | Trong 24h sau meeting |

---

## Khi Nào Dùng Template Nào

### Theo Giai Đoạn Dự Án

```
INITIATION
├── Project Charter ← Bắt buộc, cần sponsor sign
├── RACI Matrix ← Ai làm gì, ai chịu trách nhiệm
└── Risk Register (khởi tạo) ← Top 5 risks ban đầu

PLANNING
├── WBS ← Breakdown toàn bộ công việc
├── Risk Register (hoàn chỉnh) ← Phân tích đầy đủ
└── Project Kickoff Checklist ← Prep cho kickoff

EXECUTION
├── Weekly Status Report ← Mỗi tuần
├── Meeting Minutes ← Sau mỗi meeting
├── Change Request Form ← Khi có thay đổi
└── Risk Register (cập nhật) ← Mỗi tuần

CLOSING
├── Lessons Learned (xem study/07-exercises/)
└── Final Status Report (dùng Weekly template)
```

### Theo Tình Huống Cụ Thể

**Khi mới nhận dự án:**
1. Đọc brief → Tạo Project Charter draft → Present cho sponsor
2. Dùng RACI Matrix để clarify roles ngay từ đầu

**Khi có scope creep:**
1. Mở Change Request Form
2. Phân tích impact (time/cost/quality)
3. Đưa lên sponsor để quyết định
4. Cập nhật Risk Register nếu có risk mới

**Khi chuẩn bị kickoff:**
1. Dùng Project Kickoff Checklist để không bỏ sót gì
2. Kickoff meeting → Meeting Minutes → Gửi trong 24h

**Khi báo cáo lên management:**
1. Weekly Status Report — ngắn gọn, tập trung vào exceptions (vấn đề cần quyết định)
2. Dùng màu đèn giao thông (🟢🟡🔴) để một cái nhìn là hiểu ngay

---

## Tips Quan Trọng

### Dành Cho PM Mới

- **Đừng hoàn hảo hóa** — Version 1 của Project Charter 60% đủ tốt rồi. Gửi đi, nhận feedback, iterate.
- **Template phải "live"** — Một document ai cũng biết tồn tại nhưng không ai đọc thì bằng không. Gửi reminder, nhắc lại trong meeting.
- **Điền ví dụ trước** — Khi share template cho team, điền sẵn 1-2 dòng ví dụ để team hiểu format kỳ vọng.

### Dành Cho PM Có Kinh Nghiệm

- **Customize theo công ty** — Thêm logo, màu sắc brand, naming convention của tổ chức.
- **Kết nối với tools** — Link từ Jira issues → Change Request, từ Confluence page → Risk Register.
- **Retrospective sau dự án** — Sau mỗi dự án, review lại templates: cái gì thiếu? cái gì thừa? Update cho dự án sau.

---

## Mục Lục Nhanh

- [Project Charter](./project-charter-template.md) — Document khai sinh dự án
- [Risk Register](./risk-register-template.md) — Quản lý rủi ro
- [Change Request](./change-request-template.md) — Kiểm soát thay đổi
- [Project Kickoff Checklist](./project-kickoff-checklist.md) — Checklist khởi động
- [Weekly Status Report](./weekly-status-report-template.md) — Báo cáo tuần
- [RACI Matrix](./raci-matrix-template.md) — Ma trận phân công trách nhiệm
- [Meeting Minutes](./meeting-minutes-template.md) — Biên bản họp
- [WBS Template](./wbs-template.md) — Phân rã công việc

---

*Cập nhật lần cuối: 2026 | Phiên bản: 1.0*
