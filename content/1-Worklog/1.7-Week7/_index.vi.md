---
title: "Nhật ký công việc Tuần 7"
date: 2026-07-30
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu Tuần 7 (Proposal Giai đoạn 4 - SageMaker Endpoint Deployment & Automated Retraining):

* Đóng gói mô hình Machine Learning thành artifact `model.tar.gz` kèm custom inference handler (`inference.py`).
* Triển khai **Amazon SageMaker Real-time Endpoint** (cấu hình `ml.m5.xlarge`) phục vụ suy luận dự đoán gợi ý thời gian thực 24/7.
* Xây dựng `SageMakerRecommendationProvider` tích hợp mượt mà với ứng dụng Backend và tự động hóa quy trình re-train định kỳ bằng **SageMaker Processing Jobs**.

### Công việc đã hoàn thành trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | - Đóng gói trọng số mô hình và script suy luận `inference.py` (`model_fn`, `predict_fn`, `output_fn`) thành file `model.tar.gz` xuất lên S3 prefix `models/` <br> - Viết custom inference handler | 20/07/2026 | 20/07/2026 | Hướng dẫn SageMaker Inference |
| 3 | - Triển khai **Amazon SageMaker Endpoint** thực tế (cấu hình instance `ml.m5.xlarge`) phục vụ dự đoán suy luận gợi ý thời gian thực 24/7 <br> - Đảm bảo độ trễ suy luận < 50ms cho các request dự đoán | 21/07/2026 | 21/07/2026 | Đặc tả SageMaker Endpoint Proposal |
| 4 | - Phát triển class `SageMakerRecommendationProvider` triển khai interface `BaseRecommendationProvider` gọi `boto3.client('sagemaker-runtime')` <br> - Đơn giản hóa format request/response giao tiếp với Backend | 22/07/2026 | 22/07/2026 | Tích hợp Provider Backend & ML |
| 5 | - Tự động hóa quy trình tái huấn luyện mô hình bằng **SageMaker Processing Jobs** (`scripts/run_processing_job.py`) thực thi container SKLearn/PyTorch <br> - Đọc dữ liệu tương tác từ S3, tự động chạy `preprocess.py`, `train.py`, `evaluate.py`, `promote.py` | 23/07/2026 | 23/07/2026 | Tự động hóa Retrain Proposal |
| 6 | - Kiểm thử tích hợp hệ thống ML xác minh khả năng phản hồi tức thời của SageMaker Endpoint <br> - Kiểm tra kịch bản re-train tự động và cập nhật con trỏ `LATEST.json` khi nạp dữ liệu tương tác mới | 24/07/2026 | 24/07/2026 | Kiểm thử Tích hợp ML Pipeline |

### Kết quả đạt được Tuần 7:

* Triển khai thành công SageMaker Real-time Endpoint (`ml.m5.xlarge`) hoạt động 24/7 phục vụ dự đoán gợi ý phim độ trễ thấp.
* Phát triển `SageMakerRecommendationProvider` kết nối mượt mà hệ thống suy luận SageMaker với ứng dụng Backend.
* Tự động hóa hoàn toàn quy trình re-train mô hình định kỳ bằng SageMaker Processing Jobs kèm cổng kiểm duyệt Promotion Gate tự động.
