---
title: "Nhật ký công việc Tuần 7"
date: 2026-07-30
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu Tuần 7 (Proposal Giai đoạn 5 - Kiểm thử & Tối ưu hóa):

* Rà soát toàn bộ hệ thống trên 3 kịch bản người dùng chính (Khách duyệt phim, Người dùng mới onboarding, Người dùng quay lại nhận gợi ý), xử lý lỗi và đo lường hiệu suất thực tế.
* Tối ưu hóa thời gian tải trang, tốc độ truy vấn DynamoDB và hiệu quả sử dụng cache gợi ý.
* Giám sát chi phí AWS so với các hạn mức ngân sách ($91.34/tháng dự toán) và hoàn thiện tài liệu Workshop (Mục 5) & báo cáo thực tập cá nhân.

### Công việc thực hiện trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | - Rà soát toàn bộ hệ thống qua các kịch bản: Khách chưa đăng nhập, Người dùng mới chọn thể loại onboarding và Khách quay lại nhận gợi ý cá nhân hóa <br> - Kiểm thử cơ chế fallback: xác minh hệ thống tự động chuyển về đọc `PopularMovies` từ DynamoDB nếu SageMaker endpoint tắt | 27/07/2026 | 27/07/2026 | Đặc tả Kiểm thử & Fallback Proposal |
| 3 | - Đo lường hiệu suất thực tế: tối ưu thời gian tải trang Vite, độ trễ truy vấn batch DynamoDB (`BatchGetItem`) và thời gian sống cache <br> - Kiểm tra tính toàn vẹn dữ liệu: đảm bảo mọi movie ID mô hình gợi ý ra đều tồn tại trong bảng DynamoDB `Movies` | 28/07/2026 | 28/07/2026 | Tối ưu hiệu năng Proposal |
| 4 | - Kiểm tra giám sát chi phí AWS: xác minh cảnh báo AWS Budgets (ngưỡng 50% và 75%) và quy tắc S3 Lifecycle Rules (tự động xóa trọng số mô hình cũ sau 30 ngày) <br> - Rà soát chính sách IAM tối thiểu và log group CloudWatch | 29/07/2026 | 29/07/2026 | Giảm thiểu rủi ro & Ngân sách Proposal |
| 5 | - Cập nhật Sơ đồ Kiến trúc hệ thống (v2.0 / `diagram.png`) thể hiện VPC, EC2, DynamoDB, S3, SageMaker, IAM, CloudWatch và AWS Budgets <br> - Soạn thảo hoàn thiện tài liệu Workshop (từ Mục 5.1 đến 5.6) cho cả bản tiếng Anh và tiếng Việt | 30/07/2026 | 30/07/2026 | Tài liệu Workshop Mục 5 |
| 6 | - Hoàn thành Nhật ký công việc cá nhân (Tuần 1 đến Tuần 7), kiểm tra build site Hugo cục bộ, xóa các thông báo cảnh báo và xuất bản báo cáo | 31/07/2026 | 31/07/2026 | Hoàn thiện Báo cáo cá nhân |

### Kết quả đạt được Tuần 7:

* Rà soát thành công toàn bộ hệ thống trên tất cả kịch bản người dùng, chứng minh khả năng cá nhân hóa tức thời qua SageMaker Real-time Endpoints.
* Tối ưu hóa thời gian tải trang và tốc độ truy vấn DynamoDB đồng thời đảm bảo tính toàn vẹn dữ liệu giữa mô hình và database.
* Xác minh thành công các hạn mức ngân sách AWS Budgets ($91.34/tháng) và quy tắc S3 Lifecycle Rules giúp ngăn ngừa rủi ro bùng nổ chi phí.
* Hoàn thành báo cáo thực tập cá nhân (`fcaj-project-report`), đồng bộ tài liệu Workshop, xóa các ghi chú warning mẫu và xuất bản báo cáo.
