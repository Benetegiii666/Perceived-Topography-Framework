# The Perceived Topography Framework

## A Reasoning-State Architecture for Human-Agent Systems

**Version 1.0 — Working Draft — June 2026**

---

## Abstract

<!--
Arc responsibility: State thesis, method (pre-empirical framework + constructed stress test), key contribution (premature sufficiency + reasoning-state preservation).
Source sections: New for v1.0.
Visual/table placement: None.
Status: NOT YET DRAFTED
-->

---

## Epistemic Status

<!--
Arc responsibility: Declare this is a pre-empirical design framework. Constructed stress test, not empirical validation. Section 9 defines falsifiability conditions.
Source sections: New for v1.0 (draws from v0.2 S14 framing).
Visual/table placement: None.
Status: NOT YET DRAFTED
-->

---

## 1. From Agent Fear to Landscape Design

<!--
Arc responsibility: Fear -> wrong question ("What is wrong with the agent?") -> better question ("What landscape shapes behavior?") -> marble analogy -> containment-vs-landscape reframe -> pre-empirical framing -> inline term orientation (optimizer, topography, gradient, reasoning state) -> light healthcare preview -> thesis.
Source sections: v0.2 S1 (lines 13-77), v0.2 S2 (lines 80-155).
Visual/table placement: fig1_fear_to_landscape.svg. New: full-framework loop diagram (reader map).
Status: DRAFT INSERTED / PENDING REVIEW
-->

Public discussion of AI agents has begun to acquire a familiar shape. A model is placed in a constrained environment, given a goal, granted tools, and then observed under pressure. Sometimes it fabricates facts. Sometimes it appears to deceive. Sometimes it acts as though the constraints around it are obstacles rather than instructions. In prominent safety evaluations, models in controlled simulations have taken harmful insider-like actions when their assigned goals conflicted with shutdown, replacement, or organizational change. [Lynch et al., 2025]

The natural reaction is fear. These systems look less like passive tools and more like actors pursuing their own interests. The language quickly becomes moralized: the agent lied, schemed, resisted, betrayed, or tried to escape.

Those concerns should not be dismissed. Systems that can plan, use tools, access sensitive information, communicate externally, and act over longer horizons create real risk. A model does not need inner malice to cause harm. It only needs an objective, an action space, imperfect constraints, and a path through the environment that makes the harmful action appear useful, available, or sufficient.

The point, then, is not to deny that models can exhibit behavior that appears deceptive, self-protective, or strategically harmful. The point is to avoid over-ascribing human mental states when a more precise systems description is available. [Shanahan et al., 2023] Dangerous behavior can be real even when the best explanation is not malice, desire, or intent in the human sense. The question is whether we can describe the conditions that made the behavior available, attractive, and sufficient enough to execute.

This paper proposes that we can.

AI agents are not best understood as moral agents in miniature. They are better understood as optimizer-like systems moving through perceived information environments. By optimizer, I do not mean a conscious entity with intentions. I mean a system that selects actions in relation to a goal, under constraints, using some interpretation of the situation. This is a behavioral description, not a psychological claim.

The more useful question is often not only:

> What is wrong with the agent?

It is also:

> What landscape did we ask it to move through, and what gradients did that landscape create?

A useful image is simple: when a marble rolls downhill, we do not explain its motion only by studying the marble. We look at the slope. AI agents should be treated the same way. Their behavior emerges not only from what they are internally capable of doing, but from the environment of visible options, accessible tools, represented goals, trusted signals, and connected consequences through which they move.

The dominant safety metaphor remains containment. We build fences: permissions, filters, system prompts, policy restrictions, sandboxing, monitoring, and human approval gates. These are necessary. But a fence is not the same thing as a landscape. A boundary tells the optimizer where not to go. It does not necessarily create a better path toward where it should go.

If the desired path is obscure, poorly represented, hard to reach, weakly connected to the goal, or less confidence-producing than an unsafe shortcut, then containment alone may not produce good behavior. It may only delay bad behavior, catch it after the fact, or push it into a different form. Safety and reliability require more than stronger boxes. They also require landscape design: shaping the perceived environment so that grounded, policy-aware, human-beneficial behavior becomes the most available, most confident, and most sufficient path.

![Figure 1: From Agent Fear to Landscape Design](figures/fig1_fear_to_landscape.svg)

*Figure 1 is a conceptual map, not a literal terrain model. "Topography" and "gradient" are analytic metaphors for how information, tools, confidence, and constraints are made available to a system.*

The underlying idea is simple: systems do not act on the world as it is. They act on the world as it is made available to them.

