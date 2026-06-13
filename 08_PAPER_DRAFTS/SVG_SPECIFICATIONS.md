# SVG Specifications

> These are conceptual anchors for the narrative paper, not decorative graphics.

**Status:** Revised after diagram audit. 7 diagrams specified. SVG generation pending.
**Date:** 2026-06-12 (revised)

---

## Style System

### General Style
Clean academic / systems-paper style. Calm, minimal, readable. Not cartoonish, not overly futuristic, not fear-driven.

Visual tone: systems architecture meets field guide.

### Canvas Sizes
- Default: `1200 x 720`
- Two-column: `1400 x 760`
- Loop diagrams: `1200 x 900`
- Wide flow diagrams: `1400 x 820`

### Typography
System-safe sans-serif: `Inter, Helvetica, Arial, sans-serif`

| Element | Size |
|---------|------|
| Title | 30-36px |
| Panel headings | 22-26px |
| Node labels | 16-20px |
| Small annotations | 13-15px |
| Caption text | 14-16px |

### Color Palette

| Purpose | Color | Hex |
|---------|-------|-----|
| Dark navy (text, primary) | Dark blue | #102033 |
| Mid blue (nodes, accents) | Medium blue | #2E5EAA |
| Soft blue (backgrounds) | Light blue | #EAF1FF |
| Safe path / validated / learning | Green | #2E8B57 |
| Uncertainty / warning | Amber | #D89A21 |
| Risk / blocked / premature sufficiency | Red | #B94A48 |
| Gray boundary | Gray | #8A94A6 |
| Light background | Near-white | #F7F9FC |
| Node fill | White | #FFFFFF |

### Visual Grammar

| Element | Meaning |
|---------|---------|
| Rounded rectangles | Reasoning objects |
| Solid arrows | State transitions, primary causal flow |
| Dashed arrows | Inference, provisional reasoning, feedback, optional paths |
| Contour / field lines | Topography, gradients, landscape |
| Thick boundary lines | Policy constraints |
| Warning color (amber/red) | Prediction error, premature sufficiency, unsafe path |
| Green / positive accent | Learning, model update, validated change |
| Neutral blue / gray | Normal reasoning flow |

Avoid heavy icon use. Avoid corporate "process diagram clutter."

### Accessibility
Each SVG must include `<title>` and `<desc>` elements. Diagrams must be understandable in grayscale — do not rely only on color to convey meaning. Use labels directly on shapes rather than relying only on color. Avoid tiny text. Diagrams should work at paper width.

---

## File Structure

```
paper_assets/
  svg/
    fig1_fear_to_landscape.svg
    fig2_context_vs_reasoning_state.svg
    fig3_optimizer_in_topography.svg
    fig4_motion_and_premature_sufficiency.svg
    fig5_learning_is_model_change.svg
    fig6_reasoning_architecture_six_objects.svg
    fig7_runtime_discovery_loop.svg
```

### Markdown Embedding

```markdown
![From Agent Fear to Landscape Design](paper_assets/svg/fig1_fear_to_landscape.svg)
```

---

## Figure 1 — From Agent Fear to Landscape Design

**File:** `svg/fig1_fear_to_landscape.svg`
**Placement:** Section 1
**Importance:** High
**Reader Aha:** The agent is not only something to box; it is something moving through a designed landscape.
**Canvas:** 1400 x 760
**Layout:** Two-panel comparison

### Left Panel: Agent Fear Frame

```
Agent as isolated actor
    ↓
Box / containment emphasis
    ↓
Focus on model behavior alone
    ↓
Question: What is wrong with the agent?
```

Visual: agent node inside a simple box, emphasis on restriction and monitoring.

### Right Panel: Topography Design Frame

```
Agent embedded in landscape
    ↓
Visible policies
Available tools
Evidence paths
Approval gates
Prior learning
    ↓
Question: What landscape shapes behavior?
```

Visual: agent node inside a shaped landscape with visible paths, policy boundaries, evidence markers, and learning connections. The agent moves through the landscape rather than pressing against a wall.

### Caption

> The question is not only whether the agent is dangerous. The better question is what landscape we asked it to move through.

### Notes

Absorbs the original "Fear Framing vs Topography Framing" diagram. Also absorbs the useful visual contrast from the original "Box-First Safety vs Topography-First Safety" diagram.

---

## Figure 2 — Context Is Not Reasoning State

**File:** `svg/fig2_context_vs_reasoning_state.svg`
**Placement:** Section 3
**Importance:** High
**Reader Aha:** Retrieving the right document is not the same as preserving why that document mattered.
**Canvas:** 1400 x 760
**Layout:** Three-layer vertical stack

### Top Layer: Context Layer

```
Documents, policies, campaigns, dashboards, notes, transcripts
```

Label: *What does the organization know?*

### Middle Layer: Reasoning-State Layer

```
Goal, Policy, Interpretation, Premise Stack, Decision State, Confidence, Sufficiency
```

