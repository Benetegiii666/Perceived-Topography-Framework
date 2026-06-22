# Product Delivery Form Factor v0.1

**Date:** 2026-06-22
**Status:** v0.1 Initial delivery assumption. Requires review before stack selection.

---

## 1. Purpose

This artifact addresses a gap not covered by the HLD or implementation slice planning:

- **HLD v1.0** defines conceptual/reference architecture (what components exist and how they relate).
- **Slice Plan v0.2** defines first implementation scope (what to build first and what to exclude).
- **Discovery Worksheet** defines stakeholder input (what the campaign brief workflow looks like).
- **This artifact** defines delivery form: what the thing is, how users interact with it, where it might live, and what product shape it may take.

Without this artifact, the team has architecture and scope but no product direction.

---

## 2. Current Delivery Assumption

**Initial assumption:** The first deliverable should be a lightweight web application prototype.

Not:

- a paper (the paper already exists)
- a static document (does not prove the interaction loop)
- a Claude-only workflow (does not preserve reasoning state across sessions)
- a pure backend service (requires a user interface for RIPC confirmation)
- a full enterprise platform (too heavy for first cycle)

The web app should demonstrate the first campaign brief reasoning loop — from information surface selection through RIPC Discovery, governance check, brief generation, sufficiency capture, and outcome recording.

---

## 3. Primary User Experience

The first prototype presents one orchestrated flow with visible stages:

```text
1.  Select or register information surfaces
2.  Start campaign brief request
3.  Retrieve relevant surfaces and prior reasoning
4.  Infer draft goal and premises
5.  Propose reasoning state to human
6.  Human confirms / corrects / rejects / qualifies / bounds
7.  Governance / sufficiency check flags issues
8.  Generate campaign brief
9.  Capture sufficiency rationale
10. [Campaign executes — outside prototype scope]
11. Capture outcome
12. Optionally prompt learning review
```

The human is in the loop at stages 1, 6, 7, 8, 9, 11, and 12. The system does the reasoning work at stages 3, 4, 5, and 7. Each stage is visible — the user sees what the system retrieved, inferred, proposed, and flagged.

---

## 4. Candidate Application Structure

| Section | Purpose | Primary User | MVP / Future | PTF Concept | Source Artifact |
|---|---|---|---|---|---|
| **Home / Project Orientation** | Landing page explaining the prototype, the reasoning-state approach, and how to get started | All users | MVP | — | Executive Brief v1.0 |
| **Campaign Brief Workspace** | The primary work area. Orchestrates the RIPC flow: retrieve, infer, propose, confirm, generate. | Requester (campaign owner) | MVP | RIPC / Discovery, Optimizer State, Premise Stack | HLD Ch 5, Slice Plan Sec 6 |
| **Information Surface Registry** | Register, browse, and manage information surfaces. Shows authority level, owner, recency. | Governance Owner, Requester | MVP | Information surfaces, perceived topography | HLD Ch 4, Slice Plan Sec 4 |
| **Reasoning State Review** | Browse prior reasoning objects: Optimizer States, Premise Stacks, Decision States, MUOs. Filter by workflow, status, goal. | Domain Expert, Governance Owner | MVP | Reasoning state, retrieval relevance | HLD Ch 3, Ch 6 |
| **Governance / Sufficiency Review** | View governance flags, policy issues, sufficiency check results. Advisory mode. | Domain Expert, Governance Owner | MVP | Governance, sufficiency, premature sufficiency | HLD Ch 8, Ch 10 |
| **Campaign Brief Output** | View the generated brief with source citations, confidence markers, and governance flags. | Requester, Domain Expert | MVP | Decision artifact | HLD Ch 3 (Decision State) |
| **Outcome Capture** | Record campaign outcomes. Display predictions for comparison. Prompt for prediction-error assessment. | Requester | MVP | Learning loop, outcome record | HLD Ch 7, Slice Plan Sec 9 |
| **Learning Review** | Review Learning Events and draft MUOs. Human-authored, system-structured. | Domain Expert, Governance Owner | MVP-adjacent | Learning, MUO | HLD Ch 7, Capability Map |
| **Admin / Settings** | Configure roles, review periods, staleness thresholds, static Discovery Patterns. | Governance Owner | Future | Governance, lifecycle | HLD Ch 9, Ch 10 |
| **Visual Architecture / Roadmap** | Read-only view of the PTF architecture, artifact stack, and implementation roadmap. | All users | Future | — | HLD, Executive Brief |

