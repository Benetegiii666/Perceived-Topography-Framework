# v1.0 Section 6 Outside-Draft Review

---

## Reviewer Pass 1: Voice and Self-Reference

### Self-References Found

| # | Exact phrase | Line/location | Problem | Smallest concept-forward replacement | Required or optional |
| --- | --- | --- | --- | --- | --- |
| 1 | "In Section 4, sufficiency described where motion stops." | **Known pre-identified concern.** Not present in the draft as provided — the draft already uses the revised concept-forward version: "Action begins when motion stops." | Already corrected. | N/A — the fix is already in. | N/A |
| 2 | "the prior section's stress test" | Not found in the draft. | N/A | N/A | N/A |
| 3 | "The campaign stress test" | Paragraph beginning "This is where the campaign stress test becomes more than an example." | Minor — "stress test" is a concept label established in the S5 heading, not a manuscript self-reference. | No change needed. "Stress test" is the name of the exercise, not a reference to a section. | Optional |
| 4 | "The healthcare campaign did not merely produce an outcome." | Opening sentence. | Not a self-reference — it refers to the scenario, not the manuscript. | No change needed. | N/A |

**Verdict: Pass.** The draft contains no manuscript self-references. The known "In Section 4" issue has already been replaced with concept-forward language. No instances of "this section," "prior section," "next section," "as described earlier," or "as shown above" appear in argumentative prose. The closing bridge ("That problem is Discovery.") is concept-forward, not section-forward.

### Required Corrections

None.

### Optional Improvements

None.

---

## Reviewer Pass 2: Theory Coherence

### Pass or Concern

**Pass.**

### Conceptual Collapses Detected

None. All required distinctions are maintained:

| Distinction | Draft status | Evidence |
| --- | --- | --- |
| Outcome =/= Prediction Error | Preserved | "An outcome is not self-explanatory." "A result can be favorable, unfavorable, surprising, ambiguous, or misleading. None of those qualities automatically makes it learning." |
| Prediction Error =/= Explanation | Preserved | "But even prediction error is not yet learning. It is the signal that learning may be needed." |
| Investigation =/= Explanation | Preserved | Investigation and explanation appear as separate steps in the sequence. "The organization must still investigate the mismatch, develop an evidence-supported explanation..." |
| Explanation =/= Model Update | Preserved implicitly | The explanation identifies the cause; the model update states the change. The MUO payload lists both as separate fields. |
| Learning =/= Model Update Object | Preserved explicitly | "Learning is the justified reasoning transition. A Model Update Object is the representation that allows that transition to survive and influence later reasoning." |
| Model Update Object =/= Stored Outcome | Preserved | "It is not a magical memory container. It is not the same as a postmortem." |
| Changed Output =/= Changed Model | Preserved explicitly | "Correction changes the immediate object. Learning changes the future reasoning that would otherwise reproduce the error." |
| Correction =/= Learning | Preserved explicitly | Full subsection. |
| Reaction =/= Learning | Preserved explicitly | Full subsection with both weak-reaction and learning-response examples. |
| Postmortem =/= Learning | Preserved explicitly | Full subsection. |
| Storage =/= Learning | Preserved explicitly | Full subsection. |

### Definition Assessment

The primary definition — "Learning is an evidence-supported model update triggered by prediction error" — appears in the draft and is well-protected by surrounding prose.

**"Triggered by" automaticity risk:** Adequately mitigated. The draft states: "But even prediction error is not yet learning. It is the signal that learning may be needed. The organization must still investigate the mismatch, develop an evidence-supported explanation, identify what should change, and preserve that change so it can influence future reasoning." This makes clear that prediction error is necessary but not sufficient.

**Preserved expectation as logically necessary:** Yes. "That question cannot be answered reliably unless the prior expectation was preserved." The draft makes this the hinge of the argument.

**Investigation as necessary before explanation:** Yes. "The first explanation is often wrong" is implied through the investigation subsection's detailed questions. The draft asks: "Which consequence was invisible? ... Was the failure caused by missing information, weak connectivity, poor representation, misplaced confidence, or an absent escalation affordance?" These are investigation questions, not explanation.

**Not every bad outcome is prediction error:** Yes. The draft says: "A result can be favorable, unfavorable, surprising, ambiguous, or misleading. None of those qualities automatically makes it learning."

