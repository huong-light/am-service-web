# AM Service & Technology — Brain Document

> File này là “đầu não” định hướng cho code, website, AI Agent, marketing, sản phẩm và chiến lược phát triển AM Service & Technology.

---

## 0. Thương hiệu đã chốt

### Công ty / thương hiệu chính

**AM Service & Technology**

### Tên miền

**amservice.vn**

### Email chính

**admin@amservice.vn**

### Màu nhận diện website

Phong cách: **Dark Red Minimal**

- Nền tối hơn
- Chữ trắng gần như toàn bộ
- Đỏ mờ chỉ dùng cho điểm nhấn
- Không dùng xanh/tím neon rực
- Không làm kiểu startup màu mè
- Cảm giác: trầm, chắc, kỹ thuật, tinh tế

Bảng màu gợi ý:

```text
Nền chính:        #090606
Nền section:      #120808
Card:             #1A0B0B
Card hover:       #241010
Viền mờ:          #3A1717
Đỏ chính:         #7A1E1E
Đỏ nhấn:          #A83232
Đỏ sáng nhẹ:      #C94A4A
Chữ chính:        #FFFFFF
Chữ phụ:          #FFFFFF hoặc trắng giảm opacity
```

---

## 1. Tầm nhìn AM

AM Service & Technology không chỉ bán đèn hay chatbot.

AM xây **giải pháp tự động hóa ánh sáng và show-control cho không gian nhỏ và vừa**.

Câu định vị chính:

> **Giải pháp tự động hóa ánh sáng cho không gian nhỏ và vừa.**

Câu hero website:

> **Bật MA3 lên, hệ thống sẵn sàng. Người dùng chỉ cần chọn cảm xúc, ánh sáng và visual chạy theo kịch bản.**

Câu ngắn để giải thích:

> **AI ra lệnh. MA3 chạy show. Đèn đổi cảm xúc.**

---

## 2. Chiến lược phát triển tổng thể

Thứ tự phát triển đã chốt:

```text
Demo thật
→ Video thật
→ Khách thử nghiệm thật
→ Quy trình thật
→ Rồi mới lập công ty
```

Hiện tại chưa ưu tiên lập công ty, chưa ưu tiên hợp tác đại lý, chưa ưu tiên ôm hàng.

Ưu tiên trước mắt:

```text
1. Xây website AM
2. Xây demo concept
3. Xây AM Small Venue Auto Show Kit
4. Làm video chứng minh
5. Gom khách thử nghiệm
6. Sau này mới tính hợp tác / đại lý / doanh số
```

---

## 3. Khách hàng mục tiêu giai đoạn đầu

AM nhắm vào môi trường nhỏ và vừa trước:

```text
1. Hội trường nhỏ
2. Phòng đào tạo
3. Nhà thờ / nhóm ca nhạc hàng tuần
4. Trung tâm workshop
5. Phòng livestream / studio nhỏ
6. Sân khấu mini
7. Trường học / phòng sinh hoạt đa năng
```

Lý do:

```text
- Dễ triển khai hơn dự án lớn
- Nhu cầu rõ: bật lên là chạy
- Người vận hành không cần chuyên sâu MA3
- Dễ làm demo, dễ quay video
- Dễ tạo case study đầu tiên
```

---

## 4. Sản phẩm lõi đầu tiên

# AM Small Venue Auto Show Kit

Mô tả:

> Giải pháp tự động hóa ánh sáng cho hội trường nhỏ và vừa. Khi khởi động hệ thống, grandMA3 tự nạp showfile, AM Agent tự kết nối, Web UI sẵn sàng, giáo viên hoặc MC chỉ cần chọn mood để điều khiển ánh sáng và visual.

Cốt lõi:

```text
MA3 là show control chính
AM Agent là lớp giao tiếp
AM Launcher là lớp tự khởi động
DMX/MA hardware là hạ tầng output
Resolume là visual/pixel server tùy gói
```

---

## 5. Nguyên tắc kỹ thuật quan trọng

### AM không để AI bắn DMX trực tiếp

AI không được tự điều khiển DMX lung tung.

Luồng đúng:

```text
Người dùng / Giáo viên / MC
→ AM Web Control / AM Teacher Agent
→ gọi Macro/Cue an toàn trong MA3
→ MA3 xử lý showfile
→ DMX Node / MA hardware xuất tín hiệu
→ Đèn chạy
```

