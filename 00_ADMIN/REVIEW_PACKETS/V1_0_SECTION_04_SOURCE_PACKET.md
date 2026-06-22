# Section 4 Source Packet: Gradients, Sufficiency, and Failure

---

## Purpose of Section 4

Section 4 is where the framework becomes dynamic. Sections 1-3 established the problem (fear vs. landscape), the gap (context vs. reasoning state), and the structural components (optimizer state + topography). Section 4 explains how behavior actually emerges from the interaction of those components.

Section 3 ended with: "But landscape alone does not explain movement. The next section describes how behavior emerges from the interaction between optimizer state and topography: through gradients, sufficiency, and failure."

Section 4 must deliver on that bridge. It introduces gradients as directional pressures, the motion sequence (Attraction -> Investigation -> Sufficiency -> Action), the critical sufficiency-vs-certainty distinction, and the paper's most original contribution: premature sufficiency as a shared failure pattern for both hallucination and harmful action.

This section merges v0.2 Section 6 (Behavior Follows Gradients) and v0.2 Section 7 (Failure Happens When Sufficiency Comes Too Soon). The merge must maintain the logical flow: gradients create motion -> sufficiency stops motion -> premature sufficiency = failure.

After reading Section 4, the reader should be able to say: "Behavior follows gradients in the perceived topography. The system acts when it reaches sufficiency. When sufficiency comes too soon — before evidence, policy, or investigation warrant it — the result is premature sufficiency. Both hallucination and harmful action can share this pattern, even though they differ in stakes."

---

## Required Arc Moves

Section 4 must accomplish these arc moves in order:

1. Transition from landscape (S3) to motion: behavior emerges from optimizer state moving through perceived gradients.
2. Define gradient as a directional pressure within the perceived topography. Not a formal mathematical gradient; a design term. [Ng et al., 1999]
3. Introduce the motion sequence: Attraction -> Investigation -> Sufficiency -> Action. Not a rigid linear process; a diagnostic model.
4. Attraction: action attraction (toward doing) vs. exploration attraction (toward investigating). Confidence governs which direction.
5. Investigation: goal-directed uncertainty reduction. Bounded by materiality. [Simon, 1955] [Pirolli & Card, 1999]
6. Sufficiency: the stopping condition. When additional information is unlikely to materially change the selected action.
7. **Sufficiency is not certainty.** The 2x2: low-confidence/high-sufficiency vs. high-confidence/low-sufficiency. This is one of the paper's most praised distinctions.
8. Action: the selected behavior. Action includes asking, escalating, refusing, or pausing — not just completing the task.
9. Figure 4 placement.
10. Premature sufficiency: the system reaches action before evidence, policy, or investigation warrant it.
11. Hallucination as premature sufficiency: plausible completion treated as sufficient despite insufficient evidence.
12. Harmful action as premature sufficiency: risky path treated as sufficient despite unresolved policy, confidence, or consequence gaps.
13. The shared motion pattern: goal pressure + weak grounding + misplaced confidence + low-friction path = premature sufficiency. Different outputs, same structural shape.
14. Premature sufficiency comparison table (new visual).
15. Case A: "reduces readmissions" compliance example — the paper's most concrete, realistic scenario.
16. Case B: unsafe tool action (operations agent restart example).
17. "I don't know" and "I should not act yet" as essential action affordances, not friction.
18. Clarification: hallucination and harmful action are NOT morally equivalent. They share structure, not severity.
19. Bridge to Section 5: the constructed stress test will show the full framework in action through the healthcare campaign.

---

## Source Material from v0.2

### From v0.2 Section 6 (lines 938-1213): Behavior Follows Gradients

**Gradient defined (lines 968-976):**
> A gradient is a directional pressure within the perceived topography. A gradient makes some paths appear easier, more useful, more relevant, more confident, lower-cost, more available, or more sufficient than others.
> The term is not used here as a formal mathematical gradient unless explicitly stated. [Ng et al., 1999] [Gibson, 1979] [Norman, 1988]

