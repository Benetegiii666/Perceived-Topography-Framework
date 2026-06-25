# Perceived Topography in Human-Agent Systems: Reasoning-State Preservation as a Design Theory for Governable Agentic Action

**Alternative title:** From Context to Reasoning State: Perceived Topography as a Framework for Human-Agent System Design

**Version:** Academic v0.1 — Scaffold only
**Date:** 2026-06-24
**Status:** Section scaffold with intent notes and placeholders. No full prose drafted.
**Source:** Derived from frozen keystone paper `PAPER_v1.0_WORKING.md`. The frozen paper remains conceptual authority. This academic version may compress, restructure, and formalize but may not silently alter core framework concepts.
**Boundary rule:** If the academic conversion reveals a conceptual conflict with the frozen paper, HLD, or build artifacts, document it as a fault line under Protocol #1 rather than resolving it silently.

---

## Abstract

**Status:** Placeholder — to be drafted.

**Intent:** Academic abstract. State problem, gap, framework, method, contribution, and limits. Remove manifesto tone from v1.0 abstract. Retain the core claim.

**Required elements:**

1. Agentic systems increasingly act through memory, tools, retrieval, and workflow integration.
2. Current approaches focus on model capability, prompting, retrieval, tool access, or containment — necessary but insufficient.
3. These approaches under-describe the constructed operating context from which agent action becomes sufficient.
4. This paper introduces the Perceived Topography Framework: a design theory for diagnosing and shaping the constructed information-and-action landscapes through which human-agent systems reason, act, fail, and learn.
5. The framework defines optimizer state, information topography (five dimensions), gradients, sufficiency, and reasoning-state transitions.
6. A constructed healthcare marketing scenario illustrates the framework through comparative stress test — same task, same artifacts, different architecture.
7. The paper offers a pre-empirical design vocabulary, falsifiable claims, and a research agenda — not empirical validation.

**Tone target:** Formal but readable. Not a manifesto. Not dry.

**Source material:** `PAPER_v1.0_WORKING.md` lines 9-17, adapted.

---

## Epistemic Status

**Status:** Placeholder — adapt from v1.0.

**Intent:** Retain this section. It is a credibility asset. State clearly: conceptual design theory, not empirical study. Constructed stress test, not field study. Pre-empirical vocabulary with falsifiable claims.

**Source material:** `PAPER_v1.0_WORKING.md` lines 22-33, tightened.

**Editorial note:** This section may be shortened to a single paragraph for some venues. Retain the full version as the default.

---

## 1. Introduction: The Reliability Problem Has Moved

**Status:** Accepted — v0.3 with review notes applied
**Review status:** Accepted per `SECTION_1_REVIEW_v0.3_2026-06-24.md`. All 5 pass criteria met. Three review notes applied: premature sufficiency genealogy (Simon 1955), Lynch/Yao citation split, contribution enumeration varied.
**Prior versions:** v0.1 (27 AI flags, Voice 2/5), v0.2 (11 AI flags, Voice 3.5-4/5), v0.3 (5 AI flags, Voice 4/5). Reviews: `SECTION_1_REVIEW_2026-06-24.md`, `SECTION_1_REVIEW_v0.2_2026-06-24.md`, `SECTION_1_REVIEW_v0.3_2026-06-24.md`.

**Citation note:** Three anchoring citations added per v0.2 review guidance. Full citation treatment in Section 2.

---

AI agents are increasingly evaluated as actors: systems that can pursue goals, use tools, preserve state, and move through multi-step environments. [Yao et al., 2022] When these systems fail, the failure often feels different from an ordinary model error. A static model may hallucinate a citation. An agent may hallucinate, send the message, update the record, and leave the human team to discover later that the action rested on unsupported ground. [Lynch et al., 2025]

The natural reaction is to ask what is wrong with the agent.

That question is necessary. It is also incomplete.

