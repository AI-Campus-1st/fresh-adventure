# fresh-adventure — PTS Definition (Problem · Target · Solution)

| Item | Value |
| --- | --- |
| Status | **APPROVED** |
| Phase | Phase 01 — PTS Definition and Validation (closed) |
| Version | 0.2 (approved baseline) |
| Date | 2026-11-26 |
| Approved by | Project lead |
| Approval date | 2026-11-26 |
| Source | [Proposal v3.1](../proposal/proposal_v3.1.md) — historical source document, unchanged by this document; it uses the former working title "FreshLens" |
| Scope | Problem framing and validation only. Competitor benchmarking, MVP, PRD, feature specifications, technology, and architecture are out of scope. |

> This approved document is the product strategy baseline and the source of truth for Phase 02 (Market & Competitor Research), Phase 03 (MVP Definition), and Phase 04 (PRD & Project Scope).
> Where this document differs from Proposal v3.1, this document takes precedence.
>
> **Approval establishes product direction only.** It does not constitute empirical validation of user problems, analytical performance, product-market fit, or expected business outcomes. All assumptions and validation requirements below remain open.

---

## 1. Project Identity

| Item | Value | Status |
| --- | --- | --- |
| Project name | fresh-adventure | Confirmed |
| Product name | fresh-adventure | Confirmed |
| Team name | 땅굴탐험대 | Confirmed |
| Product category | Fresh Food Marketing Intelligence | Confirmed |
| Core value | Golden Time Discovery | Confirmed |
| Tagline | *Undecided* | Open decision (see Section 17) |

### Product Definition

fresh-adventure helps merchandising managers and marketers at small and mid-sized online fresh food retailers address the challenges of product perishability and missed sales opportunities by identifying potential sales golden windows and supporting proactive marketing and promotion timing through integrated external market intelligence.

---

## 2. Evidence Classification

Every statement in this document belongs to one of the following classes. They must not be conflated.

| Class | Meaning | Example in this document |
| --- | --- | --- |
| **Industry risk** | Structural characteristic of fresh food commerce | Limited shelf life, price volatility |
| **User problem (hypothesis)** | Pain point assumed for the target user, not yet verified | Difficulty identifying sales windows |
| **Intended business benefit** | Downstream outcome fresh-adventure aims to support, not measured | Waste risk mitigation, profit protection |
| **Available analytical evidence** | What external data can show or be tested against | Seasonal interest patterns, wholesale price changes |
| **Validated product capability** | Capability proven by a predefined test | *None yet* |

As of this version, **no user problem and no product capability has been validated.**

---

## 3. Industry Background

Fresh food (fruits, vegetables, seafood) differs from durable consumer goods in ways that make sales timing structurally important. These are **industry risk factors**. They are not verified pain points of any specific user, and their frequency and severity for the target have not been measured.

| Characteristic | Why it matters for timing |
| --- | --- |
| Limited shelf life | Product value declines with time; the sales window is short. |
| Restricted long-term storage | Inventory cannot simply be held until demand returns. |
| Product value deterioration | Late sales may require lower prices or may not be possible. |
| Limited return and resale opportunities | Opportunities to return or resell are often restricted. Eligibility depends on product characteristics, contracts, applicable policies, and circumstances; not all fresh food is non-returnable. |
| Seasonal demand fluctuation | Consumer interest concentrates in specific periods (seasons, holidays). |
| Market price volatility | Procurement cost can change sharply, affecting promotion margins. |
| Forced markdowns | Product approaching the end of its sellable life may need to be discounted. |
| Unsold inventory | Product not sold within its window loses value. |
| Inventory disposal and food waste | Unsold product may be discarded. |
| Potential financial losses | Markdowns and disposal can reduce margin or cause losses. |

Market-size context cited in Proposal v3.1 indicates market relevance but **does not evidence the user problem**, and has not been re-verified in this phase.

---

## 4. Root Cause Structure

```text
INDUSTRY CHARACTERISTICS (structural risk factors)
  • Perishability, limited shelf life, product value deterioration
  • Restricted storage, limited return and resale opportunities
  • Seasonal demand and market price volatility
            │
            ▼
CORE USER PROBLEM (hypothesis — to be validated)
  • Difficulty identifying potential sales golden windows
  • Uncertainty in marketing and promotion timing
  (consumer interest, seasonality, market prices, and cost risks are hard to evaluate together)
            │
            ▼
POTENTIAL BUSINESS CONSEQUENCES (not measured by fresh-adventure)
  • Missed sales opportunities      • Forced markdowns
  • Unsold inventory                • Margin deterioration
  • Inventory disposal and food waste
  • Potential financial losses
            │
            ▼
SOLUTION (fresh-adventure)
  • Integrated external market intelligence
  • Golden Time discovery
  • Proactive marketing and promotion timing support
```

