# BỘ 3 ĐỀ KIỂM TRA NÂNG CAO VỀ CƠ BẢN C

---

### **ĐỀ KIỂM TRA SỐ 8 (NÂNG CAO)**
**Thời gian: 10 phút**

**Câu 1. Cho đoạn mã: `int x=5, y=0, z=5; int result = x > y && z-- > y || y;`. Giá trị của `result` và `z` sau khi thực thi là bao nhiêu?**

A. `result = 1`, `z = 5`

B. `result = 1`, `z = 4`

C. `result = 0`, `z = 5`

D. `result = 0`, `z = 4`

**Câu 2. Cho đoạn mã: `int a, b; int count = scanf("%d %d", &a, &b);`. Nếu người dùng nhập "10 20", giá trị của `count` là bao nhiêu?**

A. 10

B. 20

C. 2

D. Không xác định (Undefined)

**Câu 3. Kết quả của phép toán `12 ^ 9` (XOR thao tác bit) là bao nhiêu? (Gợi ý: 12 là `1100`, 9 là `1001`)**

A. 8

B. 21

C. 5
D. 4

**Câu 4. Xem xét đoạn mã sau, kết quả in ra màn hình là gì?**
```c
int choice = 2;
switch (choice) {
    case 1: printf("A");
    case 2: printf("B");
    case 3: printf("C"); break;
    default: printf("D");
}
```

A. B

B. C

C. BC

D. BCD

**Câu 5. Điều gì sẽ xảy ra với đoạn mã sau: `int x = 10; if (x = 0) { printf("True"); } else { printf("False"); }`?**

A. In ra "True".

B. In ra "False".

C. Lỗi biên dịch.

D. Không in ra gì cả.

**Câu 6. Cho đoạn mã: `int num; char c; printf("Nhập số: "); scanf("%d", &num); printf("Nhập ký tự: "); scanf("%c", &c);`. Tại sao hàm `scanf("%c", &c)` dường như bị bỏ qua?**

A. Do `scanf` không thể đọc ký tự sau khi đọc số.

B. Do ký tự newline (`\n`) còn lại trong bộ đệm đầu vào sau khi nhập số đã được `scanf("%c")` đọc.

C. Cần phải khởi động lại chương trình.

D. Do lỗi cú pháp.

**Câu 7. Trong một vòng lặp lồng nhau, câu lệnh `break` sẽ thoát khỏi vòng lặp nào?**

A. Vòng lặp ngoài cùng.

B. Cả hai vòng lặp.

C. Chỉ vòng lặp trong cùng chứa nó.

D. Gây ra lỗi biên dịch.

**Câu 8. Kết quả của biểu thức `'A' + 1` là gì? (Giả sử mã ASCII của 'A' là 65)**

A. Lỗi biên dịch.

B. 'B' (dưới dạng ký tự).

C. 66 (dưới dạng số nguyên).

D. Chuỗi "A1".

**Câu 9. Sự khác biệt cơ bản giữa Trình biên dịch (Compiler) và Trình liên kết (Linker) là gì?**

A. Compiler tạo mã máy từ mã nguồn, Linker thực thi chương trình.

B. Compiler kiểm tra lỗi logic, Linker kiểm tra lỗi cú pháp.

C. Compiler dịch mã nguồn sang mã đối tượng, Linker kết hợp các tệp mã đối tượng và thư viện thành một tệp thực thi duy nhất.

D. Compiler và Linker là hai tên gọi khác nhau cho cùng một công cụ.


**Câu 10. Toán tử ba ngôi nào sau đây tìm giá trị nhỏ nhất trong ba số `a`, `b`, `c`?**

A. `(a < b && a < c) ? a : (b < c ? b : c);`

B. `(a < b || a < c) ? a : (b < c ? b : c);`

C. `(a > b && a > c) ? a : (b > c ? b : c);`

D. `(a < b) ? a : (b < c ? c : b);`

---

### **ĐỀ KIỂM TRA SỐ 9 (NÂNG CAO)**
**Thời gian: 10 phút**