A model does not need inner malice to cause harm. It only needs a goal, an action space, imperfect constraints, and a path through the environment that makes the harmful action appear useful, available, or sufficient. The behavior may look strategic, deceptive, careless, or overconfident. But before we reach for psychological explanations, we should ask a more basic systems question: what landscape did we ask the agent to move through?

This paper proposes that we can describe that landscape.

A useful image is simple. When a marble rolls downhill, we do not explain its motion only by studying the marble. We look at the slope. Human-agent systems should be studied in the same way. Their behavior emerges not only from what the model can do, but from the environment of visible information, reachable tools, represented constraints, confidence signals, and connected consequences through which the system moves.

This paper calls that environment a **perceived topography**: the information-and-action landscape made available to an optimizer-like system at the moment it reasons and acts. The term "optimizer-like" is functional, not psychological. By optimizer, I do not mean a conscious entity with intentions. I mean a system that selects actions in relation to a goal, under constraints, using some interpretation of the situation.

The contribution is not the claim that system design matters. That is already well established. The contribution is a diagnostic vocabulary for the conditions under which action becomes sufficient before reasoning warrants it.

This distinction matters because many current interventions focus on containment. Permissions, approval gates, sandboxes, and monitoring all ask where the system should not go. These controls are necessary, especially when systems can act outside the conversation. But containment alone does not explain why the unsafe path became attractive, why the safer path was harder to find, or why a policy that existed somewhere failed to shape the decision.

A second response is to add context. Retrieval-augmented systems can supply documents, policies, and prior examples, and this improves many outputs. [Lewis et al., 2020] But context is not the same as reasoning state. Context may help a system answer. Reasoning state explains why the system acted as it did.

A context layer can retrieve a policy. A reasoning-state layer must make the policy matter at the moment of decision. That difference is architectural, not cosmetic. It is the difference between information that exists and information that becomes behaviorally effective.

This is the gap the Perceived Topography Framework addresses. It treats human-agent behavior as movement through a constructed landscape of information surfaces, affordances, constraints, confidence, and consequence. Information only shapes behavior when it can be noticed, reached, interpreted, trusted, and connected to the decision where it should exert force.

The framework describes this landscape through five dimensions: **Visibility, Accessibility, Representation, Confidence, and Connectivity**. These are not offered as a complete ontology of all factors that influence agent behavior. They are a minimum viable diagnostic set. A dimension earns its place only if changing it would lead to a different diagnosis, intervention, or expected outcome.

The framework also introduces **premature sufficiency** as a recurring failure pattern. The concept extends satisficing [Simon, 1955] — the observation that agents act when a solution is good enough rather than optimal — by focusing on the conditions under which "good enough" is reached too early. Premature sufficiency occurs when a system acts before the relevant evidence, uncertainty, policy, consequence, or human confirmation has exerted enough force on the decision. The system does not merely lack information. It stops moving too soon.

This pattern can appear in different kinds of failures. In hallucination, a fluent answer may become sufficient before it is grounded. In unsafe tool use, an available action may become sufficient before risk or approval has been resolved. These failures differ in consequence and mitigation. The point is not to collapse them. The point is to notice that both can involve the same motion structure: goal pressure, weak counterpressure, misplaced confidence, and a low-friction path to action.

A human-agent system therefore needs more than better prompts, larger context windows, or stricter fences. It needs a way to preserve the reasoning state from which action became justified. The system should retain the working goal, the governing constraint, the interpretation that made action attractive, the uncertainty that remained, and the reason investigation stopped. Without that structure, the organization may keep the artifact while losing the why.

This loss is familiar in human organizations. Teams store documents but lose decisions. They remember outcomes but forget assumptions. They correct an artifact without changing the reasoning that produced the error. The next team retrieves the old material and repeats the same mistake under a new label. The organization appears to have memory but behaves as if it does not. [Walsh & Ungson, 1991; Markus, 2001]

Agentic systems can accelerate this pattern. They can retrieve more, synthesize faster, and act with less friction. But if they inherit an information landscape where policies are disconnected, evidence boundaries are weak, prior failures are hard to reuse, and uncertainty has no legitimate action path, they may become faster at reaching the wrong kind of sufficiency.

