# Figure Placeholder / Diagram Integration Audit

**Date:** 2026-06-12
**Auditor:** Claude
**Method:** Full-text search of PAPER_DRAFT.md for figure placeholders, cross-referenced against SVG_SPECIFICATIONS.md

---

## Overall Finding

**No figure placeholders currently exist in PAPER_DRAFT.md.** No `![...]()` markdown, no "See Figure X," no "Figure X shows," no "illustrated in," no diagram references of any kind. All seven figures need placeholder insertion.

**No conceptual-aid disclaimer exists.** The paper does not currently contain a note saying diagrams are conceptual aids and that topography/gradients are analytic metaphors. Line 4226 says "This is the deeper meaning of topography. It is not merely an analytic metaphor. It is a design responsibility" — which is the opposite of a disclaimer. A brief note is needed, likely in Section 2 or at the first figure.

---

## Figure-by-Figure Audit

### Figure 1 — From Agent Fear to Landscape Design

| Item | Status |
|------|--------|
| Placeholder exists? | **No** |
| Current location | N/A |
| Recommended location | **After line 29** (after marble/slope paragraph, before language-caution paragraph). The marble metaphor creates the visual setup; the figure should land here. |
| Paragraph before introduces diagram? | **Yes** — the marble/slope paragraph (AHA_001 + AHA_005) naturally introduces the visual contrast between box and landscape. |
| Paragraph after interprets diagram? | **Partial** — the next paragraph discusses language caution, not the diagram. A one-sentence bridge may be helpful: "Figure 1 illustrates this contrast." |
| Caption matches SVG_SPECIFICATIONS? | N/A (no placeholder yet). SVG caption: "The question is not only whether the agent is dangerous. The better question is what landscape we asked it to move through." |
| Terminology drift? | **None** — caption uses "landscape" (intentional in S1). |
| Risk level | **Low** |
| Recommendation | **Insert placeholder** after line 29. Add brief intro sentence. |

---

### Figure 2 — Context Is Not Reasoning State

| Item | Status |
|------|--------|
| Placeholder exists? | **No** |
| Current location | N/A |
| Recommended location | **After line 448** (after the reasoning-state transition quote block in "Reasoning State Is the Missing Unit," before "This is the unit that most organizational AI systems do not preserve"). The three-layer visual (context → reasoning → action) should land after the argument establishes what's missing. |
| Paragraph before introduces diagram? | **Yes** — the reasoning-state transition block (lines 437-441) establishes the concept. |
| Paragraph after interprets diagram? | **Yes** — "This is the unit that most organizational AI systems do not preserve" directly follows. |
| Caption matches SVG_SPECIFICATIONS? | N/A. SVG caption: "Context preserves artifacts. Reasoning state preserves why artifacts shaped action. The action/learning layer preserves how reality responded and what should change." |
| Terminology drift? | **None** |
| Risk level | **Low** |
| Recommendation | **Insert placeholder** after line 448. No surrounding paragraph changes needed. |

---

### Figure 3 — Optimizer in a Perceived Topography

| Item | Status |
|------|--------|
| Placeholder exists? | **No** |
| Current location | N/A |
| Recommended location | **After line 905** (after the introductory paragraph about why topography matters, before "## 5.1 The Five Dimensions"). This is where both optimizer and topography are first visible together. The SVG spec says "Early Section 5, immediately after Information Topography is introduced." |
| Paragraph before introduces diagram? | **Partial** — the preceding paragraph explains why information can fail to shape behavior. A brief intro sentence would help: "Figure 3 shows the core model: an optimizer moving through perceived topography." |
| Paragraph after interprets diagram? | **Yes** — Section 5.1 immediately defines the five dimensions shown in the diagram. |
| Caption matches SVG_SPECIFICATIONS? | N/A. SVG caption: "The optimizer does not move through objective reality directly. It moves through a perceived topography shaped by what is visible, accessible, represented, trusted, and connected. Behavior emerges from the interaction between optimizer state and perceived landscape." |
| Terminology drift? | **None** — uses "perceived landscape" (acceptable as closing-sentence synonym for topography). |
| Risk level | **Medium** — this is the CRITICAL diagram. Placement must be precise. |
| Recommendation | **Insert placeholder** after line 905 with intro sentence. This is the most important figure in the paper. |

---

### Figure 4 — Motion and Premature Sufficiency

