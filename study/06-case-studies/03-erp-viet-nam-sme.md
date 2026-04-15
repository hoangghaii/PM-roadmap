# Case Study 7: Triển Khai ERP cho Công Ty SME Việt Nam

**Loại:** Vietnam Context — Mixed Success
**Kỹ năng:** Change management, stakeholder management trong văn hóa VN, scope control

---

## Tổng Quan Nhanh

| Thông tin | Chi tiết |
|---|---|
| Tổ chức | Công ty nhựa Minh Phát (tên giả), Hà Nội |
| Quy mô | 200 nhân viên, doanh thu ~80 tỷ VND/năm |
| Phần mềm | SAP Business One |
| Budget | 2 tỷ VND |
| Timeline kế hoạch | 9 tháng |
| Timeline thực tế | 10.5 tháng (+6 tuần) |
| Kết quả ngân sách | ~2.2 tỷ VND (+10%) |
| Kết quả tổng thể | Mixed — hệ thống go-live thành công nhưng adoption chậm 3 tháng đầu |

---

## 1. Bối Cảnh Chi Tiết

### Về công ty

Công ty nhựa Minh Phát hoạt động từ 2005, sản xuất bao bì nhựa công nghiệp cho các nhà máy và siêu thị. Năm 2021, doanh thu tăng 35% so với năm trước nhờ bùng nổ e-commerce. Ban lãnh đạo quyết định đây là thời điểm "lên đời" hệ thống quản lý.

**Tình trạng trước ERP:**
- Kế toán: Excel + phần mềm MISA riêng lẻ
- Kho: Sổ tay + Excel của từng thủ kho
- Sản xuất: Phiếu giấy, báo cáo cuối ngày gõ lại vào Excel
- Bán hàng: CRM tự làm bằng Google Sheets
- Mua hàng: Email + Excel

Hậu quả: Tháng nào cũng mất 15-20 ngày để "đối chiếu số" giữa các phòng. Giám đốc muốn biết tồn kho thực tế phải chờ 2-3 ngày.

### Project Profile

| Hạng mục | Chi tiết |
|---|---|
| Giải pháp | SAP Business One (phiên bản cloud) |
| Vendor | Công ty tư vấn SAP tại Hà Nội (giấu tên) |
| PM phía vendor | Nguyễn Minh Tuấn, 5 năm kinh nghiệm ERP |
| PM phía client | Lê Thị Hoa, IT Manager, lần đầu làm ERP project |
| Developers | 3 từ vendor + 2 IT nội bộ |
| Key Users | 12 người từ Kế toán, Kho, Mua hàng, Bán hàng |
| Modules triển khai | Financials, Inventory, Purchasing, Sales |
| Modules chưa triển khai | Production Planning (để Phase 2) |

---

## 2. Năm Thách Thức Đặc Thù Việt Nam

### Thách Thức 1: User Resistance Cao

**Root cause:**

Người Việt Nam nói chung có xu hướng né tránh thay đổi khi cảm thấy không kiểm soát được tình huống. Trong trường hợp này, nhiều nhân viên lâu năm (5-15 năm) lo lắng:
- "Hệ thống mới có thể theo dõi tôi làm gì mỗi ngày"
- "Nếu hệ thống tự làm được, họ có cần tôi không?"
- "Tôi đã quen với cách cũ, học cái mới này làm gì?"

Đặc biệt, trưởng phòng kế toán — người có 12 năm kinh nghiệm với MISA — cảm thấy uy tín của mình bị đe dọa khi phải học lại từ đầu.

**Biểu hiện cụ thể:**
- 40% nhân viên không attend training đúng hạn (bận việc khác)
- Sau go-live 1 tháng, 30% nhân viên vẫn nhập liệu vào Excel song song, sau đó copy sang SAP
- Thủ kho tạo ra "bảng riêng" để theo dõi tồn kho vì "không tin hệ thống"
- Kế toán viên báo cáo bug liên tục nhưng nhiều bug là "user error" do không dùng đúng cách

**Chiến lược: Change Management theo 8 bước Kotter**

