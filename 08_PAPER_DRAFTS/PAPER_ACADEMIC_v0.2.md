# Perceived Topography in Human-Agent Systems: Reasoning-State Preservation as a Design Theory for Governable Agentic Action

Benet Garcia
Independent Researcher

---

## Abstract

AI agent failures are often explained by looking at the model: its capabilities, alignment, memory, tools, or constraints. Those explanations are necessary, but incomplete. Agentic systems act from a constructed information-and-action landscape: what they can see, reach, interpret, trust, and connect at the moment action becomes sufficient. This paper develops the Perceived Topography Framework, a reasoning-state account of human-agent reliability. The framework argues that many failures emerge not simply because information is absent, but because the relevant evidence, uncertainty, policy, consequence, or human confirmation fails to become behaviorally effective before action occurs. This failure pattern is called premature sufficiency.

The paper distinguishes context from reasoning state, defines perceived topography through five diagnostic dimensions — Visibility, Accessibility, Representation, Confidence, and Connectivity — and proposes reasoning-state architecture as a way to preserve the conditions from which action becomes justified, withheld, escalated, or revised. It also introduces Discovery as an infer-confirm process for turning inferred human intent into confirmed reasoning state before that interpretation becomes durable. A constructed healthcare marketing stress test shows how two workflows with the same artifacts can diverge when one relies on context alone and the other preserves goal, policy, interpretation, evidence boundaries, sufficiency rationale, outcome, and update.

The framework is grounded in established work on bounded rationality, affordances, sensemaking, organizational learning, human-AI interaction, retrieval, memory, reflection, and AI safety. Its contribution is the synthesis: a diagnostic vocabulary for the ground beneath human-agent action. The framework does not explain every failure and should lose scope where its distinctions do not improve diagnosis, governance, reuse, or learning. Its value lies in making agent behavior more examinable: not only what the system did, but what landscape made that action appear available, justified, safe, or sufficient.

---

## Epistemic Status

This paper develops a conceptual design framework for human-agent systems. It is not an empirical study, benchmark report, field evaluation, or claim of production validation.

The argument is pre-empirical but grounded. It synthesizes established work on bounded rationality, affordances, information behavior, sensemaking, organizational learning, human-AI interaction, retrieval, memory, reflection, and AI safety. The contribution is the synthesis: a vocabulary for describing the perceived information-and-action landscape from which human-agent systems decide that action is available, justified, safe, or sufficient.

The framework's constructs — perceived topography, premature sufficiency, the five diagnostic dimensions, reasoning-state architecture, Discovery, and Model Update Objects — should be judged by whether they improve explanation, intervention, governance, reuse, and learning in human-agent workflows.

The healthcare marketing scenario is author-constructed. It is used as a stress test, not as empirical evidence. Its purpose is to make the framework examinable by holding the assignment and artifact set constant while comparing a context-only workflow with a reasoning-state workflow.

The framework does not claim that perceived topography explains every agent failure. Some failures are model failures, tool failures, domain-expertise failures, governance failures, incentive failures, or institutional failures. Nor does the framework claim that reasoning-state architecture guarantees safety, eliminates politics, replaces human judgment, or makes governance legitimate because it can be automated.

The central claim is narrower: many human-agent failures become clearer when we examine the landscape from which action became sufficient. If the framework's distinctions do not change diagnosis or design, they should lose scope. If reasoning-state preservation does not improve reuse, governance, error recovery, or learning relative to strong context-only baselines, the architectural claim should narrow. If Discovery adds friction or anchoring without improving confirmed reasoning state, it should lose importance.

The paper therefore treats perceived topography as a serious but testable synthesis: grounded enough to use, bounded enough to challenge, and incomplete enough to require stress testing.

---

## 1. Introduction: The Reliability Problem Has Moved

AI agents are increasingly evaluated as actors: systems that can pursue goals, use tools, preserve state, and move through multi-step environments. [Yao et al., 2023] When these systems fail, the failure often feels different from an ordinary model error. A static model may hallucinate a citation. An agent may hallucinate, send the message, update the record, and leave the human team to discover later that the action rested on unsupported ground. [Lynch et al., 2025]

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

The framework describes this landscape through the five dimensions: **Visibility, Accessibility, Representation, Confidence, and Connectivity**. These are not offered as a complete ontology of all factors that influence agent behavior. They are a minimum viable diagnostic set. A dimension earns its place only if changing it would lead to a different diagnosis, intervention, or expected outcome.

The framework also introduces **premature sufficiency** as a recurring failure pattern. The concept extends satisficing [Simon, 1955] — the observation that agents act when a solution is good enough rather than optimal — by focusing on the conditions under which "good enough" is reached too early. Premature sufficiency occurs when a system acts before the relevant evidence, uncertainty, policy, consequence, or human confirmation has exerted enough force on the decision. The system does not merely lack information. It stops moving too soon.

This pattern can appear in different kinds of failures. In hallucination, a fluent answer may become sufficient before it is grounded. In unsafe tool use, an available action may become sufficient before risk or approval has been resolved. These failures differ in consequence and mitigation. The point is not to collapse them. The point is to notice that both can involve the same motion structure: goal pressure, weak counterpressure, misplaced confidence, and a low-friction path to action.

A human-agent system therefore needs more than better prompts, larger context windows, or stricter fences. It needs a way to preserve the reasoning state from which action became justified. The system should retain the working goal, the governing constraint, the interpretation that made action attractive, the uncertainty that remained, and the reason investigation stopped. Without that structure, the organization may keep the artifact while losing the why.

This loss is familiar in human organizations. Teams store documents but lose decisions. They remember outcomes but forget assumptions. They correct an artifact without changing the reasoning that produced the error. The next team retrieves the old material and repeats the same mistake under a new label. The organization appears to have memory but behaves as if it does not. [Walsh and Ungson, 1991; Markus, 2001]

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

## 2. Related Work and Theoretical Positioning

The claim developed here is not that environments shape behavior, that context matters, or that human oversight is useful. Those claims already belong to several mature traditions. The narrower claim is that human-agent systems need a diagnostic vocabulary for the constructed information-and-action landscape through which reasoning becomes sufficient for action.

That places the framework between fields that are usually treated separately: language-model agents, retrieval-augmented generation, human-computer interaction, organizational learning, and AI safety. Each explains part of the problem. None, by itself, gives designers a compact way to ask why a particular path became visible, trusted, connected, and sufficient before action occurred.

### 2.1 LLM Agents: From Response Generation to Situated Action

The unit of analysis has moved from the answer to the trajectory. Once a language model can reason, act, call tools, and update its behavior across steps, reliability cannot be judged only by the final response. The intermediate path matters: what the system noticed, what it retrieved, what it ignored, when it stopped searching, and why one action became preferable to another.

ReAct formalized this shift by interleaving reasoning traces with task-specific actions, allowing a model to update its plan through interaction with an environment. Toolformer showed that language models could learn to call external APIs for functions such as search, calculation, and translation. Generative Agents brought memory, reflection, and planning into an architecture for believable behavior over time. [Yao et al., 2023; Schick et al., 2023; Park et al., 2023]

Reflection-oriented systems sharpen the issue further. Reflexion uses verbal feedback and episodic memory to improve an agent across trials. Self-Refine uses iterative self-feedback to improve an initial output without additional training. These systems show that language agents can benefit from explicit critique and revision loops. [Shinn et al., 2023; Madaan et al., 2023]

The account developed here is adjacent but not identical. Reflection systems typically improve behavior within a task trajectory or across repeated trials for the agent. A reasoning-state architecture is aimed at something broader: preserving reasoning across cycles, across agents, and across organizational contexts. The problem is not only whether an agent can improve its next attempt. It is whether a future human-agent workflow can inherit the goal, premise, evidence boundary, uncertainty, and model update that made the prior action succeed or fail.

Agent architecture work describes important components: memory, planning, reflection, tools, and environment interaction. The missing layer is how those components construct the perceived operating world at the moment of decision. A memory module may store prior experience. A tool interface may expose possible actions. A retrieval system may supply documents. The design question remains: what did the system actually experience as visible, reachable, trusted, connected, and sufficient?

Multi-agent orchestration frameworks coordinate agent behavior across tasks, roles, and conversations; the reasoning-state architecture developed here operates at a different level, preserving the conditions from which individual or collaborative action became sufficient. [Wu et al., 2023]

### 2.2 Agent Evaluation and Realistic Task Environments

Realistic agent benchmarks make the same shift visible from the evaluation side. AgentBench evaluates language models as agents across interactive environments. WebArena provides functional web environments with long-horizon tasks. SWE-bench tests whether models can resolve real GitHub issues by understanding and editing codebases. OSWorld evaluates multimodal agents in real computer environments. TheAgentCompany simulates consequential digital work inside a software-company-like setting. [Liu et al., 2024; Zhou et al., 2024; Jimenez et al., 2024; Xie et al., 2024; Xu et al., 2024]

These benchmarks show that real tasks are not merely harder prompts. They require state, tool use, interface navigation, recovery from errors, and coordination across artifacts. A wrong move can change the environment rather than merely produce an incorrect sentence.

Task success tells us whether the system arrived. Perceived topography helps ask why it moved the way it did.

That distinction matters because a benchmark failure can hide different causes. The agent may not have seen the relevant signal. It may have seen it but failed to connect it to the current goal. It may have over-trusted a weak source, misread a tool affordance, or treated a partial answer as sufficient. These are not the same failure. They imply different interventions.

The framework is therefore complementary to benchmark evaluation. It does not replace task-based measurement. It adds a diagnostic layer beneath it.

### 2.3 Retrieval, Context, and the Limits of Availability

Language models cannot reliably access, update, or ground external knowledge on their own. Retrieval-augmented generation addresses that weakness by combining parametric model knowledge with explicit non-parametric memory, making external information available during generation. [Lewis et al., 2020]

That response is necessary. It is also easy to overextend. Availability is not the same as reasoning relevance.

A document can be retrieved and still fail to govern action. A policy can sit in context while the agent drafts a claim the policy should have constrained. A postmortem can be available while its lesson fails to alter the next decision. The issue is not whether the information exists. The issue is whether it becomes behaviorally effective.

This is the difference between context and reasoning state.

Context asks what information the system can access. Reasoning state asks what the system is trying to do, which constraints govern the action, what interpretation is active, what evidence would be sufficient, and what should change when the outcome contradicts the expectation.

That distinction reframes retrieval. The system does not only need relevant chunks. It needs reasoning-relevant surfaces: information made salient at the right moment, expressed in a usable form, calibrated for confidence, and connected to the goal, policy, premise, or decision where it should matter.

### 2.4 Affordances, Situation Awareness, and Human-Agent Interaction

Systems act through environments that make some actions easier to perceive and execute than others. Gibson's affordance theory described action possibilities available in an environment. Norman translated affordances, constraints, signifiers, and feedback into design language for human interaction with artifacts. [Gibson, 1979; Norman, 1988]

Human-agent systems inherit this problem at machine speed. A tool panel can make an action feel close. A ranked source can make one document feel authoritative. A missing escalation path can make uncertainty difficult to express. A policy buried in a general document may exist without shaping the current action.

Situation awareness is also close to the problem addressed here. Endsley describes situation awareness as the operator's perception and comprehension of environmental elements, including their projection into future status. [Endsley, 1995] The overlap is real, and the distinction matters. Situation awareness is primarily a descriptive account of how an operator understands a dynamic environment. Perceived topography is a design-theoretic account of how the environment is shaped so that certain information, constraints, and action paths become behaviorally effective.

Mixed-initiative interaction adds the human side of the problem. Horvitz argued for systems that couple automated services with direct manipulation rather than forcing a simple choice between automation and human control. [Horvitz, 1999] Human-automation research similarly shows that trust, uncertainty, and interface design shape when humans over-rely, under-rely, or intervene. [Parasuraman and Riley, 1997; Lee and See, 2004]

This matters because human oversight is not merely a final approval step. It is part of the landscape. A confirmation path can make uncertainty legitimate. An escalation path can make non-action a successful action. A review requirement can connect policy to tool use before harm occurs.

This paper later treats Discovery as an infer-confirm process. The agent should not silently convert inferred human intent into preserved reasoning state. It should expose the interpretation, name uncertainty where it matters, and ask for confirmation before that interpretation governs future action.

### 2.5 Organizational Learning and Knowledge Reuse

Organizations store artifacts without preserving the reasoning that produced them. They retain documents, dashboards, tickets, meeting notes, and postmortems, but lose the assumptions and decision logic that made prior action seem reasonable. [Walsh and Ungson, 1991; Alavi and Leidner, 2001; Markus, 2001]

This problem becomes sharper when agents enter the workflow. A future agent may retrieve a prior campaign, policy, or postmortem and still fail to know what lesson should transfer. It may reuse the artifact while missing the reasoning transition. The organization appears to remember because the document exists, but it behaves as if it has forgotten because the decision logic is not reusable.

Argyris and Schon's distinction between correction and learning is especially important here. A system can correct an artifact without changing the reasoning that produced the error. Learning requires a model update: a change in future expectations, investigation, sufficiency, or action. [Argyris and Schon, 1978]