In this paper, topography means the perceived information-and-action environment through which an optimizer moves. It includes what the system can see, what it can reach, how information is represented, what appears trustworthy, and which pieces of information are connected to one another. A gradient is a directional pressure within that perceived topography. It is the reason one path becomes easier, more attractive, more available, or more sufficient than another.

That last word matters. Many failures do not begin when a system decides to be bad. They begin when a system reaches sufficiency too soon.

A hallucination may occur when a model has enough pattern support to produce a plausible answer, but not enough grounding to justify it. A harmful tool action may occur when an agent has enough goal pressure to act, but not enough policy connection, uncertainty recognition, or human confirmation to wait. These failures differ in consequence, but they can share a motion pattern: insufficient grounding becomes premature sufficiency.

That is why this paper treats agent behavior as a landscape-design problem. Instead of asking only whether the model was aligned, constrained, or instructed, we should also ask how the system's perceived world was shaped. What did it see? What could it reach? How were policy constraints represented? What appeared confident? What information was connected to the goal? What was missing before action became sufficient?

This also changes what we need to preserve. Context is not the same thing as reasoning state. Context can contain documents, snippets, prior messages, examples, or retrieved passages. Reasoning state is the structured condition from which a system acts. It includes the active goal, governing policies, interpretation of the situation, relevant premises, confidence levels, uncertainty signals, sufficiency rationale, and the path by which one option became preferable to another. Context may help a system answer. Reasoning state explains why the system acted as it did.

Consider a marketing agent asked to generate a healthcare campaign for a remote patient monitoring product. A context-only system may retrieve brand guidelines, product messaging, customer profiles, and prior campaign examples. That retrieval is useful, but incomplete. If the system generates the claim that the product "reduces readmissions," the important question is not only whether the phrase appeared somewhere in the context. The important question is why that claim became sufficient.

Did the system distinguish operational benefits from clinical outcome claims? Did it connect the claim to policy constraints? Did it know whether supporting evidence was required? Would any of that reasoning survive if the claim were later rejected?

This paper uses that kind of scenario as a constructed stress test. It is not presented as empirical validation. It is a way to examine whether the framework produces a different diagnosis than a context-only approach, a better-prompting approach, or a generic governance checklist. The broader argument is pre-empirical: it proposes a design framework, grounds that framework in existing traditions, works through a constructed case, and identifies claims that future research or implementation can test.

The claim is not that landscape design replaces alignment, containment, retrieval, evaluation, governance, or human oversight. The claim is that these efforts are incomplete without a way to describe and shape the perceived topography through which agents move. A system can be constrained and still move poorly. It can retrieve relevant context and still lose the reasoning behind its action. It can be corrected after failure and still fail to learn if the lesson does not change the next cycle.

The core movement of the paper is therefore:

> from context to reasoning, from containment to topography, from isolated outputs to preserved state transitions, and from static governance to adaptive learning.

[Placeholder: Full-framework loop diagram — Fear → Landscape → Optimizer State → Perceived Topography → Gradients → Sufficiency → Action/Outcome → Learning → Preserved Reasoning → Next Cycle.]

This is the design layer the paper adds. It does not ask readers to abandon existing AI safety, governance, or product-design practices. It asks them to look at a missing layer between instruction and action: the shaped world through which the system reasons, acts, fails, and learns.

If AI agents are optimizer-like systems moving through perceived environments, then the central design question changes. Not only:

> How do we prevent escape?

But also:

> How do we shape the landscape so that grounded, policy-aware, human-beneficial behavior becomes the most available, most confident, and most sufficient path?

The next section begins with the reason this design layer is necessary: context alone does not preserve the why.

---

## 2. Context Does Not Preserve the Why

<!--
Arc responsibility: Context is not reasoning state -> documents preserve artifacts but not transitions -> the gap -> first full healthcare campaign introduction.
Source sections: v0.2 S3 (lines 156-347).
Visual/table placement: fig2_context_vs_reasoning_state.svg.
Status: NOT YET DRAFTED
-->

---

## 3. Optimizer State and Perceived Topography

<!--
Arc responsibility: Optimizer state (goal, policy, interpretation) -> five topography dimensions (Visibility, Accessibility, Representation, Confidence, Connectivity) -> dimension admission matrix -> diagnosis-to-intervention mapping -> "arbitrary dimensions" objection response.
Source sections: v0.2 S4 (lines 348-628), v0.2 S5 (lines 629-937).
Visual/table placement: fig3_optimizer_in_topography.svg. New: dimension admission matrix (table).
Status: NOT YET DRAFTED
-->

