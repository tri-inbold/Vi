# Session 8 - Pointers and AI Code Generation

### **Slide 1**

**CRANES**
**Cranes Varsity**
'Nơi Công Nghệ Hội Tụ Cùng Sự Ưu Việt'

**Chương trình:**
Chương trình Phát triển Phần mềm Ô tô

**Học kỳ 1:**
Chứng chỉ Phát triển Phần mềm Ô tô (CAS)

**Học phần:**
Lập trình C/C++ cho Hệ thống Nhúng AI

**Buổi 08:**
Con trỏ và Tạo mã AI

---

### **Slide 2**

**CRANES**
**MỤC TIÊU VÀ CHỦ ĐỀ BUỔI HỌC**

| Giới thiệu về Con trỏ, cơ bản về con trỏ, con trỏ và mảng | Cấp phát Bộ nhớ Động | TẠO MÃ AI CHO CON TRỎ | THỰC HÀNH VÀ HỎI ĐÁP |
| :--- | :--- | :--- | :--- |
| Để hiểu các nguyên tắc cơ bản về con trỏ, bao gồm khai báo, khởi tạo và tham chiếu ngược, mối quan hệ giữa con trỏ và mảng với các ví dụ thực tế. | Để tìm hiểu cấp phát bộ nhớ động bằng cách sử dụng malloc(), calloc(), realloc(), và free(). | Để sử dụng công cụ tạo mã do AI hỗ trợ để viết và tối ưu hóa các chương trình C dựa trên con trỏ. | HỎI VÀ ĐÁP |

---

### **Slide 3**

**CRANES**
**GIỚI THIỆU VỀ CON TRỎ, CƠ BẢN VỀ CON TRỎ, CON TRỎ VÀ MẢNG**

**GIỚI THIỆU VỀ CON TRỎ**

**Con trỏ là gì?**
*   Con trỏ là biến đặc biệt được sử dụng để lưu trữ địa chỉ của một biến khác.
*   Các biến thông thường chứa một giá trị cụ thể (tham chiếu trực tiếp)

---

### **Slide 4**

**CRANES**
**GIỚI THIỆU VỀ CON TRỎ, CƠ BẢN VỀ CON TRỎ, CON TRỎ VÀ MẢNG**

**GIỚI THIỆU VỀ CON TRỎ**

**Các tác vụ ví dụ được thực hiện bởi chương trình:**
1.  Các phép toán số học với con trỏ
2.  Con trỏ đến các biến
3.  Con trỏ đến chuỗi
4.  Cấp phát bộ nhớ động

---

### **Slide 5**

**CRANES**
**GIỚI THIỆU VỀ CON TRỎ, CƠ BẢN VỀ CON TRỎ, CON TRỎ VÀ MẢNG (tiếp..)**

**GIỚI THIỆU VỀ CON TRỎ**

[Hình ảnh mô tả một biến 'count' chứa giá trị 7 và một con trỏ 'countPtr' trỏ đến địa chỉ của biến 'count']

*   **count**: tham chiếu trực tiếp đến một biến chứa giá trị 7
*   **countPtr**: Con trỏ countPtr tham chiếu gián tiếp đến một biến chứa giá trị 7

---

### **Slide 6**

**CRANES**
**CƠ BẢN VỀ CON TRỎ**
**GIỚI THIỆU VỀ CON TRỎ, CƠ BẢN VỀ CON TRỎ, CON TRỎ VÀ MẢNG (tiếp..)**

**KHAI BÁO CON TRỎ**
sử dụng với các biến con trỏ
`int *myPtr;`

*   Định nghĩa một con trỏ đến một số nguyên (con trỏ kiểu int \*)
*   Nhiều con trỏ yêu cầu sử dụng dấu \* trước mỗi định nghĩa biến
*   `int *myPtr1, *myPtr2;`
*   Có thể định nghĩa con trỏ đến bất kỳ kiểu dữ liệu nào

---

### **Slide 7**

