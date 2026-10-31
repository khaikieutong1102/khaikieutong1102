# REFERENCE 01 — WORKFLOW PHIM KHẢI KIỀU v3.2 (RÚT GỌN ĐẦY ĐỦ LUẬT CỨNG)

Nguồn chuẩn: "Workflow Phim — Khải Kiều Home AI with Muse, bản 2026.10 v3.2". Đây là nền tảng cho MỌI loại phim trong SKILL này.

## Nguyên tắc cốt lõi
1. KHÔNG dùng ảnh mẫu. Nhân vật tự sinh bằng Character DNA Lock (live-action) hoặc Character Sheet (hoạt hình).
2. Độ liền mạch của thước phim là ưu tiên số 1.
3. Chế độ mặc định: làm TRỌN GÓI MỘT LÈO sau khi có đủ 3 đầu vào (số scenes, tên kênh, mô tả/link VIBE) — không dừng xin duyệt giữa chừng trừ khi được dặn riêng.
4. Giới hạn môi trường: tối đa 6 video / 1 lượt tin nhắn.

## Character DNA (live-action)
- Thứ tự ưu tiên: ETHNICITY → FACE GEOMETRY → HAIR → ACCESSORY → OUTFIT.
- 3 cấp: FULL (chính, ≥3 scenes) · MEDIUM (phụ quan trọng, ≥2 scenes) · COMPACT (khách, 1 scene).
- Ảnh DNA là FULL-BODY đầu đến chân, nền một màu liền. Dàn nhân vật linh hoạt 2–5 người/phim.
- LUẬT KHÔNG MÔ TẢ LẠI: từ khi có ảnh DNA, mọi prompt sau chỉ gán tag IMAGE X; không mô tả lại mặt/tóc/dáng/trang phục. Ngoại lệ: cụm nhận dạng ngắn 3–5 từ.

## Voice DNA
- Mẫu: `[TÊN]: [tuổi] y/o Vietnamese [MALE/FEMALE] voice, pure [giọng miền]. [timbre], clear natural articulation.`
- LẶP công thức giọng ngắn tại MỖI câu thoại theo format: `[TÊN] ([cụm nhận dạng]) — giọng [miền] [MALE/FEMALE] VOICE, [tuổi]y/o, [timbre] — SAYS: "[thoại]".`

## Scene prompt — các khối bắt buộc
1. [CHARACTER VISUAL LOCK] — tag ảnh tham chiếu, Sheet/DNA là nguồn sự thật duy nhất, medium shot, không zoom sát mặt.
2. [SPEAKER MAP] — gán tên ↔ IMAGE X + cụm nhận dạng 3–5 từ cho từng người nói.
3. [PING-PONG DIALOGUE v3.2] — camera LUÔN ở người đang nói; NEVER cut; camera GLIDES SMOOTHLY; nhịp im lặng 0.5s giữa mỗi lần đổi lượt (người trước khép miệng hẳn → camera lướt → người sau nói khi camera dừng hẳn); chỉ người được gọi tên mới nhép miệng; một giọng tại một thời điểm; two-shot chỉ dùng cho phản ứng câm.
4. [CHỐNG NHẦM THOẠI — 5 LUẬT] — (1) tối đa 2 người nói/scene, người còn lại khóa im lặng rõ ràng; (2) neo thoại bằng cụm nhận dạng vật lý 3–5 từ; (3) lặp Voice DNA tại mỗi câu; (4) cảnh 3+ người cần thoại → tách 2 scenes; (5) mỗi câu 8–12 từ (~2–3 giây nói tự nhiên), trần cứng 20 từ/beat.
5. [AUDIO VOICE DNA] + khóa âm thanh phòng thu: giọng tự nhiên, âm lượng trò chuyện thân mật, không hét, không rung méo, ambience dưới giọng nói.
6. [VIETNAMESE-ONLY SPEECH LOCK] khi thoại tiếng Việt: cấm lẫn tiếng Anh/phiên âm Anh; giữ nguyên giọng vùng miền từ scene đầu đến cuối.
7. [SMOOTH MOTION & PHYSICS] — chuyển động liên tục, không dịch chuyển tức thời, micro-movement tự nhiên khi nghe; động từ MẠNH cho hành động (brisk, energetic, decisive), từ "smooth" chỉ cho quỹ đạo/camera; tốc độ thực 1x, không slow-mo.
8. [CAMERA LOCK] — cảm giác tripod khóa cứng trên người nói, chỉ di chuyển bằng glide trong nhịp im lặng; không rung tay, không zoom kịch tính, không whip pan, không cắt cứng.
9. [CINEMATIC ENVIRONMENT LOCK] — một đoạn mô tả bối cảnh cố định (Lighting | Atmosphere | Space) dán nguyên văn mọi scene.
10. [SOUND DESIGN 3 LỚP] — Foreground (Foley) | Midground (thoại + hơi thở) | Background (ambience + nhạc).
11. [TIMELINE 3 BEATS SỐNG] — 00–03s Beat 1 Mở · 03–03.5s chuyển im lặng · 03.5–07s Beat 2 Đáp · 07–07.5s chuyển im lặng · 07.5–10s Beat 3 Đất diễn + câu chốt ≤10 từ. Beat 3 được câm tối đa 2.5s CHỈ khi là đất diễn có chủ ý (hành động diễn xuất rõ ràng).
12. [CONSISTENCY MASTER LOCK] + Negative: subtitles, watermark, text overlay, overlapping voices, voice swapping, wrong lip-sync, listener moving lips, hard cuts, jumpy camera, stiff motion, distorted hands, slow motion.

## CTA scene cuối
- 3s cuối scene cuối: icon/đạo cụ chế tác từ chất liệu kịch bản + pictogram ngón tay cái + pictogram chuông hiện ở góc trên bên phải. Mô tả icon BẰNG HÌNH DẠNG, tuyệt đối không viết tên nút ("Like"/"Subscribe") trong prompt. Không gọi thoại CTA, không chữ trên màn hình.

## Chuẩn kỹ thuật
- 9:16, 1080p (1080x1920), scene 10s tuyệt đối, tốc độ 1x. Ráp xfade + acrossfade 0.5s. Thời lượng cuối = N×10 − (N−1)×0.5s.
- Render thực tế 720x1280 → upscale lanczos lên 1080x1920 trước khi ráp.
- Không dùng CapCut; mọi xử lý bằng generation + ffmpeg. Không để model tự vẽ chữ/graphic lên phim.

## Bài học đã kiểm chứng
- Face drift: giảm bằng tham chiếu kép (frame cuối + ảnh neo mặt). Voice drift: siết bằng Voice DNA lặp tại mỗi câu.
- Trợ lý không nghe được audio mình tạo → luôn nhờ người dùng kiểm chứng giọng.
- Zoom sát mặt gây biến dạng → luôn khung trung cảnh. Mở đầu vào thẳng hành động từ frame 1.
