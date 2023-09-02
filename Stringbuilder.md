Stringbuilder và buffer là mutable (có thể thay đổi) còn string là immutable (ko thể sửa)
Stringbuilder chỉ khác Stringbuffer ở chổ buffer là synchronized còn builder thì ko
- length của string builder luôn <= capacity của nó, nếu nó vượt quá capacity nó sẽ tự tạo ra mảng mới = 2 * (length array cũ + 1)