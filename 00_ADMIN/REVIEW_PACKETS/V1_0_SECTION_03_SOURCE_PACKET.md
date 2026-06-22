# Section 3 Source Packet: Optimizer State and Perceived Topography

---

## Purpose of Section 3

Section 3 introduces the two structural components that the rest of the framework depends on: what the optimizer brings (Goal, Policy, Interpretation) and what the landscape provides (five topography dimensions). This is the section where the reader learns the tools they will use for the rest of the paper.

Section 2 ended with: "The next section defines what must be preserved first: the optimizer's working frame and the perceived landscape it moves through."

Section 3 must deliver on that promise. By the end of Section 3, the reader should understand what an optimizer state is, what perceived topography is, why these are distinct, and how the five dimensions produce diagnostic and interventional leverage.

This section merges v0.2 Section 4 (The System Needs a Working Frame) and v0.2 Section 5 (The System Moves Through a Shaped World) into a single continuous argument. The merge must preserve the conceptual distinction between what the optimizer brings and what the landscape provides.

---

## Required Arc Moves

Section 3 must accomplish these arc moves in order:

1. The optimizer as functional abstraction — behavioral description, not psychological claim. [Russell & Norvig, 2020] [Dennett, 1987]
2. Three primitives: Goal, Policy, Interpretation — the minimum elements required to explain why the same information can produce different behavior.
3. Goal gives motion direction. Goal relevance is relational, not a standalone dimension.
4. Policy shapes what counts as acceptable. Policy must exert force through the topography to affect behavior.
5. Interpretation turns signals into meaning. Three subtypes: signal meaning, causal explanation, action model. [Weick, 1995]
6. Optimizer State = Goal + Policy + Interpretation. Concise defense of why three primitives suffice.
7. Transition: optimizer state alone does not explain behavior. The optimizer needs an environment to move through.
8. Information Topography defined: the perceived information-and-action landscape. "Information only shapes behavior if it exerts force inside the optimizer's perceived topography."
9. Figure 3 placement.
10. Five dimensions defined: Visibility, Accessibility, Representation, Confidence, Connectivity. Each with its diagnostic question.
11. Dimension admission matrix: why these five, why not others (Timeliness, Salience, Completeness, Relevance, Trust, Policy, Memory).
12. Diagnosis-to-intervention mapping: if the problem is Visibility, expose the signal; if Accessibility, improve retrieval; etc.
13. Affordances bridge: topography is related to affordances. [Gibson, 1979] [Norman, 1988]
14. "Arbitrary dimensions" objection response (per authorial decision: place in S3 where it naturally arises).
15. Bridge to Section 4: topography describes the landscape; Section 4 describes how behavior emerges from it.

---

## Source Material from v0.2

### From v0.2 Section 4 (lines 348-628): Optimizer and Working Frame

**Optimizer as functional abstraction (lines 350-356):**
> The framework uses optimizer as a functional abstraction. It does not claim that a language model is internally, mechanistically, or consciously optimizing... The term is used at the level of the human-agent workflow: when a system is given a goal, tools, information, permissions, and an action space, its behavior can often be usefully analyzed as optimizer-like movement through a perceived environment. [Russell & Norvig, 2020] [Dennett, 1987]

**Three primitives (lines 358-374):**
> In this framework, an optimizer has three minimum primitives: Goal, Policy, Interpretation.
> These are the minimum elements required to explain why the same information can produce different behavior in different systems or different moments.

**Goal gives direction (lines 378-412):**
> A goal is the directional objective the optimizer acts in relation to.
> Goals determine relevance... "Goal relevance" is not treated as a standalone topography dimension. Goal relevance is relational. It emerges from the relationship between an active goal and available information.

**Policy shapes acceptability (lines 415-455):**
> A policy is a constraint on optimizer behavior... The framework treats policy as a boundary condition, not merely as text.
> A policy written in a document does not automatically constrain behavior. To shape action, the policy must become visible, accessible, represented clearly, connected to the active task, and salient at the moment of decision.

**Interpretation turns signals into meaning (lines 458-487):**
> Interpretation is the optimizer's working understanding of what information means.
> Three subtypes: Signal Meaning, Causal Explanation, Action Model.
> Action Model is not a fourth primitive. It is a subtype of Interpretation. [Weick, 1995]

