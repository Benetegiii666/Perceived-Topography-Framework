# v1.0 Section 10 Source Packet

## The Blend Has Roots

---

## Source Files Reviewed

| Source | File | Relevant sections | Line ranges |
| --- | --- | --- | --- |
| v0.2 Related Work | PAPER_v0.2.md | S15: The Blend Has Roots | Lines 3180–3369 |
| v0.1 Related Work | PAPER_v0.1.md | S15: Related Work and Intellectual Lineage | Lines ~3179–3369 |
| v1.0 Section 9 ending | PAPER_v1.0_WORKING.md | S9 closing | Lines 2160–2162 |
| v1.0 Section 10 placeholder | PAPER_v1.0_WORKING.md | S10 arc comment | Lines 2166–2173 |
| v1.0 Section 11 placeholder | PAPER_v1.0_WORKING.md | S11 arc comment | Lines 2177–2185 |
| Rewrite doctrine | V1_0_REWRITE_DOCTRINE_AND_WORKPLAN.md | Output tracks, citation workstream | Lines 195–214, 468–510 |
| S9 integrity check | V1_0_SECTION_09_POST_INSERTION_INTEGRITY_CHECK.md | S9→S10 handoff | Full |
| Concept architecture | CURRENT_STATE.md | All phases | Full |

---

## Section 10 Narrative Job

Section 10 is the intellectual legitimacy bridge. It answers:

> If the framework is bounded, falsifiable, and testable, where does it come from?

It should show:

1. The framework has roots in recognizable intellectual traditions.
2. It did not invent its ingredients.
3. Its contribution is the synthesis: arranging those traditions into a reasoning-state architecture for human-agent systems.
4. The blend is what matters, not any individual borrowing.

Section 10 should feel scholarly but not like academic sludge. The voice is: "Here is the lineage. Here is the synthesis. Here is why the blend matters."

The section should NOT:

- Keep proving the framework (Section 9 handled the rigor gate)
- Replay the architecture (Section 8)
- Re-litigate objections (Section 9)
- Become the conclusion (Section 11)
- Become an exhaustive literature review

---

## Handoff from Section 9

Section 9 ends:

> "Not belief."
>
> "Contact with evidence."

Section 9 does not provide an explicit bridge to lineage. The closing is a standalone rigor-gate ending. Section 10 should open by answering the implicit next question: if the framework makes testable claims and names its limits, where did it come from?

Do not replay falsifiability. Do not reopen objections. Begin from lineage.

---

## Historical Reconstruction

### v0.1 Source Material

**Section 15: "Related Work and Intellectual Lineage"** (~1,800 words, 19 subsections)

Narrative job: Position the framework within prior traditions, show what is borrowed, and clarify what is synthesized.

Same structure as v0.2 with slightly different subsection titles.

### v0.2 Source Material

**Section 15: "The Blend Has Roots"** (~1,900 words, 19 subsections: S15.1–S15.19)

Narrative job: Same as v0.1 with refined titles.

Key content:

**15 traditions named (S15.1–S15.15):**

