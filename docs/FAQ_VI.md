# 🙋‍♀️ Pixelle-Video - Câu hỏi thường gặp (FAQ)

### Làm sao tích hợp workflow ComfyUI tự phát triển ở local?

Nếu bạn muốn tích hợp workflow ComfyUI của riêng mình, hãy làm theo các quy ước sau:

1. **Chạy local trước**: Đảm bảo workflow chạy bình thường trong ComfyUI cục bộ của bạn.
2. **Gắn tham số**: Tìm node Text cần được chương trình truyền prompt động vào (CLIP Text Encode hoặc node nhập văn bản tương tự).
   - Sửa **Title** của node đó.
   - Đổi title thành `$prompt.text!` hoặc `$prompt.value!` tùy theo kiểu input mà node nhận.
     <img src="https://github.com/user-attachments/assets/ddb1962c-9272-486f-84ab-8019c3fb5bf4" width="600" alt="Ví dụ gắn tham số" />

   - *Tham khảo: xem cách chỉnh các file JSON có sẵn trong thư mục `workflows/selfhost/`.*
3. **Định dạng export**: Export workflow đã chỉnh sửa dưới dạng **API Format** (Save (API Format)).
4. **Đặt tên file**: Đặt file JSON đã export vào thư mục `workflows/` và tuân thủ tiền tố tên file:
   - **Workflow hình ảnh**: bắt buộc có tiền tố `image_` (ví dụ `image_my_style.json`).
   - **Workflow video**: bắt buộc có tiền tố `video_`.
   - **Workflow TTS**: bắt buộc có tiền tố `tts_`.

### Làm sao debug workflow RunningHub ở local?

Nếu bạn muốn test local workflow vốn dùng cho RunningHub cloud:

1. **Lấy ID**: Mở file workflow RunningHub và tìm ID.
2. **Load workflow**: Dán ID vào cuối URL RunningHub, ví dụ `https://www.runninghub.cn/workflow/1983513964837543938`, để mở trang workflow.
   <img src="https://github.com/user-attachments/assets/e5330b3a-5475-44f2-81e4-057d33fdf71b" width="600" alt="Ví dụ workflow RunningHub" />
3. **Tải về local**: Trong workbench, tải workflow về dưới dạng file JSON.
4. **Test local**: Kéo file đã tải vào canvas ComfyUI cục bộ để test và debug.

### Các lỗi thường gặp và cách xử lý

#### 1. Lỗi TTS (tổng hợp giọng nói)

- **Nguyên nhân**: Edge-TTS mặc định gọi API miễn phí của Microsoft, có thể thất bại khi mạng không ổn định.
- **Cách xử lý**:
  - Kiểm tra kết nối mạng.
  - Nên chuyển sang workflow **ComfyUI TTS** (workflow có tiền tố `tts_`) để ổn định hơn.

#### 2. Lỗi LLM (mô hình ngôn ngữ lớn)

- **Các bước kiểm tra**:
  1. Kiểm tra **Base URL** có đúng không, không thừa khoảng trắng hoặc sai hậu tố.
  2. Kiểm tra **API Key** còn hiệu lực và còn số dư/hạn mức.
  3. Kiểm tra **Model Name** có viết đúng không.
  - *Mẹo: hãy xem tài liệu API chính thức của nhà cung cấp model bạn dùng như OpenAI, DeepSeek, Alibaba Cloud... để lấy cấu hình chính xác.*

#### 3. Lỗi “Could not find a Chrome executable...”

- **Nguyên nhân**: Máy chưa có nhân trình duyệt Chrome, khiến các tính năng phụ thuộc trình duyệt không chạy được.
- **Cách xử lý**: Cài Google Chrome.

### Video tạo xong được lưu ở đâu?

Tất cả video tạo ra được lưu tự động trong thư mục `output/` của dự án. Khi hoàn tất, giao diện sẽ hiển thị thời lượng video, dung lượng file, số cảnh và link tải xuống.

### Có tài nguyên cộng đồng nào?

- **GitHub repo**: https://github.com/namlevia/Pixelle-Video
- **Báo lỗi**: Gửi bug hoặc yêu cầu tính năng qua GitHub Issues.
- **Hỗ trợ cộng đồng**: Tham gia nhóm thảo luận để nhận hỗ trợ và chia sẻ kinh nghiệm.
- **Đóng góp code**: Dự án dùng giấy phép Apache 2.0 và hoan nghênh đóng góp.

💡 **Mẹo**: Nếu không tìm thấy câu trả lời trong FAQ này, hãy tạo issue trên GitHub hoặc tham gia cộng đồng thảo luận. FAQ sẽ được cập nhật dần theo phản hồi của người dùng.