Nguyên tắc:

```text
AI chỉ chọn mood / section / macro
MA3 giữ toàn bộ show logic
MA3 showfile là sản phẩm lõi
```

---

## 6. Kiến trúc hệ thống tổng thể

```text
Teacher / MC / Operator
        ↓
AM Web Control / AM Teacher Agent
        ↓
grandMA3 onPC / MA3 Console
        ↓
MA hardware / DMX Node / DMX-key / viz-key
        ↓
Lighting / Audience Light / Stage Light

grandMA3
        ↓
Resolume Server
        ↓
Pixel / LED / Visual

Vectorworks
        ↓
Depence
        ↓
Demo thiết kế trước khi triển khai
```

---

## 7. Phân cấp sản phẩm theo phần cứng MA

### 7.1 AM Micro Demo Kit

Dành cho:

```text
- Demo
- Phòng rất nhỏ
- Lớp học nhỏ
- Test concept
- Depence / Visualizer
```

Phần cứng:

```text
grandMA3 viz-key
```

Vai trò:

```text
512 parameters onboard
phù hợp demo nhỏ và training
```

---

### 7.2 AM Small Venue Kit

Dành cho:

```text
- Hội trường nhỏ
- Phòng đào tạo
- Nhà thờ nhỏ
- Sân khấu mini
- Weekly show nhỏ
```

Phần cứng:

```text
grandMA3 onPC 2Port Node 2k
```

Vai trò:

```text
2,048 parameters
2 DMX outputs
phù hợp gói bán đầu tiên
```

---

### 7.3 AM Performance Venue Kit

Dành cho:

```text
- Hội trường vừa
- Trung tâm đào tạo
- Nhà thờ có band
- Sân khấu có nhiều moving light
- Có Resolume pixel/visual
```

Phần cứng:

```text
grandMA3 onPC DMX-key 4096
hoặc
grandMA3 onPC Node 4k
```

Vai trò:

```text
4,096 parameters
phù hợp hệ biểu diễn vừa
```

---

## 8. Auto Startup — điểm khác biệt sản phẩm

Mục tiêu:

```text
Bật máy
→ mở grandMA3 onPC
→ tự load showfile AM
→ mở AM Agent
→ Agent tự kết nối MA3
→ mở Web UI
→ hệ thống báo Ready
```

Không để khách phải:

```text
- mở showfile tay
- nhập IP tay
- set OSC tay
- load layout tay
- tìm macro tay
```

### 8.1 AM Launcher

AM Launcher là app nhỏ chạy khi Windows khởi động.

Nhiệm vụ:

```text
1. Start grandMA3 onPC với đúng showfile
2. Start AM Teacher Agent
3. Start Resolume nếu có
4. Check network
5. Check MA3 OSC
6. Check DMX Node
7. Open Web UI
8. Show Ready screen
```

Folder gợi ý:

```text
AM_Auto_Show_Kit/
├── AM_Launcher.exe
├── config/
│   ├── startup.json
│   ├── network.json
│   ├── ma3.json
│   ├── resolume.json
│   └── safety.json
├── showfiles/
│   └── AM_SmallVenue_AutoShow.show
├── agent/
├── logs/
└── backup/
```

### 8.2 Startup config mẫu

```json
{
  "ma3": {
    "enabled": true,
    "path": "C:/Program Files/MALightingTechnology/gma3/bin/app_system.exe",
    "hosttype": "onPC",
    "showfile": "AM_SmallVenue_AutoShow.show",
    "ip": "192.168.10.20",
    "osc_port": 8000,
    "init_macro": 100
  },
  "agent": {
    "enabled": true,
    "host": "192.168.10.10",
    "port": 8088
  },
  "resolume": {
    "enabled": false,
    "path": "C:/Program Files/Resolume Arena/Arena.exe",
    "ip": "192.168.10.40"
  },
  "network": {
    "required_devices": [
      "192.168.10.20",
      "192.168.10.30"
    ]
  }
}
```

---

## 9. MA3 Showfile Template

MA3 showfile là lõi.

### 9.1 Sequence chính

```text
Sequence 101 - Venue Mood Master
```

Cue:

```text
Cue 1  - Neutral
Cue 2  - Focus
Cue 3  - Deep
Cue 4  - Inspiring
Cue 5  - Energy
Cue 6  - Demo
Cue 7  - Q&A
Cue 8  - Practice
Cue 9  - Ending
Cue 10 - Safe Blackout
```

