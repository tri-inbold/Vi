# Session 5 - Condition Statements and AI Code Generation

### **Slide 1: Trang bìa**

**Cranes Varsity**
'Nơi Công Nghệ Gặp Gỡ Sự Hoàn Hảo'

**Chương trình:**
Chương trình Phát triển Phần mềm Ô tô

**Học kỳ 1:**
Chứng chỉ Phát triển Phần mềm Ô tô (CAS)

**Học phần:**
Lập trình C/C++ cho Hệ thống Nhúng AI

**Buổi 01:**
Các Câu lệnh Điều kiện và Tạo mã AI

---

### **Slide 2: Mục tiêu và Chủ đề Buổi học**

**CRANES**
**MỤC TIÊU VÀ CHỦ ĐỀ BUỔI HỌC**

| Giới thiệu về Các Câu lệnh Điều kiện trong C, if, If-else, if lồng nhau, Câu lệnh Switch, Toán tử Ba ngôi | Tạo mã được AI Hỗ trợ cho Lập trình C | Gỡ lỗi & Tối ưu hóa |
| :--- | :--- | :--- |
| Để hiểu và triển khai các câu lệnh if, if-else, if lồng nhau, switch và toán tử ba ngôi. | **Công cụ AI để tạo mã C, Các ví dụ được AI Hỗ trợ** <br> Để khám phá việc tạo mã được AI hỗ trợ trong C bằng các công cụ, với các ví dụ thực hành để hỗ trợ viết mã hiệu quả. | Để học các kỹ thuật gỡ lỗi và tối ưu hóa để xác định và sửa lỗi, và cải thiện hiệu suất mã. |
| **Thực hành và Ví dụ** |

---

### **Slide 3: Điều kiện tiên quyết cho các Câu lệnh Điều kiện**

**ĐIỀU KIỆN TIÊN QUYẾT CHO CÁC CÂU LỆNH ĐIỀU KIỆN**

Các câu lệnh luồng điều khiển của một ngôn ngữ chỉ định thứ tự mà các chương trình được thực hiện. Có ba loại lệnh điều khiển trong C, chúng là:

**1. Lệnh Điều khiển Tuần tự (Sequence Control Instructions)**
*   Đảm bảo rằng các lệnh được thực thi theo cùng một thứ tự mà chúng xuất hiện trong chương trình.
*   Được tích hợp sẵn trong C.
*   Các chương trình được thực thi tuần tự theo mặc định.

**2. Lệnh Điều khiển Lựa chọn hoặc Quyết định (Selection or Decision Control Instructions)**
*   Cho phép chương trình đưa ra quyết định về lệnh nào sẽ được thực thi tiếp theo.
*   C có ba loại: `if`, `if...else`, và `switch`.

**3. Lệnh Điều khiển Lặp lại hoặc Vòng lặp (Iteration or Loop Control Instructions)**
*   Giúp máy tính thực thi một nhóm các câu lệnh lặp đi lặp lại.
*   C có ba loại: `while`, `do...while` và `for`.

---

### **Slide 4: Giới thiệu về Các Câu lệnh Điều kiện**

**CÁC CÂU LỆNH ĐIỀU KIỆN**

*   Trong C, các chương trình có thể chọn phần mã nào sẽ thực thi dựa trên một điều kiện nào đó.
*   Khả năng này được gọi là ra quyết định và các câu lệnh được sử dụng cho nó được gọi là câu lệnh điều kiện.
*   Những câu lệnh này đánh giá một hoặc nhiều điều kiện và đưa ra quyết định liệu có thực thi một khối mã hay không.

---

### **Slide 5: Câu lệnh IF**

**CÂU LỆNH IF**

**1. CÂU LỆNH IF:**
*   Câu lệnh If là câu lệnh ra quyết định đơn giản nhất.
*   Nó được sử dụng để quyết định xem một câu lệnh hoặc khối câu lệnh nhất định có được thực thi hay không.
*   Tức là nếu một điều kiện nhất định là đúng thì một khối câu lệnh được thực thi, ngược lại thì không.
*   Một điều kiện là bất kỳ biểu thức nào đánh giá là đúng hoặc sai (hoặc các giá trị có thể chuyển đổi thành đúng hoặc sai).

