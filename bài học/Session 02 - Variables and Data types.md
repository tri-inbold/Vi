# Session 2 - Variables and Data types

### **Slide 1: Trang bìa**

**Cranes Varsity**
'Nơi Công Nghệ Gặp Gỡ Sự Hoàn Hảo'

**Chương trình:**
Chương trình Phát triển Phần mềm Ô tô

**Học kỳ 1:**
Chứng chỉ Phát triển Phần mềm Ô tô (CAS)

**Học phần:**
Lập trình C/C++ cho Hệ thống Nhúng AI

**Buổi 02:**
Biến và Kiểu dữ liệu

---

### **Slide 2: Mục tiêu Buổi học**

**MỤC TIÊU BUỔI HỌC**
**Mục tiêu của buổi học là**

| Khai báo và Khởi tạo Biến | Kiểu dữ liệu | Sử dụng Định dạng Chỉ định trong Nhập và Xuất | Phân biệt Chuyển đổi Kiểu Ngầm định và Tường minh |
| :--- | :--- | :--- | :--- |
| Biến trong C chỉ là một vị trí lưu trữ có tên trong bộ nhớ, nơi bạn có thể lưu trữ dữ liệu có thể thay đổi trong quá trình thực thi chương trình. | Kiểu dữ liệu trong C cho trình biên dịch biết loại dữ liệu mà một biến có thể chứa — như số nguyên, số thực, ký tự, v.v. | Một định dạng chỉ định cho các hàm `printf()` và `scanf()` biết bạn đang làm việc với loại dữ liệu nào (số nguyên, số thực, ký tự, chuỗi, v.v.). | Chuyển đổi một kiểu dữ liệu này sang một kiểu dữ liệu khác. |

---

### **Slide 3: Biến**

**Tổng quan về Biến và Kiểu dữ liệu trong C**

**Biến**
*   **Biến** là một tên được gán cho một vị trí bộ nhớ lưu trữ một giá trị.
*   Nó cho phép các lập trình viên lưu trữ, sửa đổi và truy xuất dữ liệu trong quá trình thực thi chương trình.

**Mục đích của Biến**
*   Để lưu trữ dữ liệu (số, ký tự, v.v.).
*   Để cho phép **thay đổi giá trị động** trong quá trình thực thi.
*   Để cải thiện **khả năng đọc và tái sử dụng mã**.

**Ví dụ:**
`int age = 25; // "age" là một biến lưu trữ giá trị số nguyên 25`
`float price = 99.99; // "price" là một biến lưu trữ giá trị số thực`

---

### **Slide 4: Từ khóa**

**Tổng quan về Biến và Kiểu dữ liệu trong C**

**Từ khóa**
*   **"Từ khóa"** là những từ có ý nghĩa đặc biệt đối với trình biên dịch C.
*   Những từ khóa này phải được sử dụng trong chương trình cho các mục đích cụ thể dựa trên định nghĩa.
*   Các từ khóa còn được gọi là **từ dành riêng (reserved words)**.
*   Có 32 từ khóa trong C tiêu chuẩn.

| | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| auto | break | case | default | do | double | else |
| enum | extern | for | int | float | long | return |
| short | signed | unsigned | sizeof | static | struct | switch |
| typedef | union | void | volatile | while | char | register |
| const | if | continue | goto | | | |

---

### **Slide 5: Kiểu dữ liệu**

**Hiểu về các Kiểu dữ liệu khác nhau và cách sử dụng chúng**

**Kiểu dữ liệu**

**Kiểu dữ liệu** là một phân loại định nghĩa:
*   Loại giá trị mà một biến có thể lưu trữ.
*   Cách các giá trị được lưu trữ trong bộ nhớ.
*   Phạm vi các hoạt động có thể được thực hiện trên các giá trị.

---

### **Slide 6: Phân loại Kiểu dữ liệu**

**Hiểu về các Kiểu dữ liệu khác nhau và cách sử dụng chúng (tiếp...)**

**Phân loại Kiểu dữ liệu**

[Sơ đồ các Kiểu dữ liệu trong C]
*   **Kiểu dữ liệu do người dùng định nghĩa:**
    *   structure (cấu trúc)
    *   union (hợp)
    *   enum (liệt kê)
*   **Kiểu dữ liệu Cơ bản:**
    *   int
    *   char
    *   float
    *   double
*   **Kiểu dữ liệu Thứ cấp:**
    *   array (mảng)
    *   pointer (con trỏ), v.v.

---

### **Slide 7: Phân loại Kiểu dữ liệu (tiếp...)**

**Kiểu dữ liệu Cơ bản**

| Kiểu dữ liệu Cơ bản | Từ khóa | Mô tả | Kích thước | Ví dụ |
| :--- | :--- | :--- | :--- | :--- |
| **Ký tự (Character)** | `char` | Kiểu dữ liệu này được sử dụng khi cần các giá trị ký tự. | 1 Byte | `char choice = 'y';` <br> `char name[20];` |
| **Số nguyên (Integer)** | `int` | Kiểu dữ liệu này chỉ có thể lưu trữ các số nguyên. Nó không xem xét phần thập phân. | 2 Byte (thường là 4 Byte trên hệ thống hiện đại) | `int age;` |

