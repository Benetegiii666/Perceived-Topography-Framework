# DISCOVERY_012: Failure Classification Produces Differential Interventions

**Status:** Candidate — requires additional examples and pressure testing before promotion
**Date:** 2026-06-10

## Observation

Goal Failure, Context Failure, Attention Failure, and Interpretation Failure each produce distinct corrective actions. This satisfies D011's requirement that meaningful architectural distinctions must support differential intervention.

## Evidence

| Failure Type | Primary Intervention |
|-------------|---------------------|
| Goal Failure | Objective redesign |
| Context Failure | Knowledge/context improvement |
| Attention Failure | Salience/prioritization redesign |
| Interpretation Failure | Reasoning/explanation improvement |

## Implication

The framework may function as a **practical diagnostic system** for:
- AI governance
- Context-layer governance
- Retrieval system design
- Organizational decision support

This extends the original three failure modes (Hidden Risk, Misread Signal, Attention Failure from FL_007) into a four-category diagnostic that maps to the visible-to-perceived transformation zone. The addition of Goal Failure and the split of the original categories into Goal/Context/Attention/Interpretation provides finer-grained diagnosis.

## D011 Validation

D011 (Differential Intervention Principle) states: "If you can't differentially intervene, the layers aren't real."

This discovery provides the first evidence that the four components (Goal, Context, Attention, Interpretation) pass the D011 test — each produces a different intervention. If further testing confirms that targeting the correct component outperforms targeting the wrong one, these distinctions earn their place.

## Cross-References
- D011 (Differential Intervention Principle — this is the first application of the expanded model)
- FL_007 (Failure Mode Analysis — original three-category version)
- CA_005 (Unfalsifiability — extends the falsifiability gate to four categories)
- Decision Ecosystem Mapping (07_NARRATIVE_ARCHITECTURE/EXAMPLES.md — the application pattern this validates)
