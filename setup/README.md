# Hướng dẫn cài đặt môi trường

## Yêu cầu
- Python 3.9 trở lên
- pip

## Cài đặt trên máy cá nhân

1. Kiểm tra Python: `python --version`
2. (Khuyến nghị) Tạo môi trường ảo:
   ```bash
   python -m venv venv
   # Windows
   venv\Scripts\activate
   # macOS / Linux
   source venv/bin/activate
   ```
3. Cài thư viện từ thư mục gốc của repository:
   ```bash
   pip install -r requirements.txt
   ```
4. Mở Jupyter Notebook: `jupyter notebook`, sau đó mở notebook trong thư mục `src/`.

## Chạy trên Google Colab

Google Colab đã có sẵn scikit-learn, pandas, NumPy và Matplotlib nên không cần cài thêm. Tải notebook trong `src/` lên Colab (*File → Upload notebook*) rồi chọn *Runtime → Run all*.

## Dữ liệu

Các tập dữ liệu dùng trong đồ án là dữ liệu công khai có sẵn trong scikit-learn hoặc tải từ UCI Machine Learning Repository, nên không cần tải thủ công. Kết quả có thể chạy lại giống nhau nhờ cố định tham số `random_state`.
