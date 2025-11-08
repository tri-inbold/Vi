#Session 9 - Functions and AI Code Generation

### **Slide 1**

**English:**

**Program:**
Automotive Software Development program

**Semester1:**
Certificate in Automotive Software Development (CAS)

**Module:**
C/C++ Programming for AI Embedded Systems

**Session 09:**
Functions And AI Code Generation

---

**Tiếng Việt:**

**Chương trình:**
Chương trình Phát triển Phần mềm Ô tô

**Học kỳ 1:**
Chứng chỉ Phát triển Phần mềm Ô tô (CAS)

**Học phần:**
Lập trình C/C++ cho Hệ thống Nhúng AI

**Buổi 09:**
Hàm và Sinh mã bằng AI

***

### **Slide 2**

**English:**

**SESSION OBJECTIVES AND TOPICS**

*   **Introduction to Functions:** To Understand the purpose, structure, and advantages of using functions in C programming.
*   **Defining and Using functions:** To Learn to define, declare, and call functions with parameter passing (by value/reference).
*   **Function Types and in C AI Code Generation for Functions:** To explore function types, scope, storage classes, and recursion using factorial and Fibonacci, To utilize AI for generating function-based code.
*   **Hands-on practice Q&A**

---

**Tiếng Việt:**

**MỤC TIÊU VÀ CHỦ ĐỀ BUỔI HỌC**

*   **Giới thiệu về Hàm:** Để hiểu mục đích, cấu trúc và lợi ích của việc sử dụng hàm trong lập trình C.
*   **Định nghĩa và Sử dụng hàm:** Học cách định nghĩa, khai báo và gọi hàm với việc truyền tham số (theo giá trị/tham chiếu).
*   **Các loại hàm trong C và Sinh mã AI cho Hàm:** Khám phá các loại hàm, phạm vi, lớp lưu trữ và đệ quy bằng cách sử dụng giai thừa và Fibonacci, Tận dụng AI để tạo mã dựa trên hàm.
*   **Thực hành và Hỏi đáp**

***

### **Slide 3**

**English:**

**INTRODUCTION TO FUNCTIONS**

**What is Function?**
*   A function in C is a self-contained block of code designed to perform a specific task.
*   Functions allow programmers to divide a large program into smaller, modular, and manageable sections.
*   In simple terms, a function is like a mini-program within a program that can be defined once and used (called) multiple times.

---

**Tiếng Việt:**

**GIỚI THIỆU VỀ HÀM**

**Hàm là gì?**
*   Hàm trong C là một khối mã độc lập được thiết kế để thực hiện một tác vụ cụ thể.
*   Hàm cho phép lập trình viên chia một chương trình lớn thành các phần nhỏ hơn, có tính mô-đun và dễ quản lý.
*   Nói một cách đơn giản, hàm giống như một chương trình con bên trong một chương trình lớn, có thể được định nghĩa một lần và sử dụng (gọi) nhiều lần.

***

### **Slide 4**

**English:**

**INTRODUCTION TO FUNCTIONS (cont..)**

**Why We Need Functions in C?**
Functions provide several key benefits in programming:
*   **Modularity:** Breaks down complex problems into smaller, manageable parts.
*   **Code Reusability:** Once a function is written, it can be used multiple times without rewriting the same logic.
*   **Improved Readability:** Code becomes easier to read, understand, and maintain.

---

**Tiếng Việt:**

**GIỚI THIỆU VỀ HÀM (tiếp theo..)**

**Tại sao chúng ta cần Hàm trong C?**
Hàm mang lại một số lợi ích chính trong lập trình:
*   **Tính mô-đun:** Chia các vấn đề phức tạp thành các phần nhỏ hơn, dễ quản lý.
*   **Khả năng tái sử dụng mã:** Một khi hàm được viết, nó có thể được sử dụng nhiều lần mà không cần viết lại logic tương tự.
*   **Cải thiện khả năng đọc:** Mã nguồn trở nên dễ đọc, dễ hiểu và dễ bảo trì hơn.

***

### **Slide 5**

**English:**

**INTRODUCTION TO FUNCTIONS (cont..)**

**SYNTAX:**
1.  Function Declaration
2.  Function Definition
3.  Function Calls

---

**Tiếng Việt:**

**GIỚI THIỆU VỀ HÀM (tiếp theo..)**

**CÚ PHÁP:**
1.  Khai báo hàm
2.  Định nghĩa hàm
3.  Gọi hàm

***

### **Slide 6**

**English:**

**INTRODUCTION TO FUNCTIONS**

**1. FUNCTION DECLARATION / FUNCTION PROTOTYPE**
*   In a function declaration, we must provide the function name, its return type, and the number and type of its parameters.
*   A function declaration tells the compiler that there is a function with the given name defined somewhere else in the program.
**SYNTAX:**
`return_type name_of_the_function (parameter_1, parameter_2);`

---

**Tiếng Việt:**

**GIỚI THIỆU VỀ HÀM**

**1. KHAI BÁO HÀM / NGUYÊN MẪU HÀM (FUNCTION PROTOTYPE)**
*   Trong một khai báo hàm, chúng ta phải cung cấp tên hàm, kiểu trả về, số lượng và kiểu của các tham số của nó.
*   Khai báo hàm cho trình biên dịch biết rằng có một hàm với tên đã cho được định nghĩa ở một nơi nào đó khác trong chương trình.
**CÚ PHÁP:**
`kiểu_trả_về tên_hàm (tham_số_1, tham_số_2);`

