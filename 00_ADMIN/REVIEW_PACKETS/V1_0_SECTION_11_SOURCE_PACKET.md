# v1.0 Section 11 Source Packet

## Build Better Landscapes

---

## Source Files Reviewed

| Source | File | Relevant sections | Line ranges |
| --- | --- | --- | --- |
| v0.2 Implications | PAPER_v0.2.md | S16: What Changes When Reasoning Is Preserved | Lines 3370–3517 |
| v0.2 Conclusion | PAPER_v0.2.md | S17: Build Better Landscapes | Lines 3518–3673 |
| v0.1 Conclusion | PAPER_v0.1.md | S17: Conclusion: Build Better Landscapes | Lines ~3518–3673 |
| v1.0 Section 1 opening | PAPER_v1.0_WORKING.md | S1 fear framing + thesis | Lines 40–108 |
| v1.0 Section 10 ending | PAPER_v1.0_WORKING.md | S10 closing | Lines 2219–2223 |
| v1.0 Section 11 placeholder | PAPER_v1.0_WORKING.md | S11 arc comment | Lines 2227–2234 |
| Macro narrative audit | V1_0_SECTIONS_01_10_MACRO_NARRATIVE_PURPOSE_AUDIT.md | S11 readiness | Full |
| Parallax framing review | V1_0_SECTION_11_PARALLAX_FRAMING_REVIEW.md | Mechanism-payoff approval | Full |
| Figure 8 asset note | V1_0_FIGURE_08_CAPSTONE_ASSET_NOTE.md | Capstone registration | Full |
| Rewrite doctrine | V1_0_REWRITE_DOCTRINE_AND_WORKPLAN.md | S11 arc, output tracks | Lines 195–214, 679 |
| S10 integrity check | V1_0_SECTION_10_POST_INSERTION_INTEGRITY_CHECK.md | S10→S11 handoff | Full |
| Concept architecture | CURRENT_STATE.md | All phases | Full |
| Narrative architecture | NB_001_From_Fear_of_Agents_to_Governance_of_Perceived_Topography.md | Fear→governance reframe | Lines 204–208 |
| AHA_006 | AHA_006_Governance_Shapes_Terrain.md | Governance as landscape design | Title/concept |

---

## Section 11 Narrative Job

Section 11 is the paper's close. Its job is the mechanism payoff.

It answers: **What does a better landscape actually look like?**

Not as a production HLD. Not as a product spec. Not as a new architecture. But as a conceptual reference mechanism that lets the reader connect the framework's labels to functional parts of a running human-agent system.

The intended reader reaction:

> The framework was never just a metaphor. It shows where to intervene in the system.

Section 11 does three things:

1. **Show the operating shape.** Map the framework's labels to functional parts of a conceptual reference mechanism. Present Figure 8 as the capstone visual.
2. **Run the familiar example through it.** The healthcare campaign, one last time, through the mechanism rather than the theory.
3. **Close with the imperative.** The landscapes are already being shaped; build better ones.

---

## Controlling Parallax Decision

The parallax framing review (V1_0_SECTION_11_PARALLAX_FRAMING_REVIEW.md) approved:

> **YES WITH GUARDRAILS — mechanism-payoff framing is the right close.**

Guardrails:

1. Do not repeat Section 8's parts list.
2. Stay at reference-mechanism level, not implementation.
3. Keep to 900–1,300 words.
4. Frame functional-part names as reference names, not new canonical vocabulary.
5. Ensure the closing imperative still lands as the final move.
6. Do not use a formal table for the mechanism mapping — use inline prose or compact list.

The distinction from Section 8:

- **Section 8:** These capabilities must exist. (The parts list.)
- **Section 11:** Here is how the parts fit together when the system runs. (The operating shape.)

---

## Figure 8 Capstone Decision

**Asset:** `paper_assets/png/fig8_perceived_topography_workshop_console.png`

**Displayed figure number:** Figure 8 (follows Figure 7 in Section 8)

**Candidate title:** Figure 8. The Perceived Topography Framework as a workshop control console.

**Candidate caption:** A reference mechanism for building better perceived landscapes. Fear of agent behavior enters as the design pressure; the working frame, perceived topography, gradient-guided motion, and learning loop show how a system can shape what becomes visible, trusted, sufficient, and learnable before future action.

