# Tìm hiểu mô hình Decision Tree (DT) và ứng dụng

Đồ án cơ sở ngành, Khoa Công nghệ Thông tin, Trường Đại học Trà Vinh.

- Sinh viên: Phạm Tuấn Khoa
- MSSV: 110124095
- Lớp: DA24TTC
- Email: khoap1808@gmail.com
- Số điện thoại: 0919099079
- Giảng viên hướng dẫn: ThS. Ngô Thanh Huy
- Thời gian: 12/10/2026 đến 06/12/2026

## Giới thiệu

Đồ án tìm hiểu mô hình cây quyết định (Decision Tree): cách cây được xây dựng, cách chọn thuộc tính để tách bằng entropy, information gain và chỉ số Gini, các thuật toán ID3, C4.5, CART. Sau đó em dùng Python và thư viện scikit-learn để huấn luyện, vẽ cây và đánh giá mô hình trên một số tập dữ liệu có sẵn.

## Công cụ

Python 3, Jupyter Notebook hoặc Google Colab, các thư viện scikit-learn, pandas, numpy, matplotlib.

## Các thư mục

- `src`: mã nguồn (notebook)
- `progress-report`: báo cáo tiến độ từng tuần
- `thesis/doc`: quyển báo cáo file Word
- `thesis/pdf`: quyển báo cáo file PDF
- `thesis/refs`: tài liệu tham khảo
- `setup`: hướng dẫn cài đặt

## Cách chạy

Cách đơn giản nhất là mở file notebook trong thư mục `src` bằng Google Colab rồi chọn Runtime > Run all.

Nếu chạy trên máy thì cài thư viện rồi mở Jupyter:

```
git clone https://github.com/KHOA1808/csn-da24ttc-phamtuankhoa-decisiontree.git
cd csn-da24ttc-phamtuankhoa-decisiontree
pip install -r requirements.txt
jupyter notebook
```

## Dữ liệu

Dùng 3 tập dữ liệu công khai có sẵn trong scikit-learn (nguồn gốc từ kho UCI), không cần tải về:

- Iris: 150 mẫu, 4 thuộc tính, 3 lớp
- Wine: 178 mẫu, 13 thuộc tính, 3 lớp
- Breast Cancer Wisconsin: 569 mẫu, 30 thuộc tính, 2 lớp

## Tiến độ

| Tuần | Thời gian | Công việc | Trạng thái |
|---|---|---|---|
| 1 | 12/10 - 25/10 | Tìm tài liệu, cài môi trường, tạo repository | Hoàn thành |
| 2 | 26/10 - 08/11 | ID3, C4.5, CART, tính tay, chọn dữ liệu | Đang làm |
| 3 | 09/11 - 22/11 | Huấn luyện, vẽ cây, thử tham số | Chưa làm |
| 4 | 23/11 - 06/12 | Đánh giá, so sánh, hoàn thiện báo cáo | Chưa làm |
