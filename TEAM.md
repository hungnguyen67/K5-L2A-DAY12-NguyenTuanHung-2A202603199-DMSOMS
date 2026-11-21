# TEAM — Ngày 12

Mã bộ ảnh: **G01** · Hình thức: cá nhân

| Họ tên           | MSSV        | Đã gán đủ 22 ảnh? | Review chéo với (peer diff) | Số dòng disagreement đã xử lý |
| ---------------- | ----------- | ----------------- | --------------------------- | ----------------------------- |
| Nguyễn Tuấn Hưng | 2A202603199 | có                | Đặng Minh Quân              | 0                             |

Các bất đồng ghi nhận qua diff (ghi tên ảnh + đối tượng; mục nào hai bạn chưa thống nhất thì hỏi coach):

- D01–D06: khác biệt ở nhãn DMS, gồm `seatbelt`, `gaze_zone`, trạng thái mắt, `glasses` và cờ `occluded`/`outside` của `face13`.
- S06_rgb, S06_ir: khác biệt về box `object`; S08_rgb, S08_ir: khác biệt thuộc tính `facing` của `infant_seat`.
- Tổng cộng 40 điểm khác nhau; verdict, quy tắc guideline và cách xử lý chưa được điền trong `disagreement_log.csv`, nên cần cùng xem ảnh và thống nhất trước khi chốt.

## Cá nhân

Mỗi người một mục, 1–2 dòng mỗi ý.

### NguyenTuanHung-2A202603199

- Phần mình làm (ngoài 22 ảnh của mình, ví dụ ai review ai, ai tổng hợp ca hỏi coach): Tự gán và kiểm tra đủ 22 ảnh, chạy cabin_check và đối chiếu export với Đặng Minh Quân. Diff ghi nhận 40 điểm khác nhau; hai bên cần cùng xem guideline và điền verdict, quy tắc, cách xử lý vào disagreement_log.csv.
- Điều mình học được hôm nay: Cách gán nhãn cabin theo guideline thống nhất, phân biệt OMS và DMS, đồng thời biết ghi unknown khi không nhìn rõ thay vì suy đoán.

Làm cá nhân: chỉ cần điền dòng của mình, tên bạn được coach ghép, và mục "Cá nhân" của mình.
