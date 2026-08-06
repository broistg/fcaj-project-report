---
title: "Week 2 Worklog"
date: 2026-07-30
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives (Proposal Phase 1 & Phase 2):

* Research core AWS cloud services (VPC, EC2, DynamoDB, S3, SageMaker) required for the Real-time Inference recommendation architecture.
* Analyze raw structures of The Movies Dataset (Kaggle/MovieLens) and formulate the problem statement.
* Formulate the official **Proposal** document (Section 2) and perform Cost Estimation ($91.34/month base estimate) using the AWS Pricing Calculator.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - In-depth research on real-time recommendation architecture on AWS <br> - Evaluate feasibility of combining 24/7 SageMaker Endpoints with periodic SageMaker Processing Jobs | 06/15/2026 | 06/15/2026 | SageMaker Developer Guide |
| 3 | - Analyze The Movies Dataset (Kaggle/MovieLens) raw structures <br> - Define problem statement: information overload (15-20 min browsing time) vs proactive personalization | 06/16/2026 | 06/16/2026 | Kaggle Movies Dataset |
| 4 | - Design 4-layer solution architecture (Presentation, Application, Hot/Cold Data, ML Layer) <br> - Map AWS resources: EC2 (Vite + FastAPI), DynamoDB (Hot data), S3 (Cold data), SageMaker (Processing Jobs & Endpoints) | 06/17/2026 | 06/17/2026 | Proposal Solution Architecture |
| 5 | - Calculate infrastructure budget using AWS Pricing Calculator ($91.34/month total, including 24/7 `ml.m5.xlarge` endpoint & EC2) <br> - Formulate risk matrix and cloud cost mitigation strategies | 06/18/2026 | 06/18/2026 | <https://calculator.aws/> |
| 6 | - Draft and finalize the official Proposal document (Section 2) including 8-week roadmap <br> - Review implementation milestones with project mentor | 06/19/2026 | 06/19/2026 | Proposal Document Section 2 |

### Week 2 Achievements:

* Successfully analyzed the Kaggle/MovieLens dataset structure and established core problem statement.
* Finalized the 4-layer solution architecture for real-time recommendation inference on AWS.
* Completed the official **Proposal** document (Section 2) including executive summary, problem statement, risk assessment, budget estimation, and 8-week roadmap.