***

### **Slide 7**

**English:**

**INTRODUCTION TO FUNCTIONS**

[Image shows an example of a function declaration `int sum(int a, int b);` with arrows pointing to `return type`, `Function Name`, `Parameter Type`, `Parameter Name`, and `Ending Statement Semicolon`.]

*   A function in C must always be declared globally before calling it.
*   The parameter name is not mandatory while declaring functions.
*   We can also declare the function without using the name of the data variables.

---

**Tiếng Việt:**

**GIỚI THIỆU VỀ HÀM**

[Hình ảnh minh họa một khai báo hàm `int sum(int a, int b);` với các mũi tên chỉ vào `kiểu trả về`, `Tên hàm`, `Kiểu tham số`, `Tên tham số`, và `Dấu chấm phẩy kết thúc`.]

*   Một hàm trong C luôn phải được khai báo toàn cục trước khi gọi nó.
*   Tên tham số không bắt buộc khi khai báo hàm.
*   Chúng ta cũng có thể khai báo hàm mà không cần sử dụng tên của các biến dữ liệu.

***

### **Slide 8**

**English:**

**DEFINING AND USING FUNCTIONS**

**2. FUNCTION DEFINITION**
*   The function definition consists of actual statements which are executed when the function is called (i.e. when the program control comes to the function).
*   A C function is generally defined and declared in a single step because the function definition always starts with the function declaration so we do not need to declare it explicitly.

---

**Tiếng Việt:**

**ĐỊNH NGHĨA VÀ SỬ DỤNG HÀM**

**2. ĐỊNH NGHĨA HÀM**
*   Định nghĩa hàm bao gồm các câu lệnh thực tế được thực thi khi hàm được gọi (tức là khi quyền điều khiển chương trình chuyển đến hàm).
*   Một hàm C thường được định nghĩa và khai báo trong một bước duy nhất vì định nghĩa hàm luôn bắt đầu bằng khai báo hàm, do đó chúng ta không cần phải khai báo nó một cách tường minh.

***

### **Slide 9**

**English:**

**DEFINING AND USING FUNCTIONS (cont..)**

The below example serves as both a function definition and a declaration.

```c
return_type function_name (para1_type para1_name, para2_type para2_name)
{
    // body of the function
}
```

---

**Tiếng Việt:**

**ĐỊNH NGHĨA VÀ SỬ DỤNG HÀM (tiếp theo..)**

Ví dụ dưới đây vừa là định nghĩa hàm vừa là khai báo.

```c
kiểu_trả_về tên_hàm (kiểu_tham_số_1 tên_tham_số_1, kiểu_tham_số_2 tên_tham_số_2)
{
    // thân hàm
}
```

***

### **Slide 10**

**English:**

**DEFINING AND USING FUNCTIONS (cont..)**

**3. FUNCTION CALL**
*   A function call is a statement that instructs the compiler to execute the function.
*   We use the function name and parameters in the function call.

---

**Tiếng Việt:**

**ĐỊNH NGHĨA VÀ SỬ DỤNG HÀM (tiếp theo..)**

**3. GỌI HÀM**
*   Một lời gọi hàm là một câu lệnh chỉ thị cho trình biên dịch thực thi hàm đó.
*   Chúng ta sử dụng tên hàm và các tham số trong lời gọi hàm.

***

### **Slide 11**

**English:**

**DEFINING AND USING FUNCTIONS (cont..)**

*   In the example, the first sum function is called and 10, 30 are passed to the sum function.
*   After the function call sum of a and b is returned and control is also returned back to the main function of the program.

[Image shows a C code example with `int sum(int a, int b)` as "Function Definition" and `int add = sum(10, 30);` as "Function Calling".]

---

**Tiếng Việt:**

**ĐỊNH NGHĨA VÀ SỬ DỤNG HÀM (tiếp theo..)**

*   Trong ví dụ, hàm `sum` đầu tiên được gọi và các giá trị 10, 30 được truyền cho hàm `sum`.
*   Sau khi gọi hàm, tổng của a và b được trả về và quyền điều khiển cũng được trả lại cho hàm `main` của chương trình.

[Hình ảnh minh họa một ví dụ mã C với `int sum(int a, int b)` là "Định nghĩa hàm" và `int add = sum(10, 30);` là "Gọi hàm".]

***

### **Slide 12**

**English:**

**DEFINING AND USING FUNCTIONS (cont..)**

**Function Return Type:**
*   Function return type tells what type of value is returned after all function is executed.
*   When we don't want to return a value, we can use the `void` data type.

`int function(parameter_1, parameter_2);`

---

**Tiếng Việt:**

**ĐỊNH NGHĨA VÀ SỬ DỤNG HÀM (tiếp theo..)**

**Kiểu trả về của hàm:**
*   Kiểu trả về của hàm cho biết loại giá trị nào được trả về sau khi hàm được thực thi xong.
*   Khi chúng ta không muốn trả về một giá trị, chúng ta có thể sử dụng kiểu dữ liệu `void`.

