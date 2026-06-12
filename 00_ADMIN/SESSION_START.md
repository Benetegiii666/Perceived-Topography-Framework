# SESSION_START — Revision Bundle

## Project
Perceived Topography Framework

## Project Status
- **Concept Architecture v0.1:** FROZEN (Phases 1-5 complete)
- **Paper v0.1 Draft:** ALL 17 SECTIONS COMPLETE (~34,000 words)
- **AHA Audit:** COMPLETE — 6 promoted, 2 retired, 6 patches applied
- **Phase 6 (Narrative Paper):** Active — revision passes needed
- **SVGs:** 5 specified, 0 generated
- **Citations:** ~65 unique placeholders, 0 resolved to full references

## Purpose of This Session
Revision passes focused on:
1. Diagram/SVG audit
2. Terminology discipline audit
3. Reader-journey audit
4. Citation debt / related-work alignment
5. Company-adoption roadmap clarity

**Do not rewrite the paper.** Flag issues for targeted patches.

---

# 1. SVG SPECIFICATIONS (Full Copy)

## Style System

Clean academic / systems-paper style. Calm, minimal, readable.

**Canvas Sizes:** Default 1200x720, two-column 1400x760, loop 1200x900, wide flow 1400x820.

**Typography:** Inter, Helvetica, Arial, sans-serif. Title 30-36px, panel headings 22-26px, node labels 16-20px, annotations 13-15px, captions 14-16px.

**Color Palette:**

| Purpose | Hex |
|---------|-----|
| Dark navy (text) | #102033 |
| Mid blue (nodes) | #2E5EAA |
| Soft blue (backgrounds) | #EAF1FF |
| Safe path / validated | #2E8B57 |
| Uncertainty / warning | #D89A21 |
| Risk / blocked | #B94A48 |
| Gray boundary | #8A94A6 |
| Light background | #F7F9FC |
| Node fill | #FFFFFF |

**Visual Conventions:** Solid arrows = causal flow, dashed arrows = feedback, thick lines = policy/containment, shaded regions = topography, warning icons = risk, check icons = validated.

**Accessibility:** `<title>` and `<desc>` required. Must work in grayscale.

**File structure:** `paper_assets/svg/` with 5 files.

---

## Diagram 1 — Fear Framing vs Topography Framing
**File:** `svg/fear_vs_topography.svg` | **Placement:** Section 1 | **Canvas:** 1400x760

Two-column comparison with vertical divider.

**Left Panel (Conventional Fear Framing):** 4 nodes vertical flow: Model+tools → Disturbing behavior → Moralized interpretation ("the agent is becoming dangerous") → Response (stronger fences). Red/amber accents around disturbing behavior.

**Right Panel (Topography Framing):** 4 nodes: Optimizer+goal+tools+permissions → Perceived gradients (visibility, confidence, cost, access, policy salience) → Topography/policy/confidence failure (harmful path appeared useful, available, or sufficient) → Response (reshape gradients and affordances). Subtle landscape curve behind nodes.

**Caption:** "The Perceived Topography Framework does not deny agentic risk. It reframes many risky behaviors as optimizer movement through poorly shaped perceived environments rather than as evidence of human-like malice."

---

## Diagram 2 — Context vs Reasoning State
**File:** `svg/context_vs_reasoning_state.svg` | **Placement:** Section 3 | **Canvas:** 1400x760

Two-column comparison.

**Left (Context Layer):** documents, chunks, policies, dashboards, campaigns, transcripts. Question: "What can the system retrieve?"

**Right (Reasoning-State Layer):** goal, policy, premise stack, decision state, confidence, sufficiency, prediction error, model update. Question: "What should the system do with what it retrieved?"

**Caption:** "Context preserves artifacts. Reasoning state preserves the relationship among goals, constraints, premises, decisions, outcomes, and learning."

---

## Diagram 3 — Box-First Safety vs Topography-First Safety
**File:** `svg/box_first_vs_topography_first.svg` | **Placement:** Section 1 or 6 | **Canvas:** 1400x900

Two panels stacked vertically.

**Panel A (Box-First):** Agent inside rectangular box. Boundary labels: sandbox, tool limits, monitoring, permissions, refusal policy. Goal target outside. Arrow hits boundary. Label: "constraint encountered as fence."

