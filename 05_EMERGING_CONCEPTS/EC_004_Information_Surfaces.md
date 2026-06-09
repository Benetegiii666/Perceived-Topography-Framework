# EC_004: Information Surfaces

**Status:** Nascent — emerged from FL_007
**Date:** 2026-06-09

## The Concept

Information Surfaces are the mechanisms by which reality becomes available to perception. They sit between objective topography and perception construction:

```
Reality / Topography
        ↓
  Information Surfaces    ← eyes, sensors, retrieval, memory, media, tool calls
        ↓
  Perception Construction
        ↓
  Behavior / Optimization
```

They are neither agent nor environment. They are the **interface** through which topography becomes perceivable.

## Examples

| Reality | Information Surface |
|---------|-------------------|
| Customer sentiment | Dashboard |
| Market behavior | Stock ticker |
| Corporate health | KPI report |
| Scientific truth | Journal publication |
| Physical world | Human senses |
| Enterprise data | RAG system |
| Live system state | API call |
| Student understanding | Assessment scores |
| Codebase health | CI/CD pipeline |
| Public opinion | Polling data |

### By Domain

| Domain | Information Surfaces |
|--------|---------------------|
| Human biology | Eyes, ears, proprioception, interoception |
| AI agents | RAG pipelines, context windows, tool definitions, vector search |
| Organizations | Dashboards, reports, KPIs, meeting structures, Slack channels |
| Markets | Price signals, news media, analyst reports, social sentiment |
| Research | Literature databases, peer review, citation networks |
| Politics | Polling, media coverage, constituent feedback channels |
| Education | Grades, assessments, participation metrics |

## Why This Might Be Important

1. **Third intervention point** — If you want to change behavior, you can reshape topography, reshape information surfaces, or reshape perception construction. Most organizational design focuses on the first. Most AI engineering focuses on the second. Almost nobody talks about the third.

2. **Explains KPI gaming** — KPIs are information surfaces. Gaming them doesn't change reality — it distorts the information surface, which distorts perception construction, which changes behavior. The topography hasn't moved. The interface has been corrupted.

3. **Retrieval finds its home** — Retrieval is not peripheral. It is one class of information surface. This gives EC_003 a parent concept.

## Maturity Assessment

This is a nascent concept. It needs:
- A precise definition (currently intuitive)
- Boundary conditions (what ISN'T an information surface?)
- Relationship mapping to existing architecture concepts
- At least one counterargument or limitation

## Watch For
If this concept matures, it could trigger a convergence with FL_006 and FL_007, which under Protocol #4 would be grounds for an architecture update.
