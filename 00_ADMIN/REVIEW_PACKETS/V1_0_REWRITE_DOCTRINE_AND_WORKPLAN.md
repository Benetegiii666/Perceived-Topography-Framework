# v1.0 Rewrite Doctrine and Editorial Workplan

---

## 1. Why This Paper Exists

The paper exists to change the question people ask about AI systems.

Not only:

> How do we make the agent less scary?

But:

> What kind of world are we asking the agent to move through, and what reasoning survives after it acts?

The paper's purpose is to give builders, product leaders, and organizations a way to diagnose AI behavior, preserve the reasoning behind decisions, and design human-agent systems that learn instead of repeating the same mistake with better tools.

---

## 2. Elevator Answer

Working elevator answer:

> This paper argues that safer AI is not only about controlling agents; it is about designing the landscapes they move through. AI systems act based on what is visible, trusted, connected, and treated as sufficient. If we want better behavior, we need to preserve the reasoning behind decisions, not just the documents and outputs. The goal is to help human-agent systems learn from what happened so the next cycle starts smarter.

Shorter version:

> The paper is about moving from fear of AI agents to design of the environments that shape them.

---

## 3. v1.0 Rewrite Doctrine

```
v1.0 is an arc-preserving compression, not a shortening exercise.
Reader comprehension is the target. Compression is only a method.
```

v1.0 should not be optimized for economy. It should be optimized for rightness, completeness, and the reader's ability to explain the theory arc cogently after reading this work alone.

The goal is to eliminate pontification — repeated derivation, recap-as-section, defensive prose that does not advance the argument — but never at the expense of clearly landing comprehension. If a passage helps the reader explain the framework more cogently, it stays. If it merely restates what the reader already holds, it goes.

### Compression Target Posture

```
Target: complete standalone arc.
Minimum body threshold: ~15,000 words.
Expected body range: determined by completeness chunk by chunk.
Compression guide: useful, but subordinate to reader comprehension.
```

15,000 words is the minimum body threshold, not the target ceiling. The rewrite should proceed chunk by chunk. Each chunk should be judged by whether it advances the complete standalone arc. If preserving the arc requires exceeding the estimated target, the paper should exceed the target.

```
Do not cut for length alone. Cut, compress, move, or visualize only
when doing so improves the reader's understanding of the theory arc.
```

### Section-Level Comprehension Test

Every section in the v1.0 draft should pass this test:

```
Does this section help the reader explain the framework more cogently?
If yes, preserve, clarify, or restructure it.
If no, compress, move, visualize, or cut it.
```

**v1.0 should be:**

- Clearer
- More credible
- More explicit about evidence posture
- Less repetitive
- More deliberate about the canonical example
- Stronger against objections
- Grounded in citations where concepts are introduced
- Honest that the framework is pre-empirical
- As short as it can be without sacrificing comprehension

**v1.0 should not:**

- Flatten the discovery arc
- Cut the aha moments
- Pretend a constructed scenario is empirical proof
- Turn into a product spec
- Become a citation dump
- Bounce between too many examples
- Preserve repetition merely because it already exists
- Cut for length at the expense of reader comprehension

---

## 4. Body of Work Strategy

v1.0 should be treated as the keystone systems paper for a broader Perceived Topography body of work. It should introduce the core frame, preserve the aha arc, establish the central argument, honestly state the evidence posture, and create the foundation for future academic, product, and practitioner artifacts.

The paper should not try to fully satisfy every possible audience at once.

```
v1.0 is the complete standalone theory paper. It is also the keystone
of a broader body of work. Later artifacts extend, operationalize,
validate, or specialize the framework; they do not complete the argument.
```

### The Body of Work

```
1. Keystone systems paper
   Purpose: introduce the framework, preserve the discovery arc, establish
   the core argument, and show the logic through one constructed worked scenario.

2. Academic / research track
   Purpose: formalize claims, engage prior literature more deeply, define
   validation methods, and test the framework empirically or comparatively.

3. Product / design track
   Purpose: translate the framework into operating principles for teams
   building human-agent workflows, reasoning-state systems, discovery loops,
   and learning mechanisms.

4. Practitioner / tooling track
   Purpose: provide worksheets, interviews, canvases, schemas, facilitation
   guides, and implementation templates.
```

### v1.0 Implication

```
v1.0 does not need to carry the full burden of the academic paper,
the product architecture paper, and the practitioner toolkit. It must
be strong enough that those later artifacts can grow from it coherently.
```

### Standalone Arc Requirement

The v1.0 paper must be readable as a complete work. A reader should be able to explain the full theory arc after reading v1.0 alone, even if they never read any later academic, product, toolkit, or case-study documents.

The primary reader may never encounter the academic paper, the product paper, the toolkit, or the case-study series. Therefore, v1.0 must carry the complete conceptual arc by itself. Follow-on works are satellites, not missing chapters.

**Complete arc that must be preserved in v1.0:**

```
Fear of AI agents
  -> wrong question: "What is wrong with the agent?"
  -> better question: "What landscape shapes behavior?"
  -> optimizer state
  -> perceived topography
  -> gradients
  -> sufficiency
  -> premature sufficiency
  -> failure
  -> learning
  -> reasoning-state preservation
  -> Discovery
  -> Model Update Objects
  -> validation / falsifiability
  -> Appendix A as a starting method
```

**Not deferrable from v1.0:**

- The full conceptual argument
- The fear-to-landscape reframe
- The topography and gradient model
- The sufficiency / premature-sufficiency failure model
- The reasoning-state preservation claim
- The learning / Model Update Object logic
- The Discovery logic
- The falsifiability posture
- A practical starting point through Appendix A

**Deferrable to later works:**

- Full product architecture
- Full implementation schemas
- Facilitation workbook
- Empirical study design
- Multiple case studies
- Implementation templates
- Deep academic literature expansion

**Compression rule:**

```
Cut anything that repeats the arc without advancing it.
Do not cut anything the reader needs in order to explain the arc.
```

### Track Table