**Not every prediction error produces valid learning:** Yes. The draft says: "Not every learning event begins as premature sufficiency. Sometimes the prior action was well justified and reality simply changed."

### Definitions Requiring Protection

All seven protected formulations from the source-packet review are present:

1. "Learning is an evidence-supported model update triggered by prediction error." — Present.
2. The "not learning" litany — Present as subsection structure rather than a single sentence. The function is preserved.
3. "Does the change make future reasoning more accurate under defined conditions?" — Not present verbatim. The function is covered by "Correction changes the immediate object. Learning changes the future reasoning that would otherwise reproduce the error." **Minor wording risk** — consider restoring the precise test.
4. "Narrative memory can be read. Model updates can be reused." — Not present verbatim. **Minor wording risk** — this is one of v0.2's strongest formulations. Consider restoring.
5. "Where does the learning go?" — Not present as a standalone question. The concept is preserved through the "Where the learning goes" subsection heading, but the punchy question form is lost. **Minor wording risk.**
6. "Its purpose is not simply to store what happened. Its purpose is to change future reasoning." — Present: "A Model Update Object is a bounded, reusable record of learning whose purpose is not simply to store what happened, but to change future reasoning."
7. "Learning reshapes the landscape." — Present implicitly through the "Learning changes future topography" subsection. The exact formulation is not used, but the concept is fully developed.

### Required Corrections

None required for theory coherence.

### Optional Improvements

1. Restore "Narrative memory can be read. Model updates can be reused." — This formulation from v0.2 S8.9 (line 1650) is one of the paper's most compact and memorable contrasts. It would strengthen the postmortem subsection.
2. Restore "Does the change make future reasoning more accurate under defined conditions?" — This is the v0.2 reaction-vs-learning test (S8.8 line 1632). The draft's "Correction changes the immediate object. Learning changes the future reasoning..." is strong but the test question adds diagnostic value.

---

## Reviewer Pass 3: Older-Version Preservation

### Disposition Matrix

| Original realization | Earliest location | Current draft disposition | Risk classification |
| --- | --- | --- | --- |
| Learning is not correction | v0.1/v0.2 S8 | Preserved explicitly (full subsection) | No concern |
| Learning is not a postmortem | v0.1/v0.2 S8.9 | Preserved explicitly (full subsection) | No concern |
| Learning is not an outcome | v0.1/v0.2 S8.3 | Preserved explicitly ("An outcome is not self-explanatory") | No concern |
| Learning requires prediction error | v0.1/v0.2 S8.4 | Preserved explicitly | No concern |
| Prediction error requires preserved expectation | v0.1/v0.2 S8.1 | Preserved explicitly and made the hinge of the argument | Strengthened |
| Investigation protects against convenient explanation | v0.1/v0.2 S8.5 | Preserved explicitly (investigation subsection with diagnostic questions) | Strengthened |
| Learning is an evidence-supported model update | v0.1/v0.2 S8 line 1454 | Preserved explicitly as the primary definition | No concern |
| The model update must change future behavior | v0.1/v0.2 S8.7 | Preserved explicitly ("Learning changes the future reasoning that would otherwise reproduce the error") | No concern |
| Stored lessons can become KM graveyard artifacts | v0.1/v0.2 S9 line 1767; reviewer feedback | Preserved explicitly ("The point is not to create a better archive") | No concern |
| A Model Update Object preserves the learning transition | v0.1/v0.2 S9 | Preserved explicitly | No concern |
| A Model Update Object is not the same as learning | Source packet distinction | Preserved explicitly ("Learning is the justified reasoning transition. A Model Update Object is the representation...") | No concern |
| A Model Update Object requires scope, confidence, and applicability boundary | v0.1/v0.2 S9.3 | Preserved. Payload listed. Graceful degradation acknowledged. | No concern |
| Reasoning architecture must preserve why a decision changed | v0.1/v0.2 S10 | Deferred intentionally — the six-object reasoning architecture is not introduced in the draft | Intentional and appropriate deferral |
| Ten failure modes MUOs prevent | v0.1/v0.2 S9.7 | Compressed. Not named as a numbered list, but the key modes (folklore, overgeneralization, stale updates, confidence inflation, political distortion) are addressed in prose. | Appropriate compression |
| "Narrative memory can be read. Model updates can be reused." | v0.2 S8.9 line 1650 | Missing verbatim | Minor wording risk |
| "Does the change make future reasoning more accurate under defined conditions?" | v0.2 S8.8 line 1632 | Missing verbatim | Minor wording risk |
| Figure 5: Learning Is Model Change | v0.2 S8.13 line 1741 | Described inline as a text figure; SVG placement will be needed at insertion | No concern |
| Before/after topography change examples | v0.2 S8.12 lines 1719-1727 | Preserved and expanded through the five-dimension walkthrough | Strengthened |

