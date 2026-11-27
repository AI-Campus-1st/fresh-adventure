# fresh-adventure — Project Rules

| Field | Value |
| --- | --- |
| Document | RULES.md |
| Version | 0.6 |
| Status | PROPOSED |
| Last Updated | 2026-11-27 |
| Approved by | Pending |
| Approval Date | Pending |
| Document Owner | 김한승 |
| Project | fresh-adventure |
| Team | 땅굴탐험대 |
| Track | Initial Context Engineering |
| Scope | All project repositories and contributors |

## Korean Summary

- 승인된 PTS와 프로젝트 문서를 기준으로 작업한다.
- 데이터 분석은 검증 가능한 근거와 재현성을 확보한다.
- 승인 없이 제품 범위, 분석 방법, 기술 명세를 변경하지 않는다.
- 실제 `.env`, API 키, 계정정보 및 비밀정보를 AI, Git, 로그, 공개 결과물에 노출하지 않는다.
- AI 개발 도구는 Claude Code를 사용한다. CLAUDE.md를 AI 실행 지침의 정본으로, AGENTS.md는 최소 호환 지침으로 유지한다.
- AI 생성 결과는 사람이 검토하며, 확인되지 않은 결과를 사실로 표현하지 않는다.
- AI의 커밋과 푸시는 각각 명시적 승인이 필요하다.
- 작업 위험도에 비례하는 검증을 수행하고 승인된 Context의 최신성을 유지한다.

## 1. Purpose and Scope

These rules define the shared governance, analytical, engineering, security, and collaboration standards for fresh-adventure.

They apply to all human contributors and AI agents across:

- `fresh-adventure`
- `fresh-adventure-data`
- `fresh-adventure-be`
- `fresh-adventure-fe`

Prioritize analytical reliability, reproducibility, maintainability, development efficiency, and successful delivery.

Human contributors remain accountable for project decisions and AI-assisted deliverables.

Apply controls proportionate to project size, task complexity, and actual risk without weakening mandatory safeguards.

## 2. Context Authority

### 2.1 Authoritative Sources

Apply the following precedence when resolving instruction conflicts:

1. Applicable laws, provider terms, security restrictions, and actual access permissions.
2. Approved `RULES.md` for project-wide governance.
3. Approved [`PTS.md`](docs/planning/PTS.md) for product strategy.
4. Approved [`TEAM_ROLES.md`](docs/planning/TEAM_ROLES.md) and [`docs/conventions.md`](docs/conventions.md) within their respective governance domains.
5. Approved `MVP.md` and `PRD.md` for product requirements.
6. Approved domain specifications for analytical and technical definitions.
7. Approved repository-specific `CLAUDE.md` instructions.
8. Authorized task instructions and GitHub issues.

This precedence does not authorize one document to redefine another document's domain.

`AGENTS.md` provides compatibility instructions and references the authoritative project context. It must not introduce conflicting project rules.

`SHARED_CONTEXT.md` distributes approved shared context and is not an independent authority.

GitHub issues and task prompts define authorized work scope. They must not override approved rules or requirements.

Existing conventions without verified approval status must not be treated as authoritative exceptions to project-wide rules.

### 2.2 Document Status and Conflicts

Governance and specification documents must identify their version and approval status:

- `DRAFT` — Work in progress.
- `PROPOSED` — Submitted for review.
- `APPROVED` — Authorized for project use.
- `SUPERSEDED` — Replaced by a later approved version.

A committed document is not necessarily approved or pushed.

Maintain one authoritative source for each substantive rule, requirement, metric, or specification.

Do not treat drafts, historical proposals, or AI-generated suggestions as approved decisions.

If a material conflict cannot be resolved, stop the affected work, identify the conflicting sources, and request clarification.

## 3. Project Governance

Follow the approved PTS as the strategic baseline.

Follow PTS Section 8 for the definition and interpretation constraints of Golden Time.

Do not prematurely establish product features, analytical formulas, or technical decisions.

Context Engineering is a supporting project track and does not redefine the approved PTS phase framework.

Project-wide governance documents require Project Lead approval under the approved team governance structure.

Follow the latest approved `TEAM_ROLES.md` for responsibilities and domain ownership.