**Optimizer State = Goal + Policy + Interpretation (lines 490-528):**
> The combination of Goal, Policy, and Interpretation forms the Optimizer State.
> [Campaign example walkthrough — optimizer state inference]

**Three Primitives Are Enough (lines 532-567):**
> The framework intentionally keeps the optimizer primitive set small.
> It might be tempting to add additional primitives: Capability, Memory, Tools, Reward, Decision Space, Action Model, Confidence, Attention.
> [Defense of why each is not promoted]
> The question for primitives is not: Is this important? The question is: Is this required to explain optimizer direction, constraint, and meaning?

**Safety needs the frame (lines 570-606):**
> A moralized frame asks: Why did the agent lie?
> A topography-aware optimizer frame asks: What goal was active? What policy was visible? How was the situation interpreted?
> [Three diagnostic examples: unsupported claim, unsafe tool action, constraint bypass]

**Bridge to topography (lines 609-624):**
> Optimizer State explains the starting condition... But optimizer state alone does not explain behavior. The optimizer still needs an environment to move through.

### From v0.2 Section 5 (lines 629-937): Perceived Topography

**Topography defined (lines 629-652):**
> The environment is not the objective world in full. It is the world as made available to the optimizer...
> This paper calls that environment Information Topography.
> Information only shapes behavior if it exerts force inside the optimizer's perceived topography.

**Figure 3 placement (lines 655-659):**
> ![Optimizer in a Perceived Topography](paper_assets/svg/fig3_optimizer_in_topography.svg)

**Five dimensions table (lines 661-685):**
> Visibility: Can the optimizer see that the information exists?
> Accessibility: Can the optimizer reach or retrieve it at acceptable cost?
> Representation: Can the optimizer understand and use how the information is expressed?
> Confidence: Does the optimizer trust the information enough for it to shape action?
> Connectivity: Can the optimizer connect the information to other signals, assumptions, policies, decisions, or outcomes?

**Individual dimension explanations (lines 689-799):**
Each dimension gets its own subsection (~20-30 lines each) with definition, examples, failure modes, and organizational illustrations. Key material:

- Visibility (lines 689-708): "Should have known" usually hides a topographic question.
- Accessibility (lines 711-726): Optimizers prefer available paths. Cost, latency, permissioning matter.
- Representation (lines 729-742): Information can be visible and accessible but still fail because it is poorly represented. Links Topography to Interpretation.
- Confidence (lines 745-773): Not the same as truth. Central to reliability and safety. Overconfidence and underconfidence as opposite errors.
- Connectivity (lines 776-799): Turns isolated information into a reasoning network. Bridge between context and reasoning state.

**Goal Relevance defense (lines 802-823):**
> Goal Relevance is not a standalone dimension. It cannot be evaluated without an active goal. It is a projection of Goal onto the Information Topography.
> Goal determines what matters. Topography determines whether what matters can exert force.

**Policy defense (lines 826-849):**
> Policy is part of optimizer state. It defines constraints on behavior. However, policy must be expressed through topography to affect action.
> If policy were treated as a topography dimension, the framework would blur the difference between constraint and environment.

**Affordances (lines 852-863):**
> The framework's use of topography is closely related to the idea of affordances. [Gibson, 1979] [Norman, 1988]

**Campaign topography walkthrough (lines 866-900):**
> [Full dimension-by-dimension walkthrough of the healthcare campaign through all five dimensions]

**Diagnosis-to-intervention mapping (lines 902-916):**
> If the problem is Visibility, expose the signal. If the problem is Accessibility, improve retrieval or routing. If the problem is Representation, restructure the information. If the problem is Confidence, calibrate evidence thresholds. If the problem is Connectivity, connect the signal to the relevant policy, premise, action, or model update.
> Topography turns vague failure into design diagnosis.

**Bridge to motion (lines 920-933):**
> Information Topography describes the landscape. But landscape alone does not explain movement.
> Optimizer State defines what the system brings. Information Topography defines what the system navigates. Optimizer Motion defines how behavior emerges from their interaction.

---

## Existing SVG Placement

- **fig3_optimizer_in_topography.svg** — Place after the optimizer/topography distinction has been established and the five dimensions have been introduced (or are being introduced). In v0.2 this appears at line 657, between the topography definition and the five-dimension table. In v1.0, place it after the transition from optimizer state to topography — the moment when the reader sees both components together for the first time.

