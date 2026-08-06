---
title: "Week 8 Worklog"
date: 2026-07-30
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives (Proposal Phase 5 - Testing & Optimization):

* Review the entire system across 3 main user scenarios (Guest movie browsing, New user onboarding, Returning user recommendations), resolve errors, and measure real-world performance.
* Optimize page load times, DynamoDB query speeds, and recommendation caching efficiency.
* Monitor AWS costs against budget limits ($91.34/month base estimate) and finalize Workshop documentation (Section 5) & personal internship report.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Comprehensive system review across scenarios: Unauthenticated guest, New user genre selection onboarding, and Returning user personalized recommendations <br> - Test fallback mechanisms: verify system automatically reverts to DynamoDB `PopularMovies` if SageMaker endpoint is turned off | 07/27/2026 | 07/27/2026 | Proposal Testing & Fallback Specs |
| 3 | - Real-world performance measurements: optimize Vite page loading, DynamoDB batch query latency (`BatchGetItem`), and cache TTL <br> - Verify data integrity: ensure all movie IDs recommended by the model exist in DynamoDB `Movies` catalog | 07/28/2026 | 07/28/2026 | Proposal Performance Optimization |
| 4 | - Audit AWS cost monitoring: verify AWS Budgets alerts (50% and 75% thresholds) and S3 Lifecycle Rules (auto-delete old model weights after 30 days) <br> - Review principle of least privilege IAM policies and CloudWatch log groups | 07/29/2026 | 07/29/2026 | Proposal Risk Mitigation & Budget |
| 5 | - Update System Architecture Diagram (v2.0 / `diagram.png`) illustrating VPC, EC2, DynamoDB, S3, SageMaker, IAM, CloudWatch, and AWS Budgets <br> - Finalize Workshop documentation (Sections 5.1 through 5.6) for both English and Vietnamese versions | 07/30/2026 | 07/30/2026 | Workshop Section 5 Specs |
| 6 | - Complete personal Worklog (Week 1 to Week 8), verify Hugo site build locally, clean up template warnings, and publish final report | 07/31/2026 | 07/31/2026 | Personal Report Finalization |

### Week 8 Achievements:

* Successfully reviewed the entire system across all user scenarios, demonstrating real-time personalization via SageMaker Real-time Endpoints.
* Optimized page load times and DynamoDB query speeds while guaranteeing strict data integrity between model predictions and database.
* Verified AWS Budgets thresholds ($91.34/month) and S3 Lifecycle Rules, mitigating cloud cost explosion risks.
* Completed personal internship report (`fcaj-project-report`), synchronized Workshop documentation, cleaned up template warnings, and published final report.
