---
title: "Worklog Tuần 10"
date: "`r Sys.Date()`"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---



### Mục tiêu tuần 10:

* Triển khai và quản lý ứng dụng với Red Hat OpenShift Service on AWS (ROSA) và xây dựng một quy trình CI/CD cơ bản.
* Xây dựng và phân tích một nền tảng analytics trên AWS sử dụng streaming ingestion, Glue, EMR, Athena, QuickSight và Redshift.
* Tạo các business dashboard và giám sát hoạt động mạng, hoạt động tài khoản với Amazon QuickSight, VPC Flow Logs và phân quyền truy cập billing.
* Phát triển và triển khai ứng dụng cloud sử dụng AWS CDK, kiến trúc event-driven với SNS/SQS và các mẫu serverless dựa trên Lambda.
* Xây dựng các serverless web application stack với API Gateway, Lambda, DynamoDB, Cognito và CloudFront, bao gồm SSL và authentication.
* Triển khai xử lý đơn hàng (order processing) và CI/CD pipeline cho serverless applications sử dụng SQS, SNS, SAM và CodePipeline.

### Các công việc thực hiện trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ |-----------------| -------------- |
| 2   | - **Triển khai Ứng dụng với Red Hat OpenShift Service on AWS (ROSA)** <br>&emsp; + Bật ROSA và cài đặt các công cụ command-line cần thiết <br>&emsp; + Tạo và cấu hình OpenShift cluster trên AWS <br>&emsp; + Deploy sample application lên OpenShift cluster <br>&emsp; + Thiết lập quy trình CI/CD cơ bản với CodeCommit, CodeBuild và CodePipeline <br>&emsp; + Tinh chỉnh CI/CD workflow dành riêng cho việc deploy ứng dụng <br><br> - **Xây dựng Nền tảng Analytics trên AWS** <br>&emsp; + Ingest và lưu trữ streaming data bằng Amazon Kinesis Firehose <br>&emsp; + Catalog dữ liệu với AWS Glue Crawlers để populate Glue Data Catalog <br>&emsp; + Transform dữ liệu bằng AWS Glue interactive sessions, Glue Studio và DataBrew <br>&emsp; + Xử lý dữ liệu quy mô lớn với Amazon EMR <br>&emsp; + Phân tích dữ liệu tương tác với Amazon Athena và thời gian thực với Kinesis Data Analytics <br>&emsp; + Visualize kết quả bằng cách tạo dashboards trong Amazon QuickSight <br>&emsp; + Cung cấp dữ liệu thông qua AWS Lambda và xây dựng data warehouse bằng Amazon Redshift | 10/11/2025 | 10/11/2025 | ROSA Hands-on Lab: <br> <https://000071.awsstudygroup.com/> <br> Analytics Platform: <br> <https://000072.awsstudygroup.com/> |
| 3   | - **Làm quen với Amazon QuickSight** <br>&emsp; + Chuẩn bị dữ liệu và xây dựng dashboard ban đầu với nhiều loại biểu đồ như line chart, pie chart và pivot table <br>&emsp; + Nâng cấp dashboard bằng cách áp dụng định dạng, thêm visual mới và bổ sung bảng dữ liệu chi tiết <br>&emsp; + Tạo dashboard tương tác bằng cách cấu hình filters, filter actions và navigation actions trước khi publish <br><br> - **Giám sát Hạ tầng Mạng với VPC Flow Logs** <br>&emsp; + Tạo và bật VPC Flow Logs để thu thập thông tin traffic IP cho một VPC <br>&emsp; + Publish dữ liệu flow log lên Amazon CloudWatch Logs <br>&emsp; + Giám sát và phân tích traffic thu thập được để chẩn đoán security group rules và hiểu các mẫu traffic <br><br> - **Phân quyền Truy cập AWS Billing Console** <br>&emsp; + Tạo IAM user group và bật quyền truy cập billing console <br>&emsp; + Định nghĩa custom IAM policy để cấp các quyền billing và cost management cần thiết <br>&emsp; + Gắn policy vào IAM user group để ủy quyền truy cập <br>&emsp; + Kiểm tra các quyền đã cấu hình bằng cách cho user trong group đăng nhập vào billing console | 11/11/2025 | 11/11/2025 | Amazon QuickSight Guide: <br> <https://000073.awsstudygroup.com/> <br> VPC Flow Logs Lab: <br> <https://000074.awsstudygroup.com/> <br> AWS Billing Console: <br> <https://000075.awsstudygroup.com/> |
| 4   | - **Phát triển Ứng dụng với AWS CDK** <br>&emsp; + Chuẩn bị môi trường bằng cách tạo IAM Role và launch một EC2 instance <br>&emsp; + Cấu hình môi trường phát triển với VSCode <br>&emsp; + Sử dụng CDK để tạo kiến trúc ứng dụng với API Gateway, ELB và ECS <br>&emsp; + Tích hợp Lambda và S3 vào kiến trúc <br>&emsp; + Áp dụng nested stacks để tăng khả năng tổ chức và tái sử dụng <br><br> - **Xây dựng Kiến trúc Event-driven với SNS và SQS** <br>&emsp; + Deploy hạ tầng cần thiết và cấu hình event generator <br>&emsp; + Triển khai mô hình publish/subscribe đơn giản với SNS topic và SQS queue <br>&emsp; + Áp dụng message filtering cho SNS subscription để route các message cụ thể <br>&emsp; + Sử dụng các kỹ thuật advanced message filtering cho các logic route phức tạp hơn <br><br> - **Phát triển Serverless Application với AWS Lambda** <br>&emsp; + Tạo Lambda function xử lý ảnh được trigger bởi S3 events <br>&emsp; + Thiết lập S3 bucket và IAM policy cho Lambda function <br>&emsp; + Test hoạt động resize ảnh của Lambda function <br>&emsp; + Tạo DynamoDB table để lưu trữ dữ liệu <br>&emsp; + Ghi dữ liệu vào DynamoDB table bằng Lambda function | 12/11/2025 | 12/11/2025 | AWS CDK Development: <br> <https://000076.awsstudygroup.com/> <br> Event-driven Architecture Lab: <br> <https://000077.awsstudygroup.com/> <br> Serverless Lambda Guide: <br> <https://000078.awsstudygroup.com/> |
| 5   | - **Xây dựng Serverless Frontend gọi API Gateway** <br>&emsp; + Deploy front-end application <br>&emsp; + Tạo DynamoDB table <br>&emsp; + Deploy các Lambda functions để ghi, liệt kê và xóa items <br>&emsp; + Cấu hình API Gateway methods và bật CORS <br>&emsp; + Test APIs qua Postman và từ front-end <br><br> - **Deploy Serverless Application với SAM** <br>&emsp; + Deploy front-end application <br>&emsp; + Tạo DynamoDB table <br>&emsp; + Deploy các Lambda functions để liệt kê, ghi, xóa và resize images <br>&emsp; + Cấu hình GET, POST và DELETE methods trong API Gateway <br>&emsp; + Test APIs qua Postman và front-end <br><br> - **Triển khai Serverless Authentication với Amazon Cognito** <br>&emsp; + Tạo Cognito User Pool <br>&emsp; + Tạo API và Lambda function tương ứng <br>&emsp; + Test luồng authentication với front-end application <br><br> - **Cấu hình SSL cho Serverless Application** <br>&emsp; + Tạo domain và Route 53 hosted zone <br>&emsp; + Yêu cầu SSL certificate qua AWS Certificate Manager <br>&emsp; + Tạo CloudFront distribution để serve application qua HTTPS | 13/11/2025 | 13/11/2025 | Serverless Frontend with API Gateway: <br> <https://000079.awsstudygroup.com/> <br> Serverless Application with SAM: <br> <https://000080.awsstudygroup.com/> <br> Cognito Authentication Lab: <br> <https://000081.awsstudygroup.com/> <br> SSL Configuration: <br> <https://000082.awsstudygroup.com/> |
| 6   | - **Triển khai Order Processing với SQS và SNS** <br>&emsp; + Tạo SQS queue và SNS topic <br>&emsp; + Tạo DynamoDB table cho orders <br>&emsp; + Phát triển các Lambda functions cho checkout, quản lý, xử lý và xóa orders <br>&emsp; + Test toàn bộ luồng order processing <br><br> - **Xây dựng CI/CD Pipeline cho Serverless Application** <br>&emsp; + Tạo Git repository cho SAM pipeline <br>&emsp; + Cấu hình SAM pipeline với AWS CodePipeline <br>&emsp; + Tạo Git repository cho front-end <br>&emsp; + Xây dựng pipeline cho front-end deployment <br>&emsp; + Test hoạt động của web application sau khi deploy | 14/11/2025 | 14/11/2025 | Order Processing with SQS and SNS: <br> <https://000083.awsstudygroup.com/> <br> CI/CD Pipeline for Serverless: <br> <https://000084.awsstudygroup.com/> |


