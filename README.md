![anh1](https://github.com/user-attachments/assets/3ee5b196-b60c-4933-a83a-5822f4574831)
<img width="1912" height="1029" alt="image" src="https://github.com/user-attachments/assets/ca10d867-f480-4911-ab79-47755a3cc642" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/27ea527e-96b0-4011-8af7-60a05c789b4d" />



https://github.com/user-attachments/assets/d03e841a-2b3c-49d8-952a-7b0ed1038650
Câu 1: So sánh sự khác biệt về lưu lượng dữ liệu (Payload)
Trong bài làm của em, sự khác biệt thể hiện rất rõ rệt:

Với REST API: Khi gọi một Endpoint như /api/products/1, hệ thống sẽ trả về toàn bộ dữ liệu của sản phẩm đó (bao gồm: SKU, cân nặng, kích thước, thuế, kho hàng, mô tả chi tiết, hình ảnh...). Payload lúc này rất lớn và chứa nhiều thông tin thừa mà Frontend không dùng tới.

Với GraphQL: Em chỉ gửi yêu cầu lấy name và price. Kết quả trả về chỉ gói gọn trong đúng 2 trường này.

Kết luận: GraphQL giúp tối ưu hóa băng thông, giảm tải cho đường truyền mạng và giúp trang Frontend của em tải nhanh hơn đáng kể so với REST API.

Câu 2: Thay đổi giá sản phẩm (Query hay Mutation?)
Nếu muốn thay đổi giá sản phẩm, em phải sử dụng hành động Mutation.

Giải thích:

Trong GraphQL, Query chỉ dùng cho mục đích đọc dữ liệu (tương ứng với phương thức GET trong REST), không làm thay đổi trạng thái của hệ thống.

Mutation được thiết kế riêng cho các hành động thay đổi dữ liệu trên Server (như Thêm, Sửa, Xóa - tương ứng với POST, PUT, DELETE). Việc đổi giá là một hành động cập nhật (Update) cơ sở dữ liệu, do đó bắt buộc phải dùng Mutation để đảm bảo tính toàn vẹn và đúng quy chuẩn của ngôn ngữ truy vấn này.

