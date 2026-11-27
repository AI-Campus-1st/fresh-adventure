# fresh-adventure — Decision Log

| Field | Value |
| --- | --- |
| Document | DECISION_LOG.md |
| Version | 0.2 |
| Status | PROPOSED |
| Last Updated | 2026-11-27 |
| Approved by | Pending |
| Approval Date | Pending |
| Document Owner | 김한승 |
| Project | fresh-adventure |
| Team | 땅굴탐험대 |
| Scope | Project-wide product, analytical, technical, and governance decisions |

## 1. Purpose

This log records significant project decisions, their rationale, impact, and approval status.

- Each decision has a unique, permanent ID (`D-001`, `D-002`, ...). IDs are never reused.
- Decisions are not deleted. A replaced decision is marked `SUPERSEDED` and references its successor.
- Status values follow RULES.md: `DRAFT`, `PROPOSED`, `APPROVED`, `SUPERSEDED`.
- Detailed architecture decisions may be documented as ADRs in [`docs/adr/`](adr/) and referenced here.
- A decision becomes effective only after approval under the approved team governance structure ([TEAM_ROLES.md](planning/TEAM_ROLES.md)).

## 2. Decision Index

| ID | Title | Date | Status | Related Documents |
| --- | --- | --- | --- | --- |
| D-001 | AI Coding Tools and Agent Context Architecture | 2026-11-27 | PROPOSED | [RULES.md](../RULES.md) §8, TEAM_ROLES.md v0.6 §6, §14 |
| D-002 | Repository and Documentation Architecture | 2026-11-27 | PROPOSED | [RULES.md](../RULES.md) §7, §9, §11, TEAM_ROLES.md v0.6 §5.2, §6 |

## 3. Decisions

### D-001 — AI Coding Tools and Agent Context Architecture

| Field | Value |
| --- | --- |
| Date | 2026-11-27 |
| Status | PROPOSED |
| Proposed by | 김한승 |
| Approved by | Pending |
| Approval Date | Pending |

#### Decision

- Claude Code is the designated AI-assisted development tool for fresh-adventure.
- Codex and other AI coding tools are not currently used. Introducing another AI coding tool requires an approved decision.
- Each repository maintains `CLAUDE.md` as its authoritative AI execution protocol.
- `AGENTS.md` is retained as a minimal compatibility document and does not authorize the use of additional AI coding tools.

#### Rationale

- Align the context architecture with the team's actual development workflow.
- Reduce duplicated instructions and maintenance overhead.
- Preserve future agent compatibility.
- Maintain consistent security and authorization safeguards.

#### Alternatives Considered

| Alternative | Outcome |
| --- | --- |
| Use Claude Code and Codex in parallel | Not adopted — requires maintaining two full instruction sets and increases the risk of conflicting agent behavior. |
| Remove `AGENTS.md` entirely | Not adopted — a minimal compatibility file preserves future agent compatibility at negligible maintenance cost. |

#### Impact

- Upon approval, this decision supersedes earlier AI coding tool assumptions concerning Codex in TEAM_ROLES v0.6.
- Workload estimates in TEAM_ROLES v0.6 assumed both tools. They are not invalidated by this decision, as AI productivity assumptions were not validated at approval.
- TEAM_ROLES v0.6 §6 states that `docs/SHARED_CONTEXT.md` is referenced by the local `AGENTS.md`. Under this decision, it is referenced by `CLAUDE.md`.
- All unrelated team responsibilities and approved decisions remain unchanged.

#### Follow-up

- [ ] Migrate valid existing instructions from `AGENTS.md` into `CLAUDE.md` in all four repositories.
- [ ] Reduce `AGENTS.md` to essential compatibility instructions.
- [ ] Eliminate circular references between `CLAUDE.md` and `AGENTS.md`.
- [ ] Reflect this decision in the next approved revision of TEAM_ROLES.md.


### D-002 — Repository and Documentation Architecture

| Field | Value |
| --- | --- |
| Date | 2026-11-27 |
| Status | PROPOSED |
| Proposed by | 김한승 |
| Accepted for implementation | 김한승 (document owner), 2026-11-27 |
| Approved by | Pending (project lead) |
| Approval Date | Pending |

