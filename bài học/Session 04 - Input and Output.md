# Session 4 - Input and Output

### **Slide 1: Dùng Scanf trên MacOS**

**Dùng `Scanf` trên MacOS**

**Bước 1:** Cài đặt Tiện ích mở rộng (Extension) **Code Runner**.
*   (Hình ảnh cho thấy việc tìm kiếm "code runner" trong Marketplace của VSCode và nhấn cài đặt).

**Bước 2:** Trong phần cài đặt (settings), tìm kiếm **code - runner**.
*   (Hình ảnh cho thấy việc mở bảng lệnh, chọn Cài đặt và tìm kiếm "code runner").

**Bước 3:** Đánh dấu vào tùy chọn **“Whether to run code in integrated Terminal”** (Chạy mã trong Terminal tích hợp).
*   (Hình ảnh chỉ vào hộp kiểm có nhãn "Code-runner: Run In Terminal").

**Bước 4:** Khởi động lại VSCode.

**Bước 5:** Chạy bằng tùy chọn **"Run Code"**.
*   (Hình ảnh cho thấy menu thả xuống với các tùy chọn "Debug C/C++ File", "Run Code", "Run C/C++ File", và "Run Code" được chọn).

---

### **Slide 2: Trang bìa**

**Cranes Varsity**
'Nơi Công Nghệ Hội Tụ Cùng Sự Ưu Việt'

**Chương trình:**
Chương trình Phát triển Phần mềm Ô tô

**Học kỳ 1:**
Chứng chỉ Phát triển Phần mềm Ô tô (CAS)

**Học phần:**
Lập trình C/C++ cho Hệ thống Nhúng AI

**Buổi 4:**
Nhập và Xuất (Input and Output)

---

### **Slide 3: Mục tiêu và Chủ đề Buổi học**

**MỤC TIÊU VÀ CHỦ ĐỀ BUỔI HỌC**

| Giới thiệu về Nhập và Xuất; I/O Console với `printf()` và `scanf()` | Nhập và Xuất Ký tự | Nhập và Xuất File |
| :--- | :--- | :--- |
| Học cách C xử lý tương tác người dùng thông qua các hoạt động nhập/xuất bằng các hàm console. | Hiểu về việc nhập/xuất một ký tự duy nhất bằng `getchar()`, `putchar()`, và `%c`. | Học các thao tác với file như ghi, đọc đến và từ các thiết bị lưu trữ thứ cấp như Ổ cứng (Hard Disk). |
| *   **Thực hành**
*   **Hỏi & Đáp và Tóm tắt** |

---

### **Slide 4: Giới thiệu về các Câu lệnh Nhập và Xuất**

**GIỚI THIỆU VỀ NHẬP VÀ XUẤT**

**CÁC CÂU LỆNH NHẬP (INPUT STATEMENTS)**
*   Thao tác Nhập là lấy đầu vào từ người dùng và lưu trữ các giá trị/dữ liệu do người dùng cung cấp vào các vị trí bộ nhớ cụ thể.
*   Như chúng ta đã biết, biến là một vị trí bộ nhớ để lưu trữ dữ liệu.

**CÁC CÂU LỆNH XUẤT (OUTPUT STATEMENTS)**
*   Thao tác Xuất là một hoạt động để trả lại thông tin cho người dùng sau khi xử lý nó.
*   Ngôn ngữ C Cung cấp `printf()` là hàm xuất và `scanf()` là hàm nhập.
*   `printf()` và `scanf()` là các hàm thư viện có trong tệp tiêu đề `stdio.h`.

---

### **Slide 5: Cách sử dụng hàm `printf()`**

**SỬ DỤNG HÀM PRINTF**

**Làm thế nào để sử dụng hàm `printf()`?**
*   Hàm `printf()` được gọi là hàm xuất.
*   Ví dụ 1: `printf(“Thông điệp cần in ra màn hình”);`
*   Trong ví dụ 1, thông điệp được đặt trong dấu ngoặc kép `“ ”` sẽ được in ra console.
*   Vì vậy, bất cứ điều gì bạn muốn in ra console, bạn cần đặt thông điệp đó trong dấu ngoặc kép.
*   Câu lệnh này cần được kết thúc bằng dấu chấm phẩy (`;`).