**CRANES**
**CƠ BẢN VỀ CON TRỎ**
**GIỚI THIỆU VỀ CON TRỎ, CƠ BẢN VỀ CON TRỎ, CON TRỎ VÀ MẢNG (tiếp..)**

*   Chúng ta có thể khai báo rằng một con trỏ `ptr` trỏ đến một số nguyên bằng cách nói
    `int *ptr;`
*   Giả sử chúng ta có:
    `int x = 5;`
*   Chúng ta có thể làm cho `ptr` trỏ đến `x` bằng cách gán cho `ptr` vị trí bộ nhớ nơi `x` được lưu trữ. Do đó `ptr = &x;`
*   đặt `ptr` để trỏ đến `x`.
*   Giả sử địa chỉ biến `x` là `0x2000` và biến con trỏ `ptr` giữ địa chỉ `0x2000`

[Sơ đồ minh họa biến x có giá trị 5 tại địa chỉ 0x2000 và con trỏ ptr giữ địa chỉ của x (&x)]

---

### **Slide 8**

**CRANES**
**CƠ BẢN VỀ CON TRỎ**
**GIỚI THIỆU VỀ CON TRỎ, CƠ BẢN VỀ CON TRỎ, CON TRỎ VÀ MẢNG (tiếp..)**

[Đoạn mã C minh họa việc khai báo con trỏ, gán địa chỉ và truy cập gián tiếp giá trị]

```c
1 // Khai báo con trỏ
2 #include <stdio.h>
3
4 int main()
5 {
6     int x = 5;
7
8     printf("x = %d\n", x);
9     printf("&x = %p\n", &x);
10
11    int *ptr = &x;
12    printf("ptr = %p\n", ptr);
13
14    // Truy cập gián tiếp giá trị của x thông qua con trỏ
15    printf("*ptr = %d\n", *ptr);
16
17    return 0;
18 }
```

*   Chúng ta có thể khai báo rằng một con trỏ `ptr` trỏ đến một số nguyên bằng cách nói
    *   `int *ptr;`
*   Giả sử chúng ta có:
    *   `int x = 5;`
*   Chúng ta có thể làm cho `ptr` trỏ đến `x` bằng cách gán cho `ptr` vị trí bộ nhớ nơi `x` được lưu trữ. Do đó
    *   `ptr = &x;`
*   đặt `ptr` để trỏ đến `x`.

---

### **Slide 9**

**CRANES**
**CON TRỎ CHƯA KHỞI TẠO**
**GIỚI THIỆU VỀ CON TRỎ, CƠ BẢN VỀ CON TRỎ, CON TRỎ VÀ MẢNG (tiếp..)**

Một con trỏ không được khởi tạo được gọi là **con trỏ hoang dã (wild pointer)**

*   Bất kỳ nỗ lực nào để sử dụng các con trỏ chưa được khởi tạo như vậy đều có thể gây ra hành vi không mong muốn, thường là lỗi phân đoạn (segmentation fault)
*   Khởi tạo con trỏ để ngăn chặn các kết quả không mong muốn.

---

### **Slide 10**

**CRANES**
**CON TRỎ CHƯA KHỞI TẠO**
**GIỚI THIỆU VỀ CON TRỎ, CƠ BẢN VỀ CON TRỎ, CON TRỎ VÀ MẢNG (tiếp..)**

*   Nếu không có địa chỉ hợp lệ để khởi tạo con trỏ, hãy khởi tạo thành NULL, điều đó có nghĩa là "không trỏ vào đâu cả".
*   Trước khi bạn tham chiếu ngược một con trỏ, hãy đảm bảo nó không phải là NULL
    `if(ptr) //if(ptr != NULL)`
    `{`
    `// Thực hiện một số thao tác với ptr`
    `}`

---

### **Slide 11**

**CRANES**
**CON TRỎ VÀ MẢNG**

