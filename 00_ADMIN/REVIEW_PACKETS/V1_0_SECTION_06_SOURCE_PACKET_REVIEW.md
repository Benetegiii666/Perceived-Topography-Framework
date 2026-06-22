# v1.0 Section 6 Source-Packet Review

---

## Reviewer 1: Theory-Coherence Review

### Pass or Concern

**Pass.**

### Conceptual Collapses Detected

None. The packet maintains all required distinctions:

| Distinction | Status |
| --- | --- |
| Outcome =/= Prediction Error | Preserved. Outcome is "evidence that learning may be needed." Prediction error requires a preserved expectation. |
| Prediction Error =/= Explanation | Preserved. "The first explanation is often wrong." Investigation is required. |
| Investigation =/= Explanation | Preserved as separate steps in the canonical sequence. |
| Explanation =/= Model Update | Preserved. Explanation identifies cause; model update changes future reasoning. |
| Learning =/= Model Update Object | Preserved explicitly. "Learning = the justified reasoning transition. Model Update Object = the bounded representation." |
| Model Update Object =/= Stored Outcome | Preserved. "Its purpose is not simply to store what happened. Its purpose is to change future reasoning." |
| Changed Output =/= Changed Model | Preserved. "A changed output is not enough. The model that shaped the output must change." |

### On the Primary Definition

The proposed definition — "Learning is an evidence-supported model update triggered by prediction error" — is precise and well-anchored.

**One qualification needed in surrounding prose, not in the definition itself:** "Triggered by" could be read as implying that prediction error automatically produces learning. The v0.2 source (line 1466) already addresses this: "But learning is not automatic." The packet's drafting constraints also state: "Do not imply that every prediction mismatch produces valid learning." The definition is fine; the prose must make clear that prediction error opens the door but investigation, evidence, and judgment must walk through it.

### Causal Sequence Audit

```
Expectation -> Action -> Outcome -> Prediction Error ->
Investigation -> Evidence-Supported Explanation ->
Model Update -> Changed Future Reasoning
```

**No missing steps.** Each has a distinct function:

- Expectation: what was believed before action
- Action: commits the model to contact with reality
- Outcome: reality's response
- Prediction Error: the mismatch (requires preserved expectation)
- Investigation: why the mismatch occurred (protects against false explanation)
- Evidence-Supported Explanation: the justified account of the mismatch
- Model Update: the change to future reasoning
- Changed Future Reasoning: the result that reshapes optimizer state and topography

**No collapsed steps.** Investigation and Explanation remain separate. Prediction Error and Outcome remain separate.

**No causal reversals detected.**

**Hindsight risk:** The packet correctly identifies this: "The organization constructs a post-hoc 'expectation' after seeing the outcome." The mitigation ("the expectation must be preserved before action") is correct.

### Premature Sufficiency Connection

The bridge — "Premature sufficiency explains why motion stopped too early. Prediction error reveals that the reasoning supporting that stopping condition did not fully match reality" — is coherent but should not overstate the connection.

**Qualification needed:** Not every prediction error traces back to premature sufficiency. An action may have been taken at appropriate sufficiency, with the outcome revealing a genuine unknown rather than a stopping error. The prose should acknowledge that prediction error can arise from appropriate action under genuine uncertainty, not only from premature sufficiency.

### Required Packet Corrections

1. **Add a prose note** that prediction error can arise from appropriate action under genuine uncertainty, not only from premature sufficiency. The Movement 1 bridge currently implies a tighter coupling than is warranted.

### Optional Improvements

- Consider adding one sentence to the canonical definitions section clarifying that "triggered by" means "made possible by," not "automatically produced by."

---

## Reviewer 2: Narrative-Architecture Review

### Pass or Concern

**Pass.**

### Strongest Planned Realization

Movement 3 (Reaction Is Not Learning) is the planned moment most likely to produce an aha response. The healthcare example ("abandon workflow-pain messaging entirely" vs. "update the audience model") and the unsafe-tool example ("remove all tools" vs. "identify the specific tool affordance") are concrete, recognizable, and diagnostic. The test — "Does the change make future reasoning more accurate under defined conditions?" — is the section's most quotable formulation.

### Weakest Planned Movement

Movement 1 (Reality Exposes the Stopping Error) is the weakest because it risks feeling like a replay of S5's ending. The packet correctly limits it to ~150 words and says "do not replay the campaign." But the opening bridge must earn its place by adding a new conceptual move (the generalization from one instance to a pattern) rather than merely recapping what the reader already knows.

