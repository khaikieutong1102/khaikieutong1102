# REFERENCE 02 — HOẠT HÌNH AI YOUTUBE 2027 (STYLE LOCK + CHARACTER SHEET)

Nguồn: "Hướng Dẫn Làm Hoạt Hình AI Trên YouTube 2027 — KKHome AI" (theo video "How To Start Making AI Animations in 2027", OpenArt + Seedance 2.5). Áp dụng đè lên nền Workflow v3.2 (Reference 01) cho các dự án hoạt hình.

## Bước 1 — Style Lock
Chọn MỘT phong cách cho cả video, viết thành một dòng chuẩn, dán Y NGUYÊN vào mọi lệnh tạo ảnh và video. Không trộn 2 phong cách trong 1 video.

4 phong cách được dùng:
- **2D Cartoon** — kể chuyện, nhân vật vui nhộn, nét phẳng, màu tươi.
- **3D Cartoon** — khối mềm, chuyển động mượt, hiện đại nhưng KHÔNG giống phim điện ảnh.
- **Comic Book** — viền đậm, màu mảng, giàu kịch tính.
- **Anime** — phong cách Nhật, mắt to, biểu cảm mạnh, màu điện ảnh.

**CẢNH BÁO: 3D Pixar Style BỊ LOẠI TRỪ — KHÔNG DÙNG.** Luôn ghi rõ trong mọi prompt là không dùng Pixar.

Mẫu dòng khóa (2D Cartoon):
```
STYLE LOCK: flat 2D cartoon style, bold clean outlines, flat colors, soft cel shading. Keep this exact style in every image and every shot. No 3D, no Pixar look, no photorealism.
```
Mẫu dòng khóa (Anime — đã kiểm chứng qua dự án Mochi & Nami):
```
STYLE LOCK: expressive Japanese anime style, clean line art, big emotive eyes, soft cel shading, cinematic warm colours, hand-painted backgrounds. Keep this exact style in every image and every shot. No 3D, no Pixar look, no photorealism.
```

Các biến thể mở rộng (vẫn khóa bằng cùng cơ chế Style Lock): Webtoon/Manhwa dọc, Chibi 2D, Storybook/Watercolor, Claymation, Paper Cut-out, Pixel Art, Whiteboard/Stickman.

## Bước 2 — Character Sheet 4 góc + gắn thẻ
Sheet là "chứng minh thư" của nhân vật: 4 góc nhìn của cùng một người, cùng trang phục, nền xám trung tính:
[1] Toàn thân mặt trước · [2] Toàn thân mặt sau · [3] Cận mặt trước (đầu và vai) · [4] Cận nghiêng trái 90°.

Mẫu lệnh:
```
Character reference sheet, four views on a plain neutral grey background: [1] full body front view, [2] full body rear view, [3] head-and-shoulders front close-up, [4] head-and-shoulders left profile. The same [CHARACTER: age, hair, build] wearing [FULL OUTFIT: every garment with colour and material]. Consistent face, hair, proportions and outfit across all four views. Locked style: [STYLE LINE]. No text, no watermark, no extra characters, no background environment.
```
Sau khi có sheet: lưu lại và GẮN THẺ (IMAGE 1, IMAGE 2…), gọi đúng thẻ trong mọi prompt sau — không mô tả lại nhân vật.

## Bước 3 — Keyframe khớp
Keyframe là ảnh tĩnh mở đầu (và kết thúc) của shot, tạo từ sheet + dòng Style Lock:
```
First frame for shot 1, using the character sheet as reference. [CHARACTER] is [ACTION / POSE] in [SETTING]. Same face, hair and outfit as the character sheet. Locked style: [STYLE LINE]. Wide shot, full body visible, eye-level camera. No text, no watermark.
```
Checklist trước khi làm chuyển động: Mặt đúng người trong sheet? · Trang phục đúng màu/phụ kiện? · Tỉ lệ cân đối? · Style đúng dòng khóa? — Chưa đạt thì sửa keyframe, KHÔNG render video.

## Bước 4 — Chuyển động (cấu trúc một shot)
```
SUBJECT: [CHARACTER] keeps the exact face, hair, outfit and proportions from the character sheet throughout the shot.
ACTION: 0-3s [first movement]; 3-6s [second movement]; 6-9s [closing movement]. Expressive acting: [emotion].
CAMERA: one slow push-in, eye-level, no cuts. (MỘT chuyển động camera duy nhất mỗi shot)
LIGHT: soft warm light from the left, steady all shot.
AUDIO: [ambience and sound effects].
EXCLUDE: text, logos, extra characters, style change.
```
Nhịp timeline chia 2–3s/nhịp, mỗi nhịp một hành động rõ — khớp với Luật 3 Beats Sống của v3.2. Render bản nháp ngắn kiểm tra trước khi render bản chính khi cần tiết kiệm lượt.

## Bước 5 — Audio Lock
```
AUDIO LOCK: the same warm female Vietnamese narration voice, the same background music bed, and matching sound effects in every shot. Same volume balance. No music change between shots.
```
(Sửa chất giọng theo Voice DNA của dự án; nguyên tắc là KHÓA một chất âm thanh cho cả phim.)

## Bước 6 — Sửa lệch style (style drift) + ráp
- Dấu hiệu drift: mặt tròn/méo dần, màu áo đổi tông, nét vẽ dày mỏng khác nhau giữa các shot.
- Cách sửa: quay lại keyframe + character sheet, dán lại dòng Style Lock, render lại shot lỗi. KHÔNG sửa bằng cách mô tả thêm (càng dài càng lệch).
- Ráp: xếp shots theo thứ tự câu chuyện, nối crossfade 0.5s, xem lại toàn bộ một lượt (mặt, đồ, màu, giọng, nhạc) trước khi đăng.

## Checklist cuối (trước khi đăng)
Style giống nhau mọi shot · Nhân vật đúng mặt/tóc/trang phục mọi shot · Keyframe đã duyệt trước khi render · Mỗi shot 1 chuyển động camera, timeline rõ · Âm thanh đồng nhất · Không shot nào dùng 3D Pixar Style · Không chữ lạ/logo lạ/nhân vật thừa.

## Lưu ý chính sách YouTube
YouTube có chính sách với nội dung không xác thực/rập khuôn sản xuất hàng loạt: mỗi video phải có câu chuyện, nhân vật và cách kể riêng — không đăng nhiều video giống hệt chỉ đổi tên nhân vật.
