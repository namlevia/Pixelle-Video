# Xử lý sự cố

Gặp vấn đề khi sử dụng? Dưới đây là các lỗi thường gặp và cách xử lý.

---

## Lỗi cài đặt

### Cài dependency thất bại

```bash
# Xóa cache
uv cache clean

# Cài lại
uv sync
```

---

## Lỗi cấu hình

### Kết nối ComfyUI thất bại

**Nguyên nhân có thể**:

- ComfyUI chưa chạy.
- URL cấu hình sai.
- Firewall chặn kết nối.

**Cách xử lý**:

1. Xác nhận ComfyUI đang chạy.
2. Kiểm tra URL, mặc định là `http://127.0.0.1:8188`.
3. Mở địa chỉ ComfyUI trong trình duyệt để test.
4. Kiểm tra firewall.

### Gọi LLM API thất bại

**Nguyên nhân có thể**:

- API Key sai.
- Mạng có vấn đề.
- Tài khoản hết số dư/hạn mức.

**Cách xử lý**:

1. Kiểm tra API Key.
2. Kiểm tra kết nối mạng.
3. Xem kỹ nội dung lỗi.
4. Kiểm tra số dư/hạn mức tài khoản.

---

## Lỗi tạo video

### Tạo video thất bại

**Nguyên nhân có thể**:

- File workflow bị lỗi.
- Chưa tải model cần thiết.
- Không đủ tài nguyên máy.

**Cách xử lý**:

1. Kiểm tra file workflow có tồn tại không.
2. Xác nhận ComfyUI đã tải đủ model yêu cầu.
3. Kiểm tra dung lượng ổ đĩa và RAM/VRAM.

### Tạo hình ảnh thất bại

**Cách xử lý**:

1. Kiểm tra ComfyUI có chạy ổn định không.
2. Thử chạy workflow thủ công trong ComfyUI.
3. Kiểm tra cấu hình workflow.

### Tạo TTS thất bại

**Cách xử lý**:

1. Kiểm tra workflow TTS có đúng không.
2. Nếu dùng clone giọng, kiểm tra định dạng âm thanh tham chiếu.
3. Xem log lỗi.

---

## Hiệu năng

### Tạo video quá chậm

**Mẹo tối ưu**:

1. Dùng ComfyUI local, thường nhanh hơn cloud.
2. Giảm số cảnh.
3. Dùng LLM nhanh hơn như Qwen.
4. Kiểm tra kết nối mạng.

---

## Vấn đề khác

Nếu vẫn chưa xử lý được:

1. Xem [GitHub Issues](https://github.com/namlevia/Pixelle-Video/issues) của dự án.
2. Tạo issue mới mô tả vấn đề.
3. Đính kèm log lỗi và cấu hình liên quan để dễ chẩn đoán.

---

## Xem log

File log nằm ở thư mục gốc dự án:

- `api_server.log` - log dịch vụ API.
- `test_output.log` - log test.
