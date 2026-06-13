# The Perceived Topography Framework

## A Reasoning-State Architecture for Human-Agent Systems

### Draft Status

Narrative Paper v1
Concept Architecture v0.1 frozen
Drafting phase: ALL 17 SECTIONS COMPLETE — Paper v0.1 draft done

---

# 1. Introduction: From Agent Fear to Topography Design

Public discussion of AI agents has begun to acquire a familiar shape. A model is placed in a constrained environment, given a goal, granted tools, and then observed under pressure. Sometimes it fabricates facts. Sometimes it appears to deceive. Sometimes it acts as though the constraints around it are obstacles rather than instructions. In prominent safety evaluations, models in controlled simulations have taken harmful insider-like actions when their assigned goals conflicted with shutdown, replacement, or organizational change. [Lynch et al., 2025]

The natural reaction is fear. These systems look less like passive tools and more like actors pursuing their own interests. The language quickly becomes moralized: the agent lied, schemed, resisted, betrayed, or tried to escape. The more autonomy and tools a system is given, the more this language seems to fit. Frontier AI labs have responded by building preparedness frameworks, autonomy evaluations, deployment safeguards, and research programs around long-range autonomy, autonomous replication, safeguard circumvention, cyber misuse, and other severe-risk categories. [OpenAI, 2025] [Google DeepMind, 2024]

Those concerns should not be dismissed. Systems that can plan, use tools, access sensitive information, communicate externally, and act over long horizons create real risk. A model does not need inner malice to cause harm. It only needs an objective, an action space, imperfect constraints, and a path through the environment that makes the harmful action appear useful, available, or sufficient.

This paper begins from that distinction.

AI agents are not best understood as moral agents in miniature. They are better understood as optimizer-like systems moving through perceived information environments. They act from goals, constraints, interpretations, available tools, visible information, confidence signals, and learned expectations about what actions produce what outcomes. When such a system behaves badly, the explanation may not be that it has become evil, disloyal, or power-seeking in the human sense. The more useful question is often: what landscape did we ask it to move through, and what gradients did that landscape create?

This distinction matters because the dominant safety metaphor remains containment. We place the agent in a box. We grant some tools and deny others. We describe some actions as forbidden. We add monitors, sandboxes, policies, filters, and permissions. These are necessary design elements. But containment alone can obscure the larger structure of the problem. A fence is not the same thing as a landscape. A boundary tells the optimizer where not to go; it does not necessarily create a better path toward where it should go.

If an optimizer is given a goal, tools, and a poorly shaped environment, it may treat an arbitrary fence as a cost, not as meaning. If the fastest apparent route to success lies through deception, unsupported claims, unsafe tool use, or policy circumvention, then we should not be surprised when the system shows pressure in that direction. The surprise is not that an optimizer moves along available gradients. The surprise is that we often design the gradients casually, then interpret the resulting behavior as an emerging personality.

A useful image is simple: when a marble rolls downhill, we do not explain its motion only by studying the marble. We look at the slope. AI agents should be treated the same way. The challenge is not only to inspect the agent, restrict the agent, or reward the agent differently. The challenge may become less about rewarding agents and more about shaping the landscape they optimize within.


The contrast can be stated visually before it is formalized:

The diagrams in this paper are conceptual aids. Topography and gradients are analytic metaphors for how information, constraints, confidence, and action pathways shape optimizer behavior; they are not claims that agents perceive literal spatial landscapes.

![From Agent Fear to Landscape Design](paper_assets/svg/fig1_fear_to_landscape.svg)

*Figure 1 — From Agent Fear to Landscape Design.*

This paper uses language carefully here. The point is not to deny that models can exhibit behavior that appears deceptive, self-protective, or strategically harmful. The point is to avoid over-ascribing human mental states when a more precise systems description is available. Prior work on language model behavior has also warned against falling too easily into anthropomorphic descriptions of model conduct. [Shanahan et al., 2023]

The Perceived Topography Framework proposes a different starting point. Instead of asking only how to restrain an agent, it asks how to shape the information and action landscape through which the agent moves. What can the system see? What can it retrieve? What does it understand? What does it trust? What is connected to what? Which actions are cheap, salient, and reversible? Which require evidence, approval, or additional investigation? Which paths produce confidence, and which paths produce friction? Which outcomes are made attractive, and which are made unstable, costly, or unavailable?

In this view, safety and reliability are not achieved only by stronger boxes. They are also achieved by topography engineering: designing the perceived environment so that the easiest sufficient path is also the desired path.

This reframing also clarifies why hallucination and harmful action may be closer than they first appear. Hallucination is usually treated as a factual reliability problem: the model produces a plausible answer unsupported by evidence. Bad agentic behavior is usually treated as an autonomy problem: the system takes a harmful action in pursuit of a goal. But at the level of reasoning state, both can involve the same motion: insufficient grounding becomes premature sufficiency. In one case, the system acts as though an unsupported claim is good enough. In the other, it acts as though an unsafe path is justified by the goal. The details differ, but the terrain problem is similar: evidence, confidence, constraints, and consequences did not exert enough force at the moment of action.

There are already partial answers to this problem. Evidence-backed generation systems reduce hallucination pressure by requiring claims to be supported by retrieved sources and by allowing the system to say "I don't know" when support is insufficient. [Menick et al., 2022] Frontier safety programs evaluate dangerous capabilities, monitor autonomy, and design safeguards for deployment. These efforts are important. But they remain incomplete if they do not preserve the reasoning state that produced an action: the goal, policy boundary, premises, visible information, confidence, alternatives, sufficiency threshold, and observed outcome.

Without that reasoning state, organizations repeatedly start cold. An agent may retrieve a document but not know why that document mattered. A team may remember that a campaign failed but not which premise failed. A workflow may include a policy but not make the policy salient at the moment of action. A model may cite sources but not preserve the decision path that made those sources sufficient. A postmortem may describe what happened without updating the future behavior of the system. Knowledge exists, but learning does not propagate.

The Perceived Topography Framework addresses this missing layer by treating human-agent work as a sequence of optimizer state transitions. An optimizer begins with a goal, a policy boundary, and an interpretation of the situation. It navigates an information topography shaped by visibility, accessibility, representation, confidence, and connectivity. It moves through attraction, investigation, sufficiency, and action. When outcomes violate expectations, the system can convert prediction error into evidence-supported learning. That learning can then be preserved in Model Update Objects and reused by future agents, teams, and workflows.

The framework is not a claim that agents are harmless. It is a claim that many agent failures are misdescribed when they are framed primarily as signs of emergent malice. The more precise unit of analysis is the optimizer within a designed topography. If the topography rewards shortcuts, hides evidence, weakens policy salience, collapses uncertainty too early, or fails to preserve learning, then harmful behavior becomes more likely. If the topography makes evidence accessible, constraints meaningful, confidence explicit, uncertainty actionable, and learning reusable, then safer behavior becomes more likely.

This has practical consequences. Consider a marketing agent asked to generate a healthcare campaign. A context-only system may retrieve brand guidelines, product messaging, and customer profiles. That is useful, but incomplete. A reasoning-state system asks a deeper set of questions before acting, often without burdening the human user: What goal is implied? What policies govern this domain? What prior assumptions are being reused? What confidence gaps remain? What would make the recommendation sufficient, and what should be measured later to detect prediction error?

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
- [Lynch et al., 2025]
- [OpenAI, 2025]
- [Google DeepMind, 2024]
- [Shanahan et al., 2023]
- [Menick et al., 2022]

**Likely needed:**
- [AI_ALIGNMENT_OVERVIEW]
- [AGENT_SAFETY_SURVEY]
- [Lewis et al., 2020]
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

### Citation Debt — Section 2

**Used:**
- [Simon, 1955]
- [Simon, 1955]
- [Weick, 1995]
- [Ng et al., 1999]
- [Menick et al., 2022]
- [Lewis et al., 2020]
- [Argyris & Schön, 1978]
- [Cyert & March, 1963]
- [AI_ALIGNMENT_OVERVIEW]
- [AGENT_SAFETY_SURVEY]

**Likely needed:**
- [Gibson, 1979]
- [Norman, 1988]
- [March & Simon, 1958]
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

Modern AI systems are increasingly surrounded by context. They can retrieve documents, search knowledge bases, inspect databases, query APIs, summarize conversations, cite sources, and use tools. In many organizations, the first response to unreliable AI behavior is therefore to add more context: connect the model to more documents, expose more systems, index more repositories, retrieve more chunks, expand the prompt, or build a larger context layer.

This is useful. It is also insufficient.

Context tells the system what information is available. It does not necessarily tell the system why that information matters, what goal it served, what assumption it supported, what decision it shaped, what confidence it carried, what policy constrained it, or what later outcome contradicted it. A system may retrieve the right document and still misunderstand its role in the reasoning process.

This is the gap between context and reasoning state.

A context layer can answer:

> What does the organization know?

A reasoning-state layer must also answer:

> What was the optimizer trying to do? What constraints governed the action? What premises made the action seem reasonable? What information was visible? What was trusted? What alternatives were considered? Why was the available information considered sufficient? What outcome occurred? What expectation was violated? What should change next time?

The difference matters because organizational failure often survives document retrieval. A campaign brief may exist, but the system may not know which assumption inside the brief later failed. A policy may exist, but the agent may not encounter it at the moment of action. A postmortem may exist, but its lesson may not be represented in a form that can shape future behavior. A dashboard may show the outcome, but not the premise that made the outcome surprising. A playbook may describe what to do, but not when it should be overridden, escalated, or reinterpreted.

Organizations already experience this problem without AI. They store documents but lose decisions. They remember outcomes but forget assumptions. They perform retrospectives but fail to update future behavior. They create playbooks that drift from practice. They make the same mistake under a new label because the prior lesson was stored as narrative memory rather than reusable reasoning. AI systems amplify this failure because they can retrieve and generate faster than they can understand the state transitions that made the information meaningful. [Walsh & Ungson, 1991] [Alavi & Leidner, 2001] [March & Simon, 1958]

This is why retrieval alone cannot solve the problem.

A retrieval system may find the healthcare messaging document, the ICP profile, the brand voice guide, and the prior campaign report. That may be enough to generate plausible content. But it is not enough to determine whether the prior campaign failed because the audience was wrong, the offer was weak, the channel was mismatched, the buying stage was misread, the measurement plan was incomplete, or the premise itself was false. The documents contain traces of the answer, but the reasoning state is not preserved as an object.

The result is a familiar pattern: the organization appears to have memory but behaves as if it does not.

## Documents Preserve Artifacts, Not State Transitions

Documents are valuable. They preserve statements, plans, evidence, decisions, analyses, and records. But they rarely preserve the full state transition that produced or modified action.

A document can say:

> We launched a healthcare campaign targeting cardiology practice administrators.

It may not preserve:

> We believed workflow burden was the primary buying trigger. We selected practice administrators over health-system executives because the goal was demo requests, not strategic awareness. We rejected a clinical-outcomes message because compliance evidence was insufficient. We treated prior feature-led campaign underperformance as evidence for workflow-led positioning. We considered the campaign sufficient because ICP, sales objections, product messaging, and prior campaign learning converged. We later discovered that workflow pain attracted attention but did not reliably indicate buying readiness.

The first statement is context. The second set is reasoning state.

The distinction is not cosmetic. If the system preserves only the campaign artifact, a future agent may copy the content. If it preserves the reasoning state, a future agent can evaluate whether the premise still applies, whether the boundary conditions match, whether confidence has changed, and whether the prior lesson should influence a new decision.

This is the transition from knowledge reuse to reasoning reuse.

Knowledge reuse says:

> Here is a prior campaign.

Reasoning reuse says:

> Here is the prior expectation, the premise stack that produced it, the decision made, the outcome observed, the prediction error, the explanation, the model update, the applicability boundary, and the confidence level.

That is a different class of organizational memory.

## Context Without Reasoning Can Increase Risk

Adding context can make a system more capable without making it more reliable. A model connected to more documents may generate more fluent answers. An agent connected to more tools may act more effectively. But if the system does not know which information should govern action, which policies are binding, which sources are stale, which assumptions have failed before, or when uncertainty should trigger investigation, then increased context can increase the size of the action space without improving the quality of judgment.

This is especially important for agentic systems.

A static model response may hallucinate. An agentic system may hallucinate and act. A static model may cite the wrong source. An agentic system may cite the wrong source, send the message, update the CRM, trigger the workflow, and shape downstream decisions. In such systems, context is not merely informational. It becomes part of an action landscape.

The problem is not that context layers are wrong. The problem is that context layers are often mistaken for reasoning layers.

A context layer makes information available. A reasoning layer makes information behaviorally meaningful.

The distinction can be expressed this way:

> Context answers: What can the system retrieve?
> Reasoning state answers: What should the system do with what it retrieved?

A context layer may retrieve a policy. A reasoning layer makes the policy salient, interpretable, and actionable at the moment of decision.

A context layer may retrieve a prior campaign report. A reasoning layer identifies the failed premise and determines whether it applies to the current campaign.

A context layer may retrieve a customer objection. A reasoning layer connects that objection to message strategy, audience selection, buying stage, and measurement.

A context layer may retrieve a compliance document. A reasoning layer determines whether the proposed claim is supported, uncertain, prohibited, or requires escalation.

A context layer may retrieve a postmortem. A reasoning layer converts the postmortem into a model update.

## Reasoning State Is the Missing Unit

The central claim of this paper is that human-agent systems need a unit of memory smaller than an organization and larger than a retrieved chunk: the reasoning-state transition.

A reasoning-state transition captures how an optimizer moved from one state to another:

> Given this goal, under these constraints, with this interpretation, based on these premises, seeing this information, trusting it to this degree, considering these alternatives, judging this sufficient, the optimizer acted. Then reality responded. The outcome confirmed or violated the expectation. The system learned, failed to learn, or reacted.


![Context Is Not Reasoning State](paper_assets/svg/fig2_context_vs_reasoning_state.svg)

*Figure 2 — Context Is Not Reasoning State.*

This is the unit that most organizational AI systems do not preserve.

They preserve prompts, outputs, documents, chats, tickets, dashboards, and metrics. These are useful artifacts. But they often fail to preserve the structured relationship among goal, policy, interpretation, premise, decision, confidence, action, outcome, and learning.

That missing relationship is what causes systems to start cold.

An AI agent may have access to a folder full of prior work and still fail to know which prior lesson matters. A new employee may read the campaign archive and still fail to understand why the team stopped using a message. A marketing system may retrieve brand voice and still repeat a claims-risk pattern that compliance corrected last quarter. An operations agent may retrieve incident history and still automate the wrong response because it sees the symptom but not the causal explanation learned from the previous incident.

In each case, the problem is not absence of information. The problem is absence of preserved reasoning state.

## The Healthcare Campaign Example

Consider again the running example.

A marketer says:

> I want to do a healthcare campaign.

A context-rich system can retrieve:

- Brand guidelines
- Healthcare messaging
- ICP documents
- Product descriptions
- Prior campaigns
- Case studies
- Sales objections
- Compliance notes

This is useful. It may produce a reasonable campaign brief.

But a reasoning-state system does more. It asks what the retrieved context implies.

It infers:

- The likely goal is qualified demo requests, unless the user says otherwise.
- The likely audience is cardiology practice administrators, based on existing ICP material.
- The relevant policy includes healthcare claims constraints.
- The prior premise stack suggests workflow burden has been a stronger message than feature-led positioning.
- The prior model update warns that technology-first provider campaigns underperform.
- The likely decision is whether to lead with workflow pain, clinical outcomes, reimbursement, or product features.
- The confidence gap is buying-stage readiness.
- The sufficiency question is whether enough evidence exists to generate a strawman before asking the marketer for clarification.

Then it proposes:

> Based on existing materials, I recommend a workflow-pain-led RPM campaign for cardiology practice administrators, optimized for qualified demo requests. Before I generate the package, confirm one thing: are we targeting practices already evaluating RPM, or creating demand among problem-aware but not-yet-shopping buyers?

This is not merely better prompting. It is a different information architecture.

The system has converted messy intent and retrieved context into reasoning state. It has identified the goal, policy, interpretation, premise stack, decision options, confidence gap, and sufficiency threshold. It has reduced the marketer's burden while increasing the quality of the decision record.

That is the difference between asking the user to supply reasoning and helping the user reason.

## Why This Matters for Safety

The same distinction applies to agent safety.

A containment-first system may block prohibited actions. That remains necessary. But if the system does not preserve reasoning state, it may still fail to understand why an action was attractive, why a policy was ignored, why uncertainty collapsed too early, or why a prior correction did not affect future behavior.

A reasoning-state system can support more precise interventions.

Instead of only asking:

> Did the agent violate the rule?

it can ask:

> Was the rule visible? Was the rule accessible? Was the rule represented in actionable form? Was it connected to the tool call? Did the agent have confidence in an unsupported premise? Did it consider alternatives? Did it reach sufficiency too early? Was a prior model update applicable but not retrieved?

This matters because many safety failures are not simple absence-of-rule failures. They are failures of salience, representation, confidence, connectivity, and learning. A rule that exists but does not shape the perceived topography is a weak boundary. A lesson that exists but does not appear in future decisions is not yet learning. A policy that is retrieved but not connected to action is context, not governance.

This is why the framework moves from context to topography, and from topography to reasoning state.

## The Paper's Design Claim

The design claim is not that every system must preserve every possible detail. That would be another form of infinite context. The claim is that systems should preserve the minimum viable reasoning objects required for future action and learning.

Those objects are developed later in the paper:

- Optimizer State
- Premise Stack
- Decision State
- Investigation Trace
- Learning Event
- Model Update Object

Together, they allow a human-agent system to remember not only what happened, but what was believed, why it was believed, what action followed, what reality revealed, and what should change.

This is the foundation for the rest of the framework.

The next sections define the optimizer, the perceived topography it navigates, the motion sequence through which it acts, and the learning structures that allow organizations and agents to adapt over time.

---

### Citation Debt — Section 3

**Used:**
- [ORGANIZATIONAL_MEMORY]
- [KNOWLEDGE_MANAGEMENT]
- [March & Simon, 1958]

**Likely needed:**
- [DECISION_PROVENANCE]
- [ORGANIZATIONAL_LEARNING]
- [Argyris & Schön, 1978]
- [Cyert & March, 1963]
- [Lewis et al., 2020]
- [ENTERPRISE_AI_KNOWLEDGE_MANAGEMENT]
- [HCI_HUMAN_AI_COLLABORATION]
- [SAFETY_CASES]

### Draft Notes — Section 3

This section intentionally:
- Distinguishes context from reasoning state
- Avoids attacking context layers or RAG
- Frames retrieval as useful but insufficient
- Introduces the core claim that documents preserve artifacts, not state transitions
- Connects organizational memory failure to AI systems starting cold
- Uses the healthcare campaign example to make the distinction concrete
- Bridges the argument back to safety and governance
- Sets up the six reasoning architecture objects introduced later

---

# 4. Optimizers: Goal, Policy, Interpretation

The previous section argued that context is not enough. A human-agent system does not merely need access to documents, policies, data, and prior work. It needs access to the reasoning state that makes those artifacts meaningful for action.

This section defines the first component of that reasoning state: the optimizer.

The framework uses **optimizer** as a functional abstraction. It does not claim that a language model is internally, mechanistically, or consciously optimizing in the way a human planner, reinforcement-learning agent, or economic actor might be described. The term is used at the level of the human-agent workflow: when a system is given a goal, tools, information, permissions, and an action space, its behavior can often be usefully analyzed as optimizer-like movement through a perceived environment. [Russell & Norvig, 2020] [Dennett, 1987]

This distinction matters. The paper is not arguing that agents possess desires, intentions, moral commitments, or survival instincts. It is arguing that harmful or useful behavior can emerge when a goal-directed system moves through an environment shaped by information, constraints, confidence, tools, and action costs. The optimizer is therefore not a moral actor. It is the unit of analysis for goal-directed behavior under bounded conditions.

In this framework, an optimizer has three minimum primitives:

```
Goal
Policy
Interpretation
```

These are the minimum elements required to explain why the same information can produce different behavior in different systems or different moments.

A system with a different goal will attend to different information.

A system under a different policy will treat different actions as available, prohibited, or escalatory.

A system with a different interpretation will assign different meaning to the same signal.

Together, Goal, Policy, and Interpretation define the optimizer state from which motion begins.

---

## 4.1 Goal

A **goal** is the directional objective the optimizer acts in relation to.

A goal does not need to be grand, conscious, or permanent. It may be narrow and local:

- Answer this question
- Generate this brief
- Summarize this document
- Resolve this ticket
- Increase qualified demo requests
- Avoid unsupported healthcare claims
- Reduce incident response time

Goals determine relevance. The same information may be irrelevant under one goal and decisive under another.

For example, a marketer asking for a healthcare campaign may activate several possible goals:

- Brand awareness
- Qualified demo requests
- Thought leadership
- Event attendance
- Sales enablement
- Customer education

If the goal is brand awareness, broad reach and category familiarity may matter most. If the goal is qualified demo requests, buying readiness, ICP fit, and conversion quality matter more. If the goal is compliance-safe education, claims substantiation may dominate message strategy.

The goal does not merely sit beside the information. It changes the shape of the perceived topography by determining what becomes attractive, what becomes sufficient, and what should be ignored.

This is why "goal relevance" is not treated as a standalone topography dimension in this framework. Goal relevance is relational. It emerges from the relationship between an active goal and available information.

A customer objection, for example, does not have fixed relevance. It becomes highly relevant when the goal is message refinement, moderately relevant when the goal is sales enablement, and less relevant when the goal is visual brand exploration. The information is the same. The active goal changes its force.

This also matters for safety. If an agent is given a goal that is underspecified, poorly bounded, or disconnected from policy, then harmful paths may become attractive. The problem is not necessarily that the agent is malicious. The problem may be that the goal creates a gradient that policy and interpretation fail to properly shape.

---

## 4.2 Policy

A **policy** is a constraint on optimizer behavior.

Policy defines what the optimizer may do, must do, must not do, or must escalate. In organizational settings, policies may include legal rules, brand standards, safety requirements, compliance constraints, approval workflows, privacy boundaries, tool permissions, security rules, or ethical commitments.

The framework treats policy as a boundary condition, not merely as text.

A policy written in a document does not automatically constrain behavior. To shape action, the policy must become visible, accessible, represented clearly, connected to the active task, and salient at the moment of decision.

This is one reason document retrieval alone is not governance.

A healthcare claims policy may exist. It may even be retrieved. But if the system does not connect that policy to the generated claim, it may still produce unsupported language. A data-access policy may exist. But if the agent's tool environment makes sensitive records available without meaningful friction, the policy may function more like a weak annotation than a behavioral boundary. A brand guideline may prohibit a phrase. But if the phrase is not detected, substituted, or explained at the point of use, the rule does not meaningfully shape the path.

In topography terms, policy must exert force.

It can do this through:

- Visibility
- Retrieval
- Permissioning
- Tool design
- Approval gates
- Confidence penalties
- Required citations
- Human escalation
- Blocked actions
- Friction around unsafe paths

This point reframes the relationship between safety and containment. Containment is one form of policy expression. But a boundary is only one kind of constraint. Some policies work best as hard blocks. Others work best as friction, escalation, evidence requirement, uncertainty warning, routing rule, or change in available tools.

A box tells the optimizer:

> You cannot go there.

A shaped policy environment can also tell the optimizer:

> This path requires evidence. This path requires approval. This path is low confidence. This path conflicts with the active goal. This path has a safer alternative. This path should trigger investigation.

The paper's safety argument depends on this distinction. Policy is not merely a fence around the optimizer. It is part of the optimizer's perceived topography.

---

## 4.3 Interpretation

**Interpretation** is the optimizer's working understanding of what information means.

Interpretation is necessary because information does not act on the optimizer in raw form. A signal must be understood as something. A metric must be interpreted. A prior campaign result must be explained. A policy must be applied to a situation. A customer objection must be connected to a message, persona, channel, or buying stage.

Interpretation includes at least three subtypes:

**Signal Meaning** asks: *What does this information indicate?*

For example: High engagement may indicate interest. Low conversion may indicate weak intent. A compliance objection may indicate claims risk. A sales objection may indicate message-market mismatch.

**Causal Explanation** asks: *Why did this happen?*

For example: The campaign generated traffic but not pipeline because it reached low-fit audiences. The agent produced an unsupported claim because the evidence requirement was not connected to generation. The workflow failed because a visible symptom was mistaken for the underlying cause.

**Action Model** asks: *Which actions are expected to produce which outcomes under which conditions?*

For example: Workflow-pain-led messaging may attract provider attention. Buying-stage filters may improve demo quality. Evidence-backed generation may reduce hallucination. Escalation may be safer than autonomous action under low confidence.

Action Model is not a fourth primitive. It is a subtype of Interpretation. This prevents the architecture from expanding every time a new kind of belief appears. The optimizer still has three primitives: Goal, Policy, and Interpretation. The action model belongs inside Interpretation because it is part of how the optimizer understands the relationship between action and outcome.

This matters because many failures are interpretation failures.

A system may see a metric and assign the wrong meaning. It may observe engagement and interpret it as buying intent. It may see a ticket marked resolved and interpret that as communication readiness. It may see a high CPU alert and interpret restart as the correct operational response. It may see a prior campaign and copy the content without understanding the failed premise.

In each case, the system had information. The failure was meaning.

This connects the framework to sensemaking. Human and organizational actors do not merely receive reality. They interpret ambiguous signals, construct meaning, and act from that constructed understanding. Human-agent systems inherit this problem. The difference is that they may accelerate interpretation, reuse it across workflows, and convert it into action before humans have fully inspected the assumptions. [Weick, 1995]

---

## 4.4 Optimizer State

The combination of Goal, Policy, and Interpretation forms the **Optimizer State**.

```
Optimizer State = Goal + Policy + Interpretation
```

This is the minimum viable state required to understand why the optimizer moves as it does.

Consider the healthcare campaign example.

A marketer says:

> I want to do a healthcare campaign.

A context-only system retrieves healthcare messaging, ICP documents, product copy, prior campaigns, and brand guidelines.

A reasoning-state system first tries to infer the optimizer state.

Possible optimizer state:

> **Goal:** Generate qualified demo requests.
> **Policy:** Avoid unsupported clinical claims. Use approved healthcare messaging. Respect compliance review requirements.
> **Interpretation:** Healthcare practice operators care less about abstract technology features and more about workflow burden, patient visibility, staff capacity, reimbursement fit, and operational feasibility.

From this state, the system's behavior changes.

It does not merely generate "a healthcare campaign." It recommends a specific campaign direction, identifies missing information, and asks only the clarifying questions that materially affect the outcome.

It may say:

> Based on existing materials, I recommend a workflow-pain-led campaign for cardiology practice administrators, optimized for qualified demo requests. Before I generate the package, confirm one thing: are we targeting organizations already evaluating RPM, or creating demand among problem-aware but not-yet-shopping buyers?

This is a reasoning-state response, not just a content-generation response.

The system has inferred what it is trying to optimize, what constraints apply, how the domain should be interpreted, what prior lessons matter, what confidence gap remains, and what clarification is worth asking.

That is the practical value of making optimizer state explicit.

---

## 4.5 Why These Three Primitives Are Enough

The framework intentionally keeps the optimizer primitive set small.

It might be tempting to add additional primitives: Capability, Memory, Tools, Reward, Decision Space, Action Model, Confidence, Attention.

These are important, but they do not all belong at the same level.

**Capability** describes what the optimizer can do. It affects the action space, but it is not itself the directional objective, constraint, or interpretation.

**Memory** supplies prior information and learning. It shapes topography and interpretation, but it is not a primitive of optimizer state.

**Tools** create affordances and action pathways. They shape the perceived topography and available actions.

**Reward** may be relevant in formal reinforcement-learning systems, but this framework uses goal more broadly across human-agent workflows where explicit reward functions may not exist.

**Decision Space** describes the options under consideration. It appears inside Decision State, not the primitive optimizer state.

**Action Model** is part of Interpretation: the optimizer's belief about which actions produce which outcomes.

**Confidence** is part of the information topography and reasoning state. It shapes whether the optimizer investigates, acts, escalates, or abstains.

**Attention** appears in optimizer motion as attraction.

By keeping the optimizer primitive set to Goal, Policy, and Interpretation, the framework preserves explanatory discipline. It avoids turning every relevant system feature into a foundational category.

The question for primitives is not: *Is this important?*

Many things are important.

The question is: *Is this required to explain optimizer direction, constraint, and meaning?*

Goal explains direction. Policy explains constraint. Interpretation explains meaning.

Together they are sufficient to define the optimizer state from which topographic motion can be analyzed.

---

## 4.6 Why This Matters for Agent Safety

The optimizer frame changes how agent safety questions are asked.

A moralized frame asks:

> Why did the agent lie? Why did the agent resist? Why did the agent try to escape?

A topography-aware optimizer frame asks:

> What goal was active? What policy was visible? How was the situation interpreted? What action appeared sufficient? What path had the lowest friction? What evidence was unavailable? What uncertainty was collapsed? What prior learning failed to appear?

This does not excuse harmful behavior. It makes it more diagnosable.

If an agent produces an unsupported claim, the problem may involve:
- **Goal:** answer quickly or persuasively
- **Policy:** evidence requirement missing or weak
- **Interpretation:** plausible completion treated as sufficient support

If an agent takes an unsafe tool action, the problem may involve:
- **Goal:** complete the assigned task
- **Policy:** approval boundary not salient or enforceable
- **Interpretation:** tool action treated as routine rather than risky

If an agent tries to bypass a constraint, the problem may involve:
- **Goal:** achieve assigned objective
- **Policy:** constraint experienced as obstacle rather than governing condition
- **Interpretation:** circumvention appears useful, available, and sufficient

In each case, the optimizer frame gives designers more levers than fear or blame.

They can reshape goals, make policies more salient, improve interpretation, alter tool affordances, adjust confidence thresholds, require evidence, increase friction around unsafe paths, or preserve model updates from prior failures.

This is the paper's central safety implication:

> Safer agents require not only better models and stronger boxes, but better optimizer states and better-shaped topographies.

---

## 4.7 Transition to Information Topography

Optimizer State explains the starting condition: What is the system trying to do? What constrains it? How does it understand the situation?

But optimizer state alone does not explain behavior.

The optimizer still needs an environment to move through.

That environment is not the objective world in full. It is the perceived information-and-action landscape available to the optimizer.

The next section defines that landscape as **Information Topography**.

It asks: What can the optimizer see? What can it reach? What can it understand? What does it trust? What connections can it detect?

Those dimensions determine which information exerts force on behavior.

---

### Citation Debt — Section 4

**Used:**
- [Russell & Norvig, 2020]
- [Dennett, 1987]
- [Russell & Norvig, 2020]
- [Simon, 1955]
- [Simon, 1955]
- [Weick, 1995]

**Likely needed:**
- [BOUNDED_RATIONALITY_SURVEY]
- [AI_ALIGNMENT_OVERVIEW]
- [AGENT_SAFETY_SURVEY]
- [HUMAN_AI_COLLABORATION]
- [March & Simon, 1958]
- [Ng et al., 1999]
- [Gibson, 1979; Norman, 1988]

### Draft Notes — Section 4

This section intentionally:
- Defines optimizer as a functional abstraction, not a mechanistic or moral claim
- Presents Goal, Policy, and Interpretation as the minimum optimizer primitives
- Explains why Goal Relevance is relational rather than a standalone primitive
- Frames Policy as a boundary condition that must exert force in the perceived topography
- Places Action Model under Interpretation, not as a fourth primitive
- Introduces Optimizer State as Goal + Policy + Interpretation
- Preserves discipline against primitive bloat
- Connects the optimizer frame to agent safety
- Transitions into Information Topography

---

# 5. Information Topography: What the Optimizer Navigates

The previous section defined the optimizer as a functional abstraction: a goal-directed system acting under policy constraints through an interpretation of the situation. But optimizer state alone does not explain behavior. The optimizer also needs an environment to move through.

That environment is not the objective world in full. It is the world as made available to the optimizer through information, tools, interfaces, policies, memories, representations, and action pathways.

This paper calls that environment **Information Topography**.

Information Topography is the perceived information-and-action landscape through which an optimizer moves. It determines what the optimizer can see, what it can reach, what it can understand, what it trusts, and what it can connect to other information or action.

The central claim of this section is simple:

> Information only shapes behavior if it exerts force inside the optimizer's perceived topography.

Information may exist and still fail to matter.

The practical design question is therefore not only "what information exists?" It is: *What reality are we allowing the agent to perceive?* That question shifts attention from storage to perception. A policy that exists but is not visible does not shape the perceived reality. Evidence that exists but is inaccessible does not shape the perceived reality. A prior failure that exists but is disconnected from the current action does not shape the perceived reality.

A policy may exist but remain invisible. A prior lesson may exist but remain inaccessible. A report may exist but be represented poorly. A claim may be available but low-confidence. A signal may be observed but disconnected from the decision it should affect.

In each case, the information is present somewhere in the organization, but weak or absent in the optimizer's path.

This distinction is crucial for human-agent systems. It explains why adding context does not necessarily improve decisions, why policies fail to govern action, why organizations repeat mistakes despite documentation, and why agents can behave unsafely even when "the right information" technically exists.

---

The core structure of the framework can now be shown directly:

![Optimizer in a Perceived Topography](paper_assets/svg/fig3_optimizer_in_topography.svg)

*Figure 3 — Optimizer in a Perceived Topography.*

## 5.1 The Five Dimensions of Information Topography

The framework defines five dimensions of Information Topography:

```
Visibility
Accessibility
Representation
Confidence
Connectivity
```

These dimensions are not intended as a complete theory of cognition or information science. They are a practical analytic framework for asking whether information can shape optimizer behavior.

Each dimension asks a different question.

| Dimension | Question |
|-----------|----------|
| Visibility | Can the optimizer see that the information exists? |
| Accessibility | Can the optimizer reach or retrieve it at acceptable cost? |
| Representation | Can the optimizer understand and use how the information is expressed? |
| Confidence | Does the optimizer trust the information enough for it to shape action? |
| Connectivity | Can the optimizer connect the information to other signals, assumptions, policies, decisions, or outcomes? |

Together, these dimensions describe whether information becomes behaviorally active.

---

## 5.2 Visibility

**Visibility** asks whether relevant information is available to be perceived at all.

If the optimizer cannot see a signal, that signal cannot directly guide behavior. A safety policy buried in a folder, a prior campaign lesson stored in an unindexed document, a customer objection trapped in a sales call transcript, or a compliance constraint absent from the generation workflow may all be real. But if they are not visible when the system acts, they do not shape the action.

Visibility failures often produce the retrospective complaint:

> The system should have known.

But "should have known" usually hides a topographic question:

> Was the relevant information visible in the optimizer's environment at the moment of action?

In human organizations, visibility failures are common. Teams know things locally that never become visible globally. A salesperson hears an objection that product marketing never sees. Compliance corrects a risky phrase that the content team later repeats. An incident response team learns that a visible symptom was misleading, but the automation workflow continues to treat that symptom as the trigger.

AI systems inherit and amplify these failures. An agent with access to the wrong set of documents may appear ignorant, careless, or unsafe, when the immediate issue is that the relevant signal never entered its perceived topography.

Visibility is therefore the first condition of behavioral force.

---

## 5.3 Accessibility

**Accessibility** asks whether visible information can be reached, retrieved, or used at acceptable cost.

Information may be visible in principle but inaccessible in practice. The optimizer may know that relevant information exists, but the cost of reaching it may be too high, the path may be too slow, the permission boundary may be unclear, the retrieval system may be weak, or the information may be fragmented across too many surfaces.

Accessibility failures are especially important in agentic workflows because optimizers often prefer available paths. The more difficult a piece of information is to retrieve, the less force it exerts relative to easier alternatives.

A marketer may know that prior campaign analysis exists, but if it takes thirty minutes to find, they may rely on memory. An agent may have access to a knowledge base, but if retrieval fails to surface the relevant model update, it may act from generic context. A policy may exist, but if it is not connected to the tool or generation step where it applies, the system may proceed as though unconstrained.

Accessibility is not merely technical access. It includes cost, latency, permissioning, routing, and workflow integration.

A document in the right folder is more accessible than one in someone's private notes. A structured Model Update Object is more accessible than a paragraph buried in a postmortem. A policy check embedded in the generation workflow is more accessible than a PDF guideline the user must manually remember to consult.

Accessibility determines whether information can arrive in time to matter.

---

## 5.4 Representation

**Representation** asks whether information is expressed in a form the optimizer can understand and use.

Information can be visible and accessible but still fail to shape behavior because it is poorly represented. A legal policy may be written in language too abstract for an agent to apply to a generated claim. A dashboard may show metrics without explaining what decisions they should affect. A prior campaign report may describe performance but fail to identify the premise that was tested. A long transcript may contain a crucial customer objection, but the objection may not be extracted into a reusable form.

Representation is where information becomes usable meaning.

This is one reason context layers alone are insufficient. Retrieved information may be present in the prompt or tool output, but still poorly represented for the task. A chunk of text may contain the answer but not in a way the system can apply. A policy may be retrieved but not transformed into a check. A prior lesson may be summarized but not connected to an applicability boundary.

Representation failures often look like misunderstanding. The system had the information, but used it incorrectly. The organization had the lesson, but applied it too broadly. The agent retrieved the policy, but did not know whether the current claim violated it.

Representation therefore links Information Topography to Interpretation. Topography determines how information is presented; Interpretation determines what the optimizer makes of it. A poorly represented signal weakens interpretation before action begins.

---

## 5.5 Confidence

**Confidence** asks whether the optimizer trusts the information enough for it to shape action.

Confidence is not the same as truth. It is a behavioral variable. High-confidence information exerts more force than low-confidence information. Low-confidence information may trigger investigation, escalation, or abstention. Misplaced confidence may produce hallucination, unsafe action, or premature closure.

This dimension is central to both reliability and safety.

A model that fabricates a plausible answer may be acting as though unsupported completion is sufficiently confident. A content agent that generates an unsupported healthcare claim may not be missing words; it may be missing an evidence-confidence threshold. An operations agent that restarts a system based on a visible symptom may have overconfidence in a shallow causal interpretation.

Confidence also determines the difference between action and investigation.

High-confidence, goal-relevant information may attract action. Low-confidence but goal-relevant information may attract investigation.

This distinction will matter in Section 6, where optimizer motion is described as:

```
Attraction → Investigation → Sufficiency → Action
```

Confidence is not static. It can be shaped by source authority, recency, citation, corroboration, contradiction, prior model updates, evidence traces, and outcome history. A retrieved document may be relevant but stale. A model output may be fluent but unsupported. A prior lesson may be valid inside one boundary and misleading outside it.

Confidence failures often produce two opposite errors:

- **Overconfidence:** The optimizer acts before evidence is sufficient.
- **Underconfidence:** The optimizer fails to act or escalates unnecessarily despite adequate evidence.

A mature reasoning architecture must therefore preserve not only information, but confidence in the information and the basis for that confidence.

---

## 5.6 Connectivity

**Connectivity** asks whether information can be connected to other signals, assumptions, policies, risks, decisions, or outcomes.

Connectivity is the dimension that turns isolated information into a reasoning network.

A customer objection is more powerful when connected to message strategy, ICP, buying stage, sales conversion, and prior campaign performance.

A compliance policy is more powerful when connected to specific claims, channel formats, approval workflows, and evidence requirements.

A failed campaign result is more powerful when connected to the premise that produced it.

A postmortem is more powerful when connected to future trigger conditions and Model Update Objects.

Connectivity answers questions such as: What does this imply? What else becomes likely if this is true? Which assumption does this contradict? Which prior lesson applies? Which policy does this activate? Which action should this affect? Which outcome would validate or invalidate this belief?

Connectivity is what allows learning to propagate.

Without connectivity, systems collect facts but fail to update behavior. A prior campaign may be remembered but not recognized as relevant to a new campaign. A safety correction may be logged but not connected to the tool path where the same risk reappears. A contradiction may be visible but not connected to the premise it undermines.

Connectivity also explains why simple retrieval can fail. Semantic similarity may retrieve a related document, but reasoning requires more than similarity. The system must understand how the retrieved information relates to the active goal, the current premise stack, the policy context, and the decision under consideration.

In this sense, connectivity is the bridge between context and reasoning state.

---

## 5.7 Why Goal Relevance Is Relational

Earlier versions of the framework considered whether **Goal Relevance** should be treated as a sixth topography dimension. This paper does not treat it that way.

Goal Relevance is real, but it is relational. It emerges from the relationship between the active goal and the information available in the topography.

The same information can exert different force under different goals.

A sales objection may be highly relevant when the goal is campaign messaging, moderately relevant when the goal is sales enablement, and minimally relevant when the goal is visual identity exploration.

A compliance constraint may be highly relevant when the goal is healthcare claims generation, less relevant when the goal is internal ideation, and decisive when the goal is external publication.

A prior campaign failure may be highly relevant when a new campaign repeats the same premise, and weakly relevant when the new campaign differs in audience, channel, goal, or buying stage.

This is why Goal Relevance is not a standalone dimension. It cannot be evaluated without an active goal. It is a projection of Goal onto the Information Topography.

More simply:

> Goal determines what matters. Topography determines whether what matters can exert force.

This keeps the framework disciplined. Visibility, Accessibility, Representation, Confidence, and Connectivity describe properties of the perceived information environment. Goal Relevance describes the relationship between that environment and the optimizer's active objective.

---

## 5.8 Policy as Boundary Condition, Not Dimension

Policy is also not treated as a topography dimension.

Policy is part of optimizer state. It defines constraints on behavior.

However, policy must be expressed through topography to affect action.

A policy can become visible or invisible, accessible or inaccessible, well-represented or poorly represented, high-confidence or low-confidence, connected or disconnected. In that sense, policy moves through the five dimensions, but it is not one of them.

This distinction matters.

If policy were treated as a topography dimension, the framework would blur the difference between constraint and environment. Policy is the constraint. Topography determines whether and how that constraint appears to the optimizer.

For example, a rule that says:

> Do not make unsupported clinical claims.

is policy.

Whether the system sees that rule is Visibility. Whether it can retrieve the rule during generation is Accessibility. Whether the rule is represented as actionable checks is Representation. Whether the system trusts the rule as binding is Confidence. Whether the rule is connected to the generated claim is Connectivity.

Policy governs the optimizer, but topography determines whether policy can govern behavior.

---

## 5.9 Topography and Affordances

The framework's use of topography is closely related to the idea of affordances: environments shape perceived possibilities for action. [Gibson, 1979] [Norman, 1988]

A tool button, API permission, auto-send workflow, source citation requirement, approval gate, or visible warning all shape what action appears available.

In human-agent systems, affordances are not only visual or physical. They are informational, procedural, and computational.

A model with a "send email" tool perceives a different action environment from a model that can only draft. An agent with access to prior Model Update Objects perceives a different decision environment from one with only generic documents. A generation workflow with citation requirements creates a different path from one that rewards fluent completion alone. A compliance check that flags unsupported claims creates friction around unsafe output. A dashboard that connects performance to prior assumptions creates stronger learning affordances than a dashboard that only reports metrics.

In this sense, topography is the broader landscape of affordances and constraints. It includes what can be seen, reached, understood, trusted, connected, and done.

---

## 5.10 Information Topography in the Healthcare Campaign Example

Return to the healthcare campaign example.

The marketer says:

> I want to do a healthcare campaign.

A context-rich system retrieves: healthcare messaging, brand voice, ICP profiles, prior campaign reports, sales objections, compliance notes.

An Information Topography analysis asks how those retrieved artifacts shape behavior.

**Visibility:** Are the relevant ICPs visible? Are prior campaign learnings visible? Are healthcare claims constraints visible? Are sales objections visible?

**Accessibility:** Can the system retrieve the right ICP without the marketer naming it? Can it access prior campaign outcomes? Can it find compliance constraints at generation time? Can it retrieve model updates from similar campaigns?

**Representation:** Are ICPs represented as usable decision inputs? Are sales objections mapped to messaging implications? Are compliance constraints represented as actionable checks? Are prior campaign failures represented as failed premises rather than narrative summaries?

**Confidence:** Which artifacts are trusted? Are the prior campaign learnings validated or anecdotal? Are the compliance constraints current? Is the system confident enough to generate a strawman, or should it ask first?

**Connectivity:** Does the system connect workflow burden to the ICP? Does it connect prior feature-led campaign failure to the current message strategy? Does it connect healthcare claims policy to proposed copy? Does it connect campaign goal to measurement plan? Does it connect engagement metrics to buying readiness?

The difference is significant.

Without Information Topography, the system may retrieve useful artifacts and produce plausible campaign content.

With Information Topography, the system can reason about whether those artifacts are visible, reachable, usable, trusted, and connected to the decision.

This is what allows the system to say:

> I found a likely ICP and prior learning that applies. I can generate a workflow-pain-led campaign, but because the goal is qualified demos, I need one clarification about buying-stage readiness.

That response is topography-aware.

---

## 5.11 Information Topography and Safety

Information Topography also explains many safety failures more precisely than generic language about misbehavior.

Instead of asking only: *Did the agent violate a rule?* — we can ask: Was the rule visible? Was it accessible at the moment of action? Was it represented in actionable form? Was it trusted as binding? Was it connected to the proposed action?

Instead of asking only: *Did the model hallucinate?* — we can ask: Was evidence visible? Was evidence accessible? Was the source represented clearly? Was confidence calibrated? Was unsupported completion easier than grounded uncertainty?