`int function(tham_số_1, tham_số_2);`

***

### **Slide 13**

**English:**

**DEFINING AND USING FUNCTIONS (cont..)**

**Function Arguments:**
*   Function Arguments (also known as Function Parameters) are the data that is passed to a function.
*   Functions can be called either with or without arguments and might return values. They may or might not return values to the calling functions.
    *   Function with no arguments and no return value
    *   Function with no arguments and with return value
    *   Function with argument and with no return value
    *   Function with arguments and with return value

---

**Tiếng Việt:**

**ĐỊNH NGHĨA VÀ SỬ DỤNG HÀM (tiếp theo..)**

**Đối số của hàm:**
*   Đối số của hàm (còn được gọi là Tham số của hàm) là dữ liệu được truyền cho một hàm.
*   Hàm có thể được gọi có hoặc không có đối số và có thể trả về giá trị. Chúng có thể hoặc không thể trả về giá trị cho các hàm gọi chúng.
    *   Hàm không có đối số và không có giá trị trả về
    *   Hàm không có đối số và có giá trị trả về
    *   Hàm có đối số và không có giá trị trả về
    *   Hàm có đối số và có giá trị trả về

***

### **Slide 14**

**English:**

**DEFINING AND USING FUNCTIONS (cont..)**

**1.C PROGRAM FOR DEMONSTRATING USAGE OF FUNCTIONS**
```c
#include <stdio.h>
int getNumber()
{
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    return num;
}
int main() {
    int x = getNumber();
    printf("You entered: %d\n", x);
    return 0;
}
```
**OUTPUT:**
Enter a number: 5
You entered: 5

---

**Tiếng Việt:**

**ĐỊNH NGHĨA VÀ SỬ DỤNG HÀM (tiếp theo..)**

**1. CHƯƠNG TRÌNH C MINH HỌA VIỆC SỬ DỤNG HÀM**
```c
#include <stdio.h>
int getNumber()
{
    int num;
    printf("Nhập một số: ");
    scanf("%d", &num);
    return num;
}
int main() {
    int x = getNumber();
    printf("Bạn đã nhập: %d\n", x);
    return 0;
}
```
**KẾT QUẢ:**
Nhập một số: 5
Bạn đã nhập: 5

***

### **Slide 15**

**English:**

**DEFINING AND USING FUNCTIONS (cont..)**

**Passing Parameters to Function**
*   The data passed when the function is being invoked is known as the **Actual parameters**.
*   **Formal Parameters** are the variable and the data type as mentioned in the function declaration.

---

**Tiếng Việt:**

**ĐỊNH NGHĨA VÀ SỬ DỤNG HÀM (tiếp theo..)**

**Truyền tham số cho hàm**
*   Dữ liệu được truyền khi hàm được gọi được gọi là **tham số thực tế (Đối số)**.
*   **Tham số hình thức** là biến và kiểu dữ liệu được đề cập trong khai báo hàm.

***

### **Slide 16**

**English:**

**DEFINING AND USING FUNCTIONS (cont..)**

1.  In the program, 10 and 30 are known as **actual parameters**.
2.  In the program, a and b are known as **formal parameters**.

[Image shows C code with `(int a, int b)` highlighted as "Formal Parameter" and `(10, 30)` highlighted as "Actual Parameter".]

---

**Tiếng Việt:**

**ĐỊNH NGHĨA VÀ SỬ DỤNG HÀM (tiếp theo..)**

1.  Trong chương trình, 10 và 30 được gọi là **tham số thực tế**.
2.  Trong chương trình, a và b được gọi là **tham số hình thức**.

[Hình ảnh minh họa mã C với `(int a, int b)` được tô sáng là "Tham số hình thức" và `(10, 30)` được tô sáng là "Tham số thực tế".]

***

### **Slide 17**

**English:**

**DEFINING AND USING FUNCTIONS (cont..)**

We can pass arguments to the C function in two ways:
1.  Pass by Value
2.  Pass by Reference

**1. PASS BY VALUE**
*   In Pass by Value, when you call a function and pass a variable, a copy of the actual value is passed to the function.
*   The original variable in the calling function remains unchanged.
*   Any changes made inside the called function affect only the copy, not the original.

---

**Tiếng Việt:**

**ĐỊNH NGHĨA VÀ SỬ DỤNG HÀM (tiếp theo..)**

Chúng ta có thể truyền đối số cho hàm C theo hai cách:
1.  Truyền bằng giá trị (Pass by Value)
2.  Truyền bằng tham chiếu (Pass by Reference)

**1. TRUYỀN BẰNG GIÁ TRỊ**
*   Trong Truyền bằng giá trị, khi bạn gọi một hàm và truyền một biến, một bản sao của giá trị thực tế sẽ được truyền cho hàm.
*   Biến gốc trong hàm gọi vẫn không thay đổi.
*   Mọi thay đổi được thực hiện bên trong hàm được gọi chỉ ảnh hưởng đến bản sao, không ảnh hưởng đến bản gốc.

***

### **Slide 18**

**English:**

**DEFINING AND USING FUNCTIONS (cont..)**