| Track | Purpose | What belongs there | What v1.0 should retain | What v1.0 can defer |
| --- | --- | --- | --- | --- |
| Keystone systems paper | Introduce the framework, preserve the aha arc, establish the core argument | Core reframe, optimizer/topography/motion/learning model, premature sufficiency, context-vs-reasoning-state, Discovery principle, falsifiability, one constructed worked scenario, Appendix A | Everything listed. This IS v1.0. | Nothing — this is the primary deliverable. |
| Academic / research paper | Formalize claims, deep literature engagement, validation design, empirical testing | Full citation expansion, formal dimension independence analysis, inter-rater reliability study, comparative evaluation (context-only vs. reasoning-state), detailed positioning against every related tradition | Enough citation grounding for credibility. Pre-empirical framing. Section 14 falsifiability. Section 15 lineage (compressed). | Deep engagement with every tradition. Full empirical validation design. Formal mathematical treatment of gradients/sufficiency. Inter-rater reliability study design. |
| Product / design track | Operating principles for builders | Implementation architecture, component model, data schema, maturity model, integration patterns, API contracts, reasoning-object lifecycle, MUO governance workflow | Maturity model (S13.10). "Do Not Start With the Whole Machine" (S13.11). MUO concept and eleven-field spec. Discovery loop interaction pattern. | Full JSON schema. Component table. Detailed lifecycle management. Integration with specific platforms. Governance workflow details. |
| Practitioner / tooling track | Worksheets, interviews, canvases, facilitation guides, templates | Decision Topography Interview (full 23 questions). Minimal-interview variant. Facilitation guide (who, how long, what to bring). Diagnostic canvases. MUO templates. Dimension diagnostic worksheets. | Appendix A (full interview, practical bridge). | Facilitation guide details. Workshop curriculum. Diagnostic canvases. MUO fill-in templates. Dimension worksheets. Minimal-interview variant (can be deferred or kept as brief table in Appendix A). |
| Case study / simulation series | Multiple worked examples across domains | Healthcare campaign (full depth). Incident response case. Compliance review case. Customer support case. Sales enablement case. Each analyzed through full framework. | One canonical constructed worked scenario (healthcare campaign). Optional: one tiny contrast example (2-3 paragraphs) for portability. | All additional domain examples. Full multi-domain simulation series. Real-world retrospective analyses. |
| Model Update Object specification | Full MUO design, lifecycle, governance, retrieval | Eleven-field core payload. Observability envelope. Human-ready view. Lifecycle states (Draft -> Provisional -> Validated -> Deprecated -> Superseded). Retrieval logic. Conflict resolution. Trust calibration. | MUO concept. Eleven-field spec. Ten failure modes. One filled example. | Full lifecycle governance. Retrieval UX design. Conflict resolution logic. Trust calibration mechanisms. Schema versioning. |
| Premature Sufficiency / failure diagnosis paper | Deep treatment of the hallucination/harmful-action unification | Premature sufficiency as shared motion pattern. Detailed case analyses. Empirical testing against hallucination taxonomies. Positioning against existing failure classification systems. Connection to trust-in-automation literature. | Core argument (S7). Compliance example. Structural parallel. | Empirical case analyses. Positioning against full hallucination survey literature. Formal failure taxonomy. Connection to systems-safety accident models (STAMP/STPA). |

### Implications for v1.0 Compression

- **The arc must remain complete.** Every step from fear-to-landscape through Appendix A must be present in v1.0. The reader must be able to explain the full theory after reading v1.0 alone.
- **Compression should remove repeated derivation, not required conceptual steps.** If a concept appears three times, keep the best statement and bridge the others. Do not remove the concept.
- **Later body-of-work tracks may deepen the framework, but v1.0 must still stand alone.** A reader who never encounters the academic paper, the product paper, or the toolkit should still hold a complete understanding of the framework.
- **The keystone paper should teach the frame and prove it is worth taking seriously.** It must be intellectually credible (citations, falsifiability, honest evidence posture) without requiring a companion paper to fill gaps.
- **Follow-on works are satellites, not missing chapters.** They extend, operationalize, validate, or specialize. They do not complete.
- **Move excessive implementation detail toward the product/design track.** JSON schemas, component tables, and detailed lifecycle governance overload the systems paper.
- **Move deep citation expansion and empirical validation design toward the academic/research track,** while keeping enough citation grounding in v1.0 for credibility. Every construct needs at least one inline citation, but exhaustive literature engagement belongs in a follow-up.
- **Keep Appendix A in v1.0 as the practical bridge,** but do not turn it into a full workbook. Facilitation guides, canvases, and templates belong in the practitioner track.
- **Preserve the Model Update Object concept in v1.0,** but defer full schema/tooling details to the product or practitioner track if they overload the paper.
- **Use one canonical constructed worked scenario in v1.0,** and reserve additional examples for a case/simulation series.

---

## 5. Aha / Arc Preservation Spine

The reader must experience this journey:

```
Fear of AI agents
  -> wrong question: "What is wrong with the agent?"
  -> better question: "What landscape shapes behavior?"
  -> agents move through perceived topography
  -> gradients make some paths easier than others
  -> bad behavior often comes from premature sufficiency
  -> modulate visibility, accessibility, representation, confidence, and connectivity
  -> preserve reasoning state, not just context
  -> learning means the next cycle starts differently
  -> Appendix A gives people a way to start
```

| Aha / insight | Why it matters | v0.2 location | Required v1.0 location | Treatment | Notes |
| --- | --- | --- | --- | --- | --- |
| Marble / landscape reframe | Makes the core reframe intuitive before any terminology. Single most effective moment in the paper. | S1, ~line 29 | S1, first page. Consider abstract. | Preserve | Universally praised. Do not move later. |
| Context is not reasoning state | Names a real gap every org recognizes: retrieval gives *what* but not *why*. | S3 (entire section) | S3 | Preserve | Strongest section per 4/6 reviewers. Do not compress. |
| Behavior follows gradients | Shifts from static description to dynamic motion model. | S6 | S6 | Compress lightly | Concept is clear; surrounding prose can be trimmed. Sufficiency-vs-certainty 2x2 must survive. |
| Sufficiency is not certainty | Immediately usable design heuristic. | S6.5 | S6 | Preserve | Praised by 3/6 reviewers. |
| Hallucination and harmful action share premature sufficiency | Paper's most original intellectual contribution. Connects two research domains through shared mechanism. | S7 | S7 | Preserve core; compress exposition | 5/6 reviewers identified as strongest contribution. Compliance example ("reduces readmissions") must survive. |
| Learning is not memory or reaction | Rigorous distinction that prevents the most common organizational learning failure. | S8.8 | S8 | Preserve | Well-anchored in Argyris & Schon. |
| Model Update Objects preserve lessons as reusable changes | Most concrete, falsifiable, implementable claim. | S9 | S9 | Preserve concept; address KM graveyard risk | 11-field spec and 10 failure modes are assets. |
| Discovery reduces user burden by inferring before asking | Most product-ready construct. "Do the reasoning work before asking the user." | S11 | S11 | Preserve | Most practically important design heuristic per 3/6 reviewers. |
| Reasoning-state preservation is the missing design layer | The paper's central design claim, pulling together all preceding ahas. | S1, S3, S10, S16 | S1 (stated), S3 (argued), S10 (architected) | Preserve; reduce restatements in S16 | Currently restated too many times. State clearly, argue once, architect once. |
| Appendix A makes the framework usable | Transforms theory into facilitation tool. A team could use it Monday morning. | Appendix A | Appendix A | Preserve; add facilitation guidance | Most actionable section per 4/6 reviewers. |

