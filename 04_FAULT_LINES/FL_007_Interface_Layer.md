# FL_007: The Interface Layer — Neither Agent Nor Environment

**Status:** Open
**Date:** 2026-06-09
**Source:** Co-author reaction to FL_006's open question ("Is retrieval part of the agent or the environment?")

## The Tension

FL_006 asked: Is the retrieval mechanism part of the agent or part of the environment?

The immediate reaction: **Neither.**

A search engine isn't the agent. A search engine isn't the environment. It's an interface.

Likewise:
- Eyes are not reality. Eyes are not the mind. They're the interface.
- Retrieval, memory access, sensor systems, tool calls — they may occupy a **middle layer**.

This suggests a model:

```
Reality
    ↓
Information Surfaces
    ↓
Perception Construction
    ↓
Optimization
```

## Why This Is Dangerous

If this survives scrutiny, then retrieval is not merely a component of perception. It becomes one of the **mechanisms by which reality becomes available to perception**.

That would be a major architectural shift. The current model has two layers between topography and behavior (perception, then optimization). This proposes at least three:

```
Current:    Topography → Perception → Behavior
Proposed:   Topography → Information Surfaces → Perception Construction → Behavior
```

The "Information Surfaces" layer is where retrieval, sensors, memory, tool calls, and interfaces live. It is the boundary between what exists and what the agent can know.

## What This Cracks Open

- **Agent/environment boundary** — If there's an interface layer, the clean agent/environment dichotomy breaks. Where does the agent end and the information surface begin?
- **Design implications** — If you want to change behavior, you now have three intervention points: reshape the topography, reshape the information surfaces, or reshape the agent's perception construction. Current organizational thinking mostly targets the first.
- **AI parallel** — In AI systems, the information surface is explicitly engineered (RAG pipelines, context windows, tool definitions). In human systems, it's emergent (media, social networks, institutional reporting). Same structural role, different mechanisms.

## Connection to Other Files
- Extends `FL_006_Retrieval_vs_Perception.md` — answers "part of agent or environment?" with "neither"
- Feeds `EC_003_Agentic_Retrieval_and_State.md` — retrieval is an information surface
- Feeds `EC_004_Information_Surfaces.md` — the new emerging concept

## Resolution Criteria — Three Possible Futures

This fault line resolves in one of three ways:

### Outcome A — Subset
Information Surfaces turns out to be a subset of Perception. The framework remains mostly unchanged. Information surfaces are a useful label for a class of perceptual inputs but do not warrant their own architectural layer.

### Outcome B — Mechanism
Information Surfaces becomes the mechanism by which Perception is constructed. Moderate architectural change. The layer exists but is subordinate to Perception Construction.

### Outcome C — Fundamental Layer
Information Surfaces becomes a fundamental, independent layer. Major architectural change:

```
Reality
    ↓
Information Surfaces
    ↓
Perception Construction
    ↓
Optimization
    ↓
Interaction
    ↓
Emergent Behavior
```

If Outcome C survives scrutiny, this is a genuinely new branch of the framework.

**Recommended approach:** Do not resolve prematurely. Test each outcome against the examples in EC_004 and see which one breaks first.

## Independent Variability Test (2026-06-09)

**Test:** If Information Surfaces and Perception Construction are the same thing, they should not vary independently. If they can vary independently, they are separable — and separability is evidence for a distinct layer.

**Evidence:**

1. **Same information surface, different perceptions.** Two analysts look at the same KPI dashboard (identical information surface). One sees a growth trend; the other sees a plateau masked by seasonality. The information surface is constant; perception construction varies.

2. **Same perception capability, different outcomes when information surfaces change.** The same analyst, using the same analytical methods, produces a different assessment when the dashboard is redesigned to show raw data instead of smoothed averages. Perception construction capability is constant; the information surface changed, and behavior followed.

**Implication:** Information Surfaces and Perception Construction appear **separable rather than identical**. They can vary independently of each other. This weakens Outcome A (Subset) and strengthens the case for Outcome B (Mechanism) or Outcome C (Fundamental Layer).

**Status:** This is the first successful independence test for FL_007. It does not resolve the fault line — but it narrows the solution space by weakening one of the three outcomes.

## Pressure Note: Visibility as Primitive (2026-06-09)

The recurring concept across governance, retrieval, memory, dashboards, and sensors may be **visibility** rather than information itself. Every example has the same shape:

- Dashboard *visibility*
- Retrieval *visibility*
- Memory *visibility*
- Transfer-document *visibility*
- Sensor *visibility*

The question keeps becoming: **What becomes visible to the optimizer?** — not "What exists?"

This is pressure only. Not a discovery. Not a concept promotion. But "visible" appeared in the seed material's definition of topography ("the topography *visible* from its position") and may be another instance of D009 (language precedes structure). If "visibility" turns out to be the primitive, the layer might be better named than "Information Surfaces."

Note: Information surfaces can exist without governance (nature has them — senses, weather). But governance may not be able to operate without information surfaces (governance requires visibility). This suggests information surfaces may be **more primitive than governance** — not downstream of it.

## Supporting Analysis: Gradient vs Visibility Distinction (2026-06-09)

