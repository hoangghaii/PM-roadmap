# RACI Matrix Template

## Định Nghĩa

| Letter | Vai Trò | Mô Tả | Rule |
|---|---|---|---|
| **R** | Responsible | Người thực hiện công việc | Có thể nhiều người |
| **A** | Accountable | Người chịu trách nhiệm cuối cùng | **Chỉ 1 người/task** |
| **C** | Consulted | Người được hỏi ý kiến trước quyết định | 2-way communication |
| **I** | Informed | Người được thông báo kết quả | 1-way communication |

---

## Rules Khi Tạo RACI

1. **Mỗi task phải có ít nhất 1 R và đúng 1 A** — không có A = không ai chịu trách nhiệm
2. **A không nhất thiết = R** — nhưng thường người làm (R) cũng là người chịu trách nhiệm (A)
3. **Quá nhiều C = bottleneck** — giới hạn C tối đa 2-3 người/task
4. **Không overload 1 người với quá nhiều A** — phân tán accountability
5. **Nếu không biết điền gì → điền I** — tốt hơn bỏ trống

---

## Template Blank (Software Project)

| Task / Deliverable | PM | Dev Lead | QA Lead | BA | UX/Designer | Tech Arch | Sponsor | Client | End User |
|---|---|---|---|---|---|---|---|---|---|
| Project Charter | | | | | | | | | |
| Requirements Gathering | | | | | | | | | |
| System Architecture Design | | | | | | | | | |
| Sprint Planning | | | | | | | | | |
| Development | | | | | | | | | |
| Code Review | | | | | | | | | |
| Testing (QA) | | | | | | | | | |
| UAT | | | | | | | | | |
| Change Request Evaluation | | | | | | | | | |
| Go/No-Go Decision | | | | | | | | | |
| Go-Live Execution | | | | | | | | | |
| Hypercare Support | | | | | | | | | |
| Lessons Learned | | | | | | | | | |
| Project Closure | | | | | | | | | |

---

## Ví Dụ Đã Điền (Software Project)

| Task / Deliverable | PM | Dev Lead | QA Lead | BA | Sponsor | Client |
|---|---|---|---|---|---|---|
| Project Charter | **A/R** | C | I | C | **A** | I |
| Requirements Gathering | C | I | C | **A/R** | I | **R** |
| System Architecture | I | **A/R** | C | C | I | I |
| Sprint Planning | **A** | **R** | C | R | I | I |
| Development | I | **A/R** | C | C | I | I |
| Testing (QA) | **A** | C | **R** | C | I | I |
| UAT | **A** | C | R | C | I | **R** |
| Change Request | **A/R** | C | C | C | **A** | R |
| Go/No-Go Decision | C | C | C | C | **A** | **R** |
| Go-Live | **A/R** | R | R | I | I | I |
| Hypercare | **A** | R | R | I | I | I |
| Lessons Learned | **A/R** | R | R | R | I | I |

---

## RACI cho ERP Project (ví dụ phức tạp hơn)

| Task | PM | Func Consultant | Tech Consultant | BA | IT Manager | Finance Lead | CEO/Sponsor |
|---|---|---|---|---|---|---|---|
| Business Blueprint | C | **A/R** | C | **R** | C | **R** | A |
| System Config | I | **A/R** | C | C | C | I | I |
| Data Migration | **A** | C | **R** | R | R | C | I |
| Integration Testing | **A** | C | **R** | C | R | C | I |
| UAT | **A** | R | C | C | C | **R** | I |
| Training | **A** | **R** | I | C | I | C | I |
| Go-Live Decision | C | C | C | C | C | C | **A** |
| Go-Live Execution | **A/R** | R | R | C | R | C | I |

---

## Common Mistakes

| Mistake | Problem | Fix |
|---|---|---|
| Không có A cho 1 task | Không ai chịu trách nhiệm nếu fail | Assign A rõ ràng |
| 2 người cùng là A | Conflict, blame game | Chỉ 1 A/task |
| 6 người là C | Meeting/approval bottleneck | Giới hạn C ≤ 3 |
| Tất cả là I | Không ai đọc updates | Chỉ include I với people thực sự cần biết |
| PM là A cho mọi thứ | PM overloaded, micro-management | Delegate accountability |
