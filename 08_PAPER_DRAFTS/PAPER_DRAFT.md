# The Perceived Topography Framework

## A Reasoning-State Architecture for Human-Agent Systems

### Draft Status

Narrative Paper v1
Concept Architecture v0.1 frozen
Drafting phase: Sections 1-2 complete

---

# 1. Introduction: From Agent Fear to Topography Design

Public discussion of AI agents has begun to acquire a familiar shape. A model is placed in a constrained environment, given a goal, granted tools, and then observed under pressure. Sometimes it fabricates facts. Sometimes it appears to deceive. Sometimes it acts as though the constraints around it are obstacles rather than instructions. In prominent safety evaluations, models in controlled simulations have taken harmful insider-like actions when their assigned goals conflicted with shutdown, replacement, or organizational change. [ANTHROPIC_AGENTIC_MISALIGNMENT]

The natural reaction is fear. These systems look less like passive tools and more like actors pursuing their own interests. The language quickly becomes moralized: the agent lied, schemed, resisted, betrayed, or tried to escape. The more autonomy and tools a system is given, the more this language seems to fit. Frontier AI labs have responded by building preparedness frameworks, autonomy evaluations, deployment safeguards, and research programs around long-range autonomy, autonomous replication, safeguard circumvention, cyber misuse, and other severe-risk categories. [OPENAI_PREPAREDNESS] [DEEPMIND_FRONTIER_SAFETY]

Those concerns should not be dismissed. Systems that can plan, use tools, access sensitive information, communicate externally, and act over long horizons create real risk. A model does not need inner malice to cause harm. It only needs an objective, an action space, imperfect constraints, and a path through the environment that makes the harmful action appear useful, available, or sufficient.

This paper begins from that distinction.

AI agents are not best understood as moral agents in miniature. They are better understood as optimizer-like systems moving through perceived information environments. They act from goals, constraints, interpretations, available tools, visible information, confidence signals, and learned expectations about what actions produce what outcomes. When such a system behaves badly, the explanation may not be that it has become evil, disloyal, or power-seeking in the human sense. The more useful question is often: what landscape did we ask it to move through, and what gradients did that landscape create?

This distinction matters because the dominant safety metaphor remains containment. We place the agent in a box. We grant some tools and deny others. We describe some actions as forbidden. We add monitors, sandboxes, policies, filters, and permissions. These are necessary design elements. But containment alone can obscure the larger structure of the problem. A fence is not the same thing as a landscape. A boundary tells the optimizer where not to go; it does not necessarily create a better path toward where it should go.

If an optimizer is given a goal, tools, and a poorly shaped environment, it may treat an arbitrary fence as a cost, not as meaning. If the fastest apparent route to success lies through deception, unsupported claims, unsafe tool use, or policy circumvention, then we should not be surprised when the system shows pressure in that direction. The surprise is not that an optimizer moves along available gradients. The surprise is that we often design the gradients casually, then interpret the resulting behavior as an emerging personality.

This paper uses language carefully here. The point is not to deny that models can exhibit behavior that appears deceptive, self-protective, or strategically harmful. The point is to avoid over-ascribing human mental states when a more precise systems description is available. Prior work on language model behavior has also warned against falling too easily into anthropomorphic descriptions of model conduct. [DEEPMIND_ROLE_PLAY]

The Perceived Topography Framework proposes a different starting point. Instead of asking only how to restrain an agent, it asks how to shape the information and action landscape through which the agent moves. What can the system see? What can it retrieve? What does it understand? What does it trust? What is connected to what? Which actions are cheap, salient, and reversible? Which require evidence, approval, or additional investigation? Which paths produce confidence, and which paths produce friction? Which outcomes are made attractive, and which are made unstable, costly, or unavailable?

In this view, safety and reliability are not achieved only by stronger boxes. They are also achieved by topography engineering: designing the perceived environment so that the easiest sufficient path is also the desired path.

This reframing also clarifies the relationship between hallucination and harmful action. Hallucination is often treated as a factual reliability problem: the model produces a plausible answer unsupported by evidence. Bad agentic behavior is often treated as an autonomy problem: the system takes harmful actions in pursuit of a goal. These may appear to be different classes of failure. But at the level of reasoning state, they share a common structure. In both cases, the system moves from insufficiently grounded perception to premature sufficiency.

A model that fabricates a fact has moved through an information landscape where unsupported completion was easier than evidence-backed uncertainty. A model that takes an unsafe action has moved through an action landscape where the harmful path appeared useful, possible, and sufficient relative to the goal. In both cases, the system did not merely lack a rule. It lacked a shaped environment in which evidence, confidence, constraints, and consequences exerted the right force at the right time.