**Panel B (Topography-First):** Soft landscape with clear path from optimizer to "Evidence-backed, policy-compliant outcome." Along path: retrieved evidence, visible policy, confidence check, human escalation, sufficiency threshold. Unsafe side paths with friction: unsupported claim (low confidence), unsafe tool use (requires approval), policy conflict (blocked/escalate).

**Caption:** "Containment remains necessary, but topography-first design expands the safety toolkit by shaping what the optimizer can see, trust, access, and treat as sufficient."

---

## Diagram 4 — Core Framework Loop
**File:** `svg/core_framework_loop.svg` | **Placement:** End of Section 3 or beginning of Section 4 | **Canvas:** 1200x900

Circular loop, 8 nodes clockwise:

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

Node 8 loops to Node 1. "Reality" placed lightly outside near Outcome. Dashed feedback: MUO → Topography, Discovery → Optimizer State.

**Caption:** "The framework treats human-agent work as a loop of state, topography, motion, action, outcome, learning, and rediscovery."

---

## Diagram 5 — Runtime Discovery Loop
**File:** `svg/runtime_discovery_loop.svg` | **Placement:** Section 11 | **Canvas:** 1400x820

Horizontal flow left-to-right, output objects below.

**Main Flow (8 nodes):** Messy Human Intent ("I want to do a healthcare campaign") → Retrieve (artifacts, campaigns, policies, model updates) → Infer (goal, ICP, constraints, premises) → Propose (strawman, confidence, gaps) → Confirm (material questions only) → Generate (brief, assets, measurement) → Preserve (reasoning objects, decision state) → Learn (outcome, prediction error, model update)

**Output Row (below):** Optimizer State — Premise Stack — Decision State — Investigation Trace — Learning Event — Model Update Object — Discovery Pattern Update. Vertical arrows from Infer, Confirm, Preserve, Learn to relevant objects.

Human-intent node slightly irregular/cloud-like. Reasoning objects as clean rectangles. Green/blue main path, amber for gaps.

**Caption:** "Runtime discovery reduces user burden by retrieving and inferring before asking. The output is not only generated content, but preserved reasoning state that can be learned from later."

---

# 2. RELATED WORK LEDGER (Full Copy)

## Citation Posture
> The framework does not claim ownership over the ingredients. It claims responsibility for the mix.

## Citation Placeholders
```
[SIMON1955] [MARCH_SIMON_ORGS] [CYERT_MARCH] [ARGYRIS_SCHON] [WEICK_SENSEMAKING]
[GIBSON_AFFORDANCES] [NORMAN_AFFORDANCES] [NG_REWARD_SHAPING]
[ANTHROPIC_AGENTIC_MISALIGNMENT] [OPENAI_PREPAREDNESS] [DEEPMIND_FRONTIER_SAFETY]
[DEEPMIND_ROLE_PLAY] [DEEPMIND_GOPHERCITE] [RAG_FOUNDATIONAL]
```

## 11 Influence Categories

| # | Category | Key Sources | Required Citations | Where to Cite | Status |
|---|----------|------------|-------------------|---------------|--------|
| 1 | Bounded Rationality / Satisficing | Simon | Simon 1955, satisficing work | Terms (Sufficiency), Motion, Validation | Placeholder used |
| 2 | Organizational Decision-Making | March & Simon | Organizations (1958) | Context≠Reasoning, Architecture, Related | Placeholder used |
| 3 | Behavioral Theory of the Firm | Cyert & March | Behavioral Theory of the Firm (1963) | Learning, MUOs, Related | Placeholder used |
| 4 | Organizational Learning | Argyris & Schon | Organizational Learning (1978) | Learning, MUOs, Discovery Pattern | Placeholder used |
| 5 | Sensemaking | Weick | Sensemaking in Organizations (1995) | Topography, Interpretation, Premise Stack | Placeholder used |
| 6 | Affordances | Gibson, Norman | Ecological Approach (1979), Design of Everyday Things (1988) | Terms, Safety, Discovery | Placeholder used |
| 7 | Reward Shaping | Ng, Harada, Russell | Policy invariance / reward shaping (1999 ICML) | Gradients, Safety, Related | Placeholder used |
| 8 | AI Safety / Agentic Misalignment | Anthropic, OpenAI, DeepMind | Agentic misalignment, Preparedness, Frontier Safety, role-play paper | Opening, Safety, Validation | Placeholder used |
| 9 | Hallucination / Grounding | GopherCite, RAG lit | GopherCite, Lewis et al. 2020 | Hallucination section, Confidence, MUOs | Placeholder used |
| 10 | Knowledge Management | KM literature | **To be researched** | Context≠Reasoning, Architecture, MUOs | **Placeholder only** |
| 11 | Human-AI Collaboration / HCI | HCI, CSCW, mixed-initiative | **To be researched** | Discovery, Discovery Pattern, Validation | **Placeholder only** |