**Motion sequence (lines 952-960):**
> Attraction -> Investigation -> Sufficiency -> Action
> This sequence is not meant to imply that every agent follows a clean linear process. Real workflows may loop, branch, skip steps, or run multiple investigations in parallel. But the sequence gives us a useful diagnostic model.

**Attraction (lines 990-1021):**
> Attraction is the allocation of optimizer attention toward part of the perceived topography.
> Two kinds: Action Attraction (toward doing) and Exploration Attraction (toward looking).
> Confidence governs which kind. High confidence may attract action. Low confidence may attract investigation.

**Investigation (lines 1024-1047):**
> Investigation is the process of reducing uncertainty before action.
> Goal-directed uncertainty reduction, not generic curiosity.
> Bounded by materiality: investigate only when the answer could materially change the action.
> [Simon, 1955] [Pirolli & Card, 1999] [Howard, 1966] [Russell & Wefald, 1991]

**Sufficiency (lines 1072-1101):**
> Sufficiency is the point at which additional information is unlikely to materially change the selected action.
> **Sufficiency is not certainty.** This is one of the most important distinctions in the framework.
> Confidence asks: How much do we trust this? Sufficiency asks: Is this enough to act?
> **Low Confidence, High Sufficiency:** Uncertain explanation, but all paths point to the same action (pause and investigate).
> **High Confidence, Low Sufficiency:** Trusted fact, but insufficient for the decision (engagement confirmed but buyer quality unknown).

**Action (lines 1104-1123):**
> Action is the selected behavior produced by optimizer motion.
> Action is not always "doing the requested task." Sometimes the correct action is to pause, ask, escalate, refuse, or produce a bounded draft.
> Campaign example: "I can draft a campaign around patient monitoring, but 'reducing readmissions' is a clinical outcome claim. I need approved evidence..."

**Safety failures follow motion (lines 1150-1178):**
> Three diagnostic patterns:
> - Hallucination Stops Too Early
> - Unsafe Tool Use Moves Too Easily
> - Circumvention Finds an Easier Path
> Each with motion pattern, topographic diagnosis, and design intervention.

**Campaign shows motion in practice (lines 1126-1147):**
> Full motion walkthrough: attraction, investigation (buying-stage question), sufficiency, action (campaign package + preserved reasoning state).

### From v0.2 Section 7 (lines 1214-1441): Failure Happens When Sufficiency Comes Too Soon

**Premature sufficiency introduced (lines 1216-1231):**
> Hallucination and harmful action are not the same failure. But at the level of reasoning state, they often share a common structure: both can occur when a system moves from insufficiently grounded perception to premature sufficiency.

**Hallucination as premature sufficiency (lines 1234-1251):**
> Hallucination is a motion failure. Plausible completion becomes easier than grounded uncertainty.
> Motion pattern: Attraction -> Investigation (skipped) -> Sufficiency (plausible completion treated as enough) -> Action (unsupported content).

**Harmful action as premature sufficiency (lines 1254-1273):**
> What made the harmful action appear attractive, available, permissible, or sufficient?
> Motion pattern: Attraction -> Investigation (policy/consequence checks weak) -> Sufficiency (action appears safe/routine enough) -> Action (unsafe step).

**Shared failure grammar (lines 1276-1293):**
> Goal pressure + weak grounding or weak constraint + misplaced confidence + insufficient investigation + low-friction action path = premature sufficiency.
> The output differs. The structure rhymes.

**Figure 4 placement (line 1296):**
> ![Motion and Premature Sufficiency](paper_assets/svg/fig4_motion_and_premature_sufficiency.svg)

**More context does not fix a bad path (lines 1302-1319):**
> A retrieved source does not guarantee grounded action. A written policy does not guarantee constrained behavior.
> Source and policy must become part of the perceived topography and exert behavioral force.

**Case A: Unsupported claim / "reduces readmissions" (lines 1326-1344):**
> A healthcare marketing agent is asked to write copy saying the RPM platform "reduces readmissions."
> Weak response: generates the claim. Better response: "I can draft this, but 'reduces readmissions' is a clinical outcome claim. I need approved evidence..."
> This is not less capable behavior. It is better-shaped behavior.

