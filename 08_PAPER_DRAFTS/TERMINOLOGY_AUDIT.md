# PAPER_DRAFT Terminology Discipline Audit

**Date:** 2026-06-12
**Auditor:** Claude
**Method:** Full-text search, frequency analysis, synonym-drift detection, definition-location mapping

---

## 1. Terms Used Consistently

The following terms are used with disciplined consistency throughout the paper:

| Term | Occurrences | Notes |
|------|------------|-------|
| Optimizer State | ~53 | Always means Goal + Policy + Interpretation. Never confused with Decision State. |
| Premise Stack | ~45 | Consistently means artifact-backed basis for prior expectations. |
| Prediction Error | ~57 | Always means mismatch between expected and observed outcome. |
| Model Update Object | 77 (capitalized) | Consistently capitalized. Zero lowercase instances of "model update object." |
| Sufficiency | ~96 | Clearly distinguished from Confidence throughout. |
| Decision State | ~27 | Always refers to the reasoning-architecture object, never confused with Optimizer State. |
| Investigation Trace | ~23 | Consistent usage. |
| Learning Event | ~22 | Consistent usage. |
| Discovery Pattern Update | ~5 | Consistent usage where it appears. |
| Information Topography | ~30 | Consistently refers to the five-dimension perceived environment. |
| Perceived Topography | ~30 | Consistently emphasizes the optimizer acts on perception, not reality. |
| Action Model | ~14 | Consistently identified as an Interpretation subtype, not a fourth primitive. Explicitly defended in 4.3, 4.5, and 15.5. |
| Goal Relevance | ~11 | Consistently identified as relational/derived, not a dimension. Explicitly defended in 4.1, 5.7. |

**Assessment:** These terms are clean. No action needed.

---

## 2. Terms With Possible Synonym Drift

### Issue T-1: "landscape" vs "topography"

**Section:** 1, 5, 6, 12, 16, 17 (throughout)
**Current usage:** "landscape" appears ~25 times. "topography" appears ~132 times.
**Concern:** "Landscape" is used as an informal/intuitive synonym for "topography" in narrative passages (e.g., "what landscape did we ask it to move through?"). This is intentional in Section 1 as the intuitive hook before the formal term is introduced. But in later sections, mixing "landscape" and "topography" could create ambiguity.
**Recommended handling:** Keep "landscape" in Section 1 (intuitive), Section 17 (rhetorical closure), and the marble metaphor. In Sections 4-14, prefer "topography" or "perceived topography" for precision. Review any use of "landscape" in Sections 5-13 for potential replacement.
**Risk level:** Low — the paper already uses topography dominantly. The few landscape uses are clearly narrative, not technical.

### Issue T-2: "environment" vs "topography"

**Section:** 1, 4, 5, 6, 7
**Current usage:** "environment" appears ~30 times (excluding compound phrases like "information environment").
**Concern:** In Section 1, "environment" is used loosely before "topography" is defined: "a poorly shaped environment," "a shaped environment." In Section 4, "environment shaped by information, constraints, confidence, tools, and action costs." These are pre-definition uses that work narratively but could create conceptual blur with the formal term "topography."
**Recommended handling:** Accept in Section 1 (pre-definition narrative). In Sections 4+, consider whether any standalone "environment" should become "topography" or "perceived topography."
**Risk level:** Low — the paper transitions cleanly from intuitive "environment" to formal "topography."

### Issue T-3: "reasoning state" vs "reasoning-state" hyphenation

**Current usage:** 68 unhyphenated, 28 hyphenated.
**Concern:** Inconsistent hyphenation. Should be: unhyphenated as noun phrase ("the reasoning state"), hyphenated as compound adjective ("a reasoning-state system").
**Recommended handling:** Standardize. Review all 96 instances. Apply rule: "reasoning state" as noun, "reasoning-state" before a noun.
**Risk level:** Medium — this is a presentation-quality issue that reviewers may notice.

### Issue T-4: "model update" (generic) vs "Model Update Object" (formal)

**Current usage:** 77 capitalized "Model Update Object," 63 generic "model update."
**Concern:** The generic "model update" is used in learning discussions where the full object name would be heavy. This is acceptable in context but could create ambiguity about whether a "model update" is the same thing as a "Model Update Object."
**Recommended handling:** Keep current usage but consider adding a clarifying note in Section 2 or 8 that "model update" refers to the change itself, while "Model Update Object" refers to the durable record of that change.
**Risk level:** Low — the distinction is clear in context.

### Issue T-5: "memory" used loosely

