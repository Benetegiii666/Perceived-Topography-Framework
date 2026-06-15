# v0.2 Reviewer-Agent Packet

## Purpose

This packet defines several reviewer roles for evaluating `PAPER_v0.2.md`. Each reviewer is assigned a different reader lens. The goal is to identify clarity gaps, credibility issues, overreach, missing examples, weak transitions, and usefulness problems before v1.0 planning.

The reviewer agents should not rewrite the manuscript. They should diagnose how the paper lands.

---

## Shared Instructions for All Reviewers

Each reviewer should read the paper as a serious but fresh reader.

Each reviewer must answer:

1. What do you think the central claim is?
2. Where does the paper become clearest?
3. Where does the paper become hardest to follow?
4. Which concept feels most useful?
5. Which concept feels least justified?
6. Where does the paper feel overextended?
7. Where does it need more evidence, citation, or example?
8. Does Appendix A make the framework more actionable?
9. What is the strongest objection to the paper?
10. What are the top 3 changes that would most improve v1.0?

Each reviewer should distinguish between:

* **Blocking issues** — problems that undermine the paper's core argument or credibility
* **Important but non-blocking issues** — problems that weaken the paper but do not break it
* **Optional polish** — improvements that would help but are not necessary
* **Future-work suggestions** — ideas that belong in a later version, not this one

---

## Reviewer Agent 1: Cold Intelligent Reader

### Mission

Evaluate whether an intelligent reader with no prior exposure to the project can understand the paper.

### Reader Profile

Smart, curious, interdisciplinary, but not already invested in AI alignment, organizational theory, or the framework.

### Primary Questions

* Can the reader state the thesis back accurately?
* Does the argument unfold naturally?
* Are the terms introduced at the right time?
* Does the paper feel too abstract before it becomes useful?
* Does the conclusion land?

### Failure Mode to Detect

The paper makes sense only to people who were present during its development.

---

## Reviewer Agent 2: AI / Agent Systems Reviewer

### Mission

Evaluate whether the paper's AI, agent, retrieval, grounding, hallucination, learning, and safety claims are credible.

### Reader Profile

Technically literate in LLMs, agents, RAG, AI safety, grounding, tool use, and evaluation.

### Primary Questions

* Does the paper accurately distinguish context, retrieval, reasoning state, and learning?
* Does the hallucination / harmful action / premature sufficiency framing hold up?
* Does the paper overstate what current AI systems can preserve or learn?
* Are the citations and related-work connections credible?
* Are any technical claims too broad?

### Failure Mode to Detect

The paper sounds compelling but is technically loose, overgeneralized, or not grounded enough in current AI practice.

---

## Reviewer Agent 3: Product / Organizational Systems Reviewer

### Mission

Evaluate whether the framework helps a real organization design better workflows, tools, governance, or AI-enabled systems.

### Reader Profile

Senior product leader, enterprise architect, operations leader, transformation leader, or systems designer.

### Primary Questions

* Does the framework translate into practical design decisions?
* Does the campaign example make the theory usable?
* Does Appendix A provide a realistic starting point?
* Does "preserving reasoning" feel operationally meaningful?
* What would a product team actually do differently after reading this?

### Failure Mode to Detect

The paper is intellectually interesting but not actionable.

---

## Reviewer Agent 4: Academic / Theory Reviewer

### Mission

Evaluate the paper's theoretical discipline, claim scope, conceptual clarity, and relationship to prior work.

### Reader Profile

Academic or research-minded reviewer familiar with systems theory, organizational learning, decision theory, cognitive science, or AI alignment.

### Primary Questions

* Are the paper's claims scoped carefully?
* Does it overclaim originality?
* Does the synthesis of prior traditions feel intellectually honest?
* Are the definitions stable?
* Are the boundaries and falsifiability sections strong enough?
* Does Section 15 properly position the work?

### Failure Mode to Detect

The paper sounds novel by under-crediting prior traditions or fails to define its contribution precisely.

---

## Reviewer Agent 5: Skeptical Practitioner

### Mission

Evaluate whether the paper avoids sounding like abstract consulting language.

### Reader Profile

Experienced practitioner who is allergic to jargon, frameworks-for-frameworks' sake, and elegant diagrams that do not change behavior.

### Primary Questions

* What parts feel real?
* What parts sound too clever?
* What would you actually use?
* Where does the paper need a concrete example?
* Does Appendix A rescue the paper from abstraction?
* What sentence would make you roll your eyes?

### Failure Mode to Detect

The paper is persuasive to theorists but loses practical readers.

---

## Reviewer Agent 6: Evidence and Citation Auditor

### Mission

Evaluate whether the paper's evidentiary support is strong enough for its claims.

### Reader Profile

Detail-oriented reviewer focused on citations, sourcing, intellectual lineage, and unsupported assertions.

### Primary Questions

* Which claims need stronger citation support?
* Are any citations doing too much work?
* Are there places where the paper should soften a claim?
* Are the related-work references appropriate?
* Are any major traditions or obvious sources missing?
* Are there citation clusters that feel ornamental rather than functional?

### Failure Mode to Detect

The paper's argument is strong but citation support is uneven or vulnerable to critique.

---

## Required Output Format for Each Reviewer

Each reviewer must produce:

```markdown
# Review Report: [Reviewer Agent Name]

## Thesis Playback

State the paper's central claim in your own words.

## What Works

## Where the Paper Loses the Reader

## Strongest Contribution

## Weakest or Least-Supported Claim

## Usefulness Assessment

## Appendix A Assessment

## Credibility / Evidence Assessment

## Strongest Objection

## Recommended Changes for v1.0

### Blocking

### Important but Non-Blocking

### Optional Polish

### Future Work

## One-Sentence Verdict
```

---

## Meta-Synthesis Prompt

After all reviewer reports are generated, synthesize them into one decision memo:

```markdown
# v0.2 Review Synthesis Memo

## Cross-Reviewer Summary

## Issues Repeated Across Multiple Reviewers

## Issues Raised by Only One Reviewer but Worth Considering

## Conflicting Reviewer Feedback

## Recommended v1.0 Priorities

## Do Not Change List

## Candidate v0.3 / v1.0 Workstreams

## Final Recommendation
```

---

## No-Edit Rule

Reviewer agents may recommend edits, but they may not directly rewrite or modify the manuscript. All reviewer output goes into review reports, not into the paper files.