**What the figure shows:**

- Input: Fear of AI Agents (design pressure)
- Panel 2: Working Frame (Goal, Policy, Interpretation)
- Panel 3: Perceived Topography (Visibility, Accessibility, Representation, Confidence, Connectivity)
- Panel 4: Motion: Guided by Gradients (Attraction, Investigation, Sufficiency, Action)
- Panel 5: Learning Loop (Outcome → Prediction Error → Explanation → Model Update Object → Future Reasoning)
- Output: Build Better Landscapes

**Placement:** After the mechanism walkthrough prose, before the closing imperative. The reader should see the mechanism described in words, then see it assembled in the figure, then hear the closing.

**What Figure 8 is NOT:** A software architecture, vendor platform, implementation stack, database/API/service diagram, or production HLD. It is a conceptual operating-shape diagram, a capstone synthesis figure, a metaphorical mechanism showing where the framework's concepts live when assembled.

**Discovery note:** Discovery is not explicitly labeled as a console panel in the figure. The prose should note that Discovery operates at the interface between incoming requests and the working frame — it is how messy intent enters the mechanism and becomes structured reasoning.

---

## Loop-Engineering Contrast

A user-provided external prompt-engineering graphic contrasted:

- **Normal prompting:** You ask AI something → AI gives an answer → It stops. You do the rest.
- **Loop engineering:** You give AI a task + goal → AI works, checks, fixes, and tries again → It stops when the goal is hit. Goal = the stop signal.

This contrast is useful but incomplete from the Perceived Topography perspective.

**The three-level contrast for Section 11:**

