# FL_013: Optimizer Attraction Model

**Status:** RESOLVED
**Date:** 2026-06-11
**Phase:** 3.1 (Complete)

## Origin Question

Why does an optimizer allocate attention to one thing instead of another?

This phase explains attention allocation. It does not explain investigation (FL_014) or action. It explains what receives attention.

## Core Finding

Attraction is the allocation of optimizer attention toward regions of the perceived information topography.

Not all visible information attracts attention. Not all accessible information attracts attention. Attraction emerges from the interaction between optimizer goals and information-topography properties.

---

## Two Attraction Modes

### Action Attraction

**Answers:** Should I act on this?

**Mechanism:**
```
Goal Relevance + Confidence = Action Attraction
```

**Example:** Revenue down 20%, confidence high → strong action attraction.

**Pressure test results:**
- Goal Relevance alone **failed** — relevant but untrusted information triggers investigation, not action
- Confidence alone **failed** — trusted information that doesn't affect goals rarely attracts action
- Goal Relevance + Confidence **survived** as the primary action-attraction mechanism

### Exploration Attraction

**Answers:** Should I investigate this?

**Mechanism:**
```
Goal Relevance + Confidence Gap + Connectivity = Exploration Attraction
```

**Example:** Revenue down → Conversion down → Trust down → Support delays. Strong exploration attraction because explanatory pathways exist.

**Pressure test results:**
- Connectivity alone **failed** — well-understood connected information supports action, not exploration
- Uncertainty alone **failed** — low-confidence isolated information is frequently ignored
- Connectivity + Uncertainty **survived** — especially when connected to goal-relevant signals

---

## Attraction vs Investigation

An important distinction:

| Concept | Question | Allocates |
|---------|----------|-----------|
| Attraction | What receives attention? | Attention |
| Investigation | What receives explanatory effort? | Effort |

Relationship: Attraction → Investigation. Attraction allocates attention. Investigation allocates effort.

## Architectural Significance

Attraction is the first stage of optimizer motion. The optimizer does not investigate everything. It first allocates attention. Only then does investigation occur.

## Cross-References
- FL_014 (Investigation Dynamics — the next stage after attraction)
- FL_015 (Sufficiency — when investigation stops and action begins)
- D015 (Topography Engineering Dimensions — Confidence and Connectivity are key attraction inputs)
- FL_009 (Optimizer Architecture — Goal drives attraction through Goal Relevance)
