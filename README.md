### 1. Vấn đề
AI đưa ra lệnh sửa lỗi `Path not found` khi cài Python nhưng chưa rõ độ an toàn, có nguy cơ gây lỗi hệ thống.

### 2. Yêu cầu
Phân tích theo mô hình IPO và kiểm chứng lệnh trước khi thực thi. Thiết kế Prompt để hỏi ngược lại AI.

### 3. Cách làm

**Phân tích IPO:**
- **Input:** Lệnh sửa lỗi do AI cung cấp.
- **Process:** Tìm kiếm lệnh bằng `site:stackoverflow.com` hoặc kiểm tra trên trang chủ Python để xác minh cú pháp, phiên bản và mức độ an toàn.
- **Output:** Chỉ sử dụng lệnh khi đã xác minh nguồn gốc và độ an toàn. Nếu chưa rõ thì không thực thi.

**Prompt hỏi ngược AI:**

```text
Hãy giải thích chức năng của từng phần trong câu lệnh trên.
Lệnh này có an toàn không? Có ảnh hưởng đến dữ liệu hoặc hệ thống không?
Lệnh có phù hợp với phiên bản Windows và Python của tôi không?
Hãy đưa ra nguồn chính thống để kiểm chứng trước khi tôi thực thi.
```
