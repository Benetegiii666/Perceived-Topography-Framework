# Proposed Replacement for Section 2

---

# 2. A Note on Terms

This paper uses several terms that carry established meanings in other fields, including optimization, reinforcement learning, topology, human-computer interaction, organizational learning, knowledge management, systems theory, and AI safety. The terms are used here in a specific analytic sense. They are intended to provide a shared vocabulary for describing human-agent systems, not to imply a fully mathematical model unless explicitly stated.

This section defines the core terms needed to follow the argument. Additional terms — including the five topography dimensions, the four stages of optimizer motion, and the reasoning architecture objects — are introduced in the sections where they are developed.

## Core Terms

**Optimizer.** A system that selects actions in relation to a goal, under constraints, using an interpretation of the situation. The term does not imply consciousness, desire, moral agency, or malice. An optimizer need not "want" in the human sense. It need only exhibit goal-directed action selection. In this paper, optimizer is a behavioral description, not a psychological claim. This usage is influenced by bounded rationality and satisficing: real decision-makers do not evaluate all possible actions under perfect information, but search, interpret, and stop when a course of action appears sufficient. [Simon, 1955]

**Agent.** An AI system or workflow component that can interpret information, select actions, use tools, and produce effects beyond a single static response. Agents vary in autonomy. The framework treats agency as a design condition shaped by goal, permissions, tool access, oversight, and environment.

**Topography.** The perceived information-and-action environment through which an optimizer moves. It is not the objective world itself. It is the world as made available to the optimizer through visible information, accessible tools, representations, confidence signals, policies, memories, prior learning, and action affordances. The term is metaphorical unless explicitly formalized. It is used to describe the shape of perceived possibilities.

**Gradient.** A directional pressure within the perceived topography. A gradient makes some paths appear easier, more useful, more relevant, more confident, lower-cost, or more sufficient than others. In this paper, gradient does not necessarily mean a mathematical gradient or a reinforcement-learning reward function. It is a broader design term for how goals, information, confidence, constraints, tool access, action costs, and prior learning shape movement. The framework's use of gradient is related to reward shaping and environment design, but it is not identical to formal reward shaping. [Ng et al., 1999]

**Reasoning state.** The structured condition from which an optimizer acts. It includes the active goal, relevant policies, current interpretation, premise stack, visible information, confidence levels, decision options, constraints, and sufficiency rationale. A central claim of the paper is that human-agent systems often fail because they preserve documents and outputs, but not the reasoning states that produced them.

## Terms Used With Specific Meaning

The following terms appear throughout the paper with narrower or more precise meanings than their common usage. Full definitions and development appear in the sections indicated.

**Goal** — the directional objective the optimizer acts in relation to. Not merely a task label; it determines which information becomes relevant. *(Developed in Section 4.)*

**Policy** — a constraint on optimizer behavior: what the system may do, must do, must not do, or must escalate. Treated as a boundary condition, not merely as a written rule. A policy that is not visible, salient, or connected to action may fail to shape behavior. *(Developed in Section 4.)*

**Interpretation** — the optimizer's working understanding of what information means. Includes signal meaning, causal assumptions, and action models. *(Developed in Section 4.)*

**Perceived topography** — emphasizes that the optimizer acts on what it can perceive, retrieve, interpret, and trust, not on objective reality. Information that exists but is invisible, inaccessible, or disconnected may exert little or no force on behavior. *(Developed in Section 5.)*

**Information surface** — any source, interface, artifact, memory, system, or signal through which information becomes available to the optimizer. *(Developed in Section 5.)*

**Confidence** — how trustworthy, grounded, or reliable a perceived information surface appears to the optimizer. Not the same as truth. A behavioral variable that affects whether the optimizer acts, investigates, escalates, or abstains. Capitalized Confidence refers to the topography dimension; lowercase confidence refers to general degree of belief. *(Developed in Section 5.)*

**Sufficiency** — the point at which additional information is unlikely to materially change the selected action. Not the same as certainty. *(Developed in Section 6.)*

**Learning** — an evidence-supported model update triggered by prediction error. A bad outcome alone is not learning. A postmortem alone is not learning. Learning occurs when an expectation is violated, the mismatch is investigated, an evidence-supported explanation is formed, and future behavior is updated. *(Developed in Section 8.)*

**Alignment** — used cautiously. The framework treats alignment as a property of the broader human-agent system, not only as value matching between a model and a human. *(Discussed in Section 16.)*

**Governance** — the mechanisms by which goals, policies, permissions, evidence requirements, approval paths, monitoring, and learning updates are made durable and behaviorally effective. Governance succeeds when the rules are visible, accessible, and capable of shaping behavior at the moment of decision. *(Discussed in Section 16.)*

