# 2. A Note on Terms

## How to Read the Terminology

This paper uses several terms that carry established meanings in other fields, including optimization, reinforcement learning, topology, human-computer interaction, organizational learning, knowledge management, systems theory, and AI safety. The terms are used here in a specific analytic sense. They are intended to create a shared vocabulary for describing human-agent systems, not to imply a fully mathematical model unless explicitly stated.

This clarification matters because many of the paper's central terms are overloaded. A reader may reasonably bring definitions from reinforcement learning, economics, organizational theory, HCI, or AI alignment. Those definitions are often relevant, and many are part of the intellectual lineage of this framework. But the framework uses these terms as a synthesis. It borrows, narrows, and recombines them around a specific problem: how human-agent systems perceive, decide, act, and learn across organizational workflows.

The reader does not need to memorize the full vocabulary before continuing. The terms below are the core orientation points needed for the next parts of the argument. Other concepts are introduced where they become active in the paper.

## Core Terms Needed Before Continuing

**Optimizer.** An optimizer is a system that selects actions in relation to a goal, under constraints, using an interpretation of the situation.

The term does not imply consciousness, desire, moral agency, or malice. An optimizer need not "want" in the human sense. It need only exhibit goal-directed action selection. In this paper, optimizer is a behavioral description, not a psychological claim.

This usage is influenced by bounded rationality and satisficing: real decision-makers do not evaluate all possible actions under perfect information, but search, interpret, and stop when a course of action appears sufficient. [Simon, 1955]

**Agent.** An agent is an AI system or workflow component that can interpret information, select actions, use tools, and produce effects beyond a single static response.

Agents vary in autonomy. Some require constant human direction. Others can plan, retrieve information, invoke tools, write messages, update systems, or operate across longer time horizons. The framework treats agency as a design condition shaped by goal, permissions, tool access, oversight, and environment.

**Reasoning state.** A reasoning state is the structured condition from which an optimizer acts.

It includes the active goal, relevant policies, current interpretation, premise stack, visible information, confidence levels, decision options, constraints, and sufficiency rationale. A central claim of the paper is that human-agent systems often fail because they preserve documents and outputs, but not the reasoning states that produced them.

**Topography.** Topography refers to the perceived information-and-action environment through which an optimizer moves.

It is not the objective world itself. It is the world as made available to the optimizer through visible information, accessible tools, representations, confidence signals, policies, memories, prior learning, and action affordances. The term is metaphorical unless explicitly formalized. It is used to describe the shape of perceived possibilities.

**Gradient.** A gradient is a directional pressure within the perceived topography.

A gradient makes some paths appear easier, more useful, more relevant, more confident, lower-cost, or more sufficient than others. In this paper, gradient does not necessarily mean a mathematical gradient or a reinforcement-learning reward function. It is a broader design term for how goals, information, confidence, constraints, tool access, action costs, and prior learning shape movement.

The framework's use of gradient is related to reward shaping and environment design, but it is not identical to formal reward shaping. [Ng et al., 1999]

## Terms Used With Specific Meaning

Several other terms appear throughout the paper with narrower or more precise meanings than their common usage. They are named here to prevent confusion, but they are developed more fully in the sections where they do the most work.

**Goal** means the directional objective an optimizer acts in relation to, not merely the literal task prompt. Goals shape which information becomes relevant. Section 4 develops this term.

**Policy** means a constraint on optimizer behavior: what the system may do, must do, must not do, or must escalate. A policy is treated as a boundary condition, not merely as a written rule. Section 4 develops this distinction.

**Interpretation** means the optimizer's working understanding of what information means, including signal meaning, causal assumptions, and action models. Section 4 develops this term.

**Perceived topography** emphasizes that the optimizer acts on what it can perceive, retrieve, interpret, and trust, not on objective reality as such. Section 5 develops this distinction.

**Information surface** means any source, interface, artifact, memory, system, or signal through which information becomes available to the optimizer. Section 5 develops this term.

**Confidence** means how trustworthy, grounded, or reliable a perceived information surface appears to the optimizer. It is not the same as truth. Capitalized Confidence refers to the topography dimension introduced in Section 5; lowercase confidence refers to the general degree of belief or reliability assigned in ordinary reasoning contexts.

**Sufficiency** means the point at which additional information is unlikely to materially change the selected action. It is not the same as certainty. Section 6 develops this concept as part of optimizer motion.

**Learning** means an evidence-supported model update triggered by prediction error. A bad outcome alone is not learning, and a postmortem alone is not necessarily learning. Sections 8 and 9 develop this claim.

**Hallucination** means the production of plausible but unsupported claims. In this framework, hallucination is not only an output defect; it is also a reasoning-state failure in which the system reaches sufficiency before evidence warrants the claim. Section 7 develops this argument.

**Alignment** is used cautiously. The framework does not treat alignment only as value matching between a model and a human. It treats alignment as a property of the broader human-agent system: goals, policies, interpretations, information surfaces, action affordances, confidence structures, oversight, and learning loops must work together so that behavior reliably moves toward intended outcomes. Section 16 returns to this point.

**Governance** means the mechanisms by which goals, policies, permissions, evidence requirements, approval paths, monitoring, and learning updates are made durable and behaviorally effective. Governance is not merely having rules. It succeeds when rules can shape behavior at the moment of decision. Section 16 develops this implication.

## Terms Introduced Later

Some terms are intentionally not fully defined here because they make more sense once the argument has created a need for them. The five dimensions of information topography — Visibility, Accessibility, Representation, Confidence, and Connectivity — are introduced in Section 5. The stages of optimizer motion — Attraction, Investigation, Sufficiency, and Action — are introduced in Section 6. Prediction Error appears in Section 8 as the trigger condition for learning. Premise Stack and Model Update Object appear in Section 9 as part of the paper's account of durable learning. Discovery appears in Section 11 as the process by which messy human intent and organizational artifacts are converted into structured reasoning state.

This sequencing is intentional. The framework is not a vocabulary list. It is an argument about how agent behavior emerges from the relationship between goals, constraints, interpretation, perceived information, available action, and preserved learning.

In summary, this paper uses topography to describe the environment of perceived possibilities; gradients to describe directional pressures within that environment; and optimizer to describe the system moving through it.

The central claim is that safer and more reliable human-agent systems require not only stronger constraints, but better-shaped perceived topographies.