**Section:** 9, 10, 16
**Current usage:** "memory" appears ~15 times outside compound phrases.
**Concern:** Used in phrases like "becomes memory," "unit of memory," "narrative memory," "vague memory." In Section 16.10, "agent memory" is contrasted with "model change." The framework explicitly distinguishes memory (storage) from learning (model change). The loose uses of "memory" in early sections could blur this distinction.
**Recommended handling:** Review uses in Sections 3, 9, and 10. Ensure "memory" is not used where "reasoning state" or "learning" is meant. Current usage appears acceptable — "memory" is consistently used in the negative sense ("memory is not enough").
**Risk level:** Low — the paper's rhetorical use of "memory" is deliberate and clear.

---

## 3. Terms Used Before Defined

All framework terms appear in Section 1 before their formal definitions in Section 2. This is intentional — Section 1 uses terms intuitively to set up the argument, and Section 2 provides precise definitions.

**Key pre-definition uses (Section 1):**
- "optimizer" — line 23 (defined Section 2, line 107)
- "topography" — line 1 (title; defined Section 2, line 147)
- "gradient" — line 23 (defined Section 2, line 169)
- "sufficiency" — line 37 (defined Section 2, line 225)
- "reasoning state" — line 37 (defined Section 2, line 141)
- "Model Update Object" — line 45 (defined Section 2, line 261)
- "prediction error" — line 45 (defined Section 2, line 239)

**Assessment:** This is standard paper structure — the introduction uses terms the reader will learn in the next section. The "A Note on Terms" section (Section 2) follows immediately. No action needed unless a reviewer flags confusion.

**Risk level:** Low

---

## 4. Terms That Appear With Multiple Meanings

### Issue T-6: "confidence"

**Occurrences:** ~155
**Meanings:**
1. **Formal topography dimension** — "Confidence: How trustworthy is this?" (Sections 2, 5, 6, 14)
2. **General English** — "medium-high confidence," "how confident are we," "confidence level" (Sections 8, 9, 12)
3. **Model Update Object field** — "Confidence" as a required field (Section 9)

**Concern:** The topography dimension "Confidence" and the MUO field "Confidence" share a name but serve different purposes. The dimension describes information trustworthiness. The field describes learning reliability. A reader might conflate them.
**Recommended handling:** Consider capitalizing "Confidence" when used as the formal dimension (matching Visibility, Accessibility, etc.) and using lowercase "confidence" for the general concept. Or add a brief note in Section 9 that "Confidence in a Model Update Object refers to how strongly the learning should shape future behavior, which is related to but distinct from the topography dimension Confidence."
**Risk level:** Medium — this is the most ambiguous term in the paper.

### Issue T-7: "system"

**Occurrences:** ~258
**Meanings:**
1. "the AI system" — the model/agent
2. "the human-agent system" — the broader workflow
3. "the reasoning-state system" — the architecture
4. "the implementation system" — the built product

**Concern:** "System" is heavily overloaded. Most uses are clear in context, but some sentences could be read multiple ways: "If the system does not preserve reasoning state" — which system?
**Recommended handling:** No global fix needed. Flag 5-10 high-ambiguity uses for qualification (e.g., "the human-agent system" vs "the AI system").
**Risk level:** Low — context generally disambiguates.

---

## 5. Common-Language vs Framework-Specific Conflicts

### Issue T-8: "discovery"

**Section:** 11, 12, 13
**Concern:** "Discovery" is both a framework concept (Retrieve → Infer → Propose → Confirm → Generate → Preserve → Learn) and a common English word ("during discovery," "the discovery process"). Most uses are clear, but "Initial Discovery" could be confused with generic requirements gathering.
**Recommended handling:** Keep current usage. Section 11 defines Discovery clearly enough. The capitalization convention (uppercase "Discovery" for the framework concept) could be applied more consistently.
**Risk level:** Low

### Issue T-9: "investigation"

**Section:** 6, 8, 14
**Concern:** "Investigation" is both an optimizer motion stage and a general-purpose word. In Section 8, "investigation" appears in the learning sequence and in general-purpose usage ("the team investigates"). Most uses are clear.
**Recommended handling:** No change needed. Context disambiguates.
**Risk level:** Low

---

## 6. Heading/Body Mismatches

### Issue T-10: Section 12.6 "Sufficiency" heading

