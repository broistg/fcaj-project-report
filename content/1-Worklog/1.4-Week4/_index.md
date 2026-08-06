---
title: "Week 4 Worklog"
date: 2026-07-30
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives (Proposal Phase 1 & Phase 3 - Baseline Models & API Contract):

* Develop baseline recommendation models: `PopularityRecommender` for unauthenticated guests and `ContentRecommender` (TF-IDF + Cosine Similarity) for onboarding survey users.
* Define the `BaseRecommendationProvider` ML interface contract with the Backend team to standardize prediction output integration.
* Build local testing suite for initial baseline recommendation models.

### Tasks Completed During the Week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Build `PopularityRecommender` module implementing the IMDb Weighted Rating formula $WR = \frac{v}{v+m}R + \frac{m}{v+m}C$ for guest fallback scenarios <br> - Package candidate retrieval logic | 06/29/2026 | 06/29/2026 | Popularity Baseline Algorithm |
| 3 | - Build `ContentRecommender` module extracting movie text features (overview, genres, keywords) using TF-IDF <br> - Compute Cosine similarity matrix between user onboarding genre preferences and movie catalog | 06/30/2026 | 06/30/2026 | Content-Based Filtering Algorithm |
| 4 | - Define the ML interface contract `BaseRecommendationProvider` specifying the `get_recommendations(user_id, k, context)` method <br> - Standardize recommendation result payloads (movie ID lists, confidence score, strategy tag) with Backend team | 07/01/2026 | 07/01/2026 | Backend & ML Interface Specs |
| 5 | - Construct local test runner (`tests/test_recommenders.py`) verifying recommendation candidate list generation for Popularity and Content-Based models <br> - Measure local inference response times | 07/02/2026 | 07/02/2026 | Python `unittest` Library |
| 6 | - Package baseline recommendation models into internal Python modules (`src/models/`) <br> - Write unit tests for input schema validation and recommendation format adherence | 07/03/2026 | 07/03/2026 | Python Module Structure |

### Week 4 Achievements:

* Completed initial baseline recommendation models: Popularity Ranker and Content-Based Recommender.
* Successfully finalized the `BaseRecommendationProvider` interface contract with the Backend engineering team.
* Packaged baseline models into `src/models/` and passed all local unit tests.
