---
title: "Worklog Tuần 5"
date: "`r Sys.Date()`"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---



### Mục tiêu tuần 5:

* Triển khai networking nâng cao trên AWS với VPC Peering và Transit Gateway cho kết nối multi‑VPC.
* Triển khai ứng dụng full‑stack sử dụng EC2, RDS, Auto Scaling, và tích hợp CloudFront.
* Tạo giải pháp tối ưu chi phí kiểu serverless với AWS Lambda để tự động quản lý EC2.
* Xây dựng CI/CD pipelines bằng AWS Developer Tools cho tự động triển khai ứng dụng.
* Cấu hình hybrid cloud storage với AWS Storage Gateway để tích hợp on‑premises.
* Quản lý enterprise file systems với Amazon FSx và bảo vệ web applications bằng AWS WAF.
* Tổ chức tài nguyên AWS hiệu quả bằng Tags và Resource Groups phục vụ governance.
* Nâng cao kỹ năng với cả AWS Management Console và CLI.

### Các công việc thực hiện trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | ---------- | --------------- | -------------- |
| 2   | - **Thiết lập VPC Peering giữa hai VPC:** <br>&emsp; + Khởi tạo CloudFormation Template để tạo môi trường ban đầu <br>&emsp; + Tạo Security Groups để kiểm soát traffic tới các EC2 instances <br>&emsp; + Tạo EC2 instances ở mỗi VPC để kiểm tra kết nối <br>&emsp; + Cập nhật Network ACLs để cho phép traffic giữa các VPC đã peering <br>&emsp; + Tạo và chấp nhận kết nối VPC Peering <br>&emsp; + Cấu hình Route Tables để định tuyến traffic giữa các VPC đã peering <br>&emsp; + Bật Cross‑Peer DNS cho phân giải tên giữa các VPC <br><br> - **Triển khai kiến trúc mạng có khả năng mở rộng với AWS Transit Gateway:** <br>&emsp; + Tạo Key Pair để truy cập an toàn vào instances <br>&emsp; + Khởi tạo môi trường bằng CloudFormation Template <br>&emsp; + Tạo Transit Gateway đóng vai trò hub mạng trung tâm <br>&emsp; + Gắn các VPC vào Transit Gateway để cho phép giao tiếp <br>&emsp; + Cấu hình Transit Gateway Route Tables để kiểm soát luồng traffic <br>&emsp; + Cập nhật VPC Route Tables để định tuyến traffic qua Transit Gateway <br>&emsp; | 06/10/2025 | 06/10/2025      | VPC Peering: <br> <https://000019.awsstudygroup.com/> <br> AWS Transit Gateway: <br> <https://000020.awsstudygroup.com/> |
| 3   | - **Triển khai WordPress trên AWS Cloud:** <br>&emsp; + Chuẩn bị VPC và Subnets cho hạ tầng mạng <br>&emsp; + Tạo Security Groups cho EC2 và Database instances để kiểm soát truy cập <br>&emsp; + Launch một EC2 instance để host ứng dụng WordPress <br>&emsp; + Launch một Database instance sử dụng Amazon RDS cho cơ sở dữ liệu WordPress <br>&emsp; + Cài đặt và cấu hình WordPress trên EC2 instance <br>&emsp; + Triển khai Auto Scaling cho WordPress instance <br>&emsp; + Thực hiện backup và restore database <br>&emsp; + Thiết lập CloudFront cho web server để cải thiện hiệu năng và bảo mật <br><br> - **Tối ưu chi phí EC2 với Lambda:** <br>&emsp; + Tạo tags cho EC2 instances để nhận diện cho bài toán tối ưu chi phí <br>&emsp; + Tạo một IAM Role cho Lambda function để cấp quyền cần thiết <br>&emsp; + Tạo Lambda function tự động stop/start các EC2 instances <br>&emsp; + Kiểm thử Lambda function để đảm bảo hoạt động đúng | 07/10/2025 | 07/10/2025      | WordPress on AWS: <br> <https://000021.awsstudygroup.com/> <br> Lambda Cost Optimization: <br> <https://000022.awsstudygroup.com/> |
| 4   | - **Tự động hoá triển khai ứng dụng với CI/CD Pipeline:** <br>&emsp; + Chuẩn bị các tài nguyên cần thiết cho CI/CD pipeline <br>&emsp; + Cài đặt và cấu hình CodeDeploy Agent trên các EC2 instances <br>&emsp; + Tạo CodeCommit repository để lưu trữ source code ứng dụng <br>&emsp; + Cấu hình CodeBuild để compile và build ứng dụng <br>&emsp; + Thiết lập CodeDeploy để tự động triển khai <br>&emsp; + Tạo CodePipeline để điều phối toàn bộ workflow CI/CD <br>&emsp; + Khắc phục sự cố phát sinh trong quá trình chạy pipeline <br><br> - **Sử dụng AWS Storage Gateway cho hybrid cloud storage:** <br>&emsp; + Tạo một S3 Bucket để lưu trữ dữ liệu trên cloud <br>&emsp; + Thiết lập một EC2 instance để host Storage Gateway <br>&emsp; + Tạo một Storage Gateway để kết nối on‑premises với AWS storage <br>&emsp; + Tạo File Shares trên Storage Gateway cho truy cập dạng file <br>&emsp; + Mount các File Shares trên máy on‑premises để truy cập cloud storage | 08/10/2025 | 08/10/2025      | AWS CodePipeline: <br> <https://000023.awsstudygroup.com/> <br> Storage Gateway: <br> <https://000024.awsstudygroup.com/> |
| 5   | - **Quản lý Amazon FSx for Windows File Server:** <br>&emsp; + Tạo môi trường ban đầu cho file server <br>&emsp; + Tạo cả SSD và HDD Multi‑AZ file systems <br>&emsp; + Tạo các file shares mới trên các file systems <br>&emsp; + Kiểm thử và theo dõi hiệu năng của file systems <br>&emsp; + Bật data deduplication và shadow copies để tối ưu lưu trữ và bảo vệ dữ liệu <br>&emsp; + Quản lý user sessions, open files, và user storage quotas <br>&emsp; + Bật Continuous Access share cho high availability <br>&emsp; + Scale throughput và dung lượng lưu trữ khi cần <br>&emsp; + Xoá môi trường để dọn dẹp tài nguyên <br>&emsp; + Tham khảo AWS CLI để quản lý file server <br><br> - **Triển khai AWS Web Application Firewall (WAF):** <br>&emsp; + Tạo S3 Bucket và deploy một sample web application để thử nghiệm <br>&emsp; + Dùng AWS WAF với managed rules để bảo vệ trước các mối đe doạ phổ biến <br>&emsp; + Tạo custom và advanced custom rules cho nhu cầu bảo mật cụ thể <br>&emsp; + Kiểm thử các rules mới để đảm bảo hoạt động đúng <br>&emsp; + Bật log requests để theo dõi và phân tích <br>&emsp; + Dọn dẹp toàn bộ tài nguyên đã tạo để tránh phát sinh chi phí | 09/10/2025 | 09/10/2025      | Amazon FSx: <br> <https://000025.awsstudygroup.com/> <br> AWS WAF: <br> <https://000026.awsstudygroup.com/> |
| 6   | - **Quản lý tài nguyên AWS bằng Tags và Resource Groups:** <br>&emsp; + Hiểu và sử dụng tags trên AWS Management Console <br>&emsp; + Tạo một EC2 instance kèm tags <br>&emsp; + Thêm hoặc xoá tags khỏi tài nguyên hiện có <br>&emsp; + Lọc tài nguyên dựa trên tags <br>&emsp; + Tìm hiểu cách dùng tags với AWS Command Line Interface (CLI) <br>&emsp; + Thêm tags cho một EC2 resource hiện có bằng CLI <br>&emsp; + Thêm tags cho tài nguyên mới ngay khi tạo bằng CLI <br>&emsp; + Describe các tài nguyên đã gắn tag bằng CLI <br>&emsp; + Tạo và quản lý một Resource Group để tổ chức tài nguyên AWS <br>&emsp; + Tạo một Resource Group dựa trên tags <br>&emsp; + Xem và quản lý tài nguyên trong một Resource Group | 10/10/2025 | 10/10/2025      | AWS Tags & Resource Groups: <br> <https://000027.awsstudygroup.com/> |