Consult affected domain owners before making material cross-domain decisions.

Context ownership does not grant unilateral decision authority.

Significant changes require a documented rationale, affected scope, risks, dependencies, validation approach, and appropriate approval.

Record significant architectural and governance decisions in [`DECISION_LOG.md`](docs/DECISION_LOG.md) or an equivalent approved record.

Preserve historical documents and approved decisions.

## 4. Execution Standards

Inspect relevant context, files, dependencies, requirements, and existing changes before execution.

Identify material assumptions and select the simplest appropriate approach.

| Level | Examples | Required Workflow |
| --- | --- | --- |
| 1 — Routine | Typographical corrections, comments, non-behavioral documentation fixes | Inspect, execute, validate, report |
| 2 — Standard | Approved collector implementation, EDA, approved feature implementation | Inspect, plan, execute, validate, report |
| 3 — Significant | Shared schema changes, material dependencies, methodology changes, security architecture changes | Inspect, plan, obtain approval, execute, validate, report |

The executing contributor or agent proposes the task classification. Authorized human contributors retain authority to correct it.

When classification is uncertain, apply the higher risk level.

Existing task authorization is sufficient for routine and standard work within its approved scope.

Explicit authorization in the original task request satisfies the relevant approval checkpoint when its scope is clear.

Implementation authorization does not implicitly authorize commits, pushes, merges, deployments, or destructive operations.

Authorized experiments may proceed in isolated and compliant environments without establishing unapproved production decisions.

Report actual results, validation evidence, unresolved issues, and limitations.

Mandatory security safeguards apply to every task level.

## 5. Analytical Standards

Define the business question, analytical objective, population, observation period, and measurement units.

Evaluate data coverage, representativeness, measurement limitations, missing values, and potential bias.

Choose methods appropriate to the analytical question and available evidence.

Use suitable baseline comparisons and validation procedures.

For time-dependent predictive analysis, use chronological validation and prevent future-data leakage.

Distinguish observations, estimates, assumptions, hypotheses, and recommendations.

Do not automatically interpret consumer interest indicators as actual demand, purchases, revenue, conversion, or market share.

Do not automatically interpret market prices as individual seller costs or margins.

Do not claim causation, statistical significance, model accuracy, or business outcomes without supporting evidence.

Maintain reproducible analytical code, input references, preprocessing procedures, parameters, and relevant environment information.

Trace analytical outputs to their data sources and methods.

Report uncertainty, limitations, negative results, and failed validation.

Never fabricate or selectively conceal analytical findings.

Define specific formulas, thresholds, metrics, and acceptance criteria in approved analytical specifications.

## 6. Data Governance

Verify source availability, permissions, coverage, granularity, and usage conditions before relying on data.

Record source provenance, collection dates, relevant transformations, and applicable restrictions.

Document provider-specific restrictions on collection, authentication, credential ownership, retention, redistribution, and AI processing.

Follow approved provider-specific rules in `docs/conventions.md` and relevant data specifications.

For NAVER APIs, verify applicable credential ownership, sharing, and rate-limit restrictions against current provider terms.

Do not share credentials or distribute requests across credentials to circumvent provider restrictions.

Validate schemas, missing values, duplicates, units, timestamps, and invalid observations.

Document material preprocessing decisions.

Distinguish zero values from missing, unavailable, or suppressed observations.

Preserve raw data only when permitted. Maintain permitted reproducibility records when raw data retention is restricted.

Clearly label synthetic, sample, and test data.

Apply least-privilege access.

Do not transfer restricted datasets or confidential project information into public repositories or unauthorized external systems.

Approval to use an AI tool does not authorize processing data prohibited by provider terms.

## 7. Engineering Standards

Preserve the four independent repository boundaries.

Do not introduce Git submodules, a parent Git repository, or unnecessary infrastructure without approval.

Use modular, maintainable, and proportionate implementations.

Follow approved interfaces, schemas, and data contracts.

Do not silently duplicate or redefine analytical logic across repositories.

Use appropriate dependency management, configuration management, input validation, error handling, and sanitized logging.

Test affected behavior and review affected documentation.

Keep experimental code distinguishable from production implementations.

Use existing designated experimental locations, including the Data repository's `notebooks/` structure where applicable, or approved experiment branches.

