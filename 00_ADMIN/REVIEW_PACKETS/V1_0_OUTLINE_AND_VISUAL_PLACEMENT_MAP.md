# v1.0 Outline and Visual Placement Map

## Purpose

This artifact proposes a v1.0 section structure that preserves the complete standalone theory arc while compressing repetition. It maps existing SVGs and new visual candidates to proposed sections, confirms minimum arc coverage, and lists compression hypotheses and open editorial questions.

**Planning sources:**

- `V1_0_REWRITE_DOCTRINE_AND_WORKPLAN.md`
- `V1_0_REVIEW_RESPONSE_PLAN.md`
- `PAPER_v0.2.md` (frozen, not edited)
- Existing SVG figure assets

---

## Proposed v1.0 Section Structure

```
1.  From Agent Fear to Landscape Design
2.  Context Does Not Preserve the Why
3.  Optimizer State and Perceived Topography
4.  Gradients, Sufficiency, and Failure
5.  A Constructed Stress Test: The Healthcare Campaign
6.  Learning Requires Preserved Reasoning
7.  Discovery Turns Human Intent Into Reusable Reasoning
8.  What It Would Take to Build This
9.  Boundaries, Objections, and Falsifiability
10. The Blend Has Roots
11. Build Better Landscapes
Appendix A: The Decision Topography Interview
References
```

**v0.2 had 17 sections + Appendix A + References. v1.0 proposes 11 sections + Appendix A + References.**

The reduction comes from merging sections with overlapping conceptual responsibility, not from cutting arc steps. Every arc step is preserved; repeated derivation is consolidated.

---

## Section Map

