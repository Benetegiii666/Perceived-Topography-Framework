# v1.0 Figure-Family Harmonization Preview Note

**Date:** 2026-06-19

---

## Purpose

Create harmonized preview copies of Figures 1–7 using Figure 8 as the visual anchor. The goal is to make all figures feel like relatives — simpler instructional plates from the same visual family as the richer capstone Figure 8 — without making them ornate or overdecorated.

This is a preview set for author review only. No originals were overwritten. No manuscript paths were updated.

---

## Hero Figure Reference

**Figure 8:** `paper_assets/png/fig8_perceived_topography_workshop_console.png`

Visual DNA extracted from Figure 8:

- Warm cream/off-white background
- Muted olive, green, teal, brass, and charcoal palette
- Restrained workshop/scientific-instrument feel
- Clean title treatment
- Readable labels
- Disciplined arrows
- Moderate line weight
- Subtle panel framing
- No excessive decoration

---

## Figure Inventory

| Figure | Current title | Current asset path | Asset type | Manuscript display | Narrative role | Harmonization level |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | From Agent Fear to Landscape Design | `paper_assets/svg/fig1_fear_to_landscape.svg` | SVG | Embedded (line 68) | Teaching — fear vs. landscape reframe | Level 1 |
| 2 | Context Is Not Reasoning State | `paper_assets/svg/fig2_context_vs_reasoning_state.svg` | SVG | Embedded (line 187) | Teaching — context vs. reasoning state | Level 1 |
| 3 | Optimizer in a Perceived Topography | `paper_assets/svg/fig3_optimizer_in_topography.svg` | SVG | Embedded (line 266) | Teaching — optimizer + 5 dimensions | Level 1 |
| 4 | Motion and Premature Sufficiency | `paper_assets/svg/fig4_motion_and_premature_sufficiency.svg` | SVG | Embedded (line 468) | Teaching — motion, failure shortcut | Level 1 |
| 5 | Learning Is Model Change | `paper_assets/svg/fig5_learning_is_model_change.svg` | SVG | Text placeholder (line 954) | Teaching — learning loop | Level 1 |
| 6 | Runtime Discovery Loop | `paper_assets/svg/fig7_discovery_loop.svg` | SVG | Text placeholder (line 1353) | Teaching — R→I→P→C loop | Level 1 |
| 7 | Reasoning Architecture: Six Objects | `paper_assets/svg/fig6_reasoning_architecture_six_objects.svg` | SVG | Text placeholder (line 1752) | Teaching — six-object chain | Level 1 + title fix |
| 8 | Workshop Control Console | `paper_assets/png/fig8_perceived_topography_workshop_console.png` | PNG | Embedded (line 2245) | Capstone — assembled mechanism | Unchanged (hero anchor) |

---

## Palette Translation

| Role | Original hex | Harmonized hex | Description |
| --- | --- | --- | --- |
| Background | `#F7F9FC` | `#F7F2E8` | Cool gray → warm cream |
| Primary accent | `#2E5EAA` | `#6F7F3A` | Blue → olive green |
| Light fill | `#EAF1FF` | `#EFE6D6` | Light blue → soft warm panel |
| Primary text | `#102033` | `#2B2A24` | Dark navy → warm charcoal |
| Secondary text | `#8A94A6` | `#8B8575` | Cool gray → warm gray |
| Success/learning | `#2E8B57` | `#7C9A63` | Forest green → soft green |
| Emphasis/provisional | `#D89A21` | `#B08A3A` | Gold → warm secondary accent |
| Warning/failure | `#B94A48` | `#A65E3A` | Rusty red → warm terra |
| White fills | `#FFFFFF` | `#FAF7F0` | Pure white → off-white |

---

## Preview Assets Created

| Preview file | Source file | Changes applied |
| --- | --- | --- |
| `fig1_harmonized_preview.svg` | `fig1_fear_to_landscape.svg` | Palette swap (9 color mappings) |
| `fig2_harmonized_preview.svg` | `fig2_context_vs_reasoning_state.svg` | Palette swap |
| `fig3_harmonized_preview.svg` | `fig3_optimizer_in_topography.svg` | Palette swap |
| `fig4_harmonized_preview.svg` | `fig4_motion_and_premature_sufficiency.svg` | Palette swap |
| `fig5_harmonized_preview.svg` | `fig5_learning_is_model_change.svg` | Palette swap |
| `fig6_harmonized_preview.svg` | `fig7_discovery_loop.svg` | Palette swap (title already correct: "Figure 6") |
| `fig7_harmonized_preview.svg` | `fig6_reasoning_architecture_six_objects.svg` | Palette swap + title fix ("Figure 6" → "Figure 7") |
| `fig8_hero_reference.png` | `fig8_perceived_topography_workshop_console.png` | Unchanged copy for comparison |

**Verification:** Zero instances of the original cool palette (`#F7F9FC`, `#2E5EAA`, `#102033`) remain in any preview SVG.

---