Gradients and visibility appear similar because behavior responds primarily to perceived gradients. But they may be three distinct things:

| Concept | Definition | Layer |
|---------|-----------|-------|
| **Gradient** | Pressure that exists in reality | Reality / Topography |
| **Visibility** | Whether that pressure is observable | Information Surface |
| **Perceived Gradient** | The optimizer's model of which pressures matter | Perception Construction |

**Implication:** Behavior may be driven more directly by perceived gradients than by either gradients or visibility alone. The chain is:

```
Reality → Gradient → Visibility → Perceived Gradient → Behavior
```

This suggests three layers interacting, not two:
1. A gradient exists (reality)
2. The gradient is or isn't visible (information surface / visibility)
3. The optimizer constructs a model of which visible gradients matter (perception construction)

Each layer can distort independently:
- A real gradient can be invisible (hidden risk)
- A visible gradient can be misperceived (misread signal)
- A perceived gradient can be absent despite reality and visibility (attention failure)

**Status:** Supporting analysis. Not a discovery. Not an architectural promotion. Needs further pressure testing. But this feels close to the center of the framework — it may be where future work concentrates.

## Failure Mode Analysis (2026-06-09)

Three independently testable failure modes, each with a unique intervention:

### 1. Hidden Risk
| Layer | State |
|-------|-------|
| Gradient | Exists |
| Visibility | Absent |
| Perception | N/A (nothing to perceive) |
| Behavior | Unaffected — risk is real but unobserved |

**Intervention:** Increase visibility. Add sensors, dashboards, retrieval paths. Make the gradient observable.

**Example:** A company has rising customer churn (gradient exists) but the executive dashboard doesn't show churn data (visibility absent). Leadership takes no action.

### 2. Misread Signal
| Layer | State |
|-------|-------|
| Gradient | Exists |
| Visibility | Present |
| Perception | Incorrect |
| Behavior | Responds to wrong model |

**Intervention:** Improve interpretation and model construction. Better training, analytical tools, context, or framing.

**Example:** Churn data is on the dashboard (visible), but leadership interprets a seasonal dip as a one-time anomaly rather than a structural trend. They respond to the wrong model.

### 3. Attention Failure
| Layer | State |
|-------|-------|
| Gradient | Exists |
| Visibility | Present |
| Perception | Correct |
| Behavior | Unchanged |

**Intervention:** Modify optimization pressures, incentives, or governance. The optimizer sees the problem correctly but other gradients (quarterly earnings, competitor response) exert stronger pressure.

**Example:** Leadership sees the churn trend, understands it correctly, but prioritizes a product launch because the incentive structure rewards growth over retention.

### Implication

The existence of three distinct failure modes — each with a unique intervention — suggests that Gradient, Visibility, Perception, and Optimization represent **separable components** rather than different names for the same phenomenon. This is the strongest independence argument FL_007 has produced so far.

### Falsifiability Gate (CA_005)

This analysis passes the falsifiability test. If someone can produce a failure that:
- Does not fit one of these three categories, OR
- Requires collapsing two of the layers together to explain

...that would be evidence against the multi-layer model. This is the kind of testable prediction CA_005 has been asking for.

## Relationship Between Topography and Information Surfaces (2026-06-09)

Information Surfaces may not simply be *part of* Topography. They may **mediate** Topography by determining which real gradients become visible to an optimizer.

**Candidate chain (5-layer):**

```
Reality
    → Real Gradients
        → Information Surfaces
            → Visible Gradients
                → Perceived Gradients
                    → Behavior
```

**Working distinctions:**

| Term | Definition |
|------|-----------|
| Real Gradient | Pressure that exists in reality |
| Information Surface | Mechanism/interface that reveals or hides gradients |
| Visible Gradient | Gradient exposed through an information surface |
| Perceived Gradient | Optimizer's interpreted model of the gradient |
| Behavior | Emergent response to perceived gradients |

This is more granular than the earlier 4-layer model (`Reality → Information Surfaces → Perception Construction → Behavior`). It decomposes the process into five steps and distinguishes between what an information surface *exposes* (visible gradient) and what the optimizer *makes of it* (perceived gradient).

**Key implication:** Topography produces real gradients. Information surfaces don't create gradients — they **filter** them. The surface determines which real gradients become visible. Perception construction determines which visible gradients become perceived. Optimization determines which perceived gradients drive behavior.

**Status:** Pressure only. Not an architectural promotion. But this is the most refined candidate hierarchy FL_007 has produced.

## Research Question: Visibility Alignment Hypothesis (2026-06-09)

**Question:** Can an optimizer be made safer or more effective primarily through visibility design, while holding goals constant?

**Prediction:** For a fixed goal and optimizer, increasing visibility of important gradients will improve behavioral outcomes.

**Counter-Prediction:** If behavior does not improve when important gradients become visible, the role of visibility in the framework may be overstated.

**Test domains:**

