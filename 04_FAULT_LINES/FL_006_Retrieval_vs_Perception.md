# FL_006: Retrieval vs Perception

**Status:** Open — Priority research target
**Opened:** 2026-06-09

## The Tension

The current framework models behavior as:

```
Topography → Perception → Optimization
```

But there is a growing suspicion that perception is not a passive layer — it is actively *constructed*. If so, the model becomes:

```
Topography → Perception Construction → Optimization
```

This is not a minor relabeling. "Perception" implies the agent receives a view of the landscape. "Perception Construction" implies the agent *builds* its view through active processes — retrieval, filtering, weighting, context assembly.

## Why This Matters

If perception is constructed (not received), then:

1. **Retrieval is not peripheral** — it becomes the mechanism by which perception is assembled.
2. **The framework gains a causal mechanism** — instead of just saying "perception mediates," we can explain *how* it mediates.
3. **AI systems become a primary example** — agentic retrieval (RAG, context window management, tool selection) is literally perception construction in action.
4. **The metaphor deepens** — the marble doesn't just roll on a slope it perceives. It constructs the slope through what it retrieves about the landscape.

## Connection to EC_003

`05_EMERGING_CONCEPTS/EC_003_Agentic_Retrieval_and_State.md` is developing the retrieval side of this question. If EC_003 matures, it may resolve this fault line — which under Protocol #4 would be one of the two valid triggers for changing the concept architecture.

## Open Questions

- Is all perception constructed, or only some? (Humans have involuntary perception too.)
- Does "construction" imply agency? If so, does that conflict with emergence?
- In AI systems, is the retrieval mechanism part of the agent or part of the environment?
- Can we distinguish between perception construction and attention?
