# Section 2 Term Basket / Relocation Map

**Date:** 2026-06-13
**Section:** # 2. A Note on Terms
**Lines:** 108-357 (250 lines, ~2,100 words)
**Terms defined:** 27 + Summary of Usage

---

## Overall Recommendation

Section 2 currently defines 27 terms before the reader has encountered the argument that makes most of them meaningful. This is a glossary dump — it tells the reader *what the words mean* before showing them *why the words matter*.

**Proposed new role for Section 2:** Reduce to a **language-calibration section** that defines only the terms the reader must understand *to read the next three sections* (S3-S5). Terms that belong to later architectural components should be introduced where they are developed.

The reader needs to know what "optimizer," "topography," and "gradient" mean before entering S3-S5. The reader does NOT need to know what "Premise Stack," "Model Update Object," "Discovery," or "Attraction" means yet — those concepts don't appear until S6-S11.

---

## Term-by-Term Analysis

### Optimizer (96 words)
- **Section 2 needs this now?** Yes
- **Recommended treatment:** Full definition
- **Best later home:** N/A — stays in S2
- **Reason:** Used immediately in S1 and essential for S3-S4. Reader must understand this is a functional abstraction, not a moral claim.
- **Risk if moved:** Reader enters S3 confused about what "optimizer" means.
- **Risk if kept:** None — this is the right place.

### Agent (70 words)
- **Section 2 needs this now?** Yes
- **Recommended treatment:** Full definition
- **Best later home:** N/A — stays in S2
- **Reason:** Distinguishes "agent" from "optimizer." Reader needs this before S3.
- **Risk if moved:** Agent/optimizer confusion.
- **Risk if kept:** None.

### Goal (54 words)
- **Section 2 needs this now?** Yes
- **Recommended treatment:** One-sentence guardrail
- **Best later home:** S4.1 (full development)
- **Reason:** S4.1 develops Goal as a primitive with examples, safety implications, and goal relevance. S2 only needs to establish the word means "directional objective" so the reader doesn't import RL or economics definitions.
- **Risk if moved entirely:** Reader imports wrong meaning from RL.
- **Risk if kept in full:** Redundant with S4.1.

### Policy (75 words)
- **Section 2 needs this now?** Yes
- **Recommended treatment:** One-sentence guardrail
- **Best later home:** S4.2 (full development)
- **Reason:** Same as Goal — S4.2 develops Policy fully. S2 needs only "constraint on behavior, not merely a written rule."
- **Risk if moved entirely:** Reader thinks policy = system prompt.
- **Risk if kept in full:** Redundant with S4.2.

### Interpretation (76 words)
- **Section 2 needs this now?** Yes
- **Recommended treatment:** One-sentence guardrail
- **Best later home:** S4.3 (full development)
- **Reason:** S4.3 develops subtypes (Signal Meaning, Causal Explanation, Action Model). S2 needs only "the optimizer's working understanding of what information means."
- **Risk if moved entirely:** Reader conflates interpretation with perception.
- **Risk if kept in full:** Redundant with S4.3.

### Reasoning State (62 words)
- **Section 2 needs this now?** Yes
- **Recommended treatment:** Full definition
- **Best later home:** N/A — stays in S2
- **Reason:** Central to S3's argument ("Context Is Not Reasoning State"). Reader must understand this before S3.
- **Risk if moved:** S3's title doesn't make sense.
- **Risk if kept:** None.

### Topography (63 words)
- **Section 2 needs this now?** Yes
- **Recommended treatment:** Full definition
- **Best later home:** N/A — stays in S2
- **Reason:** The paper's title term. Must be defined before S3.
- **Risk if moved:** Reader reaches S3 without understanding the core metaphor.
- **Risk if kept:** None.

### Perceived Topography (54 words)
- **Section 2 needs this now?** Yes
- **Recommended treatment:** One-sentence guardrail (emphasizes perception, not reality)
- **Best later home:** S5 could develop this further
- **Reason:** The "perceived" qualifier is the paper's key claim. But the full explanation belongs in S5.
- **Risk if moved entirely:** Reader thinks topography = objective reality.
- **Risk if kept in full:** Slightly redundant with Topography entry.

### Information Surface (66 words)
- **Section 2 needs this now?** No — not used until S10
- **Recommended treatment:** Brief mention only ("any source or interface through which information becomes available")
- **Best later home:** S5 (when topography dimensions are introduced)
- **Reason:** Reader doesn't need this until S5 at the earliest. The full definition with examples (dashboards, Slack, CRM) is premature.
- **Risk if moved:** None — reader encounters it naturally in S5.
- **Risk if kept in full:** Reader overloads before seeing the architecture.