The paper makes four contributions.

It defines **perceived topography** as the constructed information-and-action landscape through which human-agent systems reason and act — a construct that helps distinguish information that merely exists from information that becomes behaviorally effective.

It draws a hard line between **context and reasoning state**. Reliable and learnable agentic behavior requires preservation of structured reasoning transitions, not only retrieval of artifacts.

It offers a diagnostic account of **premature sufficiency** — how failures emerge when goal pressure, weak grounding, misplaced confidence, and low-friction action paths allow the system to act before the right uncertainty or constraint has shaped the decision.

And it proposes a **research and design agenda** for evaluating human-agent systems through reasoning-state preservation, topography perturbation, governance salience, human confirmation, and model-update quality.

The paper is intentionally bounded: perceived topography does not replace alignment, containment, retrieval, evaluation, governance, or human oversight; it does not guarantee safe outcomes; and it does not explain every agent failure. Rather, it argues that these existing approaches remain incomplete without a way to describe and shape the perceived environment from which action becomes sufficient.

The paper proceeds from the context/reasoning-state distinction through the framework's dimensions and motion model, then into reasoning-state architecture, Discovery, a constructed healthcare stress test, boundaries, disconfirmation conditions, and a research agenda.

The practical question is therefore not only: how do we prevent agents from taking harmful actions? It is also: how do we design the landscape so that grounded, policy-aware, human-beneficial behavior becomes easier to reach than the merely fluent, available, or locally sufficient path?

---

**Scaffold intent notes (retained for review reference):**

**Source:** ChatGPT v0.3 draft, provided by Benet 2026-06-24.

**v0.2 → v0.3 changes applied:**

- Roadmap compressed from 10 template sentences to one sentence
- Context/reasoning-state triplet reduced to one strong policy example + architectural framing
- Three citation anchors added: [Lynch et al., 2025; Yao et al., 2022], [Lewis et al., 2020], [Walsh & Ungson, 1991; Markus, 2001]
- Containment catalog reduced from 6 items to 4
- Context catalog restructured into flowing prose ("documents, policies, and prior examples")
- Bounding paragraph compressed from three "It does not claim" sentences to one semicolon-joined sentence
- Reasoning-state list restructured ("The system should retain..." instead of "That state includes...")
- "preserve state" replaces "remember prior interactions" in opening (more precise)
- Closing question remains as final rhetorical beat (after compressed roadmap)

**Elements preserved from v0.2:**

- Marble/slope metaphor
- "This paper proposes that we can describe that landscape" thesis one-liner
- "A model does not need inner malice to cause harm" (frozen paper wording restored)
- First-person "I" for optimizer definition
- "The contribution is not the claim that system design matters" preemption
- Four-contribution enumeration
- Bounding paragraph (compressed)
- Five-dimension introduction with "minimum viable diagnostic set"
- Premature sufficiency introduction
- Organizational learning paragraphs
- Agentic acceleration paragraph
- Closing question

---

## 2. Related Work and Theoretical Positioning

**Status:** Placeholder — to be drafted. This is the largest structural change from v1.0.

**Intent:** Move the current Section 10 ("The Blend Has Roots") earlier and make it more formally structured. In academic papers, related work belongs near the front so readers can position the contribution before encountering the full framework.

**Required positioning against five literatures:**

### 2.1 LLM Agents and Reasoning-Action Systems

- ReAct, tool use, agent architectures, memory/planning/reflection/orchestration
- Position: PTF does not propose a new agent architecture. It proposes a design theory for the landscape agents move through.

### 2.2 Agent Evaluation and Realistic Task Environments

- AgentBench, WebArena, SWE-bench, OSWorld, TheAgentCompany
- Position: These evaluate agent capability. PTF diagnoses the operating context that shapes whether capability translates to reliable action.

### 2.3 AI Safety and Governance