**Suggested strengthening:** Movement 1 should not only recall the campaign outcome but should immediately pose the question the reader does not yet have the tools to answer: "The outcome revealed a mismatch. But what exactly was contradicted? Not the campaign itself — the campaign ran. What was contradicted was the expectation embedded in the reasoning that shaped it." This makes the transition to Movement 2 (Learning Is Model Change) feel necessary rather than sequential.

### Repetition Risks

1. The healthcare campaign callback appears in Movement 1, Movement 3, and Movement 5 (compact filled MUO example). Three appearances of the same scenario in one section is at the upper limit. Each must do genuinely different work: M1 = recall the outcome; M3 = contrast weak reaction with real learning; M5 = show the MUO as a filled object. This is manageable but requires discipline.

2. The "learning reshapes the landscape" idea appears in Movement 4 and Movement 5. The before/after example in M4 and the "MUOs reshape the landscape" conclusion in M5 must not repeat each other. M4 should show the mechanism (how update changes topography); M5 should show the container (what the MUO preserves so it can be retrieved).

### Missing Aha Moment

No missing aha moment. The five movements cover: why preservation is necessary (M1), what learning IS (M2), what learning is NOT (M3), how learning changes the future landscape (M4), and where the learning goes (M5). The arc is complete.

### Required Packet Corrections

None required for narrative architecture.

### Optional Improvements

- Movement 1 could include one sentence that explicitly states: "The outcome alone does not tell the organization what to change." This prevents the reader from assuming that a bad outcome is self-diagnosing.

---

## Reviewer 3: Section-Boundary Review

### Pass or Concern

**Pass with one note.**

### Material Correctly Retained in Section 6

- Learning definition
- Canonical learning sequence
- Preserved expectation requirement
- Prediction error
- Investigation
- Evidence-supported explanation
- Model update and update targets
- Reaction vs. learning distinction
- Postmortem vs. learning distinction
- Minimum conceptual MUO payload (eight essential fields)
- KM graveyard confrontation (brief, with pointer to S7 for the design response)
- Five most important failure modes MUOs prevent
- Figure 5 placement
- Learning reshapes future topography
- Healthcare callback (compact)
- Unsafe-tool callback (compact)

All of this is appropriate for Section 6.

### Material That Must Be Deferred to Section 7

The packet correctly defers Discovery to S7. One item requires monitoring:

**KM graveyard confrontation allocation.** The packet places the KM graveyard acknowledgment in S6 Movement 5 ("structured learning repositories have failed before") and names Discovery as the design response. This is correct conceptually: S6 names the problem; S7 delivers the solution. However, the packet also says Discovery "shifts creation burden from humans to inference" — which is a S7 claim. The S6 prose should name the problem and point to S7 for the solution without pre-explaining the mechanism.

### Material That Must Be Deferred to Section 8

The packet correctly defers:

- Full eleven-field MUO specification
- Observability Envelope
- Human-Ready View
- Lifecycle states and governance
- Storage and retrieval architecture
- Full six-object reasoning architecture specification

**One item to monitor:** The packet recommends that Figure 6 (Reasoning Architecture: Six Objects) belongs in S6 "if the six objects receive at least a brief conceptual introduction." This is reasonable, but the brief introduction must be genuinely brief — one paragraph naming the chain, not a mini-Section-10. If it exceeds one paragraph, defer Figure 6 to S8.

### Required Packet Corrections

1. **Tighten the KM graveyard passage in Movement 5.** S6 should acknowledge the problem ("structured learning objects have historically failed to achieve reuse") and point to S7 ("Section 7 addresses how reasoning capture can be designed to reduce this risk"). It should not explain the Discovery mechanism.

### Optional Improvements

- Add an explicit word budget for Figure 6's conceptual introduction: "If the six-object chain requires more than one paragraph to introduce, defer Figure 6 to Section 8."

---

## Reviewer 4: Organizational-Learning and Knowledge-Management Critic

### Pass or Concern

**Pass with required correction.**

### KM Graveyard Risk

The packet correctly identifies the risk and proposes confronting it. However, the current allocation is slightly misplaced.

**Current allocation in the packet:**
- S6 Movement 5: Acknowledge the graveyard risk, name Discovery as the response, acknowledge secondary risk (AI-inferred objects may be wrong).

**Recommended allocation:**
- S6: Acknowledge the problem. "Structured learning repositories — lessons-learned databases, postmortem libraries, case repositories — have historically achieved low adoption and low reuse. The Model Update Object does not escape this risk merely by being better-structured."
- S6: Name the design response without explaining it: "The framework's answer is that reasoning objects should not require humans to author them from scratch. That mechanism — Discovery — is the subject of the next section."
- S7: Deliver the Discovery mechanism as the full design response.
- S8: Deliver lifecycle, retrieval, and governance as the operational defenses.

