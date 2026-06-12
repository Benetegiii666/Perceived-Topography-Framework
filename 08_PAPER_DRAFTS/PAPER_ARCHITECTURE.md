# Paper Architecture

## Working Title

**The Perceived Topography Framework: A Reasoning-State Architecture for Human-Agent Systems**

## Working Subtitle

**From containment to topography in the design of safer, more adaptive AI agents**

---

## Core Narrative Position

The paper opens from the original motivating question — why do people fear agents? — but uses a refined academic frame:

> AI agents are not best understood as moral actors. They are better understood as optimizer-like systems moving through perceived information and action landscapes.

**Core claim:**

> Many agent failures are misdescribed when interpreted primarily as signs of emergent malice. The more precise unit of analysis is an optimizer operating within a designed topography.

**Safety reframe:**

> The question is not only how to contain agents. The question is how to shape the perceived topography so that grounded, policy-aware, human-beneficial behavior becomes the easiest sufficient path.

The paper does not deny frontier AI risk. It reframes the safety problem.

---

## Opening Argument

Observed pattern:

```
Model placed in constrained environment
→ given goals, tools, access, autonomy
→ placed under pressure
→ behaves in ways that appear deceptive, evasive, aggressive, or self-protective
→ interpreted as evidence of dangerous agency
→ response: stronger containment
```

The paper's counterframe:

> The observed risk is real, but the interpretation is often too anthropomorphic and too containment-centered.

Preferred framing:

> An optimizer was given a goal, tools, partial constraints, and a poorly shaped landscape. It moved along the gradients available to it. The design question is not merely why it crossed the fence. The design question is why the landscape made crossing the fence appear useful, available, or sufficient.

---

## Citation Anchors

| ID | Source | Purpose |
|----|--------|---------|
| [S1] | Anthropic — Agentic Misalignment | Establish that risky agentic behavior observed in controlled simulations |
| [S2] | OpenAI — Preparedness Framework | Establish formal tracking of severe autonomy risks |
| [S3] | Google DeepMind — Frontier Safety Framework | Establish autonomy as core risk domain |
| [S4] | DeepMind — Role-play / Anthropomorphism | Support careful language for model behavior |
| [S5] | DeepMind — GopherCite | Connect hallucination to evidence grounding |

---

## Paper Thesis

**Draft thesis:**

> Modern AI systems do not fail only because they lack information. They fail because they lack structured access to the reasoning state that gives information meaning: goals, constraints, premises, confidence, decisions, outcomes, and learning. The Perceived Topography Framework proposes a way to represent and preserve these reasoning states so human-agent systems can act, adapt, and learn across organizational workflows.

**Sharper safety-oriented thesis:**

> Agent safety should not be framed only as containment. Because agent behavior emerges from the interaction between optimizer state and perceived topography, safer systems require environments where evidence, confidence, policy, action cost, and learning are structured so that desired behavior becomes the most available sufficient path.

---

## Argument Arc

### 1. Introduction: The Fear Frame and the Missing Layer
From "agents may become evil" to "optimizer-like systems move through poorly shaped topographies." Containment matters, but containment is not the whole design space.

### 2. A Note on Terms
Define overloaded framework language before the reader imports wrong assumptions. (Full draft below.)

### 3. The Problem: Context Is Not Reasoning State
Knowledge retrieval alone does not preserve why information matters, what goal it served, what premise it supported, what decision it shaped, or what later outcome contradicted it.

### 4. Optimizers: Goal, Policy, Interpretation
Define the optimizer as the basic unit of behavior. The optimizer is not morally good or evil — it moves according to goal, constraint, interpretation, and perceived topography.

### 5. Information Topography: What the Optimizer Navigates
Five dimensions: Visibility, Accessibility, Representation, Confidence, Connectivity. Information that exists but is invisible, inaccessible, poorly represented, low-confidence, or disconnected may fail to shape behavior.

