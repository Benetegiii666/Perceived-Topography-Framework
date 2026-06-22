# v1.0 Section 6 Source Packet

## Learning Requires Preserved Reasoning

---

## Section Purpose

Section 6 must explain what learning is, why learning requires preserved prior reasoning, how prediction error becomes identifiable, and how a durable model update can change future optimizer state and perceived topography.

The section must inherit the ending of Section 5 without merely repeating it. Section 5 has already demonstrated one concrete learning trace. Section 6 must now explain why that transition counts as learning and why an outcome, correction, reaction, or postmortem does not automatically do so.

The controlling insight:

An organization cannot learn from an outcome unless it preserved enough of the prior reasoning to identify what reality contradicted. And even a correct lesson does not become organizational learning unless it is represented so that it can reshape future reasoning, optimizer state, and perceived topography.

---

## Narrative Position

Sections 1-5 now establish:

- Landscape design (S1)
- Context versus reasoning state (S2)
- Optimizer state and perceived topography (S3)
- Gradients, attention, attraction, investigation, sufficiency, and action (S4)
- A complete healthcare campaign stress test (S5)

Section 6 begins after reality has returned an outcome. Its opening conceptual move:

Premature sufficiency explains why motion stopped too early. Prediction error becomes visible when reality reveals that the model supporting that stopping condition was incomplete or wrong.

---

## Reader Realization

After reading Section 6, the reader should be able to say:

"Learning is not the same as storing an outcome, correcting an error, reacting to a failure, or writing a postmortem. Learning occurs when a preserved expectation is contradicted by an observed outcome, the mismatch is investigated, an evidence-supported explanation is formed, and the resulting model update changes future reasoning. The Model Update Object preserves that transition so it can reshape future topography."

---

## Opening Bridge from Section 5

Section 5 ends with:

> "Memory can retrieve the old material. Learning changes the reasoning state from which the next action begins."

Section 6 should deepen that distinction. The reader has already seen one concrete instance. Section 6 generalizes: what makes something learning rather than memory, correction, or reaction?

Do not replay the campaign. Use it as a compact callback. The reader already holds the scenario.

---

## Source Files and Line Ranges

| Source | File | Relevant sections | Line ranges |
| --- | --- | --- | --- |
| v0.2 Learning section | PAPER_v0.2.md | S8: Learning Begins When Reality Pushes Back | Lines 1442-1758 |
| v0.2 MUO section | PAPER_v0.2.md | S9: Lessons Need Objects | Lines 1759-1972 |
| v0.2 Reasoning architecture | PAPER_v0.2.md | S10: The Reasoning Has to Survive the Answer | Lines 1973-2216 |
| v0.1 Learning section | PAPER_v0.1.md | S8: Learning: Prediction Error and Model Update | Lines ~1580-1720 (near-identical to v0.2 S8) |
| v0.1 MUO section | PAPER_v0.1.md | S9: Model Update Objects: Preserving Learning | Lines ~1720-1960 |
| v0.1 Reasoning architecture | PAPER_v0.1.md | S10: Reasoning Architecture: Preserving State Transitions | Lines ~1960-2200 |
| Concept architecture | CURRENT_STATE.md | Learning (Phase 4.1), MUO (Phase 4.2), Reasoning Architecture (Phase 4.3) | Lines 72-106 |
| v1.0 S5 ending | PAPER_v1.0_WORKING.md | "What survives the campaign" | Lines 820-882 |
| Reviewer synthesis | V0_2_REVIEW_SYNTHESIS_MEMO.md | KM graveyard risk, MUO adoption concern | Lines 43-45, 115, 159 |
| Rewrite doctrine | V1_0_REWRITE_DOCTRINE_AND_WORKPLAN.md | Objection response: KM graveyard | Section 11 |

---

## Inherited Claims from Sections 1-5

### Landscape Design

S1 established that safer behavior comes from shaping the landscape, not just constraining the agent. Learning must connect back: a model update reshapes the future landscape.

