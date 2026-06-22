# 4. The System Needs a Working Frame

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

## 4.1 Goals Give Motion Direction

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

## 4.2 Policies Shape What Counts as Acceptable

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

## 4.3 Interpretation Turns Signals Into Meaning

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

## 4.4 The Working Frame Makes Behavior Legible

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

## 4.5 Three Primitives Are Enough to Begin

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

## 4.6 Safety Needs the Frame, Not Just the Output

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

## 4.7 From Working Frame to Shaped World

Optimizer State explains the starting condition: What is the system trying to do? What constrains it? How does it understand the situation?

But optimizer state alone does not explain behavior.

The optimizer still needs an environment to move through.

That environment is not the objective world in full. It is the perceived information-and-action landscape available to the optimizer.

The next section defines that landscape as **Information Topography**.

It asks: What can the optimizer see? What can it reach? What can it understand? What does it trust? What connections can it detect?

Those dimensions determine which information exerts force on behavior.

---
