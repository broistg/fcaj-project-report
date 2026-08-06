---
title: "Week 3 Worklog"
date: 2026-07-30
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives (Proposal Phase 1 - ML Data Infrastructure):

* Provision S3 storage hierarchy for ML Datasets & Model Artifacts with specialized logical partition prefixes.
* Specify DynamoDB table schemas for ML interaction data collection (`UserInteractions`).
* Develop Python Data Pipeline script pre-processing raw Kaggle CSV datasets and exporting temporal Train/Validation/Test splits.

### Tasks Completed During the Week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Provision Amazon S3 bucket in `ap-southeast-1` with S3 Lifecycle Rules (auto-delete old model artifacts after 30 days) <br> - Establish specialized ML directory prefix structure (`datasets/raw/`, `datasets/processed/`, `models/`, `reports/`) | 06/22/2026 | 06/22/2026 | Proposal Data Layer Specs |
| 3 | - Define DynamoDB schema requirements for ML Data Ingestion: specify `UserInteractions` table (PK `user_id`, SK `interaction_key`) storing implicit events <br> - Specify `Movies` table (PK `movie_id`) schema for movie metadata | 06/23/2026 | 06/23/2026 | DynamoDB Developer Guide |
| 4 | - Specify requirements for DynamoDB `PopularMovies` table (PK `list_id`, SK `rank`) storing IMDb weighted popularity candidates for cold-start fallback | 06/24/2026 | 06/24/2026 | Proposal Database Requirements |
| 5 | - Write Python Data Pipeline script (`src/data/preprocess.py`) to pre-process raw Kaggle/MovieLens datasets <br> - Clean missing values, map MovieLens IDs to TMDB catalog IDs, and extract text/genre features | 06/25/2026 | 06/25/2026 | Pandas & Scikit-Learn Docs |
| 6 | - Execute temporal Train/Validation/Test splitting on interaction dataset <br> - Compute `PopularMovies` baseline rankings and upload cleaned datasets to S3 storage | 06/26/2026 | 06/26/2026 | Python Boto3 Documentation |

### Week 3 Achievements:

* Successfully provisioned S3 ML Storage with 7 logical partition prefixes and model lifecycle rules.
* Specified standardized DynamoDB schemas for `UserInteractions`, `Movies`, and `PopularMovies` required for ML training ingestion.
* Developed Python Data Pipeline cleaning raw Kaggle datasets, resolving catalog ID mapping, and uploading Train/Validation/Test splits to S3.
