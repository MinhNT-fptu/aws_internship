---
title: "Worklog Tuần 9"
date: "2026-07-18"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Tìm hiểu các dịch vụ AWS phục vụ việc triển khai frontend, backend, lưu trữ dữ liệu và giám sát hệ thống.
* Tìm hiểu cách tổ chức hạ tầng mạng và bảo mật cho ứng dụng trên AWS.
* Phân tích luồng kết nối giữa ứng dụng triển khai trên AWS với MongoDB Atlas.
* Tìm hiểu và vẽ sơ đồ architecture tổng thể phù hợp với dự án.
* Tìm hiểu phương án giám sát hoạt động và kiểm soát chi phí AWS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------- |
| 2   | - Tìm hiểu kiến trúc tổng thể của hệ thống trên AWS. <br> - Tìm hiểu các dịch vụ triển khai frontend: Route 53, CloudFront, S3 Frontend và ACM. <br> - Phân tích luồng truy cập từ người dùng đến frontend thông qua Route 53 và CloudFront. <br> - Tìm hiểu cách sử dụng ACM để cung cấp chứng chỉ SSL/TLS cho hệ thống.                                                                                                                                                                                                           | 14/07/2026   | 14/07/2026      |                |
| 3   | - Tìm hiểu các thành phần mạng trên AWS: VPC, Public Subnet và Internet Gateway. <br> - Tìm hiểu cách sử dụng Security Group để kiểm soát lưu lượng truy cập đến EC2. <br> - Tìm hiểu vai trò của Elastic IP trong việc cung cấp địa chỉ IP public cố định cho EC2. <br> - Phân tích mô hình triển khai backend trên EC2 trong Public Subnet.                                                                                                                                                                                       | 15/07/2026   | 15/07/2026      |                |
| 4   | - Tìm hiểu cách sử dụng S3 Receipts để lưu trữ ảnh hóa đơn và các tệp do người dùng tải lên. <br> - Tìm hiểu IAM Role và cách cấp quyền cho EC2 truy cập S3 mà không cần lưu Access Key trực tiếp trong source code. <br> - Phân tích luồng upload và truy xuất ảnh giữa frontend, backend EC2 và S3 Receipts. <br> - Tìm hiểu phương án kết nối backend trên EC2 với MongoDB Atlas.                                                                                                                                                | 16/07/2026   | 16/07/2026      |                |
| 5   | - Tìm hiểu dịch vụ CloudWatch để theo dõi metrics, logs và trạng thái hoạt động của EC2. <br> - Tìm hiểu cách sử dụng SNS để gửi thông báo khi hệ thống xảy ra lỗi hoặc vượt ngưỡng cảnh báo. <br> - Tìm hiểu AWS Budgets để theo dõi và cảnh báo chi phí sử dụng AWS. <br> - Phân tích phương án kết hợp CloudWatch, SNS và AWS Budgets trong hệ thống.                                                                                                                                                                            | 17/07/2026   | 17/07/2026      |                |
| 6   | - **Thực hành thiết kế architecture:** <br>&emsp; + Xác định các thành phần chính của hệ thống. <br>&emsp; + Vẽ luồng truy cập frontend qua Route 53, CloudFront và S3 Frontend. <br>&emsp; + Vẽ luồng request từ frontend đến backend trên EC2. <br>&emsp; + Thể hiện kết nối giữa EC2, S3 Receipts và MongoDB Atlas. <br>&emsp; + Bổ sung IAM Role, Security Group và các thành phần bảo mật. <br>&emsp; + Bổ sung CloudWatch, SNS và AWS Budgets vào sơ đồ. <br> - Kiểm tra và hoàn thiện sơ đồ architecture tổng thể của dự án. | 18/07/2026   | 18/07/2026      |                |

### Kết quả đạt được tuần 9:

* Tổng quát:
  * Trong tuần này, tôi tập trung tìm hiểu và xây dựng architecture triển khai dự án trên AWS.
  * Kiến trúc bao gồm các thành phần phục vụ phân phối frontend, triển khai backend, lưu trữ ảnh hóa đơn, kết nối cơ sở dữ liệu, giám sát hệ thống và quản lý chi phí.
  * Tôi đã hiểu được luồng hoạt động tổng thể của hệ thống, từ khi người dùng truy cập ứng dụng cho đến khi request được backend xử lý và dữ liệu được lưu trữ tại các dịch vụ liên quan.

* Lý thuyết đã học:
  * Route 53 được sử dụng để quản lý tên miền và định tuyến người dùng đến hệ thống.
  * CloudFront được sử dụng để phân phối nội dung frontend thông qua hệ thống CDN.
  * S3 Frontend được sử dụng để lưu trữ các tệp tĩnh của ứng dụng frontend.
  * ACM được sử dụng để quản lý chứng chỉ SSL/TLS và hỗ trợ truy cập hệ thống thông qua HTTPS.
  * VPC, Public Subnet và Internet Gateway tạo môi trường mạng cho các tài nguyên AWS.
  * Security Group kiểm soát các kết nối vào và ra khỏi EC2.
  * Elastic IP cung cấp địa chỉ IP public cố định cho EC2.
  * EC2 được sử dụng để triển khai và vận hành backend của dự án.
  * S3 Receipts được sử dụng để lưu trữ ảnh hóa đơn và các tệp do người dùng tải lên.
  * IAM Role cho phép EC2 truy cập các dịch vụ AWS khác mà không cần lưu thông tin xác thực trực tiếp trong source code.
  * MongoDB Atlas được sử dụng làm hệ thống cơ sở dữ liệu và được kết nối với backend trên EC2.
  * CloudWatch hỗ trợ theo dõi metrics, logs và trạng thái hoạt động của hệ thống.
  * SNS hỗ trợ gửi thông báo khi có cảnh báo hoặc sự cố.
  * AWS Budgets hỗ trợ theo dõi và cảnh báo khi chi phí AWS đạt đến một ngưỡng nhất định.

* Thực hành thiết kế architecture:
  * Xác định và phân nhóm các thành phần frontend, backend, storage, database, monitoring và cost management.
  * Xây dựng luồng truy cập frontend: User → Route 53 → CloudFront → S3 Frontend.
  * Xây dựng luồng xử lý backend: Frontend → Elastic IP → EC2.
  * Thiết kế EC2 nằm trong Public Subnet thuộc VPC và kết nối Internet thông qua Internet Gateway.
  * Sử dụng Security Group để giới hạn các cổng và nguồn được phép truy cập EC2.
  * Thiết kế luồng backend upload và truy xuất ảnh hóa đơn từ S3 Receipts thông qua IAM Role.
  * Thể hiện kết nối giữa backend trên EC2 và MongoDB Atlas.
  * Bổ sung CloudWatch để thu thập metrics và logs của EC2.
  * Bổ sung SNS để gửi thông báo khi phát hiện sự cố hoặc vượt ngưỡng cảnh báo.
  * Bổ sung AWS Budgets để giám sát và kiểm soát chi phí sử dụng dịch vụ.
  * Hoàn thiện sơ đồ architecture tổng thể phục vụ việc triển khai dự án trên AWS.
