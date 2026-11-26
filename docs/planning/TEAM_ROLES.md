# fresh-adventure — Team Roles and Responsibilities

## 1. Document Metadata

| Item | Value |
| --- | --- |
| Status | **PROPOSED — AWAITING TEAM APPROVAL** |
| Version | 0.3 |
| Date | 2026-11-26 |
| Team | 땅굴탐험대 (4 members) |
| Strategy baseline | [PTS v0.2 (approved)](PTS.md) — not modified by this document |
| References | [Proposal v3.1](../proposal/proposal_v3.1.md), [Proposal v3.3](../proposal/proposal_v3.3.md) — historical references, not modified; [Proposal v3.4](../proposal/proposal_v3.4.md) — latest planning reference (business analytics BA01–BA04) |
| Scope | Team organization and responsibility definition only. No MVP features, technologies, architecture, or milestone dates are decided here. |

Member names are listed in Korean alphabetical order (가나다순) throughout this document: 김민지, 김한승, 이선진, 지혜인.

---

## 2. Objectives

- Replace the "all members are PMs" structure with clearly separated roles.
- Give every member clear primary and secondary responsibilities, individual deliverables, and acceptance criteria.
- Distribute technical work so that implementation does not concentrate on one member.
- Define exactly one accountable owner for each concrete deliverable.
- Record unresolved responsibilities explicitly instead of assigning them by hierarchy.

---

## 3. Organizational Principles

1. **No all-members-PM structure.** Owning a workstream does not make a member a Project Manager.
2. **Role separation.** Team Leader, Project Manager, Product Planner, Presenter, Repository Administrator, and Domain Lead are distinct roles.
3. **Decision rule.** Major strategic decisions and scope changes require team agreement. If the team cannot reach agreement, the Team Leader (이선진) makes the final decision. The Team Leader is not automatically the Project Manager or Presenter.
4. **Career alignment guides, but does not limit, allocation.** Business, analytics, and engineering boundaries are not rigid.
5. **Repository lead ≠ sole implementer.** Repository leads coordinate and review; implementation is shared.
6. **One accountable owner per deliverable.** Shared workstreams are split into separate tasks.
7. **Strategy follows the approved PTS.** Conflicts with Proposal v3.3 are documented, not silently resolved (Section 14.7).
8. **Unconfirmed assignments remain TBD.**

---

## 4. Team Composition

| Member | Career direction | Primary role | Secondary role | Team positions |
| --- | --- | --- | --- | --- |
| 김민지 | BI Engineering | Data Engineering & BI Lead | Cloud & Integration | Product Planner (기획자); project idea originator |
| 김한승 | Data Analytics | Analytics & AI Lead | Backend Development | Repository Administrator |
| 이선진 | Business Management | Business Strategy Lead | Business Data Analyst | Team Leader (final decision when the team cannot agree) |
| 지혜인 | Marketing | Marketing & Product Experience Lead | Marketing Data Analyst / Frontend Development | Project Manager (Notion kanban board, weekly execution log) |

Project Manager: 지혜인. Presenter: **TBD** (Section 16).

---

## 5. Role Definitions

| Role | Definition |
| --- | --- |
| Team Leader | Represents the team, facilitates team agreement, and makes the final decision only when the team cannot reach agreement. No automatic authority over scheduling, presentation, or repository administration. |
| Project Manager | Manages the Notion kanban board (task owners, status, and progress tracking) and writes the weekly execution log. Schedule and scope changes still require team agreement. |
| Product Planner (기획자) | Owns product planning documents (proposal, PTS maintenance, future MVP/PRD drafting coordination). Changes to approved strategy still require team agreement and the PTS change-control process. |
| Repository Administrator | Owns repository structure, conventions, documentation consistency, and GitHub repository hygiene. Does not change permissions, visibility, or branch protection without team agreement. |
| Domain Lead | Owns a functional area (e.g., analytics, data engineering) and its quality. |
| Task Owner | Accountable for one concrete deliverable. |
| Contributor | Implements or supports a task owned by someone else. |
| Reviewer | Reviews deliverables or pull requests before acceptance. |
| Presenter | Delivers the team presentation. Q&A is supported by relevant domain owners. |

---

## 6. Individual Responsibilities

### 6.1 김민지 — Data Engineering & BI Lead

**Team positions:** Product Planner (기획자), project idea originator.

**Primary responsibilities**

