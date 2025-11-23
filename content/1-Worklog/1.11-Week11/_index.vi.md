---
title: "Worklog Tuần 11"
date: "`r Sys.Date()`"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---



### Mục tiêu tuần 11:

* Tham gia sự kiện cộng đồng AWS để tìm hiểu thêm về các dịch vụ cloud nâng cao và best practices.
* Xây dựng hạ tầng serverless cho text service với thiết kế DynamoDB table và cấu hình IAM role.
* Hiện thực các hàm truy xuất dữ liệu với hỗ trợ phân trang và filter expressions.
* Phát triển cơ chế caching trong bộ nhớ và logic kiểm tra/validate request từ API.
* Tích hợp Amazon Bedrock Agent để sinh văn bản đoạn (paragraph) bằng AI.
* Cấu hình công cụ giám sát và debug cho serverless applications.
* Phát triển GraphQL APIs sử dụng AWS AppSync với DynamoDB resolvers.

### Các công việc thực hiện trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
|-----|-----------|--------------|------------------|----------------|
| 2   | - Tham gia sự kiện "AWS Cloud Mastery Series #2" để cập nhật kiến thức về các dịch vụ AWS nâng cao và cách thiết kế giải pháp thực tế. | 17/11/2025 | 17/11/2025 | |
| 3   | - Khởi tạo hạ tầng serverless cho text service: <br>&emsp; + Tạo DynamoDB table `wordsntexts` với partition key kiểu string để lưu trữ từ (words) và đoạn văn (paragraphs) <br>&emsp; + Cấu hình IAM execution role với quyền `dynamodb:Scan`, `dynamodb:Query` và ghi log lên CloudWatch <br>&emsp; + Thiết lập Lambda handler ban đầu và tạo các đối tượng kết nối database qua `boto3` <br><br> - Xây dựng các hàm truy xuất dữ liệu từ cơ sở dữ liệu: <br>&emsp; + Phát triển hàm `fetch_words_from_db` sử dụng DynamoDB Scan kết hợp `LastEvaluatedKey` để phân trang (pagination) <br>&emsp; + Phát triển hàm `fetch_paragraph_from_db` áp dụng filter expression dựa trên thuộc tính content type và length | 18/11/2025 | 18/11/2025 | |
| 4   | - Cài đặt cơ chế caching và xử lý dữ liệu: <br>&emsp; + Thiết kế global cache dictionary trong bộ nhớ với TTL 300 giây để giảm tần suất Scan DynamoDB <br>&emsp; + Cài đặt logic `get_random_words` để ưu tiên lấy dữ liệu từ cache, fallback về DB và thực hiện random sampling <br>&emsp; + Cài đặt logic `get_paragraph` để clamp giá trị length trong khoảng 1–3 và tách chuỗi nội dung thành danh sách từ <br><br> - Phát triển validation cho API request và chuẩn hóa response: <br>&emsp; + Tạo lớp `Decimal_encoder` custom để serialize đúng các numeric type của DynamoDB khi xuất JSON <br>&emsp; + Bổ sung các khối kiểm tra input cho query parameters `type` và `count` để xử lý `TypeError` và `ValueError` <br>&emsp; + Chuẩn hóa cấu trúc JSON response với HTTP status code và headers phù hợp | 19/11/2025 | 19/11/2025 | |
| 5   | - Tích hợp Amazon Bedrock Agent cho khả năng sinh nội dung: <br>&emsp; + Cập nhật IAM permissions để bổ sung quyền `bedrock:InvokeAgent` và gán với Agent ID `HUEBUXSALX` <br>&emsp; + Khởi tạo client `bedrock-agent-runtime` và cài đặt lệnh `invoke_agent` kèm quản lý session <br>&emsp; + Xây dựng logic xử lý streaming response để ghép nối các byte chunk thành một chuỗi hoàn chỉnh <br><br> - Thực hiện prompt engineering và thử nghiệm model: <br>&emsp; + Thiết kế các "trigger" prompt để Agent trả về đúng ba đoạn văn được ngăn cách bằng dòng trống <br>&emsp; + Thử nghiệm nhiều model nền tảng khác nhau để đảm bảo format đầu ra ổn định cho logic tách đoạn <br>&emsp; + Hiện thực phần parsing để tách output AI thành các đoạn riêng biệt | 20/11/2025 | 20/11/2025 | |
| 6   | - Giám sát và debug serverless applications với CloudWatch và X-Ray: <br>&emsp; + Phân tích CloudWatch Logs của Lambda để xác định và xử lý lỗi thực thi <br>&emsp; + Định nghĩa và thu thập custom metrics phản ánh hiệu năng và hành vi ứng dụng <br>&emsp; + Cấu hình CloudWatch Alarms để gửi cảnh báo khi các metric vượt ngưỡng quan trọng <br>&emsp; + Bật AWS X-Ray tracing để trực quan hóa service map và phát hiện các điểm nghẽn độ trễ <br><br> - Phát triển GraphQL APIs với AWS AppSync và DynamoDB resolvers: <br>&emsp; + Chuẩn bị môi trường AppSync và cấu hình DynamoDB làm data source <br>&emsp; + Cài đặt resolvers cho các thao tác Write và Read với từng item dữ liệu <br>&emsp; + Cấu hình resolvers cho Update và Delete để quản lý vòng đời dữ liệu <br>&emsp; + Thực thi Scan và Query để phục vụ nhu cầu truy vấn tập dữ liệu lớn qua API <br>&emsp; + Thiết kế và cài đặt các complex object resolvers để xử lý cấu trúc dữ liệu lồng nhau | 21/11/2025 | 21/11/2025 | CloudWatch and X-Ray Monitoring: <br> <https://000085.awsstudygroup.com/> <br> AppSync GraphQL APIs: <br> <https://000086.awsstudygroup.com/> |