| # | Tradition | Key source | What it contributes | What the framework adds |
| --- | --- | --- | --- | --- |
| 1 | Bounded rationality & satisficing | Simon 1955 | Agents don't optimize from complete reality; sufficiency as stopping | Treats sufficiency as preserved, auditable state inside reasoning architecture |
| 2 | Organizational decision theory | March & Simon 1958, Cyert & March 1963 | Organizations make decisions under limits | Six-object architecture makes organizational processes durable in AI workflows |
| 3 | Behavioral theory of the firm | Cyert & March 1963 | Firms learn through imperfect search, aspiration gaps | MUO preserves expectation→outcome→explanation→update transitions |
| 4 | Organizational learning | Argyris & Schön 1978 | Single/double-loop learning; learning ≠ correction | Formalizes minimum reasoning objects to preserve reaction vs. learning distinction |
| 5 | Sensemaking | Weick 1995 | Actors construct meaning under ambiguity | Optimizer Interpretation formalizes how actors construct meaning |
| 6 | Affordances | Gibson 1979, Norman 1988 | Environment invites/permits/constrains action | Topography extends affordance beyond action to visibility, accessibility, confidence, connectivity |
| 7 | Reward shaping | Ng et al. 1999 | Designed pressures influence behavior | Gradient as broader systems-level notion across information, confidence, organizational meaning |
| 8 | RAG / grounding | Lewis et al. 2020, Menick et al. 2022, Yu et al. 2024 | Context retrieval matters in AI systems | Grounding as part of Confidence/Sufficiency; RAG alone insufficient without reasoning objects |
| 9 | AI safety / agent governance | Lynch et al. 2025, OpenAI 2025, Google DeepMind 2024 | Agent behavior must be inspectable, bounded, governable | Containment necessary but incomplete; safer systems need landscapes, not just boundaries |
| 10 | Behavioral description | Shanahan et al. 2023, Shanahan 2022 | Anthropomorphic caution for AI systems | Optimizer frame avoids both dismissal and over-ascription errors |
| 11 | Knowledge management | Alavi & Leidner 2001, Walsh & Ungson 1991 | Organizational memory, knowledge storage, retrieval | KM preserves artifacts; reasoning architecture preserves state transitions |
| 12 | Decision rationale / provenance | Moreau et al. 2013, Lee 1997 | Why decisions were made; design rationale | Six objects = provenance structure for adaptive reasoning |
| 13 | Human-centered AI / mixed-initiative | Amershi et al. 2019, Horvitz 1999, Johnson et al. 2014 | HCI, human-in-the-loop, collaborative AI | Discovery directly creates reasoning objects; is front door to reasoning architecture |
| 14 | Case-based reasoning | Aamodt & Plaza 1994 | Prior cases inform future decisions | MUO like case memory but organized around model change, not similarity |
| 15 | Uncertainty calibration | Guo et al. 2017, Kadavath et al. 2022 | Calibration and abstention under uncertainty | Places abstention/escalation inside optimizer motion as sufficiency-driven actions |

**Synthesis sections (S15.16–S15.19):**

- S15.16: "The Framework Adds the Mix" — the specific synthesis claim
- S15.17: "Boundaries Keep the Claim Honest" — what the framework is NOT
- S15.18: "Lineage Is Part of the Claim" — citation philosophy
- S15.19: "From Lineage to Implications" — transition to Section 16

**Key formulations:**

1. "The framework does not claim ownership over the ingredients. It claims responsibility for the mix." (v0.2 S15 opening)
2. "The contribution is not inventing the grapes. The contribution is the blend." (v0.2 S14.16 transition)
3. "The framework is a bridge among its influences, not a replacement for them." (v0.2 S15)

### Related Traditions Already Implicit in Sections 1–9

Citations already present in the manuscript (24 unique citations across S1–S4):

| Tradition | Already cited | Section |
| --- | --- | --- |
| AI safety / agentic risk | Lynch et al. 2025 | S1 |
| Behavioral description | Shanahan et al. 2023 | S1 |
| Organizational memory | Walsh & Ungson 1991, Alavi & Leidner 2001 | S2 |
| Organizational decision theory | March & Simon 1958 | S2 |
| AI / agents | Russell & Norvig 2020 | S3 |
| Intentional stance | Dennett 1987 | S3 |
| Sensemaking | Weick 1995 | S3 |
| Information behavior | Wilson 1999, Kuhlthau 1991, Bates 1989 | S3 |
| Situation awareness | Endsley 1995 | S3 |
| Affordances | Gibson 1979, Norman 1988 | S3, S4 |
| Reward shaping | Ng et al. 1999 | S4 |
| Bounded rationality | Simon 1955 | S4 |
| Information foraging | Pirolli & Card 1999 | S4 |
| Decision theory | Howard 1966, Russell & Wefald 1991 | S4 |
| Hallucination | Maynez et al. 2020, Ji et al. 2023, Huang et al. 2023 | S4 |
| Trust in automation | Lee & See 2004, Parasuraman & Riley 1997 | S4 |

**Not yet cited in manuscript body (S5–S9 have zero inline citations):**