---

### **Slide 6: Ví dụ về hàm `printf()`**

**SỬ DỤNG HÀM PRINTF**

**CHƯƠNG TRÌNH C ĐỂ IN THÔNG ĐIỆP “WELCOME TO C PROGRAMMING LAB“ RA CONSOLE**
```c
#include<stdio.h>
int main()
{
    printf("Welcome to C Programming Lab");
    return 0;
}
```
**ĐẦU RA:**
```
Welcome to C Programming Lab
```

---

### **Slide 7: Cách sử dụng hàm `scanf()`**

**SỬ DỤNG HÀM SCANF**

**Làm thế nào để sử dụng hàm `scanf()`?**
*   `scanf()` được sử dụng để đọc đầu vào từ người dùng.
*   Bất cứ khi nào chương trình cần đầu vào tại thời điểm chạy, `scanf()` phải được sử dụng.

**Cú pháp:** `scanf(“<định_dạng_chỉ_định>”, <toán_tử_địa_chỉ><tên_biến>);`

---

### **Slide 8: Ví dụ về `printf()` và `scanf()`**

**SỬ DỤNG PRINTF VÀ SCANF CHO CONSOLE I/O**

**CHƯƠNG TRÌNH MINH HỌA VIỆC SỬ DỤNG CÁC HÀM PRINTF VÀ SCANF**
```c
#include<stdio.h>
int main()
{
    int a,b,c;
    printf("Nhập giá trị cho a \n");
    scanf("%d",&a);
    printf("Nhập giá trị cho b \n");
    scanf("%d",&b);
    c=a+b;
    printf("a=%d \t b=%d \n",a,b);
    printf("Tổng=%d \n",c);
    return 0;
}
```
**Đầu ra:**
```
Nhập giá trị cho a
100
Nhập giá trị cho b
200
a=100 b=200
Tổng=300
```

---

### **Slide 9: Nhập và Xuất Ký tự**

**NHẬP VÀ XUẤT KÝ TỰ**

**Để đọc một ký tự từ người dùng, có hai cách:**
a) Với định dạng chỉ định `%c` sử dụng `scanf()`
b) `getchar()` được sử dụng để nhận một đầu vào ký tự duy nhất từ người dùng

**Để in một ký tự duy nhất ra console, có hai cách:**
a) Với định dạng chỉ định `%c` sử dụng `printf()`;
b) `putchar()` được sử dụng để hiển thị ký tự trên màn hình.

---

### **Slide 10: Ví dụ Nhập/Xuất Ký tự với `scanf()` và `%c`**

**CHƯƠNG TRÌNH VỀ a) Nhập và Xuất Ký tự sử dụng `scanf()` và `%c`**

**CHƯƠNG TRÌNH C MINH HỌA VIỆC NHẬP VÀ XUẤT KÝ TỰ SỬ DỤNG SCANF VÀ %C**
```c
#include <stdio.h>
int main()
{
    char ch;
    // Yêu cầu người dùng nhập một ký tự
    printf("Nhập một ký tự: ");

    // Đọc một ký tự duy nhất bằng scanf() với %c
    scanf("%c", &ch);

    // In ký tự đã nhập bằng printf() với %c
    printf("Bạn đã nhập: %c\n", ch);
    return 0;
}
```
**Đầu ra:**
```
Nhập một ký tự: n
Bạn đã nhập: n
```**GIẢI THÍCH:**
`scanf("%c", &ch);`
*   Đọc một ký tự duy nhất từ đầu vào của người dùng.
*   Dấu và (&) được sử dụng để lưu trữ đầu vào trong biến ch.
`printf("Bạn đã nhập: %c\n", ch);` In ký tự bằng cách sử dụng `%c`.

---

### **Slide 11: Ví dụ Nhập/Xuất Ký tự với `getchar()` và `putchar()`**

**CHƯƠNG TRÌNH VỀ b) Nhập và Xuất Ký tự sử dụng `getchar()` và `putchar()`**

