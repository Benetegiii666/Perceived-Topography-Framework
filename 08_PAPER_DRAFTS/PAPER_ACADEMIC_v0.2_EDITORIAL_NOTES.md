# PAPER_ACADEMIC_v0.2 — Editorial Notes

Extracted from `PAPER_ACADEMIC_v0.1.md` during v0.1 to v0.2 manuscript conversion.

---

## Title Block Metadata (removed from v0.2)

**Alternative title:** From Context to Reasoning State: Perceived Topography as a Framework for Human-Agent System Design

**Version:** Academic v0.1 — Scaffold only
**Date:** 2026-06-24
**Status:** Section scaffold with intent notes and placeholders. No full prose drafted.
**Source:** Derived from frozen keystone paper `PAPER_v1.0_WORKING.md`. The frozen paper remains conceptual authority. This academic version may compress, restructure, and formalize but may not silently alter core framework concepts.
**Boundary rule:** If the academic conversion reveals a conceptual conflict with the frozen paper, HLD, or build artifacts, document it as a fault line under Protocol #1 rather than resolving it silently.

---

## Abstract

**Status:** Accepted — v0.2
**Review status:** Accepted. All 5 pass criteria met. Voice 4/5, 2 minor AI flags (0 severe). Hostile reviewer: no basis for rejection.

---

## Epistemic Status

**Status:** Accepted — v0.1 with fix applied
**Review status:** Accepted. All 6 pass criteria met. Voice 4/5, 0 severe AI flags. Hedging qualifier cut. Construct inventory compressed.

---

## Section 1: Introduction

**Status:** Accepted — v0.3 with review notes applied
**Review status:** Accepted per `SECTION_1_REVIEW_v0.3_2026-06-24.md`. All 5 pass criteria met. Three review notes applied: premature sufficiency genealogy (Simon 1955), Lynch/Yao citation split, contribution enumeration varied.
**Prior versions:** v0.1 (27 AI flags, Voice 2/5), v0.2 (11 AI flags, Voice 3.5-4/5), v0.3 (5 AI flags, Voice 4/5). Reviews: `SECTION_1_REVIEW_2026-06-24.md`, `SECTION_1_REVIEW_v0.2_2026-06-24.md`, `SECTION_1_REVIEW_v0.3_2026-06-24.md`.

**Citation note:** Three anchoring citations added per v0.2 review guidance. Full citation treatment in Section 2.

**Scaffold intent notes (retained for review reference):**

**Source:** ChatGPT v0.3 draft, provided by Benet 2026-06-24.

**v0.2 → v0.3 changes applied:**

- Roadmap compressed from 10 template sentences to one sentence
- Context/reasoning-state triplet reduced to one strong policy example + architectural framing
- Three citation anchors added: [Lynch et al., 2025; Yao et al., 2023], [Lewis et al., 2020], [Walsh and Ungson, 1991; Markus, 2001]
- Containment catalog reduced from 6 items to 4
- Context catalog restructured into flowing prose ("documents, policies, and prior examples")
- Bounding paragraph compressed from three "It does not claim" sentences to one semicolon-joined sentence
- Reasoning-state list restructured ("The system should retain..." instead of "That state includes...")
- "preserve state" replaces "remember prior interactions" in opening (more precise)
- Closing question remains as final rhetorical beat (after compressed roadmap)

**Elements preserved from v0.2:**

- Marble/slope metaphor
- "This paper proposes that we can describe that landscape" thesis one-liner
- "A model does not need inner malice to cause harm" (frozen paper wording restored)
- First-person "I" for optimizer definition
- "The contribution is not the claim that system design matters" preemption
- Four-contribution enumeration
- Bounding paragraph (compressed)
- Five-dimension introduction with "minimum viable diagnostic set"
- Premature sufficiency introduction
- Organizational learning paragraphs
- Agentic acceleration paragraph
- Closing question

---

## Section 2: Related Work and Theoretical Positioning