### Missing or Weakened Original Insights

Two v0.2 formulations are missing verbatim but their function is preserved through other language. Both are optional restorations, not required corrections.

### Original Material Intentionally Deferred

- Six-object reasoning architecture (v0.2 S10) — correctly deferred to S8
- Full MUO eleven-field specification (v0.2 S9.3) — correctly deferred to S8
- Observability Envelope (v0.2 S9.4) — correctly deferred to S8
- Human-Ready View (v0.2 S9.5) — correctly deferred to S8
- Lifecycle states (v0.2 S9.4) — correctly deferred to S8
- Figure 6 (Reasoning Architecture: Six Objects) — correctly deferred to S8

### Any Old Material That Should Remain Out of Section 6

- The parallel campaign and safety learning walkthroughs (v0.2 S8.10-S8.11) are correctly retired as standalone subsections. The draft uses compact callbacks instead. Appropriate.

---

## Reviewer Pass 4: Boundary with Sections 7 and 8

### Pass or Concern

**Pass.**

### Material Correctly Retained in Section 6

- Learning definition and canonical sequence
- Preserved expectation requirement
- Prediction error
- Investigation
- Evidence-supported explanation
- Model update and update targets
- All five "not learning" distinctions (outcome, correction, reaction, postmortem, storage)
- Minimum conceptual MUO payload
- KM graveyard acknowledgment
- Learning reshapes future topography (five-dimension walkthrough)
- Figure 5 (text placeholder)
- Table 5
- Human judgment requirement
- Graceful degradation of MUO payload
- Healthcare campaign callback (compact)
- Unsafe-tool callback (compact)
- Bridge to Discovery

### Material to Defer to Section 7

The draft correctly avoids explaining Discovery. The closing paragraph names Discovery as "that problem" without explaining the mechanism. The RIPC loop is not mentioned. This is correct.

**One note:** The draft mentions "Discovery" by name only in the final sentence. This is appropriate. S7 owns the concept.

### Material to Defer to Section 8

The draft correctly avoids:

- Full MUO schema
- Observability Envelope
- Human-Ready View specification
- Lifecycle states
- Storage and retrieval architecture
- Six-object reasoning architecture
- Governance controls
- Figure 6

**One item to monitor:** The MUO payload list in the draft (ten fields) is slightly longer than the source packet's "essential in Section 6" list (eight fields). The draft includes "update target" and "action and context" as separate named fields. This is acceptable because they are mentioned conceptually in prose, not specified as formal schema.

### Required Corrections

None.

### Optional Improvements

None.

---

## Reviewer Pass 5: Narrative Architecture

### Pass or Concern

**Pass.**

### Strongest Movement

**"Correction is not learning."** The formulation "Correction changes the immediate object. Learning changes the future reasoning that would otherwise reproduce the error" is the draft's best single sentence. It is precise, memorable, and diagnostic. It should be protected during any cleanup.

### Weakest Movement

**"Storage is not learning."** This subsection is accurate but somewhat repetitive with the postmortem subsection. Both make the point that organizational artifacts can exist without changing future behavior. The storage subsection adds the list of alternative interpretations (audience wrong, creative weak, channel underperformed, etc.) which is useful, but the subsection overall runs ~300 words where ~150 would suffice.

### Repetition Risks

1. **Healthcare campaign appears in:** opening callback, "Learning is not the outcome" subsection, reaction-vs-learning example, postmortem-vs-learning example, MUO filled example, and five-dimension walkthrough. Six appearances total. Each does different work, but the cumulative effect in a single section is dense. Consider whether the postmortem example could use a brief non-campaign illustration to reduce campaign fatigue.

2. **"Not learning" phrasing** appears as subsection headings for correction, reaction, postmortem, and storage. This is structurally intentional and works well as a diagnostic litany. The repetition is functional, not redundant.

3. **"Future reasoning" appears frequently** (>10 times). This is a core concept and the repetition is appropriate, but the draft could vary the formulation occasionally ("future optimizer state," "later decision-making," "subsequent action") to prevent monotony.

