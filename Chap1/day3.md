# Java

## Mục lục nội dung

- [1. Đặc tả ngôn ngữ và phiên bản](#1-đặc-tả-ngôn-ngữ-và-phiên-bản)
- [2. Kiến trúc](#2-kiến-trúc)

## 1. Đặc tả ngôn ngữ và phiên bản

- Đặc tả ngôn ngữ là một định nghĩa kỹ thuật về cú pháp và ngữ nghĩa của ngôn ngữ lập trình.
- **API - application program interface** hay thư viện, chứa các class và interface đã được tạo trước phục vụ cho sử dụng.
- Có 3 version:
  - **Java SE - Java Standard Edition** để phát triển ứng dụng client-side chạy trên desktop.
  - **Java EE - Java Enterprise Edition** để phát triển ứng dụng server-side như Java servlets, JavaServer Pages (JSP) và JavaServer Faces (JSF).
  - **Java ME - Java Micro Edition** đề phát triển thiết bị di động.

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## 2. Kiến trúc

![java platform](/assets/architecture.jpg)

**JDK**

- **Java Development Kit = JRE + Development tools** ==> là bộ công cụ phát triển.
- Ngôn ngữ khác thì **JDK** chính là **SDK**.

**JRE**

- **Java Runtime Environment = JVM + Java Packages Classes(util, math, lang, awt, swing,...) + runtime libraries** ==> Chạy chương trình java **đã biên dịch, không thể tạo chương trình mới**.
- Trên máy người dùng chỉ cần cài JRE là được
- **JRE rời khác JRE trong JDK** chổ debug vì chỉ JRE trong JDK mới đi được vào trong lòng mã nguồn, method.

**JVM**

- **Java Virtual Machine == Class loader system + runtime data area + Execution Engine ==>** quản lý bộ nhớ thông qua **`garbage collection`**.

**Giai đoạn thực thi chương trình**:

![architecture](/assets/jvm.jpg)

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## Xem thêm bài viết khác

- [Computer](day1.md)
- [Operating System](day2.md)
