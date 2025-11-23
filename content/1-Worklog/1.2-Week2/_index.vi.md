---
title: "Worklog Tuần 2"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---



### Mục tiêu tuần 2:

* Xác định và giới hạn phạm vi dự án trò chơi gõ phím đầu tiên (các tính năng cốt lõi, ranh giới microservice, định hướng matchmaking sau này).
* Thiết lập nền tảng làm việc nhóm: kho mã chung, backlog ban đầu, sơ đồ ER, tech stack, phân quyền sở hữu.
* Chuẩn hoá công thức tính WPM và độ chính xác.
* Prototype dịch vụ FastAPI: sinh văn bản, ghép câu, chat; xác thực hướng tích hợp Bedrock.
* Thiết lập AWS Budgets với cảnh báo.
* Nắm vững mức cơ bản: Lambda (function URL), VPC (subnet, gateway, peering vs transit), Flow Logs, khái niệm load balancing.
* Cấp phát Amazon RDS; thiết kế schema và seed dữ liệu phục vụ truy xuất văn bản.
* Refactor TextService sang truy xuất qua DB; benchmark so với phương pháp API trước đó.
* Giới thiệu thực hành vận hành sớm: phân vai, benchmarking, định hướng khả năng mở rộng.

### Các công việc thực hiện trong tuần:
| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                   |
| --- |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|-----------------|----------------------------------|
| 2 | - Tổ chức phiên brainstorming để xác định và ưu tiên hoá các khái niệm cho dự án đầu tiên <br>&emsp; + Chuyển ghi chú brainstorming từ project canvas vào backlog nhiệm vụ ban đầu trên bảng quản lý <br>&emsp; + Nghiên cứu và ghi lại chi tiết thuật toán tính WPM và độ chính xác để thống nhất <br>&emsp; + Tạo kho mã chung và thiết lập cấu trúc dự án cơ bản cho các ngôn ngữ và microservice đã chọn <br>&emsp; + Tinh chỉnh sơ đồ ER phác thảo và bắt đầu phác thảo schema CSDL ban đầu <br>&emsp; + Phân công chính thức trách nhiệm lead cho từng microservice để tối ưu hoá phát triển                                                                                                               | 09/15/2025   | 09/15/2025      |                                  |
| 3 | - Thiết lập AWS Budgets: <br>&emsp; + Rà soát các loại budget (Cost, Usage, RI, ...) <br>&emsp; + Xác định ngưỡng chi phí hằng tháng <br>&emsp; + Cấu hình budget trong AWS Console <br>&emsp; + Thiết lập cảnh báo email/SNS <br/> - Tạo web app dùng AWS Lambda: <br>&emsp; + Học fundamentals Lambda và function URL <br>&emsp; + Viết hàm \"Hello World\" đơn giản <br>&emsp; + Cấu hình hàm và IAM role <br>&emsp; + Kích hoạt và kiểm thử endpoint function URL <br/> - Học và thử FastAPI cho microservice: <br>&emsp; + Theo tutorial chính thức FastAPI <br>&emsp; + Thiết lập môi trường dev local <br>&emsp; + Tạo proof-of-concept API <br>&emsp; + Implement và test endpoint cơ bản qua Swagger UI | 09/16/2025   | 09/16/2025      | AWS Lambda:<br/> <https://ap-southeast-1.console.aws.amazon.com/lambda> <br/> AWS Budgets: <br/><https://us-east-1.console.aws.amazon.com/costmanagement/> <br/> FastAPI: <br/> <https://www.coursera.org/learn/packt-mastering-rest-apis-with-fastapi-1xeea/> |
| 4 | - Khám phá nền tảng Networking và Security AWS: <br>&emsp; + Ôn khái niệm Amazon VPC như một khu vực cô lập trong AWS Cloud <br>&emsp; + Hiểu mục đích subnet, phân biệt public vs private subnet để cấu trúc mạng <br>&emsp; + Nắm vai trò Internet Gateway (truy cập internet cho public subnet) và NAT Gateway (cho private subnet ra internet an toàn) <br>&emsp; + Khám phá VPC Flow Logs để giám sát / troubleshoot traffic nội bộ <br>&emsp; + So sánh kết nối on-prem: Site-to-Site VPN vs Direct Connect <br>&emsp; + Hiểu use case VPC Peering so với Transit Gateway <br>&emsp; + Nắm mục tiêu tổng quát Elastic Load Balancing (phân phối traffic nâng cao tính sẵn sàng)                            | 09/17/2025   | 09/17/2025      | Module 02-(01 to 03): <br> <https://www.youtube.com/watch?v=O9Ac_vGHquM> <br> <https://www.youtube.com/watch?v=BPuD1l2hEQ4> <br> <https://www.youtube.com/watch?v=CXU8D3kyxIc>                    |
| 5 | - Khám phá Amazon Bedrock playground: <br>&emsp; + Rà soát các foundation model (Claude, Titan, ...) <br>&emsp; + Chọn model cho text generation <br>&emsp; + Thử nghiệm prompt và tham số khác nhau <br>&emsp; + Sinh và phân tích mẫu phản hồi <br/> - Prototype microservice được chỉ định: <br>&emsp; + Cấu trúc logic dịch vụ và tích hợp nhiều API sinh văn bản <br>&emsp; + Implement hàm lõi tạo câu ngẫu nhiên và quản lý chat <br>&emsp; + Rà soát bản build đầu để xác định hạn chế và phác thảo bước cải tiến tiếp theo <br>&emsp; + Xác thực hướng kỹ thuật đã chọn                                                                                                                                 | 09/18/2025   | 09/18/2025      | Amazon Bedrock:<br/><https://ap-southeast-1.console.aws.amazon.com/bedrock>                   |
| 6 | - Khởi tạo và cấu hình Amazon RDS: <br>&emsp; + Rà soát và chọn engine phù hợp nhu cầu dự án <br>&emsp; + Cấu hình thiết lập lõi: credentials, VPC, security group rules <br>&emsp; + Khởi tạo DB, theo dõi tạo xong và lưu an toàn endpoint kết nối <br> - Prototype TextService dùng Database: <br>&emsp; + Thiết kế schema đơn giản (bảng words, sentences) lưu nội dung văn bản <br>&emsp; + Tạo script một lần để seed dataset ban đầu vào RDS <br>&emsp; + Refactor TextService để lấy dữ liệu từ DB thay vì API ngoài và benchmark cải thiện hiệu năng <br>&emsp; + Chạy benchmark đơn giản so sánh thời gian phản hồi giữa phương pháp API cũ và truy vấn DB mới                                         | 09/19/2025   | 09/19/2025      | Aurora and RDS: <br/><https://ap-southeast-1.console.aws.amazon.com/rds>                     |