### Context Versus Reasoning State

S2 established that context preserves artifacts but not the reasoning behind decisions. Learning must show that preserved reasoning is what makes learning possible — without it, the organization has only outcomes and hindsight.

### Optimizer State and Perceived Topography

S3 defined Goal, Policy, Interpretation, and the five topography dimensions. Learning must show that model updates change one or more of these: a revised goal, policy, interpretation, or topography condition.

### Motion, Sufficiency, and Failure

S4 defined how motion through gradients produces action at sufficiency. Learning must show that prediction error reveals where sufficiency was premature — where the model supporting the stopping condition was incomplete.

### Healthcare Campaign Stress Test

S5 demonstrated a concrete learning trace: premise, boundary, prediction, observed outcome, interpretation update, unresolved question, decision update, next-cycle change. Section 6 must generalize from that trace, not repeat it.

---

## Original Learning Material Inventory

### Preserved Concepts

| Concept | v0.2 location | Status for v1.0 |
| --- | --- | --- |
| "Learning is an evidence-supported model update triggered by prediction error" | v0.2 S8 line 1454 | **Preserve as the primary definition** |
| Seven-step learning sequence | v0.2 S8 lines 1460-1462 | **Preserve** |
| Expectation gives reality something to test | v0.2 S8.1 lines 1470-1487 | **Preserve** |
| Prediction error as trigger | v0.2 S8.4 lines 1520-1543 | **Preserve** |
| Investigation turns surprise into explanation | v0.2 S8.5 lines 1546-1561 | **Preserve** |
| Evidence-supported explanation | v0.2 S8.6 lines 1564-1586 | **Preserve** |
| Model update changes Goal, Policy, or Interpretation | v0.2 S8.7 lines 1589-1614 | **Preserve (compressed)** |
| Reaction vs. learning distinction | v0.2 S8.8 lines 1617-1634 | **Preserve — one of the paper's most valued distinctions** |
| Postmortem is not automatically learning | v0.2 S8.9 lines 1637-1651 | **Preserve** |
| Learning reshapes the landscape | v0.2 S8.12 lines 1713-1729 | **Preserve** |
| Model Update Object definition and purpose | v0.2 S9 lines 1759-1776 | **Preserve** |
| Eleven-field Core Learning Payload | v0.2 S9.3 lines 1805-1847 | **Introduce conceptually; compress field-by-field detail** |
| Ten failure modes MUOs prevent | v0.2 S9.7 lines 1920-1934 | **Preserve (may compress to 5-6 most important)** |
| MUOs reshape the landscape | v0.2 S9.8 lines 1937-1952 | **Preserve** |
| Filled MUO example (healthcare campaign) | v0.2 S9.6 lines 1884-1913 | **Preserve (S5 already carries much of this; compact callback)** |

### Strong Original Formulations

These should be preserved or closely paraphrased:

1. "Learning is an evidence-supported model update triggered by prediction error." (v0.2 S8 line 1454)
2. "A bad outcome is not learning. A correction is not learning. A reaction is not learning. A postmortem is not necessarily learning." (v0.2 S8 line 1456)
3. "The test is simple: Does the change make future reasoning more accurate under defined conditions?" (v0.2 S8.8 line 1632)
4. "Narrative memory can be read. Model updates can be reused." (v0.2 S8.9 line 1650)
5. "Where does the learning go?" (v0.2 S9 line 1765)
6. "Its purpose is not simply to store what happened. Its purpose is to change future reasoning." (v0.2 S9 line 1775)
7. "Learning reshapes the landscape." (v0.2 S8.12 title)

### Material Requiring Refinement

- The seven-step sequence may benefit from clearer presentation: possibly a small table or structured list rather than a code block.
- The eleven-field MUO payload table (v0.2 S9.3) is useful but may be too detailed for Section 6. Section 6 should introduce the conceptual payload; Section 8 can carry the full specification if needed.