**Section:** 12.6
**Heading:** `## 12.6 Sufficiency`
**Body:** Describes why the system can act — a sufficiency rationale, not the concept of sufficiency itself.
**Concern:** The heading could be read as a re-explanation of Section 6.5 (Sufficiency). It is actually an application of sufficiency to the running example.
**Recommended handling:** Consider `## 12.6 Why the System Can Act` or `## 12.6 Sufficiency Rationale` to distinguish from the conceptual section.
**Risk level:** Low

---

## 7. Phrases That Sound Like New Primitives But Are Not Defined

### Issue T-11: "action landscape" and "information landscape"

**Section:** 1 (lines 39)
**Phrase:** "an information landscape where..." and "an action landscape where..."
**Concern:** These compound phrases appear once each in Section 1. They could be read as distinct concepts (is there an "action landscape" separate from "information topography"?). The paper does not define or use these terms again.
**Recommended handling:** These are narrative phrases in the introduction, not framework terms. No change needed unless a reviewer flags them. If concerned, rephrase to "an information environment" or simply "a landscape."
**Risk level:** Low

### Issue T-12: "reasoning-state partner"

**Section:** 13 (line ~3200)
**Phrase:** "It becomes a reasoning-state partner."
**Concern:** "Partner" could imply a new concept or relationship type. It is used rhetorically, not technically.
**Recommended handling:** Keep. Clear in context as a description of the system's role, not a new framework term.
**Risk level:** Low

### Issue T-13: "epistemic infrastructure"

**Section:** 17 (line ~4113)
**Phrase:** "It is better epistemic infrastructure."
**Concern:** This phrase appears once. It is evocative but not a framework term.
**Recommended handling:** Keep. It is a closing-section characterization, not a new concept.
**Risk level:** Low

---

## 8. Specific Drift Checks

| Potential Drift | Status |
|----------------|--------|
| "context state" vs "reasoning state" | **Clean** — "context state" does not appear in the paper. |
| "environment" vs "topography" | **Minor drift** — see Issue T-2. Acceptable in pre-definition sections. |
| "landscape" vs "topography" | **Minor drift** — see Issue T-1. Intentional in narrative sections. |
| "memory" vs "learning" | **Clean** — consistently distinguished. Memory = storage. Learning = model change. |
| "storage" vs "learning" | **Clean** — explicitly contrasted ("Storage ≠ Learning"). |
| "confidence" vs "certainty" | **Clean** — "Sufficiency is not certainty" appears 2 times. Clear distinction. |
| "constraint" vs "policy" | **Clean** — "Policy is a constraint" is the explicit framing. No confusion. |
| "evidence" vs "context" | **Clean** — evidence supports claims; context provides information. Different roles, clearly used. |
| "goal relevance as a dimension" | **Clean** — explicitly rejected in 4.1, 5.7. |
| "policy as a topography dimension" | **Clean** — explicitly rejected in 5.8. |
| "action model as separate primitive" | **Clean** — explicitly rejected in 4.3, 4.5. |
| "decision state vs optimizer state" | **Clean** — different objects at different levels. Never confused. |
| "model update vs memory update" | **Clean** — "memory update" does not appear in the paper. |

---

## 9. Summary of Recommended Actions

| ID | Issue | Risk | Action |
|----|-------|------|--------|
| T-1 | landscape vs topography | Low | Review Sections 5-13 for unnecessary "landscape" uses. Keep in S1, S17. |
| T-2 | environment vs topography | Low | Accept in S1. Check S4+ for precision. |
| T-3 | reasoning state hyphenation | Medium | Standardize: noun = unhyphenated, adjective = hyphenated. |
| T-4 | model update vs Model Update Object | Low | Consider clarifying note in S2 or S8. |
| T-5 | memory used loosely | Low | Verify uses in S3, S9, S10 are in the negative sense. |
| T-6 | confidence overload | Medium | Consider capitalization convention or brief disambiguation note. |
| T-7 | system overload | Low | Flag 5-10 high-ambiguity uses for qualification. |
| T-8 | discovery as common word | Low | Apply uppercase convention more consistently. |
| T-9 | investigation as common word | Low | No change needed. |
| T-10 | S12.6 heading mismatch | Low | Consider renaming to "Sufficiency Rationale." |
| T-11 | action/information landscape | Low | Keep as narrative. No framework term conflict. |
| T-12 | reasoning-state partner | Low | Keep. Rhetorical, not technical. |
| T-13 | epistemic infrastructure | Low | Keep. Closing characterization, not new concept. |

**Overall assessment:** The paper's terminology is well-disciplined. The two medium-risk items (T-3 hyphenation, T-6 confidence overload) are presentation-quality issues that should be addressed before submission but do not represent conceptual confusion. No high-risk terminology problems found.