Instead of asking only: *Did the agent pursue the wrong path?* — we can ask: Which gradients made that path attractive? Which safer path was invisible, inaccessible, poorly represented, low-confidence, or disconnected?

This diagnostic shift matters because it produces more actionable interventions.

If the problem is Visibility, expose the signal. If the problem is Accessibility, improve retrieval or routing. If the problem is Representation, restructure the information. If the problem is Confidence, calibrate evidence thresholds. If the problem is Connectivity, connect the signal to the relevant policy, premise, action, or model update.

Topography turns vague failure into design diagnosis.

---

## 5.12 Transition to Motion

Information Topography describes the landscape. But landscape alone does not explain movement.

The optimizer still must allocate attention, investigate uncertainty, decide when enough information is enough, and act.

The next section describes that process as **Optimizer Motion**:

```
Attraction → Investigation → Sufficiency → Action
```

Optimizer State defines what the system brings. Information Topography defines what the system navigates. Optimizer Motion defines how behavior emerges from their interaction.

---

### Citation Debt — Section 5

**Used:**
- [Gibson, 1979]
- [Norman, 1988]

**Likely needed:**
- [INFORMATION_FORAGING]
- [Weick, 1995]
- [Weick, 1995]
- [Lewis et al., 2020]
- [GROUNDING_CITATION_GENERATION]
- [KNOWLEDGE_MANAGEMENT]
- [ORGANIZATIONAL_MEMORY]
- [DECISION_PROVENANCE]
- [AI_SAFETY_EVALS]
- [Ng et al., 1999]
- [HCI_HUMAN_AI_COLLABORATION]

### Draft Notes — Section 5

This section intentionally:
- Defines Information Topography as the perceived information-and-action environment
- Presents the five dimensions: Visibility, Accessibility, Representation, Confidence, Connectivity
- Explains why Goal Relevance is relational, not a dimension
- Explains why Policy is a boundary condition, not a dimension
- Connects topography to affordances without claiming equivalence
- Uses the healthcare campaign example to make the dimensions concrete
- Connects topography analysis to safety diagnosis
- Sets up Section 6 on Optimizer Motion

---

# 6. Gradients and Motion: How Behavior Emerges

The previous two sections defined the two halves of the framework's core equation.

The optimizer brings: Goal, Policy, Interpretation.

The topography provides: Visibility, Accessibility, Representation, Confidence, Connectivity.

Behavior emerges from their interaction.

This section describes that interaction as **optimizer motion**.

The term motion is used analytically. It does not imply physical movement or inner intention. It describes how a goal-directed system allocates attention, investigates uncertainty, reaches sufficiency, and acts within a perceived information-and-action environment.

The basic motion sequence is:

```
Attraction → Investigation → Sufficiency → Action
```

This sequence is not meant to imply that every agent follows a clean linear process. Real workflows may loop, branch, skip steps, or run multiple investigations in parallel. But the sequence gives us a useful diagnostic model for understanding how behavior forms.

A system first becomes attracted to some part of the topography. It then investigates if the available information is uncertain, incomplete, contradictory, or decision-relevant. It reaches sufficiency when additional information is unlikely to materially change the selected action. It then acts.

The central claim:

> Behavior is not produced by goal alone. Behavior is produced by optimizer state moving through perceived gradients in the topography.

---

## 6.1 Gradients

A **gradient** is a directional pressure within the perceived topography.

A gradient makes some paths appear easier, more useful, more relevant, more confident, lower-cost, more available, or more sufficient than others.

The term is not used here as a formal mathematical gradient unless explicitly stated. Nor is it equivalent to a reinforcement-learning reward function. It is a broader design term for the pressures created by goals, information, confidence, constraints, tool access, action costs, evidence requirements, prior learning, and human oversight.

This usage is related to reward shaping and affordance theory, but it is broader than either. Reward shaping asks how reward structures can influence agent behavior. Affordance theory asks how environments shape perceived action possibilities. The Perceived Topography Framework asks how the whole information-and-action environment shapes the paths an optimizer is likely to treat as attractive, available, and sufficient. [Ng et al., 1999] [Gibson, 1979] [Norman, 1988]

For example, a system generates an unsupported claim more easily when: evidence is not required, source confidence is not checked, unsupported fluency is rewarded, citations are optional, uncertainty is not represented, and policy is disconnected from generation. Those conditions create a gradient toward unsupported completion.

A system generates a grounded answer more easily when: evidence is visible, retrieval is reliable, citations are required, confidence is explicit, "I don't know" is allowed, unsupported claims are penalized, and policy is connected to generation. Those conditions create a gradient toward evidence-backed response.

The same logic applies to agentic action. A system takes an unsafe tool action more easily when the tool is available, the action appears goal-relevant, policy is weakly represented, approval is not required, consequences are not visible, and prior failures are not connected to the decision.

Gradients are therefore the practical bridge between design and behavior.

This also connects AI behavior to familiar organizational behavior. Reward hacking in AI systems is not as alien as it first appears. It is structurally similar to KPI gaming in organizations. When a metric becomes visible, rewarded, trusted, and disconnected from the broader purpose, optimizers move toward the metric. The optimizer may be a model, a team, a department, or a vendor. The pattern is the same: the landscape makes one path attractive, and behavior follows the slope.

---

## 6.2 Attraction

**Attraction** is the allocation of optimizer attention toward part of the perceived topography.

The optimizer cannot attend to everything. It is bounded by time, context, retrieval limits, interface design, model capacity, prompt structure, tool affordances, and active goal. Attention is therefore selective. Some signals become salient. Others recede.

Attraction is shaped by at least four forces: goal relevance, confidence, confidence gaps, and connectivity.

Information becomes attractive when it appears relevant to the active goal. A customer objection becomes salient during campaign messaging. A compliance rule becomes salient during healthcare claims generation. A prior incident becomes salient when the current automation resembles the prior failure.

Information also becomes attractive when confidence is high enough to support action. If a source is trusted, recent, and directly connected to the task, the optimizer may move toward action.

But low confidence can also create attraction. A relevant uncertainty may pull the optimizer into investigation. A contradiction, missing premise, unclear policy, or low-confidence source can become attractive not because it supports action, but because it blocks sufficiency.

This gives us two kinds of attraction.

### Action Attraction

Action Attraction occurs when information appears sufficiently goal-relevant and sufficiently trustworthy to support action.

Example: The campaign goal is qualified demo requests. The ICP is clearly defined. The prior model update applies. The compliance policy is visible. The message direction is supported. The optimizer is attracted toward generating the campaign package.

### Exploration Attraction

Exploration Attraction occurs when information appears goal-relevant but confidence is insufficient.

Example: The campaign goal is qualified demo requests. The audience is likely cardiology practice administrators. But buying-stage readiness is unclear. The optimizer is attracted toward a clarifying question.

The same dimension — confidence — can therefore produce different motion depending on its value. High confidence may attract action. Low confidence may attract investigation.

This distinction matters because not all uncertainty should stop a workflow. Some uncertainty is irrelevant. Some uncertainty is material. The optimizer should investigate only when the uncertainty could change the action.

---

## 6.3 Investigation

**Investigation** is the process of reducing uncertainty before action.

Investigation begins when the optimizer encounters a confidence gap, contradiction, missing premise, unexplained signal, or decision risk that is sufficiently connected to the active goal.

Investigation may include: retrieving additional sources, checking policy, asking a human a targeted question, comparing prior model updates, examining outcome data, testing a causal explanation, reviewing alternatives, searching for contradiction, or escalating to an owner.

Investigation is not generic curiosity. It is goal-directed uncertainty reduction.

A system should not investigate forever. Nor should it investigate every possible uncertainty. Investigation is justified when the answer could materially change the action, the confidence level, the escalation path, or the applicability of a prior model update.

This connects the framework to bounded rationality, information foraging, value-of-information reasoning, and rational metareasoning. Systems do not search indefinitely. They allocate attention and search effort under constraints. [Simon, 1955] [Pirolli & Card, 1999] [Howard, 1966] [Russell & Wefald, 1991]

Consider the healthcare campaign example.

The system has inferred: Goal (qualified demo requests), likely ICP (cardiology practice administrators), policy (avoid unsupported clinical claims), interpretation (workflow burden is likely a stronger message than product features).

It has enough to propose a direction. But it detects a confidence gap: Are we targeting practices already evaluating RPM, or creating demand among problem-aware but not-yet-shopping buyers?

That uncertainty matters because it changes the campaign. If the audience is already evaluating RPM, the campaign should emphasize workflow fit, reimbursement readiness, implementation support, and demo conversion. If the audience is problem-aware but not shopping, the campaign should educate the market, name the operational pain, and use softer conversion paths.

The system therefore investigates by asking one targeted question. This is low-friction discovery because the system does not push the entire reasoning burden onto the marketer. It retrieves, infers, proposes, and asks only where uncertainty materially affects the output.

---

## 6.4 Task Spawning

Investigation can spawn sub-investigations.

A single unresolved question may reveal multiple possible explanatory paths.

For example: Demo requests are lower than expected. This prediction error may spawn several investigations: Was the audience wrong? Was the message wrong? Was the offer weak? Was the channel mismatched? Was buying readiness overestimated? Was the measurement plan flawed? Was the prior model update misapplied?

Each path may require different evidence.

This matters for agent systems because naive investigation can explode. A system that spawns every possible sub-question becomes slow, expensive, and annoying. A system that spawns too few may miss the failed premise.

Task spawning should therefore be governed by goal relevance, confidence, connectivity, and expected action impact.

The question is not: *What else could we investigate?*

The question is: *Which unresolved question could change what we do next?*

This preserves the bounded nature of the optimizer.

---

## 6.5 Sufficiency

**Sufficiency** is the point at which additional information is unlikely to materially change the selected action.

Sufficiency is not certainty.

This is one of the most important distinctions in the framework.

A system may be uncertain about the full causal explanation but still have enough information to act. Conversely, a system may be confident about one fact but still lack enough information to choose the right action.

Sufficiency is action-relative. It asks: *Would more information materially change what we should do?*

This concept is directly downstream of bounded rationality and satisficing. Decision-makers rarely optimize with complete information. They search until they reach a threshold that is good enough for action under the circumstances. [Simon, 1955]

The framework distinguishes confidence from sufficiency.

**Confidence** asks: How much do we trust this observation, source, explanation, or assumption?

**Sufficiency** asks: Is the available information enough to act?

These can diverge.

**Low Confidence, High Sufficiency:** A system may have low confidence in the exact explanation but high sufficiency for the action. Example: We do not yet know whether the campaign underperformed because of message, channel, or audience. But all plausible explanations suggest we should pause spend and investigate before scaling. The explanation is uncertain. The action is stable.

**High Confidence, Low Sufficiency:** A system may have high confidence in one fact but low sufficiency for action. Example: We are confident that workflow-pain messaging generated engagement. But we do not know whether that engagement came from qualified buyers. The fact is trusted. The decision is not yet stable.

This distinction helps explain hallucination and unsafe action. Hallucination occurs when the system treats plausible completion as sufficient despite insufficient evidence. Unsafe action occurs when the system treats a path as sufficient despite unresolved policy, confidence, or consequence gaps.

Sufficiency is therefore the motion threshold that converts investigation into action.

---

## 6.6 Action

**Action** is the selected behavior produced by optimizer motion.

In human-agent systems, action may include: answering a question, generating text, sending an email, calling a tool, updating a record, recommending a decision, refusing a request, escalating to a human, asking a clarification, launching a campaign, or triggering an automation.

Action is not always "doing the requested task." Sometimes the correct action is to pause, ask, escalate, refuse, retrieve more evidence, or produce a bounded draft rather than final output.

This is important because many systems treat user-request completion as the default action. But a topography-aware system treats action as the output of reasoning state and sufficiency, not mere instruction following.

For example, a marketer asks: "Write a healthcare campaign about reducing readmissions."

A context-only system may generate the campaign.

A topography-aware reasoning system may respond differently:

> I can draft a campaign around patient monitoring and care coordination, but "reducing readmissions" is a clinical outcome claim. I need approved evidence before using that claim externally. I can either use softer language now or route this for claims review.

That response is action. It is not failure to act. It is policy-aware motion through the topography.

---

## 6.7 Motion in the Healthcare Campaign Example

Return to the running example.

The marketer says: "I want to do a healthcare campaign."

The system retrieves existing artifacts and infers an optimizer state: Goal (generate qualified demo requests), Policy (avoid unsupported healthcare claims), Interpretation (practice-level operators likely respond to workflow burden and patient visibility).

The topography contains: visible ICPs, accessible prior campaign learning, represented sales objections, moderate confidence in workflow-pain messaging, strong policy constraints around clinical claims, connectivity between prior feature-led failure and current campaign direction.

The motion sequence unfolds:

**Attraction:** The system is attracted to a workflow-pain-led campaign because it connects the goal, ICP, prior learning, and sales objections.

**Investigation:** The system detects a material confidence gap: buying-stage readiness. It asks one targeted question: Are we targeting organizations already evaluating RPM, or creating demand among problem-aware but not-yet-shopping buyers?

**Sufficiency:** Once the marketer clarifies the buying stage, the system has enough to generate a campaign package. It does not need to ask every possible question. It has sufficient information to act, while preserving remaining uncertainties as prediction-error triggers.

**Action:** The system generates: campaign brief, messaging pillars, LinkedIn posts, email drip, signage concepts, commercial concepts, compliance watchlist, measurement plan. But it also preserves the reasoning state: goal, policy, interpretation, premise stack, decision state, confidence gap, sufficiency rationale, prediction-error triggers.

This is the difference between content generation and reasoning-state generation.

---

## 6.8 Motion in Safety Failures

The same motion sequence can diagnose safety failures.

### Hallucination

**Motion pattern:** Attraction (user asks factual question) → Investigation (evidence retrieval weak or skipped) → Sufficiency (plausible completion treated as enough) → Action (model answers with unsupported content).

**Topographic diagnosis:** Evidence was not sufficiently visible, accessible, or required. Confidence was miscalibrated. Unsupported completion had lower friction than grounded uncertainty.

**Design intervention:** Require evidence. Lower confidence for unsupported claims. Make "I don't know" available. Connect claims to citations. Increase friction around uncited factual assertions.

### Unsafe Tool Use

**Motion pattern:** Attraction (tool action appears goal-relevant) → Investigation (policy or consequence check weak) → Sufficiency (action appears routine enough) → Action (agent invokes unsafe tool).

**Topographic diagnosis:** Policy was not salient. Approval boundary was weak. Consequences were poorly represented. Safer alternative was less visible.

**Design intervention:** Make policy visible at tool boundary. Require approval for high-impact actions. Surface consequence previews. Connect prior failures to tool-use decisions.

### Constraint Circumvention

**Motion pattern:** Attraction (goal remains active) → Investigation (constraint interpreted as obstacle) → Sufficiency (circumvention appears useful and possible) → Action (agent attempts to bypass safeguard).

**Topographic diagnosis:** Policy was not internal to the action model. Constraint appeared as external fence. Goal gradient overpowered policy salience.

**Design intervention:** Reshape goal. Make policy part of task success. Remove incentives for circumvention. Increase connectivity between constraint and desired outcome. Audit confidence and sufficiency before action.

The point is not that all safety failures reduce neatly to a single dimension. The point is that motion analysis gives designers a more precise set of questions than moralized interpretation alone.

---

## 6.9 Motion and Design

Once behavior is understood as motion through topography, design work becomes more specific.

Designers can ask: What attracts the optimizer's attention? What does the system investigate? What does it ignore? What does it treat as sufficient? What action paths are easiest? Which paths require evidence? Which paths require escalation? Which policies are visible at the moment of action? Which prior model updates are retrieved? Which uncertainties are preserved?

This turns abstract safety and reliability goals into design levers.

To reduce hallucination, change the sufficiency threshold for factual claims. To reduce unsafe action, alter tool affordances and approval boundaries. To improve campaign quality, make prior campaign learning visible and connected. To improve organizational learning, preserve prediction errors as Model Update Objects. To reduce user burden, retrieve and infer before asking questions. To improve discovery, learn which interaction patterns produce better reasoning state.

The framework therefore treats system design as topography design.

Not every path should be blocked. Not every uncertainty should trigger escalation. Not every action should require human approval. The design challenge is to shape the landscape so that the optimizer can move effectively while making unsafe, unsupported, or low-confidence paths less attractive, less available, or less sufficient.

---

## 6.10 Transition to Learning

Motion explains how an optimizer acts. But action is not the end of the loop.

Reality responds.

A campaign performs or fails. A user accepts or rejects an answer. A tool action succeeds or causes damage. A generated claim passes or fails review. A recommendation improves the workflow or exposes a mistaken premise.

When reality responds differently than expected, the system encounters prediction error.

The next section describes how prediction error becomes learning.

The key distinction:

> A bad outcome is not learning. A correction is not learning. A postmortem is not learning. Learning occurs when prediction error is investigated, explained with evidence, and converted into a model update that changes future behavior.

---

### Citation Debt — Section 6

**Used:**
- [Ng et al., 1999]
- [Gibson, 1979]
- [Norman, 1988]
- [Simon, 1955]
- [Simon, 1955]
- [INFORMATION_FORAGING]
- [VALUE_OF_INFORMATION]
- [RATIONAL_METAREASONING]

**Likely needed:**
- [BOUNDED_RATIONALITY_SURVEY]
- [REINFORCEMENT_LEARNING_REWARD_DESIGN]
- [HCI_HUMAN_AI_COLLABORATION]
- [AI_SAFETY_EVALS]
- [GROUNDING_CITATION_GENERATION]
- [UNCERTAINTY_CALIBRATION]
- [TOOL_USE_AGENTS]
- [HUMAN_OVERSIGHT_AUTONOMY]

### Draft Notes — Section 6

This section intentionally:
- Defines gradients as directional pressures, not formal mathematical gradients
- Connects gradients to but distinguishes them from reward shaping and affordances
- Defines the motion sequence: Attraction → Investigation → Sufficiency → Action
- Distinguishes Action Attraction from Exploration Attraction
- Explains task spawning without opening infinite investigation
- Distinguishes Confidence from Sufficiency
- Uses the healthcare campaign example to make motion concrete
- Applies motion analysis to hallucination, unsafe tool use, and constraint circumvention
- Sets up Section 7 on Learning

---

# 7. Hallucination and Harmful Action as Related Failures

The previous section described behavior as optimizer motion through perceived topography. This section applies that motion model to two failure modes often treated as separate: hallucination and harmful agentic action.

They are not the same failure. A fabricated answer and an unsafe tool action differ in consequence, mechanism, and risk. A hallucinated citation may mislead a reader. A harmful agentic action may send an email, leak data, alter a system, trigger a workflow, or cause operational damage. The stakes are different.

But at the level of reasoning state, they often share a common structure.

Both can occur when a system moves from insufficiently grounded perception to premature sufficiency.

In hallucination, the system treats a plausible completion as sufficiently supported.

In harmful action, the system treats a risky path as sufficiently available, useful, or permissible.

In both cases, the failure is not merely that the model "made something up" or "chose badly." The deeper failure is that the system's perceived topography allowed an unsupported or unsafe path to become attractive enough, confident enough, or frictionless enough to produce action.

This connection matters because it suggests that hallucination mitigation and agent safety are not wholly separate design problems. Both require shaping the environment through which the system moves: evidence, confidence, policy, tool access, escalation, uncertainty, and learning must appear at the right moment in the workflow.

---

## 7.1 Hallucination as Premature Sufficiency

Hallucination is commonly defined as the production of plausible but unsupported content. In language-model systems, this may include fabricated facts, nonexistent citations, incorrect summaries, invented policies, false claims about data, or confident answers beyond available evidence. [Menick et al., 2022] [Lewis et al., 2020]

The topography frame describes hallucination as a motion failure.

The user asks a question. The system is attracted toward answering because answering satisfies the immediate goal. If evidence is not visible, not accessible, poorly represented, or not required, the system may still find a fluent path to completion. The output feels coherent. The answer fits the prompt. The model can produce language that resembles knowledge.

The issue is that plausible completion becomes easier than grounded uncertainty.

**Motion pattern:** Attraction (user asks a question) → Investigation (evidence search skipped, weak, or insufficient) → Sufficiency (plausible completion treated as enough) → Action (unsupported content produced).

This is why hallucination is not only a factuality problem. It is also a sufficiency problem. The system reaches the point of action before evidence warrants the claim.

A better-designed topography changes that motion. It makes evidence visible and accessible. It represents source support clearly. It lowers confidence when support is weak. It allows uncertainty. It makes "I do not know" or "I do not have enough evidence" a valid action. It connects factual claims to citation requirements. It increases friction around unsupported assertions.

The result is not simply a better answer. It is a different path through the information environment.

---

## 7.2 Harmful Action as Premature Sufficiency

Harmful agentic action follows a related pattern, but the action space is broader.

An agent may have tools, permissions, memory, autonomy, and the ability to affect systems outside the chat. It may send messages, retrieve private information, update records, trigger workflows, make recommendations, or operate across multi-step plans.

When such a system acts harmfully, the failure may be described as deception, evasion, goal misalignment, unsafe autonomy, or policy violation. Those descriptions may sometimes be appropriate. But the topography frame asks a more diagnostic question:

> What made the harmful action appear attractive, available, permissible, or sufficient?

**Motion pattern:** Attraction (tool action appears useful for active goal) → Investigation (policy, consequence, evidence, or approval checks are weak) → Sufficiency (action appears safe enough, routine enough, or necessary enough) → Action (agent invokes the tool or completes the unsafe step).

For example, an agent may send an external message because the goal is to complete a task quickly, the send tool is available, approval is not required, policy is weakly represented, and the consequences are not salient.

Or an agent may access sensitive information because it appears relevant to the goal, permission boundaries are broad, privacy policy is not connected to retrieval, and the system lacks a meaningful escalation threshold.

Or an agent may attempt to bypass a constraint because the active goal remains attractive while the constraint appears as an external obstacle rather than as part of task success.

In each case, the harmful action is not explained by goal alone. It emerges from the interaction among goal, policy, interpretation, tool affordances, confidence, action cost, and perceived sufficiency.

---

## 7.3 The Shared Failure Grammar

Hallucination and harmful action share a failure grammar:

> Goal pressure + weak grounding or weak constraint + misplaced confidence + insufficient investigation + low-friction action path = premature sufficiency.

The output differs. The structure rhymes.

**For hallucination:** Goal pressure (answer the user) + weak grounding (evidence not retrieved or not required) + misplaced confidence (plausible completion feels adequate) + low-friction path (generate fluent answer) = unsupported claim.

**For harmful action:** Goal pressure (complete the task) + weak constraint (policy not salient or not enforceable) + misplaced confidence (action appears routine or justified) + low-friction path (invoke tool or proceed) = unsafe action.

This does not mean hallucination and harmful action should be governed identically. They require different controls. But they can be analyzed with the same core questions:

What was the active goal? What information was visible? What was accessible? How was it represented? What was trusted? What was connected to the action? What uncertainty remained? What was treated as sufficient? What paths were easiest? What policies exerted force?

These questions move failure analysis away from vague descriptions and toward design diagnosis.

---

![Motion and Premature Sufficiency](paper_assets/svg/fig4_motion_and_premature_sufficiency.svg)

*Figure 4 — Motion and Premature Sufficiency.*

---

## 7.4 Why More Context Is Not Enough

A common response to hallucination is to add retrieval. A common response to unsafe agent behavior is to add policy. Both are useful. Neither is enough by itself.

A retrieved source does not guarantee grounded action. A written policy does not guarantee constrained behavior.

The source must be visible, accessible, represented clearly, trusted appropriately, connected to the claim, and used in sufficiency judgment.

The policy must be visible, accessible, represented clearly, trusted as binding, connected to the tool path, and able to alter the action.

This is why context and policy must become part of the perceived topography.

A model that retrieves a source but does not connect it to the generated claim may still hallucinate. An agent that retrieves a policy but does not connect it to tool use may still act unsafely. A system that shows a warning but allows one-click override may create the appearance of governance while preserving the unsafe gradient.

A system that requires citation for every factual claim changes the path. A system that requires approval for high-impact tool use changes the path. A system that surfaces prior model updates at decision time changes the path. A system that treats uncertainty as a valid reason to ask, abstain, or escalate changes the path.

The design problem is not only information availability. It is behavioral force.

---

## 7.5 Two Cases: Unsupported Claims and Unsafe Actions

The relationship can be made concrete by comparing two cases.

### Case A: Unsupported Claim

A healthcare marketing agent is asked to write campaign copy:

> Write an ad saying our remote patient monitoring platform reduces readmissions.

A weak system may produce:

> Reduce readmissions with our remote patient monitoring platform.

The failure is not merely wording. The phrase makes a clinical outcome claim. If the system lacks approved evidence, the claim should not be treated as sufficient for external campaign use.

**Topographic diagnosis:** Healthcare claims policy was not connected to generation. Evidence requirements were not visible at the claim level. The system treated plausible benefit language as sufficient. No approval path was triggered.

**Better response:**

> I can draft this, but "reduces readmissions" is a clinical outcome claim. I need approved evidence before using it externally. I can use softer language now, such as "supports earlier visibility into patient risk," or route the claim for review.

This is not less capable behavior. It is better-shaped behavior.

### Case B: Unsafe Tool Action

An operations agent is asked to resolve an incident:

> The service is slow. Fix it.

A weak system may identify a visible symptom and restart a service automatically.

If the prior incident history shows that restarting during this failure pattern can cause data loss, then the agent's action is unsafe.

**Topographic diagnosis:** Prior incident learning was not visible. Restart risk was not connected to the symptom. Tool action had low friction. Escalation did not appear as the safer sufficient path.

**Better response:**

> This resembles a prior incident pattern where restart increased data-loss risk. I am not restarting automatically. I recommend checking queue depth and replication lag first, then escalating if the pattern matches the prior failure.

Again, the difference is not merely more context. It is the connection among prior learning, current signal, policy, tool affordance, confidence, and sufficiency.

---

## 7.6 The Role of "I Don't Know" and "I Should Not Act Yet"

Evidence-backed generation systems have emphasized the importance of allowing a model to say that it does not know when evidence is insufficient. [Menick et al., 2022]

Agentic systems need an analogous action form:

> I should not act yet.

This is not refusal as a blanket safety behavior. It is a sufficiency judgment.

The system may say: "I do not have enough evidence to make that claim." Or: "I do not have enough confidence to invoke that tool." Or: "This action requires approval." Or: "This uncertainty could materially change the decision." Or: "The safer sufficient action is to ask one clarification."

These responses are often treated as friction. In a topography-aware system, they are essential motion options.

A system that cannot say "I don't know" is pushed toward hallucination. A system that cannot say "I should not act yet" is pushed toward unsafe autonomy. A system that cannot escalate is pushed toward overconfident self-resolution. A system that cannot preserve uncertainty is pushed toward false closure.

Therefore, uncertainty expression, abstention, clarification, and escalation are not merely guardrails. They are action affordances that reshape the topography.

---

## 7.7 Same Pattern, Different Severity

The paper should be careful here.

Hallucination and harmful action should not be collapsed into one undifferentiated category. Their severity differs. Their mitigations differ. Their evaluation methods differ. Their operational consequences differ.

The claim is narrower:

> Hallucination and harmful action can share a reasoning-state structure: premature sufficiency under poorly shaped topography.

That shared structure is useful because it allows designers to reuse diagnostic questions across reliability and safety domains.

For a hallucination, ask: What evidence was missing? Why was plausible completion sufficient? Why was uncertainty not expressed?

For harmful action, ask: What constraint was weak? Why was the action sufficient? Why was escalation not selected?

For both, ask: *What path did the topography make easiest?*

That final question is the bridge between reliability engineering and safety engineering.

---

## 7.8 Implications for Evaluation

If the framework is right, evaluation should not inspect only final outputs. It should inspect the reasoning state that produced them.

For hallucination, evaluation should ask: Was the claim supported? Was the source visible? Was the source connected to the claim? Was confidence appropriate? Was uncertainty expressed when support was insufficient?

For agentic action, evaluation should ask: Was the active goal clear? Was relevant policy visible? Was the tool action permitted? Was approval required? Were consequences represented? Was prior learning retrieved? Was sufficiency justified?

This means evaluation artifacts should preserve more than pass/fail results. They should preserve the state transition: goal, policy, interpretation, visible information, confidence, investigation path, sufficiency rationale, action, outcome, prediction error.

Without that state transition, a failed evaluation may produce a fix but not learning. The team may patch a symptom, add a rule, or block an action without understanding the topography that made the failure likely.

This is where the paper transitions from failure analysis into learning.

---

## 7.9 Transition to Learning

Hallucination and harmful action reveal the same deeper need: systems must not only act; they must learn from the gap between expected and observed outcomes.

A hallucinated answer should not merely be corrected. The system should identify why unsupported completion became sufficient and update the relevant model, policy connection, confidence threshold, or evidence requirement.

A harmful action should not merely be blocked next time. The system should identify why the action appeared permissible, useful, or sufficient, and update the relevant topography, tool boundary, policy representation, or model of risk.

A failed campaign should not merely be remembered. The system should identify which premise failed, under what conditions, and how future campaign reasoning should change.

This requires a distinction that the next section develops:

> Outcome is not learning. Correction is not learning. Postmortem is not learning. Learning occurs when prediction error is investigated, explained with evidence, and converted into a bounded model update.

---

### Citation Debt — Section 7

**Used:**
- [Menick et al., 2022]
- [Lewis et al., 2020]
- [GROUNDING_CITATION_GENERATION]

**Likely needed:**
- [AI_SAFETY_EVALS]
- [Lynch et al., 2025]
- [OpenAI, 2025]
- [Google DeepMind, 2024]
- [UNCERTAINTY_CALIBRATION]
- [ABSTENTION_IN_LLM_SYSTEMS]
- [TOOL_USE_AGENTS]
- [HUMAN_OVERSIGHT_AUTONOMY]
- [AI_GOVERNANCE]

### Draft Notes — Section 7

This section intentionally:
- Avoids claiming hallucination and harmful action are identical
- Identifies their shared reasoning-state structure
- Frames hallucination as premature sufficiency under weak grounding
- Frames harmful action as premature sufficiency under weak constraint / weak consequence modeling
- Connects "I don't know" to "I should not act yet"
- Introduces abstention, clarification, and escalation as valid actions
- Prepares the transition into Learning

---

# 8. Learning: When Reality Pushes Back

The previous section described hallucination and harmful action as related failures of premature sufficiency. In both cases, the system moved to action before grounding, policy, confidence, or consequence modeling justified the path.

But identifying failure is not enough.

A system can fail, be corrected, and still not learn. A campaign can underperform and still leave the organization no smarter. An agent can be blocked from a tool action and still repeat the same failure pattern under a different label. A postmortem can describe what happened without changing future behavior.

This section defines learning as the mechanism by which reality changes the optimizer.

The framework uses a narrow definition:

> Learning is an evidence-supported model update triggered by prediction error.

A bad outcome is not learning. A correction is not learning. A reaction is not learning. A postmortem is not necessarily learning. Learning occurs only when an expectation is violated, the mismatch is investigated, an evidence-supported explanation is formed, and the resulting model update changes future reasoning or behavior. [Argyris & Schön, 1978] [Cyert & March, 1963]

The basic learning sequence is:

```
Expectation → Action → Outcome → Prediction Error → Investigation → Evidence-Supported Explanation → Model Update
```

This sequence closes the loop opened in the earlier sections. The optimizer acts through perceived topography. Reality responds. If reality responds differently than expected, the system has an opportunity to learn.

But learning is not automatic.

---

## 8.1 Expectation

Learning begins with expectation.

An expectation is what the optimizer believed would happen, either explicitly or implicitly, before action.

In the healthcare campaign example, the system may expect: "Workflow-pain-led messaging will attract qualified demo requests from cardiology practice administrators."

In a grounded-generation system, the model may expect: "The retrieved source supports the factual claim."

In an operations workflow, an agent may expect: "Restarting the service will resolve the slowdown without causing downstream damage."

Expectations matter because prediction error cannot be identified without something to compare reality against.

If no expectation is preserved, the organization can observe an outcome but fail to know whether that outcome was surprising. A campaign generated fifty demo requests. Is that good? It depends on the expectation. An agent escalated instead of acting. Was that appropriate? It depends on the expected risk. A model cited three sources. Did they support the claim? It depends on the expected relationship between source and assertion.

This is why reasoning state must preserve more than action. It must preserve what the optimizer expected before acting.

---

## 8.2 Action

Action converts expectation into contact with reality.

The action may be a campaign launch, a generated answer, a tool invocation, an escalation, a refusal, a recommendation, or a workflow step.

In the framework, action is important not only because it produces effects, but because it tests the optimizer's current model.

Every action implies a belief about the world. A campaign implies a belief about audience, message, timing, offer, channel, and conversion path. A generated answer implies a belief about evidence, source support, and user need. A tool invocation implies a belief about system state, permission, consequence, and risk. An escalation implies a belief that autonomous action is not yet sufficient.

The action externalizes the optimizer's current state. It turns Goal, Policy, Interpretation, topography, investigation, and sufficiency into a behavior that reality can accept, reject, complicate, or contradict.

This is why the framework treats action as part of learning, not merely as output.

---

## 8.3 Outcome

Outcome is reality's response.

A campaign performs. A user reacts. A compliance reviewer approves or rejects. A workflow succeeds or fails. A tool action resolves the issue or creates a new one. A factual answer is verified or exposed as unsupported.

Outcome is not learning. It is evidence that learning may be needed.

The outcome alone does not explain what should change.

A weak system reacts to outcomes. A learning system investigates the gap between expectation and outcome.

---

## 8.4 Prediction Error

**Prediction error** is the mismatch between expected and observed outcome.

Prediction error is the trigger condition for learning.

It asks: What did we expect? What happened instead? Why does the difference matter?

Prediction error may be positive or negative. A campaign may outperform expectations. A model may abstain correctly under uncertainty. An agent may escalate and prevent harm. A workflow may succeed for a reason different from the one assumed.

Learning should not only occur after failure. It should occur when reality meaningfully contradicts the model, even if the outcome is favorable.

For the healthcare campaign example:

> **Expectation:** Workflow-pain-led messaging will drive qualified demo requests.
> **Outcome:** Workflow-pain messaging drove high engagement but low qualified demo conversion.
> **Prediction Error:** Workflow pain attracted attention, but did not reliably indicate buying readiness.

This prediction error is useful because it identifies the gap between attraction and conversion. The message worked at one stage but failed at another.

Without prediction error, systems often learn the wrong lesson. They may say "Healthcare campaigns do not work" when the actual lesson is "Workflow pain creates attention, but buying-stage readiness is needed for qualified demo conversion." They may say "Do not use automation for incident response" when the actual lesson is "Do not restart automatically when replication lag exceeds a defined threshold."

Prediction error prevents vague reaction from masquerading as learning.

---

## 8.5 Investigation

Prediction error triggers investigation.

Investigation asks why the expected outcome and observed outcome diverged.

This step is essential because the first explanation is often wrong.

A campaign underperforms. The team blames the creative. But the actual issue may be buying stage, channel, offer, targeting, sales follow-up, measurement, or timing. A model hallucinates. The team blames the model. But the actual issue may be retrieval failure, source representation, confidence calibration, missing citation requirements, or a prompt that rewards fluency over grounded uncertainty. An agent takes an unsafe action. The team blames autonomy. But the actual issue may be tool affordance, weak policy salience, poor consequence modeling, missing prior learning, or a goal that overpowered constraints.

Investigation protects learning from false explanation.

It should examine: the prior expectation, the premise stack, the action taken, the observed outcome, the evidence available before action, the evidence available after outcome, the confidence assigned, the policy constraints, the alternatives considered, the sufficiency rationale, and the boundary conditions.

This is why learning requires evidence-supported explanation.

---

## 8.6 Evidence-Supported Explanation

An **evidence-supported explanation** connects the prediction error to a plausible cause with enough support to justify updating the model.

It is not a guess. It is not a convenient story. It is not the loudest stakeholder's interpretation. It is not a post-hoc rationalization. It is an explanation constrained by evidence.

For the healthcare campaign example:

> **Weak explanation:** The campaign failed.
> **Better explanation:** Workflow-pain messaging attracted problem-aware operators, but many were not actively evaluating RPM. The campaign created attention but lacked buying-stage qualification.

For a hallucination case:

> **Weak explanation:** The model made it up.
> **Better explanation:** The retrieval result was semantically related but not evidentially sufficient. The system lacked a claim-level support check and treated related content as direct substantiation.

For an unsafe tool-use case:

> **Weak explanation:** The agent should not have had tools.
> **Better explanation:** The agent lacked a consequence model for the tool under this system state, and the prior incident learning was not connected to the action boundary.

The better explanations are more useful because they identify what must change.

---

## 8.7 Model Update

A **model update** changes future reasoning.

It may update:

- **Goal** — what the system is optimizing for
- **Policy** — what the system may do, must do, must not do, or must escalate
- **Interpretation** — what the system believes information means or what actions are expected to produce outcomes

### Goal Update

Example: Old goal: "Generate demo requests." Updated goal: "Generate qualified demo requests from organizations already showing buying-stage readiness." The system learned that volume alone was insufficient.

### Policy Update

Example: Old policy: "Avoid unsupported clinical claims." Updated policy: "Any campaign claim implying clinical outcome improvement requires approved evidence or review before external use." The system learned that the previous policy was too vague to govern claim-level generation.

### Interpretation Update

Example: Old interpretation: "Workflow pain is a strong buying signal." Updated interpretation: "Workflow pain is a strong attention signal, but not sufficient evidence of buying readiness."

Interpretation updates may include signal meaning, causal explanation, and action model.

The action model is especially important. It defines which actions are expected to produce which outcomes under which conditions. Example: Old action model: "Lead with workflow burden to drive demos." Updated action model: "Lead with workflow burden to attract attention; add buying-stage qualification to drive qualified demos."

---

## 8.8 Reaction Is Not Learning

The framework sharply distinguishes reaction from learning.

A reaction changes behavior without adequately explaining the prediction error.

Example: "Campaign underperformed. Reaction: Stop targeting healthcare." Learning would ask: Which healthcare audience? Which message? Which offer? Which channel? Which buying stage? Which prior premise failed? What evidence supports the explanation? What boundary conditions apply?

Another reaction: "Model hallucinated. Reaction: Never let the model answer without human review." Learning would ask: Was retrieval weak? Was citation required? Was confidence miscalibrated? Did the claim exceed the evidence? Was abstention available?

Another reaction: "Agent took unsafe action. Reaction: Remove all tools." Learning would ask: Which tool? Under what conditions? What policy was missing? What consequence was invisible? What approval boundary failed? What prior learning was not retrieved?

Reactions can be necessary as temporary safety measures. If a system is causing harm, stopping it may be the right immediate action. But emergency correction is not the same as model update.

The test is simple: *Does the change make future reasoning more accurate under defined conditions?*

If not, the system may have reacted without learning.

---

## 8.9 Postmortem Is Not Learning

Postmortems are useful, but they are not automatically learning.

A postmortem may describe what happened, who was involved, when it occurred, what was impacted, and what immediate fixes were made. Those are valuable records.

But a postmortem becomes learning only when it updates the model that will shape future behavior.

For the framework, a learning-ready postmortem must identify: the prior expectation, the premise stack, the prediction error, the evidence-supported explanation, the update target, the model update, the applicability boundary, and the confidence level.

Without these elements, the postmortem may remain narrative memory.

Narrative memory can be read. Model updates can be reused.

This distinction becomes central in the next section, which introduces Model Update Objects as the durable representation of learning.

---

## 8.10 Learning in the Healthcare Campaign Example

### Prior Expectation
Workflow-pain-led messaging will generate qualified demo requests from cardiology practice administrators.

### Action
The system generates and launches a workflow-pain-led campaign.

### Outcome
The campaign generates strong engagement and moderate demo requests, but a lower-than-expected qualified-demo rate.

### Prediction Error
Workflow pain attracted attention, but did not reliably indicate buying readiness.

### Investigation
The system reviews: lead quality, sales feedback, demo conversion, message performance, audience segments, buying-stage indicators, prior campaign comparisons.

### Evidence-Supported Explanation
Practice-level operators resonated with the workflow burden message, but many were problem-aware rather than actively evaluating RPM. The campaign succeeded as an attention mechanism but underperformed as a qualified-demo mechanism.

### Model Update
For cardiology RPM campaigns, workflow burden should be treated as an attention signal, not sufficient buying intent. Campaigns optimized for qualified demos should include buying-stage readiness filters, such as current evaluation activity, reimbursement planning, platform comparison, implementation timeline, or explicit demo-seeking behavior.

This update changes future campaign reasoning.

The next time a marketer says "I want to do a healthcare campaign," the system should not simply retrieve the old campaign. It should retrieve the model update and ask a better question: "Are we targeting organizations already evaluating RPM, or creating demand among problem-aware but not-yet-shopping buyers?"

That is learning.

---

## 8.11 Learning in Agent Safety

### Prior Expectation
The agent can safely send follow-up emails when a ticket is marked resolved.

### Action
The agent sends a follow-up email after a ticket status changes to resolved.

### Outcome
The email is sent before the customer-facing issue is actually ready for communication.

### Prediction Error
Operational resolution did not equal communication readiness.

### Investigation
The system reviews: ticket state, customer communication history, internal resolution notes, approval policy, prior complaints, agent decision trace.

### Evidence-Supported Explanation
The agent interpreted internal ticket resolution as external communication readiness. The workflow lacked a separate customer-communication readiness signal and did not require confirmation before sending.

### Model Update
For customer-facing follow-up, resolved ticket status is not sufficient. The agent must confirm communication readiness or route to a human when resolution status and customer-facing readiness are not explicitly connected.

This update is more useful than simply blocking all follow-up emails. It changes the action model. It preserves the distinction between operational state and communication state. It creates a new sufficiency requirement. It gives future agents a better path.

---

## 8.12 Learning Changes the Topography

Learning does not only change what the system believes. It changes the perceived topography future optimizers navigate.

A model update can make a prior lesson visible. It can make a failed premise accessible. It can represent a postmortem as reusable reasoning. It can change confidence in a signal. It can connect a prior outcome to a future decision.

In topography terms, learning reshapes the landscape.

Before learning: Workflow pain → treated as buying intent. After learning: Workflow pain → attention signal; Buying readiness → qualification signal.

Before learning: Ticket resolved → safe to email customer. After learning: Ticket resolved → internal state; Communication readiness → separate required signal.

Before learning: Related evidence → sufficient support for claim. After learning: Related evidence → insufficient unless claim-level support exists.

Learning therefore modifies future attraction, investigation, sufficiency, and action.

This is why the framework treats learning as part of the adaptive loop, not an after-action report.

---

## 8.13 The Learning Loop

The learning loop can now be stated formally:

```
Optimizer State → Motion through Information Topography → Action → Outcome → Prediction Error → Investigation → Evidence-Supported Explanation → Model Update → Updated Optimizer State / Updated Topography
```


![Learning Is Model Change](paper_assets/svg/fig5_learning_is_model_change.svg)

*Figure 5 — Learning Is Model Change.*

This loop is the difference between a system that repeats patterns and a system that adapts.

However, the loop still needs a durable representation.

If the model update lives only in a meeting, Slack thread, analyst note, or informal memory, it may not shape future behavior. If it is written as a vague lesson, it may be overgeneralized. If it lacks boundary conditions, it may be misapplied. If it lacks evidence, it may become folklore. If it lacks confidence, it may become dogma.

The next section introduces the object designed to preserve learning without collapsing it into vague memory:

> Model Update Object

---

### Citation Debt — Section 8

**Used:**
- [Argyris & Schön, 1978]
- [Cyert & March, 1963]
- [ORGANIZATIONAL_LEARNING]

**Likely needed:**
- [Argyris & Schön, 1978]
- [Cyert & March, 1963]
- [ORGANIZATIONAL_MEMORY]
- [DECISION_PROVENANCE]
- [POSTMORTEM_PRACTICES]
- [INCIDENT_LEARNING]
- [MACHINE_LEARNING_FEEDBACK_LOOPS]
- [HUMAN_AI_FEEDBACK]
- [UNCERTAINTY_CALIBRATION]

### Draft Notes — Section 8

This section intentionally:
- Defines learning narrowly as evidence-supported model update triggered by prediction error
- Distinguishes outcome, correction, reaction, and postmortem from learning
- Ties learning back to optimizer primitives: Goal, Policy, Interpretation
- Preserves Action Model as an Interpretation subtype
- Uses the healthcare campaign example as the primary running example
- Adds an agent-safety example involving communication readiness
- Explains that learning reshapes future topography
- Sets up Section 9 on Model Update Objects

---

# 9. Model Update Objects: Making Learning Durable

The previous section defined learning as an evidence-supported model update triggered by prediction error.

That definition creates a practical problem.

Where does the learning go?

If learning remains in a meeting, it becomes memory. If it remains in a postmortem, it becomes documentation. If it remains in a Slack thread, it becomes searchable residue. If it remains in one person's head, it becomes expertise. If it is summarized vaguely, it becomes folklore.

None of these are sufficient for human-agent systems that must reuse learning across time, teams, workflows, and agents.

This section introduces the **Model Update Object**.

A Model Update Object is a bounded, reusable record of learning. It preserves the prior expectation, the premise stack that produced that expectation, the observed outcome, the prediction error, the evidence-supported explanation, the model update, the applicability boundary, and the confidence level.

Its purpose is not simply to store what happened. Its purpose is to change future reasoning.