### Missing Aha

No missing aha. The progression from "outcome is not learning" through the five distinctions to "where the learning goes" is complete. The strongest aha is the correction-vs-learning distinction. The bridge to Discovery is earned.

### Required Corrections

None required for narrative architecture.

### Optional Improvements

1. Compress the "Storage is not learning" subsection by ~50%. The alternative-interpretation list (audience wrong, creative weak, etc.) is useful but could be shortened.
2. Consider one non-campaign example in the postmortem subsection to reduce campaign saturation.

---

## Reviewer Pass 6: Visual and Table Argument

### Figure 5

The draft includes a text-formatted sequence as a placeholder for Figure 5:

```
Prior expectation → Action → Outcome → Prediction error →
Investigation → Evidence-supported explanation →
Model update → Changed future reasoning →
loop back to: Future expectations, gradients, investigation, and sufficiency conditions
```

**Sequence:** Correct. All steps present. No missing or collapsed steps.

**Final node:** "Changed future reasoning" is clear. The loop-back to "Future expectations, gradients, investigation, and sufficiency conditions" is explicit and correctly closes the loop.

**Learning opportunity vs. completed learning:** The prose surrounding the figure makes this distinction ("But even prediction error is not yet learning"). The figure itself does not need to distinguish them.

**Side contrasts:** Not included in the text placeholder. The source-packet review recommended including Storage =/= Learning, Correction =/= Learning, Reaction =/= Learning, Postmortem =/= Learning as side labels. The draft achieves this through subsection structure instead. Both approaches are valid. The SVG can include side labels at authorial discretion.

**Recommendation:** The text figure is adequate as a placeholder. The final SVG should include the loop-back arrow and may include side contrasts.

### Table 5

**Table 5. Not Every Change Is Learning**

| Check | Assessment |
| --- | --- |
| Distinct argumentative job from Figure 5? | Yes. Figure shows sequence; table distinguishes learning from imitators. |
| "Learning status" column too binary? | No — the draft uses "Not yet learning," "Reaction," "Learning," and "Reusable learning" rather than binary yes/no. This is better than the source packet's proposal. |
| Rows accurate? | Yes. All six rows correctly reflect the prose. |
| "Durable bounded model update" wording | Acceptable. The "reusable learning" status label makes the distinction clear. |
| "Stored outcome" and "retrospective narrative" overlap? | Minor overlap. Both are "not yet learning." However, they represent genuinely different organizational artifacts (a data record vs. a narrative account), so both rows are justified. |
| Table placement | Correct. Appears after all five "not learning" subsections and before "Learning changes future topography." This is the source-packet review's recommended placement. |

**Recommendation:** Table 5 is well-constructed and well-placed. No changes needed.

### Figure 6

Figure 6 (Reasoning Architecture: Six Objects) does not appear in the draft. The six-object architecture is not introduced. This is consistent with the source-packet review's guidance: defer Figure 6 to S8 unless the six objects receive a one-paragraph introduction.

**Recommendation:** Correct as-is. Figure 6 belongs in S8.

### Required Corrections

None.

### Optional Improvements

None.

---

## Reviewer Pass 7: Reader-Comprehension and Style

### Pass or Concern

**Pass with cleanup notes.**

### Best Paragraph

"Correction changes the immediate object. Learning changes the future reasoning that would otherwise reproduce the error."

This two-sentence paragraph is the draft's strongest moment. It is precise, quotable, and diagnostic. Protect it.

### Paragraphs Needing Cleanup

1. **"Storage is not learning" subsection.** Runs ~300 words. The list of alternative interpretations ("Did the campaign fail because workflow pain was irrelevant? Because the call to action was weak? Because the audience was too broad?...") asks seven questions. Four would suffice. The subsection makes its point before it finishes.

2. **"Learning changes future topography" subsection.** The five-dimension walkthrough (Visibility, Accessibility, Representation, Confidence, Connectivity applied to the campaign update) is valuable but runs ~350 words. Each dimension gets its own paragraph beginning "It can change **Visibility**..." This is effective but could be compressed into a more flowing passage if length is a concern.

### Sentences That Should Be Cut or Compressed

1. "The same pattern appears in ordinary organizational work. A leader may correct a slide. A lawyer may revise a sentence. A product manager may update a requirement. A support lead may rewrite a response." — Four examples where two would suffice. Cut to two.