---

## 6. Dimension Admission Test

### The Reviewer Critique

4/6 reviewers challenged why the framework uses five topography dimensions:

```
Visibility
Accessibility
Representation
Confidence
Connectivity
```

instead of candidate alternatives such as:

```
Timeliness
Salience
Completeness
Relevance
Trust
Policy
Memory
```

The v1.0 answer should not be "trust us." It should show the selection logic.

### Admission Principle

```
A dimension earns its place only if changing it would lead to a different diagnosis,
intervention, or expected outcome.
```

The five dimensions are not offered as a closed ontology of information. They are offered as a minimum viable diagnostic set. A candidate dimension should be promoted only if it produces a distinct failure diagnosis and a distinct design intervention. If it does not, it should be treated as a subcase, consequence, interaction effect, or different layer.

### Candidate Dimension Assessment

| Candidate dimension | Why a reader may expect it | Likely treatment in v1.0 | Promote only if | Notes |
| --- | --- | --- | --- | --- |
| Timeliness | Stale information is a common failure mode. "The policy was updated last week but the agent used the old version." | Subsumed. Stale information is a Confidence problem (trust degrades with age), an Accessibility problem (current version not reachable), or a Visibility problem (update not surfaced). Treatment depends on which mechanism failed. | Timeliness produces a diagnosis that none of the existing five can produce. | If removing Confidence, Accessibility, and Visibility still leaves a timeliness failure undiagnosed, promote. Otherwise, treat as interaction effect. |
| Salience | Information can be technically present but not noticed. "The policy was in the context window but buried among 50 other documents." | Subsumed by Visibility (was the signal noticeable?) and Representation (was it formatted to stand out?). A salience failure is typically a Visibility failure (signal present but not prominent) or a Representation failure (signal present but not in a form the optimizer can act on). | Salience produces a distinct intervention that differs from improving Visibility or Representation. | Current treatment: salience is the behavioral consequence of low Visibility or poor Representation, not an independent dimension. |
| Completeness | "The system only retrieved 3 of 5 relevant documents." | Emergent from the interaction of all five dimensions. Incomplete information is usually a Visibility problem (some signals not surfaced), an Accessibility problem (some sources not reachable), or a Connectivity problem (retrieved information not linked to what makes it relevant). Sufficiency (Section 6) is the framework's mechanism for handling completeness at the decision level. | Completeness produces a distinct diagnosis that is not captured by any combination of the five dimensions plus the sufficiency mechanism. | Completeness is a system-level property, not a single dimension. The framework addresses it through the sufficiency threshold, not through a sixth dimension. |
| Relevance | "The system retrieved accurate information, but it was not relevant to the current goal." | Projection from the active Goal, not a topography dimension. Relevance is what the Goal does to the topography: it determines which information matters. Section 4 treats Goal as an optimizer-state primitive, not a landscape property. | Relevance produces a distinct intervention that differs from clarifying the Goal or improving Connectivity (which links information to the goal context). | If Goal and Connectivity together cannot explain a relevance failure, promote. Otherwise, treat as a consequence of goal-information interaction. |
| Trust | "The system used a source it should not have trusted." | Closely related to Confidence but may produce a distinct intervention in some cases. Confidence in the current framework describes how trustworthy a signal appears to the optimizer. Trust may involve a relational or institutional dimension (who produced the signal, under what authority) that is not fully captured by perceived signal reliability. | Trust produces a diagnosis or intervention that Confidence cannot. For example: a signal has high perceived reliability but low institutional authority. | This is the strongest candidate for future promotion. v1.0 should acknowledge the overlap and state that Confidence currently carries the trust function. If empirical use reveals cases where Confidence fails but Trust would succeed, the dimension should be reconsidered. |
| Policy | "The policy existed but the system did not follow it." | Belongs to optimizer state (Section 4), not topography. A policy is a constraint on the optimizer, not a property of the landscape. However, policies must be made Visible, Accessible, well-Represented, Confident (authoritative), and Connected in the topography to exert behavioral force. Policy failures are diagnosed through the five dimensions applied to policy signals. | Policy-as-dimension produces a diagnosis that the five dimensions applied to policy signals cannot. | v1.0 should clarify that policy is an optimizer-state primitive whose behavioral effectiveness depends on how well it is represented in the topography. |
| Memory | "The system forgot what happened last time." | Belongs to artifact/context storage or reasoning-state preservation, not the information topography itself. Memory is the substrate from which information surfaces become available. The framework addresses memory failure through the MUO and reasoning-state architecture (Sections 9-10), not through a topography dimension. | Memory-as-dimension produces a diagnosis that Visibility (was the prior learning surfaced?), Accessibility (was it retrievable?), and Connectivity (was it linked to the current decision?) cannot. | Memory is infrastructure. The topography describes what the optimizer perceives; memory is where some of that perception originates. |

### Reader-Facing Rule

```
If naming a candidate changes what the designer would diagnose or do,
it may deserve promotion. If it does not, it should not multiply the
framework's vocabulary.
```

v1.0 should include this logic (compressed) in Section 5 after the five dimensions are defined, and should explicitly name the strongest excluded candidates with brief explanations. This is not defensive prose — it is evidence that the framework has been stress-tested against alternatives.

---

## 7. Example Strategy

**Doctrine:**

```
Use one canonical worked simulation, not many competing examples.
```

**Primary example:** Healthcare / RPM / cardiology / readmissions campaign

**Why this example works:**

- Real business goal (demo requests for RPM product)
- Policy constraint (healthcare marketing compliance)
- Persuasion risk (clinical outcome claims)
- Evidence ambiguity (workflow pain vs. buying readiness)
- Repeated workflow (quarterly campaigns)
- Learning loop (performance data creates prediction error)
- Clear premature-sufficiency failure (workflow pain attracted attention but did not indicate buying readiness)

**Evidence posture:** The healthcare case must be framed as a constructed worked scenario, not empirical validation.

**Required framing language** (or equivalent, to appear at first full introduction of the example):

> The following is a constructed scenario used to stress-test the framework. It is not presented as empirical validation. Its purpose is to show how the framework produces different diagnoses and interventions than a context-only or better-RAG approach.

**Current example density by section** (campaign-related lines):

| Section | Campaign references | Assessment |
| --- | --- | --- |
| S1 | 3 | Appropriate (brief foreshadowing) |
| S3 | 15 | Appropriate (first full introduction) |
| S4 | 12 | Heavy (re-derives Goal/Policy/Interpretation through campaign) |
| S5 | 20 | Heavy (re-derives all five dimensions through campaign) |
| S6 | 20 | Heavy (re-derives motion through campaign) |
| S7 | 6 | Appropriate (compliance example is distinct and valuable) |
| S8 | 23 | Heavy (learning loop walkthrough) |
| S9 | 17 | Moderate (MUO example is useful) |
| S10 | 10 | Moderate (architecture walkthrough) |
| S11 | 15 | Moderate (Discovery walkthrough) |
| S12 | 34 | Heavy (full end-to-end re-walk) |
| S13 | 5 | Light |
| S14 | 5 | Light |

