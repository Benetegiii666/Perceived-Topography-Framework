# v1.0 Figure 8 Capstone Asset Note

**Date:** 2026-06-19

---

## Asset Path

```text
paper_assets/png/fig8_perceived_topography_workshop_console.png
```

**Format:** PNG (~2.4 MB)
**Verified:** Yes — file exists at the path above.

---

## Candidate Figure Number

**Figure 8.**

Follows Figure 7 (Reasoning Architecture: Six Objects Preserve the State Transition, Section 8). The manuscript currently displays Figures 1–7 consecutively with no gaps.

---

## Candidate Figure Title

```text
Figure 8. The Perceived Topography Framework as a workshop control console.
```

---

## Candidate Caption

Working candidate — not finalized:

> A reference mechanism for building better perceived landscapes. Fear of agent behavior enters as the design pressure; the working frame, perceived topography, gradient-guided motion, and learning loop show how a system can shape what becomes visible, trusted, sufficient, and learnable before future action.

---

## Intended Narrative Role

Figure 8 is the Section 11 capstone synthesis figure.

Its narrative job is to show the reader where every framework label lives inside a conceptual operating shape. After 10 sections of building the theory, the reader should see the assembled machine: not as a product spec, but as a reference mechanism showing how fear of agent behavior enters, how the working frame and topography shape motion, how gradients guide action through sufficiency, how the learning loop feeds back, and how the output is better landscapes.

The intended reader reaction is:

> The framework was never just a metaphor. It shows where to intervene in the system.

This is the paper's practical punchline.

---

## What the Figure Shows

The image depicts a "Workshop Control Console" metaphor with the following elements:

**Input (left):**
- "Fear of AI Agents" — the design pressure that enters the system
- Framing question: "How can we design systems people can trust and use?"

**Console panels (numbered 2–4):**

- **Panel 2: Working Frame** — Goal, Policy, Interpretation
  - Goal: What the system is trying to achieve
  - Policy: The principles and constraints that guide it
  - Interpretation: How it makes sense of signals and context

- **Panel 3: Perceived Topography** — Visibility, Accessibility, Representation, Confidence, Connectivity
  - Five dimensions of the information landscape

- **Panel 4: Motion: Guided by Gradients** — Attraction, Investigation, Sufficiency, Action
  - The motion model from Section 4

**Learning Loop (bottom, panel 5):**
- Outcome → Prediction Error → Explanation → Model Update Object → Future Reasoning
- Note: "Each loop refines understanding and shapes better landscapes"
- Flow arrow connects back up from Future Reasoning, closing the loop

**Output/Purpose (right):**
- "Build Better Landscapes"
- Safer, more trustworthy outcomes
- Resilient, adaptive landscapes
- Better experiences for people and communities
- Design with understanding; earn trust; improve outcomes

**Bottom tagline:**
- "Shape the landscape. Guide the path. Learn continuously."
- "Better perception. Better motion. Better outcomes."

---

## What the Figure Is Not

The figure is:

- A conceptual operating-shape diagram
- A capstone synthesis figure
- A metaphorical mechanism showing where the framework's concepts live when assembled

The figure is NOT:

- A software architecture diagram
- A vendor platform blueprint
- A prescribed implementation stack
- A database/API/service diagram
- A product roadmap
- A deployment topology

Section 11 prose should explicitly frame Figure 8 as a reference mechanism, not a production design.

---

## Relationship to Figures 1–7

| Figure | Section | Type | Role |
| --- | --- | --- | --- |
| Figure 1 | S1 | Teaching/analytic | Fear → landscape design reframe |
| Figure 2 | S2 | Teaching/analytic | Context vs. reasoning state |
| Figure 3 | S3 | Teaching/analytic | Optimizer in a perceived topography |
| Figure 4 | S4 | Teaching/analytic | Motion and premature sufficiency |
| Figure 5 | S6 | Teaching/analytic | Learning is model change |
| Figure 6 | S7 | Teaching/analytic | Runtime Discovery loop |
| Figure 7 | S8 | Teaching/analytic | Six-object reasoning architecture chain |
| **Figure 8** | **S11** | **Capstone/synthesis** | **The assembled framework as operating shape** |

Figures 1–7 are teaching figures that introduce individual concepts. Figure 8 is the synthesis figure that shows the assembled whole. It is the only figure that brings all framework components into a single visual.

Do not restructure Figures 1–7 because of Figure 8.

---

## Visual Harmonization Guidance

For the later visual pass, the following harmonization notes apply:

1. **Figures 1–7 are SVGs; Figure 8 is a PNG.** This format difference is acceptable for now. If a later visual pass converts Figure 8 to SVG for consistency, the content should be preserved.

2. **Consistent title treatment:** All figures should use the same caption format (`**Figure N. Title**`). Figure 8 should follow this convention.

3. **Consistent caption style:** Brief, argument-bearing captions. Figure 8's caption should explain the figure's argumentative job, not just label its parts.

4. **Shared muted palette:** Figures 1–7 use a blue/gray/white palette (Inter font, `#F7F9FC` background, `#2E5EAA` accents). Figure 8 uses a warm muted earth-tone palette (parchment, brown, gold). A mild harmonization pass could bring Figure 8 closer to the existing palette, but the warm tones may work as a deliberate capstone contrast. Authorial call.

5. **Similar line weight and label hierarchy:** Figures 1–7 use consistent line weights and font sizing. Figure 8 uses a more ornamental style. Mild harmonization to reduce visual mismatch is desirable but should not flatten the capstone effect.

6. **Numbered badges:** Figure 8 uses numbered badges (2, 3, 4, 5) for its console panels. These should not be confused with figure numbers. If ambiguity arises, the numbered badges could be changed to labeled tabs.

7. **Section 8 SVG title cleanup:** `fig6_reasoning_architecture_six_objects.svg` may still have its internal `<title>` element saying "Figure 6" even though the manuscript displays it as Figure 7. This is a known mechanical task for the visual pass.

---

## Open Questions for Section 11 Source Packet

1. **Figure placement:** Should Figure 8 appear at the beginning of Section 11 (as the mechanism the section explains), in the middle (after the mechanism is described in prose), or at the end (as the synthesis payoff)? Recommendation: after the mechanism mapping prose, before the closing imperative.

2. **Caption finalization:** The candidate caption should be refined during Section 11 drafting to match the surrounding prose tone.

3. **Console numbering:** The figure uses numbered panels (2, 3, 4, 5) but skips panel 1. The input ("Fear of AI Agents") is unlabeled. If this creates confusion, the numbering could be removed or renumbered 1–5. Authorial call.

4. **Discovery absent from the console:** The figure shows the Learning Loop but does not explicitly show Discovery (Retrieve → Infer → Propose → Confirm) as a labeled console panel. Discovery is implicitly present in how the Working Frame connects to the Topography, but it is not visually named. The drafter should decide whether to note this in prose or whether the figure is sufficient as-is.

5. **Format for final publication:** PNG is acceptable for drafting but may need conversion or recreation for final publication quality.

---

## Verification Notes

- Asset file verified at `paper_assets/png/fig8_perceived_topography_workshop_console.png`
- File size: ~2.4 MB
- Format: PNG
- Visual content matches described elements: fear input, workshop console, working frame, topography, gradients/motion, learning loop, build-better-landscapes output
- No manuscript edits made
- No source packets edited
- No review packets edited (other than this asset note)
- No existing figures or SVGs edited
- SESSION_START.md not edited
