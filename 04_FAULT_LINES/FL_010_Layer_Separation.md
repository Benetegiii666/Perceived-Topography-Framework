# FL_010: Layer Separation — Theory vs Engineering vs Architecture vs Implementation

**Status:** Open
**Date:** 2026-06-11
**Source:** Session synthesis after major course correction

## The Tension

The framework was unintentionally mixing four distinct concerns into a single conceptual layer:

1. **Theory** — Why does behavior happen? (Optimizer theory)
2. **Topography Engineering** — What environmental properties create gradients? (Design dimensions)
3. **Organizational Reasoning Architecture** — How should reasoning be structured for retrieval? (Entity schema)
4. **Implementation** — What do we build? (Software, processes, tools)

Separating them resolved confusion where contributors were arguing at different layers without realizing it (e.g., theoretical reduction to Claims vs. architectural reasoning objects like Working Theory — both correct, at different layers).

## D011 Test: Do the Layers Vary Independently?

- Change Theory (add optimizer primitive) without changing Topography Engineering → **Yes**
- Change Topography Engineering (collapse a dimension) without changing Architecture → **Yes**
- Change Architecture (rename entities) without changing Implementation → **Yes**
- Change Implementation (switch storage) without changing Architecture → **Yes**

Each layer varies independently. The separation is genuine.

## Layer Definitions

| Layer | Question | Output |
|-------|----------|--------|
| Theory | Why does behavior happen? | Explanatory model |
| Topography Engineering | What environmental properties create gradients? | Design dimensions |
| Organizational Reasoning Architecture | How should reasoning be structured? | Entity schema |
| Implementation | What do we build? | Software, processes, tools |

## Known Issues

### Soft Boundary: Theory ↔ Topography Engineering
These share a theoretical foundation. Topography Engineering could be called "applied theory." The separation earns its keep because the questions are different (what's true vs. what's designable), but the boundary is softer than the others.

### Cross-Layer Leaks
- **Goal** appears in Theory (optimizer primitive) and Architecture (reasoning object)
- **Policy** appears in Theory (optimizer primitive), Architecture (reasoning object), and Topography Engineering (Policy Constraint dimension)
- These may be legitimate cross-layer presence or naming collisions. Needs explicit resolution.

### Governance Gap
No layer explicitly addresses who decides what the system should do. Governance keeps emerging (FL_004, FL_008, AHA_012) as a distinct concern. May need its own layer — or may be absorbed by the existing four. Flagged as pressure candidate.

### Information Flow Direction
Undefined: does operational experience at the Architecture/Implementation layers feed back to Theory? Or does information only flow downward? This matters for framework evolution.

## Open Subquestions

1. Is Topography Engineering a legitimate independent layer or just applied Theory?
2. Should Governance be a fifth layer?
3. How do Goal and Policy relate across layers — same concept at different abstraction, or different concepts with shared name?
4. Does the Architecture layer have standing to pressure Theory?
5. Does this separation hold across non-marketing domains?

## Cross-References
- FL_009 (Optimizer Architecture — Theory layer)
- FL_007 (Interface Layer — Topography Engineering layer)
- D015 (Topography Engineering Dimensions — if created)
- CA_005 (Unfalsifiability — separation reduces framework drift)