**CÚ PHÁP:**
```c
if(điều_kiện)
{
    //mã lệnh
}
```

---

### **Slide 6: Câu lệnh IF - Lưu đồ và Ví dụ**

**LƯU ĐỒ:**
[Lưu đồ cho thấy luồng bắt đầu tại một khối "điều kiện". Nếu đúng (true), nó đi đến "câu lệnh 1" rồi đến "các câu lệnh khác". Nếu sai (false), nó đi thẳng đến "các câu lệnh khác".]

**CHƯƠNG TRÌNH C MINH HỌA VIỆC SỬ DỤNG CÂU LỆNH IF**
```c
#include <stdio.h>
int main() {
    int n;
    printf("nhập n:");
    scanf("%d",&n);
    if(n==5) {
        printf("Giá trị của n là:%d",n);
    }
    return 0;
}
```
**ĐẦU RA**
```
nhập n:5
Giá trị của n là:5
```

---

### **Slide 7: Câu lệnh IF-ELSE**

**CÂU LỆNH IF-ELSE**

**CÂU LỆNH IF – ELSE**
`If else` trong C là một phần mở rộng của câu lệnh `if`, không chỉ cho phép chương trình thực thi một khối mã nếu một điều kiện là đúng, mà còn một khối khác nếu điều kiện là sai.

Điều này cho phép đưa ra quyết định với hai kết quả có thể xảy ra.

**CÚ PHÁP:**
```c
if (điều_kiện) {
    // Mã để thực thi nếu điều kiện là đúng
}
else {
    // Mã để thực thi nếu điều kiện là sai
}
```

---

### **Slide 8: Câu lệnh IF-ELSE - Lưu đồ và Ví dụ**

**LƯU ĐỒ:**
[Lưu đồ bắt đầu, đi đến một khối quyết định "biểu_thức_boolean". Nếu "điều kiện là đúng", nó thực thi "mã if". Nếu "điều kiện là sai", nó thực thi "mã else". Cả hai nhánh sau đó hợp nhất và tiếp tục đến "phần còn lại của mã".]

**CHƯƠNG TRÌNH C MINH HỌA VIỆC SỬ DỤNG CÂU LỆNH IF-ELSE**
```c
#include <stdio.h>
int main() {
    int n = -7;
    if (n < 0)
    {
        printf("Âm");
    }
    else
    {
        printf("Không phải số âm");
    }
    return 0;
}
```
**ĐẦU RA**
```
Âm
```

---

### **Slide 9: Câu lệnh IF-ELSE Lồng nhau**

**CÂU LỆNH IF-ELSE LỒNG NHAU**

**CÂU LỆNH IF LỒNG NHAU**
*   `if` lồng nhau trong C là một câu lệnh `if` là mục tiêu của một câu lệnh `if` khác.
*   Các câu lệnh `if` lồng nhau có nghĩa là một câu lệnh `if` bên trong một câu lệnh `if` khác. / câu lệnh `if-else` bên trong câu lệnh `if-else`.
*   C cho phép chúng ta lồng các câu lệnh `if` bên trong các câu lệnh `if`, tức là, chúng ta có thể đặt một câu lệnh `if` bên trong một câu lệnh `if` khác.

---

### **Slide 10: Câu lệnh IF-ELSE Lồng nhau - Lưu đồ**

[Lưu đồ mô tả logic if-else lồng nhau. Bắt đầu với một "Điều kiện" chính. Nếu "SAI", nó thực thi một "Câu lệnh(s)" và kết thúc. Nếu "ĐÚNG", nó thực thi một "Câu lệnh(s)" và sau đó gặp một "Điều kiện lồng nhau". Nếu điều kiện lồng nhau này là "SAI", nó thực thi một "Câu lệnh(s)" khác. Nếu "ĐÚNG", nó thực thi một "Câu lệnh(s)" khác. Cả hai nhánh của điều kiện lồng nhau đều dẫn đến "KẾT THÚC IF LỒNG NHAU", sau đó là một "Câu lệnh(s)" cuối cùng trước khi "KẾT THÚC IF".]

---

