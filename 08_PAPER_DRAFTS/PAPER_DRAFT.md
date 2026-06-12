# The Perceived Topography Framework

## A Reasoning-State Architecture for Human-Agent Systems

### Draft Status

Narrative Paper v1
Concept Architecture v0.1 frozen
Drafting phase: Section 1 complete

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

*[To be drafted — full content available in PAPER_ARCHITECTURE.md]*

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
