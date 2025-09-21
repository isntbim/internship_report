---
title: "Worklog Tuần 1"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---



### Mục tiêu tuần 1:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Học cách viết worklog và xử lý workshop
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc thực hiện trong tuần:
| Thứ | Công việc                                                                                                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                                            |
| --- |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| ------------ | --------------- |-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 2   | - Làm quen với các thành viên FCJ <br> - Đọc và lưu ý các nội quy, quy định tại đơn vị thực tập                                                                                                                                                                             | 09/08/2025   | 09/08/2025      | Nội quy: <br> <https://policies.fcjuni.com/>                                                                                                              |
| 3   | - Tìm hiểu AWS và các loại dịch vụ (cho các project tương lai) <br>&emsp; + Compute <br>&emsp; + Storage <br>&emsp; + Networking <br>&emsp; + Database <br>&emsp; + ... <br> - Học cách viết workshop qua video và hướng dẫn <br>                                           | 09/09/2025   | 09/09/2025      | Về AWS: <br> <https://cloudjourney.awsstudygroup.com/> <br> Về workshop: <br> <https://van-hoang-kha.github.io/vi/>                                       |
| 4   | - Sử dụng kiến thức học được từ ngày trước đó về workshop để viết worklog <br> - Tạo AWS Free Tier account <br> - Tìm hiểu AWS Console & AWS CLI <br> - **Thử nghiệm:** <br>&emsp; + Tạo AWS account <br>&emsp; + Cài AWS CLI & cấu hình <br> &emsp; + Cách sử dụng AWS CLI | 09/10/2025   | 09/10/2025      | Git workshop của tôi: <br> <https://github.com/isntbim/internship_report> <br> AWS Console: <br> <https://aws.amazon.com/>                                |
| 5   | - Tìm hiểu EC2 cơ bản: <br>&emsp; + Instance types <br>&emsp; + AMI <br>&emsp; + EBS <br>&emsp; + Lưu trữ <br>&emsp; + Khởi chạy thử EC2 instance - Các cách remote SSH vào EC2 <br> - Tìm hiểu Elastic IP   <br>                                                           | 14/08/2025   | 15/08/2025      | EC2 console: <https://ap-southeast-1.console.aws.amazon.com/ec2/> <br> Cơ bản về Amazon EC2: <br> <https://www.coursera.org/learn/aws-amazon-ec2-basics/> |
| 6   | - **Thực hành:** <br>&emsp; + Tạo EC2 instance <br>&emsp; + Kết nối SSH <br>&emsp; + Gắn EBS volume                                                                                                                                                                         | 15/08/2025   | 15/08/2025      | EC2 console: <https://ap-southeast-1.console.aws.amazon.com/ec2/>                                                                                                                |

### Kết quả đạt được tuần 1:

* Hiểu AWS là gì và nắm được các nhóm dịch vụ cơ bản: 
  * Compute
  * Storage
  * Networking 
  * Database
  * ...

* Đã tạo và cấu hình AWS Free Tier account thành công.

* Làm quen với workshop và viết worklogs.

* Làm quen với AWS Management Console và biết cách tìm, truy cập, sử dụng dịch vụ từ giao diện web.

* Cài đặt và cấu hình AWS CLI trên máy tính bao gồm:
  * Access Key
  * Secret Key
  * Region mặc định
  * ...

* Tìm hiểu các khái niệm cơ bản về EC2:
  * Kiểu instance: Cân bằng giữa chi phí và hiệu suất.
  * AMI: Mẫu được cấu hình sẵn để khởi chạy instance.
  * EBS: Lưu trữ block bền vững cho instance.
  * Lưu trữ: Các loại tùy chọn lưu trữ cho các trường hợp sử dụng khác nhau.
  * Elastic IP: Địa chỉ IP tĩnh cho điện toán đám mây động.