### Material to Compress

- v0.2 S8.1-S8.3 (Expectation, Action, Outcome) each have their own subsection. In v1.0, these can be presented as a continuous narrative rather than three separate subsections.
- v0.2 S8.10-S8.11 (campaign learning walkthrough, safety learning walkthrough): S5 already carries the campaign version. The safety version can be compressed to 3-4 sentences.
- v0.2 S9.2 (three layers of MUO): can be introduced conceptually without full subsection treatment.
- v0.2 S9.4-S9.5 (Observability Envelope, Human-Ready View): defer details to S8.

### Material to Defer

- Full Observability Envelope specification -> S8
- Full Human-Ready View specification -> S8
- Lifecycle states and governance -> S8
- Full six-object reasoning architecture -> compress into S6 or defer to S8
- Complete MUO field-by-field specification -> S8

### Material to Retire

- Separate campaign and safety learning walkthroughs (v0.2 S8.10, S8.11) as distinct subsections: S5 carries the campaign; one brief safety callback is enough.

---

## Canonical Definitions

### Learning

"Learning is an evidence-supported model update triggered by prediction error." (v0.2 S8 line 1454; CURRENT_STATE.md line 74)

**Recommendation:** Preserve as the primary definition. It is precise, testable, and well-anchored in Argyris & Schon.

### Expectation

What the optimizer believed would happen before action. Without a preserved expectation, prediction error cannot be identified.

### Prediction Error

The mismatch between expected and observed outcome. The trigger condition for learning.

### Investigation

The process of examining why the expected and observed outcomes diverged. Protects learning from false explanation.

### Evidence-Supported Explanation

An explanation connecting prediction error to a plausible cause with enough support to justify updating the model. Not a guess, not a convenient story, not the loudest stakeholder's interpretation.

### Model Update

A change to future reasoning. May update Goal, Policy, Interpretation, or Action Model. Must be specific enough to change behavior but bounded enough to avoid overgeneralization.

### Preserved Reasoning

The structured reasoning state (goal, policy, interpretation, premises, confidence, sufficiency rationale) that must be preserved before action so that learning becomes possible after action.

### Model Update Object

A bounded, reusable record of learning whose purpose is not simply to store what happened, but to change future reasoning. The MUO is not identical to learning; it is the durable representation through which learning can survive and influence later reasoning.

---

## Required Conceptual Distinctions

### Outcome Versus Learning

An outcome is evidence that learning may be needed. It does not identify what was expected, why it was expected, what premise failed, or what should change.

### Correction Versus Learning

A human can repair one output without changing the model that generated it. The same error can recur because the underlying reasoning was not updated.

### Reaction Versus Learning

A reaction changes behavior without an evidence-supported explanation. Example: unsafe tool action -> remove all tools. This suppresses behavior without identifying which tool mattered, which consequence was invisible, which policy failed to exert force, or which future situations the lesson applies to.

### Postmortem Versus Learning

A postmortem becomes learning only when it produces a justified model update that changes future reasoning. Narrative memory can be read. Model updates can be reused.

### Storage Versus Learning

Storing an outcome, report, or prior copy does not guarantee that the reasoning transition becomes behaviorally available later.

### Learning Versus Model Update Object

Learning = the justified reasoning transition. Model Update Object = the bounded representation through which that transition can survive and influence later reasoning. Do not present them as identical.

---

## Five-Movement Narrative Plan

### Movement 1: Reality Exposes the Stopping Error

Use the Section 5 campaign outcome as a compact callback (~150 words):

- Workflow-pain language attracted attention; engagement was strong
- Qualified-demo conversion was weaker than expected
- The audience interpretation had been incomplete
- The clinical-claim boundary remained intact

Connect to S4: sufficiency governed when action occurred. Prediction error reveals that the reasoning supporting that sufficiency condition did not fully match reality.

