# Session 6 - Loops and AI Code Generation

### **Slide 1: Trang bìa**

**CRANES**
**Cranes Varsity**
'Nơi Công Nghệ Hội Tụ Cùng Sự Ưu Việt'

**Chương trình:**
Chương trình Phát triển Phần mềm Ô tô

**Học kỳ 1:**
Chứng chỉ Phát triển Phần mềm Ô tô (CAS)

**Học phần:**
Lập trình C/C++ cho Hệ thống Nhúng AI

**Buổi 06:**
Vòng lặp và Tạo mã AI

---

### **Slide 2: Mục tiêu và Chủ đề của Buổi học**

**CRANES**
**MỤC TIÊU VÀ CHỦ ĐỀ CỦA BUỔI HỌC**

| Giới thiệu về Vòng lặp, vòng lặp for, while, do-while | Các câu lệnh Điều khiển Vòng lặp | Tạo mã AI trong C |
| --- | --- | --- |
| Giới thiệu khái niệm về vòng lặp và tầm quan trọng của chúng trong các tác vụ lặp đi lặp lại. | • Học cách điều khiển luồng của vòng lặp bằng các câu lệnh `break` và `continue`. | Khám phá vai trò của các vòng lặp trong việc phát triển logic dựa trên AI thông qua các ví dụ tạo mã. |
| • **Thực hành** <br> • **Hỏi & Đáp và Tóm tắt** |

---

### **Slide 3: Giới thiệu về Vòng lặp**

**CRANES**
**GIỚI THIỆU VỀ VÒNG LẶP, VÒNG LẶP FOR, WHILE, DO-WHILE**

**GIỚI THIỆU VỀ VÒNG LẶP**

**VÒNG LẶP**
Quá trình lặp lại cùng một câu lệnh trong 'n' lần được gọi là lặp lại hoặc vòng lặp.
Trong lập trình C, **vòng lặp** là một cấu trúc điều khiển cho phép bạn **thực thi một khối mã lặp đi lặp lại** miễn là một điều kiện cụ thể còn đúng.

**Các tác vụ ví dụ được thực hiện bởi chương trình:**
*   In các số từ 1 đến 10
*   In các số từ 10 về 1
*   Kiểm tra xem một số cho trước có phải là số nguyên tố hay không
*   In Mẫu hình Kim tự tháp

---

### **Slide 4: Phân loại Vòng lặp**

**CRANES**
**GIỚI THIỆU VỀ VÒNG LẶP, VÒNG LẶP FOR, WHILE, DO-WHILE**

**GIỚI THIỆU VỀ VÒNG LẶP**

| Loại vòng lặp | Loại điều khiển | Mô tả |
| :--- | :--- | :--- |
| **for loop** | Vòng lặp điều khiển đầu vào (Entry-controlled) | Điều kiện được kiểm tra **trước khi** thân vòng lặp thực thi. |
| **while loop** | Vòng lặp điều khiển đầu vào (Entry-controlled) | Điều kiện được kiểm tra **trước khi** thân vòng lặp thực thi. |
| **do-while loop** | Vòng lặp điều khiển đầu ra (Exit-controlled) | Điều kiện được kiểm tra **sau khi** thân vòng lặp thực thi. |

**BẢNG 6.1 PHÂN LOẠI CÁC VÒNG LẶP TRONG C**

---

### **Slide 5: Các loại Vòng lặp - WHILE LOOP**

**CRANES**
**CÁC LOẠI VÒNG LẶP**

**a) VÒNG LẶP WHILE**
*   Vòng lặp `while` thực thi câu lệnh lặp đi lặp lại cho đến khi biểu thức trả về giá trị không (sai).

**Cú pháp:**
```c
while (<biểu_thức>)
{
    <các_câu_lệnh>;
    toán_tử_tăng/giảm;
}```

**CHƯƠNG TRÌNH**
```c
1 // Chương trình in các số từ 1 đến 10
2 #include <stdio.h>
3
4 int main() {
5    int i = 1; // Khởi tạo
6
7    while (i <= 10) { // Điều kiện
8       printf("%d\n", i); // In giá trị hiện tại của i
9       i++; // Tăng
10   }
11
12   return 0;
13 }
```

---

### **Slide 6: Các loại Vòng lặp - DO-WHILE LOOP**

**CRANES**
**CÁC LOẠI VÒNG LẶP**

**b) VÒNG LẶP DO-WHILE**
Vòng lặp `do...while` là một loại vòng lặp trong C thực thi khối mã ít nhất một lần, trước khi kiểm tra điều kiện.

Sau lần thực thi đầu tiên, nó tiếp tục lặp lại khối mã miễn là điều kiện còn đúng.
```c
do
{
    <các_câu_lệnh>;
    toán_tử_tăng/giảm;
} while (<biểu_thức>);
```