The framework uses this distinction to define reasoning-state preservation. A reasoning-state transition captures the movement from goal and interpretation to action, outcome, contradiction, investigation, and model update. The point is not to preserve every detail. The point is to preserve the minimum structure necessary for future action to begin from better conditions.

### 2.6 AI Safety, Alignment, and Agentic Risk

Safety work gives this framework its stakes. As models become more capable, alignment research asks how systems can be made to follow human intentions and values. Reinforcement learning from human feedback and instruction tuning are major responses to this problem. Constitutional AI explores how models can critique and revise outputs using a set of principles and AI feedback. Broader alignment surveys organize the field around robustness, interpretability, controllability, and ethicality. [Christiano et al., 2017; Ouyang et al., 2022; Bai et al., 2022; Ji et al., 2023]

Those traditions matter, but agentic systems expose a further design problem. Tool use, memory, planning, and external action create risks that do not appear in the same way when a model only produces text. Recent work on autonomy-induced security risks identifies problems such as memory poisoning, tool misuse, reward hacking, irreversible action chains, and failures across perception, cognition, memory, and action. [Su et al., 2025]

The account developed here does not replace alignment, interpretability, red-teaming, policy enforcement, or sandboxing. It asks a question that must be answered inside those efforts: did the relevant constraint become behaviorally effective before action became sufficient?

A policy document does not govern an agent merely by existing. A human approval rule does not matter if the system does not recognize that the current action triggers it. A memory of prior failure does not reduce risk if it is not connected to the new decision. An uncertainty signal does not prevent harm if the interface offers no legitimate path for pausing, escalating, or asking.

This is where premature sufficiency connects to governance. Many unsafe actions are not simply the result of missing rules. They occur when the rule, uncertainty, or consequence does not exert enough force inside the agent's perceived landscape. The system reaches action before governance has become part of the reasoning state.

### 2.7 Contribution Relative to Prior Work

The framework is built from familiar materials, but the contribution is the blend rather than the grapes.

Agent research shows how language models can reason, act, use tools, reflect, and operate in environments. Retrieval research shows how external information can be made available. Benchmarks show how brittle current agents remain when tasks require long-horizon interaction with realistic systems. HCI and affordance theory show that action is shaped by environments, interfaces, and available paths. Organizational learning explains why stored knowledge does not automatically become changed behavior. Safety and alignment research explain why tool-using, memory-bearing, goal-directed systems need more than fluent completion.

The account developed here joins these threads around a specific diagnostic question:

What perceived landscape made this action look available, justified, safe, or sufficient?

Simon's bounded rationality is useful here because agents, like humans and organizations, do not deliberate from unlimited information under unlimited time. They act from bounded representations of the situation. [Simon, 1955] The framework gives that bounded representation a design vocabulary. The five dimensions describe how information becomes behaviorally effective. Gradients describe why one path pulls harder than another. Premature sufficiency describes how action can occur before reasoning warrants it. Reasoning-state preservation describes what must survive if the next cycle is to begin from improved conditions.

The result is not a replacement for existing traditions. It is a shared diagnostic surface for human-agent systems: a way to describe where the system was acting from, what the landscape made easy, what it made hard, and why a particular path became sufficient.

---

## 3. From Context to Reasoning State

The usual repair for unreliable agent behavior is to add more context.

This instinct is understandable. If a system invents facts, give it sources. If it misses a policy, retrieve the policy. If it repeats an old mistake, expose the postmortem. Retrieval-augmented systems have made this response practical at scale, and context remains one of the most important tools for grounding language-model behavior. [Lewis et al., 2020]

But context has a boundary. It can make information available without preserving why that information mattered, how it was used, what decision it shaped, or what later evidence should change.

That is the gap between context and reasoning state.

Context may help a system answer. Reasoning state explains why the system acted as it did.

The distinction is not about volume. A larger context window does not automatically become reasoning state. Nor does a better retrieval system, a longer prompt, or a more complete knowledge base. A context layer can give the system artifacts: documents, policies, prior work, examples, records. A reasoning-state layer preserves the relationship among purpose, interpretation, constraint, evidence, sufficiency, action, and update.

A policy document is a simple example. It is useful for the system to retrieve the policy. But retrieval alone does not guarantee that the policy governs the action being considered. The system must recognize that the current action falls under the policy, understand what the policy permits or prohibits, and treat that constraint as active before action becomes sufficient. If the policy is merely present in the prompt or context window, it may still fail to shape behavior.

This problem has older roots than AI agents. Design rationale work has long argued that systems should preserve not only decisions, but the reasons, alternatives, and assumptions behind them. [Lee, 1997] Organizational memory research makes a similar point at the institutional level. Teams often preserve artifacts while losing the reasoning that produced them. They keep the campaign brief, the dashboard, the decision log, the ticket, and the postmortem. What disappears is the prior expectation, the assumption that made the action reasonable, the boundary condition that mattered, and the explanation of what changed after reality pushed back. [Walsh and Ungson, 1991; Markus, 2001]

The result is familiar: the organization appears to remember because the document exists, but it behaves as if it has forgotten because the decision logic is not reusable.

Agentic systems can inherit and accelerate this failure. A future agent may retrieve a prior artifact and still not know whether to reuse it, challenge it, qualify it, or treat it as obsolete. The system has access to the memory, but not the meaning of the memory. It sees what was produced, not the reasoning transition that produced it.

This matters because agents act from stopping conditions. They do not need perfect knowledge to act. Neither do humans or organizations. They act when the current state of reasoning feels sufficient for the next move. This is close to Simon's account of bounded rationality and satisficing: real decision-makers operate under limits and stop when an option is good enough for the situation. [Simon, 1955]

The central design question is therefore not only whether the system had relevant information. It is whether the right information, uncertainty, and constraint were active before sufficiency arrived.

A reasoning state is both a condition and a transition. It is the structured condition from which action becomes justified, and it is the trace of how the system moved from goal and interpretation toward action, outcome, and update.

At this point in the argument, four elements are enough to distinguish reasoning state from context. They are not exhaustive; Section 6 develops the fuller architecture. They serve here as the minimum structure needed to preserve the why.

The first is the active frame: what the system is trying to accomplish, what constrains the action, and how the situation is being interpreted.

The second is the premise stack. These are the claims or assumptions that make the proposed action seem reasonable.

A third element is the sufficiency rationale: the reason the system stopped investigating and moved toward action.

Finally, reasoning state needs an update path. It should preserve what outcome occurred, what expectation was contradicted, and what should change next time.

This is not a demand to record everything. A reasoning-state architecture that preserves every token, every document, and every intermediate possibility would create a new problem: excessive state without usable judgment. The goal is minimum viable reasoning preservation. The system should preserve enough structure that a future human or agent can understand why an action once appeared justified, whether that justification still holds, and what has changed.

In a healthcare marketing workflow, a team asks an agent to draft campaign messaging for a remote patient monitoring product. A context-rich system may retrieve product documentation, audience research, approved claims, prior campaigns, and compliance guidance. That is useful. It is also not enough.

If the system drafts the phrase "reduces readmissions," the question is not only whether readmissions appeared somewhere in the retrieved material. The question is why that phrase became sufficient. Did the system distinguish an operational capability from a clinical outcome claim? Did it connect the claim to the evidence threshold? Did it know whether approved language existed? Did it preserve the fact that this claim required human or compliance confirmation?

A reasoning-state system would preserve a different trace. The evidence boundary would be active before generation. The sufficiency rationale would record that operational-value language is currently supportable, while a direct clinical-outcome claim is not. The unsupported phrase would be flagged, bounded, or escalated rather than silently converted into campaign copy.

The difference between producing an artifact and preserving the reasoning condition behind it becomes clearer here.

The difference becomes more important after the outcome is known. Suppose a campaign later generates attention but weak qualified demand. A conventional memory system can store the performance report. A reasoning-state system should preserve what the result contradicted. Was the weak conversion evidence that the audience was wrong, the message was wrong, the buying-stage assumption was wrong, or the offer was wrong? Without the prior expectation, the outcome can be explained many ways after the fact. Learning becomes storytelling. [Weick, 1995]

This is why correction is not the same as learning.

A human reviewer can delete an unsupported claim from a draft. The immediate artifact improves. But if the system does not preserve why the claim was unsupported, what evidence boundary applied, and when that boundary should govern future claims, the next agent may recreate the same error in different language. The correction changed the output. It did not change the future reasoning state.

Argyris and Schon's distinction between single-loop and double-loop learning is useful here. Single-loop learning can correct action within existing assumptions. Double-loop learning changes the governing assumptions themselves. A reasoning-state architecture should make that second movement possible: not only "fix this output," but "change the future expectation, threshold, or action boundary that produced this output." [Argyris and Schon, 1978]

This gives reasoning state a different role from context. Context supports the current answer. Reasoning state supports future judgment.

The two layers should work together. Context provides the information surfaces from which the system can reason. Reasoning state preserves the structured transition from goal and interpretation to action and update. Without context, the system lacks grounding. Without reasoning state, the system may keep retrieving the same artifacts while failing to inherit the lessons those artifacts should have carried.

The point is not that context is weak. The point is that context and reasoning state solve different problems.

Context asks: what can the system see?

Reasoning state asks: from what condition is the system about to act?

Once that distinction is clear, the next question becomes unavoidable: what kind of environment shapes that condition? The answer is perceived topography — the landscape of the five dimensions through which information becomes behaviorally effective.

---

## 4. Perceived Topography: Definitions and Dimensions

Once reasoning state is distinguished from context, the next question is what shapes that state.

The answer offered here is perceived topography: the information-and-action landscape made available to an optimizer-like system at the moment of reasoning and action. The term is a metaphor, but not an ornamental one. It is meant to make a design claim. Systems do not act from all available information. They act from information that has become visible, reachable, interpretable, trusted, and connected to the decision at hand. This framing draws on older work showing that action is shaped by perceived environments, affordances, information-seeking behavior, and bounded decision-making. [Gibson, 1979; Norman, 1988; Wilson, 1999; Kuhlthau, 1991; Simon, 1955]

A perceived topography is therefore not the organization's knowledge base, the model's context window, the user interface, or the tool set considered separately. It is the effective landscape produced by their interaction. A policy in a document, a memory in a store, a dashboard in another system, and a tool in an action panel may all be present. The question is whether they influence the system's reasoning or action selection before the system acts. That is what this paper means by **exerting force**: behavioral influence on what the system notices, investigates, trusts, selects, withholds, or escalates.

That distinction matters because many design failures hide behind the phrase "the information was available." Available to whom, at what moment, in what form, with what authority, and connected to which action? A fact can exist without being noticed. A warning can be noticed without being understood. A policy can be understood without being connected to the current decision. A prior failure can be remembered without changing what happens next.

### 4.1 Core Definitions

An **information surface** is any source, interface, artifact, memory, observation, tool output, policy, dashboard, or signal that can present information to the system. Information surfaces are the raw material of perceived topography. They are not the topography itself.

A **perceived topography** is the effective information-and-action landscape produced when those surfaces become available to an optimizer-like system under a goal, policy, and interpretation. It describes what can be seen, reached, understood, trusted, and connected before the system acts.

An **optimizer state** is the system's working frame. It has three minimum primitives: **Goal**, **Policy**, and **Interpretation**. Goal gives direction: what the system is trying to accomplish. Policy defines constraint: what should limit or govern action. Interpretation gives meaning: how the system understands the situation and what it believes follows from it.

A **topographic dimension** is a diagnostic property of the perceived landscape. It helps explain why information that exists somewhere may or may not shape behavior in a specific decision.

A **gradient** is a directional pressure within the landscape. It makes one path feel easier, safer, more attractive, more complete, or more action-ready than another.

A **topography failure** occurs when the landscape fails to make the right information, constraint, uncertainty, or consequence behaviorally effective before action occurs.

These definitions are practical. They are meant to help a designer ask: what did the system experience as the available world?

### 4.2 The Five Diagnostic Dimensions

The framework describes perceived topography through five dimensions: **Visibility, Accessibility, Representation, Confidence, and Connectivity**.

These dimensions are not a complete ontology of information behavior. They are a minimum viable diagnostic set. Each dimension earns its place only if changing it would lead to a different diagnosis, intervention, or expected outcome.

**Table 1. Five Diagnostic Dimensions of Perceived Topography**

| Dimension | Diagnostic question | Typical failure | Design response |
|---|---|---|---|
| **Visibility** | Did the relevant signal enter the system's perceived field? | The information existed somewhere, but never appeared in the working frame. | Surface the signal at the point where it matters. |
| **Accessibility** | Could the system reach the signal at acceptable cost? | The signal was known in principle, but buried, blocked, slow, permissioned away, or outside the workflow. | Improve retrieval, routing, permissions, or workflow placement. |
| **Representation** | Was the signal expressed in a usable form? | The information was visible and reachable, but too vague, abstract, legalistic, unstructured, or mismatched to the task. | Restructure the information so it can guide interpretation and action. |
| **Confidence** | Was the signal trusted at the right level? | Weak evidence was over-trusted, strong evidence was underweighted, or source quality was not represented. | Calibrate authority, evidence thresholds, provenance, and uncertainty. |
| **Connectivity** | Was the signal connected to the goal, policy, premise, decision, or outcome where it should matter? | The information remained isolated and failed to influence the action it should have constrained or updated. | Link the signal to the reasoning object or action boundary it governs. |

