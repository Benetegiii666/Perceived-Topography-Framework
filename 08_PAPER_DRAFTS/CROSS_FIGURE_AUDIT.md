# Cross-Figure Visual Consistency Audit

**Date:** 2026-06-12
**Auditor:** Claude
**Method:** Automated extraction of typography, color, shape, and arrow properties across all 7 SVGs, plus manual review of spec alignment

---

## 1. Typography Consistency

### Main title size
All 7 figures use font-size="28" for the main title. **Consistent.** ✓

### Panel/section heading sizes
- Figures 1, 3: use 20-22 for panel headings
- Figures 2, 4, 5, 6, 7: use 16-18 for sub-headings
- **Minor inconsistency** — Fig 1 uses 20 for panel labels ("Agent Fear Frame"), Fig 3 uses 22 for region labels ("Optimizer State"). These should ideally both be 20 or both be 22.
- **Risk: Low.** Not distracting at paper width.

### Node label sizes
- Figures 3, 4, 5, 6: use 15-17 for primary node labels. **Consistent.**
- Figure 1: uses 14-16. Slightly smaller. **Low risk.**
- Figure 7: uses 13-15 for main flow nodes. Slightly smaller due to 8 nodes in a row. **Acceptable — space-constrained.**

### Small text / annotation sizes
- Figures 1, 3, 6, 7: use 10-13 for annotations. Figure 7 uses font-size="10" for step descriptions. **This is too small at paper width.**
- Figures 2, 4, 5: use 11-14. **Acceptable.**

| Figure | Issue | Risk | Recommended Fix | Apply Now? |
|--------|-------|------|----------------|------------|
| 7 | font-size="10" annotations may be too small | **Medium** | Increase to 11 minimum | Yes |
| 1 | Panel heading 20px vs Fig 3's 22px | Low | Standardize to 22 | No |
| 7 | Main flow node labels at 15px feel tight with 8 nodes | Low | Accept — space-constrained | No |

---

## 2. Color Consistency

### Color meaning alignment

| Color | Spec Meaning | Fig 1 | Fig 2 | Fig 3 | Fig 4 | Fig 5 | Fig 6 | Fig 7 |
|-------|-------------|-------|-------|-------|-------|-------|-------|-------|
| #2E5EAA (blue) | Nodes, reasoning flow | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| #2E8B57 (green) | Learning, validated, safe | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| #D89A21 (amber) | Warning, uncertainty | — | ✓ | ✓ | — | ✓ | ✓ | ✓ |
| #B94A48 (red) | Risk, unsafe, premature | ✓ | — | — | ✓ | ✓ | — | — |
| #8A94A6 (gray) | Boundary, secondary | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |

**Issues:**

| Figure | Issue | Risk | Recommended Fix | Apply Now? |
|--------|-------|------|----------------|------------|
| 4 | No amber used — Confirm step could use amber for "confidence calibration" pill | Low | Accept — red dominates the failure story | No |
| 5 | Red used for ≠ Learning box — consistent with spec (risk/blocked) | — | No change | No |

**Overall color usage: Consistent.** ✓

---

## 3. Shape Consistency

### Rounded rectangles
All figures use rx="10"-"14" for reasoning objects. **Consistent.** ✓

### Pills
Figures 1, 3, 4, 6 use rx="15"-"22" for secondary items. **Consistent.** ✓
Figure 7 uses rx="10"-"12" for output objects — slightly less pill-like than the artifacts in Fig 6. **Minor inconsistency** but acceptable since these are reasoning objects, not artifacts.

### Cloud/irregular shape
Only Figure 7 uses an ellipse with dashed stroke for "Messy Human Intent." **Correct — this is the only ambiguous-input node.** ✓

### Policy boundaries
Figure 1: curved dashed paths for policy guardrails on right panel. ✓
Figure 3: curved dashed paths for policy guardrails. ✓
No other figures need policy boundaries.

| Figure | Issue | Risk | Recommended Fix | Apply Now? |
|--------|-------|------|----------------|------------|
| — | No shape consistency issues found | — | — | — |

---

## 4. Arrow Consistency

### Solid arrows
All figures use solid lines + polygon arrowheads for main flow. **Consistent.** ✓

### Dashed arrows
- Fig 3: dashed for Goal Relevance projection ✓
- Fig 4: dashed for failure shortcut ✓
- Fig 5: dashed for feedback loop ✓
- Fig 6: dashed for artifact support + feedback ✓
- Fig 7: dashed for flow-to-output connections ✓
**Consistent.** ✓

### Arrow crossings
- Fig 6: artifact arrows cleaned in revision — no crossings ✓
- Fig 7: some dashed arrows from main flow to output objects cross (Infer→OptimizerState crosses Learn→LearningEvent path region)

| Figure | Issue | Risk | Recommended Fix | Apply Now? |
|--------|-------|------|----------------|------------|
| 7 | Some dashed arrows cross in the flow-to-output zone | Low | Accept for rough — clean in polish | No |

---

## 5. Visual Hierarchy

### 10-second comprehension test

| Figure | Primary concept clear in 10s? | Notes |
|--------|-------------------------------|-------|
| 1 | ✓ | Left = box, Right = landscape. Clear. |
| 2 | ✓ | Three layers, middle emphasized. Clear. |
| 3 | ✓ | Optimizer → Topography → Motion. Clear. |
| 4 | ✓ | Normal path vs failure shortcut. Clear. |
| 5 | ✓ | Loop + "≠ Learning" contrast. Clear. |
| 6 | ✓ | Six-object chain + artifacts below. Clear. |
| 7 | ✓ | Horizontal flow + output objects. Clear. |