| Proposed v1.0 section | Arc responsibility | Current v0.2 source sections | Existing SVG placement | New visual/table candidate | What gets retained | What gets compressed | What gets deferred | Risk / watch item |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **1. From Agent Fear to Landscape Design** | Fear -> wrong question -> better question -> marble analogy -> pre-empirical framing | S1 (lines 13-77), S2 (lines 80-155) | **fig1** (Fear to Landscape, line 36) | Full-framework loop (optional, or place before conclusion) | Marble analogy. Containment-vs-landscape reframe. Core term orientation (optimizer, topography, gradient, reasoning state — folded inline). Pre-empirical status statement. Elevator thesis. | S2 glossary removed as standalone section; 5 core terms folded inline into S1. "Terms That Arrive Later" subsection removed (terms appear where active). Containment discussion trimmed ~20%. | Full term glossary format. Defensive "what these terms are not" prose. | Folding terms inline must not sacrifice clarity. Reader must still grasp optimizer, topography, gradient, reasoning state, sufficiency before S2. Test: can a cold reader state the thesis after S1? |
| **2. Context Does Not Preserve the Why** | Context is not reasoning state -> documents preserve artifacts but not transitions -> the gap | S3 (lines 156-347) | **fig2** (Context vs Reasoning State, line 247) | -- | Full section. Strongest section per 4/6 reviewers. Campaign first introduction (healthcare example grounded here). "Appears to have memory but behaves as if it does not." | Minimal compression. This section is already well-calibrated. | -- | Do not compress. This is the paper's foundation. |
| **3. Optimizer State and Perceived Topography** | Optimizer state (goal, policy, interpretation) -> five topography dimensions -> dimension defense | S4 (lines 348-628), S5 (lines 629-937) | **fig3** (Optimizer in Topography, line 657) | **Dimension admission matrix** (replaces S5.7, S5.8, and defensive prose) | Goal/Policy/Interpretation definitions. Five dimension definitions (Visibility, Accessibility, Representation, Confidence, Connectivity). Diagnosis-to-intervention mapping (S5.11). Dimension admission matrix. Affordances bridge. | S4.5 "Three Primitives Are Enough" cut to one paragraph. S5.7 "Relevance Depends on Goal" and S5.8 "Policy Shapes the Boundary" replaced by admission matrix. Campaign walkthroughs in S4 and S5 reduced to bridge sentences. Safety re-illustrations trimmed (covered in S4). | Full defensive argumentation for excluded primitives. Multiple campaign re-derivations. | Merging S4 and S5 is the biggest structural change. Must preserve the transition from "what the optimizer brings" to "what the landscape provides." The merge must not blur the optimizer/topography distinction. |
| **4. Gradients, Sufficiency, and Failure** | Gradients -> motion stages -> sufficiency vs certainty -> premature sufficiency -> hallucination/harmful-action parallel -> compliance example | S6 (lines 938-1213), S7 (lines 1214-1441) | **fig4** (Motion and Premature Sufficiency, line 1296) | **Premature sufficiency comparison table** (hallucination path vs harmful action path, side-by-side) | Gradient concept. Attraction/Investigation/Sufficiency/Action stages (compressed). Sufficiency-vs-certainty 2x2 (preserve). Premature sufficiency as unified diagnostic. "Reduces readmissions" compliance example (Case A). Case B unsafe tool action. "I don't know" and "I should not act yet" need a path. | S6 attraction/investigation subsections trimmed. Campaign walkthroughs in S6 reduced to bridges. S7.1-S7.3 structural exposition compressed (replaced partly by comparison table). S7.7 "Same Shape Different Stakes" compressed. | Full motion-stage taxonomy detail. Repeated safety re-illustrations. | Must preserve the sufficiency-vs-certainty distinction and the premature sufficiency argument. These are the paper's most original contributions. The merge of S6+S7 must maintain the logical flow: gradients create motion -> sufficiency stops motion -> premature sufficiency = failure. |
| **5. A Constructed Stress Test: The Healthcare Campaign** | Full end-to-end trace: context-only path vs reasoning-state path vs next-cycle learning | S12 (lines 2481-2686), with elements drawn from campaign passages in S3-S11 | -- | **Healthcare worked-simulation trace table** (context-only vs reasoning-state vs next-cycle, columnar) | Constructed-scenario framing language. End-to-end trace showing the full framework in action. Learning loop outcome. What changes on the next cycle. | Narrative re-walk (S12) restructured as trace table with commentary paragraphs. Replaces 10+ scattered campaign walkthroughs across S4-S11. | Additional domain examples. Full multi-domain case series. | This is where the example doctrine is enforced. The trace table must show the framework producing different diagnoses than a context-only approach. If the table does not clearly demonstrate the framework's value-add, the paper loses its most important evidence substitute. |
| **6. Learning Requires Preserved Reasoning** | Learning is not memory or reaction -> prediction error -> evidence-supported model update -> Model Update Objects -> reasoning architecture | S8 (lines 1442-1758), S9 (lines 1759-1972), S10 (lines 1973-2216) | **fig5** (Learning Is Model Change, line 1741), **fig6** (Reasoning Architecture: Six Objects, line 2022) | -- | Reaction-vs-learning distinction. Prediction error as trigger. Seven-step learning loop. MUO concept, eleven-field spec, ten failure modes, one filled example. Six reasoning objects (compressed). KM graveyard confrontation (new prose). | S8 campaign learning walkthrough reduced to brief illustration. S8.10-S8.11 (parallel campaign/safety learning examples) converted to compact format. S9 campaign MUO example kept; surrounding narrative trimmed. S10 six-object taxonomy compressed (reduce per-object table format). S10 campaign/safety walkthroughs reduced to bridges. | Full MUO lifecycle governance. Retrieval UX design. Schema versioning. Detailed reasoning-object field specifications. | Merging S8+S9+S10 is aggressive. Must preserve three distinct moves: (1) what learning IS, (2) how lessons become objects, (3) what architecture preserves the full transition. The KM graveyard confrontation is new prose that adds length; it must be concise. |
| **7. Discovery Turns Human Intent Into Reusable Reasoning** | Discovery Framework -> Retrieve-Infer-Propose-Confirm -> "do the reasoning work before asking the user" -> Discovery Pattern Update | S11 (lines 2217-2480) | **fig7** (Runtime Discovery Loop, line 2297) | -- | Discovery principle. RIPC loop. Correctable inference over blank interrogation. Discovery Pattern Update concept. "Better RAG + better prompts" objection response (new prose, placed here or in S2). | Campaign walkthroughs in S11 reduced to bridges. | Full Discovery implementation detail. Extended interaction-design patterns. | Must preserve the Discovery principle and the RIPC loop. The "better RAG" objection response should be concise (1 paragraph). |
| **8. What It Would Take to Build This** | Implementation bridge -> maturity model -> "Do Not Start With the Whole Machine" | S13 (lines 2687-2903) | -- | **Implementation bridge / architecture map** (layered diagram replacing component prose) | Maturity model (Stage 0-4). "Do Not Start With the Whole Machine" advice. Architecture map (new visual). | Component table and JSON schema removed from body (moved to appendix or deferred). Prose-heavy implementation detail compressed. | Full JSON schema. Component table detail. Detailed lifecycle management. Platform integration patterns. API contracts. | Register-shift problem must be resolved. This section should read as "here is what building this would require" not as a product spec. The architecture map visual should carry the structural information that the component prose currently carries. |
| **9. Boundaries, Objections, and Falsifiability** | Falsifiable claims -> validation levels -> per-object "earn its place" -> unfalsifiability risk response -> "just good systems engineering" response -> "dimensions are arbitrary" response | S14 (lines 2904-3179) | -- | -- | Six testable claims. Explicit falsifiers. Validation levels. Per-object earn-its-place table. Unfalsifiability risk acknowledgment (new prose, or expanded from S14.13). "Just good systems engineering" response (new prose). | Validation study design detail trimmed (deferred to academic track). | Full empirical validation design. Inter-rater reliability study. Comparative study protocol. | Objection responses add new prose. Must be concise. This section should feel like honest self-assessment, not defensive argumentation. |
| **10. The Blend Has Roots** | Intellectual lineage -> what is borrowed -> what is synthesized -> "blend not invention" | S15 (lines 3180-3369) | -- | **Related-work lineage table** (tradition -> contribution -> what this paper adds -> key citation) | "Blend, not invention" posture. "Over-cite by design" principle. Lineage table (new visual, replaces 18 subsections). Brief commentary on the synthesis claim. | 18 subsections compressed to lineage table + 2-3 paragraphs of commentary. | Deep engagement with every tradition. Exhaustive per-tradition positioning. | Must preserve intellectual honesty without exhausting the reader. The lineage table format must carry enough information that an academic reviewer sees the lineage is real. |
| **11. Build Better Landscapes** | Forward-looking implications -> what changes in practice -> final statement | S16 (lines 3370-3517), S17 (lines 3518-3673) | -- | **Full-framework loop** (if not placed in S1) | 3-5 genuinely new implications (not recap). One forward-looking closing move. Full-framework loop diagram. | S16 recap subsections cut (anything that restates body arguments). S17 section-by-section recap removed. Combined section targets ~800-1,000 words (down from ~2,500). | -- | Must end with force, not fatigue. The conclusion should make the reader want to act, not feel they have already heard everything. |
| **Appendix A: The Decision Topography Interview** | Practical starting point -> 23 questions -> 4 phases | Appendix A (lines 3674-4298) | -- | **Minimal interview variant** (8-10 question subset table) | Full 23-question interview. Three-part structure. Four phases. Closing note. | Minimal compression. Add brief facilitation guidance (who, how long, what to bring). Add minimal-interview variant table. | Full facilitation workbook. Workshop curriculum. Diagnostic canvases. | Appendix A should remain usable without reading the full paper. Any additions (facilitation guidance, minimal variant) must be brief. |
| **References** | Bibliography | References (lines 4299-4369) | -- | -- | All existing citations. New citations added per citation workstream. | -- | -- | New citations must be verified. DOIs or stable URLs where available. |

