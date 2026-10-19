# Tìm hiểu mô hình Decision Tree (DT) và ứng dụng

Đồ án cơ sở ngành – Khoa Công nghệ Thông tin, Trường Kỹ thuật và Công nghệ, Trường Đại học Trà Vinh.

| | |
|---|---|
| **Sinh viên thực hiện** | Phạm Tuấn Khoa |
| **MSSV** | 110124095 |
| **Lớp** | DA24TTC |
| **Email** | khoap1808@gmail.com |
| **Điện thoại** | 0919099079 |
| **Giảng viên hướng dẫn** | ThS. Ngô Thanh Huy |
| **Thời gian thực hiện** | 12/10/2026 – 06/12/2026 |

## Giới thiệu

Decision Tree (cây quyết định) là mô hình học máy có giám sát biểu diễn quá trình ra quyết định thành một cây gồm các câu hỏi về giá trị thuộc tính. Nhờ vậy, người dùng có thể lần theo từng nhánh để biết vì sao mô hình đưa ra một dự đoán. Đồ án tìm hiểu nguyên lý hoạt động của Decision Tree (entropy – information gain, Gini impurity, các thuật toán ID3, C4.5, CART), sau đó cài đặt và thử nghiệm mô hình bằng Python trên một số tập dữ liệu công khai để đánh giá hiệu quả và khả năng ứng dụng.

## Mục tiêu

- Nắm được khái niệm, cấu trúc cây và nguyên lý xây dựng cây quyết định.
- Hiểu và tự tính được entropy, information gain, Gini impurity trên một tập dữ liệu nhỏ.
- So sánh các thuật toán ID3, C4.5, CART; tìm hiểu các tham số chính của `DecisionTreeClassifier`.
- Huấn luyện, trực quan hóa và thử nhiều cấu hình tham số trên 2–3 tập dữ liệu công khai.
- Đánh giá bằng accuracy, precision, recall, F1-score, ma trận nhầm lẫn, ROC–AUC và k-fold; đối chiếu với một mô hình cơ sở.

## Công nghệ sử dụng

- Python 3, Jupyter Notebook / Google Colab
- scikit-learn, pandas, NumPy, Matplotlib

## Cấu trúc thư mục

```
csn-da24ttc-phamtuankhoa-decisiontree/
├── README.md            # Giới thiệu và hướng dẫn chạy lại đồ án
├── requirements.txt     # Danh sách thư viện cần cài
├── setup/               # Hướng dẫn cài đặt môi trường
├── src/                 # Mã nguồn (notebook Python)
├── progress-report/     # Báo cáo tiến độ hằng tuần
└── thesis/              # Tài liệu văn bản của đồ án
    ├── doc/             # Quyển báo cáo dạng .docx
    ├── pdf/             # Quyển báo cáo dạng .pdf
    ├── html/            # Tài liệu dạng web (nếu có)
    ├── abs/             # Slide thuyết trình, video demo
    └── refs/            # Tài liệu tham khảo
```

## Hướng dẫn chạy lại

**Cách 1 – Google Colab (không cần cài đặt):** mở file notebook trong thư mục `src/` bằng Google Colab rồi chọn *Runtime → Run all*.

**Cách 2 – Chạy trên máy cá nhân:**

```bash
git clone https://github.com/KHOA1808/csn-da24ttc-phamtuankhoa-decisiontree.git
cd csn-da24ttc-phamtuankhoa-decisiontree
pip install -r requirements.txt
jupyter notebook
```

Sau đó mở notebook trong thư mục `src/`. Chi tiết xem thêm trong [setup/README.md](setup/README.md).

## Dữ liệu

Đồ án chỉ sử dụng các tập dữ liệu công khai, không dùng thông tin cá nhân thật. Danh sách tập dữ liệu và nguồn sẽ được cập nhật khi hoàn tất bước khảo sát dữ liệu.

## Tiến độ

| Tuần | Thời gian | Nội dung | Trạng thái |
|---|---|---|---|
| 1 | 12/10 – 25/10/2026 | Tìm tài liệu, cài môi trường, tạo repository | Hoàn thành |
| 2 | 26/10 – 08/11/2026 | ID3, C4.5, CART, tham số; tính tay; chọn và tiền xử lý dữ liệu | Chưa bắt đầu |
| 3 | 09/11 – 22/11/2026 | Huấn luyện, vẽ cây, thử cấu hình tham số | Chưa bắt đầu |
| 4 | 23/11 – 06/12/2026 | Đánh giá, so sánh mô hình cơ sở, hoàn thiện báo cáo | Chưa bắt đầu |

Báo cáo tiến độ chi tiết từng tuần nằm trong thư mục [progress-report/](progress-report/).

## Liên hệ

Phạm Tuấn Khoa – khoap1808@gmail.com – 0919099079
