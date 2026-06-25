# Section 7 Review (v0.1) — 2026-06-25

**Section:** 7. Discovery and Human Confirmation
**Draft:** ChatGPT v0.1
**Reviewers:** HCI, AI Safety, Voice Preservation, AI Voice Detection, Conceptual Rigor, Integration, Citation Auditor
**Verdict:** Minor Revision

---

## Pass Criteria

| Criterion | Result | Met? |
|---|---|---|
| Voice Quality >= 4 | Voice Preservation: 4/5. AI Voice Detection: 3.5/5 (6 flags, 2 moderate) | BORDERLINE — triggers mandatory re-review |
| No severe AI flags | 0 severe, 2 moderate, 4 minor | YES |
| RIPC operational | Steps clear; "Propose" criteria and "material uncertainty" filtering need sharpening | PARTIAL |
| Discovery as governance mechanism | Yes — five failure modes, scoped confirmation, provenance | YES |
| Confirmation bounded | Yes — "evidence within scope" | YES |
| No conceptual conflict | None | YES |
| Bridges S6→S8 | S6 bridge clean; S8 bridge is formulaic preview | PARTIAL |

---

## Required Changes (7 items)

**1. Rewrite the closing paragraph.** Cut the formulaic S8 preview. End on the design test ("Did the system make the important inference reviewable before acting from it?") or adapt the frozen paper's "Discovery gives architecture something worth carrying. Architecture gives Discovery somewhere durable to go." Four reviewers converge.

**2. Restore from frozen paper:** "Discovery is not better intake. It is pre-action topography design." This is the sentence that prevents RIPC from collapsing into "ask clarifying questions." Two reviewers converge.

**3. Fix 6 AI voice flags.** Two moderate (setup-before-point in mixed-initiative paragraph; formulaic closing transition). Four minor ("X also does Y" connector; "These risks matter because..."; "The exact wording will vary..."; "The key is that..."). See AI Voice Detection review for specific fixes.

**4. Cite Amershi et al. 2019** in the mixed-initiative or automation-bias paragraph. Already in bibliography. Two reviewers converge.

**5. Add forward reference to S9** after the Discovery failure list. One sentence: "Section 9 examines these risks further." Two reviewers converge.

**6. Acknowledge that material-uncertainty filtering is itself a design problem,** not a solved input. One sentence. Two reviewers converge.

**7. Add one sentence on anchoring risk:** the propose step can itself anchor the human toward the system's frame, which is a known limitation of propose-then-confirm patterns.

---

## AI Voice Flags (6 total: 2 moderate, 4 minor)

| # | Pattern | Severity | Fix |
|---|---|---|---|
| 1 | "This connects Discovery to mixed-initiative interaction." — setup-before-point | Moderate | Merge or cut |
| 2 | Closing paragraph — formulaic section preview | Moderate | Rewrite/cut |
| 3 | "Discovery also protects against automation bias." — weak "also" connector | Minor | Lead with the claim directly |
| 4 | "These risks matter because Discovery is not inherently good." — restating reader's thought | Minor | Cut or rephrase |
| 5 | "The exact wording will vary by domain and interface." — diplomatic qualifier | Minor | Cut |
| 6 | "The key is that Discovery should focus on material uncertainty." — filler opener | Minor | Cut "The key is that" |

---

## What Works (preserve)

- "The risk is not that the system infers. The risk is that it preserves or acts from the inference as if it had been confirmed."
- "The workflow has converted guesswork into architecture."
- "Human confirmation is not magic. It is evidence within scope."
- "A confirmation without scope can become a new source of premature sufficiency."
- Blank-form burden vs. silent inference as named failure pair
- Five Discovery failure modes (performative, manipulative, burdensome, brittle, unsafe)
- Healthcare example as proposed Optimizer State
- RIPC loop structure
- "Did the system make the important inference reviewable before acting from it?" as design test

---

## Recommendation

Minor revision. Seven changes, all sentence-level. No structural rework. After revision, re-run AI Voice Detection. Target: Voice 4/5, 0 moderate flags.
