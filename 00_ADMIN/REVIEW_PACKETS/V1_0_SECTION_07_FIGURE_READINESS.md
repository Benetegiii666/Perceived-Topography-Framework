# v1.0 Section 7 — Figure Readiness Note

**Date:** 2026-06-18

## Figure Asset

- **v1.0 SVG:** `paper_assets/svg/fig7_discovery_loop.svg`
- **Displayed manuscript number:** Figure 7
- **Legacy SVG:** `paper_assets/svg/fig7_runtime_discovery_loop.svg` (superseded; shows seven-step loop with Generate, Preserve, Learn as equal stages)

## Figure Numbering Rationale

The source-packet review initially corrected the figure number to Figure 6, reasoning that the manuscript contains Figures 1–5. However, `fig6_reasoning_architecture_six_objects.svg` is already allocated to Section 6 (referenced in the Section 6 manuscript comment at line 893 of `PAPER_v1.0_WORKING.md`). Therefore:

- **Figure 6** = Section 6's reasoning architecture figure (`fig6_reasoning_architecture_six_objects.svg`)
- **Figure 7** = Section 7's Discovery loop figure (`fig7_discovery_loop.svg`)

The source packet has been updated to reflect Figure 7. The review file retains the original Figure 6 determination as written; this readiness note documents the correction.

## What Changed from Legacy SVG

| Element | Legacy (`fig7_runtime_discovery_loop.svg`) | v1.0 (`fig7_discovery_loop.svg`) |
| --- | --- | --- |
| Core loop | Seven steps: Retrieve → Infer → Propose → Confirm → Generate → Preserve → Learn | Four steps: Retrieve → Infer → Propose → Confirm |
| Generate, Preserve, Learn | Equal loop stages | Muted downstream consequences |
| Re-entry arrow | Not present | Confirm → Retrieve (on new uncertainty) |
| Inference label | "goal, ICP, constraints" | "provisional hypothesis" (gold/italic) |
| Confirmation label | "material questions only" | "correct · reject · qualify · bound" |
| Output objects | Optimizer State, Premise Stack, Decision State, Investigation Trace, Learning Event, Model Update Object, Discovery Pattern Update | Reusable Reasoning Surface (scope, confidence, provenance, applicability boundary) → Future Topography |
| MUO / Learning Event | Present | Removed (belongs to Section 6) |
| Input | "Messy Human Intent" only | Existing Information Surfaces + Tacit Human Reasoning |
| Loop boundary | No visual boundary | Dashed blue rectangle labeled "Canonical Discovery Loop" |

## Design Decisions

- The core loop is visually enclosed to distinguish it from downstream consequences.
- Inference is labeled "provisional hypothesis" in gold italic to signal provisionality.
- Confirmation is highlighted with a gold border and lists four response types (correct, reject, qualify, bound) — not a yes/no checkbox.
- The re-entry arrow (dashed gold, labeled "new uncertainty") shows the loop is repeatable.
- Generate, Preserve, and Learn appear below a "Downstream Consequences" divider in muted styling with a note: "covered by Sections 5, 6, and 8."
- The Reusable Reasoning Surface box lists the four conceptual conditions for reusability (scope, confidence, provenance, applicability boundary) per the source-packet correction.
- Future Topography is labeled with the five topography dimensions.

## Status

Ready for manuscript insertion during Section 7 drafting.
