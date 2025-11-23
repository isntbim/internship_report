---
title: "Worklog Tuần 4"
date: "'r Sys.Date()'"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---



### Mục tiêu tuần 4:

* Học cách cấu hình cơ sở dữ liệu Amazon RDS với thiết lập VPC, security groups và thao tác backup.
* Nghiên cứu triển khai ứng dụng web có khả năng mở rộng bằng Auto Scaling Groups và Application Load Balancers.
* Hiểu các kỹ thuật giám sát với CloudWatch metrics, logs, alarms và dashboards.
* Khám phá giải pháp DNS lai (Hybrid) bằng Route 53 Resolver cho mạng doanh nghiệp.
* Phát triển kỹ năng AWS CLI để quản lý tài nguyên tự động trên S3, EC2, VPC và IAM.
* Thực hành xây dựng pipeline CI/CD với CodeCommit, CodeBuild, CodeDeploy và CodePipeline.
* Triển khai chiến lược backup tự động bằng AWS Backup với lifecycle policies.
* Học triển khai ứng dụng container hoá với Docker trên AWS và container registries.
* Nghiên cứu quy trình migrate VM bao gồm thao tác import/export giữa các môi trường.
* Xây dựng ứng dụng serverless bằng AWS Lambda và API Gateway với cấu hình IAM.
* Hiểu giám sát bảo mật bằng AWS Security Hub với tích hợp đa dịch vụ.

