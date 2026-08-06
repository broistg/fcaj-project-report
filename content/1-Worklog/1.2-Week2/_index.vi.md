---
title: "Nhật ký công việc Tuần 2"
date: 2026-07-30
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu Tuần 2 (Proposal Giai đoạn 1 & Giai đoạn 2 - ML Engineer Focus):

* Nghiên cứu chuyên sâu kiến trúc suy luận gợi ý thời gian thực (Real-time Inference) trên Amazon SageMaker.
* Phân tích cấu trúc dữ liệu thô của tập dữ liệu The Movies Dataset (Kaggle/MovieLens) cho mô hình hóa Machine Learning.
* Soạn thảo phần kiến trúc Machine Learning trong bản **Đề xuất dự án (Proposal)** (Mục 2) và tính toán dự toán chi phí hạ tầng ML ($91.34/tháng) trên AWS Pricing Calculator.

### Công việc đã hoàn thành trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | - Khảo sát chuyên sâu kiến trúc suy luận ML gợi ý phim thời gian thực trên AWS <br> - Phân tích tính khả thi việc kết hợp SageMaker Endpoints 24/7 với SageMaker Processing Jobs định kỳ cho quy trình re-train | 15/06/2026 | 15/06/2026 | Tài liệu SageMaker Developer |
| 3 | - Phân tích schema dữ liệu thô The Movies Dataset (Kaggle/MovieLens): ratings, movie metadata, user interaction IDs <br> - Xác định bài toán mô hình hóa hành vi ngầm định người dùng (implicit rating matrix modeling) | 16/06/2026 | 16/06/2026 | Kaggle Movies Dataset |
| 4 | - Thiết kế kiến trúc ML Pipeline 4 tầng (Data Ingestion, Preprocessing/Feature Engineering, Offline Model Training & Evaluation, Real-time SageMaker Inference) <br> - Định nghĩa các luồng xử lý dữ liệu nóng/lạnh với DynamoDB và S3 | 17/06/2026 | 17/06/2026 | Kiến trúc giải pháp Proposal |
| 5 | - Dự toán chi phí hạ tầng ML trên AWS Pricing Calculator ($91.34/tháng tổng cộng, bao gồm 1x `ml.m5.xlarge` SageMaker Endpoint 24/7, Processing Jobs và S3 storage) <br> - Cấu hình ma trận rủi ro suy giảm chất lượng mô hình và chiến lược giảm thiểu chi phí trên AWS | 18/06/2026 | 18/06/2026 | <https://calculator.aws/> |
| 6 | - Soạn thảo phần Machine Learning & Lộ trình triển khai 8 tuần trong bản Đề xuất dự án chính thức (Mục 2) <br> - Thông qua ý kiến mentor và rà soát mục tiêu triển khai pipeline ML cho dự án | 19/06/2026 | 19/06/2026 | Văn bản Proposal Mục 2 |

### Kết quả đạt được Tuần 2:

* Phân tích thành công tập dữ liệu Kaggle/MovieLens và xác định các yêu cầu kỹ thuật mô hình hóa hành vi người dùng.
* Hoàn thiện thiết kế kiến trúc ML Pipeline 4 tầng cho hệ thống suy luận gợi ý thời gian thực trên Amazon SageMaker.
* Hoàn thành nội dung Machine Learning trong bản **Proposal** (Mục 2) bao gồm lộ trình 8 tuần, ma trận rủi ro ML và dự toán ngân sách SageMaker.