**v1.0 example plan:**

- **Keep full** in S3 (first introduction), S7 (compliance example is distinct), S9 (MUO filled example)
- **Compress to brief bridge references** in S4, S5, S6, S10
- **Restructure S12** from narrative re-walk to compressed end-to-end trace table
- **Reduce S8** to the learning loop structure with brief campaign illustration (not full narrative replay)

**Optional contrast example:** Allow one very small contrast example (2-3 paragraphs maximum) to demonstrate portability. Possible domains:

- Incident response (system acts on stale runbook)
- Customer support escalation (agent bypasses policy under time pressure)
- Compliance review (system reaches sufficiency without checking updated regulation)

The contrast example must not become a second running case. It should appear once, in Section 7 or Section 14, to show that the framework applies beyond marketing.

---

## 8. Repetition Function Audit

Not all repetition is bad. Before cutting, classify by function.

**Classification key:**

| Code | Meaning |
| --- | --- |
| RG | Necessary regrounding (reader needs reminder of concept at this point) |
| RE | Necessary escalation (concept gains new meaning in this context) |
| RB | Necessary bridge between two ideas |
| UR | Unnecessary restatement |
| RR | Redundant example replay |
| CR | Candidate for concise restatement |
| CT | Candidate for table/figure |
| CD | Candidate for deletion |

**Repetition audit:**

| Repeated item | Locations | Function | Keep? | Recommended treatment | Why |
| --- | --- | --- | --- | --- | --- |
| Campaign setup (RPM product, cardiology, practice admins, workflow burden hypothesis) | S1, S3, S4, S5, S6, S8, S9, S10, S11, S12 | S3: RE. S4-S6: RR. S8: RE. S9: RE. S10: RR. S11: RR. S12: RR. | S3, S7, S9: yes. Others: compress. | S3: keep full. S4-S6: reduce to one-line bridge references. S8: keep learning loop structure, trim narrative. S10-S11: reduce to bridge references. S12: convert to trace table. | Example is valued; repetition is not. Reviewers want 2-3 rich appearances, not 10. |
| Goal / Policy / Interpretation definitions | S2, S4.1-S4.3, S4.5, S5.7-S5.8, S6, S10.3, S12 | S2: introduction. S4: primary definition. S4.5: defensive. S5.7-S5.8: defensive. Others: RR. | S4 (primary): yes. S4.5, S5.7, S5.8: compress. Others: bridge only. | S4: keep primary definitions. S4.5: cut by 50% or fold into S4.4. S5.7-S5.8: cut by 50% or fold into footnotes. S10, S12: bridge references only. | Reviewers flagged over-explanation. Concepts are clear on first contact. |
| Five-dimension explanations | S5.2-S5.6, S5.10, S5.11, S6, S7, S10, S12, S14 | S5: primary. S5.10-S5.11: illustrative. S6: escalation. S14: falsification. Others: RR. | S5 (primary), S14: yes. S5.10: compress. Others: bridge only. | S5: keep primary definitions. S5.10 (campaign): compress to brief illustration. S5.11: keep (diagnosis-to-intervention mapping is valued). S12: trace table. | Diagnosis-to-intervention mapping is the practical payoff. Keep that, trim the re-explanations. |
| "Context is not reasoning state" claim | S1, S3, S10.13, S16.3, S17.1 | S1: thesis setup. S3: primary argument. Others: UR/recap. | S1, S3: yes. Others: trim or delete. | S16.3: cut or reduce to one sentence. S17.1: reduce to one sentence. S10.13: keep if it adds new architectural dimension. | The argument is made in S3. Restating it in S16 and S17 adds nothing. |
| Hallucination / harmful action parallel | S1, S6.8, S7.1-S7.3, S7.5, S7.7, S10.12, S12, S16.1 | S1: preview. S6.8: brief motion-model application. S7: primary argument. S10.12, S12, S16.1: recap. | S1 (preview), S6.8 (brief), S7 (full): yes. Others: trim. | S10.12: reduce to bridge sentence. S12: trace table row. S16.1: cut or reduce to one sentence. | The primary argument is in S7. Recaps in S10, S12, S16 are redundant. |
| "Learning is not memory" / reaction vs. learning | S8.8, S8.9, S9.1, S10.13-S10.14, S16.4, S16.9, S17.3 | S8.8: primary distinction. S8.9: practical application (postmortems). S9.1: bridge to MUO. Others: recap. | S8.8, S8.9, S9.1: yes. Others: trim. | S10.13-S10.14: compress. S16.4, S16.9: cut or reduce to one sentence each. S17.3: reduce to one sentence. | Distinction is rigorous in S8. Does not need restating in S16 and S17. |
| Section 16 implications (entire section) | S16.1-S16.14 | Recap/restatement of claims already made in body | Keep 2-3 genuinely new implications. Cut recap items. | Restructure: keep only implications that make NEW claims (e.g., hiring, evaluation criteria, regulatory). Cut subsections that restate body arguments. Target: 50% reduction. | 2/6 reviewers flagged as recap. The section should say what changes, not re-argue why. |
| Section 15 lineage acknowledgments | S15.1-S15.18 | Intellectual honesty / positioning | Keep structure, compress prose. | Reduce from 18 to 8-10 subsections. Merge closely related traditions. Keep "blend not invention" and "over-cite by design." | Academic reviewer valued honesty; practitioner reviewers found it exhausting. |
| Appendix A overlap with main paper concepts | Appendix A questions reference topography, motion, sufficiency, learning | RG: necessary for standalone use | Keep | Appendix A should remain usable without reading the full paper. Overlap is functional. | The overlap is by design and should not be cut. |

---

## 9. Concise Restatement Opportunities

