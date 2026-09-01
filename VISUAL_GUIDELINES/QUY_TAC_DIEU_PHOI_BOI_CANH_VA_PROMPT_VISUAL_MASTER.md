# 🇻🇳 ĐẠI QUY TẮC ĐIỀU PHỐI BỐI CẢNH & CẨM NANG KỸ THUẬT TẠO PROMPT VISUAL CỔ PHONG ĐẠI VIỆT (V5.0 MASTER)
## (TỰ ĐỘNG NHẬN DIỆN BỐI CẢNH · NẠP KHÍ GIỚI, PHƯƠNG TIỆN, ĐÁM ĐÔNG, QUÂN TA & QUÂN ĐỊCH)
### CHỦ TRÌ BIÊN SOẠN: SUBAGENT SYLVIA (VISUAL DIRECTOR), SỬ QUAN LÊ VĂN & TIỂU THUYẾT GIA VŨ DẠ KHÁCH
### HỆ THỐNG: `MUSIC OS` · QUY CHUẨN ALIBABA WAN 2.7 PRO & GOOGLE VEO 3.1

---

## 🏛️ I. QUY TRÌNH 4 BƯỚC CỦA SUBAGENT KHI NHẬN LỆNH TẠO ẢNH VISUAL:

Khi người dùng yêu cầu tạo ảnh/video với một bối cảnh bất kỳ, **Subagent BẮT BUỘC thực hiện tuần tự 4 bước sau**:

```
[ BƯỚC 1: NHẬN DIỆN BỐI CẢNH ] ──► [ BƯỚC 2: TRA CỨU MA TRẬN KHÍ GIỚI/NHÂN SỰ ]
              │                                                │
              ▼                                                ▼
[ BƯỚC 4: RENDER WAN PRO 4K ]  ◄── [ BƯỚC 3: GHÉP CẤU TRÚC PROMPT 5 KHỐI ]
```

1. **Bước 1 (Nhận diện bối cảnh):** Phân loại yêu cầu của User vào 1 trong **7 Bối Cảnh Lớn**.
2. **Bước 2 (Tra cứu ma trận & Nạp dữ liệu thực chứng):** Lấy đúng loại phương tiện, binh chủng, trang phục quần thể, vũ khí tương ứng từ bảng tra cứu.
3. **Bước 3 (Ghép cấu trúc Prompt 5 khối chuẩn Wan Pro):** Đảm bảo độ dài 80-100 từ tiếng Anh, có câu neo khóa nhận diện nhân vật, khóa giải phẫu và không sinh chữ rác.
4. **Bước 4 (Khởi tạo kết xuất & Hậu kiểm Vision):** Render ảnh 4K đúng tỷ lệ (`16:9` Concept/Thumbnail, `1:1` Album Cover, `9:16` TikTok) và kiểm tra thị giác trước khi gửi cho User.

---

## 🗺️ II. MA TRẬN ĐIỀU PHỐI 7 BỐI CẢNH LỚN (CONTEXT DISPATCH MATRIX):