*   Mảng và con trỏ có liên quan chặt chẽ với nhau
*   Tên mảng giống như một con trỏ hằng
*   Con trỏ có thể thực hiện các thao tác lập chỉ mục mảng
*   Con trỏ và mảng có thể được sử dụng thay thế cho nhau khi truy cập các phần tử riêng lẻ.
*   Tên mảng tương đương với địa chỉ của phần tử đầu tiên trong mảng

**Ví dụ:**
`int a[10];`
`int *pa;`
`pa = &a[0]; /* tương đương với pa = a */`
`Vậy, a[1] => *(pa+1) => pa[1] => *(a+1)`
`&a[1] => pa+1 => a+1`

---

### **Slide 12**

**CRANES**
**CON TRỎ VÀ MẢNG**

[Đoạn mã C minh họa việc sử dụng con trỏ để truy cập các phần tử của mảng]

```c
1 // Chương trình: Con trỏ và mảng
2 #include <stdio.h>
3
4 int main() {
5    int arr[5] = {1, 2, 3, 4, 5};
6    int *ptr = arr; // Con trỏ trỏ đến mảng
7
8    for (int i = 0; i < 5; i++) {
9       // Truy cập các phần tử mảng bằng số học con trỏ
10      printf("%d ", *(ptr + i));
11   }
12
13   return 0;
14 }
```

**Giải thích**
*   `arr` là một mảng gồm 5 số nguyên.
*   `ptr` là một con trỏ ban đầu trỏ đến phần tử đầu tiên của `arr`.
*   Bên trong vòng lặp `for`, `*(ptr + i)` truy cập phần tử thứ `i` của mảng bằng cách sử dụng số học con trỏ.

---

### **Slide 13**

**CRANES**
**CẤP PHÁT BỘ NHỚ ĐỘNG**

*   **Cấp phát tĩnh (Static allocation):** không gian bộ nhớ được cấp phát ở các vị trí cố định và tồn tại trong suốt toàn bộ chương trình.
*   **Cấp phát tự động (Automatic allocation):** không gian bộ nhớ được cấp phát khi vào một hàm và được giải phóng khi thoát khỏi một hàm.
*   **Cấp phát động (Dynamic allocation):** không gian bộ nhớ được cấp phát và giải phóng một cách rõ ràng bởi các lập trình viên trong khi chương trình đang chạy.

*   **Bộ nhớ được cấp phát trên Heap (Heap-allocated memory)**
    *   Được sử dụng để cấp phát bộ nhớ lúc chạy. Vòng đời của bộ nhớ động kéo dài cho đến khi bạn giải phóng nó.
    *   Nó tồn tại ngoài vòng đời của một lệnh gọi hàm.
    *   Bộ nhớ heap được cấp phát theo một cách phức tạp hơn bộ nhớ stack.

---

### **Slide 14**

**CRANES**
**CẤP PHÁT BỘ NHỚ ĐỘNG (tiếp..)**

*   Nếu chúng ta muốn cấp phát bộ nhớ lúc chạy (trong heap), sau đây là các hàm thư viện sẽ được sử dụng có sẵn trong tệp tiêu đề `stdlib.h`.
    `#include <stdlib.h>`

[Sơ đồ phân loại Quản lý bộ nhớ động (DMA) thành malloc, calloc, realloc, và free]

**a) `void *malloc(size_t size);`**
*   Cấp phát một khối `size` byte,
*   trả về một con trỏ đến khối
*   (NULL nếu không thể cấp phát khối)

**b) `void *calloc(size_t num_elements, size_t element_size);`**
*   Cấp phát một khối `num_elements * element_size` byte,
*   khởi tạo mọi byte thành không,
*   trả về con trỏ đến khối
*   (NULL nếu không thể cấp phát khối)

---

### **Slide 15**

**CRANES**
**CẤP PHÁT BỘ NHỚ ĐỘNG (tiếp..)**