Not every learning event begins as premature sufficiency. The bridge here is narrower: when action occurred because a reasoning state had become sufficient, later outcomes can reveal that the sufficiency condition rested on an incomplete or mistaken model.

The reader should understand: you cannot learn from this mismatch unless you preserved the expectation that reality contradicted.

### Movement 2: Learning Is Model Change

Present the canonical learning sequence (~400 words):

Expectation -> Action -> Outcome -> Prediction Error -> Investigation -> Evidence-Supported Explanation -> Model Update

Give special weight to:

- Preserved expectation (without it, no prediction error)
- Identifying the mismatch (not just the outcome)
- Investigating the mismatch (the first explanation is often wrong)
- Evidence-supported explanation (not a guess)
- Identifying the correct update target (Goal, Policy, Interpretation, Action Model)

The reader should understand: a changed output is not enough. The model that shaped the output must change.

### Movement 3: Reaction Is Not Learning

Two examples (~300 words):

1. Healthcare campaign: weak reaction ("abandon workflow-pain messaging entirely") vs. learning (update the audience model so workflow pain is treated as attention signal, not proof of buying readiness).

2. Unsafe tool action: weak reaction ("remove all tools") vs. learning (identify the specific tool affordance, missing consequence visibility, failed policy connection, or absent approval condition).

Preserve the test: "Does the change make future reasoning more accurate under defined conditions?"

### Movement 4: Learning Reshapes Future Topography

Make explicit that learning is not only a belief change (~250 words).

A model update can alter:

- Which information surfaces are exposed
- How prior evidence is represented
- Confidence in a prior signal
- Connectivity between action and consequence
- Which uncertainty attracts investigation
- What must be true before sufficiency is reached
- Which escalation path becomes easy
- Which action affordance becomes available

This is the main connection back to Sections 1-4. Learning becomes governance when it changes the future landscape.

Show the before/after: "Before: workflow pain -> buying intent. After: workflow pain -> attention signal; buying readiness -> qualification signal."

### Movement 5: Where the Learning Goes

Introduce the Model Update Object (~400 words):

"Where does the learning go?" — the strongest opening for this movement.

Introduce the concept: a bounded, reusable record of learning whose purpose is not simply to store what happened, but to change future reasoning.

