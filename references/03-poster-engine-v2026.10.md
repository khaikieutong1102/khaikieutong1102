# REFERENCE 03 — POSTER ENGINE V2026.10 (FILE 02): CINEMATIC KEY ART

Nguồn chuẩn: "FILE 02 — Bước 2: Cinematic Key Art Poster Engine V2026.10 — Lean Output & Single Reference Edition".

## Triết lý tối thượng (luật nội bộ — không in ra màn hình)
Poster là MỘT KHOẢNH KHẮC ĐIỆN ẢNH khiến người xem dừng tay trong 0.3 giây: STOP SCROLLING → CURIOSITY → CLICK. Người xem phải thấy "Chuyện gì vừa xảy ra?", không phải "Tôi hiểu hết rồi".

## Cách làm
- Trợ lý TỰ RENDER poster bằng công cụ ảnh (mặc định của Workflow v3.2), dùng ảnh Sheet/DNA của nhân vật làm tham chiếu.
- Nếu render trực tiếp thất bại 1 lần: thử lại bằng một bố cục/khoảnh khắc KHÁC hẳn (đảo hướng, đổi tiền cảnh–hậu cảnh, đổi cảm xúc sang tươi sáng), giữ nguyên mọi luật cứng dưới đây. Chỉ khi không render được mới xuất khối lệnh để người dùng tự render trên Web UI (chọn khung 9:16 trước khi dán).
- Đầu ra khi phải xuất khối lệnh: CHỈ 2 phần — (1) MỘT code block duy nhất chứa poster prompt; (2) "Lời dặn dò của Em gái" tối đa 3–5 gạch đầu dòng ngắn.

## Luật cứng trong prompt
1. **Single Reference Lock:** khai báo `Character: TEN_KHONG_DAU @imageX` ĐÚNG 1 LẦN ở phần đầu. Trong SCENE, TITLE EVENT, WORLD ALIVENESS về sau CHỈ dùng TÊN — tuyệt đối không lặp lại @imageX.
2. **3 lớp kể chuyện + Artifact Anchor:**
   - FOREGROUND: extreme macro close-up của đạo cụ chủ chốt (Artifact Anchor) pushed right against the camera lens, hiệu ứng 3D pop-out, chiếm 30–40% khung dưới.
   - MIDGROUND: nhân vật chính + quyết định/hành động (chỉ dùng tên).
   - BACKGROUND: bối cảnh + phản ứng + ánh sáng chiều sâu. Nhìn 1 giây đọc được: ai – vượt qua gì – kết quả gì.
3. **Story Event Typography (Anti-Font Lock):** title KHÔNG BAO GIỜ là font, không phải text overlay, không trông giống font. Title là HIỆN TƯỢNG VẬT LÝ SỐNG tạo từ chính chất liệu đạo cụ trong kịch bản (hơi súp, cánh hoa, giọt nước, bụi phấn, khói, ánh sáng…). Bắt buộc đủ 5 phần:
   Story Event → Physical Event → Material Source → Transformation → Typography Integration.
   Title 3–7 từ, dạng hook, không spoil twist; chiếm 15–20% chiều cao poster, đặt ở 1/3 khung trên, không che mặt nhân vật; đọc rõ trong 0.5 giây trên điện thoại. Bỏ title đi, poster vẫn hợp lý; đổi góc máy 1 giây sau, title tan biến.
4. **Micro Realism:** với live-action dùng khóa da người thật (lỗ chân lông, subsurface scattering, không waxy/plastic). Với hoạt hình: thay bằng khóa chi tiết của phong cách phim (nét vẽ sạch, mắt sống có catchlight, chi tiết chất liệu) và giữ nguyên Style Lock của phim — KHÔNG ép khóa photoreal vào poster hoạt hình.
5. **Lighting** điện ảnh hợp vibe. **Negative** bắt buộc có anti-font: no floating digital font, no graphic text overlay, no typography plaque, no font-like letters, no watermark, no facial drift, no dark underexposure, no horizontal landscape crop (+ no Pixar/no photorealism nếu là hoạt hình; no anime/no cartoon nếu là live-action).
6. **Quality Lock:** Movie Art Key first · Artifact First (macro foreground) · 3-layer depth storytelling · 9:16 vertical locked · high CTR emotional discovery.

## Khung khối lệnh (điền nội dung kịch bản vào)
```
[POSTER PROMPT — {TEN PHIM} — FORMAT 9:16, 2K]
Character: {TEN_KHONG_DAU} @image1.
Character: {TEN_KHONG_DAU} @image2.
{Cinematic key art poster line theo phong cách phim}, 9:16 vertical format, 2K masterpiece.
SCENE (3-LAYER STORY):
FOREGROUND: Extreme macro close-up pushed right against the camera lens of {đạo cụ chủ chốt}, {chi tiết chất liệu}, dramatic 3D pop-out effect.
MIDGROUND: {TÊN} {hành động + biểu cảm}; {TÊN} {hành động + biểu cảm}.
BACKGROUND: {bối cảnh}, {ánh sáng chiều sâu}.
WORLD ALIVENESS: {hiệu ứng sống động từ chất liệu kịch bản}.
TITLE EVENT:
Story event: {sự kiện câu chuyện}.
Physical event: {hiện tượng vật lý}.
Material source: {chất liệu từ kịch bản}.
Transformation: {chất liệu xếp thành chữ "{TITLE}"}.
Typography integration: the title is a living physical event, absolutely NOT a font, NOT a text overlay; removing the text leaves the scene complete; occupies 15-20 percent of poster height in the upper third, never covering any face.
{MICRO DETAIL / MICRO REALISM LOCK theo phong cách phim}
{STYLE LOCK của phim — với live-action: Visual Style của v3.2}
LIGHTING: {ánh sáng điện ảnh hợp vibe}.
NEGATIVE: {anti-font + các cấm theo phong cách}.
QUALITY LOCK: Movie Art Key first, extreme macro foreground anchor, material formation typography, title belongs to the physical world, 3-layer depth storytelling, 9:16 vertical locked, 2K masterpiece, high CTR emotional discovery.
```

## Checklist tự soát trước khi xuất
Movie Art Key First · Artifact First (Macro Foreground) · Single Reference Lock (không lặp @imageX) · Story Event Typography (Anti-Font) · Title 3–7 từ thuộc về thế giới của phim · 3 lớp kể được kịch bản · Mobile Readability · 9:16 · Khóa chi tiết đúng phong cách phim · Dấu tiếng Việt của title đúng (nếu title có dấu).
