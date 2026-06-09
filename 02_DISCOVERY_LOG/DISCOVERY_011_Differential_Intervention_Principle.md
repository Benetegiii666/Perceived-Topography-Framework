# DISCOVERY_011: Differential Intervention Principle

**Status:** Candidate — needs pressure testing
**Date:** 2026-06-09

## Observation

A proposed architectural layer should predict that interventions targeted at failures within that layer outperform interventions targeted at other layers.

If a layer is real — if it represents a genuinely separable component of the system — then correctly diagnosing which layer failed and intervening at that layer should produce better outcomes than intervening at the wrong layer.

## The Principle

**If you can't differentially intervene, the layers aren't real.**

This gives the framework a general falsifiability mechanism: any time a new layer is proposed, ask whether it predicts differential intervention effectiveness. If it does, the layer is testable. If it doesn't, the layer may be a relabeling rather than a genuine architectural distinction.

## Example

From FL_007's failure mode analysis:

| Diagnosis | Correct Intervention | Wrong Intervention |
|-----------|---------------------|-------------------|
| Hidden Risk (visibility failure) | Increase visibility → should improve outcomes | Changing incentives or improving training → should not help as much |
| Misread Signal (perception failure) | Improve interpretation/models → should improve outcomes | Adding more dashboards or changing incentives → should not help as much |
| Attention Failure (optimization failure) | Modify incentives/governance → should improve outcomes | Adding dashboards or improving training → should not help as much |

If the correct intervention doesn't outperform the wrong one, the layer distinction has no practical value.

## Generalized Application

This principle applies beyond FL_007. For any future architectural proposal:

1. **Propose the layer**
2. **Identify a failure mode unique to that layer**
3. **Predict an intervention that targets that layer specifically**
4. **Ask: would targeting a different layer produce the same result?**

If yes → the layers may not be separable.
If no → the layer is earning its place in the architecture.

## Relationship to CA_005

This is the practical falsifiability mechanism CA_005 has been asking for. CA_005 asks "what would disprove the framework?" The Differential Intervention Principle answers: "A layer that doesn't predict differential intervention effectiveness."

This converts architectural debates from philosophical ("is this really a separate layer?") to empirical ("does intervening here outperform intervening there?").

## Cross-References
- CA_005 (Unfalsifiability — this provides the operational test)
- FL_007 (Interface Layer — failure mode analysis is the first application)
- FL_008 (Selection of Information Surfaces — candidate for differential intervention testing)
