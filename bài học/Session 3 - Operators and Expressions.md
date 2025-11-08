# Session 3 - Operators and Expressions

### **Slide 1: Trang bìa**

**Cranes Varsity**
'Nơi Công Nghệ Hội Tụ Cùng Sự Ưu Việt'

**Chương trình:**
Chương trình Phát triển Phần mềm Ô tô

**Học kỳ 1:**
Chứng chỉ Phát triển Phần mềm Ô tô (CAS)

**Học phần:**
Lập trình C/C++ cho Hệ thống Nhúng AI

**Buổi 03:**
Toán tử và Biểu thức

---

### **Slide 2: Mục tiêu Buổi học**

**MỤC TIÊU BUỔI HỌC**

**Mục tiêu của buổi học là**

| Vai trò của Toán tử | Các loại Toán tử | Độ ưu tiên và Tính kết hợp | Thực hành |
| :--- | :--- | :--- | :--- |
| Để hiểu vai trò và tầm quan trọng của các toán tử trong lập trình C. | Để học cách sử dụng hiệu quả các loại toán tử khác nhau (số học, logic, quan hệ, v.v.). | Để khám phá độ ưu tiên và tính kết hợp của toán tử để đánh giá các biểu thức một cách chính xác. | Để phát triển kỹ năng thực hành thông qua các ví dụ và bài tập. |

---

### **Slide 3: Toán tử**

**TOÁN TỬ**

*   Toán tử là một ký hiệu giúp người dùng ra lệnh cho máy tính thực hiện các thao tác toán học hoặc logic nhất định.
*   Toán tử được sử dụng để hoạt động trên dữ liệu và biến.
*   Có năm toán tử chính được thảo luận:

---

### **Slide 4: Các loại Toán tử**

**CÁC LOẠI TOÁN TỬ**

| CÁC LOẠI TOÁN TỬ | KÝ HIỆU |
| :--- | :--- |
| TOÁN TỬ SỐ HỌC | `(+, -, *, /, %)` |
| TOÁN TỬ QUAN HỆ | `(>, <, >=, <=, ==, !=)` |
| TOÁN TỬ LOGIC | `(&&, ||, !)` |
| TOÁN TỬ THAO TÁC BIT | `(&, |, ^, <<, >>, ~)` |
| TOÁN TỬ GÁN | `(=, +=, -=, *=, /=, %=)` |

---

### **Slide 5: Toán tử Số học**

**TOÁN TỬ SỐ HỌC**

**1. TOÁN TỬ SỐ HỌC**
*   Toán tử số học trong C được sử dụng để thực hiện các phép toán cơ bản trên các giá trị số.
*   Chúng hoạt động trên cả kiểu dữ liệu số nguyên và số thực.