```
Bước 1: Tạo urgency (Tháng 1)
→ Workshop: "Excel không scale khi công ty lên 500 người"
→ Demo: Tính toán sai lầm trong Excel gây thiệt hại như thế nào
→ So sánh với đối thủ cạnh tranh đã dùng ERP

Bước 2: Form coalition (Tháng 1)
→ Tìm 3-4 "ERP Champions" trong từng phòng
→ Champion = người có uy tín, được đồng nghiệp tin tưởng
→ Đào tạo Champions trước, để họ hỗ trợ đồng nghiệp

Bước 3: Communicate vision (Suốt dự án)
→ Monthly all-hands cập nhật tiến độ
→ Poster ở căng-tin về "3 tháng nữa chúng ta sẽ..."
→ CEO gửi video 2 phút mỗi tháng về tầm nhìn ERP

Bước 4: Enlist volunteers (Tháng 2-3)
→ Champions dẫn dắt user acceptance testing
→ Champions được ghi nhận trong company newsletter

Bước 5: Remove obstacles (Liên tục)
→ IT setup workstation đủ mạnh trước go-live
→ Giải quyết network issues ở tầng 3 (chỉ có WiFi yếu)
→ Support line hotline trong 3 tháng sau go-live

Bước 6: Short-term wins (Tháng 3, sau UAT đầu tiên)
→ Demo: "Giờ bạn có thể xem tồn kho real-time, không cần chờ thủ kho"
→ Demo: "Tính lương đúng hơn, không còn lỗi Excel"
→ Tính toán: Time-to-close kế toán giảm từ 20 ngày xuống 12 ngày

Bước 7: Sustain acceleration (Tháng 9-12)
→ Monthly report về adoption metrics
→ Phòng nào adoption cao nhất = recognition

Bước 8: Institute change (Tháng 12+)
→ "ERP first" = quy trình làm việc mới
→ KPI mới cho key users dựa trên data quality trong SAP
```

---

### Thách Thức 2: Sponsor Kỳ Vọng Phi Thực Tế

**Root cause:**

Giám đốc Minh Phát — một doanh nhân tự thân lập nghiệp — có mental model về phần mềm giống như mua thiết bị sản xuất: mua về, cắm điện, chạy. Ông không có kinh nghiệm với dự án IT phức tạp.

**Biểu hiện:**
- Tuần 3 của dự án: "Sao chưa dùng được? Tôi tưởng mới 9 tháng?"
- Khi PM báo risk đầu tiên: "Tôi không muốn nghe vấn đề, tôi muốn nghe giải pháp"
- Khi có một module nhỏ bị delay: "Thế này thì 9 tháng chắc không xong rồi, thôi thuê thêm người"

**Chiến lược: Education và Structured Governance**

PM vendor (Tuấn) tổ chức một buổi "ERP Education Session" trong tuần đầu tiên với giám đốc:

```
Agenda Education Session (2 giờ):
1. ERP là gì (và không phải gì) — 30 phút
   - Không phải mua phần mềm, đây là business transformation
   - SAP là công cụ, nhưng thay đổi quy trình là công việc của người dùng

2. Case studies ERP failures — 30 phút
   - Hershey's: ERP go-live sai timing → mất $150M doanh thu Giáng sinh
   - FoxMeyer Drug: ERP failure → công ty phá sản
   - Bài học: Đây không phải vì SAP kém, mà vì expectations và process

3. ERP Success Factors — 30 phút
   - Sponsor active involvement (không phải chỉ ký budget)
   - Key user availability
   - Data quality
   - Change management

4. Governance structure cho dự án này — 30 phút
   - Monthly Steering Committee: Giám đốc + PM + Department Heads
   - Agenda cố định: Status, Risks, Decisions needed
   - RAG status (Red/Amber/Green) cho mỗi area
```

Monthly Steering Committee trở thành nền tảng quan trọng — giám đốc được update định kỳ thay vì hỏi ngẫu nhiên, và PM có forum để escalate issues chính thức.

---

### Thách Thức 3: Data Quality Kém

**Root cause:**

15 năm hoạt động với Excel, mỗi phòng tự quản lý data theo cách riêng. Không có master data governance.

**Thực trạng phát hiện trong Data Audit (Tháng 1):**

| Vấn đề | Số lượng | Ví dụ cụ thể |
|---|---|---|
| Mã vật tư trùng lặp | 847 records | "Túi PE 30x40" = PE-3040 / TUI-PE-3040 / 3040PE |
| Tồn kho SAP vs thực tế | Chênh lệch 23% | SAP: 5,000 thùng; Kho thực: 4,100 thùng |
| Thông tin nhà cung cấp thiếu | 156/400 vendors | Thiếu mã số thuế, địa chỉ, account ngân hàng |
| Chart of accounts không chuẩn | 89 accounts | Tài khoản 641 và 642 bị merge sai |
| Đơn giá không nhất quán | 234 items | Giá nhập kho khác giá trên hợp đồng |