fresh-adventure intervenes at the **core user problem** layer. It does not observe or measure the business consequences layer directly (see Section 11).

---

## 5. Problem

### 5.1 Problem Statement

Fresh food products have limited shelf lives, restricted long-term storage capabilities, and limited return and resale opportunities. Missing appropriate sales opportunities may result in product value deterioration, forced markdowns, unsold inventory, inventory disposal and food waste, and potential financial losses.

However, fresh food merchandising managers and marketers with limited market analytics capabilities may struggle to identify potential sales golden windows and determine appropriate marketing and promotion timing, because seasonal changes in consumer interest, market prices, and cost-related risks are difficult to evaluate together.

### 5.2 Why the Problem May Recur

Promotion and campaign planning is assumed to be a recurring (weekly and seasonal) decision that requires judging, for multiple products at once, how consumer interest and market prices are changing. The actual planning cadence of target users is unverified.

### 5.3 Evidence Status

| Element | Status |
| --- | --- |
| Industry characteristics (Section 3) | Generally accepted structural facts; not quantified for the target |
| Users struggle to identify sales windows | **Hypothesis** |
| Users rely on experience or the previous year's calendar | **Hypothesis** |
| Timing errors cause losses for users | **Hypothesis** — frequency and severity unverified; no loss data |

---

## 6. Target

### 6.1 Primary Target

Merchandising managers and marketers at **small and mid-sized online fresh food retailers** who:

- Manage multiple fresh food products.
- Participate in product operations, marketing, and promotion planning.
- Possess relevant decision-making authority.
- Have limited dedicated market analytics support.
- Face potential business risks associated with product perishability and missed sales opportunities.

### 6.2 Priority Within the Target

Priority is given to users who are **directly exposed to the economic risks** of:

- Unsold inventory
- Product value deterioration
- Forced markdowns
- Inventory disposal

Exposure depends on **inventory ownership and contractual risk allocation** (for example, who owns the stock, who bears markdown and disposal costs, and whether returns to suppliers are possible).

### 6.3 Retailer Type Suitability (Hypotheses)

The following suitability levels are **hypotheses requiring user validation (B3)**. Sellers of the same type may bear different levels of inventory risk depending on their contracts and operations.

| Retailer type | Typical inventory risk exposure (assumed) | Hypothesized fit |
| --- | --- | --- |
| Retailers that purchase and hold their own inventory (direct purchase) | Retailer bears unsold, markdown, and disposal risk | Higher |
| Consignment or marketplace sellers | Risk may be shared with or borne by suppliers, depending on contract | Uncertain |
| Direct-shipping sellers (e.g., farm-to-consumer, made-to-order shipping) | Inventory risk may sit with producers; timing still affects sales | Uncertain |
| Intermediaries and brokers | Risk allocation varies widely | Uncertain |
| Single-product sellers | Product selection across items is less relevant | Lower |

No retailer type is assumed to experience equivalent inventory risks.

### 6.4 Rationale

- Large online retailers typically hold internal sales, search, and inventory data that is richer than public relative-interest indices; they are less likely to experience the problem severely.
- Teams without analytics support are more likely to rely on experience, so external signals may add more value for them. **This is a hypothesis.**

---

## 7. Solution

### 7.1 Solution Statement

Provide integrated decision support based on consumer interest, seasonality, market prices, and cost-related risks to help users identify potential sales golden windows and determine appropriate marketing and promotion timing.

Support proactive campaign planning and informed business decisions intended to mitigate missed sales opportunities, product value deterioration, and associated financial risks.

### 7.2 Conceptual Value Areas

These are **conceptual value areas, not feature specifications.** Ranking systems, scoring formulas, simulators, specific reports, screen counts, and implementation methods are **not approved in this phase** and are deferred to the MVP and PRD phases.

| Value area | Role |
| --- | --- |
| **Golden Time Discovery** | Core |
| **Marketing Timing** | Core |
| **Promotion Timing** | Core |
| **Cost Risk Awareness** | Core (decision-support guardrail) |
| Product Selection Support | Supporting |
| Customer Interest Understanding | Supporting (subject to data feasibility, DA1) |
| Profitability Assessment | Supporting |
| AI-assisted Interpretation | Supporting |

### 7.3 Cost Risk Governance