| TOÁN TỬ | PHÉP TOÁN | MÔ TẢ |
| :--- | :--- | :--- |
| **+** | Phép cộng | Cộng giá trị của hai toán hạng. |
| **-** | Phép trừ | Trừ hai giá trị của hai toán hạng. |
| **\*** | Phép nhân | Nhân toán hạng 1 với toán hạng 2. |
| **/** | Phép chia | Chia toán hạng 1 cho toán hạng 2 và trả về thương số. |
| **%** | Phép chia lấy dư | Chia toán hạng 1 cho toán hạng 2 và trả về số dư. |

*   Toán tử chia lấy dư đánh giá phần còn lại của các toán hạng.
*   Toán tử % chỉ có thể được áp dụng cho kiểu số nguyên.
*   Phép chia số nguyên sẽ cắt bỏ bất kỳ phần thập phân nào.

---

### **Slide 6: Ví dụ về Toán tử Số học**

**TOÁN TỬ SỐ HỌC**

**CHƯƠNG TRÌNH C MINH HỌA VIỆC SỬ DỤNG CÁC TOÁN TỬ SỐ HỌC**

```c
#include <stdio.h>
int main() {
    int num1 = 12, num2 = 3;
    printf("Các số: %d và %d\n", num1, num2);
    printf("Phép cộng: %d\n", num1 + num2);
    printf("Phép trừ: %d\n", num1 - num2);
    printf("Phép nhân: %d\n", num1 * num2);
    printf("Phép chia: %d\n", num1 / num2);
    printf("Phép chia lấy dư: %d\n", num1 % num2);
    return 0;
}
```

**KẾT QUẢ:**
```
Các số: 12 và 3
Phép cộng: 15
Phép trừ: 9
Phép nhân: 36
Phép chia: 4
Phép chia lấy dư: 0
```

---

### **Slide 7: Toán tử Quan hệ**

**TOÁN TỬ QUAN HỆ**

*   Chúng còn được gọi là toán tử so sánh.
*   Được sử dụng để kiểm tra mối quan hệ giữa hai toán hạng.
*   Trả về giá trị 1 (đúng) hoặc 0 (sai) tùy thuộc vào việc mối quan hệ được kiểm tra là đúng hay sai.

| TOÁN TỬ | PHÉP TOÁN | MÔ TẢ (toán hạng 1 là a và toán hạng 2 là b) |
| :--- | :--- | :--- |
| **<** | Nhỏ hơn | Trả về 1 nếu a nhỏ hơn b, ngược lại là 0. |
| **<=** | Nhỏ hơn hoặc bằng | Trả về 1 nếu a nhỏ hơn hoặc bằng b, ngược lại là 0. |
| **>** | Lớn hơn | Trả về 1 nếu a lớn hơn b, ngược lại là 0. |
| **>=** | Lớn hơn hoặc bằng | Trả về 1 nếu a lớn hơn hoặc bằng b, ngược lại là 0. |
| **==** | Bằng | Trả về 1 nếu a bằng b (giống hệt), ngược lại là 0. |
| **!=** | Không bằng | Trả về 1 nếu a không bằng b (không giống hệt), ngược lại là 0. |

---

### **Slide 8: Ví dụ về Toán tử Quan hệ**

**TOÁN TỬ QUAN HỆ**

**CHƯƠNG TRÌNH C MINH HỌA VIỆC SỬ DỤNG CÁC TOÁN TỬ QUAN HỆ**
```c
#include <stdio.h>
int main() {
    int num1 = 12, num2 = 3;
    printf("nhỏ hơn: %d\n", num1<num2);
    printf("nhỏ hơn hoặc bằng: %d\n", num1<=num2);
    printf("lớn hơn: %d\n", num1>num2);
    printf("lớn hơn hoặc bằng: %d\n", num1>=num2);
    printf("Bằng: %d\n", num1==num2);
    printf("không bằng: %d\n", num1 != num2);
    return 0;
}
```
**KẾT QUẢ**
```
nhỏ hơn: 0
nhỏ hơn hoặc bằng: 0
lớn hơn: 1
lớn hơn hoặc bằng: 1
Bằng: 0
không bằng: 1
```

---

### **Slide 9: Toán tử Logic**

**TOÁN TỬ LOGIC**

**3. TOÁN TỬ LOGIC**
Toán tử logic trong C là các toán tử được sử dụng để kết hợp hai hoặc nhiều điều kiện (biểu thức Boolean) và trả về một kết quả dựa trên đánh giá logic của chúng.

C cung cấp 3 toán tử logic:
A. Toán tử AND logic (`&&`)
B. Toán tử OR logic (`||`)
C. Toán tử NOT logic (`!`)

---

### **Slide 10: Toán tử AND Logic (&&)**

**TOÁN TỬ LOGIC**

**A). TOÁN TỬ AND LOGIC (&&)**
*   Toán tử AND logic (`&&`) trong C là một toán tử nhị phân được sử dụng để đánh giá hai điều kiện. Nó trả về `true` (1) nếu cả hai điều kiện đều đúng; ngược lại, nó trả về `false` (0).
*   Toán tử `&&` đánh giá điều kiện đầu tiên.
*   Nếu điều kiện đầu tiên là `false` (0), điều kiện thứ hai không được đánh giá (đánh giá đoản mạch).
*   Nếu điều kiện đầu tiên là `true` (khác không), thì điều kiện thứ hai sẽ được đánh giá.

**BẢNG:**
| ĐK 1 | ĐK 2 | ĐK 1 && ĐK 2 |
| :--- | :--- | :--- |
| Đúng | Đúng | Đúng |
| Đúng | Sai | Sai |
| Sai | Đúng | Sai |
| Sai | Sai | Sai |

---

### **Slide 11: Toán tử OR Logic (||)**

**TOÁN TỬ LOGIC**

**B). TOÁN TỬ OR LOGIC (||):**
*   Toán tử OR logic (`||`) trong C là một toán tử nhị phân được sử dụng để đánh giá hai điều kiện.
*   Nó trả về `true` (1) nếu ít nhất một trong các điều kiện là đúng; ngược lại, nó trả về `false` (0).
*   Nó thường được sử dụng trong các câu lệnh ra quyết định như `if`, `while`, và `for`.
*   Toán tử `||` đánh giá điều kiện đầu tiên.
    *   Nếu điều kiện đầu tiên là `true` (khác không), điều kiện thứ hai không được đánh giá (đánh giá đoản mạch).
    *   Nếu điều kiện đầu tiên là `false` (0), thì điều kiện thứ hai sẽ được đánh giá.

**BẢNG:**
| ĐK 1 | ĐK 2 | ĐK 1 \|\| ĐK 2 |
| :--- | :--- | :--- |
| Đúng | Đúng | Đúng |
| Đúng | Sai | Đúng |
| Sai | Đúng | Đúng |
| Sai | Sai | Sai |

---

### **Slide 12: Toán tử NOT Logic (!)**

**TOÁN TỬ LOGIC**

**C). TOÁN TỬ NOT LOGIC (!):**
*   Toán tử NOT logic (`!`) trong C là một toán tử một ngôi phủ định giá trị của một điều kiện.
*   Nếu điều kiện là `true` (khác không), `!` chuyển nó thành `false` (0).
*   Nếu điều kiện là `false` (0), `!` chuyển nó thành `true` (1).

**BẢNG:**
| ĐK 1 | ! ĐK 1 |
| :--- | :--- |
| Đúng | Sai |
| Sai | Đúng |

---

### **Slide 13: Ví dụ về Toán tử Logic**

**TOÁN TỬ LOGIC**

**CHƯƠNG TRÌNH C MINH HỌA VIỆC SỬ DỤNG CÁC TOÁN TỬ LOGIC**
```c
#include <stdio.h>
int main() {
    int a = 10, b = 20, c = 0;
    int and_result = (a < b) && (b > c);
    printf("Kết quả của AND Logic (&&): %d\n", and_result);
    int or_result = (a > b) || (c == 0);
    printf("Kết quả của OR Logic (||): %d\n", or_result);
    int not_result = !c;
    printf("Kết quả của NOT Logic (!): %d\n", not_result);
    return 0;
}
```
**KẾT QUẢ:**
```
Kết quả của AND Logic (&&): 1
Kết quả của OR Logic (||): 1
Kết quả của NOT Logic (!): 1
```

---

### **Slide 14: Toán tử Thao tác Bit**

**TOÁN TỬ THAO TÁC BIT**

**4. TOÁN TỬ THAO TÁC BIT**
*   Toán tử thao tác bit trong C hoạt động ở cấp độ bit, nghĩa là chúng thao tác các bit riêng lẻ của một biến.
*   Các toán tử thao tác bit cho phép bạn thao tác các bit riêng lẻ.
*   Chúng ta có thể kiểm tra, xóa, đặt hoặc đảo ngược bất kỳ bit hoặc nhóm bit nào.
*   Chúng ta cũng có thể dịch chuyển mẫu bit của một số nguyên sang trái hoặc phải.
*   Chỉ có thể áp dụng cho các toán hạng nguyên.
*   C cung cấp sáu toán tử để thao tác bit.

---

### **Slide 15: Bảng Toán tử Thao tác Bit**

**BẢNG CÁC TOÁN TỬ THAO TÁC BIT**

| | | |
| :--- | :--- | :--- |
| **&** | **AND thao tác bit** | So sánh mỗi bit của toán hạng đầu tiên với bit tương ứng của toán hạng thứ hai. Nếu cả hai bit đều là 1, bit kết quả tương ứng được đặt thành 1. Ngược lại, bit kết quả tương ứng được đặt thành 0. |
| **\|** | **OR thao tác bit** | So sánh mỗi bit của toán hạng đầu tiên với bit tương ứng của toán hạng thứ hai. Nếu một trong hai bit là 1, bit kết quả tương ứng được đặt thành 1. Ngược lại, bit kết quả tương ứng được đặt thành 0. |
| **^** | **XOR thao tác bit** | So sánh mỗi bit của toán hạng đầu tiên với bit tương ứng của toán hạng thứ hai. Nếu một bit là 0 và bit kia là 1, bit kết quả tương ứng được đặt thành 1. Ngược lại, bit kết quả tương ứng được đặt thành 0. |
| **~** | **Phần bù (Complement)** | Đảo mọi bit. |
| **>>** | **Dịch phải (Right Shift)**| Dịch phải toán hạng bên trái của chúng theo số vị trí bit được cho bởi toán hạng bên phải. |
| **<<** | **Dịch trái (Left Shift)** | Dịch trái toán hạng bên trái của chúng theo số vị trí bit được cho bởi toán hạng bên phải. |

---

### **Slide 16: Phép tính Dịch chuyển Bit**

**TOÁN TỬ THAO TÁC BIT**

**1. TÍNH TOÁN: DỊCH TRÁI THAO TÁC BIT (<<)**
*   `expr1 << expr2` tương đương với phép nhân với `2^expr2`.

**2. TÍNH TOÁN: DỊCH PHẢI THAO TÁC BIT (>>):**
*   `expr1 >> expr2` tương đương với phép chia cho `2^expr2`.

Kết quả của một phép dịch chuyển là không xác định nếu toán hạng thứ hai là số âm, hoặc nếu toán hạng bên phải lớn hơn hoặc bằng chiều rộng tính bằng bit của toán hạng bên trái.

---

### **Slide 17: Ví dụ về Toán tử Thao tác Bit**

**TOÁN TỬ THAO TÁC BIT**

**CHƯƠNG TRÌNH C MINH HỌA VIỆC SỬ DỤNG TOÁN TỬ THAO TÁC BIT**
```c
#include <stdio.h>
int main() {
    int a = 5, b = 3;
    printf("a = %d, b = %d\n", a, b);
    printf("AND Thao tác bit (a & b) = %d\n", a & b);
    printf("OR Thao tác bit (a | b)  = %d\n", a | b);
    printf("XOR Thao tác bit (a ^ b) = %d\n", a ^ b);
    printf("NOT Thao tác bit (~a)   = %d\n", ~a);
    printf("Dịch Trái (a << 1)      = %d\n", a << 1);
    printf("Dịch Phải (a >> 1)      = %d\n", a >> 1);
    return 0;
}
```
**KẾT QUẢ:**
```
a = 5, b = 3
AND Thao tác bit (a & b) = 1
OR Thao tác bit (a | b)  = 7
XOR Thao tác bit (a ^ b) = 6
NOT Thao tác bit (~a)   = -6
Dịch Trái (a << 1)      = 10
Dịch Phải (a >> 1)      = 2
```

---

### **Slide 18: Toán tử Gán**

**TOÁN TỬ GÁN**

**5. TOÁN TỬ GÁN**
*   Toán tử Gán được sử dụng để gán giá trị cho các biến.
*   Toán tử gán cơ bản là `=` (dấu bằng), nhưng C cũng cung cấp các toán tử gán phức hợp thực hiện một phép toán và gán kết quả trong một bước duy nhất.
*   Toán tử gán là dấu bằng đơn (`=`). Toán tử gán sao chép giá trị từ phía bên phải của nó vào biến ở phía bên trái.

**Ví dụ:**
`x = a + b`
*   Ở đây giá trị của `a + b` được đánh giá và thay thế vào biến x.
*   Ngoài ra, C có một tập hợp các toán tử gán viết tắt của dạng:
`var oper= exp;`
*   Toán tử `oper=` được gọi là toán tử gán viết tắt.

---

### **Slide 19: Các Toán tử Gán Viết tắt**

**TOÁN TỬ GÁN**

| Toán tử Gán | Phép toán Viết tắt |
| :--- | :--- |
| `a = a+b` | `a += b` |
| `a = a-b` | `a -= b` |
| `a = a*b` | `a *= b` |
| `a = a/b` | `a /= b` |
| `a = a%b` | `a %= b` |

---

### **Slide 20: Ví dụ về Toán tử Gán**

**TOÁN TỬ GÁN**

**CHƯƠNG TRÌNH C MINH HỌA VIỆC SỬ DỤNG CÁC TOÁN TỬ GÁN**
```c
#include <stdio.h>
int main() {
    int a = 10;
    printf("a ban đầu = %d\n", a);
    printf("a += 5   ->  %d\n", a += 5);
    printf("a -= 3   ->  %d\n", a -= 3);
    printf("a *= 2   ->  %d\n", a *= 2);
    printf("a /= 4   ->  %d\n", a /= 4);
    printf("a %%= 3   ->  %d\n", a %= 3);
    return 0;
}
```
**KẾT QUẢ**
```
a ban đầu = 10
a += 5   ->  15
a -= 3   ->  12
a *= 2   ->  24
a /= 4   ->  6
a %= 3   ->  0
```

---

### **Slide 21: Độ ưu tiên và Tính kết hợp của Toán tử**

**ĐỘ ƯU TIÊN VÀ TÍNH KẾT HỢP CỦA TOÁN TỬ**

| Loại | Toán tử | Tính kết hợp |
| :--- | :--- | :--- |
| Hậu tố (Postfix) | `() [] -> . ++ --` | Trái sang phải |
| Một ngôi (Unary) | `+ - ! ~ ++ -- (type)* & sizeof` | Phải sang trái |
| Nhân (Multiplicative) | `* / %` | Trái sang phải |
| Cộng (Additive) | `+ -` | Trái sang phải |
| Dịch chuyển (Shift) | `<< >>` | Trái sang phải |
| Quan hệ (Relational) | `< <= > >=` | Trái sang phải |
| Bằng (Equality) | `== !=` | Trái sang phải |
| AND Thao tác bit | `&` | Trái sang phải |
| XOR Thao tác bit | `^` | Trái sang phải |
| OR Thao tác bit | `|` | Trái sang phải |
| AND Logic | `&&` | Trái sang phải |
| OR Logic | `||` | Trái sang phải |
| Điều kiện (Conditional) | `?:` | Phải sang trái |
| Gán (Assignment) | `= += -= *= /= %= >>= <<= &= ^= |=` | Phải sang trái |
| Phẩy (Comma) | `,` | Trái sang phải |

---

### **Slide 22: Giải thích về Độ ưu tiên và Tính kết hợp**

**ĐỘ ƯU TIÊN VÀ TÍNH KẾT HỢP CỦA TOÁN TỬ**

*   Độ ưu tiên và tính kết hợp của các toán tử C ảnh hưởng đến việc nhóm và đánh giá các toán hạng trong biểu thức.
*   Độ ưu tiên cũng có thể được mô tả bằng từ "ràng buộc".
*   Các toán tử có độ ưu tiên cao hơn được cho là có sự ràng buộc chặt chẽ hơn.
*   Các toán tử có độ ưu tiên cao hơn được đánh giá trước những toán tử có độ ưu tiên thấp hơn.
*   Nếu một số toán tử có độ ưu tiên bằng nhau, chúng được ràng buộc theo tính kết hợp của chúng.
*   C, giống như hầu hết các ngôn ngữ, không chỉ định thứ tự mà các toán hạng của một toán tử được đánh giá. (Các ngoại lệ là `&&`, `||`, `?:`, và `,`.)

---

### **Slide 23: Ví dụ về Độ ưu tiên và Tính kết hợp**

**ĐỘ ƯU TIÊN VÀ TÍNH KẾT HỢP CỦA TOÁN TỬ (tiếp)**

**CHƯƠNG TRÌNH 1:**
```c
#include <stdio.h>
int main() {
    int a = 10, b = 5, c = 2, result;
    result = a + b * c;
    printf("Kết quả của a + b * c = %d\n", result);
    return 0;
}
```
Phép nhân (`*`) có độ ưu tiên cao hơn phép cộng (`+`). `b * c` được đánh giá trước: `5 * 2 = 10`. Sau đó, phép cộng xảy ra: `10 + 10 = 20`.

**CHƯƠNG TRÌNH 2:**
```c
#include <stdio.h>
int main() {
    int a = 10, b = 5, c = 2, result;
    result = a - b - c;
    printf("Kết quả của a - b - c = %d\n", result);
    return 0;
}
```
Phép trừ (`-`) có tính kết hợp từ trái sang phải, nghĩa là các phép toán được đánh giá từ trái sang phải. `(10 - 5) - 2` được đánh giá là: `10 - 5 = 5`, sau đó `5 - 2 = 3`.

---

### **Slide 24: Tóm tắt**

**TÓM TẮT**

**1. Giới thiệu về Toán tử & Biểu thức** – Các toán tử được định nghĩa và vai trò của chúng trong lập trình C.

**2. Các loại Toán tử đã học:**
*   Toán tử Số học (`+, -, *, /, %`)
*   Toán tử Quan hệ (`>, <, >=, <=, ==, !=`)
*   Toán tử Logic (`&&, ||, !`)
*   Toán tử Thao tác Bit (`&, |, ^, <<, >>, ~`)
*   Toán tử Gán (`=, +=, -=, *=, /=, %=`)

**3. Độ ưu tiên & Tính kết hợp của Toán tử** – Giải thích thứ tự thực thi của các toán tử.

**4. Triển khai Thực tế:** Các chương trình minh họa các toán tử mà không sử dụng các câu lệnh điều khiển.

**5. Thực hành với các tính toán thực tế** (ví dụ: diện tích, hoán đổi, các phép toán bitwise).

**6. Tối ưu hóa Biểu thức** – Hiểu cách đánh giá hiệu quả các biểu thức.

**7. Phiên hỏi đáp & Trắc nghiệm** – Củng cố kiến thức học được thông qua các câu hỏi dựa trên khái niệm.

---

### **Slide 25: Cảm ơn**

**CẢM ƠN**