Do not introduce unnecessary directories or production dependencies solely for exploratory work.

## 8. AI-Assisted Development

Claude Code is the designated AI-assisted development tool across all project repositories.

Codex and other AI coding tools are not currently used. Introducing another AI coding tool requires an approved decision.

This section implements decision [D-001](docs/DECISION_LOG.md#d-001--ai-coding-tools-and-agent-context-architecture).

### 8.1 Agent Instruction Architecture

Maintain one authoritative repository-specific AI execution protocol in `CLAUDE.md`.

Maintain a minimal `AGENTS.md` for compatibility with other AI agents.

The presence of `AGENTS.md` does not constitute authorization to use another AI coding tool.

`AGENTS.md` must:

- Identify the repository scope.
- Reference `CLAUDE.md` and the applicable authoritative shared context.
- Retain essential security and authorization safeguards.
- Avoid duplicating comprehensive project rules or technical specifications.

An authorized agent must explicitly read referenced instructions when its tool does not load them automatically.

Preserve valid existing instructions during migration and eliminate conflicting or circular references.

Maintain this architecture consistently across all four repositories.

### 8.2 AI Accountability

AI agents must inspect relevant approved context and existing implementations before making material changes.

Human contributors remain accountable for AI-generated code, analysis, documentation, and decisions.

Never fabricate file contents, data sources, citations, API capabilities, analytical results, test outcomes, or completion status.

Do not conceal failures or unresolved limitations.

Product-facing AI responses must rely on permitted data and appropriately validated evidence.

Communicate uncertainty when sufficient evidence is unavailable.

## 9. Security and Secret Protection

### 9.1 Mandatory Protection

Protect confidential and security-sensitive information, including:

- Actual `.env` and secret-bearing configuration files.
- API keys, restricted Client IDs, Client Secrets, passwords, and private account information.
- Database credentials and credential-bearing connection URLs.
- Cloud credentials, access tokens, private keys, cookies, and session credentials.
- Personal information, restricted datasets, and sensitive infrastructure details.

Apply these protections to both public and private repositories.

A private repository is not a secret store.

Never hardcode, commit, publish, or disclose actual credentials.

Store secrets only in authorized local secret files, runtime environment variables, or approved secret-management systems.

Configuration templates must contain placeholders only.

### 9.2 AI Access and Runtime Usage

AI agents must not directly read, print, reproduce, transmit, or disclose actual secret values.

Do not inspect secret-bearing files or circumvent access restrictions through alternate tools, shell commands, scripts, or subprocesses.

Do not dump environment variables, authentication headers, or unredacted configuration.

Use non-disclosing checks such as file existence, variable presence, and sanitized connection outcomes.

Authorized applications may consume secrets at runtime for approved operations without exposing their values to AI agents, tool outputs, or logs.

Do not include secrets in prompts, transcripts, context files, screenshots, or unauthorized services.

Establish and verify appropriate technical access restrictions before using real credentials in AI-assisted development environments.

Instruction files alone are not security controls.

### 9.3 Repository and Publication Protection

Maintain appropriate `.gitignore` rules and verify that secret-bearing files are not tracked.

Prevent confidential information from entering Git history, logs, notebooks, documentation, reports, and published artifacts.

Never expose private credentials through browser-side code, frontend configuration, or client-accessible build artifacts.

Apply technology-specific security controls when Docker, cloud services, CI/CD, or other relevant technologies are introduced.

Maintain detailed implementation procedures in an approved security guide when established.

### 9.4 Proportionate Security Verification

Perform security verification appropriate to the changed files, affected artifacts, and actual risk before committing, pushing, publishing, or deploying.

- Routine changes: verify affected files and relevant tracking status. Use automated scanning where operational.
- Standard development: review affected code and configuration for accidental disclosure, hardcoded credentials, and unsafe logging.
- Security-sensitive changes: require explicit approval and validation of affected access controls and exposure paths.

Use an approved secret scanner with redacted output when operational. Enable supported remote protection where authorized.

Until an approved scanner is operational, an authorized human contributor may perform a proportionate manual review of affected changes instead.

Do not expose potentially secret-bearing raw content to AI agents during security verification.

Separate human review from AI execution authorization. Reuse completed verification when the reviewed content remains unchanged.

Block affected operations when required security verification fails, remains incomplete, or indicates potential credential exposure.

Never bypass security warnings or disable safeguards to complete a task.

### 9.5 Incident Response

Treat suspected credential exposure as a security incident.

Stop further disclosure and affected publication or deployment.

Notify the Project Lead, repository administrator, and affected credential or data owner through an authorized private channel.

Never reproduce the exposed secret in an incident report.

The authorized credential owner must promptly revoke or rotate compromised credentials.

Assess affected Git history, logs, AI sessions, artifacts, and external systems.

Deleting a file or adding it to `.gitignore` does not resolve an existing exposure.

Perform remediation within authorized scope and verify recovery before resuming affected operations.

Keep incident records proportionate to the impact. Do not rewrite shared Git history or perform destructive cleanup without specific authorization.

## 10. Git and Collaboration

Inspect the repository, branch, working tree, and existing changes before modifying files.

Preserve unrelated work and other contributors' changes.

Follow approved Git conventions in `docs/conventions.md`.

Use focused branches and reviewable changes for implementation work.

Direct commits to `main` are permitted only for low-risk documentation changes explicitly allowed by approved conventions.

Such exceptions do not waive security verification or AI authorization requirements.

Use meaningful commits and follow applicable pull request and review requirements.

AI agents require explicit authorization for commits, pushes, merges, deployments, and destructive Git operations.

Explicit authorization in the original task request is sufficient for the specified operation and scope.

Commit authorization does not imply push authorization.

Do not force-push, reset shared history, delete branches, or discard existing changes without specific authorization.

Report working-tree changes, commit status, and remote synchronization status separately.

## 11. Context Maintenance

### 11.1 Versioning

Use `0.x` versions for initial or evolving documentation and `1.0` for the first stable baseline explicitly designated by the approving authority.

Version numbers do not determine approval status.

Substantive amendments to approved documents require a new version and appropriate approval.

Maintain revision history and preserve approved historical versions through Git history or existing archival conventions.

### 11.2 Shared Context

The main repository is the authoritative source of approved shared project context.

Maintain lightweight `docs/SHARED_CONTEXT.md` files in the Data, Backend, and Frontend repositories.

Include authoritative references, approved versions, source commit SHA, synchronization date, verified synchronization status, and essential shared constraints.

Avoid unnecessary duplication of authoritative documents.

### 11.3 Synchronization and Refinement

Follow the global and local context ownership responsibilities defined in the latest approved `TEAM_ROLES.md`, Section 6.

The global context owner identifies affected repositories when approved shared context changes.

The global context owner updates `SHARED_CONTEXT.md` snapshots through pull requests. Local context owners review those updates.

Local context owners maintain their repository-specific `CLAUDE.md` and local documentation.

Begin synchronization when a shared context change becomes the authorized baseline.

Complete synchronization before affected work relies on the changed context.

Disclose unverified context or unavailable source access.

Block material decisions that depend on missing or outdated context.

Refine repository context after relevant product requirements, analytical methods, and technical designs are approved.

Maintain concise, actionable instructions and avoid unnecessary synchronization infrastructure.

---

## Revision History

| Version | Date | Status at Revision | Description |
| --- | --- | --- | --- |
| 0.1 | 2026-11-27 | PROPOSED | Initial project-wide governance and quality standards. |
| 0.2 | 2026-11-27 | PROPOSED | Strengthened secret protection, approval rules, collaboration conventions, and context maintenance. |
| 0.3 | 2026-11-27 | PROPOSED | Clarified agent instruction governance, transitional security verification, and document references. |
| 0.4 | 2026-11-27 | PROPOSED | Established CLAUDE.md as the primary agent protocol, retained minimal AGENTS.md compatibility instructions, and introduced proportionate security verification. |
| 0.5 | 2026-11-27 | PROPOSED | Designated Claude Code as the sole AI coding tool (D-001), clarified that AGENTS.md does not authorize other tools, and qualified the security guide reference. |
| 0.6 | 2026-11-27 | PROPOSED | Moved to the repository root, corrected the TEAM_ROLES section reference (Section 6), and aligned shared context update responsibilities with TEAM_ROLES v0.6. |