---

## New Visual Candidate

### Dimension Admission Matrix

**Purpose:** Defend the five dimensions by showing why candidates were not promoted. This replaces the prose-heavy S5.7 and S5.8 subsections and the extended defensive argumentation.

**Admission rule:**

```
A dimension earns its place only if changing it would lead to a
different diagnosis, intervention, or expected outcome.
```

**Table 1. Dimension Admission Matrix**

The five dimensions below are not presented as a closed ontology. They are a minimum viable diagnostic set. A candidate dimension should be promoted only if naming it would change the diagnosis, intervention, or expected outcome.

| Candidate dimension | Why it seems tempting | Placement in this framework | Promotion test |
| --- | --- | --- | --- |
| Timeliness | Stale information is a common failure mode. | Usually handled through Confidence, Accessibility, or Visibility. A stale source may lose trust, a current source may be unreachable, or an update may not be surfaced. | Promote only if it produces a diagnosis the existing five cannot produce. |
| Salience | Information can be present but not noticed. | Usually handled through Visibility and Representation. A signal may need to be surfaced or formatted so it stands out. | Promote only if it leads to an intervention distinct from improving Visibility or Representation. |
| Completeness | The system may retrieve only part of what matters. | Usually emerges from several dimensions and becomes operational through the sufficiency mechanism in Section 4. | Promote only if it produces a distinct diagnosis not captured by the five dimensions plus sufficiency. |
| Relevance | Accurate information may not matter to the current task. | Treated as a projection from the active Goal. Goal determines what matters; topography determines whether what matters can exert force. | Promote only if it leads to an intervention other than clarifying the Goal or improving Connectivity. |
| Trust | The system may rely on the wrong source. | Treated primarily through Confidence. Confidence carries the trust function in the current framework. | Promote only if it identifies a distinct failure, such as high perceived reliability but low institutional authority, that Confidence cannot diagnose. |
| Policy | A policy may exist but fail to constrain action. | Treated as part of optimizer state. Policy must still become visible, accessible, represented, trusted, and connected in the topography to exert force. | Promote only if policy-as-dimension produces a diagnosis not captured by applying the five dimensions to policy signals. |
| Memory | The system may forget what happened last time. | Treated as artifact storage or reasoning-state preservation, not as topography itself. Prior learning must still become visible, accessible, represented, trusted, and connected to the current decision. | Promote only if it produces a diagnosis the existing dimensions cannot explain. |

**Reader-facing rule (to include in prose near the matrix):**

```
If naming a candidate changes what the designer would diagnose or do,
it may deserve promotion. If it does not, it should not multiply the
framework's vocabulary.
```

The matrix should appear after the five dimensions are defined and the diagnosis-to-intervention mapping is shown, so the reader can evaluate each candidate against the working diagnostic set.

---

## Required Retentions

| Element | Source | Why it must survive |
| --- | --- | --- |
| Optimizer as functional abstraction, not psychological claim | v0.2 S4, lines 350-356 | Prevents the most obvious objection (LLMs are not literally optimizers). Citations: Russell & Norvig, Dennett. |
| Three primitives: Goal, Policy, Interpretation | v0.2 S4, lines 358-374 | Core architecture. The reader needs these before topography. |
| Goal gives direction; goal relevance is relational | v0.2 S4, lines 378-412 | Explains why Goal Relevance is not a sixth dimension. |
| Policy must exert force through topography | v0.2 S4, lines 415-455 | Critical for the safety argument. Policy as boundary condition, not mere text. |
| Interpretation: signal meaning, causal explanation, action model | v0.2 S4, lines 458-487 | Connects to sensemaking. Weick citation. |
| Optimizer State = Goal + Policy + Interpretation | v0.2 S4, line 492 | The formula. Reader must hold this. |
| Concise defense of three primitives | v0.2 S4.5, lines 532-567 | Compressed, not removed. One paragraph, not a full subsection. |
| Information Topography defined | v0.2 S5, lines 629-652 | Core concept. "Information only shapes behavior if it exerts force." |
| Five dimensions with diagnostic questions | v0.2 S5.1, lines 661-685 | The table is the most compact and useful form. |
| Individual dimension definitions | v0.2 S5.2-S5.6 | Each dimension needs enough explanation to be understood, but not the full v0.2 treatment. |
| Figure 3 placement | v0.2 S5, line 657 | Visual anchor for the optimizer-in-topography concept. |
| Diagnosis-to-intervention mapping | v0.2 S5.11, lines 902-916 | Clearest bridge from theory to practice in the topography section. Valued by reviewers. |
| Affordances bridge | v0.2 S5.9, lines 852-863 | Gibson and Norman citations. Brief is sufficient. |
| Dimension admission matrix | New for v1.0 (doctrine Section 6) | Responds to 4/6 reviewers who challenged the five dimensions. Replaces defensive prose with a compact table. |
| Bridge to Section 4 | v0.2 S5.12, lines 920-933 | "Optimizer State defines what the system brings. Information Topography defines what the system navigates. Optimizer Motion defines how behavior emerges." |

