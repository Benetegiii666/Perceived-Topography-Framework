# Research Roadmap

> Define scope. Define done. Kill rabbit holes.

**Date:** 2026-06-11
**Status:** Active

---

## PHASE 1 — Stabilize The Theory — **COMPLETE**

**Goal:** Determine whether the optimizer/topography theory is coherent enough to serve as a foundation.

**Result:** Optimizer converged on Goal + Policy + Interpretation. Layer separation holds. Filed in `01_CONCEPT_ARCHITECTURE/OPTIMIZER_THEORY.md`.

### Task 1.1 — Lock Layer Separation

- [x] Each layer answers a distinct question ✓
- [x] D011-style independence survives ✓
- [x] No new layers added without surviving pressure testing ✓

### Task 1.2 — Resolve Cross-Layer Leaks

- [x] Goal: Theory = optimizer primitive; Engineering = dimension anchor; Architecture = reasoning object ✓
- [x] Policy: Theory = optimizer primitive; Engineering = constraint dimension; Architecture = governance object ✓
- [x] Same concept at different abstraction levels — not naming collisions ✓

---

## PHASE 2 — Find The Topography Dimensions — **COMPLETE**

**Result:** Five primary dimensions converged: Visibility, Accessibility, Representation, Confidence, Connectivity. Goal Relevance confirmed as derived (relational). Filed in `01_CONCEPT_ARCHITECTURE/INFORMATION_TOPOGRAPHY.md`.

### Task 2.1 — Candidate Dimension Review

- [x] Candidate list agreed: Visibility, Accessibility, Representation, Confidence, Connectivity ✓
- [x] Goal Relevance reclassified as derived/relational ✓
- [x] No new dimensions introduced without strong justification ✓

### Task 2.2 — D011 Reduction

- [x] Visibility/Accessibility separation tested — independent ✓
- [x] Confidence/Representation separation tested — independent ✓
- [x] Connectivity independence tested ✓
- [x] Goal Relevance collapsed to derived ✓

### Task 2.3 — Optimizer Failure Mapping

- [x] Visibility Failure = Missed Opportunity ✓
- [x] Confidence Failure = Bad Trust Decision ✓
- [x] Connectivity Failure = Failure to Connect Signals ✓
- [x] Accessibility Failure = Known but Unreachable ✓
- [x] Representation Failure = Misinterpretation from Poor Expression ✓

---

## PHASE 3 — Define Optimizer Motion — **COMPLETE**

**Result:** Motion model = Attraction → Investigation → Sufficiency → Action. Filed in `01_CONCEPT_ARCHITECTURE/OPTIMIZER_MOTION.md`.

### Task 3.1 — Define Attraction

- [x] Two attraction modes identified: Action Attraction and Exploration Attraction ✓
- [x] Action Attraction = Goal Relevance + Confidence ✓
- [x] Exploration Attraction = Goal Relevance + Confidence Gap + Connectivity ✓
- [x] Goal Relevance alone and Confidence alone both failed — combination required ✓

**Deliverable:** `FL_013_Optimizer_Attraction_Model.md` — **COMPLETE**

---

### Task 3.2 — Define Investigation

**Question:** What causes an optimizer to stop, look deeper, spawn a task, request more evidence?

**Done When:**
- [x] We can describe investigation triggers ✓ Goal-Relevant Observation + Confidence Gap = Trigger
- [x] Connectivity guides explanatory search ✓
- [x] Three termination conditions identified ✓

**Deliverable:** `FL_014_Optimizer_Investigation_Dynamics.md` — **COMPLETE**

---

### Task 3.3 — Define Sufficiency

**Question:** When does an optimizer stop searching?

**Done When:**
- [x] We can explain Continue Searching vs Act Now without introducing new primitives ✓
- [x] Sufficiency defined as Action Stability ✓
- [x] Confidence and Sufficiency shown to be independent (both directions tested) ✓

**Deliverable:** `FL_015_Sufficiency_as_Emergent_Behavior.md` — **COMPLETE**

---

## PHASE 4 — Validate Architecture — **ACTIVE**

**Only after theory is stable.** Theory is stable (Phases 1-3 complete).

### Task 4.1 — Learning Events — **COMPLETE**

- [x] Learning defined: evidence-supported optimizer modification triggered by prediction error ✓
- [x] Learning vs Reaction distinction established ✓
- [x] Four update targets identified: Interpretation, Policy, Goal, Action Model ✓
- [x] Capability and Decision Space tested — did not force new update targets ✓
- [x] Model Update Object proposed as reusable unit of learning ✓
- [x] Adaptive loop closed: Optimizer → Motion → Outcome → Error → Learning → Modified Optimizer ✓