**2.C PROGRAM THAT DEMONSTRATES THE PASS BY VALUE IN FUNCTION**
```c
#include <stdio.h>
void changeValue(int num) {
    num = num + 10;
    printf("Inside function: num = %d\n", num);
}
int main() {
    int a = 5;
    printf("Before function call: a = %d\n", a);
    changeValue(a);
    printf("After function call: a = %d\n", a);
    return 0;
}
```
**OUTPUT:**
Before function call: a = 5
Inside function: num = 15
After function call: a = 5

---

**Tiếng Việt:**

**ĐỊNH NGHĨA VÀ SỬ DỤNG HÀM (tiếp theo..)**

**2. CHƯƠNG TRÌNH C MINH HỌA TRUYỀN BẰNG GIÁ TRỊ TRONG HÀM**
```c
#include <stdio.h>
void changeValue(int num) {
    num = num + 10;
    printf("Bên trong hàm: num = %d\n", num);
}
int main() {
    int a = 5;
    printf("Trước khi gọi hàm: a = %d\n", a);
    changeValue(a);
    printf("Sau khi gọi hàm: a = %d\n", a);
    return 0;
}
```**KẾT QUẢ:**
Trước khi gọi hàm: a = 5
Bên trong hàm: num = 15
Sau khi gọi hàm: a = 5

***

### **Slide 19**

**English:**

**DEFINING AND USING FUNCTIONS (cont..)**

**PASS BY REFERENCE**
In Pass by Reference, you pass the address of a variable to a function instead of its value.
This allows the function to:
*   Access the original variable.
*   Modify its value directly.
*   Any change made inside the function will reflect outside the function too.
*   we simulate Pass by Reference by passing pointers (addresses).

---

**Tiếng Việt:**

**ĐỊNH NGHĨA VÀ SỬ DỤNG HÀM (tiếp theo..)**

**TRUYỀN BẰNG THAM CHIẾU**
Trong Truyền bằng tham chiếu, bạn truyền địa chỉ của một biến cho một hàm thay vì giá trị của nó.
Điều này cho phép hàm:
*   Truy cập biến gốc.
*   Sửa đổi trực tiếp giá trị của nó.
*   Mọi thay đổi được thực hiện bên trong hàm cũng sẽ ảnh hưởng đến bên ngoài hàm.
*   chúng ta mô phỏng Truyền bằng tham chiếu bằng cách truyền con trỏ (địa chỉ).

***

### **Slide 20**

**English:**

**DEFINING AND USING FUNCTIONS (cont..)**

**3.C PROGRAM THAT DEMONSTRATES THE PASS BY REFERENCE IN FUNCTION**
```c
#include <stdio.h>
void update(int *p) {
    *p = *p + 10;
}
int main() {
    int a = 5;
    update(&a);
    printf("Updated value: %d\n", a);
    return 0;
}
```
**OUTPUT:**
Updated value: 15

---

**Tiếng Việt:**

**ĐỊNH NGHĨA VÀ SỬ DỤNG HÀM (tiếp theo..)**

**3. CHƯƠNG TRÌNH C MINH HỌA TRUYỀN BẰNG THAM CHIẾU TRONG HÀM**
```c
#include <stdio.h>
void update(int *p) {
    *p = *p + 10;
}
int main() {
    int a = 5;
    update(&a);
    printf("Giá trị đã cập nhật: %d\n", a);
    return 0;
}
```
**KẾT QUẢ:**
Giá trị đã cập nhật: 15

***

### **Slide 21**

**English:**

**TYPES OF FUNCTIONS**

There are two types of functions in C:
1.  Library Functions.
2.  User Defined Functions.

**1. LIBRARY FUNCTION:** also referred to as a “built-in function”.
*   A compiler package already exists that contains these functions, each of which has a specific meaning and is included in the package.
*   Built-in functions have the advantage of being directly usable without being defined.
**EXAMPLES:** pow(), sqrt(), strcmp(), strcpy() etc.

---

**Tiếng Việt:**

**CÁC LOẠI HÀM**

Có hai loại hàm trong C:
1.  Hàm thư viện.
2.  Hàm do người dùng định nghĩa.

**1. HÀM THƯ VIỆN:** còn được gọi là "hàm dựng sẵn".
*   Một gói trình biên dịch đã tồn tại chứa các hàm này, mỗi hàm có một ý nghĩa cụ thể và được bao gồm trong gói.
*   Các hàm dựng sẵn có lợi thế là có thể sử dụng trực tiếp mà không cần định nghĩa.
**VÍ DỤ:** pow(), sqrt(), strcmp(), strcpy(), v.v.

***

### **Slide 22**

**English:**

**TYPES OF FUNCTIONS (cont..)**

**4. PROGRAM THAT DEMONSTRATES THE USAGE OF BUILT-IN FUNCTIONS**
```c
#include <math.h>
#include <stdio.h>
int main() {
    double Number;
    Number = 49;
    double squareRoot = sqrt(Number);
    printf("The Square root of %.2lf = %.2lf", Number, squareRoot);
    return 0;
}
```
**OUTPUT:**
The Square root of 49.00 = 7.00

---

**Tiếng Việt:**

**CÁC LOẠI HÀM (tiếp theo..)**