- API collection architecture and data pipeline development
- ETL design and implementation; data integration
- Database modeling; data warehouse and data mart design
- Data quality management and data freshness monitoring
- Data contracts between data, backend, and frontend
- BI visualization; data accessibility for other members
- Product planning document ownership (Product Planner)

**Secondary responsibilities**

- Docker environment, cloud infrastructure, and deployment
- Service integration; frontend and backend integration support
- Operational monitoring

**Direct technical contributions:** collectors, ETL modules, schema, data marts, data quality checks.

**Credential management:** The existing arrangement is preserved — the Naver DataLab key is held and used by 김민지 only, on the server, subject to verified provider requirements. Restricted credentials are never shared or committed.

**Not assigned exclusively:** all frontend, backend, and AI implementation.

### 6.2 김한승 — Analytics & AI Lead

**Team position:** Repository Administrator.

**Primary responsibilities**

- Analytical methodology design and validation governance
- **Golden Time analysis** (primary analytical responsibility): consumer interest time series, seasonality and trend, Rising Point and Peak detection, Demand Lead Time
- Market price and cost-risk analysis
- Analytical baselines, backtesting, and model evaluation
- Evidence-based AI interpretation

**Secondary responsibilities**

- Backend development; analysis result APIs
- LLM integration, grounded AI responses, and AI response quality evaluation
- RAG or SQL-based retrieval — only if approved in the MVP phase
- Repository administration (structure, conventions, documentation consistency)

**Constraints:** AI work must not delay core analytical deliverables. No complex ML, RAG, or AI architecture without demonstrated necessity. Supports other members' methodologies but is not the exclusive implementer of all analyses.

### 6.3 이선진 — Business Strategy Lead

**Team position:** Team Leader. Makes the final decision when team opinions cannot be reconciled; otherwise decisions follow team agreement. No automatic PM, scheduling, presentation, or repository administration responsibility.

**Primary responsibilities**

- Market and industry analysis; business-oriented competitor analysis
- Business value proposition evaluation; business-perspective requirements
- Fresh food pricing analysis and market price comparison
- Product cost structure, profitability, break-even, and procurement cost sensitivity analysis
- Business hypothesis validation and business interpretation of analytical results

**Secondary responsibilities**

- Business data analysis (market size and growth, price comparison, cost and profit scenarios)

**Additional business analytics (v0.2)**

| ID | Workstream | Priority | Schedule | 이선진's ownership |
| --- | --- | --- | --- | --- |
| BA01 | Cost Data Quality Assessment (Proposal v3.4 §5-10) | P0 | Weeks 2 and 4 | Define business-oriented validation rules; conduct the assessment; review excluded records; document findings and limitations |
| BA02 | Promotion Profitability Assessment (§4-3 ↔ §4-4) | P1 | Week 4 | Own profitability assumptions and calculations; implement and validate the analysis; produce promotion-level results |
| BA03 | Wholesale Price Decomposition (§4-4) | P1 — Conditional | Pilot by 2026-12-13; Week 4 only if approved | Own the business analysis and decomposition implementation; interpret principal contributing grades; document business implications |
| BA04 | Historical Weekly Margin Opportunity Analysis (§4-4) | P2 — Optional | Week 5 only if capacity permits | Own the analysis if executed; otherwise record it as a future extension |

Governance for BA01–BA04:

- Raw records are preserved; exclusions are flagged with reasons and counts. Data errors are distinguished from analytical scope exclusions. Imported products are not treated as invalid data. Genuine market price spikes are preserved.
- Observed market prices are distinguished from assumed operating costs. KAMIS wholesale prices are procurement cost proxies; KAMIS retail prices are market reference prices.
- Profit figures are scenario-based, not statistically validated prediction intervals and not actual retailer outcomes.
- Profitability warnings support user judgment and never automatically exclude promotion candidates.
- Decomposition results do not prove causal relationships.
- The implementation of these workstreams stays with 이선진; collaborators support data, methods, and integration only.

**Direct analytical contributions:** market size and growth analysis, market price analysis, cost and profitability calculation logic, sales volume and profit scenarios, break-even calculations, cost sensitivity analysis.

**Schedule-linked business tasks (Proposal v3.4 Section 10)**

