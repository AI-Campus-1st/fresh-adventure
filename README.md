# fresh-adventure

Main repository of the fresh-adventure capstone project (AI-Campus-1st).

| Item | Value |
| --- | --- |
| Project name | fresh-adventure |
| Product name | fresh-adventure |
| Team name | 땅굴탐험대 |
| Product category | Fresh Food Marketing Intelligence |
| Core value | Golden Time Discovery |

## Project Overview

fresh-adventure is a planned fresh food marketing intelligence product for merchandising managers and marketers at small and mid-sized online fresh food retailers.
It aims to combine external market data (Naver DataLab, KOSIS, KAMIS, public wholesale markets, KMA weather, customs, special-day data)
to identify potential sales golden windows and support proactive marketing and promotion timing, while flagging products with cost-related risk.
See the approved PTS baseline: [docs/planning/PTS.md](docs/planning/PTS.md) (v0.2, approved 2026-11-26).

All functionality described here is **planned**. The latest proposal ([docs/proposal/proposal_v3.1.md](docs/proposal/proposal_v3.1.md)) uses the former working title "FreshLens".

| Item | Value |
| --- | --- |
| Project period | 2026-11-24 – 2027-01-07 |
| Final competition | 2027-01-08 |
| Team size | 4 |

## Repository Directory

| Repository | Visibility | Responsibility |
| --- | --- | --- |
| [fresh-adventure](https://github.com/AI-Campus-1st/fresh-adventure) | Public | Project documentation, management, shared contracts, deliverables |
| [fresh-adventure-data](https://github.com/AI-Campus-1st/fresh-adventure-data) | Private | Data ingestion, preprocessing, analytics, validation, loading |
| [fresh-adventure-fe](https://github.com/AI-Campus-1st/fresh-adventure-fe) | Public | User interface, dashboard, data visualization |
| [fresh-adventure-be](https://github.com/AI-Campus-1st/fresh-adventure-be) | Private | API services, database access, business logic, AI/LLM integration |

Private repositories are accessible to team members only.

## Responsibility Boundaries

- **fresh-adventure (this repository):** approved documentation, project management, shared architecture specifications,
  shared data and API contracts, weekly reports, architecture decision records (ADRs), and public deliverables.
  It must not contain production application code, credentials, or restricted datasets.
- **fresh-adventure-data:** collects and processes data and produces analytical result tables. Raw data is not tracked in Git.
- **fresh-adventure-be:** serves analytical results through APIs and integrates AI/LLM features. It does not re-implement analytics.
- **fresh-adventure-fe:** presents dashboards and visualizations. It holds no secrets and calls external services only through the backend.

## Documentation Navigation

| Path | Contents |
| --- | --- |
| [docs/proposal/](docs/proposal/) | Project proposals by version (latest: v3.1) |
| [docs/planning/](docs/planning/) | PTS definition, scope, schedule, and requirements |
| [docs/architecture/](docs/architecture/) | System architecture specifications |
| [docs/data/](docs/data/) | Data sources, schemas, and data dictionary |
| [docs/analytics/](docs/analytics/) | Analytical methodology and metric definitions |
| [docs/contracts/](docs/contracts/) | Shared data and API contracts between repositories |
| [docs/design/](docs/design/) | UI/UX design and wireframes |
| [docs/management/](docs/management/) | Meeting notes, roles, and project management |
| [docs/weekly/](docs/weekly/) | Weekly reports |
| [docs/adr/](docs/adr/) | Architecture decision records |
| [docs/testing/](docs/testing/) | Test strategy and validation reports |
| [docs/deployment/](docs/deployment/) | Deployment and operations guides |
| [docs/conventions.md](docs/conventions.md) | Branch, commit, PR, and secret management conventions |
| [assets/](assets/) | Diagrams, screenshots, and branding assets |
| [deliverables/](deliverables/) | Presentations, reports, and retrospective |

## Current Status

- Phase 01 — repository initialization and directory structure setup (in progress).
- No application features, data pipelines, or analytical results have been implemented yet.
- The frontend and backend technology stacks are pending team approval.

## Security

This is a **public** repository. Never commit API keys, `.env` files, credentials, raw datasets, or Naver DataLab values.
