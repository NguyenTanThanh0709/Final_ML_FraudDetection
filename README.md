# Final_ML_FraudDetection
# Mục tiêu:
Mục tiêu chính của phân tích này là phát triển một mô hình phân loại mạnh mẽ có khả năng dự đoán chính xác liệu một giao dịch trực tuyến cụ thể có phải là gian lận hay không. Tận dụng các đặc trưng được cung cấp trong bộ dữ liệu, mục tiêu là huấn luyện một mô hình máy học có khả năng phân biệt giữa các giao dịch hợp lệ và gian lận.

# Phương pháp:
Khám phá Dữ liệu (EDA):

Khám phá Dữ liệu (EDA) là một bước quan trọng trong quá trình phân tích dữ liệu. Nó bao gồm việc sử dụng các kỹ thuật thống kê và đồ họa để khám phá các đặc điểm của một bộ dữ liệu, hiểu cấu trúc cơ bản của nó và phát hiện các mô hình, xu hướng, mối quan hệ và ngoại lệ tiềm ẩn. EDA thường được thực hiện ở các giai đoạn đầu của một dự án khoa học dữ liệu hoặc máy học để có cái nhìn sâu sắc và thông báo cho các bước tiếp theo trong phân tích.

# Tiền xử lý dữ liệu:
Giải quyết bất kỳ giá trị thiếu hoặc giá trị bất thường nào trong tập dữ liệu. Mã hóa biến phân loại, nếu cần. Chuẩn hóa các đặc trưng số để đảm bảo sự đồng đều trong ảnh hưởng của chúng đối với mô hình.

# Xử lý Mất cân bằng:
Thực hiện các kỹ thuật để đối phó với sự mất cân bằng giữa các lớp, chẳng hạn như tăng cường lớp thiểu số (giao dịch gian lận) bằng các phương pháp như SMOTE hoặc giảm lớp đa số.

# Lựa chọn Mô hình:
Thử nghiệm với các thuật toán phân loại khác nhau như Logistic Regression, Random Forest, XGBoost, v.v. Sử dụng các phương pháp đánh giá phù hợp cho các bộ dữ liệu mất cân bằng, nhấn mạnh vào các phép đo như precision, recall, F1-score và ROC-AUC.

# Tinh chỉnh Siêu tham số:
Tiến hành tìm kiếm hệ thống cho các siêu tham số tối ưu bằng các kỹ thuật như GridSearchCV hoặc RandomizedSearchCV để cải thiện hiệu suất mô hình.

# Đánh giá Mô hình:
Đánh giá hiệu suất của mô hình đã được huấn luyện trên một tập dữ liệu kiểm tra riêng biệt. Đánh giá khả năng của mô hình trong việc phân loại chính xác các giao dịch gian lận trong khi giảm thiểu số lượng dương giả.

# Giải thích và Hiểu được:
Hướng tới một mô hình không chỉ có hiệu suất tốt mà còn có khả năng giải thích. Hiểu rõ về tầm quan trọng của mỗi đặc trưng trong quá trình ra quyết định.
