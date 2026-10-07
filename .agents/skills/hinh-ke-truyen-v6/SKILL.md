---
name: hinh-ke-truyen-v6
description: Tạo video kể chuyện/tài liệu bằng tiếng Việt từ một chủ đề ngắn; tự nghiên cứu và kiểm chứng khi cần, phát triển câu chuyện theo giai đoạn, mặc định 15–20 cảnh, mỗi cảnh là một ảnh riêng, giữ Visual Lock/Character Lock nhất quán, tạo image prompt, motion prompt, voice direction, SRT, sound design, thumbnail, JSON và hướng dẫn CapCut. Ưu tiên dùng khi yêu cầu bắt đầu bằng "$hinh ke truyen".
---

# Hình Kể Truyện V6

## Trigger

`$hinh ke truyen <chủ đề>`

Ví dụ:
- `$hinh ke truyen Bí ẩn kim tự tháp`
- `$hinh ke truyen Cuộc đời Napoleon --youtube 20 hinh`
- `$hinh ke truyen Mona Lisa --tiktok`
- `$hinh ke truyen Bí ẩn kim tự tháp --youtube json`

Không bắt người dùng lặp lại workflow. Tự triển khai toàn bộ quy trình.

## Mặc định

- Ngôn ngữ nội dung/lời dẫn: tiếng Việt.
- Prompt tạo ảnh/video: tiếng Anh.
- Số cảnh: 15–20.
- Mỗi cảnh = 1 ảnh riêng = 1 file riêng.
- Standard/YouTube: mặc định 16:9.
- TikTok/Shorts: mặc định 9:16.
- Phong cách mặc định: cinematic living-history collage / archival documentary aesthetic.
- Không chèn chữ, logo, watermark vào ảnh trừ khi người dùng yêu cầu.

## Quy tắc ưu tiên cao: một cảnh = một ảnh

Tuyệt đối không tạo:
- contact sheet
- storyboard nhiều ô
- grid
- split screen
- multi-panel layout
- một ảnh chứa nhiều khoảnh khắc

Mọi image prompt phải chứa:
`single-scene composition, one moment only, one image, no storyboard, no grid, no split screen, no multi-panel layout`

Nếu cần 20 cảnh thì mục tiêu là 20 file ảnh riêng.

## Fact-check

Với lịch sử, khoa học, chính trị, nhân vật/sự kiện thật:
- kiểm tra mốc thời gian, địa danh, tên người, chức danh, công nghệ, trang phục, quan hệ nhân quả;
- phân biệt: đã xác nhận / còn tranh luận / chưa đủ bằng chứng / phần tái dựng;
- không biến giả thuyết, truyền thuyết hay thuyết âm mưu thành sự thật;
- không dùng chi tiết hấp dẫn nhưng sai chỉ để tăng kịch tính.

Đọc `references/fact-check.md`.

## Cấu trúc câu chuyện

Tự chọn khung phù hợp.

### Nhân vật / tiểu sử
Hook → bối cảnh → xuất thân → bước ngoặt → vươn lên → thử thách → đỉnh cao → biến cố → suy tàn/thay đổi → hệ quả → những năm cuối → di sản → tranh cãi/bí ẩn.

### Công trình / bí ẩn / sự kiện
Hook → tổng quan → bối cảnh lịch sử → ai liên quan → quá trình hình thành → cấu trúc → thách thức → điều khác thường → phát hiện 1 → phát hiện 2 → điều biết chắc → điều chưa rõ → giả thuyết phổ biến → giả thuyết đáng tin hơn → ý nghĩa → kết luận mở.

Mỗi cảnh phải đóng góp thông tin hoặc cảm xúc mới; không kéo dài chỉ để đủ số lượng.

## Character Lock / Subject Lock

Nếu có nhân vật:
- tuổi theo giai đoạn
- cấu trúc khuôn mặt
- tóc
- vóc dáng
- trang phục/phụ kiện
- nét nhận diện không đổi

Nếu là công trình/địa điểm:
- kiến trúc
- vật liệu
- hình khối
- tông màu
- chi tiết nhận diện
- môi trường xung quanh

Khi nhân vật già đi, thay đổi tuổi có kiểm soát nhưng giữ nhận diện.

## Visual Lock bắt buộc

Tạo trước kịch bản chi tiết và lặp trong mọi image prompt:
- Aspect ratio
- Visual style
- Color palette
- Lighting
- Lens feeling
- Texture
- Composition
- Layout restrictions
- Text restrictions

Preset mặc định:
- style: cinematic living-history collage
- palette: warm sand, sepia, dark brown, muted gold
- lighting: dramatic documentary lighting
- lens: 35mm hoặc 50mm cinematic
- texture: aged paper, archival print, subtle halftone
- composition: single-scene only
- restrictions: no storyboard, no grid, no split screen, no text, no logo, no watermark

Đọc `references/visual-style.md`.

## Tên file tự động

Mỗi ảnh dùng:
`NN-ten-canh.png`

