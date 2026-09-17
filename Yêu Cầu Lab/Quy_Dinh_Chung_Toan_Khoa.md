# QUY ĐỊNH CHUNG TOÀN KHÓA — MÔN COM108

Quy định các nội dung áp dụng chung cho toàn bộ các Lab cho môn học.

## 1. Cấu trúc Repository

Sinh viên tạo một Repository GitHub duy nhất ở chế độ Public, sử dụng chung cho toàn bộ các Lab trong môn học. Thư mục gốc của Repository phải được đặt tên đúng cú pháp `STT_MSSV_Ten`. Mỗi Lab tương ứng với một thư mục con nằm trực tiếp trong thư mục gốc, đặt tên theo quy ước `Lab1/`, `Lab2/`, `Lab3/`, và tiếp tục theo thứ tự các Lab trong học kỳ.

Trường hợp sinh viên để Repository ở chế độ Riêng tư (Private) khiến giảng viên không thể truy cập để chấm bài sẽ bị xử lý theo quy định tại Mục 5.

## 2. Quy trình Git

Sau khi hoàn thành và kiểm tra đúng mỗi bài hoặc mỗi chức năng, sinh viên đứng tại thư mục Lab tương ứng và thực hiện:

```
git add .
git commit -m "<mô tả ngắn bài vừa hoàn thành>"
```

Sinh viên chỉ thực hiện lệnh `git push origin main` một lần duy nhất vào cuối Lab, sau khi đã commit đầy đủ toàn bộ các phần của Lab, bao gồm cả file video.

Sinh viên cần thực hiện commit theo từng đơn vị nhỏ (Atomic Commit), trong đó mỗi hàm hoặc mỗi chức năng hoàn thành tương ứng với một commit riêng. Không dồn toàn bộ nội dung của một Lab vào một commit duy nhất.

## 3. Quy định về video nộp bài

| Nội dung | Yêu cầu |
|---|---|
| Số lượng | Nộp 4 video riêng biệt cho 4 bài của Lab. Không gộp chung thành một video tổng hợp, kể cả khi các bài được viết trong cùng một file code. |
| Thời lượng | Tối đa 5 phút cho mỗi video. Video vượt quá thời lượng quy định bị trừ 0.25 điểm cho mỗi phút vượt. |
| Hình thức ghi hình | Sinh viên bắt buộc mở webcam quay rõ mặt và chia sẻ màn hình IDE trong suốt video. Sử dụng phần mềm OBS, Clipchamp hoặc Loom để ghi hình; không sử dụng điện thoại để quay lại màn hình máy tính. |
| Âm thanh | Sinh viên phát âm rõ ràng bằng giọng nói thật của mình. Không sử dụng công nghệ Text-to-Speech (AI lồng tiếng); không để nhạc nền lấn át giọng nói. |
| Nội dung bắt buộc | Video phải thể hiện đầy đủ hai nội dung: (a) quá trình tự tay gõ code trực tiếp trong VS Code, không copy-paste; (b) phần diễn giải bản chất kỹ thuật của bài làm. |
| Nền tảng nộp bài | Sinh viên đăng tải từng video lên kênh YouTube cá nhân ở chế độ Công khai (Public). Không nộp trực tiếp file video định dạng .mp4. |
| Ghi nhận đường dẫn | Sinh viên tạo file `Video_LabX.md` trong thư mục LabX, ghi rõ đường dẫn video theo từng bài (Bài 1, Bài 2, Bài 3, Bài 4). |

## 4. Cách tính điểm từng bài (2.0 điểm/bài)

Điểm của mỗi bài trong Lab gồm hai thành phần: Code chạy đúng, và Quay video kèm giải thích kỹ thuật. Thành phần thứ hai do sinh viên tự đánh giá qua Google Form, sau đó được xác nhận lại bằng vấn đáp trực tiếp tại lớp.

### 4.1. Thành phần điểm