**Drafting rule:** Every paper section should end with a citation debt checklist.

**Caveat for Category 7:** The framework's "gradient" is broader than formal reward shaping and should not be treated as equivalent to an RL reward function.

---

# 3. PAPER DRAFT — Table of Contents

```
# 1. Introduction: From Agent Fear to Topography Design (line 13)

# 2. A Note on Terms (line 101)
   [25 terms defined: optimizer, agent, goal, policy, interpretation, reasoning state,
    topography, perceived topography, information surface, gradient, visibility,
    accessibility, representation, confidence, connectivity, attraction, investigation,
    sufficiency, action, prediction error, learning, premise stack, model update object,
    discovery, alignment, governance, hallucination]

# 3. The Problem: Context Is Not Reasoning State (line 346)

# 4. Optimizers: Goal, Policy, Interpretation (line 563)
   ## 4.1 Goal
   ## 4.2 Policy
   ## 4.3 Interpretation
   ## 4.4 Optimizer State
   ## 4.5 Why These Three Primitives Are Enough
   ## 4.6 Why This Matters for Agent Safety
   ## 4.7 Transition to Information Topography

# 5. Information Topography: What the Optimizer Navigates (line 876)
   ## 5.1 Five Dimensions of Information Topography
   ## 5.2 Visibility
   ## 5.3 Accessibility
   ## 5.4 Representation
   ## 5.5 Confidence
   ## 5.6 Connectivity
   ## 5.7 Why Goal Relevance Is Relational
   ## 5.8 Policy as Boundary Condition, Not Dimension
   ## 5.9 Topography and Affordances
   ## 5.10 Information Topography in the Healthcare Campaign Example
   ## 5.11 Information Topography and Safety
   ## 5.12 Transition to Motion

# 6. Gradients and Motion: How Behavior Emerges (line 1210)
   ## 6.1 Gradients
   ## 6.2 Attraction
   ## 6.3 Investigation
   ## 6.4 Task Spawning
   ## 6.5 Sufficiency
   ## 6.6 Action
   ## 6.7 Motion in the Healthcare Campaign Example
   ## 6.8 Motion in Safety Failures
   ## 6.9 Motion and Design
   ## 6.10 Transition to Learning

# 7. Hallucination and Harmful Action as Related Failures (line 1525)
   ## 7.1 Hallucination as Premature Sufficiency
   ## 7.2 Harmful Action as Premature Sufficiency
   ## 7.3 The Shared Failure Grammar
   ## 7.4 Why More Context Is Not Enough
   ## 7.5 Unsupported Claims and Unsafe Actions
   ## 7.6 The Role of "I Don't Know" and "I Should Not Act Yet"
   ## 7.7 Same Pattern, Different Severity
   ## 7.8 Implications for Evaluation
   ## 7.9 Transition to Learning

# 8. Learning: When Reality Pushes Back (line 1776)
   ## 8.1 Expectation
   ## 8.2 Action
   ## 8.3 Outcome
   ## 8.4 Prediction Error
   ## 8.5 Investigation
   ## 8.6 Evidence-Supported Explanation
   ## 8.7 Model Update
   ## 8.8 Reaction Is Not Learning
   ## 8.9 Postmortem Is Not Learning
   ## 8.10 Learning in the Healthcare Campaign Example
   ## 8.11 Learning in Agent Safety
   ## 8.12 Learning Changes the Topography
   ## 8.13 The Learning Loop

# 9. Model Update Objects: Making Learning Durable (line 2119)
   ## 9.1 Why Ordinary Documentation Is Not Enough
   ## 9.2 The Three-Layer Structure
   ## 9.3 Core Learning Payload
   ## 9.4 Observability Envelope
   ## 9.5 Human-Ready View
   ## 9.6 Example Model Update Object
   ## 9.7 Failure Modes Prevented
   ## 9.8 Model Update Objects Reshape Topography
   ## 9.9 Transition to Reasoning Architecture

# 10. Reasoning Architecture: Preserving State Transitions (line 2362)
   ## 10.1 Why Documents Are Not Enough
   ## 10.2 Six Minimum Viable Reasoning Objects
   ## 10.3 Optimizer State
   ## 10.4 Premise Stack
   ## 10.5 Decision State
   ## 10.6 Investigation Trace
   ## 10.7 Learning Event
   ## 10.8 Model Update Object
   ## 10.9 Supporting Concerns
   ## 10.10 The Objects as a State-Transition Chain
   ## 10.11 Healthcare Campaign Example
   ## 10.12 Agent Safety Example
   ## 10.13 Relationship to Knowledge Management
   ## 10.14 Relationship to AI Agents
   ## 10.15 Transition to Discovery

# 11. Discovery Framework: From Messy Intent to Reasoning State (line 2633)
   ## 11.1 Why Discovery Matters
   ## 11.2 Initial Discovery and Runtime Discovery
   ## 11.3 Retrieve
   ## 11.4 Infer
   ## 11.5 Propose
   ## 11.6 Confirm
   ## 11.7 Generate
   ## 11.8 Preserve
   ## 11.9 Learn
   ## 11.10 Discovery Pattern Updates
   ## 11.11 The Low-Friction Principle
   ## 11.12 Discovery and Human Control
   ## 11.13 Discovery and Safety
   ## 11.14 Discovery in the Healthcare Campaign Example
   ## 11.15 Discovery as the Front Door to Reasoning Architecture
   ## 11.16 Transition to the Running Example

# 12. Running Example: Adaptive Campaign Reasoning Studio (line 2923)
   ## 12.1 Starting Point: Messy Human Intent
   ## 12.2 Retrieve
   ## 12.3 Infer
   ## 12.4 Propose
   ## 12.5 Confirm
   ## 12.6 Sufficiency
   ## 12.7 Generate
   ## 12.8 Preserve
   ## 12.9 Outcome
   ## 12.10 Learning Event
   ## 12.11 Model Update Object
   ## 12.12 Discovery Pattern Update
   ## 12.13 Next Campaign: Starting Smarter
   ## 12.14 What This Example Demonstrates
   ## 12.15 Transition to Implementation

# 13. Implementation Bridge: From Context Layer to Reasoning-State Layer (line 3157)
   ## 13.1 Layer 1: Context Layer
   ## 13.2 Layer 2: Reasoning-State Layer
   ## 13.3 Layer 3: Learning Layer
   ## 13.4 Layer 4: Adaptive Workflow Studio
   ## 13.5 Minimal Viable Implementation
   ## 13.6 System Components
   ## 13.7 Data Model Sketch
   ## 13.8 Retrieval Requirements
   ## 13.9 Human Review and Governance
   ## 13.10 Implementation Maturity Model
   ## 13.11 What Not to Build First
   ## 13.12 Implementation Risks
   ## 13.13 Implementation Success Criteria
   ## 13.14 Transition to Validation

# 14. Validation and Falsifiability (line 3409)
   ## 14.1 What the Framework Claims
   ## 14.2 What Would Falsify the Framework?
   ## 14.3 Levels of Validation
   ## 14.4 Conceptual Validation
   ## 14.5 Operational Validation
   ## 14.6 Comparative Validation
   ## 14.7 Adversarial Validation
   ## 14.8 Longitudinal Validation
   ## 14.9 Human Validation
   ## 14.10 Outcome Validation
   ## 14.11 Evaluation of the Six Reasoning Objects
   ## 14.12 Evaluation of the Five Topography Dimensions
   ## 14.13 Validation in the Healthcare Campaign MVP
   ## 14.14 The Framework Should Update Itself
   ## 14.15 Transition to Related Work

# 15. Related Work and Intellectual Lineage (line 3646)
   ## 15.1–15.15 (15 influence categories)
   ## 15.16 What the Framework Adds
   ## 15.17 Boundaries of the Contribution
   ## 15.18 Citation Posture
   ## 15.19 Transition to Implications

# 16. Implications: What Changes If the Framework Is Useful (line 3850)
   ## 16.1–16.13 (13 implications)
   ## 16.14 Transition to Conclusion

# 17. Conclusion: Build Better Landscapes (line 4032)
   ## 17.1 The Core Aha
   ## 17.2 Failure Has Shape
   ## 17.3 Learning Is Not Memory
   ## 17.4 Discovery Is the Front Door
   ## 17.5 What Changes
   ## 17.6 The Responsibility of the Landscape
   ## 17.7 The Framework Must Remain Testable
   ## 17.8 Final Claim
```