| Current formulation / issue | Location | Problem | Suggested concise direction |
| --- | --- | --- | --- |
| Three-paragraph defense of why Goal, Policy, and Interpretation are sufficient | S4.5 (lines 532-569) | Defensive argumentation that reads as "I considered alternatives." Reader does not need this. | One paragraph: "Other candidates were considered (Capability, Memory, Tools). These are properties of the topography or implementation, not of the working frame itself." |
| Two-subsection defense of why Goal Relevance and Policy are not topography dimensions | S5.7-S5.8 (lines 802-851) | Same defensive pattern. Internal architecture decisions, not reader-facing. | One paragraph or footnote: "Goal Relevance and Policy shape which information matters, but they are properties of the optimizer, not of the landscape. They are treated in Section 4." |
| Full campaign setup re-derived in each of Sections 4, 5, 6 | S4 (~lines 415-490), S5 (~lines 866-901), S6 (~lines 1126-1149) | Reader already has the setup from S3. Re-establishing the scenario adds length without new insight. | One-sentence bridge: "Return to the healthcare campaign. Here, the [concept] is [specific application]." Then proceed directly to the new analytical layer. |
| Section 12 narrative re-walk of entire framework | S12 (lines 2444-2715) | Re-tells the campaign story from start to finish. Most content already shown piecemeal. | Convert to end-to-end trace table: one row per framework stage, columns for concept, campaign application, and what the system does. Add 2-3 paragraphs of commentary on what the trace reveals. |
| Section 16 subsections that restate body arguments | S16.1-S16.14 | "Safety becomes landscape design" was argued in S1, S4, S5, S6, S7. "Context is not reasoning state" was the entire argument of S3. | Keep only subsections that make genuinely new claims about what changes in practice. Cut subsections that begin by restating a concept already fully argued. |
| Section 17 conclusion recapping the entire paper | S17.1-S17.8 (lines 3518-3673) | 155 lines of recap. Each subsection re-summarizes a section already read. | Reduce to ~50 lines. One forward-looking move, not a section-by-section re-summary. |
| Repeated "documents preserve artifacts, reasoning preserves transitions" formulation | S3, S9.1, S10.13, S16.4 | Same claim stated four times in slightly different words. | State once (S3), bridge once (S9.1), do not restate in S10.13 or S16.4. |
| Repeated explanations of what a Model Update Object is | S9.1-S9.3, S10.8, S12, S13 | The object is defined in S9. Later sections re-introduce it. | S9: full definition. S10.8: one-sentence bridge. S12: trace table row. S13: reference only. |

---

## 10. Evidence Posture for v1.0

**Statement:**

v1.0 will not claim empirical validation unless actual empirical evidence exists.

If no real case is available, v1.0 should use:

- Pre-empirical design framework framing
- Constructed worked scenario (with explicit framing)
- Falsifiable claims (Section 14)
- Explicit validation path
- Stronger citation grounding

**Required posture language** (to appear in Section 1, end, or Section 2, beginning):

> This paper proposes a pre-empirical design framework. It offers a conceptual model, a constructed worked scenario, a practical discovery interview, and falsifiable claims for future validation. The framework's central predictions have not yet been empirically tested. Section 14 defines the conditions under which the framework would be confirmed, narrowed, or disconfirmed.

**Prose discipline:** Throughout the paper, avoid declarative statements that imply established findings where the framework has only predictions. Watch for:

- "The result is..." (implies observed result)
- "Learning changes the landscape" (implies demonstrated outcome)
- "The system is not merely remembering; it is reusing learning" (presents prediction as fact)

Replace with:

- "The expected result is..." or "The framework predicts that..."
- "If the learning loop operates as designed, the landscape changes"
- "The system would not merely remember; it would reuse learning"

This does not mean hedging every sentence. The conceptual argument can be stated confidently. But operational outcomes should be framed as predictions, not reports.

---

## 11. Objection Response Requirements

v1.0 must directly address these five objections:

| Objection | Where to address | Response strategy | Needs new prose? | Notes |
| --- | --- | --- | --- | --- |
| "This is just good systems engineering." | S1 (end) or S3 (end) | Concede and sharpen. The framework IS good systems engineering, applied as a unified design layer to human-agent systems. The additions: premature sufficiency as shared diagnostic, reasoning-state architecture, formalized learning loop. Test: show one case where framework diagnosis differs from standard root-cause analysis. | Yes, 1-2 paragraphs | Most important objection to address early. |
| "This is just better RAG plus better prompts." | S3 (after the context-vs-reasoning-state argument) | Draw the boundary. Better RAG gives *what*. Better prompts give *how*. The framework adds *what to preserve* and *how to reuse*. The break point: RAG cannot determine which premise in a prior report later failed. | Yes, 1 paragraph | Critical for builder audience. Place immediately after S3 makes the context argument. |
| "Structured learning objects become KM graveyards." | S9 (after MUO definition) | Name the problem, then position Discovery as the design response. Acknowledge Lotus Notes, SharePoint, ITIL. The difference: Discovery shifts creation burden from humans to inference. Acknowledge the secondary risk: AI-inferred objects may be wrong often enough to erode trust. | Yes, 1-2 paragraphs | 3/6 reviewers raised this. Must be confronted, not deferred. |
| "The framework explains everything post hoc." | S7 (end) or S14 (add subsection) | Acknowledge the risk. State the defense: distinct dimensions must produce distinct interventions. If a Visibility failure and a Connectivity failure lead to the same fix, the dimensions are not earning their keep. Demonstrate with one worked case. | Yes, 1 paragraph + worked case | 4/6 reviewers raised this. Section 14.13 partially addresses but needs body-text presence. |
| "The five dimensions are arbitrary." | S5 (after dimension definitions) | Defend on practical grounds. These are a minimum viable diagnostic set: each produces a distinct diagnosis, removing any one creates a gap. Address excluded candidates: Timeliness (subsumed by Confidence), Salience (subsumed by Visibility + Representation), Completeness (emergent from all five). | Yes, 1 paragraph | 4/6 reviewers raised this. Brief, practical defense is sufficient. |

---

## 12. Citation Workstream

**Planning map only. Do not add citations yet.**

| Section | Construct introduced | Citation gap | Candidate traditions/sources | Priority |
| --- | --- | --- | --- | --- |
| S1 | Landscape vs. containment reframe | Light gap | Systems safety: Leveson 2011, Hollnagel 2014 | Tier 2 |
| S2 | Optimizer, gradient, topography definitions | Adequate (Simon, Ng) | Broader bounded rationality: March 1978, Gigerenzer & Selten 2001 | Tier 2 |
| S3 | Context vs. reasoning state | Adequate (Walsh & Ungson, Alavi & Leidner) | Organizational forgetting, transactive memory | Tier 3 |
| S4 | Goal, Policy, Interpretation | Adequate (Russell & Norvig, Dennett, Weick) | None critical | -- |
| S5 | Five topography dimensions | **Significant gap** | Information science: Wilson 2000, Kuhlthau 1991, Bates 1989. Situation awareness: Endsley 1995. | **Tier 1** |
| S6 | Motion stages, sufficiency | Best-cited mid-section (Pirolli & Card, Howard, Russell & Wefald) | Naturalistic decision-making: Klein 1998 | Tier 2 |
| S7 | Premature sufficiency, hallucination/harmful-action unification | **Significant gap** | Hallucination surveys: Ji et al. 2023, Huang et al. 2023, Maynez et al. 2020. Trust in automation: Lee & See 2004, Parasuraman & Riley 1997. | **Tier 1** |
| S8 | Learning, prediction error, reaction vs. learning | Light gap (Argyris & Schon, Cyert & March) | Organizational routines: Feldman & Pentland 2003 | Tier 2 |
| S9 | Model Update Object | **No inline citations** | Case-based reasoning: Aamodt & Plaza 1994. KM failure: Markus 2001, Weber et al. 2001. Lessons-learned literature. | **Tier 1** |
| S10 | Six reasoning objects | **No inline citations** | Design rationale: MacLean et al. 1991 or Kunz & Rittel 1970 | Tier 2 |
| S11 | Discovery Framework | **No inline citations** | Mixed-initiative interaction: Horvitz 1999. Cognitive load: Sweller 1988. NDM: Klein 1998. | **Tier 1** |
| S12 | Full running example | No inline citations (acceptable) | -- | -- |
| S13 | Implementation architecture | **No inline citations** | Agent architectures: Yao et al. 2023 (ReAct), Shinn et al. 2023 (Reflexion), Schick et al. 2024 (Toolformer). Systems safety: Rasmussen 1997. | **Tier 1** |
| S14 | Validation, falsifiability | No inline citations | Evaluation methodology: Amershi et al. 2019 (already cited) | Tier 3 |
| S15 | Intellectual lineage | Comprehensive | -- | -- |