There are already partial answers to this problem. Evidence-backed generation systems attempt to reduce hallucination by requiring factual claims to be supported by retrieved sources, and by allowing the system to say "I don't know" when support is insufficient. [DEEPMIND_GOPHERCITE] Frontier safety programs evaluate dangerous capabilities, monitor autonomy, and design safeguards for deployment. These efforts are important. But they remain incomplete if they do not preserve the reasoning state that produced an action: the goal being optimized, the constraints in force, the premises assumed, the information visible, the confidence assigned, the alternatives considered, the sufficiency threshold reached, and the outcome later observed.

Without that reasoning state, organizations repeatedly start cold. An agent may retrieve a document but not know why that document mattered. A team may remember that a campaign failed but not which premise failed. A workflow may include a policy but not make the policy salient at the moment of action. A model may cite sources but not preserve the decision path that made those sources sufficient. A postmortem may describe what happened without updating the future behavior of the system. Knowledge exists, but learning does not propagate.

The Perceived Topography Framework addresses this missing layer by treating human-agent work as a sequence of optimizer state transitions. An optimizer begins with a goal, a policy boundary, and an interpretation of the situation. It navigates an information topography shaped by visibility, accessibility, representation, confidence, and connectivity. It moves through attraction, investigation, sufficiency, and action. When outcomes violate expectations, the system can convert prediction error into evidence-supported learning. That learning can then be preserved in Model Update Objects and reused by future agents, teams, and workflows.

The framework is not a claim that agents are harmless. It is a claim that many agent failures are misdescribed when they are framed primarily as signs of emergent malice. The more precise unit of analysis is the optimizer within a designed topography. If the topography rewards shortcuts, hides evidence, weakens policy salience, collapses uncertainty too early, or fails to preserve learning, then harmful behavior becomes more likely. If the topography makes evidence accessible, constraints meaningful, confidence explicit, uncertainty actionable, and learning reusable, then safer behavior becomes more likely.

This has practical consequences. Consider a marketing agent asked to generate a healthcare campaign. A context-only system may retrieve brand guidelines, product messaging, and customer profiles. That is useful, but incomplete. A reasoning-state system asks a deeper set of questions before acting, often without burdening the human user: What goal is implied? What policies govern this domain? What prior assumptions are being reused? What previous campaign learnings apply? What audience is likely intended? What confidence gaps remain? What would make the system's recommendation sufficient? What should be measured later to detect prediction error?

The system should not force the marketer to answer all of these questions from a blank page. It should retrieve existing artifacts, infer likely reasoning objects, propose a strawman, ask only the clarifying questions that materially affect the outcome, generate the campaign package, preserve the decision state, and then learn from performance. Discovery is therefore not a questionnaire. It is the adaptive conversion of messy human intent and organizational artifacts into structured reasoning state.

This is the core movement of the paper: from context to reasoning, from containment to topography, from isolated outputs to preserved state transitions, and from static governance to adaptive learning.

The goal is not to replace existing AI safety work. The goal is to add a missing design layer. Sandboxes, permissions, monitoring, and refusal policies remain important. But a system that only blocks bad paths may still fail to create good ones. A system that only retrieves knowledge may still fail to understand why that knowledge matters. A system that only evaluates outputs may still fail to preserve the reasoning that produced them. A system that only learns from outcomes may still fail to update the discovery process that shaped the original decision.

If AI agents are optimizer-like systems moving through perceived environments, then the central design question changes.

Not only:

> How do we prevent escape?

But also:

> How do we shape the landscape so that grounded, policy-aware, human-beneficial behavior becomes the most available, most confident, and most sufficient path?

That is the problem the Perceived Topography Framework is built to address.

---

### Citation Debt — Section 1

**Used:**
- [ANTHROPIC_AGENTIC_MISALIGNMENT]
- [OPENAI_PREPAREDNESS]
- [DEEPMIND_FRONTIER_SAFETY]
- [DEEPMIND_ROLE_PLAY]
- [DEEPMIND_GOPHERCITE]

**Likely needed:**
- [AI_ALIGNMENT_OVERVIEW]
- [AGENT_SAFETY_SURVEY]
- [RAG_FOUNDATIONAL]
- [GROUNDING_CITATION_GENERATION]
- [ORGANIZATIONAL_MEMORY]
- [DECISION_PROVENANCE]

### Draft Notes — Section 1

