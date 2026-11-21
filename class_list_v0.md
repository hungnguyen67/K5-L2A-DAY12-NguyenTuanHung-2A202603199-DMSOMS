# Danh sách lớp v0 — Nguyễn Tuấn Hưng · G01

Viết tiếp từ slide 54 bài giảng. Mỗi lớp trả lời: **model cần nhận ra cái này để làm gì?**
Xóa 2 dòng ví dụ trước khi nộp.

## DMS (ít nhất 6 lớp)

| #   | Lớp / thuộc tính           | Giá trị                                                         | Để làm gì (chức năng DMS)                             | Nhìn thấy được trên IR?                                         |
| --- | -------------------------- | --------------------------------------------------------------- | ----------------------------------------------------- | --------------------------------------------------------------- |
| 1   | person / seatbelt          | driver; worn_correct / worn_incorrect / not_worn / unknown      | Xác định tài xế và việc sử dụng dây an toàn           | Thường thấy hình người; dây có thể khó thấy do tối hoặc bị che  |
| 2   | face / eye_left, eye_right | open / closed / unknown                                         | Theo dõi trạng thái mắt để hỗ trợ phát hiện buồn ngủ  | Có thể thấy trên NIR; phản xạ hoặc kính tối làm giảm độ tin cậy |
| 3   | face / gaze_zone           | road, mirror_l, mirror_r, mirror_c, cluster, center, lap, other | Phát hiện tài xế nhìn lệch khỏi vùng tập trung lái xe | Hướng đầu thường thấy; hướng mắt có thể khó thấy                |
| 4   | face / glasses             | none, clear, sun, unknown                                       | Nhận biết kính có thể ảnh hưởng khả năng quan sát mắt | Có thể thấy, nhưng kính râm/phản xạ NIR gây mơ hồ               |
| 5   | hand / on_wheel            | yes / no / unknown                                              | Theo dõi tay tài xế có chạm vô lăng hay không         | Thường thấy hình bàn tay; có thể bị che hoặc thiếu sáng         |
| 6   | phone / state              | held, mounted, lap                                              | Phát hiện sử dụng điện thoại khi lái xe               | Thường nhận ra bằng hình dạng/vị trí; không dựa vào màu         |

## OMS (ít nhất 6 lớp)

| #   | Lớp / thuộc tính      | Giá trị                                                     | Để làm gì (chức năng OMS)                                  | Nhìn thấy được trên IR?                                               |
| --- | --------------------- | ----------------------------------------------------------- | ---------------------------------------------------------- | --------------------------------------------------------------------- |
| 1   | person / seat         | driver, front_passenger, rear_left, rear_middle, rear_right | Xác định vị trí người ngồi trong xe                        | Thường thấy theo hình người và vị trí                                 |
| 2   | person / seatbelt     | worn_correct, worn_incorrect, not_worn, unknown             | Hỗ trợ nhắc thắt dây an toàn đúng cách                     | Có thể khó thấy nếu dây tối hoặc bị che                               |
| 3   | child_seat / occupied | no, yes, unknown                                            | Nhận biết ghế trẻ em và tình trạng quan sát được của ghế   | Hình dạng thường thấy; bên trong có thể bị che                        |
| 4   | infant_seat / facing  | rear, front                                                 | Xác định loại và hướng đặt nôi em bé                       | Thường dựa vào hình dạng và hướng đặt                                 |
| 5   | object / type         | bag, box, cup, other                                        | Nhận biết đồ vật trong cabin để theo dõi bố trí/rủi ro     | Có thể nhận bằng hình dạng; màu sắc không đáng tin trên IR            |
| 6   | face / bounding box   | hình chữ nhật sát vùng mặt                                  | Xác định vị trí mặt người ngồi để hỗ trợ các chức năng DMS | Thường thấy hình dạng mặt; chi tiết có thể giảm do phản xạ/thiếu sáng |

## 2 câu hỏi leo thang

Câu hỏi bạn muốn hỏi người viết guideline (hoặc khách hàng) vì guideline v1.0 chưa trả lời. Mỗi câu kèm **tên khung** làm ví dụ.

1. Câu hỏi: Nếu trạng thái mắt là `unknown` nhưng có thể xác định gần đúng vị trí điểm mặt, khi nào chọn cờ `occluded` thay vì `outside`?
   Khung ví dụ: D01.png (trường hợp mắt không nhìn rõ).
   Bạn tạm gán thế nào và vì sao: Giữ trạng thái mắt `unknown`; chỉ đặt điểm khi xác định được vị trí, nếu không thì đánh `outside`.
2. Câu hỏi: Khi ảnh IR-sim không đủ để phân biệt loại đồ vật, có nên giữ `object` và chọn `type = other` hay bỏ box nếu không chắc đó là đồ vật?
   Khung ví dụ: S01_ir.png (trường hợp đồ vật khó nhận dạng).
   Bạn tạm gán thế nào và vì sao: Chỉ vẽ `object` khi nhận ra vật bằng hình dạng/ngữ cảnh; nếu là đồ vật nhưng không rõ loại thì chọn `other`.