---

## Existing SVG Placement Map

| SVG file | v0.2 location | v0.2 figure caption | Proposed v1.0 section | Placement rationale |
| --- | --- | --- | --- | --- |
| `fig1_fear_to_landscape.svg` | S1, line 36 | Figure 1 — From Agent Fear to Landscape Design | **S1** (From Agent Fear to Landscape Design) | Same role. Anchors the reframe visually before the argument unfolds. |
| `fig2_context_vs_reasoning_state.svg` | S3, line 247 | Figure 2 — Context Is Not Reasoning State | **S2** (Context Does Not Preserve the Why) | Same role. Visualizes the gap between context and reasoning state. S2 in v1.0 = S3 in v0.2. |
| `fig3_optimizer_in_topography.svg` | S5, line 657 | Figure 3 — Optimizer in a Perceived Topography | **S3** (Optimizer State and Perceived Topography) | Moves earlier because S4+S5 merge into S3. Figure anchors the five-dimension landscape after definitions. |
| `fig4_motion_and_premature_sufficiency.svg` | S7, line 1296 | Figure 4 — Motion and Premature Sufficiency | **S4** (Gradients, Sufficiency, and Failure) | S6+S7 merge into S4. Figure anchors the premature-sufficiency argument after the motion model. |
| `fig5_learning_is_model_change.svg` | S8, line 1741 | Figure 5 — Learning Is Model Change | **S6** (Learning Requires Preserved Reasoning) | S8+S9+S10 merge into S6. Figure anchors the learning-loop argument. |
| `fig6_reasoning_architecture_six_objects.svg` | S10, line 2022 | Figure 6 — Reasoning Architecture: Six Objects | **S6** (Learning Requires Preserved Reasoning) | Same merged section. Appears after the MUO and reasoning-object discussion. Two figures in one section is acceptable given the section's conceptual scope. |
| `fig7_runtime_discovery_loop.svg` | S11, line 2297 | Figure 7 — Runtime Discovery Loop | **S7** (Discovery Turns Human Intent Into Reusable Reasoning) | Same role. Anchors the RIPC loop visually. |

