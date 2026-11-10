# Báo cáo tiến độ – Tuần 3

- **Sinh viên:** Phạm Tuấn Khoa – MSSV 110124095 – Lớp DA24TTC
- **Đề tài:** Tìm hiểu mô hình Decision Tree (DT) và ứng dụng
- **GVHD:** ThS. Ngô Thanh Huy
- **Thời gian:** 09/11/2026 – 22/11/2026

## 1. Công việc đã thực hiện
- Vẽ cây quyết định bằng `plot_tree`, in luật bằng `export_text`, tính mức độ quan trọng của thuộc tính (`feature_importances_`).
- So sánh tiêu chí tách gini và entropy (tập kiểm tra và kiểm tra chéo 10-fold).
- Khảo sát max_depth từ 1 đến 15, vẽ đồ thị độ chính xác huấn luyện / kiểm tra / CV 5-fold để quan sát quá khớp.
- Khảo sát min_samples_leaf (1, 2, 5, 10, 20) và cắt tỉa theo độ phức tạp chi phí (ccp_alpha) trên Breast Cancer.
- Chọn tham số bằng GridSearchCV (224 tổ hợp, 5-fold, F1-macro).
- Viết Chương 3 (Hiện thực hóa nghiên cứu): môi trường, dữ liệu, tiền xử lý, quy trình và cài đặt.
- Làm notebook demo `src/demo_decision_tree.ipynb` chạy trên Google Colab: giải thích từng bước dự đoán, thử trực tiếp với tập Iris bằng thanh trượt.

## 2. Kết quả đạt được
- Thuộc tính quan trọng nhất: petal length (Iris), flavanoids và color_intensity (Wine), worst perimeter (Breast Cancer).
- Gini và entropy cho kết quả tương đương khi đánh giá bằng 10-fold.
- Độ chính xác kiểm tra cao nhất ở max_depth = 3 trên cả ba tập; sâu hơn chỉ làm tăng độ chính xác huấn luyện.
- Cắt tỉa ccp_alpha: cây Breast Cancer giảm từ 19 xuống 5–9 nút lá, độ chính xác kiểm tra tăng từ 0,901 lên 0,918.
- Tham số tốt nhất: Iris (gini, max_depth = 3), Wine (gini, max_depth = 3, ccp_alpha = 0,02), Breast Cancer (entropy, max_depth = 3, min_samples_leaf = 10).
- Các hình và bảng kết quả nằm trong `src/figures` và `src/results`; báo cáo cập nhật: `thesis/doc/BaoCao_DACSN_PhamTuanKhoa_DecisionTree.docx` (đã thêm Chương 3).

## 3. Khó khăn, vướng mắc
- Tập kiểm tra nhỏ (45 mẫu với Iris) nên mỗi mẫu dự đoán sai làm độ chính xác thay đổi khoảng 0,022; vì vậy cần thêm kiểm tra chéo để kết luận chắc chắn hơn.

## 4. Kế hoạch tuần tiếp theo (23/11 – 06/12/2026)
- Đánh giá mô hình tốt nhất bằng precision, recall, F1, ma trận nhầm lẫn, ROC–AUC.
- So sánh với Logistic Regression bằng kiểm tra chéo 10-fold.
- Viết Chương 4, Chương 5, tóm tắt; hoàn thiện báo cáo.