**CHƯƠNG TRÌNH**
```c
1 // Chương trình in các số chẵn từ 10 đến 0
2
3 #include<stdio.h>
4 int main()
5 {
6    int i=10;
7    do
8    {
9       printf("i=%d ",i);
10      i-=2;
11   } while(i>=0);
12   return 0;
13 }
```

---

### **Slide 7: Các loại Vòng lặp - FOR LOOP**

**CRANES**
**CÁC LOẠI VÒNG LẶP**

**c) Vòng lặp for**
*   Vòng lặp `for` thực thi câu lệnh và biểu thức vòng lặp lặp đi lặp lại cho đến khi biểu thức điều kiện trở thành sai.

**Cú pháp**
```c
for ( [biểu_thức_khởi_tạo]; [biểu_thức_điều_kiện]; [biểu_thức_vòng_lặp] )
{
    các_câu_lệnh;
}
```

**CHƯƠM TRÌNH**
```c
1 // Chương trình in các số từ 1 đến 10
2 #include <stdio.h>
3 int main() {
4    int i;
5
6    for (i = 1; i <= 10; i++) {
7       printf("%d ", i);
8    }
9    return 0;
10 }
```

---

### **Slide 8: So sánh WHILE và DO-WHILE**

**CRANES**
**CÁC LOẠI VÒNG LẶP**

**BẢNG 6.2 SỰ KHÁC BIỆT GIỮA WHILE VÀ DO-WHILE**

| Vòng lặp While | Vòng lặp Do..While |
| :--- | :--- |
| Kiểm tra các điều kiện trước khi thực thi thực tế thân vòng lặp. | Thân vòng lặp được thực thi trước và sau đó các điều kiện sẽ được kiểm tra. |
| **Cú pháp:** <br> `Khởi tạo;` <br> `while(điều_kiện){` <br> `...câu lệnh;` <br> `...tăng/giảm;` <br> `}` | **Cú pháp:** <br> `do {` <br> `...câu lệnh;` <br> `...tăng/giảm;` <br> `}while(điều_kiện);` |
| **Ví dụ:** <br> `int i=10;` <br> `while(i<=0){` <br> `printf("I=%d \n",i);` <br> `i++;` <br> `}` <br> Ở đây giá trị của i=10 không nhỏ hơn 0 nên thân vòng lặp sẽ không được thực thi. | **Ví dụ:** <br> `int i=10;` <br> `do {` <br> `printf("I=%d \n",i);` <br> `i++;` <br> `}while(i<=0);` <br> Ở đây giá trị của i=10 không nhỏ hơn 0 nhưng ít nhất một lần thân vòng lặp được thực thi và in ra giá trị của i=10. |

---

### **Slide 9: Vòng lặp lồng nhau**

**CRANES**
**VÒNG LẶP LỒNG NHAU**

*   Một vòng lặp bên trong một vòng lặp khác được gọi là vòng lặp lồng nhau.
*   Một vòng lặp `while` bên trong một vòng lặp `while` hoặc một vòng lặp `for` bên trong một vòng lặp `for` được gọi là vòng lặp lồng nhau.
*   Đây là một ví dụ về vòng lặp `for` lồng nhau để in một mẫu.

```c
1 /* Chương trình in một mẫu
2 *
3 **
4 ***
5 ****
6 *****
7 */
8 #include<stdio.h>
9 int main()
10 {
11    int r,c;
12    r=c=0;
13
14    for(r=1; r<=5; r++) // vòng lặp for ngoài cùng
15    {
16       for(c=1; c<=r; c++) // vòng lặp for trong cùng
17       {
18          printf("*");
19       }
20       printf("\n");
21    }
22    return 0;
23 }
```

---

### **Slide 10: Vòng lặp vô hạn**

**CRANES**
**VÒNG LẶP VÔ HẠN**

*   Vòng lặp vô hạn xảy ra khi điều kiện tiếp tục vòng lặp trong câu lệnh `while`, `for` hoặc `do...while` không bao giờ trở thành sai.
*   Vòng lặp sẽ không kết thúc nếu không có `break`, `return`, hoặc `goto` trong câu lệnh.
*   Một cách thuận tiện để chỉ định một vòng lặp vô hạn bằng cách sử dụng câu lệnh `while` và `for` là:

| `While(1)` | `for(;;)` |
| :--- | :--- |
| `{` | `{` |
| `}` | `}` |

---

### **Slide 11: Vòng lặp vô hạn trong Hệ thống nhúng**

**CRANES**
**VÒNG LẶP VÔ HẠN TRONG HỆ THỐNG NHÚNG**

Hệ thống nhúng hầu như luôn chứa một vòng lặp vô hạn.