**Câu 1. Đầu ra của đoạn mã sau là gì: `int i = 5; printf("%d %d %d", i++, i, ++i);`?**

A. 5 6 7

B. 6 6 6

C. 7 6 5

D. Hành vi không xác định (Undefined Behavior)

**Câu 2. Vòng lặp sau sẽ in ra gì: `int i, j; for (i = 0, j = 4; i < j; i++, j--) { printf("*"); }`?**

A. **

B. ***

C. ****

D. *****

**Câu 3. Điều gì xảy ra khi bạn cố gắng ghi dữ liệu vào một file được mở bằng chế độ `"r"`?**

A. Dữ liệu sẽ được ghi vào đầu file.

B. Dữ liệu sẽ được nối vào cuối file.

C. Chương trình sẽ gặp lỗi thời gian chạy hoặc hành vi không xác định.

D. File sẽ tự động được mở lại ở chế độ `"w"`.

**Câu 4. Cho đoạn mã: `int x = 0; if (x != 0 && (10 / x) > 1) { ... }`. Phép chia `10 / x` có được thực hiện không?**

A. Có, và gây ra lỗi chia cho không.

B. Không, do cơ chế đánh giá đoản mạch (short-circuit evaluation) của toán tử `&&`.

C. Tùy thuộc vào trình biên dịch.

D. Có, nhưng C sẽ tự động xử lý lỗi chia cho không.

**Câu 5. Vai trò chính của từ khóa `const` khi khai báo biến là gì (ví dụ `const int x = 10;`)?**

A. Làm cho biến có thể truy cập từ các file khác.

B. Thông báo cho trình biên dịch rằng giá trị của biến sẽ không thay đổi sau khi khởi tạo.

C. Cấp phát bộ nhớ cho biến trên heap thay vì stack.

D. Tăng tốc độ truy cập biến.

**Câu 6. Đoạn mã sau sẽ in ra màn hình bao nhiêu lần: `int i = 10; do { printf("Hello"); } while (i < 10);`?**

A. 0 lần

B. 1 lần

C. 10 lần

D. Vô hạn lần

**Câu 7. Kết quả của phép toán NOT thao tác bit `~5` là gì? (Gợi ý: 5 là `0...0101`)**

A. 5

B. 10

C. -5

D. -6

**Câu 8. Sự khác biệt về logic giữa "bậc thang if-else-if" và một "chuỗi các câu lệnh if độc lập" là gì?**

A. Không có sự khác biệt.

B. Trong bậc thang `if-else-if`, chỉ có một khối mã được thực thi. Trong chuỗi các `if`, nhiều khối mã có thể được thực thi.

C. Chuỗi các `if` hiệu quả hơn.

D. Bậc thang `if-else-if` chỉ dùng cho số nguyên, chuỗi `if` dùng cho mọi kiểu dữ liệu.

**Câu 9. Tại sao mã giả (Pseudocode) lại hữu ích trong giai đoạn đầu của việc phát triển phần mềm?**

A. Nó có thể được biên dịch trực tiếp để kiểm tra lỗi.

B. Nó cho phép lập trình viên tập trung vào logic giải quyết vấn đề mà không bị ràng buộc bởi cú pháp của một ngôn ngữ cụ thể.

C. Nó là một yêu cầu bắt buộc của tiêu chuẩn lập trình C.

D. Nó tự động tạo ra lưu đồ.

**Câu 10. Sắp xếp các kiểu dữ liệu sau theo thứ tự tiêu thụ bộ nhớ từ ít nhất đến nhiều nhất (trên một hệ thống 64-bit điển hình):**

A. `char`, `int`, `long`, `double`

B. `char`, `long`, `int`, `double`

C. `int`, `char`, `double`, `long`

D. `double`, `long`, `int`, `char`

---

### **ĐỀ KIỂM TRA SỐ 10 (NÂNG CAO)**
**Thời gian: 10 phút**

**Câu 1. Vòng lặp sau thực thi bao nhiêu lần? `for (int i = 0; i < 10; i++) { i++; }`**