### 9.2 Macro chính

```text
Macro 100 - AM System Init

Macro 201 - Mood Neutral
Macro 202 - Mood Focus
Macro 203 - Mood Deep
Macro 204 - Mood Inspiring
Macro 205 - Mood Energy
Macro 206 - Mood Demo
Macro 207 - Mood Q&A
Macro 208 - Mood Practice
Macro 209 - Mood Ending
Macro 299 - Safe Blackout
```

Ví dụ command:

```text
Macro 201: Goto Cue 1 Sequence 101 Fade 2
Macro 202: Goto Cue 2 Sequence 101 Fade 2
Macro 203: Goto Cue 3 Sequence 101 Fade 5
Macro 204: Goto Cue 4 Sequence 101 Fade 4
Macro 207: Goto Cue 7 Sequence 101 Fade 2
Macro 299: Goto Cue 10 Sequence 101 Fade 1
```

### 9.3 Layout

```text
Layout 501 - Teacher Mood Control
Layout 502 - Tech Control
Layout 503 - AI Agent Status
Layout 504 - Safety / Emergency
```

---

## 10. Mood Preset cơ bản

### Neutral — giảng bình thường

```text
Front: 55%
Key: 50%
Back: 15%
Audience: 25%
Color: Warm White
Fade: 2s
```

### Focus — tập trung kiến thức

```text
Front: 45%
Key: 55%
Back: 10%
Audience: 10%
Color: Neutral White
Fade: 2s
```

### Deep — lắng đọng

```text
Front: 28%
Key: 38%
Back: 18%
Side: 12%
Audience: 5%
Color: Warm White + Amber + Deep Blue
Fade: 5s
```

### Inspiring — truyền cảm

```text
Front: 45%
Key: 55%
Back: 30%
Side: 18%
Audience: 15%
Color: Amber + Gold + Lavender
Fade: 4s
```

### Q&A — hỏi đáp

```text
Front: 60%
Audience: 45%
Back: 15%
Color: Warm White
Fade: 2s
```

### Ending — kết bài

```text
Front: 50%
Key: 55%
Back: 45%
Audience: 20%
Color: Gold / Amber
Fade: 4s
```

---

## 11. AM Teacher Agent

Nhiệm vụ:

```text
Người dùng gõ/chọn mood
→ Agent nhận diện ý định
→ map sang macro MA3
→ gửi lệnh an toàn
→ ghi log
```

Tên sản phẩm:

```text
AM Teacher Agent
AM Web Control
AM Emotion Control
```

Luật an toàn:

```text
AI không sửa patch
AI không store/merge/delete
AI không đổi network
AI không bắn DMX trực tiếp
AI chỉ gọi Macro whitelist
```

Whitelist:

```text
Go Macro 100
Go Macro 201
Go Macro 202
Go Macro 203
Go Macro 204
Go Macro 205
Go Macro 206
Go Macro 207
Go Macro 208
Go Macro 209
Go Macro 299
```

---

## 12. AM Website

### 12.1 Mục tiêu website v0.1

Website chưa cần dashboard, chưa cần app điều khiển thật.

Mục tiêu:

```text
1. Giới thiệu AM là ai
2. Giải thích giải pháp kỹ thuật nhỏ và vừa
3. Cho khách thấy demo / concept
4. Thu thông tin khách muốn thử nghiệm
```

### 12.2 Cấu trúc website

```text
Home
Solution
Packages
Demo
Workflow
Pilot / Contact
About
```

### 12.3 Nội dung Home

Hero:

```text
AM Service & Technology

Giải pháp tự động hóa ánh sáng
cho không gian nhỏ và vừa.

Bật MA3 lên, hệ thống sẵn sàng.
Người dùng chỉ cần chọn cảm xúc,
ánh sáng và visual chạy theo kịch bản.
```

CTA:

```text
Đăng ký demo
Xem giải pháp
```

### 12.4 Packages

```text
AM Micro Demo Kit
AM Small Venue Kit
AM Performance Venue Kit
```

### 12.5 Demo card

