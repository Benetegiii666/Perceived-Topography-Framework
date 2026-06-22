# Delivery Architecture Backlog v0.1

**Date:** 2026-06-22
**Status:** v0.1 Decision and design backlog. Not an implementation backlog.

---

## 1. Purpose

This backlog captures delivery-form decisions and design tasks that must be resolved before the implementation build backlog can be created. It does not contain implementation tickets, code tasks, or sprint items.

**This is not the implementation build backlog.** Do not create implementation tickets yet. This backlog exists to clarify product delivery before code.

---

## 2. Decision Backlog

| # | Decision | Why It Matters | Decision Owner | Dependency | Urgency | Recommended Next Step |
|---|---|---|---|---|---|---|
| 1 | **Decide product form factor** | Determines everything downstream: stack, hosting, UI, interaction model. | Benet | None — first decision. | High | Review `PRODUCT_DELIVERY_FORM_FACTOR_v0.1.md`. Confirm web app direction. |
| 2 | **Choose initial front-end stack** | React/Next.js, React/Vite, or Angular affects component structure, routing, and deployment. | Benet | Decision 1 (web app confirmed). | High | Evaluate team familiarity, prototype speed, deployment simplicity. |
| 3 | **Choose deployment target** | Railway, Vercel, or self-hosted affects CI/CD, database access, and cost. | Benet | Decision 2 (stack chosen). | Medium | Railway is the initial lean. Confirm or change. |
| 4 | **Define app sections / site map** | Determines navigation structure and what the user sees first. | Benet | Decision 1 (form factor confirmed). | High | Create low-fidelity site map from `PRODUCT_DELIVERY_FORM_FACTOR_v0.1.md` Section 4. |
| 5 | **Define first user journey** | Maps the campaign owner's path through the prototype from start to finish. | Benet | Decision 4 (site map). | High | Create user journey diagram showing RIPC stages, confirmation points, and outputs. |
| 6 | **Define prototype demo flow** | Determines what the first demo shows and in what order. | Benet | Decision 5 (user journey). | Medium | Use Slice Plan v0.2 Section 15 (Demo Shape) as the starting point. |
| 7 | **Define storage/runtime assumptions** | Postgres, vector store, in-memory — affects data model design. | Benet | Decision 2 (stack chosen). | Medium | Postgres for reasoning objects. ChromaDB in-memory or pgvector for retrieval. |
| 8 | **Define visual architecture set** | Which diagrams are needed for the product and documentation. | Benet | None. | Low | Review `PRODUCT_DELIVERY_FORM_FACTOR_v0.1.md` Section 8. Prioritize site map and RIPC loop first. |
| 9 | **Define screen wireframes** | Low-fidelity wireframes for each app section before front-end build. | Benet | Decision 4 (site map), Decision 5 (user journey). | Medium | Create wireframes for Campaign Brief Workspace, Information Surface Registry, and Governance Review. |
| 10 | **Define field kit vs product UI boundary** | What belongs in the field kit (stakeholder documents) vs. the product UI (interactive features)? | Benet | Decision 1 (form factor). | Low | Initially separate. Field kit may become a product feature later. |
| 11 | **Define prototype audience** | Internal-only or stakeholder-facing? Affects auth, polish, content sensitivity. | Benet | Decision 1 (form factor). | Medium | Start internal-only. Move to stakeholder-facing after first cycle. |

---

## 3. Visual Backlog

| # | Visual Asset | Purpose | Priority | Dependency | Format |
|---|---|---|---|---|---|
| 1 | **Artifact Stack / Where We Are** | Show the relationship between paper, Executive Brief, Build Discovery Guide, HLD, Slice Plan, Delivery Architecture. | High | None. | Mermaid → SVG |
| 2 | **First Slice System Flow** | Show data flow from campaign request through RIPC to brief output to outcome capture. | High | Decision 5 (user journey). | Mermaid → SVG |
| 3 | **RIPC Loop** | Show Retrieve → Infer → Propose → Confirm with re-entry logic and human confirmation points. | High | None. | Mermaid → SVG |
| 4 | **Reasoning-State Lifecycle** | Show Draft → Provisional → Validated with transition rules, roles, and evidence requirements. | Medium | None. | Mermaid → SVG |
| 5 | **Capability Phase Map** | Show MVP core, MVP-adjacent, and future components from the Rapid Component Capability Map. | Medium | None. | Mermaid → SVG |
| 6 | **Roadmap / Proposed Work Sequence** | Show the sequence: discovery → delivery design → data model → build → demo → iterate. | Medium | None. | Mermaid → SVG |
| 7 | **Product Site Map** | Show app sections and navigation hierarchy. | High | Decision 4 (site map). | Mermaid → SVG |
| 8 | **Prototype Screen Flow** | Show the user's click path through the Campaign Brief Workspace. | Medium | Decision 5 (user journey), Visual 7 (site map). | Wireframe tool or Mermaid |
| 9 | **Deployment Architecture Draft** | Show runtime components, hosting, data stores, and service boundaries. | Low | Decision 3 (deployment target), Decision 7 (storage). | Mermaid → SVG |

---

## 4. Build Backlog Boundary

**This is not the implementation build backlog.**

The implementation build backlog should be created only after:

1. Delivery form factor is confirmed (Decision 1).
2. Stack is chosen (Decision 2).
3. Campaign workflow discovery is completed (Categories 1-3 filled).
4. Data model sketch is created from discovery outputs.
5. Site map and first screen flow are defined.

Creating implementation tickets before these steps risks building the wrong thing or building it in the wrong shape.

The sequence:

```text
Discovery → Delivery Design → Data Model → Build Backlog → Implementation
```

---

## No-Edit Confirmation

- Frozen paper edited: **No**
- Figure 8 modified: **No**
- Figures modified: **No**
- References modified: **No**
- Executive Brief v1.0 edited: **No**
- Build Discovery Guide v1.0 edited: **No**
- HLD v1.0 content edited: **No**
- Implementation backlog created: **No**
- Implementation code created: **No**
- Schemas created: **No**
