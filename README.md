<h1 align="center">🎬 Pixelle-Video —— Công cụ tạo video ngắn AI tự động</h1>

<p align="center"><b>Tiếng Việt</b> | <a href="README_EN.md">English</a> | <a href="README_ZH.md">中文</a></p>

<p align="center">
  <a href="https://github.com/AIDC-AI/Pixelle-Video/releases" target="_blank"><img src="https://img.shields.io/badge/📦 Windows-50C878" alt="Gói Windows"></a>
  <a href="https://aidc-ai.github.io/Pixelle-Video" target="_blank"><img src="https://img.shields.io/badge/📘 Tài%20liệu-4A90E2" alt="Tài liệu"></a>
  <a href="https://github.com/AIDC-AI/Pixelle-Video/stargazers"><img src="https://img.shields.io/github/stars/AIDC-AI/Pixelle-Video.svg" alt="Stargazers"></a>
  <a href="https://github.com/AIDC-AI/Pixelle-Video/issues"><img src="https://img.shields.io/github/issues/AIDC-AI/Pixelle-Video.svg" alt="Issues"></a>
  <a href="https://github.com/AIDC-AI/Pixelle-Video/network/members"><img src="https://img.shields.io/github/forks/AIDC-AI/Pixelle-Video.svg" alt="Forks"></a>
  <a href="https://github.com/AIDC-AI/Pixelle-Video/blob/main/LICENSE"><img src="https://img.shields.io/github/license/AIDC-AI/Pixelle-Video.svg" alt="License"></a>
</p>

https://github.com/user-attachments/assets/a42e7457-fcc8-40da-83fc-784c45a8b95d

<br/>

Chỉ cần nhập một **chủ đề**, Pixelle-Video có thể tự động hoàn thành:

- ✍️ Viết kịch bản video
- 🎨 Tạo hình ảnh/video bằng AI
- 🗣️ Tổng hợp giọng đọc thuyết minh
- 🎵 Thêm nhạc nền
- 🎬 Ghép thành video chỉ với một lần bấm

**Không cần kinh nghiệm dựng video**, biến việc sáng tạo video thành thao tác nhập một câu.

## 🖥️ Xem trước giao diện Web

![Giao diện Web UI](resources/webui.png)

## 📋 Cập nhật gần đây

- ✅ **2026-01-26**: Thêm module “Chuyển động tác”, tải video tham chiếu và ảnh để chuyển động tác.
- ✅ **2026-01-14**: Thêm pipeline “Người số đọc thoại” và “Ảnh thành video”, hỗ trợ nhiều giọng TTS đa ngôn ngữ.
- ✅ **2026-01-06**: Hỗ trợ gọi máy RunningHub VRAM 48G.
- ✅ **2025-12-28**: Hỗ trợ cấu hình giới hạn chạy đồng thời RunningHub, tối ưu logic dữ liệu có cấu trúc trả về từ LLM.
- ✅ **2025-12-17**: Hỗ trợ cấu hình ComfyUI API Key, gọi model Nano Banana, API hỗ trợ tham số mẫu tùy chỉnh.
- ✅ **2025-12-10**: Thêm FAQ trong sidebar, khóa phiên bản edge-tts để sửa lỗi dịch vụ TTS không ổn định.
- ✅ **2025-12-08**: Hỗ trợ nhiều cách tách kịch bản cố định (đoạn/dòng/câu), tối ưu chọn mẫu và xem trước trực tiếp.
- ✅ **2025-12-06**: Sửa xử lý URL trả về của API tạo video, hỗ trợ đa nền tảng.
- ✅ **2025-12-05**: Thêm gói Windows all-in-one, tối ưu workflow phân tích ảnh và video.
- ✅ **2025-12-04**: Thêm tính năng “Media tùy chỉnh”, cho phép tải ảnh/video riêng và để AI phân tích tạo kịch bản.
- ✅ **2025-11-18**: Tối ưu RunningHub chạy song song, thêm trang lịch sử, hỗ trợ tạo video hàng loạt.

## ✨ Tính năng nổi bật

