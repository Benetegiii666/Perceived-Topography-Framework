# DISCOVERY_016: Learning Events

**Status:** Candidate — Phase 4.1 discovery
**Date:** 2026-06-11

## Initial Question

What qualifies as a learning event?

## Rejected Candidates

- Outcome ≠ Learning (outcomes happen without learning)
- Prediction Error ≠ Learning (errors can be noticed without model updates)
- Update ≠ Learning (updates can be arbitrary, not evidence-supported)

## Candidate Definition

> A learning event is an evidence-supported update to the optimizer's model triggered by a mismatch between expectation and reality.

## Proposed Learning Flow

```
Expectation
    ↓
Action
    ↓
Outcome
    ↓
Prediction Error
    ↓
Investigation
    ↓
Evidence-Supported Explanation
    ↓
Model Update
```

## Learning Scope

This phase is currently focused on **experiential learning** (learning from doing). Not all learning requires prediction error — external evidence may also produce model updates. That remains future work.

## Model Update Targets

Learning may update:
- Action Model (how things work)
- Interpretation (how to read signals)
- Policy (what standards apply)
- Goal (what matters)

## Key Insight

Learning is NOT: Outcome, Postmortem, Lessons Learned Document.

Learning IS: **Evidence-Supported Model Update.**

## Organizational Implication

Lessons-learned repositories frequently fail because they store conclusions. They do not reliably store:
- Expectation (what we believed would happen)
- Outcome (what actually happened)
- Evidence (what we observed)
- Explanation (why the mismatch occurred)
- Model Update (what changed in our understanding)

Without the model update chain, learning cannot be reconstructed.

## Connection To Existing Literature

Maps naturally to:
- Reinforcement Learning (reward prediction error)
- Organizational Learning (Argyris & Schön)
- Single-Loop Learning (action correction)
- Double-Loop Learning (assumption revision)

## Cross-References
- CB_001 (Claude Reduction Branch — "organizations learn only from explicit comparison of beliefs to outcomes" is the same insight, less formally)
- FL_014 (Investigation Dynamics — investigation is the mechanism between prediction error and model update)
- FL_015 (Sufficiency — learning investigations also terminate via sufficiency)
- FL_009 (Optimizer Architecture — learning updates optimizer primitives)
