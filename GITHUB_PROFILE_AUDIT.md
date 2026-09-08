# GitHub Profile Audit

Audit date: 8 September 2026

Account: [`Rahul-vignesh-k`](https://github.com/Rahul-vignesh-k)

## Executive assessment

The account has three credible AI systems and sixteen early C exercise repositories. The strongest technical signal is present, but the old profile README and repository metadata make it difficult to see. The immediate strategy should be depth over volume: feature the three AI systems, document their implementation status precisely, and remove early exercises from the default recruiter path through archiving or privacy changes.

The public website and résumé currently describe Rahul as a **UNSW student / transfer candidate**, not a graduate. The redesigned README preserves the verified wording. Change it to “recent graduate” only after the education status is confirmed and the website and résumé are updated consistently.

## Public repository inventory

### Keep public + feature

| Repository | Why it belongs in the portfolio | Priority follow-up |
|---|---|---|
| [`rag-system`](https://github.com/Rahul-vignesh-k/rag-system) | Strongest production engineering evidence: hybrid retrieval, reranking, citation enforcement, evaluation, authentication, exact-source authorization, rate limiting, structured logging, hardened containers, and CI security gates. | Publish a verified evaluation report and container package. |
| [`energy_demand_web_application`](https://github.com/Rahul-vignesh-k/energy_demand_web_application) | End-to-end applied ML system with real model artifacts, backend/frontend boundaries, validation on measured data, tests, and a usable planning interface. | Add a hosted demo or short walkthrough. |
| [`Job-Application-Agent`](https://github.com/Rahul-vignesh-k/Job-Application-Agent) | Clear agentic-system signal: supervisor/specialist roles, state transitions, approval gates, RAG-assisted matching, persistent memory, audit events, API, and UI. | Implement and test one real source adapter and one non-submitting browser dry-run before calling it automated. |

### Keep public

| Repository | Reason |
|---|---|
| [`Rahul-vignesh-k`](https://github.com/Rahul-vignesh-k/Rahul-vignesh-k) | Required profile repository. Its README is now the account’s recruiter-oriented landing page and the audit records the maintenance strategy. |

### Consider archiving

Archiving is the preferred reversible action for these historical exercises. They show basic C practice but do not support the current AI Engineer positioning, and each repository contains only a code sample inside `README.md` rather than a maintained project.

| Repository | Reason |
|---|---|
| `sumseries` | Small recursion/factorial exercise with no project documentation or tests. |
| `dividing-an-array` | Single recursion exercise; no connection to current portfolio positioning. |
| `powers-of-numbers` | Basic recursive power function only. |
| `classdata` | Basic fixed-size array exercise only. |
| `lucky` | Basic loops/digit-sum exercise only. |
| `triangles` | Basic conditional/input exercise only. |
| `employee-data` | Introductory structs and sorting exercise; still too small to feature. |
| `word-frequency-using-pointers` | Introductory string exercise; the name overstates pointer-specific engineering. |
| `temperatuer` | Basic array exercise with a misspelled repository name. |
| `word-count` | Basic character-counting exercise, not a reusable word-count project. |
| `armstrong` | Introductory number-property exercise with code embedded in the README. |

### Consider making private

Use privacy rather than archiving if the goal is a very clean public footprint. These repositories contain visibly incomplete or unsafe examples that create a stronger negative signal than the other exercises.

| Repository | Reason |
|---|---|
| `accessing-characters` | The displayed C source contains a stray `kr` token and does not compile as written. |
| `changing-letters` | Missing the `ctype.h` include and uses `sizeof` on a function parameter in a misleading way. |
| `caes` | Uses `strcmp` without including `string.h`; name and purpose are unclear. |
| `lock` | Writes a null terminator beyond a five-byte array and presents a hard-coded password exercise as a “lock.” |
| `Rahulvijju` | Public API reports no accessible contents; it adds no portfolio evidence and duplicates the personal-name signal. |

No repository should be deleted automatically. Before changing visibility, check whether any links, coursework submissions, or external references depend on it.

## Pinned repository strategy

Pin only the three repositories that currently meet a meaningful portfolio bar, in this order:

1. **Job-Application-Agent** — strongest agentic/product narrative, with prototype status made explicit.
2. **energy_demand_web_application** — strongest visual applied-ML product and measured forecasting evidence.
3. **rag-system** — strongest production, security, evaluation, and delivery engineering evidence.

Do not fill the remaining three slots with introductory exercises. An intentionally sparse set of strong pins is more credible than six mixed-quality projects.

## Portfolio gaps and recommended projects

### 1. Agent Reliability Lab

Build an evaluation and observability service for agent workflows: trace ingestion, tool-call replay, golden scenarios, deterministic policy checks, cost/latency dashboards, prompt/version comparisons, and red-team cases. This would prove agent evaluation, guardrails, and operational maturity beyond orchestration.

### 2. Event-Driven Document Intelligence Platform

Create an ingestion pipeline using object storage, a queue, asynchronous workers, OCR/parsing, idempotent indexing, dead-letter handling, tenant isolation, and retrieval freshness metrics. This would add distributed systems, cloud architecture, data-pipeline reliability, and multi-tenant security.

### 3. Forecasting MLOps Service

Extract a smaller model from EnergyAI into a reproducible training-to-serving project with experiment tracking, dataset/model versioning, drift checks, canary deployment, rollback, and scheduled retraining. This would make MLOps evidence explicit instead of implicit.

## Flagship README audit

### Job-Application-Agent

| Area | Finding | Recruiter-ready action |
|---|---|---|
| Positioning | The old README described automated discovery and submission even though source connectors and form submission are stubs. | Reframe as an agentic workflow prototype and add a transparent implementation-status table. **Implemented in this redesign.** |
| Screenshot/demo | No product screenshot or verified demo recording is checked in. | Add one dashboard screenshot and a 60–90 second dry-run GIF after a repeatable seeded demo exists. |
| Architecture | State-machine text existed, but agent roles and data boundaries were not visualized. | Add supervisor/specialist/data-flow architecture. **Implemented in this redesign.** |
| Quick start | Commands existed but did not explain stub behavior. | Provide exact local and Docker commands plus verification steps. **Implemented in this redesign.** |
| API docs | Endpoint table existed; OpenAPI and prototype semantics were not prominent. | Link `/docs` and label incomplete operations. **Implemented in this redesign.** |
| Evaluation/results | No measured matching quality, workflow reliability, latency, or cost results. | Add a seeded evaluation set only after expected outputs are manually verified. |
| Testing | No automated test suite or CI workflow is present. | Add unit tests for state transitions, memory precedence, CRUD, API contracts, and non-submitting Playwright dry-runs; gate them in GitHub Actions. |
| Deployment | Docker files exist, but production readiness is not demonstrated. | Add non-root execution, dependency locking, health/readiness separation, and a CI image build before using “production.” |
| Security | Secrets are ignored and examples exist, but credentials, uploaded résumés, screenshots, and model prompts need a threat model. | Document data retention, redact audit fields, externalize secrets, and make submission opt-in with a dry-run default. |

The verification install on 8 September 2026 reported **10 npm audit findings** (1 low, 2 moderate, 7 high). Triage the affected dependency paths and test targeted upgrades; do not apply a forced major-version audit fix without reviewing UI behavior.

### energy_demand_web_application

| Area | Finding | Recruiter-ready action |
|---|---|---|
| Positioning | The old README opened with internal migration detail rather than user value. | Lead with the forecasting/solar product and connect claims to model and validation evidence. **Implemented in this redesign.** |
| Screenshot/demo | Strong screenshots exist but were absent from the README. | Add the verified 30-day results screenshot. **Implemented in this redesign.** Add a hosted demo or video later. |
| Architecture | `ARCHITECTURE.md` is useful but mostly prose. | Add an at-a-glance runtime/model flow and keep the detailed document. **Implemented in this redesign.** |
| Quick start | Core commands and `.env.example` files exist. | Separate prerequisites, configuration, backend, frontend, demo data, and verification. **Implemented in this redesign.** |
| API docs | A route list and `docs/api.md` exist. | Link the detailed API document from the first screen. **Implemented in this redesign.** |
| Evaluation/results | Real four-building results are documented with limitations. | Surface WAPE/closeness without generalizing beyond the measured portfolio. **Implemented in this redesign.** Add site-held-out and seasonal evaluation next. |
| Testing | Backend, contract, integration, model-golden, frontend, and CI tests exist. | State exact commands and what they cover. **Implemented in this redesign.** Confirm whether `httpx2` in `requirements-dev.txt` is intentional. |
| Deployment | Local Vite/FastAPI workflow and CI exist; no container or hosted production deployment is present. | Add a deployment reference architecture and health/rollback plan before claiming production deployment. |
| Security | Environment templates avoid committed secrets. A Mapbox browser token is required. | Restrict the public Mapbox token by allowed origins/scopes and document production secret handling. **Documented in this redesign.** |

The verification install on 8 September 2026 reported **19 npm audit findings** (7 moderate, 12 high), and the production build warned about large chunks. Triage dependency upgrades and add route/vendor chunking before treating the frontend bundle as deployment-ready.

### rag-system

| Area | Finding | Recruiter-ready action |
|---|---|---|
| Positioning | The old README was a long build diary; completed capabilities were buried under obsolete “Phase 1” instructions. | Replace it with a concise product README while preserving verified details. **Implemented in this redesign.** |
| Screenshot/demo | This is an API/CLI system, so a UI screenshot would be artificial. | Publish a sample evaluation report, architecture diagram, and optional terminal recording instead. Architecture is **implemented in this redesign**. |
| Architecture | Components were described across phase sections but not shown as one current system. | Add one end-to-end request/index/evaluation diagram. **Implemented in this redesign.** |
| Quick start | Docker guidance existed but was scattered. | Provide one container-first path and one native development path. **Implemented in this redesign.** |
| API docs | Typed API and `/docs` exist. | Put authenticated query and health examples near the top. **Implemented in this redesign.** |
| Evaluation/results | A 50-case golden dataset, Ragas gate, report generator, and Phase 2 retrieval result exist. | Surface only measured results and explain that live faithfulness scoring requires a provider key. **Implemented in this redesign.** |
| Testing | Broad unit/contract coverage and two CI workflows exist. | Add a test-count badge only after CI is public and consistently green; avoid hard-coding a count. |
| Deployment | Hardened Compose runtime and a multi-architecture publish workflow exist. | Verify the first GHCR publication and add an actual package link before presenting the image as available. |
| Security | Authentication, exact-source authorization, per-user limits, log allowlisting, non-root read-only containers, scanning, and provenance are strong. | Add key rotation guidance and a distributed rate limiter before multi-replica deployment. **Current limitations are documented in this redesign.** |

## Manual GitHub actions

1. Pin the three flagship repositories in the recommended order.
2. Set profile name to **Rahul Vignesh**, bio to **AI Engineer building agentic, retrieval, and applied ML systems**, location to **Sydney, Australia**, and website to `https://rahulvignesh.com`.
3. Add repository descriptions and topics for all three flagship projects; their public API metadata is currently blank.
4. Confirm the education status. The current website and résumé say “student / transfer candidate,” while the brief says “recent graduate.” Update all three surfaces together once confirmed.
5. Archive or privatize early C repositories only after checking external dependencies.
6. Add a verified JobAgent screenshot/dry-run demo, a hosted EnergyAI walkthrough, and a published RAG evaluation report.
7. Verify the RAG container workflow publishes successfully, then link the GHCR package from the repository About panel.
8. Add a professional contact email to the GitHub profile if public email exposure is intended; the README already uses the existing public résumé/profile email.
9. Triage the JobAgent and EnergyAI npm audit findings and large-bundle warnings recorded above.