#### Decision

- Preserve the four independent sibling repositories. No submodules, monorepo, or parent repository.
- Place `RULES.md` at the main repository root, next to `README.md` and `CLAUDE.md`.
- Place cross-cutting governance documents at the `docs/` root: `conventions.md`, `DECISION_LOG.md`, and a security guide when established.
- Keep the existing domain folders in `docs/`. Do not create `docs/requirements/` or `docs/archive/`; `docs/planning/` already covers requirements, and `docs/proposal/` and Git history cover archival.
- Follow the document consolidations approved in TEAM_ROLES v0.6 §5.2 (FUNCTIONS and BUSINESS_METRICS in PRD, DATA_DICTIONARY in DATA_SPEC, VALIDATION in ANALYTICS).
- Create documents only when their phase begins. Do not create empty placeholder documents.
- Keep the existing code skeletons (`fresh-adventure-data/src/fresh_adventure_data/`, `fresh-adventure-be/app/`, `fresh-adventure-fe/src/`) as provisional until TECHSTACK is approved.
- Restrict Claude Code access to secret-bearing files with a committed `.claude/settings.json` in each repository.
- Create `docs/SHARED_CONTEXT.md` in the Data, Backend, and Frontend repositories after RULES.md is approved and committed, so that it can reference a real source commit.

#### Document Placement

| Folder | Documents |
| --- | --- |
| `docs/planning/` | PTS, TEAM_ROLES, MARKET_RESEARCH, COMPETITOR_ANALYSIS, DATA_FEASIBILITY, MVP, PRD, PERSONA / USER_SCENARIO |
| `docs/architecture/` | TECHSTACK, ARCHITECTURE, AI_CONTEXT |
| `docs/data/` | DATA_SPEC, ERD |
| `docs/analytics/` | ANALYTICS, BUSINESS_ANALYTICS, MARKETING_ANALYTICS, PROMOTION_STRATEGY |
| `docs/contracts/` | DATA_CONTRACT, API_SPEC |
| `docs/design/` | DESIGN (UX, design system, BI visualization section) |
| `docs/testing/` | TEST_PLAN, AI_EVALUATION (unless merged with AI_CONTEXT), USER_TEST |
| `docs/management/` | ROADMAP |
| `docs/adr/`, `docs/deployment/` | Kept; used only when needed |

Owners follow TEAM_ROLES v0.6 §5. Whether PERSONA and USER_SCENARIO, or AI_CONTEXT and AI_EVALUATION, become one file is decided by their owners when created.

#### Rationale

- The existing domain folders are already documented in the main README. A phase-based tree would conflict with the README definition of `docs/design/` (UI/UX).
- Moving uncommitted governance documents now has no history cost.
- Fewer files and no placeholders reduce maintenance for a four-person team.

#### Alternatives Considered

| Alternative | Outcome |
| --- | --- |
| Phase-based folders (`requirements/`, technical `design/`) | Not adopted — conflicts with existing folders and the README, and requires moving approved documents. |
| Rename code skeletons to `src/` in Backend and Frontend | Not adopted — renaming adds churn without benefit before TECHSTACK. |

#### Follow-up

- [ ] Project lead approval of RULES.md, D-001, and D-002.
- [ ] Create `docs/SHARED_CONTEXT.md` in the Data, Backend, and Frontend repositories after RULES.md is committed.
- [ ] Decide the name and location of the security guide (`docs/SECURITY.md` is shown by GitHub as the repository security policy).
- [ ] Review `fresh-adventure-be/app/` and `fresh-adventure-fe/src/` structures when TECHSTACK is approved.

---

## Revision History

| Version | Date | Status at Revision | Description |
| --- | --- | --- | --- |
| 0.1 | 2026-11-27 | PROPOSED | Initial decision log with D-001 (AI coding tools and agent context architecture). |
| 0.2 | 2026-11-27 | PROPOSED | Moved to `docs/`, added the TEAM_ROLES §6 impact to D-001, and added D-002 (repository and documentation architecture). |
