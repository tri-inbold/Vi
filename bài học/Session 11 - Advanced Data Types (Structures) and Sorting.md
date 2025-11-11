# Session 11 - Advanced Data Types (Structures) and Sorting

**Học phần:** Lập trình C/C++ cho Hệ thống Nhúng AI
**Buổi 11:** Các kiểu dữ liệu nâng cao (Cấu trúc) và Sắp xếp

---

## MỤC TIÊU VÀ CHỦ ĐỀ

-   **Giới thiệu về Cấu trúc (Structures):**
    -   Hiểu mục đích và cách sử dụng cấu trúc trong C để nhóm các kiểu dữ liệu khác nhau.
-   **Khai báo, Khởi tạo và Truy cập Cấu trúc:**
    -   Học cách khai báo, khởi tạo và truy cập các thành viên của cấu trúc bằng biến và con trỏ.
-   **Các khái niệm và Thuật toán Sắp xếp:**
    -   Nắm bắt tầm quan trọng và các ứng dụng thực tế của việc sắp xếp.
    -   Triển khai Sắp xếp nổi bọt (Bubble Sort), Sắp xếp chọn (Selection Sort), và Sắp xếp chèn (Insertion Sort) cho mảng và mảng cấu trúc.
-   **Thực hành và Hỏi đáp**

---

## GIỚI THIỆU VỀ CẤU TRÚC (STRUCTURES)

### Cấu trúc là gì?

-   Cấu trúc trong C là một **kiểu dữ liệu do người dùng định nghĩa**, cho phép nhóm các biến có kiểu dữ liệu khác nhau dưới một tên duy nhất.

### Tại sao chúng ta cần Cấu trúc?

-   **Để nhóm các dữ liệu liên quan:**
    -   Không giống như mảng (chỉ lưu trữ các phần tử cùng kiểu), cấu trúc giúp nhóm nhiều biến liên quan có các kiểu khác nhau. Ví dụ: thông tin một sinh viên bao gồm mã số (int), tên (chuỗi ký tự), và điểm số (float).
-   **Mô hình hóa thế giới thực:**
    -   Giúp biểu diễn các thực thể như sinh viên, nhân viên, sách, v.v., vốn có nhiều thuộc tính đa dạng.

---

## KHAI BÁO, ĐỊNH NGHĨA VÀ KHỞI TẠO CẤU TRÚC

### 1. Định nghĩa Cấu trúc

-   Một cấu trúc được định nghĩa bằng từ khóa `struct`, theo sau là tên cấu trúc và các thành viên (biến) của nó được đặt trong dấu ngoặc nhọn `{}`.
-   Đây chỉ là một **khuôn mẫu (template)**, chưa có bộ nhớ nào được cấp phát tại thời điểm định nghĩa.

**Ví dụ:**

```c
struct Student
{
    int id;
    char name[20];
    float marks;
};
```

### 2. Khai báo Biến Cấu trúc

Sau khi định nghĩa cấu trúc, bạn có thể tạo ra các biến thuộc kiểu cấu trúc đó.

```c
// Khai báo hai biến s1 và s2 có kiểu struct Student
struct Student s1, s2;
```

Hoặc có thể định nghĩa và khai báo biến cùng lúc:

```c
struct Student {
    int id;
    char name[20];
    float marks;
} s1, s2;
```

### 3. Khởi tạo Cấu trúc

**Lưu ý quan trọng:** Không thể khởi tạo giá trị cho các thành viên ngay bên trong phần định nghĩa `struct`.

**Cách khởi tạo đúng:**

**a. Khởi tạo tại thời điểm khai báo biến:**

-   Bạn gán các giá trị cho thành viên cấu trúc khi bạn khai báo biến.

```c
struct Student s1 = {101, "John", 88.5};
```

**b. Khởi tạo sau khi khai báo (sử dụng toán tử dấu chấm `.`):**

-   Bạn khai báo biến cấu trúc trước, sau đó gán giá trị cho từng thành viên một cách riêng lẻ.

```c
struct Student s2;

s2.id = 102;
// Phải dùng hàm strcpy cho thành viên chuỗi
strcpy(s2.name, "Alice");
s2.marks = 90.0;
```
**c. Khởi tạo một phần:**
- Bạn có thể chỉ khởi tạo một vài thành viên đầu tiên. Các thành viên còn lại sẽ được tự động gán giá trị mặc định (0 cho số, `\0` cho ký tự).

```c
struct Student s3 = {103}; // Chỉ khởi tạo id, name và marks sẽ là mặc định.
```

