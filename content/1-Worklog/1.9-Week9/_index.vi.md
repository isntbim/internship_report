---
title: "Worklog Tuần 9"
date: "`r Sys.Date()`"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---



### Mục tiêu tuần 9:

* Thiết kế và tích hợp các thành phần hội thoại (conversational) và event-driven sử dụng Amazon Lex và Amazon SNS.
* Làm việc với các dịch vụ dữ liệu được quản lý và caching như DynamoDB và ElastiCache, đồng thời tự động hóa deployments cho workloads chạy trên EKS.
* Áp dụng các thực hành governance và scalability thông qua Service Quotas, kiểm soát sử dụng dựa trên IAM và EKS Blueprints.
* Xây dựng và vận hành ứng dụng serverless và containerized, và đánh giá hiệu năng lưu trữ trên S3 và EFS.
* Triển khai các cơ chế bảo mật cho S3 và xây dựng pipeline data lake cơ bản với Glue, Athena và QuickSight.

### Các công việc thực hiện trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ |-----------------| -------------- |
| 2   | - **Cấu hình Amazon Lex Chatbot** <br>&emsp; + Deploy base application và các APIs cần thiết cho chatbot <br>&emsp; + Tạo một chatbot instance mới trong Amazon Lex <br>&emsp; + Nâng cấp (enhance) chức năng và luồng hội thoại (conversational flow) của chatbot <br>&emsp; + Phát triển Lambda function để xử lý fulfillment logic cho bot <br>&emsp; + Publish chatbot để có thể sử dụng <br><br> - **Triển khai mô hình Publish/Subscribe với Amazon SNS** <br>&emsp; + Deploy hạ tầng ban đầu sử dụng SAM template <br>&emsp; + Tạo Amazon SNS Topic để xử lý message publication <br>&emsp; + Phát triển customer notification service để subscribe vào topic <br>&emsp; + Tạo customer accounting service như một subscriber khác <br>&emsp; + Triển khai "extraordinary rides" service với message filtering <br>&emsp; + Cập nhật primary management service để publish messages lên SNS topic <br>&emsp; + Test fan-out functionality và các message filtering rules | 03/11/2025 | 03/11/2025 | Amazon Lex Chatbot: <br> <https://000058.awsstudygroup.com/> <br> Messaging with Amazon SNS: <br> <https://000059.awsstudygroup.com/> |
| 3   | - **Làm việc với Amazon DynamoDB** <br>&emsp; + Tạo table và thực hiện các thao tác dữ liệu cơ bản như write, read và update <br>&emsp; + Query dữ liệu từ table <br>&emsp; + Tạo và query Global Secondary Index <br>&emsp; + Quản lý table bằng AWS CloudShell <br>&emsp; + Tương tác với DynamoDB bằng Python, bao gồm tạo tables, quản lý dữ liệu và thực hiện queries và scans <br><br> - **Làm việc với Amazon ElastiCache for Redis** <br>&emsp; + Tạo ElastiCache subnet group <br>&emsp; + Tạo ElastiCache cluster với cả hai chế độ: cluster mode disabled và enabled <br>&emsp; + Cấp quyền truy cập và kết nối tới một cluster node <br>&emsp; + Sử dụng AWS SDK để kết nối tới ElastiCache cluster <br>&emsp; + Thực hiện các thao tác dữ liệu bằng AWS SDK như get/set strings, quản lý hashes, sử dụng publish/subscribe và làm việc với streams <br><br> - **Xây dựng CI/CD Pipeline cho EKS Cluster** <br>&emsp; + Chuẩn bị môi trường với một IAM User, Cloud9 workspace và cài đặt các Kubernetes tools <br>&emsp; + Cấu hình IAM role cho EKS cluster <br>&emsp; + Tạo EKS cluster và test deployment của sample application <br>&emsp; + Thiết lập AWS CodePipeline và CodeBuild với các service roles và permissions cần thiết <br>&emsp; + Tạo pipeline để tự động hóa deployment từ source code repository <br>&emsp; + Test CI/CD pipeline bằng cách thay đổi code | 04/11/2025 | 04/11/2025 | Amazon DynamoDB Workshop: <br> <https://000060.awsstudygroup.com/> <br> Amazon ElastiCache Workshop: <br> <https://000061.awsstudygroup.com/> <br> EKS CI/CD Workshop: <br> <https://000062.awsstudygroup.com/> |
| 4   | - **Quản lý Service Quotas** <br>&emsp; + Xem và quản lý service quotas từ một vị trí trung tâm <br>&emsp; + Request tăng service quota thông qua Service Quotas console <br><br> - **Triển khai Resource Usage và Cost Management với IAM** <br>&emsp; + Tạo IAM groups và users để quản lý access <br>&emsp; + Áp dụng policy giới hạn việc tạo resource theo AWS Region <br>&emsp; + Triển khai policy giới hạn các EC2 instance families được phép <br>&emsp; + Cập nhật policies để giới hạn các EC2 instance sizes được phép <br>&emsp; + Tạo và gán policy giới hạn các loại EBS volumes có thể được tạo <br><br> - **Deploy và Quản lý EKS Cluster sử dụng EKS Blueprints** <br>&emsp; + Chuẩn bị môi trường bằng cách tạo VPC, EC2 instance và cài đặt các công cụ cần thiết <br>&emsp; + Cấu hình IAM role cho thiết lập EKS Blueprints <br>&emsp; + Tạo EKS Blueprints và một CDK project <br>&emsp; + Xây dựng deployment pipeline để tạo và quản lý cluster <br>&emsp; + Quản lý team access đến cluster bằng Infrastructure as Code (IaC) <br>&emsp; + Cấu hình và test các add-ons như Cluster Autoscaler <br>&emsp; + Deploy workloads lên cluster sử dụng ArgoCD | 05/11/2025 | 05/11/2025 | Service Quotas Workshop: <br> <https://000063.awsstudygroup.com/> <br> IAM Resource Management: <br> <https://000064.awsstudygroup.com/> <br> EKS Blueprints Workshop: <br> <https://000065.awsstudygroup.com/> |
| 5   | - **Xây dựng Serverless Web Application với Lambda và API Gateway** <br>&emsp; + Tạo Cloud9 instance và CodeCommit repository cho project <br>&emsp; + Deploy frontend application bằng AWS Amplify Console <br>&emsp; + Deploy backend infrastructure bao gồm Lambda functions và API Gateway <br>&emsp; + Nạp dữ liệu mẫu (sample data) vào DynamoDB table <br>&emsp; + Triển khai hệ thống xử lý ride times với backend và frontend deployments <br>&emsp; + Phát triển hệ thống xử lý ảnh (photo processing) sử dụng Lambda cho chroma keying và photo-compositing <br><br> - **Chuyển Monolithic Application sang Microservices với Docker và AWS Fargate** <br>&emsp; + Tạo CloudFormation stack và thiết lập môi trường <br>&emsp; + Containerize monolithic application với Docker <br>&emsp; + Deploy containerized application bằng AWS Fargate <br>&emsp; + Cấu hình Application Load Balancer và ECS Service <br>&emsp; + Tạo task definition revision mới và cập nhật ECS service <br>&emsp; + Build Docker image cho microservice mới và tạo task definition và ECS service tương ứng <br><br> - **Đánh giá Hiệu năng Lưu trữ trên AWS** <br>&emsp; + Launch CloudFormation template và cấu hình security groups <br>&emsp; + Kết nối tới EC2 instance để test <br>&emsp; + Tối ưu S3 throughput và test sync commands cho truyền dữ liệu hiệu quả <br>&emsp; + Phân tích và tối ưu hiệu năng S3 cho các thao tác small file và copy operations <br>&emsp; + Tối ưu EFS IOPS và đánh giá ảnh hưởng của I/O size và sync frequency <br>&emsp; + Khảo sát ảnh hưởng của multi-threading lên hiệu năng EFS | 06/11/2025 | 06/11/2025 | Serverless Web Application: <br> <https://000066.awsstudygroup.com/> <br> Microservices with Fargate: <br> <https://000067.awsstudygroup.com/> <br> Storage Performance Evaluation: <br> <https://000068.awsstudygroup.com/> |
| 6   | - **Triển khai S3 Security Best Practices** <br>&emsp; + Launch CloudFormation template và bảo mật network access <br>&emsp; + Tạo access keys và kết nối tới EC2 instance <br>&emsp; + Yêu cầu HTTPS và SSE-S3 encryption cho data in transit và at rest <br>&emsp; + Block public ACLs và cấu hình S3 Block Public Access settings <br>&emsp; + Giới hạn truy cập tới S3 VPC Endpoint <br>&emsp; + Sử dụng AWS Config để detect public buckets <br>&emsp; + Sử dụng Amazon Access Analyzer cho S3 <br><br> - **Xây dựng Data Lake với Dữ liệu của Chính Mình** <br>&emsp; + Tạo Cloud9 instance và chuẩn bị dataset để upload lên S3 <br>&emsp; + Sử dụng AWS DataBrew cho data profiling, cleaning và transformation <br>&emsp; + Ingest dữ liệu với AWS Glue bằng cách cấu hình roles và tạo data catalog <br>&emsp; + Transform dữ liệu sang định dạng Parquet <br>&emsp; + Query dữ liệu bằng Amazon Athena với các truy vấn basic và advanced như joins và views <br>&emsp; + Visualize dữ liệu với Amazon QuickSight bằng cách kết nối datasets và xây dựng dashboard | 07/11/2025 | 07/11/2025 | S3 Security Best Practices: <br> <https://000069.awsstudygroup.com/> <br> Data Lake Workshop: <br> <https://000070.awsstudygroup.com/> |


