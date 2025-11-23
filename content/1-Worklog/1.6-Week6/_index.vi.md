---
title: "Worklog Tuần 6"
date: "`r Sys.Date()`"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---



### Mục tiêu tuần 6:

* Học cách quản lý truy cập EC2 bằng IAM với resource tags và permission boundaries.
* Thiết lập và cấu hình công cụ giám sát gồm Grafana và AWS CloudWatch.
* Triển khai AWS Systems Manager cho patch management và chạy lệnh từ xa.
* Tối ưu EC2 theo right-sizing với AWS Compute Optimizer.
* Mã hóa dữ liệu S3 bằng AWS KMS và cấu hình audit logging.
* Phân tích chi phí và mức sử dụng bằng AWS Cost Explorer.
* Xây dựng data pipeline và data lake với S3, Kinesis, Glue, Athena và QuickSight.
* Tự động hoá provisioning hạ tầng bằng AWS CloudFormation templates.

### Các công việc thực hiện trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - **Quản lý truy cập EC2 bằng IAM với resource tags:** <br>&emsp; + Tạo IAM user cho bước chuẩn bị <br>&emsp; + Tạo custom IAM Policy để định nghĩa quyền cụ thể <br>&emsp; + Thiết lập IAM Role để user/dịch vụ có thể assume <br>&emsp; + Kiểm chứng policy bằng cách switch role và test truy cập <br><br> - **Getting started với Grafana (basic):** <br>&emsp; + Tạo VPC và Subnet cho môi trường mạng <br>&emsp; + Cấu hình Security Group kiểm soát inbound/outbound <br>&emsp; + Launch EC2 để host ứng dụng monitoring <br>&emsp; + Tạo IAM User và Role để truy cập tài nguyên AWS an toàn <br>&emsp; + Gán IAM Role cho EC2 instance <br>&emsp; + Cài đặt Grafana trên EC2 instance <br>&emsp; + Thiết lập monitoring dashboards trong Grafana | 13/10/2025 | 13/10/2025 | IAM services: <br> <https://000028.awsstudygroup.com/> <br> Grafana basic: <br> <https://000029.awsstudygroup.com/> |
| 3 | - **Giới hạn quyền với IAM Permission Boundary:** <br>&emsp; + Thực hiện các bước chuẩn bị cho bài lab <br>&emsp; + Tạo restriction policy để giới hạn quyền tối đa <br>&emsp; + Tạo IAM user mới với quyền hạn chế <br>&emsp; + Kiểm thử giới hạn của user để xác thực permission boundary <br><br> - **Quản lý patch và chạy lệnh với AWS Systems Manager:** <br>&emsp; + Tạo VPC và Subnet cho môi trường mạng <br>&emsp; + Launch EC2 Windows public <br>&emsp; + Tạo IAM Role với quyền cần thiết <br>&emsp; + Gán IAM Role cho EC2 instance <br>&emsp; + Cấu hình và dùng Patch Manager để xử lý patch <br>&emsp; + Dùng Run Command để thực thi lệnh trên servers | 14/10/2025 | 14/10/2025 | IAM Permission Boundary: <br> <https://000030.awsstudygroup.com/> <br> AWS Systems Manager: <br> <https://000031.awsstudygroup.com/> |
| 4 | - **Thực hành right-sizing cho Amazon EC2:** <br>&emsp; + Làm quen Amazon CloudWatch cho monitoring <br>&emsp; + Tạo và gắn IAM Role cho CloudWatch Agent <br>&emsp; + Cài đặt CloudWatch Agent trên EC2 instance <br>&emsp; + Dùng AWS Compute Optimizer để phân tích và tối ưu EC2 <br><br> - **Mã hóa dữ liệu at rest trên S3 với AWS KMS:** <br>&emsp; + Tạo các IAM policies, roles, groups, users cần thiết <br>&emsp; + Thiết lập KMS key <br>&emsp; + Tạo S3 bucket và upload dữ liệu <br>&emsp; + Cấu hình AWS CloudTrail để logging và Amazon Athena để truy vấn <br>&emsp; + Kiểm thử và chia sẻ dữ liệu đã mã hóa trên S3 | 15/10/2025 | 15/10/2025 | EC2 right-sizing: <br> <https://000032.awsstudygroup.com/> <br> S3 encryption with KMS: <br> <https://000033.awsstudygroup.com/> |
| 5 | - **Trực quan và phân tích chi phí với AWS Cost Explorer:** <br>&emsp; + Xem cost & usage theo service và account <br>&emsp; + Phân tích phạm vi/hiệu quả của Savings Plans & Reserved Instances <br>&emsp; + Đánh giá cost elasticity <br>&emsp; + Tạo custom reports cho EC2 instances <br>&emsp; + Dùng Cost Explorer để phân tích chi tiết <br>&emsp; + Rà soát chi phí data transfer cho kiến trúc phổ biến <br><br> - **Xây dựng data lake trên AWS:** <br>&emsp; + Tạo IAM Role và Policy cho quyền truy cập cần thiết <br>&emsp; + Thiết lập S3 bucket để lưu trữ dữ liệu <br>&emsp; + Tạo Kinesis Data Firehose delivery stream để thu thập dữ liệu <br>&emsp; + Dùng Glue Crawler để tạo data catalog <br>&emsp; + Thực hiện data transformation <br>&emsp; + Phân tích dữ liệu bằng Amazon Athena <br>&emsp; + Trực quan dữ liệu với Amazon QuickSight | 16/10/2025 | 17/10/2025 | AWS Cost Explorer: <br> <https://000034.awsstudygroup.com/> <br> Data lake on AWS: <br> <https://000035.awsstudygroup.com/> |
| 6 | - **Nghiên cứu AWS CloudWatch cho monitoring & observability:** <br>&emsp; + Khám phá CloudWatch Metrics: xem, tìm kiếm, dùng expressions <br>&emsp; + Làm việc với CloudWatch Logs, Logs Insights và Metric Filters <br>&emsp; + Cấu hình CloudWatch Alarms để gửi thông báo <br>&emsp; + Tạo CloudWatch Dashboards để trực quan dữ liệu <br><br> - **Tự động hạ tầng với AWS CloudFormation:** <br>&emsp; + Tạo IAM Users và Roles cho phần chuẩn bị <br>&emsp; + Phát triển CloudFormation template cơ bản để provision tài nguyên <br>&emsp; + Khám phá Custom Resources với Lambda <br>&emsp; + Sử dụng Mappings, StackSets và Drift Detection cho triển khai phức tạp | 17/10/2025 | 17/10/2025 | AWS CloudWatch: <br> <https://000036.awsstudygroup.com/> <br> AWS CloudFormation: <br> <https://000037.awsstudygroup.com/> |


