# OP_001: Decision Topography Discovery Framework

**Classification:** Operational tool
**Date:** 2026-06-11
**Status:** Application pattern — not architecture

## Purpose

Provide a practical interrogation framework for organizational discovery that maps decision topography rather than inventorying artifacts.

## Previous Approach: Artifact Inventory

- What reports exist?
- What dashboards exist?
- What data exists?

This maps *what the organization has*. It does not map *how the organization decides*.

## New Approach: Decision Topography Discovery

These questions map the gradients, visibility gaps, and failure modes of organizational decision-making:

### Goal Discovery
- **What decisions do you make?**
- **What outcomes matter most?**

### Signal Discovery
- **What signals influence those decisions?**
- **What information do you trust?**
- **What information do you not trust?**

### Visibility Gap Discovery
- **What information is difficult to access?**
- **What information repeatedly surprises you?**

### Assumption Discovery
- **What assumptions drive your actions?**
- **What evidence changes your mind?**
- **What evidence should change your mind but doesn't?**

### Constraint Discovery
- **What bottlenecks prevent action?**
- **What information would allow an agent to help you?**

## Mapping to Topography Engineering Dimensions

| Discovery Question | Dimension Probed |
|-------------------|-----------------|
| What decisions do you make? | Goal |
| What signals influence those decisions? | Visibility, Goal Relevance |
| What information do you trust? | Confidence |
| What information do you not trust? | Confidence (negative) |
| What information is difficult to access? | Accessibility |
| What information repeatedly surprises you? | Visibility (gaps) |
| What assumptions drive your actions? | Working Theory / Interpretation |
| What evidence changes your mind? | Confidence, Contradiction |
| What evidence should change your mind but doesn't? | Attention Failure |
| What bottlenecks prevent action? | Accessibility, Policy Constraint |
| What information would allow an agent to help you? | Goal Relevance, Visibility |

## Current Hypothesis

> The purpose of discovery is not inventory. The purpose of discovery is mapping organizational decision topography.

## Relationship to Framework

This tool naturally emerges from the theory. The old approach (artifact inventory) corresponds to the Infrastructure Layer. The new approach (decision topography discovery) corresponds to the Topography Engineering Layer. The questions directly probe the candidate dimensions from D015.

## Cross-References
- D015 (Topography Engineering Dimensions — the dimensions these questions probe)
- FL_010 (Layer Separation — this tool belongs to the Topography Engineering layer)
- VP Marketing Visibility Interview (07_NARRATIVE_ARCHITECTURE/EXAMPLES.md — the earlier, less refined version)
- Decision Ecosystem Mapping (07_NARRATIVE_ARCHITECTURE/EXAMPLES.md — the application pattern)
