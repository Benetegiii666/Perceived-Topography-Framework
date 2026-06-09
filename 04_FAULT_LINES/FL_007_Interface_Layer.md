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

## Open Questions
- Is "Information Surfaces" the right term? Alternatives: interface layer, epistemic membrane, perception substrate.
- Can an agent modify its own information surfaces? (Humans build tools. AI agents select tools.)
- Does this layer exist in all systems or only in complex ones?
- If the agent can reshape its information surfaces, is that a form of reshaping its own topography?