---

## New Visual / Table Candidates

| Candidate | Purpose | Proposed v1.0 section | Format | What prose it replaces or compresses | Priority |
| --- | --- | --- | --- | --- | --- |
| **Full-framework loop** | Show the complete arc: fear -> landscape -> topography -> gradients -> sufficiency -> action -> outcome -> learning -> next cycle | S1 (after fig1) or S11 (before closing) | Loop diagram (SVG) | Recap prose in S11 (formerly S16+S17). If the reader can see the full loop, the conclusion does not need to re-narrate it. | High |
| **Dimension admission matrix** | Defend five dimensions by showing excluded candidates and their dispositions | S3 (after dimension definitions) | Table | Defensive prose in former S5.7, S5.8, and dimension defense paragraphs. Replaces ~800 words with a compact table. | High |
| **Healthcare worked-simulation trace table** | Show context-only path vs reasoning-state path vs next-cycle learning | S5 (entire section is built around this) | Trace table: rows = framework stages, columns = context-only / reasoning-state / next cycle | Narrative re-walk from former S12. Replaces ~1,500-2,000 words. | High |
| **Premature sufficiency comparison** | Show hallucination and harmful action sharing a motion structure | S4 (near Cases A and B) | Side-by-side comparison table | Repeated structural-parallel exposition in former S7.1-S7.3. Replaces ~400-600 words. | Medium |
| **Related-work lineage table** | Preserve intellectual honesty while compressing former S15 | S10 (The Blend Has Roots) | Lineage table: tradition -> contribution -> what this paper adds -> key citation | 18 mini related-work subsections. Replaces ~800-1,000 words. | High |
| **Implementation bridge / architecture map** | Show how components connect without product-spec prose | S8 (What It Would Take to Build This) | Layered architecture diagram | Component prose and table from former S13. Replaces ~500-800 words. | Medium |
| **Minimal interview variant** | Provide 8-10 question on-ramp for Appendix A | Appendix A (before or after full interview) | Short table with phase labels | Reduces adoption friction. Does not replace prose but adds a "start here" entry point. | Medium |

---

## Minimum Complete Arc Coverage Check

Can a reader explain each of the following after reading v1.0 alone?

| # | Arc step | Covered in proposed v1.0 section | Status |
| --- | --- | --- | --- |
| 1 | Why fear of AI agents is an incomplete starting point | S1 (marble analogy, containment-vs-landscape reframe) | Covered |
| 2 | Why the better diagnostic question is: what landscape shapes behavior? | S1 (thesis statement, elevator answer) | Covered |
| 3 | What optimizer state is: goal, policy, interpretation | S3 (first half: optimizer state definitions) | Covered |
| 4 | What perceived topography is: what the system can see, reach, represent, trust, and connect | S3 (second half: five dimension definitions + fig3) | Covered |
| 5 | Why gradients matter | S4 (gradient concept, motion stages) | Covered |
| 6 | Why failures often occur through premature sufficiency | S4 (premature sufficiency argument + fig4) | Covered |
| 7 | How hallucination and harmful action can share a motion pattern | S4 (Cases A and B, comparison table) | Covered |
| 8 | Why context is not reasoning state | S2 (entire section + fig2) | Covered |
| 9 | What reasoning must survive | S6 (six reasoning objects, reasoning architecture + fig6) | Covered |
| 10 | Why learning is not memory or reaction | S6 (reaction-vs-learning distinction, prediction error) | Covered |
| 11 | How Model Update Objects preserve lessons as reusable changes | S6 (MUO concept, eleven-field spec, ten failure modes + fig5) | Covered |
| 12 | How Discovery reduces user burden | S7 (RIPC loop, "do the reasoning work before asking the user" + fig7) | Covered |
| 13 | How the framework can be tested or falsified | S9 (six testable claims, falsifiers, validation levels) | Covered |
| 14 | How Appendix A gives a team a practical starting point | Appendix A (23 questions, 4 phases, three-part structure) | Covered |

