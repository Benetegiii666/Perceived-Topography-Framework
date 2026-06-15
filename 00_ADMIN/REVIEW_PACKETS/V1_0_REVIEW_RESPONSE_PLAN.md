# v1.0 Review Response Plan

## Executive Summary

Six independent reviewer agents evaluated the frozen v0.2 manuscript (36,861 words). The consensus is clear and consistent:

**What reviewers agreed works:**
The paper's core ideas are genuinely useful and well-constructed. The marble/landscape reframe, the context-vs-reasoning-state distinction, the premature sufficiency concept, the Discovery Framework, the Model Update Object, Appendix A, and the falsifiability commitments were all repeatedly praised. No reviewer questioned the framework's fundamental coherence or recommended abandoning the argument.

**What reviewers agreed does not work yet:**
The paper is too long for its evidence base. The healthcare campaign example is repeated too many times. The mid-paper sections (3-12) are nearly citation-free. The five topography dimensions are asserted but not defended. The framework's vocabulary is flexible enough to raise unfalsifiability concerns. There is no empirical evidence of any kind.

**What must change before v1.0:**
Compress by 25-35%. Add at least one real case. Redistribute citations into the mid-paper sections. State the epistemic status (pre-empirical) early and clearly. Fix the version header.

**What should not be changed:**
The marble analogy, Section 3, premature sufficiency, the sufficiency-vs-certainty distinction, the reaction-vs-learning distinction, the Discovery principle, Section 14 (falsifiability), the "blend not invention" posture, Appendix A, and the "reduces readmissions" compliance example.

---

## Confirmed Strengths to Preserve

### 1. The marble / landscape reframe

- **Why it matters:** The single most effective moment in the paper. Makes the core argument intuitive before any terminology is introduced. Universally praised.
- **Valued by:** All 6 reviewers.
- **v1.0 instruction:** Preserve intact. Consider moving it earlier (first paragraph or abstract).

### 2. Context vs. reasoning state (Section 3)

- **Why it matters:** The paper's strongest section. Names a real gap that anyone in a knowledge-intensive organization recognizes immediately: retrieval gives the system *what* but not *why*.
- **Valued by:** Reviewers 1, 2, 3, 4 (identified as strongest section by 4/6).
- **v1.0 instruction:** Preserve intact. This section should not be compressed.

### 3. Premature sufficiency

- **Why it matters:** The paper's most original intellectual contribution. Connects hallucination and harmful action through a shared mechanism. Produces actionable design levers. The idea most likely to survive outside the paper.
- **Valued by:** Reviewers 1, 2, 3, 4, 5 (identified as strongest contribution by 5/6).
- **v1.0 instruction:** Preserve the concept. The Section 7 prose may be compressed, but the core argument and the compliance example must survive.

### 4. Discovery Framework ("do the reasoning work before asking the user")

- **Why it matters:** The most product-ready construct. Describes an interaction pattern a team could prototype within weeks. The Retrieve-Infer-Propose-Confirm loop is immediately implementable.
- **Valued by:** Reviewers 1, 2, 3, 5.
- **v1.0 instruction:** Preserve intact. Consider making this principle more prominent (e.g., callout or summary).

### 5. Model Update Object / learning loop

- **Why it matters:** The most concrete, falsifiable, and implementable claim. The eleven-field payload and ten failure modes give practitioners enough structure to build against.
- **Valued by:** Reviewers 1, 2, 6.
- **v1.0 instruction:** Preserve the concept and specification. Address the adoption/retrieval problem more directly.

### 6. Appendix A (Decision Topography Interview)

- **Why it matters:** The most practically actionable section. A team could use it Monday morning without reading Sections 4-15. Transforms the framework from theory to facilitation tool.
- **Valued by:** Reviewers 1, 3, 4, 5 (identified as most actionable by 4/6).
- **v1.0 instruction:** Keep in the paper (do not separate as companion doc). Consider adding facilitation guidance and a minimal-interview variant.

### 7. Falsifiability posture (Section 14)

