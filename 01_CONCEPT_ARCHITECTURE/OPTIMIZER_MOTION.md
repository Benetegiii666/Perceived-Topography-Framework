# Optimizer Motion — Phase 3 Complete

**Status:** Foundational — all three stages resolved
**Date:** 2026-06-11

---

## The Motion Model

```
Attraction → Investigation → Sufficiency → Action
```

### Stage 1: Attraction (FL_013 — Resolved)

**Question:** What receives attention?

Two modes:

**Action Attraction:**
```
Goal Relevance + Confidence = Action Attraction
```
Drives direct action when information is both goal-relevant and trusted.

**Exploration Attraction:**
```
Goal Relevance + Confidence Gap + Connectivity = Exploration Attraction
```
Drives investigation when goal-relevant information is uncertain and connected to explanatory pathways.

### Stage 2: Investigation (FL_014 — Resolved)

**Question:** What receives explanatory effort?

**Trigger:**
```
Goal-Relevant Observation + Confidence Gap = Investigation Trigger
```

**Navigation:** Connectivity guides explanatory search.

**Termination:** Investigation stops when:
1. Confidence becomes sufficient
2. No viable explanatory paths remain
3. The investigation is no longer goal-relevant

### Stage 3: Sufficiency (FL_015 — Resolved)

**Question:** When does investigation stop and action begin?

**Definition:** Sufficiency is **Action Stability** — the optimizer acts when additional information is unlikely to materially change the selected action.

**Independence:** Confidence ≠ Sufficiency. They vary independently:
- Low Confidence + High Sufficiency: multiple explanations, same action recommendation
- High Confidence + Low Sufficiency: one remaining fact could flip the decision

---

## Complete Motion Summary

```
Attraction:
  Goal Relevance + Confidence → Action Attraction
  Goal Relevance + Confidence Gap + Connectivity → Exploration Attraction

Investigation:
  Goal-Relevant Observation + Confidence Gap → Investigation
  Connectivity guides explanatory search
  Three termination conditions

Sufficiency:
  Additional information unlikely to change action → Act
```

Together these explain optimizer motion from initial attention allocation through investigation and ultimately action.

## Cross-References
- FL_013 (Attraction Model)
- FL_014 (Investigation Dynamics)
- FL_015 (Sufficiency)
- `OPTIMIZER_THEORY.md` (the primitives that drive motion)
- `INFORMATION_TOPOGRAPHY.md` (the dimensions motion responds to)
