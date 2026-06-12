# Learning — Phase 4.1 Complete

**Status:** Foundational — closes the adaptive loop
**Date:** 2026-06-11

---

## Core Finding

Learning is an evidence-supported optimizer modification triggered by prediction error.

```
A learning event occurs when a mismatch between expectation and outcome
is investigated, explained with evidence, and converted into a reusable
update to the optimizer's Interpretation, Policy, Goal, or Action Model.
```

---

## Learning Flow

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

Learning does not occur merely because an outcome happened. Learning does not occur merely because behavior changed. Learning occurs when the optimizer's model is updated based on an evidence-supported explanation of the mismatch between expectation and reality.

---

## Learning vs Reaction

**Reaction:** Expectation violated → immediate conclusion → behavior changes. Example: "Campaign failed. Never use TV again." This is overcorrection, not learning.

**Learning:** Expectation violated → investigation → evidence-supported explanation → model update → future behavior changes. The optimizer changes because the mismatch was *explained*.

---

## What Gets Updated — Four Targets

### 1. Interpretation Update
Updates what the optimizer believes a signal means.
*Example: "Awareness increase means sales likely increase" → "Awareness alone does not mean sales readiness. Audience composition matters."*

### 2. Policy Update
Updates the rules, gates, or constraints governing future behavior.
*Example: "Campaigns can be approved with brand-recall forecast" → "Campaigns over $X must include a purchase-intent hypothesis and measurement plan."*

### 3. Goal Update
Updates what the optimizer is optimizing for, or how the goal is framed.
*Example: "Campaign success = immediate sales growth" → "For this campaign type, optimize for qualified awareness and purchase intent."*

### 4. Action Model Update
Updates the optimizer's belief about which actions produce which outcomes.
*Example: "TV campaign → awareness → sales" → "For this audience, awareness campaigns require trust/proof-point components to influence conversion."*

---

## Pressure Test Results

**Capability** did not force a new update target. Capability limitations map to Interpretation + Action Model + Policy updates.

**Decision Space** did not force a new update target. Decision Space affects available actions after learning, but the learning event itself maps to the four targets.

Both remain under investigation but are not promoted as learning-update targets.

---

## Reusable Unit of Learning: Model Update Object

The reusable unit is NOT: Outcome, Postmortem, Lesson Learned, Conclusion.

The reusable unit IS: **Model Update Object** — preserves the reasoning chain needed for future optimizers to apply the learning without overgeneralizing.

### Why Lessons-Learned Repositories Fail

They store: Outcome, Conclusion, Recommendation.
They do NOT store: Expectation, Prediction Error, Evidence, Explanation, Update Type, Applicability Boundary, Confidence.

Without this structure, organizational memory becomes folklore. With it, organizational memory becomes reusable optimizer modification.

### Model Update Object Example

```
Prior Expectation: Broad awareness would increase sales.
Action: Run awareness campaign.
Observed Outcome: Awareness increased; sales did not.
Prediction Error: Expected sales lift did not occur.
Evidence: Awareness lift concentrated among existing customers, not prospects.
Explanation: Campaign reached wrong audience, insufficient purchase intent.
Update Type: Action Model + Interpretation
Model Update: Awareness is not independently predictive of sales.
              Supports sales only when audience fit and purchase intent are present.
Applicability Boundary: Applies to awareness campaigns evaluated against
                        near-term sales conversion. Does not imply all
                        awareness campaigns fail.
Confidence: Moderate to high.
```

---

## Adaptive Loop Closure

Phase 4.1 closes the adaptive loop:

```
Optimizer (Goal, Policy, Interpretation, Action Model)
    ↓
Motion (Attraction → Investigation → Sufficiency → Action)
    ↓
Outcome
    ↓
Prediction Error
    ↓
Learning Investigation
    ↓
Model Update Object
    ↓
Modified Optimizer
```

The optimizer produces behavior. Behavior produces outcomes. Outcomes produce prediction errors. Prediction errors trigger learning. Learning modifies the optimizer. The modified optimizer produces different future behavior.

---

## Note: Action Model

Action Model emerged as a necessary learning-update target. Its classification is under investigation:
- Optimizer subcomponent?
- Derived behavioral model?
- Architecture-layer object?

Do not automatically promote without additional pressure testing.

## Cross-References
- D016 (Learning Events — the discovery that initiated this phase)
- FL_014 (Investigation Dynamics — learning investigation follows the same trigger pattern)
- FL_015 (Sufficiency — learning investigations also terminate via sufficiency)
- FL_009 (Optimizer Architecture — learning updates optimizer primitives)
- CB_001 (Claude Reduction Branch — "organizations learn from explicit comparison of beliefs to outcomes")