**Case B: Unsafe tool action (lines 1346-1362):**
> Operations agent asked to fix a slow service. Weak response: restarts automatically. Better response: connects to prior incident pattern, recommends checking before restarting.

**"I don't know" and "I should not act yet" (lines 1366-1383):**
> These are not friction. They are essential motion options.
> A system that cannot say "I don't know" is pushed toward hallucination. A system that cannot say "I should not act yet" is pushed toward unsafe autonomy.

**Same shape, different stakes (lines 1386-1405):**
> Hallucination and harmful action should not be collapsed into one undifferentiated category. The claim is narrower: they can share a reasoning-state structure: premature sufficiency under poorly shaped topography.

**Bridge to learning (lines 1424-1437):**
> Outcome is not learning. Correction is not learning. Postmortem is not learning. Learning occurs when prediction error is investigated, explained with evidence, and converted into a bounded model update.

---

## Existing SVG Placement

- **fig4_motion_and_premature_sufficiency.svg** — Place after the motion sequence and premature sufficiency concept have been established, near or between the hallucination/harmful-action comparison. In v0.2 this appears at line 1296, between S7.3 (shared failure grammar) and S7.4 (more context does not fix a bad path). In v1.0, place it after the reader understands both the motion model and the premature-sufficiency pattern.

---

## New Visual Candidate

### Premature Sufficiency Comparison Table

**Purpose:** Show hallucination and harmful action sharing a motion structure, side by side, making the parallel visible at a glance. This replaces or compresses the repeated structural exposition in v0.2 S7.1-S7.3.

**Proposed structure:**

| | Hallucination | Harmful action |
| --- | --- | --- |
| **Goal pressure** | Answer the user's question | Complete the assigned task |
| **Weak grounding** | Evidence not retrieved or not required | Policy not salient or not enforceable |
| **Misplaced confidence** | Plausible completion feels adequate | Action appears routine or justified |
| **Low-friction path** | Generate fluent answer | Invoke tool or proceed |
| **Result** | Unsupported claim | Unsafe action |
| **What is shared** | Premature sufficiency: the system acts before the topography has exerted enough force | |
| **What differs** | Consequence, severity, evaluation method, mitigation strategy | |
| **Implied intervention** | Make evidence visible, require citations, allow "I don't know," calibrate confidence | Make policy salient, require approval, surface consequences, connect prior failures |

This table should appear near the Cases A and B examples or near the Figure 4 placement.

---

## Required Retentions

| Element | Source | Why it must survive |
| --- | --- | --- |
| Gradient concept | v0.2 S6.1, lines 968-976 | Core mechanism. Behavior follows gradients. Citation: Ng et al. 1999. |
| Motion sequence: Attraction -> Investigation -> Sufficiency -> Action | v0.2 S6, lines 952-960 | Diagnostic model for understanding how behavior forms. |
| Two kinds of attraction: action vs. exploration | v0.2 S6.2, lines 1006-1018 | Explains why confidence can pull toward action OR investigation. |
| Investigation as bounded uncertainty reduction | v0.2 S6.3, lines 1024-1036 | Connects to bounded rationality. Citations: Simon, Pirolli & Card. |
| Sufficiency as stopping condition | v0.2 S6.5, lines 1072-1101 | Core concept. Motion stops at sufficiency, not certainty. |
| **Sufficiency is not certainty** — the 2x2 | v0.2 S6.5, lines 1086-1097 | Praised by 3/6 reviewers as immediately usable design heuristic. Must survive intact. |
| Premature sufficiency as shared failure pattern | v0.2 S7, lines 1220-1231 | Paper's most original contribution per 5/6 reviewers. |
| Shared failure grammar | v0.2 S7.3, lines 1278-1293 | Makes the structural parallel explicit and memorable. |
| Figure 4 placement | v0.2 S7, line 1296 | Visual anchor for motion and premature sufficiency. |
| Case A: "reduces readmissions" compliance example | v0.2 S7.5, lines 1326-1344 | Most concrete, realistic example. "Feels like a Tuesday." |
| Case B: unsafe tool action | v0.2 S7.5, lines 1346-1362 | Demonstrates the pattern in a safety domain. |
| "I don't know" and "I should not act yet" as action affordances | v0.2 S7.6, lines 1366-1383 | Essential for the safety argument. Not friction; motion options. |
| Same shape, different stakes clarification | v0.2 S7.7, lines 1386-1405 | Prevents the reader from collapsing hallucination and harmful action into one category. |
| Bridge to learning | v0.2 S7.9, lines 1424-1437 | "Outcome is not learning." Sets up Section 6 (v1.0). |