### **Slide 11: Ví dụ về IF Lồng nhau**

**CÂU LỆNH IF-ELSE LỒNG NHAU**

**CHƯƠNG TRÌNH C MINH HỌA CÂU LỆNH IF LỒNG NHAU**
```c
#include <stdio.h>
int main() {
    int num = 10;
    if (num > 0) {
        printf("Số dương.\n");
        if (num % 2 == 0) {
            printf("Số chẵn.\n");
        }
    }
    return 0;
}
```
**ĐẦU RA:**
```
Số dương.
Số chẵn.
```

---

### **Slide 12: Ví dụ về IF-ELSE Lồng nhau (Số lớn nhất)**

**CÂU LỆNH IF-ELSE LỒNG NHAU**

**CHƯƠNG TRÌNH C IN RA SỐ LỚN NHẤT TRONG BA SỐ**
```c
#include <stdio.h>
int main() {
    int a, b, c;
    printf("Nhập ba số: ");
    scanf("%d %d %d", &a, &b, &c);
    if (a > b) {
        if (a > c) {
            printf("Số lớn nhất là: %d\n", a);
        } else {
            printf("Số lớn nhất là: %d\n", c);
        }
    } else {
        if (b > c) {
            printf("Số lớn nhất là: %d\n", b);
        } else {
            printf("Số lớn nhất là: %d\n", c);
        }
    }
    return 0;
}
```
**ĐẦU RA:**
```
Nhập ba số: 10 89 67
Số lớn nhất là: 89
```

---

### **Slide 13: Ví dụ về IF-ELSE Lồng nhau (Xếp loại)**

**CÂU LỆNH IF-ELSE LỒNG NHAU**

**CHƯƠNG TRÌNH C MINH HỌA VIỆC SỬ DỤNG CẤU TRÚC IF LỒNG NHAU (ELSE-IF)**
```c
#include <stdio.h>
int main() {
    int marks;
    printf("Nhập điểm: ");
    scanf("%d", &marks);
    if (marks >= 50) {
        printf("Bạn đã đỗ!\n");
        if (marks >= 90) {
            printf("Xếp loại: A\n");
        } else if (marks >= 75) {
            printf("Xếp loại: B\n");
        } else {
            printf("Xếp loại: C\n");
        }
    } else {
        printf("Bạn đã trượt.\n");
    }
    return 0;
}
```
**ĐẦU RA:**
```
Nhập điểm: 67
Bạn đã đỗ!
Xếp loại: C
```

---

### **Slide 14: Câu lệnh SWITCH**

**CÂU LỆNH SWITCH**

*   Câu lệnh Switch trong C là một cấu trúc luồng điều khiển cho phép một biến được kiểm tra sự bằng nhau với nhiều giá trị hằng số.
*   Nó cung cấp một giải pháp thay thế cho nhiều câu lệnh if-else, giúp mã dễ đọc và hiệu quả hơn khi xử lý nhiều điều kiện.
*   Trong C, câu lệnh switch là một cấu trúc luồng điều khiển cho phép bạn thực thi một trong nhiều khối mã dựa trên giá trị của một biểu thức.

---

### **Slide 15: Quy tắc của Câu lệnh SWITCH**

**CÂU LỆNH SWITCH**

*   Biểu thức bên trong `switch` phải là kiểu số nguyên hoặc ký tự.
*   Mỗi nhãn `case` phải chứa một biểu thức hằng (ví dụ: số, ký tự).
*   Câu lệnh `break` được sử dụng để thoát khỏi khối `switch`; nếu không, việc thực thi sẽ "rơi" xuống `case` tiếp theo.
*   `default case` là tùy chọn nhưng sẽ thực thi khi không có `case` nào khớp.

---

### **Slide 16: Cú pháp Câu lệnh SWITCH**

**CÂU LỆNH SWITCH**
```c
switch (BiểuThứcSốNguyên)
{
    case HằngSố1 :
        CâuLệnh(s);      // tùy chọn
    case HằngSố2 :
        CâuLệnh(s);      // tùy chọn
    ...
    default :            // tùy chọn
        CâuLệnh(s);      // tùy chọn
}
```

---

### **Slide 17: Cách hoạt động của SWITCH**

