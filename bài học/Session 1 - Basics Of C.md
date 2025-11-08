# Session 1 - Basics Of C

### **Slide 1: Trang bìa**

**Cranes Varsity**
'Nơi Công Nghệ Hội Tụ Cùng Sự Ưu Việt'

**Chương trình:**
Chương trình Phát triển Phần mềm Ô tô

**Học kỳ 1:**
Chứng chỉ Phát triển Phần mềm Ô tô (CAS)

**Học phần:**
Lập trình C/C++ cho Hệ thống Nhúng AI

**Buổi 01:**
Những điều cơ bản về C

---

### **Slide 2: Mục tiêu và Chủ đề Buổi học**

**MỤC TIÊU VÀ CHỦ ĐỀ BUỔI HỌC**

| Giới thiệu về chương trình, Các thành phần của bất kỳ Ngôn ngữ Lập trình nào | Thuật toán, Mã giả, Lưu đồ | Giới thiệu về C | Thực hành |
| :--- | :--- | :--- | :--- |
| Để học những điều cơ bản về lập trình và các loại ngôn ngữ. Hiểu các thành phần chính của một ngôn ngữ lập trình. | Để giới thiệu về giải quyết vấn đề logic bằng cách sử dụng thuật toán, mã giả và lưu đồ. | Để được giới thiệu về ngôn ngữ C, lịch sử, các tính năng, ứng dụng của nó. Hiểu cấu trúc chương trình C, học cách biên dịch và thực thi nó. | **Hỏi & Đáp và Tóm tắt** |

---

### **Slide 3: Giới thiệu về Chương trình**

**GIỚI THIỆU VỀ CHƯƠNG TRÌNH**

**Lập trình**, còn được gọi là **viết mã (coding)**, là quá trình tạo ra một bộ hướng dẫn để cho máy tính biết cách thực hiện một tác vụ cụ thể.

Những hướng dẫn này, được gọi là **chương trình**, được viết bằng một ngôn ngữ mà máy tính có thể hiểu và thực thi.

**Các tác vụ ví dụ được thực hiện bởi chương trình:**
*   Thực hiện các phép tính
*   Lưu trữ và quản lý dữ liệu
*   Điều khiển phần cứng (ví dụ: máy in, robot)
*   Chạy các ứng dụng (ví dụ: trình duyệt web, trò chơi)

---

### **Slide 4: Ngôn ngữ Lập trình**

**NGÔN NGỮ LẬP TRÌNH**

**a) Ngôn ngữ Bậc cao (High Level Language)**
*   Nó giống như các câu lệnh tiếng Anh.
*   Cần biết Ngữ pháp của Ngôn ngữ để viết Chương trình.
*   Nó cần được Chuyển đổi thành Ngôn ngữ Máy bằng Trình biên dịch (Compiler) hoặc Trình thông dịch (Interpreter).
*   Trình biên dịch hoặc Trình thông dịch là một trình dịch chuyển đổi HLL (Ngôn ngữ bậc cao) thành MLL/BLL (Ngôn ngữ máy/Ngôn ngữ nhị phân).
*   Ví dụ: C, C++, Java, C#

**b) Hợp ngữ (Assembly Level Language)**
*   Chương trình được viết bằng bộ Lệnh của Kiến trúc Máy tính.
*   Cần biết kiến trúc cơ bản của bộ lệnh máy tính.
*   Nó cần được chuyển đổi thành Ngôn ngữ Máy bằng Trình hợp dịch (Assembler).

**c) Ngôn ngữ Máy (Machine Level Language)**
*   Nó còn được gọi là Ngôn ngữ Nhị phân ở dạng 0 và 1.
*   Máy tính chỉ hiểu Ngôn ngữ Nhị phân.

---

### **Slide 5: Phần mềm**

**PHẦN MỀM**

Phần mềm có thể được định nghĩa là **Tập hợp các Chương trình** được viết cho máy tính để thực hiện một tác vụ được xác định rõ.