A. 10 lần

B. 5 lần

C. Vòng lặp vô hạn

D. 6 lần

**Câu 2. Giá trị của `result` trong biểu thức sau là bao nhiêu: `int result = 5 | 3 & 1;`?**

A. 1

B. 5

C. 7

D. 4

**Câu 3. Sự khác biệt về kết quả giữa `float y = 5 / 2;` và `float y = (float)5 / 2;` là gì?**

A. Cả hai đều cho `y = 2.5`.

B. Dòng đầu tiên cho `y = 2.0`, dòng thứ hai cho `y = 2.5`.

C. Dòng đầu tiên cho `y = 2.5`, dòng thứ hai cho `y = 2.0`.

D. Cả hai đều gây ra lỗi biên dịch.

**Câu 4. Mục đích chính của `return 0;` ở cuối hàm `main()` là gì?**

A. Để trả về giá trị 0 cho một hàm đã gọi nó.

B. Để báo cho hệ điều hành biết rằng chương trình đã kết thúc thành công.

C. Để giải phóng toàn bộ bộ nhớ đã được cấp phát.

D. Nó là một yêu cầu cú pháp bắt buộc nhưng không có ý nghĩa thực tế.

**Câu 5. Vòng lặp sau sẽ dừng khi nào: `int x = 5; while (x--) { ... }`?**

A. Vòng lặp chạy vô hạn.

B. Vòng lặp chạy 5 lần.

C. Vòng lặp chạy 4 lần.

D. Vòng lặp không chạy lần nào.

**Câu 6. Sự khác biệt chính về vòng đời (lifetime) giữa một biến `static` và một biến `auto` (biến cục bộ thông thường) bên trong một hàm là gì?**

A. Biến `auto` tồn tại suốt chương trình, biến `static` chỉ tồn tại trong một lần gọi hàm.

B. Biến `static` tồn tại suốt chương trình, biến `auto` được tạo lại mỗi khi hàm được gọi.

C. Không có sự khác biệt về vòng đời.

D. Biến `static` được lưu trên heap, biến `auto` lưu trên stack.

**Câu 7. Tại sao "Tính di động" (Portability) lại là một đặc điểm của ngôn ngữ C?**

A. Vì mã C có thể chạy trên mọi hệ điều hành mà không cần biên dịch lại.

B. Vì mã nguồn C có thể được biên dịch và chạy trên nhiều kiến trúc máy tính khác nhau với ít hoặc không cần thay đổi.

C. Vì trình biên dịch C được tích hợp sẵn trong mọi hệ điều hành.

D. Vì C là ngôn ngữ bậc thấp nhất.

**Câu 8. Lỗi nào sau đây thuộc loại "Lỗi thời gian chạy" (Runtime Error)?**

A. Thiếu dấu chấm phẩy `;`.

B. Sử dụng `=` thay vì `==` trong câu lệnh `if`.

C. Cố gắng chia một số cho 0.

D. Sử dụng một từ khóa làm tên biến.

**Câu 9. Thành phần nào của quá trình biên dịch chịu trách nhiệm xử lý các chỉ thị như `#include` và `#define`?**

A. Trình biên dịch (Compiler)

B. Trình liên kết (Linker)

C. Bộ tiền xử lý (Preprocessor)

D. Trình gỡ lỗi (Debugger)

**Câu 10. Cho hai số nguyên `x` và `y`. Biểu thức nào sau đây kiểm tra xem CHÍNH XÁC một trong hai số là dương (lớn hơn 0)?**

A. `(x > 0) && (y > 0)`

B. `(x > 0) || (y > 0)`

C. `(x > 0) ^ (y > 0)` (sử dụng XOR logic)

D. `(x > 0) != (y > 0)`

---
---

### **ĐÁP ÁN VÀ GIẢI THÍCH (BỘ ĐỀ NÂNG CAO)**

#### **ĐÁP ÁN ĐỀ 8**