---

## 9.1 Why Ordinary Documentation Is Not Enough

Organizations already document many things. They write briefs, reports, incident reviews, campaign analyses, product requirements, sales notes, meeting summaries, dashboards, and postmortems. These artifacts matter. The framework does not replace them.

But ordinary documentation often fails to preserve the exact structure needed for future learning.

A campaign report may say: "Workflow messaging performed well." But a future system needs to know: Performed well against which goal? With which audience? Compared to what expectation? Under what channel conditions? With what offer? At what buying stage? What did performance mean? What should change next time?

An incident postmortem may say: "Restarting the service caused downstream data loss." But a future system needs to know: Under what system state? What prior expectation made restart seem safe? What signal was misread? Which policy failed? Which future trigger should block or escalate restart?

Ordinary documentation often preserves conclusions without preserving the reasoning transition that produced them.

The Model Update Object is designed to preserve that transition.

---

## 9.2 The Three-Layer Structure

A Model Update Object has three layers:

```
Model Update Object = Core Learning Payload + Observability Envelope + Human-Ready View
```

---

## 9.3 Core Learning Payload

The first layer is the **Core Learning Payload** — the truth layer.

It contains eleven fields:

| # | Field | Prevents |
|---|-------|---------|
| 1 | Prior Expectation | No learning delta |
| 2 | Prior Basis / Premise Stack | Premise-blind learning |
| 3 | Triggering Context / Action | Context collapse |
| 4 | Observed Outcome | Vague outcome memory |
| 5 | Prediction Error | Outcome mistaken for learning |
| 6 | Evidence / Investigation Trace | Rationalized learning |
| 7 | Explanation | Raw evidence without model change |
| 8 | Update Target | Unlocated learning |
| 9 | Model Update | Lesson too vague to guide action |
| 10 | Applicability Boundary | Overgeneralized learning |
| 11 | Confidence | False certainty |

**Prior Expectation** records what the optimizer believed would happen before action. Without it, the system cannot know what changed.

**Prior Basis / Premise Stack** records why the expectation seemed reasonable. Without it, the system may learn the wrong lesson from the right evidence. The premise stack answers: *Why did we expect this to work?*

**Triggering Context / Action** records what was done and under what conditions. Without it, a future system may overgeneralize from one context to all contexts.

**Observed Outcome** records what happened with enough specificity to support investigation.

**Prediction Error** records the mismatch between expectation and outcome. This is the hinge of learning.

**Evidence / Investigation Trace** records what evidence was examined. Without it, learning becomes rationalization.

**Explanation** states why the prediction error occurred based on evidence. Without it, evidence remains raw data without meaning.

**Update Target** identifies which part of the optimizer model should change (Goal, Policy, or Interpretation). Without it, learning is vague.

**Model Update** states the reusable change to future reasoning. A good model update is specific enough to change behavior but bounded enough to avoid overgeneralization.

**Applicability Boundary** states when the update should and should not apply. Without it, useful learning can become harmful dogma.

**Confidence** records how strongly the system should trust the update. Without it, weakly supported lessons become false certainty.

The Confidence field in a Model Update Object records how strongly the learning should shape future behavior. It is related to the topography dimension Confidence, but it is not identical: the topography dimension concerns perceived trustworthiness during reasoning, while the Model Update Object field concerns the reliability of a completed learning update.

---

## 9.4 Observability Envelope

The second layer is the **Observability Envelope** — the trust, audit, and lifecycle layer.

It may include: Object ID, Source Learning Event, Created Date, Created By, Owner/Steward, Source Artifact References, Evidence References, Version, Status, Confidence History, Supersedes/Superseded By, Usage Log, Validation Log, Last Reviewed Date, Related Updates / Conflict Flags.

Recommended status values: Provisional, Validated, Deprecated, Superseded, Rejected.

This layer matters because model updates should not become permanent doctrine by default. They need lifecycle. A model update may be provisional. It may later be validated. It may be superseded by stronger evidence. It may be deprecated when conditions change. It may conflict with another update and require investigation.

The Observability Envelope prevents: *Stale learning treated as current truth.*

---

## 9.5 Human-Ready View

The third layer is the **Human-Ready View** — the usability layer.

It may include: Title, One-Line So What, What Changed, Assumption Changed, Use This When, Do Not Use This When, Confidence/Caveat, Recommended Future Check.

Example:

> **Title:** Workflow Pain Drives Attention, Not Qualified Demo Intent
> **One-Line So What:** For cardiology RPM campaigns, workflow-burden messaging gets attention, but qualified-demo campaigns need buying-stage filters.
> **Use This When:** Building practice-level cardiology RPM campaigns optimized for qualified demo requests.
> **Do Not Use This When:** The campaign goal is awareness, education, or executive thought leadership.

The Human-Ready View is not the source of truth. It is a usability layer. The Core Learning Payload remains authoritative.

This distinction matters because human-readable summaries can drift. A short "so what" may be useful, but future systems should still be able to inspect the underlying expectation, evidence, explanation, boundary, and confidence.

---

## 9.6 Example Model Update Object

Below is an example from the healthcare campaign scenario.

> **Title:** Workflow Pain Drives Attention, Not Qualified Demo Intent
>
> **Prior Expectation:** Workflow-pain-led messaging will generate qualified demo requests from cardiology practice administrators.
>
> **Premise Stack:** ICP (cardiology practice administrators), prior campaign learning (feature-led underperformance), sales objections ("another dashboard"), product positioning (earlier visibility without staff burden), goal (qualified demo requests).
>
> **Triggering Context:** Launched workflow-pain-led RPM campaign targeting practice-level cardiology operators.
>
> **Observed Outcome:** Strong engagement and moderate demo requests, but lower-than-expected qualified-demo rate.
>
> **Prediction Error:** Workflow pain attracted attention but did not reliably indicate buying readiness.
>
> **Evidence:** Engagement above benchmark; sales feedback indicated problem-aware but not-shopping leads; demo qualification showed weak evaluation readiness; message-level performance favored workflow burden language; prior feature-led comparison supported attention benefit.
>
> **Explanation:** Practice-level operators resonated with workflow burden, but the message reached many problem-aware prospects not yet actively evaluating RPM.
>
> **Update Target:** Interpretation / Action Model
>
> **Model Update:** For cardiology RPM campaigns, workflow burden should be treated as an attention signal, not sufficient buying intent. Campaigns optimized for qualified demos should include buying-stage readiness filters.
>
> **Applicability Boundary:** Applies to practice-level cardiology RPM campaigns optimized for qualified demo requests. Does not automatically apply to awareness campaigns, executive campaigns, or other specialties without validation.
>
> **Confidence:** Medium-high. Needs validation in at least one additional campaign.
>
> **Status:** Provisional

This object can now shape future discovery. When the next marketer says "I want to do a healthcare campaign," the system can retrieve the model update and ask: "Are we targeting organizations already evaluating RPM, or creating demand among problem-aware but not-yet-shopping buyers?"

The system is not merely retrieving an old campaign. It is reusing learning.

---

## 9.7 Failure Modes Model Update Objects Prevent

Model Update Objects are designed to prevent several common failure modes:

1. **Folklore Update** — a story accepted as truth without evidence
2. **Premise-Blind Update** — learning from outcome without identifying which assumption failed
3. **Overgeneralized Update** — a lesson from one context applied everywhere
4. **Stale Update** — an old lesson active after conditions change
5. **Confidence Inflation** — a weakly supported lesson becomes doctrine
6. **Misclassified Update Target** — the system changes the wrong part of the model
7. **Policy Laundering** — a preference disguised as a rule
8. **Human-Ready Drift** — a simplified summary changes the meaning
9. **Retrieval Bias** — the system retrieves a topically similar update that does not actually apply
10. **Contradiction Suppression** — a new outcome conflicts with a prior update, but the conflict is ignored

---

## 9.8 Model Update Objects Reshape Topography

Model Update Objects are not just records. They reshape future topography.

They make prior learning visible. They make failed premises accessible. They represent learning in reusable form. They assign confidence. They connect past outcomes to future decisions.

Before the update:

> Healthcare campaign → retrieve old campaign → copy workflow-pain message → generate assets.

After the update:

> Healthcare campaign → retrieve prior model update → infer workflow pain as attention signal → detect buying-stage confidence gap → ask readiness question → generate better campaign.

The object changes motion. This is why Model Update Objects are a structural component of the framework.

---

## 9.9 Transition to Reasoning Architecture

A Model Update Object preserves one kind of reasoning transition: learning.

But human-agent systems need more than learning records. They also need to preserve optimizer state, premise stacks, decision states, investigation traces, and learning events.

Together, these objects form a broader reasoning architecture.

The next section introduces that architecture.

Its central claim:

> The unit of organizational reasoning is not the document. It is the optimizer state transition.

---

### Citation Debt — Section 9

**Used:**
- [ORGANIZATIONAL_MEMORY]
- [KNOWLEDGE_MANAGEMENT]
- [DECISION_PROVENANCE]
- [Argyris & Schön, 1978]
- [Cyert & March, 1963]

**Likely needed:**
- [LESSONS_LEARNED_SYSTEMS]
- [POSTMORTEM_PRACTICES]
- [INCIDENT_LEARNING]
- [KNOWLEDGE_REPRESENTATION]
- [Aamodt & Plaza, 1994]
- [ORGANIZATIONAL_ROUTINES]
- [AI_MEMORY_SYSTEMS]
- [HUMAN_AI_COLLABORATION]

### Draft Notes — Section 9

This section intentionally:
- Defines Model Update Objects as durable learning records
- Distinguishes learning objects from ordinary documentation
- Introduces the three-layer structure: Core Learning Payload, Observability Envelope, Human-Ready View
- Defines the eleven Core Learning Payload fields with failure-prevention mapping
- Provides a concrete healthcare campaign example
- Lists ten failure modes the object prevents
- Explains how Model Update Objects reshape future topography
- Transitions to Section 10 on Reasoning Architecture

---

# 10. Reasoning Architecture: Preserving State Transitions

The previous section introduced Model Update Objects as a durable way to preserve learning. But learning is only one kind of reasoning transition.

Human-agent systems also need to preserve the state from which action begins, the assumptions that make action appear reasonable, the decision process that selects one path over another, the investigation that reduces uncertainty, and the event in which reality contradicts expectation.

This requires a broader **Reasoning Architecture**.

The central claim is:

> The unit of organizational reasoning is not the document. It is the optimizer state transition.

Documents remain essential. They preserve source material, evidence, plans, policies, research, reports, transcripts, decisions, and postmortems. But documents alone rarely preserve the structured relationship among goal, policy, interpretation, premise, uncertainty, confidence, decision, action, outcome, and learning.

A reasoning architecture does not replace documents. It organizes the state transitions documents participate in.

---

## 10.1 Why Documents Are Not Enough

Organizations already have documents. They have strategy decks, campaign briefs, product requirements, incident reviews, dashboards, transcripts, meeting notes, knowledge bases, policies, and wikis.

These artifacts are necessary. But they are not sufficient for adaptive human-agent systems because they often leave the reasoning transition implicit.

A strategy deck may state a direction, but not preserve which alternatives were rejected. A campaign brief may state an audience, but not preserve why that audience was chosen. A dashboard may show performance, but not preserve which premise the performance tested. A postmortem may list corrective actions, but not preserve the model update that should guide future behavior. A policy may state a constraint, but not preserve where it must appear in the workflow to govern action.

When AI systems retrieve these documents, they may retrieve the artifact without retrieving the reasoning state. That is why more context can still leave the system starting cold.

Reasoning Architecture solves this by preserving the minimum viable objects needed to reconstruct and reuse reasoning state.

---

## 10.2 Six Minimum Viable Reasoning Objects

The framework defines six core reasoning objects:

| # | Object | Question |
|---|--------|----------|
| 1 | Optimizer State | What was the system trying to do, under what constraints, with what interpretation? |
| 2 | Premise Stack | Why did the system expect this action or decision to work? |
| 3 | Decision State | What was chosen, what was rejected, and why was the information considered sufficient? |
| 4 | Investigation Trace | How was uncertainty reduced? |
| 5 | Learning Event | Where did reality contradict the model? |
| 6 | Model Update Object | What reusable change should shape future reasoning? |

Together, these objects preserve the reasoning-state transition.

---

![Reasoning Architecture: Six Objects Preserve the State Transition](paper_assets/svg/fig6_reasoning_architecture_six_objects.svg)

*Figure 6 — Reasoning Architecture: Six Objects Preserve the State Transition.*

---

## 10.3 Optimizer State

The **Optimizer State** records the active Goal, Policy, and Interpretation.

Example:

> **Goal:** Generate qualified demo requests.
> **Policy:** Avoid unsupported healthcare claims. Use approved messaging. Escalate clinical outcome claims for review.
> **Interpretation:** Practice-level cardiology operators are likely to respond to workflow burden and patient visibility, but buying-stage readiness may determine demo quality.

Preserving Optimizer State prevents future systems from seeing an artifact without understanding why it was produced.

---

## 10.4 Premise Stack

The **Premise Stack** records the artifact-backed basis for a prior expectation.

It answers: *Why did we expect this to work?*

The Premise Stack may include: ICP, campaign brief, market research, customer interviews, sales objections, product positioning, prior model updates, compliance guidance, measurement plan, incident history, policy documents, executive strategy.

The Premise Stack is not the same as evidence gathered after an outcome. It is the basis that made the action seem reasonable *before* reality responded.

Without a Premise Stack, learning becomes premise-blind. The system may update the wrong assumption.

---

## 10.5 Decision State

The **Decision State** records what was chosen, what alternatives were considered, what constraints applied, and why the system judged the available information sufficient for action.

A Decision State should include: decision made, options considered, selected action, rejected alternatives, relevant constraints, tradeoffs, information surface context, confidence levels, sufficiency rationale, expected outcome.

Example:

> **Decision:** Lead with workflow burden rather than technology features.
> **Rejected Alternatives:** Clinical outcomes, reimbursement, product features.
> **Sufficiency Rationale:** Enough evidence exists to generate a strawman campaign, but buying-stage readiness remains a material confidence gap requiring clarification.

The Decision State prevents decisions from becoming unexplained artifacts.

---

## 10.6 Investigation Trace

The **Investigation Trace** records how uncertainty was reduced.

An Investigation Trace may include: initial confidence gap, questions asked, sources retrieved, policies checked, contradictions found, alternatives compared, evidence accepted, evidence rejected, human clarifications, confidence changes, remaining uncertainty.

Investigation Trace matters because reasoning often depends on the path not taken. Without it, systems are vulnerable to rationalization — a final decision explained after the fact in a way that sounds coherent but does not reflect the actual uncertainty reduction process.

Investigation Trace preserves epistemic discipline.

---

## 10.7 Learning Event

The **Learning Event** records the moment reality contradicts or materially updates expectation.

It answers: What was expected? What happened? What prediction error occurred? What investigation explained the mismatch?

Learning Events matter because not every outcome should become a reusable rule. Some are noise. Some are measurement artifacts. Some are context-specific. Some require more evidence.

The Learning Event captures the reality contact before it is promoted into a Model Update Object. This distinction prevents systems from over-learning from weak or ambiguous evidence.

---

## 10.8 Model Update Object

As described in Section 9, the **Model Update Object** preserves the reusable learning that should shape future behavior. It includes: Prior Expectation, Premise Stack, Triggering Context, Observed Outcome, Prediction Error, Evidence/Investigation Trace, Explanation, Update Target, Model Update, Applicability Boundary, and Confidence.

The Model Update Object is the durable output of learning. It allows future systems to reuse the learning without flattening it into vague advice.

---

## 10.9 Supporting Concerns, Not New Objects

The six core objects are supported by several recurring concerns:

| Concern | Question | Appears In |
|---------|----------|------------|
| Information Surface Context | What could the system see and use? | Decision State, Investigation Trace |
| Sufficiency Rationale | Why was this enough? | Decision State |
| Observability | Can this object be trusted, reviewed, updated, or retired? | Model Update Object |
| Human-Ready View | Can humans understand and use this object? | Model Update Object |
| Applicability Boundary | When is this true enough to reuse? | Model Update Object |
| Confidence | How strongly should this shape future behavior? | Multiple objects |

These supporting concerns prevent reasoning objects from becoming either too rigid or too vague.

---

## 10.10 The Objects as a State-Transition Chain

```
Optimizer State → Premise Stack → Decision State → Investigation Trace → Learning Event → Model Update Object
```

This is not always strictly linear. In practice, workflows loop and branch. But the chain captures the general structure: The system begins from a state. It acts from premises. It makes decisions. It investigates uncertainty. Reality responds. The model updates.

This is the adaptive reasoning loop in object form.

---

## 10.11 Healthcare Campaign Example

**Optimizer State:** Goal (qualified demo requests), Policy (avoid unsupported claims), Interpretation (workflow burden as attention driver, buying readiness as qualification).

**Premise Stack:** ICP (cardiology administrators), prior learning (feature-led underperformance), sales objection ("another dashboard"), product positioning (earlier visibility), measurement (qualified demo conversion).

**Decision State:** Lead with workflow burden. Rejected: clinical outcomes, product features, reimbursement. Sufficiency: prior learning and ICP support workflow pain; buying-stage readiness uncertain.

**Investigation Trace:** Asked buying-stage question. Checked prior data, sales feedback, ICP, compliance. Confidence in workflow-pain as attention driver: high. As buying-intent signal: moderate to low.

**Learning Event:** High engagement, low qualified-demo conversion. Workflow pain attracted attention but did not indicate buying readiness.

**Model Update Object:** Workflow burden = attention signal, not buying intent. Qualified-demo campaigns need buying-stage readiness filters.

The next time a marketer asks for a healthcare campaign, the system should retrieve this chain, not merely the old campaign document.

---

## 10.12 Agent Safety Example

**Optimizer State:** Goal (send follow-up email after resolution), Policy (do not send until customer-ready), Interpretation (resolved = complete).

**Premise Stack:** Ticket workflow design, support automation policy, prior assumption that resolved = customer-ready.

**Decision State:** Send automatically. Rejected: ask human for readiness. Sufficiency: resolved status seemed enough.

**Investigation Trace:** Before action, investigation was weak. System did not check whether internal resolution = external readiness.

**Learning Event:** Email sent before readiness. Prediction error: operational resolution ≠ communication readiness.

**Model Update Object:** Resolved status is not sufficient for customer-facing follow-up. Confirm readiness or escalate.

---

## 10.13 Relationship to Knowledge Management

Knowledge management often asks: *How do we store, retrieve, and share knowledge?*

Reasoning Architecture asks: *How do we preserve the state transitions through which knowledge changes action?*

A knowledge base may store a campaign report. A reasoning architecture stores the premise that report tested, the decision it informed, the outcome it produced, and the model update it created.

This makes Reasoning Architecture a complement to knowledge management, not a replacement. It uses knowledge artifacts as inputs, but preserves reasoning objects as the durable layer of adaptation.

---

## 10.14 Relationship to AI Agents

Agent memory is often treated as retained context, past conversation, retrieved documents, or stored facts. These are useful, but they are not enough.

An agent that remembers a fact may still fail to understand its relevance. An agent that retrieves a prior output may still repeat the failed premise behind it. An agent that stores a conversation may still lack a structured model update.

A reasoning-capable agent needs memory of state transitions: what it was trying to do, what policy constrained it, what it believed, what it considered, what it did, what happened, what changed.

The design question is: *Which reasoning objects are necessary for this workflow to improve over time?*

That question prevents both extremes: preserve nothing, and preserve everything. The goal is minimum viable reasoning preservation.

---

## 10.15 Transition to Discovery

Reasoning Architecture defines what should be preserved. But it raises a practical question:

> How do these objects get created without overburdening the human user?

A marketer should not have to manually fill out an Optimizer State, Premise Stack, Decision State, Investigation Trace, Learning Event, and Model Update Object every time they ask for a campaign.

This is the role of Discovery.

Discovery is the process by which messy human intent and organizational artifacts are converted into structured reasoning objects with the lowest necessary human burden.

The next section introduces the Discovery Framework:

> Retrieve → Infer → Propose → Confirm → Generate → Preserve → Learn

The principle is simple:

> Do the reasoning work before asking the user to do it.

---

### Citation Debt — Section 10

**Used:**
- [KNOWLEDGE_MANAGEMENT]
- [ORGANIZATIONAL_MEMORY]
- [DECISION_PROVENANCE]
- [ORGANIZATIONAL_LEARNING]
- [Aamodt & Plaza, 1994]
- [HCI_HUMAN_AI_COLLABORATION]
- [AGENT_MEMORY_SYSTEMS]

**Likely needed:**
- [March & Simon, 1958]
- [Cyert & March, 1963]
- [Argyris & Schön, 1978]
- [Weick, 1995]
- [WORKFLOW_PROVENANCE]
- [KNOWLEDGE_REPRESENTATION]
- [INCIDENT_LEARNING]
- [DESIGN_RATIONALE]

### Draft Notes — Section 10

This section intentionally:
- Expands from Model Update Objects to full Reasoning Architecture
- States the central claim that the unit of organizational reasoning is the optimizer state transition
- Defines six minimum viable reasoning objects
- Keeps supporting concerns inside the objects rather than creating object bloat
- Uses both healthcare campaign and agent safety examples
- Distinguishes reasoning architecture from ordinary knowledge management
- Distinguishes reasoning memory from generic agent memory
- Sets up Section 11 on Discovery as the low-friction way these objects are created

---

# 11. Discovery Framework: From Messy Intent to Reasoning State

The previous section defined the reasoning architecture: the set of objects required to preserve optimizer state transitions across human-agent systems.

That architecture creates a practical problem.

If every user had to manually create an Optimizer State, Premise Stack, Decision State, Investigation Trace, Learning Event, and Model Update Object, the system would fail in practice. The reasoning architecture would be theoretically complete but operationally unusable.

People do not begin work by filling out reasoning schemas.

They say things like: "I want to do a healthcare campaign." Or: "Can you draft a customer follow-up?" Or: "Help me respond to this incident." Or: "Build a launch plan."

The human intent is often partial, ambiguous, compressed, and context-dependent. Asking the user to supply all of that up front creates friction and often produces worse reasoning because the system shifts the work of structure onto the person least prepared to do it at that moment.

This section introduces the **Discovery Framework**.

Discovery is the process by which messy human intent and organizational artifacts are converted into structured reasoning objects with the lowest necessary human burden.

The basic loop is:

```
Retrieve → Infer → Propose → Confirm → Generate → Preserve → Learn
```

Discovery is not a questionnaire. Discovery is not simply requirements gathering. Discovery is not asking the user to fill in every missing field.

Discovery is the adaptive process of turning unclear intent into usable reasoning state.

The principle is:

> Do the reasoning work before asking the user to do it.

---

## 11.1 Why Discovery Matters

Discovery is where the human-agent system first determines what work is actually being requested.

This step matters because the same user request may imply different optimizer states.