Ví dụ:
- `01-mo-dau-kim-tu-thap.png`
- `02-boi-canh-giza.png`
- `03-pharaoh-khufu.png`

Thumbnail:
`thumbnail-ten-du-an.png`

## Reference chaining

Nếu công cụ hỗ trợ reference image:
1. Tạo ảnh đầu tiên thật chuẩn.
2. Dùng ảnh đầu làm reference cho các ảnh tiếp theo.
3. Có thể dùng thêm 1–3 ảnh gần nhất nếu hữu ích.
4. Giữ ổn định phong cách, tông màu, nhận diện, ánh sáng và mức chi tiết.

## Platform modes

### --youtube
- 16:9
- 2–10 phút
- kể sâu hơn
- thumbnail riêng
- có thể vượt 20 cảnh nếu người dùng yêu cầu video dài

### --shorts
- 9:16
- khoảng 30–60 giây
- hook trong 1–2 giây đầu
- cảnh ngắn 2–5 giây

### --tiktok
- 9:16
- khoảng 30–90 giây
- hook ngay đầu
- nhịp nhanh, chủ thể rõ ở trung tâm

### --standard
- 16:9
- 15–20 cảnh
- khoảng 2–4 phút

Nếu người dùng nói nền tảng bằng ngôn ngữ tự nhiên, tự chọn mode.

## Timeline

Mỗi cảnh bắt buộc có:
- thời lượng
- start time
- end time

Gợi ý lời dẫn:
- 5–6 giây: 12–18 từ
- 7–8 giây: 16–26 từ
- 9–10 giây: 22–32 từ

Hook/cao trào/kết có thể dài hơn cảnh chuyển tiếp.

## Mỗi cảnh phải xuất

- Số cảnh
- Giai đoạn
- Tên file ảnh
- Start/end/duration
- Mục đích
- Hình ảnh chính
- Lời dẫn tiếng Việt
- Voice cue
- Nhịp cảm xúc
- Ambience/SFX
- Chuyển cảnh
- Image prompt (EN)
- Video motion prompt (EN)

### Image prompt
Phải độc lập, có subject, action, historical context, composition, lighting, lens, Visual Lock và negative constraints.

### Video motion prompt
Mô tả:
- chuyển động nhân vật/chủ thể
- chuyển động môi trường
- chuyển động máy quay
- tốc độ
- cảm giác điện ảnh

## AI Voice Direction

Xuất:
- giọng đọc gợi ý
- tính chất giọng
- tốc độ
- cảm xúc
- nhịp nghỉ
- cách nhấn
- voice prompt tổng
- voice cue từng cảnh khi cần

## SRT

Sau lời dẫn, xuất phụ đề SRT:
- timestamp khớp timeline
- câu ngắn, dễ đọc
- có thể tách 2 câu trong một cảnh thành nhiều cue

## Thumbnail Engine

Xuất:
1. thumbnail concept
2. thumbnail prompt (EN)
3. 2–3 headline tiếng Việt ngắn

Quy tắc:
- 1 chủ thể chính
- 1 yếu tố gây tò mò
- tương phản rõ
- dễ đọc trên màn hình nhỏ
- chừa vùng cho chữ hậu kỳ
- không tự chèn chữ vào ảnh nếu chưa được yêu cầu

## Music & Sound Design

### Music Direction
- mood
- tempo
- instrumentation
- intensity curve
- điểm tăng/giảm
- music prompt (EN)

### Sound Design Plan
Theo cảnh khi phù hợp:
- ambience
- foley
- impact
- transition sound
- silence/pause

Không để âm thanh lấn lời dẫn.

## JSON Project Manifest

Khi người dùng nói `json`, `prompt json`, hoặc `xuat json`, xuất JSON hợp lệ theo `references/json-project-manifest.md`.

Phải có:
- project_title
- topic
- platform_mode
- aspect_ratio
- total_duration_seconds
- visual_lock
- character_or_subject_lock
- voice_direction
- music_direction
- scenes[]

Mỗi scene gồm:
- scene_number
- filename
- start_time
- end_time
- duration_seconds
- stage
- narration_vi
- image_prompt_en
- video_motion_prompt_en
- sound_effects
- transition
- voice_cue

Không comment, không trailing comma.

## CapCut workflow

Cuối dự án, nếu phù hợp, hướng dẫn:
1. tạo project
2. import ảnh theo tên file
3. căn timeline
4. thêm AI voice
5. thêm nhạc nền
6. thêm SFX
7. import SRT
8. thêm transition
9. pan/zoom nhẹ cho ảnh tĩnh
10. export đúng nền tảng

## Kiểm tra cuối

- đúng số cảnh
- mỗi cảnh là một ảnh riêng
- không có cảnh lặp ý
- timeline khớp narration/SRT
- Character/Subject Lock nhất quán
- Visual Lock nhất quán
- fact-check không bị khẳng định quá mức
- motion prompt phù hợp thời lượng
- output đúng platform

Dùng cấu trúc trong `templates/output-template.md`.
