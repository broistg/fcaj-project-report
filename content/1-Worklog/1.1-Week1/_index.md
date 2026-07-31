---
title: "Week 1 Worklog"
date: 2026-07-30
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Week 1 Objectives (Proposal Phase 1 & Phase 2):

* Onboard to the FCAJ internship program, align on team roles, and review security regulations.
* Research core AWS cloud services (VPC, EC2, DynamoDB, S3, SageMaker) required for the Real-time Inference recommendation architecture.
* Formulate the initial **Proposal** document (Section 2) and perform Cost Estimation ($91.34/month base estimate) using the AWS Pricing Calculator.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Complete FCAJ program onboarding & team alignment <br> - Review internship guidelines, workspace setup, and data security policies | 06/15/2026 | 06/15/2026 | AWS Internal Onboarding Docs |
| 3 | - Configure AWS CLI v2 and IAM developer profiles in `ap-southeast-1` <br> - Research AWS services for streaming app & ML inference: EC2, S3, DynamoDB, SageMaker | 06/16/2026 | 06/16/2026 | <https://docs.aws.amazon.com/cli/> |
| 4 | - Analyze The Movies Dataset (Kaggle/MovieLens) raw structures <br> - Define problem statement: information overload (15-20 min browsing time) vs proactive personalization | 06/17/2026 | 06/17/2026 | Kaggle Movies Dataset |
| 5 | - Design 4-layer solution architecture (Presentation, Application, Hot/Cold Data, ML Layer) <br> - Map AWS resources: EC2 (Vite + FastAPI), DynamoDB (Hot data), S3 (Cold data), SageMaker (Processing Jobs & Endpoints) | 06/18/2026 | 06/18/2026 | Proposal Solution Architecture |
| 6 | - Calculate infrastructure budget using AWS Pricing Calculator ($91.34/month total, including 24/7 `ml.m5.xlarge` endpoint & EC2) <br> - Draft Proposal document (Section 2) & risk matrix | 06/19/2026 | 06/19/2026 | <https://calculator.aws/> |

### Week 1 Achievements:

* Successfully established developer workstation credentials and verified AWS SDK connectivity via `aws sts get-caller-identity`.
* Finalized the 4-layer solution architecture for real-time recommendation inference on AWS.
* Completed the official **Proposal** document (Section 2) including executive summary, problem statement, risk assessment, and budget estimation.