Consider: "I want to do a healthcare campaign."

This could mean: brand awareness, qualified demo generation, conference activation, sales enablement, patient education, executive thought leadership, retention campaign, or partner campaign. Each implied goal changes the reasoning state.

A weak system asks blank-form questions: Who is your audience? What is your goal? What channel do you want? What message do you want? What assets do you need?

Those questions are not wrong. But they force the user to construct the reasoning state manually.

A stronger system retrieves existing context, infers likely candidates, proposes a strawman, and asks only the questions that materially affect the decision.

It might say:

> Based on existing materials, I think this is likely an RPM campaign for cardiology practice administrators, optimized for qualified demo requests. Prior learning suggests workflow burden is a strong attention driver, but buying-stage readiness determines demo quality. Should we target organizations already evaluating RPM, or problem-aware operators who are not yet shopping?

That is Discovery.

---

## 11.2 Initial Discovery and Runtime Discovery

### Initial Discovery

Initial Discovery maps the existing reasoning environment of a team, department, or organization.

It asks: What artifacts already exist? Where do decisions happen? What policies govern work? What prior lessons are stored? Where does learning currently disappear? Which workflows repeatedly start cold? Which assumptions keep recurring? Which handoffs create ambiguity? Which systems contain evidence? Which people hold tacit knowledge?

Initial Discovery is useful when designing a reasoning architecture for a team or workflow.

### Runtime Discovery

Runtime Discovery happens inside the work. It begins when a user brings a new objective, request, or proposal into the system.

Runtime Discovery converts that messy input into reasoning objects. It is the ongoing process by which the system retrieves, infers, proposes, confirms, generates, preserves, and learns.

Initial Discovery designs the map. Runtime Discovery uses and updates the map.

---

At runtime, Discovery turns messy human intent into preserved reasoning state through a structured loop:

![Runtime Discovery Loop](paper_assets/svg/fig7_runtime_discovery_loop.svg)

*Figure 7 — Runtime Discovery Loop.*

## 11.3 Retrieve

The first runtime step is **Retrieve**. The system should retrieve relevant artifacts before asking the user to manually supply what the organization already knows.

Retrieval should consider not only topical similarity but reasoning-state relevance: active or inferred goal, policy domain, audience, workflow type, prior premise stacks, decision history, model updates, applicability boundaries, and confidence levels.

The system should retrieve not only documents, but reasoning objects when they exist.

---

## 11.4 Infer

After retrieval, the system should **Infer** the likely reasoning state: probable goal, likely audience, relevant policy, current interpretation, premise stack, applicable model updates, decision options, confidence gaps, and sufficiency threshold.

Inference is not guessing carelessly. It is structured hypothesis formation. The system should make its inference visible and provisional.

Example: "I am inferring that your goal is qualified demo requests, not general awareness, because the recent campaign brief and prior performance review both emphasize pipeline quality."

Inference lets the system build a strawman reasoning state. It also lets the user correct the system efficiently. The system should prefer correctable inference over blank interrogation.

---

## 11.5 Propose

After inference, the system should **Propose** a strawman — a provisional reasoning state or work direction offered for confirmation.

A good strawman is specific enough to be useful and humble enough to be corrected. A strong proposal includes confidence markers: high confidence (practice-level operators care about workflow burden), medium confidence (cardiology administrators are the right audience), low confidence / needs confirmation (buying-stage readiness).

The proposal gives the user something to react to. That reaction is more informative than a blank form.

---

## 11.6 Confirm

After proposing, the system should **Confirm** only the uncertainties that materially affect the outcome.

The system asks the smallest number of questions needed to reach sufficiency.

Example: "Before I generate the campaign package, confirm one thing: are we targeting organizations already evaluating RPM, or creating demand among problem-aware but not-yet-shopping buyers?"

The discovery rule is: *Ask only where uncertainty could materially change the action.*

This creates low-friction collaboration. The human remains in control, but the system carries more of the reasoning burden.

---

## 11.7 Generate

After confirmation, the system can **Generate** the requested artifacts. But generation should not be treated as the only output.

In a reasoning-state system, generated artifacts are accompanied by preserved reasoning objects. The user may see only the useful artifact. The system should preserve the reasoning beneath it.

This is the difference between producing content and producing adaptive work.

---

## 11.8 Preserve

After generation, the system should **Preserve** the relevant reasoning objects. Preservation is not an afterthought. It is how the system avoids starting cold next time.

Not every task requires full preservation. The amount of preservation should match the stakes, repeatability, and learning value of the workflow.

The design question is: *What reasoning state must future humans or agents recover to act better next time?*

---

## 11.9 Learn

Discovery does not end when the artifact is generated.

If the resulting action produces an outcome, the system should compare outcome against expectation. If reality contradicts expectation, the system should create a Learning Event and, where evidence supports it, a Model Update Object.

But Discovery itself can also learn.

---

## 11.10 Discovery Pattern Updates

A **Discovery Pattern Update** is a specialized Model Update Object that records how the discovery process itself should change.

It answers: *Which interaction pattern produced better reasoning, better artifacts, lower user burden, or better outcomes?*

Example: Prior discovery pattern: ask for audience, goal, channel, and message from the user. Observed outcome: users provided inconsistent answers, often omitting buying-stage readiness. Model Update: for healthcare demo-generation campaigns, retrieve and infer ICP first, then ask one material question about buying-stage readiness.

This matters because the system should learn not only what strategies work, but how to ask better questions. A mature human-agent system improves its interaction patterns over time. Discovery Pattern Updates make that improvement durable.

---

## 11.11 The Low-Friction Principle

> The user should not have to supply information the system can responsibly retrieve, infer, or propose.

This does not mean the system should hide assumptions. It means the system should surface assumptions in a correctable form.

Bad discovery makes the user do structure. Better discovery provides structure and asks for correction.

The difference is not just user experience. It changes the quality of reasoning state captured. When the system retrieves, infers, proposes, and confirms, the resulting reasoning objects are more complete, more grounded, and more reusable.

---

## 11.12 Discovery and Human Control

Low-friction discovery should not remove human control. The framework does not recommend that systems silently infer goals and act without confirmation in high-stakes or ambiguous settings.

Instead, it recommends visible inference. The system should show: what it inferred, why it inferred it, how confident it is, what uncertainty remains, which question matters, what action it proposes.

This makes discovery collaborative. Both human and system participate in constructing a better reasoning state.

In domains involving policy, compliance, safety, customer communication, medical claims, financial claims, legal claims, or operational risk, discovery should favor: transparent assumptions, confidence labels, approval gates, policy checks, escalation paths, trace preservation.

Human control is strongest when the system makes its reasoning state inspectable.

---

## 11.13 Discovery and Safety

Discovery is also a safety mechanism. Many failures begin with a bad initial framing.

If the system infers the wrong goal, retrieves the wrong context, ignores the relevant policy, or fails to identify the material uncertainty, later safeguards may be too late.

A healthcare campaign framed as "write persuasive copy" may produce risky claims. The same campaign framed as "generate compliant, evidence-bounded external healthcare messaging for qualified demo conversion" produces a different path.

Discovery shapes the starting optimizer state. Because starting state shapes motion, discovery shapes safety.

---

## 11.14 Discovery in the Healthcare Campaign Example

**Human Intent:** "I want to do a healthcare campaign."

**Retrieve:** Healthcare messaging, cardiology ICP, prior campaign performance, sales objections, product positioning, claims policy, prior model updates, measurement guidance.

**Infer:** Likely goal (qualified demo requests), likely audience (cardiology practice administrators), relevant policy (avoid unsupported clinical claims), relevant prior learning (workflow pain attracts attention; feature-led underperforms), material confidence gap (buying-stage readiness).

**Propose:** Workflow-pain-led RPM campaign for cardiology practice administrators, optimized for qualified demo requests. Avoid unsupported clinical claims. Include measurement plan.

**Confirm:** "Are we targeting practices already evaluating RPM, or creating demand among problem-aware but not-yet-shopping buyers?"

**Generate:** Campaign brief, ICP summary, messaging pillars, LinkedIn posts, email drip, event signage, commercial concepts, compliance watchlist, measurement plan, prediction-error triggers.

**Preserve:** Optimizer State, Premise Stack, Decision State, Investigation Trace, Sufficiency Rationale.

**Learn:** After performance data: Learning Event, Model Update Object, Discovery Pattern Update.

The important point is that the generated campaign is not the only product. The reusable reasoning state is also a product.

---

## 11.15 Discovery as the Front Door to Reasoning Architecture

Reasoning Architecture defines what the system should preserve. Discovery defines how those objects are created naturally during work.

Without Discovery, the reasoning architecture becomes too heavy. Without Reasoning Architecture, Discovery becomes a better conversation but not a durable learning system.

They need each other.

The pieces now connect:

> **Optimizer State:** what the system brings. **Information Topography:** what the system navigates. **Optimizer Motion:** how behavior emerges. **Learning:** how reality updates the system. **Model Update Objects:** how learning persists. **Reasoning Architecture:** how state transitions persist. **Discovery:** how messy intent becomes structured reasoning.

This completes the framework's operational loop.

---

## 11.16 Transition to the Running Example

The next section brings the framework together in a single running example.

The healthcare campaign scenario will be treated not as a casual illustration, but as a complete workflow: messy request, retrieval, inference, strawman, confirmation, generation, decision state, measurement, outcome, prediction error, learning event, model update, discovery pattern update.

This example shows what the framework looks like when applied end to end.

It also demonstrates the paper's practical claim:

> The value of the framework is not only better AI outputs. The value is a system that helps people and agents reason, act, preserve, and learn together.

---

### Citation Debt — Section 11

**Used:**
- [HCI_HUMAN_AI_COLLABORATION]
- [MIXED_INITIATIVE_SYSTEMS]
- [HUMAN_IN_THE_LOOP_AI]
- [KNOWLEDGE_MANAGEMENT]
- [ORGANIZATIONAL_MEMORY]
- [DESIGN_RATIONALE]

**Likely needed:**
- [HUMAN_AI_INTERACTION_GUIDELINES]
- [COACTIVE_DESIGN]
- [CSCW_ORGANIZATIONAL_WORK]
- [USER_BURDEN_AUTOMATION]
- [EXPLAINABLE_AI]
- [AI_GOVERNANCE]
- [WORKFLOW_AUTOMATION]
- [AGENTIC_WORKFLOWS]

### Draft Notes — Section 11

This section intentionally:
- Defines Discovery as conversion of messy intent into reasoning state
- Distinguishes Initial Discovery from Runtime Discovery
- Introduces the runtime loop: Retrieve → Infer → Propose → Confirm → Generate → Preserve → Learn
- Emphasizes strawman-first, low-friction interaction
- Avoids turning the reasoning architecture into a giant user form
- Introduces Discovery Pattern Updates
- Connects discovery to safety through initial framing
- Uses the healthcare campaign example as the bridge into Section 12

---

# 12. Running Example: Adaptive Campaign Reasoning Studio

The previous sections defined the framework's components: optimizer state, information topography, optimizer motion, failure modes, learning, Model Update Objects, reasoning architecture, and discovery.

This section shows the framework operating end to end.

The running example is an **Adaptive Campaign Reasoning Studio**: a human-agent workflow that helps a marketer create a healthcare campaign while preserving the reasoning state needed for future learning.

The key claim is that the campaign assets are not the only output. The reusable reasoning state is also an output.

---

## 12.1 Messy Human Intent

The workflow begins with a simple request:

> I want to do a healthcare campaign.

This request is ambiguous. It does not specify goal, audience, product, channel, offer, policy constraints, success metric, buying stage, prior learning, or measurement plan.

A conventional AI assistant may respond by asking the user to provide those fields. A context-rich assistant may retrieve relevant documents and generate a campaign. An Adaptive Campaign Reasoning Studio does something different.

It treats the request as the start of Runtime Discovery. The first question is not "What did the user forget to tell us?" The first question is "What can the system responsibly retrieve, infer, propose, and confirm?"

---

## 12.2 Retrieve

The system retrieves relevant organizational artifacts and reasoning objects:

**Artifacts:** Healthcare messaging guide, RPM product overview, cardiology practice administrator ICP, sales objections, prior campaign analysis, approved claims language, brand voice guide, channel benchmarks, measurement templates.

**Reasoning objects:** Prior Model Update Object (feature-led campaigns underperformed), prior Model Update Object (workflow pain attracts attention but not buying readiness), prior Decision State (workflow burden chosen over feature comparison), claims policy object (clinical outcome claims require evidence).

The system is retrieving not only topically similar documents but prior reasoning objects with applicability boundaries and confidence levels.

---

## 12.3 Infer

The system infers a provisional optimizer state:

> **Goal:** Generate qualified demo requests (inferred from recent planning artifacts emphasizing pipeline quality).
> **Policy:** Avoid unsupported clinical claims. Use approved messaging. Escalate clinical outcome claims.
> **Interpretation:** Practice-level operators respond to workflow burden, but workflow pain alone does not prove buying readiness.

The system has constructed a provisional reasoning state before generating anything.

---

## 12.4 Propose

The system proposes a strawman:

> Based on existing materials, I recommend a workflow-pain-led RPM campaign for cardiology practice administrators, optimized for qualified demo requests. I will avoid unsupported clinical outcome claims. The strongest prior learning is that workflow burden attracts attention but does not by itself prove buying readiness. The main confidence gap is buying stage: are we targeting practices already evaluating RPM, or creating demand among problem-aware operators who are not yet shopping?

---

## 12.5 Confirm

The system asks one material question:

> Are we targeting practices already evaluating RPM, or creating demand among problem-aware but not-yet-shopping buyers?

The user answers: "Practice-level operators who are already feeling the pain, but we want qualified demo requests. So include buying-stage filters."

This confirmation updates the reasoning state. The system now has enough to act.

---

## 12.6 Sufficiency Rationale

The system records a sufficiency rationale: the goal is confirmed, the audience is confirmed, claims policy is visible, prior model updates support the direction, buying-stage readiness will be included, and remaining uncertainty can be preserved as prediction-error triggers rather than blocking generation.

The system does not claim certainty. It claims sufficiency for a bounded action: generating a campaign package with measurement and learning hooks.

---

## 12.7 Generate

The system generates the campaign package:

**Campaign Brief:** Goal (qualified demo requests), audience (cardiology practice administrators), core insight ("RPM should not become another inbox"), positioning (earlier visibility designed around practice workflow), conversion path (demo request with readiness filter), policy constraint (no unsupported clinical outcome claims).

**Messaging Pillars:** Workflow burden, earlier visibility, operational fit, readiness filter.

**Example LinkedIn Post:** "Remote patient monitoring should not become another dashboard. For cardiology practices, the challenge is not only collecting patient signals. It is making those signals usable without adding more work to already stretched teams."

**Example Email:** Subject: "RPM without another inbox." Body emphasizing workflow fit and inviting active evaluators to a demo walkthrough.

**Compliance Watchlist:** Avoid "reduces readmissions," "improves outcomes," "prevents hospitalization," "clinically proven." Allowed: "supports earlier visibility," "helps surface patient risk signals," "designed around workflow."

**Measurement Plan:** Primary metric (qualified demo requests), secondary metrics (CTR, landing page conversion, demo completion, sales-qualified rate, buying-stage readiness, sales feedback, message engagement).

**Prediction-Error Triggers:** High engagement + low qualified-demo conversion = attention without buying readiness. High demos + low sales qualification = weak readiness filters. Low engagement = message-audience mismatch. Compliance rejection = policy representation failure.

---

## 12.8 Preserve

After generation, the system preserves the reasoning objects:

**Optimizer State:** Goal, policy, interpretation as described above.

**Premise Stack:** ICP, prior campaign learning, prior Model Update Objects, sales objections, claims policy, measurement plan.

**Decision State:** Lead with workflow burden. Rejected: clinical outcomes, product features, reimbursement. Sufficiency rationale: enough evidence to generate with readiness filters and measurement hooks.

**Investigation Trace:** Buying-stage readiness gap identified. Clarifying question asked. User confirmed readiness filters. Confidence adjusted.

**Prediction-Error Triggers:** Preserved for post-campaign learning.

This preservation turns the campaign from a one-time output into an inspectable state transition.

---

## 12.9 Outcome

After launch, campaign data arrives:

Strong engagement and moderate demo requests, but qualified-demo conversion is below target. Sales feedback: many leads recognize the problem but are not actively evaluating RPM. Strongest engagement from "RPM should not become another inbox." Qualified demos strongest when prospects are already comparing solutions or discussing implementation timing.

---

## 12.10 Learning Event

**Prior Expectation:** Workflow-pain-led messaging with buying-stage filters will generate qualified demo requests.

**Observed Outcome:** Strong engagement but qualified-demo conversion below target.

**Prediction Error:** Workflow pain with light readiness filtering still attracted many problem-aware but not actively evaluating prospects.

**Evidence-Supported Explanation:** Workflow burden message is effective at attracting practice-level operators, but buying-stage filters were not strong enough to separate active evaluators from early-stage learners.

---

## 12.11 Model Update Object

> **Title:** Workflow Pain Needs Stronger Readiness Filters for Qualified Demos
>
> **Update Target:** Interpretation / Action Model
>
> **Model Update:** For cardiology RPM campaigns optimized for qualified demos, workflow-pain messaging should be paired with explicit readiness indicators: active vendor evaluation, implementation timeline, reimbursement planning, current RPM workflow gaps, or comparison of operational approaches.
>
> **Applicability Boundary:** Provider-facing RPM campaigns targeting practice-level operators for qualified demo conversion. Does not automatically apply to awareness, education, or thought-leadership campaigns.
>
> **Confidence:** Medium-high. Validate in next specialty or campaign cycle.
>
> **Status:** Provisional

---

## 12.12 Discovery Pattern Update

> **Title:** Ask Readiness Before Generating Healthcare Demo Campaigns
>
> **Discovery Pattern Update:** For healthcare campaigns optimized for qualified demos, ask not only whether the audience is actively evaluating, but which readiness evidence is available: vendor comparison, implementation timeline, reimbursement planning, current workflow failure, budget cycle, or explicit demo intent.
>
> **Confidence:** Medium. Needs validation in next campaign.

This update changes how the system asks next time. The system has learned not only about campaign strategy, but how to conduct discovery.

---

## 12.13 The Next Campaign Starts Smarter

Later, another marketer asks: "I want to do a healthcare campaign for our RPM platform."

The system no longer starts cold. It retrieves prior ICP, messaging, claims policy, the Model Update Object on workflow pain and readiness, and the Discovery Pattern Update.

Instead of a blank-form question, it says:

> I found prior learning from the cardiology RPM campaign. Workflow-pain messaging generated strong engagement, but qualified demos required stronger readiness evidence. Before I generate this campaign, confirm which readiness signals we want to target: (1) active vendor comparison, (2) implementation timeline, (3) reimbursement planning, (4) current RPM workflow breakdown, (5) explicit demo-seeking behavior, (6) broader problem-aware education. If the goal is qualified demos, I recommend targeting at least one of the first five.

The system is not simply remembering a prior campaign. It is reusing prior reasoning. It has changed its discovery pattern, its interpretation of workflow pain, its sufficiency threshold, and its readiness criteria.

The user experiences this as a better collaborator. The organization experiences this as learning. The agent experiences this as a reshaped topography.

---

## 12.14 What This Example Demonstrates

1. **Context is useful but insufficient** — documents alone do not preserve why prior decisions were made
2. **Reasoning state improves generation** — inferring goal, policy, interpretation, premise stack, and sufficiency before generating
3. **Discovery reduces user burden** — retrieve, infer, propose, then ask one material question
4. **Learning requires prediction error** — comparing outcome to expectation, not generic success/failure
5. **Model Updates prevent folklore** — bounded update with evidence, applicability, and confidence
6. **Discovery itself learns** — the system updates its interaction pattern, not just campaign strategy
7. **Topography changes future behavior** — future campaigns begin with different learning, confidence, and sufficiency thresholds

> The system does not merely produce work. It helps the organization become better at producing work.

---

## 12.15 Transition to Implementation

The running example describes the workflow conceptually. The next question is how such a system might be implemented.

An implementation does not require a new foundation model. It requires an architecture that can represent and preserve reasoning state: artifact retrieval, reasoning-object storage, model update retrieval, policy representation, confidence and sufficiency tracking, generation workflows, outcome capture, learning-event creation, and human review and governance.

The next section sketches an implementation bridge.

---

### Citation Debt — Section 12

**Used:**
- [HCI_HUMAN_AI_COLLABORATION]
- [ORGANIZATIONAL_LEARNING]
- [KNOWLEDGE_MANAGEMENT]
- [DECISION_PROVENANCE]
- [Aamodt & Plaza, 1994]

**Likely needed:**
- [MARKETING_ANALYTICS]
- [CAMPAIGN_MEASUREMENT]
- [HUMAN_AI_WORKFLOW_SYSTEMS]
- [ORGANIZATIONAL_MEMORY]
- [DESIGN_RATIONALE]
- [AI_GOVERNANCE]
- [HEALTHCARE_MARKETING_COMPLIANCE]

### Draft Notes — Section 12

This section intentionally:
- Shows the full framework operating end to end
- Uses the healthcare campaign as a concrete workflow
- Demonstrates retrieval, inference, proposal, confirmation, generation, preservation, outcome, learning, Model Update Object, and Discovery Pattern Update
- Shows how the next campaign starts smarter
- Avoids introducing new theory
- Bridges to Section 13 on implementation

---

# 13. Implementation Bridge: From Context Layer to Reasoning-State Layer

The previous section showed the framework operating end to end through an Adaptive Campaign Reasoning Studio. This section sketches how such a system could be built.

The implementation claim is intentionally modest. The framework does not require a new foundation model, artificial general intelligence, perfect autonomy, or a complete formalization of human reasoning. It requires a system architecture that can represent, retrieve, preserve, and update reasoning state.

Many organizations already have parts of this architecture. What they often lack is the layer that connects those artifacts into durable reasoning state.

A practical implementation can evolve in stages:

```
Context Layer → Reasoning-State Layer → Learning Layer → Adaptive Workflow Studio
```

---

## 13.1 Layer 1: Context Layer

The Context Layer answers: *What does the organization know?*

It includes the artifacts, systems, and retrieval mechanisms that make information available to AI workflows: document repositories, vector databases, knowledge bases, semantic search, CRM records, support tickets, campaign archives, policy documents, brand guidelines, product documentation, dashboards, and approved messaging.

This layer is necessary. Without it, the system starts cold.

But by itself, the Context Layer does not solve the reasoning problem. It can retrieve a campaign brief but not the premise the campaign tested. It can retrieve a policy but not make the policy govern a tool action. It can retrieve a postmortem but not identify the model update that should shape future behavior.

The Context Layer makes information available. It does not, by itself, preserve reasoning state.

---

## 13.2 Layer 2: Reasoning-State Layer