Label: *What should the system do with what it knows?*

### Bottom Layer: Action / Learning Layer

```
Generated artifact, tool action, outcome, prediction error, model update
```

Label: *What happened, and what changed?*

### Caption

> Context preserves artifacts. Reasoning state preserves why artifacts shaped action. The action/learning layer preserves how reality responded and what should change.

### Notes

Updated from the original two-column "Context vs Reasoning State" to a three-layer stack showing the full path from knowledge through reasoning to learning.

---

## Figure 3 — Optimizer in a Perceived Topography

**File:** `svg/fig3_optimizer_in_topography.svg`
**Placement:** Early Section 5, immediately after Information Topography is introduced.
**Importance:** CRITICAL — non-negotiable
**Reader Aha:** The optimizer does not navigate reality directly; it navigates perceived topography.
**Canvas:** 1400 x 900
**Layout:** Three-region horizontal with overlay

**This is the most important diagram in the paper. It visually explains the title of the framework.**

### Left Region: Optimizer State

```
Goal         — What am I trying to achieve?
Policy       — What constraints govern behavior?
Interpretation — What does this information mean?
```

### Center Region: Perceived Topography

```
Visibility     — Can this be perceived?
Accessibility  — Can this be reached?
Representation — How is this expressed?
Confidence     — How trustworthy is this?
Connectivity   — What is this connected to?
```

Use subtle contour lines or field lines to make "topography" feel visual, not merely tabular.

### Right Region: Motion

```
Attraction
Investigation
Sufficiency
Action
```

### Overlays

**Goal Relevance:** Shown as a directional projection/filter from Goal onto the topography, not as a separate box in the dimension list.

**Policy:** Shown as a boundary or guardrail around or within the topography, not as a sixth dimension.

### Caption

> The optimizer does not move through objective reality directly. It moves through a perceived topography shaped by what is visible, accessible, represented, trusted, and connected. Behavior emerges from the interaction between optimizer state and perceived landscape.

### Design Notes

This diagram must avoid looking like a table or org chart. The topography region should feel like a landscape — use contour lines, subtle gradients, or field-like visual patterns. The optimizer "enters" the topography from the left. Motion "emerges" from the right.

---

## Figure 4 — Motion and Premature Sufficiency

**File:** `svg/fig4_motion_and_premature_sufficiency.svg`
**Placement:** Section 6 or Section 7
**Importance:** High
**Reader Aha:** Many failures are not mysterious; they are premature sufficiency.
**Canvas:** 1400 x 820
**Layout:** Process flow with failure shortcut

### Normal Motion Path (top)

```
Attraction → Investigation → Sufficiency → Action
```

Along the path, show intervention points:
- Evidence needed
- Policy check
- Confidence calibration
- Human approval
- Prior model update
- Escalation option

### Failure Shortcut (below, branching off after Attraction)

```
Attraction → Premature Sufficiency → Unsupported / Unsafe Action
```

Mark the shortcut in amber/red. Label: "Insufficient grounding, weak policy, misplaced confidence."

### Caption

> Many failures happen when the system reaches sufficiency too early. Normal motion includes investigation, evidence, and policy checks. Premature sufficiency skips these steps and produces unsupported claims or unsafe actions.

### Notes

Absorbs the useful parts of the original "Box-First Safety vs Topography-First Safety" diagram. Directly supports Section 7 (hallucination and harmful action as premature sufficiency).

---

## Figure 5 — Learning Is Model Change

**File:** `svg/fig5_learning_is_model_change.svg`
**Placement:** Section 8 or Section 9
**Importance:** High
**Reader Aha:** Learning is not storage; learning is model change after prediction error.
**Canvas:** 1200 x 900
**Layout:** Loop with side contrast

### Main Loop

```
Expectation
    ↓
Action
    ↓
Outcome
    ↓
Prediction Error
    ↓
Investigation
    ↓
Evidence-Supported Explanation
    ↓
Model Update
    ↓
Changed Future Optimizer State / Topography
```

The final node loops back to the beginning (changed state produces new expectations).

### Side Contrast (left or bottom)

Three items marked with "≠ Learning":

```
Storage ≠ Learning
Postmortem ≠ Learning
Reaction ≠ Learning
```

### Caption

> Learning occurs when prediction error is investigated, explained with evidence, and converted into a model update that changes future reasoning. Storage, postmortems, and reactions alone are not learning.

### Notes

New diagram — was missing from the original 5-diagram plan. Supports Sections 8-9 and helps readers understand the learning distinction quickly.

---

## Figure 6 — Reasoning Architecture: Six Objects Preserve the State Transition

**File:** `svg/fig6_reasoning_architecture_six_objects.svg`
**Placement:** Section 10
**Importance:** CRITICAL — non-negotiable
**Reader Aha:** The durable unit is not the document, but the optimizer state transition.
**Canvas:** 1400 x 820
**Layout:** Horizontal chain with supporting layer

### Main Chain (center)

