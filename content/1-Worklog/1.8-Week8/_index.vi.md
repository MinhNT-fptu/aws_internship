---
title: "Worklog Tuần 8"
date: "2026-07-11"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Tìm hiểu hệ thống cơ sở dữ liệu trên AWS: RDS, Aurora, Redshift, ElastiCache.
* Thực hành xây dựng database subnet group, test kết nối, backup & restore.
* Tìm hiểu các dịch vụ phân tích dữ liệu như Kinesis, Glue, Athena, QuickSight.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                  | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                                                             |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - Tìm hiểu về Database: RDS, Aurora, Redshift, ElastiCache <br> - Tìm hiểu về kiến trúc multi-AZ, read replica, backup/restore                                                                                                                                                                                                             | 07/07/2026   | 07/07/2026      | <https://youtu.be/OOD2RwWuLRw?si=9JsOs0PNfO1TdAUl> <br><br> <https://youtu.be/qbrobQZrokY?si=ePJjzYXWg3qE_Ca6> <br><br> <https://youtu.be/UvdiRW34aNI?si=8g3FwgsJ3VLT-_nf> |
| 3   | - **Thực hành:** <br>&emsp; + Create VPC + SG cho EC2 + RDS <br>&emsp; + Create DB subnet group <br>&emsp; + Deploy EC2 <br>&emsp; + Tạo RDS instance + Backup & Restore                                                                                                                                                                   | 08/07/2026   | 08/07/2026      | <https://000005.awsstudygroup.com>                                                                                                                                         |
| 4   | - **Thực hành:** <br>&emsp; + Kết nối MSSQL/Oracle <br>&emsp; + Schema Conversion <br>&emsp; + Create DMS Task <br>&emsp; + Inspect logs, troubleshoot                                                                                                                                                                                     | 09/07/2026   | 09/07/2026      | <https://000043.awsstudygroup.com>                                                                                                                                         |
| 5   | - Tìm hiểu tổng quan về Data Analytics (Kinesis, Glue, Athena, QuickSight) <br> - **Thực hành:** <br>&emsp; + Create DynamoDB table <br>&emsp; + Enable autoscaling <br>&emsp; + CRUD test <br>&emsp; Create Global Table và dọn dẹp resources                                                                                             | 10/07/2026   | 10/07/2026      | <https://000039.awsstudygroup.com>                                                                                                                                         |
| 6   | - **Thực hành(lab35):** <br>&emsp; + Create S3 bucket <br>&emsp; + Create Kinesis Firehose ingestion + Glue crawler <br>&emsp; + Query dữ liệu bằng Athena + Create dashboard QuickSight <br> - **Thực hành(lab40):** <br>&emsp; + Kiểm tra cost allocation <br>&emsp; + CTagging resource <br>&emsp; + Query bổ sung và dọn dẹp Resources | 11/07/2026   | 11/07/2026      | <https://000035.awsstudygroup.com> <br><br> <https://000040.awsstudygroup.com>                                                                                             |


### Kết quả đạt được tuần 8:

* Tổng quát: 
  * Trong tuần này tôi tập trung học các dịch vụ database và data analytics trên AWS, bao gồm RDS, Aurora, DynamoDB, DMS, Kinesis, Glue, Athena và QuickSight. Tôi hiểu rõ kiến trúc triển khai database, cách kết nối, backup/restore, autoscaling cũng như pipeline phân tích dữ liệu đầu cuối từ ingestion -> ETL -> query -> visualization.

* Lý thuyết đã học:
  * Khái niệm về Kiến trúc của RDS, Aurora, Multi-AZ, read replicas
  * Backup, snapshot, parameter group, option group
  * DynamoDB: partition key, sort key, throughput, autoscaling, DAX
  * Tổng quan Data Analytics: Kinesis Firehose, Glue crawler, Athena, QuickSight
  * Kiến thức về Database Migration: schema conversion, DMS task

  
* Thực hành với bài lab:
  * Tạo VPC + security group riêng cho EC2/RDS
  * Tạo DB subnet group, deploy EC2 và RDS MySQL
  * Backup & Restore database
  * Kết nối MSSQL/Oracle, thực hành Schema Conversion & tạo DMS task
  * Tạo DynamoDB table, bật autoscaling, CRUD test, tạo Global Table và cleanup
  * Xây dựng pipeline: Kinesis Firehose -> S3, chạy Glue crawler, query dữ liệu bằng Athena và dựng dashboard trên QuickSight.
  * Thực hành các tác vụ bổ sung: tagging, cost allocation và cleanup