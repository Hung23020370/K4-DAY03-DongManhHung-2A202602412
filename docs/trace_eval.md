# 📊 BÁO CÁO THU HOẠCH NGHIỆM THU BÀI LAB 3 (BƯỚC 3 — SUBMISSION ARTIFACT)

> **Họ và Tên Học viên:** Đồng Mạnh Hùng
> **Mã Sinh Viên / Mã Học viên:** 2A202602412  
> **Chủ đề Lựa chọn:** Trợ lý quản lý chi tiêu cá nhân 

---

## 1. BẢNG CHẤM ĐIỂM AGENTIC FIT SCORING MATRIX (ĐÁNH GIÁ CHỦ ĐỀ)

| Tiêu chí Đánh giá | Mức độ (1 - 5) | Giải trình chi tiết lý do chọn điểm |
| :--- | :---: | :--- |
| **1. Multi-step Reasoning** | 3/ 5 | Hệ thống không chỉ phân loại thu/chi đơn thuần mà cần lập luận đa bước: phân tích tác động của khoản chi đột xuất lên ngân sách tháng, dự báo xu hướng dòng tiền đến cuối kỳ, đánh giá mức độ ưu tiên giữa các danh mục và đề xuất kịch bản bù trừ ngân sách hợp lý.|
| **2. Tool Interaction** | 3/ 5 | Người dùng nhập chi tiêu hôm nay, SQL/Vector DB (truy vấn lịch sử và hạn mức ngân sách), Python/Calculator (tính toán chính xác chỉ số tài chính, lãi suất, tỷ lệ tiết kiệm) và Notification API (gửi cảnh báo tức thì). |
| **3. Dynamic Decision** | 3/ 5 | Kế hoạch thực thi thay đổi động theo ngữ cảnh đầu vào: nếu thông tin giao dịch mơ hồ → chủ động hỏi lại để làm rõ (Human-in-the-loop); nếu chi tiêu trong hạn mức → tự động ghi sổ; nếu phát hiện nguy cơ thâm hụt → tự kích hoạt quy trình phân tích và đề xuất điều chỉnh ngân sách cho người dùng duyệt. |
| **4. Long Horizon Goal** | 4/ 5 | Hệ thống cần phải giữ mục tiêu xuyên suốt, agent theo dõi số tiền chi tiêu hàng tháng và liên tục cân đối dòng tiền. |
| **TỔNG ĐIỂM AGENTIC FIT** | **13/ 20** | *Nếu tổng điểm > 12/20: Bài toán rất phù hợp triển khai Agentic System.* |

---

## 2. TRÍCH XUẤT KẾT QUẢ WATERFALL TRACE LOG (SAU KHI CHẠY TEST SUITE TRÊN API THẬT)

> ⚠️ **YÊU CẦU NGHIỆM THU:** Mở tệp `.env` điền `GEMINI_API_KEY` (hoặc `OPENAI_API_KEY`) để kết nối LLM thật trước khi thực thi `python src/app.py --all`. Bài nộp chỉ dùng Mock Offline Provider sẽ không đạt điểm nghiệm thực tế.

Dán 1 đoạn trích xuất log tiêu biểu từ file `docs/trace_waterfall.json` sinh ra từ phản hồi LLM API thật:

```json
[
  {
    "step": 1,
    "query": "Thời tiết ở trường hôm nay thế nào?",
    "action_type": "FINAL_ANSWER",
    "thought": "Gemini phản hồi trực tiếp bằng văn bản (không cần gọi công cụ).",
    "output": "Xin lỗi bạn, là Trợ lý Học vụ của VinUni, tôi chỉ có thể hỗ trợ bạn tra cứu thông tin học vụ (như điểm số, hồ sơ sinh viên) hoặc đặt lịch hẹn với Cố vấn học tập. Tôi không có công cụ để cập nhật thông tin thời tiết thời gian thực. \n\nBạn có thể tự kiểm tra thời tiết Hà Nội (khu vực Gia Lâm nơi trường tọa lạc) qua các ứng dụng thời tiết trên điện thoại hoặc trang web dự báo thời tiết nhé! Nếu bạn cần hỗ trợ về học vụ, hãy cho tôi biết mã sinh viên của bạn.",
    "latency_ms": 2928.89
  }
]
```

---

## 3. TỔNG KẾT KẾT QUẢ NGHIỆM THU & NỘP BÀI

- [x] Đã điền API Key thật trong `.env` và xác nhận Agent chạy mượt mà trên LLM API thật (Gemini/OpenAI).
- **Tổng số Test Cases đã chạy thành công:** 5 / 5 test cases.
- **Số lượt gọi Tool qua MCP Server chính xác:** 5/5 lượt.
- **Kết quả đẩy Repo nộp bài:** [x] Đã Commit và Push mã nguồn thành công lên GitHub cá nhân.

---

> ✅ **HOÀN TẤT NỘP BÀI:** Sao chép đường link GitHub Repository cá nhân của bạn và dán vào ô nộp bài trên hệ thống LMS VLearn để hoàn tất Bài Lab 3!
