# Full Question Bank — Internal Reference

**This full question bank is for Benet's internal preparation and later discovery passes. Do not use the entire bank in the first stakeholder conversation.**

*Source: `COMPANION_ARTIFACTS/BUILD_DISCOVERY_GUIDE_v1.0.md` — all 13 categories, 130 questions.*

The first live conversation should use `04_DISCOVERY_QUESTIONNAIRE.md` (a smaller conversational subset focused on Categories 1-3 plus assumptions, claims, sufficiency, and learning). This full bank is the reference for deeper follow-up passes.

---

## Category 1: Workflow Boundary

*Purpose: Define the repeated decision workflow the first build will target.*

1. What repeated work are we trying to improve?
2. What event starts this workflow?
3. What output ends the workflow?
4. Who produces the output, and who consumes it?
5. What goes wrong often enough to justify system design?
6. What does "better" mean for this workflow?
7. What should the first build include?
8. What should the first build intentionally exclude?
9. What evidence would show the next cycle got smarter?

---

## Category 2: Campaign Brief Structure

*Purpose: Discover the structure of the campaign brief — the decision artifact.*

1. What decision or action does this brief enable?
2. What sections must exist before work can begin?
3. Which sections are factual, which are strategic, and which are evidence-dependent?
4. Which sections require policy, legal, clinical, compliance, or brand review?
5. Which parts are usually copied forward without being rethought?
6. Which parts are most often vague but still treated as good enough?
7. What must the AI know before it begins drafting?
8. What should make the system pause before drafting?
9. What would make a brief unsafe, misleading, low-quality, or unusable?
10. What does a strong campaign brief make easier for downstream work?

---

## Category 3: KB / Information Surfaces

*Purpose: Discover what the system must be able to see, retrieve, trust, cite, compare, or ignore.*

1. What source materials do people actually rely on today?
2. Which sources are authoritative — meaning the system should treat them as governing?
3. Which sources are outdated but still being reused?
4. What knowledge categories exist today, and what is missing?
5. What knowledge should be structured before it enters the system?
6. What should be searchable, and what should be filterable?
7. What should the system cite when it drafts?
8. What should never be treated as a source of truth?
9. What needs an owner, and what needs a review cadence?
10. What metadata would make retrieval safer or more useful?

---

## Category 4: Trust, Evidence, and Confidence

*Purpose: Map what the team trusts, doubts, argues about, and treats as evidence.*

1. What sources does the team trust most, and why?
2. What sources does the team use but not fully trust?
3. What evidence is required before a claim can be used in output?
4. What signals are useful but should not be treated as authoritative?
5. Where do people disagree about what evidence means?
6. How should the system show confidence to the human reviewer?
7. What should lower the system's confidence in a piece of content?
8. What should happen when trusted sources disagree with each other?
9. What evidence should be visible to the human reviewer at decision time?
10. How should evidence standards differ by content type?

---

## Category 5: Assumptions / Premises

*Purpose: Surface working beliefs that shape the decision.*

1. What are we acting as though we already know?
2. Which assumptions shape this brief or workflow right now?
3. Which assumptions came from evidence, and which from experience or convention?
4. Which assumptions are copied from prior work without being re-examined?
5. Which assumptions are risky if wrong?
6. Which assumptions should be tested before the team acts on them?
7. Which assumptions should be preserved into the next cycle?
8. Which assumptions should expire or be rechecked on a schedule?
9. What would change if a key assumption turned out to be false?
10. Who stated or confirmed each key assumption?

---

## Category 6: Policy / Governance Boundaries

*Purpose: Shape gradients away from unsafe, non-compliant, or unsupported claims.*

1. What claims require approved evidence before the system can use them?
2. What language is approved, preferred, discouraged, or prohibited?
3. Which rules are hard constraints versus guidance?
4. Who can approve exceptions?
5. What must the system never say without supporting evidence?
6. What should be flagged but not blocked?
7. What should be blocked until reviewed?
8. What needs citation or provenance after the fact?
9. What creates the most risk if the system gets it wrong?
10. What governance exists today that the system should inherit?

