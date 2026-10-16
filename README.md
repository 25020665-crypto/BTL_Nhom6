# BÁO CÁO KẾT QUẢ BÀI TẬP LỚN LẬP TRÌNH NÂNG CAO

## 1. Thông tin nhóm

**Tên dự án:** Hệ thống đấu giá trực tuyến (Online Auction System)

**Link dự án:** [Đường dẫn GitHub của nhóm]

**Thành viên nhóm:**
- [Họ và tên thành viên 1] - [Mã sinh viên]
- [Họ và tên thành viên 2] - [Mã sinh viên]
- [Họ và tên thành viên 3] - [Mã sinh viên]
- [Họ và tên thành viên 4] - [Mã sinh viên]

**Mô hình làm việc:** Nhóm áp dụng Scrum để theo dõi tiến độ, phân chia công việc và trao đổi về các vấn đề phát sinh. Các thành viên định kỳ đánh giá công việc đã hoàn thành và thống nhất kế hoạch cho giai đoạn tiếp theo.

**Chiến lược quản lý phiên bản:** Nhóm sử dụng Git và GitHub theo Gitflow. Mỗi thành viên phát triển tính năng trên một nhánh riêng, sau đó tạo Pull Request để review và tích hợp vào nhánh `develop`.

- `main`: Phiên bản ổn định, sẵn sàng phát hành.
- `develop`: Tích hợp các tính năng đã hoàn thành và qua review.
- `feature/<ten-chuc-nang>`: Nhánh phát triển tính năng; sau khi hoàn tất sẽ được merge vào `develop`.

## 2. Giới thiệu dự án

### Mô tả

**Tên sản phẩm:** Hệ thống đấu giá trực tuyến

Dự án xây dựng một hệ thống cho phép người bán đăng sản phẩm và tổ chức các phiên đấu giá trong khoảng thời gian xác định. Người mua có thể tham gia trả giá, theo dõi mức giá hiện tại và biết kết quả khi phiên đấu giá kết thúc.

Hệ thống hướng đến việc áp dụng lập trình hướng đối tượng, kiến trúc Client–Server và các mẫu thiết kế để tổ chức mã nguồn rõ ràng, dễ bảo trì và mở rộng.

### Chức năng chính

- Đăng ký, đăng nhập và hỗ trợ các vai trò Bidder, Seller, Admin.
- Seller quản lý sản phẩm đấu giá và thông tin phiên đấu giá.
- Bidder đặt giá hợp lệ và theo dõi giá đấu hiện tại.
- Tự động kết thúc phiên đấu giá và xác định người thắng cuộc.
- Xử lý các trường hợp như đặt giá thấp hơn giá hiện tại hoặc đấu giá khi phiên đã đóng.
- Cập nhật diễn biến đấu giá theo thời gian thực.

### Định hướng kỹ thuật

- **Ngôn ngữ:** Java.
- **Giao diện:** JavaFX hoặc Swing.
- **Kiến trúc:** Client–Server; áp dụng MVC.
- **Giao tiếp:** REST API hoặc Socket với dữ liệu JSON.
- **Kiểm thử:** JUnit cho các logic quan trọng.
- **Quản lý mã nguồn:** Git và GitHub.
- **Mẫu thiết kế dự kiến:** Singleton, Factory Method, Observer; có thể mở rộng với Strategy hoặc Command.
## 3. Các chức năng chính

- **Chức năng 1: Quản lý tài khoản và người dùng**  
  Đăng ký, đăng nhập và hỗ trợ các vai trò Bidder (người tham gia đấu giá), Seller (người bán) và Admin (quản trị viên).

- **Chức năng 2: Quản lý sản phẩm đấu giá**  
  Seller thêm, sửa, xóa sản phẩm và cung cấp các thông tin như tên, mô tả, giá khởi điểm, thời gian bắt đầu và kết thúc.

- **Chức năng 3: Tham gia đấu giá**  
  Bidder đặt giá cao hơn giá hiện tại; hệ thống kiểm tra tính hợp lệ và cập nhật người đang dẫn đầu phiên.

- **Chức năng 4: Quản lý phiên đấu giá**  
  Theo dõi trạng thái phiên, tự động kết thúc khi hết thời gian và xác định người thắng cuộc.

- **Chức năng 5: Xử lý lỗi và ngoại lệ**  
  Xử lý các trường hợp đặt giá không hợp lệ, đấu giá khi phiên đã đóng, lỗi dữ liệu hoặc lỗi kết nối.

- **Chức năng 6: Cập nhật diễn biến đấu giá**  
  Thông báo giá đấu mới đến những người đang theo dõi phiên theo thời gian thực.

- **Chức năng 7: Các chức năng mở rộng**  
  Có thể phát triển thêm đấu giá tự động (Auto-Bidding), gia hạn phiên khi có giá đấu sát giờ kết thúc (Anti-sniping) và biểu đồ lịch sử giá.

## 4. Công nghệ

### 4.1. Công nghệ dự kiến sử dụng

- **Ngôn ngữ lập trình:** Java
- **Giao diện:** JavaFX (khuyến nghị) hoặc Swing
- **Kiến trúc:** Client–Server, áp dụng mô hình MVC
- **Giao tiếp:** REST API hoặc Socket, trao đổi dữ liệu JSON
- **Build tool:** Maven hoặc Gradle
- **Kiểm thử:** JUnit
- **Quản lý mã nguồn:** Git và GitHub

### 4.2. Nguyên tắc và mẫu thiết kế

- Áp dụng các nguyên tắc OOP: Encapsulation, Inheritance, Polymorphism và Abstraction.
- Sử dụng **Singleton** để quản lý thành phần dùng chung khi phù hợp.
- Sử dụng **Factory Method** để tạo các loại sản phẩm đấu giá.
- Sử dụng **Observer** để cập nhật thông tin phiên đấu giá theo thời gian thực.
- Có thể áp dụng **Strategy** hoặc **Command** để mở rộng cách xử lý giá đấu.