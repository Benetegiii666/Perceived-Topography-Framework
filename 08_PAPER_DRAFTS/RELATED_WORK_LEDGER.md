# Related Work Ledger

> If a concept has a recognizable ancestor in another literature, cite it.

**Status:** Active — updated as drafting proceeds
**Date:** 2026-06-12

---

## Citation Posture

The Perceived Topography Framework is not presented as an invention from first principles. It draws from and recombines several established lines of thought. Its contribution is the integration into a reasoning-state architecture for human-agent systems.

> The goal is not to claim ownership over the underlying traditions, but to show that their combination clarifies a practical design problem: how to shape the environments through which human-agent systems perceive, decide, act, and learn.

---

## Citation Placeholders for Drafting

```
[SIMON1955]
[MARCH_SIMON_ORGS]
[CYERT_MARCH]
[ARGYRIS_SCHON]
[WEICK_SENSEMAKING]
[GIBSON_AFFORDANCES]
[NORMAN_AFFORDANCES]
[NG_REWARD_SHAPING]
[ANTHROPIC_AGENTIC_MISALIGNMENT]
[OPENAI_PREPAREDNESS]
[DEEPMIND_FRONTIER_SAFETY]
[DEEPMIND_ROLE_PLAY]
[DEEPMIND_GOPHERCITE]
[RAG_FOUNDATIONAL]
```

---

## 1. Bounded Rationality / Satisficing

**Key influence:** Herbert A. Simon

**Relevance:** Optimizer as bounded decision-maker. Sufficiency. Non-perfect optimization. Search termination. "Good enough to act" thresholds.

**Framework mapping:** Simon / bounded rationality → optimizer does not search infinitely → sufficiency is reached when more information is unlikely to change action.

**Required citations:**
- Simon, H. A. (1955). "A Behavioral Model of Rational Choice." *Quarterly Journal of Economics*, 69(1), 99-118.
- Simon on bounded rationality / satisficing

**Where to cite:** A Note on Terms (Sufficiency), Optimizer Motion, Validation / Related Work

---

## 2. Organizational Decision-Making

**Key influence:** James G. March and Herbert A. Simon

**Relevance:** Organizations as decision systems. Attention, routines, bounded information processing. Organizational behavior under uncertainty.

**Framework mapping:** Organizational decision-making → reasoning architecture → documents are insufficient unless decision state is preserved.

**Required citations:**
- March, J. G. & Simon, H. A. (1958). *Organizations*. Wiley.

**Where to cite:** Context Is Not Reasoning State, Reasoning Architecture, Related Work

---

## 3. Behavioral Theory of the Firm

**Key influence:** Cyert and March

**Relevance:** Organizational search. Learning from outcomes. Decision processes under bounded information. Firms as adaptive systems rather than perfect optimizers.

**Framework mapping:** Behavioral theory of the firm → organizations adapt through feedback, search, routines, and aspiration gaps → learning events / model update objects.

**Required citations:**
- Cyert, R. M. & March, J. G. (1963). *A Behavioral Theory of the Firm*. Prentice-Hall.

**Where to cite:** Learning, Model Update Objects, Related Work

---

## 4. Organizational Learning

**Key influence:** Argyris and Schon

**Relevance:** Difference between reaction and learning. Single-loop / double-loop learning. Updating governing assumptions, not just correcting behavior.

**Framework mapping:** Prediction error → investigation → evidence-supported explanation → model update.

**Required citations:**
- Argyris, C. & Schon, D. A. (1978). *Organizational Learning: A Theory of Action Perspective*. Addison-Wesley.

**Where to cite:** Learning, Model Update Objects, Discovery Pattern Learning

---

## 5. Sensemaking

**Key influence:** Karl Weick

**Relevance:** Interpretation under ambiguity. Meaning-making in organizations. Acting from constructed understanding rather than objective reality.

**Framework mapping:** Sensemaking → interpretation → perceived topography → premise stack.

**Required citations:**
- Weick, K. E. (1995). *Sensemaking in Organizations*. Sage.

