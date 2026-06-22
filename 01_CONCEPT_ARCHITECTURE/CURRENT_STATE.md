# Current State — The Living Constitution

> If someone joined the project today, what do we currently believe?

**Last updated:** 2026-06-14

---

## Core Claim

Agents are optimizers. Behavior emerges from the interaction between optimizer primitives and perceived information topography — not from intelligence, intent, or instruction alone.

## Optimizer Architecture (Phase 1 — Complete)

```
Optimizer
    ├── Goal           — What am I trying to achieve?
    ├── Policy         — What constraints govern behavior?
    └── Interpretation — What does this information mean?
          ├── Signal Meaning
          ├── Causal Explanation
          └── Action Model
```

Collapsed candidates: Evaluation (→ Policy + Interpretation), Navigation (→ Goal + Policy + Interpretation), Sufficiency (→ judgment/gate). Action Model classified as Interpretation subtype (not a fourth primitive).

## Information Topography (Phase 2 — Complete)

Five primary dimensions describing how information environments create gradients:

```
Visibility     — Can this be perceived?
Accessibility  — Can this be reached?
Representation — How is this expressed?
Confidence     — How trustworthy is this?
Connectivity   — What is this connected to?
```

**Goal Relevance** is derived (relational), not a dimension. It emerges from Signal relative to Goal.

**Information Surfaces** are the structures through which optimizers encounter topography — containing all five dimensions.

## The Full Equation

```
Optimizer (Goal, Policy, Interpretation)
    +
Information Topography (Visibility, Accessibility, Representation, Confidence, Connectivity)
    =
Behavior (Attention, Exploration, Investigation, Action)
```

## Optimizer Motion (Phase 3 — Complete)

```
Attraction → Investigation → Sufficiency → Action
```

**Attraction** (FL_013 — Resolved):
- Action Attraction = Goal Relevance + Confidence
- Exploration Attraction = Goal Relevance + Confidence Gap + Connectivity

**Investigation** (FL_014 — Resolved):
- Trigger = Goal-Relevant Observation + Confidence Gap
- Connectivity guides explanatory search
- Three termination conditions

**Sufficiency** (FL_015 — Resolved):
- Action Stability — independent of Confidence
- Act when additional information is unlikely to change the selected action

## Learning (Phase 4.1 — Complete)

**Definition:** Learning is an evidence-supported optimizer modification triggered by prediction error.

```
Expectation → Action → Outcome → Prediction Error → Investigation → Evidence-Supported Explanation → Model Update
```

**Four update targets:** Interpretation, Policy, Goal, Action Model.

**Reusable unit:** Model Update Object (Phase 4.2 — Complete):
- Core Learning Payload (11 required fields including Premise Stack)
- Observability Envelope (trust, audit, lifecycle)
- Human-Ready View (usability, not authoritative)

**Premise Stack:** Artifact-backed basis for prior expectations. Topography-shaping artifacts, not topography dimensions.

**8 retrieval/use rules.** 10 identified bad-update failure modes.

**Adaptive loop closure:** Optimizer → Motion → Outcome → Prediction Error → Learning → Model Update Object → Modified Optimizer.

## Reasoning Architecture (Phase 4.3 — Complete)

**Central thesis:** The unit of organizational reasoning is not the document — it is the optimizer state transition.

Six minimum viable objects:

```
Optimizer State → Premise Stack → Decision State → Investigation Trace → Learning Event → Model Update Object → Modified Optimizer State
```

Documents are source artifacts (evidence, premises, references). Reasoning objects preserve state transitions built from those documents. Each object prevents a distinct failure mode.

Supporting concerns (required but not standalone): Information Surface Context, Sufficiency Rationale, Observability, Human-Ready View, Applicability Boundary, Confidence.

## Discovery Framework (Phase 4.4 — Complete)

> Discovery converts human intent into reasoning state.

**Two modes:**
- **Initial Discovery** — maps an existing reasoning environment (interviews, workshops, artifact review)
- **Runtime Discovery** — converts new work into reasoning objects with minimal human burden

**Runtime Discovery Loop:** Retrieve → Infer → Propose → Confirm → Generate → Preserve → Learn

**Key principles:**
- Strawman-first: propose direction from existing artifacts before asking questions
- Low-friction: do the reasoning work before asking the user to do it
- Ask only where uncertainty materially affects the result

**Discovery Pattern Learning:** The system learns which interaction patterns produce lower friction, better reasoning objects, better artifacts, and better outcomes. Captured as specialized Model Update Objects (Discovery Pattern Updates).

## Layer Separation (FL_010)

The framework operates at four distinct layers:

| Layer | Question |
|-------|----------|
| Theory | Why does behavior happen? |
| Topography Engineering | What environmental properties create gradients? |
| Architecture | How should reasoning be structured for retrieval? |
| Implementation | What do we build? |

## Paper v0.1 — Release Checkpoint (2026-06-12)

**PAPER_v0.1.md** — frozen v0.1 snapshot. 17 sections + References. ~33,677 words.

## Paper v0.2 — Release Checkpoint (2026-06-14)

**PAPER_v0.2.md** — frozen v0.2 snapshot. ACCEPTED.

- 17 sections + Appendix A + References
- ~36,861 words
- Full title architecture pass (199 headings rewritten)
- Appendix A: The Decision Topography Interview (23 items, 4 phases)
- 7 SVG figures with resolved paths
- 33 body-prose citation keys, all resolved
- D011 (Differential Intervention Principle) integrated as one sentence in S14.12
- Zero Citation Debt, Draft Notes, placeholders, or process contamination

**Current phase:** Phase 7 — Artifact Finalization and External Review

## What Has NOT Been Decided

- PDF/docx export format for v0.2
- Peer review / external reader review plan
- Abstract
- Executive-summary / adoption-roadmap companion
- Final SVG optional polish (5 deferred cosmetic items)
- Whether Decision Space and Capability are primitives, derived, or collapsible

## Active Fault Lines

- FL_007: Interface Layer (under continued pressure)
- FL_009: Optimizer Architecture (resolved to Goal/Policy/Interpretation — monitoring)
- FL_010: Layer Separation (soft boundary between Theory and Engineering)

---

*This file is regenerated with every significant architecture update. It is not a history — it is a snapshot.*