**CÁCH HOẠT ĐỘNG CỦA SWITCH:**
[Lưu đồ cho thấy một "biểu thức đơn" được đánh giá. Nó được so sánh tuần tự với "case hằng số 1?", "case hằng số 2?", "case hằng số 3?". Nếu tìm thấy một kết quả khớp (Có), "khối mã" tương ứng sẽ được thực thi. Nếu không có kết quả khớp nào (Không), "mã mặc định" sẽ được thực thi.]

---

### **Slide 18: Ví dụ về Câu lệnh SWITCH**

**CÂU LỆNH SWITCH**

**CHƯƠNG TRÌNH C MINH HỌA VIỆC SỬ DỤNG CÂU LỆNH SWITCH**
```c
#include <stdio.h>
int main() {
    int num;
    printf("Nhập một số nguyên: ");
    scanf("%d", &num);
    switch (num % 2) {
        case 0:
            printf("%d là số chẵn.\n", num);
            break;
        case 1:
            printf("%d là số lẻ.\n", num);
            break;
    }
    return 0;
}
```
**ĐẦU RA:**
```
Nhập một số nguyên: 6
6 là số chẵn.
```

---

### **Slide 19: Toán tử Ba ngôi**

**TOÁN TỬ BA NGÔI**

**TOÁN TỬ BA NGÔI**
Nó là toán tử ba ngôi trong C vì nó hoạt động trên ba toán hạng.
Nó còn được gọi là toán tử điều kiện.

Toán tử điều kiện trong C có phần tương tự như câu lệnh if-else vì nó tuân theo cùng một thuật toán như câu lệnh if-else.
Nhưng toán tử điều kiện chiếm ít không gian hơn và giúp viết các câu lệnh if-else theo cách ngắn nhất có thể.

Toán tử điều kiện có thể có dạng:
`biến = BiểuThức1 ? BiểuThức2 : BiểuThức3;`

Hoặc cú pháp cũng có thể ở dạng này:
`biến = (điều_kiện) ? BiểuThức2 : BiểuThức3;`

Hoặc cú pháp cũng có thể ở dạng này:
`(điều_kiện) ? (biến = BiểuThức2) : (biến = BiểuThức3);`

---

### **Slide 20: Lưu đồ Toán tử Ba ngôi**

**LƯU ĐỒ – TOÁN TỬ BA NGÔI**
[Lưu đồ cho thấy một "Biểu thức 1" (điều kiện) được đánh giá. Nếu "Đúng", "Phần '?' sẽ được thực thi", dẫn đến "Biểu thức 2". Nếu "Sai", "Phần ':' sẽ được thực thi", dẫn đến "Biểu thức 3". Kết quả từ Biểu thức 2 hoặc 3 trở thành "Giá trị kết quả của Biểu thức", sau đó được gán cho "Biến".]

---

### **Slide 21: Ví dụ về Toán tử Ba ngôi (So sánh 2 số)**

**CHƯƠNG TRÌNH VỀ TOÁN TỬ BA NGÔI**

**CHƯƠNG TRÌNH TÌM SỐ LỚN NHẤT TRONG HAI SỐ SỬ DỤNG TOÁN TỬ BA NGÔI**
```c
#include <stdio.h>
int main()
{
    int m = 5, n = 4;
    (m > n) ? printf("m lớn hơn n tức là %d > %d", m, n)
            : printf("n lớn hơn m tức là %d > %d", n, m);
    return 0;
}
```
**ĐẦU RA**
```
m lớn hơn n tức là 5 > 4
```

---

### **Slide 22: Ví dụ về Toán tử Ba ngôi (So sánh 3 số)**

**CHƯƠNG TRÌNH VỀ TOÁN TỬ BA NGÔI**

**CHƯƠNG TRÌNH C TÌM SỐ LỚN NHẤT TRONG BA SỐ SỬ DỤNG TOÁN TỬ BA NGÔI**
```c
#include <stdio.h>
int main()
{
    int a, b, c, largest;
    printf("Nhập ba số: ");
    scanf("%d %d %d", &a, &b, &c);
    largest = (a > b && a > c) ? a : ((b > c) ? b : c); // Sửa logic
    printf("Số lớn nhất là: %d\n", largest);
    return 0;
}
```
**ĐẦU RA**
```
Nhập ba số: 1 89 0
Số lớn nhất là: 89
```