### Kết quả đạt được tuần 6:

* Quản lý quyền truy cập EC2 qua IAM:
  * Cấu hình policy dựa trên tag để kiểm soát truy cập
  * Áp dụng permission boundary để giới hạn khả năng của user

* Thiết lập monitoring & observability:
  * Triển khai Grafana trên EC2 để tạo dashboards
  * Cấu hình CloudWatch Metrics, Logs và Alarms cho giám sát tài nguyên

* Ứng dụng AWS Systems Manager:
  * Dùng Patch Manager để cập nhật bản vá máy chủ
  * Thực thi lệnh từ xa trên nhiều instance với Run Command

* Tối ưu EC2 và quản trị chi phí:
  * Cài đặt CloudWatch Agent để thu thập metrics chi tiết
  * Phân tích cấu hình bằng AWS Compute Optimizer
  * Rà soát xu hướng chi phí với Cost Explorer

* Bảo mật lưu trữ với mã hóa:
  * Quản lý KMS key cho S3 encryption
  * Thiết lập CloudTrail và Athena cho audit logging và truy vấn

* Xây dựng pipeline data lake:
  * Cấu hình Kinesis Data Firehose để ingest dữ liệu streaming
  * Tạo data catalog với Glue Crawler
  * Phân tích với Athena và trực quan với QuickSight

* Tự động triển khai bằng CloudFormation:
  * Viết templates để provision tài nguyên
  * Khai thác Custom Resources (Lambda) và StackSets