Về cơ bản, phần mềm có thể có hai loại:
*   **Phần mềm ứng dụng**
*   **Phần mềm hệ thống**

**Phần mềm ứng dụng** là một tập hợp các chương trình được cập nhật rất thường xuyên.
Ví dụ: MS Office, Trình soạn thảo văn bản, Hệ thống Ngân hàng Trực tuyến, Đặt chỗ Trực tuyến, v.v.

**Phần mềm hệ thống** là một tập hợp các chương trình không thể sửa đổi được.
Ví dụ: Hệ điều hành, Trình biên dịch, Trình thông dịch, v.v.

---

### **Slide 6: Các thành phần của bất kỳ Ngôn ngữ Lập trình nào**

**CÁC THÀNH PHẦN CỦA BẤT KỲ**
**NGÔN NGỮ LẬP TRÌNH NÀO**

---

### **Slide 7: Bảng các thành phần của Ngôn ngữ Lập trình**

**Bảng dưới đây cung cấp một giải thích có cấu trúc về từng thành phần**

| Thành phần | Chủ đề |
| :--- | :--- |
| **Cú pháp (Syntax)** | Định nghĩa cấu trúc đúng của một chương trình, giống như ngữ pháp trong ngôn ngữ của con người. Cú pháp không chính xác dẫn đến lỗi biên dịch. |
| **Ngữ nghĩa (Semantics)** | Xác định ý nghĩa của các câu lệnh. Ngay cả khi cú pháp đúng, ngữ nghĩa không chính xác có thể tạo ra các kết quả không mong muốn. |
| **Từ khóa (Keywords)** | Các từ dành riêng có ý nghĩa đặc biệt (ví dụ: `if`, `while`, `return` trong C). Không thể được sử dụng làm tên biến. |
| **Định danh (Identifiers)** | Tên do người dùng định nghĩa cho các biến, hàm, mảng và các thực thể khác. Giúp lưu trữ và thao tác dữ liệu. |
| **Toán tử (Operators)** | Các ký hiệu thực hiện các phép toán trên các giá trị (ví dụ: `+`, `*`, `/`, `==` trong C). |
| **Kiểu dữ liệu (Data Types)** | Định nghĩa loại dữ liệu được lưu trữ trong các biến (ví dụ: `int`, `float`, `char`, `double`). |
| **Biến (Variables)** | Các vị trí bộ nhớ được đặt tên được sử dụng để lưu trữ dữ liệu có thể được sửa đổi trong quá trình thực thi. |
| **Cấu trúc điều khiển (Control Structures)**| Các câu lệnh điều khiển luồng thực thi (ví dụ: `for`, `while`, `if`). |
| **Hàm (Functions)** | Các khối mã có thể tái sử dụng thực hiện các tác vụ cụ thể, cải thiện tính mô-đun và hiệu quả. |
| **Thư viện (Libraries)** | Các hàm và quy trình được xác định trước (ví dụ: `stdio.h` cho các hoạt động I/O). |

---

### **Slide 8: Thuật toán**

**THUẬT TOÁN**

**Thuật toán** là một quy trình từng bước hoặc một tập hợp các quy tắc được thiết kế để thực hiện một tác vụ cụ thể hoặc giải quyết một vấn đề.

Nó đóng vai trò là nền tảng của lập trình và giải quyết vấn đề tính toán.

**TẦM QUAN TRỌNG CỦA THUẬT TOÁN**
*   **Nền tảng của Lập trình:** Mọi chương trình đều dựa trên một thuật toán cơ bản.
*   **Giải quyết vấn đề được tối ưu hóa:** Giúp tìm ra các giải pháp hiệu quả.
*   **Độc lập với ngôn ngữ:** Một thuật toán có thể được triển khai trong bất kỳ ngôn ngữ lập trình nào.
*   **Cải thiện Tư duy Logic:** Viết thuật toán giúp tăng cường kỹ năng giải quyết vấn đề.