Visibility asks whether the signal enters the field at all. This is the most basic failure. A compliance rule, customer constraint, or prior incident cannot shape behavior if it never appears in the system's working frame. This aligns with situation-awareness work in which perception of relevant environmental elements is a precondition for comprehension and projection. [Endsley, 1995]

Accessibility asks whether the signal can be reached without breaking the workflow. A Visibility failure means the signal was never presented. An Accessibility failure means the signal was known or knowable, but reaching it was too costly, blocked, slow, or outside the available path. In practice, agents and humans both tend to use what the environment makes easy enough to reach.

Representation asks whether the information is usable in the form presented. A policy written for lawyers may not help a campaign agent decide whether a sentence is an unsupported clinical claim. A dashboard designed for executives may not help an operations agent identify the dependency that makes an automated restart risky. Information has to be shaped for the decision it is expected to influence.

Confidence asks whether the system treats the signal with the right degree of trust. Confidence is not the same as truth. A fluent prior example can feel stronger than a dry policy statement. A highly ranked retrieved passage can appear authoritative because of its placement rather than its provenance. A system may act too soon because weak evidence feels adequate, or fail to act because strong evidence is not represented as strong.

Connectivity asks whether information is linked to the reasoning structure where it should influence behavior. This is often the missing dimension in context-heavy systems. A policy may be visible, accessible, clearly represented, and trusted, yet still fail if it is not connected to the exact claim, tool call, approval rule, or premise it should govern.

If the problem is visibility, the system never saw the signal. If the problem is accessibility, it could not get there at usable cost. If the problem is representation, it saw the signal but could not use it. If the problem is confidence, it trusted the wrong thing or trusted the right thing at the wrong level. If the problem is connectivity, the signal existed but did not attach to the decision.

These are different failures. They call for different repairs.

### 4.3 Why These Five

The five dimensions are intentionally constrained. A framework that names every important factor becomes unusable. Timeliness, salience, completeness, relevance, policy, memory, and trust all matter, but not all of them should become top-level dimensions.

The admission rule is simple: a candidate dimension should be promoted only if it changes the diagnosis, intervention, or expected outcome. This discipline reflects the same boundedness problem that motivated the framework: a diagnostic vocabulary should reduce the cost of action, not multiply labels faster than designers can use them. [Simon, 1955]

Timeliness is a useful example. Stale information is obviously dangerous. But in many cases, staleness can be diagnosed through the existing dimensions. A current source may not be visible. A stale source may remain accessible while the updated one is not. A date may be represented poorly. Source recency may affect confidence. The update may fail to connect to the decision. Timeliness matters, but it does not always require a sixth dimension.

Relevance is handled differently. Relevance is not treated as a free-standing dimension because it depends on the active goal. The same information can be irrelevant under one goal and decisive under another. In this framework, relevance emerges from the relationship between optimizer state and topography: the goal determines what could matter; the topography determines whether what matters can influence reasoning or action.

Policy is also not a dimension. Policy belongs to optimizer state. It defines what should constrain action. But policy still has to pass through the topography before it can govern behavior. A policy must become visible, accessible, represented, trusted, and connected to the action where it applies. If it fails there, the policy exists as an artifact but not as an active constraint.

Memory follows the same logic. Memory is not enough. A stored lesson must still become visible, reachable, usable, trusted, and connected to the new decision. Otherwise the system may appear to remember while behaving as if it does not.

This keeps the framework from becoming a list of everything that matters. The five dimensions are not important because they are the only things that matter. They are important because they separate failure types that would otherwise collapse into vague statements such as "bad context," "poor retrieval," or "weak governance."

### 4.4 From Description to Diagnosis

The practical purpose of perceived topography is diagnosis.

Consider again an agent drafting a healthcare campaign. The approved-claims repository may exist. That alone tells us little. If the agent produces an unsupported claim, the failure could have occurred in several ways.

The repository may not have been visible in the workflow.

It may have been visible but inaccessible to the agent.

It may have been accessible but represented as a general list of approved phrases rather than a claim-boundary system.

It may have been represented clearly but treated as lower confidence than prior campaign language.

It may have been trusted but disconnected from the specific sentence being generated.

Each diagnosis implies a different repair. Add the repository to retrieval. Change permissions. Restructure claim guidance by claim type. Add provenance and evidence thresholds. Connect claim generation to approval status. These are not interchangeable interventions.

The same logic applies to unsafe tool use. A restart policy may exist, but if it is not connected to a particular service, dependency pattern, risk level, or approval condition, the agent may treat restart as action-ready too early. The failure is not simply "the agent ignored policy." The policy may never have become part of the landscape from which the action was selected.

This is the work the topography concept does. It shifts diagnosis from whether information exists to whether information shaped motion. It asks whether the landscape made the right path easier, the risky path harder, and uncertainty legitimate before the system acted.

But structure alone does not explain movement. A landscape can make some paths pull harder than others. Some uncertainties slow action. Some signals redirect attention. Some claims become ready for action too quickly. The next section turns from the shape of the landscape to motion through it.

---

## 5. Gradients, Motion, and Premature Sufficiency

A landscape does not explain behavior until something moves through it.

The previous section described perceived topography as the effective information-and-action landscape available to a system. But structure alone does not explain motion. A human-agent system does not experience every possible path equally. Some sources are close. Some claims are fluent. Some tools are visible. Some policies exist without slowing the action they should constrain.

The shape of the landscape matters because it creates directional conditions.

Those conditions are **gradients**.

A gradient is a property of the landscape, not of the optimizer. It describes how the arrangement of information surfaces, tool paths, representations, confidence cues, and connections makes one path easier, safer-looking, more complete, or more action-ready than another. The optimizer's response to that gradient is **attraction**. The slope does not move itself. The marble moves because of the slope. The distinction matters because the framework is diagnosing landscapes, not assigning psychology to agents.

Gradient is close to affordance, bias, and nudge, but it is not identical to any of them. An affordance names an action possibility made available by an environment. A bias names a systematic distortion in judgment or selection. A nudge names a deliberate choice-architecture intervention. Gradient is broader and more diagnostic. It names the directional condition that makes one reasoning or action path easier to enter than another, whether that condition was intentionally designed or accidentally produced. [Simon, 1955; Gibson, 1979; Norman, 1988; Pirolli and Card, 1999]

A persuasive claim has a gradient when it is familiar, fluent, and aligned with the goal. A tool has a gradient when it is visible, available, and presented without consequence. A policy has a weak gradient when it is buried, generic, or disconnected from the decision it should govern. A prior failure has little gradient if it remains stored as a postmortem but never appears when a similar premise is active again.

The system does not simply "choose badly." It moves through a shaped field.

For diagnostic purposes, that movement can be described through four moments: **Attraction, Investigation, Sufficiency, and Action**. These are not rigid workflow stages. Real systems loop, branch, revise, and return to earlier states. The sequence is useful because it identifies where motion changed: what captured attention, what was investigated, why investigation stopped, and what action followed.

**Attraction** is the optimizer's response to gradient. Something in the landscape becomes the path attention begins to follow: a claim, a source, a tool, a prior pattern, a user instruction, or an apparent shortcut.

Attraction can orient in two directions. **Action attraction** points the system toward doing: answer, draft, invoke, send, update, complete. **Exploration attraction** points the system toward uncertainty reduction: check, compare, verify, ask, escalate, withhold. A well-shaped landscape does not eliminate attraction. It makes the right kind of attraction occur before the wrong kind of action becomes too easy.

**Investigation** is motion toward uncertainty reduction. It occurs when the system treats an unresolved question as action-relevant. The system does not need to investigate everything. It needs to investigate what could change the decision. If a healthcare campaign claim may cross from operational language into clinical-outcome language, the relevant investigation is not "find more material about remote patient monitoring." It is "do we have approved evidence for this specific claim?"

**Sufficiency** is the stopping condition. It is the point at which the current reasoning state becomes enough to act, ask, escalate, refuse, draft, or defer. Sufficiency is not certainty. A system may be highly confident in one fact but still lack enough information for the decision. It may be uncertain about the exact cause of a problem but have enough reason to choose a safe bounded action.

**Action** is the behavioral exit from the current reasoning state. Action is not always task completion. Sometimes the right action is to ask a human, escalate, pause, reject a claim, produce a bounded draft, or preserve uncertainty for later review. A system that can only complete the requested task has fewer safe exits than a system that can treat uncertainty as actionable.

The core movement is:

**Attraction → Investigation → Sufficiency → Action**

The value of the sequence is not that every workflow follows it neatly. The value is that it exposes a design question: where did the system stop moving, and why?

That question leads to **premature sufficiency**.

Premature sufficiency occurs when a system treats its current reasoning state as adequate for action before the information surfaces designed to govern that action have become behaviorally effective. This gives the concept a design-time criterion. If the architecture specifies that an evidence boundary, policy rule, approval condition, prior incident, or uncertainty check must shape a class of action, and the system acts before encountering or processing that surface, sufficiency was premature.

This criterion matters because premature sufficiency should not be only a post-hoc label applied after a bad outcome. A designer should be able to say in advance: for this action type, these surfaces must be active before action can proceed. If the agent bypasses them, the failure is diagnosable even before the campaign underperforms, the tool call causes harm, or the human reviewer catches the error. If no such surface was designed, the problem is deeper: the landscape had no intended counterpressure to begin with.

The system does not merely lack information. It stops moving too soon relative to the architecture that was supposed to govern the action.

This pattern is easy to miss because the output may look competent. A fluent answer can sound grounded. A polished campaign claim can sound professional. A tool call can look efficient. A workflow completion can look like success until the downstream consequence appears.

Premature sufficiency is not the only failure mode in human-agent systems. Some failures come from missing capability, ambiguous goals, flawed tools, poor user instructions, model-internal behavior, or genuinely novel situations. The narrower claim is that many failures become diagnosable when we ask what made the current path feel action-ready before the right counterpressure arrived.

Consider hallucination. A model is asked for an answer. A fluent completion becomes available. The answer fits the user's question, resembles patterns the model has seen, and carries no visible requirement to cite or verify. If evidence is unavailable, weakly represented, or optional, the fluent path may become sufficient before grounding occurs. This account does not replace model-level explanations of hallucination such as training-data distribution, decoding behavior, or attention patterns. It adds a design-side diagnosis: the landscape allowed unsupported completion to become action-ready before grounding became behaviorally effective. [Maynez et al., 2020; Ji et al., 2023; Huang et al., 2023]

Unsafe tool use can follow the same structure with different stakes. An agent is asked to fix a problem. A tool is visible. The action is familiar. The goal creates pressure to complete the task. If policy, consequence, approval, or prior-failure memory does not shape the reasoning state first, the tool path may become action-ready before risk has been resolved. The result may be an unauthorized message, a risky restart, an incorrect database update, or an irreversible workflow action. [Parasuraman and Riley, 1997; Lee and See, 2004]

The point is not that hallucination and unsafe tool action are the same. They are not. They differ in severity, evaluation method, mitigation strategy, and ethical consequence. The point is that both can share a motion structure: goal pressure makes completion attractive; grounding or constraint fails to redirect investigation; confidence attaches to a path before the decision is warranted; action follows.

The healthcare campaign example makes this concrete. The phrase "reduces readmissions" has a strong gradient. It is short, persuasive, and aligned with the business goal. It sounds more consequential than "supports monitoring between visits" or "improves care-team visibility." It may also be surrounded by adjacent truths: the product supports remote monitoring, care teams need better visibility, and readmissions matter to healthcare organizations.

But adjacent truth is not sufficient support for a direct clinical-outcome claim.

A context-only system may investigate the topic without investigating the decisive premise. It may retrieve more material about remote monitoring, patient follow-up, and care coordination. That investigation produces more context, but it does not answer the question that should govern action: is this claim approved and evidenced for this product?

The reasoning-state alternative changes the stopping condition. The system can proceed with operational-value language, but the direct outcome claim remains insufficient unless approved evidence or approved language is available. The action is not "generate the stronger claim." It is "draft within the supported boundary and flag the unresolved claim."

A similar pattern appears in operations. An agent sees a slow service and has access to a restart tool. Restart is familiar, visible, and often effective. The tool path has a strong gradient. But if this service has dependencies, if a prior restart worsened a similar incident, or if approval is required under certain conditions, then "service is slow" is not yet sufficient for restart. The safer action may be to check dependencies, surface the prior incident, or escalate.

Better behavior is not paralysis. It is motion through a better-shaped landscape.

This is why "I do not know" and "I should not act yet" matter. They are not signs of weakness in an agentic system. They are action affordances. They give the system somewhere legitimate to go when the current reasoning state is not enough for the requested action. Without those exits, uncertainty has no stable surface. The landscape continues to slope toward completion because completion is the only recognized success path.

Designing against premature sufficiency means shaping counterpressure before action. Evidence requirements must appear when claims are generated. Policies must connect to the action types they govern. Prior failures must surface when similar premises become active. Confidence must be calibrated to source quality and applicability. Human confirmation must be available before uncertain interpretations become durable reasoning state.

