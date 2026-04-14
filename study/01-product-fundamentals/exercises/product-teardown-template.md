# Product Teardown Template

## Mục Đích

Product teardown giúp bạn nhìn bất kỳ sản phẩm nào qua "mắt PM" — hiểu decisions đằng sau features, không chỉ là user bình thường.

---

## Template (Copy và Điền Cho Mỗi App)

```
Tên App: _______________
Platform: iOS / Android / Web
Category: _______________
Ngày phân tích: _______________
```

---

### 1. Thông Tin Cơ Bản

**Mô tả 1 câu:**
> [App X] giúp [target users] [làm gì] để [đạt được gì].

**Business model:**
- [ ] Freemium (free + paid features)
- [ ] Subscription (monthly/yearly)
- [ ] Transaction fee
- [ ] Advertising
- [ ] Enterprise licensing
- [ ] Marketplace commission

**Giai đoạn product:**
- [ ] Early (< 1M users)
- [ ] Growth (1M - 50M users)
- [ ] Mature (> 50M users)

---

### 2. Target Users

**Primary users (ai dùng nhiều nhất?):**
- Độ tuổi: ___
- Nghề nghiệp: ___
- Tech savviness: Low / Medium / High
- Tần suất dùng: Daily / Weekly / Monthly

**Secondary users:**
- ___

**User goals chính:**
1. ___
2. ___
3. ___

---

### 3. Core Value Proposition

**Tuyên bố giá trị cốt lõi (1-2 câu):**
> ___

**Tại sao users chọn sản phẩm này thay vì alternatives?**
- ___

**JTBD (Jobs To Be Done):**
> "When [situation], I want to [do something], so I can [outcome]."

---

### 4. Feature Analysis

**3 Core Features (quan trọng nhất):**

| Feature | Mô Tả | Tại Sao Quan Trọng | Observation |
|---------|-------|-------------------|-------------|
| Feature 1 | | | |
| Feature 2 | | | |
| Feature 3 | | | |

**Features đáng chú ý (design decisions):**
- ___

**Missing features (gaps bạn nhận thấy):**
- ___

---

### 5. UX Analysis

**Onboarding flow (mô tả step-by-step):**
1. ___
2. ___
3. ___

**Aha moment (khi nào user "hiểu" giá trị):**
> ___

**Friction points (điểm gây khó chịu):**
- ___

**Delighters (điều bất ngờ thú vị):**
- ___

---

### 6. Metrics (Assumptions)

**North Star Metric có thể là:**
> ___

**Các metrics quan trọng có thể track:**
- Acquisition: ___
- Activation: ___
- Retention: ___
- Revenue: ___

---

### 7. Competitive Position

**Direct competitors:**
- ___

**Indirect competitors:**
- ___

**Differentiators:**
- ___

---

### 8. Đánh Giá & Cải Tiến

**3 điểm mạnh:**
1. ___
2. ___
3. ___

**3 điểm yếu:**
1. ___
2. ___
3. ___

**3 cải tiến tôi sẽ đề xuất:**
1. **[Feature/Change]:** [Mô tả] → **Tại sao:** [Impact dự kiến]
2. **[Feature/Change]:** [Mô tả] → **Tại sao:** [Impact dự kiến]
3. **[Feature/Change]:** [Mô tả] → **Tại sao:** [Impact dự kiến]

---

## Ví Dụ Hoàn Chỉnh: GrabFood Vietnam

### 1. Thông Tin Cơ Bản

**Mô tả 1 câu:**
> GrabFood giúp người dùng đô thị Việt Nam đặt đồ ăn từ nhà hàng gần đó, giao đến tận nơi trong 30-45 phút.

**Business model:** Marketplace commission (từ restaurant 25-30%) + delivery fee từ user

---

### 2. Target Users

**Primary users:** Người đi làm 22-40 tuổi, TP.HCM/Hà Nội, smartphone savvy, bận rộn không muốn nấu ăn.

**Secondary users:** Families order vào cuối tuần, office groups order cùng nhau.

**User goals:**
1. Ăn nhanh mà không cần ra ngoài
2. Khám phá món mới gần nhà
3. Lưu lại địa chỉ giao hàng quen thuộc

---

### 3. Core Value Proposition

> GrabFood là cách nhanh nhất và đáng tin nhất để đặt đồ ăn tại Việt Nam, với delivery được track real-time và tích hợp vào hệ sinh thái Grab.

**JTBD:** "When tôi về nhà mệt và không muốn nấu, tôi muốn đặt đồ ăn nhanh từ nhà hàng quen, so I can ăn tối trong 30 phút không cần suy nghĩ nhiều."

---

### 4. Feature Analysis

| Feature | Mô Tả | Tại Sao Quan Trọng | Observation |
|---------|-------|-------------------|-------------|
| Real-time tracking | Map tracking shipper | Giảm anxiety "hàng đến chưa?" | UX tốt, nhưng ETA thường lệch |
| Saved addresses | Lưu nhà, cơ quan | Giảm friction khi order | Smart — first order friction cao nhất |
| GrabRewards | Điểm thưởng từ mọi dịch vụ Grab | Lock-in users trong Grab ecosystem | Cross-product rewards là moat lớn |

**Missing features:**
- Group order cho văn phòng (order cùng nhau, tách bill)
- Scheduled order (đặt trước cho giờ ăn trưa)

---

### 8. Đánh Giá & Cải Tiến

**3 điểm mạnh:**
1. Ecosystem integration với GrabCar/GrabPay — cross-sell tự nhiên
2. Real-time tracking tạo trust
3. Flash deals và vouchers tạo habit (daily active usage)

**3 điểm yếu:**
1. Commission cao → restaurants tăng giá → users cảm thấy đắt
2. Delivery time estimate không chính xác → frustration
3. Customer support chậm khi có vấn đề

**3 cải tiến tôi sẽ đề xuất:**
1. **Group Order Feature:** Cho phép nhiều người cùng order vào một đơn → chia bill tự động → Target: tăng order value 40% cho office segment
2. **Smarter ETA:** Machine learning dựa vào traffic real-time + kitchen prep time thực → Target: giảm ETA error xuống < 5 phút
3. **Restaurant Partner Portal improvement:** Dashboard metrics cho restaurants → Giúp restaurant owners cải thiện menu → Win-win: happy restaurant = better quality = happy users
