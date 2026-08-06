---
title: "Week 8 Worklog"
date: 2026-07-30
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives (Proposal Phase 5 - ML System Testing, Fallback Verification & Report Finalization):

* Conduct end-to-end ML system testing across 3 main user scenarios (Unauthenticated guest, New onboarding user, Returning user personalized recommendations).
* Test and verify safe Fallback mechanisms (DynamoDB `RecommendationCache` / `PopularMovies`) during SageMaker Endpoint downtime or network failure.
* Optimize ML inference latency, monitor AWS SageMaker budget ($91.34/month base estimate), and finalize Workshop documentation (Section 5) & Machine Learning Engineer internship report.

### Tasks Completed During the Week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Review end-to-end ML system across 3 user scenarios: Unauthenticated guest (Popularity Ranker), New user onboarding (Content-Based), and Returning user (Implicit ALS / Hybrid RRF via SageMaker Endpoint) <br> - Measure recommendation output quality | 07/27/2026 | 07/27/2026 | ML User Scenario Testing |
| 3 | - Test safe Fallback mechanisms: simulate SageMaker Endpoint downtime or network disconnects <br> - Verify backend automatically falls back to reading DynamoDB `RecommendationCache` and `PopularMovies` without disrupting user experience | 07/28/2026 | 07/28/2026 | Proposal Fallback Specs |
| 4 | - Measure and optimize ML inference latency: streamline JSON request/response payload size, cache short-term recommendation lists in DynamoDB `RecommendationCache` <br> - Audit Movie ID consistency between ML model matrices and database catalogs | 07/29/2026 | 07/29/2026 | ML Inference Latency Optimization |
| 5 | - Audit AWS SageMaker budget governance: verify AWS Budgets alert thresholds ($91.34/month) <br> - Confirm S3 Lifecycle Rules automatically clean up old model weight artifacts after 30 days to prevent hidden storage costs | 07/30/2026 | 07/30/2026 | Proposal Cloud Cost Governance |
| 6 | - Update ML Architecture Diagram (v2.0), finalize Workshop documentation (Sections 5.1 through 5.6) for both English and Vietnamese versions <br> - Complete personal Machine Learning Engineer Worklog (Week 1 to Week 8) and publish final report | 07/31/2026 | 07/31/2026 | ML Engineer Report Finalization |

### Week 8 Achievements:

* Successfully verified end-to-end ML recommendation system across all 3 real-world user scenarios.
* Confirmed reliable operation of safe Fallback mechanisms via DynamoDB `RecommendationCache` and `PopularMovies`.
* Optimized ML inference latency, ensured Movie ID data consistency, and verified AWS Budgets thresholds ($91.34/month).
* Completed personal Machine Learning Engineer internship report (`fcaj-project-report`), Workshop Section 5 documentation, and published final report.