---

## Compression Candidates

| Element | Source | Why it can be compressed | Suggested treatment |
| --- | --- | --- | --- |
| Full campaign walkthrough in S4.4 (lines 500-528) | v0.2 S4.4 | S1 and S2 already preview the campaign. S5 carries the full trace. | One brief bridge: "Return to the healthcare campaign. The optimizer state can now be made explicit: the goal is demo requests, the policy includes claims constraints, the interpretation treats workflow burden as the primary buying trigger." No full re-derivation. |
| "Three Primitives Are Enough" subsection (lines 532-567) | v0.2 S4.5 | ~500 words of defensive argumentation. Reads as "I considered alternatives." | Compress to one paragraph: "Other candidates were considered (Capability, Memory, Tools, Reward). These are properties of the topography or implementation, not of the optimizer's working frame. The question is not whether they are important, but whether they are required to explain direction, constraint, and meaning." |
| Safety needs the frame subsection (lines 570-606) | v0.2 S4.6 | Three diagnostic examples (unsupported claim, unsafe tool, constraint bypass). | Keep one or two diagnostic examples. The third can be cut. The point is made with two. S4 will carry the full premature-sufficiency argument. |
| Full campaign topography walkthrough (lines 866-900) | v0.2 S5.10 | Walks all five dimensions through the campaign. ~35 lines. | Compress heavily or remove. The diagnosis-to-intervention mapping (S5.11) already shows the practical payoff. S5 carries the full trace. A brief 2-3 sentence bridge is enough. |
| Goal Relevance defense (lines 802-823) | v0.2 S5.7 | Full subsection defending why Goal Relevance is not a dimension. | Replace with one row in the dimension admission matrix. The matrix handles this more concisely. |
| Policy defense (lines 826-849) | v0.2 S5.8 | Full subsection defending why Policy is not a dimension. | Replace with one row in the dimension admission matrix. |
| Individual dimension subsections (lines 689-799) | v0.2 S5.2-S5.6 | Each dimension gets ~20-30 lines. Some examples overlap with S4 safety examples and S5.10 campaign walkthrough. | Keep each dimension definition and its core diagnostic question. Trim organizational illustrations by ~30-40%. One example per dimension is enough. |

---

## Deferrable Material

| Element | Where it goes instead | Why |
| --- | --- | --- |
| Full campaign topography walkthrough | v1.0 S5 (Constructed Stress Test) | S5 owns the end-to-end trace. S3 needs only enough campaign reference to ground the concepts. |
| Extended safety diagnostic examples | v1.0 S4 (Gradients, Sufficiency, and Failure) | S4 carries the premature-sufficiency argument and the full hallucination/harmful-action parallel. S3 needs only 1-2 brief safety examples. |
| Formal dimension independence analysis | Academic/research track | The dimension admission matrix provides a practical defense. Formal independence testing belongs in the academic paper. |
| Information science citations for dimensions | v1.0 S3 inline (per citation workstream) | Wilson, Kuhlthau, Bates, Endsley should be cited inline where the dimensions are introduced, not deferred to S10. This is a citation addition, not a deferral. |

---

## Risks / Watch Items

1. **The S4+S5 merge must not blur the optimizer/topography distinction.** This is the biggest structural change in v1.0. The section must clearly show: first, what the optimizer brings (Goal, Policy, Interpretation); then, what the landscape provides (five dimensions). Use a clear transition between the two halves. Consider a subheading break.

