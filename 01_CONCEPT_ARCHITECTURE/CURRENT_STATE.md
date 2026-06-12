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
```

Collapsed candidates: Evaluation (→ Policy + Interpretation), Navigation (→ Goal + Policy + Interpretation), Sufficiency (→ judgment/gate).

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

## Learning (Emerging)

```
Expectation → Action → Outcome → Prediction Error → Investigation → Evidence-Supported Explanation → Model Update
```

Learning is evidence-supported model update, not outcome or postmortem (D016).

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
- Whether Learning vs Reaction is a clean distinction
- Structure of reusable model updates for organizational/agent memory
- Phase 4 validation: Do reasoning architecture objects trace to theory?
- Phase 4 validation: Do discovery questions trace to dimensions?
- Cross-layer leaks: How Goal and Policy relate across Theory/Engineering/Architecture layers

## Active Fault Lines

- FL_007: Interface Layer (under continued pressure)
- FL_009: Optimizer Architecture (resolved to Goal/Policy/Interpretation — monitoring)
- FL_010: Layer Separation (soft boundary between Theory and Engineering)

---

*This file is regenerated with every significant architecture update. It is not a history — it is a snapshot.*