- Cost risk is a **decision-support guardrail, not an automatic exclusion rule.**
- fresh-adventure does not automatically exclude products or promotional periods solely because of elevated market price or procurement cost risk.
- Cost risk information is presented for the user's judgment. Actual profitability depends on retailer-specific costs, inventory, selling prices, and operational conditions that fresh-adventure does not observe.

---

## 8. Golden Time and Timing Terminology

### 8.1 Golden Time

**Golden Time** is a potential sales opportunity window identified by jointly evaluating consumer interest, seasonality, market prices, and cost-related risks.

- Golden Time is **not** predetermined to begin at the Rising Point or to end after the Peak.
- Its precise boundaries, thresholds, calculation methods, and analytical conditions **remain undecided until the analysis phase.**
- Golden Time must **not** be presented as a verified revenue-maximizing, profit-maximizing, or waste-minimizing period.

### 8.2 Terminology

| Term | Definition | Basis | Notes |
| --- | --- | --- | --- |
| **Rising Point** | The beginning of a sustained increase in consumer interest | Consumer interest data | Detection method undecided |
| **Peak** | The maximum consumer interest point within a defined seasonal cycle | Consumer interest data | Cycle definition undecided |
| **Golden Time** | A potential sales opportunity window inferred from external market signals | Interest, seasonality, prices, cost risk | Boundaries undecided (8.1) |
| **Marketing Timing** | Appropriate preparation and exposure timing for marketing activities | External signals and user preparation needs | Depends on Preparation Lead Time |
| **Promotion Timing** | Appropriate timing for promotional activities | External signals and user conditions | Cost risk informs but does not exclude (7.3) |
| **Demand Lead Time** | The interval between the Rising Point and the Peak | Consumer interest data | Derivable from external data |
| **Preparation Lead Time** | The preparation period required before executing marketing or promotional activities | User operations (sourcing, content, ad setup, approvals) | **User-specific; cannot be derived from consumer interest data; requires validation (B2)** |

---

## 9. Core Value Proposition

| Value area | Type | Status |
| --- | --- | --- |
| Golden Time Discovery | Primary product value | To be validated (AV1, PV1) |
| Marketing Timing | Primary product value | To be validated (AV1, B2, PV1) |
| Promotion Timing | Primary product value | To be validated (AV1, PV1) |
| Cost Risk Awareness | Primary product value (guardrail) | To be validated (AV2, PV1) |
| Waste Risk Mitigation | Intended downstream business benefit | Not independently validated; not measurable with external data |
| Profit Protection | Intended downstream business benefit | Not independently validated; not measurable with external data |

Waste risk mitigation and profit protection depend on how users act on the information and are outside what fresh-adventure can measure.

---

## 10. PTS Alignment

| Link | Assessment | Reasoning | Remaining gap |
| --- | --- | --- | --- |
| Problem ↔ Target | Moderate | Targeting users directly exposed to inventory risk connects the perishability problem to economic consequences | Inventory ownership and severity unverified (B1, B3) |
| Target ↔ Solution | Strong (expected) | Decision support suits teams without analysts | Usefulness without internal data unverified (PV1) |
| Problem ↔ Solution | Strong (expected) | Timing and price signals are where external data is deepest (interest data since 2016, KAMIS prices since 1996, wholesale settlement data since 2018) | Predictive performance vs. seasonal baselines unverified (AV1) |

---

## 11. Scope and Analytical Limitations

fresh-adventure relies on **external market data only**. Without retailer-level inventory, shelf-life, sales, procurement, promotion performance, and disposal data, fresh-adventure **cannot directly validate or guarantee**:

- Inventory optimization
- Product-level waste reduction
- Actual disposal quantity prediction
- Revenue maximization
- Profit maximization
- Optimal sell-through rates
- Actual promotion effectiveness

fresh-adventure is **not** an inventory management system or a food waste prediction system, and will not be expanded into one in this phase.

Additional data limitations:

- Search and shopping interest are **relative indices** from a single platform (Naver), not sales volumes.
- Relative demographic indices may not support direct cross-segment comparison (DA1).
- Online transaction statistics are available at **category level** only, not product level (DA2).
- Online competitor prices are unavailable through legitimate automated collection; offline retail prices (KAMIS) are used as the market price reference.
- Preparation Lead Time cannot be derived from external data.

---

## 12. Alternative PTS Comparison

| Option | Description | Strengths | Weaknesses | Decision |
| --- | --- | --- | --- | --- |
| **A. Golden Time (this document)** | Timing-centered, cost risk as guardrail, small and mid-sized retailers exposed to inventory risk | Strongest data coverage; perishability gives a clear rationale | User problem unverified; predictive value vs. seasonal baselines unverified | **Selected (approved 2026-11-26)** |
| B. Cost-risk-centered | Procurement price risk as the main product | Richest supply-side data | Possible overlap with existing public price outlook services (to be checked later); reverses the v3 demand-side decision | Not recommended |
| C. Proposal v3.1 as is | Five decision questions, broad target including large retailers | Broad demonstration scope | Weak evidence for "who" and "how much"; target likely has better internal data | Not recommended |