**Missing tradition summary:**

| Tradition | Key sources | Target sections | Why it matters |
| --- | --- | --- | --- |
| Agent architectures | Yao et al. 2023 (ReAct), Shinn et al. 2023 (Reflexion), Schick et al. 2024 (Toolformer) | S8-S9, S13, S15 | Reflexion implements a version of the learning loop. Major gap. |
| Hallucination surveys | Ji et al. 2023, Huang et al. 2023, Maynez et al. 2020 | S7 | Broadens support for premature-sufficiency claim beyond Menick et al. alone. |
| Information science | Wilson 2000, Kuhlthau 1991, Bates 1989 | S5 | Topography dimensions overlap with established info quality/behavior models. |
| Situation awareness | Endsley 1995 | S5 | "Perceived topography" is closely related to SA model. |
| Naturalistic decision-making | Klein 1998, 2008 | S6, S11 | Sufficiency-based decision-making under uncertainty. Directly relevant. |
| Trust in automation | Lee & See 2004, Parasuraman & Riley 1997 | S7 | Confidence and escalation design is trust calibration. |
| Systems safety | Leveson 2011, Rasmussen 1997, Hollnagel 2014 | S1, S7, S15 | "Failures emerge from system structure, not component malice" = paper's core claim. |
| KM failure / lessons-learned reuse | Markus 2001, Weber et al. 2001 | S9 | Directly addresses KM graveyard objection. |
| Cognitive load | Sweller 1988 | S11 | "Do the reasoning work before asking the user" is a cognitive load argument. |
| Bounded rationality (broadened) | March 1978, Gigerenzer & Selten 2001 | S2, S4 | Reduces lone reliance on Simon 1955. |
| Organizational routines | Feldman & Pentland 2003 | S8 | How model updates change future behavior = routines as generative systems. |

**Claims needing support vs. softening:**

| Claim | Current support | Action |
| --- | --- | --- |
| Hallucination and harmful action share premature-sufficiency structure | Structural analogy only | Cite hallucination surveys + trust-in-automation literature, OR soften to "testable hypothesis" |
| Five topography dimensions are the right decomposition | Author judgment | Add brief defense + cite information science for grounding |
| MUOs reduce repeated mistakes more effectively than postmortems | None | Soften to hypothesis + cite KM failure literature |
| Reasoning-state preservation improves future agent behavior | None | Soften to hypothesis + add pre-empirical framing |
| Discovery reduces user burden while increasing quality | None | Soften to "design hypothesis" + cite cognitive load and mixed-initiative interaction |

---

## 13. Compression Principles for v1.0

1. **Reader comprehension governs compression.** Do not cut for length alone. Every compression decision should be tested: does removing this material improve or degrade the reader's ability to explain the framework? Eliminate pontification; preserve everything that lands comprehension.

2. **Compress repetition, not discovery.** The arc from fear to landscape to learning must survive intact. Cut restatements, not first statements.

3. **Preserve the aha sequence.** Every aha in Section 5 has a required v1.0 location. Compression cannot skip or flatten an aha.

4. **One example should carry the framework.** The healthcare campaign is the canonical worked simulation. It should appear in full 2-3 times, not 10. Other appearances become one-sentence bridge references.

5. **Do not cut a repeated idea until its function is classified.** Use the repetition function audit (Section 8). Some repetition is regrounding or escalation; only unnecessary restatement and redundant replay should be cut.

6. **Convert repeated walkthroughs into trace tables where possible.** Section 12 is the primary candidate. Sections 8.10-8.11 (learning loop examples) are secondary candidates.

7. **Prefer clear bridge sentences over recap paragraphs.** "Return to the healthcare campaign. Here, [concept] manifests as [specific]." is better than re-establishing the full scenario.

8. **Keep Appendix A practical.** Its overlap with the main paper is functional (standalone usability). Do not compress Appendix A to match main-paper compression targets.

9. **Do not hide evidentiary limits.** State pre-empirical posture early and clearly. Soften operational predictions. Keep falsifiability commitments.

10. **Do not add citations as decoration.** Every new citation must do work: grounding a construct, positioning against prior work, or strengthening a claim. Section 15's "over-cite by design" principle applies to intellectual honesty, not to bulk.

11. **Every retained framework object must earn its place.** If a reasoning object, a topography dimension, or a motion stage does not produce a distinct diagnosis or intervention, it should be questioned.

12. **Compress prose into visuals where the relationship matters more than the paragraph.** Trace tables, admission matrices, lineage tables, and loop diagrams can preserve structure that prose obscures through repetition. See Section 16 (Visual Compression Strategy) for candidates and rules.

---

## 14. High-Risk Cuts

Cutting these areas too aggressively would damage the paper:

| Element | Location | Why it is high-risk |
| --- | --- | --- |
| Marble analogy | S1 | The paper's most effective single moment. Universally praised. |
| Section 3 (entire) | S3 | Strongest section per 4/6 reviewers. The foundation of the argument. |
| Premature sufficiency argument | S7 core | Paper's most original contribution per 5/6 reviewers. |
| "Reduces readmissions" compliance example | S7.5, Case A | Most concrete, realistic example. "Feels like a Tuesday." |
| Sufficiency vs. certainty 2x2 | S6.5 | Immediately usable design heuristic per 3/6 reviewers. |
| Reaction vs. learning distinction | S8.8 | Rigorous, well-anchored, practically important. |
| Discovery principle | S11 | Most product-ready construct. "Do the reasoning work before asking the user." |
| MUO eleven-field specification | S9.3 | Most concrete, falsifiable claim. Practitioners could build against it. |
| MUO ten failure modes | S9.7 | Useful standalone. Prevents learning from becoming folklore. |
| Section 14 (falsifiability) | S14 | Stronger than most framework papers. Builds credibility. |
| "Blend, not invention" posture | S15.16 | Prevents the most common academic objection. |
| Appendix A | Full | Most practically actionable section per 4/6 reviewers. |
| Diagnosis-to-intervention mapping | S5.11 | Clearest bridge from theory to practice in the topography section. |