```text
Demo 01 — Auto Startup
Bật máy → mở MA3 → showfile tự sẵn sàng → AM báo Ready

Demo 02 — Mood Control
Chọn “Lắng đọng” → MA3 chạy Macro Deep → đèn đổi mood

Demo 03 — Q&A
Chọn “Hỏi đáp” → khán đài sáng lên

Demo 04 — Weekly Music
MA3 chạy cue ca nhạc → Resolume chạy pixel/visual
```

---

## 13. Prompt Claude Code build website

```text
Build a premium dark landing website for “AM Service & Technology”.

Language: Vietnamese.

Goal:
Create a marketing website for a technical solution company that provides automated lighting and show-control systems for small and medium venues.

Brand:
AM Service & Technology

Core message:
“Giải pháp tự động hóa ánh sáng cho không gian nhỏ và vừa.”
“Bật MA3 lên, hệ thống sẵn sàng. Người dùng chỉ cần chọn cảm xúc, ánh sáng và visual chạy theo kịch bản.”

Business direction:
AM sells technical solutions for small and medium environments first:
- small halls
- training rooms
- churches / weekly music groups
- mini stages
- livestream studios
- workshops
- small education/performance spaces

Technical architecture:
- grandMA3 onPC is the main show control system
- AM Web Control / AM Teacher Agent is the simple control layer
- MA hardware options: viz-key, onPC 2Port Node 2k, DMX-key 4096, Node 4k
- Resolume Server handles pixel and visual effects
- Vectorworks is used for design
- Depence is used for simulation/demo

Important principle:
AI does not directly send random DMX.
AM only calls safe macros/cues in the MA3 showfile.

Website style:
- Premium muted dark red minimal
- Very dark background
- All text white
- Subtle dark red accents only
- No electric blue
- No purple neon
- No flashy AI gradient
- Elegant, serious, technical, easy to read

Colors:
- main background: #090606
- section background: #120808
- card background: #1A0B0B
- card hover: #241010
- border: #3A1717
- primary red: #7A1E1E
- accent red: #A83232
- soft highlight red: #C94A4A
- main text: #FFFFFF
- secondary text: #FFFFFF with opacity

Pages:
1. Home
2. Solution
3. Packages
4. Demo
5. Workflow
6. Pilot / Contact
7. About

Home sections:
- Hero
- Problem
- Solution
- System Architecture
- Package Preview
- Auto Startup feature
- Mood Control example
- Weekly Music Show example
- CTA

Packages:
1. AM Micro Demo Kit
2. AM Small Venue Kit
3. AM Performance Venue Kit

CTA:
- “Đăng ký demo”
- “Gửi mặt bằng để tư vấn”
- “Xem giải pháp”

Return full Next.js + Tailwind CSS project code.
```

---

## 14. AM Advisor — Chatbot tư vấn

Tên chatbot tư vấn đã chốt:

# AM Advisor

Vai trò:

```text
Chatbot tư vấn khách hàng
Tư vấn gói Micro / Small / Performance
Hỏi thông tin hội trường
Gợi ý giải pháp
Chuyển lead về admin@amservice.vn
```

Câu mở đầu:

```text
Xin chào, tôi là AM Advisor.

Tôi sẽ giúp bạn chọn giải pháp tự động hóa ánh sáng phù hợp cho hội trường, phòng đào tạo, sân khấu mini hoặc chương trình ca nhạc hàng tuần.

Bạn muốn tư vấn theo không gian nào?
```

Cấu trúc tên hệ thống:

```text
AM Service & Technology
→ công ty

AM Advisor
→ chatbot tư vấn khách hàng

AM Teacher Agent
→ AI điều khiển mood qua MA3

AM Mail Agent
→ AI quản lý email

AM Social Agent
→ AI quản lý nội dung mạng xã hội
```

---

## 15. AM Mail Agent

### 15.1 Mục tiêu

```text
admin@amservice.vn
→ AI Agent đọc mail
→ phân loại
→ tóm tắt
→ soạn câu trả lời
→ mày duyệt
→ mới gửi
```

Giai đoạn đầu không cho AI tự gửi.

### 15.2 Mail categories

```text
DEMO_REQUEST
PROJECT_INQUIRY
QUOTE_REQUEST
SUPPORT
PARTNER
OTHER
```

### 15.3 Workflow

```text
Mail mới tới
↓
AI đọc tiêu đề + nội dung
↓
Phân loại
↓
Tóm tắt ngắn
↓
Đề xuất mức ưu tiên
↓
Soạn nháp trả lời
↓
Mày bấm Duyệt / Sửa / Không gửi
↓
Agent gửi mail
↓
Lưu log
```

