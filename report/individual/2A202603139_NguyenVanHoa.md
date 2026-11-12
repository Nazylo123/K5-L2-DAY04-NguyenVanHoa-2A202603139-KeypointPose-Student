# Báo cáo cá nhân — Nguyễn Văn Hòa — 2A202603139

Dữ liệu: 12 ảnh người COCO 2017 và 8 ảnh khuôn mặt từ bộ ảnh được giao; nguồn cụ thể xem `src/lab/NGUON_ANH.md`.

## 0. Thông tin học viên

- Họ tên: Nguyễn Văn Hòa
- MSSV: 2A202603139
- Email:
- Link repository: https://github.com/Nazylo123/K5-L2-DAY04-NguyenVanHoa-2A202603139-KeypointPose-Student
- Phiên bản CVAT (Help → About):
- Máy: hệ điều hành ___ · RAM ___ GB · chạy CVAT chế độ đầy đủ / lite
- Bộ ảnh (`src/exports/assignment.json` do `lab.py setup` tạo): có
- Giờ bắt đầu:
- Giờ kết thúc:

## 1. Kiểm tra label (CP0)

| Label | Kiểu | Số điểm | Tên điểm đúng bảng của lab? | Đúng thứ tự? | Số cạnh |
|---|---|---:|---|---|---:|
| `person` | | | | | |
| `face` | | | | | |

Mẫu `person` dựng theo người quay mặt về camera (các điểm `left_*` nằm bên phải khung mẫu)? Có / Không

Cách đổi cờ `occluded` / `outside` cho **một điểm**: rê chuột vào điểm rồi nhấn `Q` để đổi `occluded`, hoặc nhấn `O` để đổi `outside` (theo `docs/CVAT_CHEATSHEET.md`; cần tự kiểm trên phiên bản đang dùng).

## 2. Số lượng đã gán và thời gian (CP1, CP2)

| Nhóm ảnh | Số ảnh | Số skeleton đã gán | Số người dưới 60 px (không gán) | Số poster / gương / màn hình bỏ qua | Thời gian (phút) |
|---|---:|---:|---:|---:|---:|
| `easy` | 5 | | | | |
| `occluded` | 3 | | | | |
| `back` | 2 | | | | |
| `small` | 1 | | | | |
| `crowd` | 1 | | | | |
| `faces` | 8 | | — | | |

- Số ảnh người đã xong ở mốc phút 105: ___ / 10
- Thời gian thực tế (phút): CP1 ___ · CP2 ___ · CP3 ___
- Ảnh tốn thời gian nhất là ảnh nào, vì sao?

...

## 3. Bảng ca khó (CP1, CP2)

Mỗi điểm bạn phân vân một dòng, nhất là phân vân giữa `v = 1` và `v = 0`, hoặc không chắc hướng người.

| Ảnh | Người / mặt | Điểm | Cờ đã chọn | Phân vân giữa | Lý do chọn |
|---|---|---|---:|---|---|
| | | | | | |
| | | | | | |
| | | | | | |

## 4. Bảng tự review (CP3)

Đi từ ảnh cuối về ảnh đầu. 5 ảnh người (ít nhất 2 ảnh `back` hoặc `crowd`) và 3 ảnh mặt. Ít nhất 8 dòng, kể cả dòng `ok`. Ghi lỗi trước, sửa sau.

Mã lỗi dùng đúng một trong: `lr_swap`, `vis_flag`, `position`, `missing`, `extra`, `ok`.

| Ảnh | Người / mặt | Điểm | Mã lỗi | Ghi chú | Đã sửa? |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |
| | | | | | |
| | | | | | |
| | | | | | |
| | | | | | |
| | | | | | |
| | | | | | |

Tổng hợp số lỗi theo mã:

| `lr_swap` | `vis_flag` | `position` | `missing` | `extra` | `ok` |
|---:|---:|---:|---:|---:|---:|
| | | | | | |

Điểm còn phân vân giữa `v = 1` và `v = 0` (ghi cả hai lựa chọn và lý do chọn):

...

## 5. Kiểm file xuất và kết quả tự kiểm (CP4)

Tự kiểm tay trong file JSON:

| File | Người / mặt kiểm (ảnh, thứ tự) | Số phần tử `keypoints` | Điểm `outside` ra `v = 0`, `occluded` ra `v = 1`? | `num_keypoints` khớp? |
|---|---|---:|---|---|
| `HoVaTen_persons.zip` | | | | |
| `HoVaTen_persons.zip` | | | | |
| `HoVaTen_faces.zip` | | | | |

Sau khi xuất, CVAT ghi `occluded` thành `v = ___` và `outside` thành `v = ___`. Tọa độ của điểm `outside` trong file là `0, 0` hay tọa độ cũ? ___

Hai job đã chuyển sang completed trên CVAT? Có / Không

Dán phần **TÓM TẮT** in ra từ `src/check_submission.py`:

