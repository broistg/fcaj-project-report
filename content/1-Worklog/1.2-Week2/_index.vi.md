---
title: "Nhật ký công việc Tuần 2"
date: 2026-07-30
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu Tuần 2 (Proposal Giai đoạn 1 & Giai đoạn 2):

* Nghiên cứu chuyên sâu các dịch vụ AWS cho kiến trúc hệ thống suy luận gợi ý thời gian thực (Real-time Inference).
* Phân tích cấu trúc thô của tập dữ liệu The Movies Dataset (Kaggle/MovieLens) và xác định tuyên bố vấn đề.
* Soạn thảo bản **Đề xuất dự án (Proposal)** (Mục 2) và tính toán dự toán chi phí ($91.34/tháng) trên AWS Pricing Calculator.

### Công việc thực hiện trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | - Khảo sát chuyên sâu kiến trúc gợi ý phim thời gian thực trên AWS <br> - Phân tích tính khả thi việc kết hợp SageMaker Endpoints 24/7 với SageMaker Processing Jobs định kỳ | 15/06/2026 | 15/06/2026 | Tài liệu SageMaker Developer |
| 3 | - Phân tích cấu trúc thô của tập dữ liệu The Movies Dataset (Kaggle/MovieLens) <br> - Xác định bài toán: quá tải thông tin (mất 15-20 phút chọn phim) vs gợi ý chủ động | 16/06/2026 | 16/06/2026 | Kaggle Movies Dataset |
| 4 | - Thiết kế kiến trúc giải pháp 4 tầng (Presentation, Application, Hot/Cold Data, ML Layer) <br> - Ánh xạ tài nguyên AWS: EC2 (Vite + FastAPI), DynamoDB (Hot data), S3 (Cold data), SageMaker (Processing Jobs & Endpoints) | 17/06/2026 | 17/06/2026 | Kiến trúc giải pháp Proposal |
| 5 | - Tính toán dự toán chi phí trên AWS Pricing Calculator ($91.34/tháng tổng cộng, bao gồm endpoint `ml.m5.xlarge` 24/7 & EC2) <br> - Cấu hình ma trận rủi ro và chiến lược giảm thiểu chi phí trên AWS | 18/06/2026 | 18/06/2026 | <https://calculator.aws/> |
| 6 | - Soạn thảo và hoàn thiện văn bản Đề xuất dự án chính thức (Mục 2) bao gồm lộ trình 8 tuần <br> - Thông qua ý kiến mentor và rà soát mục tiêu triển khai dự án | 19/06/2026 | 19/06/2026 | Văn bản Proposal Mục 2 |

### Kết quả đạt được Tuần 2:

* Phân tích thành công tập dữ liệu Kaggle/MovieLens và xác định tuyên bố bài toán cốt lõi.
* Hoàn thiện kiến trúc giải pháp 4 tầng cho hệ thống suy luận gợi ý thời gian thực trên AWS.
* Hoàn thành văn bản **Proposal** (Mục 2) chính thức bao gồm tóm tắt dự án, bài toán, ma trận rủi ro, dự toán ngân sách và lộ trình triển khai 8 tuần.
