# Session 7 - Arrays (One-dimensional & Two-dimensional)

### **Slide 1: Trang bìa**

**CRANES**

**Chương trình:**
Chương trình Phát triển Phần mềm Ô tô

**Học kỳ 1:**
Chứng chỉ Phát triển Phần mềm Ô tô (CAS)

**Học phần:**
Lập trình C/C++ cho Hệ thống nhúng AI

**Buổi 07:**
Mảng (Một chiều & Hai chiều)

---

### **Slide 2: Mục tiêu và Chủ đề**

**CRANES**
**MỤC TIÊU VÀ CHỦ ĐỀ**

| Giới thiệu về Mảng | Mảng Một chiều (1D) | Mảng Hai chiều (2D) |
| :--- | :--- | :--- |
| Để hiểu khái niệm, sự cần thiết và cấu trúc của mảng trong lập trình C. | Học cách khai báo, khởi tạo và truy cập các phần tử của mảng một chiều. | Khám phá mảng hai chiều và thực hiện các phép toán ma trận bằng chương trình C. |
| • **Thực hành** <br> • **Hỏi & Đáp** |

---

### **Slide 3: Giới thiệu về Mảng**

**CRANES**
**ĐỊNH NGHĨA VỀ MẢNG**

**MẢNG:** Mảng trong C là một tập hợp có kích thước cố định gồm các mục dữ liệu tương tự được lưu trữ ở các vị trí bộ nhớ liền kề.

*   Nó có thể được sử dụng để lưu trữ tập hợp các kiểu dữ liệu nguyên thủy như `int`, `char`, `float`, v.v.
*   Nó cũng là các kiểu dữ liệu dẫn xuất và do người dùng định nghĩa như con trỏ, cấu trúc, v.v.
*   Mảng giúp quản lý và thao tác khối lượng lớn dữ liệu dễ dàng hơn.
*   Các phần tử được truy cập bằng số chỉ mục, bắt đầu từ 0.

---

### **Slide 4: Sự cần thiết của Mảng**

**CRANES**
**SỰ CẦN THIẾT CỦA MẢNG**

*   Hãy tưởng tượng việc lưu trữ điểm của 100 sinh viên.
*   Thay vì tạo 100 biến khác nhau (diem1, diem2, ..., diem100), chúng ta có thể sử dụng một mảng như `diem[100]`.

---

### **Slide 5: Phân loại Mảng**

**CRANES**
**PHÂN LOẠI MẢNG**

**ĐỊNH NGHĨA MẢNG MỘT CHIỀU**

1.  Mảng Một chiều.
2.  Mảng Hai chiều.

**1. MẢNG MỘT CHIỀU**
*   Mảng một chiều là một tập hợp tuyến tính các phần tử cùng kiểu dữ liệu, được lưu trữ ở các vị trí bộ nhớ liền kề và được truy cập bằng một chỉ mục duy nhất.
*   Nó giống như một danh sách các phần tử được sắp xếp trong một hàng duy nhất.

---

### **Slide 6: Khai báo Mảng Một chiều**

**CRANES**
**KHAI BÁO MẢNG MỘT CHIỀU**

**Khai báo Mảng là gì?**
Khai báo một mảng trong C có nghĩa là dành riêng một khối bộ nhớ để lưu trữ nhiều giá trị cùng kiểu dữ liệu dưới một tên biến duy nhất bằng cách sử dụng một chỉ mục.

**CÚ PHÁP:**
`kieu_du_lieu ten_mang[kich_thuoc];`

*   Khi chúng ta khai báo một mảng trong C, trình biên dịch sẽ cấp phát khối bộ nhớ có kích thước được chỉ định cho tên mảng.

---

### **Slide 7: Khởi tạo Mảng Một chiều**

**CRANES**
**KHỞI TẠO MẢNG MỘT CHIỀU**