**Status:** Accepted — v0.2 with Su et al. 2025 reference resolved
**Review status:** Accepted per `SECTION_2_REVIEW_v0.2_2026-06-24.md`. All pass criteria met. Su et al. 2025 blocking citation resolved. Bibliography backlog (12 entries) remains for pre-submission.
**Prior versions:** v0.1 (Voice 3/5, 8 AI flags), v0.2 (Voice 4/5, 0 AI flags). Reviews: `SECTION_2_REVIEW_v0.1_2026-06-24.md`, `SECTION_2_REVIEW_v0.2_2026-06-24.md`.

**Scaffold intent notes:**

**Source:** ChatGPT v0.2 draft, provided by Benet 2026-06-24. Revised from v0.1 per Section 2 Review.

**v0.1 → v0.2 changes applied:**

- Opening rewritten: claim-first instead of field-mapping
- "This section positions that claim against the literature" cut
- Reflection/self-critique engagement added (Reflexion, Self-Refine) with PTF distinction (cross-cycle vs. within-trajectory)
- Horvitz (1999) added to 2.4 (mixed-initiative interaction)
- Endsley (1995) added to 2.4 with PTF/SA distinction (design-theoretic vs. descriptive)
- Section 2.4 retitled to "Affordances, Situation Awareness, and Human-Agent Interaction"
- Safety subsection retitled to "AI Safety, Alignment, and Agentic Risk"
- RLHF citations added (Christiano 2017, Ouyang 2022)
- Constitutional AI added (Bai et al. 2022)
- Ji et al. 2023 (alignment survey) added
- Deng et al. 2024 removed (unresolvable reference)
- Su et al. 2025 retained (autonomy-induced security risks)
- Simon (1955) added to 2.7 with bounded rationality framing
- 2.7 rewritten: "the contribution is the blend rather than the grapes" restored from frozen paper voice
- 2.7 patterned six-sentence list replaced with flowing prose
- Subsection openings revised to lead with claims (2.1, 2.3, 2.4, 2.5)
- "PTF also draws from..." and "The framework also inherits from..." patterns eliminated
- "This matters for agentic systems because..." pattern eliminated

**New citations in v0.2 (not in v0.1):**
- Shinn et al., 2023 (Reflexion)
- Madaan et al., 2023 (Self-Refine)
- Endsley, 1995 (already in frozen bibliography)
- Horvitz, 1999 (already in frozen bibliography)
- Christiano et al., 2017
- Ouyang et al., 2022
- Bai et al., 2022
- Ji et al., 2023 (already in frozen bibliography)
- Simon, 1955 (already in frozen bibliography)

**Citations needing full reference entries (not in frozen bibliography):**
- Schick et al., 2023 (Toolformer)
- Park et al., 2023 (Generative Agents)
- Liu et al., 2024 (AgentBench)
- Zhou et al., 2024 (WebArena)
- Jimenez et al., 2024 (SWE-bench)
- Xie et al., 2024 (OSWorld)
- Xu et al., 2024 (TheAgentCompany)
- Shinn et al., 2023 (Reflexion)
- Madaan et al., 2023 (Self-Refine)
- Christiano et al., 2017 (RLHF)
- Ouyang et al., 2022 (InstructGPT)
- Bai et al., 2022 (Constitutional AI)
- Su et al., 2025 (autonomy-induced security risks)

---

## Section 3: From Context to Reasoning State

**Status:** Accepted — v0.2
**Review status:** Accepted. All 6 pass criteria met. 8/8 v0.1 notes addressed. Voice 4/5, 4 AI flags (0 severe).
**Prior versions:** v0.1 (Voice 4/5, 7 flags). Reviews: `SECTION_3_REVIEW_v0.1_2026-06-24.md`.

**Scaffold intent notes:**

**Source:** ChatGPT v0.2 draft, provided by Benet 2026-06-24. Revised from v0.1 per Section 3 Review notes.

**v0.1 → v0.2 changes applied:**