### Kết quả đạt được tuần 5:

* Triển khai thành công các giải pháp networking nâng cao trên AWS:
  * VPC Peering cho kết nối trực tiếp giữa các VPC
  * Transit Gateway như kiến trúc hub mạng tập trung
  * Cấu hình Cross‑VPC DNS resolution và routing

* Triển khai và tối ưu ứng dụng cloud full‑stack:
  * Ứng dụng WordPress tích hợp database trên RDS
  * Auto Scaling và CloudFront cho hiệu năng và tính sẵn sàng
  * Tối ưu chi phí serverless bằng Lambda functions

* Xây dựng workflow DevOps tự động hoá toàn diện:
  * CI/CD pipelines end‑to‑end với AWS Developer Tools
  * Quy trình triển khai tự động với CodePipeline integration
  * Giải pháp hybrid cloud storage với Storage Gateway

* Cấu hình hệ thống file và bảo mật cấp doanh nghiệp:
  * Amazon FSx for Windows File Server với triển khai Multi‑AZ
  * AWS WAF với các custom security rules
  * Kỹ thuật theo dõi hiệu năng và tối ưu lưu trữ

* Thiết lập thực hành quản trị tài nguyên AWS hiệu quả:
  * Chiến lược gắn thẻ (tagging) để theo dõi chi phí và tổ chức
  * Resource Groups giúp quản trị tài nguyên tinh gọn
  * Thành thạo sử dụng cả AWS Console và CLI

* Trải nghiệm thực hành với Infrastructure as Code bằng CloudFormation templates để cung cấp môi trường nhất quán.