### Kết quả đạt được tuần 10:

* Triển khai ứng dụng với Red Hat OpenShift Service on AWS bằng cách bật ROSA, provision cluster, deploy sample workload và kết nối quy trình CI/CD cơ bản với CodeCommit, CodeBuild và CodePipeline.

* Xây dựng và khám phá một nền tảng analytics trên AWS:
  * Ingest streaming data với Kinesis Firehose và catalog bằng AWS Glue Crawlers.
  * Transform và xử lý dữ liệu với Glue (Studio và interactive sessions), DataBrew, EMR, và phân tích với Athena cùng Kinesis Data Analytics.
  * Visualize insights qua QuickSight dashboards và cung cấp dữ liệu với Lambda và Redshift.

* Tạo visualizations và cải thiện observability:
  * Thiết kế QuickSight dashboards tương tác với nhiều loại biểu đồ, định dạng, filters và navigation.
  * Bật và xem xét VPC Flow Logs trong CloudWatch Logs để hiểu traffic patterns và xác thực hành vi security group.
  * Phân quyền truy cập AWS Billing Console thông qua IAM groups và custom billing policies, sau đó kiểm tra quyền được ủy thác.

* Phát triển hạ tầng và ứng dụng với AWS CDK và các mẫu event-driven:
  * Thiết lập môi trường phát triển CDK trên EC2 với VSCode, IAM roles và dùng CDK để định nghĩa kiến trúc với API Gateway, ELB, ECS, Lambda và S3.
  * Triển khai luồng event-driven SNS + SQS, bao gồm pub/sub cơ bản và advanced message filtering.
  * Tạo các workflow xử lý ảnh và lưu trữ dữ liệu dựa trên Lambda, tích hợp với S3 và DynamoDB.

* Xây dựng serverless application stack end-to-end:
  * Deploy front-end applications gọi API Gateway, backend bởi Lambda và DynamoDB, với cả cấu hình thủ công và thông qua SAM.
  * Cấu hình API Gateway methods với CORS, triển khai authentication dựa trên Cognito và test các luồng từ front-end cũng như với Postman.
  * Bảo mật serverless applications với custom domain, Route 53 hosted zone, ACM certificate và CloudFront distribution qua HTTPS.

* Triển khai order processing và tự động hóa cho serverless workloads:
  * Xây dựng pipeline xử lý đơn hàng sử dụng SQS, SNS, DynamoDB và nhiều Lambda functions cho checkout, quản lý và xóa orders.
  * Thiết lập CI/CD pipelines cho backend SAM-based và front-end applications với CodePipeline, kết nối với Git repositories và xác nhận deploy thành công.
