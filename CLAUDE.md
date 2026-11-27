# CLAUDE.md — fresh-adventure

Authoritative AI execution protocol for this repository (decision D-001). Claude Code is the designated AI coding tool.

## Repository

- Name: `fresh-adventure` (Public)
- Role: Main repository — project planning, governance, shared documentation, shared data and API contracts, and deliverables.
- This repository is public. Never add credentials, restricted datasets, NAVER DataLab values, or private repository internals.

## Read Before Work

Read the documents relevant to the task. Do not load everything by default.

| Document | Purpose |
| --- | --- |
| [RULES.md](RULES.md) | Project-wide governance and quality standards |
| [docs/planning/PTS.md](docs/planning/PTS.md) | Product strategy, target users, Golden Time definition |
| [docs/planning/TEAM_ROLES.md](docs/planning/TEAM_ROLES.md) | Responsibilities and document ownership |
| [docs/DECISION_LOG.md](docs/DECISION_LOG.md) | Significant decisions (D-001, D-002, ...) |
| [docs/conventions.md](docs/conventions.md) | Branch, commit, PR, secret, and data-file rules |

## Essential Rules

1. Classify each task by risk level (RULES.md §4). Level 3 work requires explicit human approval before execution. When uncertain, use the higher level.
2. Never commit, push, merge, or deploy without explicit authorization. Commit authorization does not imply push authorization.
3. Never read, print, copy, or summarize actual secret values. Do not open `.env` or other secret-bearing files. Use non-disclosing checks (file existence, variable presence).
4. Do not install dependencies or initialize frameworks until the technology stack (TECHSTACK) is approved.
5. Do not change the approval status (`DRAFT`, `PROPOSED`, `APPROVED`, `SUPERSEDED`) of any document. Approval is a human decision.
6. Do not treat drafts, proposals, or AI-generated suggestions as approved decisions. Check each document's Status field.
7. Do not duplicate definitions owned by another document (for example, Golden Time in PTS §8). Link to the source instead.
8. Report actual results only. Never fabricate file contents, data, test results, or completion status. Report failures and limitations.
9. Preserve unrelated work and other contributors' changes. Inspect the branch and working tree before editing.
10. Follow Git conventions in the main repository's `docs/conventions.md`.

## Repository-Specific Rules

- Place documents according to D-002 (Document Placement). Create a document only when its phase begins. Do not create empty placeholder documents.
- Use English for new technical and governance documents. Keep the root `README.md` and existing Korean documents in Korean.
- Governance and specification documents carry a metadata table (Version, Status, Approved by, Approval Date) and a Revision History.
- Never modify historical proposals in `docs/proposal/`. Add new versions as new files and update `docs/proposal/README.md`.
- When approved shared context changes, identify affected repositories and update their `docs/SHARED_CONTEXT.md` through pull requests (TEAM_ROLES §6).