**c) `void *realloc(void *ptr, size_t size);`**
*   `ptr` là một con trỏ đến khối bộ nhớ đã được cấp phát trước đó bằng `malloc`, `calloc` hoặc `realloc`. `size` là kích thước mới (tính bằng byte) cho khối bộ nhớ.
*   `realloc` trả về một con trỏ đến bộ nhớ mới được cấp phát, có thể khác với `ptr`.
*   Nếu không thành công, nó trả về NULL và khối ban đầu không thay đổi.

**d) `void free(void *ptr);`**
*   `ptr` là một con trỏ được trả về trước đó bởi `malloc`, `calloc` hoặc `realloc`. `free` giải phóng khối bộ nhớ được trỏ đến bởi `ptr`.
*   Sau khi gọi `free`, bộ nhớ đó không còn hợp lệ để truy cập.
*   Nếu bạn truyền NULL vào `free`, không có gì xảy ra — nó an toàn.

---

### **Slide 16**

**CRANES**
**CẤP PHÁT BỘ NHỚ ĐỘNG (tiếp..)**

[Đoạn mã C minh họa hàm malloc()]

```c
1 // Cấp phát bộ nhớ động (DMA) - hàm malloc()
2 #include <stdlib.h>
3 #include <stdio.h>
4
5 int main()
6 {
7    int *p = NULL;
8    int n;
9
10   printf("Nhập số byte cần cấp phát: ");
11   scanf("%d", &n);
12
13   printf("GIÁ TRỊ CỦA P TRƯỚC KHI CẤP PHÁT = %p &p = %p\n", p, &p);
14
15   p = malloc(n);
16
17   if (p == NULL)
18      printf("Không thể cấp phát bộ nhớ\n");
19   else
20   {
21      printf("Cấp phát bộ nhớ thành công\n");
22      printf("GIÁ TRỊ CỦA P SAU KHI CẤP PHÁT = %p &p = %p\n", p, &p);
23   }
24   return 0;
25 }
```

**Đầu ra mẫu:**
`Nhập số byte cần cấp phát: 1`
`GIÁ TRỊ CỦA P TRƯỚC KHI CẤP PHÁT = (nil) &p = 0x7ffe8bbdce20`
`Cấp phát bộ nhớ thành công`
`GIÁ TRỊ CỦA P SAU KHI CẤP PHÁT = 0x5aee1fd71ac0 &p = 0x7ffe8bbdce20`

**Giải thích**
*   Hỏi người dùng có bao nhiêu byte để cấp phát.
*   In giá trị của con trỏ `p` trước khi cấp phát.
*   Cấp phát bộ nhớ bằng `malloc`.
*   Kiểm tra xem việc cấp phát có thành công không.
*   In lại giá trị của `p` sau khi cấp phát.

---

### **Slide 17**

**CRANES**
**CẤP PHÁT BỘ NHỚ ĐỘNG (MẢNG SỐ NGUYÊN)**

[Đoạn mã C minh họa cấp phát bộ nhớ động cho một mảng số nguyên]
```c
// Code
#include <stdlib.h> // Cho malloc() và free()
#include <stdio.h>  // Cho printf() và scanf()

int main() {
    int *p = NULL; // Con trỏ để giữ địa chỉ của bộ nhớ được cấp phát động
    int n;         // Biến để lưu trữ số lượng phần tử

    // Yêu cầu người dùng nhập số lượng phần tử
    printf("Nhập số lượng phần tử: ");
    scanf("%d", &n);

    // Cấp phát động bộ nhớ cho n số nguyên
    p = (int *)malloc(n * sizeof(int));

    // Kiểm tra xem việc cấp phát bộ nhớ có thành công không
    if (p == NULL) {
        printf("Không thể cấp phát bộ nhớ\n");
    } else {
        // Cấp phát bộ nhớ thành công
        printf("Nhập các giá trị:\n");
        for (int i = 0; i < n; i++) {
            scanf("%d", &p[i]); // Đọc các phần tử vào bộ nhớ đã cấp phát
        }

        // Hiển thị các phần tử đã nhập
        printf("Các phần tử là:\n");
        for (int i = 0; i < n; i++) {
            printf("%d ", p[i]);
        }
        printf("\n");

        free(p); // Giải phóng bộ nhớ được cấp phát động
    }
    return 0; // Trả về thành công
}
```

