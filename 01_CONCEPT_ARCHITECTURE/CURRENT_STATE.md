# Current State — The Living Constitution

> If someone joined the project today, what do we currently believe?

**Last updated:** 2026-06-11

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

## Layer Separation (FL_010)

The framework operates at four distinct layers:

| Layer | Question |
|-------|----------|
| Theory | Why does behavior happen? |
| Topography Engineering | What environmental properties create gradients? |
| Architecture | How should reasoning be structured for retrieval? |
| Implementation | What do we build? |

## What Has NOT Been Decided

- Whether Decision Space and Capability are primitives, derived, or collapsible
- Whether Phase 4.3 (Model Update Lifecycle/Governance) is needed or is implementation-layer work
- Phase 4 validation: Do reasoning architecture objects trace to theory?
- Phase 4 validation: Do discovery questions trace to dimensions?

## Active Fault Lines

- FL_007: Interface Layer (under continued pressure)
- FL_009: Optimizer Architecture (resolved to Goal/Policy/Interpretation — monitoring)
- FL_010: Layer Separation (soft boundary between Theory and Engineering)

---

*This file is regenerated with every significant architecture update. It is not a history — it is a snapshot.*
