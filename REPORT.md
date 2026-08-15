# Báo cáo kết quả training và inference trên CPU

1. Mô hình LightGBM được huấn luyện trên 227.845 mẫu dữ liệu giao dịch, với thời gian training là **2,083 giây**.
2. Thời gian đọc dữ liệu là **1,784 giây**, cho thấy bước chuẩn bị dữ liệu chiếm thời gian tương đương quá trình huấn luyện.
3. Mô hình đạt **AUC-ROC = 0,902379**, thể hiện khả năng phân biệt giao dịch gian lận và hợp lệ khá tốt.
4. Accuracy đạt **0,977301**, còn Recall đạt **0,867347**, phù hợp với bài toán phát hiện gian lận cần hạn chế bỏ sót mẫu dương tính.
5. Precision chỉ đạt **0,062271** và F1-Score **0,1162**, cho thấy vẫn còn nhiều cảnh báo dương tính giả do dữ liệu mất cân bằng.
6. Inference một dòng có độ trễ khoảng **1,189 ms**, phù hợp cho các yêu cầu dự đoán đơn lẻ trên CPU.
7. Với batch 1.000 dòng, throughput đạt khoảng **687.509 dòng/giây**, cho thấy tốc độ inference trên CPU rất tốt.
8. Nhìn chung, mô hình có chất lượng phân loại tốt và tốc độ xử lý nhanh; có thể cải thiện precision bằng cách tinh chỉnh threshold hoặc xử lý mất cân bằng dữ liệu.