- Four-part structure justified ("They are not exhaustive; Section 6 develops the fuller architecture")
- Reasoning state defined as both condition and transition (reconciling justification vs. transition framing)
- Patterned "First...Second...Third...Fourth..." list varied ("The first is... The second is... A third element is... Finally...")
- Reasoning-state alternative shown in healthcare example (evidence boundary active, sufficiency rationale records the distinction, unsupported claim flagged)
- Lee (1997) added for design rationale systems
- Simon (1955) added for satisficing/stopping conditions
- Weick (1995) added for "learning becomes storytelling" / retrospective sensemaking
- Single-loop / double-loop learning named explicitly with Argyris & Schon
- "Consider a healthcare marketing workflow" setup sentence cut
- "That question prepares the framework's next move" setup sentence cut
- Fourth restatement of context/reasoning-state distinction removed ("This gives reasoning state a different role from context" kept; earlier duplicate cut)
- Closing bridge rewritten without formulaic transition

---

## Section 4: Perceived Topography — Definitions and Dimensions

**Status:** Accepted — v0.2
**Review status:** Accepted. All 6 pass criteria met. 7/7 v0.1 fixes resolved. Voice 4/5, 2 minor AI flags.
**Prior versions:** v0.1 (Voice 4/5, 5 flags). Reviews: `SECTION_4_REVIEW_v0.1_2026-06-25.md`.

**Scaffold intent notes:**

**Source:** ChatGPT v0.2 draft, provided by Benet 2026-06-25. Revised from v0.1 per Section 4 Review.

**v0.1 → v0.2 changes applied:**

- Citations added: Gibson 1979, Norman 1988, Kuhlthau 1991, Simon 1955 in opening; Endsley 1995 for Visibility/situation-awareness; Simon 1955 in admission rule discussion
- "Exert force" defined explicitly: "behavioral influence on what the system notices, investigates, trusts, selects, withholds, or escalates"
- Visibility/Accessibility boundary defended: "A Visibility failure means the signal was never presented. An Accessibility failure means the signal was known or knowable, but reaching it was too costly, blocked, slow, or outside the available path."
- Optimizer state formally defined with three primitives (Goal, Policy, Interpretation) — resolves cross-section definition gap
- "Topography failure" definition revised to avoid forward-dependency on "sufficient" — now says "before action occurs"
- "This section defines..." setup sentence cut
- "These definitions are deliberately practical" → "These definitions are practical" (cut empty intensifier)
- "The dimensions are easiest to understand through failure" setup sentence cut
- Closing rewritten: "But structure alone does not explain movement" replaces formulaic preview paragraph
- "sufficient" replaced with "action-ready" in gradient definition and tool-use example to avoid overloading Section 5's territory
- "exert force" replaced with "influence behavior/reasoning/action" in several instances where the phrase was becoming repetitive

**Elements preserved from v0.1:**
- Information-surfaces-are-not-topography distinction
- Five dimensions with diagnostic table
- Dimension admission rule with four candidate discussions
- Healthcare claims-repository diagnostic walkthrough
- Tool-use diagnostic example
- Policy/memory treatment as non-promoted candidates
- All core definitions

---

## Section 5: Gradients, Motion, and Premature Sufficiency

**Status:** Accepted — v0.2
**Review status:** Accepted. All 6 pass criteria met. 8/8 v0.1 items resolved. Voice 4/5, 0 moderate/severe AI flags.
**Prior versions:** v0.1 (Voice 4/5, 6 flags, 4 required changes). Reviews: `SECTION_5_REVIEW_v0.1_2026-06-25.md`.

**Scaffold intent notes:**

**Source:** ChatGPT v0.2 draft, provided by Benet 2026-06-25. Revised from v0.1 per Section 5 Review.

**v0.1 → v0.2 changes applied:**

