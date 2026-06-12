# Model Update Objects — Phase 4.2 Complete

**Status:** Foundational — defines the reusable artifact of learning
**Date:** 2026-06-11

---

## Core Finding

A Model Update Object is a bounded, observable, human-readable record of a model transition.

> A Model Update Object is a bounded optimizer modification, wrapped in observability metadata and expressed through a human-ready view, so future optimizers can retrieve, evaluate, and apply learning safely.

---

## Three-Layer Structure

```
Model Update Object
    = Core Learning Payload
    + Observability Envelope
    + Human-Ready View
```

### 1. Core Learning Payload — The Truth Layer

| Field | Prevents |
|-------|---------|
| Prior Expectation | No learning delta |
| Prior Basis / Premise Stack | Misdiagnosed failed assumption |
| Triggering Context / Action | Context collapse |
| Observed Outcome | Speculation |
| Prediction Error | Ambiguous mismatch |
| Evidence / Investigation Trace | Rationalization |
| Explanation | Raw data without meaning |
| Update Target | Vague reuse |
| Model Update | Postmortem without learning |
| Applicability Boundary | Overgeneralization |
| Confidence | False certainty |

### 2. Observability Envelope — The Trust Layer

Answers: Where did this come from? Who owns it? Is it still valid?

Fields: Object ID, Source Learning Event, Created Date/By, Owner/Steward, Source/Evidence References, Version, Status, Confidence History, Supersedes/Superseded By, Usage Log, Validation Log, Last Reviewed Date, Conflict Flags.

**Status values:** Provisional, Validated, Deprecated, Superseded, Rejected.

### 3. Human-Ready View — The Usability Layer

Fields: Title, One-Line So What, What Changed, Assumption Changed, Use This When, Do Not Use This When, Confidence/Caveat, Recommended Future Check.

**Rule:** Human-ready copy is not authoritative. The Core Learning Payload remains the source of truth.

---

## Premise Stack

A Premise Stack is the artifact-backed set of assumptions, source materials, and prior model inputs that produced an optimizer's expectation before action or observation.

**Short definition:** The artifact-backed basis for a prior expectation.

**Examples:** Campaign brief, ICP, persona, PRD, runbook, incident history, agent policy, prompt design, measurement plan, historical data, executive strategy, market research.

**Key distinction:**
- Premise Stack answers: *Why did we expect this to work?*
- Evidence answers: *Why do we now believe the model should change?*
- Prior Basis / Premise Stack ≠ Evidence

### Topography-Shaping Artifacts

Premise artifacts are not topography dimensions. They are **topography-shaping artifacts** — they influence what the optimizer perceives as visible, relevant, trusted, connected, and actionable.

| Artifact | Shapes |
|----------|--------|
| ICP | Goal Relevance, Representation, Connectivity |
| Campaign Brief | Goal, Action Model, Success Criteria, Policy |
| Measurement Plan | Visibility, Confidence, Sufficiency |
| Historical Data | Confidence, Interpretation, Action Model |
| PRD | Goal, Interpretation, Action Model, Success Criteria |

These should be tracked as premise/provenance structures, not as new topography dimensions.

---

## Action Model Classification — RESOLVED

Action Model is **not** a fourth optimizer primitive. It is a named substructure of Interpretation.

```
Optimizer
    Goal
    Policy
    Interpretation
        Signal Meaning
        Causal Explanation
        Action Model
```

**Definition:** Action Model is the optimizer's causal expectation model for which actions produce which outcomes under which conditions.

**Usage:** `Update Target: Interpretation / Update Subtype: Action Model`

This keeps the optimizer primitive set stable at three: Goal, Policy, Interpretation.

---

## Retrieval / Use Rules

1. **Start With Active Goal** — cannot apply without knowing current goal
2. **Match On Premise, Not Just Topic** — retrieve by premise-stack similarity
3. **Applicability Boundary Gates Reuse** — weak match = context for investigation, not action guide
4. **Confidence Controls Force** — Low = hypothesis; Moderate = planning consideration; High = strong constraint unless contradicted
5. **Status Matters** — deprecated/superseded/rejected retrieved for history only
6. **Update Target Controls Application** — apply to correct optimizer component
7. **Conflicting Updates Trigger Investigation** — do not average blindly
8. **Human-Ready Copy Is Not Authoritative** — Core Learning Payload is source of truth

---

## Bad-Update Failure Modes

1. **Folklore Update** — conclusion without evidence
2. **Premise-Blind Update** — ignores assumptions that produced original expectation
3. **Overgeneralized Update** — bounded learning becomes universal dogma
4. **Stale Update** — remains active after context changed
5. **Confidence Inflation** — claims more certainty than evidence supports
6. **Misclassified Update Target** — updates wrong optimizer component
7. **Policy Laundering** — recommendation mistaken for authorized policy
8. **Human-Ready Drift** — summary corrupts core learning
9. **Retrieval Bias** — most visible retrieved instead of most applicable
10. **Contradiction Suppression** — conflicting updates hidden instead of investigated

---

## Cross-Domain Validation

Tested across Marketing, Product, Operations, AI Agent Behavior, and Hiring/Organizational Design. In each case, Premise Stack identified which prior assumption failed. The structure generalized beyond marketing.

### Marketing
- Bad: "TV campaigns do not drive sales"
- Better: "Awareness supports sales only when it reaches qualified prospects and connects to purchase intent"
- Failed Premise: Campaign brief assumed broad awareness → near-term conversion

### Product
- Bad: "Users do not want customization"
- Better: "Flexibility may mean better adaptive defaults, not more setup burden"
- Failed Premise: PRD interpreted flexibility requests as desire for configuration

### Operations
- Bad: "Do not automate restarts"
- Better: "CPU saturation should be interpreted as a symptom requiring dependency checks before restart"
- Failed Premise: Runbook treated CPU saturation as cause rather than symptom

### AI Agent Behavior
- Bad: "Agents should not send emails"
- Better: "Auto-send requires sentiment, escalation, and relationship-risk checks"
- Failed Premise: Policy confused ticket resolution with customer readiness

### Hiring
- Bad: "Do not hire process-heavy leaders"
- Better: "Distinguish execution-process failure from decision-rights failure before hiring for operational control"
- Failed Premise: Misdiagnosed bottleneck as weak execution rather than unclear decision rights

---

## Cross-References
- `LEARNING.md` (Phase 4.1 — the learning process that produces Model Update Objects)
- `OPTIMIZER_THEORY.md` (the primitives that get updated)
- FL_009 (Optimizer Architecture — Action Model classification resolved here)
- D016 (Learning Events — the discovery that initiated Phase 4)
- CA_006 (Architecture vs Theory Conflation — Premise Stack and Model Update Object are architecture-layer, not theory-layer)