**KHỞI TẠO MẢNG:**
*   Khởi tạo trong C là quá trình gán một số giá trị ban đầu cho biến.
*   Khi mảng được khai báo hoặc được cấp phát bộ nhớ, các phần tử của mảng chứa một số giá trị rác. Vì vậy, chúng ta cần khởi tạo mảng thành một số giá trị có ý nghĩa.

Có nhiều cách để chúng ta có thể khởi tạo một mảng trong C.
*   Khởi tạo tại thời điểm biên dịch (Compile time)
*   Khởi tạo tại thời điểm chạy (Run time)

---

### **Slide 8: Khởi tạo tại thời điểm biên dịch**

**CRANES**
**KHỞI TẠO MẢNG MỘT CHIỀU**

**1. KHỞI TẠO TẠI THỜI ĐIỂM BIÊN DỊCH**
*   Trong phương pháp này, chúng ta khởi tạo mảng cùng với khai báo của nó.
*   Chúng ta sử dụng một danh sách khởi tạo để khởi tạo nhiều phần tử của mảng.
*   Danh sách khởi tạo là danh sách các giá trị được đặt trong dấu ngoặc nhọn `{ }` và cách nhau bằng dấu phẩy.
*   `int arr[5] = {10,20,30,40,50};`

---

### **Slide 9: Khởi tạo tại thời điểm chạy**

**CRANES**
**KHỞI TẠO MẢNG MỘT CHIỀU**

**2. KHỞI TẠO TẠI THỜI ĐIỂM CHẠY**
*   Gán giá trị cho các phần tử mảng trong quá trình thực thi chương trình, thường sử dụng đầu vào (ví dụ: `scanf`) hoặc logic.
*   Các giá trị không được biết trước.
*   Các giá trị được gán bằng cách sử dụng vòng lặp hoặc đầu vào của người dùng.
*   Bộ nhớ được cấp phát trong thời gian biên dịch, nhưng các giá trị được thiết lập tại thời gian chạy.

---

### **Slide 10: Truy cập phần tử Mảng**

**CRANES**
**TRUY CẬP CÁC PHẦN TỬ MẢNG**

Để truy cập các phần tử của mảng một chiều (1D) trong C, bạn sử dụng chỉ số của mảng bên trong dấu ngoặc vuông `[]`.
```c
int numbers[5] = {10, 20, 30, 40, 50};
// Truy cập và in phần tử thứ ba
printf("%d", numbers[2]); // Đầu ra: 30
```

---

### **Slide 11: Chương trình C in Mảng (Thời gian biên dịch)**

**CRANES**
**CHƯƠNG TRÌNH VỀ MẢNG MỘT CHIỀU**

**1. CHƯƠNG TRÌNH C ĐỂ IN CÁC PHẦN TỬ CỦA MẢNG (THỜI GIAN BIÊN DỊCH)**```c
#include <stdio.h>
int main()
{
    int arr[5] = {10,20,30,40,50};
    printf("Các phần tử là: ");
    for(int i=0; i<5; i++)
    {
        printf("%d ", arr[i]);
    }
    return 0;
}
```

---

### **Slide 12: Chương trình C in Mảng (Thời gian chạy)**

**CRANES**
**CHƯƠNG TRÌNH VỀ MẢNG MỘT CHIỀU**

**2. CHƯƠNG TRÌNH C ĐỂ IN CÁC PHẦN TỬ CỦA MẢNG (THỜI GIAN CHẠY)**
```c
#include <stdio.h>
int main()
{
    int arr[5];
    printf("Nhập các phần tử: ");
    for(int i=0; i<5; i++)
    {
        scanf("%d", &arr[i]);
    }
    printf("Các phần tử là: ");
    for(int i=0; i<5; i++)
    {
        printf("%d ", arr[i]);
    }
    return 0;
}
```

---

### **Slide 13: Chương trình C tính tổng các phần tử Mảng**

**CRANES**
**CHƯƠNG TRÌNH VỀ MẢNG MỘT CHIỀU**