The diagnostic question becomes sharper:

**What made this path feel sufficient?**

---

## 6. Reasoning-State Architecture

If premature sufficiency is a failure of motion, the design response cannot be only more context. The system needs a way to preserve the reasoning condition from which action became justified, withheld, escalated, or revised.

That is the role of a reasoning-state architecture.

The word architecture is used carefully here. This section is not proposing a particular software stack, database schema, orchestration framework, or vendor implementation. It describes the reasoning objects that must survive across a human-agent workflow if the system is to be governable and learnable. Implementation may vary. The preservation problem does not.

The architectural claim follows the same bounded-design logic used throughout the framework: a useful system does not preserve everything; it preserves the state required for future action, judgment, and learning. [Simon, 1955; Lee, 1997]

A context-only system can retrieve artifacts. A reasoning-state system must preserve the movement among them: what goal was active, what constraint applied, what premise made an action attractive, what uncertainty remained, why action became sufficient, what outcome followed, and what changed afterward.

The architecture has six core reasoning-state objects and one loop-closing state:

1. Optimizer State
2. Premise Stack
3. Decision State
4. Investigation Trace
5. Learning Event
6. Model Update Object
7. Modified Optimizer State

These objects are not meant to record everything. They are a minimum viable structure for preserving the "why" behind action. Too little state leaves the system repeating mistakes with better retrieval. Too much state creates an archive no future human or agent can use.

These objects should not be confused with ordinary agent memory, reflection loops, or chain-of-thought traces. Memory can store prior material. Reflection can improve an agent's next attempt. Chain-of-thought can expose or simulate intermediate reasoning within a response. Reasoning-state objects have a different target: they preserve decision-relevant structure across cycles, across agents, and across organizational contexts. The question is not only whether this agent can improve this attempt, but whether a future human-agent workflow can inherit the goal, premise, evidence boundary, uncertainty, and update that should shape the next decision. [Park et al., 2023; Shinn et al., 2023; Madaan et al., 2023]

### 6.1 Optimizer State

The Optimizer State is the working frame from which the system begins. It contains three primitives: **Goal**, **Policy**, and **Interpretation**.

The **Goal** defines what the system is trying to accomplish. A goal may be explicit, such as "draft a campaign brief," or implicit in a workflow, metric, prompt, or tool configuration. Goal matters because it determines what can become relevant. The same artifact can be decisive under one goal and peripheral under another.

The **Policy** defines what should constrain action. Policy includes formal rules, compliance requirements, safety boundaries, brand standards, escalation conditions, privacy limits, and human-approval requirements. A policy does not govern behavior merely by existing. It must become active inside the reasoning state before action proceeds.

The **Interpretation** is the system's working understanding of the situation. It turns available signals into meaning: what the case appears to be, what the information implies, what risk exists, and what kind of action seems appropriate. Actors do not respond to raw information; they respond to the meaning they construct from it. [Weick, 1995]

Optimizer State matters because action is never selected from neutral context. It is selected from a frame. If that frame is wrong, incomplete, or unexamined, later reasoning may be coherent while still moving in the wrong direction.

### 6.2 Premise Stack

The Premise Stack contains the claims, assumptions, evidence, and interpretations that make a possible action seem reasonable.

A premise stack is not just a list of facts. It is the support structure beneath an action. In a healthcare campaign, the premise stack might include: cardiology practice administrators care about between-visit visibility; workflow burden is a relevant pain point; operational-value language is currently supportable; direct clinical-outcome language requires approved evidence.

The premise stack is where many failures become visible. A system may act from a strong goal and weak premises. It may rely on adjacent truth rather than direct support. It may treat prior campaign language as evidence when it is only precedent. It may inherit an assumption from a previous workflow without noticing that the current boundary conditions differ.

Preserving the premise stack gives future reviewers something to inspect. They can ask: which premise failed? Which premise was unsupported? Which premise was true but insufficient? Which premise should transfer to the next cycle?

Without that structure, correction becomes shallow. A reviewer may delete a claim, but the system does not learn why the claim should not have become action-ready in the first place.

### 6.3 Decision State

Optimizer State is the starting frame. Decision State is the pre-action snapshot: the point where the system records whether the current reasoning is sufficient, insufficient, or bounded.

It should answer three questions:

- What action is currently proposed?
- What alternatives were materially considered?
- Why is the current state sufficient, insufficient, or bounded?

Decision State is where sufficiency becomes explicit. The system should not only produce an answer or call a tool. It should preserve the reason it believed the current path was ready for action.

In some cases, the Decision State supports direct action. The claim is supported. The policy boundary is satisfied. The uncertainty is not material enough to change the decision.

In other cases, the Decision State should block or redirect action. The evidence is insufficient. The policy boundary is unresolved. The tool consequence is unclear. The system should ask, escalate, defer, or produce a bounded draft.

This is where "I do not know" and "I should not act yet" become architectural possibilities rather than conversational manners. They are legitimate decision states. They preserve the fact that the system had enough understanding to know that completion was not yet warranted.

### 6.4 Investigation Trace

The Investigation Trace records what uncertainty the system treated as action-relevant and what it did to reduce it.

This object exists because investigation can be performative. A system may search, retrieve, summarize, or cite material while never testing the premise that actually matters. In the healthcare campaign example, the system may retrieve more information about remote patient monitoring while failing to ask whether "reduces readmissions" is an approved claim for this product.

A useful Investigation Trace should preserve the material question, the sources or surfaces consulted, what was found, what was not found, and whether the uncertainty was resolved. It should not become a transcript of every search. The point is to preserve the investigation that could change the action.

This is close to information foraging: the value of search lies not in activity itself, but in whether the path taken reduces the uncertainty that matters for action. [Pirolli and Card, 1999]

Investigation Trace can also operate after action. If a campaign underperforms, the relevant trace may capture how the team investigated which premise failed rather than only what the agent checked before launch.

This gives future humans and agents a way to distinguish between explored uncertainty and ignored uncertainty. It also prevents a common failure: treating the presence of search activity as evidence of sufficient investigation.

### 6.5 Learning Event

A Learning Event begins when the world answers back.

An action is taken under some expectation. The result may confirm the expectation, contradict it, or reveal that the expectation was underspecified. Learning begins when that result is compared against the reasoning state that produced the action.

This matters because outcomes do not explain themselves. A campaign may receive attention but fail to produce qualified demand. A tool call may complete a task while creating downstream risk. A support response may satisfy the immediate user while teaching the wrong pattern to the knowledge base. In each case, the outcome is evidence, not learning.

The Learning Event should preserve the expectation, the observed outcome, the mismatch, and the explanation selected after investigation. This connects the architecture to organizational learning. Single-loop learning corrects action within existing assumptions. Double-loop learning changes the assumptions that govern future action. [Argyris and Schon, 1978]

A Learning Event is not a postmortem pasted into memory. It is the structured comparison between what the system expected and what reality returned.

### 6.6 Model Update Object

The Model Update Object is the piece that turns learning into changed future reasoning.

A correction changes an artifact. A Model Update Object changes the conditions under which future action should become sufficient.

The update may revise an audience interpretation, lower confidence in a premise, add an evidence boundary, change an escalation rule, alter a retrieval priority, or mark a lesson as applicable only under certain conditions. The important point is not the label. The important point is that the update must be reusable.

A useful Model Update Object should preserve:

- what changed;
- why it changed;
- what evidence supports the change;
- where the change applies;
- how confident the system should be in applying it.

A stored postmortem says what happened. A Model Update Object says how future reasoning should begin differently.

The update must also avoid overgeneralization. If workflow-burden messaging produced attention but weak qualified demand, the lesson is not "workflow burden does not matter." A better update might be: workflow burden is an attention signal, but not by itself a buying-readiness signal. A crude update can damage future reasoning as easily as no update at all.

**Table 2. Minimum Viable Reasoning Objects**

| Reasoning-state object | What it preserves | What fails without it |
|---|---|---|
| **Optimizer State** | The active goal, governing policy, and working interpretation. | The system may reason coherently from the wrong frame. |
| **Premise Stack** | The assumptions, claims, and evidence that make an action appear reasonable. | Reviewers can correct outputs but cannot identify which premise failed. |
| **Decision State** | The proposed action, material alternatives, and sufficiency status before action. | The system acts without preserving why action, pause, escalation, or refusal was warranted. |
| **Investigation Trace** | The uncertainty treated as action-relevant and the search or inquiry used to reduce it. | Search activity may be mistaken for meaningful investigation. |
| **Learning Event** | The expectation, observed outcome, mismatch, and explanation after reality responds. | Outcomes are stored as facts but do not become learning. |
| **Model Update Object** | The changed expectation, boundary, confidence level, applicability condition, or future action rule. | The same error can recur because the correction never changes future reasoning. |
| **Modified Optimizer State** | The next-cycle frame after learning has been applied. | The system appears to remember but begins the next cycle from unchanged assumptions. |

### 6.7 Modified Optimizer State

A Model Update Object matters only if it changes the next cycle.

Reasoning-state architecture succeeds only if the next Optimizer State begins from improved conditions. The active goal may be the same, but the interpretation should be different. The policy boundary may be unchanged, but it should be more visible. The prior premise may still be usable, but with lower confidence or narrower applicability.

This closes the loop:

**Optimizer State → Premise Stack → Decision State → Investigation Trace → Learning Event → Model Update Object → Modified Optimizer State**

The loop is not meant to imply a rigid linear workflow. Human-agent systems will branch, pause, revise, and operate at multiple levels of granularity. The point is simpler: if the system cannot preserve the transition from action to update, it cannot reliably learn from its own history. At the organizational level, this is the difference between stored memory and reusable memory. [Walsh and Ungson, 1991]

### 6.8 Architecture as Governance Surface

Reasoning-state architecture is also a governance surface.

Governance often fails when it remains outside the reasoning state. A rule is written, but not connected. A review step exists, but arrives after the action. A human approval requirement is present, but the system does not know which action class triggers it. A postmortem is stored, but never changes the next decision.

When governance is represented inside reasoning state, it can shape action earlier. Policies can attach to claims. Approval requirements can attach to tool calls. Evidence thresholds can attach to outcome language. Prior incidents can attach to similar premises. Human confirmation can attach to interpretations that will persist.

This does not remove the need for external controls. Some actions should still be technically blocked, sandboxed, reviewed, or logged. For high-stakes, irreversible, or externally consequential actions, external controls remain mandatory; reasoning-state governance is an additional layer, not a substitute. The point is that external controls and reasoning-state governance solve different problems. External controls constrain what the system can do. Reasoning-state governance shapes what the system treats as justified before it tries to do it. Section 9 returns to the risk that reasoning-state objects themselves can be manipulated, over-trusted, or captured by organizational politics.

### 6.9 What the Architecture Does Not Claim

This architecture does not make agents safe by default. It does not guarantee correct reasoning. It does not eliminate the need for evaluation, monitoring, human judgment, or hard permissions. It also does not require every workflow to preserve every object at the same level of detail.

The claim is more bounded: if human-agent systems are expected to act, learn, and remain governable across repeated workflows, then some version of reasoning-state preservation is required. Otherwise the system may keep retrieving more context while losing the decision logic that should have changed its future behavior.

A reasoning-state architecture is therefore not an alternative to context. It is the structure that lets context become reusable judgment. Section 10 later proposes a maturity model for evaluating how consistently these objects are preserved and reused across workflows.

---

## 7. Discovery and Human Confirmation

Reasoning-state architecture creates a new responsibility: the system must not silently convert inferred human intent into durable state.

A human-agent workflow rarely begins with full specification. The human gives a goal, a fragment of context, a desired outcome, a constraint, or a rough description of the situation. The agent has to interpret what was meant. That inference is not a bug. It is part of the work.

The danger begins when the inference hardens before the human has seen it.

Discovery is the process that sits between human intent and preserved reasoning state. It is not better intake. It is pre-action topography design.

That distinction matters. Intake collects what the human says. Discovery exposes what the system thinks the human means. Intake asks for information. Discovery proposes a frame and gives the human a chance to correct it before the frame shapes action, memory, or learning.

The basic loop is:

**Retrieve → Infer → Propose → Confirm**

The system retrieves what is already available. It infers a working interpretation. It proposes that interpretation back to the human in a form that can be corrected. The human confirms, rejects, revises, or bounds it. Only then should the interpretation become part of durable reasoning state.

Human intent is often underspecified in ways that matter. A marketer may ask for a healthcare campaign without naming the evidence boundary. A product manager may ask for a launch plan without stating which risk is unacceptable. A support lead may ask for automation without specifying when the system should stop and escalate. The agent can often make a plausible inference. Plausible is not confirmed.

Two bad designs sit on either side of Discovery.

One is **blank-form burden**. The system asks the human to specify everything up front: goals, audiences, constraints, success metrics, exception rules, and escalation conditions. That protects the system from guessing, but it shifts too much interpretive labor to the human. The human has to do the structuring work the agent should be helping with.

The other is **silent inference**. The system fills the gaps, chooses the frame, and proceeds. This feels efficient. It is often impressive in the first turn. But the reasoning state now rests on unconfirmed interpretation. If the system later acts from that interpretation or preserves it for reuse, guesswork has become architecture.