| Week | Tasks |
| --- | --- |
| Week 0 | Proposal sharing; Naver AI-usage inquiry |
| Week 1 | Scope confirmation; first-demonstration scope confirmation (team agreement); cost default research |
| Week 2 | Sample product configurations (3); cost defaults and sources; promotion score weights and calculation (owner pending R9); BA01 KAMIS validation for sample products; BA03 pilot (cabbage, apple) |
| Week 3 | Verification of scores and figures on integrated screens (12/14–15); first-demonstration materials |
| Week 4 | First-feedback plan; validation-result interpretation frame; BA01 expansion; BA02; BA03 full analysis if approved |
| Week 5 | Final presentation material draft; BA04 only if capacity permits |
| Week 6 | Rehearsal and material finalization |

Technical implementation support may come from other members; ownership of business analysis deliverables stays with 이선진.

### 6.4 지혜인 — Marketing & Product Experience Lead

**Team position:** Project Manager.

- Manages the Notion kanban board: task owners, status, due dates, and progress tracking.
- Writes the weekly execution log in `docs/weekly/` using the existing template; members update their own tasks before the weekly meeting.
- Facilitates weekly progress review. Schedule and scope changes require team agreement; unresolved disagreements go to the Team Leader.

**Primary responsibilities**

- Target-user research; MD and marketer interviews
- Customer interest analysis; product and keyword selection
- Seasonal, holiday, and event interest analysis
- Marketing and promotion strategy
- Product experience design, user journeys, dashboard wireframes, user testing

**Secondary responsibilities**

- Frontend development; marketing-related dashboard components; analytical result visualization
- AI report content and marketing interpretation support
- Demonstration scenario development

**Direct analytical contributions:** gender, age, and device interest patterns; seasonal and holiday interest changes; marketing and promotion interpretation.

**Constraint:** Demographic shares are not calculated unless the source data supports valid cross-segment comparison (PTS DA1).

---

## 7. Primary and Secondary Responsibilities (Summary)

| Member | Primary | Secondary | Individual technical/analytical contribution |
| --- | --- | --- | --- |
| 김민지 | Data Engineering & BI; Product Planning | Cloud & Integration | Pipeline, ETL, schema, marts, data quality |
| 김한승 | Analytics & AI | Backend; Repository Administration | Golden Time analysis, cost risk, baselines, backend APIs |
| 이선진 | Business Strategy | Business Data Analysis | Market size, price comparison, cost and profitability model, BA01–BA04 business analytics |
| 지혜인 | Marketing & Product Experience; Project Management | Marketing Data Analysis; Frontend | Customer interest and seasonal analysis, frontend components, kanban board, weekly execution logs |

---

## 8. Analytical Ownership Matrix

These are potential workstreams, **not approved MVP features**. Where two names appear as owners, the workstream is split into separate tasks with one accountable owner each.

| Workstream | Accountable owner | Collaborator(s) |
| --- | --- | --- |
| Market size and growth | 이선진 | 김민지 |
| Consumer interest trends | 김한승 | 지혜인 |
| Customer interest characteristics | 지혜인 | 김한승 |
| Seasonal and holiday analysis | 지혜인 | 김한승 |
| Golden Time analysis | 김한승 | 지혜인 |
| Marketing preparation strategy | 지혜인 | 김한승 |
| Promotion strategy | 지혜인 | 이선진 |
| Market price comparison | 이선진 | 김민지 |
| Cost and profitability analysis | 이선진 | 김한승 |
| Cost risk analysis | 김한승 | 이선진 |
| Data collection and integration | 김민지 | All members |
| Data quality validation | 김민지 | All members |
| Analytical methodology validation | 김한승 | Domain owners |
| AI-assisted interpretation | 김한승 | 지혜인 |
| Business value validation | 이선진 | All members |
| User value validation | 지혜인 | All members |


**Business analytics collaboration (v0.2)**

| Workstream | Accountable owner | Collaborator(s) |
| --- | --- | --- |
| Cost data validation rules | 이선진 | 김민지 |
| Cost data quality assessment | 이선진 | 김민지 |
| Pipeline validation implementation | 김민지 | 이선진 |
| Promotion profitability calculation | 이선진 | 김한승 |
| Golden Time analytics | 김한승 | 지혜인 |
| Cost risk analytics | 김한승 | 이선진 |
| Wholesale price decomposition | 이선진 | 김한승, 김민지 |
| Historical margin analysis | 이선진 | 김한승 |
| Marketing interpretation | 지혜인 | 이선진, 김한승 |
| Backend integration | 김한승 | 김민지 |
| Dashboard integration | Relevant FE and BI owners (one accountable owner per screen, assigned in the MVP phase) | Analytical owners |

Business analysis ownership (이선진), data engineering (김민지), analytical methodology review (김한승), and application integration (FE/BE/BI owners) are kept separate.