- Tool misuse, memory risks, autonomy-induced security risks, human oversight, constrained action
- Position: PTF complements containment with environmental design. Safety is not only about what the agent can do; it is about what the landscape makes sufficient.

### 2.4 Human-Computer Interaction and Mixed-Initiative Systems

- Human confirmation, automation bias, uncertainty representation, affordances
- Position: Discovery (RIPC) is a mixed-initiative interaction pattern. The framework draws on affordance theory and Horvitz's mixed-initiative principles.

### 2.5 Organizational Learning and Knowledge Reuse

- Organizational memory vs. learning, postmortems, model update, repeated organizational mistakes
- Position: PTF distinguishes storing artifacts from preserving reasoning-state transitions. Learning requires preserved prediction error and evidence-supported model change, not just storage.

**Gap statement:**

> Existing work explains agent components, risks, benchmarks, and controls. Less developed is a vocabulary for the constructed information-and-action landscape through which an agent's reasoning becomes sufficient for action.

**Source material:** `PAPER_v1.0_WORKING.md` Section 10 (lines ~2098+), plus references section. Citations to add: ReAct (Yao et al.), AgentBench, WebArena, SWE-bench, TheAgentCompany, and other agent evaluation benchmarks not yet in bibliography.

**Citation backlog:** This section will require significant new citations. Mark as [CITE NEEDED] during drafting.

---

## 3. From Context to Reasoning State

**Status:** Placeholder — to be drafted from v1.0 Sections 2 and 3.

**Intent:** Combine the strongest parts of "Context Does Not Preserve the Why" and "Optimizer State and Perceived Topography" into a single section that makes the core conceptual move.

**Required argument arc:**

1. Context is available information — documents, data, policies, artifacts.
2. Reasoning state is the structured condition from which action becomes justified — goal, interpretation, constraints, premises, confidence, sufficiency rationale.
3. The gap: organizations store context but not reasoning state. The next cycle inherits artifacts without inheriting the judgment that produced them.
4. Perceived topography is the landscape that makes some reasoning paths easier, more trusted, more connected, or more sufficient than others. It is the design surface.

**Formal definitions to introduce (crisp, not over-explained):**

- Information surface
- Optimizer state (goal, policy, interpretation)
- Perceived topography
- Gradient
- Sufficiency
- Reasoning-state transition

**What to reduce from v1.0:**

- Extended discursive explanation of why context is not enough (the point should land in 2-3 paragraphs, not 8)
- Repeated contrast between context and reasoning state after the distinction is established

**Source material:** `PAPER_v1.0_WORKING.md` Sections 2 and 3.

---

## 4. Perceived Topography: Definitions and Dimensions

**Status:** Placeholder — to be drafted from v1.0 Section 3 (dimensions material).

**Intent:** Give the five dimensions their own section. They are one of the paper's best assets and deserve formal treatment.

**Five dimensions:**

| Dimension | Definition | Diagnostic Question | Failure Mode | Design Intervention |
|---|---|---|---|---|
| **Visibility** | Can this be perceived? | What relevant information exists but is not visible to the system at decision time? | Hidden risk: the gradient exists but exerts no behavioral force. | Increase visibility of the relevant surface. |
| **Accessibility** | Can this be reached? | What information is visible but too costly, slow, or difficult to retrieve? | Friction barrier: the information exists and is visible but does not reach the decision. | Reduce retrieval cost; improve access paths. |
| **Representation** | How is this expressed? | Is the information expressed in a form the system can interpret and act on? | Misread signal: the information arrives but is misinterpreted. | Improve representation; structure for interpretation. |
| **Confidence** | How trustworthy is this? | How much weight should the system give this information? | False confidence or unwarranted doubt: the system over- or under-trusts. | Surface confidence metadata; distinguish evidence from assertion. |
| **Connectivity** | What is this connected to? | Is this information connected to the decision, policy, action, or consequence it should influence? | Disconnected policy: the constraint exists but does not shape the decision. | Connect the surface to the decision point. |