- **Why it matters:** Stronger than most framework papers. Builds credibility with academic and technical audiences. The explicit falsifiers and validation levels are a genuine commitment to testability.
- **Valued by:** Reviewers 1, 2, 4, 6.
- **v1.0 instruction:** Preserve intact. Strengthen by addressing unfalsifiability risk more directly in the body text.

### 8. Intellectual lineage honesty ("blend, not invention")

- **Why it matters:** Prevents the most common academic objection (under-crediting prior traditions). The over-cite-by-design principle is exactly right for a synthetic framework.
- **Valued by:** Reviewers 2, 4, 6.
- **v1.0 instruction:** Preserve the posture. Section 15 prose can be compressed, but the lineage acknowledgment must remain clear.

### 9. Sufficiency vs. certainty distinction (Section 6.5)

- **Why it matters:** Immediately useful design heuristic. The 2x2 is one of the clearest conceptual moves in the paper.
- **Valued by:** Reviewers 1, 4, 5.
- **v1.0 instruction:** Preserve intact.

### 10. "Reduces readmissions" compliance example (Section 7.5)

- **Why it matters:** The most concrete, realistic example in the paper. Feels like a real problem a real practitioner faces.
- **Valued by:** Reviewer 5 (explicitly praised as "feels like a Tuesday").
- **v1.0 instruction:** Preserve intact.

---

## Confirmed Weaknesses to Address

| Issue | Reviewers | Severity | Why it matters | v1.0 response |
| --- | --- | --- | --- | --- |
| Paper too long (36,861 words) | 6/6 | Blocking | Target audience will not finish it. Estimates: need 25-35% cut. | Compression pass. Primary targets: running example consolidation, Sections 4-6 defensive subsections, Section 12 re-walk, Section 15, Section 16. |
| Healthcare campaign example repeated 10-12 times | 6/6 | Blocking | Diminishing returns after Section 4. Cumulative repetition numbs the reader. | Consolidate to 2-3 rich appearances: one early (Section 3-4), one mid-paper (Section 7 or 8), one full end-to-end (Section 12, compressed to trace table). Remove intermediate replays. |
| No empirical evidence | 6/6 | Blocking | Every claim is currently untested. Paper sometimes writes as though benefits are established. | Add at least one real case or retrospective analysis. If none available, add explicit pre-empirical framing. |
| Citation desert in Sections 3-12 | 3/6 | Blocking | Core architecture presented without inline engagement with prior work. Credibility vulnerability for peer review. | Redistribute citations from Section 15 into sections where constructs are introduced. Each new construct gets at least one inline citation. |
| Five topography dimensions asserted, not defended | 4/6 | Important | No argument for why these five, why not others, whether independent or exhaustive. | Add brief justification. Address excluded alternatives (Timeliness, Salience, Completeness). Explain what changes if one is removed. |
| Unfalsifiability / post-hoc rationalization risk | 4/6 | Important | Framework vocabulary broad enough to explain any failure. Real test: does it produce different interventions? | Acknowledge risk in body text (near Section 7 or Section 14). State defense: distinct dimensions must produce distinct interventions. Demonstrate with at least one case. |
| "Better RAG + better prompts" objection not addressed | 1/6 | Important | Builder audience will compare against simpler alternative. Paper does not argue why 80% of benefit can't be achieved without framework. | Add explicit comparison. Show where simpler alternative breaks down. |
| Knowledge-management graveyard risk | 3/6 | Important | MUOs resemble structured knowledge objects that historically fail adoption. Paper's answer (Discovery) is never explicitly stated as the response. | Add direct confrontation. Name the graveyard problem. Position Discovery as the design response. |
| Section 2 glossary breaks momentum | 3/6 | Important | Reader goes from compelling marble analogy to term-definition section. Interrupts argument flow. | Restructure: fold core terms (5) inline into Sections 1 and 3. Reduce Section 2 to half-page orientation or remove. |
| Section 13 register problem | 2/6 | Polish | Oscillates between research paper and product spec. JSON schema feels out of place. | Compress. Keep maturity model and "Do Not Start With the Whole Machine." Move schema and component table to appendix. |
| Section 15 too long (18 subsections) | 3/6 | Polish | Product and practitioner audiences will skip it. Academic reviewers valued the honesty but not the length. | Compress to 8-10 subsections. Consider a lineage table with brief commentary. Keep "blend not invention" statement. |
| Version header says "Version 0.1" in v0.2 file | 1/6 | Trivial | Factual error. | Fix in v1.0 working copy. |

