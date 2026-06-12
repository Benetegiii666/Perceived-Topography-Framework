# Research Roadmap

> Define scope. Define done. Kill rabbit holes.

**Date:** 2026-06-11
**Status:** Active

---

## PHASE 1 — Stabilize The Theory

**Goal:** Determine whether the optimizer/topography theory is coherent enough to serve as a foundation.

### Task 1.1 — Lock Layer Separation

**Question:** Do Theory, Topography Engineering, Architecture, and Implementation remain independent layers?

**Current Status:** Strongly supported.

**Done When:**
- [ ] Each layer answers a distinct question
- [ ] D011-style independence survives
- [ ] No new layers added without surviving pressure testing

**Deliverable:** `FL_011_Layer_Separation_Finalization.md`

---

### Task 1.2 — Resolve Cross-Layer Leaks

**Question:** Are Goal and Policy the same thing across layers?

**Current Status:** Open. Flagged in FL_010.

**Done When:** For each of Goal and Policy, we can explain:
- [ ] Theory meaning
- [ ] Topography Engineering meaning
- [ ] Architecture meaning
- [ ] No contradictions between meanings

**Deliverable:** `D016_Cross_Layer_Entity_Analysis.md`

---

## PHASE 2 — Find The Topography Dimensions

**This is now the most important work. Everything else depends on it.**

### Task 2.1 — Candidate Dimension Review

**Current candidates:**

| Dimensions | Modifiers | Constraint Candidate |
|-----------|-----------|---------------------|
| Visibility | Contradiction | Policy |
| Accessibility | Recency | |
| Representation | | |
| Confidence | | |
| Connectivity | | |
| Goal Relevance | | |

**Done When:**
- [ ] Candidate list agreed
- [ ] No new dimensions introduced without strong justification

**Deliverable:** `D017_Topography_Dimension_Candidate_Set.md`

---

### Task 2.2 — D011 Reduction

Run pairwise attacks:
- Can Visibility exist without Accessibility?
- Can Accessibility exist without Visibility?
- Can Confidence exist without Representation?
- Can Connectivity exist without Goal Relevance?
- (all pairs)

**Done When:**
- [ ] Every surviving dimension demonstrates independence
- [ ] Every collapsed dimension is removed

**Deliverable:** AHA Candidate — Irreducible Topography Dimensions

---

### Task 2.3 — Optimizer Failure Mapping

**Question:** Can optimizer failures be mapped to dimension failures?

| Failure | Dimension |
|---------|-----------|
| Missed Opportunity | Visibility Failure |
| Bad Trust Decision | Confidence Failure |
| Failure To Connect Signals | Connectivity Failure |

**Done When:**
- [ ] 80%+ of realistic failures map cleanly

**Deliverable:** `FL_012_Topography_Failure_Taxonomy.md`

---

## PHASE 3 — Define Optimizer Motion

**This is where the gold probably lives. Not the dimensions. The movement.**

### Task 3.1 — Define Attraction

**Question:** Why does an optimizer pursue one signal over another?

**Example:** High Visibility / Low Confidence vs Medium Visibility / High Confidence — what wins?

**Done When:**
- [ ] We can describe how dimensions combine to create gradient strength

**Deliverable:** `FL_013_Optimizer_Attraction_Model.md`

---

### Task 3.2 — Define Investigation

**Question:** What causes an optimizer to stop, look deeper, spawn a task, request more evidence?

**Done When:**
- [x] We can describe investigation triggers ✓ Goal-Relevant Observation + Confidence Gap = Trigger
- [x] Connectivity guides explanatory search ✓
- [x] Three termination conditions identified ✓

**Deliverable:** `FL_014_Optimizer_Investigation_Dynamics.md` — **COMPLETE**

---

### Task 3.3 — Define Sufficiency

**Question:** When does an optimizer stop searching?

**Done When:**
- [x] We can explain Continue Searching vs Act Now without introducing new primitives ✓
- [x] Sufficiency defined as Action Stability ✓
- [x] Confidence and Sufficiency shown to be independent (both directions tested) ✓

**Deliverable:** `FL_015_Sufficiency_as_Emergent_Behavior.md` — **COMPLETE**

---

## PHASE 4 — Validate Architecture

**Only after theory is stable.**

### Task 4.1 — Revisit Reasoning Architecture

Return to: Working Theory, Evidence, Decision, Outcome, Uncertainty.

**Question:** Do these emerge naturally from the theory?

**Done When:**
- [ ] Each object traces back to Optimizer Theory + Topography Dimensions

**Deliverable:** `CA_007_Reasoning_Architecture_Validation.md`

**Progress:** D016 (Learning Events) discovered during this phase — learning defined as evidence-supported model update, not outcome or postmortem. Learning flow: Expectation → Action → Outcome → Prediction Error → Investigation → Evidence-Supported Explanation → Model Update. Under continued investigation.

---

### Task 4.2 — Validate Discovery Framework

**Question:** Do interview questions naturally emerge from theory?

**Done When:**
- [ ] Every discovery question maps to a Dimension or Optimizer Primitive

**Deliverable:** `OP_002_Discovery_Framework_Validation.md`

---

## PHASE 5 — Stop

**Seriously. Stop.**

### Success Criteria

- [ ] Stable Layer Separation
- [ ] Stable Topography Dimensions
- [ ] Stable Optimizer Motion Model
- [ ] Validated Architecture
- [ ] Validated Discovery Framework

### Definition of Gold

Gold is **NOT:** Perfect Theory

Gold **IS:** We can explain optimizer behavior, describe the information dimensions that shape it, explain how movement occurs through that landscape, and derive practical architecture and discovery methods from the theory.

If we achieve that, this phase is complete and worthy of filing as a major milestone. The next phase is implementation and experimentation, not more foundational digging.

---

### Anti-Drift Rules

1. No new dimensions without strong justification
2. No new primitives without D011 survival
3. No new layers without pressure testing
4. No new entities without tracing back to theory
5. If a rabbit hole opens, file it and move on — don't chase it
6. Phase 3 is the priority target — dimensions without motion is taxonomy, not theory
