# AHA_010: Retrieval Is Really Gradient Selection

**Status:** Promoted — explicitly in paper
**Paper Status:** Appears in Section 13.8 (Retrieval Requirements)
**Date:** 2026-06-09

## The Moment

We kept talking about RAG, agentic retrieval, concept retrieval, tool-augmented state. Eventually the common thread appeared.

The important question isn't: *"What documents should be retrieved?"*

It's: **"Which gradients deserve attention for the decision being made?"**

## Why It Matters

This was the first moment the retrieval discussion connected directly to the framework. Retrieval stopped being a technical implementation detail and became a specific instance of gradient selection — the act of choosing which pressures from reality become visible to the optimizer.

This reframe changes how you evaluate retrieval systems: not by recall or precision, but by whether the retrieved gradients are capable of changing the decision.

## Cross-References
- EC_003 (Agentic Retrieval and State)
- EC_004 (Information Surfaces — retrieval as surface design)
- Decision Support vs Information Retrieval (07_NARRATIVE_ARCHITECTURE/EXAMPLES.md)
- FL_006 (Retrieval vs Perception)