**4. CHƯƠNG TRÌNH MINH HỌA VIỆC SỬ DỤNG CÁC HÀM DỰNG SẴN**
```c
#include <math.h>
#include <stdio.h>
int main() {
    double Number;
    Number = 49;
    double squareRoot = sqrt(Number);
    printf("Căn bậc hai của %.2lf = %.2lf", Number, squareRoot);
    return 0;
}
```
**KẾT QUẢ:**
Căn bậc hai của 49.00 = 7.00

***

### **Slide 23**

**English:**

**TYPES OF FUNCTIONS (cont..)**

**2. USER-DEFINED FUNCTIONS:**
*   Functions that the programmer creates are known as User-Defined functions.
*   User-defined functions can be improved and modified according to the need of the programmer.
*   Whenever we write a function that is case-specific and is not defined in any header file, we need to declare and define our own functions according to the syntax.

---

**Tiếng Việt:**

**CÁC LOẠI HÀM (tiếp theo..)**

**2. HÀM DO NGƯỜI DÙNG ĐỊNH NGHĨA:**
*   Các hàm do lập trình viên tạo ra được gọi là hàm do người dùng định nghĩa.
*   Các hàm do người dùng định nghĩa có thể được cải tiến và sửa đổi theo nhu cầu của lập trình viên.
*   Bất cứ khi nào chúng ta viết một hàm dành riêng cho trường hợp cụ thể và không được định nghĩa trong bất kỳ tệp tiêu đề nào, chúng ta cần khai báo và định nghĩa các hàm của riêng mình theo cú pháp.

***

### **Slide 24**

**English:**

**TYPES OF FUNCTIONS (cont..)**

**5. PROGRAM THAT DEMONSTRATES THE USAGE OF USER-DEFINED FUNCTIONS**
```c
#include <stdio.h>
int add(int a, int b)
{
    return a + b;
}
int main()
{
    int a = 10, b = 20;
    int sum = add(a, b);
    printf("Sum is: %d", sum);
    return 0;
}
```
**OUTPUT:**
Sum is: 30

---

**Tiếng Việt:**

**CÁC LOẠI HÀM (tiếp theo..)**

**5. CHƯƠNG TRÌNH MINH HỌA VIỆC SỬ DỤNG HÀM DO NGƯỜI DÙNG ĐỊNH NGHĨA**
```c
#include <stdio.h>
int add(int a, int b)
{
    return a + b;
}
int main()
{
    int a = 10, b = 20;
    int sum = add(a, b);
    printf("Tổng là: %d", sum);
    return 0;
}
```
**KẾT QUẢ:**
Tổng là: 30

***

### **Slide 25**

**English:**

**SCOPE**

**SCOPE:**
*   In C programming, scope refers to the visibility and accessibility of a variable or function within different parts of the program.
*   It defines where a variable can be used or modified in your code.
*   Think of scope like permissions: some variables can be accessed only in one room (function), while others are visible everywhere (global).

---

**Tiếng Việt:**

**PHẠM VI (SCOPE)**

**PHẠM VI:**
*   Trong lập trình C, phạm vi đề cập đến khả năng hiển thị và khả năng truy cập của một biến hoặc hàm trong các phần khác nhau của chương trình.
*   Nó xác định nơi một biến có thể được sử dụng hoặc sửa đổi trong mã của bạn.
*   Hãy coi phạm vi giống như quyền hạn: một số biến chỉ có thể được truy cập trong một phòng (hàm), trong khi những biến khác có thể nhìn thấy ở mọi nơi (toàn cục).

***

### **Slide 26**

**English:**

**SCOPE (cont..)**

**Why Scope Matters in Functions?**
When writing functions in C, understanding variable scope helps you:
*   Avoid naming conflicts,
*   Control access to data,
*   Manage memory efficiently.

---

**Tiếng Việt:**

**PHẠM VI (tiếp theo..)**

**Tại sao phạm vi lại quan trọng trong các hàm?**
Khi viết các hàm trong C, việc hiểu phạm vi của biến sẽ giúp bạn:
*   Tránh xung đột tên,
*   Kiểm soát quyền truy cập vào dữ liệu,
*   Quản lý bộ nhớ hiệu quả.

***

### **Slide 27**

**English:**

**SCOPE (cont..)**

**Local Scope**
*   **Definition:** A variable declared inside a function or block {} is called a local variable.
*   It is only accessible within that function/block.
*   Memory is allocated when function is called and deallocated when it ends.
**Characteristics:**
*   Declared inside a function.
*   Not known to other functions.
*   Re-initialized every time the function runs.

---

**Tiếng Việt:**

**PHẠM VI (tiếp theo..)**

**Phạm vi cục bộ (Local Scope)**
*   **Định nghĩa:** Một biến được khai báo bên trong một hàm hoặc khối lệnh {} được gọi là biến cục bộ.
*   Nó chỉ có thể được truy cập trong hàm/khối lệnh đó.
*   Bộ nhớ được cấp phát khi hàm được gọi và được giải phóng khi nó kết thúc.
**Đặc điểm:**
*   Được khai báo bên trong một hàm.
*   Không được biết đến bởi các hàm khác.
*   Được khởi tạo lại mỗi khi hàm chạy.

***

### **Slide 28**

**English:**

**SCOPE (cont..)**