---

## 13. Assumptions and Evidence Gaps

| ID | Assumption | Current evidence | Validation |
| --- | --- | --- | --- |
| A1 | Target users set promotion timing mainly by experience or the previous year's calendar | None | B1, B4 |
| A2 | Timing errors cause meaningful losses for target users | None; no loss figures are assumed | B1, B3 |
| A3 | Changes in consumer interest track actual demand | Testable at category level only | AV3 |
| A4 | Timing inference adds value beyond seasonal baselines | None | AV1 |
| A5 | Product-level demographic interest can be queried and compared across segments | Not tested | DA1 |
| A6 | Category-level online transaction statistics are available | Table ID not confirmed | DA2 |
| A7 | Market statistics cited in Proposal v3.1 are accurate | Sources cited, not re-verified | Primary source check |
| A8 | Perishability is a significant consideration in promotion planning | Structural reasoning only | B1 |
| A9 | Users directly exposed to inventory risk can be identified and reached | None | B3 |
| A10 | Integrated external intelligence reduces research effort or improves decisions | None | PV1 |

---

## 14. Validation Requirements

All acceptance criteria must be **defined and agreed before testing**. Results are reported as observed, including negative results.

### 14.1 Business Validation

| ID | Topic | What to learn from actual user experiences |
| --- | --- | --- |
| B1 | Problem frequency and severity | Recent promotion planning examples; how often timing was missed; what happened as a result |
| B2 | Decision-making constraints | Preparation Lead Time (sourcing, content, ad setup, approvals); who decides and when |
| B3 | Inventory ownership and financial risk | Who owns inventory; who bears markdown and disposal costs; how unsold inventory is handled |
| B4 | Existing workarounds and research effort | Current information sources, tools, and time spent on market research |
| B5 | Value of earlier market signals | Whether earlier signals would change actual decisions, and how |

- Interviews should collect concrete recent examples rather than opinions.
- **Majority agreement in interviews alone is not sufficient evidence of product-market fit.**

### 14.2 Analytical Validation

| ID | Validation | Requirements |
| --- | --- | --- |
| AV1 | Timing inference (Rising Point, Peak, Golden Time) | Predefine evaluation products, metrics, and acceptance criteria. Compare against appropriate **seasonal baselines** (e.g., same week last year, multi-year seasonal average timing). |
| AV2 | Cost risk detection | Compare against meaningful **simple baselines** (e.g., previous-period price, seasonal average price). Random selection must not be the only baseline. |
| AV3 | Proxy validity | Relationship between category-level interest and category-level online transaction values, after seasonal adjustment. Product-level sales validation is not expected. |

All analytical validations must maintain **temporal consistency** (only information available at each decision point) and **prevent data leakage**.

### 14.3 Data Availability

| ID | Requirement | Notes |
| --- | --- | --- |
| DA1 | Product-level demographic interest query feasibility | Before calculating demographic shares, verify whether the relative indices support valid cross-segment comparisons. |
| DA2 | Category-level online shopping transaction statistics availability | Confirm the statistics table. Product-level sales data is **not** required from this source. |

### 14.4 Product Value Validation

| ID | Validation | Requirements |
| --- | --- | --- |
| PV1 | Overall product usefulness | Evaluate whether integrated market intelligence provides additional decision value or reduces research effort compared with existing workflows (B4). This is distinct from analytical performance. |

---

## 15. Risks and Limitations

| Risk | Type | Impact | Mitigation |
| --- | --- | --- | --- |
| User problem not confirmed | Business | High | Business validation before MVP scope is fixed |
| Target users with inventory risk are hard to reach | Business | Medium | Identify retailer types early (B3) |
| Timing inference does not beat seasonal baselines | Analytical | High | AV1 early; see Section 16 |
| Golden Time misread as a guaranteed outcome | Communication | Medium | "Potential" wording; show evidence and uncertainty |
| Cost risk misread as an exclusion rule | Communication | Medium | Guardrail governance (7.3) |
| Relative interest ≠ sales | Analytical | Medium | AV3; disclose limitation |
| Naver user bias | Analytical | Low–Medium | Disclose as proxy limitation |
| Demographic data unavailable or not comparable | Data | Medium (supporting value only) | DA1 |
| DataLab terms of service (no fees, no redistribution; interpretation of AI usage) | Legal | Medium | Non-commercial operation; derived indicators only for AI inputs |
| No commercial model under current data terms | Business | Medium | Position as a prototype; commercialization requires license review |
| Short schedule (2026-11-24 to 2027-01-07) | Delivery | High | Keep core value narrow |