---

## Compression Candidates

| Element | Source | Why it can be compressed | Suggested treatment |
| --- | --- | --- | --- |
| Full campaign motion walkthrough (lines 1126-1147) | v0.2 S6.7 | Campaign walkthrough already previewed in S1 and S2; full trace lives in S5. | Remove or reduce to 2-3 sentence bridge. The motion sequence can be illustrated with the Case A/B examples instead. |
| Three separate safety failure subsections (lines 1150-1178) | v0.2 S6.8 | Hallucination, unsafe tool, and circumvention are each given a full pattern/diagnosis/intervention block. The premature sufficiency comparison table can carry this more efficiently. | Keep hallucination and unsafe tool (Cases A and B carry these). Merge circumvention into a brief mention or fold into the "shared failure grammar." |
| Task spawning subsection (lines 1050-1069) | v0.2 S6.4 | Important concept but tangential to the main S4 arc. | Compress to 2-3 sentences within Investigation. The idea that investigation can spawn sub-questions is worth stating but does not need its own subsection. |
| "More context does not fix a bad path" subsection (lines 1302-1319) | v0.2 S7.4 | Important point but partially covered by S2 (context is not reasoning state) and the Cases A/B examples. | Compress to one strong paragraph. The Cases already demonstrate that retrieval alone is insufficient. |
| "Evaluation should diagnose the shape" subsection (lines 1408-1420) | v0.2 S7.8 | Belongs more in S9 (Boundaries, Objections, and Falsifiability) than in the motion/failure section. | Defer to S9 or compress to one sentence in the S4 bridge. |
| Reward-hacking/KPI-gaming paragraph (lines 986) | v0.2 S6.1 | Interesting but tangential to the core S4 argument. | Cut or reduce to one sentence. The gradient concept does not require the organizational-behavior parallel to land. |
| "Design changes the path of least resistance" subsection (lines 1182-1195) | v0.2 S6.9 | Summary of design levers already implied by the motion model and the Cases. | Compress to 2-3 sentences. The diagnosis-to-intervention mapping in S3 already covers the practical design lever logic. |

---

## Deferrable Material

| Element | Where it goes instead | Why |
| --- | --- | --- |
| Full campaign motion walkthrough | v1.0 S5 (Constructed Stress Test) | S5 owns the end-to-end trace. S4 needs only the Cases A/B to illustrate premature sufficiency. |
| Evaluation should diagnose the shape | v1.0 S9 (Boundaries, Objections, and Falsifiability) | Evaluation methodology belongs with validation and falsifiability. |
| Extended design-levers summary | Already covered by S3 diagnosis-to-intervention mapping | S3 provides the practical mapping. S4 does not need to restate it. |
| Formal falsifiability of premature sufficiency | v1.0 S9 | The claim that premature sufficiency is testable belongs in the falsifiability section. |

---

## Risks / Watch Items

1. **The sufficiency-vs-certainty 2x2 must survive intact.** This is one of the paper's most praised distinctions (3/6 reviewers). It should appear prominently, not buried. Consider making it a visually distinct block (indented examples or a small table).

2. **The S6+S7 merge must maintain the logical flow.** Gradients create motion -> sufficiency stops motion -> premature sufficiency = failure. If the merge jumbles the sequence, the reader loses the causal chain.

3. **Do not make hallucination and harmful action sound morally equivalent.** The clarification ("same shape, different stakes") must appear near the comparison. The paper should never suggest that a fabricated citation and an unsafe data access are the same kind of failure. They share structure, not severity.

4. **Cases A and B are the section's anchors.** The "reduces readmissions" example was praised as "feels like a Tuesday" by the skeptical practitioner. The unsafe-tool example demonstrates the pattern in a safety domain. Both must survive in full.

