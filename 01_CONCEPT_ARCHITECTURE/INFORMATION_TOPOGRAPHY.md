# Information Topography — Phase 2 Complete

**Status:** Foundational — dimensions survived D011 separation testing
**Date:** 2026-06-11

---

## Origin Question

Once agents were understood as optimizers, the next question became:

> What properties of information create gradients that influence optimizer behavior?

This led to the concept of **Information Topography**.

## Core Finding

Optimizers do not move through reality directly. They move through **perceived information environments**.

Information environments possess structure. That structure creates gradients. Those gradients influence:
- Attention
- Exploration
- Investigation
- Action

---

## Five Primary Dimensions

### Visibility

**Answers:** Can this information be perceived?

**Examples:** Displayed, hidden, surfaced, obscured.

Information that cannot be perceived cannot influence optimization.

### Accessibility

**Answers:** Can this information be reached?

**Examples:** Permission barriers, retrieval cost, latency, distance.

Information may be visible but inaccessible. Visibility and Accessibility survived separation testing and remain distinct dimensions.

### Representation

**Answers:** How is information expressed?

**Examples:** Text, graph, metric, dashboard, narrative, visualization.

Representation influences interpretability. Different representations create different optimizer behavior.

### Confidence

**Answers:** How trustworthy is this information?

**Examples:** Reliable, uncertain, conflicting, verified.

Confidence influences willingness to act. Confidence later became critical to Investigation, Sufficiency, and Learning.

### Connectivity

**Answers:** What is this connected to?

**Examples:** Cause relationships, dependency relationships, correlations, explanatory links.

Connectivity became one of the most important dimensions. It explains exploration, investigation, task decomposition, and explanatory search.

---

## Goal Relevance — Derived, Not a Dimension

Goal Relevance is **relational**, not a topography dimension.

**Answers:** Why does this matter to me?

It emerges from Signal relative to Goal, rather than existing as an independent property of the information environment.

---

## Information Surfaces

Information does not exist merely as isolated facts. Information appears to optimizers as **surfaces** containing:

```
Visibility + Accessibility + Representation + Confidence + Connectivity
```

The optimizer navigates these surfaces. This became one of the central organizing concepts of the framework.

---

## Retrieval vs Topography

An important distinction:

- **Traditional retrieval** focuses on: Finding information
- **The framework** asks: What information environment is being presented to the optimizer?

This distinction became foundational to later discussions around agent enablement, knowledge systems, context layers, and research injection layers.

---

## Architectural Significance

Information Topography provides the environmental model for optimizer behavior.

```
Optimizer (Goal, Policy, Interpretation)
    encounters
Information Topography (Visibility, Accessibility, Representation, Confidence, Connectivity)
    through
Information Surfaces
```

Goal Relevance emerges from the interaction between Goal and Signal.

Together these elements create the gradients that drive Attention, Exploration, Investigation, Action, and Learning.

## Cross-References
- D015 (Topography Engineering Dimensions — the discovery that identified candidates)
- FL_007 (Interface Layer — the original fault line on information surfaces)
- EC_004 (Information Surfaces — the emerging concept that matured into this)
- FL_010 (Layer Separation — this belongs to the Topography Engineering layer)
