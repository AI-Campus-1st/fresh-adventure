# fresh-adventure — Team Roles, Context Ownership, and Workload

## 1. Document Metadata

| Item | Value |
| --- | --- |
| Status | **APPROVED** |
| Version | 0.6 |
| Date | 2026-11-26 |
| Approved by | Project lead |
| Approval date | 2026-11-26 |
| Document owner | 김한승 |
| Team | 땅굴탐험대 (4 members) |
| Strategy baseline | [PTS v0.2 (approved)](PTS.md) — not modified |
| Planning reference | [Proposal v3.4](../proposal/proposal_v3.4.md) (latest; Proposal Owner: 김민지). Proposals v3.1–v3.4 are not modified |
| Verified state | Main repository at `e49cf95` (= `origin/main`) with TEAM_ROLES v0.5 as the only uncommitted change (revised here to v0.6); data `0b45bb2`, backend `e206e51`, frontend `65fd007`, all clean |
| Scope | Team organization, context ownership, BI/frontend boundaries, responsibility audit, and workload reassessment. No MVP features, technologies, architecture, or milestone dates are decided here |

Member names are listed in Korean alphabetical order (가나다순): 김민지, 김한승, 이선진, 지혜인.

### 1.0 What v0.6 Changes

1. **이선진:** responsibilities preserved; no new mandatory analytics.
2. **지혜인:** marketing analysis made explicit as four reproducible workstreams (MA01–MA04); promotion opportunity scoring proposed as the R9 resolution (not approved).
3. **김민지:** BI work extended with analytical depth (BI01–BI04), counted as incremental effort over existing profiling, modeling, chart, and validation tasks.
4. **김한승:** existing core analytics, planning, context engineering, backend, AI, and repository responsibilities preserved; adds methodology review of the new domain analyses.
5. **Delivery model:** workload reassessed under AI-assisted development (Claude Code, Codex) with explicit productivity scenarios; human accountability preserved.

### 1.1 What v0.5 Corrected

1. **Baseline correction.** Product planning and context engineering (PTS, MVP, PRD, AI master prompt, RULES, CLAUDE, AGENTS, README, repository structure) were **existing responsibilities of 김한승**, not work transferred from 김민지. v0.4 §14.4 reported "≈ 31 h product planning transferred out of 김민지"; that statement is withdrawn. The v0.4 baseline (scenario A) also undercounted 김한승 by omitting this work.
2. **Role realignment.** 김민지's direction is BI Engineering and Data Visualization. Her primary role becomes **BI & Data Visualization Lead** with direct ownership of visualization implementation; collectors, backend support, cloud, and end-to-end integration are reassessed.

### 1.2 Evidence Inspected (2026-11-26)

| Item | Evidence | Status |
| --- | --- | --- |
| Four repositories, folder structure, templates, conventions | Commits by han0210 (김한승): `f7a4dc9`, `7050e7d`, `6e02254`, `22eb34d`, `0b45bb2`, `06c587d`, `e206e51`, `1b2995c`, `577a65c` | Completed |
| README (main and repositories) | `f7a4dc9`, `bf8a45b`, `67850a8`, `65fd007` | Completed (maintenance remains) |
| PTS v0.1–v0.2 | `bf8a45b`; status APPROVED | Completed (maintenance remains) |
| TEAM_ROLES v0.1–v0.4 | `e49cf95` (v0.3); v0.4 uncommitted | Completed; v0.5 in progress |
| Root and repository AGENTS.md / CLAUDE.md | Phase 01 placeholders in all repositories | In progress |
| RULES.md, DATA_FEASIBILITY.md, MVP.md, PRD.md, DECISION_LOG.md, ROADMAP.md, research documents | Not found | Not started |
| AI master role prompt | Referenced in Phase 01 instructions; not stored in any repository | **UNKNOWN** (treated as not completed) |
| Proposals v3.1–v3.4 | Files in `docs/proposal/`, committed by 김한승; content authorship not verifiable from Git | Completed (effort not attributed) |
| API call tests (proposal §5-2) | Referenced as `api_check/api_check_report.md`; not in any repository | Completed per proposal; evidence outside repositories |
| Application, analysis, BI, or frontend code | Package skeletons only | Not started |
| December 1 planning presentation | Not found in any document | Unverified (R12) |

---

## 2. Team Organization

### 2.1 Organizational Responsibilities

| Member | Organizational responsibility |
| --- | --- |
| 김민지 | Proposal Owner; project idea originator |
| 김한승 | Product Planning & Context Engineering Owner; Repository Administrator |
| 이선진 | Team Leader (final decision only when the team cannot reach agreement) |
| 지혜인 | Project Manager (Notion kanban, progress tracking, weekly execution log) |
| Presenter | **TBD** |

Governance: the all-members-PM structure stays abolished; the Team Leader is not automatically PM or Presenter; major strategic decisions and scope changes require team agreement, with the Team Leader deciding only if agreement cannot be reached; **document ownership does not grant strategic approval authority**.

### 2.2 Role Structure

| Member | Primary role | Secondary role | Additional responsibility |
| --- | --- | --- | --- |
| 김민지 | **BI & Data Visualization Lead** | **Data Engineering & Data Modeling** | Proposal Owner |
| 김한승 | Analytics & AI Lead | Product Planning & Backend Development | Context Engineering; Repository Administration |
| 이선진 | Business Strategy Lead | Business Data Analyst | Team Leader |
| 지혜인 | Marketing & Product Experience Lead | Marketing Data Analytics & Frontend Development | Project Manager |

Change from v0.4: 김민지's primary role was Data Engineering & BI Lead with Cloud & Integration as secondary. Cloud and end-to-end integration are no longer part of her default role (Section 8.3).

### 2.3 Ownership Types

| Type | Responsibility |
| --- | --- |
| Document Owner | Authorship, maintenance, completeness, and versioning |
| Domain Owner | Professional accuracy and feasibility in the domain |
| Implementation Owner | Delivery of the component |
| Reviewer | Review before acceptance |
| Approver | Team agreement (Team Leader decides if agreement cannot be reached); PTS changes follow PTS change control |

---

## 3. Responsibility Baseline: Existing vs. New