---

### **Slide 8: Phân loại Kiểu dữ liệu (tiếp...)**

**Kiểu dữ liệu Cơ bản (tiếp)**

| Kiểu dữ liệu Cơ bản | Từ khóa | Mô tả | Kích thước | Ví dụ |
| :--- | :--- | :--- | :--- | :--- |
| **Số thực / Số chấm động (Floating / Real Numbers)** | `float` | Kiểu dữ liệu này có thể lưu trữ/đọc các giá trị phân số. Nó có thể có độ chính xác lên đến 6 chữ số thập phân. | 4 Byte | `float sal;` <br> `float height;` |
| **Số thực kép (Double)** | `double` | Tương tự như số chấm động. Nó có thể có độ chính xác lên đến 8 (thường là 15) chữ số thập phân. | 8 Byte | `double sal;` <br> `double speed;` |

---

### **Slide 9: Phân loại Kiểu dữ liệu (tiếp...)**

**Kiểu dữ liệu Thứ cấp**

| Kiểu dữ liệu Thứ cấp | Ví dụ | Mô tả | Kích thước (Thường gặp) |
| :--- | :--- | :--- | :--- |
| **Mảng (Array) `[]`** | `char name[20];` | Kiểu dữ liệu này được sử dụng khi cần các giá trị ký tự. | 20 Byte |
| **Con trỏ (Pointers) `*ptr`** | `int a;` <br> `int *p=&a;` | Kiểu dữ liệu này có thể lưu trữ địa chỉ của một biến khác. | 8 byte (trên hệ thống 64-bit) |

---

### **Slide 10: Quy tắc Khai báo Biến**

**Khai báo và khởi tạo biến một cách chính xác**

**Quy tắc Khai báo Biến**
*   Tên biến không được bắt đầu bằng số.
    *   Ví dụ: `int 1a; //không hợp lệ`
*   Tên biến không được bắt đầu bằng các ký tự đặc biệt ngoại trừ dấu gạch dưới `_` và `$`.
    *   Ví dụ: `int #a; //không hợp lệ`
*   Tên biến có phân biệt chữ hoa chữ thường.
    *   Ví dụ: `int a; A=10; // A khác a nên nó là một ký hiệu chưa được định nghĩa`
*   Từ khóa không được sử dụng làm tên biến.
    *   Ví dụ: `int int; //không hợp lệ`
*   Tên biến không thể có khoảng trắng.
    *   Ví dụ: `char First Name[20]; //không hợp lệ`

---

### **Slide 11: Quy tắc Khai báo Biến (tiếp...)**

**Khai báo và khởi tạo biến một cách chính xác**

**Cú pháp:**
`kiểu_dữ_liệu tên_biến = <giá_trị>;`
**Ví dụ:** `int x = 4;`

Ở đây `x` là một biến kiểu số nguyên và giá trị được lưu trữ trong `x` là 4.

---

### **Slide 12: Ví dụ về Tên Biến Hợp lệ và Không hợp lệ**

**Khai báo và khởi tạo biến một cách chính xác**

| ✅ Hợp lệ | ❌ Không hợp lệ |
| :--- | :--- |
| `count` | `1count` (bắt đầu bằng một chữ số) |
| `_score` | `float` (từ khóa dành riêng) |
| `num_1` | `total marks` (chứa khoảng trắng) |
| `value_2024` | `@price` (chứa ký tự đặc biệt) |

---

### **Slide 13: Chương trình Ví dụ**

**Khai báo và khởi tạo biến một cách chính xác**

**Chương trình minh họa (khai báo, khởi tạo, in biến ra console.)**
```c
#include <stdio.h>
int main()
{
    int age;
    age = 25;
    printf("Tuổi: %d tuổi", age);
    return 0;
}
```

---

### **Slide 14: Định dạng Chỉ định**

**Sử dụng định dạng chỉ định (%d, %f, %c, %s, v.v.) trong `printf()` và `scanf()`**

**Định dạng Chỉ định (Format Specifiers)**

Định dạng chỉ định là các giữ chỗ được sử dụng bên trong các chuỗi để chỉ ra cách một giá trị nên được định dạng khi được chèn vào chuỗi. Chúng rất phổ biến khi bạn muốn hiển thị số, chuỗi, ngày tháng, hoặc dữ liệu khác theo một cách nhất định.

---

### **Slide 15: Bảng Định dạng Chỉ định (phần 1)**

**Sử dụng định dạng chỉ định (%d, %f, %c, %s, v.v.) trong `printf()` và `scanf()`**

| Kiểu dữ liệu | Mô tả | Định dạng Chỉ định |
| :--- | :--- | :--- |
| **int** | Số nguyên (số nguyên) | `%d` hoặc `%i` |
| **float** | Số chấm động (độ chính xác đơn) | `%f` |
| **double** | Số chấm động (độ chính xác kép) | `%lf` |
| **char** | Ký tự đơn | `%c` |
| **unsigned long**| Số nguyên dương lớn | `%lu` |
| **unsigned char**| Ký tự đơn (0 đến 255) | `%c` |
| **void** | Không có giá trị (sử dụng trong hàm) | N/A |