This allocation is cleaner than having S6 explain "Discovery shifts creation burden from humans to inference," which is S7's conceptual contribution.

### Overclaim Risks

1. "A bounded, reusable record of learning whose purpose is to change future reasoning" — this is a design aspiration, not a demonstrated outcome. The prose must retain the pre-empirical framing. The packet's boundary with S9 correctly handles this.

2. The minimum MUO payload (eight essential fields) is presented as necessary. The packet should note that in practice, some fields may be partially inferred or incomplete, and the system should degrade gracefully rather than requiring all eight fields before the object is useful.

### Human-Governance Requirements

The packet correctly lists "learning presented as automatic" as a theory risk and states that "investigation requires human participation, evidence requires judgment, and model updates require review." This is sufficient if it survives into the prose.

### What Must Be Stated in Section 6

- Learning is not storage.
- Model Update Objects can be wrong, stale, overgeneralized, or politically distorted.
- Human judgment is required at the investigation and explanation stages.
- The MUO is a proposed design concept, not a proven solution.

### What Should Be Deferred

- The full Discovery mechanism -> S7
- Lifecycle governance -> S8
- Retrieval architecture -> S8
- Formal falsifiability of MUO effectiveness -> S9

### Required Packet Corrections

1. **Add a note** that the minimum MUO payload should degrade gracefully: not all fields must be complete for the object to be useful. A partially filled MUO is better than no preserved reasoning at all. This prevents the reader from treating eight fields as a gate rather than a target.

### Optional Improvements

- Add one sentence acknowledging that model updates can be politically distorted or organizationally convenient rather than evidence-supported. This strengthens intellectual honesty.

---

## Reviewer 5: Visual-Argument Review

### Pass or Concern

**Pass.**

### Figure 5 Recommendation

The proposed sequence is correct:

```
Expectation -> Action -> Outcome -> Prediction Error ->
Investigation -> Evidence-Supported Explanation ->
Model Update -> [Final Node]
```

**Exact final-node wording recommendation:** "Changed Future Reasoning" is the clearest single formulation. It is more general than "Changed Optimizer State" (which omits topography changes) and more precise than "Changed Future Topography" (which omits goal/policy/interpretation changes). The prose should clarify that "changed future reasoning" includes both optimizer state and perceived topography.

Alternatively: "Updated Optimizer State and Reshaped Topography" — more precise but longer.

**Recommendation:** Use "Changed Future Reasoning" in the figure. Use the prose to explain that this includes changes to optimizer state (Goal, Policy, Interpretation) and perceived topography (what becomes visible, accessible, represented, trusted, connected).

**Loop back:** The figure should show an arrow from the final node back to "Expectation" to indicate that the updated reasoning state generates new expectations for the next cycle. This closes the loop visually.

### Side-Contrast Recommendation

Add "Correction =/= Learning" to the side contrasts. The full set should be:

- Storage =/= Learning
- Correction =/= Learning
- Reaction =/= Learning
- Postmortem =/= Learning (unless it produces a model update)

These can appear as side labels or footnotes in the figure, or in prose immediately surrounding it. All four are important because they represent the most common organizational substitutes for actual learning.

### Table Recommendation

**Include the table.** It has a distinct argumentative job from Figure 5:

- Figure 5 shows the causal sequence of learning.
- The table shows which common organizational responses count as learning and which do not.

These are different questions. The figure answers "how does learning work?" The table answers "is this thing I already do actually learning?"

**One refinement:** The "Does it count as learning?" column should not be strictly binary. The current packet uses "No," "Not automatically," and "Yes." This is appropriate. Consider using:

| Classification | Meaning |
| --- | --- |
| No | This does not constitute learning in the framework's sense |
| Not automatically | This could become learning if it includes investigation, evidence, and model update |
| Yes | This meets the framework's definition of learning |

### Table Placement

Place the table **after** Movement 3 (Reaction Is Not Learning) and **before** Movement 4 (Learning Reshapes Future Topography). At that point, the reader has understood both what learning IS (M2) and what it is NOT (M3). The table crystallizes the distinction before the section moves to how learning changes the landscape (M4).

Do not place it after Movement 5 (where the MUO is introduced) because by then the reader's attention has shifted from "what counts as learning" to "where does the learning go."

### Required Packet Corrections

None required for visuals.

### Optional Improvements

- Specify that Figure 5 should include a loop-back arrow from the final node to Expectation.
- Add "Correction =/= Learning" to the side-contrast list.

---

## Cross-Reviewer Synthesis

### Agreements

All five reviewers agree on:

1. The packet preserves all required conceptual distinctions. No collapses detected.
2. The five-movement structure is sound and produces a coherent reader journey.
3. The canonical definition ("Learning is an evidence-supported model update triggered by prediction error") should be preserved.
4. The Section 6/7/8 boundaries are correctly drawn with minor tightening needed.
5. The healthcare and unsafe-tool callbacks are appropriately compact.
6. The optional table adds a distinct argumentative job and should be included.
7. Figure 5 should include a loop-back to Expectation.
8. The KM graveyard risk must be acknowledged in S6 but the Discovery mechanism belongs in S7.

### Disagreements

No genuine disagreements among reviewers. The following are tensions resolved through allocation:

| Tension | Resolution |
| --- | --- |
| KM graveyard: S6 or S7? | S6 names the problem; S7 delivers the solution. S6 should not pre-explain the Discovery mechanism. |
| Figure 6 placement: S6 or S8? | S6 if one-paragraph introduction; S8 if longer. Budget: one paragraph maximum. |
| MUO payload detail: how much in S6? | Eight conceptual fields in S6. Full eleven-field specification in S8. |

### Required Corrections Before Drafting

| # | Issue | Why it matters | Smallest sufficient correction | Location in packet | Authorial approval |
| --- | --- | --- | --- | --- | --- |
| 1 | Movement 1 implies all prediction error traces to premature sufficiency | Prediction error can arise from appropriate action under genuine uncertainty, not only stopping errors. | Add one sentence to Movement 1 plan: "Prediction error can also arise when an action was taken at appropriate sufficiency but reality revealed a genuine unknown. Not every learning event begins with a failure of motion." | Five-Movement Narrative Plan, Movement 1 | No |
| 2 | KM graveyard passage pre-explains Discovery mechanism | "Discovery shifts creation burden from humans to inference" is S7's claim, not S6's. | Revise Movement 5 to: acknowledge the graveyard problem, state that the framework's design response is addressed in the next section, and acknowledge the secondary risk that AI-inferred reasoning objects may be inaccurate. Do not explain the RIPC mechanism. | Five-Movement Narrative Plan, Movement 5 | No |
| 3 | Minimum MUO payload presented as all-or-nothing | A partially filled MUO is better than no preserved reasoning. The eight fields should be a target, not a gate. | Add one sentence to Minimum Model Update Object Payload section: "Not all fields must be complete for the object to be useful. A partially filled model update that preserves the prediction error and a bounded explanation is better than no preserved reasoning at all." | Minimum Model Update Object Payload, Essential in Section 6 | No |

### Optional Improvements

1. Movement 1: add "The outcome alone does not tell the organization what to change."
2. Figure 5: add loop-back arrow from final node to Expectation.
3. Figure 5: add "Correction =/= Learning" to side contrasts.
4. Figure 5: use "Changed Future Reasoning" as the final-node wording; explain in prose that this includes both optimizer state and topography.
5. Table: place after Movement 3, before Movement 4.
6. Figure 6: set a one-paragraph budget for the six-object introduction; defer Figure 6 to S8 if it exceeds that budget.
7. Add one sentence acknowledging that model updates can be politically distorted or organizationally convenient.

### Protected Concepts

These must survive into the drafted prose:

1. "Learning is an evidence-supported model update triggered by prediction error."
2. "A bad outcome is not learning. A correction is not learning. A reaction is not learning. A postmortem is not necessarily learning."
3. "Does the change make future reasoning more accurate under defined conditions?"
4. "Narrative memory can be read. Model updates can be reused."
5. "Where does the learning go?"
6. "Its purpose is not simply to store what happened. Its purpose is to change future reasoning."
7. "Learning reshapes the landscape."
8. Learning =/= Model Update Object (the transition vs. the container)

### Material Explicitly Deferred

| Material | Deferred to | Reason |
| --- | --- | --- |
| Discovery mechanism (RIPC loop) | S7 | S7's primary responsibility |
| Full MUO eleven-field specification | S8 | Implementation detail |
| Observability Envelope | S8 | Governance/operational |
| Human-Ready View specification | S8 | Usability layer detail |
| Lifecycle states and governance | S8 | Implementation detail |
| Full six-object architecture specification | S8 | Implementation detail |
| Storage and retrieval architecture | S8 | Implementation detail |
| Formal falsifiability of MUO effectiveness | S9 | Validation/testing |
| KM graveyard design response (how Discovery addresses it) | S7 | S7's contribution |

### Final Verdict

**PASS WITH REQUIRED PACKET CORRECTIONS**

Three corrections are required before drafting. All are small (one sentence each). None require authorial approval. No conceptual architecture changes are needed. The five-movement structure is sound. The section boundaries are correctly drawn. The visual plan is appropriate. The packet is ready for drafting after the three corrections are applied.
