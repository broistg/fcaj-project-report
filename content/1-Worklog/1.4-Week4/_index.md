---
title: "Week 4 Worklog"
date: 2026-07-30
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives (Proposal Phase 1 & Phase 3 - Web Component):

* Build the FastAPI backend framework, Docker container environment, and AWS SDK dependency management layer (`app/container.py`).
* Implement authentication flows: PBKDF2 password hashing, JWT session authentication (HS256), and genre survey onboarding.
* Develop movie catalog display APIs to retrieve metadata from DynamoDB `Movies` and `PopularMovies` tables.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Set up backend project structure, Docker containerization, and basic CI/CD foundation <br> - Initialize Pydantic configuration (`app/core/config.py`) and Boto3 AWS factory (`app/aws/infrastructure.py`) | 06/29/2026 | 06/29/2026 | Proposal Web Component Specs |
| 3 | - Develop `PasswordHasher` class using PBKDF2-HMAC-SHA256 algorithm <br> - Develop `JWTService` class for signing, verifying, and managing access token expiration | 06/30/2026 | 06/30/2026 | FastAPI Security Guide |
| 4 | - Implement DynamoDB repositories (`UsersRepository`, `MoviesRepository`, `PopularMoviesRepository`) <br> - Build authentication routes `/api/v1/auth/register`, `/login`, and `/me` | 07/01/2026 | 07/01/2026 | Proposal Authentication Requirements |
| 5 | - Develop `/api/v1/auth/onboarding` endpoint to store genre preferences for newly registered users <br> - Build metadata endpoints `/api/v1/movies` to retrieve movie details from DynamoDB | 07/02/2026 | 07/02/2026 | Proposal Phase 3 Metadata APIs |
| 6 | - Add startup health checks to verify AWS identity, DynamoDB schemas, and S3 access <br> - Write backend unit test suite using `unittest` to ensure strict API contract adherence | 07/03/2026 | 07/03/2026 | Python `unittest` Library |

### Week 4 Achievements:

* Successfully built FastAPI backend architecture following the Presentation, Application, and Hot Data layer design.
* Implemented secure user authentication system (PBKDF2 + JWT) verifying user credentials against DynamoDB `Users` table.
* Completed movie metadata display APIs and guest browsing flow backed by DynamoDB `PopularMovies` and `Movies`.
* Verified startup AWS resource integrity and passed all unit test suits.
