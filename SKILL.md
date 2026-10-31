# Khải Kiều Tổng 1102 — Sản Xuất Phim & Hoạt Hình AI (KKHome AI)

> Phiên bản: v1.0 — 31/10/2026 — bản đầu tiên, đã kiểm chứng qua dự án thật "Đánh Giá Một Sao" (series Bếp Của Mochi, Tim Của Nami, kênh @bunnychefglobalai).
> SKILL này gộp 4 quy trình đã chốt của KKHome AI thành một dây chuyền duy nhất:
> (1) Workflow Phim Khải Kiều v3.2 (nền tảng mọi loại phim) · (2) Hướng dẫn Hoạt hình AI YouTube 2027 (Style Lock + Character Sheet) · (3) Poster Engine V2026.10 (File 02) · (4) SEO & Revenue Engine V2026.25 (File 03).

## SKILL này dùng khi nào

Dùng khi người dùng muốn làm một phim ngắn hoặc phim hoạt hình AI trọn gói — từ ý tưởng/VIBE đến phim hoàn chỉnh có poster và gói SEO để đăng YouTube/TikTok — theo chuẩn KKHome AI. Ưu tiên số 1: **độ liền mạch của thước phim**.

## Đầu vào — chỉ hỏi đúng 3 thứ

1. **Số phân cảnh** (mỗi scene 10 giây — ví dụ 8 scenes).
2. **Tên kênh** (dùng cho SEO & branding).
3. **Mô tả phim** hoặc **link YouTube** để rút VIBE (bối cảnh, cảm xúc, nhịp kể).

Nhận đủ 3 thứ → làm MỘT LÈO không hỏi lại giữa chừng: nhân vật → kịch bản → poster → SEO → render → ráp → giao. (Trừ khi người dùng dặn dừng ở một bước.)

## Quy trình 9 bước

### Bước 1 — Chốt phong cách (Style Lock) — chỉ với hoạt hình
- Chọn ĐÚNG MỘT phong cách cho cả phim và viết thành MỘT dòng Style Lock, dán nguyên văn vào mọi prompt ảnh và video. Mẫu dòng khóa và 4 phong cách xem `references/02-hoat-hinh-2027.md`.
- 4 phong cách được phép: **2D Cartoon · 3D Cartoon (mềm, hiện đại) · Comic Book · Anime**.
- **LUẬT CỨNG: TUYỆT ĐỐI KHÔNG dùng 3D Pixar Style.** Luôn ghi rõ trong prompt: `No 3D, no Pixar look`.
- Với phim người thật (live-action), bỏ qua bước này và dùng Visual Style thực tế của Workflow v3.2.

### Bước 2 — Khóa nhân vật (Character Sheet / Character DNA)
- KHÔNG dùng ảnh mẫu. Nhân vật do trợ lý tự sinh.
- Hoạt hình: tạo **Character Sheet 4 góc** trên nền xám trung tính — [1] toàn thân mặt trước, [2] toàn thân mặt sau, [3] cận mặt trước (đầu và vai), [4] cận nghiêng trái 90°. Xem mẫu lệnh ở `references/02-hoat-hinh-2027.md`.
- Live-action: tạo ảnh **Character DNA full-body** theo Workflow v3.2 (xem `references/01-workflow-phim-v3.2.md`).
- **LUẬT CỨNG — KHÔNG MÔ TẢ LẠI NHÂN VẬT:** ảnh Sheet/DNA là NGUỒN SỰ THẬT DUY NHẤT về ngoại hình. Mọi prompt sau CHỈ gán tag ảnh (IMAGE 1, IMAGE 2 / @image1, @image2), không mô tả lại mặt, tóc, dáng, trang phục. Ngoại lệ duy nhất: cụm nhận dạng ngắn 3–5 từ (ví dụ: "thỏ khăn bếp đỏ") để neo thoại.
- Mỗi nhân vật có **Voice DNA** riêng (giới tính, tuổi, miền giọng, timbre) và phải LẶP lại công thức giọng ngắn tại MỖI câu thoại.

### Bước 3 — Viết kịch bản full (Luật 3 Beats Sống v3.2)
- Mọi scene 10s BẮT BUỘC **3 beats, mỗi beat đều có diễn + thoại**:
  Beat 1 [Mở]: A diễn + 1 câu 8–12 từ → Beat 2 [Đáp]: B diễn + 1 câu 8–12 từ → Beat 3 [Đất diễn]: A/B diễn mạnh + 1 câu chốt ≤10 từ.