**Dimension Admission Matrix:** Preserve this. It gives the paper discipline and prevents framework sprawl.

**Source material:** `PAPER_v1.0_WORKING.md` Section 3 (dimensions) and Section 4 (failure modes).

---

## 5. Gradients, Motion, and Premature Sufficiency

**Status:** Placeholder — to be drafted from v1.0 Section 4.

**Intent:** Formalize the motion model and the premature sufficiency claim.

**Core sequence:**

> Attraction → Investigation → Sufficiency → Action

**Key contribution:** The claim that different failures can share a motion pattern — the system acts when a path becomes sufficient before the right uncertainty, evidence, policy, or consequence has become behaviorally effective.

**Careful framing for hallucination and unsafe tool action:**

- They differ in consequence.
- They differ in mitigation.
- But they can share a structural pattern: premature sufficiency.
- Do not overclaim equivalence. Claim structural similarity, not identity.

**Three failure classes (from v1.0):**

1. Hidden Risk — gradient exists, not visible
2. Misread Signal — gradient visible, misinterpreted
3. Attention Failure — gradient visible and interpreted, but other gradients exert stronger pressure

**Source material:** `PAPER_v1.0_WORKING.md` Section 4.

---

## 6. Reasoning-State Architecture

**Status:** Placeholder — to be drafted from v1.0 Sections 6, 7, and 8.

**Intent:** Combine learning, discovery, and architecture into a cleaner presentation. The v1.0 paper presents these across three sections with significant overlap. The academic version should present the architecture as a unified design.

**Six reasoning objects (Table 7 from v1.0):**

1. Optimizer State — what was the system trying to do?
2. Premise Stack — why did the system expect this to work?
3. Decision State — what was chosen, rejected, and why was it sufficient?
4. Investigation Trace — how was uncertainty reduced?
5. Learning Event — where did reality contradict the model?
6. Model Update Object — what reusable change should shape future reasoning?
7. Modified Optimizer State — (derived, not stored)

**The chain:**

> Optimizer State → Premise Stack → Decision State → Investigation Trace → Learning Event → Model Update Object → Modified Optimizer State

**Key claim:**

> A reasoning-state layer preserves the transition from goal and interpretation to action, outcome, contradiction, and future update.

**Maturity model (Table 8 from v1.0):**

| Stage | Capability | Failure if stopped here |
|---|---|---|
| 0. Unstructured | Scattered documents, chats, decisions | Every cycle starts cold |
| 1. Context Layer | Artifacts indexed and retrievable | System finds information but not reasoning state |
| 2. Reasoning-State Capture | Reasoning objects preserved | Reasoning survives action but outcomes may not update behavior |
| 3. Learning Layer | Learning events and MUOs connect outcomes to model change | System can learn but Discovery and governance may not adapt |
| 4. Adaptive Loop | Prior reasoning, discovery patterns, and governance shape future decisions | Must now manage conflict, staleness, overgeneralization |

**Editorial note:** This section must avoid sounding like a software requirements document. Define architecture as a design theory, not a system spec. The HLD exists for implementation detail.

**Source material:** `PAPER_v1.0_WORKING.md` Sections 6, 7, 8. Tables 7 and 8.

---

## 7. Discovery and Human Confirmation

**Status:** Placeholder — to be drafted from v1.0 Section 7.

**Intent:** Narrower than v1.0's treatment. Focus on the core interaction pattern and its academic significance.

**Core formalization:**

> Discovery is the process by which provisional system interpretations are exposed to human confirmation before becoming preserved reasoning state.

**Core loop:**

> Retrieve → Infer → Propose → Confirm

**Academic value:** This connects the framework to mixed-initiative systems (Horvitz 1999), affordance theory (Gibson 1979, Norman 1988), and automation bias research (Parasuraman & Riley 1997, Lee & See 2004).

**Key distinction from v1.0 Table 6:**