1.  **A. `result = 1`, `z = 5`**
    *   **Lý giải:** Do cơ chế đoản mạch, biểu thức `x > y` (5 > 0) là đúng. Sau đó `z-- > y` (5 > 0) cũng đúng. Vì `&&` đúng, toàn bộ vế trái của `||` là đúng. Do đó, vế phải (`|| y`) không được đánh giá. `result` là 1. Vì `z--` là hậu tố, `z` được sử dụng (giá trị 5) để so sánh trước, *nhưng vì vế sau không được đánh giá*, phép giảm `z` không bao giờ được thực thi. `z` vẫn là 5.
    *   **Nguồn:** Bài 3, Slide 10, 11, 21.
2.  **C. 2**
    *   **Lý giải:** Hàm `scanf()` trả về số lượng mục dữ liệu đã được đọc và gán thành công. Trong trường hợp này, nó đọc thành công 2 số nguyên.
    *   **Nguồn:** Bài 4 (khái niệm nâng cao về hàm).
3.  **C. 5**
    *   **Lý giải:** `1100 XOR 1001 = 0101`, giá trị thập phân là 5.
    *   **Nguồn:** Bài 3, Slide 15.
4.  **C. BC**
    *   **Lý giải:** `switch` sẽ nhảy đến `case 2`. Vì không có `break`, nó sẽ tiếp tục thực thi `case 3` (hiện tượng "fall-through"). Nó sẽ dừng lại khi gặp `break`.
    *   **Nguồn:** Bài 5, Slide 15.
5.  **B. In ra "False".**
    *   **Lý giải:** Biểu thức `x = 0` là một phép gán, không phải so sánh. Giá trị của phép gán này là giá trị được gán, tức là 0. Trong C, 0 được coi là `false`. Do đó, khối `else` được thực thi.
    *   **Nguồn:** Bài 5, Slide 30 (Lỗi logic).
6.  **B. Do ký tự newline (`\n`) còn lại trong bộ đệm đầu vào sau khi nhập số đã được `scanf("%c")` đọc.**
    *   **Lý giải:** Đây là một lỗi phổ biến. Khi bạn nhập một số và nhấn Enter, `scanf("%d")` chỉ đọc số đó, để lại ký tự `\n` trong bộ đệm. `scanf("%c")` tiếp theo sẽ đọc ngay ký tự `\n` đó.
    *   **Nguồn:** Bài 4 (hành vi nâng cao của I/O).
7.  **C. Chỉ vòng lặp trong cùng chứa nó.**
    *   **Lý giải:** `break` chỉ ảnh hưởng đến cấu trúc lặp hoặc `switch` gần nhất chứa nó.
    *   **Nguồn:** Bài 6, Slide 9, 12.
8.  **C. 66 (dưới dạng số nguyên).**
    *   **Lý giải:** Đây là một ví dụ về thăng hạng kiểu ngầm định. Ký tự `'A'` được thăng hạng thành giá trị ASCII số nguyên của nó (65) trước khi thực hiện phép cộng. Kết quả là một số nguyên.
    *   **Nguồn:** Bài 2, Slide 18.
9.  **C. Compiler dịch mã nguồn sang mã đối tượng, Linker kết hợp các tệp mã đối tượng và thư viện thành một tệp thực thi duy nhất.**
    *   **Lý giải:** Đây là vai trò riêng biệt của hai giai đoạn trong quá trình xây dựng chương trình.
    *   **Nguồn:** Bài 1, Slide 4, 24.
10. **A. `(a < b && a < c) ? a : (b < c ? b : c);`**
    *   **Lý giải:** Đây là logic lồng nhau đúng. Đầu tiên kiểm tra `a` có phải nhỏ nhất không. Nếu không, so sánh `b` và `c` để tìm ra số nhỏ hơn.
    *   **Nguồn:** Bài 5, Slide 19, 22.

#### **ĐÁP ÁN ĐỀ 9**