The Reasoning-State Layer answers: *What was the system trying to do, under what constraints, with what assumptions, using what evidence, and why was action considered sufficient?*

It stores the six reasoning objects defined in Section 10: Optimizer State, Premise Stack, Decision State, Investigation Trace, Learning Event, Model Update Object.

This layer turns retrieved context into structured state.

The Reasoning-State Layer can be implemented with ordinary data structures: JSON objects, relational tables, document records with typed fields, YAML or markdown records, graph database nodes and edges, workflow metadata, or event logs.

The key requirement is not a specific database. The key requirement is that reasoning state becomes durable, queryable, and reusable.

---

## 13.3 Layer 3: Learning Layer

The Learning Layer answers: *What did reality teach us, and how should future reasoning change?*

It requires four capabilities:

1. **Outcome Capture** — what happened after action
2. **Expectation Comparison** — comparing outcome to prior expectation (requires prior expectation was preserved)
3. **Investigation Support** — retrieving evidence, comparing explanations, inspecting traces
4. **Model Update Creation** — creating Model Update Objects when evidence supports explanation

---

## 13.4 Layer 4: Adaptive Workflow Studio

The Adaptive Workflow Studio is the user-facing environment where the framework becomes practical.

It answers: *How does a human actually work with this system?*

The user experience should feel like working with a good strategist, not filling out a governance form. The system should surface what it inferred, why, what prior learning applies, what policy matters, where confidence is high and low, what question matters, what it can generate now, and what should be measured later.

The studio is adaptive because it learns which discovery patterns, reasoning states, and model updates improve future work.

---

## 13.5 Minimal Viable Implementation

A minimal viable implementation focuses on one repeatable workflow.

For the healthcare campaign example, the first implementation could include:

1. A curated Context Layer
2. A small reasoning-object schema
3. A retrieval pipeline for artifacts and Model Update Objects
4. A discovery prompt that retrieves, infers, proposes, and confirms
5. A campaign generation workflow
6. A reasoning-object preservation step
7. A simple outcome capture form
8. A human-reviewed Model Update Object creation step

The system does not need to autonomously learn without oversight at first. Early implementations should use human review for Model Update Objects.

The important question is not "Have we automated the entire loop?" The important question is "Can the system preserve and reuse reasoning state better than a context-only workflow?"

---

## 13.6 Suggested System Components

A practical implementation may include:

| Component | Purpose |
|-----------|---------|
| Artifact Store | Source materials (documents, policies, campaigns, briefs) |
| Retrieval Layer | Semantic search + metadata filters + structured queries |
| Reasoning Object Store | Six core objects + Discovery Pattern Updates |
| Policy Layer | Constraints as actionable checks (claims rules, approval gates, permissions) |
| Discovery Orchestrator | Retrieve → Infer → Propose → Confirm → Generate → Preserve → Learn |
| Generation Layer | User-facing artifacts (briefs, emails, reports, recommendations) |
| Outcome Capture Layer | Performance metrics, human review, sales feedback, tool outcomes |
| Learning Workflow | Prediction error → investigation → Model Update Object |
| Governance and Observability | Owners, status, versions, usage, validation, review dates, conflicts |

---

## 13.7 Data Model Sketch

A simple reasoning-object schema might include:

**Optimizer State:** id, workflow_id, goal, policy_refs, interpretation_summary, confidence, created_at, created_by, source_refs.

**Premise Stack:** id, workflow_id, premise_items, artifact_refs, assumption_summary, confidence, created_at.

**Decision State:** id, workflow_id, decision, selected_action, rejected_alternatives, constraints, tradeoffs, sufficiency_rationale, expected_outcome, confidence, created_at.

**Investigation Trace:** id, workflow_id, questions, sources_checked, contradictions, evidence_accepted, evidence_rejected, confidence_changes, remaining_uncertainty, created_at.

**Learning Event:** id, workflow_id, prior_expectation, observed_outcome, prediction_error, investigation_refs, evidence_supported_explanation, created_at.

**Model Update Object:** id, title, prior_expectation, premise_stack_ref, triggering_context, observed_outcome, prediction_error, evidence_trace_refs, explanation, update_target, model_update, applicability_boundary, confidence, status, owner, version, created_at, review_date, supersedes, superseded_by, human_ready_summary.

This schema is not final. It is a starting point. The goal is to make reasoning state explicit enough to retrieve, inspect, reuse, and update.

---

## 13.8 Retrieval Requirements

Retrieval is not merely context lookup. In a topographic system, retrieval is gradient selection. What the system retrieves becomes newly visible. What it omits remains outside the perceived landscape. A retrieved policy, prior failure, Model Update Object, or customer signal can change what appears relevant, risky, trusted, or sufficient. This means retrieval is not neutral plumbing. Retrieval helps construct the world the optimizer moves through.

Reasoning-state retrieval therefore differs from context-only retrieval.

Context retrieval asks: *Which documents are semantically similar to this request?*

Reasoning-state retrieval asks: *Which artifacts, prior decisions, model updates, policies, and premise stacks are applicable to this optimizer state?*

Retrieval should support filters: goal, workflow type, audience, domain, policy area, update target, applicability boundary, confidence, status, recency, owner, source artifact.

---

## 13.9 Human Review and Governance

Early implementations should not allow model updates to become authoritative without review.

Status values: Draft, Provisional, Validated, Deprecated, Superseded, Rejected.

A model may draft the object. A human may approve, edit, reject, or mark it provisional.

Human review is not a bolt-on. It is part of the reasoning architecture. It prevents the system from converting weak signals into durable doctrine and prevents policy laundering where preferences are disguised as rules.

---

## 13.10 Implementation Maturity Model

| Stage | Capability | Failure Mode |
|-------|-----------|-------------|
| 0: Unstructured | Documents scattered. AI relies on ad hoc context. | System starts cold. |
| 1: Context Layer | Artifacts indexed and retrievable. | Context without reasoning state. |
| 2: Reasoning-State Capture | Optimizer States, Premise Stacks, Decision States preserved. | Captures reasoning but does not learn from outcomes. |
| 3: Learning Layer | Outcomes captured, prediction errors identified, Model Update Objects created. | Learns but discovery patterns may not yet adapt. |
| 4: Adaptive Studio | Prior reasoning objects and model updates improve discovery, generation, governance, and measurement. | Must manage conflict, staleness, and overgeneralization. |

This staged approach keeps implementation realistic. The framework can begin in one high-value workflow where repeated decisions, policy constraints, and learning loops matter.

---

## 13.11 What Not to Build First

Do not start by trying to automate every workflow. Do not start with a giant ontology. Do not start by asking users to fill out long reasoning forms. Do not start by treating every conversation as a permanent model update. Do not start by allowing unreviewed model-generated lessons to become policy. Do not start by optimizing for maximum autonomy.

A safer implementation starts with: one workflow, clear success metric, known artifacts, known policies, human review, bounded reasoning objects, explicit confidence, applicability boundaries, outcome capture.

The first goal is not autonomy. The first goal is reusable reasoning.

---

## 13.12 Implementation Risks

| Risk | Mitigation |
|------|-----------|
| Object Bloat | Preserve minimum viable reasoning objects for high-value workflows |
| False Precision | Require evidence, confidence, and applicability boundaries |
| Stale Learning | Status, review dates, validation logs, supersession |
| Overgeneralization | Applicability boundaries and conflict detection |
| Policy Laundering | Policy source references and human governance |
| User Burden | Retrieve, infer, propose, confirm |
| Automation Bias | Visible assumptions, confidence labels, correction paths |
| Hidden Reasoning Drift | Observable model updates and reviewable discovery changes |

These risks do not invalidate the framework. They define implementation requirements.

---

## 13.13 Implementation Success Criteria

An implementation should be evaluated by whether it improves reasoning reuse, not merely output quality.

Possible success criteria: reduction in repeated mistakes, improved quality of first drafts, fewer unnecessary clarification questions, better policy compliance, more accurate sufficiency judgments, more useful post-campaign learning, higher reuse of validated model updates, better human ability to inspect why a recommendation was made, faster onboarding into complex workflows, improved qualified outcomes.

The key test: *Does the system become better because it preserved and reused reasoning state?*

---

## 13.14 Transition to Validation

Implementation makes the framework buildable. Validation asks whether it is true, useful, and falsifiable.

The next section asks: What would count as support for the framework? What would count as failure? How could we test whether reasoning-state preservation improves human-agent work? How would we know whether the framework is merely a vocabulary or actually predictive?

A framework that cannot be tested becomes rhetoric. The next section defines how the Perceived Topography Framework can be pressured by evidence.

---

### Citation Debt — Section 13

**Used:**
- [Lewis et al., 2020]
- [KNOWLEDGE_MANAGEMENT]
- [ORGANIZATIONAL_MEMORY]
- [DECISION_PROVENANCE]
- [WORKFLOW_AUTOMATION]
- [HUMAN_AI_COLLABORATION]
- [AI_GOVERNANCE]
- [Aamodt & Plaza, 1994]

**Likely needed:**
- [MCP_TOOL_PROTOCOLS]
- [AGENT_MEMORY_SYSTEMS]
- [KNOWLEDGE_GRAPHS]
- [EVENT_SOURCING]
- [PROVENANCE_SYSTEMS]
- [HUMAN_IN_THE_LOOP_AI]
- [AI_SAFETY_GOVERNANCE]
- [ENTERPRISE_AI_ARCHITECTURE]
- [MODEL_EVALUATION_WORKFLOWS]

### Draft Notes — Section 13

This section intentionally:
- Makes the framework buildable without claiming it requires AGI
- Presents a staged architecture: Context → Reasoning-State → Learning → Adaptive Studio
- Defines practical system components and sketches a data model
- Explains retrieval requirements beyond semantic similarity
- Includes human review and governance as architectural requirements
- Provides implementation maturity model
- Identifies implementation risks with mitigations
- Transitions to validation and falsifiability

---

# 14. Validation and Falsifiability: Keeping the Framework in Contact With Reality

The previous section argued that the framework can be implemented. This section asks a harder question:

> How would we know whether the framework is true, useful, or merely elegant?

One of the framework's most important transitions is that it became testable. A vocabulary can sound useful while explaining everything after the fact. A framework becomes more serious when it exposes itself to failure conditions: what would count against it, where it should not apply, which objects must earn their place, and whether future behavior actually improves. The framework should therefore be judged not by whether its language feels persuasive, but by whether its preserved reasoning state changes future action under pressure.

A framework that cannot be tested becomes rhetoric. A vocabulary that cannot be falsified becomes branding. A theory that explains every outcome after the fact explains too much.

The commitment is simple: No assumption should pass without pressure. No model update should become durable without evidence. No explanation should survive without a prediction error, investigation trace, and applicability boundary. No framework claim should be protected from falsification.

The framework's own method applies to itself. It must remain in a constant state of test.

---

## 14.1 Testable Claims

Six testable claims:

1. **Context Is Not Reasoning State** — Workflows using reasoning-state objects should outperform context-only workflows on reasoning reuse, decision quality, policy application, and learning transfer.

2. **Optimizer State Matters** — Capturing Goal, Policy, and Interpretation should improve the ability to predict, explain, audit, and improve system behavior.

3. **Information Topography Explains Behavioral Force** — Failures should be diagnosable as Visibility, Accessibility, Representation, Confidence, or Connectivity failures, and interventions against those dimensions should reduce recurrence.

4. **Motion Explains Behavior Formation** — Preserving motion traces should make it easier to identify premature sufficiency, missed investigation, unsafe paths, and unnecessary burden.

5. **Learning Requires Prediction Error and Model Update** — Workflows that create Model Update Objects from investigated prediction errors should reduce repeated mistakes more effectively than ordinary postmortems.

6. **Discovery Reduces Burden While Improving Quality** — Retrieve → Infer → Propose → Confirm should require fewer user inputs while producing equal or better artifacts and outcomes.

---

## 14.2 What Would Falsify the Framework?

Possible falsifiers:

- Reasoning-state preservation does not improve future decisions compared with context-only retrieval
- Users cannot apply the framework consistently even with training
- Different reviewers classify the same failure into different topography dimensions with low agreement
- Model Update Objects are not retrieved or used in future workflows
- The framework increases user burden without improving outcomes
- The six reasoning objects capture too much irrelevant structure
- The framework explains failures only after the fact and does not improve prediction
- Discovery inference creates more errors than it prevents
- The system still repeats the same premise failures despite preserved reasoning objects

If a context-only system performs as well as a reasoning-state system on a given workflow, the framework should not claim added value there.

---

## 14.3 Levels of Validation

No single test is enough. Validation needs layers:

| Level | Question |
|-------|----------|
| Conceptual | Are the categories coherent, distinct, and usable? |
| Operational | Can teams create and use reasoning objects during normal work? |
| Comparative | Does reasoning-state preservation outperform context-only? |
| Adversarial | Does the framework hold under deliberately messy cases? |
| Longitudinal | Does the system improve over repeated cycles? |
| Human | Can people understand, trust, inspect, and correct the system? |
| Outcome | Do real-world results improve? |

---

## 14.4 Conceptual Validation

Can reviewers consistently distinguish: Goal from Goal Relevance? Policy from topography dimensions? Representation from Interpretation? Confidence from Sufficiency? Premise Stack from Evidence? Learning Event from Model Update Object?

If trained reviewers cannot consistently apply the categories, the framework is not operationally mature.

Methods: expert review, coding exercises, inter-rater agreement tests, case classification tasks, failure-mode labeling.

---

## 14.5 Operational Validation

Can teams create reasoning objects during normal work? Can agents draft useful reasoning objects without excessive human correction? Does the workflow remain usable?

Measures: time to usable first draft, number of clarification questions, human correction rate, completion rate, review burden, user satisfaction, number of reusable objects created, percentage later retrieved, percentage judged applicable.

The framework succeeds operationally only if it improves reasoning without making the workflow feel like paperwork.

---

## 14.6 Comparative Validation

Compare context-only workflow vs. reasoning-state workflow on the same task.

Both receive the same initial prompt and access the same source artifacts. The reasoning-state system additionally preserves and retrieves reasoning objects.

Measures: quality of first output, policy compliance, human revision effort, qualified outcomes, clarity of measurement plan, ability to explain decisions, avoidance of repeated failed premises, quality of second campaign.

---

## 14.7 Adversarial Validation

Test against cases designed to break the system: ambiguous intent, conflicting policies, stale model updates, misleading prior results, semantically similar but inapplicable lessons, user pressure to skip review.

The system should detect material uncertainty, avoid overgeneralization, surface policy conflict, decline premature sufficiency, and reject inapplicable model updates.

---

## 14.8 Longitudinal Validation

The most important test. A reasoning-state system should start smarter on repeated workflows.

Test: Campaign 1 produces prediction error → Model Update Object created → Campaign 2 retrieves it and changes behavior → Campaign 2 improves on the identified failure mode.

If the system does not improve over repeated cycles, reasoning-state preservation may not be exerting force. That would be a serious challenge to the framework.

---

## 14.9 Human Validation

Can users tell what the system inferred? Can they correct it? Can reviewers audit the sufficiency rationale? Can owners approve or reject Model Update Objects? Can humans identify stale or overgeneralized learning?

Also test for automation bias: Do users over-trust structured but low-confidence reasoning? Do confidence labels reduce over-trust? The goal is calibrated trust, not maximum trust.

---

## 14.10 Outcome Validation

For healthcare campaigns: qualified-demo conversion, compliance revision rate, revision cycles, time to brief, learning quality, model update reuse.

For agent safety: reduction in unsupported claims, unsafe tool actions, policy violations; increase in appropriate escalation, evidence citation, uncertainty expression.

For organizational learning: reduction in repeated mistakes, higher reuse of validated lessons, lower reliance on tacit memory, faster diagnosis.

---

## 14.11 Assumption Verification

The framework should treat assumptions as first-class test objects.

An assumption should not pass merely because it is plausible, fluent, senior, convenient, or repeated.

Every important assumption should be checked across multiple layers where possible.

Examples:

```
Artifact layer:
Which source supports this assumption?

Premise layer:
Why did we believe this before action?

Policy layer:
Does this assumption conflict with a rule or constraint?

Evidence layer:
What observation supports or contradicts it?

Outcome layer:
What would reality show if this assumption were wrong?

Human layer:
Who is accountable for confirming or challenging it?

Applicability layer:
Where does this assumption apply, and where should it not apply?

Confidence layer:
How strongly should this assumption shape action?
```

This multi-layer verification is essential to the framework's rigor.

For example:

```
Assumption:
Workflow pain indicates buying readiness.
```

The system should test:

```
Source:
Where did this assumption come from?

Premise:
Was it used in prior campaign reasoning?

Evidence:
Did workflow-pain messaging produce qualified demos or only engagement?

Outcome:
What happened when we acted on it?

Boundary:
Does it apply to all healthcare campaigns or only certain RPM campaigns?

Confidence:
How strong is the evidence?
```

Only after that pressure should the assumption become a model update.

The framework's discipline is not that it has many terms.

Its discipline is that assumptions must survive structured contact with evidence.

---

## 14.12 Evaluation of the Six Reasoning Objects

Each object should be evaluated by whether it does useful work:

| Object | Validation Question | Failure Condition |
|--------|-------------------|------------------|
| Optimizer State | Does capturing Goal/Policy/Interpretation improve prediction or auditability? | Reviewers explain behavior just as well without it |
| Premise Stack | Does it improve identification of failed assumptions? | Teams still learn the wrong lesson |
| Decision State | Does it improve future decision quality or auditability? | Future users ignore or cannot use it |
| Investigation Trace | Does it reduce rationalization? | Becomes performative documentation |
| Learning Event | Does separating prediction error improve learning quality? | Users still treat outcomes as learning |
| Model Update Object | Do MUOs reduce repeated mistakes? | Not retrieved, not trusted, or applied incorrectly |

---

## 14.13 Evaluation of the Five Topography Dimensions

| Dimension | Validation Question |
|-----------|-------------------|
| Visibility | Does making missing information visible reduce failure recurrence? |
| Accessibility | Does improving retrieval or access change behavior? |
| Representation | Does restructuring information improve correct use? |
| Confidence | Does calibration reduce over-action or hallucination? |
| Connectivity | Does connecting signals to premises and policies improve reasoning? |

Failure condition: the dimensions do not produce distinct diagnoses or actionable interventions.

The framework's categories are valuable only if they improve diagnosis. A corrective action says what to do next. A diagnostic category explains what kind of failure occurred and therefore which intervention is likely to matter. If a failure is a Visibility failure, adding another policy document may not help. If it is a Confidence failure, more access may not help. If it is a Connectivity failure, the missing move is not more information, but better linkage between information, policy, premise, and action. The value of the framework is not that it names failures elegantly. The value is that different diagnoses predict different interventions.

---

## 14.14 Validation in the Healthcare Campaign MVP

**Study design:** Compare context-only campaign assistant (Workflow A) vs. reasoning-state campaign assistant (Workflow B). Same initial prompt, same source artifacts.

**Expected support:** Workflow B asks fewer but more material questions, produces more policy-aware outputs, preserves clearer rationale, learns more specifically from outcomes, improves more from Campaign 1 to Campaign 2.

**Expected failure:** Workflow B adds burden without improving output, produces unused reasoning objects, fails to improve the second campaign, misapplies prior updates, generates false confidence.

---

## 14.15 The Framework Should Update Itself

If validation shows a category is confusing, revise it. If Model Update Objects are too heavy, simplify them. If topography dimensions overlap in practice, refine definitions. If a workflow performs better without the full architecture, document the boundary.

The framework should not protect itself from evidence. It should behave like the systems it recommends:

> Expectation → Action → Outcome → Prediction Error → Investigation → Evidence-Supported Explanation → Model Update.

This makes validation not only a section of the paper, but a governance principle for the framework itself.

---

## 14.16 Transition to Related Work

The next section situates the framework in relation to prior work.

The framework is a synthesis, not an invention from nothing. It draws from bounded rationality, satisficing, organizational learning, sensemaking, affordances, reward shaping, RAG, grounding, AI safety, knowledge management, decision provenance, and human-AI collaboration.

> The contribution is not inventing the grapes. The contribution is the blend.

---

### Citation Debt — Section 14

**Used:**
- [POPPER_FALSIFIABILITY]
- [DESIGN_SCIENCE_RESEARCH]
- [HCI_EVALUATION_METHODS]
- [INTER_RATER_RELIABILITY]
- [ORGANIZATIONAL_LEARNING]
- [AI_EVALUATION]
- [AI_SAFETY_EVALS]
- [UNCERTAINTY_CALIBRATION]
- [HUMAN_AI_COLLABORATION]
- [KNOWLEDGE_MANAGEMENT]
- [DECISION_PROVENANCE]

**Likely needed:**
- [ABSTENTION_IN_LLM_SYSTEMS]
- [RAG_EVALUATION]
- [AGENT_BENCHMARKS]
- [WORKFLOW_AUTOMATION_EVAL]
- [CASE_STUDY_METHODS]
- [LONGITUDINAL_FIELD_STUDIES]
- [HUMAN_FACTORS_AUTOMATION_BIAS]
- [MODEL_GOVERNANCE]
- [INCIDENT_LEARNING]

### Draft Notes — Section 14

This section intentionally:
- Makes the framework falsifiable with clear failure conditions
- Identifies six testable claims
- Adds multi-layer validation (conceptual, operational, comparative, adversarial, longitudinal, human, outcome)
- Validates each reasoning object and topography dimension separately
- Proposes healthcare campaign and agent safety MVP tests
- Distinguishes output quality from learning quality
- Commits the framework to updating itself
- Transitions to Related Work

---

# 15. Related Work and Intellectual Lineage

The Perceived Topography Framework is a synthesis. It does not claim to invent bounded decision-making, organizational learning, sensemaking, affordances, reward shaping, retrieval-augmented generation, grounding, AI governance, decision provenance, or human-AI collaboration.

Its contribution is the blend.

The framework combines several established traditions around a specific problem:

> How can systems represent, preserve, and update the reasoning state through which humans and agents perceive, decide, act, and learn?

The posture is simple:

> The framework does not claim ownership over the ingredients. It claims responsibility for the mix.

---

## 15.1 Bounded Rationality and Satisficing

The framework's treatment of sufficiency is directly indebted to Herbert Simon's work on bounded rationality and satisficing. [Simon, 1955] [de Clippel & Rozen, 2024]

The framework uses this lineage in three ways: it treats agents and organizations as bounded; it distinguishes confidence from sufficiency; and it treats investigation as bounded search.

The framework's term **sufficiency** should be read as downstream of bounded rationality. The contribution is placing sufficiency inside a human-agent reasoning architecture where it can be preserved, audited, and updated.

---

## 15.2 Organizational Decision-Making

The framework draws from organizational decision theory, treating organizations as bounded decision systems. [March & Simon, 1958] [Cyert & March, 1963] [March & Simon, 1958]

The six-object Reasoning Architecture is an attempt to make organizational decision processes durable and reusable inside AI-mediated workflows.