Separation of concerns: business interpretation (이선진, 지혜인), analytical implementation (김한승 and domain owners), and data engineering (김민지) are owned separately.

---

## 9. Repository Ownership

The four-repository architecture is preserved. No permissions, visibility, branch protection, or GitHub settings are changed by this document.

| Repository | Visibility | Lead | Contributors | Responsibilities |
| --- | --- | --- | --- | --- |
| `fresh-adventure` | Public | 김한승 (Repository Administrator) | All members | Shared documentation, product strategy, requirements, research reports, project records, weekly logs, collaboration documentation |
| `fresh-adventure-data` | Private | 김민지 | All members | Data collection, ETL, preprocessing, analytical modules, data quality, data contracts, analytical result generation |
| `fresh-adventure-be` | Private | 김한승 | 김민지 (technical collaborator) | Backend APIs, analytical result serving, business logic, AI service integration, backend tests |
| `fresh-adventure-fe` | Public | 지혜인 | 김민지 and analytical owners | Web interface, dashboard components, user experience, analytical visualization, API integration, frontend tests |

- **Repository Administrator (김한승):** repository structure, conventions, and documentation consistency across all four repositories. Content ownership stays with each repository lead and task owner.
- **Repository leads** coordinate contributions and review changes; they are not required to implement every component.

---

## 10. Shared Responsibilities

| Responsibility | Assignment |
| --- | --- |
| Team Leader | 이선진 (final decision when the team cannot agree) |
| Product Planner (기획자) | 김민지 |
| Repository Administration | 김한승 |
| Project Manager | 지혜인 |
| Task and schedule tracking (Notion kanban board) | 지혜인 |
| Weekly execution log | 지혜인 (members provide updates) |
| Risk management (risk register) | **TBD** (not included in the defined PM scope; to confirm) |
| Product planning input | All members (documents owned by the Product Planner) |
| Major strategic decisions and scope changes | Team agreement; Team Leader decides if agreement cannot be reached |
| Presentation material preparation | All members |
| Presenter | **TBD** |
| Demonstration and Q&A | Relevant domain owners |
| Cross-functional quality review | All members |

---

## 11. RACI Matrix

R = Responsible, A = Accountable, C = Consulted, I = Informed. Each row has exactly one A. Rows marked TBD have no confirmed accountable owner.

| Task | 김민지 | 김한승 | 이선진 | 지혜인 |
| --- | --- | --- | --- | --- |
| Project management (Notion kanban board) | C | C | C | A/R |
| Weekly execution log | C | C | C | A/R |
| Final decision when agreement cannot be reached | C | C | A/R | C |
| Product strategy (planning documents) | A/R | C | C | C |
| Market research | I | I | A/R | C |
| User research | I | I | C | A/R |
| Competitor analysis | C | I | A/R | C |
| Customer interest analysis | I | C | I | A/R |
| Golden Time analysis | C | A/R | I | C |
| Seasonal analysis | I | C | I | A/R |
| Marketing strategy | I | C | C | A/R |
| Promotion strategy | I | C | C | A/R |
| Pricing analysis | C | I | A/R | I |
| Profitability analysis | I | C | A/R | I |
| Cost-risk analysis | C | A/R | C | I |
| Data collection | A/R | R | I | C |
| Data preprocessing | A/R | R | I | I |
| Database design | A/R | C | I | I |
| Data mart development | A/R | C | C | I |
| BA01 Cost data validation rules and assessment | C | C | A/R | I |
| BA01 Pipeline validation implementation | A/R | I | C | I |
| BA02 Promotion profitability assessment | C | C | A/R | C |
| BA03 Wholesale price decomposition (conditional) | C | C | A/R | I |
| BA04 Historical weekly margin analysis (optional) | I | C | A/R | I |
| Analytical validation | C | A/R | C | C |
| AI integration | C | A/R | I | C |
| Backend development | R | A/R | I | I |
| Frontend development | R | C | C | A/R |
| Infrastructure and deployment | A/R | C | I | I |
| Integration testing | A/R | R | C | R |
| Documentation (structure and consistency) | R | A/R | R | R |
| Repository administration | I | A/R | I | I |
| Presentation material | R | R | R | R |
| Presentation delivery | C | C | C | C |

**TBD accountable owners**

| Task | Accountable | Responsible |
| --- | --- | --- |
| Presentation material | **TBD** | All members |
| Presentation delivery | **TBD** (Presenter) | **TBD** |