**6.C PROGRAM THAT DEMONSTRATES THE USAGE OF LOCAL SCOPE**
```c
#include <stdio.h>
void display() {
    int localVar = 10; // local to display()
    printf("Value of localVar inside display(): %d\n", localVar);
}
int main() {
    display();
    // printf("%d", localVar);
    // Uncommenting above line will cause an error (localVar not accessible here)
    return 0;
}
```
**OUTPUT:**
Value of localVar inside display(): 10

---

**Tiếng Việt:**

**PHẠM VI (tiếp theo..)**

**6. CHƯƠNG TRÌNH C MINH HỌA VIỆC SỬ DỤNG PHẠM VI CỤC BỘ**
```c
#include <stdio.h>
void display() {
    int localVar = 10; // biến cục bộ của hàm display()
    printf("Giá trị của localVar bên trong display(): %d\n", localVar);
}
int main() {
    display();
    // printf("%d", localVar);
    // Bỏ chú thích dòng trên sẽ gây ra lỗi (localVar không thể truy cập ở đây)
    return 0;
}
```
**KẾT QUẢ:**
Giá trị của localVar bên trong display(): 10

***

### **Slide 29**

**English:**

**SCOPE (cont..)**

**GLOBAL SCOPE**
A variable declared outside all functions (usually at the top of the file).
It is accessible to all functions in the program.
**Characteristics:**
*   Known throughout the program.
*   Memory is allocated once and stays till the end of the program.
*   Can be modified by any function.

---

**Tiếng Việt:**

**PHẠM VI (tiếp theo..)**

**PHẠM VI TOÀN CỤC (GLOBAL SCOPE)**
Một biến được khai báo bên ngoài tất cả các hàm (thường ở đầu tệp).
Nó có thể được truy cập bởi tất cả các hàm trong chương trình.
**Đặc điểm:**
*   Được biết đến trong toàn bộ chương trình.
*   Bộ nhớ được cấp phát một lần và tồn tại cho đến khi kết thúc chương trình.
*   Có thể được sửa đổi bởi bất kỳ hàm nào.

***

### **Slide 30**

**English:**

**SCOPE (cont..)**

**7.C PROGRAM THAT DEMONSTRATES THE USAGE OF GLOBAL SCOPE**
```c
#include <stdio.h>
// Global variable
int globalVar = 100;
void display()
{
    printf("Value of globalVar inside display(): %d\n", globalVar);
}
int main()
{
    printf("Value of globalVar inside main(): %d\n", globalVar);
    display();
    return 0;
}
```
**OUTPUT:**
Value of globalVar inside main(): 100
Value of globalVar inside display(): 100

---

**Tiếng Việt:**

**PHẠM VI (tiếp theo..)**

**7. CHƯƠNG TRÌNH C MINH HỌA VIỆC SỬ DỤNG PHẠM VI TOÀN CỤC**
```c
#include <stdio.h>
// Biến toàn cục
int globalVar = 100;
void display()
{
    printf("Giá trị của globalVar bên trong display(): %d\n", globalVar);
}
int main()
{
    printf("Giá trị của globalVar bên trong main(): %d\n", globalVar);
    display();
    return 0;
}
```
**KẾT QUẢ:**
Giá trị của globalVar bên trong main(): 100
Giá trị của globalVar bên trong display(): 100

***

### **Slide 31**

**English:**

**SCOPE: PROGRAM EXECUTION STACK**

**Program execution stack**
*   A stack is a last-in, first-out (LIFO) data structure.
*   Anything put into the stack is placed “on top”.
*   The only data that can be taken out is the data on top.
*   C uses a program execution stack to keep track of which functions have been called.
*   When a function is called, it is placed on top of the stack.
*   When a function ends, it is taken off the stack and control returns to the function immediately below it.
*   Calling more functions than C can handle at once is known as a “stack overflow error”.

---

**Tiếng Việt:**

**PHẠM VI: NGĂN XẾP THỰC THI CHƯƠNG TRÌNH (STACK)**

**Ngăn xếp thực thi chương trình**
*   Ngăn xếp (stack) là một cấu trúc dữ liệu vào sau, ra trước (LIFO - last-in, first-out).
*   Bất cứ thứ gì được đưa vào ngăn xếp đều được đặt "lên trên cùng".
*   Dữ liệu duy nhất có thể được lấy ra là dữ liệu ở trên cùng.
*   C sử dụng một ngăn xếp thực thi chương trình để theo dõi các hàm đã được gọi.
*   Khi một hàm được gọi, nó được đặt lên trên cùng của ngăn xếp.
*   Khi một hàm kết thúc, nó được lấy ra khỏi ngăn xếp và quyền điều khiển trở về hàm ngay bên dưới nó.
*   Việc gọi nhiều hàm hơn mức C có thể xử lý cùng một lúc được gọi là "lỗi tràn ngăn xếp" (stack overflow error).

***

### **Slide 32**

**English:**

**SCOPE: STORAGE CLASSES**

**Storage classes** govern the:
*   **storage duration** - how long an object exists in memory
*   **Scope** – where object can be referenced in program
*   **Default value** – initial value if no value is assigned
*   **storage area** – where the variable would get stored
*   **Linkage** - specifies the files in which an identifier is known
**C has 4 storage class specifiers**
*   auto
*   register
*   static
*   extern