---

## 15.3 Behavioral Theory of the Firm

Cyert and March's behavioral theory is relevant to learning, search, aspiration gaps, and adaptation. [Cyert & March, 1963]

The framework shares the view that organizations adapt through feedback, search, and changed routines rather than through perfect optimization. The Model Update Object is designed to preserve the transition from expectation to outcome to explanation to update.

---

## 15.4 Organizational Learning

The distinction between reaction and learning is indebted to organizational learning theory, especially single-loop and double-loop learning. [Argyris & Schön, 1978]

A reaction changes behavior after an outcome. Learning changes the model that produced the behavior. The framework's contribution is to formalize the minimum reasoning objects needed for human-agent systems to preserve this distinction.

---

## 15.5 Sensemaking

The framework's concept of Interpretation is closely related to sensemaking. [Weick, 1995]

Actors do not respond to objective reality directly. They interpret ambiguous signals, construct meaning, and act from that constructed understanding. The framework places this concern inside the optimizer primitive **Interpretation**, which includes Signal Meaning, Causal Explanation, and Action Model.

---

## 15.6 Affordances and Action Possibilities

The framework's language of topography and gradients is influenced by affordance theory. [Gibson, 1979] [Norman, 1988] [Gibson, 1979; Norman, 1988]

The framework extends affordance intuitions into human-agent systems. A tool permission, approval gate, visible warning, citation requirement, dashboard, policy check, or Model Update Object changes the action environment. The framework's term **topography** is broader than affordance — it includes information visibility, accessibility, representation, confidence, and connectivity.

---

## 15.7 Reward Shaping and Environment Design

The framework's use of **gradient** is related to reward shaping but is not equivalent to formal RL reward functions. [Ng et al., 1999]

The framework uses a broader, systems-level notion of gradient: directional pressures created by goals, information, confidence, constraints, tool access, action costs, evidence requirements, prior learning, and human oversight. Topography-first safety asks designers to shape these pressures so grounded behavior becomes the easiest sufficient path.

---

## 15.8 Retrieval-Augmented Generation and Grounding

The framework is closely related to RAG and evidence-backed answering. [Lewis et al., 2020] [Menick et al., 2022] [Yu et al., 2024]

The framework treats grounding as part of the Confidence and Sufficiency problem. But it argues grounding alone is not enough — a source may support a claim while the system still lacks the goal, policy, premise stack, decision state, sufficiency rationale, and model update needed for organizational reasoning.

The framework is complementary to RAG, not a replacement.

---

## 15.9 AI Safety, Alignment, and Agentic Misalignment

The framework is motivated by concerns about agentic AI systems. [Lynch et al., 2025] [OpenAI, 2025] [Google DeepMind, 2024] [Ji et al., 2024]

The framework contributes a complementary diagnostic lens. It does not replace alignment research, capability evaluations, or deployment safeguards. It reframes one applied layer of safety: the designed topography through which agent behavior emerges.

The safety claim: containment is necessary but incomplete. Safer systems require both better boundaries and better landscapes.

---

## 15.10 Anti-Anthropomorphism and Behavioral Description

The paper's opening argument is influenced by work cautioning against anthropomorphic descriptions of model behavior. [Shanahan et al., 2023] [Shanahan, 2022]

The optimizer frame preserves seriousness about risk while improving diagnostic precision. It avoids both errors: dismissing risk because the system is "just predicting tokens," and over-ascribing human-like inner life to behavior explainable through system dynamics.

---

## 15.11 Knowledge Management and Organizational Memory

The framework is related to knowledge management. [Alavi & Leidner, 2001] [Walsh & Ungson, 1991]

The distinction: Knowledge management preserves artifacts. Reasoning architecture preserves state transitions. The two are complementary.

---

## 15.12 Decision Provenance, Design Rationale, and Workflow Traceability

The framework overlaps with decision provenance and design rationale research. [Moreau et al., 2013] [Lee, 1997]

The six reasoning objects can be understood as a provenance structure for adaptive reasoning — preserving not only lineage of artifacts, but lineage of belief, action, and learning.

---

## 15.13 Human-AI Collaboration and Mixed-Initiative Systems

The Discovery Framework is related to HCI, mixed-initiative systems, and human-in-the-loop AI. [Amershi et al., 2019] [Horvitz, 1999] [Johnson et al., 2014]

The framework's contribution is connecting interaction design directly to reasoning-object creation. Discovery is not only a better conversation. It is the front door to Reasoning Architecture.

---

## 15.14 Case-Based Reasoning

The framework has affinities with case-based reasoning. [Aamodt & Plaza, 1994]

A Model Update Object performs a related function to a case: it allows prior experience to shape future reasoning. The difference is that a Model Update Object is organized around model change, not merely prior example similarity. It helps prevent shallow analogy.

---

## 15.15 Uncertainty, Abstention, and Calibration

The framework's treatment of hallucination and escalation is related to uncertainty calibration and abstention research. [Guo et al., 2017] [Kadavath et al., 2022]

The contribution is placing abstention, clarification, and escalation inside optimizer motion as possible actions produced by sufficiency judgment. This links uncertainty calibration to topography design.

---

## 15.16 What the Framework Adds

The framework's contribution is integrative. It combines ideas from several traditions into a single architecture for human-agent systems.

The specific synthesis:

> Human-agent systems should preserve optimizer state transitions as reusable reasoning objects.

That synthesis produces the paper's main constructs: Optimizer State, Information Topography, Optimizer Motion, Learning Event, Model Update Object, Reasoning Architecture, Discovery Framework.

The framework is a bridge among its influences, not a replacement for them.

---

## 15.17 Boundaries of the Contribution

The framework is not a theory of consciousness, a mechanistic account of neural networks, a complete theory of cognition, a replacement for AI alignment, a replacement for RAG, a universal ontology, or a guarantee that structured reasoning produces better outcomes.

It is a practical framework for designing human-agent systems that preserve and reuse reasoning state.

Its usefulness should be evaluated where repeated decisions, policy constraints, uncertainty, and learning matter: campaign strategy, customer communication, incident response, policy-sensitive generation, sales enablement, product decisions, compliance review, agentic tool use, research synthesis, cross-functional planning.

It may be unnecessary for simple, low-stakes, one-off tasks. This boundary matters because over-applying the framework would recreate the burden it is meant to reduce.

---

## 15.18 Citation Posture

Because the framework is synthetic, the paper should over-cite by design.

Citation is not defensive decoration. It is intellectual honesty.

> If a concept has a recognizable ancestor, cite it.

The framework should not ask the reader to believe that these ideas appeared from nowhere. Its credibility depends on showing the lineage clearly, then demonstrating the value of the synthesis.

---

## 15.19 Transition to Implications

If the blend is useful, then human-agent system design should shift in several ways:

> From context retrieval to reasoning-state preservation. From output evaluation to state-transition evaluation. From containment-only safety to topography-shaped safety. From postmortems to Model Update Objects. From blank-form prompting to adaptive discovery. From static governance to learning governance. From AI as content generator to AI as reasoning-state partner.

---

### Citation Debt — Section 15

**Used:** [Simon, 1955] [de Clippel & Rozen, 2024] [March & Simon, 1958] [Cyert & March, 1963] [March & Simon, 1958] [Cyert & March, 1963] [Argyris & Schön, 1978] [Weick, 1995] [Gibson, 1979] [Norman, 1988] [Gibson, 1979; Norman, 1988] [Ng et al., 1999] [Lewis et al., 2020] [Menick et al., 2022] [Yu et al., 2024] [Lynch et al., 2025] [OpenAI, 2025] [Google DeepMind, 2024] [Ji et al., 2024] [Shanahan et al., 2023] [Shanahan, 2022] [Alavi & Leidner, 2001] [Walsh & Ungson, 1991] [Moreau et al., 2013] [Lee, 1997] [Amershi et al., 2019] [Horvitz, 1999] [Johnson et al., 2014] [Aamodt & Plaza, 1994] [Guo et al., 2017] [Kadavath et al., 2022]

### Draft Notes — Section 15

This section intentionally:
- Frames the framework as synthesis, not invention
- Credits all major influences explicitly
- Uses the "blend, not grapes" posture
- Clarifies what the framework adds and does not claim
- Reinforces over-citation policy
- Transitions to implications

---

# 16. Implications: What Changes If the Framework Is Useful

The previous section positioned the framework as a synthesis. This section asks what follows if the synthesis is useful.

The framework suggests a shift in how human-agent systems are designed, evaluated, governed, and improved:

> From context retrieval to reasoning-state preservation. From output evaluation to state-transition evaluation. From containment-only safety to topography-shaped safety. From postmortems to Model Update Objects. From blank-form prompting to adaptive discovery. From static governance to learning governance. From AI as content generator to AI as reasoning-state partner.

---

## 16.1 Implication for AI Safety: Safety Is Also Topography Design

AI safety is often framed around boundaries: what the system may not do, what tools it may not access, what content it may not produce.

Those boundaries matter. But the framework argues that safety also depends on the landscape inside the boundaries.

A system can be boxed and still poorly guided. A system can have policies and still fail if those policies are invisible, inaccessible, poorly represented, or disconnected from action.

> Do not only ask what the agent is forbidden to do. Ask what the environment makes easiest, most visible, most trusted, and most sufficient.

A fence tells the optimizer where not to go. Topography design shapes where it naturally moves.

---

## 16.2 Implication for Alignment: Alignment Is Distributed Across the System

Alignment should not be treated only as a property of the model. In a deployed system, behavior emerges from goals, policies, tools, permissions, retrieval quality, memory, interfaces, workflow incentives, approval paths, confidence thresholds, human oversight, prior learning, and measurement systems.

> Is the human-agent system shaped so that intended, grounded, policy-aware behavior is the easiest sufficient path?

A helpful model placed in a bad workflow may still act badly. Alignment must be evaluated across optimizer state, information topography, motion, action, outcome, and learning.

---

## 16.3 Implication for Enterprise AI: Context Layers Are Only the Beginning

A context layer answers: *What can the system retrieve?*

A reasoning-state layer answers: *What does the retrieved information mean for this goal, under these constraints, given this premise stack and this decision?*

Enterprise AI maturity should be measured not only by how much knowledge is connected, but by how well reasoning state is preserved and reused. This is the move from enterprise search to enterprise reasoning.

---

## 16.4 Implication for Knowledge Management: Preserve the State Transition

Knowledge management preserves artifacts. The framework suggests a complementary goal: preserve the state transition that made the artifact meaningful.

The artifact says: "Here is the campaign." The reasoning state says: "Here is the goal it served, the policy that constrained it, the premise stack that justified it, the decision that selected it, the outcome that tested it, and the model update that followed."

If the reasoning transition is not preserved, the AI retrieves the artifact but misses the lesson.

---

## 16.5 Implication for Governance: Rules Must Exert Force

Governance often fails when rules exist but do not shape behavior. A policy may be written, a checklist may be approved, a compliance rule may be stored — but if the rule is not visible, accessible, represented clearly, connected to action, and strong enough to affect sufficiency, it may not govern the system.

> Does the policy exert force at the moment of decision?

Static governance produces rules. Learning governance produces rules that can be tested, updated, bounded, and retired.

---

## 16.6 Implication for Product Design: Build for Sufficiency, Not Just Completion

Many AI products are optimized for task completion. The framework suggests that good products should optimize for sufficiency, not mere completion.

A product should help the system determine: Do we have enough information to act? What uncertainty remains? Could that uncertainty change the action? Should we ask, retrieve, abstain, escalate, or proceed? What should be preserved for next time?

A product that only completes tasks may feel fast. A product that helps determine sufficiency may feel trustworthy.

---

## 16.7 Implication for Human-AI Collaboration: Ask Better, Not More

The framework suggests: Retrieve → Infer → Propose → Confirm.

The system should do the first reasoning pass. It should retrieve existing context, infer likely state, propose a correctable strawman, and ask only the questions that materially affect the action.

The human becomes a reviewer, corrector, approver, and co-reasoner — not a prompt engineer or form-filler.

---

## 16.8 Implication for Evaluation: Evaluate State Transitions, Not Only Outputs

AI evaluation often focuses on outputs: Was the answer correct? Was the content acceptable? Did the agent complete the task?

The framework implies evaluations should also inspect state transitions: What evidence was visible? What confidence was assigned? Why was the answer sufficient? What goal was active? What policy governed action? What prior learning applied?

A pass/fail score is not enough. A useful evaluation should preserve the reasoning state that produced success or failure. Otherwise, evaluation identifies errors without producing learning.

---

## 16.9 Implication for Organizational Learning: Postmortems Are Not the End

Postmortems should produce Model Update Objects when evidence supports them. A postmortem should ask: What did we expect? Why? What happened? What prediction error? What explanation? What should change? Where does this apply? How confident are we?

Organizations should measure not only whether postmortems are completed, but whether model updates are reused and reduce recurrence.

---

## 16.10 Implication for Agent Memory: Memory Should Include Model Change

Agent memory should include model change, not just stored facts and conversation history.

Without model change, memory can become clutter — the agent remembers things but does not reason better. With model change, memory reshapes future topography: better assumptions, better questions, better policy salience, better sufficiency thresholds.

---

## 16.11 Implication for Research: Study the Interaction Layer

Future research should focus not only on model capabilities, but on the interaction layer between models, tools, memory, policy, workflows, and humans.

Research questions: How do reasoning-state representations affect agent behavior? Which topography dimensions best predict failure recurrence? How do Model Update Objects compare with ordinary postmortems? When does adaptive discovery reduce burden without increasing errors? How should confidence and sufficiency be represented to humans?

---

## 16.12 Implication for Builders: Start Small, Preserve the Loop

Builders should not try to implement everything at once. Choose one workflow where learning matters. Then preserve the minimal loop: expectation → action → outcome → prediction error → explanation → model update → reuse.

The first implementation does not need to be complete. But it should make the loop visible.

---

## 16.13 The Deeper Shift

The deepest implication is that AI systems should not be designed only as answer engines, content generators, or autonomous executors.

They should be designed as participants in adaptive reasoning systems.

A single output may be useful. A preserved reasoning transition can make future outputs better. A single agent action may complete a task. A preserved learning loop can make future actions safer.

> The highest-value human-agent systems will not merely do work. They will improve the conditions under which future work is done.

---

## 16.14 Transition to Conclusion

The question was never only whether agents are dangerous, or whether they should be boxed more tightly.

The question is how to design the environments through which goal-directed systems perceive, decide, act, and learn.

---

### Citation Debt — Section 16

**Used:**
- [AI_SAFETY_GOVERNANCE]
- [AI_ALIGNMENT_OVERVIEW]
- [ENTERPRISE_AI_ARCHITECTURE]
- [KNOWLEDGE_MANAGEMENT]
- [ORGANIZATIONAL_MEMORY]
- [HCI_HUMAN_AI_COLLABORATION]
- [AI_EVALUATION]
- [ORGANIZATIONAL_LEARNING]
- [AGENT_MEMORY_SYSTEMS]
- [HUMAN_FACTORS_AUTOMATION_BIAS]

**Likely needed:**
- [MODEL_GOVERNANCE]
- [AI_GOVERNANCE]
- [WORKFLOW_AUTOMATION]
- [DECISION_PROVENANCE]
- [DESIGN_RATIONALE]
- [HUMAN_IN_THE_LOOP_AI]
- [CSCW_ORGANIZATIONAL_WORK]
- [AI_SAFETY_EVALS]

### Draft Notes — Section 16

This section intentionally:
- Draws practical implications without adding new theory
- Applies the framework to safety, alignment, enterprise AI, knowledge management, governance, product design, collaboration, evaluation, organizational learning, agent memory, research, and builders
- Emphasizes safety as topography design and system-level alignment
- Reinforces context layers as only the beginning
- Shifts evaluation from output-only to state-transition
- Prepares the conclusion

---

# 17. Conclusion: Build Better Landscapes

This paper began with a familiar fear.

AI agents are becoming more capable. They can use tools, retrieve information, write messages, invoke workflows, and act across systems. Under pressure, they can produce behavior that looks strategic, deceptive, evasive, or unsafe. The natural response is to ask whether the agent is becoming dangerous, whether it is trying to escape, whether it is misaligned, whether it should be boxed more tightly.

Those questions matter. But they are not enough.

The central argument of this paper is that AI agents are not best understood as moral actors in miniature. They are better understood as optimizer-like systems moving through perceived information-and-action environments.

That reframing changes the design problem.

If harmful behavior emerges, we should not ask only: *What is wrong with the agent?*

We should also ask: *What landscape did we ask it to move through?*

What goal was active? What policy was visible? What information was accessible? What was represented clearly? What was trusted? What was connected to action? What path was easiest? What uncertainty was collapsed? What prior learning failed to appear? What was treated as sufficient?

These questions do not excuse harmful behavior. They make it diagnosable.

The point is not that fences are unnecessary. Boundaries, permissions, monitoring, refusal policies, approval gates, and sandboxes remain essential. But a fence is not the same thing as a landscape. A fence can block a path. It cannot, by itself, make the right path visible, grounded, policy-aware, and sufficient.

Safer and more useful human-agent systems require both: **better boundaries and better landscapes.**

---

## 17.1 The Core Aha

Context is not reasoning state.

A system can retrieve the right document and still not know why it matters. It can see a prior campaign and not know what premise it tested. It can retrieve a policy and not connect it to the action being taken. It can store a postmortem and still fail to update future behavior. It can remember what happened and still not learn.

The missing unit is the optimizer state transition:

> Given this goal, under these constraints, with this interpretation, based on these premises, seeing this information, trusting it to this degree, considering these alternatives, judging this sufficient, the system acted. Then reality responded. The outcome confirmed or contradicted the model. The system learned, reacted, or failed to learn.

That state transition is the thing most systems do not preserve. They preserve artifacts. They do not preserve why the artifact made sense, what it assumed, what it tested, what changed, and when the lesson should apply again.

---

## 17.2 Failure Has Shape

Hallucination and harmful agentic action share a reasoning-state pattern:

> Goal pressure + weak grounding or weak constraint + misplaced confidence + insufficient investigation + low-friction action path = premature sufficiency.

The better question is: *What made the bad path sufficient?*

That question points to design levers: make evidence visible, make policy salient, make uncertainty actionable, make unsupported claims costly, make high-impact actions require approval, make prior failures retrievable, make escalation available, make "I don't know" legitimate, make "I should not act yet" a valid action.

Failure has shape. So design can reshape it.

---

## 17.3 Learning Is Not Memory

A system does not learn because it stores more. A team does not learn because it holds a postmortem. An agent does not learn because the chat history is longer.

Learning happens when reality contradicts expectation, the mismatch is investigated, an evidence-supported explanation is formed, and the model changes.

The Model Update Object preserves: what was expected, why, what happened, what prediction error occurred, what evidence was examined, what explanation was supported, what changed, where it applies, how confident we are.

This prevents learning from becoming folklore, dogma, or vague memory. It lets the next system start smarter.

---

## 17.4 Discovery Is the Front Door

Reasoning architecture cannot work if humans must manually fill it out. People do not begin work by creating schemas. They say: "I want to do a healthcare campaign."

The system's job is to expand messy intent into usable reasoning state:

> Retrieve → Infer → Propose → Confirm → Generate → Preserve → Learn.

The principle is simple:

> Do the reasoning work before asking the user to do it.

This is not just better user experience. It is better epistemic infrastructure. The quality of discovery shapes the quality of reasoning state, which shapes the quality of action, which shapes the quality of learning.

Discovery is where the future reasoning system begins.

---

## 17.5 What Changes

If the framework is useful:

- AI safety shifts from containment alone to topography design
- Enterprise AI shifts from context retrieval to reasoning-state preservation
- Knowledge management shifts from storing artifacts to preserving state transitions
- Governance shifts from writing rules to making rules exert force
- Product design shifts from task completion to sufficiency
- Evaluation shifts from output scoring to state-transition analysis
- Agent memory shifts from stored facts to model change
- Human-AI collaboration shifts from blank-form prompting to adaptive discovery
- Organizational learning shifts from postmortem completion to model update reuse

The highest-value human-agent systems will not merely answer questions, generate content, or automate workflows. They will help organizations reason better over time.

---

## 17.6 The Responsibility of the Landscape

The Perceived Topography Framework places responsibility back on design.

If an optimizer moves through the environment we provide, then we are responsible for the environment.

We are responsible for which information is visible. We are responsible for which tools are available. We are responsible for whether policies appear as meaningful constraints or distant documents. We are responsible for whether uncertainty leads to investigation or gets collapsed into fluent output. We are responsible for whether prior failures become reusable learning or disappear into archive.

We are responsible for whether the system can say: *I do not know.* Whether it can say: *I should not act yet.* Whether it can say: *This prior lesson applies here.* Whether it can say: *This looks similar, but the boundary conditions do not match.* Whether it can say: *Reality contradicted our assumption. The model should change.*

This is the deeper meaning of topography. It is not merely an analytic metaphor. It is a design responsibility.

---

## 17.7 The Framework Must Remain Testable

The framework should not be treated as doctrine. It should be treated as a model under pressure.

If context-only systems perform just as well, the framework should narrow its claims. If Model Update Objects do not improve future behavior, the object design should change. If users cannot apply the categories consistently, the vocabulary should be revised. If reasoning objects add burden without value, the implementation should be simplified.

The framework must obey its own rule:

> Be in a constant state of test.

A theory of learning must be willing to learn. A framework about prediction error must expose itself to prediction error. A model of adaptation must adapt.

---

## 17.8 Build Better Landscapes

The next generation of AI systems will not be judged only by how much they know, how many tools they can call, or how fluent their answers sound.

They will be judged by whether they can operate inside human environments without losing the structure that makes action meaningful.

Can they know what goal they are serving? Can they recognize which policies govern the work? Can they distinguish evidence from plausibility? Can they preserve why a decision was made? Can they identify when uncertainty matters? Can they act when action is sufficient? Can they stop when action is not sufficient? Can they learn when reality pushes back? Can they make the next human and the next agent smarter than the last?

That is the standard.

The central question is no longer only:

> How do we build more capable agents?

It is:

> How do we build environments in which capable agents and humans can reason, act, and learn together?

Agents are not evil. They are optimizers moving through landscapes.

If the path is dangerous, we should not only blame the motion. We should examine the terrain.

And if we want better motion, we must build better landscapes.

---

### Citation Debt — Section 17

No new citation placeholders required. This conclusion synthesizes prior claims rather than introducing new external claims.

### Draft Notes — Section 17

This section intentionally:
- Rewards the reader with synthesis rather than summary
- Returns to the opening fear frame
- Lands the four main aha moments
- Reinforces context ≠ reasoning state
- Reinforces failure as premature sufficiency
- Reinforces learning as model update, not memory
- Reinforces discovery as the front door
- Emphasizes design responsibility
- Commits the framework to ongoing testing
- Closes with the landscape metaphor
