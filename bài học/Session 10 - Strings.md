# Session 10 - Strings

**Học phần:** Lập trình C/C++ cho Hệ thống Nhúng AI
**Buổi 10:** Chuỗi (Strings)

---

## MỤC TIÊU VÀ CHỦ ĐỀ

-   **Giới thiệu về Chuỗi:**
    -   Hiểu khái niệm và tầm quan trọng của chuỗi trong lập trình C.
-   **Khai báo và Khởi tạo Chuỗi:**
    -   Học cách khai báo và khởi tạo chuỗi bằng mảng ký tự.
-   **Các thao tác trên Chuỗi sử dụng Hàm dựng sẵn:**
    -   Sử dụng các hàm xử lý chuỗi dựng sẵn từ thư viện `<string.h>` để thao tác chuỗi.
-   **Thực hành và Hỏi đáp**

---

## GIỚI THIỆU VỀ CHUỖI (STRINGS)

### Chuỗi là gì?

-   Một nhóm các ký tự được gọi là chuỗi.
-   Chuỗi được đặt trong dấu ngoặc kép (`" "`), trong khi ký tự được đặt trong dấu ngoặc đơn (`' '`), ví dụ: `char ch = 'y';`.
-   Mỗi chuỗi trong C đều được kết thúc bằng một **ký tự NULL** (`\0`).

### Tại sao chúng ta cần Chuỗi?

-   **Xử lý Dữ liệu Văn bản:**
    -   Chuỗi rất cần thiết để lưu trữ và thao tác các thông tin dạng văn bản như tên, địa chỉ, tin nhắn, v.v.
-   **Thao tác Nhập/Xuất:**
    -   Nhiều ứng dụng trong thực tế liên quan đến việc đọc hoặc hiển thị chuỗi (ví dụ: in tên, nhập mật khẩu).
-   **Giao tiếp:**
    -   Chuỗi được sử dụng trong tin nhắn, nội dung tệp, các câu lệnh, và cả trong việc trao đổi dữ liệu giữa các hệ thống.

---

## KHAI BÁO VÀ KHỞI TẠO CHUỖI

### Khai báo Chuỗi

-   Khai báo một chuỗi trong C cũng đơn giản như khai báo một mảng một chiều.
-   **Cú pháp:** `char tên_chuỗi[kích_thước];`
-   Trong đó `tên_chuỗi` là tên của biến chuỗi và `kích_thước` xác định độ dài của chuỗi (số ký tự tối đa mà chuỗi có thể lưu trữ).

### Khởi tạo Chuỗi

Trong C, một chuỗi thực chất là một mảng ký tự kết thúc bằng ký tự `\0`.

**Ví dụ:**
`char name[] = "CRANES";`

Trình biên dịch sẽ tự động cấp phát bộ nhớ và thêm ký tự `\0` vào cuối:

| `name[0]` | `name[1]` | `name[2]` | `name[3]` | `name[4]` | `name[5]` | `name[6]` |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 'C' | 'R' | 'A' | 'N' | 'E' | 'S' | '\0' |

### Bảng các phương pháp khởi tạo chuỗi

| STT | Phương pháp | Cú pháp | Kích thước xác định? | Tự động thêm `\0`? | Ghi chú |
| :-- | :--- | :--- | :--- | :--- | :--- |
| 1 | Chuỗi ký tự (string literal) không có kích thước | `char str[] = "Hello";` | Không | Có | Trình biên dịch tự đặt kích thước và thêm `\0`. |
| 2 | Chuỗi ký tự với kích thước định sẵn | `char str[50] = "Hello";` | Có | Có | Đảm bảo kích thước >= độ dài chuỗi + 1. |
| 3 | Từng ký tự với kích thước định sẵn | `char str[6] = {'H','e','l','l','o','\0'};` | Có | Không (thủ công) | Phải tự thêm `\0` vào cuối để kết thúc chuỗi. |
| 4 | Từng ký tự không có kích thước | `char str[] = {'H','e','l','l','o','\0'};` | Không | Không (thủ công) | Trình biên dịch tính toán kích thước, nhưng `\0` vẫn phải được thêm thủ công. |

---

## CÁC CHƯƠNG TRÌNH VÍ DỤ VỀ CHUỖI

### 1. Đọc và In một chuỗi