### Kết quả đạt được tuần 2:

* Xác định phạm vi trò chơi gõ phím đầu tiên:
    * Tính năng cốt lõi
    * Ranh giới microservice
    * Backlog khởi tạo
    * Phân quyền sở hữu
  
* Đã nghiên cứu và chuẩn hoá công thức WPM và độ chính xác.
* Khởi tạo repository chung với cấu trúc đa ngôn ngữ nền tảng.
* Tinh chỉnh sơ đồ ER và phác thảo schema quan hệ ban đầu.
* Hoàn thành prototype FastAPI (sinh văn bản, ghép câu, chat) và xác thực qua Swagger UI.
* Thiết lập AWS Budgets với ngưỡng tháng và cảnh báo.
* Nắm các nền tảng AWS cốt lõi:
    * Lambda (function URL)
    * VPC (subnet, IGW, NAT, Flow Logs)
    * Peering vs Transit Gateway
    * Khái niệm Load Balancing
  
* Khám phá model Amazon Bedrock; xác thực model ứng viên và chiến lược prompt.
* Khởi tạo phiên bản RDS, tạo schema, nạp seed dataset.
* Refactor TextService sang truy xuất DB với cải thiện hiệu năng ban đầu (benchmark).
* Giới thiệu thực hành vận hành sớm: phân quyền sở hữu, tập trung benchmarking, cân nhắc khả năng mở rộng.