---

### **Slide 23: Tạo mã được AI Hỗ trợ**

**TẠO MÃ ĐƯỢC AI HỖ TRỢ CHO LẬP TRÌNH C**

**TẠO MÃ ĐƯỢC AI HỖ TRỢ LÀ GÌ?**

Tạo mã được AI hỗ trợ đề cập đến việc sử dụng các công cụ Trí tuệ nhân tạo (AI) để giúp viết, hoàn thành và cải thiện mã tự động dựa trên các hướng dẫn ngôn ngữ tự nhiên hoặc mã một phần.

Các công cụ này được đào tạo trên các cơ sở mã lớn và tài liệu lập trình.
**Mục tiêu:** Tăng năng suất, giảm lỗi và giúp các nhà phát triển (đặc biệt là người mới bắt đầu) học và viết mã nhanh hơn.

---

### **Slide 24: Quy trình Tạo mã AI**

**TẠO MÃ ĐƯỢC AI HỖ TRỢ CHO LẬP TRÌNH C**

**1. Viết một Lời nhắc (Prompt) Rõ ràng**
Sử dụng các hướng dẫn đơn giản, dựa trên mục tiêu.
Ví dụ: "Viết một chương trình C để kiểm tra xem một số có phải là số chẵn không."

**2. AI Xử lý Yêu cầu**
Công cụ diễn giải lời nhắc bằng cách sử dụng NLP và tìm kiếm các mẫu.
Nó sử dụng kiến thức đã học của mình để tạo ra một phản hồi phù hợp.

**3. AI Tạo mã**
Một chương trình C đầy đủ, hoạt động được tạo ra.
Đầu ra cũng có thể bao gồm các bình luận hoặc giải thích logic.

---

### **Slide 25: Quy trình Tạo mã AI (tiếp)**

**TẠO MÃ ĐƯỢC AI HỖ TRỢ CHO LẬP TRÌNH C**

**4. Người dùng Đánh giá và Kiểm tra Mã**
Bạn sao chép mã vào trình biên dịch của mình (ví dụ: Code::Blocks, GCC).
Chạy nó, kiểm tra đầu ra và đảm bảo tính đúng đắn.

**5. Yêu cầu Sửa đổi hoặc Cải tiến**
Bây giờ bạn có thể hỏi: "Bây giờ hãy thêm xác thực đầu vào." "Chuyển đổi điều này để sử dụng toán tử ba ngôi."
"Giải thích logic."

**6. Tinh chỉnh và Học hỏi**
Bước cuối cùng là học từ mã.
Sửa đổi nó thủ công, thử các trường hợp biên và áp dụng nó cho các vấn đề khác.

---

### **Slide 26: Luồng làm việc với AI**

**TẠO MÃ ĐƯỢC AI HỖ TRỢ CHO LẬP TRÌNH C**

**Lời nhắc:** "Viết một chương trình C để kiểm tra chẵn hoặc lẻ"
↓
**Phản hồi của AI:** (Tạo mã hoạt động)
↓
**Học viên:** "Bây giờ hãy thêm các bình luận giải thích"
↓
**AI:** Thêm các bình luận nội tuyến để học hỏi
↓
**Học viên:** Sao chép mã vào IDE, kiểm tra và hiểu logic

---

### **Slide 27: Công cụ được AI Hỗ trợ**

**CÔNG CỤ ĐƯỢC AI HỖ TRỢ**

**ChatGPT (bởi OpenAI)**
**Nó là gì:** Mô hình AI đàm thoại có thể tạo mã từ ngôn ngữ tự nhiên.

**Nó giúp gì trong C:**
*   Viết các chương trình C đầy đủ từ các câu lệnh bài toán
*   Gỡ lỗi hoặc giải thích mã khó hiểu
*   Sửa đổi mã hiện có hoặc tối ưu hóa nó
*   Tạo ví dụ để thực hành (vòng lặp, mảng, con trỏ, v.v.)