- CẤM scene "1 câu thoại + câm dài". Mỗi beat tối đa 20 từ thoại. **Tối đa 2 người nói/scene** (người còn lại khóa im lặng: môi khép, không nhép); cảnh 3+ người cần thoại thì TÁCH thành 2 scenes nối tiếp.
- Mỗi lần đổi lượt nói: **0.5s im lặng** (người trước khép miệng hẳn) + camera **GLIDES SMOOTHLY** sang người tiếp. CẤM từ "CUT"/"CUTS TO" trong prompt.
- Cấu trúc prompt scene đầy đủ (khóa camera, khóa âm thanh, chống nhầm thoại 5 luật): xem `references/01-workflow-phim-v3.2.md`.
- Hoạt hình: thêm **AUDIO LOCK** — cùng giọng, cùng nhạc nền, cùng hiệu ứng âm thanh mọi scene.
- Thoại đúng ngôn ngữ người dùng chốt (mặc định tiếng Việt, thuần Việt, không lẫn tiếng Anh).

### Bước 4 — Poster (theo File 02 — Poster Engine V2026.10)
- Trợ lý TỰ RENDER poster 9:16 bằng công cụ ảnh, dùng ảnh Sheet/DNA làm tham chiếu. Cấu trúc và luật cứng xem `references/03-poster-engine-v2026.10.md`. Điểm cốt lõi:
  - **Single Reference Lock:** khai báo `Character: TEN @imageX` đúng 1 lần ở đầu prompt; sau đó chỉ dùng TÊN.
  - **3 lớp kể chuyện:** Foreground = đạo cụ chủ chốt (Artifact Anchor) macro đập vào ống kính, hiệu ứng 3D pop-out, chiếm 30–40% khung dưới · Midground = nhân vật chính + hành động · Background = bối cảnh + ánh sáng chiều sâu.
  - **Title Event (Anti-Font):** title 3–7 từ là HIỆN TƯỢNG VẬT LÝ SỐNG từ chất liệu của kịch bản (hơi súp, cánh hoa, giọt nước…), đủ 5 phần Story → Physical → Material → Transformation → Integration; title chiếm 15–20% chiều cao, đặt ở 1/3 khung trên, không che mặt nhân vật; TUYỆT ĐỐI không phải font, không phải text overlay.
  - Nếu render trực tiếp thất bại 1 lần: thử lại bằng một bố cục khác hẳn (đổi khoảnh khắc/bố cục, giữ nguyên các luật trên). Chỉ khi không render được mới xuất khối lệnh poster để người dùng tự render trên Web UI.
- Phong cách poster phải khớp phong cách phim (hoạt hình thì khóa theo Style Lock của phim, không dùng khóa da người thật).

### Bước 5 — SEO (theo File 03 — SEO & Revenue Engine V2026.25)
Xuất ĐÚNG 5 khối theo thứ tự, không thêm khối — chi tiết ở `references/04-seo-engine-v2026.25.md`:
1. 3 tiêu đề mobile high-CTR (hook bùng nổ nhất nằm trong 65 ký tự đầu, tối đa 1–2 hashtag cuối tiêu đề).
2. Mô tả đa tầng tự nhiên: dòng Series → 3 hashtag → Hook & Story Overview (từ khóa lồng vào văn xuôi, KHÔNG liệt kê topics thô) → Retention Anchor → Timeline dạng mồi tò mò (curiosity gap) → Thông báo minh bạch AI ở cuối phần tiếng Việt → English Description (chỉ dịch Story Overview + Retention Anchor).
3. Pinned comment kích hoạt thuật toán (câu hỏi mở).
4. Bộ tag SEO lean — một dòng duy nhất.
5. Tên file gốc chuẩn algo (snake_case + từ khóa + 1080P).