---

### **Slide 9: Cấu trúc cơ bản của Thuật toán**

**THUẬT TOÁN (tiếp...)**

**CẤU TRÚC CƠ BẢN CỦA THUẬT TOÁN**
Một thuật toán được xác định rõ tuân theo một định dạng có cấu trúc để giải quyết một vấn đề từng bước. Dưới đây là cấu trúc chung của một thuật toán:
*   **Bắt đầu (Start):** Cho biết sự bắt đầu của thuật toán.
*   **Nhập (Input):** Chấp nhận các đầu vào cần thiết cho quá trình.
*   **Xử lý (Processing):** Logic chính hoặc tập hợp các bước để giải quyết vấn đề.
*   **Xuất (Output):** Hiển thị kết quả dựa trên quá trình xử lý.
*   **Kết thúc (End):** Đánh dấu sự kết thúc của thuật toán.

---

### **Slide 10: Ví dụ về Thuật toán**

**THUẬT TOÁN (tiếp...)**

**Ví dụ 1: Thuật toán Cộng hai số**
*   BƯỚC 01: Bắt đầu
*   BƯỚC 02: Nhập hai số A và B
*   BƯỚC 03: Tính Tổng = A + B
*   BƯỚC 04: In Tổng
*   BƯỚC 05: Kết thúc

**Ví dụ 2: Thuật toán Tìm số lớn nhất trong hai số**
1.  Bắt đầu
2.  Nhập hai số A và B
3.  Nếu A > B, in "A lớn hơn"
4.  Ngược lại, in "B lớn hơn"
5.  Dừng

---

### **Slide 11: Mã giả (Pseudocode)**

**MÃ GIẢ**

**Mã giả** là một biểu diễn cấp cao của một thuật toán sử dụng tiếng Anh đơn giản và cú pháp giống lập trình để mô tả các bước của một chương trình.

Nó được sử dụng như một bước trung gian giữa tuyên bố vấn đề và việc viết mã thực tế trong một ngôn ngữ lập trình.

**Đặc điểm của mã giả**
*   **Dễ đọc & Dễ hiểu** – Sử dụng các câu lệnh giống tiếng Anh đơn giản.
*   **Độc lập với ngôn ngữ** – Không được viết bằng bất kỳ ngôn ngữ lập trình cụ thể nào.
*   **Tập trung vào Logic** - Bỏ qua cú pháp và chỉ tập trung vào logic của thuật toán.
*   **Quy trình từng bước** – Xác định rõ ràng trình tự các hoạt động.

---

### **Slide 12: Ví dụ về Mã giả**

**MÃ GIẢ (tiếp...)**

**VÍ DỤ 01: MÃ GIẢ ĐỂ KIỂM TRA ĐỦ ĐIỀU KIỆN BỎ PHIẾU**
```
BẮT ĐẦU
  NHẬP Tuổi
  NẾU Tuổi >= 18 THÌ
    IN "Bạn đủ điều kiện để bỏ phiếu"
  NGƯỢC LẠI
    IN "Bạn không đủ điều kiện để bỏ phiếu"
  KẾT THÚC NẾU
DỪNG
```

**VÍ DỤ 02: CỘNG HAI SỐ**
```
BẮT ĐẦU
  NHẬP số1
  NHẬP số2
  TỔNG = số1 + số2
  IN TỔNG
DỪNG
```

---

### **Slide 13: Lưu đồ (Flowcharts)**

**LƯU ĐỒ**

**Lưu đồ** là một biểu diễn đồ họa của một thuật toán bằng cách sử dụng các ký hiệu và mũi tên.

Nó biểu diễn trực quan luồng từng bước của một quy trình, giúp dễ hiểu logic hơn trước khi viết mã.

