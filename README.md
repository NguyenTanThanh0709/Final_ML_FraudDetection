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
- step:
Một bước ánh xạ một đơn vị thời gian tới thế giới thực. Trong tập dữ liệu này, 1 bước là 1 giờ
của thời gian. Có tổng cộng 743 bước mô phỏng 30 ngày.
- Có 5 loại giao dịch khác nhau:
• PAYMENT - Khi khách hàng thanh toán để mua hàng hóa hoặc dịch vụ từ
một thương gia, giao dịch được gọi là Thanh toán. Nó làm giảm
số dư tài khoản của người gửi trong khi số dư tài khoản của người nhận
tăng lên (tức là số tiền được ghi có vào tài khoản của anh ấy).
• TRANSFER - Khi một người dùng gửi tiền cho người dùng khác thông qua
nền tảng dịch vụ tiền di động, giao dịch được gọi là Chuyển khoản.
CASH_OUT - Người bán đóng vai trò là máy ATM cho khách hàng và
khách hàng có thể giảm số dư tài khoản bằng cách rút
tiền mặt từ các thương gia.
• CASH_IN - Người bán đóng vai trò là máy ATM cho khách hàng và
khách hàng có thể tăng số dư tài khoản bằng cách thanh toán bằng tiền mặt
tới các thương gia.
• DEBIT - Khi khách hàng gửi tiền từ dịch vụ mobile money
vào tài khoản ngân hàng, giao dịch được gọi là Ghi nợ. Nó giảm
số dư trong tài khoản giống như giao dịch CASH_OUT
- amount
Số tiền giao dịch bằng nội tệ.
- nameOrig
Tên của tài khoản đã thực hiện giao dịch.
- oldbalanceOrg
Số dư ban đầu của người gửi.
- newbalanceOrig
Số dư mới của người gửi.
- nameDest
Tên tài khoản đã nhận giao dịch.
- oldbalanceDest
Số dư ban đầu của người nhận trước khi giao dịch.
- newbalanceDest
Số dư mới của người nhận sau khi giao dịch.
- isFraud
Nếu giao dịch được xác định là gian lận (1) hoặc không lừa đảo (0).
- isFlaggedFraud
Gắn cờ các giao dịch đáng ngờ là gian lận khi người dùng cố gắng trái phép
chuyển hơn 200,00 trong một giao dịch.

# Kỹ thuật
- Kỹ thuật dữ liệu mất cân bằng:
Như đã đề cập trước đó, tập dữ liệu rất mất cân bằng và sẽ
phải được sửa đổi để mô hình đưa ra dự đoán chính xác.
Chỉ có 0,13% giao dịch lừa đảo và 99,87% giao dịch thật
giao dịch. Dữ liệu mất cân bằng đề cập đến một vấn đề phân loại trong đó
các lớp không được đại diện như nhau. Với sự mất cân bằng giai cấp thiểu số
mô hình có thể hoàn toàn bỏ qua và kết quả sẽ không chính xác.
Dữ liệu sẽ phải được lấy mẫu quá mức, lấy mẫu dưới mức hoặc lớp
trọng số phải được thay đổi để mô hình có độ chính xác
phỏng đoán.
- Kỹ thuật SMOTE được sử dụng trong dự án này để có thể cân bằng tập dữ liệu.
Thật không may, việc lấy mẫu quá mức ngẫu nhiên sẽ dẫn đến việc mô hình bị trang bị quá mức,
làm cho nó không chính xác trong việc dự đoán dữ liệu thực tế trong khi ngẫu nhiên
việc lấy mẫu dưới mức sẽ loại bỏ phần lớn các giao dịch thực sự và
các mô hình sẽ được đào tạo lại.