### Các công việc thực hiện trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| ------------ | --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - **Cấu hình và quản trị cơ sở dữ liệu quan hệ với Amazon RDS:** <br>&emsp; + Tạo VPC, security groups cho EC2 và RDS, và DB subnet group <br>&emsp; + Khởi tạo EC2 instance và tạo RDS database instance <br>&emsp; + Triển khai ứng dụng mẫu trên EC2 instance để kết nối tới RDS database <br>&emsp; + Thực hiện các thao tác backup và restore cho RDS instance <br>&emsp; + Thực hành resource cleanup bằng cách xoá các tài nguyên đã tạo <br><br> - **Triển khai và cấu hình ứng dụng web có khả năng mở rộng bằng Auto Scaling:** <br>&emsp; + Thiết lập hạ tầng mạng cần thiết, bao gồm VPC, subnets và security groups <br>&emsp; + Tạo EC2 Launch Template để định nghĩa cấu hình cho các instance mới <br>&emsp; + Cấu hình Target Group và Application Load Balancer để quản lý và phân phối lưu lượng vào <br>&emsp; + Tạo và cấu hình Auto Scaling Group để tự động quản lý số lượng EC2 instances <br>&emsp; + Kiểm thử các phương án scaling bao gồm manual, scheduled và dynamic scaling policies <br>&emsp; + Dọn dẹp toàn bộ AWS resources đã tạo để tránh phát sinh chi phí <br><br> - **Giám sát và phân tích tài nguyên AWS với CloudWatch:** <br>&emsp; + Khám phá và phân tích metrics từ các dịch vụ AWS bằng search và math expressions <br>&emsp; + Điều tra và truy vấn log data bằng CloudWatch Logs Insights <br>&emsp; + Tạo Metric Filter để trích xuất dữ liệu từ log events phục vụ giám sát <br>&emsp; + Cấu hình CloudWatch Alarm để kích hoạt thông báo dựa trên ngưỡng metric xác định <br>&emsp; + Xây dựng CloudWatch Dashboard tuỳ biến để trực quan hoá các metrics và alarms <br>&emsp; + Dọn dẹp toàn bộ tài nguyên đã tạo, bao gồm alarms và dashboards | 29/09/2025 | 29/09/2025 | Amazon RDS: <br> <https://000005.awsstudygroup.com/> <br> Auto Scaling Group: <br> <https://000006.awsstudygroup.com/> <br> CloudWatch Metrics <br> <https://000008.awsstudygroup.com/> |
| 3   | - **Triển khai giải pháp DNS lai (Hybrid) với Route 53 Resolver:** <br>&emsp; + Chuẩn bị môi trường lab bằng cách triển khai hạ tầng nền tảng với CloudFormation template <br>&emsp; + Triển khai Microsoft Active Directory để mô phỏng DNS server on-premises <br>&emsp; + Tạo Route 53 Resolver outbound endpoint để chuyển tiếp truy vấn DNS từ VPC <br>&emsp; + Cấu hình Route 53 Resolver rules để điều hướng truy vấn DNS đến resolver phù hợp <br>&emsp; + Thiết lập Route 53 Resolver inbound endpoint để mạng on-premises có thể truy vấn tài nguyên VPC <br>&emsp; + Kiểm thử phân giải tên DNS hybrid và dọn dẹp toàn bộ tài nguyên đã triển khai <br><br> - **Quản lý dịch vụ AWS bằng Command Line Interface (CLI):** <br>&emsp; + Cài đặt và cấu hình AWS CLI với access key, secret key và default region <br>&emsp; + Luyện tập sử dụng CLI để xem và mô tả tài nguyên ở các dịch vụ như S3, SNS và IAM <br>&emsp; + Thực hiện các thao tác Amazon S3 như tạo bucket và quản lý objects qua dòng lệnh <br>&emsp; + Tạo và quản lý các thành phần VPC, bao gồm Internet Gateway, bằng các lệnh CLI <br>&emsp; + Khởi tạo, mô tả và huỷ Amazon EC2 instance hoàn toàn bằng dòng lệnh <br>&emsp; + Dọn dẹp toàn bộ tài nguyên tạo trong lab để tránh chi phí | 30/09/2025 | 30/09/2025 | Route 53 Resolver: <br> <https://cloudjourney.awsstudygroup.com/> <br> AWS CLI: <br> <https://000011.awsstudygroup.com/> |
| 4   | - **Xây dựng pipeline CI/CD để tự động hoá triển khai ứng dụng:** <br>&emsp; + Tạo kho mã nguồn (version control repository) bằng AWS CodeCommit để lưu source code ứng dụng <br>&emsp; + Cấu hình build project với AWS CodeBuild để compile, test và package ứng dụng <br>&emsp; + Thiết lập application và deployment group trong AWS CodeDeploy để quản lý quá trình triển khai <br>&emsp; + Tạo pipeline CI/CD hợp nhất với AWS CodePipeline để điều phối toàn bộ quy trình <br>&emsp; + Kiểm thử end-to-end pipeline bằng cách đẩy một thay đổi mã và xác minh triển khai tự động <br>&emsp; + Dọn dẹp toàn bộ tài nguyên AWS tạo trong lab để tránh chi phí không cần thiết <br><br> - **Tự động hoá backup EC2 instance với AWS Backup:** <br>&emsp; + Triển khai hạ tầng cần thiết, bao gồm VPC mới và EC2 instance, bằng CloudFormation template <br>&emsp; + Tạo backup plan trong AWS Backup để định nghĩa tần suất, retention policies và lifecycle rules <br>&emsp; + Cấu hình thông báo để nhận alert về trạng thái các backup jobs <br>&emsp; + Kiểm thử quy trình backup và restore để bảo đảm có thể phục hồi dữ liệu <br>&emsp; + Dọn dẹp toàn bộ tài nguyên, bao gồm CloudFormation stack và các bản backup đã tạo | 01/10/2025 | 01/10/2025 | AWS IAM Identity Center: <br> <https://000012.awsstudygroup.com/> <br> AWS Backup: <br> <https://000013.awsstudygroup.com/> |
| 5   | - **Triển khai ứng dụng Dockerized trên AWS:** <br>&emsp; + Cấu hình hạ tầng AWS cần thiết, bao gồm VPC, security groups và IAM roles <br>&emsp; + Khởi tạo Amazon RDS instance để làm database cho ứng dụng <br>&emsp; + Thiết lập EC2 instance và cài đặt các phụ thuộc cần thiết để chạy ứng dụng <br>&emsp; + Triển khai và kiểm thử ứng dụng trên EC2 instance bằng Docker image <br>&emsp; + Triển khai lại ứng dụng bằng Docker Compose để quản lý nhiều containers <br>&emsp; + Push Docker image lên container registry như Amazon ECR hoặc Docker Hub <br>&emsp; + Dọn dẹp toàn bộ tài nguyên AWS đã tạo để tránh phát sinh chi phí <br><br> - **Migrate Virtual Machine đến và từ AWS:** <br>&emsp; + Export một virtual machine từ môi trường on-premises <br>&emsp; + Tải image virtual machine đã export lên Amazon S3 bucket <br>&emsp; + Import virtual machine từ S3 vào AWS để tạo Amazon Machine Image (AMI) mới <br>&emsp; + Khởi tạo EC2 instance mới từ AMI đã import <br>&emsp; + Export một EC2 instance hiện có trở lại S3 bucket <br>&emsp; + Dọn dẹp toàn bộ tài nguyên đã tạo, bao gồm S3 bucket và EC2 instance | 02/10/2025 | 02/10/2025 | Docker on AWS: <br> <https://000015.awsstudygroup.com/> <br> VM Import/Export: <br> <https://000014.awsstudygroup.com/> |
| 6   | - **Triển khai ứng dụng serverless với Lambda và API Gateway:** <br>&emsp; + Chuẩn bị và zip gói triển khai (deployment package) cho Lambda, bảo đảm bao gồm source code của function và mọi dependencies cần thiết <br>&emsp; + Định nghĩa và tạo IAM role với execution permissions cần thiết và trust policy cho phép Lambda assume role <br>&emsp; + Tạo Lambda function trên AWS Console, chỉ định runtime và upload gói triển khai đã zip <br>&emsp; + Xây dựng HTTP API endpoint bằng Amazon API Gateway và cấu hình integration để gọi Lambda function <br>&emsp; + Triển khai API Gateway ra một stage và kiểm thử end-to-end ứng dụng serverless qua URL công khai <br>&emsp; + Dọn dẹp toàn bộ tài nguyên liên quan, bao gồm API Gateway, Lambda function và IAM role để tránh chi phí <br><br> - **Tổng hợp và ưu tiên các phát hiện bảo mật với AWS Security Hub:** <br>&emsp; + Kích hoạt AWS Security Hub để bắt đầu tổng hợp dữ liệu bảo mật từ nhiều dịch vụ AWS <br>&emsp; + Xem dashboard tích hợp để trực quan hoá các cảnh báo và phát hiện bảo mật <br>&emsp; + Tổ chức và ưu tiên các phát hiện từ các dịch vụ như Amazon GuardDuty, Inspector và Macie <br>&emsp; + Khám phá các rủi ro được tóm tắt qua các biểu đồ và bảng tương tác | 03/10/2025 | 03/10/2025 | AWS Lambda: <br> <https://000016.awsstudygroup.com/> <br> AWS Security Hub: <br> <https://000018.awsstudygroup.com/> |