**Hallucination** — the production of plausible but unsupported claims. In this framework, hallucination is not only an output defect. It is also a reasoning-state failure: the system reaches sufficiency before evidence warrants the claim. *(Developed in Section 7.)*

## Terms Introduced Later

The following terms are introduced and defined in the sections where they are first needed. They are listed here for reference only.

| Term | Introduced In | Brief |
|------|--------------|-------|
| Visibility, Accessibility, Representation, Confidence, Connectivity | Section 5 | The five dimensions of Information Topography |
| Attraction, Investigation, Sufficiency, Action | Section 6 | The four stages of optimizer motion |
| Prediction Error | Section 8 | Mismatch between expected and observed outcome |
| Premise Stack | Section 9 | The artifact-backed basis for a prior expectation |
| Model Update Object | Section 9 | A reusable record of learning |
| Discovery | Section 11 | The process of converting messy intent into structured reasoning state |

## Summary of Usage

This paper uses *topography* to describe the environment of perceived possibilities; *gradients* to describe directional pressures within that environment; and *optimizer* to describe the system moving through it.

The central claim is that safer and more reliable human-agent systems require not only stronger constraints, but better-shaped perceived topographies.

---

# Relocation Ledger

| Term | Section 2 treatment | Later full home | Notes |
|------|-------------------|----------------|-------|
| Optimizer | Full definition (kept) | S4.1 further development | Core term — must be in S2 |
| Agent | Full definition (kept) | S4 context | Core term |
| Topography | Full definition (kept) | S5 full treatment | Core term — paper title |
| Gradient | Full definition (kept) | S6.1 full treatment | Core term — needs RL caveat |
| Reasoning State | Full definition (kept) | S3, S10 | Core term — S3 title depends on it |
| Goal | One-sentence guardrail | S4.1 | Full development with examples, safety, goal relevance |
| Policy | One-sentence guardrail | S4.2 | Full development with force/salience discussion |
| Interpretation | One-sentence guardrail | S4.3 | Full development with subtypes (Signal, Causal, Action Model) |
| Perceived Topography | One-sentence guardrail | S5 | Emphasis on perception vs reality |
| Information Surface | One-sentence guardrail | S5 | Examples (dashboards, CRM, etc.) moved to S5 |
| Confidence | One-sentence guardrail + capitalization note | S5.5 | Full dimension treatment + hallucination connection in S5.5 |
| Sufficiency | One-sentence guardrail | S6.5 | Simon connection, Confidence/Sufficiency distinction in S6.5 |
| Learning | One-sentence guardrail | S8 | Argyris/Schön connection, reaction vs learning in S8 |
| Alignment | One-sentence guardrail | S16.2 | System-level alignment discussion |
| Governance | One-sentence guardrail | S16.5 | Rules-must-exert-force discussion |
| Hallucination | One-sentence guardrail | S7.1 | Premature sufficiency framing |
| Visibility | Listed in "Later" table | S5.2 | Dimension definition + failure examples |
| Accessibility | Listed in "Later" table | S5.3 | Dimension definition + failure examples |
| Representation | Listed in "Later" table | S5.4 | Dimension definition + failure examples |
| Connectivity | Listed in "Later" table | S5.6 | Dimension definition + failure examples |
| Attraction | Listed in "Later" table | S6.2 | Motion stage — two attraction modes |
| Investigation | Listed in "Later" table | S6.3 | Motion stage — bounded search |
| Action | Listed in "Later" table | S6.6 | Motion stage — output of reasoning |
| Prediction Error | Listed in "Later" table | S8.4 | Learning trigger |
| Premise Stack | Listed in "Later" table | S9.3 | MUO field — why we expected this to work |
| Model Update Object | Listed in "Later" table | S9.1 | Reusable learning record |
| Discovery | Listed in "Later" table | S11.1 | Messy intent → reasoning state |

---

## Estimated Word Counts

| Component | Current S2 | Proposed S2 |
|-----------|-----------|------------|
| Intro paragraphs | ~130 | ~100 |
| Core Terms (5 full definitions) | ~385 | ~385 |
| Terms With Specific Meaning (11 guardrails) | ~815 | ~280 |
| Terms Introduced Later (table) | 0 | ~80 |
| Summary of Usage | ~60 | ~60 |
| **Total** | **~2,100** | **~905** |

**Net reduction: ~1,200 words (~57%)**

All removed content is preserved in later sections. No conceptual material is deleted from the manuscript.