**Chiến lược:**

Phase Data Cleansing riêng (2 tháng, trước khi configure SAP):

```
Tháng 1: Data Audit
- IT internal + Vendor consultant review tất cả data sources
- Output: Data Quality Report với danh sách vấn đề và priority

Tháng 2: Data Cleansing
- Mỗi phòng có Data Quality Champion (người am hiểu nghiệp vụ nhất)
- Champion phụ trách clean data của phòng mình
- PM theo dõi via Data Quality Dashboard

Tiêu chí chấp nhận (Data Quality Acceptance Criteria):
✓ Mã vật tư: 100% unique, naming convention chuẩn
✓ Tồn kho: Chênh lệch < 2% sau physical count
✓ Nhà cung cấp: 100% có mã số thuế và account ngân hàng
✓ Chart of accounts: Review và approve bởi kiểm toán viên bên ngoài
✓ Đơn giá: 100% khớp với hợp đồng hoặc có approval exception
```

Kết quả: Data Cleansing mất thêm 3 tuần so với kế hoạch, nhưng tránh được thảm họa migrate data xấu vào SAP.

---

### Thách Thức 4: Scope Creep Từ Nhiều Phòng Ban

**Root cause:**

Khi nhân viên thấy ERP, họ nghĩ: "À, đây là cơ hội để làm cái tôi muốn từ lâu." Mỗi phòng có wish list riêng.

**Yêu cầu bổ sung phát sinh trong dự án:**

| Phòng | Yêu cầu | Ước tính công | Thời điểm |
|---|---|---|---|
| Kế toán | Auto-generate báo cáo thuế theo format mới nhất của Bộ TC | 40 giờ | Tháng 4 |
| Kho | Tích hợp barcode scanner (chưa có trong scope) | 80 giờ | Tháng 5 |
| Bán hàng | CRM module với email automation | 120 giờ | Tháng 5 |
| Mua hàng | Supplier portal để vendor tự nhập invoice | 160 giờ | Tháng 6 |
| Giám đốc | Dashboard mobile app | 200 giờ | Tháng 7 |

Nếu chấp nhận tất cả: +600 giờ công = +3 tháng và +500 triệu VND.

**Chiến lược: Change Advisory Board (CAB)**

```
CAB Structure:
- Họp: 2 tuần/lần, 1 giờ
- Thành viên: PM vendor, PM client, IT Manager, CFO
- Quorum: 3/4 thành viên

CAB Process cho mỗi Change Request:
1. Requestor điền Change Request Form (template chuẩn)
2. PM estimate effort + impact + risk
3. CAB review trong meeting tiếp theo
4. CAB vote: Approve cho Phase 1 / Defer to Phase 2 / Reject

Tiêu chí đánh giá:
- Business value (1-5): Ảnh hưởng đến doanh thu, chi phí, compliance
- Urgency (1-5): Cần go-live mới làm được hay có thể chờ?
- Effort (1-5): 1 = < 8 giờ, 5 = > 80 giờ
- Risk (1-5): Nguy cơ ảnh hưởng đến timeline go-live

Decision matrix:
- (Business Value × Urgency) > (Effort × Risk) → Xem xét Phase 1
- Còn lại → Phase 2 list
```

Kết quả: Từ 5 requests trên, chỉ có Báo cáo thuế được approve vào Phase 1 (compliance requirement). Phần còn lại vào Phase 2 list — và 2/4 được implement trong 6 tháng sau go-live.

---

### Thách Thức 5: Key User Vắng Mặt

**Root cause:**

Key users là những nhân viên giỏi nhất và bận nhất của công ty. Giám đốc kỳ vọng họ vừa làm công việc hàng ngày, vừa tham gia dự án ERP — mà không giảm workload.

**Biểu hiện:**
- Tỷ lệ tham dự UAT sessions: 60% (cần 100%)
- Business Analyst mất 2 ngày chờ feedback từ Trưởng kho
- Training bị reschedule 3 lần vì key users bận họp khác

**Chiến lược:**