**Giải thích**
*   `malloc` được sử dụng để cấp phát bộ nhớ.
*   Luôn kiểm tra xem `malloc` có trả về NULL không (nghĩa là cấp phát bộ nhớ không thành công).
*   Luôn giải phóng bộ nhớ sau khi sử dụng để tránh rò rỉ bộ nhớ.
*   Ép kiểu `(int *)` với `malloc` là tùy chọn trong C nhưng thường được thực hiện để rõ ràng.

**Đầu ra mẫu:**
`Nhập các giá trị:`
`10 20 30 40 50`
`Các phần tử là:`
`10 20 30 40 50`

---

### **Slide 18**

**CRANES**
**DMA - RÒ RỈ BỘ NHỚ**
**CẤP PHÁT BỘ NHỚ ĐỘNG (tiếp..)**

*   **Rò rỉ bộ nhớ (Memory leakage)** xảy ra khi bộ nhớ được cấp phát động không được giải phóng sau khi sử dụng, dẫn đến lãng phí bộ nhớ không thể được tái sử dụng trong quá trình thực thi của chương trình.

`void free(void *pointer);`
*   Đưa một con trỏ đến bộ nhớ đã được cấp phát trước đó, đặt vùng đó trở lại vào heap của bộ nhớ chưa được cấp phát.

**Lưu ý:** Rất dễ quên giải phóng bộ nhớ khi không còn cần thiết..
*   Đây là nguồn gốc của vấn đề "rò rỉ bộ nhớ" khét tiếng
*   Khó theo dõi – chương trình sẽ chạy tốt trong một thời gian, cho đến khi đột nhiên không còn bộ nhớ!

---

### **Slide 19**

**CRANES**
**DMA - HÀM FREE()**
**CẤP PHÁT BỘ NHỚ ĐỘNG (tiếp..)**

[Đoạn mã C để minh họa hàm free]

```c
1 // Chương trình minh họa hàm free
2 #include <stdio.h>
3 #include <stdlib.h>
4
5 int main()
6 {
7    int *ptr1 = malloc(20);
8    printf("ptr1 = %p \n", ptr1);
9
10   int *ptr2 = malloc(20);
11   printf("ptr2 = %p \n", ptr2);
12
13   return 0;
14 }
```

**Đầu ra:**
`ptr1 = 0x5b2aff1db2a0`
`ptr2 = 0x5b2aff1db6d0`

**Giải thích**
Khối bộ nhớ riêng biệt được cấp phát cho `ptr1` và `ptr2`.

---

### **Slide 20**

**CRANES**
**DMA - HÀM FREE()**
**CẤP PHÁT BỘ NHỚ ĐỘNG (tiếp..)**

[Đoạn mã C để minh họa hàm free]
```c
1 // Chương trình minh họa hàm free
2 #include <stdio.h>
3 #include <stdlib.h>
4
5 int main()
6 {
7    int *ptr1 = malloc(20);
8    printf("ptr1 = %p \n", ptr1);
9
10   free(ptr1);
11
12   int *ptr2 = malloc(20);
13   printf("ptr2 = %p \n", ptr2);
14
15   return 0;
16 }
```
**Đầu ra:**
`ptr1 = 0x6344b923e2a0`
`ptr2 = 0x6344b923e2a0`

**Giải thích**
Cùng một khối bộ nhớ có thể được cấp phát cho `ptr1` và `ptr2`.

---

### **Slide 21**

**CRANES**
**DMA - CON TRỎ LƠ LỬNG (DANGLING POINTER)**
**CẤP PHÁT BỘ NHỚ ĐỘNG (tiếp..)**