**CHƯƠNG TRÌNH C MINH HỌA VIỆC SỬ DỤNG CÁC HÀM GETCHAR() VÀ PUTCHAR()**
```c
#include <stdio.h>
int main()
{
    char ch;
    // Yêu cầu người dùng nhập một ký tự
    printf("Nhập một ký tự: ");

    // Đọc một ký tự duy nhất bằng getchar()
    ch = getchar();

    // In ký tự đã nhập bằng putchar()
    printf("Bạn đã nhập: ");
    putchar(ch);
    printf("\n");
    return 0;
}
```
**Đầu ra:**
```
Nhập một ký tự: Y
Bạn đã nhập: Y
```
**Giải thích:**
*   `getchar()` được sử dụng để nhận một đầu vào ký tự duy nhất từ người dùng.
*   `putchar()` được sử dụng để hiển thị ký tự trên màn hình. `printf()` được sử dụng để in các thông điệp hướng dẫn người dùng.

---

### **Slide 12: Nhập và Xuất File**

**NHẬP VÀ XUẤT FILE**

**File trong C là gì?**
*   File là một tập hợp dữ liệu được lưu trữ vĩnh viễn trên một thiết bị lưu trữ (như ổ cứng, SSD hoặc USB).
*   Trong lập trình C, file được sử dụng để lưu trữ, truy xuất và thao tác dữ liệu ngoài phạm vi thực thi của chương trình.
*   Nhập và Xuất File (File I/O) trong C liên quan đến việc đọc từ và ghi vào các file được lưu trữ trên các thiết bị lưu trữ thứ cấp như ổ cứng.

---

### **Slide 13: Các Thao tác Xử lý File**

**NHẬP VÀ XUẤT FILE**

**Các Thao tác Xử lý File**

**Mở một File:**
`fopen("tên_file", chế_độ);`
Nó được sử dụng để mở file để đọc, ghi hoặc nối thêm dữ liệu vào file.
Ví dụ: `fopen("tên_file", "chế_độ")` được sử dụng để mở một file.

**Các chế độ:**
*   `"r"` → Đọc (file phải tồn tại).
*   `"w"` → Ghi (tạo một file mới hoặc ghi đè lên file hiện có).
*   `"a"` → Nối thêm (thêm dữ liệu vào cuối file hiện có).

---

### **Slide 14: Ghi File với `fprintf`**

**NHẬP VÀ XUẤT FILE (ghi)**

**CHƯƠNG TRÌNH C ĐỂ GHI DỮ LIỆU VÀO FILE OUTPUT.TXT SỬ DỤNG `fprintf`**
```c
#include <stdio.h>
int main()
{
    FILE *file; // Khai báo một con trỏ file
    // Mở file ở chế độ ghi
    file = fopen("output.txt", "w");
    if (file == NULL)
    {
        printf("Lỗi khi mở file!\n");
        return 1;
    }
    // Ghi vào file
    fprintf(file, "Xin chào, đây là một ví dụ ghi file trong C.\n");
    // Đóng file
    fclose(file);
    printf("Dữ liệu đã được ghi vào file thành công.\n");
    return 0;
}
```
**(Một file có tên `output.txt` sẽ được tạo với nội dung bên trong.)**

**Đầu ra chương trình:**
`Dữ liệu đã được ghi vào file thành công.`

**Nội dung file `output.txt`:**
`Xin chào, đây là một ví dụ ghi file trong C.`

---

### **Slide 15: Đọc File với `fscanf`**

**NHẬP VÀ XUẤT FILE (đọc)**

**CHƯƠNG TRÌNH C ĐỂ ĐỌC DỮ LIỆU TỪ FILE SỬ DỤNG `fscanf()`**
```c
#include <stdio.h>
int main()
{
    FILE *file;
    char name[50];
    int age;
    // Mở file ở chế độ đọc
    file = fopen("data.txt", "r");
    // Kiểm tra xem file có tồn tại không
    if (file == NULL)
    {
        printf("Không tìm thấy file!\n");
        return 1;
    }
    // Đọc dữ liệu từ file bằng fscanf
    fscanf(file, "%s %d", name, &age);
    // Hiển thị dữ liệu
    printf("Tên: %s\n", name);
    printf("Tuổi: %d\n", age);
    // Đóng file
    fclose(file);
    return 0;
}
```
**Nội dung file `data.txt`:**
```
Basavaraju
40
```
**Đầu ra chương trình:**
```
Tên: Basavaraju
Tuổi: 40
```

