---
title: "Nhật ký công việc Tuần 7"
date: 2026-07-30
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu Tuần 7 (Proposal Giai đoạn 4 - Tích hợp hệ thống & Triển khai Cloud):

* Tích hợp mô hình Machine Learning vào quy trình Backend: Xây dựng POST API gợi ý (`/api/v1/recommend`) định tuyến request từ Frontend tới server dự đoán.
* Đóng gói mô hình AI và tích hợp với **SageMaker Real-time Endpoint** (`InvokeEndpoint`) phục vụ dự đoán 24/7 độ trễ siêu thấp kèm cơ chế fallback DynamoDB `RecommendationCache`.
* Thiết lập tự động hóa quy trình tái huấn luyện định kỳ qua **SageMaker Processing Jobs** và triển khai container ứng dụng lên Amazon EC2 qua GitHub Actions CI/CD.

### Công việc thực hiện trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | - Xây dựng route POST API gợi ý backend (`/api/v1/recommend/{user_id}`) xử lý kịch bản (`onboarding_user`, `returning_user`) <br> - Phát triển `SageMakerRecommendationProvider` gọi `boto3.client('sagemaker-runtime')` | 20/07/2026 | 20/07/2026 | Tích hợp Giai đoạn 4 Proposal |
| 3 | - Cấu hình tích hợp SageMaker Real-time Endpoint (cấu hình `ml.m5.xlarge`) phục vụ dự đoán thời gian thực 24/7 <br> - Triển khai cơ chế fallback tự động: khi Endpoint quá tải/không khả dụng, tự động chuyển về đọc `RecommendationCache` / `PopularMovies` từ DynamoDB | 21/07/2026 | 21/07/2026 | Đặc tả SageMaker Endpoint Proposal |
| 4 | - Tự động hóa quy trình tái huấn luyện mô hình bằng SageMaker Processing Jobs (`scripts/run_processing_job.py`) đọc dữ liệu tương tác lịch sử từ S3 | 22/07/2026 | 22/07/2026 | Tự động hóa Retrain Proposal |
| 5 | - Triển khai Amazon EC2 (`t3.micro`) trong Public Subnet của VPC mặc định kèm IAM Instance Profile <br> - Viết workflow GitHub Actions (`.github/workflows/deploy.yml`) thực thi SSH deploy và `docker compose up -d` | 23/07/2026 | 23/07/2026 | Triển khai EC2 & CI/CD Proposal |
| 6 | - Kiểm thử tích hợp hệ thống xác minh kết nối giữa container EC2 với SageMaker Endpoint, DynamoDB và S3 | 24/07/2026 | 24/07/2026 | Kiểm thử tích hợp Proposal |

### Kết quả đạt được Tuần 7:

* Xây dựng API tích hợp gợi ý backend định tuyến mượt mà giữa ứng dụng React frontend và server dự đoán.
* Tích hợp thành công SageMaker Real-time Endpoint phục vụ gợi ý độ trễ thấp kèm cơ chế fallback DynamoDB an toàn.
* Tự động hóa các tác vụ tái huấn luyện mô hình định kỳ bằng SageMaker Processing Jobs.
* Cấu hình pipeline CI/CD GitHub Actions tự động triển khai ứng dụng lên server Amazon EC2 thông qua SSH.
