# PM Interview Prep — Cheat Sheet

> Compact, printable. Dùng ngay trước buổi phỏng vấn để warm up.

---

## PRODUCT DESIGN INTERVIEW (45 phút)

### Khung Thời Gian Chuẩn
```
Phút 0–5    CLARIFY       → Hỏi câu làm rõ, set scope
Phút 5–10   USERS         → Identify & prioritize user segments
Phút 10–20  PAIN POINTS   → Brainstorm + prioritize pain points của segment chính
Phút 20–35  SOLUTIONS     → Brainstorm ideas, prioritize top 2–3
Phút 35–43  METRICS       → Define success metrics
Phút 43–45  TRADEOFFS     → Tự nêu limitations của solution bạn đề xuất
```

### 5 Câu Clarify Hay Nhất
1. "Đây là product mới hay cải thiện product hiện tại?"
2. "Mục tiêu kinh doanh chúng ta đang solve là gì — growth, retention, hay revenue?"
3. "Có platform nào được focus không (mobile, web, desktop)?"
4. "Có market/geography nào cụ thể không?"
5. "Timeline constraints có không?"

### Câu Nói Mở Đầu (sau clarify)
> "OK, để cấu trúc câu trả lời của mình, tôi sẽ đi theo flow: identify users → pain points → solutions → metrics. Bạn có muốn tôi theo hướng này không?"

### Prioritize Users
Không list tất cả users — chọn 1 segment để deep dive:
- "Tôi sẽ focus vào [segment X] vì đây là [largest/most underserved/highest value] segment"
- Dùng 2×2: User size × User underservedness → chọn góc top-right

### Brainstorm Pain Points
Structure pain points theo user journey:
```
[Trigger] → [Discovery] → [Onboarding] → [Core action] → [Retention] → [Share]
Ghi pain points tại TỪNG BƯỚC, sau đó prioritize
```

### Prioritize Solutions
Không chọn random — explain trade-offs:
- "Solution A có impact cao nhưng effort lớn, phù hợp long-term"
- "Solution B có thể ship trong 1 sprint, test hypothesis trước"
- "Tôi chọn Solution B để ship nhanh và validate, với kế hoạch evolve sang A"

### Common Mistakes — 5 Điều Tránh
1. **Nhảy vào solution ngay** — Luôn clarify + identify users + pain points TRƯỚC
2. **Quên metrics** — Mọi solution cần success metrics. Interviewer chú ý điều này.
3. **Chọn feature không khả thi** — Brief check: "Từ tech perspective, điều này cần [X time/resources] nhưng value là [Y] nên worthwhile"
4. **Không prioritize** — List 10 solutions mà không chọn = không có PM thinking
5. **Không nói trade-offs** — PM tốt acknowledge downsides của giải pháp họ chọn

---

## MARKET SIZING (ESTIMATION)

### 4-Bước Framework
```
Bước 1: CLARIFY   → "Bạn muốn tôi estimate cái gì chính xác? [metric cụ thể]"
Bước 2: APPROACH  → "Tôi sẽ approach top-down / bottom-up vì..."
Bước 3: ESTIMATE  → Tính từng component, state assumptions rõ ràng
Bước 4: SANITY    → "Kết quả X có vẻ [reasonable/unreasonable] vì..."
```

### Vietnam Reference Numbers (Học Thuộc)
```
Dân số Việt Nam:          ~100 triệu người (2025)
Dân số đô thị:            ~40% = ~40 triệu
Dân số HCM:               ~10 triệu (nội thành) / 13M (toàn thành phố)
Dân số Hà Nội:            ~8 triệu (nội thành) / 10M (toàn thành phố)
Internet users:           ~80 triệu (~80% dân số)
Smartphone users:         ~70 triệu (~70%)
E-commerce users:         ~57 triệu
GDP per capita VN:        ~$4,200 USD/năm (~350 USD/tháng)
GDP HCM/Hanoi:            ~$6,000–7,000 USD/năm cao hơn

Hộ gia đình:              ~25 triệu hộ (TB 4 người/hộ)
Lực lượng lao động:       ~55 triệu người
Người dùng smartphone trẻ (18–35): ~30 triệu
```

### Global Reference Numbers (Thường Dùng)
```
Dân số thế giới:          ~8 tỷ người
Dân số Mỹ:                ~335 triệu
Dân số SEA:               ~700 triệu
Internet users toàn cầu:  ~5 tỷ
Smartphone users:         ~6.8 tỷ
```

