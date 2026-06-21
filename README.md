Link youtube : https://youtu.be/3SVeqzP0RiU?si=2AC7MHlJDM_wCrJm
# Phân tích và dự đoán xu hướng giá xăng RON95 tại Việt Nam
## Thông tin sinh viên

- Họ và tên : Ngô Thị Hiền 
- Mã sinh viên: K225480106014 
- Lớp: K58 KTP
- Môn học: Khoa học dữ liệu
- Giảng viên hướng dẫn: Thầy Nguyễn Văn Huy
- Đề tài: Phân tích và dự đoán xu hướng giá xăng RON95 tại Việt Nam
  ### Link trình bày :
## 1. Giới thiệu đề tài
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/f17dbebf-994c-4d8d-bee7-b9877145fd56" />

Đề tài thực hiện phân tích dữ liệu giá xăng RON95 tại Việt Nam trong giai đoạn 2018–2026. Mục tiêu chính là khai thác dữ liệu lịch sử để tìm ra các xu hướng biến động giá, xác định các mốc giá quan trọng, phân tích mối liên hệ giữa giá dầu Brent thế giới và giá xăng RON95 tại Việt Nam, đồng thời xây dựng mô hình dự đoán giá xăng RON95 trong tương lai.

Toàn bộ quá trình phân tích được thực hiện bằng Python trên Jupyter Notebook.

## 2. Bộ dữ liệu sử dụng

Bộ dữ liệu sử dụng trong đề tài:

**Vietnam Petroleum Price Dataset 2018–2026**

Nguồn dữ liệu:

https://www.kaggle.com/datasets/nhidoyen/vietnam-petroleum-price-dataset-20182026

File dữ liệu sử dụng:

```text
vn_fuel_price_2018_present.csv
```

Thông tin dữ liệu:

```text
Số dòng: 2946 bản ghi
Số cột: 22 trường dữ liệu
Thời gian dữ liệu: từ 08/05/2018 đến 31/05/2026
```

Các trường dữ liệu chính được sử dụng:

```text
date                    Ngày ghi nhận dữ liệu
ron95_retail_price      Giá bán lẻ xăng RON95
brent_usd_per_barrel    Giá dầu Brent thế giới
usd_vnd                 Tỷ giá USD/VND
is_adjustment_day       Ngày điều chỉnh giá
```

## 3. Công nghệ và thư viện sử dụng

Đề tài sử dụng các công nghệ và thư viện sau:

```text
Python
Jupyter Notebook
Pandas
NumPy
Matplotlib
Scikit-learn
```

Vai trò của các thư viện:

```text
Pandas: đọc, xử lý và phân tích dữ liệu dạng bảng
NumPy: hỗ trợ tính toán số học
Matplotlib: vẽ biểu đồ trực quan hóa dữ liệu
Scikit-learn: xây dựng mô hình hồi quy tuyến tính để dự đoán
```

## 4. Cấu trúc thư mục

Cấu trúc thư mục project:

```text
btl KHDL/
│
├── main_ron95.ipynb
├── vn_fuel_price_2018_present.csv
├── README.md
│
└── output_ron95/
    │
    ├── bang_01_gia_ron95_cao_nhat.csv
    ├── bang_02_gia_ron95_trung_binh_theo_thang.csv
    ├── bang_03_gia_ron95_trung_binh_theo_nam.csv
    ├── bang_04_tuong_quan_brent_ron95.csv
    ├── bang_05_bien_dong_gia_ron95.csv
    ├── bang_06_du_doan_gia_ron95_06_thang_cuoi_2027.csv
    ├── bang_07_phan_nhom_gia_ron95_theo_ngay.csv
    ├── bang_07_thong_ke_nhom_gia_ron95.csv
    │
    └── bieu_do/
        ├── bieu_do_01_gia_ron95_cao_nhat.png
        ├── bieu_do_02_gia_ron95_trung_binh_theo_thang.png
        ├── bieu_do_03_gia_ron95_trung_binh_theo_nam.png
        ├── bieu_do_04_tuong_quan_brent_ron95.png
        ├── bieu_do_04_so_sanh_xu_huong_brent_ron95.png
        ├── bieu_do_05_tat_ca_bien_dong_gia_ron95.png
        ├── bieu_do_06_chi_du_doan_gia_ron95_06_thang_cuoi_2027.png
        ├── bieu_do_07_so_ngay_theo_nhom_gia_ron95.png
        └── bieu_do_07_phan_nhom_gia_ron95_theo_thoi_gian.png
```

## 5. Quy trình thực hiện

Quy trình thực hiện chương trình gồm các bước chính:

```text
1. Đọc dữ liệu từ file CSV
2. Kiểm tra dữ liệu ban đầu
3. Tiền xử lý dữ liệu
4. Tạo các cột phục vụ phân tích
5. Phân tích dữ liệu theo 7 câu hỏi
6. Vẽ biểu đồ minh họa
7. Xuất bảng kết quả ra file CSV
8. Đưa ra nhận xét cho từng kết quả
```

Các cột được tạo thêm trong quá trình xử lý:

```text
gia_ron95    Giá xăng RON95 sử dụng cho phân tích
nam          Năm của bản ghi
thang        Tháng của bản ghi
nam_thang    Năm-tháng của bản ghi
```

## 6. Các câu hỏi phân tích

Đề tài tập trung trả lời 7 câu hỏi chính:

```text
Câu 1: Giá xăng RON95 cao nhất trong thời gian qua là ngày nào?

Câu 2: Tháng nào có giá xăng RON95 trung bình cao nhất?

Câu 3: Năm nào có giá xăng RON95 trung bình cao nhất và thấp nhất?

Câu 4: Giá dầu Brent thế giới có liên quan như thế nào đến giá xăng RON95 tại Việt Nam?

Câu 5: Giá xăng RON95 thay đổi mạnh nhất vào giai đoạn nào?

Câu 6: Dự đoán giá xăng RON95 trung bình trong 06 tháng cuối năm 2027?

Câu 7: Phân nhóm giá xăng RON95 thành thấp, trung bình và cao?
```

## 7. Kết quả chính

### Câu 1: Giá RON95 cao nhất
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/4e8ec8e8-46e6-4c9d-b6c9-2b9fd85d9cfa" />



Kết quả:

```text
Giá RON95 cao nhất: 32.873 VND/lít
Thời gian xuất hiện: từ 21/06/2022 đến 30/06/2022
Số ngày duy trì mức giá cao nhất: 10 ngày
```

Nhận xét:

```text
Đây là giai đoạn giá xăng RON95 đạt mức cao nhất trong bộ dữ liệu.
Năm 2022 là giai đoạn giá xăng tăng nổi bật.
```

### Câu 2: Giá trung bình theo tháng
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/b339c2b7-142d-425a-b145-f8facc05b05e" />

Kết quả:

```text
Tháng có giá RON95 trung bình cao nhất: tháng 3
Giá trung bình khoảng: 22.342 VND/lít

Tháng có giá RON95 trung bình thấp nhất: tháng 12
Giá trung bình khoảng: 20.701 VND/lít
```

Nhận xét:

```text
Giá RON95 trung bình có sự khác nhau giữa các tháng.
Việc phân tích theo tháng giúp nhận biết tháng nào thường có mức giá cao hơn.
```

### Câu 3: Giá trung bình theo năm
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/ffb60a8d-0986-416d-a401-f6153062521a" />

Kết quả:

```text
Năm có giá RON95 trung bình cao nhất: 2022
Giá trung bình khoảng: 26.361 VND/lít

Năm có giá RON95 trung bình thấp nhất: 2020
Giá trung bình khoảng: 16.127 VND/lít
```

Nhận xét:

```text
Năm 2022 là năm có giá xăng RON95 trung bình cao nhất.
Năm 2020 là năm có giá RON95 trung bình thấp nhất trong dữ liệu.
```

### Câu 4: Mối liên hệ giữa Brent và RON95
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/579b9736-915f-4705-8b5b-4d23cb56f4ca" />


Kết quả:

```text
Hệ số tương quan Pearson giữa Brent và RON95: khoảng 0,897
```

Nhận xét:

```text
Giá dầu Brent và giá xăng RON95 có mối liên hệ cùng chiều khá mạnh.
Khi giá dầu Brent tăng hoặc giảm, giá RON95 tại Việt Nam cũng thường có xu hướng thay đổi theo.
Tuy nhiên, giá RON95 trong nước còn phụ thuộc vào thuế, phí, tỷ giá USD/VND và kỳ điều chỉnh giá.
```

### Câu 5: Biến động giá RON95
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/66007b56-7c59-4a44-b9a0-cbfe0e3dce89" />


Kết quả:

```text
Ngày biến động mạnh nhất: 07/03/2026
Mức thay đổi: 4.707 VND/lít

Ngày tăng mạnh nhất: 07/03/2026
Mức tăng: 4.707 VND/lít

Ngày giảm mạnh nhất: 13/04/2020
Mức giảm: 4.273 VND/lít
```

Nhận xét:

```text
Giá RON95 có những giai đoạn biến động rõ rệt.
Các biến động thường xuất hiện vào các ngày điều chỉnh giá.
```

### Câu 6: Dự đoán giá RON95 trong 06 tháng cuối năm 2027

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/787ecfbc-5d42-4d74-875c-d74c153ab7bb" />

Kết quả dự đoán:

```text
Tháng 07/2027: khoảng 23.295 VND/lít
Tháng 08/2027: khoảng 22.793 VND/lít
Tháng 09/2027: khoảng 22.562 VND/lít
Tháng 10/2027: khoảng 22.418 VND/lít
Tháng 11/2027: khoảng 22.608 VND/lít
Tháng 12/2027: khoảng 22.088 VND/lít
```

Giá RON95 trung bình lịch sử:

```text
Khoảng 21.466 VND/lít
```

Nhận xét:

```text
Giá dự đoán trong 06 tháng cuối năm 2027 cao hơn mức trung bình lịch sử.
Kết quả dự đoán chỉ mang tính tham khảo vì giá xăng thực tế còn phụ thuộc vào nhiều yếu tố như giá dầu thế giới, tỷ giá, thuế phí và chính sách điều hành.
```

### Câu 7: Phân nhóm giá RON95

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/7a1a09c8-f9b8-4680-9cf4-9590337d2c27" />

Ngưỡng phân nhóm:

```text
Ngưỡng 33%: 20.465 VND/lít
Ngưỡng 66%: 22.342 VND/lít
```

Quy tắc phân nhóm:

```text
Giá thấp: giá <= 20.465 VND/lít
Giá trung bình: 20.465 < giá <= 22.342 VND/lít
Giá cao: giá > 22.342 VND/lít
```

Kết quả thống kê:

```text
Nhóm giá thấp: 1003 ngày, chiếm khoảng 34,05%
Nhóm giá trung bình: 963 ngày, chiếm khoảng 32,69%
Nhóm giá cao: 980 ngày, chiếm khoảng 33,27%
```

## 8. Cách chạy chương trình

### Bước 1: Tạo môi trường ảo

Mở terminal tại thư mục project và chạy:

```bash
python -m venv .venv
```

### Bước 2: Kích hoạt môi trường ảo

Trên Windows PowerShell:

```bash
.\.venv\Scripts\activate
```

### Bước 3: Cài đặt thư viện

```bash
pip install pandas numpy matplotlib scikit-learn jupyter notebook openpyxl
```

### Bước 4: Mở Jupyter Notebook

```bash
jupyter notebook
```

Sau đó mở file:

```text
main_ron95.ipynb
```

### Bước 5: Chạy toàn bộ chương trình

Trong Jupyter Notebook hoặc VS Code, chọn:

```text
Run All
```

## 9. Kết quả đầu ra

Sau khi chạy chương trình, kết quả được lưu trong thư mục:

```text
output_ron95
```

Bao gồm:

```text
Các bảng kết quả dạng CSV
Các biểu đồ trực quan dạng PNG
Các nhận xét hiển thị trực tiếp trong Notebook
```

## 10. Kết luận
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/660daffe-64b6-4bf8-9f2d-ff6e5a87ddf1" />

Đề tài đã hoàn thành việc phân tích và dự đoán xu hướng giá xăng RON95 tại Việt Nam. Chương trình đã xử lý được dữ liệu giá xăng dầu Việt Nam giai đoạn 2018–2026, trả lời được 7 câu hỏi phân tích chính, xuất được bảng kết quả và biểu đồ minh họa.

Kết quả cho thấy năm 2022 là giai đoạn giá RON95 tăng cao nổi bật. Giá dầu Brent có mối liên hệ cùng chiều khá mạnh với giá xăng RON95 tại Việt Nam. Ngoài ra, chương trình cũng đã xây dựng mô hình dự đoán giá RON95 trong 06 tháng cuối năm 2027 và phân nhóm giá thành ba mức: thấp, trung bình và cao.

## 11. Hạn chế và hướng phát triển

Hạn chế:

```text
Mô hình dự đoán còn đơn giản
Dữ liệu chưa cập nhật sau ngày 31/05/2026
Chưa xét đầy đủ các yếu tố như thuế, phí, cung cầu và chính sách điều hành giá
```

Hướng phát triển:

```text
Cập nhật thêm dữ liệu mới
Sử dụng mô hình dự đoán nâng cao hơn
Bổ sung thêm các biến đầu vào như thuế, phí, tỷ giá, giá dầu thế giới
Xây dựng dashboard trực quan để theo dõi giá xăng RON95
```

https://jupyter-notebook.readthedocs.io/
```