### Kết quả đạt được tuần 9:

* Thiết kế các luồng hội thoại và messaging bằng cách cấu hình Amazon Lex chatbot, kết nối Lambda cho fulfillment và triển khai mô hình publish/subscribe với Amazon SNS cùng nhiều subscriber services.

* Làm việc với các dịch vụ dữ liệu được quản lý và cache:
  * Thực hành các thao tác DynamoDB cốt lõi, Global Secondary Indexes, quản lý table qua CloudShell và tương tác bằng Python.
  * Tạo và kết nối tới ElastiCache for Redis clusters, sử dụng SDK để thực hiện các thao tác như strings, hashes, publish/subscribe và streams.

* Tự động hóa deployments cho workloads dựa trên Kubernetes bằng cách provision EKS clusters, cấu hình IAM roles và xây dựng CI/CD pipelines với CodePipeline và CodeBuild để deploy sample applications từ các thay đổi trong source.

* Áp dụng governance và quản lý quotas:
  * Rà soát và điều chỉnh AWS Service Quotas cho nhu cầu capacity.
  * Triển khai IAM policies để kiểm soát việc sử dụng resources theo Region, EC2 instance family/size và EBS volume types.

* Sử dụng EKS Blueprints và Infrastructure as Code để chuẩn bị networking, cấu hình cluster roles, quản lý team access và deploy add-ons như Cluster Autoscaler cùng workloads thông qua ArgoCD.

* Xây dựng và đánh giá kiến trúc ứng dụng:
  * Phát triển serverless web application sử dụng Lambda, API Gateway, DynamoDB, Amplify và CodeCommit, bao gồm các luồng xử lý ride times và xử lý ảnh (photo processing).
  * Chuyển một monolithic application sang microservices với Docker và AWS Fargate, phía trước là Application Load Balancer và các ECS services.

* Phân tích hiệu năng lưu trữ trên AWS bằng cách test S3 throughput và các mẫu sync, khảo sát thao tác trên small files và tinh chỉnh EFS IOPS, I/O size, sync frequency và tác động của multi-threading.

* Tăng cường bảo mật S3:
  * Bắt buộc HTTPS và SSE-S3 encryption, block public access thông qua ACLs và Block Public Access, và giới hạn traffic qua S3 VPC Endpoint.
  * Sử dụng AWS Config và Access Analyzer để phát hiện và rà soát các buckets có khả năng public hoặc misconfigured.

* Xây dựng workflow data lake đơn giản bằng cách staging dữ liệu trong S3, transform với DataBrew và Glue sang Parquet, query bằng Athena và tạo visualizations trong QuickSight.