### Ví Dụ Estimation: "Thị trường food delivery VN là bao nhiêu?"
```
Approach: Bottom-up (order frequency)

Giả định:
- Smartphone users HCM + Hanoi ≈ 15 triệu người
- Food delivery users ≈ 30% = 4.5 triệu users active
- Orders/user/tháng ≈ 4 orders (1 lần/tuần)
- Average order value ≈ 80,000 VND ($3.2 USD)
- Platform take rate ≈ 20%

GMV = 4.5M × 4 × 80,000 = 1.44 nghìn tỷ VND/tháng = ~$58M USD/tháng
Annual GMV ≈ $700M USD/năm
Platform revenue ≈ $140M USD/năm (20% take rate)

Sanity check: Grab + Baemin + ShopeeFood total est. $300–500M GMV 
→ Reasonable order of magnitude ✓
```

---

## BEHAVIORAL QUESTIONS (STAR Method)

### 10 Câu Hay Nhất — Chuẩn Bị Câu Trả Lời Cho Từng Câu
1. "Hãy kể về lần bạn influence team mà không có authority."
2. "Mô tả lần bạn phải đưa ra quyết định khó với dữ liệu không đầy đủ."
3. "Kể về lần feature bạn build không đạt kết quả mong đợi. Bạn đã làm gì?"
4. "Mô tả lần bạn phải prioritize giữa nhiều projects cạnh tranh nhau."
5. "Kể về lần bạn nhận feedback khó về công việc của mình."
6. "Hãy nói về sản phẩm bạn tự hào nhất đã contribute vào."
7. "Mô tả lần bạn phải thuyết phục stakeholder về một quyết định khó."
8. "Kể về lần bạn phải trì hoãn/cancel feature vì data hoặc research."
9. "Mô tả cách bạn work với engineer/designer để solve technical challenge."
10. "Kể về lần bạn fail và bạn học được gì?"

### STAR Template Điền Nhanh
```
Câu [số]: _______________________________________________

S (Situation): Thời điểm [công ty, role, context]...
T (Task): Tôi cần/chịu trách nhiệm...
A (Action): Tôi đã [verb cụ thể] bằng cách...
             Đầu tiên tôi... Sau đó tôi... Cuối cùng tôi...
R (Result): Kết quả là [metric cụ thể nếu có]...
```

### Power Verbs Dùng Trong STAR
```
Led, Drove, Launched, Shipped, Increased, Reduced, Improved,
Aligned, Facilitated, Prioritized, Proposed, Validated, Tested,
Synthesized, Presented, Negotiated, Influenced, Collaborated,
Defined, Designed, Analyzed, Identified, Resolved, Delivered
```

### Câu Trả Lời Cho "Điểm Yếu"
**Template tốt:**
> "Điểm yếu của tôi là [weakness thật, không fake]. Ví dụ cụ thể là [situation]. Tôi đã nhận ra điều này và đang actively work on it bằng [cách cụ thể bạn đang improve]. Gần đây tôi đã thấy improvement khi [evidence]."

**Không nói:** "Tôi perfectionist" / "Tôi làm việc quá chăm" — mọi người đều nói vậy, interviewer ghét.

---

## TECHNICAL PM QUESTIONS

### API Knowledge Cần Biết
```
REST API:
- Endpoint = URL + HTTP method (GET, POST, PUT, DELETE, PATCH)
- Request = gửi data lên server
- Response = server trả về (200 OK, 404 Not Found, 500 Server Error)
- Status codes quan trọng: 200 (success), 201 (created), 400 (bad request), 
  401 (unauthorized), 403 (forbidden), 404 (not found), 429 (rate limited), 500 (server error)

PM context:
- "API-first" design = build API trước, UI sau
- "Breaking change" = API thay đổi làm hỏng existing integrations
- "Versioning" = /v1/users, /v2/users → backward compatibility
- "Rate limiting" = throttle requests để protect server
```

### System Design Vocabulary (PM Level)
```
Load Balancer    → Distribute traffic across servers
CDN              → Serve static files from edge servers gần user
Cache            → Store frequently accessed data in memory (Redis, Memcached)
Database sharding → Split database horizontally để scale
Microservices    → Architecture chia nhỏ app thành independent services
Message queue    → Async processing (Kafka, RabbitMQ) — "fire and forget"
API Gateway      → Single entry point cho all microservices

Latency targets:
< 100ms   = Users feel instant
100–300ms = Acceptable
300–1000ms = Slow, users notice
> 1000ms  = Users frustrated (abandon)
```