All v0.2 S15 citations for traditions not yet named in the manuscript:
- Argyris & Schön 1978 (organizational learning)
- Cyert & March 1963 (behavioral theory)
- Lewis et al. 2020, Menick et al. 2022, Yu et al. 2024 (RAG/grounding)
- OpenAI 2025, Google DeepMind 2024 (AI governance)
- Shanahan 2022 (behavioral description — book)
- Moreau et al. 2013, Lee 1997 (provenance/design rationale)
- Amershi et al. 2019, Horvitz 1999, Johnson et al. 2014 (HCI/mixed-initiative)
- Aamodt & Plaza 1994 (case-based reasoning)
- Guo et al. 2017, Kadavath et al. 2022 (calibration)
- de Clippel & Rozen 2024 (bounded rationality)

### Traditions Reserved for Section 10

All 15 traditions from v0.2 S15 should be at least named. But v1.0 compresses from 15 subsections to a compact table + brief narrative synthesis.

---

## Core Claim of Section 10

> The framework does not claim to invent its ingredients. It claims responsibility for the blend.

The synthesis is:

> Human-agent systems should preserve optimizer state transitions as reusable reasoning objects, and the environment of information, confidence, representation, connectivity, and visibility shapes what becomes sufficient.

No single tradition makes this claim. The framework arranges them.

---

## Traditions to Name

All 15 traditions from v0.2 S15 should appear in the lineage table. In prose, the most important clusters are:

**Cluster 1: Why agents stop** — bounded rationality, satisficing, sufficiency

**Cluster 2: Why organizations forget** — organizational learning, knowledge management, sensemaking

**Cluster 3: Why environments shape action** — affordances, reward shaping, information behavior

**Cluster 4: Why context retrieval alone is not enough** — RAG/grounding, decision rationale, provenance

**Cluster 5: Why human-agent systems need design** — AI safety, human-centered AI, mixed-initiative, calibration

---

## What the Framework Borrows

| Source tradition | What is borrowed |
| --- | --- |
| Bounded rationality | Agents act under limits; sufficiency is a stopping condition, not optimal completion |
| Organizational learning | Learning changes the model, not just the action; single vs. double loop |
| Sensemaking | Actors construct meaning; interpretation shapes perception |
| Affordances | Environments invite and constrain action through design |
| Reward shaping | Designed pressures influence which paths feel attractive |
| RAG / grounding | Context retrieval improves fluency and accuracy |
| Knowledge management | Organizational memory requires structure, retrieval, and reuse |
| Decision rationale | Why-reasoning matters for audit, governance, and future use |
| AI safety | Agent behavior requires inspectability, governance, and boundaries |
| Human-centered AI | Discovery is collaborative, not extractive; burden matters |
| Calibration | Confidence should be explicit, not hidden |
| Case-based reasoning | Prior cases inform future reasoning |

---

## What the Framework Adds

The framework's contribution is not any single concept. It is the synthesis:

1. **Perceived topography as the unit of analysis.** The environment of visibility, accessibility, representation, confidence, and connectivity shapes what becomes sufficient. Not just affordances (action availability) but the full information landscape.

2. **Premature sufficiency as a shared diagnostic.** Hallucination, harmful action, weak decisions, and organizational repetition share a common motion structure: reaching "good enough" too early.

3. **Reasoning-state architecture.** Six objects preserve the optimizer state transition, not just the artifact or the outcome. Learning requires preserved reasoning, not just stored documents.

4. **Discovery as infer-confirm.** Tacit reasoning becomes reusable through Retrieve → Infer → Propose → Confirm, not through forms or silent inference.

5. **Model Update Objects as durable learning.** Learning is not correction, reaction, postmortem, or storage. It is evidence-supported model change with confidence, applicability, and provenance.

6. **The blend itself.** Arranging bounded rationality, organizational learning, sensemaking, affordances, reward shaping, RAG, safety, governance, HCI, and decision rationale into a unified design layer for human-agent systems.

---

## Candidate Section Movement

### Recommended narrative arc (~1,000–1,500 words)

**Movement 1: This is a synthesis, not a claim of invention (~150 words)**

Open by establishing intellectual humility. The framework borrows from established traditions. It does not claim to have invented bounded rationality, sensemaking, affordances, or organizational learning. Its contribution is the blend.

Key formulation: "The framework does not claim ownership over the ingredients. It claims responsibility for the mix."

**Movement 2: The lineage table (~400 words including table)**