- Gradient/attraction distinction restored: "A gradient is a property of the landscape, not of the optimizer... The optimizer's response to that gradient is attraction. The slope does not move itself."
- Gradient defended against alternatives in dedicated paragraph: affordance (action possibility), bias (systematic distortion), nudge (deliberate intervention) vs. gradient (directional condition, designed or accidental)
- Action-attraction / exploration-attraction pair restored: "Action attraction points toward doing... Exploration attraction points toward uncertainty reduction"
- Premature sufficiency given design-time criterion: "before the information surfaces designed to govern that action have become behaviorally effective"
- Design-time criterion explained with falsifiability argument: "A designer should be able to say in advance..."
- Model-internal hallucination causes acknowledged: "This account does not replace model-level explanations of hallucination such as training-data distribution, decoding behavior, or attention patterns"
- Closing rewritten: ends on diagnostic question "What made this path feel sufficient?" — no formulaic section preview
- "This distinction matters because..." setup sentence cut
- "This paper calls that pressure a gradient" naming ceremony cut — gradient introduced through heading and definition
- "That question leads to the central failure pattern" naming ceremony cut
- "This is the core movement:" cut — sequence stands alone
- "That is a better exit from motion" cut
- "Again, the better behavior is not paralysis" → "Better behavior is not paralysis" (cut "Again")
- One healthcare-example pass removed (the post-sufficiency dimension-list paragraph)
- "Designing against premature sufficiency therefore means" → removed "therefore"

**Elements preserved from v0.1:**
- Opening: "A landscape does not explain behavior until something moves through it"
- "The system does not simply 'choose badly.' It moves through a shaped field."
- Four-moment motion model (A-I-S-A) with non-prescriptive bounding
- "Adjacent truth is not sufficient support"
- Hallucination/tool-use comparison with explicit structural-similarity bounding
- Healthcare and operations examples
- "I do not know" / "I should not act yet" as action affordances
- Counterpressure design paragraph
- All citations preserved

**Forward connection:** Section ends on the diagnostic question. Section 6 opens with the architectural response.

---

## Section 6: Reasoning-State Architecture

**Status:** Accepted — v0.2
**Review status:** Accepted. All 6 pass criteria met. 10/10 v0.1 notes resolved. Voice 5/5, 0 AI flags. Citations: 8 (up from 2). Table 7 reinstated.
**Prior versions:** v0.1 (Voice 4/5, 3 minor flags, 10 notes). Reviews: `SECTION_6_REVIEW_v0.1_2026-06-25.md`.

**Scaffold intent notes:**

**Source:** ChatGPT v0.2 draft (patched per v0.1 review notes), applied by Claude 2026-06-25.

**Structural relationship to frozen paper:** Combines and compresses material from frozen paper Sections 6 (Learning), 7 (Discovery), and 8 (What It Would Take to Build This). Discovery separated into Section 7.

**v0.1 → v0.2 changes applied (10 patches):**

1. Citation support added in opening (Simon 1955, Lee 1997)
2. Agent memory/reflection distinction paragraph added (Park 2023, Shinn 2023, Madaan 2023)
3. Pirolli & Card 1999 citation added in Investigation Trace
4. Post-action Investigation Trace acknowledged
5. Temporal distinction added: Optimizer State = starting frame, Decision State = pre-action snapshot
6. Table 7 (Minimum Viable Reasoning Objects) reinstated after 6.6
7. Walsh & Ungson 1991 citation added in 6.7
8. External controls reaffirmation added in 6.8
9. Three AI voice fixes applied (cut setup clauses, cut empty transition)
10. Forward references added to Sections 9 and 10

**Citation count: v0.1 had 2 citations. v0.2 has 8** (Simon, Lee, Park, Shinn, Madaan, Weick, Argyris & Schon, Pirolli & Card, Walsh & Ungson).

**Table 7:** Reinstated. Table 8 (Maturity Model) deferred to Section 10 with forward reference.

**Forward connection:** Section ends with the claim that reasoning-state architecture lets context become reusable judgment + forward reference to Section 10 maturity model. Section 7 addresses how reasoning state is captured before action through Discovery.

---

## Section 7: Discovery and Human Confirmation

**Status:** Accepted — v0.2
**Review status:** Accepted. All 5 pass criteria met. 7/7 v0.1 fixes resolved. Voice 4/5, 0 AI flags. Frozen paper closing restored.
**Prior versions:** v0.1 (Voice 3.5-4/5, 6 flags, 7 required changes). Reviews: `SECTION_7_REVIEW_v0.1_2026-06-25.md`.

