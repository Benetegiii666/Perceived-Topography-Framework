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

## 6.10 Transition to Hallucination and Harmful Action

Motion explains how an optimizer acts. But once behavior is understood as motion through a perceived topography, several familiar AI failures begin to look less separate than they first appear.

A hallucinated answer, an unsafe tool call, and an attempted constraint bypass are different events. They may involve different risks, different interventions, and different levels of consequence. But each can be analyzed as a motion failure: attention is attracted, investigation is skipped or weakened, sufficiency is reached too early, and action follows through a path that the system treats as available, useful, or justified.

This does not make the failures identical. It makes them comparable.

The next section applies the motion model to hallucination and harmful action. It asks why unsupported claims and unsafe behavior can share a common structure: the system moves from insufficiently grounded perception to premature sufficiency.

Learning comes after that. Once an action occurs and reality responds, the system may encounter prediction error. But before the paper turns to learning, it first examines the failure pattern that makes learning necessary.

---