2. **The dimension admission matrix must not feel defensive.** It should feel like a natural part of the argument: "Here is how we selected these dimensions. Here is the test. Here are the candidates that did not pass." The tone should be confident and practical, not apologetic.

3. **Dimension definitions must be concise but not cryptic.** v0.2 gives each dimension 20-30 lines. v1.0 should give each dimension ~10-15 lines: definition, diagnostic question, one concrete example, one failure mode. The five-dimension table provides the compact overview; the prose provides the understanding.

4. **The affordances bridge should be brief.** Gibson and Norman citations earn their place, but the affordances connection can be made in 3-4 sentences, not a full subsection.

5. **The "arbitrary dimensions" objection must be addressed in this section, not deferred.** Per the authorial decisions, this objection is placed where it naturally arises (S3). The dimension admission matrix is the primary response. One sentence of framing ("These five are offered as a minimum viable diagnostic set, not a closed ontology") plus the matrix is sufficient.

6. **Citations from information science should be added inline.** The citation workstream identifies a significant gap: Wilson, Kuhlthau, Bates, Endsley. These should appear in S3 where the dimensions are introduced, not only in S10. This is a Tier 1 citation priority.

7. **Do not introduce gradients, sufficiency, or premature sufficiency.** Section 4 owns those concepts. Section 3 ends with "landscape alone does not explain movement" and bridges to S4.

---

## Drafting Instructions for ChatGPT and Benet

**Goal:** Draft S3 as a single continuous section that introduces both the optimizer's working frame and the perceived topography. The reader should finish S3 able to state: "An optimizer has a goal, policy, and interpretation. It moves through a topography shaped by visibility, accessibility, representation, confidence, and connectivity. These dimensions determine whether information exerts force on behavior."

**Tone:** Precise but not jargon-heavy. Each concept should feel like a useful tool being handed to the reader, not an abstract category being imposed.

**Length target:** ~2,000-3,000 words. v0.2 S4 is ~280 lines (~3,500 words) and S5 is ~310 lines (~3,800 words), totaling ~7,300 words. The merge should produce ~2,000-3,000 words through compression of repeated walkthroughs, defensive prose, and overlapping examples. Reader comprehension governs.

**Structure suggestion (not binding):**

1. Opening: transition from S2's design claim. The system needs a working frame for what to preserve. (~100 words)
2. Optimizer as functional abstraction. Three primitives introduced. (~200 words)
3. Goal: gives direction. Goal relevance is relational. (~200 words)
4. Policy: shapes what counts as acceptable. Must exert force through topography. (~250 words)
5. Interpretation: turns signals into meaning. Three subtypes. Sensemaking connection. (~250 words)
6. Optimizer State = Goal + Policy + Interpretation. Concise "why three" defense. (~150 words)
7. Brief campaign bridge: optimizer state made explicit for the healthcare example. (~100 words)
8. Transition: optimizer state alone does not explain behavior. The optimizer needs an environment. (~100 words)
9. Information Topography defined. "Information only shapes behavior if it exerts force." (~200 words)
10. Figure 3 placement.
11. Five dimensions: table with diagnostic questions, then ~10-15 lines per dimension. (~600-800 words)
12. Dimension admission matrix. Admission rule. Reader-facing rule. (~300 words including table)
13. Affordances bridge. Gibson and Norman. (~100 words)
14. Diagnosis-to-intervention mapping. (~200 words)
15. Bridge to Section 4: landscape describes the environment; next section describes motion. (~100 words)

**Rewrite standard:** Does every paragraph help the reader use the optimizer/topography distinction to diagnose behavior? If yes, preserve it. If no, compress or cut it.

**What to write toward:**
- A reader finishes S3 and can say: "The framework has two structural components. The optimizer brings a goal, policy, and interpretation. The topography provides information shaped by five dimensions. When I diagnose a failure, I should ask: was the relevant information visible, accessible, well-represented, trusted, and connected? Each dimension points to a different intervention."

**What to avoid:**
- Blurring optimizer state and topography into one undifferentiated list.
- Making the five dimensions sound arbitrary or defensive.
- Running the full healthcare stress test — S5 owns that.
- Introducing gradients, sufficiency, or premature sufficiency — S4 owns those.
- Over-explaining each dimension with multiple examples when one suffices.
- Listing every excluded primitive with full defense — the one-paragraph version is enough.
