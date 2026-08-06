---
title: "Week 3 Worklog"
date: 2026-07-30
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives (Proposal Phase 1):

* Provision AWS storage infrastructure: Amazon S3 bucket hierarchy and Amazon DynamoDB table schemas.
* Execute Machine Learning Data Pipeline pre-processing on raw Kaggle CSV dataset files.
* Split cleaned interaction dataset into Train, Validation, and Test sets for recommendation model training.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Provision Amazon S3 bucket in `ap-southeast-1` with S3 Lifecycle Rules (auto-delete old model artifacts after 30 days) <br> - Establish prefix directory layout (`datasets/raw/`, `datasets/processed/`, `models/`, `reports/`) | 06/22/2026 | 06/22/2026 | Proposal Data Layer Specs |
| 3 | - Design DynamoDB Hot Data schema: Primary Keys (PK) & Sort Keys (SK) <br> - Create `Movies` table (PK `movie_id`) and `PopularMovies` table (PK `list_id`, SK `rank`) on AWS | 06/23/2026 | 06/23/2026 | DynamoDB Developer Guide |
| 4 | - Create `Users` table (PK `user_id`), `UserInteractions` table (PK `user_id`, SK `interaction_key`), and `RecommendationCache` table | 06/24/2026 | 06/24/2026 | Proposal Database Requirements |
| 5 | - Write Python Data Pipeline script to pre-process raw Kaggle/MovieLens dataset <br> - Clean missing values, extract movie features, and map MovieLens IDs to TMDB catalog IDs | 06/25/2026 | 06/25/2026 | Pandas & Scikit-Learn Docs |
| 6 | - Split processed interaction records into Train/Validation/Test datasets based on timestamps <br> - Seed movie catalog items into DynamoDB `Movies` table and save pre-computed `PopularMovies` ranks | 06/26/2026 | 06/26/2026 | Python Boto3 Documentation |

### Week 3 Achievements:

* Successfully provisioned S3 Cold Storage Data with 7 logical partition prefixes and lifecycle lifecycle rules.
* Created 5 DynamoDB Hot Data tables on AWS strictly aligned with the Proposal schema design.
* Cleaned raw Kaggle movie datasets and uploaded Train/Validation/Test split artifacts to S3.
* Populated TMDB movie metadata into the `Movies` table and saved `PopularMovies` ranks computed with IMDb weighted formula.
