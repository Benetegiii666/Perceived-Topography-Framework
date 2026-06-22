# Build Discovery Guide v0.4 QA Review

**Date:** 2026-06-22
**Artifact reviewed:** `COMPANION_ARTIFACTS/BUILD_DISCOVERY_GUIDE_v0.4.md`
**Source paper:** `PAPER_v1.0_WORKING.md` (frozen)
**Artifact edited:** No.
**Manuscript edited:** No.

---

## QA Status: PASS

The Build Discovery Guide v0.4 is ready to be promoted to v1.0.

---

## Structural Completeness

| Check | Result |
| --- | --- |
| All 13 categories fully drafted | Yes — zero placeholders remain |
| Total line count | 2,201 lines |
| Front matter sections present | Yes (What This Guide Is, What It Is Not, Keystone relation, Appendix A relation, Executive Brief relation, HLD relation, Design Rule) |
| Category Map table present | Yes — 13-row table with all four columns |
| Design Rule stated | Yes — "Every Question Must Have a Build Target" |
| Both appendices present | Yes (HLD Inputs, Case-Study Observations) |
| Draft status note present | Yes — correct v0.4 text |

## Pattern Compliance

All 13 categories follow the required 9-section pattern:

| Section | Present in all 13 categories |
| --- | --- |
| Purpose | Yes |
| Build output produced | Yes |
| Core questions | Yes |
| Follow-up probes | Yes |
| What good answers contain | Yes |
| What weak answers look like | Yes |
| What this informs in the system | Yes |
| What this feeds in the HLD | Yes |
| Case-study observations to preserve | Yes |

## Question Pattern Compliance

All core questions across all 13 categories follow the required three-part pattern:

- "Ask this because…" — present in every question
- "Listen for:" — present in every question
- "This becomes:" — present in every question

## Build Target Compliance

Every question produces at least one build target from the required list:

- Campaign brief structure: Q2.1–Q2.10
- KB structure: Q3.1–Q3.10
- Metadata field: Q3.5, Q3.6, Q3.10, Q4.3, Q10.3, Q12.4, Q13.3
- Reasoning object: Q5.1–Q5.10, Q8.1–Q8.10, Q13.8
- Governance rule: Q6.1–Q6.10, Q7.5, Q13.4
- Retrieval rule: Q10.1–Q10.10, Q13.5
- Confidence/provenance requirement: Q4.1–Q4.10, Q10.6
- Lifecycle requirement: Q12.1–Q12.10, Q13.9
- HLD input: Q13.1–Q13.10 (all)
- Future case-study observation: Each category's observation section

No question exists without a build target.

## Final Four Categories — Specific Review

### Category 10: Retrieval Relevance

- **Correctly distinguishes reasoning-relevant retrieval from semantic search:** Yes. The purpose statement opens with "Reasoning-relevant retrieval is not the same as semantic document retrieval" and Q10.2 explicitly states "relevance is not similarity."
- **Covers applicability boundaries:** Yes (Q10.4, Q10.5)
- **Covers false-analogy prevention:** Yes (Q10.9)
- **Covers match-rationale display:** Yes (Q10.6, Q10.7)
- **Covers retrieval miss/gap logging:** Yes (Q10.8)
- **Covers reuse confirmation (RIPC Confirm for retrieval):** Yes (Q10.10)
- **HLD feed-through:** Section 6 (retrieval), Section 5 (RIPC), Section 14 (risks). Correct.

### Category 11: Human Confirmation

- **Operationalizes RIPC Confirm step:** Yes. Purpose statement names RIPC and places Confirm at the end of each reasoning cycle.
- **Addresses confirmation fatigue explicitly:** Yes (Q11.7, Q11.8). Identifies rubber-stamping as the operational enemy.
- **Covers correction propagation:** Yes (Q11.5). States corrections must propagate, not just be logged.
- **Covers override logic with scope rules:** Yes (Q11.6). Overrides are bounded to specific instances unless explicitly promoted.
- **Covers tiered confirmation (essential/recommended/optional):** Yes (Q11.9).
- **Covers authority mapping:** Yes (Q11.10).
- **HLD feed-through:** Section 5 (RIPC), Section 10 (governance), Section 14 (risks). Correct.

### Category 12: Ownership / Lifecycle