---

## Category 7: Sufficiency and Stopping Conditions

*Purpose: Define when the system can act or must pause.*

1. What makes a draft or decision feel "good enough" today?
2. Where does the team move too fast and regret it later?
3. What information must be present before the system acts?
4. What uncertainty should force a pause?
5. What evidence gap should block action entirely?
6. What should trigger a human review?
7. What should the system ask before continuing?
8. What should the system refuse to complete?
9. What are the signs that fluency is being mistaken for evidence?
10. What does "sufficient to proceed" mean for each major field or step?

---

## Category 8: Reasoning to Preserve

*Purpose: Keep "why" from disappearing between cycles.*

1. What should someone understand later about why this decision was made?
2. What goal shaped this decision?
3. What constraints shaped the decision?
4. What assumptions shaped the decision?
5. What evidence was checked before the decision was made?
6. What evidence was missing or unavailable?
7. What alternatives were considered or rejected?
8. What made the answer feel sufficient?
9. What human judgment changed the system's interpretation or output?
10. What should be available to the next cycle that is not available today?

---

## Category 9: Learning Loop

*Purpose: Make the next run smarter.*

1. What outcome data matters for this workflow?
2. What result would tell us an assumption was wrong?
3. What did the team expect to happen?
4. What actually happened, and how does it compare to the prediction?
5. What should change next time based on what happened?
6. What should NOT be generalized beyond this case?
7. Who confirms that the lesson is valid before it enters the system?
8. Where should the confirmed lesson live in the system?
9. How does the lesson reach the next cycle?
10. How will we know the next cycle actually started smarter?

---

## Category 10: Retrieval Relevance

*Purpose: Retrieve prior reasoning, not just similar text.*

1. What prior decisions should be retrievable for this workflow?
2. What makes a prior decision relevant to a current decision?
3. What metadata is needed to retrieve prior reasoning safely?
4. What applicability boundaries should travel with prior reasoning?
5. What would make a prior lesson not apply to the current decision?
6. What should the system show when it retrieves prior reasoning?
7. How should the system explain why it retrieved something?
8. What should happen when no relevant prior reasoning is found?
9. What should happen when retrieved reasoning is similar but not applicable?
10. What should the human confirm before prior reasoning is reused?

---

## Category 11: Human Confirmation

*Purpose: Keep humans in the correction loop.*

1. Where should the system ask for human confirmation?
2. What exactly should the human be confirming?
3. What should the human be able to correct, reject, or bound?
4. What should be recorded when a human confirms?
5. What should happen after a correction?
6. What should happen after an override?
7. Where is confirmation likely to become rubber-stamping?
8. How should the system make review meaningful without slowing everything down?
9. What confirmation points are essential versus optional?
10. Who has authority for which types of confirmation?

---

## Category 12: Ownership / Lifecycle

*Purpose: Keep knowledge current and governed.*

1. Who owns each knowledge category?
2. Who owns each policy or rule?
3. Who approves learning updates?
4. How often should each source be reviewed?
5. What makes a source stale?
6. What happens when a source expires?
7. What should be archived, deprecated, or retained?
8. Who is accountable when the system uses stale or wrong knowledge?
9. What lifecycle states does the team need?
10. How should handoffs work when ownership changes?

---

## Category 13: Build Translation

*Purpose: Turn all discovery answers into build inputs.*

1. What build inputs have we produced from each category?
2. Which answers become data objects?
3. Which answers become metadata fields?
4. Which answers become governance rules?
5. Which answers become retrieval rules?
6. Which answers become UI/review workflow requirements?
7. Which answers become sufficiency gates?
8. Which answers become reasoning-state objects?
9. Which answers become learning-loop requirements?
10. What is the smallest useful build from these inputs?