---

## 5. Candidate Technical Delivery Options

### Option A — Static / Markdown-First Prototype

**Pros:**

- Fastest to create
- Simple to maintain
- Good for conceptual validation and internal review
- Works with existing repo structure

**Cons:**

- Does not prove the RIPC interaction loop
- No dynamic state management (reasoning objects, lifecycle transitions)
- Poor fit for human confirmation (confirm/correct/reject/qualify/bound)
- Weak as a demo — reads like documentation, not a product

**Best for:** Internal conceptual review only. Not suitable as the first prototype delivery.

### Option B — React / Vite Front End + Lightweight API

**Pros:**

- Fast UI prototyping with modern tooling
- Clean separation of front end and service layer
- Deployable as a simple static + API app
- Flexible — can swap API backend without touching UI
- Familiar pattern from Rapid Marketing Context Layer (single-file React-like frontend + FastAPI backend)

**Cons:**

- Must decide backend framework separately (FastAPI, Express, etc.)
- More wiring than a full-stack framework
- State management (reasoning objects, lifecycle) must be explicitly designed

**Best for:** Teams that want front-end flexibility and already have API preferences.

### Option C — Next.js Full-Stack App

**Pros:**

- Front end and API routes in one repo
- Server-side rendering available if needed
- Can deploy with Postgres (Vercel, Railway, or self-hosted)
- Good for end-to-end prototype demo
- Strong ecosystem for auth, data fetching, and deployment

**Cons:**

- Framework decisions come earlier (routing conventions, server/client boundary)
- Opinionated structure may constrain experimentation
- Heavier than a pure Vite setup for early iteration

**Best for:** Teams that want a single-repo full-stack prototype with deployment simplicity.

### Option D — Angular Enterprise-Style App

**Pros:**

- Structured framework with strong routing, forms, and dependency injection conventions
- Enterprise-friendly — aligns with organizations that use Angular
- Good for complex form-based workflows (governance review, confirmation flows)

**Cons:**

- Heavier for a first prototype
- May slow early iteration unless the team already prefers Angular
- Smaller ecosystem for rapid prototyping compared to React/Next

**Best for:** Teams with existing Angular expertise or enterprise deployment requirements.

### Initial Recommendation

Use a web-app direction. Prefer React/Next.js or React/Vite unless a team constraint points to Angular. The Rapid Marketing Context Layer used a single-file HTML/CSS/JS frontend with FastAPI — a React-based approach is a natural evolution.

**This is not final.** Mark as an initial delivery assumption requiring review.

---

## 6. Candidate Hosting / Runtime Direction

| Concern | Initial Direction | Notes |
|---|---|---|
| **Deployment target** | Railway (likely prototype host) | Familiar from Rapid and capstone projects. Simple deployment. |
| **Structured state storage** | Postgres | Reasoning objects, lifecycle state, audit records. |
| **Vector retrieval** | Deferred or simple implementation | ChromaDB in-memory for prototype (as in Rapid). Postgres pgvector or Pinecone for production. |
| **External integrations** | Deferred | Beacon/MCP/co-worker/model router are future-phase. |
| **Authentication** | TBD | Internal prototype may not need auth. Stakeholder-facing prototype needs basic auth. |

**Hosting choice is not final.** The MVP should remain portable — no vendor lock-in at the hosting layer.

---

## 7. Data / Service Boundaries

