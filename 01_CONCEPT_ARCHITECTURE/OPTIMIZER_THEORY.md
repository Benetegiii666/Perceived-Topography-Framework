# Optimizer Theory — Phase 1 Complete

**Status:** Foundational — survived repeated pressure testing
**Date:** 2026-06-11

---

## Origin Question

The original question was: *Are agents evil?*

This evolved into: **What are agents?**

## Core Finding

Agents are not inherently good or evil. Agents are **optimizers**.

An optimizer is a system that attempts to move reality toward preferred states according to some internal model.

This definition applies to:
- Humans
- Organizations
- Software Agents
- AI Systems
- Biological Systems

The framework is intentionally optimizer-centric rather than AI-centric.

---

## Optimizer Decomposition

After multiple pressure tests (D011), the optimizer model converged on three primitives:

```
Optimizer
    ├── Goal
    ├── Policy
    └── Interpretation
```

### Goal

**Answers:** What am I trying to achieve?

**Examples:** Increase revenue, reduce risk, improve customer satisfaction, reach destination.

**Without a goal:** No preference exists. No optimization occurs.

Goal survived repeated attempts to remove it.

### Policy

**Answers:** What constraints govern behavior?

**Examples:** Budget limits, safety rules, legal restrictions, ethical constraints, operating procedures.

**Determines:** What may be done.

Policy is distinct from goals. Two optimizers may share the same goal while operating under different policies.

### Interpretation

**Answers:** What does this information mean?

**Examples:** Customer complaint, market signal, revenue decline, competitor action.

**Function:** Converts observations into meaning. Without interpretation, signals exist but significance does not.

Interpretation survived repeated attacks and became a foundational optimizer component.

---

## Architectural Significance

Optimizer behavior emerges from Goal + Policy + Interpretation rather than from intelligence alone.

This became the basis for all later reasoning regarding:
- Attention
- Investigation
- Action
- Learning

## Collapsed Candidates

The following were tested and found to be emergent rather than primitive:
- **Evaluation** → collapsed into Policy + Interpretation
- **Navigation** → collapsed into Goal + Policy + Interpretation
- **Sufficiency** → reclassified as a judgment/gate (Action Stability)

## Cross-References
- FL_009 (Optimizer Architecture — the fault line that produced this)
- D011 (Differential Intervention Principle — the test used)
- FL_010 (Layer Separation — this belongs to the Theory layer)