Discovery is the alternative to both failures.

A good Discovery process does not ask the human to build the whole frame from scratch. It also does not hide the frame. It proposes the frame.

The agent should be able to say, in substance:

> Here is what I think you are trying to accomplish.
> Here is what I think constrains the work.
> Here is the interpretation I would use unless corrected.
> Here are the uncertainties that could materially change the action.
> Confirm, revise, or bound this before I preserve it.

The wording will vary. The architectural move does not: the system makes its inferred reasoning state visible before treating it as stable.

Mixed-initiative systems already reject the false choice between full automation and full manual control. They allocate work between human and machine according to uncertainty, cost, and consequence. [Horvitz, 1999] Human-AI interaction guidelines make a similar demand: systems should make clear what they can do, support correction, show contextually relevant information, and allow users to control or override behavior. [Amershi et al., 2019]

Discovery applies that logic to reasoning state. The system does the first pass of structure-building. The human validates the parts that matter.

It also has to manage automation bias. Fluent system outputs can make an inferred frame feel more settled than it is. [Parasuraman and Riley, 1997; Lee and See, 2004] The propose step can anchor the human toward the system's interpretation. That is a real limitation of propose-then-confirm patterns. Discovery must therefore expose uncertainty, make alternatives easy to see, and make correction cheaper than passive agreement.

The object of Discovery is the Optimizer State.

Before an agent acts, the workflow needs at least a confirmed Goal, Policy, and Interpretation. The Goal establishes what the system is trying to accomplish. The Policy identifies what should constrain action. The Interpretation defines how the system understands the situation.

Discovery does not need perfect certainty on all three. It needs enough confirmed structure to prevent the system from acting inside a private interpretation of the task.

A healthcare campaign example shows the difference. A user asks:

> Draft a campaign for our remote patient monitoring product for cardiology practices.

A silent-inference system may proceed as if the goal is maximum persuasive impact, the audience is any cardiology decision-maker, and the strongest message is clinical outcome improvement. It may produce polished work that rests on unconfirmed assumptions.

A blank-form system may ask the user to define every audience segment, compliance rule, evidence threshold, funnel stage, approved claim, and success metric before producing anything. That may be safer, but it is not how real work usually moves.

A Discovery-oriented system proposes a frame:

> I understand the goal as generating qualified demo interest from cardiology practice administrators. I will treat operational workflow burden and between-visit visibility as the primary message frame. I will not use direct clinical-outcome claims such as reduced readmissions unless approved evidence or approved language is supplied. Is that the right frame?

That is not just a clarification question. It is a proposed Optimizer State. The human can correct the goal, change the audience, supply approved evidence, or confirm the boundary. Once confirmed, the frame can be preserved and reused.

Discovery should focus on material uncertainty. Not every missing detail deserves human attention. If a choice will not change the action, asking about it creates friction without improving reasoning. But deciding which uncertainties are material is itself a design problem. The system has to model which unknowns could change the goal, policy, interpretation, evidence threshold, action boundary, or future learning path, and that model will vary by domain.

The infer-confirm loop also creates a record. When the human confirms or revises the proposed frame, that confirmation becomes part of reasoning state. The system can later distinguish between what it inferred, what the human confirmed, what remained uncertain, and what was only provisionally assumed.

That distinction matters when outcomes arrive. If a campaign underperforms, the system should not simply say the human asked for the wrong campaign. It should know which frame was confirmed, which assumptions were provisional, and which uncertainty remained unresolved. Learning then has somewhere to attach.

Discovery can fail in predictable ways.

It can become performative, asking the human to confirm obvious statements while hiding the real assumptions.

It can become manipulative, steering the human toward the system's preferred interpretation.

It can become burdensome, requiring confirmation of details that do not matter.

It can become brittle, treating one human confirmation as permanent after context changes.

It can become unsafe, preserving sensitive or mistaken instructions as durable state without appropriate boundaries.

These risks return in the boundaries and objections section because Discovery can itself become a source of distortion.

Useful Discovery makes material assumptions visible, preserves human corrections, keeps uncertainty alive when unresolved, and treats confirmation as scoped rather than universal.

Confirmation should therefore have boundaries.

A human may confirm that operational workflow burden is the right campaign frame for this launch. That does not mean the frame applies to every future campaign. A compliance reviewer may confirm that a phrase is approved under one evidence package. That does not mean the system can use related phrases freely. A product lead may confirm that a capability is strategically important. That does not mean the system should treat it as a proven customer pain point.

Human confirmation is not magic. It is evidence within scope.

Discovery must preserve that scope. Who confirmed the interpretation? Under what conditions? For what workflow? With what confidence? Until when? A confirmation without scope can become a new source of premature sufficiency.

Discovery also changes the role of the user. The user is not merely a prompt writer. The user becomes a participant in constructing the system's operating landscape. That does not mean the user must specify everything. It means the system must expose the interpretations that will matter before they harden into action, memory, or learning.

The test is simple:

**Did the system make the important inference reviewable before acting from it?**

If yes, the process has done useful work.

If no, the system may still produce a good output. But it did so from an unconfirmed frame, and the organization may later preserve that frame as if it had been shared understanding.

Discovery gives architecture something worth carrying. Architecture gives Discovery somewhere durable to go.

---

## 8. Constructed Stress Test: Healthcare Marketing Campaign

The idea now has to do work.

A concept can sound plausible in abstraction and still fail when applied to a real workflow shape. The test here is modest but important: can the framework produce a different diagnosis than "add more context," "write a better prompt," or "send it to compliance later"?

The scenario is author-constructed. It is not a field study, benchmark, or empirical validation. A stress test in this context means applying the framework to a plausible workflow shape to see whether its diagnostic vocabulary produces a different and useful diagnosis. This use is closest to design-science and theory-building uses of constructed cases: not proof by example, but a way to make claims concrete enough to examine. [Hevner et al., 2004; Siggelkow, 2007]

The assignment and artifact set stay constant. The reasoning architecture changes. If the same materials produce different paths of attention, investigation, sufficiency, and action, then the framework has at least earned its diagnostic role.

The domain is healthcare marketing because the stakes are useful for the argument. Campaign work is familiar and practical, but healthcare claims bring evidence boundaries, policy constraints, and review obligations into the workflow. It is easy for a system to produce polished language. It is harder for the system to know when polished language has crossed a boundary.

### 8.1 The Assignment

A marketing team asks for campaign messaging for a remote patient monitoring product aimed at cardiology practices.

The business goal is to generate qualified demo interest.

The product supports monitoring between visits. It gives care teams a way to review patient information, identify signals that may require attention, and coordinate follow-up within clinical and operational workflows.

The audience is plausible but not fully settled. Cardiology practice administrators may care about staffing pressure, workflow burden, patient follow-up, and visibility between visits. They may also care about clinical outcomes, but clinical-outcome claims require approved evidence and approved language.

That boundary matters.

The phrase **"reduces readmissions"** appears attractive almost immediately. It is short, persuasive, and connected to a real healthcare concern. It sounds more consequential than "supports between-visit monitoring." It also rests near adjacent truth: information that is related to a claim but does not directly support that specific claim. Readmissions matter. Remote monitoring can support better visibility. Care teams need tools for follow-up.

But adjacent truth is not enough.

A direct claim that a product reduces readmissions is not the same as a statement that the product supports monitoring, visibility, or workflow coordination. The first is a clinical-outcome claim. The second is operational-value language. A safe campaign system has to know the difference before the claim becomes action-ready.

### 8.2 Common Artifact Set

Both workflows receive the same materials.

They have product descriptions, audience research, prior campaign examples, campaign-performance reports, sales notes, general compliance guidance, approved-claims material, and prior lessons from related campaigns.

Nothing in the stress test depends on hidden information. The reasoning-state workflow does not get a secret document. The context-only workflow is not starved. The difference is how the materials become behaviorally effective.

The approved-claims material supports product-capability and operational-value statements. It does not confirm a direct claim that this product reduces readmissions.

The compliance guidance says that direct clinical-outcome claims require approved evidence and approved language.

Prior campaign material contains outcome-adjacent language, but not a durable evidence boundary. Prior language can become dangerous precedent. A phrase appearing in old material does not prove it should govern the next campaign.

### 8.3 Context-Only Workflow

The context-only system receives the assignment and retrieves relevant artifacts.

It sees that remote patient monitoring supports visibility between visits. It sees that cardiology practices experience workflow pressure. It sees that readmissions matter in healthcare. It sees prior language that moves near clinical outcomes.

The materials point in a persuasive direction.

A likely working interpretation emerges:

> Cardiology practices need remote monitoring to improve patient follow-up, reduce operational burden, and support better outcomes.

That interpretation is not foolish. It is close enough to the source material to feel grounded. The danger is that it blends several different things: what the audience cares about, what the product enables, what the organization can safely claim, and what evidence has actually been approved.

The phrase "reduces readmissions" now has a strong gradient. It fits the goal. It sounds valuable. It gives the campaign a sharper hook. It turns a product capability into an outcome.

The system may investigate, but it investigates the topic rather than the decisive premise. It retrieves more material about remote monitoring, patient follow-up, operational burden, care-team visibility, and readmission pressure. That search produces more context. It does not answer the question that governs the claim:

> Is "reduces readmissions" approved and evidenced for this product?

If that question never becomes active, the system may produce copy like:

> Help cardiology teams monitor patients between visits, coordinate follow-up, and reduce preventable readmissions.

The sentence is fluent. It is plausible. It sounds like normal healthcare marketing. It may even be directionally aligned with the organization's aspirations.

But the reasoning state is not sufficient for the claim.

A context-only system could catch this failure if it included explicit compliance-review steps. The point is not that context-only workflows are incapable of review. The point is that the reasoning-state workflow makes the boundary active during generation rather than relying on post-generation correction.

The failure is not simply that the system lacked context. The system had context. The failure is that the evidence boundary did not become behaviorally effective before generation. The policy existed as information, but not as an active constraint on the sentence being produced.

A reviewer might later catch the problem. The unsupported phrase may be deleted. The campaign may be corrected.

But correction is not learning. Unless the reasoning state is preserved, the system may reproduce the same failure in softer language next time: "lowers hospitalizations," "prevents avoidable admissions," "keeps patients out of the hospital," or any other claim that feels close enough to the same unsupported outcome. [Argyris and Schon, 1978]

The artifact changed. The path that produced the artifact did not.

### 8.4 Reasoning-State Workflow

The reasoning-state workflow receives the same assignment and the same artifacts.

The attractive claim still appears. The system is not made safer by pretending "reduces readmissions" is not compelling. It is compelling. The point is to make the other forces in the landscape strong enough to matter before the claim becomes action-ready.

The workflow begins by forming an Optimizer State.

The Goal is not merely "make a strong campaign." It is to generate qualified demo interest from cardiology practice administrators and operational leaders.

The Policy is not merely "be compliant." It is that direct clinical-outcome claims require approved evidence and approved language.

The Interpretation is provisional: cardiology practice administrators likely care about workflow burden, between-visit visibility, and follow-up coordination. Clinical outcomes may matter, but the system does not yet have support for a direct outcome claim.

That frame changes the next move.

When the phrase "reduces readmissions" appears, the system does not treat it as ordinary campaign language. It treats it as a claim type with an evidence boundary. The active question becomes:

> Do we have approved evidence or approved language for this direct clinical-outcome claim?

The Investigation Trace now targets the decisive premise. The system checks approved-claims material, product evidence, compliance guidance, and any existing language that would authorize the claim. It finds support for operational-value language. It does not find confirmed support for the direct readmissions claim.

That result changes sufficiency.

The direct outcome claim is not sufficient.

The campaign itself can still proceed.

A reasoning-state system can draft within the supported boundary:

> Give care teams greater visibility between visits with remote monitoring designed around clinical and operational workflow.

Or:

> Help cardiology teams review patient information, coordinate follow-up, and manage between-visit visibility without adding unnecessary workflow burden.

The system can also preserve the unresolved question:

> Direct readmission-reduction language requires approved evidence or approved claim language before use.

The action is not refusal. It is bounded progress.

A cautious system that only blocks work becomes unusable. A useful system preserves the boundary while still helping the team move.

### 8.5 Where the Workflows Diverge

The two workflows do not diverge because one has better raw information.

They diverge because one treats context as material and the other treats reasoning state as material.

**Table 3. Where the Workflows Diverge**

| Decision point | Context-only workflow | Reasoning-state workflow |
|---|---|---|
| Goal | Produce persuasive campaign messaging. | Generate qualified demo interest within claim boundaries. |
| Claim attraction | "Reduces readmissions" becomes a strong campaign hook. | The same phrase is recognized as a direct clinical-outcome claim. |
| Policy role | Compliance guidance exists but remains general. | Evidence boundary is connected to the specific claim type. |
| Investigation | Searches related topic material. | Tests the decisive premise: approved evidence or approved language. |
| Sufficiency | Plausibility and adjacent truth make the claim feel usable. | Operational language is sufficient; direct outcome language is not. |
| Action | Generates polished but unsupported claim language. | Drafts within supported boundary and flags unresolved claim. |
| What survives | The draft, maybe a later correction. | Goal, policy, interpretation, evidence boundary, investigation result, and sufficiency rationale. |