```c
#include <stdio.h>

int main() {
    char name[20];
    printf("Nhập tên của bạn: ");
    scanf("%s", name); // Lưu ý: scanf chỉ đọc đến khoảng trắng đầu tiên.
    printf("Tên của bạn là: %s\n", name);
    return 0;
}
```
**Kết quả:**```
Nhập tên của bạn: Basavaraju
Tên của bạn là: Basavaraju
```

### 2. Tính độ dài của một chuỗi (thủ công)

```c
#include <stdio.h>

int main() {
    char str[20];
    int i = 0;
    printf("Nhập một chuỗi: ");
    scanf("%s", str);
    
    // Vòng lặp chạy cho đến khi gặp ký tự null
    while(str[i] != '\0') {
        i++;
    }
    
    printf("Độ dài của chuỗi là: %d\n", i);
    return 0;
}
```
**Kết quả:**
```
Nhập một chuỗi: Cranes
Độ dài của chuỗi là: 6
```

---

## THAO TÁC CHUỖI SỬ DỤNG CÁC HÀM DỰNG SẴN

### Hàm xử lý chuỗi trong C là gì?

-   C cung cấp một tập hợp các hàm thư viện chuẩn để thực hiện nhiều thao tác khác nhau trên chuỗi.
-   Các hàm này được khai báo trong tệp tiêu đề `<string.h>` và giúp thao tác, truy vấn các mảng ký tự (chuỗi) một cách hiệu quả.

### Bảng một số hàm xử lý chuỗi phổ biến

| Hàm | Mô tả |
| :--- | :--- |
| `strlen()` | Trả về độ dài của chuỗi (không bao gồm ký tự `\0`). |
| `strcpy()` | Sao chép một chuỗi này sang một chuỗi khác. |
| `strncpy()` | Sao chép một số lượng ký tự được chỉ định từ chuỗi này sang chuỗi khác. (An toàn hơn `strcpy`). |
| `strcat()` | Nối một chuỗi vào cuối một chuỗi khác. |
| `strncat()` | Nối một số lượng ký tự được chỉ định từ chuỗi này vào cuối chuỗi khác. (An toàn hơn `strcat`). |
| `strcmp()` | So sánh hai chuỗi theo thứ tự từ điển (dựa trên mã ASCII). |
| `strchr()` | Tìm kiếm sự xuất hiện đầu tiên của một ký tự trong chuỗi. |
| `strstr()` | Tìm kiếm sự xuất hiện đầu tiên của một chuỗi con trong chuỗi. |

### 1. Hàm `strlen()`

-   Dùng để tính độ dài của một chuỗi.
-   Đếm số lượng ký tự cho đến khi gặp ký tự `\0`.
-   Giá trị trả về không bao gồm ký tự `\0`.
-   **Cú pháp:** `strlen(chuỗi);`

### 2. Hàm `strcpy()`

-   Dùng để sao chép chuỗi nguồn (`src`) vào chuỗi đích (`dest`).
-   Sao chép tất cả các ký tự, bao gồm cả ký tự `\0`.
-   **Cú pháp:** `strcpy(dest, src);`

### 3. Hàm `strcat()`

-   Dùng để nối chuỗi nguồn (`src`) vào cuối của chuỗi đích (`dest`).
-   Chuỗi đích phải đủ lớn để chứa cả hai chuỗi.
-   **Cú pháp:** `strcat(dest, src);`

### 4. Hàm `strcmp()`

-   Dùng để so sánh hai chuỗi `s1` và `s2` theo thứ tự từ điển.
-   **Giá trị trả về:**
    -   `0` nếu `s1` và `s2` bằng nhau.
    -   Giá trị **âm** nếu `s1` nhỏ hơn `s2`.
    -   Giá trị **dương** nếu `s1` lớn hơn `s2`.
-   **Cú pháp:** `strcmp(s1, s2);`

---

## TỔNG KẾT

-   **Giới thiệu về Chuỗi:**
    -   Chuỗi là các mảng ký tự được kết thúc bằng ký tự `\0`, dùng để xử lý văn bản trong C.
-   **Khai báo và Khởi tạo Chuỗi:**
    -   Chuỗi được khai báo giống như mảng và có thể được khởi tạo bằng chuỗi ký tự hoặc chuỗi các ký tự riêng lẻ.
-   **Thao tác Chuỗi với Hàm dựng sẵn:**
    -   Các hàm như `strlen()`, `strcpy()`, `strcat()`, `strcmp()` từ thư viện `<string.h>` giúp đơn giản hóa việc xử lý chuỗi.