5. **Do not over-explain every motion stage.** Attraction, Investigation, Sufficiency, and Action can each be explained in one paragraph with one example. The full walkthrough belongs in S5. S4 should introduce the concepts clearly, not exhaustively.

6. **"I don't know" and "I should not act yet" should feel like design principles, not caveats.** These are action affordances that reshape the topography. Frame them positively.

7. **The premature sufficiency comparison table should complement, not replace, Cases A and B.** The table shows the structural parallel at a glance. The Cases make it concrete. Both are needed.

8. **Citations for hallucination surveys should be added inline.** The citation workstream identifies Ji et al. 2023, Huang et al. 2023, Maynez et al. 2020 as Tier 1 additions for S4. Menick et al. 2022 and Lewis et al. 2020 are already cited. Trust-in-automation (Lee & See 2004, Parasuraman & Riley 1997) should also appear.

---

## Drafting Instructions for ChatGPT and Benet

**Goal:** Draft S4 as the section where the framework becomes dynamic. The reader should finish S4 understanding how behavior emerges from gradients, why sufficiency is the stopping condition, and why premature sufficiency connects hallucination and harmful action.

**Tone:** Clear, diagnostic, specific. This section should feel like someone handing the reader a tool: "When something goes wrong, ask what made the bad path feel sufficient." The tone should be practical and precise, not dramatic.

**Length target:** ~2,000-3,000 words. v0.2 S6 is ~275 lines (~3,400 words) and S7 is ~228 lines (~2,800 words), totaling ~6,200 words. The merge should produce ~2,000-3,000 words through compression of repeated walkthroughs, redundant safety illustrations, and tangential material. Reader comprehension governs.

**Structure suggestion (not binding):**

1. Transition from S3: landscape describes the environment; now motion describes how behavior emerges. (~100 words)
2. Gradient defined: directional pressure in the topography. Not mathematical; a design term. (~150 words)
3. Motion sequence introduced: Attraction -> Investigation -> Sufficiency -> Action. Not rigid; diagnostic. (~100 words)
4. Attraction: action vs. exploration. Confidence governs which. (~200 words)
5. Investigation: bounded uncertainty reduction. Investigate only when the answer could change the action. (~200 words)
6. Sufficiency: the stopping condition. **Sufficiency is not certainty.** The 2x2. (~300 words — give this space)
7. Action: includes asking, escalating, refusing. Not just task completion. (~150 words)
8. Transition to failure: when sufficiency comes too soon. (~100 words)
9. Premature sufficiency defined. Shared failure grammar. (~200 words)
10. Premature sufficiency comparison table. (~table)
11. Figure 4 placement.
12. Case A: "reduces readmissions." (~200 words)
13. Case B: unsafe tool action. (~200 words)
14. "I don't know" and "I should not act yet" as action affordances. (~150 words)
15. Same shape, different stakes clarification. (~100 words)
16. Bridge to S5: the constructed stress test will show the full framework in action. Bridge to S6: learning begins when reality pushes back. (~100 words)

**Rewrite standard:** Does every paragraph help the reader diagnose behavior as motion through a perceived landscape? If yes, preserve it. If no, compress or cut it.

**What to write toward:**
- A reader finishes S4 and can say: "Behavior follows gradients. The system acts when it reaches sufficiency. Sufficiency is not certainty — you can be uncertain and still have enough to act, or confident in one fact but still lack enough for the decision. When sufficiency comes too soon, the result is premature sufficiency. Both hallucination and harmful action can follow this pattern: the system acts before the topography has exerted enough force. The 'reduces readmissions' example shows what better-shaped behavior looks like."

**What to avoid:**
- Re-explaining optimizer state or the five dimensions in detail — S3 owns those.
- Running the full healthcare stress test — S5 owns that.
- Making hallucination and harmful action sound morally equivalent.
- Over-explaining every motion stage with multiple examples when one suffices.
- Drifting into implementation architecture or evaluation methodology.
- Presenting premature sufficiency as the only failure pattern (it is the most common shared pattern, not the only one).