### Critical figures (3 and 6) feel strongest?
**Yes.** Both are the most detailed, most carefully revised, and largest SVGs (12.8KB and 13.8KB). They carry the most visual weight. ✓

### Captions/callouts compete with main diagram?
- Fig 6: contrast statement was lightened in revision — no longer competes ✓
- All other figures: captions are in smaller italic gray text. **Subordinate.** ✓

---

## 6. Terminology Consistency

### New terms introduced?
**None found across all 7 SVGs.** ✓

### Exact paper terminology preserved?
All node labels, dimension names, object names, and motion stages match the paper exactly. ✓

### Specific terminology checks

| Term | Expected | All figures consistent? |
|------|----------|----------------------|
| Optimizer State (not "optimizer state") | Capitalized in diagrams | ✓ |
| Premise Stack | Capitalized | ✓ |
| Decision State | Capitalized | ✓ |
| Investigation Trace | Capitalized | ✓ |
| Learning Event | Capitalized | ✓ |
| Model Update Object | Capitalized | ✓ |
| Visibility, Accessibility, etc. | Capitalized as dimensions | ✓ (Fig 3) |
| Goal Relevance | Labeled as "projection / filter" | ✓ (Fig 3) |
| Policy boundary | Labeled as boundary, not dimension | ✓ (Figs 1, 3) |

---

## 7. Accessibility / Grayscale Robustness

### Meaning carried by shape/line/label, not color only?

| Figure | Grayscale-safe? | Issue |
|--------|----------------|-------|
| 1 | ✓ | Left uses dashed box + vertical flow; right uses landscape + pills + path |
| 2 | ✓ | Three layers distinguished by position, border weight, and labels |
| 3 | ✓ | Three regions by position; guardrail by dash pattern; projection by dash + cone |
| 4 | ✓ | Normal vs failure path distinguished by position (top/bottom) + dash pattern |
| 5 | **Partial** | ≠ Learning box uses red + dashed border — in grayscale, the dashed border still distinguishes it, but the red-vs-blue distinction becomes gray-vs-gray |
| 6 | ✓ | Chain vs artifacts by position + stroke weight + dash pattern |
| 7 | ✓ | Cloud shape vs rectangles; main flow vs output objects by position |

### Rotated text
Figure 5 has one rotated text element ("new expectations" rotated 90°). **This is hard to read.**

### Font-size 10
Figure 7 uses font-size="10" for step descriptions above the main flow nodes. **May be too small at paper width.**

| Figure | Issue | Risk | Recommended Fix | Apply Now? |
|--------|-------|------|----------------|------------|
| 5 | Rotated text "new expectations" | **Medium** | Replace with horizontal label along the feedback arrow path | Yes |
| 7 | font-size="10" step descriptions | **Medium** | Increase to 11 minimum | Yes |
| 5 | ≠ Learning box grayscale distinction | Low | Add a label or heavier line style to distinguish without color | No |

---

## 8. Specific Rough-Edge Checks

| Figure | Reported Rough Edge | Verified? | Severity | Fix Now? |
|--------|-------------------|-----------|----------|----------|
| 1 | Right panel path could be more organic | Verified — path is a simple Q-curve | Low | No |
| 1 | Left containment could be more visually oppressive | Verified — dashed rect is functional | Low | No |
| 1 | Right policy guardrails subtle | Verified — 2.5px dashed, visible | Low | No |
| 2 | Three layers could use stronger differentiation | Verified — middle layer has thicker border (3px) + blue fill | Low | No |
| 4 | Intervention pills could be positioned cleaner | Verified — they stagger but are readable | Low | No |
| 4 | "Skips investigation" path could be smoother | Verified — dashed Q-curve is functional | Low | No |
| 5 | Feedback loop text rotated 90° | **Verified — hard to read** | **Medium** | **Yes** |
| 5 | Side contrast box may need repositioning | Verified — positioned left, reasonable | Low | No |
| 7 | Dashed arrows to output objects cross | Verified — some crossing in dense area | Low | No |
| 7 | Healthcare campaign text may need larger size | Verified — font-size="11", adequate | Low | No |

---

## Overall Visual System Judgment

The seven SVGs form a **reasonably consistent visual system** at the rough-draft stage. The dominant style (rounded rectangles, solid/dashed arrows, blue/green/amber/red/gray palette, direct labels) is consistent across all figures. The two critical figures (3 and 6) are the most polished. The remaining five are functional rough drafts that communicate their concepts clearly.

**No figure needs to be regenerated.** All are refinable.

---

## Top 5 Fixes Before Final Polish

1. **Figure 5: Replace rotated text** — "new expectations" is rotated 90° and hard to read. Replace with horizontal label positioned along or near the feedback arrow. **Medium priority.**

2. **Figure 7: Increase minimum font size** — Step descriptions use font-size="10" which may be too small at paper width. Increase to 11. **Medium priority.**

3. **All figures: Standardize panel heading size** — Figures vary between 16-22px for panel/section headings. Standardize to 20 for panel headings, 18 for sub-headings. **Low priority but improves consistency.**

4. **Figure 5: Improve grayscale distinction for ≠ Learning box** — Add heavier border or pattern to distinguish from main loop without color. **Low priority.**

5. **Figure 7: Reduce arrow crossing in output zone** — Some dashed arrows overlap in the flow-to-output area. Simplify routing. **Low priority.**

---

## Figures Acceptable as Rough

| Figure | Status |
|--------|--------|
| 3 | **Approved** — already refined |
| 6 | **Approved** — already refined |
| 1 | Acceptable as rough |
| 2 | Acceptable as rough |
| 4 | Acceptable as rough |
| 5 | Needs 1 fix (rotated text) before acceptable |
| 7 | Needs 1 fix (font size) before acceptable |
