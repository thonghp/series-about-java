# Comment - scanner - variable

## Mục lục nội dung

- [1. Chương trình đơn giản](#1-chương-trình-đơn-giản)
- [2. Comment](#2-comment)
- [3. Scanner](#3-scanner)
- [4. Quy tắc đặt tên](#4-quy-tắc-đặt-tên)
- [5. Variable](#5-variable)

## 1. Conditional statement

### 1.1 If

Câu lệnh **`if`** sẽ được thực thi khi điều kiện là **`true`**.

**Syntax**

```java
if (condition) { // condition true mới excute code trong block
  // statement
}
```

**Vd**

```java
boolean isValue = true;
if (isValue) { // isValue = true
  System.out.println("hello");
}
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

### 1.2 If else

Câu lệnh **`if`** sẽ được thực thi khi điều kiện **`true`** và câu lệnh **`else`** sẽ được thực thi khi điều kiện **`false`**.

**Syntax**

```java
if (condition) {
    // statement
} else {
  // statement
}
```

**Vd**

```java
boolean isValue = false;
// in ra hi
if (isValue) {
  System.out.println("hello");
} else {
  System.out.println("hi");
}

// gán isValue = true 
if (isValue = true) { // true => excute block
  System.out.println("condition is assigned to true");
}
System.out.println(isValue); // true do isValue được gán = true
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

### 1.3 If else if

**`If ==> else if ==> else`**

**Syntax**

```java
if (condition1) {
    // statement1
} else if (condition2) {
    // statement2
} else {
    // statement3
}
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

### 1.4 Nested if

**Syntax**

```java
if (condition1) {
  ...
   if (condition2) {
      // statement
   }
}
```

### 1.5 Viết tắt gây hiểu nhầm trong if

**Hiểu sai {}**

```java
if (radius >= 0)
  area = radius * radius * PI;
  System.out.println("The area " + " is " + area);
==
if (radius >= 0) { // good
  area = radius * radius * PI;
}
System.out.println("The area " + " is " + area);
```

**If empty**

```java
if (radius >= 0); 
== 
if (radius >= 0) {}; // good
```

**True**

```java
if (even == true)
==
if (even) // good
```

**Else**

```java
int i = 1, j = 2, k = 3;
if (i > j)
  if (i > k)
     System.out.println("A");
else 
     System.out.println("B");
==
int i = 1, j = 2, k = 3;
if (i > j) // good
  if (i > k)
    System.out.println("A");
  else 
    System.out.println("B");
```

**boolean**

```java
if (number % 2 == 0)
  even = true;
else
  even = false;
==
boolean even = number % 2 == 0; // good
```

**print**

```java
if (inState) {
  tuition = 5000;
  System.out.println("The tuition is " + tuition);
}
else {
  tuition = 15000;
  System.out.println("The tuition is " + tuition);
}
==
if (inState) { // good
  tuition = 5000;
}
else {
  tuition = 15000;
}
System.out.println("The tuition is " + tuition); 
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## 2. 

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## 3. 

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## 4. 

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## 5. 

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## Xem thêm bài viết khác

- [Datatype - Operator - Math - Type Convention - Import](day2.md)