| Service Area | Purpose | MVP / Future |
|---|---|---|
| **Information Surface Registry** | Register, store, and query information surface metadata. Serve surfaces to Retrieve step. | MVP |
| **Retrieval Service** | Semantic search + metadata filters over information surfaces and reasoning objects. Match rationale generation. | MVP |
| **RIPC Orchestrator** | Execute Retrieve → Infer → Propose → Confirm. Manage the multi-step interaction flow. | MVP |
| **Reasoning State Service** | Store, version, and query reasoning objects (Optimizer State, Premise Stack, Decision State, etc.). Enforce referential integrity. | MVP |
| **Governance / Sufficiency Service** | Advisory governance checks. Flag policy violations, unsupported claims, sufficiency concerns. Coaching posture. | MVP |
| **Campaign Brief Generation** | Produce the decision artifact from confirmed reasoning state. Source citations. | MVP |
| **Outcome Capture Service** | Record outcomes. Display predictions for comparison. | MVP |
| **Learning Review Service** | Structure Learning Events and draft MUOs. Human-authored, system-structured. | MVP-adjacent |
| **Audit / Lifecycle Service** | Log state transitions. Manage lifecycle states. Staleness detection. | MVP (basic), Future (full) |
| **Admin / Configuration Service** | Roles, review periods, Discovery Patterns, retention settings. | Future |

---

## 8. Visual Design Views Needed

These visual assets should be created during delivery architecture design. They may be produced as Mermaid diagrams with SVG/PNG exports.

| Visual | Purpose | When Needed |
|---|---|---|
| Product site map | Shows app sections and navigation structure | Before screen design |
| User journey map | Shows the campaign owner's path through the RIPC flow | Before screen design |
| First slice system flow | Shows data flow from request through RIPC to brief output | Before implementation |
| RIPC loop diagram | Shows Retrieve → Infer → Propose → Confirm with re-entry | Before implementation |
| Reasoning object lifecycle diagram | Shows Draft → Provisional → Validated with transition rules | Before implementation |
| Information surface registry model | Shows surface records, authority levels, relationships | Before data model sketch |
| MVP / future capability map | Shows what is MVP vs. what is deferred | For stakeholder communication |
| Roadmap diagram | Shows proposed work sequence (discovery → design → build) | For stakeholder communication |
| Screen wireframes | Low-fidelity wireframes for each app section | Before front-end build |
| Deployment architecture diagram | Shows runtime components, hosting, data flow | Before deployment |

---

## 9. Open Delivery Decisions

| # | Decision | Options | Notes |
|---|---|---|---|
| 1 | Front-end framework | React/Next.js, React/Vite, Angular | Initial lean: React/Next.js or React/Vite. Not final. |
| 2 | Deployment target | Railway, Vercel, self-hosted | Initial lean: Railway. Not final. |
| 3 | Repo structure | Monorepo (front end + API), split repos | Monorepo simpler for prototype. |
| 4 | Storage | Postgres only, Postgres + vector store | Postgres for reasoning objects. Vector store deferred or simple (ChromaDB in-memory). |
| 5 | Brief output format | Markdown, structured JSON object, hybrid | Markdown is simplest. Structured enables governance checks. |
| 6 | Authentication | None (internal), basic auth, OAuth | Depends on whether prototype is internal-only or stakeholder-facing. |
| 7 | Visual asset location | In-app (rendered), docs-only (static), both | In-app for product; docs-only for architecture review. |
| 8 | Prototype audience | Internal-only, stakeholder-facing, both | Affects auth, polish level, and content sensitivity. |
| 9 | Field kit → product | Field kit remains separate, field kit becomes a product page, hybrid | Field kit is currently a repo artifact. It could become a product feature later. |

---

## 10. Recommended Next Action

1. **Finish Rapid stakeholder field kit** — done (committed and pushed).
2. **Run campaign workflow discovery** — use field kit with Rapid marketing stakeholders.
3. **Create delivery architecture backlog** — done (this folder).
4. **Create low-fidelity site map and first screen flow** — next visual design task.
5. **Create data model sketch** — translate HLD Ch 3 MVP fields + discovery outputs into concrete schema.
6. **Create build backlog** — sequence implementation tasks with dependencies and acceptance criteria.

---

## No-Edit Confirmation

- Frozen paper edited: **No**
- Figure 8 modified: **No**
- Figures modified: **No**
- References modified: **No**
- Executive Brief v1.0 edited: **No**
- Build Discovery Guide v1.0 edited: **No**
- HLD v1.0 content edited: **No**
- Slice Plan v0.2 edited: **No**
- Implementation code created: **No**
- Schemas created: **No**
- Stack selected as final: **No** (initial assumptions only)