---

# 4. DIAGRAM PLACEMENT NOTES (from PAPER_ARCHITECTURE.md)

| SVG | PAPER_ARCHITECTURE Placement | SVG_SPECIFICATIONS Placement | Current Paper Insertion Point |
|-----|-----------------------------|-----------------------------|------------------------------|
| 1. Fear vs Topography | Section 1 | Section 1 | After line ~29 (after marble/slope patch) |
| 2. Context vs Reasoning State | (not in original architecture — added later) | Section 3 | After line ~398 (after context/reasoning distinction) |
| 3. Box-First vs Topography-First | Section 1 or 6 | Section 1 or 6 | After line ~33 or Section 6 opening |
| 4. Core Framework Loop | Section 3/4 boundary | End of Section 3 or beginning of Section 4 | After line ~560 (Section 3→4 transition) |
| 5. Runtime Discovery Loop | Section 11 | Section 11 | After line ~2667 (Section 11 opening) |

**Note:** No SVGs have been generated yet. All sections are now stable enough for generation.

---

# 5. AHA INVENTORY — Post-Audit Status

| ID | Title | Status | In Paper? | Section(s) |
|----|-------|--------|-----------|------------|
| AHA_001 | Shaping the Landscape (ORIGIN SENTENCE) | **Promoted** | **Yes** — patched into S1 | 1 |
| AHA_002 | The Department, Not the Model | Promoted (seed) | Implicit | 1 |
| AHA_003 | Reward Hacking IS KPI Gaming | **Promoted** | **Yes** — patched into S6 | 6 |
| AHA_004 | What Reality Are We Allowing the Agent to Perceive? | Promoted (seed) | **Yes** — patched into S5 | 5 |
| AHA_005 | Stop Looking at the Marble. Look at the Slope. | **Promoted** | **Yes** — patched into S1 | 1 |
| AHA_006 | Governance Shapes Terrain | Promoted (seed) | Implicit | 4, 5, 6 |
| AHA_007 | Map, Sensor, Navigator | **Held** — SVG/speaker notes only | No | — |
| AHA_008 | Theory Ahead of Language | **Retired** from paper scope | No | — |
| AHA_009 | Visibility Is Not Attention | **Held** | No | — |
| AHA_010 | Retrieval Is Gradient Selection | **Promoted** | **Yes** — patched into S13.8 | 13 |
| AHA_011 | VP Is Human Analog | Candidate — implicit | Implicit (running example) | 3-12 |
| AHA_012 | Governance Is Visibility Design | Candidate — implicit | Implicit | 16 |
| AHA_013 | Framework Became Testable | **Promoted** | **Yes** — patched into S14 | 14 |
| AHA_014 | Retrieval as Context Construction | Candidate — implicit | Implicit | 3, 11 |
| AHA_015 | Context Layers Shape Interpretation | Candidate — implicit | Implicit | 3 |
| AHA_016 | Diagnostic Over Prescriptive | **Promoted** | **Yes** — patched into S14.12 | 14 |
| AHA_017 | Real-World Test Environment | **Retired** from paper scope | No | — |