1.  **D. Hành vi không xác định (Undefined Behavior)**
    *   **Lý giải:** Tiêu chuẩn C không xác định thứ tự các đối số của một hàm được đánh giá. Việc sửa đổi và đọc cùng một biến nhiều lần giữa hai "điểm tuần tự" (sequence points) dẫn đến hành vi không xác định. Kết quả có thể khác nhau tùy trình biên dịch.
    *   **Nguồn:** Bài 3 (khái niệm cực kỳ nâng cao về toán tử).
2.  **A. ** **
    *   **Lý giải:** Vòng lặp sẽ chạy khi `i < j`. Các cặp giá trị (i, j) sẽ là (0, 4) -> in *, (1, 3) -> in *. Khi i=2, j=2, điều kiện `i < j` là sai, vòng lặp dừng.
    *   **Nguồn:** Bài 6, Slide 7 (kết hợp logic).
3.  **C. Chương trình sẽ gặp lỗi thời gian chạy hoặc hành vi không xác định.**
    *   **Lý giải:** Mở file ở chế độ chỉ đọc (`"r"`) không cho phép ghi. Mọi nỗ lực ghi sẽ thất bại.
    *   **Nguồn:** Bài 4, Slide 13.
4.  **B. Không, do cơ chế đánh giá đoản mạch (short-circuit evaluation) của toán tử `&&`.**
    *   **Lý giải:** Vì `x != 0` là sai, toàn bộ biểu thức `&&` không thể là đúng, do đó phần bên phải (`10 / x`) sẽ không được đánh giá, tránh được lỗi chia cho không.
    *   **Nguồn:** Bài 3, Slide 10.
5.  **B. Thông báo cho trình biên dịch rằng giá trị của biến sẽ không thay đổi sau khi khởi tạo.**
    *   **Lý giải:** `const` là viết tắt của constant (hằng số). Bất kỳ nỗ lực nào để thay đổi giá trị của biến `const` sau này sẽ gây ra lỗi biên dịch.
    *   **Nguồn:** Bài 2, Slide 4 (từ khóa).
6.  **B. 1 lần**
    *   **Lý giải:** Vòng lặp `do-while` luôn thực thi thân vòng lặp ít nhất một lần trước khi kiểm tra điều kiện.
    *   **Nguồn:** Bài 6, Slide 6, 8.
7.  **D. -6**
    *   **Lý giải:** Toán tử `~` đảo ngược tất cả các bit. Trong biểu diễn bù hai, `~x` tương đương với `-(x+1)`. Vì vậy, `~5` là `-(5+1)`, tức là `-6`.
    *   **Nguồn:** Bài 3, Slide 15, 17.
8.  **B. Trong bậc thang `if-else-if`, chỉ có một khối mã được thực thi. Trong chuỗi các `if`, nhiều khối mã có thể được thực thi.**
    *   **Lý giải:** Bậc thang `if-else-if` là loại trừ lẫn nhau. Chuỗi các `if` độc lập kiểm tra từng điều kiện riêng biệt.
    *   **Nguồn:** Bài 5, Slide 13 (so sánh logic).
9.  **B. Nó cho phép lập trình viên tập trung vào logic giải quyết vấn đề mà không bị ràng buộc bởi cú pháp của một ngôn ngữ cụ thể.**
    *   **Lý giải:** Đây là mục đích chính và lợi ích lớn nhất của mã giả.
    *   **Nguồn:** Bài 1, Slide 11.
10. **A. `char`, `int`, `long`, `double`**
    *   **Lý giải:** Trên hệ 64-bit điển hình: `char` (1 byte), `int` (4 bytes), `long` (thường là 8 bytes, nhưng ít nhất là 4), `double` (8 bytes).
    *   **Nguồn:** Bài 2, Slide 7, 8.

#### **ĐÁP ÁN ĐỀ 10**

1.  **B. 5 lần**
    *   **Lý giải:** Biến `i` được tăng hai lần trong mỗi lần lặp (một lần ở bước cập nhật `i++`, một lần trong thân `i++`). Các giá trị của `i` ở đầu mỗi lần lặp sẽ là 0, 2, 4, 6, 8. Lần lặp tiếp theo, `i` là 10, điều kiện `i < 10` sai. Vòng lặp chạy 5 lần.
    *   **Nguồn:** Bài 6, Slide 7 (hành vi nâng cao của vòng lặp).
