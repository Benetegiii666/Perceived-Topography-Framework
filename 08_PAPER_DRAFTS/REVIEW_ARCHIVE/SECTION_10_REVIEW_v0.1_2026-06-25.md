# Section 10 Review (v0.1) — 2026-06-25

**Section:** 10. Research Agenda and Evaluation Methods
**Draft:** ChatGPT v0.1
**Reviewers:** Methodology, Conceptual Rigor, AI Safety, Org Learning, Integration, Voice Preservation, AI Voice Detection, Citation Auditor
**Verdict:** Minor Revision

---

## Pass Criteria

| Criterion | Result | Met? |
|---|---|---|
| Voice Quality >= 4 | 4 (all 8 reviewers) | YES |
| No severe AI flags | 0 severe, 2 minor | YES |
| Research agenda concrete/actionable | Six families, seven RQs, two rubrics | YES |
| Avoids pretending framework is validated | Negative-result language in every subsection | YES |
| Context-only baseline fair | Fair intent but underspecified | PARTIAL |
| Maturity model provisional | "Not a ladder" framing present | YES |
| Bridges S9→S11 | Clean | YES |
| No conceptual conflict | None | YES |
| Negative results valued | 10.9 + throughout | YES |

---

## Required Changes (7 items)

**1. Add positioning paragraph against existing agent benchmarks.** The section proposes evaluation methods but never says how they relate to or depart from AgentBench, SWE-bench, WebArena, GAIA. A methodology reviewer needs this.

**2. Sharpen context-only baseline definition.** Systems like Reflexion already preserve structured feedback loops. "Context-only" must be defined sharply — what exactly is being varied? Acknowledge that the comparator is not always pure retrieval. Two reviewers converge.

**3. Define or cross-reference "required pre-action surfaces."** Used in 10.3 but not formally defined. Either define it or add a parenthetical to S5/S6 where the concept draws from.

**4. Acknowledge Argyris single-loop / double-loop / deutero-learning parallel in maturity model.** Levels 3-5 recapitulate this progression. State what PTF's version adds: reasoning-state granularity, architectural specificity, fit-based rather than developmental.

**5. Add brief adversarial evaluation scoping for RQ7** — even 2-3 sentences noting that RQ7 requires its own methodology, or add a brief subsection. Currently RQ7 has no evaluation subsection while RQ1-6 all do.

**6. Fix 2 AI voice flags:**
- Cut "The useful research program is plural rather than grand" — decorative aphorism with no information content
- Rewrite "Together, these methods ask whether the vocabulary changes diagnosis, whether architecture changes behavior, and whether preserved reasoning improves future action" — symmetrical AI tricolon

**7. Add high-priority citations:** Peffers et al. 2007 (design science methodology), Shinn et al. 2023 or Yao et al. 2023 (structured-state systems as baseline comparators), March 1991 (exploration/exploitation for premature/over-delayed sufficiency distinction).

---

## What Works (preserve)

- "A framework that can lose needs methods that can make it lose" — opening
- Four-outcome sufficiency classification (appropriate, premature, over-delayed, blocked)
- MUO quality rubric (specificity, evidence, boundary, confidence, future-state, contestability)
- Table 8 maturity model — provisional, fit-based, six levels
- RQ7 as first-class research question
- Negative results valued throughout
- Instrumentation without surveillance governance
- "A useful framework does not need to win everywhere" — closing

---

## Recommendation

Minor revision. Seven changes, all additive. No structural rework. After revision, re-run AI Voice Detection only.