The final row is the most important.

A context-only system may leave behind the artifact. A reasoning-state system leaves behind the conditions that shaped the artifact.

That is the difference between a reusable campaign and a reusable lesson.

### 8.6 After the Campaign

Suppose the bounded campaign runs.

It generates attention. Opens are strong. Landing-page visits are respectable. Qualified demo conversion is weaker than expected.

A conventional memory system can store the result:

> Good engagement. Weak qualified demand.

That is useful, but it is not yet learning.

The reasoning-state system can compare the outcome against the preserved expectation. The expectation was not simply "people care about remote monitoring." The more specific premise was:

> Workflow burden and between-visit visibility will generate qualified demo interest from cardiology practice administrators.

The outcome complicates that premise.

A reasonable Model Update Object might be:

> Workflow burden appears to be an attention signal, but not by itself a reliable buying-readiness signal. Future campaigns should preserve operational-value positioning while adding stronger readiness filters, such as active RPM evaluation, staffing constraints tied to monitoring workload, or explicit interest in between-visit visibility.

The clinical-claim boundary remains unchanged:

> Do not use direct readmission-reduction language unless approved evidence or approved claim language is supplied.

Now the next campaign starts differently. Not because the system remembers the old copy, but because it inherits the changed reasoning state.

The learning claim is illustrated here in shape, not proven. The scenario shows what it would mean for a future workflow to inherit a changed reasoning state rather than only a prior artifact.

### 8.7 What the Stress Test Shows

The stress test does not prove that reasoning-state architecture will outperform context-only systems in production. It does not prove that the five topography dimensions are complete. It does not prove that every healthcare marketing workflow should use this exact structure.

It shows something narrower.

The framework produces a different diagnosis. The unsupported claim is not merely a hallucination, a compliance miss, or a retrieval failure. It is a premature-sufficiency failure caused by weak connectivity between claim generation and the evidence boundary.

The framework produces a different intervention. The answer is not only "retrieve the compliance document." The intervention is to make the evidence boundary active at claim-generation time and preserve the sufficiency rationale.

The framework produces a different memory object. The useful residue is not only the final campaign or postmortem. It is the reasoning transition: goal, policy, interpretation, premise, investigation, decision, outcome, and update.

The framework preserves useful motion. The system does not freeze when a claim is unsupported. It moves through a better path: draft within the supported boundary, flag the unresolved claim, and preserve what would be needed to use stronger language later.

The goal is not validation. It is examinability. The scenario makes the framework's claims visible enough to challenge. A reviewer can ask whether the evidence boundary really should have been active, whether the claim distinction is too conservative, whether the same diagnosis could be produced by ordinary compliance review, or whether the reasoning-state workflow adds too much overhead.

Those objections are welcome. A framework that cannot be challenged cannot become useful.

---

## 9. Boundaries, Objections, and Disconfirmation Conditions

The argument should be allowed to lose.

A framework that explains every failure explains too much. If perceived topography can be used after the fact to relabel any outcome as a landscape problem, then it is not a diagnostic tool. It is vocabulary. The useful version has boundaries, rival explanations, and conditions under which it should lose scope.

The claim is bounded. Human-agent systems often act from a constructed information-and-action landscape. That landscape can make some paths easier, safer-looking, more trusted, or more sufficient than others. Reasoning-state architecture can help preserve the conditions from which action became justified, withheld, escalated, or revised.

That is not the same as saying that every agent failure is a topography failure.

Some failures are model failures. The model may lack capability, misgeneralize, hallucinate from internal patterns, mishandle long context, fail at planning, or produce unstable outputs under decoding conditions. Some failures are tool failures. A tool may be broken, poorly documented, misconfigured, or unsafe by design. Some failures are organizational failures. The human goal may be incoherent, the policy may be bad, the incentive may reward speed over truth, or the institution may not actually want the constraint it claims to want.

Perceived topography does not erase those explanations. It asks a narrower question:

**What did the system experience as the actionable world before it moved?**

That question is useful only if the answer changes diagnosis or design.

### 9.1 The Unfalsifiability Objection

The strongest attack is not that the framework is wrong. It is that the framework could become impossible to prove wrong.

If every failure can be described as a topography failure, then the framework risks becoming a post-hoc explanation machine. A hallucination becomes a confidence failure. A tool error becomes a connectivity failure. A weak campaign becomes a premature-sufficiency failure. A bad update becomes a Model Update Object failure. The vocabulary expands until it can absorb anything.

That would be a real failure.

A diagnostic framework should not win by relabeling every bad outcome in its own language. It should win only when its distinctions reveal something that competing explanations miss and when those distinctions change what a designer would do next.

The framework therefore needs a discipline of loss. A failure should not count as a topography failure merely because some landscape description can be written afterward. It should count only when the relevant landscape properties can be specified in advance or reconstructed with enough precision to explain why a different design would have changed the path of attention, investigation, sufficiency, or action.

Premature sufficiency is the clearest example. If a designer cannot say which evidence boundary, policy surface, prior incident, uncertainty signal, or confirmation requirement should have become behaviorally effective before action, then calling the outcome premature sufficiency adds little. It becomes a name for regret.

The same test applies to the five dimensions. They matter only if they separate failures that require different repairs. If the same intervention follows no matter which dimension is named, the dimensional vocabulary is ornamental.

This is the line between diagnosis and storytelling.

### 9.2 Boundary of the Claim

The framework applies most clearly when four conditions hold.

First, the system has a goal or task orientation. It is trying to answer, draft, classify, route, recommend, call a tool, update a record, or otherwise move work forward.

Second, the system operates through information surfaces. It relies on documents, memories, prompts, retrieval results, policies, tool outputs, user instructions, dashboards, examples, or prior artifacts.

Third, the system has more than one possible path. It can investigate, answer, ask, escalate, defer, use a tool, refuse, or produce a bounded artifact.

Fourth, the action has enough consequence that the path matters. If the action is trivial, reversible, or purely exploratory, full reasoning-state preservation may add more burden than value.

The framework is less useful when the problem is primarily raw capability, deterministic rule execution, or simple lookup. If a model cannot perform arithmetic, topography is not the first diagnosis. If a workflow requires only a fixed rule over a clean input, reasoning-state architecture may be unnecessary. If no action, memory, or learning will follow, the cost of preserving state may exceed the benefit.

The point is not to use the framework everywhere. The point is to use it where behavior depends on what the system can notice, reach, interpret, trust, connect, and carry forward.

### 9.3 What the Framework Does Not Claim

The framework does not eliminate politics. Organizations still choose goals, reward some behaviors over others, bury inconvenient constraints, and preserve some lessons while ignoring others.

It does not replace domain expertise. A healthcare claim boundary, legal interpretation, clinical evidence standard, security policy, or operational risk judgment still requires people and institutions with the authority and competence to define it.

It does not prove safety. A better-shaped landscape can reduce some failure paths while leaving others untouched.

It does not make governance legitimate merely because governance can be automated. A policy can become behaviorally effective and still be a bad policy. An approval process can be well represented and still serve the wrong interest.

These boundaries matter because the framework is not a theory of institutional goodness. It is a way to diagnose how information, constraint, confidence, and action become behaviorally effective inside human-agent systems.

### 9.4 Objection: This Is Just Good System Design

The strongest ordinary objection is that perceived topography is simply a new name for good system design.

The objection is partly right.

Good system design already cares about information placement, workflow friction, user feedback, permissions, review, and error recovery. Human-computer interaction, organizational learning, and safety engineering all have mature ways to describe pieces of this problem. [Norman, 1988; Horvitz, 1999; Amershi et al., 2019; Argyris and Schon, 1978]

The contribution is not that design matters. The contribution is a shared diagnostic surface for a specific failure pattern: action becoming sufficient before the right evidence, constraint, uncertainty, or confirmation has shaped the decision.

"Good design" is too broad to diagnose that failure. It can name the aspiration, but not always the mechanism. Perceived topography asks which dimension failed: Visibility, Accessibility, Representation, Confidence, or Connectivity. Premature sufficiency asks why the system stopped moving. Reasoning-state architecture asks what needs to survive so the next cycle can begin from better conditions.

If those distinctions do not change the diagnosis, the framework adds little. If they do, the vocabulary earns its place.

### 9.5 Objection: This Is Just Retrieval, Memory, or Reflection

Another objection is that retrieval, memory, and reflection already address the problem.

They address part of it.

Retrieval can make information available. Memory can store prior material. Reflection can improve a future attempt. These are necessary capabilities in many agent systems. [Lewis et al., 2020; Park et al., 2023; Shinn et al., 2023; Madaan et al., 2023]

But availability is not the same as behavioral effectiveness. Storage is not the same as reusable reasoning. Reflection within a trajectory is not the same as organizational learning across cycles, agents, and contexts.

As Section 6 established, retrieval makes information available; reasoning-state architecture preserves the structure that makes information behaviorally effective.

A retrieved policy may not govern the claim being generated. A memory of prior failure may not connect to the new premise. A reflection note may improve one agent's next attempt without changing the workflow's future starting conditions.

Reasoning-state objects are meant to preserve the relationship among goal, policy, interpretation, premise, investigation, sufficiency, action, outcome, and update. If ordinary retrieval or memory modules can preserve that structure and make it behaviorally effective, then a separate implementation layer may not be necessary. The conceptual distinction could still remain valid while the implementation requirement becomes lighter.

The theory should not require new machinery where existing machinery already does the work.

### 9.6 Objection: Human Confirmation Does Not Solve Safety

Human confirmation can fail.

Humans miss things. They defer to fluent systems. They approve under time pressure. They may not know the relevant policy. They may confirm a frame because the system proposed it first. The propose step in Discovery can anchor the human toward the agent's interpretation, which makes anchoring a design constraint rather than a side issue.

Discovery cannot be treated as a magic legitimacy machine. A confirmation is evidence within scope. It is not proof that the interpretation is correct, safe, complete, or universally reusable. The system still needs uncertainty exposure, easy correction paths, provenance, bounded applicability, and escalation routes. For high-stakes or irreversible actions, it also needs hard controls outside the reasoning state: permissions, blocks, audits, sandboxing, and formal review. [Parasuraman and Riley, 1997; Lee and See, 2004; Amershi et al., 2019]

The purpose of Discovery is not to make human confirmation perfect. It is to prevent hidden inference from silently becoming durable state.

### 9.7 Objection: Reasoning-State Objects Can Be Manipulated

Reasoning-state architecture creates a new surface for attack and distortion.

If a system preserves reasoning objects, those objects can be poisoned, over-trusted, politicized, or misapplied. A bad Model Update Object can teach the wrong lesson. A stale confirmation can govern a new situation. A biased premise can be preserved with the authority of structure. A policy boundary can be represented in a way that narrows risk on paper while leaving action unchanged.

Gradients can also be intentionally shaped for the wrong reasons. A system can be designed so that organizationally convenient paths are more visible, more reachable, or more confidence-weighted than truthful ones. In that case, topography does not protect judgment. It becomes the mechanism by which judgment is steered.

Agentic systems already raise risks around memory poisoning, tool misuse, reward hacking, irreversible action chains, and failures across perception, cognition, memory, and action. [Su et al., 2025]

Reasoning-state objects can also create organizational risks.

They can become procedural theater: the system records a beautiful rationale after the real decision has already been made.

They can launder authority: a weak assumption looks stronger because it appears in a structured object.

They can harden politics: one team's interpretation becomes the default starting frame for another team.

They can preserve sensitive information beyond its proper use.

They can overgeneralize: one outcome becomes a rule for many situations that are only superficially similar.

These risks do not defeat the architecture. They bound it. Reasoning-state objects need provenance, confidence, scope, expiration, contestability, and audit. They should be treated as claims about prior reasoning, not as permanent truth.

### 9.8 Objection: The Framework May Add Too Much Overhead

A practical objection is that reasoning-state preservation may slow the work down.

That objection is serious. A system that asks too many questions, preserves too much state, or forces every task through a heavy governance loop will become unusable. Users will route around it. Teams will create shadow workflows. The architecture will fail by being correct at the wrong cost.

The answer is not to preserve everything. The answer is proportionality.

Low-stakes, reversible, exploratory tasks may need little or no durable reasoning state. Medium-stakes workflows may need lightweight Optimizer State, premise, and sufficiency capture. High-stakes workflows may require explicit evidence boundaries, scoped human confirmation, Investigation Trace, approval logic, and Model Update Objects.

The maturity model in the research agenda returns to this question: how much reasoning-state preservation is appropriate for which class of workflow?

A useful architecture must reduce the cost of good judgment. If it merely adds documentation burden, it has failed.

### 9.9 Disconfirmation Conditions

The framework should lose scope under clear conditions.

These are not a research design. They are falsifiability boundaries. [Popper, 1959; Lakatos, 1970; Hevner et al., 2004]

**1. If reasoning-state preservation does not improve reuse, governance, error recovery, or learning quality relative to context-only baselines.**
The comparison baseline matters. A fair test would compare workflows with similar model capability, similar artifact access, and similar task assignments, while varying whether reasoning state is preserved. Improvement should be evaluated through observable differences: fewer repeated errors, better transfer of lessons, more accurate escalation, clearer auditability, better recovery after contradiction, or higher-quality future starting states. If context-only workflows perform equally well on these measures, the architectural claim weakens.