*   **Con trỏ lơ lửng** là các con trỏ không trỏ đến một đối tượng hợp lệ.
*   Con trỏ lơ lửng phát sinh khi một đối tượng bị xóa hoặc giải phóng, mà không sửa đổi giá trị của con trỏ, do đó con trỏ vẫn trỏ đến vị trí bộ nhớ của bộ nhớ đã được giải phóng.

---

### **Slide 22**

**CRANES**
**DMA - HÀM REALLOC()**
**CẤP PHÁT BỘ NHỚ ĐỘNG (tiếp..)**

`void *realloc(void *ptr, size_t new_size);`
*   Cho một khối đã được cấp phát trước đó bắt đầu tại `ptr`,
*   thay đổi kích thước khối thành `new_size`,
*   trả về con trỏ đến khối đã thay đổi kích thước
*   Nếu kích thước khối được tăng lên, nội dung sẽ không thay đổi đến mức tối thiểu của kích thước cũ và mới; bộ nhớ mới được cấp phát sẽ không được khởi tạo.

Nếu `ptr` là NULL, `realloc` giống hệt như `malloc`
Nếu `new_size` bằng không, lệnh gọi tương đương với `free(ptr);`

---

### **Slide 23**

**CRANES**
**DMA - HÀM REALLOC()**
**CẤP PHÁT BỘ NHỚ ĐỘNG (tiếp..)**

[Đoạn mã C để minh họa hàm Realloc]
```c
// Chương trình minh họa hàm Realloc
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n, *arr, i, new_n;

    printf("Nhập số lượng phần tử: ");
    scanf("%d", &n);

    // Cấp phát bộ nhớ để lưu trữ n số nguyên
    arr = (int *)malloc(n * sizeof(int));
    if (arr == NULL) {
        printf("Cấp phát bộ nhớ không thành công!\n");
        return 1;
    }

    printf("Nhập %d phần tử:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("Các phần tử đã nhập:\n");
    for (i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    printf("Nhập số lượng phần tử cần thêm: ");
    scanf("%d", &new_n);

    // Thay đổi kích thước bộ nhớ đã cấp phát
    arr = (int*) realloc(arr, (n + new_n) * sizeof(int));
    if (arr == NULL) {
        printf("Tái cấp phát bộ nhớ không thành công!\n");
        return 1;
    }

    printf("Nhập %d phần tử mới:\n", new_n);
    for (i = n; i < n + new_n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("Tất cả các phần tử sau khi thêm mới:\n");
    for (i = 0; i < n + new_n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    // Giải phóng bộ nhớ đã cấp phát
    free(arr);
    return 0;
}
```

---

### **Slide 24**

**CRANES**
**TÓM TẮT**

1.  **Con trỏ lưu trữ địa chỉ bộ nhớ**
    - Một con trỏ giữ địa chỉ của một biến, cho phép truy cập và sửa đổi gián tiếp.

2.  **DMA cho phép sử dụng bộ nhớ linh hoạt lúc chạy**
    - Các hàm như \`malloc\`, \`calloc\`, \`realloc\`, và \`free\` quản lý bộ nhớ heap một cách động.

3.  **Luôn kiểm tra \`NULL\` sau khi cấp phát bộ nhớ**
    - Nếu \`malloc\` hoặc \`calloc\` không thành công, chúng trả về \`NULL\`. Sử dụng một con trỏ null gây ra sự cố.

4.  **Sử dụng \`free()\` để tránh rò rỉ bộ nhớ**
    - Bộ nhớ được cấp phát phải được giải phóng thủ công bằng cách sử dụng \`free()\` khi không còn cần thiết.

5.  **Số học con trỏ mạnh mẽ nhưng rủi ro**
    - Bạn có thể di chuyển qua các khối bộ nhớ bằng cách sử dụng toán học con trỏ, nhưng nó phải được sử dụng cẩn thận để tránh hành vi không xác định.

---

### **Slide 25**

**CRANES**

**CẢM ƠN**
