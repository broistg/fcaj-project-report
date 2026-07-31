---
title: "Week 7 Worklog"
date: 2026-07-30
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives (Proposal Phase 5 - Testing & Optimization):

* Review the entire system across 3 core user scenarios (Guest browsing, New user onboarding, Returning user recommendations), handle errors, and measure real-world performance.
* Optimize page load times, DynamoDB query speeds, and recommendation cache efficiency.
* Monitor AWS costs against budget guardrails ($91.34/month estimate) and finalize Workshop documentation (Section 5) & personal internship report.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Conduct comprehensive system review across Unauthenticated Guest, New User Onboarding, and Returning User recommendation scenarios <br> - Test fallback mechanisms: verify system degrades gracefully to DynamoDB `PopularMovies` if SageMaker endpoint is offline | 07/27/2026 | 07/27/2026 | Proposal Testing & Fallback Spec |
| 3 | - Measure real-world performance: optimize Vite page load times, DynamoDB batch query latency (`BatchGetItem`), and cache TTL settings <br> - Verify cross-data validation: ensure movie IDs returned by model exist in DynamoDB catalog | 07/28/2026 | 07/28/2026 | Proposal Performance Optimization |
| 4 | - Audit AWS cost monitoring: verify AWS Budgets alerts (50% and 75% thresholds) and S3 Lifecycle Rules (auto-deleting old model versions after 30 days) <br> - Review IAM least-privilege policies and CloudWatch log groups | 07/29/2026 | 07/29/2026 | Proposal Budget & Risk Mitigation |
| 5 | - Update system Architecture Diagram (v2.0 / `diagram.png`) reflecting VPC, EC2, DynamoDB, S3, SageMaker, IAM, CloudWatch, and AWS Budgets <br> - Complete Section 5 Workshop documentation in both English and Vietnamese | 07/30/2026 | 07/30/2026 | Workshop Report Section 5 |
| 6 | - Complete personal Worklog (Week 1 to Week 7), verify Hugo site build locally, clean up template warnings, and publish final report | 07/31/2026 | 07/31/2026 | Personal Report Finalization |

### Week 7 Achievements:

* Reviewed the entire system across all user scenarios, proving instant personalization and zero cold-start latency via SageMaker Real-time Endpoints.
* Optimized page load times and DynamoDB query speeds while enforcing cross-data validation assertions.
* Confirmed AWS Budgets cost guardrails ($91.34/month) and S3 lifecycle rules preventing unexpected storage cost blowouts.
* Completed personal internship report (`fcaj-project-report`), synchronized Workshop documentation, removed template warnings, and published deliverables.