| Ordinary intake asks | Discovery additionally asks | Why the answer changes future reasoning |
|---|---|---|
| What do you want produced? | What decision should this output support? | System distinguishes completion from usefulness. |
| Who is the audience? | What do we believe about this audience, and how confident are we? | Audience claims become bounded interpretations. |
| What constraints apply? | Which constraints must interrupt action if unresolved? | Policy becomes behaviorally meaningful. |
| What does success look like? | What outcome would prove our premise wrong? | Learning has a prediction to compare against. |

**What to compress from v1.0:**

- Reduce the extended explanation of each RIPC step (the concept lands quickly; v1.0 over-explains)
- Reduce the multiple examples (keep the healthcare campaign example; cut redundant examples from other domains)

**Source material:** `PAPER_v1.0_WORKING.md` Section 7. Table 6. Figure 6.

---

## 8. Constructed Stress Test: Healthcare Marketing Campaign

**Status:** Placeholder — to be drafted from v1.0 Section 5.

**Intent:** Keep the healthcare scenario but make it shorter and more explicitly methodological.

**Required framing:**

> This is not a case study. It is a constructed comparative stress test. It holds the business assignment and available organizational materials constant, then compares two information architectures: context-only and reasoning-state.

**Compression target:** Reduce by 30-40% from v1.0.

**Required comparison (three-column from v1.0):**

| Aspect | Context-only workflow | Reasoning-state workflow |
|---|---|---|
| Available information | Same | Same |
| Goal representation | Implicit in request | Explicit optimizer state |
| Assumption tracking | None | Premise stack |
| Claim governance | Policy exists but disconnected | Policy connected to claim at decision point |
| Sufficiency condition | Draft sounds professional | Evidence, policy, and uncertainty checked |
| Outcome learning | Campaign report stored | Prediction error identified, model update created |

**What to cut:**

- Extended narrative buildup
- Repeated restatement of the same distinction
- Examples that illustrate points already made

**What to keep:**

- The readmissions claim as the key failure point
- The workflow-burden/buying-readiness distinction as the premise failure
- The comparison table showing same artifacts, different outcomes

**Source material:** `PAPER_v1.0_WORKING.md` Section 5.

---

## 9. Boundaries, Objections, and Disconfirmation Conditions

**Status:** Placeholder — to be drafted from v1.0 Section 9.

**Intent:** This is a major credibility asset. Keep it. It should answer:

- What the framework does not claim
- Where the metaphor may fail
- When reasoning-state capture creates burden rather than value
- When governance becomes illegitimate or manipulative
- When preserving reasoning becomes surveillance
- When the framework becomes post-hoc storytelling
- What evidence would weaken or falsify the framework

**Disconfirmation conditions (Table 9 from v1.0):**

| Claim | What would support it | What would weaken it |
|---|---|---|
| Context is not reasoning state | Reasoning-state systems outperform context-only on reuse, governance, learning | Context-only performs just as well |
| Topography dimensions diagnose differently | Different dimensions lead to different interventions | Dimensions are interchangeable |
| Discovery improves starting state | Infer-confirm reduces ambiguity and rework | Discovery adds burden without improving quality |
| Model updates improve learning | MUOs reduce repeated failures more than postmortems | MUOs are not retrieved, trusted, or used |
| Framework predicts, not just explains | Identifies likely failures before action | Only classifies after the fact |
| Reasoning objects earn their place | Removing an object degrades quality | Removing an object makes no difference |

**Risks introduced by the framework:**

- False precision
- Authority conflict
- Surveillance and manipulation
- Stale reasoning
- Policy laundering
- Automation bias
- Metaphor drift

**Source material:** `PAPER_v1.0_WORKING.md` Section 9. Table 9.

---

## 10. Research Agenda and Evaluation Methods

**Status:** Placeholder — NEW SECTION (not in v1.0).

**Intent:** This section makes the paper publishable. It shows the framework wants to be tested, not believed.

**Proposed evaluation paths:**

### 10.1 Comparative Workflow Studies

Context-only agent vs. reasoning-state agent on the same task, same artifacts, different architecture. Measure: reuse quality, governance reliability, error recovery, learning transfer.