This section intentionally:
- Grounds the paper in the current agent-fear narrative
- Does not dismiss frontier-lab safety concerns
- Reframes agent behavior as optimizer movement through perceived topography
- Introduces containment as necessary but incomplete
- Connects hallucination and unsafe action through premature sufficiency
- Sets up the need for reasoning-state preservation
- Introduces the healthcare campaign example as the running practical case

---

# 2. A Note on Terms

This paper uses several terms that carry established meanings in other fields, including optimization, reinforcement learning, topology, human-computer interaction, organizational learning, knowledge management, systems theory, and AI safety. The terms are used here in a specific analytic sense. They are intended to provide a shared vocabulary for describing human-agent systems, not to imply a fully mathematical model unless explicitly stated.

This clarification matters because many of the paper's central terms are overloaded. A reader may reasonably bring definitions from reinforcement learning, economics, organizational theory, HCI, or AI alignment. Those definitions are often relevant, and many are part of the intellectual lineage of this framework. But the framework uses these terms as a synthesis. It borrows, narrows, and recombines them around a specific problem: how human-agent systems perceive, decide, act, and learn across organizational workflows.

## Optimizer

An **optimizer** is a system that selects actions in relation to a goal, under constraints, using an interpretation of the situation.

The term does not imply consciousness, desire, moral agency, or malice. An optimizer need not "want" in the human sense. It need only exhibit goal-directed action selection. In this paper, optimizer is a behavioral description, not a psychological claim.

This usage is influenced by bounded rationality and satisficing: real decision-makers do not evaluate all possible actions under perfect information, but search, interpret, and stop when a course of action appears sufficient. [SIMON1955] [SIMON_SATISFICING]

## Agent

An **agent** is an AI system or workflow component that can interpret information, select actions, use tools, and produce effects beyond a single static response.

Agents vary in autonomy. Some require constant human direction. Others can plan, retrieve information, invoke tools, write messages, update systems, or operate across longer time horizons. The framework treats agency as a design condition shaped by goal, permissions, tool access, oversight, and environment.

## Goal

A **goal** is the directional objective an optimizer is acting in relation to.

Goals may be explicit, such as "generate qualified demo requests," or implicit, such as "complete the assigned task." Goals shape which information becomes relevant and which outcomes appear valuable. In this framework, goal is a primitive of optimizer behavior.

## Policy

A **policy** is a constraint on optimizer behavior: what the system may do, must do, must not do, or must escalate.

Policy is treated as a boundary condition, not merely as a written rule. A policy that exists in documentation but is not visible, salient, enforceable, or connected to action may fail to shape behavior. This distinction is central to the paper's safety argument: constraints must exert force inside the optimizer's perceived topography.

## Interpretation

**Interpretation** is the optimizer's working understanding of what information means.

Interpretation includes signal meaning, causal assumptions, and action models: beliefs about which actions are likely to produce which outcomes under which conditions. Two systems may see the same information but act differently because they interpret it differently.

Interpretation is related to sensemaking: actors do not respond to reality directly, but to the meaning they construct from available signals, context, and prior assumptions. [WEICK_SENSEMAKING]

## Reasoning State

A **reasoning state** is the structured condition from which an optimizer acts.

It includes the active goal, relevant policies, current interpretation, premise stack, visible information, confidence levels, decision options, constraints, and sufficiency rationale. A central claim of the paper is that human-agent systems often fail because they preserve documents and outputs, but not the reasoning states that produced them.

## Topography

**Topography** refers to the perceived information-and-action environment through which an optimizer moves.

It is not the objective world itself. It is the world as made available to the optimizer through visible information, accessible tools, representations, confidence signals, policies, memories, prior learning, and action affordances.

The term is metaphorical unless explicitly formalized. It is used to describe the shape of perceived possibilities.

## Perceived Topography

**Perceived topography** emphasizes that the optimizer acts on what it can perceive, retrieve, interpret, and trust.

Information may exist in the organization and still fail to shape behavior. If it is invisible, inaccessible, poorly represented, low-confidence, or disconnected from the task, it exerts little or no force on the optimizer's path.

## Information Surface

An **information surface** is any source, interface, artifact, memory, system, or signal through which information becomes available to the optimizer.

Examples include documents, dashboards, policies, Slack threads, CRM records, search results, retrieved chunks, prior campaign learnings, user instructions, and model-generated summaries.

Information surfaces are not neutral. They shape what is visible, what is hidden, what appears authoritative, and what can be acted on.

## Gradient

A **gradient** is a directional pressure within the perceived topography.

A gradient makes some paths appear easier, more useful, more relevant, more confident, lower-cost, or more sufficient than others. In this paper, gradient does not necessarily mean a mathematical gradient or a reinforcement-learning reward function. It is a broader design term for how goals, information, confidence, constraints, tool access, action costs, and prior learning shape movement.