| Item | Status |
|------|--------|
| Placeholder exists? | **No** |
| Current location | N/A |
| Recommended location | **After line 1616** (after "The Shared Failure Grammar" section's closing paragraph, before "## 7.4 Why More Context Is Not Enough"). The failure grammar establishes the pattern; the figure visualizes it. |
| Paragraph before introduces diagram? | **Yes** — the closing paragraph of 7.3 asks the diagnostic questions that the figure answers visually. |
| Paragraph after interprets diagram? | **Partial** — 7.4 discusses why more context isn't enough, which follows from the figure but doesn't directly reference it. A brief bridge sentence could help. |
| Caption matches SVG_SPECIFICATIONS? | N/A. SVG caption: "Many failures happen when the system reaches sufficiency too early. Normal motion includes investigation, evidence, and policy checks. Premature sufficiency skips these steps and produces unsupported claims or unsafe actions." |
| Terminology drift? | **None** |
| Risk level | **Low** |
| Recommendation | **Insert placeholder** after line 1616. |

---

### Figure 5 — Learning Is Model Change

| Item | Status |
|------|--------|
| Placeholder exists? | **No** |
| Current location | N/A |
| Recommended location | **After line 2079** (after the learning loop is stated formally in 8.13, before "This loop is the difference between a system that repeats patterns and a system that adapts"). The loop has just been expressed in text; the figure visualizes it with the ≠ Learning contrast. |
| Paragraph before introduces diagram? | **Yes** — the formal loop statement (lines 2074-2079) is the exact content the figure visualizes. |
| Paragraph after interprets diagram? | **Yes** — "This loop is the difference between a system that repeats patterns and a system that adapts" directly follows. |
| Caption matches SVG_SPECIFICATIONS? | N/A. SVG caption: "Learning occurs when prediction error is investigated, explained with evidence, and converted into a model update that changes future reasoning. Storage, postmortems, and reactions alone are not learning." |
| Terminology drift? | **None** |
| Risk level | **Low** |
| Recommendation | **Insert placeholder** after line 2079. No surrounding changes needed — the text perfectly frames the figure. |

---

### Figure 6 — Reasoning Architecture: Six Objects Preserve the State Transition

| Item | Status |
|------|--------|
| Placeholder exists? | **No** |
| Current location | N/A |
| Recommended location | **After line 2416** (after the six-object table in 10.2 and "Together, these objects preserve the reasoning-state transition," before "## 10.3 Optimizer State"). The table defines the objects; the figure shows them as a chain with supporting artifacts. |
| Paragraph before introduces diagram? | **Yes** — the summary line "Together, these objects preserve the reasoning-state transition" is the perfect setup. |
| Paragraph after interprets diagram? | **Yes** — Section 10.3 begins explaining the first object in detail. |
| Caption matches SVG_SPECIFICATIONS? | N/A. SVG caption: "The unit of organizational reasoning is not the document. It is the optimizer state transition. Documents provide evidence and context. Reasoning objects preserve how that evidence shaped action and learning." |
| Terminology drift? | **None** |
| Risk level | **Medium** — this is the other CRITICAL diagram. |
| Recommendation | **Insert placeholder** after line 2416. No surrounding changes needed. |

---

### Figure 7 — Runtime Discovery Loop

| Item | Status |
|------|--------|
| Placeholder exists? | **No** |
| Current location | N/A |
| Recommended location | **After line 2715** (after the Initial/Runtime Discovery distinction in 11.2 and before "## 11.3 Retrieve"). The discovery modes have been explained; the figure shows the runtime loop with output objects before the individual steps are detailed. |
| Paragraph before introduces diagram? | **Partial** — the preceding paragraph explains that Runtime Discovery "retrieves, infers, proposes, confirms, generates, preserves, and learns." A brief intro sentence would help: "Figure 7 shows this loop with the reasoning objects it produces." |
| Paragraph after interprets diagram? | **Yes** — Section 11.3 begins walking through the Retrieve step. |
| Caption matches SVG_SPECIFICATIONS? | N/A. SVG caption: "Runtime discovery reduces user burden by retrieving and inferring before asking. The output is not only generated content, but preserved reasoning state that can be learned from later." |
| Terminology drift? | **None** |
| Risk level | **Low** |
| Recommendation | **Insert placeholder** after line 2715 with brief intro sentence. |

---

## Conceptual-Aid Disclaimer

**Status:** Not present in the paper.

**Recommended location:** Add a brief note at the first figure insertion (Figure 1, Section 1) or in Section 2 (A Note on Terms) near the Summary of Usage.

**Recommended text:**

> The diagrams in this paper are conceptual aids. They illustrate the framework's analytical structure, not a claim that agents perceive literal spatial landscapes. Topography and gradients are used as analytic metaphors for the perceived information-and-action environment.

**Note:** Line 4226 in the conclusion says "This is the deeper meaning of topography. It is not merely an analytic metaphor. It is a design responsibility." This is a rhetorical escalation that builds on the earlier disclaimer — the paper should first establish that topography is a metaphor (disclaimer), then argue that it's more than just a metaphor (conclusion). The disclaimer enables the escalation.

**Risk level:** Medium — without the disclaimer, a reader may dismiss the framework as naive spatial metaphor before reaching the argument.

---

## Summary of Recommendations

| Figure | Action | Priority |
|--------|--------|----------|
| 1 | Insert placeholder after line 29 + brief intro sentence | High |
| 2 | Insert placeholder after line 448 | High |
| 3 | Insert placeholder after line 905 + brief intro sentence | **Critical** |
| 4 | Insert placeholder after line 1616 | High |
| 5 | Insert placeholder after line 2079 | High |
| 6 | Insert placeholder after line 2416 | **Critical** |
| 7 | Insert placeholder after line 2715 + brief intro sentence | High |
| Disclaimer | Add conceptual-aid note at first figure or in Section 2 | Medium |

**No placeholders need to be moved** (none exist yet).
**No surrounding paragraphs need substantive revision** — the argument naturally frames each figure.
**3 figures would benefit from a brief intro sentence** (Figures 1, 3, 7).
**No terminology drift from captions.**