---

## v1.0 Priority Tiers

### Tier 1 — Required for v1.0

1. **Compression pass.** Target: 25-35% reduction (from ~18,000 body words to ~12,000-13,500). Primary sources: running example consolidation, Sections 4-6 defensive subsections, Section 12 re-walk, Section 15 and 16. Do not compress Sections 3, 7, 8, 9, 11, 14, or Appendix A.

2. **Real or retrospective case.** At least one non-hypothetical example analyzed through the framework. Options ranked below in Evidence/Case Strategy.

3. **Citation redistribution.** Move inline citations from Section 15 into Sections 3-12. Add missing tradition citations. Every section introducing a construct needs at least one inline citation.

4. **Epistemic status statement.** Add a clear paragraph in Section 1 (end) or Section 2 (beginning): "This paper proposes a design framework. It has not yet been empirically validated. All examples are illustrative. Section 14 defines conditions under which the framework would be confirmed or disconfirmed."

5. **Fix version header.** Update "Version 0.1" to "Version 1.0" in the working copy.

### Tier 2 — Strongly Recommended

6. **Defend the five topography dimensions.** Brief subsection or paragraph in Section 5: why these five, what was excluded (Timeliness, Salience, Completeness), why excluded candidates are subsumed or unnecessary. Even a brief argument pre-empts the most common reviewer objection.

7. **Address knowledge-management graveyard risk.** Direct confrontation in Section 9 or 13: structured learning repositories have failed before (Lotus Notes, SharePoint, ITIL). State why Discovery is the design response. Acknowledge that AI-inferred reasoning objects introduce their own trust challenge.

8. **Address "better RAG + better prompts" objection.** Add a subsection (Section 3 or Section 13): compare the framework against the simplest alternative. Show specifically where better retrieval + better prompting breaks down (premise tracking, cross-cycle learning, policy salience at moment of action).

9. **Add missing tradition citations.** See Citation Strategy below.

10. **Strengthen or soften premature-sufficiency claim.** Either cite empirical work supporting the structural parallel between hallucination and harmful action, or reframe as a testable hypothesis the framework generates. Current presentation asserts a strong unification with no supporting evidence.

### Tier 3 — Optional / Polish

11. **Appendix A facilitation guidance.** Add brief practical notes: who should be in the room, how long it takes, what artifacts to bring, what "good enough" looks like for a first pass. Low cost, high practical value.

12. **Minimal-interview variant.** Identify 8-10 questions from the 23 that constitute a "minimum viable interview" for teams doing their first pass.

13. **Full-framework visual.** Single diagram showing the complete loop: Optimizer State -> Topography -> Motion -> Action -> Outcome -> Learning -> Model Update -> reshaped Topography. Individual figures are good but section-local; no single overview exists.

14. **Related-work compression.** Reduce Section 15 from 18 subsections to 8-10. Consider a lineage table with brief commentary per tradition.

15. **Section 13 compression / schema relocation.** Keep maturity model and minimal-start guidance. Move JSON schema and component table to Appendix B.

16. **Tighten Section 17 (Conclusion).** Reduce from ~170 lines of recap to ~50 lines that make one final forward-looking move.

---

## Compression Strategy

Section-by-section compression classification for v1.0:

| Section | Current role | Compression class | Notes |
| --- | --- | --- | --- |
| 1. Introduction | Sets up the reframe | Compress lightly | Marble analogy arrives early — good. Trim the containment discussion by ~20%. Move epistemic status statement here. |
| 2. Terms | Vocabulary orientation | Restructure | Fold 5 core terms inline into Sections 1 and 3. Reduce to half-page "How to Read This Paper" note or remove entirely. |
| 3. Context vs. Reasoning State | Core argument | Preserve mostly | Strongest section. Do not compress. Add inline citations. |
| 4. Optimizer State | Goal, Policy, Interpretation | Compress heavily | Cut "Three Primitives Are Enough" (4.5) by 50%. Remove one of the two campaign-example passes. Cut safety re-illustration if redundant with Section 7. Target: ~30% reduction. |
| 5. Information Topography | Five dimensions | Compress heavily | Cut "Relevance Depends on the Goal" (5.7) and "Policy Shapes the Boundary" (5.8) by 50% or fold into footnotes. Remove one campaign-example pass. Add dimension-defense paragraph. Target: ~30% reduction. |
| 6. Gradients and Motion | Four stages | Compress lightly | Sufficiency-vs-certainty distinction must survive. Trim investigation and attraction subsections. Target: ~15% reduction. |
| 7. Failure | Premature sufficiency | Compress lightly | Core argument and compliance example must survive. Trim the structural-parallel exposition. Target: ~15% reduction. |
| 8. Learning | Prediction error, reaction vs. learning | Preserve mostly | Rigorous and well-scoped. Minor trim possible in the KM-failure examples. |
| 9. Model Update Objects | MUO specification | Preserve mostly | Add knowledge-management graveyard confrontation. Consider moving filled-out example earlier than schema. |
| 10. Reasoning Architecture | Six objects | Compress heavily | Heavy taxonomy section. Reduce table-per-object format. Consolidate campaign and safety examples. Target: ~25% reduction. |
| 11. Discovery | Retrieve-Infer-Propose-Confirm | Preserve mostly | Most product-ready section. Minor trim only. |
| 12. Running Example | Full end-to-end | Restructure | Convert from narrative re-walk to compressed end-to-end trace table with brief commentary. This is the single largest compression opportunity. Target: ~40-50% reduction. |
| 13. Implementation Bridge | Components, schema, maturity model | Compress heavily | Keep maturity model and "Do Not Start With the Whole Machine." Move JSON schema and component table to Appendix B. Target: ~40% reduction. |
| 14. Validation | Falsifiability, testable claims | Preserve mostly | Preserve intact. Add body-text acknowledgment of unfalsifiability risk if not placed elsewhere. |
| 15. Related Work | Intellectual lineage | Compress heavily | Reduce from 18 to 8-10 subsections. Consider lineage table. Keep "blend not invention." Target: ~40% reduction. |
| 16. Implications | What changes | Restructure | Replace summary restatements with genuinely new implications (organizational hiring, product evaluation criteria, regulatory implications). Target: ~50% reduction. |
| 17. Conclusion | Final statement | Compress heavily | Reduce from ~170 lines of recap to ~50 lines with one forward-looking move. Target: ~70% reduction. |
| Appendix A | Decision Topography Interview | Preserve mostly | Add facilitation guidance. Consider minimal-interview variant. Do not remove. |
| References | Bibliography | Leave unchanged | Add new citations as needed. |

**Projected compression outcome:** If targets are met, body text drops from ~18,000 words to ~12,000-13,000 words (28-33% reduction). Additions (case study, epistemic statement, dimension defense, objection responses) may add ~1,500-2,500 words back, resulting in a net v1.0 body of ~13,500-15,500 words.

---

## Evidence / Case Strategy

Options for adding empirical grounding, ranked by value and feasibility:

| Option | Description | Pros | Cons |
| --- | --- | --- | --- |
| **Retrospective case analysis** | Take an actual AI failure (public or from authors' experience) and analyze it through the framework | Highest credibility. Shows the framework producing a diagnosis. Relatively low effort. | Requires a real case the authors have access to. May require anonymization. |
| **Organizational learning failure** | Take a documented case where an org repeated a known mistake (with or without AI) and show how reasoning-state preservation would have changed the outcome | Demonstrates the context-vs-reasoning-state distinction concretely. Many available public cases. | Counterfactual — shows what *would* have helped, not what *did* help. |
| **Appendix A pilot** | Conduct the Decision Topography Interview with one team on one workflow and report what it surfaced | Demonstrates the framework's most actionable artifact. Low effort if the authors have a willing team. | Does not demonstrate the full learning loop. Only shows the discovery phase. |
| **Minimal prototype** | Build a minimal reasoning-state layer (even as structured prompts + metadata) and run one workflow through it | Demonstrates buildability. Would answer the "better RAG + better prompts" objection directly. | Highest effort. May not be feasible for v1.0 timeline. |
| **Pre-empirical framing only** | Do not add a case. Instead, strengthen the epistemic framing: state clearly that the framework is a design hypothesis, all examples are illustrative, and Section 14 defines the validation path. | Honest. Low effort. | Does not address the credibility gap. Every reviewer asked for a real case. |

**Recommendation:** Pursue the retrospective case analysis as the primary strategy. If unavailable, use the organizational learning failure option. In either case, also add the pre-empirical framing statement regardless.

---

## Citation Strategy

### Sections needing inline citations

| Section | Constructs introduced | Currently cited | Needs |
| --- | --- | --- | --- |
| 3 | Context vs. reasoning state | Walsh & Ungson 1991, Alavi & Leidner 2001, March & Simon 1958 | Adequate, but could add organizational forgetting / transactive memory |
| 4 | Optimizer, Goal, Policy, Interpretation | Russell & Norvig 2020, Dennett 1987, Weick 1995 | Adequate |
| 5 | Five topography dimensions | Gibson 1979, Norman 1988 | **Needs:** Information science (Wilson, Kuhlthau, Bates), situation awareness (Endsley 1995) |
| 6 | Motion stages, sufficiency | Ng et al. 1999, Gibson, Norman, Simon, Pirolli & Card, Howard, Russell & Wefald | Best-cited mid-paper section. Adequate. |
| 7 | Premature sufficiency, hallucination/harmful action unification | Menick et al. 2022, Lewis et al. 2020 | **Needs:** Hallucination surveys (Ji et al. 2023, Huang et al. 2023), trust in automation (Lee & See 2004, Parasuraman & Riley 1997) |
| 8 | Learning, prediction error, reaction vs. learning | Argyris & Schon 1978, Cyert & March 1963 | Could add organizational routines (Feldman & Pentland 2003) |
| 9 | Model Update Object | None inline | **Needs:** Case-based reasoning positioning (Aamodt & Plaza 1994), lessons-learned literature, KM failure literature |
| 10 | Six reasoning objects | None inline | **Needs:** At least one citation to design rationale or argumentation frameworks |
| 11 | Discovery Framework | None inline | **Needs:** Mixed-initiative interaction (Horvitz 1999), cognitive load (Sweller 1988), naturalistic decision-making (Klein 1998) |
| 12 | Full running example | None inline | Acceptable — illustrative section |
| 13 | Implementation architecture | None inline | **Needs:** Agent architectures (ReAct, Reflexion, Toolformer), maturity model precedents |

### Missing traditions to add

| Tradition | Key sources | Where to cite | Why it matters |
| --- | --- | --- | --- |
| Agent architectures | Yao et al. 2023 (ReAct), Shinn et al. 2023 (Reflexion), Schick et al. 2024 (Toolformer) | Sections 8-9, 13, 15 | Reflexion implements a version of the learning loop. Not citing it is a gap. |
| Hallucination surveys | Ji et al. 2023, Huang et al. 2023, Maynez et al. 2020 | Section 7 | Broadens support for premature-sufficiency claim. Replaces lone reliance on Menick et al. |
| Information science / info behavior | Wilson 2000, Kuhlthau 1991, Bates 1989 | Section 5 | Topography dimensions overlap with established information quality and behavior models. |
| Situation awareness | Endsley 1995 | Section 5 | "Perceived topography" is closely related to Endsley's SA model. |
| Naturalistic decision-making | Klein 1998, 2008 | Sections 6, 11 | Sufficiency-based decision-making under uncertainty. Directly relevant to Discovery. |
| Trust in automation | Lee & See 2004, Parasuraman & Riley 1997 | Section 7 | Confidence and escalation design is essentially trust calibration. |
| Systems safety | Leveson 2011, Rasmussen 1997, Hollnagel 2014 | Sections 1, 7, 15 | "Failures emerge from system structure, not component malice" is the paper's core claim. These are natural allies. |
| KM failure / lessons-learned reuse | Markus 2001, Weber et al. 2001 | Section 9 | Directly addresses the knowledge-management graveyard objection. |
| Cognitive load | Sweller 1988 | Section 11 | "Do the reasoning work before asking the user" is a cognitive load argument. |
| Bounded rationality (broadened) | March 1978, Gigerenzer & Selten 2001 | Section 2, 4 | Reduces lone reliance on Simon 1955. |
| Organizational routines | Feldman & Pentland 2003 | Section 8 | How model updates change future behavior relates to routines as generative systems. |

### Claims needing support vs. softening

| Claim | Current support | Recommended action |
| --- | --- | --- |
| Hallucination and harmful action share premature-sufficiency structure | Structural analogy only | Either cite supporting evidence OR soften to "testable hypothesis the framework generates" |
| Five topography dimensions are the right decomposition | Author judgment | Add brief justification. Acknowledge alternatives. |
| MUOs reduce repeated mistakes more effectively than postmortems | None | Soften to hypothesis. Add KM failure literature to contextualize. |
| Reasoning-state preservation improves future agent behavior | None | Soften to hypothesis. Add pre-empirical framing. |
| Discovery reduces user burden while increasing quality | None | Soften to "design hypothesis." Strongest if paired with Appendix A pilot. |

---

## Objection Response Strategy

### "This is just good systems engineering"

**Concede and sharpen.** The paper should acknowledge that much of what it recommends *is* good systems engineering. The framework's contribution is not that these practices are new, but that they have not been applied as a unified design layer to human-agent systems. The specific addition: (a) the premature-sufficiency diagnostic connects hallucination and safety research through a shared mechanism; (b) the reasoning-state architecture makes explicit what "good systems engineering" leaves implicit; (c) the learning loop formalizes what postmortems attempt but rarely achieve. The test: show at least one case where framework-derived diagnosis differs from what standard root-cause analysis would produce.

### "This is just better RAG + better prompts"

**Draw the boundary.** Better RAG gives the system *what* to read. Better prompts tell the system *how* to reason about what it reads. The framework adds *what to preserve* (reasoning state) and *how to reuse it* (MUOs, Discovery, premise tracking). The specific break point: a better RAG system can retrieve the prior campaign report. It cannot determine which premise in that report later failed, whether the boundary conditions still match, or whether the confidence that made the prior decision sufficient has changed. State this comparison explicitly in the paper.

### "Structured learning objects become knowledge-management graveyards"

**Name the problem, then position Discovery as the design response.** The paper should acknowledge that Lotus Notes, SharePoint lessons-learned libraries, ITIL post-incident templates, and corporate wikis all attempted structured knowledge capture and most failed. The common failure mode: humans had to create the objects. Discovery changes the creation economics: the system infers reasoning objects from existing artifacts and conversations, proposes a strawman, and asks only for confirmation or correction. This shifts the burden from authoring to reviewing. The paper should also acknowledge the secondary risk: AI-inferred objects may be wrong, and if they are wrong often enough, users will learn to ignore them. This is a design challenge, not a refutation.

### "The framework explains everything post hoc"

**Acknowledge the risk and state the defense.** Rich analytic vocabularies can explain any failure after the fact. The framework's defense is specificity: each topography dimension must produce a *distinct* diagnosis leading to a *distinct* intervention. If a Visibility failure and a Connectivity failure lead to the same fix, the dimensions are not earning their keep. Section 14.13 already states this standard; the paper should (a) repeat it in the body text near Section 7, and (b) demonstrate it with at least one worked case where two dimensions produce genuinely different interventions.

### "The five dimensions are arbitrary"

**Defend on practical grounds, not on theoretical necessity.** The paper should not claim these are the only possible five. It should argue they are a *minimum viable diagnostic set*: each dimension produces a distinct diagnosis, and removing any one creates a gap (e.g., without Connectivity, the framework cannot explain failures where information was visible but not linked to the relevant policy). Address the most plausible missing candidates — Timeliness (subsumed by Confidence, which degrades when information is stale), Salience (subsumed by Visibility and Representation), Completeness (emergent from the interaction of all five) — and explain why they do not require promotion to independent dimensions.

---

## Do Not Change List

These elements should survive v1.0 intact or with only minimal editing:

1. The marble analogy (Section 1)
2. Section 3 in its entirety (Context vs. Reasoning State)
3. The premature sufficiency argument (Section 7 core)
4. The "reduces readmissions" compliance example (Section 7.5)
5. The sufficiency-vs-certainty 2x2 (Section 6.5)
6. The reaction-vs-learning distinction (Section 8.8)
7. The Discovery Framework's "do the reasoning work before asking the user" principle (Section 11)
8. The Model Update Object eleven-field specification (Section 9.3)
9. The ten MUO failure modes (Section 9)
10. Section 14 (Validation and Falsifiability)
11. Section 15's "blend, not invention" posture and over-cite-by-design principle
12. Appendix A (Decision Topography Interview)
13. All 7 SVG figures (content current, no stale language)

---

## Open Editorial Decisions for Benet/ChatGPT

These questions require authorial judgment and cannot be resolved by reviewer consensus alone:

1. **What is the v1.0 target word count?** Reviewers suggest 12,000-13,500 body words (down from ~18,000). Is this acceptable, or is there a minimum length the argument requires?

2. **What real case can be used?** The single highest-value addition. Options: (a) retrospective analysis of a real AI failure, (b) documented organizational learning failure, (c) Appendix A pilot with a real team, (d) minimal prototype evaluation. Which is available and feasible?

3. **Should the paper explicitly name itself "pre-empirical" in Section 1?** All six reviewers recommended this. The alternative is softer language ("design hypothesis" or "proposed framework"). How strong should the epistemic disclaimer be?

4. **Should Section 2 (Terms) survive as a section, be folded inline, or be reduced to a half-page note?** Three reviewers found it momentum-breaking. One (Academic) found it useful. The current structure tries to serve two functions (orient quickly + define precisely) and partially succeeds at both.

5. **Should Appendix A stay in the paper or become a companion document?** Reviewers 2 and 4 suggested separation. Reviewers 3 and 5 said it is the most useful section and should be more prominent. The synthesis recommendation is to keep it, but the decision is yours.

6. **Should Section 15 (Related Work) become a table, or keep its current subsection structure?** Academic reviewer praised the honesty; product and practitioner reviewers found it exhausting. Compression to 8-10 subsections is a middle path.

7. **Should Section 13's JSON schema and component table move to an appendix?** This resolves the register-shift problem (too abstract for builders, too specific for researchers) without losing the content.

8. **Should "Model Update Object" be renamed?** Reviewer 3 suggested "Learning Record" or "Decision Lesson" for organizational audiences. This trades precision for accessibility.

9. **How many appearances should the healthcare campaign example have?** Reviewers valued the example but not the repetition. The synthesis recommends 2-3 rich appearances. Is that sufficient, or does the argument require more?

10. **Should a second domain example be added?** Reviewer 5 (blocking) and Reviewer 3 (important) recommended a non-marketing example to demonstrate generalizability. Options: incident response, compliance review, customer support triage, sales enablement. Adding a second domain is high value but high effort.

11. **Should the paper add a "Framework at a Glance" one-page summary?** Three reviewers recommended a single visual showing the full loop. This would be a new artifact (Figure 8 or a summary page after Section 2).

12. **What is the target venue or audience for v1.0?** The compression strategy, citation depth, and evidence requirements differ significantly depending on whether v1.0 targets an academic journal, a conference, a practitioner audience (blog/whitepaper), or a mixed audience.

---

## Recommended Next Action

1. **Decide v1.0 target length.** This determines the aggressiveness of the compression pass.

2. **Decide case strategy.** The real case is the single highest-value addition but may require the most calendar time. Starting early is critical.

3. **Build the citation workstream.** Citation research and redistribution can run in parallel with case strategy. Start with the gap sections (5, 7, 9, 11, 13).

4. **Begin compression from a working copy, not from frozen v0.2.** Create a `PAPER_v1.0_WORKING.md` or a branch. v0.2 remains frozen and unchanged.

5. **Resolve the open editorial decisions** (above) before beginning prose work. Several compression and restructuring decisions depend on authorial judgment that reviewer consensus cannot supply.

---

## No-Edit Confirmation

No manuscript files were edited in the creation of this plan. `PAPER_v0.2.md`, `PAPER_DRAFT.md`, section files, references, SVGs, and release files remain unchanged.