**Result: All 14 arc steps are covered. No gaps.**

---

## Compression Hypotheses

These are likely compression moves for v1.0. They are listed as hypotheses, not instructions. No prose editing has been performed.

1. **Repeated healthcare walkthroughs consolidate into one constructed stress test (S5).** v0.2 walks the campaign example through S3, S4, S5, S6, S7, S8, S9, S10, S11, and S12 (193 campaign-related lines across 12 sections). v1.0 keeps the first introduction (S2), the compliance example (S4), the MUO filled example (S6), and the full trace table (S5). All other appearances become one-sentence bridge references. Estimated savings: ~2,000-3,000 words.

2. **Section 15 related work compresses into lineage table plus commentary (S10).** v0.2 runs 18 subsections of "the framework draws from X." v1.0 replaces with a lineage table (tradition / contribution / what this paper adds / key citation) plus 2-3 paragraphs preserving the "blend not invention" and "over-cite by design" statements. Estimated savings: ~800-1,000 words.

3. **Section 13 product-spec detail compresses into implementation bridge (S8).** v0.2 includes JSON schema, component table, and detailed lifecycle governance. v1.0 keeps the maturity model, "Do Not Start With the Whole Machine," and replaces component prose with an architecture-map diagram. Schema and component table deferred to product/design track. Estimated savings: ~500-800 words.

4. **Dimension defense becomes an admission matrix (S3).** v0.2 devotes S5.7 and S5.8 (two full subsections) to defending why Goal Relevance and Policy are not topography dimensions. v1.0 replaces with a compact admission matrix showing all candidates and their dispositions. Estimated savings: ~800 words.

5. **Recap prose in S16 and S17 becomes the full-framework loop plus concise implications (S11).** v0.2 runs ~2,500 words of implications-as-recap and conclusion-as-recap. v1.0 replaces with a full-framework loop diagram, 3-5 genuinely new implications, and a ~400-word forward-looking close. Estimated savings: ~1,500-2,000 words.

6. **S2 glossary folds into S1 inline definitions.** v0.2 devotes a full section to term definitions. v1.0 folds 5 core terms (optimizer, agent, reasoning state, topography, gradient) inline into S1. "Terms That Mean Something Specific Here" and "Terms That Arrive Later" subsections removed. Estimated savings: ~800 words.

7. **S4.5 "Three Primitives Are Enough" compresses to one paragraph.** v0.2 devotes ~500 words to defending the sufficiency of Goal/Policy/Interpretation. v1.0 states the defense in one paragraph. Estimated savings: ~350 words.

8. **S8+S9+S10 merge into unified learning section (S6).** The three sections cover learning, MUOs, and reasoning architecture as separate treatments. v1.0 presents them as one continuous argument: what learning is -> how lessons become objects -> what architecture preserves the full transition. Campaign and safety re-illustrations trimmed to bridges. Estimated savings: ~1,500-2,000 words.

9. **S6+S7 merge into unified motion/failure section (S4).** Gradients and premature sufficiency are currently separate sections. v1.0 presents them as one continuous argument: gradients create motion -> sufficiency stops motion -> premature sufficiency = failure. Estimated savings: ~800-1,000 words.

10. **Premature sufficiency structural exposition partly replaced by comparison table (S4).** v0.2 explains the hallucination/harmful-action parallel in prose across S7.1-S7.3. v1.0 uses a side-by-side comparison table to make the parallel visible at a glance, with brief prose commentary. Estimated savings: ~400-600 words.

**Estimated total compression: ~9,000-12,000 words.** At ~18,000 body words in v0.2, this would produce a v1.0 body of ~6,000-9,000 words before additions (objection responses, KM graveyard confrontation, epistemic framing, citation redistribution, pre-empirical statement). Additions may add ~1,500-2,500 words, producing a net v1.0 body of ~7,500-11,500 words.

**NOTE: This is an aggressive lower-bound scenario, not the approved target.** The 7,500-11,500 estimate assumes maximum compression on every hypothesis. Benet and ChatGPT have agreed that reader comprehension is the target, not economy. The approved compression posture is:

```
Target: complete standalone arc.
Minimum body threshold: ~15,000 words.
Expected body range: determined by completeness chunk by chunk.
Compression guide: useful, but subordinate to reader comprehension.
```