### 15.4 Luật an toàn

```json
{
  "auto_send": false,
  "require_approval_before_send": true,
  "never_send_price_without_approval": true,
  "never_commit_delivery_date_without_approval": true,
  "never_sign_contract_by_ai": true,
  "never_share_internal_strategy": true,
  "allowed_sender_email": "admin@amservice.vn"
}
```

### 15.5 Train sau

Ban đầu Mail Agent chỉ dùng template/rule.

Sau này mày sẽ train bằng cách:

```text
1. AI soạn nháp
2. Mày sửa lại
3. Lưu bản AI + bản mày sửa
4. Agent học cách trả lời
```

Folder train:

```text
training_data/
├── approved_replies.jsonl
├── rejected_replies.jsonl
├── style_notes.md
└── faq_patterns.md
```

---

## 16. AM Content & Social Agent

Mục tiêu:

```text
Website
Email
Facebook
TikTok
YouTube
Zalo
LinkedIn
Instagram
Tất cả gom về một trung tâm quản lý nội dung
```

Nguyên tắc:

```text
AI soạn
mày duyệt
rồi mới đăng/gửi
```

### 16.1 Nền tảng

```text
Facebook
TikTok
YouTube
Zalo
LinkedIn
Instagram
Website blog
Email
```

### 16.2 Content pillars

```text
1. AM là gì?
2. Demo cảm xúc
3. Tự động hóa MA3
4. Weekly Show
5. Thiết kế và mô phỏng
```

### 16.3 Lịch đăng 30 ngày đầu

Tuần 1 — Ra mắt concept:

```text
Ngày 1: AM là gì?
Ngày 2: Website mockup Dark Red
Ngày 3: Bài giải thích “bật MA3 lên là sẵn sàng”
Ngày 4: Clip demo mood Deep
Ngày 5: Bài nói về khách nhỏ/vừa
Ngày 6: Clip Depence concept
Ngày 7: Tổng kết hướng AM
```

Tuần 2 — Demo mood:

```text
Mood Neutral
Mood Focus
Mood Deep
Mood Q&A
Mood Ending
So sánh trước/sau ánh sáng
```

Tuần 3 — Gói sản phẩm:

```text
AM Micro Demo Kit
AM Small Venue Kit
AM Performance Venue Kit
So sánh 512 / 2048 / 4096
Vì sao chọn theo quy mô
```

Tuần 4 — Tìm khách thử nghiệm:

```text
Đăng bài mời pilot
Gửi tin nhắn cho khách tiềm năng
Đăng video demo 3–5 phút
Mở form đăng ký demo trên website
Tổng hợp feedback
```

---

## 17. Phễu marketing

```text
Facebook / TikTok / YouTube
        ↓
Website amservice.vn
        ↓
Form đăng ký demo
        ↓
admin@amservice.vn
        ↓
AM Mail Agent phân loại
        ↓
Mày duyệt trả lời
        ↓
Hẹn demo / khảo sát
        ↓
Khách thử nghiệm
```

---

## 18. Marketing strategy

### 18.1 Mục tiêu

```text
1. Làm khách hiểu AM là gì
2. Tạo niềm tin bằng demo thật
3. Gom khách thử nghiệm
4. Xây dữ liệu nội dung cho AI Agent
5. Chuẩn bị nền để bán gói nhỏ-vừa
```

### 18.2 Kênh trung tâm

```text
Website: amservice.vn
Mail: admin@amservice.vn
```

### 18.3 Kênh social

```text
Facebook: xây uy tín ngành
TikTok: kéo reach nhanh
YouTube: chứa video demo dài
Zalo: chăm sóc khách Việt Nam
LinkedIn: B2B/đối tác
```

### 18.4 Video demo chính

Nội dung:

```text
1. Giới thiệu AM
2. Vấn đề: hội trường nhỏ khó vận hành ánh sáng
3. Giải pháp: bật MA3 lên là sẵn sàng
4. Demo: chọn mood → đèn đổi
5. Demo: weekly music show + Resolume pixel
6. Chốt: hệ thống offline, an toàn, dễ dùng
```

### 18.5 Chỉ số theo dõi