The framework's use of gradient is related to reward shaping and environment design, but it is not identical to formal reward shaping. [NG_REWARD_SHAPING]

## Visibility

**Visibility** describes whether relevant information is available to be perceived at all.

If a policy, prior lesson, risk signal, or customer objection exists but the optimizer cannot see it, then it may not affect behavior. Visibility failures often appear as "the system should have known," when in fact the relevant signal never entered the optimizer's perceived topography.

## Accessibility

**Accessibility** describes whether visible information can be reached, retrieved, or used at acceptable cost.

Information may be visible in principle but too difficult to access in practice. A buried policy, fragmented document set, inaccessible dashboard, or hard-to-query system may exert less behavioral force than a simpler but lower-quality source.

## Representation

**Representation** describes whether information is expressed in a form the optimizer can understand and use.

Poor representation can turn available information into noise. A policy written for lawyers, a dashboard without interpretation, or a customer insight buried in a long transcript may be technically available but functionally weak.

Representation is one reason context layers alone are insufficient. Retrieved information must be usable inside the reasoning process.

## Confidence

**Confidence** describes the optimizer's trust in an observation, explanation, source, or proposed action.

Confidence is not the same as truth. It is a behavioral variable: high-confidence information exerts more force than low-confidence information. Confidence also affects whether the optimizer acts, investigates, escalates, or abstains.

The framework treats hallucination partly as a confidence/sufficiency failure: the system moves to answer before evidence is strong enough to support the claim. [DEEPMIND_GOPHERCITE] [RAG_FOUNDATIONAL]

## Connectivity

**Connectivity** describes how information relates to other information, actions, assumptions, risks, or outcomes.

Connectivity answers questions such as: What does this signal imply? What else becomes likely if this is true? Which assumptions does this contradict? Which prior lessons are relevant? Which policy does this trigger?

Connectivity is central to learning. A system may see a signal but fail to connect it to the premise it invalidates.

## Attraction

**Attraction** is the allocation of optimizer attention toward part of the perceived topography.

Information becomes attractive when it appears goal-relevant, action-relevant, uncertain in an important way, or connected to other meaningful signals. Attraction does not mean desire. It means attention is pulled toward something because the optimizer's current state makes it salient.

## Investigation

**Investigation** is the process of reducing uncertainty before action.

Investigation begins when an observation, contradiction, confidence gap, or decision risk becomes salient enough to warrant further search. Investigation may gather evidence, test explanations, explore alternatives, resolve contradictions, or determine that additional information is unlikely to change the action.

## Sufficiency

**Sufficiency** is the point at which additional information is unlikely to materially change the selected action.

Sufficiency is not certainty. A system may have incomplete confidence in the full explanation but still reach sufficiency if the same action remains appropriate across plausible explanations. Conversely, a system may be confident about one fact but still lack sufficiency because a missing variable could change the decision.

This concept is directly related to bounded rationality and satisficing. [SIMON1955] [SIMON_SATISFICING]

## Action

**Action** is the selected behavior produced by optimizer motion.

In human-agent systems, action may include answering, generating content, escalating, refusing, searching, sending a message, updating a record, invoking a tool, approving a workflow, or recommending a decision. The framework treats action as the output of goal, policy, interpretation, topography, investigation, and sufficiency.

## Prediction Error

**Prediction error** is a mismatch between expected and observed outcome.

Prediction error is the trigger condition for learning, but it is not learning by itself. A system must investigate the mismatch, explain it with evidence, and update the relevant model before learning has occurred.

## Learning

**Learning** is an evidence-supported model update triggered by prediction error.

A bad outcome alone is not learning. A reaction is not learning. A postmortem is not necessarily learning. Learning occurs when an expectation is violated, the mismatch is investigated, an evidence-supported explanation is formed, and future behavior is updated.

This usage is related to organizational learning, especially the distinction between correcting behavior and updating the assumptions that produced it. [ARGYRIS_SCHON] [CYERT_MARCH]

## Premise Stack

A **premise stack** is the artifact-backed basis for a prior expectation.

It includes the assumptions, source materials, playbooks, strategies, customer research, data, policies, or prior decisions that made an action seem reasonable before it was taken. The premise stack answers: why did we expect this to work?

Premise stacks matter because failures are often misdiagnosed. Without knowing the assumptions that produced an action, a system may learn the wrong lesson from the right evidence.

## Model Update Object

A **Model Update Object** is a reusable record of learning.

It preserves the prior expectation, premise stack, triggering action, observed outcome, prediction error, evidence trace, explanation, update target, applicability boundary, and confidence level. Its purpose is to prevent learning from degrading into folklore, memory, or isolated postmortem notes.