2.  **B. 5**
    *   **Lý giải:** Theo độ ưu tiên, `&` được thực hiện trước `|`. `3 & 1` (nhị phân `011 & 001`) là `1`. Sau đó, `5 | 1` (nhị phân `101 | 001`) là `101`, tức là 5.
    *   **Nguồn:** Bài 3, Slide 21.
3.  **B. Dòng đầu tiên cho `y = 2.0`, dòng thứ hai cho `y = 2.5`.**
    *   **Lý giải:** Ở dòng đầu, `5 / 2` là phép chia số nguyên, cho kết quả `2`. Sau đó `2` được chuyển đổi ngầm định thành `2.0` và gán cho `y`. Ở dòng hai, `(float)5` ép số 5 thành số thực, do đó phép chia là phép chia số thực, cho kết quả `2.5`.
    *   **Nguồn:** Bài 2, Slide 19 và Bài 3, Slide 5.
4.  **B. Để báo cho hệ điều hành biết rằng chương trình đã kết thúc thành công.**
    *   **Lý giải:** Theo quy ước, giá trị trả về 0 từ `main` cho biết chương trình đã chạy mà không gặp lỗi. Các giá trị khác thường chỉ ra một loại lỗi nào đó.
    *   **Nguồn:** Bài 1, Slide 22, 23.
5.  **B. Vòng lặp chạy 5 lần.**
    *   **Lý giải:** `while(x--)` kiểm tra giá trị của `x` trước, sau đó giảm `x`. Vòng lặp sẽ chạy khi `x` là 5, 4, 3, 2, 1. Khi `x` là 0, điều kiện trở thành sai và vòng lặp dừng.
    *   **Nguồn:** Bài 6, Slide 5 (hành vi nâng cao của điều kiện).
6.  **B. Biến `static` tồn tại suốt chương trình, biến `auto` được tạo lại mỗi khi hàm được gọi.**
    *   **Lý giải:** Biến `static` chỉ được khởi tạo một lần và giữ giá trị của nó giữa các lần gọi hàm. Biến `auto` (mặc định) bị hủy khi hàm kết thúc.
    *   **Nguồn:** Bài 2, Slide 4 (từ khóa, khái niệm nâng cao).
7.  **B. Vì mã nguồn C có thể được biên dịch và chạy trên nhiều kiến trúc máy tính khác nhau với ít hoặc không cần thay đổi.**
    *   **Lý giải:** Tính di động (portability) đề cập đến khả năng biên dịch lại mã nguồn trên các nền tảng khác nhau.
    *   **Nguồn:** Bài 1, Slide 26 (ngụ ý trong các đặc điểm).
8.  **C. Cố gắng chia một số cho 0.**
    *   **Lý giải:** Đây là lỗi chỉ có thể được phát hiện khi chương trình đang chạy (runtime), không thể phát hiện lúc biên dịch. A và D là lỗi cú pháp. B là lỗi logic.
    *   **Nguồn:** Bài 5, Slide 30.
9.  **C. Bộ tiền xử lý (Preprocessor)**
    *   **Lý giải:** Bộ tiền xử lý là giai đoạn đầu tiên của quá trình biên dịch, có nhiệm vụ xử lý các dòng mã bắt đầu bằng `#`.
    *   **Nguồn:** Bài 1, Slide 21, 22.
10. **D. `(x > 0) != (y > 0)`**
    *   **Lý giải:** Biểu thức `(x > 0)` và `(y > 0)` sẽ trả về 0 hoặc 1. So sánh `!=` (khác nhau) sẽ chỉ đúng khi một bên là 1 và bên kia là 0, tức là chính xác một trong hai số là dương. `(x > 0) ^ (y > 0)` cũng đúng về mặt logic, nhưng `!=` là cách phổ biến và rõ ràng hơn.
    *   **Nguồn:** Bài 3 (toán tử logic và quan hệ).
