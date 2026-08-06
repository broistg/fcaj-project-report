---
title: "Nhật ký công việc Tuần 8"
date: 2026-07-30
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu Tuần 8 (Proposal Giai đoạn 5 - ML System Testing, Fallback Verification & Report Finalization):

* Kiểm thử toàn bộ hệ thống ML trên 3 kịch bản người dùng (Khách chưa đăng nhập, Người dùng mới chọn thể loại onboarding, Người dùng quay lại nhận gợi ý cá nhân hóa).
* Kiểm thử và xác minh cơ chế Fallback an toàn (DynamoDB `RecommendationCache` / `PopularMovies`) khi SageMaker Endpoint quá tải hoặc đứt kết nối.
* Tối ưu hóa độ trễ suy luận, giám sát ngân sách AWS SageMaker ($91.34/tháng) và hoàn thiện tài liệu Workshop (Mục 5) & Báo cáo thực tập cá nhân Kỹ sư Machine Learning.

### Công việc đã hoàn thành trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | - Rà soát toàn bộ hệ thống ML qua 3 kịch bản: Khách chưa đăng nhập (Popularity Ranker), Người dùng mới onboarding (Content-Based), và Người dùng quay lại (Implicit ALS / Hybrid RRF via SageMaker Endpoint) <br> - Đo lường chất lượng danh sách gợi ý | 27/07/2026 | 27/07/2026 | Kiểm thử Kịch bản ML |
| 3 | - Kiểm thử cơ chế Fallback an toàn: giả lập tắt SageMaker Endpoint hoặc đứt kết nối mạng <br> - Xác minh backend tự động chuyển sang đọc `RecommendationCache` và `PopularMovies` từ DynamoDB mà không gây gián đoạn trải nghiệm người dùng | 28/07/2026 | 28/07/2026 | Đặc tả Fallback Dự phòng Proposal |
| 4 | - Đo lường và tối ưu độ trễ suy luận ML: tối ưu kích thước payload JSON request/response, cache kết quả gợi ý ngắn hạn trong DynamoDB `RecommendationCache` <br> - Kiểm tra tính toàn vẹn Movie ID giữa mô hình ML và catalog database | 29/07/2026 | 29/07/2026 | Tối ưu Hiệu năng ML Inference |
| 5 | - Giám sát ngân sách AWS SageMaker: kiểm tra các ngưỡng cảnh báo AWS Budgets ($91.34/tháng) <br> - Xác minh S3 Lifecycle Rules tự động xóa các tệp trọng số mô hình cũ sau 30 ngày để chống bùng nổ chi phí lưu trữ ngầm | 30/07/2026 | 30/07/2026 | Quản trị Chi phí Cloud Proposal |
| 6 | - Cập nhật sơ đồ kiến trúc ML v2.0, hoàn thiện tài liệu Workshop (từ Mục 5.1 đến 5.6) cho cả bản tiếng Anh và tiếng Việt <br> - Hoàn thành Nhật ký công việc cá nhân Kỹ sư Machine Learning (Tuần 1 đến Tuần 8) và xuất bản báo cáo | 31/07/2026 | 31/07/2026 | Hoàn thiện Báo cáo ML Engineer |

### Kết quả đạt được Tuần 8:

* Kiểm thử thành công toàn bộ hệ thống suy luận gợi ý ML trên cả 3 kịch bản người dùng thực tế.
* Xác minh tính hoạt động ổn định của cơ chế Fallback an toàn qua DynamoDB `RecommendationCache` và `PopularMovies`.
* Tối ưu hóa độ trễ phản hồi suy luận ML, đảm bảo tính toàn vẹn dữ liệu Movie ID và xác minh hạn mức ngân sách AWS Budgets ($91.34/tháng).
* Hoàn thành toàn bộ báo cáo thực tập cá nhân Kỹ sư Machine Learning (`fcaj-project-report`), tài liệu Workshop Mục 5 và xuất bản báo cáo chính thức.