**Lời nhắc ví dụ:**
"Viết một chương trình C để kiểm tra xem một số có phải là số chẵn không."

---

### **Slide 28: Bảng các Lời nhắc AI**

**BẢNG 5.1 CÁC LỜI NHẮC AI**

| Chủ đề | Lời nhắc AI (Yêu cầu Chương trình) |
| :--- | :--- |
| **1. Câu lệnh if** | Viết một chương trình C để kiểm tra xem một số có phải là số dương không. |
| **2. Câu lệnh if-else** | Viết một chương trình C để kiểm tra xem một số là chẵn hay lẻ bằng cách sử dụng if-else. |
| **3. Câu lệnh if lồng nhau** | Viết một chương trình C để tìm số lớn nhất trong ba số bằng cách sử dụng if lồng nhau. |
| **4. Bậc thang if-else-if** | Viết một chương trình C để phân loại điểm của học sinh dựa trên điểm số bằng cách sử dụng bậc thang if-else-if. |
| **5. Câu lệnh Switch** | Viết một chương trình C sử dụng switch case để hiển thị ngày trong tuần (1 đến 7). |
| **6. Switch - Máy tính đơn giản** | Viết một chương trình C sử dụng switch case để xây dựng một máy tính đơn giản (cộng, trừ, v.v.). |
| **7. Toán tử Ba ngôi (Max của 2)** | Viết một chương trình C để tìm giá trị lớn nhất của hai số bằng toán tử ba ngôi. |
| **8. Toán tử Ba ngôi (Dương/Âm)** | Viết một chương trình C để kiểm tra xem một số là dương hay âm bằng toán tử ba ngôi. |

---

### **Slide 29: Gỡ lỗi và Tối ưu hóa**

**GỠ LỖI**

**Gỡ lỗi trong Lập trình C là gì?**
Gỡ lỗi là quá trình tìm và sửa lỗi (bugs) trong chương trình C của bạn để nó hoạt động chính xác.

**Gỡ lỗi giúp:**
*   Sửa lỗi logic hoặc cú pháp
*   Hiểu tại sao một chương trình không hoạt động như mong đợi
*   Cải thiện chất lượng và độ tin cậy của mã của bạn

---

### **Slide 30: Các loại Lỗi (Bug)**

**GỠ LỖI**

| Loại Lỗi | Ví dụ | Điều gì xảy ra |
| :--- | :--- | :--- |
| **Lỗi cú pháp (Syntax Error)** | Thiếu `;` hoặc cú pháp `if` sai | Chương trình sẽ không biên dịch |
| **Lỗi logic (Logical Error)** | Sử dụng `=` thay vì `==` trong điều kiện | Chương trình biên dịch nhưng cho kết quả sai |
| **Lỗi thời gian chạy (Runtime Error)** | Chia cho không, truy cập mảng không hợp lệ | Chương trình bị treo hoặc hoạt động kỳ lạ |

---

### **Slide 31: Quy trình Gỡ lỗi**

**GỠ LỖI**

**Viết và Biên dịch Mã**
Bắt đầu bằng cách viết một chương trình C và biên dịch nó bằng một trình biên dịch (ví dụ: gcc, Turbo C, v.v.).
Quan sát Lỗi.
*   Lỗi Cú pháp: Hiển thị trong quá trình biên dịch (ví dụ: thiếu dấu chấm phẩy).
*   Lỗi Thời gian chạy: Sập trong quá trình thực thi (ví dụ: chia cho không).
*   Lỗi Logic: Đầu ra sai, không hiển thị lỗi.

**Sử dụng Công cụ/Kỹ thuật Gỡ lỗi**
*   Chèn `printf()` để kiểm tra giá trị của các biến (gỡ lỗi thủ công).
*   Sử dụng một trình gỡ lỗi (ví dụ: gdb) để đi qua mã từng dòng một.
*   Theo dõi giá trị biến và luồng điều khiển.

**Xác định và Sửa lỗi**
*   Sửa logic hoặc cú pháp.
*   Biên dịch lại và kiểm tra lại.

**Lặp lại cho đến khi không còn lỗi**
*   Tiếp tục chu trình kiểm tra và sửa lỗi cho đến khi chương trình hoạt động như mong đợi.