| Thành phần | Tiêu chí | Điểm |
|---|---|---|
| Code chạy đúng | Chương trình biên dịch và chạy đúng theo yêu cầu của đề bài | 0.5đ |
| Quay video & giải thích kỹ thuật | Có video quay tự gõ code, nhưng không có phần giải thích kỹ thuật | 0.5đ |
| | Chỉ đọc lại code trên màn hình, không nêu được lý do kỹ thuật (ví dụ: lý do chọn kiểu dữ liệu, bản chất của hàm hoặc cấu trúc đang sử dụng) | 0.75đ |
| | Nêu được mục đích của các câu lệnh và giải thích được phần lớn logic của bài làm, nhưng còn lúng túng khi trình bày về cơ chế nền tảng hoặc các trường hợp biên | 1.0đ |
| | Giải thích lưu loát toàn bộ luồng xử lý của chương trình, phân tích rõ lý do kỹ thuật và các trường hợp biên có thể xảy ra | 1.5đ |

Tổng điểm tối đa của mỗi bài là 2.0 điểm, tương ứng với 0.5 điểm (Code chạy đúng) cộng 1.5 điểm (Quay video & giải thích kỹ thuật, ở mức cao nhất).

### 4.2. Tự đánh giá qua Google Form

Đối với mỗi bài trong Lab, sinh viên tự đánh giá trên Form các nội dung sau:

- Code của bài này có chạy đúng không.
- Bài này có video quay tự gõ code không.
- Mức độ giải thích kỹ thuật mà sinh viên tự nhận đã đạt được, chọn một trong bốn mức tại Mục 4.1 (0.5đ / 0.75đ / 1.0đ / 1.5đ).

Form tự động tính ra "Điểm đề xuất", là tổng điểm của cả 4 bài, tối đa 8.0 điểm. Điểm đề xuất chỉ là điểm khởi điểm, chưa phải điểm cuối cùng. Đối với hai mục "code chạy" và "có video", giảng viên đối chiếu trực tiếp với bài nộp trên GitHub và YouTube. Tổng điểm đề xuất sẽ được sử dụng để xác định cấp câu hỏi vấn đáp tại Mục 4.3.

### 4.3. Vấn đáp trực tiếp tại lớp — Luồng hỏi và trần điểm

Căn cứ vào tổng điểm đề xuất của 4 bài (trên thang 8.0 điểm), không xét riêng từng bài, để xác định cấp câu hỏi vấn đáp sẽ bắt đầu:

| Tổng điểm đề xuất (4 bài, /8.0đ) | Cấp câu hỏi vấn đáp bắt đầu |
|---|---|
| Từ 7.0 đến 8.0 điểm | Cấp 3 – Vận dụng |
| Từ 5.0 đến dưới 7.0 điểm | Cấp 2 – Thông hiểu |
| Dưới 5.0 điểm | Cấp 1 – Nhận biết |

```
Hỏi Cấp 3
├─ Trả lời được          → Giữ nguyên điểm đề xuất từ Form (không giới hạn, tối đa 8.0đ)
└─ Trả lời không được    → Hỏi Cấp 2
    ├─ Trả lời được       → Điểm 4 bài tối đa 6.5đ
    └─ Trả lời không được → Hỏi Cấp 1
        ├─ Trả lời được       → Điểm 4 bài tối đa 5.0đ
        └─ Trả lời không được → Điểm 4 bài tối đa 3.0đ
```

## 5. Chế tài

Nộp bài muộn so với thời hạn quy định.
- Chấm bài qua đợt 2: điểm tối đa còn 8đ/10đ
- Chấm bài qua đợt 3: trở đi tối đa còn 6đ/10đ

Sinh viên vi phạm một trong các lỗi sau đây sẽ bị trừ trực tiếp trên tổng điểm của Lab, mức trừ căn cứ theo mức độ vi phạm:

- Repository để ở chế độ Private, giảng viên không thể truy cập để chấm bài: -0.5đ

- Sắp xếp sai cấu trúc cây thư mục (thư mục Lab1, Lab2,... không nằm đúng vị trí trong thư mục gốc của Repository): -0.5đ

## 6. Điểm thưởng (tối đa +2.0 điểm/Lab)

Sinh viên có thể được cộng điểm thưởng cho Lab theo hai hạng mục sau:

- Chuyên cần và hoạt động học tập tại lớp: tối đa +1.0 điểm.
- Mini Hackathon / Live Coding tại lớp, là thử thách biến đổi nhỏ so với đề bài, thực hiện trực tiếp tại Lab: tối đa +1.0 điểm.

