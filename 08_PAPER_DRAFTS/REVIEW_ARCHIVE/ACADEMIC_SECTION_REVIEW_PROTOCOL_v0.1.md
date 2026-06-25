# Academic Section Review Protocol v0.1

**Date:** 2026-06-24
**Status:** Active review protocol for `PAPER_ACADEMIC_v0.1.md`
**Purpose:** Govern how each section of the Path 2 academic manuscript is reviewed before revision.

---

## Design Principle

Staged convergence, not unstructured swarm. Each reviewer applies a specific lens, produces structured notes, and flags risks before revision. The synthesis step decides what to accept, reject, defer, or convert into fault lines.

---

## Review Gates

Each section must pass through five gates:

| Gate | Question |
|---|---|
| **Argument Gate** | Does the section perform its intended argumentative function? |
| **Field Gate** | Is the section positioned correctly against relevant literature? |
| **Construct Gate** | Are definitions and concepts precise, distinct, and useful? |
| **Hostile Gate** | How would a skeptical reviewer attack this section? |
| **Integration Gate** | Does the section preserve the frozen keystone paper and fit the whole manuscript? |

---

## Reviewer Panel

### 1. Argument Architect

Reviews thesis clarity, section purpose, contribution logic, and argumentative sequence. Asks: does the reader know what this section claims, why it matters, and how it connects to what came before and after?

### 2. AI Agents Literature Reviewer

Reviews positioning against LLM agents, reasoning-action loops (ReAct), tool use, memory, planning, reflection, orchestration, and agent benchmarks (AgentBench, WebArena, SWE-bench). Asks: is the framework positioned accurately against what the field already provides?

### 3. HCI / Human-Agent Interaction Reviewer

Reviews human confirmation, mixed-initiative interaction (Horvitz), automation bias (Parasuraman & Riley, Lee & See), affordance theory (Gibson, Norman), and usability of the human-agent framing. Asks: does the Discovery/RIPC pattern hold up as an interaction design contribution?

### 4. AI Safety / Governance Reviewer

Reviews safety claims, policy boundaries, tool-use risk, approval gates, governance design, and overclaim risk. Asks: does the paper responsibly describe what governance can and cannot do? Does it avoid implying that governance automation solves political or institutional problems?

### 5. Organizational Learning Reviewer

Reviews knowledge reuse (Markus), organizational memory (Walsh & Ungson), the distinction between correction and learning (Argyris & Schon), postmortems, and model-update claims. Asks: does the framework genuinely advance beyond "better postmortems" or is it relabeling existing practice?

### 6. Conceptual Rigor Reviewer

Reviews construct clarity, metaphor discipline (is "topography" doing real work or just decoration?), dimensional overlap (do the five dimensions diagnose differently?), and framework sprawl (is the framework trying to explain too much?). Asks: would a philosopher of science accept these constructs as well-formed?

### 7. Methodology / Epistemic Status Reviewer

Reviews whether the paper correctly represents itself as conceptual, pre-empirical, and design-theoretic. Checks the constructed stress test framing. Asks: does the paper make claims its method cannot support? Does it confuse illustration with evidence?

### 8. Hostile Reviewer #2

Attempts to reject the section. Identifies the strongest objections a reviewer at a top venue would raise. Writes the rejection paragraph. Asks: what is the single strongest reason to reject this section?

### 9. Voice Preservation Editor

Ensures academic rigor is gained without losing the distinctive practitioner-builder voice. Checks for committee-paper drift, jargon inflation, and loss of the directness that makes the frozen paper readable. Asks: does this still sound like someone who builds these systems, or does it sound like someone who only reads about them?

### 10. AI Voice Detection Editor

Identifies and flags AI-generated writing patterns that undermine credibility. This review is rigorous and specific.

**Detection targets:**

- Transitional filler ("It is worth noting that...", "This is particularly important because...", "Moreover,...", "Furthermore,...", "Indeed,...")
- Setup-before-the-point sentences (stating what the section will do before doing it)
- Restating the reader's likely thought before responding to it
- Symmetrical parallel structure used decoratively rather than structurally
- Overly balanced hedging ("While X, it is also true that Y") when the author actually has a position
- Adverb overuse ("critically", "fundamentally", "importantly", "notably")
- Empty intensifiers ("deeply", "profoundly", "truly", "significantly")
- Formulaic section transitions ("Having established X, we now turn to Y")
- Patterned lists where each item follows the same grammatical template
- Sentences that sound authoritative but contain no information ("This distinction is central to the framework's contribution")
- Passive constructions that hide agency ("It can be observed that..." instead of stating the observation)
- Diplomatic qualifiers that weaken claims the author actually means ("It might be suggested that..." when the author is making the suggestion)

**Voice model:** The target voice is Benet's — direct, opinionated, practitioner-grounded, willing to make strong claims and then bound them honestly. Not diplomatic. Not hedged. Not committee-polished. The author has built these systems and has opinions about what works and what does not. The academic version should gain citation discipline and structural rigor without losing that.

**Reference for AI pattern detection:** Martin Vejmelka flagged AI patterns in Benet's prior email drafts (see memory: `feedback_voice_ai_detection.md`). The same detection discipline applies here. Transitional filler, setup-before-point, and restating-their-words patterns should be flagged and removed.

**Scoring note:** AI Voice Detection scores on Voice Quality. Any sentence flagged as AI-pattern must be rewritten or cut. The standard is not "does it sound okay" — the standard is "would a careful reader suspect this was AI-generated?"

### 11. Citation Auditor

Identifies claims requiring citations, missing literature, weak support, and citation backlog gaps. Checks that existing citations are correctly attributed and that original synthesis is not accidentally attributed to prior work.