**Deliverable:** `01_CONCEPT_ARCHITECTURE/LEARNING.md` — **COMPLETE**

---

### Task 4.2 — Model Update Objects — **COMPLETE**

- [x] Required fields defined (11 Core Learning Payload fields) ✓
- [x] Observability Envelope defined (trust, audit, lifecycle) ✓
- [x] Human-Ready View defined (usability, non-authoritative) ✓
- [x] Premise Stack defined as artifact-backed basis for prior expectations ✓
- [x] Applicability boundaries formalized (field + retrieval rules) ✓
- [x] Confidence handling specified (low/moderate/high force levels) ✓
- [x] 8 retrieval/use rules defined ✓
- [x] 10 failure modes identified ✓
- [x] Action Model classified as Interpretation subtype (not fourth primitive) ✓
- [x] Cross-domain validation: Marketing, Product, Operations, AI, Hiring ✓

**Deliverable:** `01_CONCEPT_ARCHITECTURE/MODEL_UPDATE_OBJECTS.md` — **COMPLETE**

---

### Task 4.3 — Reasoning Architecture Validation — **COMPLETE**

- [x] Central thesis: unit of reasoning is optimizer state transition, not document ✓
- [x] Six minimum viable objects defined (Optimizer State, Premise Stack, Decision State, Investigation Trace, Learning Event, Model Update Object) ✓
- [x] Two candidates demoted to supporting concerns (Information Surface Snapshot → context, Sufficiency Rationale → field) ✓
- [x] Each object prevents a distinct failure ✓
- [x] Document/reasoning-object relationship formalized (documents = source artifacts, reasoning objects = state transitions) ✓
- [x] Validated against AI agent customer communication scenario ✓

**Deliverable:** `01_CONCEPT_ARCHITECTURE/REASONING_ARCHITECTURE.md` — **COMPLETE**

---

### Task 4.4 — Validate Discovery Framework — **COMPLETE**

- [x] Discovery reframed: not a static questionnaire but adaptive conversion of intent to reasoning state ✓
- [x] Two modes: Initial Discovery (map existing reasoning) + Runtime Discovery (process new work) ✓
- [x] Runtime Discovery loop: Retrieve → Infer → Propose → Confirm → Generate → Preserve → Learn ✓
- [x] Strawman-first and low-friction principles established ✓
- [x] Discovery Pattern Learning identified as architecture-level concern ✓
- [x] Validated through healthcare campaign simulation (full cycle including post-campaign learning) ✓

**Deliverable:** `01_CONCEPT_ARCHITECTURE/DISCOVERY_FRAMEWORK.md` — **COMPLETE**

---

## PHASE 4 STATUS: **COMPLETE**

All subtasks resolved: 4.1 ✅ 4.2 ✅ 4.3 ✅ 4.4 ✅

---

## PHASE 5 — Stop

**Seriously. Stop.**

### Success Criteria

- [x] Stable Layer Separation ✓
- [x] Stable Topography Dimensions ✓
- [x] Stable Optimizer Motion Model ✓
- [x] Validated Architecture ✓
- [x] Validated Discovery Framework ✓

### Definition of Gold

Gold is **NOT:** Perfect Theory

Gold **IS:** We can explain optimizer behavior, describe the information dimensions that shape it, explain how movement occurs through that landscape, and derive practical architecture and discovery methods from the theory.

If we achieve that, this phase is complete and worthy of filing as a major milestone. The next phase is implementation and experimentation, not more foundational digging.

---

### Anti-Drift Rules

1. No new dimensions without strong justification
2. No new primitives without D011 survival
3. No new layers without pressure testing
4. No new entities without tracing back to theory
5. If a rabbit hole opens, file it and move on — don't chase it

---

## PHASE 6 — Narrative Paper v1 — **ACTIVE**

**Concept Architecture v0.1 frozen.** No new theory expansion unless contradiction emerges during drafting.

**Working title:** The Perceived Topography Framework: A Reasoning-State Architecture for Human-Agent Systems

### Deliverables

- [x] PAPER_ARCHITECTURE.md — 17-section argument arc ✓
- [ ] PAPER_DRAFT.md — Section-by-section narrative
- [ ] SVG_SPECIFICATIONS.md — Four diagram specifications
- [ ] RELATED_WORK.md — Literature and citations
- [ ] Final paper assembly

### Guardrails

**Allowed:** Clarify language, compress concepts, define terms, choose examples, add citations, design diagrams, write narrative sections, identify validation methods.

**NOT allowed without explicit approval:** New primitives, new topography dimensions, new optimizer phases, new foundational architecture documents, major theory expansion.