Present Table 10 showing the traditions, what each contributes, and what the framework adds.

The table should be compact — one row per tradition, with short entries. The prose around the table should organize the traditions into clusters rather than walking through each one separately.

**Movement 3: What the blend produces (~250 words)**

Name the specific synthesis contributions:
- Perceived topography as the unit of analysis
- Premature sufficiency as shared diagnostic
- Reasoning-state architecture
- Discovery as infer-confirm
- Model Update Objects as durable learning

Each in 1–2 sentences. Not a replay of prior sections — a naming of what the blend produces that no single tradition provides alone.

**Movement 4: Why lineage strengthens the claim (~150 words)**

Close by explaining that lineage is not a weakness. A framework with deep roots is more trustworthy than a framework with none. The traditions named here have been tested, criticized, refined, and applied across decades of research and practice.

The framework's job is to show that those traditions, when arranged around the problem of human-agent reasoning-state preservation, produce a design language that is more useful than any single tradition alone.

End by creating the need for Section 11: if the framework is rooted, bounded, testable, and synthesized from established traditions, what should builders do with it?

---

## Visual and Table Plan

### Table 10: Roots of the Perceived Topography Framework (confirmed)

**12-row table. Citations placed in the Tradition column using compact author-year format.**

| Tradition | What it contributes | What this framework adds |
| --- | --- | --- |
| Bounded rationality and satisficing (Simon, 1955) | Agents act under limits; sufficiency is a stopping condition | Sufficiency as preserved, auditable state inside reasoning architecture |
| Organizational decision and learning theory (March & Simon, 1958; Cyert & March, 1963; Argyris & Schön, 1978) | Organizations make decisions under limits; learning changes the model, not just the action | Six-object chain formalizes what must be preserved for learning across human-agent systems |
| Sensemaking (Weick, 1995) | Actors construct meaning under ambiguity | Optimizer Interpretation made explicit and correctable |
| Affordances (Gibson, 1979; Norman, 1988) | Environments invite and constrain action | Topography extends affordance to visibility, confidence, connectivity |
| Reward shaping (Ng et al., 1999) | Designed pressures shape behavior | Gradient as broader systems-level notion across organizational context |
| RAG / grounding (Lewis et al., 2020; Menick et al., 2022) | Context retrieval improves accuracy | Context retrieval insufficient without reasoning-state preservation |
| Knowledge management (Alavi & Leidner, 2001; Walsh & Ungson, 1991) | Organizations need structured memory | Reasoning architecture preserves transitions, not just artifacts |
| Decision rationale / provenance (Lee, 1997; Moreau et al., 2013) | Why-reasoning matters for governance | Six objects as provenance structure for adaptive reasoning |
| AI safety, governance, and behavioral description (Lynch et al., 2025; Shanahan et al., 2023) | Agent behavior must be bounded, inspectable, and described without false minds | Landscape design, not just containment; topography shapes safety |
| Human-centered AI (Amershi et al., 2019; Horvitz, 1999) | Collaboration and burden reduction matter | Discovery creates reasoning objects through infer-confirm |
| Calibration (Guo et al., 2017; Kadavath et al., 2022) | Confidence should be explicit | Confidence as topography dimension; abstention as sufficiency action |
| Case-based reasoning (Aamodt & Plaza, 1994) | Prior cases inform future decisions | MUO organized around model change, not similarity |

**Table number:** Table 10 (follows Table 9 in Section 9).

**Argumentative job:** Make the lineage visible and compact. Show at a glance what is borrowed and what is added. Prevent the section from becoming a list of subsections walking through each tradition.

**Placement:** Movement 2.

### Figure Recommendation (confirmed)

**No figure.** Section 10 is about intellectual positioning, not process or architecture. A figure would not add argumentative value here.

---

## Citation and Reference Needs

### Citations already present in manuscript (S1–S4)

24 unique citations. Major traditions already cited: Simon, March & Simon, Weick, Gibson, Norman, Ng et al., Dennett, Russell & Norvig, plus information behavior, situation awareness, hallucination, and trust-in-automation literature.

### Citations needed for Section 10 lineage table

