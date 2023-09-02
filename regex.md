# Regular expression

## Mục lục nội dung

## 1. Khái niệm

- Hay gọi tắt là regex

## 2. Matches

- Tương tự **`equals()`** nhưng mạnh hơn vì nó không bắt buộc phải là **`String`** cố định

```java
"Java".matches("Java"); // true

// đều true, .* chính là 
"Java is fun".matches("Java.*")
"Java is cool".matches("Java.*")
"Java is powerful".matches("Java.*")

// d biểu diễn là con số, 3 là đại diện có 3 ký tự ==> d{3} là 3 ký tự số
"440–02–4534".matches("\\d{3}–\\d{2}–\\d{4}")
```