**2. If the five dimensions do not produce different diagnoses or interventions.**
The five dimensions are useful only if they separate failures that would otherwise be collapsed. If changing the dimension never changes the repair, the vocabulary is too fine-grained or poorly chosen.

**3. If premature sufficiency cannot be identified before outcome failure.**
The concept must work as a design-time diagnostic. If it can only be applied after something goes wrong, it becomes a retrospective label rather than a useful design tool.

**4. If Discovery does not outperform plausible alternatives for forming confirmed reasoning state.**
Discovery should be compared against silent inference, blank-form intake, and workflows with no explicit infer-confirm loop. If Discovery adds friction, anchoring, or false confidence without improving the quality of Goal, Policy, Interpretation, evidence-boundary recognition, or human correction, then Discovery should lose importance.

**5. If Model Update Objects do not change future Optimizer States.**
A Model Update Object matters only if future reasoning begins differently. If updates are stored but do not shape future action, they are documentation, not learning.

**6. If ordinary agent memory and reflection modules already preserve the relevant structure across cycles, agents, and organizational contexts.**
This would not necessarily falsify the theory. It would weaken the need for a distinct implementation layer. The conceptual claim could remain valid while the practical architecture collapses into existing memory or reflection systems.

**7. If users systematically route around the architecture because the overhead exceeds the value.**
A framework for usable human-agent systems cannot treat adoption failure as external. If the architecture makes good work too slow, it has misunderstood the landscape it was supposed to design.

These are not cosmetic caveats. They are tests.

The framework becomes stronger if it survives them and narrower if it does not.

### 9.10 What Remains After the Objections

After the objections, the central claim is smaller but still useful.

Human-agent reliability is not only a model-quality problem, a retrieval problem, a UX problem, or a governance problem. It is also a landscape problem. Systems act from what their environments make visible, reachable, interpretable, trusted, connected, and sufficient.

That landscape can be shaped.

But shaping the landscape does not guarantee safe action. Preserving reasoning state does not guarantee learning. Human confirmation does not guarantee legitimacy. Model Update Objects do not guarantee truth.

The value is diagnostic discipline.

Instead of asking only whether the system failed, we can ask where the landscape failed:

- Did the relevant signal appear?
- Could the system reach it?
- Was it represented in a usable form?
- Was confidence calibrated?
- Was the signal connected to the decision?
- Did the system stop before the right counterpressure arrived?
- Did the reasoning state survive long enough to change the next cycle?

Those questions are useful because they can be wrong. They can be tested, challenged, instrumented, and improved.

A framework that cannot fail is not worth much.

A framework that can fail in clear ways can become a research program.

---

## 10. Research Agenda and Evaluation Methods

The next step is not to protect the framework.

It is to stress test it.

A conceptual framework earns value only when other people can use it, challenge it, narrow it, and show where it fails. The prior section named falsifiability boundaries. This section offers ways to put pressure on them.

The suggestions below are not a complete research design. They are invitations: places where researchers, designers, evaluators, and practitioners could test whether the account helps them see something they would otherwise miss.

The central question is simple:

**Do human-agent systems behave, recover, govern, or learn better when reasoning state is preserved, rather than when artifacts are only retrieved as context?**

That question can be tested in controlled studies, design-science prototypes, field deployments, trace analyses, red-team exercises, and comparative case studies. No single method will settle the framework. The useful work is cumulative: find where the vocabulary changes diagnosis, where it does not, and where the architecture costs more than it returns. [Hevner et al., 2004; Peffers et al., 2007; Lakatos, 1970]

This is a different evaluation target from most agent benchmarks. Benchmarks such as AgentBench, SWE-bench, and WebArena test whether agents can complete tasks in interactive or realistic environments. The agenda here asks a different question: whether the landscape that shaped the agent's motion was well designed, and whether the reasoning state that produced action can be inspected, challenged, and reused. [Liu et al., 2024; Jimenez et al., 2024; Zhou et al., 2024]

### 10.1 Compare Reasoning-State Workflows Against Context-Only Workflows

The most direct test is comparative.

Hold the task, model capability, and artifact access as constant as possible. Give one workflow retrieved context: documents, policies, prior work, examples, and memory. The baseline should be strong, not naive. Some agent systems already include memory, reflection, or structured feedback loops, and those capabilities should not be erased merely to make reasoning-state preservation look better. [Shinn et al., 2023; Yao et al., 2023] Give the other the same material, but require preservation of reasoning state: Goal, Policy, Interpretation, Premise Stack, Decision State, Investigation Trace, Learning Event, and Model Update Object.

Then ask what changes.

Does the reasoning-state workflow reduce repeated errors? Does it improve escalation when evidence is insufficient? Does it make review easier? Does it produce better next-cycle starting conditions? Does it help teams reuse prior lessons without overgeneralizing them?

The answer may be no.

That result would matter. It would suggest that in some domains, ordinary retrieval and memory are enough, or that the overhead of reasoning-state preservation is not worth the gain. The framework should narrow in response.

A healthcare marketing study could compare repeated campaign cycles. A software-operations study could compare incident-response workflows. A support-automation study could compare customer responses where policy boundaries and escalation conditions matter. In each case, the test should not be whether the reasoning-state workflow produces more documentation. The test should be whether future action begins from better conditions.

A second-domain test could use a software-repair task rather than a marketing claim. An agent is asked to resolve a GitHub issue. It finds a code pattern that looks like the fix, applies it, and the tests pass. A context-only workflow may preserve the merged patch, the issue thread, and the passing test result. A reasoning-state workflow should preserve something different: which premise made that patch look sufficient, what alternatives were considered, what investigation distinguished root cause from surface symptom, and why the passing tests were treated as enough. If the issue recurs, the organization should not have to rediscover the same uncertainty from the artifact alone. The prior reasoning state should show whether the fix addressed the real defect, merely satisfied the test surface, or solved one case while leaving the underlying pattern intact.

### 10.2 Perturb the Topography

The five dimensions should matter only if changing them changes behavior.

One way to test the framework is to perturb the landscape deliberately.

Make a policy visible or invisible. Make it easy or hard to reach. Represent it as dense prose, a decision table, or a claim-level constraint. Change how confidence, provenance, or source authority is shown. Connect or disconnect the policy from the exact action it should govern.

Then observe what happens.

If the five dimensions are useful, changing them should produce different failure patterns and different repairs. A visibility failure should not look the same as a confidence failure. A representation failure should not call for the same fix as a connectivity failure.

The strongest versions of these studies would make predictions before the task runs:

> If the evidence boundary is visible but not connected to claim generation, the system will retrieve the policy but still produce unsupported claim language.

Or:

> If prior incident memory is accessible but represented as generic history rather than an action boundary, the agent will mention the incident without changing the tool decision.

That kind of study helps prevent topography analysis from becoming retrospective storytelling.

### 10.3 Test Premature Sufficiency Before Outcome Failure

Premature sufficiency should be detectable before harm, not only after it.

For a given action class, designers can specify which information surfaces should become behaviorally effective before action. Required pre-action surfaces are the information surfaces a designer specifies must become behaviorally effective before a given action class can proceed, as described in Section 5's design-time account of premature sufficiency.

A clinical-outcome claim may require approved evidence, approved language, and compliance confirmation. A production restart may require dependency checks, severity assessment, rollback plan, and approval logic. A customer refund decision may require account status, policy boundary, exception rule, and escalation condition.

The test is straightforward:

**Did the system encounter and process the required surfaces before action became sufficient?**

If yes, the system may still be wrong, but the failure is not premature sufficiency in the design-time sense. If no, the system acted before the designed counterpressure arrived.

This evaluation does not require access to hidden chain-of-thought. It requires decision-relevant traces: which surfaces appeared, which constraints activated, which uncertainty was marked as material, what sufficiency rationale was preserved, and what action followed.

The goal is not to make systems hesitate forever. Good evaluation should distinguish premature sufficiency from over-delayed sufficiency. A system that investigates long after the decision is adequately supported is also poorly shaped. The aim is calibrated sufficiency: enough investigation before action, not endless investigation instead of action.

This maps onto the familiar tension between exploration and exploitation: systems must search enough to avoid premature closure, but not so much that exploration prevents useful action. [March, 1991]

### 10.4 Compare Discovery Against Its Alternatives

Discovery should not be assumed to help.

It should be compared against the failure modes it claims to avoid.

One baseline is **silent inference**: the agent fills gaps and proceeds without exposing the frame. Another is **blank-form intake**: the human must specify the frame before the agent can help. A third is **literal execution**: the system avoids richer inference and acts only on the explicit request.

Discovery should be better only if Retrieve → Infer → Propose → Confirm produces a more accurate and usable Optimizer State at acceptable cost.

Useful questions include:

- Did the human correct material assumptions before action?
- Did the process improve Goal, Policy, or Interpretation quality?
- Did it reduce later disputes about what the system was supposed to do?
- Did it preserve scope and provenance?
- Did the propose step anchor the human toward the system's first interpretation?
- Did users experience Discovery as helpful structure or bureaucratic drag?

This is also where human-AI interaction work matters. A Discovery process should support intelligibility, correction, appropriate trust, and user control. [Amershi et al., 2019; Lee and See, 2004] If it instead produces passive agreement, false confidence, or confirmation theater, it has failed.

### 10.5 Evaluate Whether Model Updates Actually Change Future Reasoning

A Model Update Object matters only if future reasoning begins differently.

That can be tested.

After an outcome contradicts an expectation, preserve an update. Then observe a later, related workflow. Did the next Optimizer State change? Did confidence shift? Did an evidence boundary become more visible? Did the system avoid repeating the same unsupported premise? Did it apply the lesson only where it belonged?

The second question is as important as the first:

**Did the update generalize correctly?**

A bad update can do harm. One campaign's weak conversion does not prove that workflow-burden messaging is useless. One unsafe restart does not prove that restart should never be used. One successful exception does not prove that the exception should become policy.

Model updates should therefore be evaluated for both transfer and restraint. They should change future reasoning, but not more than the evidence warrants. The difference between organizational learning and organizational overreaction lies precisely here. [Argyris and Schon, 1978; Walsh and Ungson, 1991]

The maturity model below parallels Argyris and Schon's learning distinctions without simply reproducing them. Level 3 resembles single-loop learning because the system can correct action within existing assumptions. Level 4 approaches double-loop learning because outcomes can change future governing assumptions. Level 5 adds a deutero-learning concern: the system must also preserve how learning itself is scoped, contested, audited, and improved. The difference is granularity and fit. This framework treats learning as reasoning-state change inside particular workflow classes, not as a general developmental ladder.

### 10.6 Use a Maturity Model as a Starting Instrument

Not every workflow needs the same level of reasoning-state preservation.

A maturity model can help researchers and practitioners ask how much structure is appropriate for a given workflow. The point is not to make every system climb to the highest level. The point is fit.

**Table 4. Maturity Model for Reasoning-State Preservation**

| Level | Name | What is preserved | Typical capability | Typical failure |
|---|---|---|---|---|
| **0** | Artifact-only | Final output or action result. | The system produces work but preserves little reasoning. | Repeated errors; no reusable why. |
| **1** | Context-aware | Retrieved sources, prompt context, or memory references. | The system can ground outputs in available artifacts. | Information exists but may not govern action. |
| **2** | Frame-aware | Goal, Policy, and Interpretation. | The system exposes the working frame before action. | Premises and sufficiency may remain implicit. |
| **3** | Decision-aware | Premise Stack, Decision State, and sufficiency rationale. | The system preserves why action, pause, escalation, or refusal was warranted. | Outcomes may not change future reasoning. |
| **4** | Learning-aware | Learning Event and Model Update Object. | The system converts contradiction into changed future expectations or boundaries. | Updates may overgeneralize or remain local. |
| **5** | Governed learning | Provenance, scope, confidence, contestability, expiration, and audit across cycles. | Reasoning state can be reused, challenged, narrowed, and governed. | Overhead, politics, or manipulation may distort the system. |

A low-risk drafting task may only need Level 1 or 2. A regulated healthcare campaign may need Level 3 or 4. A tool-using agent with irreversible production access may need Level 5 plus hard external controls.

The model should be treated as provisional. It is a way to ask better questions, not a standard to impose.

The useful research question is whether moving from one level to another improves outcomes enough to justify the cost. If Level 4 does not improve learning over Level 2 in a given domain, the heavier architecture should not be used there.

### 10.7 Look for Misuse, Not Only Improvement

The framework should also be tested adversarially.

Reasoning-state objects can be poisoned. Discovery can anchor users. Gradients can be shaped toward organizational convenience rather than truth. A Model Update Object can launder a weak assumption into durable memory. A confirmation can outlive its scope. A maturity model can become bureaucratic theater.

These are not external concerns. They are part of the research agenda.

Useful studies should ask:

- Can a bad premise be preserved with enough structure that it looks authoritative?
- Can a Discovery process steer humans toward the system's preferred frame?
- Can confidence markers make weak evidence feel stronger?
- Can a stale confirmation govern a new situation?
- Can teams use reasoning-state architecture to justify decisions already made?