The compression hypotheses above remain useful as a guide for where pontification can be eliminated. But the rewrite should proceed chunk by chunk, and each chunk should be judged by whether it helps the reader explain the framework more cogently — not by whether it hits a word-count target. If preserving the arc requires exceeding the estimated compression, the paper should exceed it.

---

## Final Authorial Decisions Before v1.0 Working Draft

The following decisions were made by Benet and ChatGPT after reviewing the outline map, compression hypotheses, and rewrite doctrine.

| # | Decision | Detail |
| --- | --- | --- |
| 1 | **11-section structure approved** | The proposed structure (S1-S11 + Appendix A + References) is the working v1.0 structure. Merges of S4+S5, S6+S7, and S8+S9+S10 are accepted. |
| 2 | **Body target is comprehension, not economy** | 15,000 words is the minimum body threshold, not the ceiling. Final body length determined chunk by chunk according to reader comprehension and completeness of the standalone arc. |
| 3 | **Compression hypotheses are diagnostic, not governing** | The hypotheses identify where repetition may be compressed. They do not force the paper below the level needed for conceptual completeness. |
| 4 | **Stress test remains S5; brief preview added to S1 or S2** | The full constructed stress test stays at S5, after the core mechanics are introduced in S1-S4. A brief preview example should appear in S1 or S2 so the reader knows the theory is moving toward a concrete scenario. |
| 5 | **Three-column stress test required** | The trace table must use three columns: Context-only path / Reasoning-state path / Next-cycle learning. This comparison demonstrates the framework's value-add. |
| 6 | **Full-framework loop appears early (S1)** | The loop diagram goes in S1 as a reader map. It may be lightly echoed in S11 but not re-explained at length. |
| 7 | **Objections distributed where they arise; S9 is the formal synthesis** | "Better RAG + better prompts" in S2 or S7. "KM graveyard" in S6. "Arbitrary dimensions" in S3. "Post-hoc explains everything" in S9. "Just good systems engineering" introduced early, addressed formally in S9. |
| 8 | **No Appendix B** | Full schema, component tables, lifecycle governance, and implementation templates deferred to product/design or practitioner/tooling track. Keep only enough implementation structure in v1.0 for the theory to be credible and understandable. |
| 9 | **v1.0 includes an abstract and epistemic-status paragraph** | Abstract states thesis, method (pre-empirical framework + constructed stress test), and key contribution (premature sufficiency + reasoning-state preservation). Epistemic-status paragraph states this is a pre-empirical design framework, not an empirical validation paper. |
| 10 | **New visuals specified before drafting; creation follows outline finalization** | Highest-priority candidates: full-framework loop, dimension admission matrix, healthcare trace table, premature sufficiency comparison, related-work lineage table, implementation architecture map, Appendix A minimal interview variant. |
| 11 | **S11 contains 3-4 genuinely new implications** | Preferred candidates: product evaluation, governance/regulation, organizational learning, research agenda. No recap of body arguments. |
| 12 | **Rewrite standard** | "Does this section help the reader explain the framework more cogently? If yes, preserve, clarify, or restructure. If no, compress, move, visualize, or cut." |

---

## Open Editorial Questions (Remaining)

The following questions were NOT resolved by the decisions above and remain open:

1. **Should a tiny contrast example be added?** If yes, which domain (incident response, customer support, compliance review)? Maximum 2-3 paragraphs. Placement: S4 or S9.

2. **Should "Model Update Object" be renamed?** "Learning Record" or "Decision Lesson" trades precision for accessibility.

3. **What is the target audience / venue for v1.0?** Academic journal, conference, practitioner whitepaper, or mixed audience? This determines citation depth and evidence requirements.

4. **Should v1.0 explicitly describe itself as the keystone paper for a broader body of work?** If explicit, a brief statement in S1 or S11 names the tracks. If internal, the body-of-work strategy guides compression without appearing in the manuscript.

5. **How will a real case be sourced for future validation?** Options remain: retrospective analysis of a public AI failure, documented organizational learning failure, Appendix A pilot, minimal prototype. This does not block v1.0 (which uses a constructed stress test), but should be decided for the research roadmap.

---

## No-Edit Confirmation

No manuscript or release files were edited in the creation of this document. `PAPER_v0.2.md`, `PAPER_DRAFT.md`, section files, references, SVGs, and release files remain unchanged.