Notes:

- Data collection: 김한승 is listed as R for selected non-DataLab collectors, subject to feasibility confirmation. DataLab calls remain with 김민지 only.
- Data preprocessing: 김한승 is R for analysis-specific preprocessing; shared preprocessing stays with 김민지.
- Integration testing: proposed A is 김민지 (integration secondary role); repository leads are R for their components.

---

## 12. Individual Deliverables

| Member | Deliverable | Type |
| --- | --- | --- |
| 김민지 | API collection pipeline | Technical |
| 김민지 | ETL modules | Technical |
| 김민지 | Database schema and data mart documentation | Technical / documentation |
| 김민지 | Data quality reports | Analytical |
| 김민지 | Data contracts | Documentation |
| 김민지 | Pipeline implementation of approved BA01 validation rules (reproducible, with data lineage) | Technical |
| 김민지 | BI dashboard contributions | Technical |
| 김민지 | Infrastructure and deployment documentation | Documentation |
| 김민지 | Product planning documents (proposal maintenance, MVP/PRD drafting coordination) | Documentation |
| 김한승 | Golden Time analytical methodology | Analytical |
| 김한승 | Time-series analysis notebooks and modules | Analytical / technical |
| 김한승 | Cost-risk analysis | Analytical |
| 김한승 | Baseline comparison results and analytical validation report | Analytical |
| 김한승 | Backend contributions (analysis result APIs) | Technical |
| 김한승 | Evidence-grounded AI evaluation | Analytical / technical |
| 이선진 | Market and business analysis report | Analytical |
| 이선진 | Pricing analysis report | Analytical |
| 이선진 | Cost and profitability model | Analytical |
| 이선진 | Business validation report | Analytical |
| 이선진 | Business decision-support documentation | Documentation |
| 이선진 | BA01 Cost data quality assessment report, validation rule specification, exclusion and warning summary, reproducible validation code, cost data readiness assessment | Analytical / technical |
| 이선진 | BA02 Representative product configurations (15), profitability calculation module, promotion candidate profitability assessment, break-even and margin analysis, calculation validation report | Analytical / technical |
| 이선진 | BA03 Cabbage and apple pilot, price and mix effect results, grade-level contributions, methodology and limitations report, adoption or deferral recommendation (conditional) | Analytical |
| 이선진 | BA04 Historical weekly margin scenario analysis (optional) | Analytical |
| 지혜인 | User research report | Research |
| 지혜인 | Customer interest analysis | Analytical |
| 지혜인 | Seasonal and holiday analysis | Analytical |
| 지혜인 | Marketing strategy report and promotion planning framework | Strategy |
| 지혜인 | Product experience documentation (journeys, wireframes) | Design |
| 지혜인 | Frontend contributions | Technical |
| 지혜인 | Notion kanban board (maintained) and weekly execution logs | Project management |

---

## 13. Deliverable Acceptance Criteria

General criteria for every deliverable:

- Stored in the correct repository and path, with a named owner.
- Data sources, time ranges, and assumptions are stated.
- Unverified results are labeled as such (PTS evidence classification).
- Reviewed by at least one other member before acceptance.

Deliverable-specific criteria (thresholds to be agreed before testing, per PTS Section 14):

| Deliverable | Acceptance criteria |
| --- | --- |
| API collection pipeline | Re-runnable for agreed sources; raw responses stored; failures logged; no credentials in code |
| ETL modules and schema | Documented schema; code mapping applied; tests for core transformations |
| Data quality reports | Coverage, missing rates, and freshness reported per source and product |
| Data contracts | Columns, types, units, and delivery format agreed by producer and consumer |
| Golden Time methodology | Definitions consistent with PTS Section 8; evaluation products, baselines, and metrics predefined |
| Baseline comparison and validation report | Seasonal baselines compared; temporal consistency and no data leakage; negative results reported |
| Cost-risk analysis | Compared with simple baselines; presented as a guardrail, not an exclusion rule |
| Backend contributions | Endpoints documented; tests pass; no secrets |
| AI evaluation | Responses grounded in result tables; DataLab derived indicators only |
| Market, pricing, and profitability deliverables | Formulas documented; user-entered assumptions labeled; outputs presented as estimates |
| BA01 Cost data quality | Every rule has counts and reasons; raw records preserved; data errors vs. scope exclusions distinguished; genuine price spikes retained; re-runnable code |
| BA02 Promotion profitability | Hand-checked example calculations; non-positive contribution margin and invalid assumptions return defined warnings; default selling price uses only comparable KAMIS retail observations; outputs labeled scenario-based; no automatic exclusion |
| BA03 Wholesale price decomposition | Price + mix (+ interaction) reconciles with observed change; residuals reported separately; grade definitions and coverage documented; adoption decided at Decision Item 6 |
| BA04 Historical margin | Off-season values not filled with zero; benchmarks from comparable seasonal periods; labeled as a historical cost-driven scenario |
| User research report | Concrete recent examples per PTS B1–B5; majority agreement not treated as product-market fit |
| Customer interest and seasonal analysis | DA1 comparability checked before demographic shares are calculated |
| Frontend contributions | Matches approved wireframes; charts cite data sources; no secrets in the public repository |
| Kanban board and weekly execution logs | One log per week in `docs/weekly/` using `_template.md`; kanban shows current owner and status for every active task; no credentials or restricted data in Notion or logs |
| Infrastructure documentation | Reproducible setup steps; cost controls documented |