---

### **Slide 16: Nối thêm vào File với `fprintf`**

**NHẬP VÀ XUẤT FILE (nối thêm)**

**CHƯƠNG TRÌNH C ĐỂ NỐI DỮ LIỆU VÀO FILE HIỆN CÓ SỬ DỤNG `fprintf()`**
```c
#include <stdio.h>
int main() {
    FILE *file;
    // Mở file ở chế độ nối thêm
    file = fopen("output.txt", "a");
    if (file == NULL) {
        printf("Lỗi khi mở file!\n");
        return 1;
    }
    // Nối thêm văn bản mới
    fprintf(file, "Nối thêm dữ liệu mới vào file.\n");
    fclose(file);
    printf("Dữ liệu đã được nối thêm thành công.\n");
    return 0;
}
```
**Đầu ra chương trình:**
`Dữ liệu đã được nối thêm thành công.`

**Nội dung của file `output.txt` (sau khi chạy):**
```
Basavaraju
40
Nối thêm dữ liệu mới vào file.
```

---

### **Slide 17: Thực hành**

**THỰC HÀNH**

**Bài tập 2: Hiển thị Chuỗi đầu vào có Dấu cách**
**Yêu cầu:** Đọc một câu đầy đủ bằng `scanf()` với `%[^\n]` và in nó ra.
| Đầu vào: | Đầu ra: |
| :--- | :--- |
| Cranes Varsity | Bạn đã nhập: Cranes Varsity |

**Bài tập 13: Đọc Hóa đơn từ File và Tính tổng**
**Yêu cầu:** Tạo một chương trình C thực hiện các công việc sau:
1.  Ghi dữ liệu sản phẩm (tên sản phẩm, số lượng, và giá) vào một file có tên `invoice.txt`.
2.  Đọc lại dữ liệu này từ file.
3.  Tính toán và hiển thị tổng chi phí cho mỗi sản phẩm theo định dạng:
    `Sản phẩm Tổng cộng: <tổng_giá>`
    Tổng giá được tính bằng `số lượng * giá`, hiển thị với **2 chữ số thập phân**.
| Đầu vào (trong file): | Đầu ra: |
| :--- | :--- |
| Pen 5 10.5 <br> Book 2 150 | Pen Tổng cộng: 52.50 <br> Book Tổng cộng: 300.00 |

---

### **Slide 18: Câu hỏi**

**Câu hỏi**

**1. Hàm nào được sử dụng để hiển thị đầu ra trên console trong C?**
(A) `scanf()`
(B) `printf()`
(C) `getchar()`
(D) `fscanf()`

**2. Cú pháp nào là đúng để đọc một đầu vào số nguyên bằng `scanf()`?**
(A) `scanf("%d", num);`
(B) `scanf("%d", &num);`
(C) `scanf("%d", *num);`
(D) `scanf("%d", &&num);`

---

### **Slide 19: Câu hỏi (tiếp)**

**Câu hỏi**

**3. Hàm nào được sử dụng để đọc một đầu vào ký tự duy nhất trong C?**
(A) `scanf("%c", &ch);`
(B) `getchr();`
(C) `getche();`
(D) Tất cả các câu trên

**4. Chế độ file nào được sử dụng để mở một file để đọc dữ liệu từ file?**
(A) `"r"`
(B) `"w"`
(C) `"a+"`
(D) `"r+"`

---

### **Slide 20: Tóm tắt**

**TÓM TẮT**

Trong buổi học này, chúng ta đã học các hàm sau và mục đích của chúng:

*   `printf()`: Hàm xuất để in thông điệp ra console.
*   `scanf()`: Hàm nhập để đọc dữ liệu từ bàn phím.
*   `fopen()`: Mở một file trong một chế độ cho trước (r, w, a, v.v.).
*   `fclose()`: Đóng một file đang mở.
*   `fprintf()`: Ghi văn bản đã định dạng vào một file.
*   `fscanf()`: Đọc văn bản đã định dạng từ một file.

---

### **Slide 21: Cảm ơn**

**CẢM ƠN**
