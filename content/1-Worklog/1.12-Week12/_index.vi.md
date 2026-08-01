---
title: "Worklog Tuần 12"
date: "2026-08-06"
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu tuần 12:

* Nghiên cứu và thiết kế kiến trúc AWS phục vụ môi trường phát triển và kiểm thử của dự án.
* Xác định luồng kết nối giữa frontend, backend, hệ thống lưu trữ và MongoDB Atlas.
* Triển khai frontend và backend của dự án lên AWS theo kiến trúc đã thiết kế.
* Thiết lập các thành phần mạng, bảo mật, quản lý thông tin bí mật và phân quyền truy cập.
* Cấu hình hệ thống giám sát, cảnh báo và theo dõi chi phí sử dụng tài nguyên AWS.
* Kiểm tra hoạt động của hệ thống sau khi triển khai trên môi trường AWS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------- |
| 2   | - Phân tích yêu cầu triển khai dự án trên môi trường AWS phục vụ dev/test. <br> - Xác định các thành phần chính của hệ thống gồm S3 Frontend Bucket, S3 Receipts Bucket, VPC, Public Subnet, Internet Gateway, EC2, Elastic IP và MongoDB Atlas. <br> - Phân tích luồng truy cập từ người dùng đến frontend và backend. <br> - Lựa chọn AWS Region `ap-southeast-1` để triển khai tài nguyên.                                                                                                                                                                                    | 01/08/2026   | 01/08/2026      |                |
| 3   | - Nghiên cứu và vẽ sơ đồ architecture tổng thể cho môi trường dev/test. <br>&emsp; + Thiết kế frontend được lưu trữ trên S3 Frontend Bucket. <br>&emsp; + Thiết kế backend được triển khai trên EC2 trong Public Subnet. <br>&emsp; + Kết nối Public Subnet với Internet Gateway. <br>&emsp; + Gán Elastic IP cho EC2 để cung cấp địa chỉ IP public cố định. <br>&emsp; + Thiết kế S3 Receipts Bucket để lưu trữ ảnh hóa đơn. <br>&emsp; + Thể hiện kết nối giữa backend trên EC2 và MongoDB Atlas. <br> - Rà soát và hoàn thiện sơ đồ architecture trước khi triển khai.        | 02/08/2026   | 02/08/2026      |                |
| 4   | - Triển khai hạ tầng mạng và backend trên AWS. <br>&emsp; + Tạo VPC và Public Subnet. <br>&emsp; + Tạo và kết nối Internet Gateway với VPC. <br>&emsp; + Cấu hình route table để Public Subnet có thể kết nối Internet. <br>&emsp; + Tạo Web Security Group và giới hạn các cổng được phép truy cập. <br>&emsp; + Khởi tạo EC2 và gán Elastic IP. <br>&emsp; + Cấu hình môi trường chạy backend trên EC2. <br>&emsp; + Deploy source code backend và kiểm tra API.                                                                                                               | 03/08/2026   | 03/08/2026      |                |
| 5   | - Triển khai frontend và hệ thống lưu trữ trên AWS. <br>&emsp; + Tạo S3 Frontend Bucket để lưu trữ các tệp build của frontend. <br>&emsp; + Build và upload source code frontend lên S3. <br>&emsp; + Tạo S3 Receipts Bucket để lưu trữ ảnh hóa đơn của người dùng. <br>&emsp; + Tạo IAM Role và cấp quyền cần thiết để EC2 truy cập S3 Receipts Bucket. <br>&emsp; + Sử dụng Secrets Manager để quản lý các thông tin nhạy cảm của backend. <br>&emsp; + Cấu hình kết nối từ EC2 đến MongoDB Atlas. <br> - Kiểm tra luồng frontend gọi API backend và luồng upload ảnh hóa đơn. | 04/08/2026   | 04/08/2026      |                |
| 6   | - Cấu hình hệ thống quản lý, giám sát và cảnh báo. <br>&emsp; + Sử dụng CloudWatch để theo dõi EC2 metrics và logs của backend. <br>&emsp; + Thiết lập cảnh báo CloudWatch cho các chỉ số cần theo dõi. <br>&emsp; + Kết nối CloudWatch với SNS để gửi thông báo khi có cảnh báo. <br>&emsp; + Thiết lập AWS Budgets để theo dõi và cảnh báo chi phí sử dụng AWS. <br> - Kiểm tra toàn bộ hệ thống sau khi triển khai. <br> - Ghi nhận các lỗi phát sinh, thực hiện sửa lỗi và hoàn thiện tài liệu triển khai.                                                                   | 05/08/2026   | 05/08/2026      |                |

### Kết quả đạt được tuần 12:

* Tổng quát:
  * Trong tuần này, tôi tập trung nghiên cứu, thiết kế và triển khai kiến trúc AWS phục vụ môi trường phát triển và kiểm thử của dự án.
  * Tôi đã hoàn thiện sơ đồ architecture thể hiện các thành phần frontend, backend, storage, database, network, security, monitoring và cost management.
  * Frontend và backend của dự án đã được triển khai lên AWS theo kiến trúc đã thiết kế.
  * Hệ thống đã có thể kết nối với MongoDB Atlas, lưu trữ ảnh hóa đơn trên S3 và được theo dõi thông qua CloudWatch.

* Kiến trúc đã thiết kế:
  * Sử dụng AWS Region `ap-southeast-1` để triển khai các tài nguyên.
  * Sử dụng S3 Frontend Bucket để lưu trữ các tệp tĩnh của frontend.
  * Sử dụng S3 Receipts Bucket để lưu trữ ảnh hóa đơn và các tệp do người dùng tải lên.
  * Triển khai backend trên EC2 nằm trong Public Subnet của VPC.
  * Sử dụng Internet Gateway để cho phép các tài nguyên trong Public Subnet kết nối Internet.
  * Sử dụng Elastic IP để cung cấp địa chỉ IP public cố định cho EC2.
  * Sử dụng Web Security Group để kiểm soát inbound và outbound traffic của EC2.
  * Kết nối backend trên EC2 với MongoDB Atlas.
  * Sử dụng IAM Role để cấp quyền cho EC2 truy cập các dịch vụ AWS cần thiết.
  * Sử dụng Secrets Manager để quản lý thông tin nhạy cảm của ứng dụng.
  * Sử dụng CloudWatch, SNS và AWS Budgets để giám sát hoạt động và chi phí của hệ thống.

* Các công việc triển khai đã hoàn thành:
  * Tạo VPC, Public Subnet, Internet Gateway và route table.
  * Tạo và cấu hình Security Group cho backend.
  * Khởi tạo EC2 và gán Elastic IP.
  * Cấu hình môi trường và deploy backend lên EC2.
  * Tạo S3 Frontend Bucket và triển khai frontend lên S3.
  * Tạo S3 Receipts Bucket phục vụ lưu trữ ảnh hóa đơn.
  * Tạo IAM Role và cấp quyền để EC2 truy cập S3.
  * Thiết lập thông tin cấu hình và thông tin nhạy cảm cho backend.
  * Kết nối backend với MongoDB Atlas.
  * Kiểm tra luồng frontend gửi request đến backend.
  * Kiểm tra chức năng upload và truy xuất ảnh hóa đơn từ S3.
  * Cấu hình CloudWatch để thu thập metrics và logs.
  * Kết nối cảnh báo CloudWatch với SNS.
  * Thiết lập AWS Budgets để theo dõi chi phí.

* Luồng hoạt động của hệ thống:
  * Người dùng truy cập frontend được triển khai trên S3 Frontend Bucket.
  * Frontend gửi API request đến backend thông qua Elastic IP của EC2.
  * Internet Gateway hỗ trợ kết nối giữa EC2 trong Public Subnet và Internet.
  * Backend xử lý nghiệp vụ và kết nối đến MongoDB Atlas để truy xuất hoặc lưu dữ liệu.
  * Backend sử dụng IAM Role để upload và truy xuất ảnh hóa đơn từ S3 Receipts Bucket.
  * Thông tin nhạy cảm của ứng dụng được quản lý thông qua Secrets Manager.
  * CloudWatch thu thập metrics và logs từ EC2.
  * SNS gửi thông báo khi hệ thống phát sinh cảnh báo.
  * AWS Budgets theo dõi và cảnh báo khi chi phí đạt đến ngưỡng đã thiết lập.

* Kiến thức và kinh nghiệm đạt được:
  * Hiểu rõ hơn quy trình thiết kế architecture cho môi trường dev/test trên AWS.
  * Có thêm kinh nghiệm triển khai frontend tĩnh trên Amazon S3.
  * Có thêm kinh nghiệm triển khai backend trên EC2 và cấu hình mạng trong VPC.
  * Hiểu cách sử dụng Internet Gateway, route table, Elastic IP và Security Group.
  * Biết cách sử dụng IAM Role để cấp quyền cho EC2 mà không lưu Access Key trong source code.
  * Hiểu cách quản lý thông tin nhạy cảm bằng Secrets Manager.
  * Có thêm kinh nghiệm kết nối ứng dụng trên AWS với MongoDB Atlas.
  * Biết cách sử dụng CloudWatch và SNS để giám sát và gửi cảnh báo.
  * Hiểu cách sử dụng AWS Budgets để theo dõi và kiểm soát chi phí.
  * Có thêm kinh nghiệm kiểm tra và xử lý lỗi sau khi triển khai dự án lên môi trường AWS.