### Kết quả đạt được tuần 11:

* Tham gia sự kiện "AWS Cloud Mastery Series #2" và cập nhật kiến thức về các dịch vụ AWS nâng cao, mô hình kiến trúc thực tế và những best practices trong vận hành.

* Xây dựng hạ tầng serverless cho ứng dụng luyện gõ văn bản:
  * Tạo DynamoDB table `wordsntexts` với partition key kiểu string để lưu khoảng hơn 64.000 từ và đoạn văn.
  * Cấu hình IAM execution role cho phép DynamoDB Scan/Query và ghi log lên CloudWatch.
  * Thiết lập Lambda handler (128 MB memory, timeout 15 giây) cùng các đối tượng kết nối database bằng `boto3`.

* Hiện thực các thuật toán truy xuất dữ liệu:
  * Phát triển hàm `fetch_words_from_db` sử dụng DynamoDB Scan kết hợp `LastEvaluatedKey` để xử lý phân trang.
  * Xây dựng hàm `fetch_paragraph_from_db` với filter expression dựa trên content type và length (short: 10–25 từ, medium: 25–60 từ, long: trên 60 từ).

* Tối ưu hiệu năng ứng dụng và xử lý request:
  * Thiết kế hệ thống cache trong bộ nhớ với TTL 300 giây để giảm số lần Scan DynamoDB cho tải dự kiến ~500 request/giờ.
  * Cài đặt các hàm `get_random_words` và `get_paragraph` với random sampling và cơ chế giới hạn length trong khoảng 1–3.
  * Tạo lớp `Decimal_encoder` để serialize chính xác các numeric type của DynamoDB khi trả về JSON.
  * Thêm kiểm tra đầu vào cho query parameters `type` và `count` để xử lý lỗi `TypeError`/`ValueError` hợp lý.
  * Chuẩn hóa JSON response với HTTP status codes và headers rõ ràng.

* Tích hợp Amazon Bedrock Agent để sinh đoạn văn bằng AI:
  * Mở rộng IAM permissions với `bedrock:InvokeAgent` và cấu hình truy cập đến Agent ID `HUEBUXSALX`.
  * Khởi tạo client `bedrock-agent-runtime` với cơ chế session cho các lời gọi `invoke_agent`.
  * Xây dựng logic ghép các streaming byte chunk thành chuỗi văn bản hoàn chỉnh.
  * Thiết kế trigger prompts để sinh đúng ba đoạn văn ngăn cách bằng dòng trống, phục vụ tính năng thử thách gõ hàng ngày.
  * Cài đặt logic parsing tách output AI thành các trường JSON.

* Cấu hình khả năng quan sát (observability) và debug cho serverless applications:
  * Phân tích log thực thi của Lambda trong CloudWatch để bắt lỗi và tối ưu.
  * Tạo custom CloudWatch metrics theo dõi hiệu năng và hành vi ứng dụng.
  * Thiết lập CloudWatch Alarms với ngưỡng quan trọng cho error rate và duration.
  * Bật AWS X-Ray để xem service map và nhận diện các đoạn có độ trễ cao.

* Phát triển GraphQL APIs với AWS AppSync:
  * Cấu hình AppSync và DynamoDB làm data source.
  * Hiện thực resolvers cho các thao tác Write, Read, Update, Delete.
  * Cấu hình các Scan/Query resolvers cho nhu cầu truy vấn tập dữ liệu lớn.
  * Thiết kế complex object resolvers để xử lý cấu trúc dữ liệu lồng nhau và quan hệ giữa các thực thể.
