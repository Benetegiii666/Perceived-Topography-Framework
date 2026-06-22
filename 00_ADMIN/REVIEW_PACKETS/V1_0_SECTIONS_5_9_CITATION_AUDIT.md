# v1.0 Sections 5–9 Citation Audit

**Date:** 2026-06-20
**Scope:** Sections 5–9 of PAPER_v1.0_WORKING.md
**Purpose:** Determine where citations are genuinely needed vs. where claims are original synthesis or paper-internal.

---

## Citation Audit Table

| Section | Paragraph/concept | Claim needing review | Classification | Candidate source | Confidence | Recommended action | Notes |
|---|---|---|---|---|---|---|---|
| S5 | Opening | "The scenario is constructed rather than empirical." | No citation needed | — | — | Leave uncited | Self-declaration of method. Already clear. |
| S5 | Entire section | Healthcare campaign walkthrough | No citation needed | — | — | Leave uncited | Constructed scenario using paper's own framework. No external claims made. |
| S6 | Line ~911 | "Learning begins only when the organization can compare what happened with what it expected" | Lineage / background | Argyris & Schön, 1978 (single/double-loop learning) | High | Cite existing source | The prediction-error → model-update sequence draws directly from organizational learning theory. One citation here would anchor the section. |
| S6 | Line ~927 | "Learning is an evidence-supported model update triggered by prediction error." | Original synthesis — do not force citation | — | — | Leave uncited | This is the paper's own definition. It synthesizes from organizational learning and prediction-error traditions, but the specific formulation is original. S10 already cites Argyris & Schön in the lineage table. |
| S6 | Lines ~994–1008 | "Correction is not learning" distinction | Lineage / background | Argyris & Schön, 1978 (single-loop vs. double-loop) | High | Cite existing source | The correction-vs-learning distinction is the paper's strongest borrowing from Argyris & Schön. One citation would strengthen credibility. |
| S6 | Lines ~1010–1045 | "Reaction is not learning" — blanket restriction example | Original synthesis — do not force citation | — | — | Leave uncited | The specific tool-action example and the "restriction preserves ignorance" framing are original to this paper. |
| S6 | Lines ~1047–1075 | "Postmortem is not learning" — KM graveyard | Real support needed | Markus, 2001; Weber et al., 2001 (KM failure/reuse) | Medium | Find source | The "lessons-learned graveyard" is a well-documented phenomenon in KM literature. One citation would prevent the claim from sounding like assertion. SOURCE NEEDED — verify exact references before inserting. |
| S6 | Lines ~1077–1108 | "Storage is not learning" | No citation needed | — | — | Leave uncited | Follows from the paper's own distinction chain. No external claim. |
| S6 | Lines ~1183–1230 | Model Update Object specification (11-field) | Original synthesis — do not force citation | — | — | Leave uncited | The MUO is the paper's own contribution. Citing case-based reasoning (Aamodt & Plaza, 1994) as lineage is already done in S10's table. |
| S7 | Lines ~1274–1287 | Discovery captures tacit reasoning before action | Lineage / background | Nonaka & Takeuchi, 1995 (tacit knowledge); Klein, 1998 (naturalistic decision-making) | Medium | Cite if available | The tacit-to-explicit conversion is well-studied. One citation would ground the claim. S10 does not explicitly cite Nonaka & Takeuchi. SOURCE NEEDED — verify availability. |
| S7 | Lines ~1328–1342 | "Blank forms create burden. Silent inference creates false confidence." | Original synthesis — do not force citation | — | — | Leave uncited | The middle-path framing between blank forms and silent inference is the paper's original design argument. |
| S7 | Lines ~1342 | "The system should do the reasoning work before asking the user to do it." | Lineage / background | Horvitz, 1999 (mixed-initiative interaction); Sweller, 1988 (cognitive load) | Medium | Cite existing source | The burden-reduction principle echoes mixed-initiative interaction design. Already cited in S10 lineage table (Horvitz). An inline citation here would connect the claim to its tradition. |
| S7 | Lines ~1344–1375 | Retrieve → Infer → Propose → Confirm loop | Original synthesis — do not force citation | — | — | Leave uncited | The RIPC loop is the paper's own contribution. It draws on mixed-initiative and requirements-elicitation traditions but the specific formulation is new. |
| S7 | Lines ~1459–1467 | "Confirmation is not a yes/no approval click" — governance humility | No citation needed | — | — | Leave uncited | Paper-internal claim about the framework's own design. |
| S7 | Lines ~1497 | Table 6: Ordinary Intake vs. Discovery questions | Original synthesis — do not force citation | — | — | Leave uncited | Original table showing framework-specific contrasts. |
| S8 | Lines ~1661–1679 | "The unit of organizational reasoning is not the document. It is the optimizer state transition." | Original synthesis — do not force citation | — | — | Leave uncited | Central claim of the paper. Drawing on organizational learning and decision rationale but the specific formulation is new. |
| S8 | Lines ~1681–1707 | "Documents are not enough" — postmortems, lessons-learned, compliance updates create artifacts but not reasoning | Lineage / background | Markus, 2001 (KM reuse failure); Feldman & Pentland, 2003 (organizational routines) | Medium | Find source | The "artifact but not reasoning" failure pattern is well-documented. One citation would strengthen. SOURCE NEEDED — verify exact references. |
| S8 | Lines ~1778–1807 | Context layer vs. reasoning-state layer distinction | Original synthesis — do not force citation | — | — | Leave uncited | The specific two-layer distinction is the paper's contribution. RAG literature is already cited in S10. |
| S8 | Lines ~1809–1831 | "Retrieval must be by reasoning relevance" — retrieval as gradient selection | Original synthesis — do not force citation | — | — | Leave uncited | Novel framing. Builds on RAG/grounding but the "reasoning relevance" concept is new. |
| S8 | Lines ~1833–1853 | Status lifecycle (Draft → Provisional → Validated → Deprecated → Superseded) | No citation needed | — | — | Leave uncited | Framework-internal design. Not claimed to be borrowed. |
| S8 | Lines ~1903 | Table 8: Maturity Model (Stage 0–4) | Original synthesis — do not force citation | — | — | Leave uncited | Original framework contribution. Maturity models exist in CMM/CMMI tradition but this specific model is novel. |
| S9 | Lines ~1967–1987 | "A framework that explains everything explains nothing" — falsifiability posture | No citation needed | — | — | Leave uncited | Philosophical principle. Does not need attribution. |
| S9 | Lines ~1989–2013 | Unfalsifiability objection and response | No citation needed | — | — | Leave uncited | Self-directed critique. Paper is arguing with itself. |
| S9 | Lines ~2015–2049 | "Just good systems engineering" objection | No citation needed | — | — | Clarify prose if needed | The paper concedes and sharpens. No external claim requires citation. |
| S9 | Lines ~2081 | Table 9: Disconfirmation Conditions | Original synthesis — do not force citation | — | — | Leave uncited | Framework-specific falsifiability conditions. Original. |
| S9 | Lines ~2095–2123 | Risks: false precision, authority, surveillance, stale reasoning, policy laundering, automation bias, metaphor limits | Lineage / background | Lee & See, 2004 (automation bias/trust); Parasuraman & Riley, 1997 (automation misuse) | Medium | Consider citing | Automation bias and overtrust are well-studied. Already cited in S4. A brief callback citation here would connect the risk to the literature. |
| S9 | Lines ~2134–2136 | "Governance automation... inspectable, routable, reviewable, auditable, contestable" | No citation needed | — | — | Leave uncited | Framework-internal design claim. |
| S9 | Lines ~2136 | "Qualitative distinctions can become hard measurements when operationalized through rubrics, categorical labels, inter-rater agreement..." | No citation needed | — | — | Leave uncited | Methodological observation. Standard research-methods knowledge. |

