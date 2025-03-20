# Dự án Dự đoán giá cổ phiếu từ dữ liệu VNDIRECT
## Giới thiệu dự án 
- Dự án này tập trung vào việc thu thập dữ liệu giá cổ phiếu từ API của VNDIRECT dưới dạng chuỗi thời gian (time series), sau đó xử lý và xây dựng mô hình dự đoán nhằm hỗ trợ việc phân tích xu hướng và đưa ra nhận định cho nhà đầu tư.
## Mục tiêu
- Thu thập dữ liệu giá cổ phiếu lịch sử  
- Phân tích xu hướng, mùa vụ và biến động giá  
- Xây dựng mô hình dự báo giá tương lai dựa trên dữ liệu quá khứ  
- Trực quan hóa kết quả và so sánh giữa mô hình
## Dữ liệu
- Nguồn: API VNDIRECT
- Dữ liệu thu thập:
    - Mã cổ phiếu
    - Ngày giao dịch
    - Giá mở cửa, đóng cửa, giá cao nhất, giá thấp nhất, khối lượng giao dịch
 
## Quy trình thực hiện
- ***Thu thập***
- Sử dụng `requests` để truy vấn API VNDIRECT
- Lưu trữ dữ liệu thành file
- **Xử lý dữ liệu:**  
  - Làm sạch dữ liệu (loại bỏ ngày nghỉ, ngày không giao dịch)  
  - Chuyển đổi dữ liệu về định dạng chuỗi thời gian
- **Phân tích dữ liệu:**  
  - Vẽ biểu đồ đường thể hiện xu hướng giá  
  - Phân tích biến động và seasonality  
- **Xây dựng mô hình:**  
  - Thử nghiệm mô hình ARIMA để dự báo giá ngắn hạn  
  - Xây dựng mô hình LSTM để dự báo dài hạn với dữ liệu nhiều ngày liên tiếp  
- **Trực quan hóa:**  
  - So sánh giá trị dự đoán và giá trị thực tế trên biểu đồ  
  - Matplot trình bày diễn biến giá theo thời gian và dự báo
## kết quả
 - Mô hình LSTM chính xác ***85%*** trên tập kiểm nghiệm
 - ARIMA cho dự báo ngắn hạn với sai số nhỏ trong khoảng 3–5%
 - Biểu đồ so sánh giữa giá dự đoán và giá thực tế trực quan, dễ theo dõi