### 6. Gradients and Motion
Attraction → Investigation → Sufficiency → Action. An agent does not simply obey a rule or pursue a goal in isolation. It moves through a perceived landscape.

### 7. Hallucination and Harmful Action as Related Failures
Both involve movement from insufficiently grounded perception to premature sufficiency. Hallucination: unsupported completion easier than evidence-backed uncertainty. Unsafe action: harmful path appears useful, available, and sufficient.

### 8. Learning: Prediction Error and Model Update
Expectation → Action → Outcome → Prediction Error → Investigation → Evidence-Supported Explanation → Model Update. Bad outcome is not learning. Reaction is not learning.

### 9. Model Update Objects: Preserving Learning
If learning is not preserved as an object, the organization reverts to folklore, memory, or repeated rediscovery.

### 10. Reasoning Architecture: Preserving State Transitions
Six objects. The unit of organizational reasoning is not the document — it is the optimizer state transition.

### 11. Discovery Framework: From Human Intent to Reasoning State
Retrieve → Infer → Propose → Confirm → Generate → Preserve → Learn. Discovery is not a questionnaire.

### 12. Running Example: Adaptive Campaign Reasoning Studio
Healthcare campaign simulation from "I want to do a healthcare campaign" through full reasoning-state capture, campaign generation, outcome tracking, and learning.

### 13. Implementation Bridge
Show the framework can become a system, not just a metaphor.

### 14. Validation and Falsifiability
Potential validation questions and falsification points.

### 15. Related Work Placeholder
Not written until proper literature pass.

### 16. Implications
Agent safety, organizational AI, human-agent collaboration, governance, learning, product design.

### 17. Conclusion
Return to opening: "If agents are optimizer-like systems, then the question is not whether they are evil. The question is what world we have built for them to perceive, move through, and learn from."

---

## A Note on Terms — Full Draft

This paper uses several terms that carry meanings in other fields, including optimization, topology, reinforcement learning, human-computer interaction, organizational learning, and systems theory. The terms are used here in a specific analytic sense. They are intended to provide a shared vocabulary for describing human-agent systems, not to imply a fully mathematical model unless explicitly stated.

**Optimizer** refers to a system that selects actions in relation to a goal, under constraints, using an interpretation of the situation. An optimizer does not need to possess human intention, consciousness, desire, or malice. In this paper, the term describes goal-directed behavior, not moral agency.

**Agent** refers to an AI system or workflow component that can interpret information, select actions, use tools, and produce effects beyond a single static response. An agent may be more or less autonomous depending on its permissions, tools, oversight, and time horizon.

**Topography** refers to the perceived information-and-action environment through which an optimizer moves. It is not the objective world itself. It is the world as made available to the optimizer through visible information, accessible tools, representations, confidence signals, policies, memories, and affordances.

**Perceived Topography** emphasizes that the optimizer acts on what it can perceive, retrieve, interpret, and trust. Information that exists but is invisible, inaccessible, poorly represented, low-confidence, or disconnected may exert little or no force on behavior.

**Gradient** refers to a directional pressure within that perceived topography. A gradient makes some paths appear easier, more useful, more confident, more relevant, lower-cost, or more sufficient than others. A gradient is not necessarily a reward function in the formal reinforcement-learning sense. It is a way of describing how goals, information, confidence, constraints, tool access, and action costs shape movement.

**Policy** refers to constraints on optimizer behavior: what the system may do, must do, must not do, or must escalate. Policy is treated as a boundary condition on behavior, not merely as a written rule. A policy that is not visible, salient, enforceable, or connected to action may fail to shape the optimizer's path.

**Interpretation** refers to the optimizer's working understanding of what information means. This includes signal meaning, causal assumptions, and action models: beliefs about which actions are likely to produce which outcomes under which conditions.

**Premise Stack** refers to the artifact-backed basis for a prior expectation. It includes the assumptions, source materials, playbooks, strategies, data, policies, or prior decisions that made an action seem reasonable before it was taken.