---

## Section Reviewer Assignments

| Section | Required Reviewers |
|---|---|
| 1. Introduction | Argument Architect, Hostile Reviewer #2, Voice Preservation Editor, AI Voice Detection Editor |
| 2. Related Work | AI Agents Lit Reviewer, HCI Reviewer, AI Safety Reviewer, Org Learning Reviewer, Citation Auditor |
| 3. From Context to Reasoning State | Conceptual Rigor Reviewer, Org Learning Reviewer, Hostile Reviewer #2, AI Voice Detection Editor |
| 4. Definitions and Dimensions | Conceptual Rigor Reviewer, HCI Reviewer, Argument Architect |
| 5. Gradients, Motion, Premature Sufficiency | Conceptual Rigor Reviewer, AI Safety Reviewer, Hostile Reviewer #2 |
| 6. Reasoning-State Architecture | AI Agents Lit Reviewer, Org Learning Reviewer, Integration Gate |
| 7. Discovery and Human Confirmation | HCI Reviewer, AI Safety Reviewer, Voice Preservation Editor, AI Voice Detection Editor |
| 8. Constructed Stress Test | Methodology Reviewer, Hostile Reviewer #2, Integration Gate |
| 9. Boundaries, Objections, Disconfirmation | Hostile Reviewer #2, Methodology Reviewer, Conceptual Rigor Reviewer |
| 10. Research Agenda | Methodology Reviewer, AI Agents Lit Reviewer, Citation Auditor |
| 11. Conclusion | Argument Architect, Voice Preservation Editor, AI Voice Detection Editor, Integration Gate |

---

## Scoring Rubric

Each reviewer scores the section from 1 to 5 on relevant criteria:

| Score | Meaning |
|---|---|
| **5** | Strong, manuscript-ready |
| **4** | Usable with minor revision |
| **3** | Promising but needs revision |
| **2** | Structurally weak |
| **1** | Not acceptable in current form |

**Criteria:**

1. **Purpose Fit** — Does the section do what it is supposed to do in the manuscript?
2. **Argument Clarity** — Is the claim clear, bounded, and logically sequenced?
3. **Construct Discipline** — Are concepts precise, distinct, and earning their place?
4. **Academic Positioning** — Is the section correctly positioned against relevant literature?
5. **Overclaim Control** — Does the section claim only what its method supports?
6. **Reviewer Resistance** — Would this survive a hostile review at a top venue?
7. **Voice Quality** — Does the section sound like a practitioner-builder, not a committee? Is it free of AI-generated writing patterns?
8. **Keystone Fidelity** — Does the section preserve the frozen paper's concepts without silent alteration?
9. **Citation Readiness** — Are claims supported, citations present or backlogged, and original synthesis correctly identified?

**Thresholds:**

- Any criterion below **4** requires a revision note.
- Any criterion below **3** requires section-level rework.
- **Voice Quality below 4** triggers mandatory AI Voice Detection Editor re-review after revision.

---

## Required Reviewer Output Format

```markdown
## Reviewer: [Role Name]

### Section Reviewed
[Section number and title]

### Verdict
Pass / Revise / Reject

### Scores

| Criterion | Score | Note |
|---|---:|---|
| Purpose Fit | | |
| Argument Clarity | | |
| Construct Discipline | | |
| Academic Positioning | | |
| Overclaim Control | | |
| Reviewer Resistance | | |
| Voice Quality | | |
| Keystone Fidelity | | |
| Citation Readiness | | |

### Top Strengths

1.
2.
3.

### Top Risks

1.
2.
3.

### Required Changes

1.
2.
3.

### Optional Improvements

1.
2.
3.

### Citation Needs

-

### AI Voice Flags (if applicable)

- [Quote the flagged sentence]
- [Pattern identified: e.g., "transitional filler", "setup-before-point", "empty intensifier"]
- [Suggested fix or "cut"]

### Conceptual Conflict Warnings

-
```

---

## Synthesis Protocol

After all assigned reviewers complete their notes for a section:

1. **Collect** all reviewer notes.
2. **Identify convergence** — where multiple reviewers flag the same issue.
3. **Identify conflicts** — where reviewers disagree.
4. **Decide** for each flagged item: accept, reject, defer, or convert to fault line.
5. **Produce a synthesis memo** listing accepted changes, rejected suggestions with reason, deferred items, and any new fault lines.
6. **Revise the section** based on the synthesis memo.
7. **Re-run Voice Quality and AI Voice Detection** on the revised section if either scored below 4.

---

## Frozen Keystone Rule

The frozen paper (`PAPER_v1.0_WORKING.md`) remains the conceptual authority.

If a reviewer identifies a conflict between the academic draft and the frozen keystone paper, do not silently resolve it in prose. Mark it as a potential fault line under Protocol #1 and file in `04_FAULT_LINES/`.

---

## Review Discipline

- Reviewers diagnose, score, and identify required changes. They do not rewrite unless explicitly asked.
- Reviewers should flag the specific sentence or paragraph, not make vague complaints.
- Reviewers should distinguish "I disagree with the claim" from "the claim is poorly supported."
- The AI Voice Detection Editor should quote the flagged text and name the pattern.

---

## Goal

The goal is not more notes.

The goal is a publishable academic manuscript that is rigorous, defensible, readable, and still recognizably authored by someone who understands how these systems are actually built.

---

## No-Edit Confirmation

- Frozen paper edited: **No**
- Figure 8 modified: **No**
- Figures modified: **No**
- References modified: **No**
- Academic scaffold edited: **No** (this protocol governs review of the scaffold's future drafts)
- HLD v1.0 edited: **No**