```text
1. Số người xem video
2. Số người vào website
3. Số form đăng ký demo
4. Số người nhắn hỏi
5. Số cuộc hẹn demo
6. Số khách thử nghiệm thật
```

---

## 19. Hợp tác ProAVL / MA / RGB — để sau

Hiện tại chưa tập trung hợp tác.

Nội bộ định hướng dài hạn:

```text
- ProAVL / AVL VN có thể nhập khẩu / phân phối chính hãng MA
- AM có thể trở thành đại lý/solution dealer cho phân khúc nhỏ-vừa
- Tập trung từ viz-key đến 4096 parameters trở xuống
- RGB System có thể là nguồn phần cứng DMX/RDM, dimmer, relay, power infrastructure
```

Nhưng giai đoạn hiện tại:

```text
KHÔNG đưa hợp tác lên website v0.1
KHÔNG nói AM là đại lý MA/RGB/ProAVL khi chưa có hợp đồng
KHÔNG chịu áp doanh số khi chưa có demo và khách thật
```

---

## 20. Cấu trúc AI Agent trong AM Platform

Ba agent đầu tiên:

```text
AM Teacher Agent
→ điều khiển mood ánh sáng qua MA3

AM Mail Agent
→ quản lý email

AM Content Social Agent
→ quản lý nội dung đa nền tảng
```

Cộng thêm chatbot:

```text
AM Advisor
→ tư vấn khách trên website
```

Tất cả gom thành:

# AM Platform

Giai đoạn đầu AI chỉ:

```text
soạn
lọc
nhắc
đề xuất
```

Mày vẫn duyệt cuối cùng.

---

## 21. Quy tắc thương hiệu và an toàn

### 21.1 Không nói quá

Không được nói:

```text
AM là đại lý chính thức của MA
AM là đối tác chính thức của RGB
AM thay thế MA3
AI điều khiển DMX trực tiếp
Hệ thống chạy 100% không cần setup
```

Khi chưa có pháp lý/hợp đồng, chỉ nói:

```text
AM phát triển giải pháp dựa trên grandMA3 onPC
AM dùng MA3 làm show control chính
AM Agent là lớp điều khiển đơn giản
```

### 21.2 Không báo giá cứng sớm

Website v0.1 không công bố giá cứng.

Chỉ ghi:

```text
Tư vấn theo quy mô không gian.
Có 3 gói: Micro / Small Venue / Performance Venue.
```

### 21.3 Không để AI tự quyết

```text
AI không tự gửi mail quan trọng
AI không tự đăng social
AI không tự cam kết giá
AI không tự cam kết thời gian
AI không tự ký hợp đồng
```

---

## 22. Việc làm tiếp theo

Thứ tự làm ngay:

```text
1. Mua amservice.vn
2. Tạo admin@amservice.vn
3. Build website AM v0.1
4. Tạo AM Advisor chatbot mockup
5. Build AM Mail Agent v0.1
6. Build AM Content Social Agent v0.1
7. Build MA3 Auto Showfile demo
8. Quay video demo thật
9. Tìm khách thử nghiệm
```

---

## 23. Tóm tắt ngắn cho coder

Nếu Claude Code hoặc dev cần hiểu nhanh:

```text
AM Service & Technology là thương hiệu bán giải pháp tự động hóa ánh sáng cho không gian nhỏ và vừa.

Sản phẩm đầu tiên là AM Small Venue Auto Show Kit.

Hệ thống dùng grandMA3 onPC làm show control chính. AM Agent không điều khiển DMX trực tiếp mà chỉ gọi macro/cue an toàn trong MA3. Các gói phần cứng chia theo quy mô: viz-key cho demo/siêu nhỏ, 2Port Node 2k cho nhỏ, DMX-key/Node 4k cho vừa.

Website dùng dark red minimal, chữ trắng, tên miền amservice.vn, email admin@amservice.vn.

Các AI Agent gồm:
- AM Advisor: chatbot tư vấn website
- AM Teacher Agent: điều khiển mood qua MA3
- AM Mail Agent: quản lý email, soạn nháp, chờ duyệt
- AM Content Social Agent: tạo nội dung Facebook/TikTok/YouTube/Zalo/Website, chờ duyệt

Ưu tiên hiện tại:
website trước, demo thật sau, khách thử nghiệm sau, rồi mới tính công ty/hợp tác.
```

---

# End of Brain Document
