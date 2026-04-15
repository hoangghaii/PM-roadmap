# Bài Tập 2: Risk Register

**Mục tiêu:** Identify và assess rủi ro cho dự án thực tế
**Thời gian:** 2-4 giờ
**Cấp độ:** Giai đoạn 1-2

---

## Hướng Dẫn

**Yêu cầu:** Viết Risk Register với ít nhất **8 rủi ro** đầy đủ: Probability, Impact, Score, Strategy, Action, Owner.

**Bước 1:** Chọn dự án (dự án thực tế bạn đang tham gia, hoặc dùng scenario bên dưới)
**Bước 2:** Brainstorm risks theo categories
**Bước 3:** Assess từng risk (Probability × Impact)
**Bước 4:** Chọn response strategy và define actions

---

## Risk Categories (để brainstorm)

- **Technical:** Integration failures, technology unknown, technical debt
- **Schedule:** Key person unavailable, dependency delays, underestimation
- **Resource:** Developer turnover, skill gaps, budget cuts
- **External:** Vendor issues, regulatory changes, third-party APIs
- **Stakeholder:** Scope creep, lack of engagement, changing requirements
- **Quality:** Testing insufficient, unclear acceptance criteria

---

## Risk Scoring Matrix

```
Impact →    1 (Negligible)  2 (Minor)  3 (Moderate)  4 (Significant)  5 (Critical)
Prob ↓
  5 (Very High)    5         10         15            20              25
  4 (High)         4          8         12            16              20
  3 (Medium)       3          6          9            12              15
  2 (Low)          2          4          6             8              10
  1 (Very Low)     1          2          3             4               5

Score 15-25: 🔴 HIGH   → Escalate ngay, active mitigation
Score 8-14:  🟡 MEDIUM → Monitor chặt, có mitigation plan
Score 1-7:   🟢 LOW    → Accept, periodic review
```

---

## Template Blank

| ID | Mô Tả Rủi Ro | Category | P (1-5) | I (1-5) | Score | Level | Strategy | Action | Owner | Due | Status |
|---|---|---|---|---|---|---|---|---|---|---|---|
| R001 | | | | | | | | | | | |

**Response Strategies:**
- **Avoid:** Loại bỏ nguyên nhân của risk
- **Transfer:** Chuyển risk sang bên khác (insurance, contract)
- **Mitigate:** Giảm probability hoặc impact
- **Accept:** Chấp nhận risk, có contingency plan

---

## Ví Dụ Hoàn Chỉnh: Risk Register cho Migration Project

**Project:** Migration hệ thống Delphi legacy sang .NET modern stack
**Budget:** 2 tỷ VND | **Duration:** 9 tháng | **Team:** 5 developers

| ID | Mô Tả Rủi Ro | Cat. | P | I | Score | Level | Strategy | Action | Owner | Due |
|---|---|---|---|---|---|---|---|---|---|---|
| R001 | Key developer (senior .NET) nghỉ việc giữa dự án | Resource | 3 | 5 | 15 | 🔴 | Mitigate | Cross-train 1 dev thứ 2, document architecture | PM | M2 |
| R002 | Third-party payment API thay đổi breaking change | External | 2 | 4 | 8 | 🟡 | Mitigate | Monitor release notes, abstraction layer, fallback manual | Tech Lead | M1 |
| R003 | Client không release UAT environment đúng deadline | Stakeholder | 4 | 3 | 12 | 🟡 | Mitigate | Commitment letter từ client IT, buffer 1 tuần trong plan | PM | M1 |
| R004 | Budget bị cắt 20% sau Q3 company review | Resource | 2 | 5 | 10 | 🟡 | Mitigate | Prepare scope reduction plan (20% scope cut) sẵn sàng | PM | M3 |
| R005 | Data migration corrupt partial data từ Oracle sang PostgreSQL | Technical | 3 | 5 | 15 | 🔴 | Mitigate | Data validation scripts, rollback plan, parallel run 2 tuần | Tech Lead | M5 |
| R006 | Security audit phát hiện critical issues trước go-live | Quality | 2 | 5 | 10 | 🟡 | Mitigate | Early security review ở M4, fix buffer 2 tuần trước go-live | PM+SecTeam | M7 |
| R007 | Legacy system documentation không đầy đủ → mất thêm thời gian reverse engineer | Technical | 4 | 3 | 12 | 🟡 | Accept | Budget thêm 2 tuần trong schedule cho reverse engineering | Tech Lead | M1 |
| R008 | Key stakeholder thay đổi ở phía client (sponsor mới) | Stakeholder | 2 | 4 | 8 | 🟡 | Mitigate | Stakeholder documentation, relationship với multiple contacts | PM | Ongoing |
| R009 | Network performance kém ở remote offices làm UAT chậm | External | 3 | 2 | 6 | 🟢 | Accept | Note trong UAT plan, test qua VPN trước, have IT contact | QA | M7 |
| R010 | Scope creep: client BA thêm requirements trong UAT | Stakeholder | 4 | 3 | 12 | 🟡 | Avoid | Change Request process, CAB approval required cho bất kỳ change | PM | Kickoff |

---

## Tips Identify Risks Không Bỏ Sót

### Technique 1: PESTLE Analysis
- **Political:** Government regulation, company politics
- **Economic:** Budget freeze, currency fluctuation
- **Social:** User resistance, culture change
- **Technological:** New tech unknown, legacy constraints
- **Legal:** Compliance, contract terms
- **Environmental:** Natural disaster, pandemic (less common)

### Technique 2: Historical Data
Hỏi: "Dự án tương tự trong quá khứ gặp vấn đề gì?"
- Check lessons learned từ projects trước
- Ask PM khác đã làm dự án tương tự

### Technique 3: Assumption Analysis
Mọi assumption trong Project Charter đều là potential risk nếu assumption sai:
- Assumption: "Client IT team sẽ available 20%/tuần" → Risk nếu không available
- Assumption: "Legacy API documentation đầy đủ" → Risk nếu incomplete

### Technique 4: WBS Risk Review
Đi qua từng work package trong WBS và hỏi:
- "Điều gì có thể làm work package này fail?"
- "Ai phụ thuộc vào work package này?"
- "Điều gì ngoài tầm kiểm soát của chúng ta?"

---

## Checklist Tự Đánh Giá

- [ ] Ít nhất 8 risks được identified
- [ ] Mỗi risk có đủ: P, I, Score, Strategy, Action, Owner
- [ ] Ít nhất 1 risk mỗi category: Technical, Schedule, Resource, External, Stakeholder
- [ ] HIGH risks có mitigation action cụ thể với deadline
- [ ] Action items assignable và measurable
- [ ] Risk Review cadence được define (weekly? biweekly?)