---

## 14. Workload and Dependency Assessment

### 14.1 Assumptions

- Individual skill levels and available working hours have **not been confirmed**.
- Effort levels below are qualitative estimates (S/M/L) based on task scope, not measured data.
- Proposal v3.3 workload percentages are **not reused**.
- No claim is made that workloads are balanced.

### 14.2 Estimated Effort by Member (qualitative)

| Member | Large (L) | Medium (M) | Small (S) |
| --- | --- | --- | --- |
| 김민지 | Data pipeline and ETL (all sources); deployment | Schema and marts; data quality; integration support; product planning documents | Docker setup; credential handling |
| 김한승 | Golden Time analysis and validation | Cost-risk analysis; backend APIs; AI integration | Repository administration |
| 이선진 | BA01 cost data quality (P0); BA02 promotion profitability | Market analysis; cost and profitability model; business validation; BA03 pilot | Pricing comparison; BA04 (optional, only with spare capacity) |
| 지혜인 | Frontend development (if confirmed) | User research; customer interest and seasonal analysis; wireframes; project management (kanban, weekly logs) | Keyword selection |

### 14.3 Concentration Risks

1. **김민지 carries the critical path and the most roles** (data engineering lead, cloud and deployment, integration support, Product Planner, sole DataLab caller). Every downstream analysis and screen depends on her pipeline.
2. **김한승 combines analytics lead, backend lead, AI integration, and repository administration.** Golden Time analysis is the core product value and must not be delayed by backend or AI work.
3. **Technical feasibility is unconfirmed** for business analysis implementation (이선진), frontend development (지혜인), backend development (김한승), AI integration (김한승), data pipeline development (김민지), and cloud deployment (김민지).
4. **이선진's Week 2 and Week 4 load increased (v0.2).** Week 2 already holds sample product configurations, cost defaults, and promotion score preparation; BA01 (KAMIS validation) and the BA03 pilot are added before the 12/13 result-table deadline and first-demonstration preparation. Week 4 combines BA01 expansion, BA02 (15 configurations), and BA03 full analysis if approved, during the 12/25 holiday week.
5. **BA dependencies.** BA03 depends on cleaned settlement data from 김민지; Proposal v3.3/v3.4 allows settlement history loading to slip after the first demonstration, which would leave the pilot without data by 12/13. BA02 depends on approved promotion candidate outputs and result contracts.
6. **지혜인 combines the Project Manager role with marketing lead and frontend secondary work (v0.3).** Kanban and weekly-log duties recur every week, including demonstration weeks.

### 14.4 Critical Path and Dependencies

```text
Product and keyword selection (지혜인)
        │
        ▼
Code mapping (지혜인, 김한승) ──► Data collection and ETL (김민지)
                                        │
                                        ▼
                          Data marts and data contracts (김민지)
                                        │
              ┌─────────────────────────┼─────────────────────────┐
              ▼                         ▼                         ▼
   Golden Time / cost risk    Market, price, profitability   Customer interest
        (김한승)                     (이선진)                     (지혜인)
              └─────────────────────────┼─────────────────────────┘
                                        ▼
                            Result tables (per data contract)
                                        │
                     ┌──────────────────┴──────────────────┐
                     ▼                                     ▼
              Backend APIs (김한승)                Frontend (지혜인)
                     └──────────────────┬──────────────────┘
                                        ▼
                       Integration testing (김민지) ──► Demonstration
```