---

## 15. Best Compression Opportunities

Safest compression targets (highest word reduction, lowest argument damage):

| Target | Location | Estimated savings | Risk |
| --- | --- | --- | --- |
| Healthcare campaign setup repetitions in S4, S5, S6 | S4 (~415-490), S5 (~866-901), S6 (~1126-1149) | ~1,500 words | Low. Replace with one-sentence bridges. |
| Section 2 glossary | S2 (lines 80-155) | ~800 words | Low. Fold 5 core terms inline. Reduce to half-page orientation or remove. |
| Defensive subsections S4.5, S5.7, S5.8 | S4.5 (532-569), S5.7 (802-825), S5.8 (826-851) | ~1,000 words | Low. Reduce to one paragraph each or fold into footnotes. |
| Section 12 narrative re-walk | S12 (lines 2444-2715) | ~1,500-2,000 words | Low. Convert to trace table with brief commentary. |
| Section 17 conclusion recap | S17 (lines 3518-3673) | ~1,000 words | Low. Reduce from 155 lines to ~50 lines. One forward-looking move. |
| Section 16 recap implications | S16 (lines 3370-3517) | ~800-1,000 words | Low. Cut subsections that restate body arguments. Keep genuinely new implications. |
| Section 15 lineage subsections | S15 (lines 3180-3369) | ~800-1,000 words | Moderate. Compress from 18 to 8-10 subsections. Keep "blend not invention." |
| Repeated campaign example passes in S8, S10, S11 | S8.10-8.11, S10.11, S11 various | ~800-1,000 words | Moderate. S8 learning loop structure is valuable; trim narrative wrapping. |
| Section 13 schema and component table | S13 (lines ~2716-3009) | ~500-800 words | Low. Move JSON schema and component table to Appendix B. Keep maturity model and "Do Not Start." |

**Estimated total recoverable:** ~8,000-10,000 words from compression targets alone. At 25-35% of ~18,000 body words, the target is ~4,500-6,300 words cut. These targets provide ample room.

---

## 16. Visual Compression Strategy

### Principle

```
Visual compression is allowed and encouraged when it preserves
relationships better than prose.
```

```
Visual representation is argument, not decoration. Tables, figures,
matrices, and diagrams should be treated with the same care as prose.
A visual is successful only if it helps the reader understand, remember,
or explain the argument more clearly.
```

```
Visuals should not merely shorten the paper. They should improve the
reader's ability to compare, sequence, distinguish, diagnose, or
explain the framework.
```

v1.0 should look for opportunities to replace repeated explanation with:

- Trace tables
- Admission matrices
- Loop diagrams
- Lineage tables
- Architecture diagrams
- Compact before/after comparisons

The guiding rule:

```
A visual should replace prose only when it makes the relationship
clearer, not merely shorter.
```

### Candidate Visuals

| Candidate visual | Current problem it solves | Likely location | Format | What prose it could replace or compress | Priority |
| --- | --- | --- | --- | --- | --- |
| Full framework loop | No single diagram shows the complete arc: fear -> landscape -> topography -> gradients -> sufficiency -> action -> outcome -> learning -> next cycle. Three reviewers requested this. | Early summary (after S2 or S3), or before conclusion | Loop diagram (SVG) | Repeated recap language in S16 and S17. If the reader can see the full loop, the paper does not need to re-narrate it in prose. | High |
| Dimension admission matrix | The five dimensions are asserted without defending why these five and not others. 4/6 reviewers flagged this. | S5, after dimension definitions | Table or matrix | Long prose defense of the five dimensions. Replaces or compresses S5.7, S5.8, and the dimension defense paragraph. Shows each candidate, its proposed treatment, and the admission test result in one view. | High |
| Healthcare worked-simulation trace table | The campaign example is walked through narratively 10-12 times across the paper. S12 re-walks the entire framework end-to-end. | S12 (replaces narrative re-walk) | Trace table: rows = framework stages, columns = concept / campaign application / system behavior / what changes next cycle | Repeated healthcare campaign walkthroughs. The single largest compression opportunity. Could also show context-only path vs. reasoning-state path vs. next-cycle learning in parallel columns. | High |
| Premature sufficiency failure pattern | Hallucination and harmful action are explained as sharing a motion structure. The structural parallel is currently argued in prose across multiple subsections. | S7, near Cases A and B | Compact comparison table or small diagram showing shared motion path: goal pressure + weak grounding + low friction + premature sufficiency -> action | Repeated structural explanation in S7.1-S7.3 and S7.7. A side-by-side table (hallucination path vs. harmful action path) would make the parallel visible at a glance. | Medium |
| Related-work lineage table | Section 15 runs 18 subsections of "the framework draws from X." Practitioner reviewers found it exhausting. Academic reviewer valued the honesty. | S15 | Lineage table: tradition -> what it contributes -> what this paper adds -> key citation | 18 mini related-work subsections. Preserves intellectual honesty while compressing to ~1 page. Keep "blend not invention" and "over-cite by design" statements as prose before or after the table. | High |
| Implementation bridge / architecture map | Section 13 oscillates between too abstract and too specific. Component prose and JSON schema feel out of place. | S13 or Appendix B | Layered architecture diagram or component map showing: Artifact Store, Retrieval Layer, Reasoning Object Store, Discovery Engine, Learning Loop, Governance Layer | Component prose and schema-heavy material in S13. A diagram shows how the pieces connect without requiring the reader to parse a product spec. Prose can then focus on the maturity model and "Do Not Start With the Whole Machine." | Medium |
| Appendix A minimal interview variant | The full interview is 23 questions across 4 phases. Practitioners may find this intimidating for a first engagement. | Appendix A, before or after the full interview | Short table: 8-10 questions identified as the minimum viable interview, with phase labels and brief rationale for inclusion | Facilitation uncertainty and adoption friction. Does not replace the full interview; it provides a "start here" on-ramp. | Medium |

### Visual Compression Rules

1. Do not create visuals merely to decorate the paper.
2. Use visuals to preserve relationships, sequences, contrasts, or taxonomies.
3. A visual must reduce prose burden or improve comprehension.
4. A visual must not introduce new terminology that the prose does not support.
5. A visual must not become a second framework competing with the text.
6. If a visual replaces prose, verify that no load-bearing aha is lost.
7. Prefer tables for comparison and admission tests.
8. Prefer loop diagrams for system motion and learning cycles.
9. Prefer trace tables for worked scenarios.
10. Prefer lineage tables for related work compression.

