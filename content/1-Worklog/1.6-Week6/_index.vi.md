---
title: "Worklog Tuần 6"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---


### Mục tiêu tuần 6:

* Hiểu rõ khái niệm và lợi ích của mô hình kiến trúc Không máy chủ (Serverless).
* Lập trình, kiểm thử và triển khai các hàm AWS Lambda.
* Công khai các hàm Lambda ra bên ngoài thông qua Amazon API Gateway.
* Cấu hình kích hoạt (trigger) hàm Lambda chạy tự động dựa trên sự kiện của S3 bucket.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 4 | - Tìm hiểu mô hình Serverless và dịch vụ FaaS AWS Lambda, phân biệt với mô hình truyền thống sử dụng máy chủ ảo EC2. | 27/05/2026 | 27/05/2026 | [Serverless on AWS Details](https://aws.amazon.com/serverless/) |
| 5 | - Thực hành tạo và triển khai Lambda Function cơ bản (Python/Node.js). Tìm hiểu biến môi trường và cách debug qua CloudWatch Logs. | 28/05/2026 | 28/05/2026 | [AWS Lambda Dev Guide](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html) |
| 6 | - Thực hành kết nối Lambda với Amazon S3 Event Trigger: Tự động chạy xử lý ảnh/dữ liệu khi có tệp tin được upload lên S3. | 29/05/2026 | 29/05/2026 | [S3 Event Trigger Tutorial](https://docs.aws.amazon.com/lambda/latest/dg/with-s3.html) |
| 2 | - Nghiên cứu dịch vụ Amazon API Gateway. Hiểu các tùy chọn thiết lập HTTP API và REST API. | 01/06/2026 | 01/06/2026 | [API Gateway Overview Guide](https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html) |
| 3 | - Thực hành xây dựng API Gateway liên kết trực tiếp với Lambda Function để làm backend API. Sử dụng Postman để kiểm thử API endpoint. | 02/06/2026 | 02/06/2026 | [API Gateway with Lambda Integration](https://docs.aws.amazon.com/apigateway/latest/developerguide/getting-started-with-lambda-integration.html) |


### Kết quả đạt được tuần 6:

* Hiểu rõ mô hình tính phí theo số lượng lượt gọi (pay-per-request) và tối ưu chi phí của Serverless.
* Xây dựng thành công luồng xử lý tự động theo sự kiện (event-driven) khi upload file lên S3.
* Thiết lập thành công API Gateway làm cổng kết nối bảo mật cho các hàm backend Lambda.
