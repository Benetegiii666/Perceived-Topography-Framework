# 2. A Note on Terms

This paper uses several terms that carry established meanings in other fields, including optimization, reinforcement learning, topology, human-computer interaction, organizational learning, knowledge management, systems theory, and AI safety. The terms are used here in a specific analytic sense. They are intended to provide a shared vocabulary for describing human-agent systems, not to imply a fully mathematical model unless explicitly stated.

This clarification matters because many of the paper's central terms are overloaded. A reader may reasonably bring definitions from reinforcement learning, economics, organizational theory, HCI, or AI alignment. Those definitions are often relevant, and many are part of the intellectual lineage of this framework. But the framework uses these terms as a synthesis. It borrows, narrows, and recombines them around a specific problem: how human-agent systems perceive, decide, act, and learn across organizational workflows.

## Optimizer

An **optimizer** is a system that selects actions in relation to a goal, under constraints, using an interpretation of the situation.

The term does not imply consciousness, desire, moral agency, or malice. An optimizer need not "want" in the human sense. It need only exhibit goal-directed action selection. In this paper, optimizer is a behavioral description, not a psychological claim.

This usage is influenced by bounded rationality and satisficing: real decision-makers do not evaluate all possible actions under perfect information, but search, interpret, and stop when a course of action appears sufficient. [Simon, 1955]

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

Interpretation is related to sensemaking: actors do not respond to reality directly, but to the meaning they construct from available signals, context, and prior assumptions. [Weick, 1995]

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

The framework's use of gradient is related to reward shaping and environment design, but it is not identical to formal reward shaping. [Ng et al., 1999]

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


In this paper, capitalized Confidence refers to the topography dimension: how trustworthy, grounded, or reliable a perceived information surface appears to the optimizer. Lowercase confidence refers to the general degree of belief or reliability assigned in ordinary reasoning contexts.

The framework treats hallucination partly as a confidence/sufficiency failure: the system moves to answer before evidence is strong enough to support the claim. [Menick et al., 2022] [Lewis et al., 2020]

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

This concept is directly related to bounded rationality and satisficing. [Simon, 1955]

## Action

**Action** is the selected behavior produced by optimizer motion.

In human-agent systems, action may include answering, generating content, escalating, refusing, searching, sending a message, updating a record, invoking a tool, approving a workflow, or recommending a decision. The framework treats action as the output of goal, policy, interpretation, topography, investigation, and sufficiency.

## Prediction Error

**Prediction error** is a mismatch between expected and observed outcome.

Prediction error is the trigger condition for learning, but it is not learning by itself. A system must investigate the mismatch, explain it with evidence, and update the relevant model before learning has occurred.

## Learning

**Learning** is an evidence-supported model update triggered by prediction error.

A bad outcome alone is not learning. A reaction is not learning. A postmortem is not necessarily learning. Learning occurs when an expectation is violated, the mismatch is investigated, an evidence-supported explanation is formed, and future behavior is updated.

This usage is related to organizational learning, especially the distinction between correcting behavior and updating the assumptions that produced it. [Argyris & Schön, 1978] [Cyert & March, 1963]

## Premise Stack

A **premise stack** is the artifact-backed basis for a prior expectation.

It includes the assumptions, source materials, playbooks, strategies, customer research, data, policies, or prior decisions that made an action seem reasonable before it was taken. The premise stack answers: why did we expect this to work?

Premise stacks matter because failures are often misdiagnosed. Without knowing the assumptions that produced an action, a system may learn the wrong lesson from the right evidence.

## Model Update Object

A **Model Update Object** is a reusable record of learning.

It preserves the prior expectation, premise stack, triggering action, observed outcome, prediction error, evidence trace, explanation, update target, applicability boundary, and confidence level. Its purpose is to prevent learning from degrading into folklore, memory, or isolated postmortem notes.

A model update is the change in future reasoning. A Model Update Object is the durable record of that change.

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

This does not replace existing AI alignment work. It reframes one applied layer of the problem: the designed topography through which agent behavior emerges. [Ji et al., 2024]

## Governance

**Governance** refers to the mechanisms by which goals, policies, permissions, evidence requirements, approval paths, monitoring, and learning updates are made durable and behaviorally effective.

Governance is not merely having rules. Governance succeeds when the rules are visible, accessible, represented clearly, connected to action, and capable of shaping behavior at the moment of decision.

## Hallucination

**Hallucination** refers to the production of plausible but unsupported claims.

In this framework, hallucination is not only an output defect. It is also a reasoning-state failure: the system reaches sufficiency before evidence warrants the claim. Grounding, citation, uncertainty expression, and "I don't know" behavior can be understood as ways of reshaping the information topography so unsupported completion becomes less attractive than evidence-backed response. [Menick et al., 2022] [Lewis et al., 2020]

---

## Summary of Usage

This paper uses *topography* to describe the environment of perceived possibilities; *gradients* to describe directional pressures within that environment; and *optimizer* to describe the system moving through it.

The central claim is that safer and more reliable human-agent systems require not only stronger constraints, but better-shaped perceived topographies.

---