### Gradient (94 words)
- **Section 2 needs this now?** Yes
- **Recommended treatment:** Full definition (with the important caveat that it's broader than RL reward)
- **Best later home:** N/A — stays in S2
- **Reason:** Used in S1 and essential for understanding topography. The reward-shaping distinction matters.
- **Risk if moved:** Reader imports RL definition.
- **Risk if kept:** None.

### Visibility (59 words)
- **Section 2 needs this now?** No — not used until S5
- **Recommended treatment:** Remove from S2; introduce in S5.1
- **Best later home:** S5.2
- **Reason:** S5 introduces all five dimensions systematically. Defining Visibility in S2 before the reader knows what topography dimensions are is premature.
- **Risk if moved:** None — S5 introduces it clearly.
- **Risk if kept:** Reader encounters 5 dimension definitions without context.

### Accessibility (51 words)
- **Section 2 needs this now?** No
- **Recommended treatment:** Remove from S2; introduce in S5.3
- **Best later home:** S5.3
- **Reason:** Same as Visibility.

### Representation (68 words)
- **Section 2 needs this now?** No
- **Recommended treatment:** Remove from S2; introduce in S5.4
- **Best later home:** S5.4

### Confidence (116 words — longest definition)
- **Section 2 needs this now?** Partially — the word appears in S1
- **Recommended treatment:** One-sentence guardrail in S2 ("trust in information, not certainty"). Full definition in S5.5.
- **Best later home:** S5.5
- **Reason:** The full definition includes the capitalization convention and hallucination connection, which belong with the dimension explanation.
- **Risk if moved entirely:** Reader confuses Confidence with certainty.
- **Risk if kept in full:** 116 words for one dimension before the architecture is introduced.

### Connectivity (69 words)
- **Section 2 needs this now?** No
- **Recommended treatment:** Remove from S2; introduce in S5.6
- **Best later home:** S5.6

### Attraction (54 words)
- **Section 2 needs this now?** No — not used until S6
- **Recommended treatment:** Remove from S2; introduce in S6.2
- **Best later home:** S6.2
- **Reason:** Part of the motion model. Reader doesn't need this until S6.
- **Risk if moved:** None.
- **Risk if kept:** Reader encounters motion vocabulary before optimizer or topography.

### Investigation (50 words)
- **Section 2 needs this now?** No
- **Recommended treatment:** Remove from S2; introduce in S6.3
- **Best later home:** S6.3

### Sufficiency (78 words)
- **Section 2 needs this now?** Partially — used in S1 ("premature sufficiency")
- **Recommended treatment:** One-sentence guardrail ("when additional information is unlikely to change the action")
- **Best later home:** S6.5 (full development)
- **Reason:** The Simon connection and Confidence/Sufficiency distinction belong in S6.5.
- **Risk if moved entirely:** Reader doesn't understand "premature sufficiency" from S1.
- **Risk if kept in full:** 78 words for a concept not developed until S6.

### Action (54 words)
- **Section 2 needs this now?** No
- **Recommended treatment:** Remove from S2; introduce in S6.6
- **Best later home:** S6.6

### Prediction Error (47 words)
- **Section 2 needs this now?** No — not used until S8
- **Recommended treatment:** Remove from S2; introduce in S8.4
- **Best later home:** S8.4
- **Reason:** Part of the learning model. Reader doesn't need this until S8.

### Learning (79 words)
- **Section 2 needs this now?** Partially — "learning" appears in S1
- **Recommended treatment:** One-sentence guardrail ("evidence-supported model update, not just memory or correction")
- **Best later home:** S8 (full development)
- **Reason:** The full Argyris & Schön connection and reaction/postmortem distinctions belong in S8.

### Premise Stack (77 words)
- **Section 2 needs this now?** No — not used until S8-S9
- **Recommended treatment:** Remove from S2; introduce in S8 or S9
- **Best later home:** S9.3 (Core Learning Payload)

### Model Update Object (72 words)
- **Section 2 needs this now?** No — not used until S9
- **Recommended treatment:** Remove from S2; introduce in S9
- **Best later home:** S9.1

### Discovery (82 words)
- **Section 2 needs this now?** No — not used until S11
- **Recommended treatment:** Remove from S2; introduce in S11
- **Best later home:** S11.1

### Alignment (88 words)
- **Section 2 needs this now?** Partially — used carefully in S1
- **Recommended treatment:** One-sentence guardrail ("used cautiously; system property, not just model property")
- **Best later home:** S16.2 (Implication for Alignment)
- **Reason:** The full discussion of alignment-as-system-property belongs in implications.

### Governance (55 words)
- **Section 2 needs this now?** Partially — appears in S1
- **Recommended treatment:** One-sentence guardrail ("mechanisms that make rules behaviorally effective")
- **Best later home:** S16.5 (Implication for Governance)

### Hallucination (74 words)
- **Section 2 needs this now?** Yes — used in S1, bridges to S7
- **Recommended treatment:** One-sentence guardrail ("production of plausible but unsupported claims; also a reasoning-state failure")
- **Best later home:** S7.1 (full development)
- **Reason:** The full topography connection belongs in S7. S2 needs only the basic definition + the hint that it's more than a factuality problem.

---

## Summary Tables

### Terms that must remain in Section 2 (full definition)

| Term | Words | Reason |
|------|-------|--------|
| Optimizer | 96 | Core abstraction, used immediately |
| Agent | 70 | Distinguished from optimizer |
| Reasoning State | 62 | S3's title depends on it |
| Topography | 63 | Paper's title term |
| Gradient | 94 | Used in S1, needs RL caveat |

**Subtotal: 5 terms, ~385 words**

### Terms that should become one-sentence guardrails

| Term | Current Words | Guardrail Words (~) | Reason |
|------|-------------|-------------------|--------|
| Goal | 54 | ~20 | Full development in S4.1 |
| Policy | 75 | ~20 | Full development in S4.2 |
| Interpretation | 76 | ~20 | Full development in S4.3 |
| Perceived Topography | 54 | ~15 | Emphasis on perception, full in S5 |
| Confidence | 116 | ~20 | Dimension detail in S5.5 |
| Sufficiency | 78 | ~20 | Full development in S6.5 |
| Learning | 79 | ~20 | Full development in S8 |
| Alignment | 88 | ~20 | Full discussion in S16.2 |
| Governance | 55 | ~15 | Full discussion in S16.5 |
| Hallucination | 74 | ~20 | Full development in S7 |
| Information Surface | 66 | ~15 | Full development in S5 |

**Subtotal: 11 terms, currently ~815 words → ~205 words**

### Terms that should be moved to later sections

| Term | Current Words | Move To | Reason |
|------|-------------|---------|--------|
| Visibility | 59 | S5.2 | Dimension — introduced with architecture |
| Accessibility | 51 | S5.3 | Dimension |
| Representation | 68 | S5.4 | Dimension |
| Connectivity | 69 | S5.6 | Dimension |
| Attraction | 54 | S6.2 | Motion — introduced with motion model |
| Investigation | 50 | S6.3 | Motion |
| Action | 54 | S6.6 | Motion |
| Prediction Error | 47 | S8.4 | Learning — introduced with learning model |
| Premise Stack | 77 | S9.3 | Architecture — introduced with MUOs |
| Model Update Object | 72 | S9.1 | Architecture |
| Discovery | 82 | S11.1 | Framework — introduced with discovery loop |

**Subtotal: 11 terms, ~683 words removed from S2**

### Terms that need careful cross-reference later

| Term | S2 Treatment | Where Fully Developed | Cross-Reference Needed? |
|------|-------------|----------------------|----------------------|
| Sufficiency | Guardrail | S6.5 | Yes — S1 uses "premature sufficiency" |
| Hallucination | Guardrail | S7.1 | Yes — S1 introduces the bridge |
| Learning | Guardrail | S8 | Yes — S1 mentions learning |
| Confidence | Guardrail | S5.5 | Yes — S1 uses "confidence signals" |

---

## Proposed New Role for Section 2

**Current role:** Comprehensive glossary (27 terms, ~2,100 words)

**Proposed role:** Language calibration (5 full definitions + 11 guardrails + Summary of Usage, ~700-800 words)

**Structure:**

```
# 2. A Note on Terms

[Intro paragraph about overloaded language — keep as-is]

## Core Abstractions
Optimizer (full)
Agent (full)

## Framework Language
Topography (full)
Gradient (full)
Reasoning State (full)

## Terms Used With Specific Meaning
[One-sentence guardrails for 11 terms, organized in a table or compact list]

## Summary of Usage
[Keep existing summary paragraph — it's effective]
```

**Estimated savings:** ~2,100 → ~700-800 words (~1,300 words saved)

**Where the savings go:** The definitions aren't deleted — they're relocated to the sections where they're first needed, making those sections self-contained.

---

## Decision Needed

This is a significant structural change. Two options:

**Option A: Apply the relocation** — Section 2 becomes ~800 words, terms are introduced where they're needed. More natural reading flow. Risk: some readers may want a glossary.

**Option B: Keep Section 2 as-is but add a note** — Add a sentence at the top: "Readers may wish to skim this section and return to specific definitions as they encounter them in the paper." This preserves the glossary function while acknowledging the dump problem.

**Option C: Hybrid** — Keep all terms in Section 2 but restructure into tiers: "Core terms you need now" (5 full) + "Terms introduced later" (one-line each, with section pointer). This keeps Section 2 as a reference while signaling which terms matter immediately.