**CÁCH SỬ DỤNG:**
*   **Thiết kế & Phát triển Chương trình:** Giúp hình dung các thuật toán và cấu trúc mã trước khi triển khai.
*   **Gỡ lỗi & Giải quyết Vấn đề:** Xác định các lỗi logic và đơn giản hóa việc khắc phục sự cố.
*   **Giáo dục & Đào tạo:** Giúp người mới bắt đầu dễ dàng hiểu logic lập trình.
*   **Mô hình hóa Quy trình Kinh doanh:** Ghi lại các quy trình công việc và cải thiện các quy trình ra quyết định.
*   **Thiết kế Hệ thống & Phần mềm:** Sơ đồ hóa kiến trúc phần mềm và các tương tác hệ thống.

---

### **Slide 14: Ký hiệu Lưu đồ**

| Ký hiệu Lưu đồ | Tên Ký hiệu | Mô tả |
| :--- | :--- | :--- |
| Hình Oval | Bắt đầu/Kết thúc (Terminal) | Được sử dụng để biểu diễn điểm bắt đầu và kết thúc của lưu đồ. |
| Mũi tên | Đường luồng (Flow Lines) | Được sử dụng để kết nối các ký hiệu trong lưu đồ và chỉ ra hướng của luồng. |
| Hình bình hành | Nhập/Xuất (Input/Output) | Được sử dụng để đọc dữ liệu đầu vào và xuất hoặc hiển thị thông tin. |
| Hình chữ nhật | Xử lý (Process) | Thường được sử dụng để biểu diễn một quy trình. Ví dụ: Các phép toán số học, Di chuyển dữ liệu, v.v. |
| Hình thoi | Quyết định (Decision) | Thường được sử dụng để kiểm tra bất kỳ điều kiện nào hoặc đưa ra quyết định có hai câu trả lời, là có (đúng) hoặc không (sai). |
| Hình tròn | Nối (Connector) | Được sử dụng để kết nối hoặc nối các đường luồng. |
| Hình chữ nhật hở | Chú thích (Annotation) | Được sử dụng để cung cấp thông tin bổ sung về một ký hiệu lưu đồ khác dưới dạng nhận xét hoặc ghi chú. |

---

### **Slide 15: Ví dụ về Lưu đồ**

**VÍ DỤ 01: LƯU ĐỒ CỘNG HAI SỐ**

[Lưu đồ bắt đầu bằng một hình oval "Bắt đầu". Một mũi tên chỉ xuống một hình bình hành "Nhập Số1, Số2". Mũi tên tiếp theo chỉ xuống một hình chữ nhật "Tổng = Số1 + Số2". Mũi tên tiếp theo chỉ xuống một hình bình hành "In Tổng". Mũi tên cuối cùng chỉ xuống một hình oval "Kết thúc".]

---

### **Slide 16: Lịch sử của C**

**LỊCH SỬ CỦA C**

**Nguồn gốc của C**
*   **Phát triển bởi:** Dennis Ritchie
*   **Năm:** Đầu những năm 1970
*   **Địa điểm:** Bell Labs, Hoa Kỳ
*   **Mục đích:** Được tạo ra cho lập trình hệ thống, đặc biệt là để viết hệ điều hành **Unix**.

**Tiền thân của C**
*   **ALGOL (thập niên 1950):** Một ngôn ngữ lập trình có cấu trúc đã ảnh hưởng đến nhiều ngôn ngữ sau này.
*   **BCPL (1966):** Được phát triển bởi Martin Richards. BCPL (Ngôn ngữ Lập trình Kết hợp Cơ bản) được thiết kế cho phần mềm hệ thống.
*   **Ngôn ngữ B (1969):** Được phát triển bởi Ken Thompson, dựa trên BCPL, được sử dụng để phát triển Unix thời kỳ đầu.

---

### **Slide 17: Lịch sử của C (tiếp)**

