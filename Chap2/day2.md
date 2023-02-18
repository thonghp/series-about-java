# Datatype - Operator - Math - Type Convention - Import

## Mục lục nội dung

- [1. Datatype](#1-datatype)
  - [1.1 Integer](#11-integer)
  - [1.2 Floating point](#12-floating-point)
  - [1.3 Character](#13-character)
  - [1.4 Sự khác nhau giữa primitive và reference](#14-sự-khác-nhau-giữa-primitive-và-reference)
- [2. Operator](#2-operator)
  - [2.1 Arithmetic](#21-arithmetic)
  - [Lưu ý](#lưu-ý)
  - [2.2 Unary](#22-unary)
  - [2.3 Assignment](#23-assignment)
  - [2.4 Relational](#24-relational)
  - [2.5 Logical](#25-logical)
  - [2.6 Ternary](#26-ternary)
  - [2.7 Bitwise](#27-bitwise)
  - [2.8 Shift](#28-shift)
  - [2.9 Instance of](#29-instance-of)
  - [2.10 Arithmetic promotion](#210-arithmetic-promotion)
  - [2. 11 Thứ tự ưu tiên trong operator](#2-11-thứ-tự-ưu-tiên-trong-operator)
  - [2.10 Sự khác nhau giữa logical và bitwise](#210-sự-khác-nhau-giữa-logical-và-bitwise)
- [3. Một vài Math thường dùng](#3-một-vài-math-thường-dùng)
- [4. Type Convention](#4-type-convention)
- [5. Import](#5-import)

## 1. Datatype

- Chia làm 2 loại là primitive và reference:

**Primitive**

- Còn gọi là kiểu dữ liệu nguyên thuỷ, chia thành các loại **`Integer, floating-point, character, boolean`**.
- Chia làm 2 dạng là **Signed** và **Unsigned**
  - **Signed** có phạm vi từ âm đến dương.
  - **Unsigned** có phạm vi từ 0 đến phạm vi tối đa của datatype.
    - Chỉ có **char** sử dụng **Unsigned**, còn lại sử dụng **Signed**.
    - Java 8 hỗ trợ **Unsigned** cho **`int`** và **`long`**.

![datatype](/assets/datatype.jpg)

**Reference**

- Còn gọi là non-primitive hay kiểu dữ liệu tham chiếu.
- **`Array, String, Interface, Class, Anotation, Enumeration`**.

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

### 1.1 Integer

**`byte, short, int, long`**

- **`long`** thường dùng trong dân số thế giới, đường kính hành tinh,...
  - Java 7 hỗ trợ **`_`** cho phân tách con số.
  - Không thể sử dụng **`_`** ở đầu hoặc ở cuối, ở cạnh **`.`**, cạnh **`L,f`** và cạnh **`0x`**.
  - Vd **`long value = 3_000_000_000L;`**
- **`byte, short`** thường dùng trong file.
  - Đọc stream của bit
  - Tiết kiệm bộ nhớ array
  - 1 ký tự biểu diển 1 byte
- Có 3 cách lưu trữ Integer: **decimal(10), octal(8), hexadecimal(16)**

```java
int decimal = 12;
int octal = 012;
int hexa = 0xDeadCafe; // hexa ko phân biệt chữ hoa hay thường
```

**Max và Min**

```java
int myMinIntValue = Integer.MIN_VALUE;
int myMaxIntValue = Integer.MAX_VALUE;

long myMinlongValue = Long.MIN_VALUE;
long myMaxlongValue = Long.MAX_VALUE;

// Vượt quá miền sẽ quay đầu lại, áp dụng cho long và int
System.out.println(myMinIntValue - 1); // == myMaxIntValue
System.out.println(myMaxIntValue + 1); // == myMinIntValue

// byte và short khi vượt quá miền sẽ ép sang kiểu int
byte myMinByteValue = Byte.MIN_VALUE;
byte myMaxByteValue = Byte.MAX_VALUE;

short myMinShortValue = Short.MIN_VALUE;
short myMaxShortValue = Short.MAX_VALUE;
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

### 1.2 Floating point

- Còn gọi là dấu phẩy động, chia thành 2 loại: **`float, double`**.
  - Kiểu float khi sử dụng bắt buộc phải có f java mới hiểu.
  - Vd **`float a = 3.5F; // f hay F đều được`**.
- **`float`** có **độ chính xác 8** chữ số trong khi **`double`** là **16**.
- Có 3 giá trị đặc biệt trong floating point là **`positive infinity, negative infinity, NaN`**
- Dấu phẩy động không thích hợp trong tính toán tài chính vì nó không làm tròn.
  - Vd **`2.0 - 1.1 = 0.8999999...`**
  - Muốn chính xác thì dùng **`BigDecimal`**

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

### 1.3 Character

- Đại diện là **`char`**, dùng để mô tả đơn vị trong bảng mã **`UTF-16`**.
- Một vài escape thường dùng

```java
\b ==> backspace
\t ==> tab
\n ==> linefeed
\r ==> carriage return
\" ==> double quote
\' ==> single quote
\\ ==> backslash
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

### 1.4 Sự khác nhau giữa primitive và reference

| Primitive                             | Reference                                       |
| ------------------------------------- | ----------------------------------------------- |
| Lưu trực tiếp giá trị                 | Lưu địa chỉ bộ nhớ của giá trị                  |
| Đã được định nghĩa trước              | Phải tạo trước trừ **`String`**                 |
| Luôn gán giá trị                      | Không cần gán giá trị vì mặc định là **`null`** |
| Kích thước phụ thuộc vào kiểu dữ liệu | Có cùng kích thước                              |
| Không có method                       | Có thể viết method riêng                        |

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## 2. Operator

- Trong java có 3 dạng toán tử là toán tử 1 ngôi, 2 ngôi, 3 ngôi
  - **`a++`** ==> 1 ngôi
  - **`a + b`** ==> 2 ngôi
  - **`(a > 2) ? a : 2`** ==> 3 ngôi
- Toán tử gồm **Arithmetic (số học), Assignment, Unary, Relational, Logical, Ternary, Bitwise, Shift, Type Comparison.**

### 2.1 Arithmetic

- Còn gọi là toán tử số học bao gồm **`+, -, *, /, %`**.
- Khi giá trị trả về là **floating-point** thì 1 trong 2 toán hạng phải là kiểu **floating-point**.

```java
double add = 3 + 2.2; // 5.2
double subtract = 3 - 2.2; // 0.79...8
double multiply = 3 * 2.2; // 6.60...5
double devision = 5 / 2; // 2.0
double devision = 5.0 / 2; // 2.5
double devision = (double) 5 / 2 ; // 2.5
double remainder = 5 % 2; // 1
double remainder = 5.5 % 2; // 1.5
```

### Lưu ý

**Chia cho 0**

```java
int integer = 1 / 0; // runtime
double result = 10 / 0; // runtime
double result = 10.0 / 0; // infinity
```

**Kiểm tra NaN**

```java
// kiểm tra NaN thông qua isNaN ****
double x = 7.0 / 0.0;
x != Double.NaN; // true
x <  Double.NaN; // false
x <=  Double.NaN; // false
x >  Double.NaN; // false
x >=  Double.NaN; // false
x ==  Double.NaN; // false
```

**Byte**

- Lỗi tràn miền **`byte`** khi phép tính kiểu **`int`** cast qua **`byte`** gây tràn miền.

```java
// Range -128 -> 127
byte result = 70 * 5; // compile
byte a = 70, b = 5, c = a * b; // compile
byte result = (byte) 70 * 5; // compile
```

- Để không bị tràn miền thực hiện như sau:

```java
byte result = (byte) (70 * 5); // 94
byte result = 70;
result *= 5; // 94 <=> (byte)(70 * 5)
```

- Khi giá trị byte vượt quá range sẽ quay đầu lại range bên kia.
- Như vd trên range lúc này là **`350`** **==>** vượt quá **`350 - 127 = 233`**
- Quay đầu lại **`-128`** **==>** **-128 + 223 - 1 = 94** (trừ 1 ở đây là trừ con số 0)

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

### 2.2 Unary

Toán tử Unary gồm **`++, --, +, -, ~`**

- **`++`** áp dụng với **`char`** sẽ ra ký tự tiếp theo.

```java
int a = 5, b = 6;
// đứng trước thì gán trước, đứng sau thì gán sau
System.out.println(++a); // 6
System.out.println(a); // 6


System.out.println(b++); // 6
System.out.println(b); // 7

System.out.println(+b); // 7
System.out.println(-b); // -7

System.out.println(--a--); // lỗi kể cả bỏ trong ()
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

### 2.3 Assignment

Toán tử Assignment gồm **`=, +=, -=, *=, /=, %=, &=, |=, ^=, <<=, >>=, >>>=`**

### 2.4 Relational

Toán tử Relational gồm **`==, !=, <, <=, >, >=`**

### 2.5 Logical

- Toán tử Logical gồm **`&&, ||, !`**
- **`Short-circuiting` ==>** Kiểm tra bên trái toán tử đúng mới kiểm tra bên phải.

```java
int i = 5, j = 10, k = 15;

// do tính chất short-circuting thì khi i < j thỏa => ko chạy đk bên phải
if ((i < j) || ( k++ > j)) {
  System.out.println("k: " + k); // 15
}

if ((i < j) && ( k++ < j)) {
  System.out.println("k: " + k); // 16
}
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

### 2.6 Ternary

```java
// ưu tiên kiểu nào lớn hơn để trả về giá trị
int x = 4;
System.out.println(x > 4 ? 99.99 : 9); // 9.0
```

### 2.7 Bitwise

- Toán tử Bitwise gồm **`&, |, ^, ~, !`** và làm việc dựa trên **`bit`**.
- **`O`** đứng đầu là âm, **`1`** đứng đầu là dương.
  - **`&`** => and
    - **`0 & 0 => 0`**
    - **`0 & 1 => 0`**
    - **`1 & 0 => 0`**
    - **`1 & 1 => 1`**
  - **`|`** => or
    - **`0 | 0 => 0`**
    - **`0 | 1 => 1`**
    - **`1 | 0 => 1`**
    - **`1 | 1 => 1`**
  - **`^`** => xor
    - **`0 ^ 0 => 0`**
    - **`0 ^ 1 => 1`**
    - **`1 ^ 0 => 1`**
    - **`1 ^ 1 => 0`**
  - **`~`** => inversion, đảo ngược bit.
    - **`~ 0101 => 1010`**
  - **`!`** => sử dụng trên boolean
    - **`boolean a = true, b = !a; // fasle`**
  - **`false = 0`** và **`true = 1`**

**Vd**

```java
System.out.println(10 & 12); // 8
/*
 * 256 128 64 32 16 8 4 2 1
 *                  1 0 1 0 // 10
 *                  1 1 0 0 // 12
 *                &
 *                  1 0 0 0 => 8
 */
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

### 2.8 Shift

- Toán tử Shift gồm **`<<, >>, >>>`**.
- Sử dụng để dịch chuyển các **`bit`** của toán hạng đầu tiên sang phải hoặc trái.
- Áp dụng với **`int, long, short, byte, char`**.

**Vd**

```java
/*
 * 13 -> 00000000 00000000 00000000 00001101
 * << 2  00000000 00000000 00000000 00110100
 */
int result = 13 << 2; // 52

/*
 * 13 -> 00000000 00000000 00000000 00001101
 * >> 2  00000000 00000000 00000000 00000011
 */
int result = 13 >> 2; // 3

/*
 * -1 -> 11111111 11111111 11111111 11111111
 * <<2   11111111 11111111 11111111 11111100
 * >>2   11111111 11111111 11111111 11111111
 * >>>2  11111111 11111111 11111111 111111
 */
int result = -1 << 2;
result = result >> 2;
result = result >>> 2;
// Đối với toán tử >>> không thể lấy lại các bit bị mất
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

### 2.9 Instance of

- **`instance of`** dùng để kiểm tra xem **object** có phải là **instance** của **`class`**, **subclass**(**`extends`**) hay class **implement** **`interface`**.
- Kiểm tra **runtime**.

**Vd**

```java
interface  X{}
class A implements X {}
class B extends A {}
A a = new A();
B b = new B();

if (b instanceof X) // true
if (b instanceof B) // true
if (b instanceof A) // true
if (a instanceof A) // true
if (a instanceof X) // true
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

### 2.10 Arithmetic promotion

- Thăng hạng toán tử là trình biên dịch sẽ convert type thành type khác cho phù hợp.
- Áp dụng cho biểu thức 2 toán tử
  - Nếu toán tử có type là **`byte, short, char`** => promotion lên **`int`**.
  - 1 trong 2 toán tử có cái lớn hơn thì ưu tiên promotion theo cái lớn hơn.

```java
byte b = 5;
int i = 3;
// lúc này b sẽ được compiler tự động promotion lên int
double d =  b / i; // 1.0
```

### 2. 11 Thứ tự ưu tiên trong operator

![operator precedence](/assets/operator-precedence.png)

**Vd**

```java
boolean a = true;
boolean b = false;
boolean c = false;

/*
 * (b && c) => false (1)
 * (b && b) => false (2)
 * a || (b && c) => true (3)
 * (a || (b && c)) || (b && b) => true (4)
 */
boolean result = a || b && c || b && b; // true

/*
 * (b & b) => false (1)
 * (a | b) => true (2)
 * (a | b) && c => false (3)
 * ((a | b) && c) || (b & b) => false (4)
 */
boolean result = a  | b && c || b & b; // false
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

### 2.10 Sự khác nhau giữa logical và bitwise

- **Logical ==> kiểm tra bên trái ==> true ==> kiểm tra bên phải**.
- **Bitwise ==> kiểm tra cả 2 bên**

**Vd**

```java
int x = 1;
System.out.println((x != 0) & (1 / x) > 1); // false
System.out.println((x != 0) && (1 / x) > 1); // false

int x = 0;
System.out.println((x != 0) & (1 / x) > 1); // runtime
System.out.println((x != 0) && (1 / x) > 1); // false
/*
 * Thứ 1 lỗi runtime do check 2 bên mà 1 / x <=> 1 / 0 lỗi
 * Thứ 2 (x != 0 false) mà && 1 cái false thì false hết => ko check bên phải
 */

int a = 10;
if(++a==10 && ++a==12) {}
System.out.println(a); // 11
if(++a==10 & ++a==12) {}
System.out.println(a); // 12
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## 3. Một vài Math thường dùng

Các phương thức trong lớp **`Math`** đều là **`static`** method.

```java
System.out.println(Math.abs(-4.7)); // 4.7
System.out.println(Math.ceil(1.4)); // 2.0
System.out.println(Math.floor(1.7)); // 1.0
System.out.println(Math.round(1.49)); // 1
System.out.println(Math.round(1.5)); // 2
System.out.println(Math.max(5, 10)); // 10
System.out.println(Math.min(5.2, 10)); // 5.2

System.out.println(Math.sqrt(64)); // 8.0
System.out.println((double)Math.sqrt(-3)); // NaN tương tự cho float
System.out.println((int)Math.sqrt(-3)); // 0

System.out.println(Math.pow(2, 3)); // 2 ^ 3 = 8.0
System.out.println(Math.random()); // return 0.0 < x < 1.0
System.out.println((int) (Math.random() * 2)); // return giá trị từ 0 <= value < 2
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## 4. Type Convention

- Còn được gọi là **type casting hay ép kiểu**.
- Có 2 loại ép kiểu là **wide (rộng) và narrow (hẹp)**.

![type casting](/assets/type-convention.png)

- Mũi tên **liền nét** thể hiện **độ chính xác giữ nguyên**.
- Mũi tên **không liền nét** thì **độ chính xác bị mất**.

**Vd**

```java
int a = 123456789; // độ chính xác dữ nguyên
float b = a; // 1.23456792E8
```

- **Wide ==> ép từ nhỏ sang lớn ==> tự động**

```java
int typeInt = 3;
double intToDouble = typeInt;
System.out.println(intToDouble); // 3.0
```

- **Narrow ==> ép từ lớn sang nhỏ ==> thủ công**

```java
double typeDouble = 3.5;
int typeCastInt = (int) typeDouble;
System.out.println(typeCastInt); // 3
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## 5. Import

- Có 2 loại **`import`** là **specific `import`** và **wildcard `import`**.
- **Specific import** ==> import 1 lớp sử dụng.
- **Wildcard import** ==> import tất cả lớp có trong package.

```java
// import java.util.ArrayList; // import một class arraylist
// import java.util.*; // import tất cả class trong gói util
```

**[⬆ Quay trở lại đầu trang](#mục-lục-nội-dung)**

## Xem thêm bài viết khác

- [Comment - scanner - variable](day1.md)
