# v1.0 Figure/Table Numbering Reconciliation

**Date:** 2026-06-18

---

## Files Reviewed

- `PAPER_v1.0_WORKING.md` — full manuscript
- `V1_0_REWRITE_DOCTRINE_AND_WORKPLAN.md`
- `V1_0_SECTION_06_POST_INSERTION_INTEGRITY_CHECK.md`
- `V1_0_SECTION_07_FIGURE_READINESS.md`
- `V1_0_SECTION_07_POST_INSERTION_INTEGRITY_CHECK.md`
- `V1_0_SECTION_08_SOURCE_PACKET.md`
- `V1_0_SECTION_REWRITE_QUEUE.md`
- `paper_assets/svg/` (full listing)

---

## Current Displayed Figure Captions in Manuscript

| Order | Caption | Line | Section | Format |
| --- | --- | --- | --- | --- |
| 1 | Figure 1: From Agent Fear to Landscape Design | 68 | S1 | `![Figure 1: ...](figures/...)` embedded |
| 2 | Figure 2: Context vs. Reasoning State | 187 | S2 | `![Figure 2: ...](figures/...)` embedded |
| 3 | Figure 3: Optimizer in a Perceived Topography | 266 | S3 | `![Figure 3: ...](figures/...)` embedded |
| 4 | Figure 4: Motion and Premature Sufficiency | 468 | S4 | `![Figure 4: ...](figures/...)` embedded |
| 5 | Figure 5. Learning Is Model Change | 954 | S6 | `**Figure 5. ...**` text placeholder |
| — | *(no Figure 6)* | — | — | — |
| 6 | Figure 7. Runtime Discovery Loop | 1353 | S7 | `**Figure 7. ...**` text placeholder |

**Observation:** The manuscript jumps from Figure 5 to Figure 7. There is no displayed Figure 6.

---

## Current Displayed Table Captions in Manuscript

| Order | Caption | Line | Section |
| --- | --- | --- | --- |
| 1 | Table 1. Dimension Admission Matrix | 312 | S3 |
| 2 | Table 2. Sufficiency Is Not Certainty | 415 | S4 |
| 3 | Table 3. Premature Sufficiency Comparison | 450 | S4 |
| 4 | Table 4. Healthcare Campaign Stress-Test Trace | 805 | S5 |
| 5 | Table 5. Not Every Change Is Learning | 1112 | S6 |
| 6 | Table 6. Ordinary Intake and Discovery Ask Different Questions | 1497 | S7 |

**Observation:** Tables are consecutively numbered 1–6 with no gaps.

---

## Figure 6 Status

**Is there a displayed Figure 6 in the manuscript?** No.

**Where does `fig6_reasoning_architecture_six_objects.svg` appear?**

1. **Section 6 arc comment** (line 893): `Visual/table placement: fig5_learning_is_model_change.svg, fig6_reasoning_architecture_six_objects.svg.` — This is an HTML comment, not displayed prose. It records the original plan to use the asset in Section 6.

2. **Section 6 post-insertion integrity check** (line 251): `Figure 6 is correctly absent (deferred to S8)` — The integrity check confirms that fig6 was intentionally NOT inserted into Section 6.

3. **Rewrite queue, Section 6 row** (line 25): `fig6 deferred to S8` — Explicitly deferred.

4. **Rewrite queue, Section 8 row** (line 27): `fig6/fig8 (existing SVG, display number TBD)` — Acknowledged but display number unresolved.

**Conclusion:** `fig6_reasoning_architecture_six_objects.svg` was originally planned for Section 6, was intentionally deferred to Section 8, and has never been displayed in the manuscript. The filename is a legacy artifact from the original plan.

---

## Section 7 Figure Number Status

Section 7 currently displays `**Figure 7. Runtime Discovery Loop**` at line 1353.

**How was Figure 7 determined?**

The Section 7 figure-readiness note (lines 13–18) documents the reasoning:

> "The source-packet review initially corrected the figure number to Figure 6, reasoning that the manuscript contains Figures 1–5. However, `fig6_reasoning_architecture_six_objects.svg` is already allocated to Section 6 (referenced in the Section 6 manuscript comment at line 893 of `PAPER_v1.0_WORKING.md`). Therefore:
> - Figure 6 = Section 6's reasoning architecture figure
> - Figure 7 = Section 7's Discovery loop figure"

