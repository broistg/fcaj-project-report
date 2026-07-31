---
title: "Week 6 Worklog"
date: 2026-07-30
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives (Proposal Phase 4 - System Integration & Cloud Deployment):

* Integrate Machine Learning model into Backend process: Build POST recommendation API (`/api/v1/recommend`) routing Frontend requests to prediction server.
* Package AI model and integrate with **SageMaker Real-time Endpoint** (`InvokeEndpoint`) to serve 24/7 low-latency predictions with DynamoDB `RecommendationCache` fallback.
* Set up automation for the periodic model re-training process via **SageMaker Processing Jobs** and deploy application containers to Amazon EC2 via GitHub Actions CI/CD.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Build backend POST recommendation API route (`/api/v1/recommend/{user_id}`) to handle scenario hints (`onboarding_user`, `returning_user`) <br> - Develop `SageMakerRecommendationProvider` calling `boto3.client('sagemaker-runtime')` | 07/20/2026 | 07/20/2026 | Proposal Phase 4 Integration |
| 3 | - Configure SageMaker Real-time Endpoint integration (`ml.m5.xlarge` instance) serving real-time predictions 24/7 <br> - Implement automatic fallback mechanism: if endpoint is unavailable, fall back to DynamoDB `RecommendationCache` / `PopularMovies` | 07/21/2026 | 07/21/2026 | Proposal SageMaker Endpoint Spec |
| 4 | - Automate model retraining process via SageMaker Processing Jobs (`scripts/run_processing_job.py`) reading historical interaction data from S3 | 07/22/2026 | 07/22/2026 | Proposal Re-train Automation |
| 5 | - Provision Amazon EC2 (`t3.micro`) inside default VPC Public Subnet with IAM Instance Profiles <br> - Write GitHub Actions workflow (`.github/workflows/deploy.yml`) executing SSH deployment and `docker compose up -d` | 07/23/2026 | 07/23/2026 | Proposal EC2 & CI/CD Deployment |
| 6 | - Conduct integration tests verifying EC2 container communication with SageMaker Endpoint, DynamoDB, and S3 | 07/24/2026 | 07/24/2026 | Proposal System Integration Test |

### Week 6 Achievements:

* Built backend recommendation integration API routing requests seamlessly between React frontend and prediction servers.
* Integrated SageMaker Real-time Endpoint client offering low-latency recommendation serving backed by DynamoDB cache fallbacks.
* Automated periodic batch retraining jobs using SageMaker Processing Jobs.
* Configured automated GitHub Actions CI/CD pipeline deploying application updates to Amazon EC2 via SSH.
