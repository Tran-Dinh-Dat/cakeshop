#Setting
1. Import database cakeshop_db.sql
2. Move cakeshop directory to root http directory. Example: http://localhost/cakeshop 
3. Config database:
- Open file config/database.php and setting $db_user, $db_password
4. Username/password login: root/1
5. Understand: http://itmagical.com/hoc-lap-trinh-php/php-co-ban/tao-cau-truc-mvc-cho-project-php-thuan-oop.html


#Các module chính của website:
1. Module Tin Tức
	- Hiển thị những tin tức mới, nổi bật về Shop, những báo cáo, sự kiện, quảng cáo liên quan Shop
2. Module Sản Phẩm
	- Thiết kế bố trí giao diện trưng bày sản phẩm hài hòa với chủng loại sản phẩm
	- Sản phẩm được chia theo các chủng loại.
	- Chi tiết sản phẩm được phân theo các chi tiết rõ ràng như: hình ảnh, chủng loại, thương hiệu, giá cả, mô tả chi tiết sản phẩm.
3. Module Đăng nhập đăng kí
	- Khách hàng có thể đăng kí thành viên, thêm, sửa xóa thông tin của mình.
4. Module Đặt hàng
	- Hệ thống sản phẩm được thể hiện giá bán và tính năng đặt hàng. Khách hàng có thể đặt mua những sản phẩm ưng ý sau khi lựa chọn và đưa vào giỏ hàng. Thông tin đơn hàng sẽ được lưu lại và được quản lý chi tiết trong hệ quản trị website.
5. Module Phản hồi
 	- Khách hàng có thể phản hồi lại về các vấn đề của Shop
6. Module Bình luận
	- Khách hàng đăng kí thành viên có thể trực tiếp bình luận trên mỗi sản phẩm
7. Module gửi mail tự động
	- Khách hàng đăng kí nhận mail sẽ được gửi thông tin các đợt khuyến mại, các sản phẩm mới...
8. Hệ quản trị Website
	- Admin có thể đăng sản phẩm, sửa sản phẩm, user,...

Đọc kĩ các quy chuẩn trong Source Code
Frontend
1. Xây dựng Website theo mô hình MVC (Model - View - Controller)
	- View được đặt trong thư muc : site/views. Mỗi View sẽ có 1 folder riêng có tên trùng với tên view. Ví dụ Trang chủ sẽ có thư mục home, trang sản phẩm sẽ có thư mục product, trang tin tức sẽ có thu muc news
	- Controller đặt trong thư mục : site/controllers. Tương ứng với mỗi View sẽ có 1 file controller trùng tên. Ví dụ View home có controller home.php. Tên controller phải viết hoa chữ cái đầu và thêm Controller ở phía sau. Ví dụ HomeController.php, ProductController.php
	- Model cũng có cách đặt tên như Controller. Ví dụ HomeModel.php, ProductModel.php. Các Model sẽ kế thừa từ MasterModel (chứa các hàm có tham số dựng sẵn. Dễ viết truy vấn CSDL hơn);
Backend
1. Xây dựng các trang thêm, sửa, xoá:
    - Categories
    - Sub Categories
    - Product
    - News
    - Members
    - Order
    - Feedback