*   Sự khác biệt cơ bản giữa hệ thống nhúng và các chương trình được viết cho các nền tảng máy tính khác.
*   Vòng lặp vô hạn thường bao quanh một phần quan trọng của chức năng của chương trình.
*   Cần thiết vì công việc của phần mềm nhúng không bao giờ kết thúc.
*   Dự định chạy cho đến khi thế giới kết thúc hoặc bo mạch được đặt lại, tùy điều gì xảy ra trước.
*   Đối với các hệ thống nhúng, nếu phần mềm ngừng chạy, phần cứng sẽ trở nên vô dụng.

---

### **Slide 12: Câu lệnh Break và Continue**

**CRANES**
**CÂU LỆNH BREAK VÀ CONTINUE**

**CÁC CÂU LỆNH ĐIỀU KHIỂN VÒNG LẶP**

*   **break**
    *   Gây ra việc thoát ngay lập tức khỏi một câu lệnh `while`, `for`, `do...while` hoặc `switch`.
    *   Việc thực thi chương trình tiếp tục với câu lệnh đầu tiên sau cấu trúc vòng lặp/switch.
    *   Các cách sử dụng phổ biến của câu lệnh `break`:
        *   Thoát sớm khỏi một vòng lặp
        *   Bỏ qua phần còn lại của một câu lệnh `switch`

**CHƯƠNG TRÌNH C MINH HỌA VIỆC SỬ DỤNG CÂU LỆNH BREAK:**
```c
1 // Từ khóa break được sử dụng để thoát khỏi vòng lặp
2 // Chương trình kiểm tra xem một số cho trước có phải là số nguyên tố hay không
3 #include <math.h>
4 #include <stdio.h>
5 int main()
6 {
7    int num,i;
8    printf("\n NHẬP MỘT SỐ :");
9    scanf("%d",&num);
10
11   for(i=2; i <= sqrt(num); i++) {
12      if(num % i == 0)
13         break; // nếu num chia hết cho i thì vòng lặp kết thúc
14   }
15
16   if(i > sqrt(num))
17      printf("\n SỐ NGUYÊN TỐ");
18   else
19      printf("\n KHÔNG PHẢI SỐ NGUYÊN TỐ");
20   return 0;
21 }
```

---

### **Slide 13: Câu lệnh Break và Continue (tiếp)**

**CRANES**
**CÂU LỆNH BREAK VÀ CONTINUE**

**CÁC CÂU LỆNH ĐIỀU KHIỂN VÒNG LẶP (tiếp..)**

*   **continue**
    *   Bỏ qua các câu lệnh còn lại trong thân của một câu lệnh `while`, `for` hoặc `do...while`.
    *   Tiến hành với lần lặp tiếp theo của vòng lặp.
    *   **while và do...while**
        *   Kiểm tra tiếp tục vòng lặp được đánh giá ngay sau khi câu lệnh `continue` được thực thi.
    *   **for**
        *   Biểu thức cập nhật được thực thi, sau đó kiểm tra tiếp tục vòng lặp được đánh giá.

```c
1  // Từ khóa continue được sử dụng để bỏ qua giá trị hiện tại và tiếp tục vòng lặp
2  // Chương trình tìm tổng của n số
3  #include <stdio.h>
4  int main()
5  {
6     int number, sum = 0, count = 0;
7     printf("Nhập 4 số dương, MỖI SỐ TRÊN MỘT DÒNG:\n");
8     while (count < 4)
9     {
10        scanf("%d", &number);
11        if (number <= 0) // Sửa lỗi logic, kiểm tra số không dương
12        {
13           printf("LỖI: số âm (hoặc không)! \
14           Nhập lại số và tiếp tục:\n");
15           continue;
16        }
17        sum = sum + number;
18        count++;
19     }
20     printf("%d là tổng của %d số", sum, count);
21     return 0;
22  }
```

---

### **Slide 14: Tóm tắt**

**CRANES**
**TÓM TẮT**

*   Một **vòng lặp** trong lập trình được sử dụng để **lặp lại một khối mã nhiều lần** cho đến khi một điều kiện nhất định được đáp ứng.
*   `for` là tốt nhất khi số lần lặp đã được biết.
*   `while` và `do...while` là tốt nhất khi số lần lặp chưa được biết.
*   `do...while` đảm bảo mã chạy ít nhất một lần.

---

### **Slide 15: Thực hành**

**Thực hành**

Viết chương trình tính giai thừa của một số dương cho trước bằng cách sử dụng:
- vòng lặp `for`
- vòng lặp `while`
- vòng lặp `do-while`

| Đầu vào mẫu: | Đầu ra mẫu: |
| :--- | :--- |
| 5 | Sử dụng vòng lặp for: 120 <br> Sử dụng vòng lặp while: 120 <br> Sử dụng vòng lặp do - while: 120 |

Viết chương trình đếm số chữ số trong một số bằng logic vòng lặp.

| Đầu vào mẫu: | Đầu ra mẫu: |
| :--- | :--- |
| Nhập số: 123456 | Số chữ số: 6 |

---

### **Slide 16: Cảm ơn**

**CRANES**

**CẢM ƠN BẠN**
