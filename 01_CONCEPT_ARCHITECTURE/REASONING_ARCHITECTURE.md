# Reasoning Architecture — Phase 4.3 Complete

**Status:** Foundational — minimum viable reasoning architecture validated
**Date:** 2026-06-12

---

## Central Thesis

> The unit of organizational reasoning is not the document. It is the optimizer state transition.

Documents remain important — they are source artifacts. But documents preserve what was written, observed, proposed, or recorded. Reasoning objects preserve what was believed, why, what was being optimized, what constraints existed, what evidence was trusted, what uncertainty remained, why action was sufficient, what outcome contradicted expectation, what model changed, and when that update should apply again.

**Document retrieval** helps an optimizer access artifacts.
**Reasoning architecture** helps an optimizer reconstruct state transitions.

---

## Correct Relationship: Documents and Reasoning Objects

```
Documents = evidence, premises, references, context (source artifacts)
Reasoning Objects = structured state transitions built from those documents
```

| Source Artifact | Becomes Part Of |
|----------------|----------------|
| Campaign brief | Premise Stack |
| ICP | Premise Stack |
| Dashboard | Information Surface Context |
| Postmortem | Learning Event |
| Customer emails | Evidence references in Investigation Trace |
| Model Update Object | Reusable reasoning artifact derived from above |

Documents support reasoning. They do not, by themselves, preserve reasoning.

---

## Minimum Viable Reasoning Architecture — Six Objects

### 1. Optimizer State

**Captures:** Active Goal, Relevant Policy, Current Interpretation.

**Purpose:** Preserve what the optimizer was trying to do, under what constraints, and how it understood the situation.

### 2. Premise Stack

**Captures:** Artifacts and assumptions that produced the expectation.

**Purpose:** Preserve why the optimizer believed the action or decision would work.

### 3. Decision State

**Captures:** Decision under consideration, available options, selected action, rejected actions, constraints, tradeoffs, Information Surface Context, Sufficiency Rationale.

**Purpose:** Preserve what was chosen, from what options, under what constraints, and why the optimizer stopped investigating and acted.

### 4. Investigation Trace

**Captures:** Questions asked, evidence gathered, contradictions found, paths explored, paths abandoned, confidence changes.

**Purpose:** Preserve how uncertainty was reduced and prevent unsupported rationalization.

### 5. Learning Event

**Captures:** Expectation, Outcome, Prediction Error, Evidence-supported explanation.

**Purpose:** Preserve where reality contradicted the optimizer's model.

### 6. Model Update Object

**Captures:** Reusable bounded model transition — Premise Stack, Evidence, Update Target, Applicability Boundary, Confidence, Observability, Human-ready view.

**Purpose:** Preserve what future optimizers should change, when they should apply it, and how strongly they should rely on it.

---

## The Adaptive State-Transition Chain

```
Optimizer State
    ↓
Premise Stack
    ↓
Decision State
    ↓
Investigation Trace
    ↓
Learning Event
    ↓
Model Update Object
    ↓
Modified Optimizer State
```

---

## Supporting Concerns (Required But Not Standalone Objects)

| Concern | Contained Within |
|---------|-----------------|
| Information Surface Context | Decision State |
| Sufficiency Rationale | Decision State |
| Observability | Model Update Object |
| Human-Ready View | Model Update Object |
| Applicability Boundary | Model Update Object |
| Confidence | Multiple objects |

---

## Reduction History

Initial candidates (8):
- Optimizer State, Premise Stack, Information Surface Snapshot, Decision State, Investigation Trace, Sufficiency Rationale, Learning Event, Model Update Object

After reduction (6):
- Information Surface Snapshot → demoted to Information Surface Context (required concern inside Decision State)
- Sufficiency Rationale → demoted to required field inside Decision State

Each surviving object prevents a distinct failure:

| Object | Failure Prevented |
|--------|------------------|
| Optimizer State | Misreading the goal or policy |
| Premise Stack | Learning the wrong lesson from failed assumptions |
| Decision State | Forgetting alternatives, constraints, and sufficiency rationale |
| Investigation Trace | Rationalization and shallow explanation |
| Learning Event | Losing the prediction error |
| Model Update Object | Failing to preserve reusable learning |

---

## Validation Scenario: AI Agent Customer Communication

**Scenario:** AI agent authorized to auto-send follow-up emails after support tickets marked resolved. Expected: reduce workload, preserve experience. Observed: workload decreased, CSAT declined.

The architecture successfully reconstructed the full state transition:
- **Goal:** Reduce workload while preserving customer experience
- **Premise:** Resolved tickets are safe for auto-follow-up
- **Decision:** Allow auto-send based on resolved status
- **Sufficiency:** Ticket status + resolution notes + tone prompt judged enough
- **Outcome:** Workload improved, CSAT worsened
- **Prediction Error:** Efficiency improved but experience degraded
- **Investigation:** Missing emotional and relationship context, not factual correctness
- **Learning:** Resolved status ≠ communication readiness
- **Model Update:** Auto-send requires sentiment and relationship-risk checks

A document repository could store the policy, prompt, ticket data, postmortem, and CSAT report — but would not automatically preserve why the decision was considered sufficient, what assumptions produced the expectation, what prediction error occurred, or when the new learning applies.

---

## Key Architectural Claim

> Most knowledge systems preserve artifacts. Reasoning systems must preserve optimizer state transitions.

---

## Cross-References
- `OPTIMIZER_THEORY.md` (the primitives captured in Optimizer State)
- `OPTIMIZER_MOTION.md` (the motion model the architecture tracks)
- `LEARNING.md` (the learning process captured in Learning Event)
- `MODEL_UPDATE_OBJECTS.md` (the reusable artifact specification)
- FL_010 (Layer Separation — this is Architecture layer, not Theory layer)
- CA_006 (Architecture vs Theory Conflation — these are architectural objects, not theoretical primitives)