2. "Did the campaign fail because workflow pain was irrelevant? Because the call to action was weak? Because the audience was too broad? Because the offer attracted researchers rather than buyers? Because the buying committee was different from expected? Because the channel reached administrators but not decision-makers? Because the clinical claim boundary made the message less dramatic but more trustworthy?" — Seven questions. Cut to four.

### Sentences That Should Be Made More Concrete

None identified. The draft is consistently concrete throughout.

### Claims That Need Qualification

1. "A Model Update Object is a bounded, reusable record of learning whose purpose is not simply to store what happened, but to change future reasoning." — This is appropriately framed as a design goal, not a proven outcome. No additional qualification needed.

### Required Corrections

None required for comprehension.

### Optional Improvements

1. Compress the organizational-correction examples from four to two.
2. Compress the alternative-interpretation questions from seven to four.
3. Minor: vary "future reasoning" phrasing occasionally to reduce repetition.

---

## Cross-Reviewer Synthesis

### Required Corrections Before Insertion

**None.** The draft passes all seven reviewer passes without any required corrections. The known "In Section 4" self-reference has already been replaced with concept-forward language. All conceptual distinctions are preserved. Section boundaries are respected. The theory is coherent. The visual and table arguments are sound.

### Optional Improvements

| # | Improvement | Location | Impact | Authorial approval |
| --- | --- | --- | --- | --- |
| 1 | Restore "Narrative memory can be read. Model updates can be reused." | Postmortem subsection | Restores one of v0.2's strongest compact formulations | Optional — authorial preference |
| 2 | Restore "Does the change make future reasoning more accurate under defined conditions?" | Reaction subsection, near the test | Restores the v0.2 diagnostic test | Optional — authorial preference |
| 3 | Compress organizational-correction examples from four to two | Correction subsection | Saves ~30 words | Optional |
| 4 | Compress alternative-interpretation questions from seven to four | Storage subsection | Saves ~40 words, tightens pace | Optional |
| 5 | Vary "future reasoning" phrasing occasionally | Throughout | Reduces mild monotony | Optional |
| 6 | Consider one non-campaign example in postmortem subsection | Postmortem subsection | Reduces campaign saturation | Optional |

### Protected Language

These formulations must survive cleanup:

1. "Learning is an evidence-supported model update triggered by prediction error."
2. "An outcome is not self-explanatory."
3. "What did reality contradict?"
4. "Correction changes the immediate object. Learning changes the future reasoning that would otherwise reproduce the error."
5. "A weak reaction says: ... A learning response says: ..."
6. "The point is not to create a better archive."
7. "A partial lesson is not useless. It is less governable."
8. "Learning is the justified reasoning transition. A Model Update Object is the representation that allows that transition to survive and influence later reasoning."
9. "It is not a magical memory container."
10. "The organization repaired the answer without changing the conditions that generated it."
11. "That problem is Discovery."
12. Table 5 title: "Not Every Change Is Learning"

### Material Explicitly Deferred

| Material | Deferred to | Confirmed absent from draft |
| --- | --- | --- |
| Discovery mechanism (RIPC loop) | S7 | Yes — only named in final sentence |
| Full MUO eleven-field specification | S8 | Yes — only conceptual payload listed |
| Observability Envelope | S8 | Yes |
| Human-Ready View | S8 | Yes |
| Lifecycle states | S8 | Yes |
| Six-object reasoning architecture | S8 | Yes — not introduced |
| Figure 6 | S8 | Yes |
| Storage and retrieval architecture | S8 | Yes |
| Formal falsifiability of MUO effectiveness | S9 | Yes |

### Final Verdict

**PASS — ready for insertion after minor cleanup.**

The draft is conceptually sound, narratively coherent, and properly bounded. All required distinctions are preserved. No conceptual collapses, no boundary drift, no manuscript self-references, no overclaims. The six optional improvements are quality refinements, not structural requirements. The draft can be inserted into the working manuscript after authorial cleanup at the author's discretion.

---

## No-Edit Confirmation

- **Draft edited:** No
- **Source packet edited:** No
- **Source-packet review edited:** No
- **Manuscript edited:** No
- **Rewrite queue edited:** No
- **v0.1 edited:** No
- **v0.2 edited:** No
- **Concept architecture edited:** No
- **References edited:** No
- **Figures or SVGs edited:** No
- **Release files edited:** No
- **SESSION_START.md edited:** No