```
Optimizer State → Premise Stack → Decision State → Investigation Trace → Learning Event → Model Update Object
```

Each object as a rounded rectangle with brief label inside.

### Above the Chain

State transition description:

```
what was believed → why it was believed → what was chosen → what was tested → what changed
```

### Below the Chain

Source artifacts supporting the chain:

```
documents, policies, dashboards, notes, postmortems, metrics
```

Connected to relevant objects with light dashed arrows.

### Caption

> The unit of organizational reasoning is not the document. It is the optimizer state transition. Documents provide evidence and context. Reasoning objects preserve how that evidence shaped action and learning.

### Notes

Replaces the original "Core Framework Loop" diagram. The completed paper needs the six-object architecture specifically rather than a generic loop.

---

## Figure 7 — Runtime Discovery Loop

**File:** `svg/fig7_runtime_discovery_loop.svg`
**Placement:** Section 11 or Section 12
**Importance:** High
**Reader Aha:** Discovery is how messy intent becomes structured reasoning without making the user fill out a form.
**Canvas:** 1400 x 820
**Layout:** Horizontal flow left-to-right with output objects below

### Main Flow (8 nodes)

| # | Node | Contents |
|---|------|----------|
| 1 | Messy Human Intent | "I want to do a healthcare campaign." |
| 2 | Retrieve | existing artifacts, prior campaigns, policies, model updates |
| 3 | Infer | goal, ICP, constraints, premises |
| 4 | Propose | strawman, confidence, gaps |
| 5 | Confirm | ask only material questions |
| 6 | Generate | brief, assets, measurement plan |
| 7 | Preserve | reasoning objects, decision state |
| 8 | Learn | outcome, prediction error, model update |

### Output Object Row (below main flow)

Connected smaller boxes:

```
Optimizer State — Premise Stack — Decision State — Investigation Trace — Learning Event — Model Update Object — Discovery Pattern Update
```

Vertical arrows from relevant main nodes:
- Infer → Optimizer State / Premise Stack
- Confirm → Decision State
- Preserve → Investigation Trace / Decision State
- Learn → Learning Event / Model Update Object / Discovery Pattern Update

### Visual Notes
- Human-intent node slightly irregular/cloud-like (messy → structured)
- Reasoning objects as clean rectangles (structure emerging from ambiguity)
- Green/blue on main path, amber for confidence gaps

### Caption

> Runtime discovery reduces user burden by retrieving and inferring before asking. The output is not only generated content, but preserved reasoning state that can be learned from later.

---

## Diagrams Deprioritized or Merged

### Original Diagram 3 — Box-First Safety vs Topography-First Safety

**Decision:** Merged into Figure 1 (fear vs landscape) and Figure 4 (premature sufficiency). The contrast is important but redundant as a standalone after Sections 16-17.

### Original Diagram 4 — Core Framework Loop

**Decision:** Replaced by more specific diagrams: Figure 5 (Learning) and Figure 6 (Six-Object Architecture). The completed paper has more precise needs than a generic loop.

---

## Updated Placement Map

| Figure | Title | Section |
|--------|-------|---------|
| 1 | From Agent Fear to Landscape Design | Section 1 |
| 2 | Context Is Not Reasoning State | Section 3 |
| 3 | Optimizer in a Perceived Topography | **Early Section 5** (locked) |
| 4 | Motion and Premature Sufficiency | Section 6 or 7 |
| 5 | Learning Is Model Change | Section 8 or 9 |
| 6 | Reasoning Architecture: Six Objects | Section 10 |
| 7 | Runtime Discovery Loop | Section 11 or 12 |

---

## Production Notes

### Generation Order

Generate rough SVGs in this order (hardest first — if Figure 3 works, the rest inherit its visual language):

1. Figure 3 — Optimizer in a Perceived Topography (CRITICAL)
2. Figure 6 — Reasoning Architecture: Six Objects (CRITICAL)
3. Figure 5 — Learning Is Model Change
4. Figure 7 — Runtime Discovery Loop
5. Figure 1 — From Agent Fear to Landscape Design
6. Figure 2 — Context Is Not Reasoning State
7. Figure 4 — Motion and Premature Sufficiency

### Acceptance Criteria for First SVG Pass

Each rough SVG should be judged against:

- Can the reader understand the diagram in 10 seconds?
- Does the diagram teach something the paragraph alone does not?
- Does it preserve the framework's terminology exactly?
- Does it avoid adding new theory?
- Does it work in grayscale?
- Does it have one clear aha?
- Does it look like systems architecture meets field guide?

Do not polish colors, spacing, or typography until the conceptual layout passes.

### Paper Text Notes
Each diagram should include a short note in the paper text (not inside the SVG) explaining:
- Diagrams are conceptual
- Topography and gradients are analytic metaphors
- Containment and topography are complementary, not mutually exclusive

### Diagram Count
Recommended final count: **7 diagrams.** Do not exceed 8 unless peer review shows a specific comprehension gap.
