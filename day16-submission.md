# Day 16 Submission — Team [tên team]

## Members
- [tên + vai trò]
- [tên + vai trò]
- [tên + vai trò]

---

## 1. Idea reframed

**Original idea:**
> Một app fitness dùng AI giám sát tư thế tập luyện qua camera điện thoại, đưa cảnh báo khi tập sai và feedback sau buổi tập.

**Reframed as a product opportunity:**
> **Observed gap:** Sinh viên và dân văn phòng trẻ muốn tập tại nhà để cải thiện sức khỏe, nhưng đang "tập mù" — không có ai quan sát để biết động tác đúng/sai, dẫn tới (a) không hiệu quả, (b) tăng rủi ro chấn thương và đau cơ–xương–khớp mãn tính. YouTube chỉ là one-way, PT thì quá đắt so với thu nhập.
> **Founding belief:** Pose-detection trên mobile (MediaPipe / MoveNet / Apple Vision) hiện đã đủ chín để thay thế phần lớn use-case "giám sát form cho người mới" của PT. Kết hợp với mô hình freemium giá thấp, chúng tôi có thể biến 15–30 phút tập tại nhà thành buổi tập có phản hồi đo lường được — ở mức chi phí bằng ~5% của 1 buổi PT.

---

## 2. Customer / Segment Card

- **Segment name:** Sinh viên và dân văn phòng trẻ (18–30 tuổi) không có thời gian đến phòng gym, chưa có nền tảng kỹ thuật tập luyện.
- **Operational context:** Tập tại nhà / phòng trọ / văn phòng, vào bất kỳ khung giờ rảnh nào, **một mình hoàn toàn** — không có người quan sát hoặc góp ý. Thu nhập hạn chế (sinh viên chưa đi làm, office worker mới ra trường), không đủ tài chính thuê PT (400–800k/buổi).
- **Recurring workflow:**
  1. Sắp xếp một khoảng không gian đủ rộng (~2m²) tại nơi ở
  2. Mở app, chọn bài tập theo mục tiêu (giảm mỡ / tăng cơ / giảm đau lưng cổ)
  3. AI giám sát real-time qua camera, cảnh báo khi động tác sai
  4. Sau buổi tập: nhận report % form chuẩn, những lỗi lặp lại, điều chỉnh cho buổi sau
  5. Vòng lặp này lặp lại mỗi buổi tập (3–5 lần/tuần)
- **Pain moment:** Sau một đợt bị đau cổ–vai–gáy hoặc lưng do ngồi sai tư thế + ít vận động → quyết định phải tập để cải thiện → nhưng **không có cách nào tự kiểm tra mình tập đúng hay không**, sợ tập sai lại càng đau thêm.
- **Why now:**
  - Thị trường dân văn phòng Việt Nam đang phình to, bệnh nền cơ–xương–khớp đang **trẻ hóa** rõ rệt (trước 40 đã đau lưng, thoái hóa cổ)
  - Công nghệ pose-detection on-device đã đủ chín + giá smartphone đã phổ cập
  - Chi phí app rẻ, tối ưu được địa điểm/thời gian, hiệu quả có thể đo lường
- **Access path:** TikTok viral content (before/after, trend tư thế đúng), App Store SEO (từ khóa "tập gym tại nhà", "chữa đau lưng"), word-of-mouth trong nhóm bạn cùng phòng/đồng nghiệp, YouTube fitness channel hợp tác (affiliate).

**One-sentence description:**
> Sinh viên và dân văn phòng trẻ muốn tập tại nhà để khỏe hơn và giảm đau do ngồi nhiều, nhưng không có tiền thuê PT và không biết mình tập đúng hay sai — nên cần một "PT ảo" giám sát form real-time qua camera.

---

## 3. Need Map (2–3 needs)

