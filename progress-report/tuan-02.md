# Báo cáo tiến độ – Tuần 2

- **Sinh viên:** Phạm Tuấn Khoa – MSSV 110124095 – Lớp DA24TTC
- **Đề tài:** Tìm hiểu mô hình Decision Tree (DT) và ứng dụng
- **GVHD:** ThS. Ngô Thanh Huy
- **Thời gian:** 26/10/2026 – 08/11/2026

## 1. Công việc đã thực hiện
- Tìm hiểu và so sánh ba thuật toán ID3, C4.5, CART (độ đo chọn thuộc tính, kiểu thuộc tính xử lý, số nhánh mỗi nút, cách cắt tỉa); xác định scikit-learn cài đặt phiên bản tối ưu của CART.
- Tìm hiểu các tham số chính của `DecisionTreeClassifier`: criterion, max_depth, min_samples_split, min_samples_leaf, max_features, ccp_alpha, class_weight, random_state.
- Tính tay entropy, information gain, gain ratio và Gini trên tập "Chơi tennis" (14 mẫu); viết code kiểm chứng, kết quả trùng khớp (H(S) = 0,940; IG(Quang cảnh) = 0,247).
- Chọn 3 tập dữ liệu công khai: Iris (150 mẫu), Wine (178 mẫu), Breast Cancer Wisconsin (569 mẫu); khảo sát số mẫu, số thuộc tính, phân bố lớp, giá trị thiếu (không có).
- Tiền xử lý: đảo nhãn Breast Cancer để lớp dương là malignant; chia 70% huấn luyện / 30% kiểm tra có phân tầng, random_state = 42.
- Huấn luyện thử mô hình với tham số mặc định trên cả ba tập.
- Viết quyển báo cáo: Chương 1 (Tổng quan) và Chương 2 (Cơ sở lý thuyết).

## 2. Kết quả đạt được
- Bảng so sánh ID3/C4.5/CART và bảng tham số (Bảng 2.3, 2.4 trong báo cáo).
- Mô hình mặc định: độ chính xác huấn luyện 1,000 trên cả ba tập; kiểm tra 0,933 (Iris), 0,963 (Wine), 0,901 (Breast Cancer) → có dấu hiệu quá khớp, sẽ khảo sát ở tuần 3.
- File: `thesis/doc/BaoCao_DACSN_PhamTuanKhoa_DecisionTree.docx` (Chương 1, 2).

## 3. Khó khăn, vướng mắc
- scikit-learn chỉ tạo cây nhị phân và cần thuộc tính dạng số, nên cây trên tập "Chơi tennis" (sau khi mã hóa one-hot) khác cây ID3 tính tay; đã tìm hiểu nguyên nhân và ghi nhận để trình bày trong báo cáo.

## 4. Kế hoạch tuần tiếp theo (09/11 – 22/11/2026)
- Vẽ cây quyết định, xem các luật rẽ nhánh và mức độ quan trọng của thuộc tính.
- Thử các cấu hình tham số: criterion, max_depth, min_samples_leaf, ccp_alpha; ghi lại kết quả.
- Viết Chương 3 (Hiện thực hóa nghiên cứu).