**LỊCH SỬ CỦA C (tiếp)**
*   **1972:** C được tạo ra bởi Dennis Ritchie tại Bell Labs.
*   **1973:** Unix được viết lại bằng C, thúc đẩy sự phổ biến của nó.
*   **1978:** Sách "The C Programming Language" (bởi Brian Kernighan và Dennis Ritchie) được xuất bản.
*   **1983:** ANSI (Viện Tiêu chuẩn Quốc gia Hoa Kỳ) bắt đầu chuẩn hóa C.
*   **1989:** ANSI C (C89) được phát hành chính thức.
*   **1990:** ISO (Tổ chức Tiêu chuẩn hóa Quốc tế) đã thông qua ANSI C với tên gọi C90.
*   **1999:** C99 giới thiệu các tính năng mới như hàm nội tuyến và mảng có độ dài thay đổi.
*   **2011:** C11 đã thêm hỗ trợ đa luồng và các cải tiến khác.
*   **2018:** C18 đã mang lại các bản sửa lỗi nhỏ và làm rõ.

---

### **Slide 18: Ảnh hưởng của C**

**ẢNH HƯỞNG CỦA C**

*   C đã trở thành nền tảng cho nhiều ngôn ngữ hiện đại, bao gồm **C++, Java, C#, Python, và JavaScript.**
*   Nó vẫn được sử dụng rộng rãi trong **lập trình hệ thống**, **hệ thống nhúng**, và các **hệ điều hành** như **Linux và Windows**.

---

### **Slide 19: Đặc điểm của C**

**ĐẶC ĐIỂM CỦA C**

*   Ngôn ngữ bậc trung
*   Ngôn ngữ Lập trình có cấu trúc
*   Tính mô-đun
*   Hiệu quả
*   Nhanh hơn và Đơn giản hơn

---

### **Slide 20: Ứng dụng của C**

**ỨNG DỤNG CỦA C**

*   Phần mềm hệ thống
*   Phần mềm nhúng/firmware
*   Ứng dụng thời gian thực
*   Trình điều khiển thiết bị (Device Drivers)
*   Chương trình ứng dụng

---

### **Slide 21: Cấu trúc Chương trình C**

**CẤU TRÚC CHƯƠNG TRÌNH C**

*   **Phần Chú thích (Tùy chọn)**
*   **Các chỉ thị Tiền xử lý hoặc các tệp Tiêu đề**
*   **Phần Nguyên mẫu Hàm hoặc Khai báo Hàm**
*   **Phần Khai báo Biến Toàn cục**
*   **Phần hàm chính (Main)**
*   **Phần chương trình con**

```c
#include <stdio.h>
int main()
{
    printf("Hello World \n");
    return 0;
}
```

---

### **Slide 22: Chương trình C đầu tiên**

**CHƯƠNG TRÌNH C ĐẦU TIÊN**

*   **Chỉ thị Tiền xử lý (`#include <stdio.h>`)**
    *   Bao gồm thư viện đầu vào/đầu ra tiêu chuẩn.
*   **Hàm chính (`int main()`)**
    *   Điểm vào của chương trình.
*   **Thân hàm (`{ ... }`)**
    *   Chứa các câu lệnh có thể thực thi.
*   **Câu lệnh Xuất (`printf("Hello World\n");`)**
    *   In "Hello World" với một dòng mới.
*   **Câu lệnh Trả về (`return 0;`)**
    *   Cho biết chương trình kết thúc thành công.

---

### **Slide 23: Hàm main()**

**HÀM `int main()`**
*   Các chương trình C chứa một hoặc nhiều hàm, trong đó chính xác một hàm phải là `main`.
*   Dấu ngoặc đơn `()` được sử dụng để chỉ ra một hàm.
*   `int` có nghĩa là `main` "trả về" một giá trị số nguyên.
*   Dấu ngoặc nhọn (`{` và `}`) chỉ ra một khối.
*   Thân của tất cả các hàm phải được chứa trong dấu ngoặc nhọn.

---

### **Slide 24: Trình biên dịch C**

**TRÌNH BIÊN DỊCH C**