### 10.2 Reasoning-State Reuse Tests

Can future agents use prior premise stacks and model updates to avoid repeating errors? Measure: premise-failure recurrence rate across cycles.

### 10.3 Governance Salience Tests

Does connecting policy to claim/action type at decision time reduce unsafe or unsupported outputs? Measure: policy-violation rate with and without governance connectivity.

### 10.4 Premature Sufficiency Tests

Can evaluators identify where action became sufficient too early using the framework's diagnostic vocabulary? Measure: inter-rater reliability on premature sufficiency classification.

### 10.5 Topography Perturbation Tests

Alter visibility, accessibility, representation, confidence, or connectivity and observe behavioral change. Measure: whether dimension-specific perturbations produce dimension-specific behavioral shifts.

### 10.6 Human-Agent Confirmation Studies

Does infer-confirm Discovery improve intent capture without excessive user burden compared with blank-form intake or silent inference? Measure: intent accuracy, user burden, rework rate.

**Source material:** New. Draws on disconfirmation conditions from v1.0 Section 9.

---

## 11. Conclusion: Designing Better Perceived Landscapes

**Status:** Placeholder — to be drafted from v1.0 Section 11.

**Intent:** Keep the "build better landscapes" energy but make it academically restrained.

**Required closing contribution statement:**

> Agentic reliability is not only a property of model capability, prompt quality, or tool restriction. It is also a property of the perceived landscape from which action becomes sufficient. The Perceived Topography Framework provides a vocabulary for diagnosing that landscape, a reasoning-state architecture for preserving its transitions, and a research agenda for testing whether better-shaped landscapes produce more governable, learnable human-agent systems.

**Source material:** `PAPER_v1.0_WORKING.md` Section 11.

---

## References / Citation Backlog

**Status:** Existing references from v1.0 preserved below. New citations needed for Section 2 (Related Work) marked in citation backlog.

### Existing References (from frozen v1.0)

Aamodt, A., & Plaza, E. (1994). Case-based reasoning. *AI Communications*, *7*(1), 39–59.

Alavi, M., & Leidner, D. E. (2001). Knowledge management and knowledge management systems. *MIS Quarterly*, *25*(1), 107–136.

Amershi, S., et al. (2019). Guidelines for human-AI interaction. *CHI '19*.

Argyris, C., & Schon, D. A. (1978). *Organizational learning*. Addison-Wesley.

Bates, M. J. (1989). Browsing and berrypicking. *Online Review*, *13*(5), 407–424.

Cyert, R. M., & March, J. G. (1963). *A behavioral theory of the firm*. Prentice-Hall.

Dennett, D. C. (1987). *The intentional stance*. MIT Press.

Endsley, M. R. (1995). Situation awareness in dynamic systems. *Human Factors*, *37*(1), 32–64.

Gibson, J. J. (1979). *The ecological approach to visual perception*. Houghton Mifflin.

Guo, C., et al. (2017). On calibration of modern neural networks. *ICML*, 1321–1330.

Horvitz, E. (1999). Mixed-initiative user interfaces. *CHI '99*, 159–166.

Howard, R. A. (1966). Information value theory. *IEEE Trans. Systems Science*, *2*(1), 22–26.

Huang, L., et al. (2023). Hallucination in large language models. *arXiv:2311.05232*.

Ji, J., et al. (2023). AI alignment: A comprehensive survey. *arXiv:2310.19852*.

Kadavath, S., et al. (2022). Language models (mostly) know what they know. *arXiv:2207.05221*.

Kuhlthau, C. C. (1991). Inside the search process. *JASIS*, *42*(5), 361–371.

Lee, J. (1997). Design rationale systems. *IEEE Expert*, *12*(3), 78–85.

Lee, J. D., & See, K. A. (2004). Trust in automation. *Human Factors*, *46*(1), 50–80.

Lewis, P., et al. (2020). Retrieval-augmented generation. *NeurIPS*, *33*, 9459–9474.