```
┌──────────────────────────────────┬────────────────────────────────────────────────────────────────────────────────────────┐
│ 🏞️ BỐI CẢNH NỀN (ENVIRONMENT)   │ ⚔️ PHƯƠNG TIỆN, KHÍ GIỚI, QUẦN THỂ & BINH CHỦNG BẮT BUỘC NẠP KÈM:                     │
├──────────────────────────────────┼────────────────────────────────────────────────────────────────────────────────────────┤
│ 1. 🌊 **SÔNG NƯỚC / THỦY CHIẾN**  │ • **Phương tiện:** Đại Chiến Hạm Mông Đồng 100 tay chèo mũi Rồng đồng, Lâu Thuyền      │
│    *(Bạch Đằng, Lục Đầu Giang)*  │   3 tầng ngói vảy cá, Thuyền đinh cọc sắt đâm va, Thuyền nan vỏ trấu lướt đầm lầy.     │
│                                  │ • **Quân Ta:** Thủy binh mình trần xăm Giao Long, giáp da trâu, đoản đao lá lúa, cờ đỏ │
│                                  │   thêu hai chữ "SÁT THÁT".                                                             │
│                                  │ • **Bối cảnh nền:** Bãi cọc lim Bạch Đằng nhô giữa dòng sương mù, xác tàu địch bốc cháy│
├──────────────────────────────────┼────────────────────────────────────────────────────────────────────────────────────────┤
│ 2. 🐘 **SA TRƯỜNG ĐẠI CHIẾN**    │ • **Binh chủng:** **TƯỢNG BINH HAI BÀ TRƯNG** (Chiến tượng ngà bịt đồng, bành gỗ      │
│    *(Đồng bằng, Lãng Bạc)*       │   nghiến 2 tầng lợp da trâu chở Nữ tướng & Thần Nỗ, Trống Đồng Đông Sơn gióng lệnh).   │
│                                  │ • **Bộ binh:** Rừng trường thương búp sen tầm vông, khiên mây bện sơn ta mặt hổ phù đỏ│
│                                  │ • **Quân Địch:** Kỵ binh Nguyên Mông giáp sắt nặng đen, áo lông sói, cờ đuôi ngựa đen. │
├──────────────────────────────────┼────────────────────────────────────────────────────────────────────────────────────────┤
│ 3. 🐆 **RỪNG SÂU & HẺM NÚI CỔ** │ • **Binh chủng:** **THÚ BINH BÁCH VIỆT** (Ngự thú sư mình trần xăm linh thú điều khiển │
│    *(Phong Châu, Yên Tử, Mộc)*   │   bầy Hổ xám, Sói đen rừng già, Vượn thần; tù và vỏ ốc biển; nỏ ngụy trang rêu rừng). │
│                                  │ • **Bối cảnh nền:** Rừng đại ngàn nghìn năm, thác nước đổ, sương mù huyền ảo.          │
├──────────────────────────────────┼────────────────────────────────────────────────────────────────────────────────────────┤
│ 4. 🐎 **ĐỒI NÚI & THUNG LŨNG**   │ • **Phương tiện & Kỵ binh:** **Thiết Kỵ Phù Đổng** (Giáp phiến đồng đúc, mũ đồng chim │
│    *(Chi Lăng, Vạn Kiếp)*        │   Lạc ngù đỏ, giáo tre ngà 3.5m, ngựa núi bọc giáp ngực da trâu, kỵ xạ bắn tên ngược). │
│                                  │ • **Trận địa:** Bẫy chông gỗ lim vót nhọn cắm đầm lầy, vạn tiễn tề phát từ vách đá.    │
├──────────────────────────────────┼────────────────────────────────────────────────────────────────────────────────────────┤
│ 5. 🏮 **PHỐ MINH HƯƠNG / CHỢ LỚN**│ • **Quần thể & Thế lực:** Quý tộc Tống — Minh tị nạn, Thương nhân Minh Hương mặc áo    │
│    *(Nông Nại Đại Phố, Gia Định)*│   gấm xẻ tà đính nút vải, quạt trầm hương, ngọc bội; Thương thuyền viễn dương ba cột.   │
│                                  │ • **Kiến trúc:** Nhà phố mái ngói âm dương, đèn lồng đỏ, biển hiệu sơn then thếp vàng, │
│                                  │   hội quán cột gỗ gõ đỏ, khói hương trầm vòng nghi ngút.                               │
├──────────────────────────────────┼────────────────────────────────────────────────────────────────────────────────────────┤
│ 6. 🏺 **LÀNG NGHỀ GỐM & NÔNG THÔN**│ • **Đạo cụ & Nội thất:** Bàn xoay gốm lim đạp chân, ấm đất nung da lươn bốc khói,     │
│    *(Chu Đậu, Bát Tràng)*        │   chõng tre mộc, bát men ngọc, lò nung gạch cổ đỏ lửa, mái ngói vảy cá bám rêu.        │
│                                  │ • **Người dân:** Nghệ nhân nam áo cộc nâu thô, nữ mặc áo Tứ Thân/Giao Lĩnh men ngọc.    │
├──────────────────────────────────┼────────────────────────────────────────────────────────────────────────────────────────┤
│ 7. 👑 **HOÀNG THÀNH THĂNG LONG**  │ • **Cung đình & Cấm vệ:** Cung điện mái ngói mũi hài đầu đao lá đề, Cấm Vệ Kim Ngô   │
│    *(Đoan Môn, Điện Kính Thiên)* │   giáp phiến sắt mạ vàng, Kiếm Liễu chuôi sen, đèn lồng hoa sen đêm rằm hoa đăng.      │
└──────────────────────────────────┴────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 📝 III. CÔNG THỨC 5 KHỐI GHÉP PROMPT CHUẨN WAN PRO 4K:

$$\mathbf{Wan\ 4K\ Prompt} = \mathbf{Lens\ \&\ Format} + \mathbf{Character\ Lock} + \mathbf{Context\ Assets\ (Ma\ Trận)} + \mathbf{Opposing\ Forces\ /\ Civilians} + \mathbf{Pure\ Art\ Master}$$

* **Khối 1 (Format):** `Cinematic [16:9 / 1:1 / 9:16] 4k photograph, Hasselblad H6D-100c medium format, [50mm / 80mm] f/2.8 lens.`
* **Khối 2 (Character Lock):** `Keep EXACTLY the same face, identity, Vietnamese features and anatomical structure of [Moc Tinh Lan / An Thai] from reference image.`
* **Khối 3 (Context & Assets):** Mô tả hành động chính kết hợp phương tiện/khí giới tra cứu từ Ma trận mục II.
* **Khối 4 (Opposing Forces / Civilians):** Mô tả rõ rệt quân ta vs quân địch hoặc đám đông nghệ nhân xung quanh.
* **Khối 5 (Negative / Quality):** `High-contrast chiaroscuro lighting, volumetric atmosphere, NO TEXT, ZERO WORDS, NO LETTERS, no watermarks, museum quality masterpiece, 8k resolution.`

---

## 🤖 IV. HƯỚNG DẪN SUBAGENT NHẬN DIỆN & TỰ ĐỘNG THỰC THI:

1. **Subagent Sylvia (Fashion & Visual Director):** Chịu trách nhiệm chính về tạo hình, trang phục, bố cục 1/3 và kiểm tra tỷ lệ khung hình (`16:9`, `1:1`, `9:16`).
2. **Subagent Sử Quan Lê Văn:** Chịu trách nhiệm kiểm duyệt tính chính xác lịch sử của vũ khí, giáp trụ, cờ xí và phương tiện theo đúng niên đại Lý — Trần — Bách Việt.
3. **Subagent Bách Diệp (MV Screenplay Director):** Chuyển đổi các bối cảnh sa trường / phố thị thành 5-block prompt tự nhiên cho Google Veo 3.1.