**3. CHƯƠNG TRÌNH C ĐỂ IN TỔNG CÁC PHẦN TỬ CỦA MẢNG**
```c
#include <stdio.h>
int main()
{
    int arr[5], sum=0;
    printf("Nhập các phần tử: ");
    for(int i=0; i<5; i++)
    {
        scanf("%d", &arr[i]);
    }
    for(int i=0; i<5; i++)
    {
        sum += arr[i];
    }
    printf("Tổng các phần tử: %d", sum);
    return 0;
}
```

---

### **Slide 14: Chương trình C tìm phần tử lớn nhất**

**CRANES**
**CHƯƠNG TRÌNH VỀ MẢNG MỘT CHIỀU**

**4. CHƯƠNG TRÌNH C ĐỂ IN PHẦN TỬ LỚN NHẤT TRONG MẢNG**
```c
#include <stdio.h>
int main()
{
    int arr[5] = {56, 786, 564, 90, 34};
    int maximum = arr[0]; // Khởi tạo maximum với phần tử đầu tiên
    for(int i=1; i<5; i++)
    {
        if(arr[i] > maximum)
        {
            maximum = arr[i];
        }
    }
    printf("Phần tử lớn nhất trong mảng: %d", maximum);
    return 0;
}
```

---

### **Slide 15: Mảng Hai chiều**

**CRANES**
**MẢNG HAI CHIỀU**

**MẢNG HAI CHIỀU:**
*   Mảng 2D là một mảng của các mảng. Nó được sử dụng để lưu trữ dữ liệu dưới dạng bảng (hàng và cột), giống như một ma trận.
*   Mảng có chính xác hai chiều. chúng có thể được hình dung dưới dạng các hàng và cột được tổ chức trong một mặt phẳng hai chiều.

**CÚ PHÁP:**
*   `kieu_du_lieu ten_mang[so_hang][so_cot];`
*   `int matrix[2][3];`

---

### **Slide 16: Khởi tạo Mảng Hai chiều**

**CRANES**
**KHỞI TẠO MẢNG HAI CHIỀU**

**KHỞI TẠO TẠI THỜI ĐIỂM BIÊN DỊCH:**
```c
1. int matrix[2][3] = {{1, 2, 3}, {4, 5, 6}};
2. int matrix[2][3] = {1, 2, 3, 4, 5, 6};
```

**KHỞI TẠO TẠI THỜI ĐIỂM CHẠY:**
`kieu_du_lieu ten_mang[so_hang][so_cot];`
```c
for (int i = 0; i < so_hang; i++) {
    for (int j = 0; j < so_cot; j++) {
        scanf("%d", &ten_mang[i][j]); // Nhận đầu vào tại thời điểm chạy
    }
}
```

---

### **Slide 17: Chương trình C in Mảng 2D**

**CRANES**
**CHƯƠNG TRÌNH VỀ MẢNG HAI CHIỀU**

**5. CHƯƠNG TRÌNH C ĐỂ IN CÁC PHẦN TỬ CỦA MẢNG 2D**
```c
#include <stdio.h>
int main()
{
    int arr[2][2] = {{10, 20}, {30, 40}};
    for(int i=0; i<2; i++)
    {
        for(int j=0; j<2; j++)
        {
            printf("%d ", arr[i][j]);
        }
        printf("\n");
    }
    return 0;
}
```

---

### **Slide 18: Chương trình C cộng hai ma trận**

**CRANES**
**CHƯƠNG TRÌNH VỀ MẢNG HAI CHIỀU**

**6. CHƯƠNG TRÌNH C MINH HỌA PHÉP CỘNG HAI MA TRẬN**```c
#include <stdio.h>
int main()
{
    int arr1[2][2] = {{10, 20}, {30, 40}};
    int arr2[2][2] = {{10, 20}, {30, 40}};
    int add[2][2];
    for(int i=0; i<2; i++)
    {
        for(int j=0; j<2; j++)
        {
            add[i][j] = arr1[i][j] + arr2[i][j];
        }
    }
    for(int i=0; i<2; i++)
    {
        for(int j=0; j<2; j++)
        {
            printf("%d ", add[i][j]);
        }
        printf("\n");
    }
    return 0;
}
```

