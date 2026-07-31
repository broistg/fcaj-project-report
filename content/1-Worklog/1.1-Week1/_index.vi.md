---
title: "Nhật ký công việc Tuần 1"
date: 2026-07-30
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu Tuần 1 (Proposal Giai đoạn 1 & Giai đoạn 2):

* Khởi động chương trình thực tập FCAJ, thống nhất phân công nhóm và nắm rõ quy định bảo mật.
* Nghiên cứu các dịch vụ AWS cốt lõi (VPC, EC2, DynamoDB, S3, SageMaker) phục vụ kiến trúc suy luận gợi ý Real-time.
* Soạn thảo bản **Đề xuất dự án (Proposal)** (Mục 2) và tính toán dự toán chi phí ($91.34/tháng) trên AWS Pricing Calculator.

### Công việc thực hiện trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | - Hoàn thành onboarding chương trình FCAJ & thống nhất phân công nhóm <br> - Đọc và ghi nhớ quy định thực tập, thiết lập workspace và chính sách an toàn thông tin | 15/06/2026 | 15/06/2026 | Tài liệu Onboarding nội bộ |
| 3 | - Cấu hình AWS CLI v2 và IAM developer profile tại region `ap-southeast-1` <br> - Nghiên cứu các dịch vụ AWS cho ứng dụng phim & ML inference: EC2, S3, DynamoDB, SageMaker | 16/06/2026 | 16/06/2026 | <https://docs.aws.amazon.com/cli/> |
| 4 | - Phân tích cấu trúc thô của tập dữ liệu The Movies Dataset (Kaggle/MovieLens) <br> - Xác định bài toán: quá tải thông tin (mất 15-20 phút chọn phim) vs gợi ý chủ động | 17/06/2026 | 17/06/2026 | Kaggle Movies Dataset |
| 5 | - Thiết kế kiến trúc giải pháp 4 tầng (Presentation, Application, Hot/Cold Data, ML Layer) <br> - Ánh xạ tài nguyên AWS: EC2 (Vite + FastAPI), DynamoDB (Hot data), S3 (Cold data), SageMaker (Processing Jobs & Endpoints) | 18/06/2026 | 18/06/2026 | Kiến trúc giải pháp Proposal |
| 6 | - Tính toán dự toán chi phí trên AWS Pricing Calculator ($91.34/tháng tổng cộng, bao gồm endpoint `ml.m5.xlarge` 24/7 & EC2) <br> - Soạn thảo văn bản Đề xuất dự án (Mục 2) & ma trận rủi ro | 19/06/2026 | 19/06/2026 | <https://calculator.aws/> |

### Kết quả đạt được Tuần 1:

* Thiết lập thành công môi trường máy trạm và xác minh xác thực AWS SDK qua `aws sts get-caller-identity`.
* Hoàn thiện kiến trúc giải pháp 4 tầng cho hệ thống suy luận gợi ý thời gian thực trên AWS.
* Hoàn thành văn bản **Proposal** (Mục 2) chính thức bao gồm tóm tắt dự án, bài toán, ma trận rủi ro và dự toán ngân sách.