---

**Tiếng Việt:**

**PHẠM VI: CÁC LỚP LƯU TRỮ (STORAGE CLASSES)**

**Các lớp lưu trữ** quy định:
*   **thời gian lưu trữ** - một đối tượng tồn tại trong bộ nhớ bao lâu
*   **Phạm vi** – nơi đối tượng có thể được tham chiếu trong chương trình
*   **Giá trị mặc định** – giá trị ban đầu nếu không có giá trị nào được gán
*   **vùng lưu trữ** – nơi biến sẽ được lưu trữ
*   **Liên kết (Linkage)** - chỉ định các tệp trong đó một định danh được biết đến
**C có 4 chỉ định lớp lưu trữ**
*   auto
*   register
*   static
*   extern

***

### **Slide 33**

**English:**

**SCOPE: STORAGE CLASSES**

**TABLE 9.1 STORAGE CLASSES**
| Keyword | Storage Location | Default Initial Value | Scope | Lifetime |
| :--- | :--- | :--- | :--- | :--- |
| **Automatic** | auto | Memory (Stack) | Garbage (undefined) | Local to the block |
| **Register** | register | CPU Register (if available) | Garbage (undefined) | Local to the block |
| **Static** | static | Memory (Data Segment) | Zero (for global) / Retains last value | Local to block (if inside function), Global (if outside) |
| **External** | extern | Memory (Data Segment) | Depends on actual definition | Global across files |

---

**Tiếng Việt:**

**PHẠM VI: CÁC LỚP LƯU TRỮ**

**BẢNG 9.1 CÁC LỚP LƯU TRỮ**
| Từ khóa | Vị trí lưu trữ | Giá trị khởi tạo mặc định | Phạm vi | Vòng đời |
| :--- | :--- | :--- | :--- | :--- |
| **Automatic** | auto | Bộ nhớ (Ngăn xếp - Stack) | Rác (không xác định) | Cục bộ trong khối lệnh |
| **Register** | register | Thanh ghi CPU (nếu có) | Rác (không xác định) | Cục bộ trong khối lệnh |
| **Static** | static | Bộ nhớ (Vùng dữ liệu - Data Segment) | Không (cho biến toàn cục) / Giữ lại giá trị cuối cùng | Cục bộ trong khối (nếu trong hàm), Toàn cục (nếu bên ngoài) |
| **External** | extern | Bộ nhớ (Vùng dữ liệu - Data Segment) | Phụ thuộc vào định nghĩa thực tế | Toàn cục trên các tệp |

***

### **Slide 34**

**English:**

**RECURSION**

**RECURSION:**
*   Recursion is a programming technique in which a function calls itself, either directly or indirectly, to solve a problem.
*   A recursive function keeps calling itself with a modified input until a base condition is met.

---

**Tiếng Việt:**

**ĐỆ QUY (RECURSION)**

**ĐỆ QUY:**
*   Đệ quy là một kỹ thuật lập trình trong đó một hàm tự gọi chính nó, một cách trực tiếp hoặc gián tiếp, để giải quyết một vấn đề.
*   Một hàm đệ quy tiếp tục tự gọi chính nó với đầu vào đã được sửa đổi cho đến khi một điều kiện cơ sở được thỏa mãn.

***

### **Slide 35**

**English:**

**RECURSION (cont..)**

**WHY RECURSION IS USED?**
*   To solve problems that can be broken into similar sub-problems.
*   To solve problems that naturally follow a recursive pattern, like:
    *   Factorial calculation
    *   Fibonacci series

---

**Tiếng Việt:**

**ĐỆ QUY (tiếp theo..)**

**TẠI SAO SỬ DỤNG ĐỆ QUY?**
*   Để giải quyết các vấn đề có thể được chia thành các bài toán con tương tự.
*   Để giải quyết các vấn đề tuân theo một khuôn mẫu đệ quy tự nhiên, như:
    *   Tính giai thừa
    *   Dãy Fibonacci

***

### **Slide 36**

**English:**

**RECURSION (cont..)**

**HOW IT WORKS?**
*   Function call stack is used by the compiler to keep track of all function calls.
*   Each recursive call creates a new instance of the function with its own set of variables.
*   Recursion continues until a base case is met.
*   Once the base case is met, the calls return in reverse order, completing the operation.

---

**Tiếng Việt:**

**ĐỆ QUY (tiếp theo..)**

**NÓ HOẠT ĐỘNG NHƯ THẾ NÀO?**
*   Ngăn xếp gọi hàm được trình biên dịch sử dụng để theo dõi tất cả các lần gọi hàm.
*   Mỗi lần gọi đệ quy tạo ra một thể hiện mới của hàm với bộ biến riêng của nó.
*   Đệ quy tiếp tục cho đến khi một trường hợp cơ sở được đáp ứng.
*   Khi trường hợp cơ sở được đáp ứng, các lệnh gọi sẽ trả về theo thứ tự ngược lại, hoàn thành hoạt động.

***

### **Slide 37**

**English:**

**RECURSION (cont..)**