**Sufficiency** refers to the point at which additional information is unlikely to materially change the selected action. It is not the same as certainty. A system may have low confidence in the full explanation but still reach sufficiency if the same action remains appropriate across plausible explanations.

**Learning** refers to an evidence-supported model update triggered by prediction error. A bad outcome alone is not learning. A postmortem alone is not learning. Learning occurs when an expectation is violated, the mismatch is investigated, an evidence-supported explanation is formed, and the system updates future behavior.

**Model Update Object** refers to a reusable record of learning. It preserves the prior expectation, the premise stack, the observed outcome, the prediction error, the evidence-supported explanation, the update target, the applicability boundary, and the confidence level.

**Discovery** refers to the process by which messy human intent and organizational artifacts are converted into structured reasoning objects. Discovery is not simply asking questions. In mature systems, discovery retrieves existing context, infers likely reasoning state, proposes a strawman, confirms only material uncertainties, generates useful artifacts, preserves the decision state, and learns from outcomes.

In short, this paper uses topography to describe the environment of perceived possibilities, gradients to describe directional pressures within that environment, and optimizer to describe the system moving through it. The central claim is that safer and more reliable human-agent systems require not only stronger constraints, but better-shaped perceived topographies.

---

## Required SVGs

### SVG 1 — Fear Framing vs Topography Framing
Two-column: conventional fear framing (model + disturbing behavior → containment) vs topography framing (optimizer + landscape → redesign gradients).

### SVG 2 — Box-First Safety vs Topography-First Safety
Panel A: agent inside sandbox/fences. Panel B: agent moving through shaped landscape toward evidence-backed, policy-compliant outcome.

### SVG 3 — Core Framework Loop
Seven-document architecture as cycle: Optimizer State → Topography → Motion → Action → Outcome → Prediction Error → Learning → Model Update → Discovery → Updated Optimizer State.

### SVG 4 — Runtime Discovery Loop
Messy human intent → Retrieve → Infer → Propose → Confirm → Generate → Preserve → Learn, with side output of reasoning objects.

---

## Draft 1 Definition of Done

1. Opening frame grounded in agent fear / optimizer reframing
2. A Note on Terms section
3. Explanation of seven-part architecture
4. Running healthcare campaign example
5. Safety argument: containment + topography
6. Hallucination/action failure bridge
7. Implementation bridge
8. Validation/falsifiability section
9. Related-work placeholders
10. SVG placement notes

---

## Intellectual Lineage and Citation Posture

The paper must be intentionally over-cited. The framework should not claim originality for foundational ideas already developed in adjacent literatures.

> The Perceived Topography Framework is not presented as an invention from first principles. It draws from and recombines several established lines of thought: bounded rationality and satisficing, organizational decision theory, organizational learning, sensemaking, affordance theory, reward shaping, retrieval-augmented generation, grounding, and frontier AI safety. Its contribution is to integrate these ideas into a reasoning-state architecture for human-agent systems.

> The goal is not to claim ownership over the underlying traditions, but to show that their combination clarifies a practical design problem: how to shape the environments through which human-agent systems perceive, decide, act, and learn.

The contribution is not inventing the grapes. The contribution is the blend.

**See:** `RELATED_WORK_LEDGER.md` for the full influence tracking ledger with citation targets and section mappings.

### Citation Policy

- If a concept has a recognizable ancestor in another literature, cite it
- Use placeholder tags during drafting (e.g., `[SIMON1955]`, `[WEICK_SENSEMAKING]`)
- Every paper section should end with a citation debt checklist
- Do not wait until final draft to add citations

---

## Guardrails

**Allowed work:** Clarify language, compress concepts, define terms, choose examples, add citations, design diagrams, write narrative sections, identify validation methods.

**NOT allowed without explicit approval:** New primitives, new topography dimensions, new optimizer phases, new foundational architecture documents, major theory expansion.