- ✅ **Tạo tự động hoàn toàn** - Nhập chủ đề, tự động tạo video hoàn chỉnh.
- ✅ **Viết kịch bản bằng AI** - AI tạo lời dẫn theo chủ đề, không cần tự viết script.
- ✅ **Tạo ảnh bằng AI** - Mỗi câu có thể đi kèm minh họa AI đẹp mắt.
- ✅ **Tạo video bằng AI** - Hỗ trợ các model tạo video AI như WAN 2.1 để tạo nội dung động.
- ✅ **Tạo giọng đọc bằng AI** - Hỗ trợ Edge-TTS, Index-TTS và nhiều giải pháp TTS phổ biến.
- ✅ **Nhạc nền** - Thêm BGM để video có không khí hơn.
- ✅ **Phong cách hình ảnh** - Nhiều mẫu để tạo phong cách video riêng.
- ✅ **Kích thước linh hoạt** - Hỗ trợ video dọc, ngang và nhiều tỉ lệ khác.
- ✅ **Nhiều model AI** - Hỗ trợ GPT, Qwen, DeepSeek, Ollama và các LLM tương thích OpenAI.
- ✅ **Ghép nối năng lực linh hoạt** - Dựa trên kiến trúc ComfyUI, dùng workflow có sẵn hoặc tự tùy biến từng năng lực như đổi model tạo ảnh sang FLUX, đổi TTS sang ChatTTS, v.v.

## 📊 Quy trình tạo video

Pixelle-Video dùng thiết kế module hóa, quy trình tạo video rõ ràng:

![Sơ đồ quy trình tạo video](resources/flow.png)

Từ văn bản đầu vào đến video cuối cùng: **Tạo kịch bản → Lập kế hoạch hình ảnh → Xử lý từng khung → Ghép video**.

Mỗi bước đều có thể tùy chỉnh linh hoạt: chọn model AI, engine âm thanh, phong cách hình ảnh, template video, v.v.

## 🎬 Ví dụ video

Dưới đây là một số video được tạo bằng Pixelle-Video, thể hiện nhiều chủ đề và phong cách khác nhau.

### 📱 Module mở rộng

<table>
<tr>
<td width="33%">
<h3>👤 Người số đọc thoại</h3>
<video src="https://github.com/user-attachments/assets/7c122563-c2e0-4dcd-a73c-25ba1d4fa2dd" controls width="100%"></video>
<p align="center"><b>Người số đọc tiếng Hàn</b></p>
</td>
<td width="33%">
<h3>🖼️ Ảnh thành video</h3>
<video src="https://github.com/user-attachments/assets/5b4eef17-07d0-4bde-9748-2ed68cc9888e" controls width="100%"></video>
<p align="center"><b>Video hoạt hình</b></p>
</td>
<td width="33%">
<h3>💃 Chuyển động tác</h3>
<video src="https://github.com/user-attachments/assets/7b1240bc-e965-434c-b343-118ec4793d4f" controls width="100%"></video>
<p align="center"><b>Mèo con nhảy múa</b></p>
</td>
</tr>
</table>

### 📱 Video dọc

<table>
<tr>
<td width="33%">
<h3>🌄 Phóng sự đời sống - Mẫu mặc định</h3>
<video src="https://github.com/user-attachments/assets/e6716c1d-78de-453d-84c2-10873c8c595f" controls width="100%"></video>
<p align="center"><b>Phong cảnh trên hành trình</b></p>
</td>
<td width="33%">
<h3>🔍 Giải mã văn hóa - Mẫu mặc định</h3>
<video src="https://github.com/user-attachments/assets/f5de75f6-135a-4ab4-9f5f-079f649764d5" controls width="100%"></video>
<p align="center"><b>Santa ID</b></p>
</td>
<td width="33%">
<h3>🔭 Tư duy khoa học - Mẫu mặc định</h3>
<video src="https://github.com/user-attachments/assets/ceb8b0df-8331-4e1f-88e7-db5b295a1c1d" controls width="100%"></video>
<p align="center"><b>Vì sao chúng ta chưa tìm thấy văn minh ngoài hành tinh?</b></p>
</td>
</tr>
<tr>
<td width="33%">
<h3>🌱 Phát triển bản thân - Clone giọng</h3>
<video src="https://github.com/user-attachments/assets/1bad9a49-df83-4905-9cc8-9a7640e9c7d8" controls width="100%"></video>
<p align="center"><b>Cách nâng cấp bản thân</b></p>
</td>
<td width="33%">
<h3>🧠 Tư duy sâu - Mẫu mặc định</h3>
<video src="https://github.com/user-attachments/assets/663b705a-2aea-44bc-b266-4bb27aa255a8" controls width="100%"></video>
<p align="center"><b>Hiểu về phản mong manh</b></p>
</td>
<td width="33%">
<h3>🏯 Lịch sử văn hóa - Khung tĩnh</h3>
<video src="https://github.com/user-attachments/assets/56e0a018-fa99-47eb-a97f-fc2fa8915724" controls width="100%"></video>
<p align="center"><b>Tư trị thông giám</b></p>
</td>
</tr>
<tr>
<td width="33%">
<h3>☀️ Cảm xúc - Clone giọng</h3>
<video src="https://github.com/user-attachments/assets/4687df95-dd21-4a7b-b01e-f33a7b646644" controls width="100%"></video>
<p align="center"><b>Nắng ấm mùa đông</b></p>
</td>
<td width="33%">
<h3>📜 Kể chuyện tiểu thuyết - Kịch bản tự viết</h3>
<video src="https://github.com/user-attachments/assets/d354465e-3fa8-40b4-93e9-61ad75ef0697" controls width="100%"></video>
<p align="center"><b>Đấu phá thương khung</b></p>
</td>
<td width="33%">
<h3>🧬 Kiến thức phổ thông - Tạo ảnh Qwen</h3>
<video src="https://github.com/user-attachments/assets/8ac21768-41ce-4d41-acdd-e3dd3eb9725a" controls width="100%"></video>
<p align="center"><b>Kiến thức dưỡng sinh</b></p>
</td>
</tr>
</table>