---

### **Slide 32: Kỹ thuật Gỡ lỗi - Gỡ lỗi thủ công**

**KỸ THUẬT GỠ LỖI**

**1. Gỡ lỗi thủ công bằng câu lệnh `printf()`**
Gỡ lỗi thủ công với `printf()` có nghĩa là thêm các lệnh gọi hàm `printf()` tạm thời vào các điểm chiến lược trong mã của bạn để:
*   Theo dõi giá trị biến
*   Theo dõi luồng chương trình
*   Xác định nơi có sự cố

Đây là một trong những kỹ thuật đơn giản và được sử dụng rộng rãi nhất, đặc biệt khi mới bắt đầu với lập trình C.

---

### **Slide 33: Kỹ thuật Gỡ lỗi - Sử dụng Debugger**

**KỸ THUẬT GỠ LỖI**

**2. Sử dụng một Trình gỡ lỗi (như gdb)**
GDB (GNU Debugger) là một công cụ dòng lệnh giúp bạn:
*   Chạy một chương trình từng bước
*   Tạm dừng thực thi tại các dòng cụ thể (điểm dừng - breakpoints)
*   Kiểm tra các biến và bộ nhớ
*   Tìm lỗi phân đoạn (segmentation faults), lỗi logic, và nhiều hơn nữa
*   Nó được sử dụng rộng rãi trong các môi trường dựa trên Linux để gỡ lỗi các chương trình C/C++.

---

### **Slide 34: Bảng hướng dẫn GDB**

**KỸ THUẬT GỠ LỖI**

**BẢNG 5.3 GỠ LỖI VỚI GDB**

| Bước | Mô tả | Lệnh/Hành động GDB | Giải thích Ví dụ |
| :--- | :--- | :--- | :--- |
| **1** | Viết chương trình C của bạn | Tạo tệp .c của bạn | `int main() { int a = 10, b = 0; int result = a / b; ... }` |
| **2** | Biên dịch với thông tin gỡ lỗi | `gcc -g program.c -o program` | Cờ `-g` bao gồm các ký hiệu gỡ lỗi cần thiết cho GDB |
| **3** | Bắt đầu GDB | `gdb ./program` | Khởi chạy GDB với chương trình đã biên dịch của bạn |
| **4** | Đặt điểm dừng | `break main` hoặc `break 5` | Dừng chương trình tại hàm `main()` hoặc tại dòng 5 |
| **5** | Chạy chương trình bên trong GDB | `run` | Bắt đầu thực thi và tạm dừng tại điểm dừng |
| **6** | Đi qua mã | `next` hoặc `step` | `next` chuyển đến dòng tiếp theo, `step` đi vào bên trong các lệnh gọi hàm |
| **7** | In giá trị biến | `print a`, `print b`, `print result` | Kiểm tra giá trị hiện tại của các biến |
| **8** | Tiếp tục thực thi chương trình | `continue` | Chạy cho đến điểm dừng tiếp theo hoặc chương trình kết thúc |
| **9** | Thoát GDB | `quit` | Thoát khỏi trình gỡ lỗi |

---

### **Slide 35: Tối ưu hóa**

**TỐI ƯU HÓA**

**TỐI ƯU HÓA:**
*   Tối ưu hóa có nghĩa là làm cho chương trình C của bạn chạy nhanh hơn, sử dụng ít bộ nhớ hơn, hoặc hoạt động tốt hơn, mà không thay đổi những gì nó làm.
*   Hãy nghĩ về nó như việc dọn dẹp và cải thiện mã của bạn để nó thông minh và hiệu quả hơn.

---

### **Slide 36: Sự cần thiết của Tối ưu hóa**

**TỐI ƯU HÓA**

**BẢNG 5.4 SỰ CẦN THIẾT CỦA TỐI ƯU HÓA**

| Kịch bản | Tại sao phải tối ưu hóa? |
| :--- | :--- |
| **Thực thi chương trình chậm** | Làm cho nó nhanh hơn để cải thiện trải nghiệm người dùng |
| **Tiêu thụ bộ nhớ cao** | Tiết kiệm RAM, đặc biệt trong các hệ thống nhúng |
| **Các tính toán lặp lại hoặc không cần thiết** | Giảm tải CPU |
| **Môi trường Di động/IoT/Nhúng** | Cải thiện tuổi thọ pin và hiệu suất |

