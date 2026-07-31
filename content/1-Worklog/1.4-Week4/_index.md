---
title: "Week 4 Worklog"
date: 2026-07-30
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives (Proposal Phase 1 & Phase 3 - Web Component):

* Design UI/UX and build the streaming Web interface on Vite (React + TypeScript).
* Build Register, Login, and Onboarding genre survey flows on Vite.
* Build complete **Interaction Pipeline**: capture implicit user events (`click`, `watch`, `rate`, `like`) from Frontend and save to `UserInteractions` table on DynamoDB.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Initialize Vite React/TypeScript frontend project structure and dark-mode styling tokens <br> - Build centralized `apiClient` service with auto JWT authorization header injection | 07/06/2026 | 07/06/2026 | Proposal Frontend Tech Specs |
| 3 | - Build Register, Login, and User Profile UI components <br> - Implement Genre Onboarding modal allowing new users to select their favorite movie categories | 07/07/2026 | 07/07/2026 | Proposal Onboarding Flow |
| 4 | - Build Movie Catalog grid, Movie Detail modal, and poster-based simulated playback player <br> - Connect Frontend state to backend `/api/v1/movies` metadata endpoints | 07/08/2026 | 07/08/2026 | Proposal Movie Detail Page |
| 5 | - Implement backend `UserInteractionsRepository` and `InteractionService` <br> - Connect Frontend interaction handlers (`click`, `watch >= 0.5`, `rate`, `like/dislike`, `share`) to `/api/v1/interactions` route | 07/09/2026 | 07/09/2026 | Proposal Interaction Pipeline Spec |
| 6 | - Configure `docker-compose.yml` to orchestrate React frontend (port 5173) and FastAPI backend (port 8000) <br> - Verify that interaction events write successfully into DynamoDB `UserInteractions` table | 07/10/2026 | 07/10/2026 | Proposal Docker Environment |

### Week 4 Achievements:

* Built modern, responsive Vite/React web application interface matching Proposal UI/UX requirements.
* Implemented Register/Login flows and Onboarding genre selection for new users.
* Successfully constructed the complete Interaction Pipeline, capturing 5 implicit user interaction types directly into DynamoDB `UserInteractions`.
* Configured local container environment via `docker-compose.yml` for unified frontend and backend deployment testing.