- **Goes beyond review cadence:** Yes. Covers ownership per category and reasoning object, lifecycle states (draft/provisional/validated/deprecated/superseded/archived), staleness detection (time-based and event-based), deprecation vs. deletion, archival/retention, accountability, and ownership transfer.
- **Covers ownership-transfer handoffs:** Yes (Q12.10). Addresses the "someone leaves" scenario.
- **Covers accountability when stale knowledge produces bad output:** Yes (Q12.8).
- **Covers lifecycle states with transition rules:** Yes (Q12.9).
- **HLD feed-through:** Section 8 (lifecycle), Section 10 (governance), Section 12 (volume management). Correct.

### Category 13: Build Translation

- **Does not draft the HLD:** Correct. It produces an HLD input packet, not architecture.
- **Includes BUILD TRANSLATION TABLE:** Yes. 12-row table mapping all discovery categories to system components, HLD sections, MVP priority, and future phases.
- **MVP priority is well-distributed:** Yes. High: Categories 1, 2, 3, 6, 7, 8, 11. Medium: Categories 4, 5, 9, 10, 12. This is a reasonable prioritization — the core workflow, brief structure, KB, governance, sufficiency, reasoning preservation, and human confirmation are MVP; trust calibration, premise tracking, learning automation, retrieval sophistication, and full lifecycle management are second-phase.
- **HLD feed-through:** All sections. Correct — this is the architecture-landing summary.

## Guide Character

| Check | Result |
| --- | --- |
| Remains a build-discovery instrument | Yes |
| Not a generic facilitator workbook | Yes — no session agendas, room setup, or facilitation theory |
| Not a calendar plan | Yes — no Day 1/Week 1 framing |
| Not a research instrument | Yes — case-study observations are captured as byproducts, not primary purpose |
| Not a RapidSOS-specific artifact | Yes — examples reference brand voice, ICPs, competitive intel, campaign analytics, healthcare/K-12/enterprise verticals generically |
| RapidSOS used as practical grounding | Yes — examples are concrete enough to be useful without being specific to one organization |

## Keystone → Companion → Build → Academic Flow

The guide correctly positions itself within the two-track strategy:

- References the keystone paper as the conceptual foundation
- References Appendix A as the conceptual seed
- References the Executive Brief as the leadership-facing entry point
- References the HLD as the downstream consumer of its outputs
- Preserves case-study observations for the future academic path
- Does not collapse the build path into the academic path

## Required Fixes Before v1.0

**None.**

## Optional Polish (Should Not Block v1.0)

| # | Item | Location | Type |
| --- | --- | --- | --- |
| 1 | Category 13 Q13.1 "Listen for" says "This is an internal review question, not a stakeholder interview question" — this is accurate but breaks the Listen-for pattern slightly. Consider rephrasing as "Listen for: the facilitator's own review of discovery records" or simply noting this is a builder-facing step. | Q13.1, line ~2016 | Cosmetic |
| 2 | Category 13 Q13.10 "Listen for" similarly breaks pattern with "This is a scoping decision, not a discovery question." Same recommendation. | Q13.10, line ~2088 | Cosmetic |
| 3 | The BUILD TRANSLATION TABLE uses pipe-separated columns that may render poorly in some markdown viewers due to long cell content. Consider whether the table should be simplified for readability. | Line ~2094 | Cosmetic |

These are minor cosmetic items. None affects the guide's usability, accuracy, or completeness.

## Frozen Artifact Confirmation

- `PAPER_v1.0_WORKING.md`: Untouched
- `COMPANION_ARTIFACTS/EXECUTIVE_BRIEF_v1.0.md`: Untouched
- Figures: Untouched
- Figure 8: Untouched
- References: Untouched
- Freeze records: Untouched
- Prior review packets: Untouched

## Verdict

**`BUILD_DISCOVERY_GUIDE_v0.4.md` is ready to be promoted to `BUILD_DISCOVERY_GUIDE_v1.0.md`.**

No required fixes. Three optional cosmetic items that should not block promotion.

## Recommended Next Action

Create `COMPANION_ARTIFACTS/BUILD_DISCOVERY_GUIDE_v1.0.md` by copying v0.4 and updating the draft status note to:

```
*Status: v1.0 companion artifact. All thirteen build-discovery categories are fully drafted. Derived from PAPER_v1.0_WORKING.md, the accepted Executive Brief, the Keystone / Two-Track Strategy note, and prior Build Discovery Guide drafts. Not a replacement for the full paper or the HLD.*
```

Then commit all companion artifacts (Executive Brief v0.1, v0.2, v1.0; Build Discovery Guide v0.1–v0.4, v1.0) and push.