### 14.5 Recommendations

- Split collectors by source so that 김한승 (and others, if feasible) can implement non-DataLab collectors under 김민지's review.
- Keep deployment minimal until the final phase; prioritize local demonstration.
- Share product planning drafting: section owners write their sections; 김민지 consolidates.
- Confirm skill levels and weekly available hours in the first team meeting; if capacity is insufficient, reduce scope rather than concentrate work.
- If business analytics capacity is insufficient: (1) defer BA04, (2) defer BA03 beyond the pilot, (3) simplify BA02 while keeping its business purpose. BA01 and core analytical validation are preserved. Milestone dates are not changed without approval.

### 14.6 Milestone Alignment (Proposal v3.3/v3.4, not changed here)

| Milestone (v3.3) | Dependency / risk |
| --- | --- |
| 12/6 data confirmation (products, code mapping, collectors, DB design, result table spec) | Depends on 지혜인 product selection and 김민지 pipeline; data contract must be agreed by all producers and consumers |
| 12/13 final result tables | Analytical owners deliver in parallel; 김민지 must have marts ready |
| 12/13 Decision Item 6 (BA03 adoption) | Requires settlement data for cabbage and apple; same date as result-table delivery |
| 12/14–15 integration and testing | Requires backend and frontend owners available; integration testing owner proposed as 김민지 |
| 12/18 first demonstration | See conflicts below |
| 12/27 feature completion, 1/3 feature freeze | Depends on MVP scope not yet defined |
| 1/6 final presentation and submission | Conflicts with the 2027-01-07 period end and 2027-01-08 competition date recorded elsewhere; must be reconciled before a roadmap is approved |

### 14.7 Conflicts with the Approved PTS (documented, not resolved here)

| Area | Proposal v3.3 | Approved PTS v0.2 |
| --- | --- | --- |
| First demonstration focus | Main (interest surge, promotion Top 5 score), demand trends, cost and profitability; marketing timing shown as "in preparation" | Core value is Golden Time Discovery and marketing/promotion timing |
| Promotion score | Fixed-weight scoring and Top 5 ranking | Ranking and scoring formulas not approved; deferred to MVP/PRD |
| Cost risk | Filters products to exclude from promotions | Guardrail, not automatic exclusion |
| Target | Includes large-mart online channels | Small and mid-sized retailers exposed to inventory risk |
| Promotion profitability (BA02) | Attached to the promotion Top 5 display | Promotion ranking and scoring are not approved in the PTS; BA02 display scope must be decided in the MVP phase |
| Promotion candidate ownership | v3.3/v3.4 schedule assigns promotion score calculation to business (이선진); BA02 expects candidate outputs from 김한승 | Not defined in the PTS; owner must be decided (R9) |
| Role structure | All four members act as PMs; team leader owns schedule, final decisions, and presentation | Superseded by this document once approved |

---

## 15. Collaboration and Handoff Rules

1. **Data contracts first.** Producers and consumers agree on columns, types, units, and delivery format before implementation.
2. **Result tables are the handoff.** Analytical owners deliver result tables; backend and frontend serve and display them without re-implementing analysis.
3. **Pull requests.** Work on branches; at least one reviewer per pull request; repository leads review their repositories.
4. **Credentials.** DataLab calls only by 김민지 on the server; others request data and use loaded results. No credentials in any repository.
5. **Methodology support.** 김한승 supports difficult methods (change-point detection, cross-correlation) for other owners, who keep ownership of their deliverables.
6. **Decisions.** Domain owners decide within their domain; cross-domain and scope decisions require team agreement. If agreement cannot be reached, the Team Leader (이선진) decides. Decisions are recorded in the decision register (Section 16).
7. **Weekly sync.** Members update their tasks on the Notion kanban board; the Project Manager (지혜인) writes the weekly execution log in `docs/weekly/`.

---

## 16. Unassigned Responsibilities (Decision Register)