**Scaffold intent notes:**

**Source:** ChatGPT v0.2 draft, provided by Benet 2026-06-25. Revised from v0.1 per Section 7 Review.

**v0.1 → v0.2 changes applied:**

- "Discovery is not better intake. It is pre-action topography design." restored from frozen paper (v0.1 note #2)
- Closing rewritten: formulaic S8 preview replaced with frozen paper's "Discovery gives architecture something worth carrying. Architecture gives Discovery somewhere durable to go." Design test bolded as final rhetorical beat before closing. (v0.1 note #1)
- Amershi et al. 2019 cited in mixed-initiative paragraph (v0.1 note #4)
- Forward reference to S9 added after Discovery failure list (v0.1 note #5)
- Material-uncertainty filtering acknowledged as a design problem: "But deciding which uncertainties are material is itself a design problem" (v0.1 note #6)
- Anchoring risk acknowledged: "The propose step can anchor the human toward the system's interpretation. That is a real limitation of propose-then-confirm patterns." (v0.1 note #7)
- AI voice fixes applied:
  - "This connects Discovery to mixed-initiative interaction" setup sentence cut — mixed-initiative integrated into flowing prose
  - Formulaic closing cut — replaced with frozen paper closing
  - "Discovery also protects against automation bias" → rewritten as "It also has to manage automation bias"
  - "These risks matter because Discovery is not inherently good" → cut; failure modes speak for themselves
  - "The exact wording will vary by domain and interface" → compressed to "The wording will vary"
  - "The key is that Discovery should focus on material uncertainty" → "Discovery should focus on material uncertainty"

**Elements preserved from v0.1:**
- "The risk is not that the system infers. The risk is that it preserves or acts from the inference as if it had been confirmed." → adapted to "The danger begins when the inference hardens before the human has seen it."
- "Guesswork has become architecture"
- "Human confirmation is not magic. It is evidence within scope."
- "A confirmation without scope can become a new source of premature sufficiency."
- Blank-form burden vs. silent inference
- Five Discovery failure modes
- Healthcare example as proposed Optimizer State
- RIPC loop
- Provenance requirement

**Forward connection:** Closing bridges to S8 through the final line about architecture and Discovery needing each other.

---

## Section 8: Constructed Stress Test — Healthcare Marketing Campaign

**Status:** Accepted — v0.2
**Review status:** Accepted. All 5 pass criteria met. 9/9 v0.1 fixes resolved. Voice 5/5, 0 AI flags. Methodology grounded (Hevner, Siggelkow). Straw-man closed.
**Prior versions:** v0.1 (Voice 5/5, 2 minor flags, 9 required changes). Reviews: `SECTION_8_REVIEW_v0.1_2026-06-25.md`.

**Scaffold intent notes:**

**Source:** ChatGPT v0.1 draft, provided by Benet 2026-06-25.

**Structural relationship to frozen paper:** Draws from frozen paper Section 5 ("A Constructed Stress Test: The Healthcare Campaign"). The academic version is compressed (~30-40% shorter than frozen Section 5) and more explicitly methodological. The frozen paper's healthcare scenario spans two full sections (Section 5 for the stress test, with callbacks throughout Sections 6-8). The academic version consolidates the stress test into one section.

**Key elements preserved:**
- "Reduces readmissions" as the key failure point
- Same-assignment / same-artifact design
- Context-only vs. reasoning-state comparison
- Adjacent truth formulation
- Correction is not learning
- Bounded progress (not refusal)
- What survives the campaign (final row of comparison table)
- Workflow-burden as attention signal, not buying-readiness signal (MUO)
- Clinical-claim boundary preserved across campaigns
- Constructed scenario framing (not empirical validation)

**Compression from frozen paper:**
- Frozen Section 5 was ~5,000 words. This draft is ~2,800 words (~44% reduction).
- Frozen paper repeated the healthcare example across Sections 5, 6, 7, and 8. The academic version concentrates it here with brief callbacks in S3, S5, and S7.
- The frozen paper's extended "three-column comparison" with context-only / reasoning-state / next-cycle learning is compressed into a single comparison table (8.5) plus a post-campaign subsection (8.6).
- The frozen paper's "Start small, stay credible" and maturity model content is deferred to Section 10.

**New elements not in frozen paper:**
- "The framework now needs to do work" — opening frames the section's purpose directly
- 8.7 "What the Stress Test Shows" — explicit enumeration of what the stress test demonstrates (different diagnosis, different intervention, different memory object, useful motion)
- "The goal is not validation. It is examinability." — compressed epistemic framing
- "Those objections are welcome. A framework that cannot be challenged cannot become useful." — closing

**v0.1 → v0.2 changes applied (9 required fixes):**

1. Methodology citations added: Hevner et al. 2004, Siggelkow 2007
2. "Author-constructed" stated explicitly
3. "Stress test" defined as applied here
4. Context-only fairness sentence added in 8.3
5. Learning claim qualified: "illustrated in shape, not proven"
6. Argyris & Schon 1978 cited at "correction is not learning"
7. "Adjacent truth" defined as a construct
8. "That distinction matters because" cut from 8.2
9. "That is enough for a constructed stress test" cut from 8.7

**Citation count: v0.1 had 0. v0.2 has 3** (Hevner, Siggelkow, Argyris & Schon).

**Forward connection:** Section closes with an invitation to challenge. Section 9 (Boundaries, Objections, and Disconfirmation Conditions) is the natural response.

---

## Section 9: Boundaries, Objections, and Disconfirmation Conditions

**Status:** Accepted — v0.2
**Review status:** Accepted. All 7 pass criteria met. 7/7 v0.1 fixes resolved. Voice 5/5, 0 AI flags. Unfalsifiability confronted. Disconfirmation conditions tightened. "Does not claim" negations restored.
**Prior versions:** v0.1 (Voice 4-5/5, 2 minor flags, 7 required changes). Reviews: `SECTION_9_REVIEW_v0.1_2026-06-25.md`.

**Scaffold intent notes:**

**Source:** ChatGPT v0.1 draft, provided by Benet 2026-06-25.

**Structural relationship to frozen paper:** Draws from frozen paper Section 9 ("Boundaries, Objections, and Falsifiability"). The academic version reorganizes the material into eight subsections: claim boundary, four named objections with responses, overhead/proportionality, disconfirmation conditions, and closing. The frozen paper's Table 9 (Disconfirmation Conditions) is converted from a table into a numbered list with fuller prose treatment of each condition. The frozen paper's risk inventory (false precision, authority conflict, surveillance, staleness, policy laundering, automation bias, metaphor drift) is distributed across the objection subsections rather than presented as a separate list.

**Key elements preserved:**
- "The argument should be allowed to lose" opening stance
- Not every failure is a topography failure
- Boundary conditions for framework applicability
- "Good system design" objection with honest concession + distinction
- Human confirmation is not magic / evidence within scope
- Reasoning-state objects as new attack surface
- Organizational risks (procedural theater, authority laundering, political hardening, overgeneralization)
- Seven disconfirmation conditions (expanded from frozen paper's six in Table 9)
- Overhead/proportionality concern
- Diagnostic discipline as the surviving value
- "A framework that cannot fail is not worth much"

**New elements not in frozen paper:**
- 9.3 explicitly distinguishes PTF from retrieval, memory, and reflection (separate from "good system design" objection)
- 9.5 cites Su et al. 2025 for agentic risk landscape
- 9.6 introduces proportionality and maturity model forward reference
- Disconfirmation condition #7 (user routing-around as failure signal) is new
- Closing diagnostic question list maps to five dimensions + premature sufficiency + learning loop

**Forward connection:** Section closes with "A framework that can fail in clear ways can become a research program." Section 10 (Research Agenda) is the natural next step.

---

## Section 10: Research Agenda and Evaluation Methods

**Status:** Accepted — v0.3
**Review status:** Accepted. All pass criteria met. Voice 5/5, 0 AI flags. All v0.2 additions resolved. March 1991 reference entry needed in bibliography.
**Prior versions:** v0.1 (Voice 4/5, 7 changes), v0.2 (Voice 5/5, 4 additions). Reviews: `SECTION_10_REVIEW_v0.1_2026-06-25.md`, `SECTION_10_REVIEW_v0.2_2026-06-25.md`.

**Scaffold intent notes:**

**Source:** ChatGPT v0.2 draft, provided by Benet 2026-06-25. Rewritten with new framing ("stress-testing the framework" rather than "research agenda and evaluation methods").

**v0.1 → v0.2 changes applied:**

- Title changed from "Research Agenda and Evaluation Methods" to "Research Agenda: Stress-Testing the Framework"
- Opening rewritten: "The next step is not to protect the framework. It is to stress test it." replaces the old opening
- Framing shifted from formal methodology to invitation: "These are invitations" rather than "The agenda below focuses on six evaluation families"
- "The useful research program is plural rather than grand" cut (v0.1 AI voice flag)
- Symmetrical tricolon "Together, these methods ask whether..." rewritten (v0.1 AI voice flag)
- Subsection titles rewritten as action verbs ("Compare..." "Perturb..." "Test..." "Evaluate...") rather than noun phrases ("Reasoning-State Preservation Studies")
- RQ list removed as separate subsection — the subsections themselves serve as the research questions
- Instrumentation subsection (10.7 in v0.1) removed — governance-of-measurement content distributed into 10.7 (misuse) and the closing
- Adversarial evaluation (RQ7) gets its own subsection (10.7) — resolves v0.1 asymmetry
- Context-only baseline sharpened in 10.1 — acknowledges that the answer may be no
- Maturity model framing tightened: "not a standard to impose" + "provisional" + "a way to ask better questions"
- Closing rewritten: "The invitation is not to accept the framework. The invitation is to put it under pressure."

**Key elements preserved from v0.1:**
- Central question (reasoning state vs. context-only)
- Six core evaluation directions (comparative, perturbation, sufficiency detection, Discovery, MUO quality, maturity)
- Table 8 (maturity model, six levels, fit-based)
- MUO transfer + restraint evaluation
- Premature sufficiency as design-time testable
- Discovery vs. alternatives (silent inference, blank-form, literal execution)
- Negative results valued
- Citations: Hevner, Lakatos, Amershi, Lee & See, Argyris & Schon, Walsh & Ungson

**Notable changes from v0.1:**
- Four-outcome sufficiency table removed (appropriate/premature/over-delayed/blocked) — prose treatment in 10.3 covers the same ground more fluidly
- MUO quality rubric table removed — the evaluation questions in 10.5 cover the same criteria in prose
- Formal RQ list (RQ1-7) removed as a separate subsection — each subsection IS the research question
- Instrumentation subsection removed — content on governance cost and sensitive data preserved in closing and 10.7

**Forward connection:** "A useful framework does not need to win everywhere." Section 11 (Conclusion) follows.

---

## Section 11: Conclusion

**Status:** Accepted — v0.2
**Review status:** Accepted. All 7 pass criteria met. Voice 4/5 (up from 2/5). 2 minor AI flags (down from 14). All 3 severe flags eliminated.
**Prior versions:** v0.1 (Voice 2/5, 14 flags, 3 severe). Reviews: `SECTION_11_REVIEW_v0.1_2026-06-25.md`.

**Scaffold intent notes:**

**Source:** ChatGPT v0.2 draft, provided by Benet 2026-06-25. Rewritten per v0.1 review (14 AI flags, Voice 2/5).

**v0.1 → v0.2 changes applied:**

- Cut entirely: two glossary re-enumeration paragraphs (Flags 6, 7), five "may" hedging sentences (Flag 8), "Those risks do not make the framework weak. They make it serious." (Flag 9), "The reason to do that work is that the pattern keeps appearing." (Flag 10), "That condition is not created by the model alone." (Flag 2), "The core argument is simple:" prefix (Flag 4), "The practical implication is direct." (Flag 12)
- Rewritten: tradition list grouped into clusters instead of 10-item flat enumeration (Flag 5); seven-item verb-object list compressed to three concrete examples (Flag 1); five failure-pattern sentences rewritten with varied grammar — some concrete, one names a specific scenario (Flag 11); balanced hedge restructured to state position first (Flag 13); diplomatic qualifier in closing replaced with direct claim (Flag 14)
- Word count: ~850 → ~500 (41% reduction)
- The seven questions preserved exactly
- "That is why the framework has legs" preserved
- "It does not explain everything. It should not try." preserved
- Closing line preserved

**Title:** "The Ground Beneath Action" — preserved from v0.1.

**Forward connection:** Final section. Closes with the paper's central design claim.

---

## References / Citation Backlog

**Status:** Bibliography audit completed 2026-06-25. All entries verified. 14 orphan entries removed. 17 new entries added. Citation years standardized (conference year preferred over arXiv year). Full audit: `BIBLIOGRAPHY_AUDIT_2026-06-25.md`.

---

## Figures

**Status:** Placeholder — to be determined.

**Figure 8** (workshop control console / hero asset) is locked and should not be modified.

Figures from v1.0 that should be adapted or preserved for the academic version:

| Figure | Content | Disposition |
|---|---|---|
| Fig 1 | Fear to landscape design | Adapt for academic tone |
| Fig 2 | Context vs. reasoning state | Preserve — strong |
| Fig 3 | Optimizer in topography | Preserve |
| Fig 4 | Motion and premature sufficiency | Preserve |
| Fig 5 | Learning is model change | Preserve |
| Fig 6 | Runtime Discovery loop | Preserve |
| Fig 7 | Reasoning architecture: six objects | Preserve — essential |
| Fig 8 | Workshop control console (hero) | Locked — do not modify |

---

## No-Edit Confirmation (moved from manuscript body)

- Frozen paper (`PAPER_v1.0_WORKING.md`) edited: **No**
- Figure 8 modified: **No**
- Figures modified: **No**
- References modified: **No** (existing references copied for reference; new citations added to backlog only)
- Executive Brief v1.0 edited: **No**
- Build Discovery Guide v1.0 edited: **No**
- HLD v1.0 content edited: **No**
- Core framework concepts altered: **No** (all concepts preserved per Required Preservation list)

---

## v0.2 Conversion Notes

**Voice fixes applied during v0.1 → v0.2 extraction:**

1. **"That distinction matters because"** — appeared 3 times in manuscript prose (lines 180, 414, 767). Kept two strongest instances (S2.2 benchmark failure diagnosis, S4 "information was available" challenge). Cut from S6.6 by letting the following sentence lead directly.

2. **Full five-dimension enumeration** — appeared 7 times. Kept in Abstract (S0), S4.2 definition, S9.10 diagnostic list, S11 closing. Replaced with "the five dimensions" in S1 (introduction), S2.7, S9.1, S9.9 (disconfirmation #2), S10.2.

3. **"That is the" / "That is why" capstone sentences** — appeared 8 times. Kept strongest instances: "That is the gap between context and reasoning state" (S3), "That is the role of a reasoning-state architecture" (S6), "That is the difference between a reusable campaign and a reusable lesson" (S8.5), "That is the space this framework names" (S11), "That is why the framework has legs" (S11). Varied or cut in S2.4, S3 ("That is the difference between producing an artifact..."), S10.5.

4. **Section 6 object count** — Changed "six core objects" to "six core reasoning-state objects and one loop-closing state" to account for Modified Optimizer State (7th entry in Table 7).

5. **Multi-agent sentence** — Added to end of S2.1 per instruction.

6. **Second-domain diagnostic** — Added to S10.1 per instruction.

7. **Wu et al. 2023** — Added to bibliography alphabetically.
