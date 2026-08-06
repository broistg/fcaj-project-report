---
title: "Week 2 Worklog"
date: 2026-07-30
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives (Proposal Phase 1 & Phase 2 - ML Engineer Focus):

* Conduct in-depth research on real-time ML recommendation architecture on Amazon SageMaker.
* Analyze raw structures of The Movies Dataset (Kaggle/MovieLens) for Machine Learning model requirements.
* Draft the Machine Learning architecture section of the official **Proposal** document (Section 2) and perform ML infrastructure Cost Estimation ($91.34/month base estimate) using the AWS Pricing Calculator.

### Tasks Completed During the Week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - In-depth research on real-time recommendation architecture on AWS <br> - Evaluate feasibility of combining 24/7 SageMaker Endpoints with periodic SageMaker Processing Jobs for retraining | 06/15/2026 | 06/15/2026 | SageMaker Developer Guide |
| 3 | - Analyze raw schema of The Movies Dataset (Kaggle/MovieLens): ratings, movie metadata, user interaction IDs <br> - Define implicit user preference matrix modeling requirements (implicit feedback matrix) | 06/16/2026 | 06/16/2026 | Kaggle Movies Dataset |
| 4 | - Design 4-layer ML Pipeline architecture (Data Ingestion, Preprocessing/Feature Construction, Offline Training & Evaluation, Real-time SageMaker Inference) <br> - Define hot/cold data flow specifications with DynamoDB and S3 | 06/17/2026 | 06/17/2026 | Proposal Solution Architecture |
| 5 | - Estimate ML infrastructure budget using AWS Pricing Calculator ($91.34/month total, including 24/7 `ml.m5.xlarge` SageMaker Endpoint, Processing Jobs, and S3 storage) <br> - Formulate ML quality degradation risk matrix and cloud cost mitigation strategies | 06/18/2026 | 06/18/2026 | <https://calculator.aws/> |
| 6 | - Draft Machine Learning section & 8-week implementation roadmap in the official Proposal document (Section 2) <br> - Review ML pipeline implementation milestones with project mentor | 06/19/2026 | 06/19/2026 | Proposal Document Section 2 |

### Week 2 Achievements:

* Successfully analyzed Kaggle/MovieLens dataset structures and defined user behavior matrix modeling requirements.
* Finalized the 4-layer ML Pipeline architecture for real-time recommendation inference on Amazon SageMaker.
* Completed the Machine Learning specifications in the official **Proposal** document (Section 2) including 8-week roadmap, ML risk matrix, and SageMaker budget estimate.