### 🖥️ Video ngang

<table>
<tr>
<td width="50%">
<h3>💰 Kiếm tiền từ nghề tay trái - Mẫu điện ảnh</h3>
<video src="https://github.com/user-attachments/assets/c9209d4e-73a6-4b82-aaad-cf102248c9e2" controls width="100%"></video>
<p align="center"><b>Kiếm tiền từ nghề tay trái</b></p>
</td>
<td width="50%">
<h3>🏛️ Bình luận lịch sử - Mẫu tùy chỉnh</h3>
<video src="https://github.com/user-attachments/assets/a767c452-d5f1-4cff-bb34-b80fff0d4c3e" controls width="100%"></video>
<p align="center"><b>Gợi mở từ Tư trị thông giám</b></p>
</td>
</tr>
</table>

> 💡 **Mẹo**: Các video trên đều được AI tạo tự động chỉ từ một từ khóa/chủ đề, không cần kinh nghiệm dựng video.

<div id="tutorial-start" />

## 🚀 Bắt đầu nhanh

### 🪟 Gói Windows all-in-one (khuyên dùng cho Windows)

**Không cần cài Python, uv hoặc ffmpeg — giải nén là dùng.**

👉 **[Tải gói Windows all-in-one](https://github.com/AIDC-AI/Pixelle-Video/releases/latest)**

1. Tải gói Windows all-in-one mới nhất và giải nén.
2. Nhấp đúp `start.bat` để mở giao diện Web.
3. Trình duyệt sẽ tự mở http://localhost:8501.
4. Trong “⚙️ Cấu hình hệ thống”, cấu hình LLM API và dịch vụ tạo ảnh.
5. Bắt đầu tạo video.

> 💡 **Mẹo**: Gói này đã kèm mọi dependency. Lần đầu dùng chỉ cần cấu hình API key.

### Cài từ source (cho macOS / Linux hoặc người cần tùy biến)

#### Yêu cầu trước khi cài

Cần cài trình quản lý package Python `uv` và công cụ xử lý video `ffmpeg`.

##### Cài uv

Xem hướng dẫn phù hợp với hệ điều hành tại tài liệu chính thức của uv:  
👉 **[Hướng dẫn cài uv](https://docs.astral.sh/uv/getting-started/installation/)**

Sau khi cài, chạy `uv --version` trong terminal để kiểm tra.

##### Cài ffmpeg

**macOS**
```bash
brew install ffmpeg
```

**Ubuntu / Debian**
```bash
sudo apt update
sudo apt install ffmpeg
```

**Windows**
- Tải tại: https://ffmpeg.org/download.html
- Giải nén và thêm thư mục `bin` vào biến môi trường PATH.

Sau khi cài, chạy `ffmpeg -version` để kiểm tra.

#### Bước 1: Tải dự án

```bash
git clone https://github.com/namlevia/Pixelle-Video.git
cd Pixelle-Video
```

#### Bước 2: Mở giao diện Web

```bash
uv run streamlit run web/app.py
```

Trình duyệt sẽ tự mở http://localhost:8501.

#### Bước 3: Cấu hình trong Web UI

Lần đầu sử dụng, mở panel “⚙️ Cấu hình hệ thống” và điền:

- **Cấu hình LLM**: Chọn model AI như Qwen, GPT, DeepSeek, Ollama... và nhập API Key.
- **Cấu hình hình ảnh**: Nếu cần tạo ảnh, cấu hình địa chỉ ComfyUI hoặc RunningHub API Key.

Sau khi cấu hình xong, bấm “Lưu cấu hình” để bắt đầu tạo video.

<div id="tutorial-end" />

## 💻 Cách sử dụng

Sau khi mở Web UI, bạn sẽ thấy bố cục ba cột.

### ⚙️ Cấu hình hệ thống (bắt buộc lần đầu)

#### 1. Cấu hình LLM

LLM dùng để tạo kịch bản video.

**Chọn preset nhanh**

- Chọn model preset từ menu như Qwen, GPT-4o, DeepSeek...
- Sau khi chọn, `base_url` và `model` sẽ tự điền.
- Bấm link “🔑 Lấy API Key” để đăng ký và lấy key.

**Cấu hình thủ công**

- API Key: nhập key của bạn.
- Base URL: địa chỉ API.
- Model: tên model.

#### 2. Cấu hình hình ảnh

Dùng để tạo ảnh minh họa/video bằng AI.

**Triển khai cục bộ (khuyên dùng)**

- ComfyUI URL: địa chỉ ComfyUI cục bộ, mặc định `http://127.0.0.1:8188`.
- Bấm “Kiểm tra kết nối” để xác nhận dịch vụ hoạt động.

**Triển khai cloud**

- RunningHub API Key: key cho dịch vụ tạo ảnh cloud.

### 📝 Nhập nội dung (cột trái)

#### Chế độ tạo

- **AI tạo nội dung**: Nhập chủ đề, AI tự viết kịch bản.
  - Phù hợp khi muốn tạo nhanh và để AI viết lời.
  - Ví dụ: “Vì sao nên xây dựng thói quen đọc sách”.
- **Nội dung kịch bản cố định**: Nhập trực tiếp kịch bản hoàn chỉnh, bỏ qua bước AI viết.
  - Phù hợp khi đã có sẵn nội dung.

#### Nhạc nền (BGM)

- **Không dùng BGM**: Chỉ có giọng đọc.
- **Nhạc có sẵn**: Chọn nhạc nền preset như `default.mp3`.
- **Nhạc tùy chỉnh**: Đặt file MP3/WAV vào thư mục `bgm/`.
- Bấm “Nghe thử BGM” để nghe trước.

### 🎤 Cài đặt giọng đọc (cột giữa)

#### Workflow TTS

- Chọn workflow TTS từ menu (Edge-TTS, Index-TTS, v.v.).
- Hệ thống tự quét workflow TTS trong thư mục `workflows/`.
- Nếu biết ComfyUI, bạn có thể tự tạo workflow TTS.

#### Âm thanh tham chiếu (tùy chọn)

- Tải file âm thanh lên để clone giọng (MP3/WAV/FLAC...).
- Chỉ áp dụng cho workflow hỗ trợ clone giọng như Index-TTS.
- Có thể nghe thử sau khi tải lên.

#### Xem trước

- Nhập văn bản thử và bấm “Xem trước giọng” để nghe.
- Hỗ trợ dùng âm thanh tham chiếu khi xem trước.

### 🎨 Cài đặt hình ảnh (cột giữa)

#### Tạo hình ảnh/video

Quyết định AI tạo hình minh họa/video theo phong cách nào.

**Workflow ComfyUI**

- Chọn workflow tạo ảnh/video từ menu.
- Hỗ trợ selfhost cục bộ và RunningHub cloud.
- Mặc định dùng `image_flux.json`.
- Có thể đặt workflow riêng vào thư mục `workflows/`.

**Kích thước hình ảnh**

- Thiết lập chiều rộng/chiều cao theo pixel.
- Mặc định 1024x1024, có thể chỉnh theo nhu cầu.
- Mỗi model có giới hạn kích thước riêng.

**Prompt Prefix**

- Điều khiển phong cách hình ảnh tổng thể; nên dùng tiếng Anh để model hiểu tốt hơn.
- Ví dụ: `Minimalist black-and-white matchstick figure style illustration, clean lines, simple sketch style`.
- Bấm “Xem trước phong cách” để thử.

#### Mẫu video

Quyết định bố cục và thiết kế video.

**Quy ước đặt tên mẫu**

- `static_*.html`: mẫu tĩnh, không cần media AI.
- `image_*.html`: mẫu dùng ảnh AI làm nền.
- `video_*.html`: mẫu dùng video AI làm nền.

**Cách dùng**

- Chọn mẫu từ menu, được nhóm theo tỉ lệ dọc/ngang/vuông.
- Bấm “Xem trước mẫu” để thử với tham số tùy chỉnh.
- Nếu biết HTML, có thể tạo mẫu riêng trong thư mục `templates/`.

### 🎬 Tạo video (cột phải)

- Sau khi cấu hình xong, bấm “🎬 Tạo video”.
- Giao diện hiển thị tiến độ theo thời gian thực: tạo kịch bản → tạo ảnh/video → tạo giọng → ghép video.
- Khi hoàn tất, video sẽ tự hiện để xem trước.
- File video được lưu trong thư mục `output/`.

## ❓ Câu hỏi thường gặp

**Q: Lần đầu dùng mất bao lâu?**  
A: Thời gian tạo phụ thuộc số cảnh, mạng và tốc độ suy luận AI; thường hoàn tất trong vài phút.

**Q: Video chưa ưng ý thì làm sao?**  
A: Có thể thử:

1. Đổi model LLM để thay phong cách lời dẫn.
2. Chỉnh kích thước ảnh và Prompt Prefix để đổi phong cách hình.
3. Đổi workflow TTS hoặc tải âm thanh tham chiếu để đổi giọng.
4. Thử mẫu video và tỉ lệ khác.

**Q: Chi phí khoảng bao nhiêu?**  
A: **Dự án hỗ trợ chạy miễn phí hoàn toàn.**

- **Miễn phí hoàn toàn**: Ollama cục bộ + ComfyUI cục bộ = 0 đồng.
- **Khuyến nghị**: Qwen + ComfyUI cục bộ, chi phí rất thấp.
- **Cloud**: OpenAI + RunningHub, chi phí cao hơn nhưng không cần môi trường cục bộ.

**Gợi ý chọn lựa**: Nếu có GPU cục bộ, dùng phương án miễn phí. Nếu không, dùng Qwen để tối ưu chi phí.

## 🤝 Dự án tham khảo

Pixelle-Video được truyền cảm hứng từ các dự án mã nguồn mở sau:

- [Pixelle-MCP](https://github.com/AIDC-AI/Pixelle-MCP) - ComfyUI MCP server, cho phép trợ lý AI gọi ComfyUI trực tiếp.
- [MoneyPrinterTurbo](https://github.com/harry0703/MoneyPrinterTurbo) - Công cụ tạo video xuất sắc.
- [NarratoAI](https://github.com/linyqh/NarratoAI) - Công cụ tự động hóa video thuyết minh.
- [MoneyPrinterPlus](https://github.com/ddean2009/MoneyPrinterPlus) - Nền tảng sáng tạo video.
- [ComfyKit](https://github.com/puke3615/ComfyKit) - Thư viện đóng gói workflow ComfyUI.

Cảm ơn tinh thần mã nguồn mở của các dự án này.

## 💬 Cộng đồng

Quét mã QR bên dưới để tham gia cộng đồng, nhận cập nhật mới nhất và hỗ trợ kỹ thuật:

| WeChat | Discord |
| ---- | ---- |
| <img src="resources/wechat.png" alt="Nhóm WeChat" width="250" /> | <img src="resources/discord.png" alt="Cộng đồng Discord" width="250" /> |

## 📢 Phản hồi và hỗ trợ

- 🐛 **Gặp lỗi**: Tạo [Issue](https://github.com/namlevia/Pixelle-Video/issues).
- 💡 **Đề xuất tính năng**: Tạo [Feature Request](https://github.com/namlevia/Pixelle-Video/issues).
- ⭐ **Star dự án**: Nếu dự án hữu ích, hãy cho repo một star để ủng hộ.

## 📝 Giấy phép

Dự án sử dụng giấy phép Apache 2.0. Xem chi tiết trong file [LICENSE](LICENSE).

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=AIDC-AI/Pixelle-Video&type=Date)](https://star-history.com/#AIDC-AI/Pixelle-Video&Date)
