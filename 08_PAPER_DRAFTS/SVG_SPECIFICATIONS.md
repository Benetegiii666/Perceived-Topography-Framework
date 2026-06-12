# SVG Specifications

> These are conceptual anchors for the narrative paper, not decorative graphics.

**Status:** Specifications complete. SVG generation pending after Sections 3-6 stabilize.
**Date:** 2026-06-12

---

## Style System

### General Style
Clean academic / systems-paper style. Calm, minimal, readable. Not cartoonish, not overly futuristic, not fear-driven.

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
| Safe path / validated | Green | #2E8B57 |
| Uncertainty / warning | Amber | #D89A21 |
| Risk / blocked | Red | #B94A48 |
| Gray boundary | Gray | #8A94A6 |
| Light background | Near-white | #F7F9FC |
| Node fill | White | #FFFFFF |

### Visual Conventions
- Solid arrows = primary causal / process flow
- Dashed arrows = feedback / influence
- Thick boundary lines = policy / containment
- Soft shaded regions = topography / environment
- Small warning icons = risk or uncertainty
- Small check icons = validated / evidence-backed

### Accessibility
Each SVG must include `<title>` and `<desc>` elements. Diagrams must be understandable in grayscale — do not rely only on color to convey meaning.

---

## File Structure

```
paper_assets/
  svg/
    fear_vs_topography.svg
    context_vs_reasoning_state.svg
    box_first_vs_topography_first.svg
    core_framework_loop.svg
    runtime_discovery_loop.svg
```

### Markdown Embedding

```markdown
![Fear framing vs topography framing](paper_assets/svg/fear_vs_topography.svg)
```

---

## Diagram 1 — Fear Framing vs Topography Framing

**File:** `svg/fear_vs_topography.svg`
**Placement:** Section 1
**Canvas:** 1400 x 760
**Layout:** Two-column comparison with vertical divider

### Left Panel: Conventional Fear Framing

Vertical flow (4 nodes):

```
Model + tools                    (annotation: goal, access, autonomy)
    ↓
Disturbing behavior              (annotation: deception, evasion, harmful action)
    ↓
Moralized interpretation         ("the agent is becoming dangerous")
    ↓
Response                         (stronger fences)
```

Red/amber accents lightly around "disturbing behavior." Simple box around containment node.

### Right Panel: Topography Framing

Vertical flow (4 nodes):

```
Optimizer + goal + tools         (annotation: goal-directed behavior under constraints)
    ↓
Perceived gradients              (annotation: visibility, confidence, cost, access, policy salience)
    ↓
Topography/policy/confidence     (annotation: harmful path appeared useful, available, or sufficient)
failure
    ↓
Response                         (reshape gradients and affordances)
```

Subtle landscape curve behind right-side nodes. Arrows move through landscape, not against fence.

### Caption

> The Perceived Topography Framework does not deny agentic risk. It reframes many risky behaviors as optimizer movement through poorly shaped perceived environments rather than as evidence of human-like malice.

---

## Diagram 2 — Context vs Reasoning State

**File:** `svg/context_vs_reasoning_state.svg`
**Placement:** Section 3
**Canvas:** 1400 x 760
**Layout:** Two-column comparison

### Left Column: Context Layer

Contains:

```
documents
chunks
policies
dashboards
campaigns
transcripts
```

Question at bottom: *What can the system retrieve?*

### Right Column: Reasoning-State Layer

Contains:

```
goal
policy
premise stack
decision state
confidence
sufficiency
prediction error
model update
```

Question at bottom: *What should the system do with what it retrieved?*

### Caption

> Context preserves artifacts. Reasoning state preserves the relationship among goals, constraints, premises, decisions, outcomes, and learning.

---

## Diagram 3 — Box-First Safety vs Topography-First Safety

**File:** `svg/box_first_vs_topography_first.svg`
**Placement:** Section 1 or Section 6
**Canvas:** 1400 x 900
**Layout:** Two horizontal panels stacked vertically

### Panel A: Box-First Safety

Agent node inside rectangular box. Boundary labels: sandbox, tool limits, monitoring, permissions, refusal policy. Goal target outside box. Arrow from agent toward target hitting boundary. Label at boundary: "constraint encountered as fence."

Visual meaning: Agent has goal and boundary, but desired path is not designed. Pressure against box without making agent look evil.

### Panel B: Topography-First Safety

Soft landscape with clear path from optimizer to "Evidence-backed, policy-compliant outcome." Along main path: retrieved evidence, visible policy, confidence check, human escalation, sufficiency threshold.

Unsafe side paths with friction markers:
- Unsupported claim → low confidence
- Unsafe tool use → requires approval
- Policy conflict → blocked / escalate

Visual meaning: Desired path is made easier, clearer, and more sufficient than unsafe alternatives.

### Caption

> Containment remains necessary, but topography-first design expands the safety toolkit by shaping what the optimizer can see, trust, access, and treat as sufficient.

---

## Diagram 4 — Core Framework Loop

**File:** `svg/core_framework_loop.svg`
**Placement:** End of Section 3 or beginning of Section 4
**Canvas:** 1200 x 900
**Layout:** Circular loop with 8 major nodes

### Clockwise Node Order

| # | Node | Contents |
|---|------|----------|
| 1 | Optimizer State | Goal, Policy, Interpretation |
| 2 | Information Topography | Visibility, Accessibility, Representation, Confidence, Connectivity |
| 3 | Optimizer Motion | Attraction, Investigation, Sufficiency |
| 4 | Action | answer, tool use, recommendation, workflow step |
| 5 | Outcome | reality responds |
| 6 | Learning Event | prediction error, evidence-supported explanation |
| 7 | Model Update Object | bounded reusable learning |
| 8 | Discovery / Updated Reasoning State | retrieve, infer, propose, confirm |

Node 8 loops back to Node 1.

### Visual Notes
- "Reality" placed lightly outside loop near Outcome
- Dashed feedback arrow: Model Update Object → Information Topography (prior learning changes what future agents retrieve)
- Dashed feedback arrow: Discovery → Optimizer State

### Caption

> The framework treats human-agent work as a loop of state, topography, motion, action, outcome, learning, and rediscovery.

---

## Diagram 5 — Runtime Discovery Loop

**File:** `svg/runtime_discovery_loop.svg`
**Placement:** Section 11
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
- Human-intent node slightly irregular/cloud-like
- Reasoning objects as clean rectangles (structure emerging from ambiguity)
- Green/blue on main path, amber for confidence gaps

### Caption

> Runtime discovery reduces user burden by retrieving and inferring before asking. The output is not only generated content, but preserved reasoning state that can be learned from later.

---

## Production Notes

### First SVG Pass
Conceptual, not final. Generate all five after Sections 3-6 stabilize.

### Paper Text Notes
Each diagram should include a short note in the paper text (not inside the SVG) explaining:
- Diagrams are conceptual
- Topography and gradients are analytic metaphors
- Containment and topography are complementary, not mutually exclusive
