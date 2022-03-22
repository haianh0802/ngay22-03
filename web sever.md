# Cài đặt Nginx trên Ubuntu

Nginx là 1 phần mềm mã nguồn mở để phục vụ web. Nó sử dụng kiến trúc đơn luồng và được thiết kế để có hiệu suất và độ ổn định tối đa, vì thế nó hiệu quả hơn Apache nếu được cấu hình chính xác. Ngoài các khả năng của máy chủ HTTP, NGINX cũng có thể hoạt động như một máy chủ proxy cho email (POP3, SMTP, …), một trình cân bằng tải và proxy ngược cho các máy chủ HTTP, TCP và UDP.

### Bước 1: Cài đặt Nginx
Vì Nginx có sẵn trong kho lưu trữ của Ubuntu nên ta có thể trực tiếp cài đặt Nginx bằng hệ thống cài đặt và quản lý gói apt.

Đầu tiên, tiến hành update các gói trong hệ thống :

sudo apt install -y update

Cài đặt Nginx cho máy chủ Ubuntu của bạn :

sudo apt install -y nginx

Kiểm tra phiên bản Nginx:

sudo nginx -v

Cho phép Nginx khởi động cùng hệ thống :

sudo systemctl enable nginx

Khởi động và kiểm tra trạng thái của dịch vụ Nginx :

systemctl start nginx 

systemctl status nginx

### Bước 2: Cấu hình tường lửa
Sử dụng ufw để biết cách sử dụng cấu hình tường lửa cho Nginx :

sudo ufw app list 

Kích hoạt điều trên bằng cách sử dụng câu lệnh sau:

sudo ufw allow 'Nginx HTTP'

Sau đó kiểm tra lại thay đổi với lệnh sau:

sudo ufw status

### Bước 3: Kiểm tra trang web
Để kiểm tra trang web, ta mở trình duyệt và nhập vào địa chỉ ip của máy chủ Nginx.

http://IP_address 

ta sẽ được điều hướng đến trang web mặc định của Nginx :


![image](https://user-images.githubusercontent.com/101684058/159430154-3b55685e-b397-42a3-85cc-a89de693c443.png)

Khi bạn hiển thị như này tức là đã cài đặt thành công và nginx đã sẵn sàng để được quản lý.



