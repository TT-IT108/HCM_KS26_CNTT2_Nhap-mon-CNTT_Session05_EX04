**Bài 4 : Xử lý lỗi đường dẫn khi triển khai dự án**   
**Phần 1:** Lập bảng so sánh 2 giải pháp trên dựa trên các tiêu chí: Độ dài, Tính di động khi gửi project cho người khác.

| Tiêu chí | Đường dẫn tuyệt đối | Đường dẫn tương đối |
| :---- | :---- | :---- |
| Độ dài | Lộ trình hoàn chỉnh bắt đầu từ gốc ổ đĩa (Root: C:\\ hoặc /)  | Lộ trình tính từ vị trí tệp tin đang đứng (Working Directory) tới tệp đích  |
| Tính di động  | Chỉ chạy đúng trên máy tính của người tạo và bị gãy khi sang máy khác  | Giúp toàn bộ dự án di chuyển, nén zip hoặc deploy linh hoạt mà không bị lỗi.  |

**Phần 2:** Lựa chọn giải pháp tối ưu. Giải thích ý nghĩa của ký hiệu .. trong lựa chọn đó.

\-Giải pháp tối ưu: Chọn Đường dẫn tương đối vì đảm bảo khi đưa toàn bộ dự án đến người khác không bị gãy đứt đoạn, linh hoạt hơn nhiều so với đường dẫn tuyệt đối. Đường dẫn ../data/logs.csv chỉ đúng khi cấu trúc thư mục thực tế phù hợp với vị trí của script Python.   
\-Kí hiệu .. Đại diện cho thư mục cha, tức là lùi lên một cấp thư mục so với thư mục hiện tại. 