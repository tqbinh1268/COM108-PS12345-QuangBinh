# BÀI THỰC HÀNH 01

Các quy định về video nộp bài, quy trình Git, cách tính điểm và vấn đáp, cùng các chế tài áp dụng chung, được trình bày tại văn bản [Quy định chung toàn khóa](Quy_Dinh_Chung_Toan_Khoa.md). Văn bản này chỉ trình bày Yêu cầu bài tập và Rubric điểm số riêng của Lab 1.

## MỤC TIÊU

Sau bài thực hành này, sinh viên có khả năng:

- Cài đặt thành thạo công cụ lập trình Visual Studio Code (VS Code), trình biên dịch GCC (MinGW) và phần mềm quản lý mã nguồn Git.
- Khởi tạo Repository và quản lý tiến độ học tập môn học bằng Git/GitHub theo cấu trúc phân mục khoa học.
- Xây dựng chương trình C đầu tiên, hiểu rõ cách xuất dữ liệu ra màn hình, cách khai báo và lựa chọn kiểu dữ liệu phù hợp, xử lý biểu thức toán học và thao tác hoán vị biến.
- Quay video thao tác gõ code trực tiếp và diễn giải bản chất kỹ thuật của từng dòng lệnh.

---

## YÊU CẦU
**Lưu ý kỹ thuật:** printf có sử dụng các định kiểu `%d`, `%s`, `%.2f` cho phù hợp vời từng biến.

### Bài 1 (2đ): Cài đặt môi trường và khởi tạo Repository

Sinh viên xem và thực hiện đúng theo các bước trong video hướng dẫn của giảng viên tại địa chỉ: https://youtu.be/vP0j3Xrc3Rs

1. Tải và cài đặt VS Code. Cài đặt hai extension bắt buộc: C/C++ và Code Runner.
2. Tải và cài đặt trình biên dịch MinGW-w64, bao gồm việc cấu hình biến môi trường Environment Path, và cài đặt phần mềm Git.
3. Tạo tài khoản GitHub nếu chưa có. Thiết lập thư mục gốc trên máy tính, đặt tên đúng cú pháp `STT_MSSV_Ten`.
4. Mở thư mục gốc bằng VS Code, khởi tạo Git và đẩy lên một Repository ở chế độ Public trên GitHub. Repository này được sử dụng chung cho tất cả các buổi Lab trong học kỳ (xem [Quy định chung](Quy_Dinh_Chung_Toan_Khoa.md), Mục 1).
5. Tạo thư mục con `Lab1` nằm bên trong thư mục gốc.

**Kiểm chứng bản chất cấu trúc C:** Trong thư mục `Lab1`, sinh viên tạo file `Bai1_HelloC.c`, viết một chương trình C đơn giản gồm các nội dung sau:

- Khai báo thư viện bằng chỉ thị `#include`.
- Hàm `main()`.
- Một câu lệnh in ra dòng chữ giới thiệu bản thân, gồm họ tên và MSSV.
- Câu lệnh `return 0;`.

Chương trình này được dùng để xác nhận môi trường biên dịch hoạt động đúng, và làm cơ sở để diễn giải trong video.


### Bài 2 (2đ): Khai báo kiểu dữ liệu và xuất dữ liệu

Sinh viên tạo file `Bai2_KieuDuLieu.c` nằm trực tiếp trong thư mục `Lab1`.

**Yêu cầu:** Khai báo các biến, chọn kiểu dữ liệu phù hợp, gán giá trị (không cần nhập) là thông tin thật của sinh viên: mã số sinh viên (MSSV), họ và tên, năm sinh, điểm trung bình.

**Dữ liệu xuất ra màn hình**, theo đúng định dạng mẫu sau:

```
Ma so sinh vien: [MSSV]
Ho Va Ten: [Họ tên]
Nam sinh: [Năm sinh]
Tuoi: [Số tuổi tự động tính = 2026 - Năm Sinh]
Diem Trung Binh: [Điểm trung bình]
```



### Bài 3 (2đ): Xử lý biểu thức toán học

Sinh viên tạo file `Bai3_TinhDiem.c` nằm trực tiếp trong thư mục `Lab1`.

**Yêu cầu:** Khai báo các biến và gán giá trị trực tiếp (không cần nhập): MSSV, họ và tên, điểm Toán, điểm Lý, điểm Hóa (điểm khai báo kiểu số thực, giá trị gán trực tiếp tuỳ chọn từ 0 đến 10).

**Dữ liệu xuất ra màn hình**, theo đúng định dạng mẫu sau:

```
Ma so sinh vien: [MSSV]
Ho Va Ten: [Họ tên]
Diem Trung Binh: [Giá trị tính được, làm tròn 1-2 chữ số thập phân]
```

**Công thức tính toán:** `DiemTrungBinh = (Toan × 2 + Ly + Hoa) / 4`, trong đó điểm Toán được nhân hệ số 2. Sinh viên cần ép kiểu `(float)` khi thực hiện phép chia để tránh mất phần thập phân của kết quả.

### Bài 4 (2đ): Hoán vị biến và toán tử

Sinh viên tạo file `Bai4_HoanVi.c` nằm trực tiếp trong thư mục `Lab1`.

**Yêu cầu:** Khai báo trực tiếp trong code hai biến kiểu số nguyên `a` và `b` với giá trị cho trước (ví dụ `a = 5`, `b = 10`). Viết chương trình hoán đổi giá trị giữa `a` và `b`, nhưng không được sử dụng biến trung gian (temp). Gợi ý sử dụng phép cộng và trừ:

```c
a = a + b;
b = a - b;
a = a - b;
```

**Dữ liệu xuất ra màn hình**, theo đúng định dạng mẫu sau:

```
Truoc khi hoan vi: a = [giá trị a], b = [giá trị b]
Sau khi hoan vi: a = [giá trị a mới], b = [giá trị b mới]
```

**Tổng điểm Lab 1 = 8.0 điểm (4 bài) + điểm cộng: tối đa 2.0 điểm = 10.0 điểm.**