```
Commitment Framework (ký từ tháng 1):

1. Commitment Letter:
   - Trưởng phòng mỗi bộ phận ký cam kết cụ thể
   - Ví dụ: "Tôi cam kết Nguyễn Văn A sẽ available 30% thời gian 
     từ tháng 6-9 cho dự án ERP"

2. Manager buy-in:
   - Giám đốc gửi email toàn công ty: "ERP project là priority #1"
   - KPI của trưởng phòng có thêm tiêu chí: "ERP project participation"

3. Capacity Planning rõ ràng:
   Project Plan thể hiện:
   ┌──────────┬────────────────────────────┬──────────┐
   │ Tháng    │ Key User                   │ % Time   │
   ├──────────┼────────────────────────────┼──────────┤
   │ T1-T3    │ Data Quality Champions     │ 20%      │
   │ T4-T5    │ UAT participants           │ 30%      │
   │ T6-T7    │ UAT leads + Sign-off       │ 50%      │
   │ T8       │ Training participants      │ 80%      │
   │ T9       │ Go-live + Hypercare        │ 100%     │
   └──────────┴────────────────────────────┴──────────┘

4. Replacement plan:
   Mỗi key user có backup được train trước (phòng khi nghỉ phép, ốm)
```

---

## 3. Timeline Thực Tế

```
TIMELINE DỰ ÁN ERP — MINH PHÁT

Tháng 1-2: ANALYSIS + DATA CLEANSING
├── Tháng 1: Business Process Analysis (as-is mapping)
│   ├── Workshop từng phòng: quy trình hiện tại là gì?
│   ├── Pain points identification
│   └── To-be process design
├── Tháng 1-2: Data Audit & Data Cleansing
│   ├── Data quality audit
│   ├── Cleansing by Data Champions
│   └── Data quality sign-off
└── Education Session cho Giám đốc & Steering Committee setup

Tháng 3-5: CONFIGURATION + DEVELOPMENT
├── SAP Business One configuration theo to-be processes
├── Custom reports development
├── Integration với phần mềm chấm công (không trong scope ban đầu)
└── Unit testing từng module

Tháng 6-7: USER ACCEPTANCE TESTING (UAT)
├── UAT Round 1: Functional testing (Tháng 6)
│   ├── 156 test cases
│   ├── 23 bugs critical, 45 bugs minor
│   └── Fail → fix → retest
├── UAT Round 2: Regression + Integration testing (Tháng 7 đầu)
└── UAT Sign-off (Tháng 7 cuối) ← trễ 2 tuần so với kế hoạch

Tháng 8: TRAINING
├── Train-the-trainer: Champions được train trước
├── End-user training theo phòng (8 sessions)
├── Power user training (SAP super users)
└── Cut-off date planning

Tháng 9: GO-LIVE + HYPERCARE
├── Data migration final (weekend trước go-live)
├── Go-live: đầu tháng 9 ← trễ 4 tuần (tổng 6 tuần so với plan)
└── Hypercare: support intensive 30 ngày sau go-live

Tháng 10-11: STABILIZATION
└── Hypercare tiếp tục (nhẹ hơn), adoption monitoring
```

---

## 4. Go-Live Strategy: Big Bang vs Phased

### Hai lựa chọn

**Big Bang:**
- Tất cả modules go-live cùng một ngày
- Risk cao, nhưng nhanh thoát khỏi giai đoạn "hai hệ thống song song"
- Phù hợp khi: team đã UAT kỹ, organization có change capacity cao

**Phased:**
- Go-live từng module hoặc từng bộ phận
- Risk thấp hơn, nhưng phức tạp hơn về data sync
- Phù hợp khi: công ty lớn, nhiều location, module phức tạp

### Minh Phát chọn gì và tại sao

**Quyết định: Big Bang (một ngày, tất cả modules)**

Lý do:
1. Công ty nhỏ (200 người), đơn vị sản xuất đơn lẻ — không có multiple sites
2. Modules có quan hệ chặt chẽ (mua hàng → nhập kho → tồn kho → kế toán) — khó phased
3. Rủi ro của việc duy trì hai hệ thống song song (Excel + SAP) quá lớn về data integrity
4. UAT đã đủ kỹ (2 rounds)

**Hypercare Plan (3 tháng sau go-live):**