### Need #1 (priority)
- **Statement (JTBD):** When tôi tập một mình tại nhà, I want biết ngay lập tức động tác của mình đúng hay sai, so I can tránh chấn thương và đảm bảo buổi tập thực sự có hiệu quả.
- **Current workaround:** Xem video YouTube và tự đối chiếu qua gương / quay video rồi xem lại / hỏi bạn có đi gym / chịu tập sai không biết.
- **Pain signal:** Đau cơ–khớp kéo dài sau buổi tập, không tiến bộ sau nhiều tháng, sợ hãi bỏ luôn không tập nữa.
- **Evidence / proxy evidence:** Tỷ lệ drop-out của người mới tập gym >60% trong 3 tháng đầu; các group Facebook "hội tập gym tại nhà" có hàng trăm post/ngày hỏi "động tác này đúng chưa?" kèm video.
- **Why underserved:** PT 1-1 quá đắt với segment này (~400–800k/buổi); YouTube/Instagram là one-way, không feedback cá nhân; app fitness hiện có (Nike Training, Keep) chỉ hướng dẫn chứ **không kiểm tra form**.

### Need #2
- **Statement (JTBD):** When tôi chỉ có 15–30 phút rảnh xen kẽ trong ngày, I want một buổi tập ngắn nhưng hiệu quả, so I can duy trì thói quen mà không phải đi lại tới gym.
- **Current workaround:** Bỏ buổi tập / lướt TikTok tìm video ngẫu nhiên / đi bộ quanh nhà.
- **Pain signal:** Không duy trì được lịch tập, cảm giác tội lỗi, thể lực giảm dần.
- **Evidence / proxy evidence:** Gym membership Việt Nam có retention rate 5–6 tháng là con số phổ biến; lý do hàng đầu để hủy là "không có thời gian đi".
- **Why underserved:** Gym yêu cầu di chuyển + thay đồ + chờ máy (~45 phút overhead); lớp học nhóm có giờ cố định; app hiện tại không tối ưu cho các lát cắt thời gian ngắn.

### Need #3 (optional)
- **Statement (JTBD):** When tôi đang cố cải thiện sức khỏe, I want thấy được tiến bộ đo lường được, so I can giữ động lực và biết mình đang đi đúng hướng.
- **Current workaround:** Ghi nhật ký thủ công / cân nặng / chụp ảnh before–after (nhưng đa số bỏ giữa chừng).
- **Pain signal:** Mất động lực sau 2–4 tuần vì "không thấy gì thay đổi".
- **Evidence / proxy evidence:** Apps habit-tracker có churn rate >70% trong tháng đầu; reviews tiêu cực về app fitness thường là "không biết mình có tiến bộ không".
- **Why underserved:** Self-tracking tốn công, dữ liệu chủ quan; chưa có app nào track được **chất lượng form** thay vì chỉ số lượng rep.

---

## 4. Strategy Statement

For **sinh viên và dân văn phòng Việt trẻ (18–30) muốn tập khỏe tại nhà**
who struggle with **không có PT để giám sát form và không đủ tiền/thời gian đến phòng gym**,
our product helps them **biết ngay động tác đúng/sai qua phản hồi real-time từ camera điện thoại, và tiến bộ đo lường được theo từng tuần**
through **computer-vision pose-detection on-device + lộ trình cá nhân hóa theo mục tiêu sức khỏe + feedback bằng tiếng Việt**,
unlike **YouTube/Instagram (một chiều, không feedback)** và **PT truyền thống (đắt, phải đặt lịch)** và **apps fitness quốc tế (không tracking form, không hiểu người Việt)**,
because we can leverage **(1) mô hình CV đã đủ chín chạy trên mid-range smartphone, (2) data network effect từ body-type người Việt, (3) chi phí phân phối thấp qua TikTok/ASO tại thị trường trẻ đang lên**.

---

## 5. Moat Hypothesis

**Moat mechanism:** Domain-learning flywheel trên dữ liệu form-correction của cơ thể người Việt.

If we deploy với **N = 10.000** người dùng active trong **thị trường fitness tại nhà ở Việt Nam**, the following improve:
1. **Độ chính xác pose-detection** cho tỷ lệ cơ thể người Việt (chiều cao, cấu trúc xương) tăng rõ rệt — data này các global player (Nike, Peloton, Apple Fitness+) không có vì họ tối ưu cho cơ thể Mỹ/Âu.
2. **Thư viện bài tập + cách sửa lỗi** mở rộng theo các lỗi phổ biến người Việt mới tập hay gặp (vd: squat bị cong lưng vì thói quen ngồi xổm, plank bị cong mông vì yếu core do ngồi nhiều).
3. **Ngôn ngữ & cách feedback** (tiếng Việt, tone phù hợp văn hóa) được tinh chỉnh qua retention signal — competitor nước ngoài dịch máy sẽ luôn thua.