---

## MẢNG CẤU TRÚC (ARRAY OF STRUCTURES)

Khi cần làm việc với nhiều mục dữ liệu có cùng kiểu cấu trúc (ví dụ: danh sách nhiều sinh viên), chúng ta có thể sử dụng một mảng các cấu trúc.

-   **Cấu trúc:** Nhóm các kiểu dữ liệu khác nhau (như id, name, marks).
-   **Mảng Cấu trúc:** Nhóm nhiều bản ghi (như nhiều sinh viên).

### Ví dụ về Mảng Cấu trúc

Để lưu trữ dữ liệu cho 3 sinh viên, thay vì tạo 3 biến riêng lẻ, bạn có thể làm như sau:

```c
// Khai báo một mảng có thể chứa 3 bản ghi Student
struct Student s[3];

// Truy cập và gán giá trị cho sinh viên đầu tiên (chỉ số 0)
s[0].id = 101;
strcpy(s[0].name, "Alice");
s[0].marks = 89.5;
```

---

## CÁC KHÁI NIỆM VÀ THUẬT TOÁN SẮP XẾP

### Sắp xếp là gì?

-   Sắp xếp (Sorting) là quá trình sắp đặt dữ liệu theo một thứ tự cụ thể, có thể là:
    -   **Tăng dần (Ascending):** ví dụ: 1, 2, 3, 4...
    -   **Giảm dần (Descending):** ví dụ: 9, 8, 7, 6...
-   Bạn có thể sắp xếp số, ký tự, chuỗi, cấu trúc, v.v.

### 1. Sắp xếp nổi bọt (Bubble Sort)

-   Là một thuật toán so sánh đơn giản, trong đó các phần tử liền kề được so sánh và hoán đổi vị trí nếu chúng không đúng thứ tự.
-   **Cách hoạt động:**
    1.  Bắt đầu từ phần tử đầu tiên.
    2.  So sánh phần tử hiện tại với phần tử kế tiếp. Nếu không đúng thứ tự (ví dụ: phần tử trái > phần tử phải khi sắp xếp tăng dần), hãy hoán đổi chúng.
    3.  Lặp lại quá trình này cho đến hết mảng. Sau lượt duyệt đầu tiên, phần tử lớn nhất sẽ "nổi" lên cuối mảng.
    4.  Lặp lại các bước trên cho phần mảng chưa được sắp xếp cho đến khi toàn bộ mảng được sắp xếp.

### 2. Sắp xếp chọn (Selection Sort)

-   Là một thuật toán hoạt động bằng cách lặp đi lặp lại việc tìm phần tử nhỏ nhất (hoặc lớn nhất) từ phần chưa được sắp xếp của mảng và chuyển nó về đầu phần đó.
-   **Cách hoạt động:**
    1.  Bắt đầu từ phần tử đầu tiên.
    2.  Tìm phần tử nhỏ nhất trong phần còn lại của mảng (từ vị trí hiện tại đến cuối).
    3.  Hoán đổi phần tử nhỏ nhất đó với phần tử ở vị trí hiện tại.
    4.  Di chuyển đến phần tử tiếp theo và lặp lại cho đến khi toàn bộ mảng được sắp xếp.

### 3. Sắp xếp chèn (Insertion Sort)

-   Hoạt động tương tự như cách chúng ta sắp xếp các quân bài trên tay.
-   **Cách hoạt động:**
    1.  Bắt đầu từ phần tử thứ hai (giả sử phần tử đầu tiên đã được sắp xếp).
    2.  Lấy phần tử hiện tại (gọi là `key`).
    3.  So sánh `key` với các phần tử ở phía trước nó (phần đã được sắp xếp).
    4.  Dịch chuyển tất cả các phần tử lớn hơn `key` lên một vị trí để tạo khoảng trống.
    5.  Chèn `key` vào đúng vị trí.
    6.  Lặp lại quá trình này cho tất cả các phần tử.

---

## TỔNG KẾT

-   Giới thiệu khái niệm và tầm quan trọng của **cấu trúc** trong C.
-   Giải thích cách **khai báo, khởi tạo và truy cập** các thành viên của cấu trúc.
-   Trình bày các khái niệm **sắp xếp** và ứng dụng thực tế của chúng.
-   Đã triển khai các thuật toán **Sắp xếp nổi bọt, Sắp xếp chọn, và Sắp xếp chèn**.
-   Minh họa việc sắp xếp với các kiểu dữ liệu cơ bản và **mảng cấu trúc**.