```
Tháng 1 (Intensive):
- Hotline support: 8AM-8PM, 7 ngày/tuần
- 2 consultant on-site mỗi ngày
- Daily issue log review
- Mục tiêu: Giải quyết P1/P2 bugs trong 24 giờ

Tháng 2 (Standard):
- Hotline: Giờ hành chính
- 1 consultant on-site 3 ngày/tuần
- Weekly issue review
- Bắt đầu train super users về self-service

Tháng 3 (Transition):
- Remote support only
- Monthly support call
- Chuyển giao knowledge base cho IT nội bộ
- Handover document hoàn chỉnh
```

---

## 5. Kết Quả và ROI

### Kết quả dự án

| Chỉ số | Kế hoạch | Thực tế |
|---|---|---|
| Timeline | 9 tháng | 10.5 tháng (+6 tuần) |
| Budget | 2 tỷ VND | 2.2 tỷ VND (+10%) |
| Milestones delivered | 100% | 94% (5 milestones trễ, 1 bị defer) |
| User adoption sau 3 tháng | 90% | 72% |
| User adoption sau 6 tháng | 90%+ | 88% |

### ROI sau 1 năm vận hành

| Cải tiến | Baseline | Sau ERP | Tiết kiệm/năm |
|---|---|---|---|
| Thời gian đóng sổ kế toán | 20 ngày/tháng | 12 ngày/tháng | ~240 ngày-người/năm |
| Thời gian kiểm kho định kỳ | 3 ngày/quý | 1 ngày/quý | ~24 ngày-người/năm |
| Sai lệch đơn mua hàng | 8%/tháng | 1.5%/tháng | Tránh được ~120 triệu VND over-order |
| Báo cáo quản trị | 3 ngày/report | Real-time | Giám đốc có data ngay |
| Lỗi nhập liệu kép | Thường xuyên | Gần như 0 | Không đo được, nhưng rõ ràng |

---

## 6. Bài Học PM Quan Trọng Từ VN Context

### Bài học 1: Change Management không phải "nice to have" trong VN

Văn hóa Việt Nam có xu hướng tôn trọng cấp trên và tránh conflict. Điều này có thể dẫn đến "silent resistance" — người ta không phản đối công khai nhưng không thực sự adoption. PM cần proactively tạo safe space để người dùng express concerns.

### Bài học 2: Education trước implementation

Giải thích "tại sao" trước khi nói "làm gì". Đặc biệt với giám đốc SME Việt Nam, họ cần hiểu ERP như một business decision, không phải IT project.

### Bài học 3: Data Cleansing là critical path, không phải parallel track

Nhiều dự án ERP VN thất bại vì migrate "garbage data" vào hệ thống mới. "Garbage in, garbage out" — hệ thống 2 tỷ với data xấu sẽ cho ra kết quả xấu.

### Bài học 4: Commitment letter không đủ — cần quản lý trực tiếp của key user cam kết

Nhân viên VN không dám "trái lệnh sếp". Nếu sếp trực tiếp của họ không prioritize ERP, họ sẽ làm gì? Đúng, không prioritize ERP.

### Bài học 5: CAB là công cụ quản lý kỳ vọng, không chỉ scope control

CAB không chỉ ngăn scope creep — nó còn cho stakeholders thấy yêu cầu của họ được xét nghiêm túc, có process rõ ràng, và có lý do cụ thể khi bị defer.

---

## 7. Câu Hỏi Reflection

1. Trong dự án ERP này, User Resistance được giải quyết bằng Education và Champions. Nhưng nếu Trưởng phòng kế toán (người có uy tín nhất) vẫn resistant sau mọi can thiệp — PM nên làm gì?

2. Dự án trễ 6 tuần (+67% so với kế hoạch nếu tính theo budget). CEO hỏi PM: "Lần sau làm gì để không trễ?" — bạn sẽ trả lời gì?

3. Nếu bạn là PM client (Lê Thị Hoa, lần đầu làm ERP), bạn sẽ chuẩn bị những gì trước khi bắt đầu dự án? Kỹ năng gì cần học thêm?

4. Big Bang vs Phased go-live: Trong scenario nào, bạn sẽ chọn Phased mặc dù phức tạp hơn?

5. ROI của dự án này tính bằng tiền có vẻ không quá ấn tượng so với 2.2 tỷ đầu tư. Những giá trị "intangible" nào của ERP mà khó đo bằng số nhưng thực sự quan trọng?