Present the minimum conceptual payload (see below). Show one compact filled example (compact callback from S5's learning trace, not a full replay).

Introduce the KM graveyard confrontation: structured learning repositories have failed before (Lotus Notes, SharePoint, ITIL). Acknowledge the risk directly. The point is not to create a better archive. A model update must be represented so that it can exert future behavioral force, or it becomes another lessons-learned artifact that exists without changing later action. The framework's design response to this risk is addressed in Section 7. Acknowledge the secondary risk: AI-inferred reasoning objects may be inaccurate, and trust in them must be earned rather than assumed.

Name the ten failure modes MUOs prevent (compressed to 5-6 most important): folklore, premise-blind updates, overgeneralization, stale updates, confidence inflation.

End with: MUOs reshape the landscape. The next campaign begins from a different topography.

---

## Healthcare Campaign Callback

Use as a compact callback (~100 words), not a replay:

| Element | Content |
| --- | --- |
| Prior expectation | Workflow-pain messaging will generate qualified demo interest |
| Observed outcome | Strong engagement, weaker-than-expected qualified conversion |
| Prediction error | Workflow pain attracted attention but did not indicate buying readiness |
| Evidence-supported interpretation update | Practice operators resonated with workflow burden, but many were problem-aware rather than actively evaluating |
| Next-cycle change | Workflow pain treated as attention signal; buying-stage readiness added as qualification requirement |

The reader already holds this from S5. Do not re-derive it.

---

## Unsafe Tool-Action Callback

Use as a compact secondary example (~100 words):

| Element | Content |
| --- | --- |
| Weak reaction | Remove all tools |
| Material investigation | Which tool? Under what conditions? What policy was missing? What consequence was invisible? What prior learning was not retrieved? |
| Model-level learning | Restart is unsafe when replication lag exceeds a threshold. The issue is not the tool; it is the missing consequence visibility and approval condition. |
| Future topography change | Prior incident learning made visible at tool boundary. Consequence preview connected to restart action. Approval required when pattern matches prior failure. |

---

## Minimum Model Update Object Payload

### Essential in Section 6

These fields must be introduced conceptually (not necessarily as a formal table):

| Field | What it prevents |
| --- | --- |
| Prior expectation | No learning delta — system cannot identify what changed |
| Premise stack / basis | Premise-blind learning — system learns from outcome without knowing which assumption failed |
| Observed outcome | Vague outcome memory |
| Prediction error | Outcome mistaken for learning |
| Evidence / investigation trace | Rationalized learning — first convenient explanation accepted |
| Model update | Lesson too vague to guide future action |
| Applicability boundary | Overgeneralized learning |
| Confidence | False certainty |

The minimum payload is a target, not an all-or-nothing validity test. Partial records may still be useful, but missing expectation, explanation, applicability boundary, or confidence reduces reuse reliability and should remain visible.

### Optional in Section 6

- Update target (Goal, Policy, Interpretation, Action Model) — can be mentioned in prose
- Explanation as a separate field — can be folded into the evidence/investigation description
- Triggering context / action — can remain implicit in the narrative

### Deferred to Section 8

- Full eleven-field specification with field-by-field definitions
- Observability Envelope (ID, source, dates, owner, status, version, validation log)
- Human-Ready View (title, so-what, use-when, do-not-use-when)
- Lifecycle states (Provisional, Validated, Deprecated, Superseded, Rejected)
- Storage and retrieval architecture
- Governance controls
- Full six-object reasoning architecture specification

---

## Boundary with Section 7

Section 7: Discovery Turns Human Intent Into Reusable Reasoning

Section 6 explains what learning is and how lessons become durable objects.

Section 7 explains how human intent, tacit knowledge, assumptions, boundaries, and decision logic are elicited — how organizations capture reasoning that otherwise remains inside people.

The bridge from S6 to S7: "Model Update Objects preserve learning after action. But reasoning must also be captured before action — from the messy intent, tacit assumptions, and organizational knowledge that humans carry but rarely make explicit."

Do not turn Section 6 into a Discovery section. Do not explain the RIPC loop (Retrieve-Infer-Propose-Confirm) in S6.

---

## Boundary with Section 8

Section 8: What It Would Take to Build This

Section 6 establishes conceptual requirements (what learning is, what must be preserved, what a model update must contain).

Section 8 handles implementation architecture (how to build the storage, retrieval, governance, lifecycle, and reasoning-object system).

Do not prematurely formalize the entire reasoning-object system in Section 6. Section 6 should make the reader understand what the objects are for. Section 8 should make the reader understand how they could be built.

---

## Boundary with Section 9

Section 9: Boundaries, Objections, and Falsifiability

Section 6 should present learning and MUOs as proposed design concepts, not as validated claims. Section 9 handles the formal falsifiability argument, including the testable claim that "Model Update Objects reduce repeated mistakes more effectively than ordinary postmortems."

Do not present MUOs as proven effective in Section 6. Present them as the framework's proposed solution, with Section 9 defining how they could be tested.

---

## Visual Plan

### Figure 5: Learning Is Model Change

Existing SVG: `fig5_learning_is_model_change.svg`

Argumentative job: Show the learning sequence as a causal loop that closes the gap between action and updated reasoning.

The figure should show:

```
Expectation -> Action -> Outcome -> Prediction Error ->
Investigation -> Evidence-Supported Explanation ->
Model Update -> Changed Future Optimizer State / Perceived Topography
```

The final node should show that learning changes both optimizer state AND topography — the update reshapes the landscape for future motion.

Side distinctions the figure may include or that the surrounding prose should make clear:

- Storage =/= Learning
- Reaction =/= Learning
- Correction =/= Learning
- Postmortem =/= Learning (unless it produces a model update)

Place Figure 5 after the learning sequence is fully explained and before the "where does the learning go?" movement.

### Figure 6: Reasoning Architecture — Six Objects

Existing SVG: `fig6_reasoning_architecture_six_objects.svg`

Argumentative job: Show how the six reasoning objects form a chain that preserves the full state transition.

Evaluate whether Figure 6 belongs in Section 6 or Section 8.

**Recommendation:** If Section 6 introduces the six objects conceptually (even briefly), Figure 6 belongs in S6. If the six objects are fully deferred to S8, Figure 6 belongs there instead.

The v1.0 outline places both fig5 and fig6 in S6. This is appropriate if the six objects receive at least a brief conceptual introduction (one paragraph naming them and their chain relationship) before the full specification is deferred to S8.

### Optional Table

Possible table role: distinguish learning from non-learning organizational responses.

| Event or artifact | What changed | Does it count as learning? | Why or why not? |
| --- | --- | --- | --- |
| Corrected output | One answer was fixed | No | The model that produced the error was not updated |
| Stored outcome | The result was recorded | No | No expectation was compared; no investigation occurred |
| Retrospective narrative | A story about what happened was written | Not automatically | Unless it identifies prediction error, investigates with evidence, and produces a bounded model update |
| Blanket restriction | A category of behavior was removed | No | Behavior changed without identifying which specific condition mattered |
| Evidence-supported interpretation update | The audience model was revised based on outcome data | Yes | Expectation compared, mismatch investigated, evidence identified, model changed |
| Durable bounded model update | A reusable record preserves the lesson with boundary and confidence | Yes | The learning is represented so it can reshape future reasoning |

**Recommendation:** Include this table. It has a distinct argumentative job from Figure 5. Figure 5 shows the sequence; the table distinguishes learning from its imitators. Both add comprehension.

---

## Citation Inventory

### Existing Citations

- Argyris & Schon, 1978 — single-loop vs. double-loop learning (v0.2 S8 line 1456)
- Cyert & March, 1963 — organizational learning through imperfect search (v0.2 S8 line 1456)

### Citations Requiring Verification

- None identified. Both citations are in the existing bibliography.

### Missing Citation Needs

Per the citation workstream (doctrine Section 12):

- **Organizational routines:** Feldman & Pentland, 2003 — how model updates change future behavior relates to routines as generative systems. Target: S6.
- **KM failure literature:** Markus 2001, Weber et al. 2001 — directly addresses the KM graveyard objection. Target: S6 Movement 5.
- **Case-based reasoning:** Aamodt & Plaza, 1994 — position MUO relative to existing case-based reasoning structures. Target: S6 Movement 5 or S10.
- **Agent architectures (Reflexion):** Shinn et al. 2023 — Reflexion implements a version of the learning loop. Target: S6 or S10.

### Claims That Are Framework Propositions Rather Than Empirical Claims

- "Learning is an evidence-supported model update triggered by prediction error" — framework definition, not empirical finding
- "Model Update Objects reduce repeated mistakes more effectively than ordinary postmortems" — testable claim, not yet validated (S9 handles falsifiability)
- "Reasoning-state preservation improves future agent behavior" — testable claim (S9)

---

## Theory Risks

### Learning Reduced to Storage

Risk: the reader confuses preserving a model update with learning itself. Mitigation: the "learning vs. MUO" distinction must be clear. Learning is the justified transition. The MUO is the container.

### Outcome Mistaken for Prediction Error

Risk: the reader treats a bad outcome as automatically constituting prediction error. Mitigation: prediction error requires a preserved expectation to compare against.

### Hindsight Substituted for Preserved Expectation

Risk: the organization constructs a post-hoc "expectation" after seeing the outcome. Mitigation: emphasize that the expectation must be preserved before action.

### First Explanation Mistaken for Evidence

Risk: the most convenient explanation is accepted without investigation. Mitigation: the investigation step must be emphasized as essential.

### Model Update Object Mistaken for Learning

Risk: creating a Model Update Object is treated as proof that learning occurred. Mitigation: an MUO is useful only if it contains a genuine evidence-supported model change.

### Formal Schema Introduced Too Early

Risk: presenting the full eleven-field specification before the reader understands why each field matters. Mitigation: introduce the conceptual payload in S6; defer the full specification to S8.

### Discovery Material Pulled Forward

Risk: explaining how human reasoning is elicited (the Discovery process) before Section 7. Mitigation: S6 should show that learning requires preserved reasoning. S7 should show how that reasoning is captured from humans.

### Implementation Material Pulled Forward

Risk: presenting storage architecture, lifecycle governance, or retrieval systems before Section 8. Mitigation: S6 establishes what must be preserved; S8 explains how to build the system that preserves it.

### Learning Presented as Automatic

Risk: implying that the learning loop runs without human judgment, review, or investigation. Mitigation: emphasize that investigation requires human participation, evidence requires judgment, and model updates require review.

---

## Drafting Constraints

- Define before specifying.
- Make the need for preserved expectation felt before naming prediction error.
- Keep the Section 5 callback compact (~100 words, not a replay).
- Do not replay the healthcare campaign.
- Do not treat an outcome as self-explanatory.
- Do not imply that every prediction mismatch produces valid learning.
- Do not imply that evidence automatically selects one explanation.
- Keep human investigation, review, and judgment visible.
- Do not make Model Update Objects magical memory containers.
- Do not present the complete implementation schema.
- Do not collapse learning into documentation.
- Do not collapse learning into a changed answer.
- End with the need to capture human reasoning before action, creating the bridge to Discovery (S7).

---

## Transition into Section 7

The closing bridge should be conceptually:

"Model Update Objects preserve learning after action. But reasoning must also be captured before action — from the messy intent, tacit assumptions, and organizational knowledge that humans carry but rarely make explicit. That is the work of Discovery."

Do not draft this as final prose. Treat it as the closing conceptual move.

---

## Recommended Section Length

~2,000-3,000 words.

v0.2 S8 is ~3,400 words. v0.2 S9 is ~2,200 words. v0.2 S10 is ~2,500 words. Total: ~8,100 words.

v1.0 S6 merges the essential conceptual content of all three while deferring implementation detail to S8. The target is ~2,000-3,000 words. Reader comprehension governs.

---

## Readiness Assessment

The source packet answers all ten readiness questions:

1. **What exactly counts as learning?** Evidence-supported model update triggered by prediction error.
2. **Why is a preserved expectation necessary?** Without it, prediction error cannot be identified — the organization has only outcomes and hindsight.
3. **How is prediction error different from a bad outcome?** Prediction error is the mismatch between a preserved expectation and an observed outcome. A bad outcome alone does not identify what the system expected or what should change.
4. **Why is investigation necessary?** The first explanation is often wrong. Investigation protects learning from false explanation.
5. **What makes an explanation evidence-supported?** It connects the prediction error to a plausible cause with enough support to justify updating the model. Not a guess, not a convenient story.
6. **What exactly changes in a model update?** Goal, Policy, Interpretation, or Action Model. The update must be specific enough to change behavior but bounded enough to avoid overgeneralization.
7. **How can that update reshape future topography?** By making prior learning visible, changing confidence in a signal, connecting outcomes to future decisions, altering sufficiency conditions, or reshaping which paths become easy or hard.
8. **Why is a Model Update Object not identical to learning?** Learning is the justified reasoning transition. The MUO is the durable representation through which that transition can survive and influence later reasoning.
9. **What remains for Section 7?** Discovery — how human intent, tacit knowledge, and organizational reasoning are captured before or during action.
10. **What remains for Section 8?** Implementation architecture — how the reasoning-object system is built, stored, retrieved, governed, and maintained.
