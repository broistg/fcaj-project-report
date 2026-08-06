---
title: "Week 7 Worklog"
date: 2026-07-30
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives (Proposal Phase 4 - System Integration & Cloud Deployment):

* Integrate Machine Learning models into Backend workflow: Construct recommendation POST API (`/api/v1/recommend`) routing requests from Frontend to prediction server.
* Package AI models and integrate with **SageMaker Real-time Endpoint** (`InvokeEndpoint`) serving ultra-low latency 24/7 predictions backed by DynamoDB `RecommendationCache` fallback.
* Automate periodic model retraining via **SageMaker Processing Jobs** and deploy application containers to Amazon EC2 via GitHub Actions CI/CD.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Build backend recommendation POST API route (`/api/v1/recommend/{user_id}`) handling scenarios (`onboarding_user`, `returning_user`) <br> - Develop `SageMakerRecommendationProvider` calling `boto3.client('sagemaker-runtime')` | 07/20/2026 | 07/20/2026 | Proposal Phase 4 Integration |
| 3 | - Configure SageMaker Real-time Endpoint integration (`ml.m5.xlarge` instance) serving real-time 24/7 predictions <br> - Implement automated fallback logic: when Endpoint is overloaded/unavailable, automatically fallback to DynamoDB `RecommendationCache` / `PopularMovies` | 07/21/2026 | 07/21/2026 | Proposal SageMaker Endpoint Specs |
| 4 | - Automate model retraining process using SageMaker Processing Jobs (`scripts/run_processing_job.py`) reading historical interactions from S3 | 07/22/2026 | 07/22/2026 | Proposal Automated Retraining |
| 5 | - Provision Amazon EC2 (`t3.micro`) in Public Subnet of default VPC attached with IAM Instance Profile <br> - Write GitHub Actions workflow (`.github/workflows/deploy.yml`) executing SSH deploy and `docker compose up -d` | 07/23/2026 | 07/23/2026 | Proposal EC2 Deployment & CI/CD |
| 6 | - System integration testing verifying connectivity between EC2 containers, SageMaker Endpoint, DynamoDB, and S3 | 07/24/2026 | 07/24/2026 | Proposal Integration Testing |

### Week 7 Achievements:

* Built integrated recommendation backend API smoothly routing requests between React frontend and prediction server.
* Successfully integrated SageMaker Real-time Endpoint serving low-latency predictions with safe DynamoDB fallback mechanisms.
* Automated periodic model retraining tasks using SageMaker Processing Jobs.
* Configured GitHub Actions CI/CD pipeline automatically deploying application updates to Amazon EC2 server over SSH.