---

## 16. Redesign and No-Go Conditions

Thresholds must be agreed before testing. A failed analytical test triggers **simplification, claim restriction, or solution review**; it does not automatically invalidate the entire product.

| Condition | Response |
| --- | --- |
| B1–B3: target users do not report timing difficulty, or are not exposed to inventory risk | Re-examine the target segment or re-frame the problem |
| AV1: timing inference does not beat seasonal baselines | Restrict claims to descriptive market monitoring; simplify timing outputs; review the solution |
| AV2: cost risk detection does not beat simple baselines | Present cost information as reference only; restrict claims |
| AV3: no meaningful category-level relationship between interest and transactions | Present interest as attention signals only, not demand |
| DA1: demographic data unavailable or not comparable across segments | Remove or restrict Customer Interest Understanding |
| PV1: no additional decision value or effort reduction vs. existing workflows | **Solution review**; consider No-Go |
| DataLab usage judged non-compliant | **No-Go** for DataLab-based value; rebuild on other sources or redesign |

---

## 17. Decisions, Approval, and Change Control

### 17.1 Approved Decisions

Decisions D1–D7 were approved by the project lead on 2026-11-26 as the product strategy baseline. They define direction; they are not validated findings.

| ID | Decision | Approved baseline | Status |
| --- | --- | --- | --- |
| D1 | Primary target and priority | Small and mid-sized online fresh food retailers; priority to users directly exposed to inventory risk (Section 6) | Approved 2026-11-26 |
| D2 | Core value areas | Golden Time Discovery, Marketing Timing, Promotion Timing, Cost Risk Awareness | Approved 2026-11-26 |
| D3 | Supporting value areas | Product Selection Support, Customer Interest Understanding, Profitability Assessment, AI-assisted Interpretation | Approved 2026-11-26 |
| D4 | Golden Time and timing terminology | Section 8 | Approved 2026-11-26 |
| D5 | Cost risk governance | Guardrail, not exclusion (Section 7.3) | Approved 2026-11-26 |
| D6 | Validation plan | Section 14 | Approved 2026-11-26 |
| D7 | Redesign and No-Go conditions | Section 16 | Approved 2026-11-26 |

### 17.2 Unresolved Items

| Item | Resolution phase |
| --- | --- |
| Tagline | Branding decision (open) |
| Golden Time boundaries, thresholds, and calculation methods | Analysis phase |
| Evaluation products, baselines, metrics, and acceptance criteria | Before analytical validation |
| Retailer type suitability | Business validation (B3) |
| Preparation Lead Time ranges | Business validation (B2) |
| Feature specifications, ranking, scoring, simulators, reports, screens | MVP and PRD phases |

### 17.3 Approval Record

| Approver | Scope | Decision | Date |
| --- | --- | --- | --- |
| Project lead | PTS v0.2, decisions D1–D7 | Approved | 2026-11-26 |

Individual approvals by other team members are not recorded in this document.

### 17.4 Baseline and Change Control

This approved PTS (v0.2) is the baseline for:

- Phase 02 — Market & Competitor Research
- Phase 03 — MVP Definition
- Phase 04 — PRD & Project Scope

Any material change to this PTS (problem, target, solution, value areas, terminology, validation plan, or No-Go conditions) must be documented, justified with evidence, and explicitly approved. Approved changes are recorded as a new version in the change log (Section 18).

---

## 18. Change Log

| Version | Date | Changes |
| --- | --- | --- |
| 0.1 | 2026-11-26 | Initial proposed PTS: perishability-centered problem, small and mid-sized retailer target, Golden Time definitions, validation plan |
| 0.2 | 2026-11-26 | Applied project identity (fresh-adventure, 땅굴탐험대); tagline marked undecided; added inventory-risk priority and retailer type hypotheses; redefined Golden Time without fixed boundaries; split Demand Lead Time and Preparation Lead Time; cost risk changed to guardrail (no automatic exclusion); value areas made conceptual (no feature specifications); validation restructured into business, analytical, data availability, and product value; seasonal and simple baselines required; failed analytical tests trigger simplification or review rather than automatic invalidation |
| 0.2 (approved) | 2026-11-26 | Approved by the project lead as the product strategy baseline; decisions D1–D7 accepted; status changed to APPROVED. No change to strategy content. Approval does not constitute empirical validation. |