**Why competitors cannot easily replicate this:**
> Global players không ưu tiên Việt Nam đủ sớm để thu đủ data tương tự; local players không có technical bar để làm CV + LLM feedback loop chất lượng; và data network effect có compound return — càng nhiều user thì model càng tốt, user lại càng retention → bên đến sau sẽ cần đốt nhiều tiền hơn chỉ để đuổi kịp chất lượng chứ chưa nói tới vượt.

---

## 6. Initial TAM / SAM / SOM view

| Layer | Estimate | Key assumptions | Confidence |
|---|---|---|---|
| TAM | ~$15–20B/năm (global at-home fitness apps) | Thị trường app fitness toàn cầu, bao gồm subscription + in-app purchase | medium |
| SAM | ~$100–180M/năm (Vietnam digital fitness 18–30) | ~3M urban young adults có smartphone + quan tâm sức khỏe × $3–5/tháng ARPU | low |
| SOM (12–24mo) | ~$500K–1.5M ARR | Chiếm 0.5–1% SAM, ~15–30k paid users × $40/năm | low |

**Top 3 unknowns requiring further research:**
1. **Willingness-to-pay thực tế** của segment sinh viên + office worker VN (freemium → paid conversion rate trên thị trường đã quen với "everything free on TikTok")
2. **Độ chính xác kỹ thuật** của pose-detection trên mid-range Android (~$200 phone) — nếu không chạy mượt thì segment sinh viên không dùng được
3. **Retention vs YouTube miễn phí** — liệu user có chịu trả tiền khi có hàng nghìn video miễn phí, dù không có feedback form?

**Judgment:**
- [ ] Worth pursuing now
- [x] Worth pursuing but not now (need to validate **độ chính xác pose-detection trên mobile VN + willingness-to-pay qua landing page test** first)
- [ ] Not worth pursuing as currently framed

---

## 7. Positioning Note (2 sentences)

**What we are:**
> Một AI Personal Trainer tiếng Việt trong điện thoại của bạn — giám sát form tập real-time qua camera và cá nhân hóa lộ trình, với chi phí bằng 1/20 của PT truyền thống.

**What we are not / not yet:**
> Chúng tôi không phải là app đếm rep hay social network fitness; chưa thay thế được PT cho các bài tập phức tạp với tạ nặng hoặc cho người đang có chấn thương cần phục hồi chức năng.

---

## 8. Self-assessment before Day 17

Trong 6 mắt xích (Idea • Customer • Need • Strategy • Moat • Market Size), mắt xích nào yếu nhất và vì sao?

> **Yếu nhất: Market Size (SAM/SOM) và Moat.**
> - **Market Size:** Con số $100–180M SAM đang là top-down estimation dựa trên giả định thô (3M users × $3–5/tháng). Chưa có bottom-up validation từ survey/landing page thực tế — không biết WTP thật sự là bao nhiêu, đặc biệt với sinh viên quen với content free trên TikTok.
> - **Moat:** "Data network effect" nghe hợp lý nhưng chưa rõ defensibility thực sự. Nếu Google MediaPipe / Apple Vision tiếp tục mở rộng model cho body types Đông Nam Á, phần technical của chúng tôi có nguy cơ bị commoditize. Cần rõ hơn moat nằm ở data, workflow, hay distribution.

Open questions chúng tôi muốn khám phá thêm ở Day 17:
1. Làm sao validate được **willingness-to-pay** của sinh viên + office worker VN với mức giá khả thi (29k? 49k? 99k/tháng?) — test bằng landing page kiểu Smoke Test?
2. Làm sao đo **độ chính xác pose-detection** mức độ "đủ tốt để thay thế PT cho người mới" — benchmark nào? Cần bao nhiêu labeled data để tin cậy?
3. Moat thật sự nằm ở đâu: data người Việt, workflow feedback-loop theo văn hóa, hay distribution qua TikTok creator economy? Nếu là distribution thì có defensibility không?