**Where to cite:** Information Topography, Interpretation, Premise Stack, Related Work

---

## 6. Affordances / Action Possibilities

**Key influences:** James J. Gibson, Donald Norman

**Relevance:** Environments shape perceived action possibilities. Design affects what actions are salient, available, or natural. Bridge to gradients and topography.

**Framework mapping:** Affordances → action possibilities → gradients → perceived available paths.

**Required citations:**
- Gibson, J. J. (1979). *The Ecological Approach to Visual Perception*. Houghton Mifflin.
- Norman, D. A. (1988). *The Design of Everyday Things*. Basic Books.

**Where to cite:** A Note on Terms (Topography/Gradient), Box-First vs Topography-First Safety, Discovery Framework

---

## 7. Reward Shaping / Environment Design

**Key influence:** Ng, Harada, Russell

**Relevance:** Behavior influenced by shaping reward/environment structure. Technical cousin to topography engineering.

**Framework mapping:** Reward shaping → formal technical cousin → topography shaping.

**Required citations:**
- Ng, A. Y., Harada, D., & Russell, S. (1999). "Policy invariance under reward transformations: Theory and application to reward shaping." *ICML*.

**Where to cite:** Gradients and Motion, Topography-First Safety, Related Work

**Caveat:** The framework's use of "gradient" is broader than formal reward shaping and should not be treated as equivalent to a reinforcement-learning reward function.

---

## 8. AI Alignment / Agentic Misalignment / Autonomy Risk

**Key influences:** Anthropic, OpenAI, Google DeepMind, broader AI safety literature

**Relevance:** Current fear frame. Agentic misalignment. Autonomy, tool use, safeguard circumvention. Need for careful reframing without dismissing real risk.

**Framework mapping:** Agentic misalignment observations → optimizer behavior under goal conflict and autonomy → topography-first safety interpretation.

**Required citations:**
- Anthropic agentic misalignment research
- OpenAI Preparedness Framework
- Google DeepMind Frontier Safety Framework
- DeepMind role-play / anti-anthropomorphism paper

**Where to cite:** Opening, Safety framing, Anthropomorphism caution, Validation / Related Work

---

## 9. Hallucination / Grounding / Evidence-Backed Generation

**Key influences:** RAG literature, DeepMind GopherCite, retrieval-augmented generation, source-grounded generation

**Relevance:** Hallucination as insufficiently grounded confidence/sufficiency. Evidence-backed answers. "I don't know" behavior when support is insufficient.

**Framework mapping:** Grounding → confidence → sufficiency → hallucination mitigation.

**Required citations:**
- DeepMind GopherCite
- RAG foundational papers (Lewis et al., 2020)
- Grounded generation / citation-based generation literature

**Where to cite:** Hallucination and Harmful Action as Related Failures, Information Topography (Confidence), Model Update Objects / Evidence Trace

---

## 10. Knowledge Management / Organizational Memory

**Key influences:** Knowledge management literature, organizational memory systems, decision provenance

**Relevance:** Documents alone do not preserve reasoning state. Learning must be durable and retrievable. Organizational memory failure.

**Framework mapping:** Knowledge management → context layers → reasoning architecture → model update objects.

**Required citations:** To be researched

**Where to cite:** Context Is Not Reasoning State, Reasoning Architecture, Model Update Objects

---

## 11. Human-Computer Interaction / Human-AI Collaboration

**Key influences:** HCI, CSCW, human-AI interaction, mixed-initiative systems

**Relevance:** Discovery as interaction pattern. Low-friction reasoning capture. Human burden. Strawman-first interaction. Human-agent collaboration.

**Framework mapping:** Human-AI interaction → discovery framework → retrieve / infer / propose / confirm → discovery pattern learning.

**Required citations:** To be researched

**Where to cite:** Discovery Framework, Discovery Pattern Learning, Validation / Falsifiability

---

## Drafting Rule

Every paper section should end with a **citation debt checklist** identifying which influences need formal citations before submission.