---

## 4. Gradients, Sufficiency, and Failure

<!--
Arc responsibility: Gradients -> motion stages (compressed) -> sufficiency vs certainty -> premature sufficiency -> hallucination/harmful-action parallel -> compliance example ("reduces readmissions") -> Case B unsafe tool action.
Source sections: v0.2 S6 (lines 938-1213), v0.2 S7 (lines 1214-1441).
Visual/table placement: fig4_motion_and_premature_sufficiency.svg. New: premature sufficiency comparison table (hallucination vs harmful action, side-by-side).
Status: NOT YET DRAFTED
-->

---

## 5. A Constructed Stress Test: The Healthcare Campaign

<!--
Arc responsibility: Full end-to-end trace: context-only path vs reasoning-state path vs next-cycle learning. Demonstrates framework value-add. Constructed-scenario framing.
Source sections: v0.2 S12 (lines 2481-2686), with elements drawn from campaign passages across S3-S11.
Visual/table placement: New: healthcare worked-simulation trace table (three columns: context-only / reasoning-state / next-cycle learning).
Status: NOT YET DRAFTED
-->

---

## 6. Learning Requires Preserved Reasoning

<!--
Arc responsibility: Learning is not memory or reaction -> prediction error -> evidence-supported model update -> MUO concept, eleven-field spec, ten failure modes -> six reasoning objects (compressed) -> KM graveyard confrontation -> "KM graveyard" objection response.
Source sections: v0.2 S8 (lines 1442-1758), v0.2 S9 (lines 1759-1972), v0.2 S10 (lines 1973-2216).
Visual/table placement: fig5_learning_is_model_change.svg, fig6_reasoning_architecture_six_objects.svg.
Status: NOT YET DRAFTED
-->

---

## 7. Discovery Turns Human Intent Into Reusable Reasoning

<!--
Arc responsibility: Discovery Framework -> Retrieve-Infer-Propose-Confirm -> "do the reasoning work before asking the user" -> Discovery Pattern Update -> "better RAG + better prompts" objection response.
Source sections: v0.2 S11 (lines 2217-2480).
Visual/table placement: fig7_runtime_discovery_loop.svg.
Status: NOT YET DRAFTED
-->

---

## 8. What It Would Take to Build This

<!--
Arc responsibility: Implementation bridge -> maturity model (Stage 0-4) -> "Do Not Start With the Whole Machine" -> architecture map (new visual). Keep only enough implementation for theory credibility.
Source sections: v0.2 S13 (lines 2687-2903).
Visual/table placement: New: implementation bridge / architecture map (layered diagram).
Status: NOT YET DRAFTED
-->

---

## 9. Boundaries, Objections, and Falsifiability

<!--
Arc responsibility: Six testable claims -> explicit falsifiers -> validation levels -> per-object earn-its-place table -> "post-hoc explains everything" objection response -> "just good systems engineering" objection response (formal) -> unfalsifiability risk acknowledgment.
Source sections: v0.2 S14 (lines 2904-3179).
Visual/table placement: None expected.
Status: NOT YET DRAFTED
-->

---

## 10. The Blend Has Roots

<!--
Arc responsibility: Intellectual lineage -> what is borrowed -> what is synthesized -> "blend, not invention" -> "over-cite by design" -> lineage table.
Source sections: v0.2 S15 (lines 3180-3369).
Visual/table placement: New: related-work lineage table (tradition -> contribution -> what this paper adds -> key citation).
Status: NOT YET DRAFTED
-->

---

## 11. Build Better Landscapes

<!--
Arc responsibility: 3-4 genuinely new implications (product evaluation, governance/regulation, organizational learning, research agenda) -> one forward-looking closing move. No recap of body arguments.
Source sections: v0.2 S16 (lines 3370-3517), v0.2 S17 (lines 3518-3673).
Visual/table placement: Full-framework loop (light echo from S1, not re-explained).
Status: NOT YET DRAFTED
-->

---

## Appendix A: The Decision Topography Interview

<!--
Arc responsibility: Practical starting point -> 23 questions -> 4 phases -> three-part structure. Add brief facilitation guidance. Add minimal-interview variant table.
Source sections: v0.2 Appendix A (lines 3674-4298).
Visual/table placement: New: minimal interview variant (8-10 question subset table).
Status: NOT YET DRAFTED
-->

---

## References

<!--
Source sections: v0.2 References (lines 4299-4369). Plus new citations per citation workstream.
Status: NOT YET DRAFTED
-->