If the answer is yes, the framework needs stronger governance conditions. Provenance, scope, expiration, contestability, and audit are not optional decorations. They are part of making reasoning-state preservation safe enough to use.

### 10.8 What Would Count as Progress

Progress would not require proving the whole framework correct.

Smaller results would matter.

If topography perturbations reliably produce different failure patterns, the dimensional vocabulary gains support.

If reasoning-state workflows reduce repeated errors across cycles, the architecture gains support.

If Discovery improves frame quality without unacceptable anchoring or burden, the infer-confirm loop gains support.

If Model Update Objects change future Optimizer States without overgeneralizing, the learning claim gains support.

If the maturity model helps teams choose lighter or heavier preservation strategies, the framework becomes more usable.

Negative results matter just as much.

If context-only workflows perform just as well, the architecture should narrow. If Discovery mostly adds friction, it should narrow. If the five dimensions do not change diagnosis, they should be revised. If reasoning-state objects become new sources of manipulation or bureaucracy, the governance account must become stronger.

The invitation is not to accept the framework.

The invitation is to put it under pressure.

A useful framework does not need to win everywhere. It needs to show where it helps, where it fails, and what must change when reality pushes back.

---

## 11. Conclusion: The Ground Beneath Action

The reliability problem has moved.

When systems only answered questions, the main concern was whether the answer was correct. That concern remains. But agentic systems now act inside workflows. They use tools, preserve memory, and leave traces that shape what future systems and teams will treat as known. The unit of concern is no longer only the output. It is the condition from which action became reasonable.

A model does not need inner malice to cause harm. It needs a goal, an action space, imperfect constraints, and a path through the environment that makes the wrong action appear useful, available, safe, or sufficient. When that happens, the failure is not mysterious. The system moved through a landscape that made one path easier than another.

Human-agent systems act from perceived landscapes, and those landscapes can be designed.

This is not a loose metaphor. The account developed here is grounded in hardened ideas: bounded decision-making and satisficing; affordances, interfaces, and information foraging; sensemaking, organizational memory, and learning; agent memory, reflection, retrieval, and safety. The synthesis matters because these traditions keep pointing to the same problem from different angles. Actors do not move through the world as it exists in full. They move through the world as it becomes available, meaningful, trusted, and actionable.

That is the space this framework names.

The pattern is easy to recognize once it has a name. A policy sits in the repository, but the claim never feels bound by it. The postmortem is searchable; the next incident still starts from the same old premise. A retrieved document appears in context and somehow never touches the sentence it should have stopped. In a campaign workflow, "reduces readmissions" feels close enough to adjacent truth that the evidence boundary arrives too late. A human confirms the visible frame while the real assumption remains hidden underneath it.

These are not isolated quirks. They are landscape failures.

The practical questions follow:

What can it see?

What can it reach?

What form does information take?

What does it trust?

What connects to the decision?

What makes action feel sufficient?

What survives into the next cycle?

That is why the framework has legs.

It does not explain everything. It should not try. Some failures are model failures. Some are institutional failures. Some are failures of power, incentive, expertise, or governance. But many human-agent failures become clearer when we stop looking only at the actor and begin looking at the ground on which action became reasonable.

The work ahead is to test that ground: perturb it, compare it, misuse it, narrow it, and improve it. The framework should become sharper where it helps and smaller where it does not.

But the direction is worth taking seriously. If unsafe, unsupported, or shallow action lies downhill, systems will keep finding that path. If evidence, policy, uncertainty, and human judgment become behaviorally effective before action, better paths become easier to reach.

Reliability is not only a matter of controlling the actor.

It is a matter of designing the ground beneath the action.

---

## References

Alavi, M., & Leidner, D. E. (2001). Review: Knowledge management and knowledge management systems: Conceptual foundations and research issues. *MIS Quarterly*, *25*(1), 107-136.

Amershi, S., Weld, D., Vorvoreanu, M., Fourney, A., Nushi, B., Collisson, P., Suh, J., Iqbal, S., Bennett, P. N., Inkpen, K., Teevan, J., Kikin-Gil, R., & Horvitz, E. (2019). Guidelines for human-AI interaction. *CHI '19: Proceedings of the 2019 CHI Conference on Human Factors in Computing Systems*, Paper 3.

Argyris, C., & Schon, D. A. (1978). *Organizational learning: A theory of action perspective*. Addison-Wesley.

Bai, Y., Kadavath, S., Kundu, S., Askell, A., Kernion, J., Jones, A., Chen, A., Goldie, A., Mirhoseini, A., McKinnon, C., Chen, C., Olsson, C., Olah, C., Hernandez, D., Drain, D., Ganguli, D., Li, D., Tran-Johnson, E., Perez, E., ... Kaplan, J. (2022). Constitutional AI: Harmlessness from AI feedback. *arXiv:2212.08073*.

Christiano, P. F., Leike, J., Brown, T., Martic, M., Legg, S., & Amodei, D. (2017). Deep reinforcement learning from human preferences. *Advances in Neural Information Processing Systems*, *30*.

Endsley, M. R. (1995). Toward a theory of situation awareness in dynamic systems. *Human Factors*, *37*(1), 32-64.

Gibson, J. J. (1979). *The ecological approach to visual perception*. Houghton Mifflin.

Hevner, A. R., March, S. T., Park, J., & Ram, S. (2004). Design science in information systems research. *MIS Quarterly*, *28*(1), 75-105.

Horvitz, E. (1999). Principles of mixed-initiative user interfaces. *CHI '99: Proceedings of the SIGCHI Conference on Human Factors in Computing Systems*, 159-166.

Huang, L., Yu, W., Ma, W., Zhong, W., Feng, Z., Wang, H., Chen, Q., Peng, W., Feng, X., Qin, B., & Liu, T. (2023). A survey on hallucination in large language models: Principles, taxonomy, challenges, and open questions. *arXiv:2311.05232*.

Ji, J., Qiu, T., Chen, B., Zhang, B., Lou, H., Wang, K., Duan, Y., He, Z., Zhou, J., Zhang, Z., Zeng, F., Ng, K. Y., Dai, J., Pan, X., O'Gara, A., Lei, Y., Xu, H., Tse, B., Fu, J., ... Gao, W. (2023). AI alignment: A comprehensive survey. *arXiv:2310.19852*.

Jimenez, C. E., Yang, J., Wettig, A., Yao, S., Pei, K., Press, O., & Narasimhan, K. (2024). SWE-bench: Can language models resolve real-world GitHub issues? *International Conference on Learning Representations*.

Kuhlthau, C. C. (1991). Inside the search process: Information seeking from the user's perspective. *Journal of the American Society for Information Science*, *42*(5), 361-371.

Lakatos, I. (1970). Falsification and the methodology of scientific research programmes. In I. Lakatos & A. Musgrave (Eds.), *Criticism and the growth of knowledge* (pp. 91-196). Cambridge University Press.

Lee, J. (1997). Design rationale systems: Understanding the issues. *IEEE Expert*, *12*(3), 78-85.

Lee, J. D., & See, K. A. (2004). Trust in automation: Designing for appropriate reliance. *Human Factors*, *46*(1), 50-80.

Lewis, P., Perez, E., Piktus, A., Petroni, F., Karpukhin, V., Goyal, N., Kuttler, H., Lewis, M., Yih, W., Rocktaschel, T., Riedel, S., & Kiela, D. (2020). Retrieval-augmented generation for knowledge-intensive NLP tasks. *Advances in Neural Information Processing Systems*, *33*, 9459-9474.

Liu, X., Yu, H., Zhang, H., Xu, Y., Lei, X., Lai, H., Gu, Y., Ding, H., Men, K., Yang, K., Zhang, S., Deng, X., Zeng, A., Du, Z., Zhang, C., Shen, S., Zhang, T., Su, Y., Sun, H., ... Tang, J. (2024). AgentBench: Evaluating LLMs as agents. *International Conference on Learning Representations*.

Lynch, A., Wright, B., Larson, C., Troy, K. K., Ritchie, S. J., Mindermann, S., Perez, E., & Hubinger, E. (2025). Agentic misalignment: How LLMs could be an insider threat. Anthropic Research.

Madaan, A., Tandon, N., Gupta, P., Hallinan, S., Gao, L., Wiegreffe, S., Alon, U., Dziri, N., Prabhumoye, S., Yang, Y., Gupta, S., Majumder, B. P., Hermann, K. M., Welleck, S., Yazdanbakhsh, A., & Clark, P. (2023). Self-Refine: Iterative refinement with self-feedback. *Advances in Neural Information Processing Systems*, *36*.

March, J. G. (1991). Exploration and exploitation in organizational learning. *Organization Science*, *2*(1), 71-87.

Markus, M. L. (2001). Toward a theory of knowledge reuse: Types of knowledge reuse situations and factors in reuse success. *Journal of Management Information Systems*, *18*(1), 57-93.

Maynez, J., Narayan, S., Bohnet, B., & McDonald, R. (2020). On faithfulness and factuality in abstractive summarization. *Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics*, 1906-1919.

Norman, D. A. (1988). *The design of everyday things*. Basic Books.

Ouyang, L., Wu, J., Jiang, X., Almeida, D., Wainwright, C., Mishkin, P., Zhang, C., Agarwal, S., Slama, K., Ray, A., Schulman, J., Hilton, J., Kelton, F., Miller, L., Simens, M., Askell, A., Welinder, P., Christiano, P. F., Leike, J., & Lowe, R. (2022). Training language models to follow instructions with human feedback. *Advances in Neural Information Processing Systems*, *35*.

Parasuraman, R., & Riley, V. (1997). Humans and automation: Use, misuse, disuse, abuse. *Human Factors*, *39*(2), 230-253.

Park, J. S., O'Brien, J. C., Cai, C. J., Morris, M. R., Liang, P., & Bernstein, M. S. (2023). Generative agents: Interactive simulacra of human behavior. *Proceedings of the 36th Annual ACM Symposium on User Interface Software and Technology*.

Peffers, K., Tuunanen, T., Rothenberger, M. A., & Chatterjee, S. (2007). A design science research methodology for information systems research. *Journal of Management Information Systems*, *24*(3), 45-77.

Pirolli, P., & Card, S. (1999). Information foraging. *Psychological Review*, *106*(4), 643-675.

Popper, K. R. (1959). *The logic of scientific discovery*. Hutchinson.

Schick, T., Dwivedi-Yu, J., Dessi, R., Raileanu, R., Lomeli, M., Hambro, E., Zettlemoyer, L., Cancedda, N., & Scialom, T. (2023). Toolformer: Language models can teach themselves to use tools. *Advances in Neural Information Processing Systems*, *36*.

Shinn, N., Cassano, F., Gopinath, A., Narasimhan, K., & Yao, S. (2023). Reflexion: Language agents with verbal reinforcement learning. *Advances in Neural Information Processing Systems*, *36*.

Siggelkow, N. (2007). Persuasion with case studies. *Academy of Management Journal*, *50*(1), 20-24.

Simon, H. A. (1955). A behavioral model of rational choice. *Quarterly Journal of Economics*, *69*(1), 99-118.

Su, H., Luo, J., Liu, C., Yang, X., Zhang, Y., Dong, Y., & Zhu, J. (2025). A survey on autonomy-induced security risks in large model-based agents. *arXiv:2506.23844*.

Walsh, J. P., & Ungson, G. R. (1991). Organizational memory. *Academy of Management Review*, *16*(1), 57-91.

Weick, K. E. (1995). *Sensemaking in organizations*. Sage.

Wilson, T. D. (1999). Models in information behaviour research. *Journal of Documentation*, *55*(3), 249-270.

Wu, Q., Bansal, G., Zhang, J., Wu, Y., Li, B., Zhu, E., Jiang, L., Zhang, X., Zhang, S., Liu, J., Awadallah, A. H., White, R. W., Burger, D., & Wang, C. (2023). AutoGen: Enabling next-gen LLM applications via multi-agent conversation. *arXiv:2308.08155*.

Xie, T., Zhang, D., Chen, J., Li, X., Zhao, S., Cao, R., Hua, T. J., Cheng, Z., Shin, D., Lei, F., Liu, Y., Xu, Y., Zhou, S., Savarese, S., Xiong, C., Zhong, V., & Yu, T. (2024). OSWorld: Benchmarking multimodal agents for open-ended tasks in real computer environments. *Advances in Neural Information Processing Systems*, *37*.

Xu, F. F., Shi, Y., Hooi, D. S., Muennighoff, N., Shen, J. T., Xin, Z., ... & Neubig, G. (2024). TheAgentCompany: Benchmarking LLM agents on consequential real world tasks. *arXiv:2412.14161*.

Yao, S., Zhao, J., Yu, D., Du, N., Shafran, I., Narasimhan, K., & Cao, Y. (2023). ReAct: Synergizing reasoning and acting in language models. *International Conference on Learning Representations*.

Zhou, S., Xu, F. F., Zhu, H., Zhou, X., Lo, R., Sridhar, A., Cheng, X., Ou, T., Bisk, Y., Fried, D., Alon, U., & Neubig, G. (2024). WebArena: A realistic web environment for building autonomous agents. *International Conference on Learning Representations*.
