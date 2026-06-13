# Final SVG Polish Audit

**Date:** 2026-06-13
**Auditor:** Claude

---

## Overall Verdict

**SVGs ready for export as-is:** Yes — all 7 are functional and communicate their concepts clearly.

**Minimum fixes before export:** 2 (both low-effort)

**Optional polish to defer:** 5 (cosmetic, no comprehension impact)

**Any figure needing regeneration:** None

---

## Issue-by-Issue Report

### Issue 1 — Figure 3 title size inconsistency

**Figure:** 3
**Issue:** Title font-size is 30px; all other figures use 28px.
**Risk:** Low
**Recommended fix:** Change Fig 3 title from font-size="30" to font-size="28" for consistency.
**Apply before export:** Yes — trivial, improves consistency.

---

### Issue 2 — Panel heading size inconsistency

**Figures:** 1 (20px), 3 (22px), others have no panel headings
**Issue:** Fig 1 panel headings ("Agent Fear Frame," "Topography Design Frame") use 20px. Fig 3 region headings ("Optimizer State," "Perceived Topography," "Motion") use 22px.
**Risk:** Low
**Recommended fix:** Standardize both to 20px. Fig 3's region headings at 22px are only 2px larger — barely visible — but consistency is cleaner.
**Apply before export:** No — barely perceptible difference. Defer to final polish.

---

### Issue 3 — Figure 1 left panel could be more oppressive

**Figure:** 1
**Issue:** The left "Agent Fear Frame" uses a dashed rectangle that feels functional but not visually oppressive enough to contrast with the landscape on the right.
**Risk:** Low
**Recommended fix:** Could increase stroke-width of the containment box from 3 to 4, or add a second inner border. But the current version communicates the concept.
**Apply before export:** No — the conceptual contrast is already clear.

---

### Issue 4 — Figure 1 right panel path could be more organic

**Figure:** 1
**Issue:** The green path through the landscape is a simple Q-curve. Could be more organic with multiple curves.
**Risk:** Low
**Recommended fix:** Add slight additional curves to the path. Cosmetic only.
**Apply before export:** No — the path communicates "movement through landscape" adequately.

---

### Issue 5 — Figure 2 layer differentiation

**Figure:** 2
**Issue:** The three layers are distinguished by border weight (2px, 3px, 2px) and color (gray, blue, green). The middle "Reasoning-State Layer" has a thicker blue border (3px) and blue fill. This is adequate but the layers could be more visually distinct.
**Risk:** Low
**Recommended fix:** Could increase the height difference between layers or add subtle background shading to each. But the current version has the "— the missing layer —" label which draws attention effectively.
**Apply before export:** No — the emphasis on the middle layer is already achieved through border weight + color + label.

---

### Issue 6 — Figure 5 grayscale distinction for ≠ Learning box

**Figure:** 5
**Issue:** The ≠ Learning box uses red (#B94A48) stroke with dashed border. In grayscale, the dashed border still distinguishes it from the main loop (which uses solid borders). However, the internal items (Storage, Postmortem, Reaction) also use red stroke, which becomes indistinguishable from the main loop's blue stroke in grayscale.
**Risk:** Low-Medium
**Recommended fix:** Add a heavier border (2.5px instead of 1px) to the ≠ Learning internal items, or use a different fill pattern (e.g., light gray fill instead of #F7F9FC). The dashed outer border + the "≠ Learning" label already provide non-color distinction.
**Apply before export:** Yes — small change, improves accessibility. Increase internal item stroke-width from 1 to 2 for better grayscale contrast.

---

### Issue 7 — Figure 7 arrow crossings

**Figure:** 7
**Issue:** 7 dashed arrows from main flow nodes to output objects cross in the dense middle zone (Infer→OptimizerState crosses Learn→LearningEvent visual region).
**Risk:** Low
**Recommended fix:** Could route some arrows differently, but the crossings are at low opacity (0.45-0.5) and don't impair comprehension. The main flow is clear; the output connections are secondary.
**Apply before export:** No — crossings are at low opacity and don't block comprehension.

---

## Summary

| # | Figure | Issue | Risk | Apply Before Export? |
|---|--------|-------|------|---------------------|
| 1 | 3 | Title 30px → 28px | Low | **Yes** |
| 2 | 1, 3 | Panel heading 20/22px inconsistency | Low | No |
| 3 | 1 | Left panel not oppressive enough | Low | No |
| 4 | 1 | Right panel path not organic enough | Low | No |
| 5 | 2 | Layer differentiation could be stronger | Low | No |
| 6 | 5 | ≠ Learning items need grayscale help | Low-Medium | **Yes** |
| 7 | 7 | Arrow crossings in output zone | Low | No |

---

## Minimum Fixes Before Export

1. **Figure 3:** Change title font-size from 30 to 28.
2. **Figure 5:** Increase ≠ Learning internal item stroke-width from 1 to 2.

Both are one-line edits. Total effort: <2 minutes.

## Optional Polish to Defer

- Panel heading size standardization (Issues 2)
- Figure 1 visual oppressiveness (Issue 3)
- Figure 1 path organicness (Issue 4)
- Figure 2 layer differentiation (Issue 5)
- Figure 7 arrow routing (Issue 7)

None of these affect comprehension or accessibility. They are cosmetic improvements for publication-quality polish.

## Figures 3 and 6 Still Act as Visual Templates

**Yes.** Figure 3 (12.8KB) and Figure 6 (13.8KB) remain the most detailed and refined. Their visual language (rounded rectangles, contour lines, solid/dashed arrows, color conventions) is consistent with all other figures. No template drift detected.