Most traditions cited in v0.2 S15 are not yet cited in the v1.0 manuscript body (S5–S9 have zero inline citations). Per resolved decision #2, citations appear in the Tradition column of Table 10 using compact author-year format. Each tradition row carries at least one citation:

| Tradition | Needed citation | Status in manuscript |
| --- | --- | --- |
| Bounded rationality | Simon 1955 | Already cited (S4 line 361) |
| Organizational learning | Argyris & Schön 1978 | Not yet cited |
| Org decision theory | March & Simon 1958, Cyert & March 1963 | March & Simon cited (S2 line 141) |
| Sensemaking | Weick 1995 | Already cited (S3 line 242) |
| Affordances | Gibson 1979, Norman 1988 | Already cited (S3 line 304) |
| Reward shaping | Ng et al. 1999 | Already cited (S4 line 355) |
| RAG / grounding | Lewis et al. 2020, Menick et al. 2022 | Not yet cited in body |
| KM | Alavi & Leidner 2001, Walsh & Ungson 1991 | Already cited (S2 line 141) |
| Decision rationale | Lee 1997, Moreau et al. 2013 | Not yet cited |
| AI safety | Lynch et al. 2025 | Already cited (S1 line 40) |
| HCI / mixed-initiative | Amershi et al. 2019, Horvitz 1999 | Not yet cited in body |
| CBR | Aamodt & Plaza 1994 | Not yet cited |
| Calibration | Guo et al. 2017, Kadavath et al. 2022 | Not yet cited |

**Risk:** Section 10 will need to cite ~8–10 sources that have not yet appeared in the manuscript. This is appropriate for a lineage section. The drafter should add inline citations for each tradition when referencing it.

**Risk of overclaiming:** Any tradition listed without a citation risks sounding like unsupported name-dropping. Each row in the lineage table should have at least one citable source.

---

## Boundary Conditions

### Do Not Reopen Section 9

Section 9 already handled:
- Limits and boundaries
- Objections
- Disconfirmation conditions
- Misuse risks
- Evidence boundary

Section 10 may briefly note the framework is bounded and testable, but should not reopen the debate.

### Do Not Become Literature Review

Section 10 is not a survey paper. It should:
- Name traditions, not review them
- Show what is borrowed, not what each tradition says in full
- Use the lineage table to compress what v0.2 spread across 15 subsections

v0.2 S15 had 15 subsections, each walking through a tradition. v1.0 should compress to a table + 2–3 paragraphs of synthesis. The reader needs to see the roots, not read summaries of each field.

### Do Not Become the Conclusion

Section 11 is the close. Section 10 should end by handing Section 11 the idea:

> The framework is rooted, bounded, testable, and synthesized. The remaining question is what builders should do with it.

---

## Drafting Risks

### Section 10 as Literature Review

If Section 10 walks through each tradition in a separate paragraph (as v0.2 did), it becomes 15 mini-reviews. The lineage table prevents this by compressing the mapping into a scannable format.

### Over-Citation Anxiety

If the drafter tries to cite every influence thoroughly, Section 10 becomes citation-heavy and loses momentum. One citation per tradition in the table is enough. Deeper engagement belongs in later scholarship.

### Under-Citation

If the drafter names traditions without citing anyone, the section sounds unsupported. Each row in the table should have at least one [Author, Year].

### Claiming Too Much Originality

If Section 10 overstates what the framework adds, it contradicts the humility posture. The contribution is the blend, not the ingredients.

### Claiming Too Little

If Section 10 only lists what was borrowed, the reader may wonder why the framework exists. The "what this framework adds" column must show genuine synthesis.

### Burying the Synthesis Under Names

If the names and citations dominate, the reader loses the synthesis. The prose should lead with what the blend produces, not with a chronological history of ideas.

### Repeating Sections 1–9

If Section 10 explains each concept again to show its lineage, it replays the paper. The lineage table should reference concepts the reader already holds, not re-teach them.

---

## Specific Questions Answered

1. **What is the central job of Section 10?** Establish intellectual legitimacy by showing the framework's roots in existing traditions and clarifying what the synthesis adds beyond any single tradition.

2. **What exact problem does Section 9 hand off?** No explicit handoff. Section 9 closes the rigor gate. Section 10 answers the implicit next question: where does this come from?

