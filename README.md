# Trợ lý AI Tiểu học

Ứng dụng tạo bài luyện tập theo mức độ cho từng học sinh, chia sẻ bài bằng link, đặt thời lượng làm bài và tạo nhận xét sau khi học sinh nộp.

## Chạy ứng dụng

1. Sao chép `.env.example` thành `.env` và điền `GEMINI_API_KEY`.
2. Chạy `npm start`.
3. Mở `http://localhost:3000`.

Bài tập và kết quả được lưu trong `data/assignments.json` trên máy chủ. Thư mục `data/` đã được loại khỏi Git vì có thể chứa câu trả lời của học sinh.

## Gửi link cho học sinh

Link `localhost` chỉ dùng được trên máy đang chạy ứng dụng. Muốn học sinh mở bằng điện thoại hoặc máy khác, hãy triển khai ứng dụng lên hosting hoặc một máy chủ trong mạng nội bộ, rồi đặt `PUBLIC_APP_URL` trong `.env` thành địa chỉ học sinh truy cập được. Khởi động lại máy chủ sau khi đổi cấu hình.

Ở tab **Giao bài theo link**, giáo viên tạo một bài cho mỗi học sinh, chọn mức độ, số câu và thời gian từ 1 đến 90 phút. Học sinh mở link, bấm bắt đầu, trả lời và nộp; hệ thống chấm, hiện nhận xét và lưu kết quả để giáo viên xem lại bằng nút **Xem kết quả học sinh** trên trình duyệt đã tạo bài.

Chỉ nhập tên gọi hoặc biệt danh của học sinh. Nhận xét do AI tạo cần được giáo viên xem lại.
