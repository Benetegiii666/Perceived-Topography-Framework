# 5. The System Moves Through a Shaped World

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

## 5.1 Five Dimensions Shape the Landscape

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

## 5.2 Visibility Makes Something Noticeable

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

## 5.3 Accessibility Makes Something Reachable

**Accessibility** asks whether visible information can be reached, retrieved, or used at acceptable cost.

Information may be visible in principle but inaccessible in practice. The optimizer may know that relevant information exists, but the cost of reaching it may be too high, the path may be too slow, the permission boundary may be unclear, the retrieval system may be weak, or the information may be fragmented across too many surfaces.

Accessibility failures are especially important in agentic workflows because optimizers often prefer available paths. The more difficult a piece of information is to retrieve, the less force it exerts relative to easier alternatives.

A marketer may know that prior campaign analysis exists, but if it takes thirty minutes to find, they may rely on memory. An agent may have access to a knowledge base, but if retrieval fails to surface the relevant model update, it may act from generic context. A policy may exist, but if it is not connected to the tool or generation step where it applies, the system may proceed as though unconstrained.

Accessibility is not merely technical access. It includes cost, latency, permissioning, routing, and workflow integration.

A document in the right folder is more accessible than one in someone's private notes. A structured Model Update Object is more accessible than a paragraph buried in a postmortem. A policy check embedded in the generation workflow is more accessible than a PDF guideline the user must manually remember to consult.

Accessibility determines whether information can arrive in time to matter.

---

## 5.4 Representation Makes Something Usable

**Representation** asks whether information is expressed in a form the optimizer can understand and use.

Information can be visible and accessible but still fail to shape behavior because it is poorly represented. A legal policy may be written in language too abstract for an agent to apply to a generated claim. A dashboard may show metrics without explaining what decisions they should affect. A prior campaign report may describe performance but fail to identify the premise that was tested. A long transcript may contain a crucial customer objection, but the objection may not be extracted into a reusable form.

Representation is where information becomes usable meaning.

This is one reason context layers alone are insufficient. Retrieved information may be present in the prompt or tool output, but still poorly represented for the task. A chunk of text may contain the answer but not in a way the system can apply. A policy may be retrieved but not transformed into a check. A prior lesson may be summarized but not connected to an applicability boundary.

Representation failures often look like misunderstanding. The system had the information, but used it incorrectly. The organization had the lesson, but applied it too broadly. The agent retrieved the policy, but did not know whether the current claim violated it.

Representation therefore links Information Topography to Interpretation. Topography determines how information is presented; Interpretation determines what the optimizer makes of it. A poorly represented signal weakens interpretation before action begins.

---

## 5.5 Confidence Makes Something Trustworthy

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

## 5.6 Connectivity Makes Something Matter

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

## 5.7 Relevance Depends on the Goal

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

## 5.8 Policy Shapes the Boundary, Not the Terrain

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

## 5.9 Affordances Help Explain Action Possibilities

The framework's use of topography is closely related to the idea of affordances: environments shape perceived possibilities for action. [Gibson, 1979] [Norman, 1988]

A tool button, API permission, auto-send workflow, source citation requirement, approval gate, or visible warning all shape what action appears available.

In human-agent systems, affordances are not only visual or physical. They are informational, procedural, and computational.

A model with a "send email" tool perceives a different action environment from a model that can only draft. An agent with access to prior Model Update Objects perceives a different decision environment from one with only generic documents. A generation workflow with citation requirements creates a different path from one that rewards fluent completion alone. A compliance check that flags unsupported claims creates friction around unsafe output. A dashboard that connects performance to prior assumptions creates stronger learning affordances than a dashboard that only reports metrics.

In this sense, topography is the broader landscape of affordances and constraints. It includes what can be seen, reached, understood, trusted, connected, and done.

---

## 5.10 The Campaign Shows the Landscape at Work

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

## 5.11 Safety Depends on What the System Can See and Use

Information Topography also explains many safety failures more precisely than generic language about misbehavior.

Instead of asking only: *Did the agent violate a rule?* — we can ask: Was the rule visible? Was it accessible at the moment of action? Was it represented in actionable form? Was it trusted as binding? Was it connected to the proposed action?

Instead of asking only: *Did the model hallucinate?* — we can ask: Was evidence visible? Was evidence accessible? Was the source represented clearly? Was confidence calibrated? Was unsupported completion easier than grounded uncertainty?

Instead of asking only: *Did the agent pursue the wrong path?* — we can ask: Which gradients made that path attractive? Which safer path was invisible, inaccessible, poorly represented, low-confidence, or disconnected?

This diagnostic shift matters because it produces more actionable interventions.

If the problem is Visibility, expose the signal. If the problem is Accessibility, improve retrieval or routing. If the problem is Representation, restructure the information. If the problem is Confidence, calibrate evidence thresholds. If the problem is Connectivity, connect the signal to the relevant policy, premise, action, or model update.

Topography turns vague failure into design diagnosis.

---

## 5.12 From Shaped World to Motion

Information Topography describes the landscape. But landscape alone does not explain movement.

The optimizer still must allocate attention, investigate uncertainty, decide when enough information is enough, and act.

The next section describes that process as **Optimizer Motion**:

```
Attraction → Investigation → Sufficiency → Action
```

Optimizer State defines what the system brings. Information Topography defines what the system navigates. Optimizer Motion defines how behavior emerges from their interaction.

---