---

## 17. v1.0 Workstreams

| # | Workstream | Purpose | Inputs | Outputs | Before manuscript editing? |
| --- | --- | --- | --- | --- | --- |
| 1 | Arc preservation map | Ensure every aha survives compression | This doctrine (Section 5) | Checklist for compression pass | Yes |
| 2 | Compression map | Section-by-section compression targets with specific cut/keep decisions | This doctrine (Sections 8, 9, 14, 15), v0.2 manuscript | Annotated compression plan per section | Yes |
| 3 | Dimension admission test / five-dimension defense | Finalize dimension defense prose, candidate assessments, and reader-facing rule | This doctrine (Section 6), v0.2 S5, reviewer feedback | Defense paragraph for S5, candidate disposition table | Yes |
| 4 | Canonical worked simulation design | Finalize example framing, placement, density, and evidence posture language | This doctrine (Section 7), v0.2 S3/S7/S9/S12 | Example placement plan, framing paragraph | Yes |
| 5 | Citation redistribution map | Identify exact insertion points for new citations | This doctrine (Section 12), BIBLIOGRAPHY.md, RELATED_WORK_LEDGER.md | Section-by-section citation insertion plan | Yes |
| 6 | Objection-response placement map | Draft response paragraphs and locate insertion points | This doctrine (Section 11) | 5 response drafts with target locations | Yes |
| 7 | Appendix A facilitation guidance | Add practical notes (who, how long, what to bring, minimal variant) | Appendix A, reviewer feedback | Updated Appendix A plan | Can run during editing |
| 8 | Visual compression map | Identify which repeated prose blocks can become figures, trace tables, lineage tables, or matrices before manuscript rewriting begins | This doctrine (Section 16), v0.2 manuscript, existing SVGs | Visual placement plan: which candidates to create, which prose they replace, and verification that no aha is lost | Yes |
| 9 | v1.0 working-file setup | Create `PAPER_v1.0_WORKING.md` from frozen v0.2, update version header | `PAPER_v0.2.md` | Working copy ready for edits | Yes (final pre-editing step) |

---

## 18. Open Authorial Decisions

### Resolved Decisions

The following decisions have been resolved by Benet and ChatGPT (see also `V1_0_OUTLINE_AND_VISUAL_PLACEMENT_MAP.md`, Final Authorial Decisions):

1. ~~**What is the v1.0 target word count?**~~ **RESOLVED.** 15,000 words is the minimum body threshold, not the ceiling. Final body length determined chunk by chunk according to reader comprehension and completeness of the standalone arc. The aggressive lower-bound estimate (7,500-11,500) is a diagnostic guide, not a governing target.

2. ~~**Should Section 2 (Terms) survive as a section?**~~ **RESOLVED.** No. S2 glossary folds into S1 inline definitions as part of the approved 11-section structure.

3. ~~**Should Section 13 schema and component table move to an appendix?**~~ **RESOLVED.** No Appendix B. Full schema, component tables, lifecycle governance, and implementation templates deferred to product/design or practitioner/tooling track. Keep only enough implementation structure in v1.0 S8 for the theory to be credible.

4. ~~**Should Section 15 (Related Work) become a table?**~~ **RESOLVED.** Yes. S15 compresses into a related-work lineage table plus 2-3 paragraphs of commentary in v1.0 S10.

5. ~~**What is the exact framing of pre-empirical status?**~~ **RESOLVED.** v1.0 includes an abstract and an epistemic-status paragraph. The epistemic status states this is a pre-empirical design framework supported by a constructed stress test, not an empirical validation paper.

7. ~~**Should Appendix A get a minimal-interview variant?**~~ **RESOLVED.** Yes. Minimal interview variant is a high-priority new visual/table candidate.

8. ~~**Should a full-framework visual be created?**~~ **RESOLVED.** Yes. Full-framework loop appears early in S1 as a reader map. May be lightly echoed in S11.

10. ~~**How aggressively should the five dimensions be defended?**~~ **RESOLVED.** Dimension admission matrix in S3 (table format). "Arbitrary dimensions" objection addressed in S3 where it naturally arises.

13. ~~**Should v1.0 include an abstract?**~~ **RESOLVED.** Yes.

14. ~~**What is the minimum complete arc?**~~ **RESOLVED.** The 14-step arc (fear through Appendix A) is a hard constraint. The compression pass uses this list as the governing requirement.

### Remaining Open Decisions

The following questions are NOT yet resolved:

6. **Should a tiny contrast example be added?** If yes, which domain (incident response, customer support, compliance review)? Maximum 2-3 paragraphs. Placement: v1.0 S4 or S9.

9. **What is the target audience / venue for v1.0?** Academic journal, conference, practitioner whitepaper, or mixed audience? This determines citation depth and evidence requirements.

11. **Should "Model Update Object" be renamed?** "Learning Record" or "Decision Lesson" trades precision for accessibility.

12. **How will the real case be sourced for future validation?** Options: (a) retrospective analysis of a public AI failure, (b) documented organizational learning failure, (c) Appendix A pilot with a real team, (d) minimal prototype evaluation. This does not block v1.0 (which uses a constructed stress test), but should be decided for the research roadmap.

15. **Should v1.0 explicitly describe itself as the keystone paper for a broader body of work, or should that framing remain internal?** If explicit, a brief statement in S1 or S11 names the tracks. If internal, the body-of-work strategy guides compression without appearing in the manuscript.

---

## 19. Recommended Next Step

Most authorial decisions have been resolved. The 11-section structure is approved, the compression posture is set, and the visual/objection/evidence strategies are decided. Five open decisions remain (contrast example, target venue, MUO naming, real case sourcing, body-of-work framing visibility) — none of which block the creation of the working draft.

1. **Create `PAPER_v1.0_WORKING.md` from frozen v0.2.** The working copy is where edits happen. v0.2 remains frozen and unchanged. Update the version header.

2. **Begin the rewrite chunk by chunk.** Follow the approved 11-section structure, the arc preservation spine, the compression hypotheses (as diagnostic guides), and the section-level comprehension test: "Does this section help the reader explain the framework more cogently?"

3. **Resolve remaining open decisions as they arise during drafting.** The five remaining questions can be answered in context rather than in advance.

4. **Specify new visuals before or during drafting.** The full-framework loop, dimension admission matrix, healthcare trace table, premature sufficiency comparison, related-work lineage table, implementation architecture map, and Appendix A minimal interview variant should be specified as they are needed by the prose.

---

## No-Edit Confirmation

No manuscript or release files were edited in the creation of this document. `PAPER_v0.2.md`, `PAPER_DRAFT.md`, section files, references, SVGs, and release files remain unchanged.
