# FL_014: Optimizer Investigation Dynamics

**Status:** RESOLVED
**Date:** 2026-06-11
**Phase:** 3.2 (Complete)

## Core Finding

Investigation is not triggered by information alone. Investigation occurs when:

```
Goal-Relevant Observation + Confidence Gap = Investigation Trigger
```

## Investigation Navigation

Connectivity guides explanatory search. The optimizer follows connected explanatory paths attempting to reduce uncertainty around a goal-relevant observation.

## Investigation Continuation

Investigation continues while explanatory confidence remains insufficient.

## Investigation Termination

Investigation terminates when:

1. Confidence becomes sufficient
2. No viable explanatory paths remain
3. The investigation is no longer goal-relevant

## Architectural Significance

This provides a coherent explanation for:
- Why investigation starts (goal-relevant observation + confidence gap)
- Why investigation continues (insufficient confidence + viable paths)
- Why task spawning occurs (new explanatory paths discovered during investigation)
- Why investigation stops (sufficiency, path exhaustion, or goal-relevance loss)

## Cross-References
- FL_015 (Sufficiency — investigation termination depends on sufficiency)
- FL_009 (Optimizer Architecture — investigation emerges from Goal + Policy + Interpretation)
- D015 (Topography Engineering Dimensions — Confidence and Connectivity guide investigation)
