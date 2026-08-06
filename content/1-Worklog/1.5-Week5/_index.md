---
title: "Week 5 Worklog"
date: 2026-07-30
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives (Proposal Phase 1 & Phase 3 - Web Component):

* Design basic UI/UX and build the movie web application frontend on Vite (React + TypeScript).
* Build Register, Login, and genre onboarding survey user flows on Vite.
* Implement a complete **Interaction Pipeline**: Capture interaction events (`click`, `watch`, `rate`, `like`) from Frontend and persist to DynamoDB `UserInteractions` table.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Initialize Vite React/TypeScript frontend project structure and dark-mode styling system <br> - Build centralized `apiClient` service automatically injecting JWT auth headers | 07/06/2026 | 07/06/2026 | Proposal Frontend Specs |
| 3 | - Build Register, Login, and personal Profile UI components <br> - Implement Onboarding modal allowing new users to select preferred movie genres | 07/07/2026 | 07/07/2026 | Proposal Onboarding Flow |
| 4 | - Construct movie catalog grid, Movie Details modal, and poster-based simulated video player <br> - Connect Frontend state to backend metadata APIs `/api/v1/movies` | 07/08/2026 | 07/08/2026 | Proposal Movie Detail Screen |
| 5 | - Implement backend `UserInteractionsRepository` and `InteractionService` <br> - Connect Frontend interaction handlers (`click`, `watch >= 0.5`, `rate`, `like/dislike`, `share`) to `/api/v1/interactions` route | 07/09/2026 | 07/09/2026 | Proposal Interaction Pipeline |
| 6 | - Configure `docker-compose.yml` packaging React frontend (port 5173) and FastAPI backend (port 8000) <br> - Test and verify interaction events successfully written to DynamoDB `UserInteractions` table | 07/10/2026 | 07/10/2026 | Proposal Docker Environment |

### Week 5 Achievements:

* Built modern, responsive Vite/React web interface fully satisfying Proposal UI/UX requirements.
* Completed user Register/Login flows and genre survey onboarding for new users.
* Successfully built Interaction Pipeline capturing 5 implicit interaction types directly to DynamoDB `UserInteractions`.
* Packaged local containerized environment via `docker-compose.yml` for integration testing.