### Kết quả đạt được tuần 4:

* Đã cấu hình và quản trị thành công Amazon RDS databases:
  * Thiết lập VPC với cấu hình security groups
  * Tạo DB subnet group và tích hợp EC2-RDS
  * Triển khai ứng dụng với kết nối database
  * Thực hiện backup và restore operations

* Đã triển khai ứng dụng web có khả năng mở rộng bằng hạ tầng Auto Scaling:
  * Thiết lập hạ tầng mạng với VPC, subnets và security groups
  * Cấu hình EC2 Launch Template cho chuẩn hoá instances
  * Triển khai Application Load Balancer và Target Group
  * Cấu hình Auto Scaling Group với scaling policies

* Đã triển khai giám sát toàn diện với CloudWatch services:
  * Khám phá metrics với search và math expressions
  * Phân tích log data bằng CloudWatch Logs Insights
  * Cấu hình alarms tuỳ chỉnh với ngưỡng thông báo
  * Xây dựng dashboard tương tác để trực quan hoá

* Đã cấu hình giải pháp DNS lai với Route 53 Resolver:
  * Triển khai hạ tầng bằng CloudFormation
  * Tích hợp Microsoft Active Directory để mô phỏng
  * Cấu hình outbound và inbound endpoints
  * Kiểm thử phân giải tên 2 chiều

* Đã phát triển kỹ năng AWS CLI cho quản lý tài nguyên tự động:
  * Cài đặt và cấu hình CLI với thông tin truy cập
  * Quản lý đa dịch vụ (S3, SNS, IAM)
  * Thao tác S3 gồm quản lý bucket và object
  * Quản lý vòng đời EC2 instance qua CLI

* Đã xây dựng pipeline CI/CD tự động bằng các dịch vụ AWS:
  * Thiết lập repository với AWS CodeCommit
  * Cấu hình build project bằng AWS CodeBuild
  * Tự động hoá triển khai bằng AWS CodeDeploy
  * Điều phối end-to-end với CodePipeline

* Đã triển khai chiến lược backup tự động với AWS Backup:
  * Triển khai hạ tầng bằng CloudFormation templates
  * Tạo backup plan với lifecycle policies
  * Cấu hình thông báo giám sát backup jobs
  * Kiểm thử khôi phục qua quy trình backup

* Đã triển khai ứng dụng container hoá bằng Docker trên AWS:
  * Cấu hình hạ tầng AWS gồm VPC và IAM roles
  * Tích hợp RDS cho ứng dụng containerized
  * Triển khai và kiểm thử Docker image trên EC2
  * Vận hành container registry với Amazon ECR

* Đã hoàn tất quy trình migrate VM giữa các môi trường:
  * Export virtual machine từ hệ thống on-premises
  * Lưu trữ và truyền image qua S3
  * Import VM để tạo AMI
  * Khởi tạo EC2 từ images đã import

* Đã xây dựng ứng dụng serverless bằng AWS Lambda và API Gateway:
  * Chuẩn bị và cấu hình deployment package cho Lambda
  * Tạo IAM role với execution permissions
  * Triển khai function và cấu hình runtime
  * Tạo endpoint API Gateway và tích hợp Lambda

* Đã cấu hình giám sát bảo mật tập trung với AWS Security Hub:
  * Kích hoạt Security Hub để gom dữ liệu đa dịch vụ
  * Sử dụng dashboard để trực quan cảnh báo
  * Tổ chức findings từ GuardDuty, Inspector, Macie
  * Phân tích rủi ro qua biểu đồ và bảng tương tác
