---
title: "Week 3 Worklog"
date: 2026-07-30
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives (Proposal Phase 1 & Phase 3 - Web Component):

* Build FastAPI backend framework, Docker environment, and AWS SDK composition layer (`app/container.py`).
* Build authentication flows: PBKDF2 password hashing, JWT (HS256) session validation, and onboarding genre selection.
* Develop movie catalog display APIs to retrieve metadata from DynamoDB `Movies` and `PopularMovies`.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Set up backend project structure, Docker containerization, and basic CI/CD pipeline foundation <br> - Initialize Pydantic configuration (`app/core/config.py`) and Boto3 AWS factory (`app/aws/infrastructure.py`) | 06/29/2026 | 06/29/2026 | Proposal Web Component Spec |
| 3 | - Build `PasswordHasher` class using PBKDF2-HMAC-SHA256 <br> - Build `JWTService` class for signing, validating, and expiring access tokens | 06/30/2026 | 06/30/2026 | FastAPI Security Guide |
| 4 | - Implement DynamoDB repositories (`UsersRepository`, `MoviesRepository`, `PopularMoviesRepository`) <br> - Build `/api/v1/auth/register`, `/login`, and `/me` routes | 07/01/2026 | 07/01/2026 | Proposal Authentication Requirements |
| 5 | - Develop `/api/v1/auth/onboarding` endpoint to store initial genre preferences for newly registered users <br> - Build `/api/v1/movies` metadata endpoints to fetch movie details from DynamoDB | 07/02/2026 | 07/02/2026 | Proposal Phase 3 Metadata APIs |
| 6 | - Implement startup health checks verifying AWS caller identity, DynamoDB key schemas, and S3 bucket access <br> - Write backend unit tests using `unittest` to ensure 100% route contract validity | 07/03/2026 | 07/03/2026 | Python `unittest` Framework |

### Week 3 Achievements:

* Built FastAPI backend architecture adhering strictly to Proposal presentation, application, and hot data layers.
* Implemented secure user authentication (PBKDF2 + JWT) validated against DynamoDB `Users` table.
* Developed movie metadata display APIs and guest browsing endpoints querying `PopularMovies` and `Movies`.
* Verified backend startup resource validation and passed all unit test assertions.