---

### **Slide 16: Bảng Định dạng Chỉ định (phần 2)**

**Sử dụng định dạng chỉ định (%d, %f, %c, %s, v.v.) trong `printf()` và `scanf()`**

| Kiểu dữ liệu | Mô tả | Định dạng Chỉ định |
| :--- | :--- | :--- |
| **char[] (string)**| Chuỗi (mảng ký tự) | `%s` |
| **short** | Số nguyên ngắn (nhỏ hơn int) | `%hd` |
| **long** | Số nguyên dài (lớn hơn int) | `%ld` |
| **long long** | Số nguyên rất lớn | `%lld` |
| **unsigned int** | Chỉ các giá trị số nguyên dương | `%u` |

---

### **Slide 17: Chương trình Ví dụ về Định dạng Chỉ định**

**Chương trình đọc các loại dữ liệu khác nhau để minh họa các định dạng chỉ định**
```c
#include <stdio.h>
int main()
{
    int num;
    float pi;
    char letter;
    char name[20];

    //Đọc giá trị số nguyên, số thực và ký tự bằng %d, %f và %c
    printf("Nhập một số nguyên, một số thực và một ký tự: ");
    scanf("%d %f %c", &num, &pi, &letter);
    printf("Bạn đã nhập: %d, %.2f, %c\n", num, pi, letter);

    //Đọc một chuỗi bằng %s
    printf("Nhập tên của bạn: ");
    scanf("%s", name); // Không cần & cho chuỗi
    printf("Tên bạn đã nhập là: %s ", name);

    return 0;
}
```

---

### **Slide 18: Chuyển đổi Kiểu Ngầm định và Tường minh**

**Phân biệt giữa chuyển đổi kiểu ngầm định (tự động) và tường minh (thủ công)**

**Chuyển đổi Kiểu Ngầm định và Tường minh**

Chuyển đổi kiểu trong C đề cập đến việc chuyển đổi một kiểu dữ liệu này sang một kiểu dữ liệu khác. Có hai loại:
**1. Chuyển đổi Kiểu Ngầm định (Chuyển đổi Tự động)**
**2. Chuyển đổi Kiểu Tường minh (Ép kiểu Thủ công)**

**1. Chuyển đổi Kiểu Ngầm định (Tự động)**
*   Xảy ra **tự động** khi một kiểu dữ liệu nhỏ hơn được gán cho một kiểu dữ liệu lớn hơn.
*   **Không mất dữ liệu** xảy ra trong các chuyển đổi mở rộng.
*   Ví dụ: `int` → `float` hoặc `char` → `int`.

---

### **Slide 19: Ví dụ về Chuyển đổi Kiểu**

**Ví dụ về: Chuyển đổi Ngầm định và Tường minh**
```c
//Chuyển đổi Ngầm định và Tường minh
#include <stdio.h>
int main() {
    float num = 10.75;
    int result;

    result = (int) num; // Chuyển đổi tường minh từ float sang int

    printf("Số thực ban đầu: %f\n", num);
    printf("Số nguyên đã chuyển đổi: %d\n", result);
    return 0;
}
```
**Đầu ra:**
```
Số thực ban đầu: 10.750000
Số nguyên đã chuyển đổi: 10
```
**Giải thích:**
Phép ép kiểu `(int)` buộc chuyển đổi `num` từ `float` sang `int`, **cắt bỏ phần thập phân**.

---

### **Slide 20: Sự khác biệt chính giữa các loại Chuyển đổi**

**Phân biệt giữa chuyển đổi kiểu ngầm định (tự động) và tường minh (thủ công)**

| Đặc điểm | Chuyển đổi Ngầm định | Chuyển đổi Tường minh |
| :--- | :--- | :--- |
| **Kích hoạt** | Tự động | Thủ công (sử dụng ép kiểu) |
| **Cú pháp** | Xảy ra ngầm định | `(kiểu)` giá_trị |
| **Mất dữ liệu**| Không mất dữ liệu (trong chuyển đổi mở rộng) | Có thể mất dữ liệu (trong chuyển đổi thu hẹp) |
| **Ví dụ** | `int` → `float` | `float` → `(int)` |

---

### **Slide 21: Tóm tắt**

**TÓM TẮT**

Trong buổi 2 này, chúng ta đã học về các kiểu dữ liệu dùng để lưu trữ các giá trị của các loại khác nhau. Chúng ta cũng đã học cách in các giá trị của các kiểu dữ liệu khác nhau bằng cách sử dụng các định dạng chỉ định.

Chúng ta cũng học cách đọc các giá trị của các kiểu dữ liệu khác nhau bằng cách sử dụng các định dạng chỉ định và câu lệnh `scanf()`, cũng như chuyển đổi kiểu dữ liệu ngầm định và tường minh.

---

### **Slide 22: Cảm ơn**

**CẢM ƠN**
