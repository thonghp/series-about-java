# Comment - scanner - variable - naming convention

## Mục lục nội dung

- [1. Chương trình đơn giản](#1-chương-trình-đơn-giản)
- [2. Comment](#2-comment)
- [3. Scanner](#3-scanner)
- [4. Quy tắc đặt tên](#4-quy-tắc-đặt-tên)
- [5. Variable](#5-variable)

## 1. Chương trình đơn giản

```java
package com.edu.demo
public class DemoJavaProgram {
/*
 * public static void main(String... args) { cũng hợp lệ
 * static public void main(String[] args) cũng hợp lệ
 */
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

- Đặt tên class phải viết hoa mỗi chữ cái đầu tiên do java phân biệt chữ hoa chữ thường - **case sensitive**.
- **`public`** là một access modifier và không thể đảo thứ tự **`public`** với **`class`**.
- Phương thức **`main`** để thực thi những gì nằm trong nó.
- **`System.out.println("<message>")` ==>** gọi method **`println()`** của Object **`System.out`** và in ra màn hình console.

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## 2. Comment

- **`\\`** comment với nội dung ngắn và chỉ trên 1 dòng.
- **`/* */`** comment khối với nội dung mô tả nhiều.
- **`/** */`** comment dành cho document (thường là document API).

Quy tắc khi comment

- Rule 1: comment không trùng với code.
- Rule 2: comment phải giải thích code đang làm gì.
- Rule 3: comment đường dẫn copy code trên mạng.
- Rule 4: comment sau khi fix bug lại.

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## 3. Scanner

```java
import java.util.Scanner;

public class DemoJavaProgram {
    public static void main(String[] args) {
        System.out.print("Nhập vào số tuổi: ");
        Scanner input = new Scanner(System.in);
        int age = input.nextInt();
    }
}

nextByte() ==> đọc giá trị byte
nextShort() ==> đọc giá trị short
nextLong() ==> đọc giá trị long
nextFloat() ==> đọc giá trị float
nextDouble() ==> đọc giá trị double
```

- Đọc giá trị nhập vào từ bàn phím trên màn hình console.

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## 4. Quy tắc đặt tên

- Thiên về kiểu **camel**.
- Bắt đầu bằng chữ thường, **`$`** hay **`_`** và không nên bắt đầu bằng number hay ký hiệu khác.
  - Nhưng không nên dùng các ký hiệu **`$`** và **`_`** để đặt tên ở vị trí đầu tiên.
- Không sử dụng java keyword để đặt tên.
  - Có 2 keyword không sử dụng trong java là **`const, goto`**.

![keyword in java](/assets/keyword.jpg)

**Cách đặt tên**

- **Viết hoa đầu mỗi cụm từ ==> Vd: HelloWorld**
  - **`class`** sử dụng noun **==> Vd: User**
  - **`interface`** sử dụng adjective **==> Vd: Runnable**
- **Bắt đầu bằng chữ thường và đầu mỗi cụm chữ sẽ viết hoa ==> Vd: doSomething**
  - **`method`** sử dụng verb-noun
    - **`getName, setName, addNumbers, find, crud,...`**
  - **`variable`** có nghĩa và ngắn
    - **`boolean` ==> `isActive, isEnabled, isWorking, isCompleted, isRunning, hasPermission, isAuthorized, isAccepted, isConfirmed, hasErrors,...`**
    - **`int` ==> `quantity, count, number, total, index, position, offset, length, size, capacity, dimension,...`**
    - **`double` ==> `amount, price, value, balance, ratio, percentage, proportion, distance, length, size, measurement,...`**
    - **`String` ==> `fullName,...`**
    - **`List` ==> `customers, clientList,...`**
- Constant nên viết hoa hết, phân cách giữa các cụm từ bằng **`_`** và bắt đầu có final ở trước **==> Vd: MAX_SPEED**
  - **`public final static`** hay **`public static final`** đều được nhưng thường hay dùng **`final static`**
- package nên viết thường hết, bắt đầu bằng **`domain.organization.name`** ==> **Vd: edu.nlu.exercise**

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## 5. Variable

- Dùng để biểu diễn các giá trị có thể thay đổi trong chương trình.
- Chiếm số byte nhất định tuỳ vào **`datatype`**.
- Syntax khai báo biến: **`datatype variableName`**
- Phải gán giá trị trước khi sử dụng biến.

```java
int age; // declare
age = 10; // assign a value

age = 10 / (2 + 3); // assign the value of the expression

int year = 2023; // declare and assign values
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## Xem thêm bài viết khác

- [Java](day3.md)
- [Datatype - Operator - Math - Type Convention - Import](day5.md)