### Performance Metrics (PM Context)
```
p50 (median)   = 50% requests faster than this → "typical user experience"
p90            = 90% requests faster than this
p95            = 95% requests faster than this
p99            = 99% requests faster than this → "worst normal case"

Khi nói về performance với engineering:
"p99 latency cao = 1 trong 100 users gặp trải nghiệm tệ"
"Tôi muốn p95 < 500ms và p99 < 1s cho critical flows"

Availability SLA:
99%    = 3.65 ngày downtime/năm (không acceptable)
99.9%  = 8.77 giờ/năm
99.99% = 52 phút/năm (typical enterprise SLA)
99.999% = 5.25 phút/năm (high availability)
```

### Khi Interviewer Hỏi Technical Depth
```
Nếu câu hỏi technical quá: "Tôi không đi sâu vào implementation chi tiết, 
nhưng từ PM perspective, điều quan trọng là [business/user impact]. 
Tôi sẽ work với engineering team để evaluate [specific tradeoffs]."

Lợi thế Developer: Bạn CÓ THỂ đi sâu hơn. Dùng khi relevant.
Câu: "Với background Engineering của tôi, tôi hiểu rằng [technical consideration] 
ảnh hưởng đến [user experience / scalability / maintenance cost]..."
```

---

## QUESTIONS TO ASK INTERVIEWERS (15 Câu Hay)

### About the Role (Hỏi 2–3 câu)
1. "Trong 90 ngày đầu, bạn expect tôi sẽ accomplish gì?"
2. "PM này sẽ own product area nào, và metrics nào?"
3. "Sự khác biệt giữa PM tốt và PM excellent trong team này là gì?"
4. "Team có product strategy rõ ràng cho 12 tháng tới không?"

### About the Team (Hỏi 1–2 câu)
5. "Team Engineering và Product work với nhau như thế nào? Discovery có phải là joint activity không?"
6. "PM và Designer work thế nào? Ai own wireframes/specs?"
7. "Engineering team có empowered không — họ có thể push back và suggest alternatives không?"

### About the Product (Hỏi 1–2 câu)
8. "North Star Metric hiện tại của product là gì? Nó đang trending như thế nào?"
9. "Challenges lớn nhất product đang đối mặt trong 6 tháng tới là gì?"
10. "Quyết định product nào gần đây bạn tự hào nhất? Và một quyết định bạn nhìn lại muốn làm khác?"

### About Culture & Growth (Hỏi 1–2 câu)
11. "Người trong team này thường grow như thế nào — cả trong công ty lẫn industry?"
12. "Failure được handle như thế nào ở đây? Có thể cho ví dụ về team learning từ failure không?"
13. "Decision making process như thế nào? PM có autonomy thực sự hay nhiều process phải qua không?"

### Closing Questions (Hỏi ít nhất 1)
14. "Còn điều gì về background hoặc skills của tôi mà bạn muốn biết thêm không?"
15. "Next steps trong hiring process là gì?"

### Câu Không Nên Hỏi
- "Lương là bao nhiêu?" (đợi vòng offer)
- "Có remote work không?" (hỏi sau khi có offer)
- "Đọc trên website rồi" (cho thấy bạn không research)

---

## PRODUCT SENSE — QUICK EVALUATION RUBRIC

### Câu "Sản phẩm yêu thích của bạn là gì?"
**Template trả lời:**
1. Tên product và vì sao bạn chọn (1 câu)
2. Target user là ai, problem nào được solve (2 câu)
3. 1–2 điều product làm đặc biệt tốt (với ví dụ cụ thể)
4. 1 điều bạn sẽ improve (với lý do và metric cụ thể)

**Không chọn:** Google, Facebook (quá generic). Chọn product bạn THỰC SỰ dùng.

**Ví dụ tốt:** "Tôi thích Grab Pay vì [specific reason] — họ giải quyết [specific pain] cho [specific users]. Điều tôi sẽ improve là [specific feature] vì [data/reasoning]..."

---

## NGÀY PHỎNG VẤN — CHECKLIST

**Đêm trước:**
- [ ] Đọc lại JD và research company (products, recent news, metrics)
- [ ] Chuẩn bị 3–5 STAR stories (không cần học thuộc, hiểu structure)
- [ ] Review cheat sheet này 1 lần

**30 phút trước:**
- [ ] Đọc lại AARRR, RICE, product design framework một lần
- [ ] Nghĩ về 1 product bạn admire và WHY (dùng cho product sense questions)

**Trong phỏng vấn:**
- [ ] Luôn clarify trước khi answer
- [ ] Think out loud — interviewer muốn nghe process, không chỉ answer
- [ ] "Tôi muốn dành 30 giây organize suy nghĩ trước khi trả lời" — OK để nói điều này

**Sau phỏng vấn:**
- [ ] Gửi thank-you email trong 24 giờ (ngắn, specific)
- [ ] Ghi lại câu hỏi bạn stumble để improve cho lần sau