---

### **Slide 19: Chương trình C nhân hai ma trận**

**CRANES**
**CHƯƠNG TRÌNH VỀ MẢNG HAI CHIỀU**

**7. CHƯƠNG TRÌNH C MINH HỌA PHÉP NHÂN HAI MA TRẬN**
```c
#include <stdio.h>
int main()
{
    int arr1[2][2] = {{1, 2}, {3, 4}};
    int arr2[2][2] = {{5, 6}, {7, 8}};
    int product[2][2];
    for(int i=0; i<2; i++)
    {
        for(int j=0; j<2; j++)
        {
            product[i][j] = 0;
            for(int k=0; k<2; k++)
            {
                product[i][j] += arr1[i][k] * arr2[k][j];
            }
        }
    }
    printf("Tích là:\n");
    for(int i=0; i<2; i++)
    {
        for(int j=0; j<2; j++)
        {
            printf("%d ", product[i][j]);
        }
        printf("\n");
    }
    return 0;
}
```

---

### **Slide 20: Chương trình C tính tổng đường chéo**

**CRANES**
**CHƯƠNG TRÌNH VỀ MẢNG HAI CHIỀU**

**8. CHƯƠNG TRÌNH C IN TỔNG CÁC PHẦN TỬ ĐƯỜNG CHÉO**
```c
#include <stdio.h>
int main() {
    int arr[3][3] = {{1,2,3},{4,5,6},{7,8,9}};
    int sum=0;
    for(int i=0; i<3; i++)
    {
        for(int j=0; j<3; j++)
        {
            if(i==j)
            {
                sum += arr[i][j];
            }
        }
    }
    printf("Tổng các phần tử đường chéo: %d", sum);
    return 0;
}
```

---

### **Slide 21: Thực hành**

**Thực hành**

**Bài tập 1: Đảo ngược mảng 1D**
Viết chương trình C để nhập 5 số vào mảng 1D và in chúng ra theo thứ tự ngược lại.

| Đầu vào mẫu | Đầu ra mẫu |
| :--- | :--- |
| Nhập 5 số: <br> Số 1: 12 <br> Số 2: 45 <br> Số 3: 78 <br> Số 4: 23 <br> Số 5: 56 | Các số theo thứ tự ngược lại: <br> 56 23 78 45 12 |

**Bài tập 2: Tổng ma trận theo cột**
Viết chương trình tính tổng của mỗi cột trong ma trận 3x3.

| Đầu vào mẫu | Đầu ra mẫu |
| :--- | :--- |
| Nhập ma trận 3x3: <br> 1 2 3 <br> 4 5 6 <br> 7 8 9 | Tổng cột 1 = 12 <br> Tổng cột 2 = 15 <br> Tổng cột 3 = 18 |

---

### **Slide 22: Tóm tắt**

**CRANES**
**TÓM TẮT**

*   Mảng lưu trữ nhiều giá trị cùng loại bằng một tên biến duy nhất.
*   Mảng 1D được sử dụng cho dữ liệu tuyến tính;
*   Mảng 2D được sử dụng cho dữ liệu dạng bảng (ma trận).
*   Mảng có thể được khởi tạo tại thời điểm biên dịch hoặc thời điểm chạy.
*   Các phần tử được truy cập bằng cách sử dụng vị trí chỉ mục (array[i], array[i][j]).
*   Các chương trình bao gồm: in các phần tử, tính tổng, tìm max/min, và các phép toán ma trận.
*   Mảng tạo thành nền tảng để học con trỏ, chuỗi và cấu trúc dữ liệu.
