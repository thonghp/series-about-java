# Operating Systems

## Mục lục nội dung

- [1. Tổng quát](#1-tổng-quát)
- [2. Kiểm soát và giám sát hoạt động của hệ thống](#2-kiểm-soát-và-giám-sát-hoạt-động-của-hệ-thống)
- [3. Phân bổ và chỉ định tài nguyên hệ thống](#3-phân-bổ-và-chỉ-định-tài-nguyên-hệ-thống)
- [4. Lập kế hoạch hoạt động](#4-lập-kế-hoạch-hoạt-động)

## 1. Tổng quát

- (OS) là chương trình quan trọng nhất chạy trên máy tính.
- Nó quản lý và điều khiển các hoạt động của máy tính.
![alt](/assets/os.png)
- Người dùng và ứng dụng truy cập phần cứng máy tính thông qua OS.
- Nhiệm vụ chính là: 
    - Kiểm soát và giám sát hoạt động của hệ thống.
    - Phân bổ và chỉ định tài nguyên hệ thống.
    - Lập kế hoạch hoạt động.

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## 2. Kiểm soát và giám sát hoạt động của hệ thống

Thực hiện các tác vụ cơ bản như:

- Nhận dạng đầu vào từ bàn phím, gửi đầu ra tới màn hình.
- Theo dõi các tệp và thư mục trên thiết bị lưu trữ.
- Điều khiển các thiết bị ngoại vi như ổ đĩa và máy in.
- Đảm bảo các chương trình và người dùng khác nhau hoạt động đồng thời không can thiệp lẫn nhau.
- Bảo mật, đảm bảo người dùng và chương trình trái phép không được phép truy cập vào hệ thống.

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## 3. Phân bổ và chỉ định tài nguyên hệ thống

Xác định tài nguyên máy tính mà chương trình cần chẳng hạn như CPU time, dung lượng bộ nhớ, disks, thiết bị input-output đẻ phân bổ và chỉ định chúng chạy chương trình.

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## 4. Lập kế hoạch hoạt động.

- Lên lịch các hoạt động của chương trình để sử dụng hiệu quả tài nguyên hệ thống.
- Hỗ trợ multiprogramming, multithreading và multiprocessing (đa xử lý).
- Multiprogramming - đa chương trình, cho phép nhiều chạy đồng thời bằng cách chia sẽ CPU khi nó không hoạt động.
    - Vd: word, web, email chạy cùng lúc.
- Multithreading - đa luồng, cho phép một chương trình thực hiện nhiều tác vụ cùng một lúc.
    - Vd: word vừa chỉnh sửa văn bản và lưu nó vào đĩa. Chỉnh sửa và lưu là 2 tác vụ.
- Multiprocessing - đa xử lý, tương tự như đa luồng nhưng đa xử lý để chạy nhiều chương trình đồng thời bằng nhiều bộ xử lý.  

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## Xem thêm bài viết khác

- [Computer](day1.md)
- [Java](day3.md)