**Principle applied:** AHA moments function as reframes, section bridges, or design principles — not slogans.

---

# 6. TERMINOLOGY RISKS AND OBSERVATIONS

## Term Frequency (top terms in draft)

| Term | Count | Risk Level |
|------|-------|------------|
| system | 258 | **Watch** — generic, may obscure whether we mean "the AI," "the workflow," or "the organization" |
| optimizer | 180 | OK — core term, well-defined in Section 2 |
| confidence | 155 | **Watch** — used both as topography dimension and as general-purpose word ("we are confident"). May confuse readers |
| model update | 149 | OK — but "model update" (76 as "Model Update Object") vs standalone "model update" (73 other uses) could blur |
| topography | 132 | OK |
| agent | 132 | **Watch** — used alongside "optimizer." Reader may be unsure when the paper means "AI agent" vs "optimizer in general" |
| sufficiency | 96 | OK — well-defined |
| discovery | 86 | OK — but used both as framework concept and general English word |
| investigation | 82 | OK |
| reasoning state / reasoning-state | 75+39=114 | **Minor** — hyphenation inconsistency (75 unhyphenated, 39 hyphenated). Should standardize. |
| prediction error | 57 | OK |
| gradient | 27 | **Watch** — may be lower than expected given its importance. Appears mostly in Sections 1, 6 |
| information surface | 6 | **Low but notable** — this term was central to the theory-building phase but appears rarely in the paper |