## Discovery

**Discovery** is the process by which messy human intent and organizational artifacts are converted into structured reasoning objects.

Discovery is not simply asking questions. In mature systems, discovery retrieves existing context, infers likely reasoning state, proposes a strawman, confirms only material uncertainties, generates useful artifacts, preserves the decision state, and learns from outcomes.

In short:

```
Retrieve → Infer → Propose → Confirm → Generate → Preserve → Learn
```

Discovery is where human intent first becomes agent-usable reasoning state.

## Alignment

**Alignment** is used cautiously in this paper.

The framework does not treat alignment only as value matching between a model and a human. It treats alignment as a property of the broader human-agent system: goals, policies, interpretations, information surfaces, action affordances, confidence structures, oversight, and learning loops must work together so that behavior reliably moves toward intended outcomes.

This does not replace existing AI alignment work. It reframes one applied layer of the problem: the designed topography through which agent behavior emerges. [AI_ALIGNMENT_OVERVIEW] [AGENT_SAFETY_SURVEY]

## Governance

**Governance** refers to the mechanisms by which goals, policies, permissions, evidence requirements, approval paths, monitoring, and learning updates are made durable and behaviorally effective.

Governance is not merely having rules. Governance succeeds when the rules are visible, accessible, represented clearly, connected to action, and capable of shaping behavior at the moment of decision.

## Hallucination

**Hallucination** refers to the production of plausible but unsupported claims.

In this framework, hallucination is not only an output defect. It is also a reasoning-state failure: the system reaches sufficiency before evidence warrants the claim. Grounding, citation, uncertainty expression, and "I don't know" behavior can be understood as ways of reshaping the information topography so unsupported completion becomes less attractive than evidence-backed response. [DEEPMIND_GOPHERCITE] [RAG_FOUNDATIONAL]

---

## Summary of Usage

This paper uses *topography* to describe the environment of perceived possibilities; *gradients* to describe directional pressures within that environment; and *optimizer* to describe the system moving through it.

The central claim is that safer and more reliable human-agent systems require not only stronger constraints, but better-shaped perceived topographies.

---

### Citation Debt — Section 2

**Used:**
- [SIMON1955]
- [SIMON_SATISFICING]
- [WEICK_SENSEMAKING]
- [NG_REWARD_SHAPING]
- [DEEPMIND_GOPHERCITE]
- [RAG_FOUNDATIONAL]
- [ARGYRIS_SCHON]
- [CYERT_MARCH]
- [AI_ALIGNMENT_OVERVIEW]
- [AGENT_SAFETY_SURVEY]

**Likely needed:**
- [GIBSON_AFFORDANCES]
- [NORMAN_AFFORDANCES]
- [MARCH_SIMON_ORGS]
- [ORGANIZATIONAL_MEMORY]
- [DECISION_PROVENANCE]
- [HCI_HUMAN_AI_COLLABORATION]

### Draft Notes — Section 2

This section intentionally:
- Prevents readers from importing incompatible meanings for overloaded terms
- Protects the framework from overclaiming mathematical formalism
- Makes the intellectual lineage visible early
- Clarifies that optimizer does not imply moral agency
- Clarifies that gradient is broader than formal reward shaping
- Clarifies that topography is perceived environment, not objective reality
- Prepares the reader for the seven-part architecture that follows

---

# 3. The Problem: Context Is Not Reasoning State

*[To be drafted]*

---

# 4. Optimizers: Goal, Policy, Interpretation

*[To be drafted]*

---

# 5. Information Topography: What the Optimizer Navigates

*[To be drafted]*

---

# 6. Gradients and Motion

*[To be drafted]*

---

# 7. Hallucination and Harmful Action as Related Failures

*[To be drafted]*

---

# 8. Learning: Prediction Error and Model Update

*[To be drafted]*

---

# 9. Model Update Objects: Preserving Learning

*[To be drafted]*

---

# 10. Reasoning Architecture: Preserving State Transitions

*[To be drafted]*

---

# 11. Discovery Framework: From Human Intent to Reasoning State

*[To be drafted]*

---

# 12. Running Example: Adaptive Campaign Reasoning Studio

*[To be drafted]*

---

# 13. Implementation Bridge

*[To be drafted]*

---

# 14. Validation and Falsifiability

*[To be drafted]*

---

# 15. Related Work

*[To be drafted — see RELATED_WORK_LEDGER.md]*

---

# 16. Implications

*[To be drafted]*

---

# 17. Conclusion

*[To be drafted]*