## Contact Sheet / Review Index

**HTML contact sheet:** `paper_assets/preview_harmonized_figures/v1_0_figure_family_contact_sheet.html`

Open this file in a browser to see all 8 figures side by side with:

- Figure number and short title
- Source and preview asset paths
- Harmonization level
- Per-figure notes
- Figure 8 highlighted as hero/capstone

---

## Figure-by-Figure Notes

### Figure 1 — From Agent Fear to Landscape Design

- Two-panel comparison: Agent Fear (left, warm terra accent) vs. Landscape Design (right, olive accent)
- The red/blue semantic contrast from the original translates to terra/olive in the harmonized version
- Layout preserved; no structural changes needed

### Figure 2 — Context Is Not Reasoning State

- Three-column comparison with learning/action layer
- Blue accents → olive; gold emphasis → warm brass
- Clean translation; no layout issues

### Figure 3 — Optimizer in a Perceived Topography

- Most complex teaching figure (130 lines SVG)
- Optimizer State panel, five topography dimensions, goal-relevance projection
- Multiple accent colors; all translated cleanly
- Consider whether the five-dimension labels remain readable at the new contrast level

### Figure 4 — Motion and Premature Sufficiency

- Normal motion path (olive) vs. failure shortcut (warm terra)
- The semantic contrast between safe and unsafe paths must remain clear
- Original used blue vs. red; harmonized uses olive vs. terra — still distinct

### Figure 5 — Learning Is Model Change

- Learning loop with prediction error accent
- Brass accent for prediction error moment is effective
- "≠ Learning" comparison section uses warm terra for contrast

### Figure 6 — Runtime Discovery Loop

- Retrieve → Infer → Propose → Confirm core loop
- Confirm step highlighted with warm brass border
- Re-entry arrow in brass
- Downstream consequences muted in warm gray
- Title already correct ("Figure 6")

### Figure 7 — Reasoning Architecture: Six Objects

- Six-object state-transition chain
- Title corrected from "Figure 6" to "Figure 7" in the preview copy
- Learning Event uses brass accent; Model Update Object uses soft green
- Source artifacts section in warm gray
- Most detailed architecture figure — benefits from the warm palette softening

---

## PNG Rendering Status

**SVG-to-PNG rendering is not available in this environment.** The preview assets are SVG files that can be:

1. Opened directly in a browser for visual review
2. Rendered to PNG using external tools (e.g., Inkscape, Chrome screenshot, Figma import)
3. Used as-is if the final publication accepts SVG

The HTML contact sheet embeds the SVGs via `<img>` tags and can be opened in any browser for side-by-side comparison.

**Figure 8 is PNG-only** — it was created externally and is included as a copy for comparison.

---

## Known Issues

1. **Section 8 SVG title:** The original `fig6_reasoning_architecture_six_objects.svg` still has its `<title>` saying "Figure 6" even though the manuscript displays it as Figure 7. The **preview copy** (`fig7_harmonized_preview.svg`) has the title corrected to "Figure 7." The original has not been edited.

2. **SVG font dependency:** All SVGs reference `Inter, Helvetica, Arial, sans-serif`. If Inter is not installed, the system will fall back to Helvetica or Arial. This is unchanged from the originals.

3. **Figure 8 palette mismatch:** Figure 8 uses a richer, more ornamental palette with photographic landscape imagery, textured backgrounds, and decorative framing. The harmonized Figures 1–7 use a flatter, simpler warm palette derived from Figure 8's color tokens. This is intentional — the teaching figures should be simpler instructional plates, not miniature versions of the hero graphic.

4. **Semantic color contrast:** The original figures used blue (positive/system) vs. red (failure/warning) as a strong semantic contrast. The harmonized version uses olive (positive/system) vs. warm terra (failure/warning). This contrast is weaker than the original blue/red. Author should verify that the semantic distinction remains clear, especially in Figure 1 (fear vs. landscape) and Figure 4 (normal path vs. failure shortcut).

---

## Recommended Next Decision

The author should:

1. **Open the HTML contact sheet** in a browser to review all figures side by side.
2. **Assess whether the warm palette** preserves enough semantic contrast for the teaching figures (especially Figures 1 and 4).
3. **Decide whether to:**
   - Accept the harmonized previews and replace the originals
   - Request adjustments to specific figures (e.g., stronger failure-warning contrast)
   - Keep the originals and harmonize only selected figures
   - Defer harmonization to a final design pass

If accepted, the next steps would be:

1. Replace original SVGs with the harmonized versions
2. Update the Section 8 original SVG title from "Figure 6" to "Figure 7"
3. Render SVGs to PNG if needed for the final publication format
4. Update manuscript image paths if the file structure changes

---

## No-Edit Confirmation

- Working manuscript edited: No
- Rewrite queue edited: No
- Source packets edited: No
- Review packets edited other than this note: No
- Original figure assets overwritten: No
- References edited: No
- Figures or SVGs in original locations edited: No
- SESSION_START.md edited: No
