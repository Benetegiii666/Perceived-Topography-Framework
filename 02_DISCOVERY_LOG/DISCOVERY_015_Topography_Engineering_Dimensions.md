# DISCOVERY_015: Topography Engineering Dimensions

**Status:** Candidate — dimensions need D011 reduction
**Date:** 2026-06-11
**Source:** Session synthesis — Topography Engineering layer extraction

## Observation

When translating optimizer theory into actionable environmental design, a set of candidate dimensions emerged that describe how an optimizer experiences an information environment. These are not organizational entities — they are **navigation dimensions**.

## Core Question

What properties of an information environment create gradients that influence optimizer behavior?

## Candidate Independent Dimensions

| Dimension | Definition |
|-----------|-----------|
| **Visibility** | Can the optimizer see this gradient? |
| **Accessibility** | Can the optimizer reach/use this information? |
| **Representation** | How is the gradient expressed/structured? |
| **Confidence** | How much should the gradient be trusted? |
| **Connectivity** | How does this gradient relate to other gradients? |
| **Goal Relevance** | How much does this gradient matter for the current objective? |

## Candidate Modifiers

| Modifier | Definition |
|----------|-----------|
| **Contradiction** | Does this gradient conflict with other evidence? |
| **Recency** | How current is this gradient? |

## Potential Separate Category

| Candidate | Definition | Question |
|-----------|-----------|----------|
| **Policy Constraint** | Rules governing what the optimizer may do with this gradient | Is this a dimension of the environment or an optimizer primitive? (Cross-layer leak flagged in FL_010) |

## D011 Reduction Needed

Which dimensions are truly independent? Initial pressure tests:

- **Accessibility vs Visibility:** Something accessible but unknown (not visible) and something visible but locked (not accessible) — seem independent
- **Confidence vs Representation:** Well-represented with low confidence vs poorly represented with high confidence — seem independent
- **Goal Relevance vs Goal (optimizer primitive):** Goal Relevance may be the projection of the optimizer's Goal onto the surface, not a property of the surface itself — potential collapse

## Implication

These dimensions are the design vocabulary for Topography Engineering. When designing a context layer, dashboard, retrieval system, or agent workspace, these are the parameters being manipulated. Each dimension should predict a differential intervention (D011): changing Visibility should produce different effects than changing Accessibility or Representation.

## Cross-References
- FL_010 (Layer Separation — this belongs to the Topography Engineering layer)
- FL_007 (Interface Layer — environmental decomposition)
- D011 (Differential Intervention Principle — the test these must pass)
- D014 (Concepts as Active Structures — concepts may influence multiple dimensions simultaneously)