3. **What older content should be preserved?** The lineage table structure from v0.2 S15 (15 traditions). The key formulations: "The framework does not claim ownership over the ingredients. It claims responsibility for the mix." The "blend" metaphor.

4. **What traditions must be named?** All 15 from v0.2 S15, compressed into a table. In prose, the five clusters: why agents stop, why organizations forget, why environments shape action, why retrieval alone is not enough, why human-agent systems need design.

5. **What does the framework borrow?** See "What the Framework Borrows" section above.

6. **What does the framework add?** Perceived topography as unit of analysis, premature sufficiency as shared diagnostic, reasoning-state architecture, Discovery as infer-confirm, MUOs as durable learning, and the blend itself.

7. **What should Section 10 not claim?** That any single concept is invented here. That the framework replaces any tradition it draws from. That the blend is the only possible synthesis.

8. **What should be deferred?** Deep engagement with any single tradition. Exhaustive citation. Positioning against every related framework. Empirical comparison with alternative approaches.

9. **Should Section 10 include a table?** Yes — Table 10: Roots of the Perceived Topography Framework. 12 rows, 3 columns.

10. **What would make Section 10 strengthen the paper?** Showing that the framework is rooted in decades of established research, that its concepts are not ad hoc, and that the synthesis produces something genuinely useful for human-agent system design that no single tradition provides alone.

---

## Drafting Guidance

- Do not replay Sections 1–9. Reference concepts the reader already holds.
- Do not walk through each tradition in a separate paragraph. Use the table.
- Do not over-cite. One citation per tradition row is sufficient.
- Do not under-cite. Each tradition needs at least one source.
- Do not reopen objections or falsifiability. Section 9 handled that.
- Do not write the conclusion. Section 11 closes.
- Lead with the synthesis claim, not with the list of influences.
- Make the "what this framework adds" column the strongest column in the table.
- End by creating the need for Section 11: what should builders do?
- Avoid manuscript self-reference.
- Keep the section short. ~1,000–1,500 words.

v0.2 S15 was ~1,900 words across 19 subsections. v1.0 should be shorter because:
- The lineage table compresses 15 tradition subsections into one table
- Many traditions are already cited in Sections 1–4
- The synthesis claim can be stated in 3–5 sentences, not a full subsection
- The "boundaries keep the claim honest" subsection (v0.2 S15.17) is now covered by Section 9

Reader comprehension governs.

---

## Resolved Authorial Decisions

All five authorial questions resolved on 2026-06-19:

1. **Table row count:** ~~RESOLVED.~~ 12 rows. The table preserves the lineage without expanding into a literature review. Each row adds without overwhelming.

2. **Citation placement:** ~~RESOLVED.~~ Citations appear in the Tradition column of Table 10 using compact author-year format (e.g., "Bounded rationality and satisficing (Simon, 1955)"). This keeps the table self-contained.

3. **Behavioral description tradition (Shanahan):** ~~RESOLVED — folded.~~ Folded into the "AI safety, governance, and behavioral description" row alongside Lynch et al. The behavioral-description point (avoid anthropomorphism) is already conceptually handled in Section 1 and does not need its own table row.

4. **Behavioral theory of the firm (Cyert & March):** ~~RESOLVED — merged.~~ Merged into the "Organizational decision and learning theory" row alongside March & Simon and Argyris & Schön. The distinction matters in academic context but not for the lineage table's argumentative job.

5. **Prose-to-table ratio:** ~~RESOLVED.~~ Table as centerpiece. Structure: 2–3 opening paragraphs establishing the synthesis claim → Table 10 as the central lineage device → 2–3 closing paragraphs naming what the blend produces and handing off to Section 11. Do not walk through each tradition in a separate paragraph.

---

## Verification Notes

- Section 10 placeholder in manuscript: `NOT YET DRAFTED` (line 2172)
- Section 10 arc comment preserved: "Intellectual lineage -> what is borrowed -> what is synthesized -> 'blend, not invention' -> 'over-cite by design' -> lineage table." (lines 2169–2171)
- Rewrite queue status for Section 10: will update to "Source packet ready"
- No v1.0 manuscript edits made
- No existing source/review packets edited
- No figures or SVGs edited
- SESSION_START.md not edited
