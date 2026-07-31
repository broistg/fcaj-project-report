---
title: "Week 2 Worklog"
date: 2026-07-30
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives (Proposal Phase 1):

* Provision AWS storage infrastructure: Amazon S3 bucket layout and Amazon DynamoDB table schemas.
* Execute Machine Learning data preprocessing pipeline on raw Kaggle CSV sources.
* Output cleaned dataset splits into Train, Validation, and Test sets for model training.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Provision Amazon S3 bucket in `ap-southeast-1` with S3 Lifecycle Rules (30-day artifact deletion) <br> - Establish prefix structure (`datasets/raw/`, `datasets/processed/`, `models/`, `reports/`) | 06/22/2026 | 06/22/2026 | Proposal Data Layer Spec |
| 3 | - Design DynamoDB Hot Data schemas: Primary Keys & Sort Keys <br> - Create `Movies` table (`movie_id` PK) and `PopularMovies` table (`list_id` PK, `rank` SK) on AWS | 06/23/2026 | 06/23/2026 | DynamoDB Developer Guide |
| 4 | - Create `Users` table (`user_id` PK), `UserInteractions` table (`user_id` PK, `interaction_key` SK), and `RecommendationCache` table | 06/24/2026 | 06/24/2026 | Proposal Database Requirements |
| 5 | - Build Python Data Pipeline to preprocess raw Kaggle/MovieLens CSV files <br> - Filter null values, extract movie features, and map MovieLens IDs to TMDB catalog IDs | 06/25/2026 | 06/25/2026 | Pandas & Scikit-Learn Docs |
| 6 | - Partition preprocessed interaction logs into Train/Validation/Test temporal splits <br> - Upload movie catalog records into DynamoDB `Movies` and pre-computed `PopularMovies` tables | 06/26/2026 | 06/26/2026 | Python Boto3 Documentation |

### Week 2 Achievements:

* Successfully provisioned S3 Cold Storage Data pipeline with 7 logical prefix zones and lifecycle policies.
* Created all 5 DynamoDB Hot Data tables on AWS matching exact Proposal key schemas.
* Preprocessed Kaggle movie datasets, outputting clean Train/Validation/Test split frames to S3.
* Uploaded TMDB catalog items to DynamoDB `Movies` and populated initial IMDb-weighted `PopularMovies` rankings.