| ID | Decision | Status | Notes |
| --- | --- | --- | --- |
| R1 | Project Manager | **Decided (2026-11-26): 지혜인** | Scope: Notion kanban board and weekly execution log. Risk management not yet assigned |
| R2 | Presenter | **TBD** | Q&A supported by domain owners |
| R3 | Presentation material accountable owner | **TBD** | Preparation shared by all members |
| R4 | Scope of Repository Administrator | To confirm | Proposed: all four repositories (structure and conventions); content ownership stays with repository leads |
| R5 | Scope of Product Planner (기획자) | To confirm | Proposed: product planning document ownership; not Project Manager; strategic changes require team agreement |
| R6 | Member skill levels and weekly available hours | **TBD** | Required for workload validation |
| R7 | Collector split across members | **TBD** | Depends on R6 |
| R8 | Final submission and competition dates | **TBD** | 1/6 (Proposal v3.3) vs. 1/7–1/8 (README, PTS) |
| R9 | Owner of promotion candidate scoring outputs used by BA02 | **TBD** | 이선진 (v3.3/v3.4 schedule) vs. 김한승 (BA02 input specification) |
| R10 | BA03 adoption (Proposal v3.4 Decision Item 6) | Due 2026-12-13 | Based on cabbage and apple pilot findings |

---

## 17. Risks and Mitigation

| Risk | Impact | Mitigation |
| --- | --- | --- |
| Pipeline delay blocks all analyses and screens | High | Early data contracts; split collectors; sample extracts for parallel work |
| Golden Time analysis delayed by backend or AI work | High | Analytics deliverables prioritized over AI features |
| Frontend or backend skills insufficient | High | Confirm in first meeting; simplify scope; pair with collaborators |
| Project Manager workload on top of marketing lead and frontend work (지혜인) | Medium | Members update their own kanban tasks; weekly log uses the existing template; reassess at the first-demonstration retrospective |
| Role overlap between Product Planner and Team Leader | Medium | Clarify R5; record decisions in the register |
| Business analysis implementation support unavailable | Medium | Spreadsheet- or SQL-level implementation first; 김한승 supports methods |
| Business analytics overload in Weeks 2 and 4 | High | Apply BA reduction order; decide BA03 strictly from pilot results |
| BA03 pilot lacks settlement data by 12/13 | Medium | Prioritize cabbage and apple settlement history; otherwise defer BA03 |
| Credentials concentrated on one member | Medium | Document request process; keep server-side access |

---

## 18. Team Approval Requirements

### 18.1 Decisions to Approve

| ID | Decision |
| --- | --- |
| T1 | Abolish the all-members-PM structure |
| T2 | Role assignments in Section 4 |
| T3 | Analytical ownership matrix (Section 8) |
| T4 | Repository ownership (Section 9) |
| T5 | RACI matrix (Section 11) |
| T6 | Individual deliverables and acceptance criteria (Sections 12–13) |
| T7 | Resolution of R1–R10 (may be approved separately) |
| T8 | Business analytics responsibilities BA01–BA04 and their priorities |

| Member | Approval | Date |
| --- | --- | --- |
| 김민지 | ☐ | |
| 김한승 | ☐ | |
| 이선진 | ☐ | |
| 지혜인 | ☐ | |

### 18.2 References Requiring Update After Approval

These are **not modified** until this document is approved.

| Reference | Required update |
| --- | --- |
| Proposal v3.4 Sections 1, 10, 11 | Already reflect this proposal as "pending approval"; update the status note after approval (v3.3 remains unchanged as a historical document) |
| `README.md` (main) | Add team roles or link to this document |
| `AGENTS.md` / `CLAUDE.md` (all repositories) | Role and ownership rules in the next phase |
| Future MVP, PRD, roadmap, and milestone documents | Use this document for ownership |

---

## 19. Change History

| Version | Date | Changes |
| --- | --- | --- |
| 0.1 | 2026-11-26 | Initial proposal: removed all-members-PM structure; separated Team Leader, Project Manager, Product Planner, Presenter, and Repository Administrator; assigned Product Planner (김민지) and Repository Administrator (김한승); PM and Presenter left TBD; names ordered by 가나다 |
| 0.2 | 2026-11-26 | Added business analytics BA01–BA04 to 이선진 (priorities P0/P1/conditional P1/optional P2); added collaboration matrix, RACI rows, deliverables, and acceptance criteria; updated workload risks, milestone alignment (Decision Item 6), conflicts (R9), and decision register (R9, R10); fixed Section 6 subsection numbering. Other members' roles unchanged; status remains PROPOSED |
| 0.3 | 2026-11-26 | Assigned Project Manager to 지혜인 (Notion kanban board, weekly execution log); Team Leader 이선진 makes the final decision when the team cannot agree; added 이선진's schedule-linked tasks from Proposal v3.4; updated role definitions, shared responsibilities, RACI, deliverables, acceptance criteria, workload, collaboration rules, decision register (R1), and risks. Presenter and risk management remain TBD; status remains PROPOSED |