**8.C PROGRAM THAT CALCULATES THE FACTORIAL OF NUMBER USING RECURSION**
```c
#include <stdio.h>
int factorial(int n) {
    if (n == 0)
        return 1; // base case
    else
        return n * factorial(n - 1); // recursive call
}
int main() {
    int num = 5;
    printf("Factorial of %d is %d\n", num, factorial(num));
    return 0;
}
```

---

**Tiếng Việt:**

**ĐỆ QUY (tiếp theo..)**

**8. CHƯƠNG TRÌNH C TÍNH GIAI THỪA CỦA MỘT SỐ SỬ DỤNG ĐỆ QUY**
```c
#include <stdio.h>
int factorial(int n) {
    if (n == 0)
        return 1; // trường hợp cơ sở
    else
        return n * factorial(n - 1); // gọi đệ quy
}
int main() {
    int num = 5;
    printf("Giai thừa của %d là %d\n", num, factorial(num));
    return 0;
}
```

***

### **Slide 38**

**English:**

**RECURSION (cont..)**

**WORKING:**
*   Each time any function is called in C—be it recursive or not—the function gets its own set of local variables and formal parameters with which to work!
*   These local automatic variables are stored in a memory area called stack.
*   Each new function call pushes a new activation record on the stack.
*   This activation record contains its set of automatic local variables.
*   When a function call returns, its activation record is removed from the top of the stack.

[Image illustrates the stack frames for calculating factorial(3), showing separate `n` and `result` for each call.]

---

**Tiếng Việt:**

**ĐỆ QUY (tiếp theo..)**

**CÁCH HOẠT ĐỘNG:**
*   Mỗi khi một hàm bất kỳ được gọi trong C—dù là đệ quy hay không—hàm đó sẽ nhận được một bộ biến cục bộ và tham số hình thức riêng để làm việc!
*   Các biến tự động cục bộ này được lưu trữ trong một vùng nhớ gọi là ngăn xếp (stack).
*   Mỗi lời gọi hàm mới sẽ đẩy một bản ghi kích hoạt (activation record) mới vào ngăn xếp.
*   Bản ghi kích hoạt này chứa tập hợp các biến tự động cục bộ của nó.
*   Khi một lời gọi hàm trả về, bản ghi kích hoạt của nó sẽ được xóa khỏi đỉnh ngăn xếp.

[Hình ảnh minh họa các khung ngăn xếp để tính giai thừa (3), hiển thị các biến `n` và `result` riêng biệt cho mỗi lần gọi.]

***

### **Slide 39**

**English:**

**RECURSION (cont..)**

**9.C PROGRAM PRINTS FIBONACCI SERIES USING RECURSION**
```c
#include <stdio.h>
int fibonacci(int n) {
    if (n == 0)
        return 0;
    else if (n == 1)
        return 1;
    else
        return fibonacci(n - 1) + fibonacci(n - 2);
}
int main() {
    int i, terms = 7;
    printf("Fibonacci Series: ");
    for (i = 0; i < terms; i++) {
        printf("%d ", fibonacci(i));
    }
    return 0;
}
```
**OUTPUT:**
Fibonacci Series: 0 1 1 2 3 5 8

---

**Tiếng Việt:**

**ĐỆ QUY (tiếp theo..)**

**9. CHƯƠNG TRÌNH C IN DÃY FIBONACCI SỬ DỤNG ĐỆ QUY**
```c
#include <stdio.h>
int fibonacci(int n) {
    if (n == 0)
        return 0;
    else if (n == 1)
        return 1;
    else
        return fibonacci(n - 1) + fibonacci(n - 2);
}
int main() {
    int i, terms = 7;
    printf("Dãy Fibonacci: ");
    for (i = 0; i < terms; i++) {
        printf("%d ", fibonacci(i));
    }
    return 0;
}
```
**KẾT QUẢ:**
Dãy Fibonacci: 0 1 1 2 3 5 8

***

### **Slide 40**

**English:**

**SUMMARY**
*   **Introduction to Functions:** Introduced the concept of functions to promote modularity and code reusability.
*   **Function Syntax & Parameter Passing:** Covered function declaration, definition, calling, and parameter passing (by value and by reference).
*   **Types, Scope & Storage Explained:** function types, variable scope (local/global), and storage classes (auto, static, etc.).
*   **Recursion Concepts:** Demonstrated recursion through factorial and Fibonacci programs.
*   **AI Code Generation:** Showcased the use of AI tools to generate function-based code from natural language prompts.

---

**Tiếng Việt:**

**TỔNG KẾT**
*   **Giới thiệu về Hàm:** Giới thiệu khái niệm về hàm để thúc đẩy tính mô-đun và khả năng tái sử dụng mã.
*   **Cú pháp hàm & Truyền tham số:** Đã trình bày về khai báo, định nghĩa, gọi hàm và truyền tham số (theo giá trị và theo tham chiếu).
*   **Giải thích về Loại, Phạm vi & Lưu trữ:** các loại hàm, phạm vi biến (cục bộ/toàn cục) và các lớp lưu trữ (auto, static, v.v.).
*   **Khái niệm Đệ quy:** Minh họa đệ quy thông qua các chương trình tính giai thừa và Fibonacci.
*   **Sinh mã bằng AI:** Trình bày việc sử dụng các công cụ AI để tạo mã dựa trên hàm từ các câu lệnh ngôn ngữ tự nhiên.