---

### **Slide 37: Các loại Tối ưu hóa - Thời gian biên dịch**

**TỐI ƯU HÓA**

**CÁC LOẠI TỐI ƯU HÓA:**
**1. TỐI ƯU HÓA THỜI GIAN BIÊN DỊCH** đề cập đến quá trình mà trình biên dịch C tự động cải thiện mã của bạn trong quá trình biên dịch để làm cho nó:
*   Chạy nhanh hơn
*   Sử dụng ít bộ nhớ hơn
*   Hiệu quả hơn

Tất cả điều này xảy ra trước khi chương trình chạy – tại thời điểm biên dịch.
Bởi vì những tối ưu hóa này được thực hiện bởi trình biên dịch (như gcc, clang) khi bạn biên dịch mã — không phải trong thời gian chạy.

`gcc -O2 mycode.c -o optimized_program`

Cờ `-O2` báo cho trình biên dịch:
"Vui lòng tối ưu hóa mã của tôi trong quá trình biên dịch."

---

### **Slide 38: Các loại Tối ưu hóa - Thời gian chạy**

**TỐI ƯU HÓA**

**2. TỐI ƯU HÓA THỜI GIAN CHẠY**
*   Tối ưu hóa thời gian chạy đề cập đến các kỹ thuật và thực tiễn giúp chương trình của bạn hoạt động hiệu quả hơn trong khi nó đang chạy — ngay cả sau khi biên dịch.
*   Không giống như tối ưu hóa thời gian biên dịch, tối ưu hóa thời gian chạy là về việc viết mã thông minh hơn để đưa ra quyết định và điều chỉnh hành vi trong quá trình thực thi chương trình.

---

### **Slide 39: Thực hành**

**THỰC HÀNH**

1.  **Viết một chương trình để tạo một máy tính cơ bản bằng cách sử dụng “Switch - Case”:**
    *   Nhập 2 số
    *   Nhập toán tử
    *   In kết quả
    *   **Ví dụ đầu ra:**
        ```
        Nhập toán tử (+, -, *, /): -
        Nhập hai toán hạng: 9 8
        9.00 - 8.00 = 1.00
        ```

2.  **Viết một chương trình để kiểm tra xem một năm có phải là năm nhuận không bằng cách sử dụng "if - lồng nhau"**
    *   **Ví dụ đầu ra:**
        ```
        Nhập một năm: 2024
        Năm nhuận
        ```

3.  **Viết một chương trình để mô phỏng một giao diện ATM đơn giản bằng cách sử dụng “switch - case”**
    *   **Ví dụ đầu ra:**
        ```
        1. Kiểm tra số dư
        2. Rút tiền
        3. Gửi tiền
        4. Thoát
        Nhập lựa chọn của bạn: 1
        Số dư của bạn là $5000
        ```

---

### **Slide 40: Tóm tắt**

**TÓM TẮT**

*   **Các Câu lệnh Điều kiện trong C**
    *   Học cách sử dụng `if`, `if-else`, `if` lồng nhau, `switch`, và toán tử ba ngôi để ra quyết định.
    *   Hiểu luồng điều khiển và cách C xử lý các điều kiện.
*   **Tạo mã được AI Hỗ trợ**
    *   Sử dụng các công cụ như ChatGPT và Replit để tạo và giải thích các chương trình C.
    *   Học cách viết lời nhắc và tinh chỉnh mã do AI tạo ra.
*   **Gỡ lỗi & Tối ưu hóa**
    *   Xác định và sửa lỗi bằng `printf()` và các công cụ như `gdb`.
    *   Cải thiện hiệu suất mã với tối ưu hóa thời gian biên dịch và thời gian chạy.
*   **Thực hành**
    *   Áp dụng các khái niệm với các chương trình C thực tế (kiểm tra năm nhuận, máy tính, ATM, v.v.)

---

### **Slide 41: Cảm ơn**

**CRANES**
**CẢM ƠN BẠN**