Trình biên dịch C biên dịch chương trình C đã cho, kiểm tra lỗi, cố gắng tối ưu hóa nếu cần và cuối cùng tạo ra mã máy.

Nếu trình biên dịch tìm thấy bất kỳ lỗi nào, nó sẽ báo cáo thất bại, do đó quá trình tiếp theo (liên kết) không được thực hiện.

**Biên dịch một Chương trình C**
`$ gcc program.c`
Tạo một tệp thực thi có tên là `a.out` (theo mặc định) từ tệp nguồn `program.c`.

**Thực thi một Chương trình**
`$ ./a.out`

---

### **Slide 25: Thực hành**

**VIẾT THUẬT TOÁN VÀ LƯU ĐỒ CHO CÁC BÀI TOÁN SAU:**

*   **Kiểm tra Chẵn hay Lẻ**
    *   Nhập một số và xác định xem nó là chẵn hay lẻ.
*   **Tìm Tổng của N số tự nhiên đầu tiên**
    *   Nhập một số N và tính tổng của N số tự nhiên đầu tiên (1 + 2 + ... + N).
*   **Máy tính đơn giản**
    *   Nhận hai số và một toán tử (+, *, /) làm đầu vào và thực hiện phép toán số học tương ứng.

---

### **Slide 26: Câu hỏi**

**Câu hỏi**

**1. Điều nào sau đây KHÔNG phải là một đặc điểm chính của ngôn ngữ lập trình C?**
A) Truy cập cấp thấp vào bộ nhớ
B) Hỗ trợ thư viện phong phú
C) Lập trình hướng đối tượng
D) Tính di động

**2. Điều nào sau đây KHÔNG phải là một ứng dụng thực tế của lập trình C?**
A) Phát triển hệ điều hành
B) Lập trình hệ thống nhúng
C) Phát triển web (sử dụng HTML)
D) Phát triển phần mềm hệ thống

---

### **Slide 27: Câu hỏi (tiếp)**

**Câu hỏi**

**3. Thứ tự đúng của các thành phần trong một cấu trúc chương trình C điển hình là gì?**
A) Chỉ thị tiền xử lý, hàm chính, khai báo biến, câu lệnh thực thi, câu lệnh trả về
B) Hàm chính, câu lệnh thực thi, chỉ thị tiền xử lý, câu lệnh trả về
C) Chỉ thị tiền xử lý, khai báo biến, hàm chính, câu lệnh thực thi, câu lệnh trả về
D) Hàm chính, câu lệnh trả về, chỉ thị tiền xử lý, câu lệnh thực thi

**4. Ngôn ngữ lập trình nào là tiền thân trực tiếp của C?**
A) Java
B) Python
C) Ngôn ngữ B
D) C++

---

### **Slide 28: Đáp án**

**Đáp án**

**1. C) Lập trình hướng đối tượng**
*   **Lý giải:**
    *   C là một ngôn ngữ lập trình thủ tục, không phải hướng đối tượng.
    *   Nó không hỗ trợ các tính năng như lớp, đối tượng và kế thừa, là những khía cạnh chính của lập trình hướng đối tượng.

**2. C) Phát triển web (sử dụng HTML)**
*   **Lý giải:**
    *   C chủ yếu được sử dụng cho lập trình hệ thống, hệ thống nhúng và phát triển HĐH chứ không phải để phát triển web.
    *   HTML (HyperText Markup Language) là một ngôn ngữ đánh dấu, không phải là ngôn ngữ lập trình và được sử dụng để cấu trúc các trang web.
    *   Phát triển web thường liên quan đến các ngôn ngữ như JavaScript, PHP và Python, chứ không phải C.

---

### **Slide 29: Đáp án (tiếp)**

**Đáp án**