| Domain | Fixed Goal | Visibility Intervention | Expected Outcome |
|--------|-----------|------------------------|-----------------|
| Marketing | Maximize campaign ROI | Add lost-deal and churn data to knowledge platform | More balanced campaign strategy |
| Organizations | Meet quarterly targets | Add long-term retention metrics to executive dashboard | Reduced short-termism |
| AI agents | Maximize engagement | Add trust/churn/support signals to context | Sustainable vs aggressive engagement |
| AI assistants | Complete user task | Add user history and preference context | More relevant, personalized responses |

**Why this matters:** This is the framework's most direct testable claim. If visibility design alone — without changing goals, incentives, or the optimizer — produces measurably better outcomes, the information surface layer earns its architectural place empirically, not just theoretically.

**Status:** Research question. Requires experimental validation. The agent governance example (Agent A vs Agent B) provides the clearest thought experiment, but has not been tested with real systems.

## Pressure Note: Goal-Driven Gradient Selection (2026-06-09)

Visibility alone may not determine behavior. Goals may influence which *visible* gradients are considered relevant and therefore incorporated into perception construction.

**Example:** A VP told "maximize revenue" and a VP told "maximize customer lifetime value" may look at the same dashboard (identical visibility) and attend to different metrics. The goal acts as a filter on visible gradients — a form of attention allocation that sits between visibility and perception.

A richer goal specification naturally generates information needs, which guide retrieval and attention. This suggests the relationship between goals and visibility may be bidirectional:
- Visibility shapes what the optimizer can perceive (framework's current claim)
- Goals shape what the optimizer *does* perceive among what's visible (pressure against the Visibility Alignment Hypothesis)

**Pressure Question:** Does behavior depend more strongly on visibility or on goal-driven selection among visible gradients?

If goal-driven selection dominates, then the Visibility Alignment Hypothesis ("increasing visibility improves outcomes") needs qualification: visibility improves outcomes *only when the goal specification is rich enough to make the new gradients relevant*.

**Connections:**
- Visibility Alignment Hypothesis (direct pressure)
- EC_003 (Agentic Retrieval — goal-driven retrieval is goal-driven gradient selection)
- FL_008 (Selection of Information Surfaces — goals may be one of the selection principles)
- Concept-based retrieval, goal interpretation

**Status:** Pressure only. No promotion.

## Pressure Note: Context as Contributor to Interpretation (2026-06-10)

Two optimizers exposed to the same visible gradients may construct different perceived gradients because they bring different **contextual knowledge** to the interpretation process.

**Example:** Both VPs observe the same data: churn rising, complaints increasing, revenue flat.

- VP A (product background) interprets: **Product Quality Problem**
- VP B (marketing background) interprets: **Marketing Messaging Problem**

Visibility is identical. Interpretation differs. The difference is the context each VP brings — prior experience, domain knowledge, mental models.

**Candidate sub-chain:**

```
Visible Gradient → Context → Interpretation → Perceived Gradient
```

**Pressure Question:** Does context represent:
- (a) An independent mechanism between visibility and perception?
- (b) A contributor to interpretation (a sub-process within perception construction)?
- (c) A property of perception construction (not separable)?

**D011 test:** If context is independent (a), then "change the context" should be a different intervention from "improve visibility" or "change the goal," and it should be differentially effective for interpretation failures specifically.

**Status:** Pressure only. No promotion. Requires D011 evaluation.

## Pressure Note: Concepts as Behavioral Gradients for Agents (2026-06-10)

Concepts are not passive categories when used by agents. They become **navigable structures** that influence what agents retrieve, notice, interpret, and recommend. In framework terms, well-structured concepts function as gradients — they exert behavioral pull on the optimizer.

**Key Risk:** Well-structured concepts may exert more behavioral pull than poorly structured but more important concepts. The structure of the concept layer becomes a form of topography that the agent navigates.

**Example:** If competitor analysis assets are clean, well-tagged, and richly linked, while customer-pain assets are messy, scattered, and poorly labeled — an agent may over-index on competitive positioning and under-index on customer reality. Not because competitive positioning matters more, but because the gradient is steeper. The landscape is easier to traverse in that direction.

**Implication:** Concept governance must account for:
- Over-weighting risk (clean concepts attract disproportionate attention)
- Under-weighting risk (messy but important concepts get ignored)
- Counterbalancing concepts (deliberately strengthening weak-but-important areas)
- Authoritative sources (which assets are canonical for a given concept)
- Allowed agent uses (what an agent should and should not do with a concept)

**Hard Principle:**

> Do not create first-class concepts merely because humans recognize them. Create them only if you are willing for agents to navigate by them.

**Connection to D014:** If concepts are active structures (D014), then concept quality directly shapes agent behavior. Concept governance is a form of information surface governance — and potentially one of the most operationally important forms.

**Status:** Pressure note. Not promotion. Requires operational validation.

## Open Questions
- Is "Information Surfaces" the right term? Alternatives: interface layer, epistemic membrane, perception substrate, **visibility layer**.
- Can an agent modify its own information surfaces? (Humans build tools. AI agents select tools.)
- Does this layer exist in all systems or only in complex ones?
- If the agent can reshape its information surfaces, is that a form of reshaping its own topography?
- Is "visibility" the more fundamental concept underlying information surfaces?
- Does goal specification act as a filter between visibility and perception construction?