Lynch, A., et al. (2025). Agentic misalignment. Anthropic Research.

March, J. G., & Simon, H. A. (1958). *Organizations*. Wiley.

Markus, M. L. (2001). Toward a theory of knowledge reuse. *JMIS*, *18*(1), 57–93.

Maynez, J., et al. (2020). Faithfulness and factuality in abstractive summarization. *ACL*, 1906–1919.

Menick, J., et al. (2022). Teaching language models to support answers with verified quotes. *arXiv:2203.11147*.

Moreau, L., & Missier, P. (2013). PROV-DM: The PROV data model. W3C Recommendation.

Ng, A. Y., et al. (1999). Policy invariance under reward transformations. *ICML*, 278–287.

Norman, D. A. (1988). *The design of everyday things*. Basic Books.

Parasuraman, R., & Riley, V. (1997). Humans and automation. *Human Factors*, *39*(2), 230–253.

Pirolli, P., & Card, S. (1999). Information foraging. *Psychological Review*, *106*(4), 643–675.

Russell, S., & Norvig, P. (2020). *Artificial intelligence: A modern approach* (4th ed.). Pearson.

Russell, S., & Wefald, E. (1991). *Do the right thing*. MIT Press.

Shanahan, M., et al. (2023). Role play with large language models. *Nature*, *623*, 493–498.

Simon, H. A. (1955). A behavioral model of rational choice. *QJE*, *69*(1), 99–118.

Walsh, J. P., & Ungson, G. R. (1991). Organizational memory. *AMR*, *16*(1), 57–91.

Weick, K. E. (1995). *Sensemaking in organizations*. Sage.

### Citation Backlog (needed for Section 2)

| Citation Needed | Section | Topic |
|---|---|---|
| Yao, S., et al. (2023). ReAct. | 2.1 | LLM agent reasoning-action |
| [CITE NEEDED] AgentBench | 2.2 | Agent evaluation |
| [CITE NEEDED] WebArena | 2.2 | Agent evaluation |
| [CITE NEEDED] SWE-bench | 2.2 | Agent evaluation |
| [CITE NEEDED] OSWorld | 2.2 | Agent evaluation |
| [CITE NEEDED] TheAgentCompany | 2.2 | Agent evaluation |
| [CITE NEEDED] LangChain / agent orchestration frameworks | 2.1 | Agent architecture |
| [CITE NEEDED] Tool use and function calling (Schick et al., Toolformer) | 2.1 | Tool use |
| [CITE NEEDED] Agentic memory and reflection (Generative Agents, Park et al.) | 2.1 | Agent memory |
| [CITE NEEDED] RLHF / Constitutional AI / alignment techniques | 2.3 | Safety and governance |

---

## Figures

**Status:** Placeholder — to be determined.

**Figure 8** (workshop control console / hero asset) is locked and should not be modified.

Figures from v1.0 that should be adapted or preserved for the academic version:

| Figure | Content | Disposition |
|---|---|---|
| Fig 1 | Fear to landscape design | Adapt for academic tone |
| Fig 2 | Context vs. reasoning state | Preserve — strong |
| Fig 3 | Optimizer in topography | Preserve |
| Fig 4 | Motion and premature sufficiency | Preserve |
| Fig 5 | Learning is model change | Preserve |
| Fig 6 | Runtime Discovery loop | Preserve |
| Fig 7 | Reasoning architecture: six objects | Preserve — essential |
| Fig 8 | Workshop control console (hero) | Locked — do not modify |

---

## No-Edit Confirmation

- Frozen paper (`PAPER_v1.0_WORKING.md`) edited: **No**
- Figure 8 modified: **No**
- Figures modified: **No**
- References modified: **No** (existing references copied for reference; new citations added to backlog only)
- Executive Brief v1.0 edited: **No**
- Build Discovery Guide v1.0 edited: **No**
- HLD v1.0 content edited: **No**
- Core framework concepts altered: **No** (all concepts preserved per Required Preservation list)
