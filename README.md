# MyTickets_MVC_ASP.NET
---
# eTickets - Hệ thống bán vé phim trực tuyến
eTickets là một dự án website sử dụng mô hình MVC (Model-View-Controller) để cung cấp một nền tảng bán vé phim trực tuyến. Dự án này cho phép người dùng mua vé xem phim từ các rạp khác nhau, quản lý thông tin người dùng, diễn viên, và rạp phim.

## Tính năng chính
- Đặt vé trực tuyến: Người dùng có thể tìm kiếm các bộ phim đang chiếu tại các rạp phim và đặt vé trực tuyến thông qua giao diện dễ sử dụng.
- Quản lý người dùng: Hệ thống cho phép người dùng đăng ký tài khoản, đăng nhập và quản lý thông tin cá nhân, lịch sử đặt vé.
- Quản lý diễn viên: Quản trị viên có khả năng thêm, sửa đổi và xóa thông tin về các diễn viên tham gia trong các bộ phim.
- Quản lý rạp phim: Quản trị viên có quyền quản lý danh sách các rạp phim, thêm, sửa đổi và xóa thông tin rạp.
- Xem thông tin chi tiết phim: Người dùng có thể xem thông tin chi tiết về các bộ phim, bao gồm diễn viên, thời lượng, thể loại, và giá vé.

# Cài đặt và chạy dự án
- Yêu cầu môi trường: Đảm bảo bạn đã cài đặt .NET SDK phiên bản 6 trở lên.
- Tạo dự án: Mở Command Prompt hoặc Terminal và chạy lệnh sau để tạo một dự án mới:
```bash
dotnet new web -n eTickets
```

- Cài đặt Entity Framework: Chạy lệnh sau để cài đặt Entity Framework Core:
````bash
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
````

- Cấu hình Database: Trong tệp appsettings.json, cấu hình chuỗi kết nối đến cơ sở dữ liệu SQL Server:
````json
"ConnectionStrings": {
  "DefaultConnection": "Server=your-server;Database=your-database;Trusted_Connection=True;MultipleActiveResultSets=true"
}
````

- Tạo Migration và Update Database: Chạy các lệnh sau để tạo migration và cập nhật cơ sở dữ liệu:

````bash
dotnet ef migrations add InitialCreate
dotnet ef database update
````
- Chạy ứng dụng
````bash
dotnet run
````
Truy cập ứng dụng: Mở trình duyệt và truy cập vào http://localhost:port để trải nghiệm ứng dụng.