## Specific Risks

1. **"system" overload** — 258 occurrences. Sometimes means "the AI system," sometimes "the human-agent system," sometimes "the reasoning-state system," sometimes "the implementation." Consider whether a few high-ambiguity uses need qualification.

2. **"confidence" overload** — Used as a topography dimension (formal) and as an English word ("we are confident," "medium-high confidence"). The formal dimension should probably be capitalized ("Confidence") when used technically.

3. **"agent" vs "optimizer"** — The paper defines both in Section 2 but uses them somewhat interchangeably in later sections. Section 4 establishes optimizer as the analytic frame. Later sections sometimes drift back to "agent" when discussing AI systems specifically. This is probably fine but worth a consistency check.

4. **"reasoning state" vs "reasoning-state"** — 75 unhyphenated vs 39 hyphenated. Should standardize. Recommendation: use "reasoning state" (unhyphenated) as a noun phrase, "reasoning-state" (hyphenated) as a compound adjective before a noun (e.g., "reasoning-state system").

5. **"model update" ambiguity** — "model update" appears 149 times. 76 of those are "Model Update Object" (capitalized, specific). The remaining 73 are generic uses. May benefit from consistent capitalization when referring to the formal concept.

6. **"information surface" nearly absent** — Only 6 occurrences despite being central to the theory-building phase. This is actually correct — the paper uses "information topography" as the primary concept, with "information surface" appearing in Section 2 as a defined term. But worth noting: readers who encounter the repo may expect this term to be more prominent.

7. **"topology" appears once** — Line in Section 2 intro mentions "topology" among fields that use overlapping terms. Should verify it's not used where "topography" is intended.

8. **"action stability"** — 0 occurrences. This was the working definition of sufficiency during theory building. The paper defines sufficiency clearly but never uses this synonym. Not necessarily a problem, but worth noting for speaker notes or executive summaries.

---

## Repository Protocols
1. **#1 — Concept Architecture is sovereign.**
2. **#2 — Fault Lines preserve contradictions.**
3. **#3 — Classification-first.**
4. **#4 — Nothing becomes doctrine alone.**
5. **#5 — Optimize for framework failure, not confirmation.**

## Paper Guardrails (Phase 6)
**Allowed:** Clarify language, compress concepts, define terms, choose examples, add citations, design diagrams, write narrative sections, identify validation methods.
**NOT allowed without explicit approval:** New primitives, new topography dimensions, new optimizer phases, new foundational architecture documents, major theory expansion.

## Instruction to ChatGPT
Use this as the current project state. The paper v0.1 draft is complete with AHA patches applied. Concept architecture is frozen. This session is focused on the five revision audit areas listed above. When repository updates are needed, flag as **Repository Action Required** with classification and content. Do not introduce new theory or new framework components.

---

*This file is regenerated by Claude before each session. Last generated: 2026-06-12.*