| Responsibility | Owner | Classification | Status | Remaining work |
| --- | --- | --- | --- | --- |
| Project execution framework, repositories, folder structure | 김한승 | Existing responsibility | Completed | None (maintenance in P09) |
| README | 김한승 | Existing responsibility | Completed | Maintenance |
| PTS | 김한승 | Existing responsibility | Completed (v0.2 approved) | Maintenance under change control |
| TEAM_ROLES | 김한승 | Existing responsibility | Completed (v0.6 approved) | Maintenance under change control |
| AI master role prompt | 김한승 | Existing responsibility | UNKNOWN | Store in repository (P07) |
| RULES.md, root CLAUDE.md/AGENTS.md, context standards | 김한승 | Existing responsibility | In progress (placeholders) / not started (RULES) | P06 |
| DATA_FEASIBILITY.md | 김한승 | Existing responsibility | Not started | P02 |
| MVP.md, PRD.md (incl. functions, business metrics) | 김한승 | Existing responsibility | Not started | P03, P04 |
| ANALYTICS, TEST_PLAN, API_SPEC, AI_CONTEXT, AI_EVALUATION, DECISION_LOG | 김한승 | Existing responsibility (documented in v0.4) | Not started | H01, H07, H10–H12, P09 |
| Backend database access layer | 김한승 | **Newly transferred** from 김민지 (v0.4 placement) | Not started | H09 |
| BI visualization section, chart components, visualization validation | 김민지 | **Newly introduced** for 김민지 (previously inside frontend scope of 지혜인) | Not started | V01–V05 |
| Wholesale settlement collector | 이선진 | **Newly transferred** from 김민지 (pilot scope in C) | Not started | D08p |
| AWS deployment, end-to-end integration coordination | **TBD** | **Newly unassigned** (removed from 김민지's default role) | Not started | D23, D22 (R21, R22) |
| Frontend charts | 김민지 | Transferred from 지혜인's v0.4 frontend scope | Not started | V03, V04 |
| BA04, BA03 full, two nonessential collectors, separate FUNCTIONS/BUSINESS_METRICS/VALIDATION/DATA_DICTIONARY files, WBS.md | — | Deferred or eliminated (C) | — | — |
| MA01–MA02 (customer interest segmentation, event analysis) | 지혜인 | **Expanded** existing analyses (J04, J05) | Not started | Incremental effort only |
| MA03 marketing timing decision rules | 지혜인 | **Clarified** (proposal §11 '마케팅 적기 분석'; not estimated before) | Not started | New estimate |
| MA04 promotion opportunity scoring | 지혜인 (proposed) | **Previously unassigned** (R9); not a transfer from 김한승 | Not started | Conditional on MVP |
| BI01–BI04 (EDA, semantic model, integrated visual analytics, reconciliation) | 김민지 | **New (incremental)** over profiling, marts, charts; BI04 replaces V05 | Not started | Incremental effort only |
| Methodology review of MA/BI handoffs | 김한승 | **New** (small) | Not started | ≈ 3 h |

---

## 4. Individual Responsibilities

### 4.1 김민지 — BI & Data Visualization Lead, Proposal Owner

- **BI and visualization (primary):** analytical dashboard design; BI data modeling and visualization marts; KPI visualization; chart selection and visual encoding; reusable chart components; chart-level filters and interactions; visualization data integration.
- **BI analytics (v0.6):**

| ID | Analytical question | Methods | Data | Validation | Deliverables | Effort classification |
| --- | --- | --- | --- | --- | --- | --- |
| BI01 Exploratory data analysis and visual profiling | What distributions, anomalies, coverage differences, and patterns exist across the integrated datasets? | Descriptive statistics, distributions, missing-value exploration, variability, visual anomaly exploration, product and period comparison | Integrated marts (all sources) | Reuses common data quality outputs; distinct from BA01 (business cost rules), cost-risk modeling (김한승), and marketing analysis (지혜인) | Reproducible EDA notebook, profiling results, visual findings, BI data-readiness notes | **Incremental** over common data quality (D19); merged with it in C |
| BI02 Multidimensional BI analysis | How can users compare indicators across product, time, category, and other supported dimensions? | Multidimensional aggregation, grouped and period-over-period comparison, drill-down/roll-up, semantic modeling | Marts and analytical result tables | No rankings across independently normalized indices; no inferred customer or purchase shares | BI semantic model, dimension and metric mapping, reusable analytical queries | **Incremental** over visualization marts (D18) |
| BI03 Integrated visual analytics | How can Golden Time, business, and marketing results be combined into an interpretable decision-support view? | Indicator-to-chart mapping, comparison structures, cross-domain patterns, uncertainty representation | Approved analytical result tables | No causal claims from visual patterns; no redefinition of domain metrics | Visual analysis scenarios, chart rationale, cross-domain insight examples, interpretation notes | **Incremental** over chart components (V01–V04); MVP visuals only in C |
| BI04 Metric and visualization validation | Do BI datasets and charts reproduce the analytical results correctly? | Reconciliation tests; checks of values, aggregation, filters, units, labels, missing values, comparison periods, uncertainty, data volume | Result tables vs. BI datasets and charts | Separates analytical, integration, visualization, and UX correctness; does not repeat domain validation | Validation checklist, reproducible reconciliation tests, accuracy report, discrepancy log | **Expanded** (replaces V05) |

- **Data engineering and modeling (secondary):** common ETL architecture; shared collector interface; DataLab and standard-code collectors; collector integration; common preprocessing; schema and availability; data marts; common data quality; source and mart contracts; shared Docker Compose for database and pipeline services.
- **Contexts:** Proposal; TECHSTACK; ARCHITECTURE; DATA_SPEC; ERD; DATA_CONTRACT (source, mart); BI visualization section (incl. BI01–BI04 methods and validation; location R20); `fresh-adventure-data` local context.
- **Credential:** sole DataLab key holder and caller.
- **Not assigned by default:** backend code, AWS deployment, end-to-end integration coordination, page-level frontend implementation, predictive modeling.
- **Portfolio focus:** multidimensional fresh food market analytics and decision-support BI — raw data → data model → data mart → exploratory analysis → visual analytics → metric validation → decision support.

### 4.2 김한승 — Analytics & AI Lead, Product Planning & Context Engineering Owner

- **Existing planning and context responsibilities (not transferred):** PTS, DATA_FEASIBILITY, MVP, PRD (incl. functions and business metrics), requirements traceability, AI master prompt, RULES, root CLAUDE/AGENTS, shared context, AI-assisted execution standards, README, TEAM_ROLES, DECISION_LOG, documentation conventions.
- **Core analytics:** consumer interest time series; shared seasonal statistics; trend analysis; Rising Point and Peak detection; Demand Lead Time; Golden Time; cost-risk analysis; baselines; backtesting (AV1, AV2); analytical methodology and validation standards.
- **Backend and AI:** API_SPEC; analytical-output contracts; backend APIs, backend database access, backend runtime; LLM integration (grounded summary), AI evaluation; backend and AI tests. Advanced RAG and SQL agents remain subject to MVP approval.
- **Methodology review (v0.6):** reviews the analytical handoffs of MA01–MA04 and BI01–BI04 (inputs, definitions, misuse risks). Domain owners implement and validate their own analyses; 김한승 is not their validator.
- **Collector:** ASOS weather (proposed).

### 4.3 이선진 — Business Strategy Lead, Team Leader (unchanged)

- MARKET_RESEARCH, COMPETITOR_ANALYSIS, BUSINESS_ANALYTICS (BA01–BA04), business metric definitions.
- Market size and growth; industry and competitor research; market price comparison; historical and seasonal price indices (single source); cost structure; profitability and contribution margin; break-even; procurement cost sensitivity; business value validation; AV3.
- BA01 (P0, required), BA02 (P1, planned), BA03 (P1, conditional; pilot and Decision Item 6 by 12/13), BA04 (P2, optional). Methods and criteria unchanged.
- Collectors (proposed in v0.5): KOSIS online shopping, KAMIS, settlement pilot (cabbage and apple).
- **No additional mandatory analytics in v0.6.** Portfolio focus: business data analytics for pricing, profitability, cost structures, and promotion decision support.

### 4.4 지혜인 — Marketing & Product Experience Lead, Project Manager

- **Marketing analytics (v0.6):**

| ID | Analytical question | Methods | Data | Validation | Deliverables | Effort classification |
| --- | --- | --- | --- | --- | --- | --- |
| MA01 Customer interest segmentation | Which customer segments show distinct interest patterns for selected products? | Segment-specific EDA, time-series comparison, relative change, variability, trend and seasonal comparison; clustering only if justified (excluded in C) | Naver Shopping Insight (gender, age, device) | DA1 availability and comparability; normalization limits; consistency over time; unsupported interpretations listed. Indices are never customer, purchase, conversion, or market shares | Methodology, reproducible notebook/module, segment outputs, targeting hypotheses, validation and limitations | **Expanded** (replaces J04 customer interest analysis) |
| MA02 Seasonal and event interest analysis | How does interest change around holidays and events? | Event-relative alignment, pre/post comparison, multi-year comparison, reference periods, year-to-year reproducibility | Search Trend, Shopping Insight, holiday information; shared seasonal statistics (김한승) | Comparable reference periods; seasonality and overlapping events; coverage; no causal claims | Event analysis notebook/module, product event profiles, event marketing calendar, validation, interpretation | **Expanded** (replaces J05 seasonal interpretation) |
| MA03 Marketing timing decision analysis | How can opportunity windows become practical preparation and execution timing? | Consumes Golden Time, Rising Point, Peak, Demand Lead Time (김한승); event profiles (MA02); Preparation Lead Time from user research or labeled assumptions; decision rules; feasibility evaluation | Golden Time outputs; interviews (B2) | Demand Lead Time ≠ Preparation Lead Time; preparation needs not inferred from search data | Timing methodology, decision-rule specification, preparation/execution scenarios, reproducible rule implementation, limitations | **Clarified** (proposal §11 listed "마케팅 적기 분석"; not estimated in v0.4/v0.5) |
| MA04 Promotion opportunity scoring | Which candidates are promising from a marketing perspective, and how stable is the ranking? | Criteria definition, indicator integration, normalization options, redundancy and correlation checks, scoring methods, weight sensitivity, ranking stability, explanation | Golden Time outputs (김한승), price and profitability indicators (이선진, reused), marketing indicators | Not a prediction of sales, conversion, or promotion effect; cost and profitability warnings advisory; weights and thresholds not final before MVP | Methodology, reproducible scoring module, sensitivity and stability results, candidate evaluation, limitations (conditional on MVP) | **Previously unassigned** (R9); proposed owner, **not approved**; expanded scope |

- **Existing:** user research and interviews; product and keyword selection; marketing and promotion strategy; UX and design system; frontend application (pages, routing, global filters, chart integration, runtime, hosting); user testing; Notion kanban; weekly logs.
- **Contexts:** PERSONA, USER_SCENARIO, DESIGN (UX), MARKETING_ANALYTICS (MA01–MA04), PROMOTION_STRATEGY, USER_TEST, ROADMAP, weekly logs, `fresh-adventure-fe` local context.
- **Portfolio focus:** data-driven customer interest analysis, event-oriented marketing analytics, marketing timing, and promotion opportunity assessment, backed by reproducible notebooks and validation — not only strategy, frontend, or PM work.
- MA01–MA04 are analytical workstreams; whether their outputs become product features is decided in the MVP.

---

## 5. Context Ownership

| Member | Contexts owned |
| --- | --- |
| 김민지 | Proposal; TECHSTACK; ARCHITECTURE; DATA_SPEC; ERD; DATA_CONTRACT (source, mart); BI visualization section (incl. BI01–BI04 methods and validation); `fresh-adventure-data` local context |
| 김한승 | PTS; DATA_FEASIBILITY; MVP; PRD; AI master prompt; RULES; root CLAUDE/AGENTS; global context; ANALYTICS; TEST_PLAN; API_SPEC; DATA_CONTRACT (analytical output, API, consolidation); AI_CONTEXT; AI_EVALUATION; README; TEAM_ROLES; DECISION_LOG; `fresh-adventure` and `fresh-adventure-be` local context |
| 이선진 | MARKET_RESEARCH; COMPETITOR_ANALYSIS; BUSINESS_ANALYTICS; business metric definitions |
| 지혜인 | PERSONA; USER_SCENARIO; DESIGN (UX, design system, information architecture); MARKETING_ANALYTICS (MA01–MA04); PROMOTION_STRATEGY; USER_TEST; ROADMAP; weekly logs; Notion kanban; `fresh-adventure-fe` local context |

### 5.1 BI Visualization Specification (ownership only; not created in this revision)

Owner: 김민지. Location: a BI visualization section inside DESIGN.md with explicit section ownership (preferred), or VISUALIZATION_SPEC.md if the section grows beyond DESIGN.md's scope (R20). Required content: dashboard objectives; mapping from metrics and result tables to visuals; chart selection; data granularity; visual encoding; interaction requirements; uncertainty representation (ranges, confidence grades, "reference only" labels); visualization validation; performance requirements; reusable component conventions. 지혜인 remains accountable for the overall design system and application UX.

### 5.2 Phase Matrix (status and consolidation)

| Phase | Deliverable | Owner | Status | Consolidation (C) |
| --- | --- | --- | --- | --- |
| 0 | Execution framework, repositories, README | 김한승 | Completed | — |
| 0 | AI master role prompt | 김한승 | UNKNOWN | Stored with context set |
| 1 | Proposal | 김민지 | Completed (v3.4); v3.5 needed (R17) | — |
| 1 | PTS | 김한승 | Completed (approved) | — |
| 1 | MARKET_RESEARCH, COMPETITOR_ANALYSIS | 이선진 | Not started | — |
| 1 | DATA_FEASIBILITY | 김한승 | Not started | Reuses proposal §5-2 evidence |
| 1 | MVP | 김한승 | Not started | Optional PRD section (R-b) |
| 2 | RULES, root CLAUDE/AGENTS | 김한승 | In progress | — |
| 3 | PRD (incl. FUNCTIONS, BUSINESS_METRICS) | 김한승 | Not started | Sections of PRD |
| 3 | PERSONA, USER_SCENARIO | 지혜인 | Not started | May be one file |
| 3 | TECHSTACK | 김민지 | Not started | — |
| 4 | ARCHITECTURE (incl. infrastructure overview) | 김민지 | Not started | — |
| 4 | DATA_SPEC (incl. DATA_DICTIONARY, PIPELINE) | 김민지 | Not started | Sections of DATA_SPEC |
| 4 | ERD | 김민지 | Not started | — |
| 4 | DATA_CONTRACT (source/mart: 김민지; analytical/API and consolidation: 김한승) | 김민지, 김한승 | Not started | One file |
| 4 | ANALYTICS (incl. VALIDATION, experiment log) | 김한승 | Not started | Sections of ANALYTICS |
| 4 | API_SPEC | 김한승 | Not started | — |
| 4 | DESIGN (UX, design system) | 지혜인 | Not started | Contains BI visualization section (김민지) |
| 4 | TEST_PLAN (incl. AI and user-test plans) | 김한승 | Not started | — |
| 4 | AI_CONTEXT, AI_EVALUATION | 김한승 | Not started | May be one file |
| 4 | BUSINESS_ANALYTICS | 이선진 | Not started | Contains BA01–BA04 |
| 4 | MARKETING_ANALYTICS, PROMOTION_STRATEGY, USER_TEST | 지혜인 | Not started | — |
| 5 | TEAM_ROLES | 김한승 | In progress | Decision register moves to DECISION_LOG |
| 5 | ROADMAP (references Notion), weekly logs | 지혜인 | Not started | WBS.md eliminated |
| 5 | DECISION_LOG | 김한승 | Not started | — |

---

## 6. Repository-Specific Context Ownership

| Repository | Visibility | Repository lead | Local context owner | Global context owner | Contributors |
| --- | --- | --- | --- | --- | --- |
| `fresh-adventure` | Public | 김한승 | 김한승 | 김한승 | All |
| `fresh-adventure-data` | Private | 김민지 | 김민지 | 김한승 | All (collectors, analyses) |
| `fresh-adventure-be` | Private | 김한승 | 김한승 | 김한승 | 김민지 (schema review) |
| `fresh-adventure-fe` | Public | 지혜인 | 지혜인 | 김한승 | **김민지 (BI chart components)**, analytical owners |

Cross-repository context: shared rules live only in the main repository; each code repository holds a versioned `docs/SHARED_CONTEXT.md` snapshot (source commit and date) referenced by its local AGENTS.md; 김한승 updates snapshots by pull request; local owners review. Agents are not assumed to read other repositories. Snapshots in public repositories exclude credentials, restricted data descriptions, and private repository internals.

---

## 7. Analytical and Visualization Ownership

### 7.1 Analytical Ownership Matrix

| Analytical workstream | Accountable owner | Collaborators | Status |
| --- | --- | --- | --- |
| Consumer interest trends | 김한승 | 지혜인 | Existing |
| Shared seasonality statistics | 김한승 | 지혜인 | Existing |
| Golden Time detection | 김한승 | 지혜인 | Existing |
| Rising Point and Peak detection | 김한승 | — | Existing |
| Demand Lead Time | 김한승 | 지혜인 | Existing |
| Cost-risk analysis | 김한승 | 이선진 | Existing |
| Analytical methodology and validation standards; review of MA/BI handoffs | 김한승 | Domain owners | Existing; review added |
| MA01 Customer interest segmentation | 지혜인 | 김한승, 김민지 | Expanded |
| MA02 Event-relative interest analysis | 지혜인 | 김한승 | Expanded |
| MA03 Marketing timing decision rules | 지혜인 | 김한승 | Clarified |
| MA04 Promotion opportunity scoring | 지혜인 (**proposed R9 resolution, not approved**) | 김한승, 이선진, 김민지 | Previously unassigned |
| Market size and growth | 이선진 | 김민지 | Existing |
| Historical and seasonal price indices | 이선진 | 김민지 | Existing |
| BA01 Cost data quality assessment | 이선진 | 김민지 | Existing (P0) |
| Cost, profitability, contribution margin | 이선진 | 김한승 | Existing |
| Break-even and sensitivity | 이선진 | 김한승 | Existing |
| BA02 Promotion profitability | 이선진 | 지혜인 | Existing (P1) |
| BA03 Wholesale price decomposition | 이선진 | 김한승, 김민지 | Existing (conditional) |
| BA04 Historical margin analysis | 이선진 | 김한승 | Existing (optional) |
| AV3 Proxy validation | 이선진 | 김한승 | Existing |
| BI01 Exploratory visual analysis | 김민지 | Domain owners | New (incremental) |
| BI02 Multidimensional BI analysis and semantic modeling | 김민지 | 김한승 | New (incremental) |
| BI03 Integrated visual analytics | 김민지 | Domain owners, 지혜인 | New (incremental) |
| BI04 Visualization metric reconciliation | 김민지 | Domain owners | Expanded |
| Domain-specific analytical validation | Each domain owner | 김한승 (standards) | Existing |

### 7.2 Handoffs and Duplication Prevention

| Boundary | Producer → consumer | Rule |
| --- | --- | --- |
| 김한승 ↔ 지혜인 | Shared seasonal statistics, Golden Time, Rising Point, Peak, Demand Lead Time → MA02, MA03, MA04 | No second seasonality or Golden Time implementation; 지혜인 owns event-specific analysis and marketing decision rules |
| 이선진 ↔ 지혜인 | Price indices, profitability, BA02 warnings → MA04 | Profitability is reused, not recalculated; BA02 (economic feasibility) and MA04 (marketing opportunity) remain separate |
| Analytical owners ↔ 김민지 | Result tables → BI02 semantic model, BI03 visuals, BI04 reconciliation | BI aggregates and displays; it never redefines domain metrics |
| 김민지 ↔ 지혜인 | Chart components → pages | One frontend application; 김민지 charts, 지혜인 UX, layouts, routing, integration, user testing |
| 김한승 ↔ 김민지 | Schema and marts → backend data access and APIs | Explicit producer–consumer contracts |
| Common data quality (김민지) ↔ BI01 ↔ BA01 | Quality flags → profiling → business cost rules | BI01 reuses quality outputs; BA01 rules stay with 이선진 |

### 7.3 Visualization Ownership Matrix (subject to approved MVP scope)

Analytical owners are accountable for metric validity and result tables. 김민지 is accountable for accurate, interpretable visual representation. 지혜인 is accountable for usability and page integration. Charts never recompute analytical metrics.

| Analytical area | Analytical owner | Visualization owner | Page integration |
| --- | --- | --- | --- |
| Consumer interest trends | 김한승 | 김민지 | 지혜인 |
| Golden Time | 김한승 | 김민지 | 지혜인 |
| Customer interest characteristics | 지혜인 | 김민지 | 지혜인 |
| Seasonal and holiday patterns | 지혜인 | 김민지 | 지혜인 |
| Promotion candidates | 지혜인 (MA04, proposed R9) | 김민지 | 지혜인 |
| Cost and profitability | 이선진 | 김민지 | 지혜인 |
| Break-even analysis | 이선진 | 김민지 | 지혜인 |
| Margin sensitivity | 이선진 | 김민지 | 지혜인 |
| Wholesale price decomposition (if BA03 adopted) | 이선진 | 김민지 | 지혜인 |
| Cost risk | 김한승 | 김민지 | 지혜인 |
| AI report — evidence charts | 김한승 | 김민지 | 지혜인 |
| AI report — page presentation (text, layout, interaction) | 김한승 (content) | — | 지혜인 |

### 7.4 BI and Frontend Boundary

| Area | 김민지 (BI and visualization) | 지혜인 (frontend application) |
| --- | --- | --- |
| Metrics on screen | KPI presentation, chart selection, visual encoding | Page placement and reading order |
| Components | Reusable chart components and their props contract | Page components, layouts, design system |
| Data | Visualization data models; display-only transformations (sorting, formatting, unit display) | API calls and application state |
| Filters | Chart-level filters and interactions | Global filters, navigation, routing |
| Validation | Chart values match result tables; uncertainty shown correctly; render performance | Usability; page integration; user testing |
| Runtime | — | Frontend build, runtime, static hosting |

One integrated frontend application (`fresh-adventure-fe`). 김민지 contributes chart components there under the agreed component interface; no separate BI dashboard application is built unless approved.

---

## 8. Implementation Ownership

### 8.1 Components

| Component | Accountable owner | Collaborators |
| --- | --- | --- |
| Collector interface, integration, scheduling, raw storage | 김민지 | Collector contributors |
| Common preprocessing, normalization, data quality | 김민지 | Domain owners |
| Analysis-specific transformations and features | Each analytical owner | 김한승 (standards) |
| Database schema, availability, data marts, BI data models | 김민지 | 김한승 |
| Backend APIs, backend database access layer, backend runtime | 김한승 | 김민지 (schema) |
| LLM integration and AI evaluation | 김한승 | 지혜인 |
| Chart components and visualization validation | 김민지 | Analytical owners |
| Frontend pages, routing, global state, runtime, static hosting | 지혜인 | 김민지 |
| Shared Docker Compose (database and pipeline services; others add their services) | 김민지 | Component owners |
| Data-to-visualization integration | 김민지 | 지혜인 |
| End-to-end integration coordination | **TBD (R22)** | All component owners |
| AWS deployment | **TBD (R21)** | Component owners |

### 8.2 Collector Distribution (proposal; feasibility per contributor)

| Source | Collector owner | Integration | MVP need | Assessment |
| --- | --- | --- | --- | --- |
| Naver Search Trend | 김민지 | 김민지 | Core | Credential restriction |
| Naver Shopping Insight | 김민지 | 김민지 | Core | Credential restriction |
| KOSIS Online Shopping | 이선진 | 김민지 | Core | Low complexity |
| KAMIS | 이선진 | 김민지 | Core | Medium complexity; skill unconfirmed |
| Wholesale settlement | 이선진 (C: cabbage and apple pilot; 김민지 supports code mapping) | 김민지 | BA03 pilot; comparisons secondary | High volume and code mapping; full collection deferred unless BA03 is adopted or comparisons are approved |
| Standard codes | 김민지 | 김민지 | Core | Low complexity |
| ASOS weather | 김한승 | 김민지 | Supporting | Low–medium |
| Holiday information | 지혜인 | 김민지 | Core | Very low |
| KOSIS agricultural production | Deferred | — | Not core | — |
| Customs trade | Deferred | — | Not core | — |

Overhead is counted: collector review and integration (D16) and settlement support (D08s) remain with 김민지. If a contributor cannot deliver by the W1 milestone, 김민지 takes the collector back and an optional item is deferred.

### 8.3 Backend and Infrastructure

| Responsibility | v0.4 | v0.5 proposal |
| --- | --- | --- |
| Backend database access layer | 김민지 | 김한승 (backend owner) |
| Backend APIs and runtime | 김한승 | 김한승 |
| Database schema and availability | 김민지 | 김민지 |
| Frontend runtime and hosting | 지혜인 | 지혜인 |
| Shared Docker Compose | 김민지 | 김민지 (database and pipeline services); each owner adds and tests their service |
| AWS deployment | 김민지 | **TBD (R21)** |
| End-to-end integration coordination | 김민지 | **TBD (R22)**; each owner supports their component |

R21 options: (a) component split — 김민지 database/storage, 김한승 backend compute, 지혜인 static hosting — with one accountable owner for the shared account, budget alerts, and networking; (b) 김민지 as single owner (adds ≈ 11 h and conflicts with the BI realignment); (c) 김한승 as single owner (adds ≈ 11 h to the most-loaded member). Recommendation: (a), accountable owner to be chosen after R6 capacity is known.

R22 options: 김한승 (TEST_PLAN owner, most loaded), 김민지 (data-to-visualization path already hers), or 지혜인 scheduling integration sessions as PM with technical checks by owners. Recommendation: decide with R6; 김한승 is not recommended because of load.

---

## 9. RACI Matrix

R = Responsible, A = Accountable, C = Consulted, I = Informed. Each row has exactly one A or an explicit TBD.

| Task | 김민지 | 김한승 | 이선진 | 지혜인 |
| --- | --- | --- | --- | --- |
| Notion kanban, progress tracking, ROADMAP | C | C | C | A/R |
| Weekly execution log | C | C | C | A/R |
| Final decision when agreement cannot be reached | C | C | A/R | C |
| Project execution framework and repository structure | I | A/R | I | C |
| Decision log maintenance | I | A/R | C | C |
| Project Proposal | A/R | C | C | C |
| PTS maintenance, DATA_FEASIBILITY | C | A/R | C | C |
| Data acquisition feasibility verification | A/R | C | C | I |
| MVP and PRD (incl. functions, business metrics) | C | A/R | C | C |
| Business metric definitions | I | C | A/R | C |
| Global context engineering (master prompt, RULES, root CLAUDE/AGENTS, snapshots) | C | A/R | I | C |
| Local context — data repository | A/R | C | I | I |
| Local context — frontend repository | C | C | I | A/R |
| README, TEAM_ROLES, documentation conventions | C | A/R | C | C |
| Market research | I | C | A/R | C |
| Competitor analysis | I | C | A/R | C |
| User research, persona, user scenarios | I | C | C | A/R |
| Product and keyword selection | C | C | C | A/R |
| TECHSTACK, ARCHITECTURE | A/R | C | I | C |
| DATA_SPEC, ERD | A/R | C | I | I |
| DATA_CONTRACT — source and mart | A/R | C | I | C |
| DATA_CONTRACT — analytical output, API, consolidation | C | A/R | C | C |
| DataLab and standard-code collectors | A/R | I | I | I |
| KOSIS online shopping and KAMIS collectors (proposed) | C | I | A/R | I |
| Wholesale settlement collector, pilot scope (proposed) | R | I | A/R | I |
| ASOS collector (proposed) | C | A/R | I | I |
| Holiday collector (proposed) | C | I | I | A/R |
| Collector interface, integration, scheduling | A/R | C | C | C |
| Common preprocessing and data quality | A/R | C | C | C |
| BA01 business cost validation | C | C | A/R | I |
| BA01 pipeline rule implementation | A/R | I | C | I |
| Database schema, availability, data marts, BI data models | A/R | C | C | I |
| Shared seasonal statistics | I | A/R | I | C |
| Golden Time analysis | C | A/R | I | C |
| MA02 Seasonal and event interest analysis | I | C | I | A/R |
| MA01 Customer interest segmentation | C | C | I | A/R |
| MA03 Marketing timing decision rules | I | C | C | A/R |
| MA04 Promotion opportunity scoring (proposed R9; conditional on MVP) | C | C | C | A/R |
| Methodology review of MA and BI handoffs | I | A/R | I | C |
| Normal-year price index and price comparison | C | C | A/R | I |
| Cost-risk anomaly analysis | C | A/R | C | I |
| Profitability and break-even | C | C | A/R | I |
| BA02 promotion profitability | C | C | A/R | C |
| BA03 (conditional) | C | C | A/R | I |
| BA04 (optional) | I | C | A/R | I |
| Marketing and promotion strategy | I | C | C | A/R |
| Analytics standards and validation coordination | C | A/R | C | C |
| AV1, AV2 | I | A/R | C | I |
| AV3 | I | C | A/R | I |
| TEST_PLAN | C | A/R | C | C |
| API_SPEC, backend APIs, backend runtime | C | A/R | I | C |
| Backend database access layer | C | A/R | I | I |
| LLM integration, AI_CONTEXT, AI evaluation | I | A/R | I | C |
| BI visualization specification section | A/R | C | C | C |
| Chart components (all approved analytical areas) | A/R | C | C | C |
| BI01 Exploratory analysis and visual profiling | A/R | C | C | C |
| BI02 Multidimensional BI analysis and semantic model | A/R | C | C | C |
| BI03 Integrated visual analytics | A/R | C | C | C |
| BI04 Metric and visualization validation | A/R | C | C | C |
| DESIGN (UX, design system, information architecture) and wireframes | C | C | C | A/R |
| Frontend pages, routing, global filters, runtime, static hosting | C | C | I | A/R |
| Integration of chart components into pages | R | I | I | A/R |
| Shared Docker Compose | A/R | R | I | R |
| Data-to-visualization integration | A/R | C | I | R |
| User testing | C | C | C | A/R |
| Business value validation | C | C | A/R | C |
| Presentation material | R | R | R | R |
| Presentation delivery | C | C | C | C |
| Retrospective | R | R | R | R |
| End-to-end integration coordination | R | R | R | R |
| AWS deployment | R | R | I | R |

| Task | Accountable | Responsible |
| --- | --- | --- |
| End-to-end integration coordination | **TBD (R22)** | Component owners |
| AWS deployment | **TBD (R21)** | Component owners |
| Presentation material | **TBD** | All |
| Presentation delivery | **TBD** (Presenter) | **TBD** |
| Retrospective coordination | **TBD** | All |
| Risk management | **TBD (R13)** | — |

MA04 accountable owner (지혜인) is a **proposed** R9 resolution and is not approved.

---

## 10. Individual Deliverables (portfolio evidence)

Document ownership, AI-generated code, dashboard screenshots, or presentation materials alone do not count as analytical evidence. Each analytical deliverable needs reproducible code or notebooks on actual data, interpretation, validation, and documented limitations.

| Member | Analytical and technical portfolio evidence | Other deliverables |
| --- | --- | --- |
| 김민지 | BI01 reproducible EDA and profiling; BI02 semantic model and multidimensional queries; data marts; reusable chart components; BI03 integrated decision-support dashboard and visual analysis scenarios; BI04 reconciliation tests and accuracy report | Proposal v3.5; TECHSTACK; ARCHITECTURE; DATA_SPEC; ERD; source/mart contracts; DataLab and code collectors; collector integration; common preprocessing and data quality; shared Compose |
| 김한승 | Reproducible Golden Time analysis; methodology; seasonal baselines and backtesting (AV1); cost-risk analysis (AV2); analysis-result APIs; evidence-grounded AI evaluation | PTS, DATA_FEASIBILITY, MVP, PRD; context set (master prompt, RULES, CLAUDE/AGENTS, snapshots); ANALYTICS; TEST_PLAN; API_SPEC; README, TEAM_ROLES, DECISION_LOG; ASOS collector |
| 이선진 | Market size analysis; price indices; profitability, contribution margin, break-even, and sensitivity models; BA01–BA03 (BA04 optional); AV3; business validation (unchanged) | MARKET_RESEARCH; COMPETITOR_ANALYSIS; BUSINESS_ANALYTICS; KOSIS, KAMIS, settlement-pilot collectors |
| 지혜인 | MA01 segmentation analysis; MA02 event-relative analysis; MA03 marketing timing rules; MA04 scoring with sensitivity and stability (if approved); marketing interpretation | User research; PERSONA; USER_SCENARIO; DESIGN; PROMOTION_STRATEGY; frontend application; USER_TEST; ROADMAP; Notion kanban; weekly logs; holiday collector |

---

## 11. Acceptance Criteria

### 11.1 General

- Agreed repository and path, named owner, version.
- Sources, time ranges, assumptions stated; unverified results labeled (PTS evidence classification).
- Reviewed by at least one other member.
- No credentials, restricted data, or private details in public repositories or Notion.

### 11.2 Specific

| Deliverable | Acceptance criteria |
| --- | --- |
| Collectors | Agreed interface; raw responses stored; failures logged; re-runnable; no credentials in code |
| Pipeline, marts, schema | Documented schema; code mapping applied; tests for core transformations |
| Data contracts | Columns, types, units, delivery format agreed by producer and consumer before implementation |
| Context set | Snapshot with source commit in each repository; local AGENTS.md references it; master prompt stored in the main repository |
| PTS, MVP, PRD | Traceable to PTS decisions; changes recorded in DECISION_LOG; approval by team governance |
| Golden Time methodology, AV1/AV2/AV3 | Consistent with PTS §8; baselines predefined; temporal consistency; negative results reported |
| Shared statistics and price index | One implementation; consumers import it |
| BA01–BA04 | As in v0.4 (counts and reasons; spikes retained; scenario labels; no automatic exclusion; reconciliation; no zero-filled off-season values) |
| BI visualization specification | Every chart maps to a named result table and metric owner; uncertainty encoding defined; performance targets stated |
| Chart components | Values match result tables in automated or scripted checks; no analytical recalculation; uncertainty and "reference only" labels shown; source cited; agreed props interface |
| Frontend pages | Match approved wireframes; integrate chart components without modifying their data logic; no secrets |
| Backend APIs and data access | Match API_SPEC; tests pass; schema changes coordinated with 김민지 |
| AI features | Grounded in result tables; DataLab derived indicators only |
| User research and testing | Concrete recent examples (PTS B1–B5); majority agreement not treated as product-market fit |
| Kanban and weekly logs | One log per week; kanban shows owner and status for every active task |
| Deployment | Reproducible steps; cost controls documented |
| MA01 | Comparability (DA1) checked before cross-segment statements; no share interpretation of indices; reproducible on actual data; limitations listed |
| MA02 | Reuses shared seasonal statistics; reference periods defined; overlapping events handled; year-to-year consistency reported; no causal claims |
| MA03 | Demand and Preparation Lead Time separated; preparation assumptions sourced or labeled; rules reproducible and testable on past seasons |
| MA04 | Reuses profitability indicators; sensitivity and ranking-stability results reported; not presented as sales or effect prediction; weights not final before MVP |
| BI01 | Reuses common quality outputs; findings reproducible; no duplicate validation logic |
| BI02 | Dimensions and metrics mapped to owners; no rankings across independently normalized indices |
| BI03 | Every visual traces to an approved result table; uncertainty shown; no causal claims |
| BI04 | Automated reconciliation of displayed values against result tables; discrepancies logged and resolved |

---

## 12. Responsibility Boundaries and Overlap Audit

### 12.1 Boundary Rules

| Boundary | Rule |
| --- | --- |
| Historical vs. actual planning ownership | Planning and context engineering are 김한승's existing responsibilities; v0.4 "transfer" wording withdrawn |
| Proposal vs. product planning | 김민지 authors the proposal; 김한승 owns PTS/MVP/PRD; proposal is a planning record once PRD exists |
| BI visualization vs. frontend | Section 7.3 |
| Metric presentation vs. calculation | Analytical owners calculate; charts only display; display transformations must not redefine metrics |
| Shared vs. analysis-specific processing | 김민지 shared ingestion and normalization; analytical owners their own transformations |
| Data mart vs. backend data access | 김민지 schema, marts, availability; 김한승 backend access code |
| Chart vs. page components; chart vs. application filters | Section 7.3 |
| Analytical validation vs. visualization accuracy | Analytical owners validate metrics; 김민지 validates that charts reproduce result tables |
| Component vs. system testing | Owners test their components; end-to-end coordination TBD (R22); TEST_PLAN by 김한승 |
| Infrastructure | Shared Compose 김민지; runtimes by component owners; AWS TBD (R21) |
| Documentation creation vs. maintenance | Owner of a created document maintains it; status tracked in §3 and §14 |
| Project management vs. execution framework | Framework (김한승, completed); tracking and progress (지혜인) |

### 12.2 Status of v0.4 Audit Items

| ID | v0.4 issue | v0.5 status |
| --- | --- | --- |
| I-01 | 김민지 "Product Planner" owning PTS/MVP/PRD | **Reclassified**: baseline correction (I-25), not a workload transfer |
| I-02 | v3.4 §10 BI column holds backend, screens, LLM | **Updated**: charts to 김민지 (BI), pages to 지혜인, backend/LLM to 김한승; proposal v3.5 needed (R17) |
| I-03 | Duplicate profitability module | Resolved in this proposal (이선진 single source) |
| I-04 | Promotion scoring owner | **Open** (R9) |
| I-05 | Duplicate seasonal calculation | Resolved in this proposal (shared statistics) |
| I-06 | Duplicate price index | Resolved in this proposal (이선진 single source) |
| I-07 | Data quality layers | Resolved in this proposal |
| I-08 | Preprocessing split | Resolved in this proposal |
| I-09 | BI vs. dashboard duplication | **Updated** by I-26 |
| I-10 | Joint result-table specification | Resolved in this proposal (DATA_CONTRACT sections) |
| I-11 | Test planning owner | Resolved (TEST_PLAN 김한승); end-to-end coordination reopened as I-31 |
| I-12 | Environment setup concentrated on 김민지 | **Updated** by I-32 |
| I-13 | Stale proposal reference in v3.4 §10 W0 | Open until v3.5 (R17) |
| I-14 | Duplicate task tracking | Resolved in this proposal (Notion authoritative) |
| I-15 | Two decision registers | Resolved in this proposal (DECISION_LOG absorbs register) |
| I-16 | Final dates inconsistent | **Open** (R8) |
| I-17 | December 1 planning presentation not documented | **Open** (R12) |
| I-18 | First demo omits Golden Time | **Open** (R18) |
| I-19 | Full AI assistant in scope | Resolved in C (grounded summary first) |
| I-20 | Proposal vs. future specifications duplication | Resolved in this proposal (proposal becomes planning record) |
| I-21 | DataLab single point of failure | **Open** (mitigated by early sample extract) |
| I-22 | 이선진 W2 overload | Partially resolved; settlement pilot adds W1–W2 load (I-36) |
| I-23 | Nonessential collectors | Resolved in C (deferred) |
| I-24 | 김한승 concentration | **Open** (still the largest remaining workload) |

### 12.3 New and Updated Issues

| ID | Source and section | Current assignment | Conflicting assignment | Existing or new | Revised owner | Collaborators | Workload impact (remaining, C) | Remaining uncertainty |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| I-25 | TEAM_ROLES v0.4 §14.4, §16.1 item 1 | "≈ 31 h planning transferred from 김민지" | Planning was always 김한승's responsibility | Existing | 김한승 | Domain owners | 0 h new; ≈ 31 h of 김한승's planning is **remaining existing work** (P01–P04) | Completion of the AI master prompt (UNKNOWN) |
| I-26 | TEAM_ROLES v0.4 §8.1 ("UI, dashboard charts" to 지혜인; BI = models only) | Charts inside 지혜인's frontend scope | 김민지's BI career direction | New for 김민지 | 김민지 (charts), 지혜인 (pages) | Analytical owners | 김민지 +≈ 44 h; 지혜인 −≈ 19 h frontend | Chart library choice depends on TECHSTACK |
| I-27 | Proposal v3.4 §8 dashboard; v0.4 §7 | Metrics computed by analytics, shown by FE | Risk of recalculation in charts | Clarification | Analytical owners (metrics), 김민지 (display) | — | None | — |
| I-28 | New BI/FE split | Filters undefined | Chart-level vs. global filters | New | 김민지 (chart), 지혜인 (global) | — | Included in V03/J08b | Component interface not yet agreed |
| I-29 | TEAM_ROLES v0.4 §8.1 (data-access layer to 김민지) | 김민지 | Backend ownership | Newly transferred | 김한승 | 김민지 | 김한승 +5 h, 김민지 −5 h | — |
| I-30 | v0.4 §11 acceptance | Analytical validation only | Charts can misrepresent valid metrics | New | 김민지 (visualization accuracy) | Analytical owners | +5 h (V05) | — |
| I-31 | v0.4 §8.1, RACI "System integration" (김민지) | 김민지 coordinates end-to-end | BI realignment, workload | Newly unassigned | **TBD (R22)** | All | ≈ 10 h in TBD bucket | Owner and capacity |
| I-32 | v0.4 §8.1 (Compose and AWS to 김민지) | 김민지 | BI realignment | Newly unassigned (AWS) | Compose 김민지; AWS **TBD (R21)** | Component owners | ≈ 11 h in TBD bucket | Skills for AWS unconfirmed |
| I-33 | Documents in §5.2 | Creation and maintenance not separated | — | Clarification | Document owners | — | Recurring maintenance counted separately (§14) | — |
| I-34 | v0.3/v0.4 PM vs. framework | Overlap perceived | — | Clarification | 김한승 (framework, completed), 지혜인 (tracking) | — | None | — |
| I-35 | DESIGN.md | Single owner (지혜인) | BI section needs 김민지 ownership | New | Section-level ownership; location R20 | — | V01 ≈ 5 h | Separate file vs. section |
| I-36 | §8.2 settlement collector | 김민지 (v0.4) | Domain ownership (BA03) vs. 이선진 skill and load | Newly transferred | 이선진 (pilot scope) | 김민지 (support ≈ 3 h) | 이선진 +7 h; 김민지 −11 h | Python skill; settlement volume |
| I-37 | Proposal v3.4 §1, §8, §10, §11 | Career-based columns; "기획자 김민지"; BI does backend/screens | v0.5 roles | Proposal update needed | 김민지 (Proposal Owner) | 김한승 | D01 ≈ 6 h | Proposal Owner review |
| I-38 | §8.3, §9 | — | AWS, end-to-end integration, promotion scoring unassigned | New | **TBD** | — | ≈ 27 h unassigned | Must be assigned before W3 |

### 12.4 Issues Introduced or Clarified in v0.6

| ID | Source | Risk | Resolution | Owner | Remaining uncertainty |
| --- | --- | --- | --- | --- | --- |
| I-39 | MA02 vs. shared seasonal statistics (H04) | Duplicate seasonality implementation | MA02 imports shared statistics; adds only event alignment | 지혜인 (MA02), 김한승 (H04) | Interface of shared statistics not yet defined |
| I-40 | MA03 vs. Golden Time (H03) | Duplicate timing detection | MA03 consumes Golden Time outputs; adds preparation lead time and rules | 지혜인 (MA03), 김한승 (H03) | Golden Time output schema pending |
| I-41 | MA04 vs. BA02 | Profitability recalculated in scoring | MA04 reuses BA02 and price-index outputs | 지혜인 (MA04), 이선진 (BA02) | MA04 approval (R9); BA02 timing (W4) vs. MA04 (W4) |
| I-42 | MA01, BI02 | Misreading normalized indices as shares or cross-product rankings | Explicit prohibition in acceptance criteria | 지혜인, 김민지 | DA1 result |
| I-43 | BI01 vs. common data quality (D19) vs. BA01 | Three overlapping quality checks | Layers: pipeline flags (D19) → exploratory profiling (BI01) → business cost rules (BA01) | 김민지, 이선진 | — |
| I-44 | BI04 vs. domain validation | Repeating domain validation in BI | BI04 checks reproduction only | 김민지 | — |
| I-45 | 지혜인 W3–W4 load (MA01–MA04 + frontend + PM) | Weekly overload around the demo | MA03 and MA04 moved after 12/18; MA01 clustering excluded; MA04 lightweight and conditional | 지혜인 | Capacity (R6); frontend skill |
| I-46 | 김민지 W1–W2 load (collectors, contracts, marts, BI01, BI02, demo charts) | Critical-path overload | BI01 split W2–W3; DATA_SPEC and TECHSTACK started in W0 | 김민지 | Capacity (R6) |
| I-47 | AI-assisted estimates | Overconfidence in AI productivity | Three productivity scenarios; human-owned shares not discounted; pilot calibration (R25) | 김한승 (method), all | No measured productivity yet |

---

## 13. Collaboration and Handoff Rules

1. **Contracts before code.** DATA_CONTRACT sections and the chart component interface are agreed before dependent implementation.
2. **Sample-first.** Analyses start on validated samples; charts and pages start on contract-conformant mock data.
3. **Result tables are the handoff.** Backend serves them; charts display them; nobody re-implements analysis.
4. **Single implementation for shared metrics** (seasonal statistics, price index, profitability).
5. **Pull requests:** at least one reviewer; repository leads review their repositories; 김민지 is a required reviewer for chart components in the frontend repository, 지혜인 for page integration.
6. **Credentials:** DataLab calls only by 김민지; others submit requests.
7. **Decisions:** team agreement; Team Leader decides if agreement cannot be reached; recorded in DECISION_LOG.
8. **Weekly cycle:** update Notion before the Sunday meeting; 지혜인 writes the weekly log; 김한승 updates context documents when shared rules change.
9. **Analytical handoffs (v0.6):** MA02/MA03/MA04 consume shared seasonal statistics and Golden Time outputs through agreed result tables; MA04 consumes BA02 and price-index outputs; BI02–BI04 consume approved result tables. Producers publish a short schema note with each table.
10. **AI-assisted work:** every AI-generated change has a human owner who reviews, tests, and explains it; generated analysis code is re-run on actual data before results are reported.

---

## 14. Workload and Dependency Assessment

### 14.1 Method

- Unit: person-hours. Three-point estimates; PERT = (O + 4M + P) / 6. **Illustrative estimates, not measured work or commitments.**
- Base task list and estimates are the v0.5 model, unchanged; new or expanded tasks are added with their own estimates. Completed work (≈ 41 h, 김한승: C01–C04) is excluded from remaining effort. UNKNOWN status is treated as not completed.
- Classification per task: Completed, Existing, Recurring, Clarified, Expanded, New (incremental), Previously unassigned, Deferred, Eliminated.
- **BI01–BI04 and MA01–MA04 are counted only as incremental effort** over existing tasks: BI01 over common data quality (D19), BI02 over visualization marts (D18), BI03 over chart components (V01–V04), BI04 replaces V05, MA01 replaces J04, MA02 replaces J05, MA04 replaces the TBD scoring task X01.
- All three scenarios share v0.5 base deferrals (BA04, BA03 full, two collectors, separate documents, advanced AI), so differences isolate the responsibility changes.
- Calendar: W0 11/26–11/29, W1 11/30–12/6, W2 12/7–12/13, W3 12/14–12/20, W4 12/21–12/27 (12/25), W5 12/28–1/3 (1/1), W6 1/4–1/6; effective ≈ 5.6 weeks.

### 14.2 AI-Assisted Delivery Model

The team will use Claude Code and Codex. **v0.4 and v0.5 estimates did not assume AI assistance**; they are treated as unassisted-equivalent, so AI effects are applied once (no double counting).

Each task's effort is split into an accelerable share (AI-assisted implementation and drafting) and a human-owned share (specification, interpretation, review, testing, debugging and rework, integration). Only the accelerable share is reduced; a verification overhead of 10% of the original accelerable effort is added in every AI scenario.

| Category | Accelerable share (implementation, drafting) | Human-owned share (specification, interpretation, review, testing, rework, integration) |
| --- | --- | --- |
| Frontend development | 60% | 40% |
| Backend development | 60% | 40% |
| AI development | 50% | 50% |
| BI and visualization | 50% | 50% |
| Data collection | 50% | 50% |
| Data engineering | 45% | 55% |
| Documentation | 40% | 60% |
| Deployment | 35% | 65% |
| Context engineering | 30% | 70% |
| Analytics | 30% | 70% |
| Product planning | 25% | 75% |
| Testing and validation | 25% | 75% |
| Recurring maintenance | 20% | 80% |
| Integration | 15% | 85% |
| Research | 15% | 85% |
| Project management | 10% | 90% |
| Collaboration and support | 0% | 100% |
| Code review | 0% | 100% |

| Productivity scenario | Accelerable effort multiplier | Net effect on accelerable share (incl. 10% verification) | Assumption |
| --- | --- | --- | --- |
| None | 1.00 | 1.00 | v0.5 basis |
| Conservative | 0.85 | 0.95 | Team new to agents; frequent rework of generated code |
| **Expected (planning basis)** | 0.65 | 0.75 | Agents used with the context set (RULES, AGENTS, snapshots); human review of every change |
| Optimistic | 0.50 | 0.60 | Stable context, small well-specified tasks, few integration surprises |

Human accountability remains for problem definition, data interpretation, methodology and statistical assumptions, data quality, code review, security, testing, integration, business interpretation, and user research. AI assistance does not guarantee correctness or delivery, and does not increase available hours.

### 14.3 AI-Assisted Competency Assumptions

| Member | Competencies required by assigned work | Evidence | Status | Calibration pilot (≈ 3–5 h, W0–W1) |
| --- | --- | --- | --- | --- |
| 김민지 | Data modeling, SQL, Python ETL, chart library use, generated-code review, metric reconciliation | None in repositories | **Unconfirmed** | One chart component on mock contract data with a reconciliation test |
| 김한승 | Time-series analysis, statistical baselines, Python, backend API, context engineering, review | Phase 01 repository and documentation work (commits) | Planning and context: evidenced; analytics and backend: **unconfirmed** | Rising Point detection for one product with a seasonal baseline |
| 이선진 | Data literacy, spreadsheet/Python analysis, API collection with agent support, business interpretation | None in repositories | **Unconfirmed** | KAMIS collector for one product plus one BA01 rule |
| 지혜인 | Marketing analytics, Python notebooks with agent support, frontend framework use, UX, review | None in repositories | **Unconfirmed** | Event-relative analysis for one product plus one page integrating a chart |

Pilot results (actual hours vs. estimate, rework needed) are used to recalibrate O/M/P values (R25). Traditional engineering proficiency is useful but not the only assignment criterion.

### 14.4 Work Breakdown (Scenario C owners)

| ID | Task | Owner (C) | Classification | Category | Remaining PERT, no AI (h) | Remaining, expected AI (h) | Weeks (C) | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| C01 | Phase 01 execution framework: four repositories, folder structure, conventions, templates | 김한승 | Completed | Product planning | 0.0 | 0.0 | — | P0 |
| C02 | README (main and repository READMEs, Korean root READMEs) | 김한승 | Completed | Documentation | 0.0 | 0.0 | — | P0 |
| C03 | PTS v0.1–v0.2 (approved) | 김한승 | Completed | Product planning | 0.0 | 0.0 | — | P0 |
| C04 | TEAM_ROLES v0.1–v0.4 | 김한승 | Completed | Documentation | 0.0 | 0.0 | — | P0 |
| P01 | PTS maintenance under change control | 김한승 | Recurring | Product planning | 2.2 | 2.0 | Recurring | P0 |
| P02 | DATA_FEASIBILITY.md (consolidates proposal §5-2 test evidence) | 김한승 | Existing | Product planning | 6.2 | 5.8 | W1 | P0 |
| P03 | MVP.md | 김한승 | Existing | Product planning | 8.3 | 7.8 | W0, W1 | P0 |
| P04 | PRD.md (incl. functions and business metrics in C) | 김한승 | Existing | Product planning | 14.7 | 13.8 | W1, W2, W3 | P0 |
| P06 | Context set: RULES.md, root AGENTS/CLAUDE (placeholders exist), shared-context snapshots | 김한승 | Existing | Context engineering | 8.3 | 7.6 | W0, W1 | P0 |
| P07 | AI master role prompt (stored in repository) | 김한승 | Existing | Context engineering | 2.2 | 2.0 | W0 | P0 |
| P08 | Context maintenance and cross-repository sync | 김한승 | Recurring | Recurring maintenance | 8.2 | 7.8 | Recurring | P0 |
| P09 | README, TEAM_ROLES (v0.5+), DECISION_LOG maintenance | 김한승 | Recurring | Documentation | 7.0 | 6.3 | Recurring | P0 |
| H01 | ANALYTICS.md (incl. validation and experiment log in A/C) | 김한승 | Existing | Documentation | 8.2 | 7.3 | W1, W2 | P0 |
| H03 | Golden Time analysis (seasonality, Rising Point, Peak, Demand Lead Time) | 김한승 | Existing | Analytics | 30.8 | 28.5 | W2, W3, W4 | P0 |
| H04 | Shared seasonal statistics reused by marketing analysis | 김한승 | Existing | Analytics | 3.2 | 2.9 | W2 | P0 |
| H05 | Seasonal baselines and backtesting (AV1) | 김한승 | Existing | Testing and validation | 14.3 | 13.4 | W3, W4, W5 | P0 |
| H06 | Cost-risk anomaly analysis and AV2 | 김한승 | Existing | Analytics | 12.7 | 11.7 | W3, W4 | P0 |
| H07 | API_SPEC.md and analytical output contracts | 김한승 | Existing | Documentation | 5.2 | 4.7 | W1, W2 | P0 |
| H08 | Backend analysis-result APIs, backend Dockerfile and runtime | 김한승 | Existing | Backend development | 15.5 | 13.2 | W2, W3 | P0 |
| H09 | Backend database access layer | 김한승 | Existing | Backend development | 5.2 | 4.4 | W2 | P0 |
| H10 | LLM integration (grounded summary) and AI_CONTEXT.md | 김한승 (×0.55) | Existing | AI development | 5.9 | 5.1 | W4 | P0 |
| H11 | AI evaluation (AI_EVALUATION.md) | 김한승 (×0.5) | Existing | AI development | 2.6 | 2.3 | W5 | P0 |
| H12 | TEST_PLAN.md (integrated) | 김한승 | Existing | Testing and validation | 4.0 | 3.8 | W3 | P0 |
| H13 | Backend and main repository code review, method support | 김한승 | Recurring | Code review | 10.2 | 10.2 | Recurring | P0 |
| H14 | ASOS weather collector | 김한승 | Existing | Data collection | 5.2 | 4.5 | W1 | P0 |
| D01 | Proposal v3.5 alignment (Proposal Owner) | 김민지 | Existing | Product planning | 6.2 | 5.8 | W0, W1 | P0 |
| D02 | TECHSTACK.md | 김민지 | Existing | Documentation | 4.0 | 3.6 | W0, W1 | P0 |
| D03 | ARCHITECTURE.md (incl. infrastructure overview) | 김민지 | Existing | Documentation | 5.2 | 4.7 | W3, W4 | P0 |
| D04 | DATA_SPEC.md (incl. data dictionary, pipeline notes, collector interface) | 김민지 | Existing | Documentation | 8.0 | 7.2 | W0, W1, W2 | P0 |
| D06 | ERD.md and schema DDL | 김민지 | Existing | Data engineering | 6.3 | 5.6 | W1 | P0 |
| D07 | DataLab collectors (search trend, shopping insight incl. demographics) | 김민지 | Existing | Data collection | 10.3 | 9.0 | W1 | P0 |
| D08p | Wholesale settlement collector, pilot scope (cabbage and apple) | 이선진 | Existing | Data collection | 7.3 | 6.4 | W1, W2 | P0 |
| D08s | Settlement collector support (code mapping, unit conversion) | 김민지 | Existing | Collaboration and support | 3.2 | 3.2 | W1 | P0 |
| D09 | Standard code collector and mapping load | 김민지 | Existing | Data collection | 4.0 | 3.5 | W1 | P0 |
| D10 | KOSIS online shopping collector | 이선진 | Existing | Data collection | 5.3 | 4.7 | W1 | P0 |
| D11 | KAMIS collector | 이선진 | Existing | Data collection | 8.3 | 7.3 | W1 | P0 |
| D13 | Holiday collector | 지혜인 | Existing | Data collection | 2.2 | 1.9 | W1 | P0 |
| D16 | Collector review and integration (shared interface, scheduling, retries) | 김민지 | Existing | Integration | 5.3 | 5.1 | W1, W2 | P0 |
| D17 | Common preprocessing and normalization | 김민지 | Existing | Data engineering | 10.3 | 9.2 | W2 | P0 |
| D18 | Data marts incl. BI/visualization marts | 김민지 (×1.2) | Existing | Data engineering | 10.2 | 9.1 | W2 | P0 |
| D19 | Common data quality and BA01 rule implementation | 김민지 | Existing | Testing and validation | 7.3 | 6.9 | W2, W4 | P0 |
| D20 | DATA_CONTRACT source and mart sections | 김민지 | Existing | Documentation | 4.0 | 3.6 | W1 | P0 |
| D21 | Shared Docker Compose (services contributed by component owners) | 김민지 | Existing | Deployment | 4.3 | 4.0 | W0, W1 | P0 |
| D22 | System integration and integration-test coordination (end-to-end) | TBD | Existing | Integration | 10.3 | 9.9 | W3, W4 | P0 |
| D22v | Data-to-visualization integration | 김민지 | Existing | Integration | 4.0 | 3.9 | W3 | P0 |
| D23 | AWS deployment | TBD | Existing | Deployment | 11.0 | 10.0 | W5 | P0 |
| D25 | Data repository code review | 김민지 | Recurring | Code review | 9.3 | 9.3 | Recurring | P0 |
| V01 | BI visualization section (DESIGN.md section owned by 김민지) | 김민지 | Existing | Documentation | 5.2 | 4.7 | W1, W2 | P0 |
| V02 | Chart component interface and conventions | 김민지 | Existing | Frontend development | 2.2 | 1.8 | W1 | P0 |
| V03 | Chart components for first demonstration (KPI, time series, profitability/BEP) | 김민지 | Existing | BI and visualization | 20.7 | 18.1 | W2, W3 | P0 |
| V04 | Remaining chart components (customer interest, seasonal, cost risk, decomposition, AI report charts) | 김민지 (×0.75) | Existing | BI and visualization | 10.8 | 9.4 | W4 | P0 |
| V05 | Visualization accuracy and performance validation | — (replaced in C) | Existing | Testing and validation | 0.0 | 0.0 | W3, W4 | P0 |
| B01 | MARKET_RESEARCH.md and market size/growth | 이선진 | Existing | Research | 16.3 | 15.7 | W1, W3, W4 | P0 |
| B02 | COMPETITOR_ANALYSIS.md | 이선진 | Existing | Research | 8.2 | 7.9 | W3, W4 | P0 |
| B03 | BUSINESS_ANALYTICS.md (BA01–BA04) | 이선진 | Existing | Documentation | 6.3 | 5.7 | W1, W2 | P0 |
| B04 | Sample product configurations (3) and cost defaults | 이선진 | Existing | Analytics | 6.3 | 5.9 | W2 | P0 |
| B05 | Normal-year price index and price comparison (single source) | 이선진 | Existing | Analytics | 7.3 | 6.8 | W2 | P0 |
| B06 | Profitability and break-even module, sensitivity | 이선진 | Existing | Analytics | 10.3 | 9.6 | W2, W3 | P0 |
| B07 | BA01 phase 1 | 이선진 | Existing | Testing and validation | 6.3 | 5.9 | W2 | P0 |
| B08 | BA03 pilot (cabbage, apple) | 이선진 | Existing | Analytics | 8.5 | 7.9 | W2 | P1 |
| B09 | BA01 phase 2 | 이선진 | Existing | Testing and validation | 7.3 | 6.9 | W4 | P0 |
| B10 | BA02 promotion profitability (15 configurations) | 이선진 | Existing | Analytics | 12.7 | 11.7 | W4 | P1 |
| B13 | Business value validation | 이선진 | Existing | Testing and validation | 5.2 | 4.8 | W5 | P0 |
| B14 | Team Leader duties | 이선진 | Recurring | Project management | 6.2 | 6.0 | Recurring | P0 |
| B16 | AV3 proxy validation | 이선진 | Existing | Testing and validation | 5.2 | 4.8 | W5 | P0 |
| J01 | PERSONA.md and USER_SCENARIO.md | 지혜인 | Existing | Documentation | 7.3 | 6.6 | W1, W2, W3 | P0 |
| J02 | User interviews and synthesis | 지혜인 | Existing | Research | 14.7 | 14.1 | W1, W2, W3 | P0 |
| J03 | Product and keyword selection, mapping | 지혜인 | Existing | Research | 7.3 | 7.1 | W1 | P0 |
| J04 | Customer interest analysis incl. DA1 check | — (replaced in C) | Existing | Analytics | 0.0 | 0.0 | W2 | P0 |
| J05 | Seasonal and holiday interpretation (reuses shared statistics) | — (replaced in C) | Existing | Analytics | 0.0 | 0.0 | W2, W3 | P0 |
| J06 | PROMOTION_STRATEGY.md | 지혜인 | Existing | Analytics | 6.3 | 5.9 | W4 | P0 |
| J07 | DESIGN.md (UX, design system, information architecture) and wireframes | 지혜인 | Existing | Frontend development | 8.5 | 7.2 | W1, W2 | P0 |
| J08b | Frontend: app shell, routing, layouts, first-demo pages, API integration | 지혜인 | Existing | Frontend development | 16.7 | 14.2 | W2, W3 | P0 |
| J09b | Frontend: remaining MVP pages | 지혜인 (×0.75) | Existing | Frontend development | 9.5 | 8.1 | W4 | P0 |
| J15 | Integration of BI chart components into pages | 지혜인 | Existing | Integration | 2.2 | 2.1 | W3, W4 | P0 |
| J10 | USER_TEST.md and user testing | 지혜인 | Existing | Testing and validation | 5.2 | 4.8 | W5 | P0 |
| J11 | PM: Notion kanban, weekly execution logs, progress tracking | 지혜인 | Recurring | Project management | 15.3 | 15.0 | Recurring | P0 |
| J12 | ROADMAP.md (references Notion) | 지혜인 | Existing | Project management | 3.2 | 3.1 | W1 | P0 |
| J13 | Demonstration scenarios | 지혜인 | Existing | Collaboration and support | 4.0 | 4.0 | W3, W5 | P0 |
| J14 | Frontend static hosting setup | 지혜인 | Existing | Deployment | 2.2 | 2.0 | W5 | P0 |
| X01 | Promotion scoring implementation (R9) | — (replaced in C) | Existing | Analytics | 0.0 | 0.0 | W2 | P1 |
| MA01 | MA01 Customer interest segmentation (method, notebook, validation, targeting hypotheses) | 지혜인 (×0.85) | Expanded (replaces J04) | Analytics | 8.8 | 8.1 | W2, W3 | P1 |
| MA02 | MA02 Seasonal and event interest analysis (event-relative alignment, multi-year comparison) | 지혜인 | Expanded (replaces J05) | Analytics | 10.3 | 9.6 | W2, W3 | P1 |
| MA03 | MA03 Marketing timing decision rules (consumes Golden Time; preparation lead-time scenarios) | 지혜인 | Clarified (proposal §11 '마케팅 적기 분석'; not estimated before) | Analytics | 8.5 | 7.9 | W4 | P1 |
| MA04 | MA04 Promotion opportunity scoring (criteria, normalization, sensitivity, ranking stability) | 지혜인 (×0.7) | Previously unassigned (R9), expanded | Analytics | 7.2 | 6.7 | W4, W5 | P1-cond |
| BI01 | BI01 Exploratory analysis and visual profiling (incremental over common data quality) | 김민지 (×0.7) | New (incremental) | BI and visualization | 4.4 | 3.9 | W2, W3 | P1 |
| BI02 | BI02 Multidimensional BI semantic model and reusable queries (incremental over marts) | 김민지 | New (incremental) | BI and visualization | 5.2 | 4.5 | W2 | P1 |
| BI03 | BI03 Integrated visual analytics scenarios and interpretation (incremental over chart components) | 김민지 (×0.6) | New (incremental) | BI and visualization | 3.1 | 2.7 | W4, W5 | P1 |
| BI04 | BI04 Metric and visualization validation with reconciliation tests (replaces V05) | 김민지 | Expanded (replaces V05) | Testing and validation | 7.3 | 6.9 | W3, W4 | P0 |
| RV01 | Methodology review for MA01–MA04 and BI01–BI04 handoffs | 김한승 | New | Code review | 3.2 | 3.2 | W2, W3, W4 | P1 |
| S-* | Shared per member: first-demo preparation, final presentation, integration participation, weekly meetings (recurring), bug fixing | Each member | Existing | Collaboration and support | 27.9 each | 27.0–27.9 each | W3–W6 | P0 |

### 14.5 Scenario Comparison (remaining hours, PERT)

| Scenario | AI productivity | 김민지 | 김한승 | 이선진 | 지혜인 | TBD | Team (= sum) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| A — v0.5 allocation | None | 174 | 208 | 155 | 145 | 27 | 708 |
| A — v0.5 allocation | Conservative | 171 | 205 | 153 | 143 | 26 | 698 |
| A — v0.5 allocation | Expected | 160 | 193 | 146 | 135 | 25 | 658 |
| A — v0.5 allocation | Optimistic | 152 | 184 | 140 | 130 | 24 | 628 |
| B — enhanced domain analytics | None | 193 | 211 | 155 | 172 | 21 | 752 |
| B — enhanced domain analytics | Conservative | 189 | 208 | 153 | 169 | 21 | 741 |
| B — enhanced domain analytics | Expected | 177 | 196 | 146 | 160 | 20 | 698 |
| B — enhanced domain analytics | Optimistic | 167 | 187 | 140 | 153 | 19 | 666 |
| C — enhanced, core-scope-first | None | 189 | 211 | 155 | 167 | 21 | 743 |
| C — enhanced, core-scope-first | Conservative | 186 | 208 | 153 | 165 | 21 | 732 |
| C — enhanced, core-scope-first | Expected | 173 | 196 | 146 | 156 | 20 | 690 |
| C — enhanced, core-scope-first | Optimistic | 164 | 187 | 140 | 149 | 19 | 659 |

Team totals equal the sum of the four members and the unassigned (TBD) effort.

### 14.6 Incremental Effort (no-AI basis, remaining hours)

| Member | A (v0.5) | B | C | Change A → C | Of which: new or expanded analytics | Of which: replaced/merged tasks |
| --- | --- | --- | --- | --- | --- | --- |
| 김민지 | 174 | 193 | 189 | +15 | BI01 +6.3×0.7, BI02 +5.2, BI03 +5.2×0.6, BI04 7.3 | V05 −5.2 |
| 김한승 | 208 | 211 | 211 | +3 | RV01 +3.2 | — |
| 이선진 | 155 | 155 | 155 | +0 | — | — |
| 지혜인 | 145 | 172 | 167 | +22 | MA01 10.3×0.85, MA02 10.3, MA03 8.5, MA04 10.3×0.7 | J04 −8.5, J05 −4.4 |
| TBD | 27 | 21 | 21 | -5 | R9 removed (−5.2) | — |
| **Team** | **708** | **752** | **743** | **+35** | | |

- 이선진: no change (scope preserved).
- 김한승: +3 h methodology review; R9 assignment to 지혜인 does **not** reduce his existing workload (the task was previously unassigned).
- 김민지: +15 h net in C (BI01–BI04 incremental; V05 replaced).
- 지혜인: +22 h net in C (MA01–MA04; J04 and J05 replaced). The largest relative increase.
- TBD: −5 h (R9 moved to a proposed owner); AWS and end-to-end integration (≈ 21 h) remain unassigned.

### 14.7 Weekly Effort, Scenario C (remaining hours)

**Expected AI productivity (planning basis):**

| Week | 김민지 | 김한승 | 이선진 | 지혜인 | TBD |
| --- | --- | --- | --- | --- | --- |
| W0 | 11 | 10 | 2 | 3 | 0 |
| W1 | 43 | 37 | 26 | 25 | 0 |
| W2 | 46 | 41 | 38 | 31 | 0 |
| W3 | 32 | 48 | 25 | 36 | 6 |
| W4 | 25 | 32 | 31 | 33 | 4 |
| W5 | 7 | 16 | 15 | 17 | 10 |
| W6 | 10 | 12 | 9 | 10 | 0 |
| **Total** | **173** | **196** | **146** | **156** | **20** |
| Recurring | 16 | 33 | 13 | 22 | 0 |

**No AI productivity (upper reference):**

| Week | 김민지 | 김한승 | 이선진 | 지혜인 | TBD |
| --- | --- | --- | --- | --- | --- |
| W0 | 12 | 11 | 2 | 3 | 0 |
| W1 | 48 | 40 | 29 | 27 | 0 |
| W2 | 52 | 45 | 41 | 34 | 0 |
| W3 | 34 | 51 | 26 | 39 | 6 |
| W4 | 27 | 34 | 33 | 36 | 4 |
| W5 | 7 | 17 | 16 | 18 | 11 |
| W6 | 10 | 13 | 9 | 10 | 0 |
| **Total** | **189** | **211** | **155** | **167** | **21** |
| Recurring | 16 | 35 | 13 | 22 | 0 |

C re-sequences without moving milestones: MA03 to W4, MA04 to W4–W5 (after the demo, conditional on MVP), BI01 split W2–W3, BI03 to W4–W5, TECHSTACK and DATA_SPEC started in W0.

### 14.8 Critical Path

```text
W1  Keywords (지혜인) + collector interface, DATA_SPEC, ERD (김민지) + DataLab (김민지 only)
      → collectors (김민지, 이선진, 김한승, 지혜인) → 12/6 sample extract, DATA_CONTRACT, chart interface
W2  Marts, BI02 semantic model (김민지) → Golden Time on samples, shared seasonal statistics (김한승)
      → MA01, MA02 (지혜인)   price index, profitability, BA01, BA03 pilot (이선진)   BI01 (김민지)
      → charts and pages on mock data (김민지, 지혜인); APIs (김한승) → 12/13 result tables, Decision Item 6
W3  Data-to-visualization integration, BI04 (김민지) → end-to-end integration (TBD, R22) → 12/16 freeze → 12/18 demo
W4  Golden Time complete (김한승) → MA03, MA04 (지혜인) ← BA02 (이선진); BI03 (김민지)
W5  AWS (TBD, R21); AV1, AV3; user testing
```

| Blocking item | Owner | Consumers | Mitigation |
| --- | --- | --- | --- |
| DataLab collection | 김민지 | All interest analyses | Sample extract in W1 |
| Shared seasonal statistics and Golden Time output schema | 김한승 | MA02, MA03, MA04, BI03 | Publish schema with the first sample results in W2 |
| BA02 outputs | 이선진 | MA04 | MA04 scheduled after BA02 (W4–W5) |
| Result tables (12/13) | Analytical owners | BI02–BI04, backend, pages | Contracts and mock data from W1 |
| End-to-end integration, AWS | TBD | Demo, release | Assign R21/R22 before W3 |

### 14.9 Risk Classification (Scenario C, expected AI)

| Member | Remaining | Weekly peak | Recurring | Status |
| --- | --- | --- | --- | --- |
| 김민지 | ≈ 173 h | W2 ≈ 46 h, W1 ≈ 43 h | ≈ 16 h | **AMBER** (critical path in W1–W2) |
| 김한승 | ≈ 196 h | W3 ≈ 48 h | ≈ 33 h (highest) | **RED** without relief options |
| 이선진 | ≈ 146 h | W2 ≈ 38 h | ≈ 13 h | **AMBER** |
| 지혜인 | ≈ 156 h | W3 ≈ 36 h, W4 ≈ 33 h | ≈ 22 h | **AMBER** (PM + frontend + MA01–MA04) |
| TBD | ≈ 20 h | W5 ≈ 10 h | — | **RED** until assigned |

### 14.10 Member-Based Weekly Schedule (milestone dates unchanged)

| Week | Milestone | 김민지 | 김한승 | 이선진 | 지혜인 | Acceptance criteria |
| --- | --- | --- | --- | --- | --- | --- |
| W0 11/26–11/29 | Kickoff; Dec 1 planning presentation (R12, unverified) | Proposal v3.5 start; TECHSTACK; DATA_SPEC start; Compose; calibration pilot | Context set; master prompt stored; MVP start; calibration pilot | AI-usage inquiry; calibration pilot | Notion; keyword candidates; calibration pilot | Pilots logged; kanban live |
| W1 11/30–12/6 | **12/6** data, contracts, interfaces | DataLab and code collectors; collector interface; ERD; DATA_SPEC; source/mart contracts; chart interface; sample extract | DATA_FEASIBILITY; MVP; PRD draft; ANALYTICS; API_SPEC; ASOS | KOSIS, KAMIS, settlement-pilot collectors; BUSINESS_ANALYTICS; market size | Keyword selection; mapping; PERSONA; DESIGN; holiday collector; ROADMAP | Contracts agreed; sample extract loaded |
| W2 12/7–12/13 | 12/8 KAMIS check; 12/11 demo data (R11); **12/13** result tables, Decision Item 6 | Preprocessing; marts; BI02 semantic model; BI01 (part); BA01 rules; demo charts (mock) | Golden Time on samples; shared seasonal statistics (schema published); APIs and data access | Sample products; price index; profitability; BA01 phase 1; BA03 pilot | MA01; MA02; app shell and demo pages (mock); interviews | Result tables per contract |
| W3 12/14–12/20 | 12/14–15 integration; 12/16 freeze; **12/18** demo | Data-to-visualization integration; BI01 (part); BI04; ARCHITECTURE | Golden Time; AV1 start; cost risk; TEST_PLAN; PRD final; MA/BI review | Figure checks; research documents | Chart integration; MA02 finish; demo scenario | Demo on real data; charts reconcile |
| W4 12/21–12/27 | **12/27** feature completion | Remaining MVP charts; BI03; BI04; BA01 phase-2 rules | Golden Time complete; AV2; grounded LLM summary | BA01 phase 2; BA02; BA03 full only if approved | MA03; MA04 (if approved); remaining MVP pages; promotion strategy | Features complete |
| W5 12/28–1/3 | **1/3** freeze | BI03 finish; deployment data support | AV1 complete; AI evaluation | AV3; business validation; BA04 only if capacity | MA04 finish; user testing; hosting | Validations reported |
| W6 1/4–1/6 | Final (date R8) | Bug fixes | Bug fixes; documentation consistency | Rehearsal | Final log; rehearsal | Submission |

Required proposal updates for 김민지's review (R17): v3.4 §1 and §11 roles (incl. MA and BI workstreams and R9 proposal); §8 dashboard wording; §10 member-based schedule.

---

## 15. Capacity Assumptions

| Member | Weekly available hours | Confirmed skill constraints | Recurring duties (C, expected) | Status |
| --- | --- | --- | --- | --- |
| 김민지 | TBD | Unconfirmed (pilot) | ≈ 16 h | UNKNOWN |
| 김한승 | TBD | Partially evidenced | ≈ 33 h | UNKNOWN |
| 이선진 | TBD | Unconfirmed (pilot) | ≈ 13 h | UNKNOWN |
| 지혜인 | TBD | Unconfirmed (pilot) | ≈ 22 h | UNKNOWN |

Illustrative capacity (assumptions, not commitments): effective ≈ 5.6 weeks; contingency 20% for debugging, integration, communication, data problems, rework, and schedule changes. AI agents do not add hours.

| Weekly hours | Gross per member | Net per member | Net team (4) | C team remaining, expected AI (690 h incl. TBD) |
| --- | --- | --- | --- | --- |
| 20 | 112 h | 90 h | 358 h | Not feasible |
| 30 | 168 h | 134 h | 538 h | Not feasible (−152 h) |
| 40 | 224 h | 179 h | 717 h | Feasible at team level (+27 h margin) |

Individual sensitivity, Scenario C, expected AI (remaining minus net capacity; positive = overload):

| Member | 20 h | 30 h | 40 h |
| --- | --- | --- | --- |
| 김민지 (173) | +83 | +39 | −6 |
| 김한승 (196; ≈ 172 with relief options) | +106 (+82) | +62 (+38) | +17 (−7) |
| 이선진 (146) | +56 | +12 | −33 |
| 지혜인 (156) | +66 | +22 | −23 |
| TBD (20) | must be assigned | | |

Even where totals fit at 40 h/week, weekly peaks exceed ≈ 32 usable hours for 김민지 (W1–W2), 김한승 (W1–W4), 이선진 (W2), and 지혜인 (W3–W4). Under conservative AI productivity the team needs ≈ 732 h, above the 40 h/week net team capacity.

---

## 16. Workload Optimization Recommendations

### 16.1 Recommended Allocation: Scenario C

| Criterion | A — v0.5 allocation | B — enhanced, full | C — enhanced, core-first |
| --- | --- | --- | --- |
| Analytical quality and portfolio | Weak for 지혜인 and 김민지 (strategy and charts only) | Strong | Strong |
| Role alignment | 김민지 BI without analytics; 지혜인 without analytics | Aligned | Aligned |
| Workload (expected AI) | 658 h | 698 h | 690 h |
| Weekly peaks | Lower | 지혜인 W3 overload | Re-sequenced after the demo |
| Delivery feasibility | Highest on hours, lowest on portfolio value | Lowest | Medium (requires ≈ 40 h/week or further reductions) |

C adds ≈ 32 h (expected AI) over A, concentrated on 지혜인 and 김민지, in exchange for reproducible analytical portfolio evidence for both. B is not recommended because clustering, full BI03, and full MA04 before MVP approval add effort without confirmed product value.

### 16.2 Relief Options (require approval)

| ID | Option | Saving (≈ h, no-AI basis) |
| --- | --- | --- |
| R-a | Domain owners draft PRD sections; 김한승 integrates | 5 (김한승) |
| R-b | MVP as a PRD section | 4 (김한승) |
| R-c | LLM and AI evaluation deferred until MVP confirms AI | 8 (김한승) |
| R-d | PM records decisions in DECISION_LOG during meetings | 3 (김한승), +3 (지혜인) |
| R-e | Cost risk with shared price index and simple baselines only | 4 (김한승) |
| R-f | Minimal context set first | 3 (김한승) |
| R-g | TECHSTACK and DATA_SPEC started in W0 | Peak shift for 김민지 (applied in C) |
| R-j | MA04 deferred entirely if MVP excludes scoring | 7 (지혜인) |
| R-k | BI03 limited to the first-demo screens until MVP approval | 2 (김민지) |
| R-l | R-d not applied while 지혜인 carries MA01–MA04 | Avoids adding PM load |

### 16.3 Reduction Order

Optional documentation → redundant implementations → nonessential collectors → BA04 → BA03 beyond the pilot → MA04 if scoring is not in the MVP → advanced RAG and SQL agents → nonessential charts → excessive model complexity. Preserve essential data quality, Golden Time analysis, baselines, analytical validation, BA01, essential business decision support, and integration and deployment testing.

---

## 17. Decision Register

| ID | Decision | Status | Notes |
| --- | --- | --- | --- |
| R1 | Project Manager | Decided: 지혜인 | — |
| R2 | Presenter | **TBD** | — |
| R3 | Presentation material accountable owner | **TBD** | — |
| R4 | Repository Administrator | Decided: 김한승 | — |
| R5 | Product planning ownership | Corrected | Existing responsibility of 김한승; 김민지 Proposal Owner |
| R6 | Weekly hours and skill constraints | **TBD** | Blocks validation of §14–§15; calibrate with pilots (R25) |
| R7 | Collector distribution incl. settlement pilot for 이선진 | Proposed | §8.2 |
| R8 | Final submission and competition dates | **TBD** | 1/6 vs. 1/7–1/8 |
| R9 | Promotion scoring implementation owner | **Proposed: 지혜인 (MA04), not approved** | Conditional on MVP including scoring; workload +≈ 7 h (C) |
| R10 | BA03 adoption (Decision Item 6) | Due 12/13 | — |
| R11 | BA03 data-readiness gate (12/11) | Recommendation, not approved | — |
| R12 | December 1 planning presentation | Unverified | — |
| R13 | Risk management owner | **TBD** | — |
| R14 | Relief options R-a to R-l | Proposed | §16.2 |
| R15 | Document consolidation | Proposed | §5.2 |
| R16 | Scope reduction if capacity is insufficient | Proposed | §16.4 |
| R17 | Proposal v3.5 | Proposed; Proposal Owner (김민지) review | §14.10 |
| R18 | First-demo scope vs. Golden Time core value | **TBD** | — |
| R19 | Retrospective coordinator | **TBD** | — |
| R20 | BI visualization specification location (DESIGN.md section vs. VISUALIZATION_SPEC.md) | Proposed: DESIGN.md section owned by 김민지 | — |
| R21 | AWS deployment owner | **TBD** | Options in §8.3 |
| R22 | End-to-end integration coordination owner | **TBD** | Options in §8.3 |
| R23 | 김민지 role realignment (BI & Data Visualization Lead; Data Engineering & Data Modeling) | Proposed | — |
| R24 | Marketing analytics MA01–MA04 and BI analytics BI01–BI04 | Proposed | §4, §7 |
| R25 | AI productivity scenario and calibration pilots | Proposed | §14.2–§14.3; expected scenario as planning basis |
| R26 | Re-sequencing of MA03, MA04, BI01, BI03 (no milestone change) | Proposed | §14.7 |

---

## 18. Approval Requirements

| ID | Item |
| --- | --- |
| T1 | Baseline correction (§1.1, §3, §14.3) |
| T2 | Role structure and 김민지 realignment (§2, R23) |
| T3 | Context ownership and BI visualization specification (§5) |
| T4 | Visualization ownership and BI/frontend boundary (§7) |
| T5 | Implementation ownership, collectors, backend and infrastructure (§8) |
| T6 | RACI, deliverables, acceptance criteria (§9–§11) |
| T7 | Overlap resolutions (§12) |
| T8 | Scenario C and relief options (§14–§16) |
| T9 | Open decisions R2, R3, R6–R26 |
| T10 | Marketing analytics MA01–MA04 (§4.4, §7) |
| T11 | BI analytics BI01–BI04 (§4.1, §7) |
| T12 | AI-assisted estimation model and pilots (§14.2–§14.3) |

> **Approval record (2026-11-26):** v0.6 approved by the project lead as the team-role baseline (T1–T8, T10–T12). Items marked *Proposed*, *Recommendation*, or *TBD* in the decision register (§17, T9) remain open and are resolved individually through team governance. Approval does not validate workload estimates, AI productivity assumptions, or member capacity (R6, R25).

| Member | Approval | Date |
| --- | --- | --- |
| 김민지 | ☐ | |
| 김한승 | ☐ | |
| 이선진 | ☐ | |
| 지혜인 | ☐ | |

---

## 19. Change History

| Version | Date | Changes |
| --- | --- | --- |
| 0.1 | 2026-11-26 | Initial proposal: removed all-members-PM structure; separated roles |
| 0.2 | 2026-11-26 | Business analytics BA01–BA04 for 이선진 |
| 0.3 | 2026-11-26 | PM 지혜인; Team Leader tie-break rule |
| 0.4 | 2026-11-26 | Context ownership; overlap audit I-01–I-24; three-point workload model; member-based schedule |
| 0.5 | 2026-11-26 | Baseline correction: planning and context engineering classified as existing responsibilities of 김한승 (v0.4 "31 h transfer" withdrawn) with completed vs. remaining status from repository evidence; 김민지 realigned to BI & Data Visualization Lead (secondary: Data Engineering & Data Modeling) with chart-component ownership; BI/frontend boundary; visualization ownership matrix; backend data access to 김한승; settlement collector pilot to 이선진; AWS and end-to-end integration recorded as TBD (R21, R22); updated audit (I-25–I-38); workload model rebuilt with lifecycle vs. remaining effort for scenarios A/B/C; decision register R1–R23. Status remains PROPOSED |
| 0.6 (approved) | 2026-11-26 | Domain analytics enhancement: 이선진 preserved without new mandatory work; 지혜인 marketing analytics MA01–MA04 (MA04 as proposed R9 resolution, not approved); 김민지 BI analytics BI01–BI04 counted as incremental effort; 김한승 core responsibilities preserved plus methodology review; handoff and duplication rules; issues I-39–I-47; AI-assisted delivery model with conservative/expected/optimistic scenarios and competency calibration pilots; workload model rebuilt on the v0.5 task list; re-sequenced weekly schedule; decision register R24–R26. Status remains PROPOSED |
| 0.6 approval | 2026-11-26 | Approved by the project lead; status changed to APPROVED. No content change; open decisions in §17 remain open |