**The problem:** This reasoning assumed Section 6 would eventually display a Figure 6. But the S6 post-insertion integrity check and rewrite queue confirm that fig6 was deferred to Section 8 and was never inserted into Section 6. Section 6 does not display a Figure 6 and will not display one.

**Result:** Section 7 is labeled Figure 7 based on a Figure 6 that does not exist and will not exist in Section 6. The manuscript jumps from Figure 5 (Section 6) to Figure 7 (Section 7) with no Figure 6.

---

## Two Options

### Option A: Renumber Section 7 to Figure 6

- Section 7's Discovery loop becomes **Figure 6**
- Section 8's six-object chain becomes **Figure 7**
- Figures are consecutively numbered 1–7 with no gap
- Requires editing the inserted Section 7 caption in `PAPER_v1.0_WORKING.md` (one line) and the SVG title in `fig7_discovery_loop.svg`
- The Section 7 figure-readiness note's rationale becomes outdated but is a review artifact, not manuscript prose

### Option B: Keep Figure 7 in Section 7, use Figure 8 in Section 8

- Gap persists: Figures 1–5, then Figure 7, then Figure 8
- No Figure 6 exists in the manuscript
- The gap is cosmetically odd but not structurally harmful
- No edits to already-inserted Section 7
- Requires no changes to existing files

### Option C: Insert fig6 into Section 6 as Figure 6

- Would fill the gap: Figures 1–5, then Figure 6 (S6), then Figure 7 (S7), then Figure 8 (S8)
- Requires re-opening Section 6 to insert a figure
- The S6 post-insertion integrity check explicitly deferred fig6 to S8 — inserting it into S6 reverses that decision
- The six-object chain figure arguably belongs with the architecture section (S8), not the learning section (S6)

---

## Section 8 Figure Number Recommendation

**Depends on which option is chosen:**

| Option | S6 figure | S7 figure | S8 figure | Gap? |
| --- | --- | --- | --- | --- |
| A (renumber S7) | None | Figure 6 | Figure 7 | No |
| B (keep gap) | None | Figure 7 | Figure 8 | Yes (no Figure 6) |
| C (insert into S6) | Figure 6 | Figure 7 | Figure 8 | No |

---

## Table 7 Recommendation

Tables are consecutively numbered 1–6. The next table should be **Table 7**. No ambiguity.

If Section 8 includes a maturity model table, it should be captioned:

```text
Table 7. [Title TBD]
```

---

## Required Authorial Decision

One decision is needed before Section 8 drafting:

**Should Section 7's Discovery loop figure be renumbered from Figure 7 to Figure 6?**

- If **yes** (Option A): The manuscript will have consecutive figures 1–7 with no gap. Section 7's caption changes from `Figure 7` to `Figure 6`. Section 8's architecture figure becomes `Figure 7`. The SVG filename (`fig7_discovery_loop.svg`) does not need to change — only the displayed caption.
- If **no** (Option B): The manuscript will have a Figure 5 → Figure 7 gap. Section 8's architecture figure becomes `Figure 8`.
- If **insert fig6 into S6** (Option C): Section 6 is re-opened. The six-object chain appears in S6 rather than S8, which reverses a prior editorial decision.

**Recommendation:** Option A. Renumber Section 7 to Figure 6. This produces clean consecutive numbering with no gap. The cost is one caption edit in the manuscript and one SVG title update — both mechanical. The editorial substance is unchanged.

---

## Recommended Mechanical Patch, If Option A Is Approved

If Option A is approved, the following changes are needed:

1. In `PAPER_v1.0_WORKING.md`: change `**Figure 7. Runtime Discovery Loop**` to `**Figure 6. Runtime Discovery Loop**` (one line).
2. In `paper_assets/svg/fig7_discovery_loop.svg`: change the `<title>` element from `Figure 7` to `Figure 6`.
3. In the Section 8 source packet: use `Figure 7` as the displayed number for the six-object chain figure.
4. In the Section 8 source packet: use `Table 7` for the maturity model table.

The SVG *filename* (`fig7_discovery_loop.svg`) does not need to change — filenames are internal references, not displayed numbers.

**No changes to Section 7 prose or argument are needed.** This is a caption-only mechanical patch.

---

## No-Edit Confirmation

- Working manuscript edited: No
- Rewrite queue edited: No
- Source packets edited: No
- Review packets edited: No
- References edited: No
- Figures or SVGs edited: No
- SESSION_START.md edited: No