| Level | What happens | What is missing |
| --- | --- | --- |
| Normal prompting | Answer generation. One pass. | No loop, no landscape, no learning. |
| Loop engineering | Goal-seeking with retries. Agent loops until goal is met. | The loop has no shaped landscape. Goal as stop signal is too simple — it does not account for what the loop can see, trust, investigate, or learn from. |
| Perceived topography design | Shaped motion through visible, trusted, governed, learnable landscapes. | — (This is the framework's contribution.) |

**Core insight:**

> The problem is not only whether the agent loops. The problem is what landscape the loop moves through, what counts as sufficient, and whether the system learns from what happens next.

**Candidate protected formulation:**

> Better systems are not only prompted differently. They are looped differently, stopped differently, and taught differently.

**Treatment:** Use as a conceptual contrast in Movement 1 (design target). Not as a cited source — treat as user-provided conceptual inspiration unless a citable source is later supplied. The contrast should open Section 11 by showing that the framework offers something beyond both single-pass prompting and simple goal-seeking loops.

**Guardrail:** Do not let the loop-engineering contrast dominate. It is the setup for the mechanism payoff, not the payoff itself. ~50–80 words maximum.

---

## Handoff from Section 10

Section 10 ends:

> "The framework is a bridge among its influences, not a replacement for them. It takes the limits of bounded rationality, the constructed meaning of sensemaking, the action-shaping logic of affordances, the memory problem of organizational learning, the retrieval problem of AI systems, and the governance problem of agentic behavior, and arranges them around a practical design question:"
>
> "What landscape is this system acting from, and how can that landscape be made more visible, learnable, governable, and correctable?"
>
> "With the roots named, the practical question becomes harder to avoid. Human-agent systems will shape perceived landscapes either way. The remaining choice is whether builders shape those landscapes accidentally or deliberately."

Section 11 takes this handoff by answering: what does deliberate landscape design look like as a functioning mechanism?

Do not replay the lineage argument. Do not reopen objections. Begin from the design target.

---

## Historical Reconstruction

### v0.1 Source Material

**Section 17: "Conclusion: Build Better Landscapes"** (~1,500 words, 8 subsections)

Narrative job: Close the paper. Recap key claims, assign design responsibility, insist on testability, reframe the central question.

Key closing lines:
- "Agents are not evil. They are optimizers moving through landscapes."
- "If the path is dangerous, we should not only blame the motion. We should examine the terrain."
- "And if we want better motion, we must build better landscapes."

### v0.2 Source Material

**Section 16: "What Changes When Reasoning Is Preserved"** (~1,500 words, 14 subsections)

Narrative job: Name implications across domains.

Key formulation:
- "The highest-value human-agent systems will not merely do work. They will improve the conditions under which future work is done."

**Section 17: "Build Better Landscapes"** (~1,500 words, 8 subsections)

Same closing as v0.1 with refined titles. Same final lines.

### Prior Conclusion Material to Preserve

1. "Build better landscapes." — Title and final imperative.
2. "Agents are not evil. They are optimizers moving through landscapes." — Callback to S1.
3. "If the path is dangerous, we should not only blame the motion. We should examine the terrain." — Core reframe.
4. Design responsibility: builders shape landscapes whether they intend to or not.
5. The reframed question: "How do we build environments in which capable agents and humans can reason, act, and learn together?"
6. "The highest-value human-agent systems will not merely do work. They will improve the conditions under which future work is done."

### Prior Conclusion Material to Avoid

1. v0.2 S17.1–S17.5: Claim-by-claim recap of context, failure, learning, Discovery, domain shifts — **avoid entirely.** Section 11 should not summarize.
2. v0.2 S16.1–S16.13: 14 separate implication subsections — **avoid.** The mechanism payoff replaces the implication catalog.
3. v0.2 S17.7: Testability insistence — **already handled in S9.**
4. Failure formula (S17.2): "Goal pressure + weak grounding + misplaced confidence..." — **already handled in S4.**

---

## What Sections 1–10 Have Earned

By the end of Section 10, the reader holds:

| Concept | Where established |
| --- | --- |
| Fear → landscape design reframe | S1 |
| Context ≠ reasoning state | S2 |
| Optimizer state (Goal, Policy, Interpretation) | S3 |
| Five topography dimensions | S3 |
| Gradients, attention, investigation, sufficiency | S4 |
| Premature sufficiency as shared failure | S4 |
| Healthcare campaign (full stress test) | S5 |
| Learning requires preserved reasoning | S6 |
| Model Update Objects | S6 |
| Discovery (Retrieve → Infer → Propose → Confirm) | S7 |
| Reusable reasoning surfaces | S7 |
| Six reasoning objects (chain) | S8 |
| Context layer vs. reasoning-state layer | S8 |
| Maturity model | S8 |
| Falsifiability and disconfirmation conditions | S9 |
| Misuse risks | S9 |
| Intellectual lineage | S10 |

The paper has earned its close. Section 11 should use this vocabulary, not re-teach it.

---

## What the Parallax Review Changed

The macro audit (pre-parallax) recommended:

- 500–800 words
- 2–4 implications
- No mechanism
- Short builder's imperative

The parallax review changed this to:

- 900–1,300 words
- Mechanism payoff instead of implications
- Operating shape showing where labels attach
- Healthcare campaign through the mechanism
- Figure 8 as capstone

The parallax review determined that implications-only was adequate but not the strongest close. The mechanism payoff completes the design arc.

---

## What Figure 8 Changes

Without Figure 8, the mechanism payoff would be prose-only — a list of functional parts that the reader must imagine.

With Figure 8, the reader sees the assembled machine. Every label from Sections 1–10 has a visible position. The figure is the practical punchline: the framework was always about where to intervene.

Figure 8 makes the mechanism payoff visual and immediate rather than abstract and sequential.

---

## What the Loop-Engineering Contrast Adds

The loop-engineering contrast gives Section 11 a sharper opening move. Instead of jumping directly to the mechanism, the section can first show why the mechanism matters by contrasting three levels:

1. **Single-pass prompting** — no loop, no landscape.
2. **Loop engineering** — goal-seeking, but the loop has no shaped environment. Sufficiency is just "goal = stop."
3. **Perceived topography design** — the loop moves through a shaped landscape where visibility, confidence, policy, evidence, and learning determine what becomes sufficient.

This positions the framework as going beyond both prompting and agentic looping — it shapes the environment the loop acts from.

---

## Core Claim of Section 11

> A better human-agent system is not just a prompt or a loop. It is an operating environment that shapes what the system can see, trust, investigate, stop on, preserve, and learn from.

The framework was never just a metaphor. It shows where to intervene in the machine.

---

## Mechanism-Payoff Target

The reader should finish Section 11 able to point at each part of a human-agent system and say:

- "That is where information surfaces enter."
- "That is where Discovery happens."
- "That is where the topography is constructed."
- "That is where gradients create motion."
- "That is where sufficiency is judged."
- "That is where reasoning is preserved."
- "That is where learning changes the next landscape."

Then they should hear: "Build better landscapes."

---

## Functional Mapping

Framework labels map to functional parts of the reference mechanism:

| Framework label | Functional responsibility |
| --- | --- |
| Fear of AI Agents | Design pressure entering the system — the reason the mechanism exists |
| Working Frame | Holds the active Goal, Policy, and Interpretation that shape how the system moves |
| Perceived Topography | Assembles what is visible, accessible, represented, trusted, and connected for the current decision |
| Gradients | Makes some paths attractive, some risky, some requiring investigation, and some requiring escalation |
| Sufficiency | Decides whether the current state is enough to act, or whether the system should investigate, ask, escalate, or abstain |
| Action | Commitment into the world — the moment the system moves |
| Learning Loop | Converts outcomes and prediction errors into reusable changes that reshape future topography |
| Build Better Landscapes | The output/purpose — not a numbered step but the reason the mechanism exists |

**Discovery note:** Discovery operates at the interface between incoming requests and the working frame. It is how messy intent enters the mechanism and becomes structured reasoning. The figure's input side implicitly includes Discovery.

**Drafting guidance:** Present this mapping in inline prose with bold terms, not as a formal Table 11. Use language like: "A system shaped by the framework would need functions like these. The names matter less than the responsibilities."

---

## Figure 8 Placement and Caption Guidance

**Placement:** After the mechanism walkthrough prose (Movement 2/3), before the closing imperative (Movement 4). The reader should:

1. Read the three-level contrast (prompting → loops → landscapes)
2. Read the mechanism mapping in prose
3. See Figure 8 as the visual crystallization
4. Hear the closing imperative

**Caption guidance:** The caption should explain the figure's argumentative job. Candidate:

> Figure 8. The Perceived Topography Framework as a workshop control console. A reference mechanism for building better perceived landscapes. Fear of agent behavior enters as the design pressure; the working frame, perceived topography, gradient-guided motion, and learning loop show how a system can shape what becomes visible, trusted, sufficient, and learnable before future action.

The caption may be refined during drafting to match surrounding prose tone.

---

## Healthcare Campaign Through the Mechanism

### Weak landscape (~100 words)

A marketer asks for a cardiology campaign brief. The system retrieves product docs, prior campaign copy, and audience profiles. It generates a plausible brief. It stores the output. The reasoning behind the brief — why the audience was chosen, what evidence was trusted, what claims were bounded, what would make the result sufficient — is not preserved.

### Better landscape (~150 words)

The request enters a system shaped by the framework. The **working frame** clarifies the goal (qualified demo generation, not generic awareness), the policy (no unsupported clinical claims), and the interpretation (workflow burden as attention hook, not buying signal). The **perceived topography** makes approved claims visible, stale assumptions weaker, risky language harder to use, and missing evidence easier to notice. **Gradient-guided motion** pulls the system through attraction, investigation, and sufficiency in a more disciplined sequence — workflow burden attracts attention, but buying-stage readiness requires investigation before the campaign becomes sufficient. The **learning loop** captures what happened, what surprised the system, why it happened, what should change, and how future reasoning should be shaped differently.

**Drafting note:** Keep the contrast vivid but compact. The point is not marketing — it is showing framework labels attaching to a functioning mechanism.

---

## Concepts to Recall Without Re-Explaining

Section 11 should reference these concepts by name without re-teaching them:

- Perceived topography
- Optimizer state / working frame
- Gradients
- Sufficiency / premature sufficiency
- Discovery
- Model Update Objects
- Six reasoning objects
- Reusable reasoning surfaces
- Information surfaces
- Context vs. reasoning state
- Learning as model change

The reader holds all of these from Sections 1–10.

---

## Concepts and Moves to Avoid

Section 11 must NOT:

- Summarize each of Sections 1–10
- Re-introduce the six objects, maturity model, or lifecycle (Section 8's job)
- Reopen objections or falsifiability (Section 9's job)
- Replay the lineage table (Section 10's job)
- Re-derive the healthcare campaign (Section 5's job)
- Introduce new canonical vocabulary
- Let Figure 8 become a product architecture interpretation
- Treat "goal = stop signal" as sufficient — deepen into sufficiency
- Claim the framework solves safety, governance, learning, or alignment
- Imply deliberate landscape design guarantees good outcomes
- Add citation burden unless required for a specific external claim
- Become a product roadmap, governance checklist, or implementation plan

---

## Candidate Section Movement

### Recommended narrative arc (~900–1,300 words)

**Movement 1: The design target / three-level contrast (~150–200 words)**

Open from Section 10's handoff. The practical answer is not merely more context. It is also not merely a task loop where the goal is the stop signal.

Use the three-level contrast:
- Normal prompting: single-pass answer generation.
- Loop engineering: goal-seeking with retries. Better, but the loop has no shaped landscape.
- Perceived topography design: shaped motion through visible, trusted, governed, learnable landscapes.

Core insight: "The problem is not only whether the agent loops. The problem is what landscape the loop moves through, what counts as sufficient, and whether the system learns from what happens next."

Candidate formulation: "Better systems are not only prompted differently. They are looped differently, stopped differently, and taught differently."

**Movement 2: Figure 8 + mechanism walkthrough (~300–400 words)**

Introduce Figure 8 as a reference mechanism, not a product architecture.

Walk through the console at a functional level:
- Fear enters as design pressure
- Working frame clarifies goal, policy, interpretation
- Perceived topography shapes what stands out
- Motion guided by gradients leads through attraction, investigation, sufficiency, and action
- Learning loop feeds future reasoning
- Output: build better landscapes

Note that Discovery operates at the interface between incoming requests and the working frame.

Present Figure 8 here.

**Movement 3: The campaign through the machine (~200–300 words)**

Weak landscape: retrieve, generate, store.

Better landscape: working frame clarifies, topography shapes what stands out, gradients discipline motion, sufficiency is judged before action, reasoning is preserved, learning changes the next landscape.

The contrast shows what "better landscape" means functionally.

**Movement 4: The close (~150–200 words)**

Better does not mean perfect. Better means more visible, contestable, learnable, governable, and correctable.

Return to Section 1's image: agents moving through landscapes. A model does not need inner malice to cause harm. It only needs a path through the environment that makes the harmful action appear useful, available, or sufficient.

The framework's answer was never just a vocabulary. It was always about where to intervene.

Callback: "Agents are not evil. They are optimizers moving through landscapes. If the path is dangerous, we should not only blame the motion. We should examine the terrain."

Final imperative: "Build better landscapes."

---

## Visual and Table Plan

**Figure 8:** Use the registered capstone figure (`paper_assets/png/fig8_perceived_topography_workshop_console.png`). Display as Figure 8. Place after mechanism walkthrough, before closing imperative.

**No formal Table 11.** The manuscript already has Tables 1–10. The mechanism mapping should be handled in prose around Figure 8. A new formal table would make the close feel like another artifact instead of a final landing.

**No additional figure.** Figure 8 is sufficient.

---

## Citation Guidance

Section 11 should require few or no new citations. It synthesizes the argument already built. Every tradition has been cited in Sections 1–4 or in Section 10's lineage table.

The loop-engineering contrast is user-provided conceptual inspiration, not cited scholarship. Do not cite it unless a citable source is later supplied.

Do not add citation burden to the closing section.

---

## Relationship to Figures 1–7

- Figures 1–7 remain teaching/analytic figures.
- Figure 8 becomes the capstone/synthesis figure.
- Do not restructure Figures 1–7.
- Later harmonization should be mild only: consistent title treatment, caption style, muted palette, line weight, label hierarchy.
- Section 8 SVG (`fig6_reasoning_architecture_six_objects.svg`) may still need mechanical `<title>` cleanup from "Figure 6" to "Figure 7." Known visual-pass task.

---

## Boundary Conditions

Section 11 must NOT:

- Summarize Sections 1–10
- Repeat Section 8's parts list (six objects, maturity model, lifecycle)
- Reopen Section 9's objections or falsifiability
- Replay Section 10's lineage
- Become an implementation section, product roadmap, or governance checklist
- Introduce new claims requiring citations
- Become motivational fluff
- Let Figure 8 become a product architecture interpretation
- Overclaim that the framework solves safety, governance, learning, or alignment
- Treat "goal = stop signal" as the complete sufficiency story

---

## Tone Guidance

The tone should be:

- Clear
- Earned
- Practical
- Responsible
- Slightly elevated
- Not grandiose
- Not apologetic
- Not hype
- Not academic sludge
- Not product pitch

It should close with confidence grounded in responsibility and testability. The paper earned this confidence through Section 9's rigor gate and Section 10's lineage.

---

## Candidate Final Move

**Final sentence:** "Build better landscapes."

This should land as an earned imperative, not a slogan. It lands because the reader has just seen what a better landscape looks like inside a running system. The preceding ~1,000 words showed the mechanism, ran the example through it, and returned to the opening image of agents moving through shaped environments.

**Preceding context for the final sentence:**

The closing should echo Section 1's opening:

> S1 (line 44): "A model does not need inner malice to cause harm. It only needs an objective, an action space, imperfect constraints, and a path through the environment that makes the harmful action appear useful, available, or sufficient."

The close inverts this: the framework shows how to make the grounded, policy-aware, learnable path the easiest sufficient one.

Then:

> "Agents are not evil. They are optimizers moving through landscapes."
>
> "If the path is dangerous, we should not only blame the motion. We should examine the terrain."
>
> "Build better landscapes."

---

## Drafting Risks

| Risk | Mitigation |
| --- | --- |
| Figure 8 overwhelms the prose | Describe the mechanism in words first; Figure 8 crystallizes, not replaces |
| Mechanism becomes HLD | Stay at functional-label level; if a sentence could appear in a design document, cut it |
| Mechanism repeats Section 8 | S8 = parts list; S11 = operating shape. Do not re-introduce capabilities |
| Section too long | Target 900–1,300 words; if exceeding 1,300, it becomes a new architecture section |
| Loop-engineering contrast becomes tangent | Limit to ~50–80 words; it is the setup, not the payoff |
| "Goal = stop signal" accepted too simply | Deepen into sufficiency: what counts as sufficient depends on the landscape, not just the goal |
| Functional-part names sound like new doctrine | Frame as "one practical shape" and "the names matter less than the responsibilities" |
| Healthcare example becomes a second case study | Keep to ~250 words total; it runs through the mechanism, not through the theory |
| Final imperative gets crowded | Allocate last ~150 words exclusively to the close |
| Section feels too inspirational | Ground in the mechanism and the campaign; the payoff is practical, not motivational |
| Section feels too technical | The mechanism walkthrough is functional, not engineering; the close returns to the human stakes |
| "Build better landscapes" lands as slogan | It should land only after the reader has seen what "better" means functionally |

---

## Specific Questions Answered

1. **What is the central job of Section 11?** Show the operating shape (mechanism payoff), run the campaign through it, and close with the builder's imperative.

2. **What exact problem does Section 10 hand off?** "The remaining choice is whether builders shape those landscapes accidentally or deliberately."

3. **What did the parallax review change?** Replaced implications-only close with mechanism-payoff framing. Extended from 500–800 words to 900–1,300.

4. **What does Figure 8 change?** Makes the mechanism payoff visual and immediate. The reader sees where every label lives.

5. **What does the loop-engineering contrast add?** A sharper opening that positions the framework beyond both prompting and simple goal-seeking loops.

6. **What has the paper earned?** All framework concepts, the stress test, learning, Discovery, architecture, falsifiability, lineage. The reader holds everything needed to see the mechanism.

7. **What should Section 11 recall?** All major concepts by name. The healthcare campaign. The S1 fear framing.

8. **What should it avoid re-explaining?** Six objects, maturity model, lifecycle, Discovery loop, topography dimensions, disconfirmation conditions, lineage table.

9. **What functional mapping?** See Functional Mapping section above.

10. **Where should Figure 8 be placed?** After mechanism walkthrough, before closing imperative.

11. **What caption guidance?** Working candidate provided; refine during drafting.

12. **How should the campaign run through the mechanism?** Weak landscape (retrieve, generate, store) vs. better landscape (working frame, topography, gradients, sufficiency, learning loop). ~250 words total.

13. **Should Section 11 include a formal table?** No.

14. **Should Section 11 include an additional figure?** No. Figure 8 is sufficient.

15. **Should Section 11 add citations?** No, unless introducing an external factual claim.

16. **What should the final move be?** "Build better landscapes." — earned imperative after the mechanism payoff.

17. **What would make Section 11 too weak?** Implications-only. Summary. No mechanism. No figure.

18. **What would make Section 11 overclaim?** Claiming the framework solves safety/governance/learning. Claiming the mechanism is the only possible design. Treating Figure 8 as a product architecture.

19. **What would make the reader put the paper down and feel they have found something valuable?** Seeing every label from Sections 1–10 assemble into a functioning design target. Realizing the framework was always about where to intervene. Hearing "Build better landscapes" after knowing what that means.

---

## Drafting Guidance

- Do not summarize Sections 1–10.
- Do not re-introduce capabilities from Section 8.
- Do not reopen objections from Section 9.
- Do not replay lineage from Section 10.
- Do not introduce new canonical vocabulary.
- Use the three-level contrast (prompting → loops → landscapes) as a compact opening, not a long argument.
- Show the mechanism mapping in prose with bold terms, not as a formal table.
- Place Figure 8 after the mechanism walkthrough, before the closing.
- Run the healthcare campaign through the mechanism compactly (~250 words).
- Return to Section 1's opening image for the close.
- Echo the v0.2 closing: "Agents are not evil. They are optimizers moving through landscapes."
- End with: "Build better landscapes."
- Avoid manuscript self-reference.
- Keep to 900–1,300 words.
- The section should feel like a builder's imperative grounded in a visible design target, not a scholar's summary or a motivational poster.

### Recommended Section Length

~900–1,300 words.

v0.2 S16+S17 were ~3,000 words across 22 subsections. v1.0 S11 replaces implication catalog and recap with mechanism payoff and Figure 8. Much shorter because:
- No implication-by-implication walk (v0.2 S16.1–S16.13 eliminated)
- No claim-by-claim recap (v0.2 S17.1–S17.5 eliminated)
- The mechanism payoff and Figure 8 do the work that 22 subsections tried to do
- The three-level contrast replaces abstract motivation

Reader comprehension and closing energy govern.

---

## Resolved Authorial Decisions

All decisions resolved on 2026-06-19:

1. **Framing:** ~~RESOLVED.~~ Mechanism-payoff framing approved (parallax review: YES WITH GUARDRAILS).

2. **Figure 8:** ~~RESOLVED.~~ Capstone synthesis figure registered. Display as Figure 8. Asset at `paper_assets/png/fig8_perceived_topography_workshop_console.png`. Place after mechanism walkthrough, before closing.

3. **Formal table:** ~~RESOLVED.~~ No Table 11. Inline bold-term prose for mechanism mapping. Figure 8 carries the visual.

4. **Healthcare campaign:** ~~RESOLVED.~~ Reuse through the mechanism (weak landscape vs. better landscape).

5. **Length:** ~~RESOLVED.~~ 900–1,300 words.

6. **Section 8 guardrail:** ~~RESOLVED.~~ S8 = parts list. S11 = operating shape.

7. **Discovery in Figure 8:** ~~RESOLVED.~~ Not explicitly labeled as a panel. Prose notes Discovery operates at the interface between incoming requests and the working frame.

8. **Loop-engineering contrast:** ~~RESOLVED.~~ Three-level contrast (prompting → loops → landscapes) as compact opening setup (~50–80 words). Not a cited source. Deepens sufficiency beyond "goal = stop signal."

9. **Final sentence:** ~~RESOLVED.~~ "Build better landscapes." — earned imperative, not slogan.

---

## Verification Notes

- Section 11 placeholder in manuscript: `NOT YET DRAFTED` (line 2233)
- Section 11 arc comment preserved (lines 2230–2232)
- Figure 8 asset verified at `paper_assets/png/fig8_perceived_topography_workshop_console.png`
- Rewrite queue status for Section 11: `Source packet ready`
- No v1.0 manuscript edits made
- No existing source/review packets edited
- No figures or SVGs edited
- SESSION_START.md not edited