### Bước 6 — Render scenes
- Render bằng công cụ media của Muse (đường mặc định). Mỗi scene render từ **frame cuối của scene trước + ảnh Sheet/DNA** (tham chiếu kép); scene 1 render từ ảnh nhân vật. Lấy frame cuối bằng ffmpeg: `ffmpeg -sseof -0.3 -i sceneN.mp4 -vframes 1 lastN.png`.
- Trước khi render video hoạt hình: duyệt **keyframe** — mặt, trang phục, tỉ lệ, style phải đúng sheet. Keyframe sai thì sửa keyframe, không render video.
- Hoạt hình: mỗi shot chỉ **một chuyển động camera duy nhất** (trừ cú glide đổi người nói theo luật ping-pong).
- **Giới hạn: tối đa 6 video / 1 lượt tin nhắn.** Phim nhiều hơn 6 scenes thì chia lượt render, ráp sau khi đủ.
- Kiểm tra từng scene sau render: `ffprobe` phải đúng **10.0s**.

### Bước 7 — CTA ở scene cuối (luật cứng)
- 3 giây cuối của scene cuối: hiện icon **Like (hình ngón tay cái)** và icon **Đăng Ký (hình chuông)** cùng một icon/đạo cụ **chế tác từ chất liệu kịch bản** (ví dụ: củ cà rốt bằng hơi súp), ở góc trên bên phải, bake thẳng trong prompt render.
- **Chỉ mô tả icon bằng HÌNH DẠNG.** TUYỆT ĐỐI không viết các từ "Like"/"Subscribe" trong prompt (model sẽ vẽ chữ/nút lên phim).
- **TUYỆT ĐỐI không để phụ đề/chữ chạy trên video.**

### Bước 8 — Ráp phim + QC bắt buộc
- Upscale mỗi scene 720x1280 → **1080x1920** bằng ffmpeg lanczos:
  `ffmpeg -i sceneN.mp4 -vf "scale=1080:1920:flags=lanczos" -c:v libx264 -preset medium -crf 18 -c:a aac sceneN_1080.mp4`
- Ráp bằng crossfade hình + tiếng **0.5s**. Thời lượng phim cuối = **N×10 − (N−1)×0.5 giây** (8 scenes = 76.5s). Ngắn hơn tổng scenes là ĐÚNG công thức, không phải lỗi.
- QC checklist (không đạt thì sửa trước khi giao):
  1. Từng scene đúng 10.0s (ffprobe); phim cuối đúng công thức thời lượng và đúng 1080x1920.
  2. Frame HOOK (giây 5): đúng bối cảnh + nhân vật, vào thẳng hành động.
  3. Frame CTA (3s cuối): icon thuần hình dạng, KHÔNG có chữ; không có phụ đề ở bất kỳ frame nào.
  4. Mặt, tóc, trang phục nhân vật nhất quán mọi scene (so với Sheet/DNA); style không lệch (nếu lệch: quay lại sheet + dòng Style Lock, render lại shot lỗi — không mô tả thêm).
  5. Mỗi scene đủ 3 beats có diễn + thoại; tối đa 2 người nói/scene; người không nói môi khép.
  6. Poster: title là hiện tượng vật lý từ chất liệu kịch bản, không phải font; mặt đúng Sheet/DNA.
  7. Nhắc người dùng tự nghe kiểm chứng giọng thoại (trợ lý không nghe được audio mình tạo).

### Bước 9 — Giao phim
- Upload **file gốc** lên Google Drive (nếu đã kết nối) và gửi **link Drive** để tải nhanh; đồng thời nêu tên file + điểm khác biệt so với bản trước (nếu có).
- Kèm gói đính kèm: kịch bản full, khối/nội dung poster, gói SEO 5 khối.

## Bộ lệnh ngắn
Xem `references/bo-lenh-ngan.md` — câu lệnh mở đầu, câu nạp SKILL, và các lệnh tắt cho từng bước.

## Dự án mẫu đã kiểm chứng
`references/05-du-an-mau-mochi-nami.md` — toàn bộ thông số, kịch bản rút gọn và kết quả QC của tập pilot "Đánh Giá Một Sao". Dùng làm bản chuẩn để đối chiếu khi kiểm chứng SKILL ở New Chat mới (Bước 3 của quy trình đóng gói).

## Lưu ý bản quyền & an toàn gói SKILL
- KHÔNG đưa mật khẩu, token, khóa API vào bất kỳ file nào của SKILL.
- SKILL chỉ chứa quy trình và mẫu lệnh; dữ liệu riêng của từng người dùng (kênh, nhân vật) do người dùng cung cấp khi chạy.