---

## Summary Findings

### 1. Top citation gaps that are genuinely important

| Priority | Section | Claim | Candidate source | Action |
|---|---|---|---|---|
| **1** | S6 (~line 911 or 994) | Learning as model change / correction-vs-learning distinction | Argyris & Schön, 1978 | **Cite.** One inline citation anchoring the organizational learning tradition. Already in S10 lineage table. |
| **2** | S6 (~line 1055) | KM graveyard / lessons-learned failure | Markus, 2001 or equivalent | **Find and cite.** The "lessons become shelfware" claim is well-documented but currently unsupported. SOURCE NEEDED — verify before inserting. |
| **3** | S7 (~line 1342) | "Do the reasoning work before asking the user to do it" / burden reduction | Horvitz, 1999 (mixed-initiative) | **Cite.** Already in S10 lineage table. An inline citation connects the design principle to its tradition. |

### 2. Claims that should remain uncited because they are original synthesis

- "Learning is an evidence-supported model update triggered by prediction error" (S6) — the paper's own definition
- Retrieve → Infer → Propose → Confirm loop (S7) — the paper's own contribution
- "The unit of organizational reasoning is not the document" (S8) — the paper's central claim
- Context layer vs. reasoning-state layer distinction (S8) — novel two-layer architecture
- "Retrieval by reasoning relevance" (S8) — novel retrieval concept
- Six-object chain (S8) — novel architecture
- Maturity model (S8) — novel staging
- Disconfirmation conditions table (S9) — framework-specific falsifiability
- All of Section 5 — constructed scenario using the paper's own framework

### 3. Places where prose should be softened instead of cited

None identified. The prose is already appropriately hedged where needed (e.g., "the scenario is constructed rather than empirical," "the framework is not empirically validated here").

### 4. Places where a citation would create false lineage

- Do NOT cite organizational learning literature as saying "Model Update Objects" — that is the paper's term.
- Do NOT cite RAG literature as supporting "reasoning-state retrieval" — that is the paper's extension beyond RAG.
- Do NOT cite decision-rationale literature as supporting the six-object chain — the chain is novel.
- Do NOT cite Nonaka & Takeuchi as supporting the Retrieve → Infer → Propose → Confirm loop — Discovery is the paper's synthesis, not a direct borrowing from tacit-knowledge literature.

### 5. Citation work assessment

**Sections 5–9 need: light citation work.**

- **3 citations genuinely needed** (Argyris & Schön in S6, KM failure source in S6, Horvitz in S7)
- **1 optional citation** (automation bias in S9, but already cited in S4)
- **1 optional citation** (tacit knowledge in S7, but may create false lineage)
- **~20 claims correctly left uncited** as original synthesis, paper-internal definitions, or no-citation-needed transitions

The "citation desert" flagged in the pressure test is real but less severe than it appeared. Sections 5–9 are primarily original synthesis and constructed-scenario sections. They do not make many externally grounded claims. The 3 genuinely needed citations would close the most visible gaps without turning the sections into citation-heavy academic prose.

---

## No-Edit Confirmation

- Working manuscript edited: No
- Citations inserted: No
- Prose rewritten: No
- Figures modified: No
- Bibliography modified: No
- Sources invented: No
