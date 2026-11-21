# Tự đánh giá — Nguyễn Tuấn Hưng · G01

## 1. Tự rà soát 4 cảnh

Nghỉ tay 1 phút, mở lại bài của mình, chọn 4 ảnh (2 S##, 2 D##), đọc như người lạ.

Loại lỗi: `seat_flip`, `wrong_class`, `guess`, `box`, `missing`, `extra`, `lr_flip` (trái/phải mặt), `flag` (thiếu cờ điểm), `ok`.

| Ảnh | Đối tượng | Loại lỗi | Ghi chú | Đã sửa? |
| --- | --------- | -------- | ------- | ------- |
| D02.png | Mắt trái/phải và kính | ok | Hai mắt bị đốm phản xạ che nên giữ `unknown`; kính `clear` được gán riêng với vùng mắt rõ. | Không cần sửa |
| D03.png | Vùng nhìn của mặt | ok | Mình xem lại và giữ `gaze_zone=lap`; hướng mắt và đầu trong khung hình phù hợp với vùng nhìn xuống đùi. | Không cần sửa |
| S01_rgb.png | Ghế trẻ em và nôi em bé | ok | Hai ghế được gán theo vị trí xe, không theo bên trái/phải ảnh; hai nhãn đều rõ. | Không cần sửa |
| S06_rgb.png | Vật trong hàng ghế sau | ok | Vật ở ghế giữa có hình dạng túi/bao rõ nên giữ `object`, `seat=rear_middle`, `type=bag`. | Không cần sửa |

## 2. Lỗi mình lặp lại nhiều nhất hôm nay

Lỗi: `guess` - đoán thuộc tính không chắc thay vì chọn `unknown` hoặc `other`.

Vì sao mình mắc: Dựa vào hướng đầu hoặc một mắt/rìa ảnh thay vì quan sát rõ toàn bộ khe mắt hoặc vùng nhìn.

Lần sau tránh bằng cách: Mỗi mắt/vùng nhìn đều kiểm riêng; nếu bị phản xạ, che, nghiêng hoặc không phân biệt rõ thì dùng `unknown`/`other`, không suy từ ảnh bên kia hoặc tên file.

## 3. Ghi chú về disagreement_log

Một dòng bạn của mình đúng và mình sai: ở D03, peer gán `gaze_zone=other` còn mình gán `lap`; một dòng khác ở D05 cũng cho thấy `gaze_zone` chưa đủ chắc để gán `road`. Mình học được là vùng nhìn phải theo hướng mắt và đầu rõ ràng, còn mơ hồ thì `other` an toàn hơn đoán.