**3. A) Chỉ thị tiền xử lý, hàm chính, khai báo biến, câu lệnh thực thi, câu lệnh trả về**
*   **Lý giải:**
    *   Một chương trình C điển hình tuân theo cấu trúc này:
    *   **Chỉ thị Tiền xử lý (`#include <stdio.h>`)** – Xử lý các thư viện và macro.
    *   **Hàm chính (`int main() { }`)** – Điểm vào của chương trình.
    *   **Khai báo Biến** – Định nghĩa các biến được sử dụng trong chương trình.
    *   **Câu lệnh Thực thi** – Logic cốt lõi (ví dụ: `printf()`, vòng lặp, tính toán).
    *   **Câu lệnh Trả về (`return 0;`)** – Cho biết việc thực thi thành công.

---

### **Slide 30: Đáp án (tiếp)**

**Đáp án**

**4. Lựa chọn C) Ngôn ngữ B**
*   **Lý giải:**
    *   Ngôn ngữ B là tiền thân trực tiếp của C, được phát triển bởi Ken Thompson vào cuối những năm 1960.
    *   Nó được bắt nguồn từ BCPL và ảnh hưởng đến sự phát triển của C bởi Dennis Ritchie tại Bell Labs vào năm 1972.
*   **Các lựa chọn khác không chính xác vì:**
    *   Java & Python được phát triển muộn hơn nhiều và không phải là tiền thân của C.
    *   C++ thực sự là một hậu duệ của C, bổ sung các tính năng hướng đối tượng.

---

### **Slide 31: Tóm tắt**

**TÓM TẮT**

Buổi học này giới thiệu những nguyên tắc cơ bản của lập trình C, bao gồm:

1.  **Thuật toán** – Một quy trình từng bước để giải quyết vấn đề, tạo thành nền tảng của logic lập trình. Các thuộc tính chính bao gồm tính đúng đắn, hiệu quả và rõ ràng.
2.  **Mã giả** – Một biểu diễn đơn giản, cấp cao của một thuật toán sử dụng tiếng Anh đơn giản và cú pháp giống lập trình. Nó bắc cầu khoảng cách giữa tư duy của con người và việc viết mã thực tế.
3.  **Lưu đồ** – Một biểu diễn đồ họa của một thuật toán sử dụng các ký hiệu được tiêu chuẩn hóa để mô tả luồng quy trình. Nó tăng cường sự rõ ràng trong việc giải quyết vấn đề và gỡ lỗi.
4.  **Sự phát triển của C** – Được phát triển bởi Dennis Ritchie vào đầu những năm 1970 tại Bell Labs, C được thiết kế cho lập trình hệ thống, đặc biệt là để viết Unix. Trong những năm qua, nó đã trải qua nhiều lần chuẩn hóa (C89, C99, C11, C18).
5.  **Các đặc điểm chính** – C là một ngôn ngữ bậc trung, có cấu trúc, mô-đun, hiệu quả, cung cấp quyền truy cập bộ nhớ trực tiếp.
6.  **Ứng dụng** – Được sử dụng trong phần mềm hệ thống, hệ thống nhúng, ứng dụng thời gian thực, trình điều khiển thiết bị và phần mềm ứng dụng.

---

### **Slide 32: Tóm tắt (tiếp)**

**TÓM TẮT**

7.  **Ứng dụng** – Được sử dụng trong phần mềm hệ thống, hệ thống nhúng, ứng dụng thời gian thực, trình điều khiển thiết bị và phần mềm ứng dụng.
8.  **Cấu trúc Chương trình C** – Một chương trình C điển hình bao gồm các chỉ thị tiền xử lý, nguyên mẫu hàm, biến toàn cục và định nghĩa hàm.
9.  **Chương trình C đầu tiên** – Buổi học giới thiệu cấu trúc cơ bản của một chương trình C với một ví dụ.
10. **Biên dịch & Thực thi** – Quá trình này bao gồm việc biên dịch mã nguồn bằng một trình biên dịch (gcc), tạo một tệp thực thi và chạy nó.

---

### **Slide 33: Cảm ơn**

**CẢM ƠN**