```text
- File person: NguyenVanHoa_persons.zip
  Số ảnh: 12 · số skeleton `person`: 17 · mỗi annotation 51 số
  Skeleton theo ảnh: 000000078170=2, 000000090646=1, 000000175703=1, 000000253584=1, 000000294329=1, 000000294379=1, 000000307757=2, 000000311300=2, 000000413160=2, 000000429594=1, 000000508269=1, 000000521817=2
  Cờ v: v=2 214 (74%) · v=1 23 (8%) · v=0 52 (18%)
  num_keypoints trung bình: 13.9
- File face: NguyenVanHoa_faces.zip
  Số ảnh: 8 · số skeleton `face`: 8 · mỗi annotation 39 số
  Skeleton theo ảnh: face_255797=1, face_3348=1, face_359139=1, face_362568=1, face_442231=1, face_483667=1, face_79591=1, face_81239=1
  Cờ v: v=2 96 (92%) · v=1 0 (0%) · v=0 8 (8%)
  num_keypoints trung bình: 12.0
- Ghi chú: 60 điểm v = 0 vẫn mang tọa độ cũ (CVAT 2.x xuất như vậy; chuẩn COCO ghi 0, 0). Không phải lỗi: điểm v = 0 bị bỏ qua khi huấn luyện và khi chấm.
- Số [LỖI]: 1 · số [CẢNH BÁO]: 5
Kết quả: CHƯA ĐẠT (1 lỗi). Sửa trên CVAT rồi xuất lại.
```

Kết quả trên phản ánh hai file export hiện có, chưa phải kết quả cuối. Cần kiểm tra 5 cảnh báo trên CVAT và ghi lý do thực tế sau khi kiểm; hiện chưa thể kết luận cảnh báo nào được giữ nguyên. Lỗi cần sửa: ảnh `000000521817.jpg`, người #2, `left_knee` có `v = 2` nhưng nằm ngoài ảnh. Sửa trong CVAT và xuất lại, không sửa JSON bằng tay.

## 6. Ảnh chụp màn hình

1. Label `person` trong label constructor (đủ 17 điểm có tên):

   ![Label person](images/1_label_person.png)

2. Một người quay lưng đã gán, cờ đã đặt:

   ![Người quay lưng](<images/Screenshot 2026-11-12 183959.png>)

3. Một khuôn mặt đã gán 13 điểm, phóng to vùng mắt:

   ![Khuôn mặt](<images/Screenshot 2026-11-12 184224.png>)

4. Một đoạn JSON xuất của một người:

   ![JSON export](<images/Screenshot 2026-11-12 185006.png>)

Nguồn ảnh: COCO 2017; thông tin nguồn từng ảnh xem `src/lab/NGUON_ANH.md`. Các ảnh hiện có cần kiểm tra lại mức phóng to và nội dung theo yêu cầu; ảnh label constructor vẫn cần bổ sung.

## 7. Tự đánh giá

1. Lỗi bạn mắc nhiều nhất hôm nay, và cách bạn sẽ tránh ở dự án thật:

   ...

2. Một quy tắc bạn đề xuất thêm vào guideline (kèm ảnh ví dụ nếu có):

   ...

3. Nhãn của bạn đi vào model ở đâu? Chọn một lỗi bạn đã sửa và nói nó sẽ làm model học sai thế nào (heatmap, trọng số trong loss, hay bước lật ảnh):

   ...

## 8. Khó khăn và lỗi kỹ thuật

...

## Bonus (nếu làm)

### B1 — 3 ảnh người khó thêm

| Ảnh | Số skeleton | Số người dưới 60 px | Ca khó nhất |
|---|---:|---:|---|
| | | | |
| | | | |
| | | | |

Kết quả `src/check_submission.py` cho `HoVaTen_bonus_persons.zip`:

```text
(dán ở đây)
```

### B2 — 5 ảnh khuôn mặt đen trắng / hồng ngoại

Ảnh không màu khó hơn ở điểm nào? Kính râm trên ảnh hồng ngoại có còn là `v = 1` không?

...

### B3 — Model so với nhãn của tôi (không tính điểm)

- Demo đã dùng:
- Ảnh đã thử:

1. Model có trả điểm cho khớp bị che, hay khớp ngoài ảnh không? Confidence ở các điểm đó thế nào?

   ...

2. Với người quay lưng, model có đổi trái/phải không?

   ...

3. Bộ điểm của model có giống 17 điểm COCO không?

   ...

## 9. Tài liệu tham khảo và công cụ AI đã dùng

- Tài liệu của lab: `README.md`, `docs/GUIDELINE.md`, `docs/CVAT_CHEATSHEET.md`, `docs/COCO_KEYPOINTS.md` và `SUBMISSION.md`.
- Hermes Agent (trợ lý AI): hỗ trợ kiểm tra file nộp, giải thích kết quả script và điền các thông tin có thể đối chiếu; không thực hiện thay bảng ca khó, tự review hoặc tự đánh giá.
