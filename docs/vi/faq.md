# FAQ

Các câu hỏi thường gặp.

---

## Cài đặt

### Q: Cài uv như thế nào?

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### Q: Có thể dùng công cụ khác ngoài uv không?

Có. Bạn có thể dùng cách truyền thống với `pip` + `venv`, nhưng `uv` được khuyến nghị vì nhanh và đơn giản hơn.

---

## Cấu hình

### Q: Có bắt buộc cấu hình ComfyUI không?

**Không nhất thiết** — tùy loại template bạn chọn:

| Loại template | ComfyUI | Phù hợp cho | Tốc độ |
|--------------|---------|-------------|--------|
| Chỉ văn bản<br/>(ví dụ `simple.html`) | ❌ Không cần | Trích dẫn, thông báo, nội dung đọc | ⚡⚡⚡ Rất nhanh |
| Ảnh AI<br/>(ví dụ `default.html`) | ✅ Cần | Nội dung giàu hình ảnh | ⚡ Bình thường |

**Mẹo**: Người mới có thể bắt đầu bằng template chỉ văn bản để trải nghiệm nhanh, không cần cấu hình phức tạp.

**Thay thế**: Nếu cần ảnh AI nhưng không muốn chạy ComfyUI local, có thể dùng RunningHub cloud.

### Q: Hỗ trợ những LLM nào?

Mọi LLM tương thích OpenAI API, bao gồm:

- Qwen
- GPT-4o
- DeepSeek
- Ollama local

---

## Sử dụng

### Q: Lần đầu tạo video mất bao lâu?

Một video 3-5 cảnh thường mất khoảng 2-5 phút, tùy model, mạng và tài nguyên máy.

### Q: Nếu chưa hài lòng với video thì làm gì?

Hãy thử:

1. Đổi model LLM.
2. Chỉnh kích thước ảnh và Prompt Prefix.
3. Đổi workflow TTS.
4. Thử template video khác.

### Q: Chi phí thế nào?

- **Miễn phí hoàn toàn**: Ollama + ComfyUI local = 0 đồng.
- **Khuyến nghị**: Qwen + ComfyUI local, chi phí thấp.
- **Cloud**: OpenAI + RunningHub, chi phí cao hơn.

---

## Xử lý sự cố

### Q: Kết nối ComfyUI thất bại

1. Xác nhận ComfyUI đang chạy.
2. Kiểm tra URL có đúng không.
3. Bấm “Kiểm tra kết nối” trong Web UI.

### Q: Gọi LLM API thất bại

1. Kiểm tra API Key.
2. Kiểm tra kết nối mạng.
3. Đọc thông báo lỗi chi tiết.

---

## Câu hỏi khác

Nếu còn câu hỏi khác, hãy xem [Xử lý sự cố](troubleshooting.md) hoặc tạo [Issue](https://github.com/namlevia/Pixelle-Video/issues).
