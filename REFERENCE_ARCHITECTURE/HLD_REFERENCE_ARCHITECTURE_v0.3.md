# HLD / Reference Architecture v0.3 — Complete Draft

**Date:** 2026-06-22
**Status:** v0.3 Complete Draft. All 16 chapters drafted.
**Classification:** HLD v0.3 Complete Draft
**Base:** v0.2 Architecture Spine (2026-06-22)

---

## Architecture Charter

### What This Document Is

This is the complete draft of the Perceived Topography Framework HLD / Reference Architecture. All 16 chapters are drafted. Spine chapters (2, 3, 5, 6, 8, 13) were established in v0.2. Remaining chapters (4, 7, 9, 10, 11, 12, 14, 15) are expanded in this version.

### What This Document Is Not

- Not an implementation manual. The HLD specifies what must exist and how components relate; it does not specify code, database DDL, or deployment scripts.
- Not a product pitch or vendor recommendation.
- Not a paper revision or companion artifact edit.

### Source Hierarchy

| Priority | Source | Authority |
|---|---|---|
| 1 | Frozen keystone paper (`PAPER_v1.0_WORKING.md`) | Conceptual authority. The HLD must preserve the paper's logic. |
| 2 | Build Discovery Guide v1.0 (`BUILD_DISCOVERY_GUIDE_v1.0.md`) | Build-input authority. The HLD translates discovery outputs into architecture. |
| 3 | Executive Brief v1.0 (`EXECUTIVE_BRIEF_v1.0.md`) | Leadership / funding framing. Sets the organizational language. |
| 4 | RapidSOS Marketing Context Layer (`Rapid/`) | Practical grounding example only. Illustrates patterns; does not set architecture. |
| 5 | Martin implementation work (Beacon, model router, co-worker) | Compatibility / interface surface. Not conceptual authority unless explicitly promoted. |

### HLD Design Stance

**Design from reasoning-state preservation outward.**

Do not start from model choice, vendor choice, chatbot UI, or generic RAG. Start from:

- The repeated decision workflow
- The decision artifact produced by the workflow, plus the six reasoning-state objects that explain how and why that artifact became sufficient
- The information surfaces
- The sufficiency gates
- The governance gradients
- The human confirmation points
- The ownership lifecycle
- The learning loop

The HLD must show how the system makes premature sufficiency harder by changing what the human-agent system can **see**, **retrieve**, **trust**, **question**, **preserve**, **stop on**, **escalate**, and **learn from**.

### Blueprint Used

This document preserves the 16-chapter structure from `V1_0_HLD_REFERENCE_ARCHITECTURE_PLANNING_BLUEPRINT.md` (dated 2026-06-21). The task specification's 23 required sections are mapped into this structure — additional concerns appear as subsections rather than replacements.

### Relationship to Keystone Paper and Companion Artifacts

```text
Paper (teaches the framework — conceptual authority)
        |
        v
Build Discovery Guide v1.0 (discovers the reasoning — build-input authority)
        |
        v
HLD / Reference Architecture (builds the system — this document)
```

- The paper defines what reasoning-state preservation means and why it matters.
- The Build Discovery Guide defines how to discover what an organization knows, believes, and needs.
- The HLD defines what to build, how components relate, and how reasoning-state preservation operates as a system.

The HLD does not redefine concepts from the paper. It translates them into buildable components.
The HLD does not replace the Build Discovery Guide. It consumes discovery outputs as architecture inputs.

---

## Part I: Foundation

### Chapter 1 — Introduction

#### 1.1 Purpose of the HLD / Reference Architecture

**Section purpose:** Establish what the HLD is for, who it serves, and what it is not.

**Inputs from Build Discovery Guide:** Category 13 (Build Translation) — architecture-landing summary, MVP scope.

**Expected technical outputs:**

- Audience table (enterprise architects, platform teams, product engineers, governance teams, AI enablement teams, technical program leads)
- Scope boundary (reasoning-state preservation for repeated decision workflows — not all of enterprise AI)
- Anti-pattern list (not vendor-specific, not product pitch, not implementation manual, not universal platform, not generic RAG)

**MVP / Future Phase:** Foundation — applies to all phases.

**Open questions:**

- How should this document be versioned alongside the paper and companion artifacts?

**Martin compatibility notes:** N/A for this section.

#### 1.2 Relationship to the Paper and Build Discovery Guide

**Section purpose:** Make the artifact chain explicit so readers understand where concepts originate, where build inputs come from, and where architecture decisions live.

**Inputs from Build Discovery Guide:** Preamble and Category 13 (Build Translation).

**Expected technical outputs:**

- Artifact chain diagram (paper → guide → HLD)
- Responsibility matrix (which artifact owns which decisions)
- Cross-reference index (paper section → guide category → HLD chapter)

**MVP / Future Phase:** Foundation — applies to all phases.

**Open questions:**

- Should the HLD carry forward the paper's table/figure numbering, or establish its own?

**Martin compatibility notes:** N/A for this section.

#### 1.3 Scope and Non-Scope

**Section purpose:** Define what the HLD must cover and what it must not become.

**Inputs from Build Discovery Guide:** Category 1 (Workflow Boundary), Category 13 (Build Translation — MVP scope).

**Expected technical outputs:**

- Scope table (from blueprint Section 2): reasoning-state preservation, Discovery/RIPC, reasoning-relevant retrieval, governance/lifecycle, confidence/provenance, applicability boundaries, human confirmation, integration with RAG/agentic systems, audit/observability, minimal viable implementation
- Anti-pattern table (from blueprint Section 2): not vendor-specific, not product pitch, not implementation manual, not universal platform, not generic RAG

**MVP / Future Phase:** Foundation — applies to all phases.

**Open questions:**

- Where does the boundary between "reasoning-state preservation" and "organizational knowledge management" fall?

**Martin compatibility notes:** The scope must accommodate future integration with Beacon, co-worker, and model router without being designed around them.

#### 1.4 How to Read This Document

**Section purpose:** Provide a reading guide so different audiences can navigate to what they need.

**Inputs from Build Discovery Guide:** N/A.

**Expected technical outputs:**

- Audience-to-chapter mapping
- Reading order recommendations by role

**MVP / Future Phase:** Foundation — applies to all phases.

**Open questions:** None.

**Martin compatibility notes:** N/A for this section.

---

### Chapter 2 — Architecture Principles

These nine principles are derived from the keystone paper's conceptual architecture and function as non-negotiable design constraints. Every subsequent chapter must satisfy them. A system that violates a principle may still work technically, but it is no longer implementing the Perceived Topography Framework.

---

#### Principle 1: Preserve Reasoning, Not Just Artifacts

**Meaning:** The unit of organizational reasoning is the optimizer state transition — the movement from perceived landscape through investigation, sufficiency, action, outcome, and model change. Documents preserve artifacts. A reasoning architecture preserves the transition: what the system was trying to do, what it believed, why the available information felt sufficient, what reality later contradicted, and what should change.

**Architectural implication:** The system must store and retrieve structured reasoning objects (Optimizer State, Premise Stack, Decision State, Investigation Trace, Learning Event, Model Update Object) — not only the decision artifact itself (the campaign brief, the support summary, the policy decision). The decision artifact is the output of the workflow. The reasoning objects explain how and why that artifact became sufficient.

**What would violate this principle:** A system that stores only the final brief, email draft, or approval record without preserving the goal, premises, rejected alternatives, sufficiency rationale, or unresolved uncertainties that produced it. A system where "preserved reasoning" means saving the LLM's chain-of-thought output rather than structured, human-confirmed reasoning state.

**MVP consequence:** Even the first implementation cycle must capture at least an Optimizer State (goal + interpretation), a small Premise Stack (3-5 key assumptions), a Decision State (what was chosen, why it felt sufficient), and an outcome record. Without this minimum, the system is a context layer, not a reasoning-state layer.

---

#### Principle 2: Retrieve by Reasoning Relevance, Not Just Semantic Similarity

**Meaning:** The most important prior reasoning may not use similar language. It may be relevant because it shares a goal, a policy boundary, an audience assumption, an unresolved uncertainty, a confidence limit, or a failure pattern. Semantic similarity finds text that sounds alike. Reasoning relevance finds reasoning that matters to the decision at hand.

**Architectural implication:** Retrieval must combine semantic search with structured metadata filtering. Reasoning objects must carry indexable metadata — goal, policy scope, applicability boundary, confidence, status, workflow context, audience, provenance — that supports filtering beyond text similarity. The retrieval system must present a match rationale explaining why each result was surfaced, not just a similarity score.

**What would violate this principle:** A system where retrieval is reducible to "embed the query, return the top-K nearest chunks from a vector store." A system where reasoning objects are stored but can only be found by keyword or embedding match.

**MVP consequence:** The first implementation must support at least semantic search plus metadata filters on goal, workflow type, and lifecycle status. Match rationale should be displayed even if it is simple ("matched on similar goal and same workflow type"). Full reasoning-relevant retrieval with multi-dimensional filtering is a later maturity stage, but the schema and metadata must be in place from the start so that richer retrieval can be added without re-architecting.

---

#### Principle 3: Behavioral Availability

**Meaning:** A reasoning surface is behaviorally available when it can appear at the moment it matters, with enough confidence, provenance, scope, and status for the human-agent system to know how to use it. Storage without behavioral availability is a knowledge-management graveyard. A model update that exists but is never surfaced when a similar decision forms has no behavioral force.

**Architectural implication:** The system must surface prior reasoning at decision time — during Discovery, during drafting, during review — not only when explicitly searched. Retrieval must be triggered by workflow events (workflow start, similar decision detected, repeated pattern identified), not only by user queries. Surfaced reasoning must carry enough metadata (confidence, provenance, applicability, status) for the recipient to judge whether to use it.

**What would violate this principle:** A system that stores reasoning objects but only surfaces them when a user explicitly searches for them. A reasoning-state store that exists alongside the workflow but never proactively introduces prior reasoning into the decision context.

**MVP consequence:** In the first cycle, behavioral availability may be manual — the RIPC loop retrieves prior reasoning at the start of each new workflow instance. Full event-driven surfacing is a maturity concern. But the architecture must be designed so that retrieval can be triggered by workflow events, not only by user queries.

---

#### Principle 4: Human Confirmation of Applicability Before Reuse

**Meaning:** Prior reasoning must not be silently applied to new decisions. The system proposes; the human confirms that the prior reasoning applies to the current situation. Confirmation is not a yes/no approval click. The human must be able to confirm, correct, reject, qualify, or bound the proposed reasoning.

**Architectural implication:** Every point where prior reasoning enters a new decision must include a confirmation step. The confirmation record must preserve who confirmed, what they confirmed, what they changed, what authority they held, and what scope the confirmation covers. The system must not treat non-response as confirmation. The system must not apply retrieved reasoning automatically without a human applicability judgment.

**What would violate this principle:** A system that retrieves a prior Model Update Object and automatically incorporates it into the next cycle's reasoning without human review. A system that treats all retrieved reasoning as equally applicable. A system where "human in the loop" means a single approval button at the end of a generated draft.

**MVP consequence:** The first cycle must include explicit confirmation before any prior reasoning shapes the current decision. Confirmation may be lightweight (a single review screen showing the prior reasoning with its applicability boundary and asking the human to confirm, correct, or reject), but it must exist. Confirmation fatigue mitigation (adaptive frequency, skip for already-validated reasoning) is a later maturity concern.

---

#### Principle 5: Confidence and Provenance as First-Class Metadata

**Meaning:** Every reasoning object must carry information about how confident the system or human is, where the reasoning came from, who confirmed it, and what evidence supports it. Without this metadata, all prior reasoning becomes equally authoritative and equally misleading. A premise confirmed by a domain expert with outcome evidence is not the same as a system-inferred assumption that nobody reviewed.

**Architectural implication:** Confidence and provenance fields must be required (not optional) on every reasoning object. Confidence must distinguish system-inferred from human-confirmed. Provenance must track creator, confirmer, confirmation authority, evidence basis, and timestamp. Retrieval must surface confidence and provenance so recipients can judge weight. Display must make confidence and provenance visible without burying them in metadata panels.

**What would violate this principle:** A system where reasoning objects have no confidence indicator. A system where system-inferred reasoning looks identical to human-confirmed reasoning. A system where provenance is stored but not displayed at retrieval time.

**MVP consequence:** Every reasoning object in the first cycle must carry at least: confidence level (Low / Medium / High), source type (system-inferred / human-created / human-confirmed), and confirmer identity. Numeric confidence, evidence-linked confidence, or multi-dimensional confidence are future-phase refinements.

---

#### Principle 6: Applicability Boundaries

**Meaning:** A lesson learned about cardiology campaign targeting should not automatically reshape oncology outreach or partner enablement. Every reasoning object must carry explicit boundaries about where it applies and where it does not. Without boundaries, reasoning surfaces become invisible governance — they shape future action without anyone knowing the limits of their relevance.

**Architectural implication:** Applicability boundary and non-applicability boundary must be fields on every reasoning object (especially Model Update Objects and Premise Stack entries). Retrieval must use non-applicability boundaries as negative filters — if a reasoning object explicitly declares it does not apply to the current context, it should be excluded or flagged. Display must show boundaries alongside content so the human can assess fit.

**What would violate this principle:** A system that stores model updates without scope limits. A system where a lesson from one campaign type is silently applied to all campaigns. A system where "applicability boundary" is a free-text field that is never used in retrieval filtering.

**MVP consequence:** Every Model Update Object in the first cycle must carry at least a free-text applicability description ("applies to cardiology practice administrator campaigns") and a free-text non-applicability note ("does not apply to partner enablement without further validation"). Structured tag-based boundaries are a future-phase refinement, but the fields must exist from day one.

---

#### Principle 7: Lifecycle Status

**Meaning:** Reasoning objects are not permanent truths. They may be drafts, provisional interpretations, validated lessons, deprecated assumptions, or superseded rules. Without status, every preserved reasoning surface risks becoming equally available and equally misleading. A provisional interpretation may be reused as if it were validated. A deprecated assumption may continue to shape action.

**Architectural implication:** Every reasoning object must carry a lifecycle status field. The system must distinguish at least Draft (unconfirmed), Provisional (confirmed by a human but not yet outcome-validated), and Validated (confirmed and supported by evidence or authoritative review). Retrieval must filter and rank by status. Display must visibly mark status so the recipient knows the weight of the reasoning.

**What would violate this principle:** A system where all stored reasoning has the same status. A system where a system-generated inference becomes indistinguishable from a human-validated lesson. A system where deprecated reasoning continues to be retrieved without flagging.

**MVP consequence:** Three lifecycle states for MVP: Draft, Provisional, Validated. Status must be displayed on every surfaced reasoning object. Transitions must be logged (who moved it, when, from what state to what state). Full seven-state lifecycle (adding Deprecated, Superseded, Rejected, Archived) is a future-phase concern.

---

#### Principle 8: Selective Capture, Not Total Capture

**Meaning:** The goal is not to turn every human thought into a field. The goal is to preserve the minimum reasoning structure required for future action, learning, and governance. If the system tries to capture everything, it becomes bureaucracy. Workers will avoid it, game the inputs, or become unwilling to express genuine uncertainty.

**Architectural implication:** The system must capture reasoning only for workflows where reasoning repeatedly disappears and where its disappearance causes material harm. Within those workflows, the system must capture the minimum set of reasoning objects that changes future action. The system must not require reasoning capture for routine, low-consequence work. The system must give humans control over what is recorded. The system must not capture reasoning that the human has not chosen to share.

**What would violate this principle:** A system that requires full six-object reasoning capture for every workflow. A system that records every user hesitation, question, or revision as a reasoning object. A system where the overhead of reasoning capture exceeds the cost of starting over.

**MVP consequence:** The first implementation targets one repeated decision workflow. Within that workflow, it captures Optimizer State, Premise Stack (3-5 premises), Decision State, and outcome. Investigation Trace, Learning Event, and MUO are captured only when the outcome contradicts expectations and the team can identify an evidence-supported explanation. If a reasoning object does not change future action, it should not be created.

---

#### Principle 9: Govern Reuse, Not Merely Storage

**Meaning:** The critical governance question is not whether reasoning is stored. It is whether reasoning is reused appropriately. An ungoverned reasoning-state store is worse than no reasoning-state store because it creates false confidence from prior experience. Governance must address who can create, confirm, reject, modify, deprecate, supersede, and audit reasoning objects — and under what conditions prior reasoning can shape future action.

**Architectural implication:** Governance must operate at reuse time, not only at storage time. When prior reasoning is surfaced during Discovery, the system must enforce: lifecycle status check (is this still valid?), applicability check (does it apply here?), authority check (was it confirmed by someone with relevant authority?), and staleness check (is it recent enough?). Governance must also operate at creation time: system-inferred reasoning must be visibly marked as Draft and must not shape action until confirmed.

**What would violate this principle:** A system that governs knowledge intake (brand voice checking, quality scoring) but does not govern reasoning reuse. A system where prior reasoning is surfaced without status, applicability, or provenance checks. A system where an unreviewed model update silently becomes organizational policy.

**MVP consequence:** In the first cycle, governance operates at two points: (1) system-inferred reasoning is marked Draft and requires human confirmation before use, and (2) prior reasoning surfaced during Discovery includes status and applicability boundary so the human can judge. Full governance workflows (review chains, approval gates, staleness automation) are future-phase concerns.

*Grounding note: The RapidSOS Marketing Context Layer demonstrated governance on intake (brand voice checking, ICP fit evaluation) and on output (brand consistency scoring, source citation). The coaching model (flag and suggest, not reject) is a useful design pattern. But the PTF HLD requires governance at a third point that the RapidSOS prototype did not address: governance at reasoning reuse time — when prior reasoning surfaces during a new decision and the system must determine whether to treat it as applicable.*

---

## Part II: Data Architecture

### Chapter 3 — Six-Object Reasoning-State Data Model

The reasoning-state data model is the foundation for everything else in this architecture. Retrieval, governance, lifecycle, and learning all operate on these objects. If the data model is wrong, every other chapter inherits the error.

The six objects form a chain that preserves the optimizer state transition — the movement from perceived landscape through investigation, sufficiency, action, outcome, and model change:

```text
Optimizer State → Premise Stack → Decision State → Investigation Trace
        → Learning Event → Model Update Object → Modified Optimizer State
```

Modified Optimizer State is derived, not stored. It is the resulting condition when one or more MUOs are applied to a new Optimizer State. The system stores the MUOs and the new Optimizer State separately, with explicit links showing which MUOs were applied.

**Critical distinction:** The six reasoning objects are not the decision artifact. In the first implementation slice, the campaign brief (or support summary, or policy decision) is the decision artifact — the output of the workflow. The six reasoning objects explain how and why that artifact became sufficient. Both must be preserved, but they are different things.

---

#### Object 1: Optimizer State

**Purpose:** Preserves what the system was trying to do, under what interpretation, goal, and constraints. Without it, future systems inherit outputs without knowing what objective shaped them.

**MVP fields (required):**

| Field | Type | Description |
|---|---|---|
| `optimizer_state_id` | UUID | Unique identifier |
| `workflow_id` | UUID | Links to the workflow instance |
| `goal` | text | Working objective — what the system is trying to achieve |
| `interpretation` | text | How the situation is understood — what the goal means in this context |
| `policy_scope` | text | Governing constraints — what rules apply |
| `requester` | text | Who initiated the workflow |
| `status` | enum | Draft / Provisional / Validated |
| `confidence` | enum | Low / Medium / High |
| `source_type` | enum | system-inferred / human-created / human-confirmed |
| `confirmed_by` | text (nullable) | Who confirmed this state |
| `created_at` | timestamp | When created |
| `version` | integer | Append-only version number |

**Future fields:**

- `confirmed_at` — timestamp of confirmation
- `authority_scope` — what authority the confirmer held
- `information_surfaces_consulted` — which information surfaces informed the interpretation
- `applied_muo_ids` — which Model Update Objects were applied when this state was created (provenance link for Modified Optimizer State)
- `tags` — structured metadata for retrieval filtering

**Lifecycle:** Draft → Provisional → Validated. System-inferred Optimizer States must start as Draft and remain visibly provisional until a human confirms.

**Relationships:**

- Parent of Premise Stack entries (1:many)
- Parent of Decision State (1:1 per decision point)
- Referenced by Learning Events (to identify what the system was trying to do when the outcome occurred)
- Links to workflow definition

**Capture trigger:** Created at the start of the RIPC loop when a new workflow instance begins. The system infers a Draft Optimizer State from the request and retrieved context. The human confirms or corrects it during the Propose step.

**Reuse rules:** Prior Optimizer States are retrievable by goal, policy scope, workflow type, and audience. When surfaced during a new cycle, they must be presented with their applicability boundary and status. The human confirms whether the prior state applies before it shapes the current cycle.

**Campaign brief example:** Goal: generate qualified demo requests from cardiology practice administrators. Interpretation: workflow burden is an attention hook, not a qualification signal — qualified means actively evaluating RPM. Policy scope: no direct clinical-outcome claims without approved evidence. Source type: human-confirmed. Confidence: Medium. Confirmed by: campaign owner.

---

#### Object 2: Premise Stack

**Purpose:** Preserves why the system expected this action or decision to work. Without it, learning becomes premise-blind — the system may observe failure but update the wrong assumption.

**MVP fields (required):**

| Field | Type | Description |
|---|---|---|
| `premise_id` | UUID | Unique identifier |
| `optimizer_state_id` | UUID | Links to parent Optimizer State |
| `statement` | text | The assumption — what is being taken as true |
| `confidence` | enum | Low / Medium / High |
| `evidence_basis` | text | What evidence supports this premise |
| `assumption_type` | enum | explicit / tacit / inferred |
| `status` | enum | Draft / Provisional / Validated |
| `source_type` | enum | system-inferred / human-created / human-confirmed |
| `applicability_boundary` | text | Where this premise applies |
| `created_at` | timestamp | When created |

**Future fields:**

- `non_applicability_boundary` — where this premise explicitly does not apply
- `staleness_flag` — whether the premise has exceeded its review period
- `evidence_artifacts` — links to specific information surfaces that support the premise
- `contradiction_flags` — links to Learning Events that have contradicted this premise
- `last_validated` — when the premise was last confirmed as still valid

**Lifecycle:** Draft → Provisional → Validated → Deprecated (when contradicted by evidence) → Superseded (when replaced by updated premise). A Premise Stack typically contains 3-5 entries for MVP. Not every assumption needs to be formalized — only assumptions whose failure could materially change the decision.

**Relationships:**

- Child of Optimizer State (many:1)
- Referenced by Learning Events (to identify which premise failed)
- Referenced by Decision State (premises that were active when the decision was made)

**Capture trigger:** Created during the Infer step of RIPC. The system identifies assumptions implied by the request and retrieved context. The human confirms, corrects, or adds premises during the Propose step.

**Reuse rules:** Prior premises are retrievable by topic, confidence, status, and linked goal. When surfaced during a new cycle, premises that have been deprecated or contradicted must be visibly flagged. Prior premises that have been validated across multiple cycles may carry higher reuse confidence.

**Campaign brief example:**
- Premise 1: "Workflow burden is a useful attention hook for cardiology administrators." Confidence: Medium. Evidence: prior campaign engagement data. Type: explicit. Boundary: does not establish buying readiness.
- Premise 2: "Practices with existing remote-monitoring reimbursement workflows are higher-priority targets." Confidence: Low. Evidence: sales anecdote, not validated. Type: tacit. Boundary: cardiology segment only.
- Premise 3: "Direct readmissions claims require approved evidence before use." Confidence: High. Evidence: compliance policy. Type: explicit. Boundary: all campaigns.

---

#### Object 3: Decision State

**Purpose:** Preserves what was chosen, what was rejected, and why the available information felt sufficient. Without it, later reviewers see the answer but not the stopping condition that produced it.

**MVP fields (required):**

| Field | Type | Description |
|---|---|---|
| `decision_state_id` | UUID | Unique identifier |
| `optimizer_state_id` | UUID | Links to parent Optimizer State |
| `chosen_action` | text | What was decided — the action taken or artifact produced |
| `rejected_alternatives` | text | What was considered but not chosen, and why |
| `sufficiency_rationale` | text | **Required.** Why investigation stopped. What made the available information feel sufficient for action. |
| `confidence_at_decision` | enum | Low / Medium / High |
| `unresolved_uncertainties` | text | What was still unknown when the decision was made |
| `status` | enum | Active / Archived / Superseded |
| `created_at` | timestamp | When the decision was made |

**Future fields:**

- `active_premise_ids` — explicit links to the premises that were active at decision time
- `information_surfaces_at_decision` — what information surfaces were available
- `investigation_trace_id` — link to the investigation that preceded the decision
- `decision_authority` — who had authority to make this decision
- `consequence_level` — Low / Medium / High / Critical — affects governance requirements

**Lifecycle:** Active (current decision), Archived (after outcome captured), Superseded (if a later decision replaced it).

**Relationships:**

- Child of Optimizer State (1:1 per decision point)
- References Premise Stack entries
- Parent of Investigation Trace (1:1)
- Referenced by Learning Events (what the decision's outcome revealed)

**Capture trigger:** Created when the workflow reaches a decision point — when the system or human commits to an action. The sufficiency rationale is the most important field. "We decided X" is common; "we stopped investigating because Y" is the reasoning that matters.

**Reuse rules:** Prior Decision States are retrievable by decision type, outcome, sufficiency rationale, and linked goal. They surface when a similar decision arises so that prior stopping conditions are visible. A prior Decision State where the sufficiency rationale later proved inadequate (identified by a subsequent Learning Event) is especially valuable — it shows where premature sufficiency occurred.

**Campaign brief example:** Chosen: use workflow-burden messaging without direct readmissions claim. Rejected: direct clinical-outcome language (insufficient evidence per compliance policy). Sufficiency rationale: approved operational claims available; clinical claims require evidence review that has not been completed; campaign timeline does not allow evidence review before launch. Unresolved: whether workflow pain actually indicates buying readiness (not just attention).

---

#### Object 4: Investigation Trace

**Purpose:** Preserves how uncertainty was reduced before action. Without it, the organization becomes vulnerable to after-the-fact rationalization — a final answer that sounds coherent but does not reflect the actual path of uncertainty reduction.

**MVP fields (required):**

| Field | Type | Description |
|---|---|---|
| `trace_id` | UUID | Unique identifier |
| `decision_state_id` | UUID | Links to the decision this investigation supported |
| `questions_asked` | text[] | Questions that drove the investigation |
| `sources_checked` | text[] | Information surfaces consulted |
| `contradictions_found` | text | Conflicting information encountered |
| `evidence_accepted` | text | Evidence that supported the decision path |
| `evidence_rejected` | text | Evidence that was considered but not used, and why |
| `status` | enum | In Progress / Complete / Reopened |
| `created_at` | timestamp | When the investigation began |

**Future fields:**

- `investigation_path` — ordered sequence of investigative steps
- `investigation_duration` — how long the investigation took (relevant to confirmation fatigue analysis)
- `tools_used` — which agent tools or information retrieval methods were used
- `confidence_changes` — how confidence shifted during investigation
- `human_judgment_applied` — where a human overrode or directed the investigation

**Lifecycle:** In Progress (investigation active), Complete (investigation finished and decision made), Reopened (new evidence requires re-investigation).

**Relationships:**

- Child of Decision State (1:1)
- May trigger re-entry into Discovery if investigation reveals new uncertainty
- Referenced by Learning Events (to understand what investigation preceded the outcome)

**Capture trigger:** Created during the investigation phase of a decision. The trace must be created during investigation, not reconstructed after the decision — this is the architectural protection against rationalization.

**Reuse rules:** Prior Investigation Traces are retrievable by investigation topic, sources used, and linked decision. They surface when a similar uncertainty appears so that prior investigation paths are visible — preventing the team from re-investigating questions that have already been answered, and revealing where prior investigation was insufficient.

**Campaign brief example:** Questions: Is "reduces readmissions" an approved claim? What evidence exists for workflow-burden messaging converting to qualified pipeline? Sources checked: approved-claims repository, compliance guidelines, prior campaign reports, sales feedback. Contradictions: prior campaign showed high engagement but sales reported low qualified conversion. Evidence accepted: workflow burden drives attention. Evidence rejected: workflow burden as buying-readiness indicator (sales feedback contradicts).

---

#### Object 5: Learning Event

**Purpose:** Preserves where reality contradicted, qualified, or sharpened the model. Without it, outcomes become anecdotes rather than evidence for model change. A Learning Event is not a reaction ("it didn't work, do something different"). It is a structured record of prediction error plus evidence-supported explanation.

**MVP fields (required):**

| Field | Type | Description |
|---|---|---|
| `event_id` | UUID | Unique identifier |
| `decision_state_id` | UUID | Links to the decision whose outcome triggered learning |
| `prediction` | text | What was expected to happen |
| `outcome` | text | What actually happened |
| `prediction_error` | text | The gap between expected and actual — stated precisely |
| `evidence_supported_explanation` | text | Why the gap occurred, supported by evidence — not narrative or blame |
| `linked_premise_ids` | UUID[] | Which premises failed or need revision |
| `status` | enum | Draft / Provisional / Validated / Rejected |
| `confidence` | enum | Low / Medium / High |
| `created_at` | timestamp | When the learning event was recorded |

**Future fields:**

- `outcome_data_source` — where the outcome data came from
- `prediction_error_category` — classification of the error type (premise failure, goal misalignment, investigation gap, external change)
- `reviewed_by` — who validated the explanation
- `evidence_artifacts` — links to supporting evidence

**Lifecycle:** Draft (outcome recorded, explanation pending), Provisional (explanation proposed), Validated (explanation confirmed with evidence), Rejected (explanation found insufficient or unsupported).

**Relationships:**

- References Decision State and Premise Stack entries
- Parent of Model Update Objects (1:many)
- References Investigation Trace (what investigation preceded the decision that produced this outcome)

**Capture trigger:** Created only when an outcome materially contradicts expectations. Not every outcome gets a Learning Event. A Learning Event is warranted when: (a) the prediction error is significant enough to change future behavior, and (b) the team can identify an evidence-supported explanation for the gap. If the team can only say "it didn't work" without explaining why, the Learning Event remains Draft until investigation produces an explanation.

**Reuse rules:** Prior Learning Events are retrievable by outcome type, prediction-error category, linked premises, and workflow context. They surface when similar decisions are forming so that prior failures are visible. A Learning Event where the explanation has been validated is more authoritative than one that remains provisional.

**Campaign brief example:** Prediction: workflow-burden messaging will generate qualified demo requests from cardiology administrators. Outcome: high engagement (click-through, asset downloads) but low qualified conversion (demo requests that sales classified as ready to evaluate). Prediction error: engagement ≠ buying readiness. Explanation: workflow burden is broadly recognized across practices, so it generates attention, but it does not distinguish practices actively evaluating RPM from those with general frustration. Evidence: sales feedback from 12 demo conversations; 9 of 12 expressed interest but had no timeline or budget for RPM evaluation. Linked premises: Premise 1 (workflow burden as attention hook — validated), Premise 2 (practices with reimbursement workflows as higher priority — insufficient evidence to validate or refute).

---

#### Object 6: Model Update Object (MUO)

**Purpose:** Preserves what reusable change should shape future reasoning. An MUO is not a postmortem note. It is a bounded, reusable record of learning designed to change future reasoning by altering what the next cycle's optimizer sees, trusts, questions, or treats as sufficient. Without MUOs, learning remains local — it lives in one person's memory, one meeting's notes, one campaign's report — and fails to alter future topography.

**MVP fields (required):**

| Field | Type | Description |
|---|---|---|
| `muo_id` | UUID | Unique identifier |
| `learning_event_id` | UUID | Links to the Learning Event that produced this update |
| `update_target` | text | What should change — which aspect of future reasoning (audience model, qualification logic, evidence requirements, policy interpretation, sufficiency criteria) |
| `update_content` | text | The specific change — stated precisely enough to be actionable |
| `evidence_basis` | text | What evidence supports this update |
| `confidence` | enum | Low / Medium / High |
| `applicability_boundary` | text | **Required.** Where this update applies |
| `non_applicability_boundary` | text | **Required.** Where this update does NOT apply |
| `status` | enum | Draft / Provisional / Validated / Deprecated / Superseded / Rejected |
| `created_by` | text | Who created the MUO |
| `reviewed_by` | text (nullable) | Who reviewed and validated the MUO |
| `created_at` | timestamp | When created |

**Future fields:**

- `reuse_count` — how many times this MUO has been retrieved and applied
- `reuse_outcomes` — whether applying this MUO improved outcomes
- `supersedes_muo_id` — link to the MUO this one replaces
- `superseded_by_muo_id` — link to the MUO that replaced this one
- `last_reviewed` — when the MUO was last reviewed for continued validity
- `conflict_flags` — whether this MUO conflicts with other active MUOs

**Lifecycle:** Draft (proposed), Provisional (under review), Validated (approved for reuse), Deprecated (no longer applicable), Superseded (replaced by a newer MUO), Rejected (found incorrect or overgeneralized). MUOs must be human-reviewed before they shape future reasoning. An unreviewed system-generated lesson must not become policy by default.

**Relationships:**

- Child of Learning Event (many:1)
- When applied, creates a link to the future Optimizer State it influenced (the Modified Optimizer State relationship)
- May conflict with other MUOs (conflict detection is a future-phase concern)

**Capture trigger:** Created only when a Learning Event has been validated and the team identifies a reusable change that should shape future reasoning. Not every Learning Event produces an MUO. An MUO is warranted when the learning is reusable — it applies beyond the single instance and can be stated with a clear applicability boundary.

**Reuse rules:** MUOs are the most important retrieval challenge. A relevant MUO must surface when a future decision matches its applicability boundary, not merely when the text is similar. When surfaced, the MUO must be presented with its confidence, applicability boundary, non-applicability boundary, evidence basis, and status. The human must confirm that the MUO applies to the current situation before it shapes the current cycle's reasoning.

**Campaign brief example:** Update target: campaign qualification logic. Update content: future campaigns should distinguish workflow-burden attention from active RPM evaluation readiness. Workflow pain is a valid attention hook, but demo requests generated by workflow pain alone should not be classified as qualified pipeline without additional readiness indicators (active evaluation timeline, reimbursement workflow in place, or budget allocated). Applicability: cardiology practice administrator campaigns targeting RPM adoption. Non-applicability: does not apply to partner enablement, executive education, or general awareness campaigns without further validation. Confidence: Medium (one cycle of evidence — 12 demo conversations, consistent pattern).

---

#### Cross-Object Relationships and Chain Integrity

```text
Optimizer State (1) ──→ (many) Premise Stack entries
Optimizer State (1) ──→ (1) Decision State
Decision State  (1) ──→ (1) Investigation Trace
Decision State  (1) ──→ (many) Learning Events
Learning Event  (1) ──→ (many) Model Update Objects
Model Update Object ──→ (applied to) Future Optimizer State
```

**Referential integrity rules:**

- Every Premise Stack entry must reference an Optimizer State.
- Every Decision State must reference an Optimizer State.
- Every Investigation Trace must reference a Decision State.
- Every Learning Event must reference a Decision State and at least one Premise Stack entry.
- Every MUO must reference a Learning Event.
- When an MUO is applied to a new Optimizer State, the link must be explicit (via `applied_muo_ids`).
- Orphaned reasoning objects (no parent reference) must be flagged for review.
- The chain from Optimizer State through MUO must remain intact for audit. Breaking the chain breaks provenance.

#### Versioning and Immutability

- Reasoning objects are append-only once created. Corrections are new versions, not overwrites.
- Each version carries a timestamp, author, and reason for revision.
- The original version is retained alongside corrections — no silent overwrites.
- Status transitions are logged as lifecycle events, not as mutations of the original record.

---

### Chapter 4 — Supporting Data Objects

Supporting data objects are not reasoning objects. They do not represent optimizer state transitions. They support the six core reasoning objects by recording what information was available, what governance actions occurred, what outcomes were observed, and what retrieval patterns proved useful.

---

#### Object: Information Surface Record

**Purpose:** Registers what information sources exist, their type, authority, recency, and accessibility. Information surfaces are the raw material from which reasoning is constructed. Without a registry, the system cannot assess retrieval completeness — it cannot know what it failed to find because it does not know what exists.

**MVP fields:**

| Field | Type | Description |
|---|---|---|
| `surface_id` | UUID | Unique identifier |
| `name` | text | Human-readable name |
| `type` | enum | document / policy / data_source / report / transcript / tool_output / external_system |
| `domain` | text | Subject area (e.g., "healthcare marketing," "compliance," "sales feedback") |
| `authority` | enum | primary / secondary / informal | How authoritative is this source? |
| `owner` | text | Who maintains this information surface |
| `last_updated` | timestamp | When the content was last updated |
| `accessibility` | enum | direct / requires_request / restricted | How easily can the system access this surface? |
| `registered_at` | timestamp | When this surface was added to the registry |

**Future fields:** `recency_score`, `retrieval_frequency`, `linked_reasoning_object_ids` (which reasoning objects were informed by this surface), `quality_notes`, `staleness_threshold`.

**Lifecycle:** Active (available for retrieval), Inactive (exists but not currently available), Retired (no longer maintained).

**Relationship to Martin / co-worker:** Co-worker indexes enterprise data systems (Salesforce, Zendesk, JIRA, Slack). Each indexed system is an information surface. The registry should be able to register co-worker-accessible surfaces without requiring them to conform to PTF schema — a pointer record ("co-worker can access Salesforce deal data") is sufficient for MVP.

*Grounding example: The RapidSOS Marketing Context Layer maintained 44 seed knowledge chunks across 5 categories (brand_voice, competitive, icp, messaging, playbook), each with YAML front-matter specifying category, title, vertical, and update date. These are information surface records. The PTF registry is more general — it registers any information source, not only marketing knowledge.*

---

#### Object: Outcome Record

**Purpose:** Records what happened after the decision. Outcome records are the raw material for Learning Events. Without outcomes, the system cannot detect prediction errors.

**MVP fields:**

| Field | Type | Description |
|---|---|---|
| `outcome_id` | UUID | Unique identifier |
| `decision_state_id` | UUID | Links to the decision this outcome follows |
| `outcome_description` | text | What actually happened |
| `outcome_data_source` | text | Where the outcome data came from |
| `recorded_by` | text | Who recorded the outcome |
| `created_at` | timestamp | When the outcome was recorded |

**Future fields:** `outcome_metrics` (structured quantitative data), `outcome_category` (success / partial / failure / ambiguous), `time_to_outcome` (how long between decision and observable outcome).

**Lifecycle:** Recorded (captured), Linked (connected to a Learning Event), Archived.

---

#### Object: Governance Audit Record

**Purpose:** Logs every governance-relevant action on reasoning objects — creation, confirmation, rejection, state transitions, modifications. Without audit records, the reasoning-state layer cannot demonstrate that governance controls are operating.

**MVP fields:**

| Field | Type | Description |
|---|---|---|
| `audit_id` | UUID | Unique identifier |
| `reasoning_object_id` | UUID | Which reasoning object was affected |
| `reasoning_object_type` | enum | optimizer_state / premise / decision_state / investigation_trace / learning_event / muo |
| `action` | enum | created / confirmed / rejected / validated / deprecated / superseded / modified / archived |
| `from_status` | enum (nullable) | Status before the action |
| `to_status` | enum (nullable) | Status after the action |
| `performed_by` | text | Who performed the action |
| `role` | text | What role they held when performing the action |
| `reason` | text (nullable) | Why the action was taken |
| `timestamp` | timestamp | When the action occurred |

**Future fields:** `authority_scope` (what authority justified this action), `evidence_cited` (what evidence supported the transition), `workflow_context` (which workflow instance this occurred in).

**Lifecycle:** Audit records are immutable. They are never modified or deleted. They may be archived after a retention period.

---

#### Object: Discovery Pattern Record

**Purpose:** Records which interaction patterns produce valuable confirmations for a given workflow type. Discovery Patterns allow the RIPC loop to improve over time — asking better questions, inferring more accurately, and proposing more useful candidate reasoning states.

**MVP fields:** Not implemented in MVP. Static question sets per workflow type are sufficient initially.

**Future fields:**

| Field | Type | Description |
|---|---|---|
| `pattern_id` | UUID | Unique identifier |
| `workflow_type` | text | Which workflow type this pattern applies to |
| `question_template` | text | The question or inference pattern |
| `confirmation_value` | enum | high / medium / low | How valuable confirmations from this question tend to be |
| `frequency` | integer | How often this pattern has been used |
| `correction_rate` | float | How often humans correct the inference from this pattern |
| `created_at` | timestamp | When the pattern was first identified |
| `last_used` | timestamp | When the pattern was last applied |

**Lifecycle:** Active (currently used in RIPC), Dormant (not recently effective), Retired (replaced by a better pattern).

**Open question (OAD-10):** Should Discovery Patterns be static configuration per workflow type (MVP) or dynamic patterns that update based on confirmation quality (future)?

---

#### Object: Retrieval-Relevance Metadata

**Purpose:** Records why a reasoning object was surfaced during retrieval, what its match rationale was, and whether the human confirmed or rejected its applicability. Over time, this metadata enables retrieval quality improvement.

**MVP fields:** Match rationale is displayed at retrieval time (Chapter 6) but not stored as a separate object in MVP. The confirmation record in the Governance Audit log captures whether the human accepted or rejected the surfaced reasoning.

**Future fields:**

| Field | Type | Description |
|---|---|---|
| `retrieval_id` | UUID | Unique identifier |
| `reasoning_object_id` | UUID | Which reasoning object was retrieved |
| `query_context` | text | What the retrieval query was |
| `match_rationale` | text | Why the system believed this object was relevant |
| `relevance_score` | float | System-assessed relevance |
| `human_judgment` | enum | confirmed / rejected / qualified / not_reviewed |
| `reuse_outcome` | enum (nullable) | improved / neutral / degraded / unknown | Did reusing this reasoning improve the outcome? |
| `timestamp` | timestamp | When retrieval occurred |

**Lifecycle:** Recorded at retrieval time. Updated when human judgment and reuse outcome are known.

**Martin compatibility notes:** Co-worker indexes enterprise data (Salesforce, Zendesk, JIRA, Slack). These are information surfaces in PTF terms. The Information Surface Record registry can register co-worker-accessible surfaces without requiring them to conform to the PTF schema — a pointer record is sufficient.

---

## Part III: Service Architecture

### Chapter 5 — Discovery / RIPC Service Pattern

Discovery is the process by which compressed human intent becomes structured, confirmed reasoning state. It is the primary interaction pattern of the system. It is not a chatbot exchange, not a form, and not a single API call. It is a multi-step service pattern where the system does the reasoning work first and asks the human to confirm only what matters.

The core loop:

```text
Retrieve → Infer → Propose → Confirm
```

Discovery differs from ordinary intake in a specific way: ordinary intake asks the human to provide information. Discovery infers what it can from existing surfaces, proposes a candidate reasoning state, and asks the human to confirm, correct, reject, qualify, or bound the interpretation. The human corrects a draft rather than filling a blank form.

---

#### Step 1: Retrieve

**Service responsibility:** Gather relevant information surfaces and prior reasoning objects for the current decision context.

**Inputs:**

- Workflow context (type, requester, domain)
- Initial request text
- Workflow history (prior instances of this workflow type)

**Outputs:**

- Retrieved information surfaces (documents, policies, prior work, data, reports)
- Retrieved prior reasoning objects (Optimizer States, Premise Stacks, Decision States, MUOs from prior cycles)
- Relevance scores and match rationale for each retrieved item
- Applicability assessments (does the prior reasoning claim to apply to the current context?)

**What gets written to reasoning-state objects:** Retrieval log — what was retrieved, what was omitted, and why. The retrieval log must be inspectable by humans but does not require human interaction at this step.

**Human confirmation points:** None. Retrieve is system-only. However, the retrieval log must be inspectable.

**How this differs from a chatbot exchange:** A chatbot retrieves documents to augment a response. Retrieve surfaces prior reasoning objects — including goals, premises, decisions, sufficiency rationale, investigation traces, and model updates — so the system can infer a provisional reasoning state, not just a better prompt.

**Failure modes:**

- False negative: relevant prior reasoning exists but is not retrieved (the system starts cold when it should not)
- False positive: irrelevant reasoning is surfaced and anchors the system toward a wrong interpretation
- Volume overload: too many results create cognitive burden rather than reducing it
- Staleness: prior reasoning is retrieved as current when conditions have changed

**Governance controls:** Retrieval must respect lifecycle status — do not retrieve Deprecated or Rejected reasoning without flagging it. Retrieval must surface provenance so the Infer step can assess trustworthiness.

---

#### Step 2: Infer

**Service responsibility:** Construct a provisional reasoning state from retrieved information and the current request. The system does the reasoning work before asking the human to do it.

**Inputs:**

- Retrieved information surfaces and prior reasoning objects from Step 1
- Current request text
- Workflow context

**Outputs:**

- Draft Optimizer State (inferred goal, policy scope, interpretation)
- Draft Premise Stack (inferred assumptions — typically 3-5)
- Provisional confidence levels for each inferred element
- Identified uncertainties — where the system lacks confidence
- Identified gaps — what information surfaces are missing

**What gets written to reasoning-state objects:** Draft Optimizer State and Draft Premise Stack, both marked as `source_type: system-inferred` and `status: Draft`. These must remain visibly provisional.

**Human confirmation points:** None. Infer is system-only. The critical requirement is that inferred reasoning is never treated as confirmed.

**How this differs from a chatbot exchange:** A chatbot generates a response from retrieved context. Infer constructs a candidate reasoning state — a structured representation of what the system believes the goal, assumptions, boundaries, and uncertainties are. The output is not text to deliver; it is reasoning to confirm.

**Failure modes:**

- System infers a plausible-but-wrong goal (compressed request is misinterpreted)
- System treats its interpretation as confirmed (missing the Draft boundary)
- System anchors toward a prior reasoning object that does not apply here
- System fails to flag low-confidence inferences
- System treats non-response as confirmation

**Governance controls:** All inferred reasoning must be marked as Draft. The system must not act on inferred reasoning without human confirmation. Inference must surface uncertainty, not hide it.

---

#### Step 3: Propose

**Service responsibility:** Present the candidate reasoning state to the human in a form that supports confirmation, correction, rejection, qualification, or bounding.

**Inputs:**

- Draft Optimizer State and Draft Premise Stack from Step 2
- Identified uncertainties and gaps
- Relevant prior reasoning with provenance (especially prior MUOs with applicability assessments)

**Outputs:**

- A human-readable proposal that includes:
  - Inferred goal and interpretation
  - Inferred assumptions (the Premise Stack)
  - Confidence levels for each element
  - Prior reasoning being reused, with applicability assessment and provenance
  - Identified uncertainties
  - Specific questions for the human — focused on reasoning whose absence could materially change the goal, boundary, investigation, sufficiency condition, or action

**What gets written to reasoning-state objects:** Proposal record — what was proposed, when, to whom.

**Human confirmation points:** **This is the primary human interaction point.** The human must be able to:

- Confirm the reasoning ("yes, that is the goal")
- Correct specific elements ("the goal is awareness, not qualified pipeline")
- Reject the entire interpretation ("you are asking the wrong question")
- Qualify with additional boundaries ("only for practices with existing reimbursement workflows")
- Bound the applicability ("this is for current cardiology campaign only")
- Add information the system does not have ("sales told us practices are not evaluating RPM this quarter")
- Identify that the proposal is asking the wrong question (triggers re-entry)

**How this differs from a chatbot exchange:** A chatbot presents a finished draft for approval. Propose presents a candidate reasoning state for correction. The human is not editing output; the human is shaping the reasoning that will produce the output. The proposal is designed to invite challenge, not agreement.

**Failure modes:**

- Proposal is too complex for the human to evaluate (information overload defeats the purpose)
- Proposal uses framework jargon instead of plain language
- Proposal anchors the human toward accepting the system's interpretation (the system presents its inference too confidently)
- Proposal does not expose enough uncertainty for the human to make an informed judgment
- Confirmation fatigue leads to rubber-stamping

---

#### Step 4: Confirm

**Service responsibility:** Record the human's response and update reasoning objects accordingly.

**Inputs:**

- Human response (confirmation, correction, rejection, qualification, bounding, re-entry request)

**Outputs:**

- Updated Optimizer State — status changed from Draft to Provisional (or Validated if the confirmer has sufficient authority)
- Updated Premise Stack — status changed from Draft to Provisional or Validated
- Confirmation record — who confirmed, what they confirmed, what they changed, what authority they held, what scope the confirmation covers
- Re-entry signal — if the human's response reveals new uncertainty that requires another Retrieve → Infer → Propose cycle

**What gets written to reasoning-state objects:** Updated Optimizer State and Premise Stack with new status. Confirmation record linked to the reasoning objects it governs. If corrections were made, the Draft versions are retained as prior versions (append-only; no overwrites).

**Human confirmation points:** This step records the human's judgment. The human has already interacted in Step 3.

**How this differs from a chatbot exchange:** A chatbot records "user approved the draft." Confirm records what reasoning was accepted, what was corrected, what authority the confirmer held, what scope the confirmation covers, and what remains unresolved. The confirmation is linked to specific reasoning objects, not to a text output.

**Failure modes:**

- Human confirms without reading (confirmation fatigue / automation bias)
- Human lacks authority to confirm the reasoning (wrong person in the loop)
- Confirmation is recorded but not linked to the reasoning objects it governs
- Human correction is lost because the system overwrites rather than versions

---

#### Re-Entry Logic

Confirmation may reveal that the system needs to re-enter the loop. Re-entry happens when:

- The human provides information that changes the goal or interpretation fundamentally
- The human identifies that a critical information surface was not retrieved
- The human rejects the entire framing and the system needs to start from a different premise
- The human's correction creates a new uncertainty that was not previously visible

Re-entry is not failure. It is the system learning from human feedback within the current decision cycle. Re-entry creates a new Retrieve → Infer → Propose → Confirm cycle with updated context. Prior Draft reasoning objects are retained as version history.

---

#### Confirmation Fatigue and Automation Bias Mitigation

These are first-class design concerns, not edge cases.

| Risk | Mitigation direction | MVP implementation |
|---|---|---|
| Confirmation fatigue | Minimize confirmation requests to those that materially affect the decision. Reduce review burden for already-validated reasoning, but do not allow silent reuse. | MVP: confirm the initial Optimizer State and Premise Stack. For prior MUOs that have been Validated and are within their applicability boundary, do not require full re-review, but still require lightweight applicability acknowledgment before the MUO shapes the current decision. The human must see the MUO, its applicability boundary, non-applicability boundary, confidence, provenance, and status, then acknowledge that it applies to the current workflow instance. Validated reasoning earns reduced burden, not silent application. |
| Automation bias | Expose the system's uncertainty and the inferential basis for its proposal. Do not present proposals as conclusions. Make correction and rejection as easy as confirmation. | MVP: every Propose screen shows confidence levels and flags system-inferred elements. Correction and rejection are single-action operations, not multi-step workflows. |
| Rubber-stamping detection | Track whether humans are confirming without meaningful review (confirmation time < reading time). | Future phase. Requires enough confirmation data to establish baselines. |

---

### Chapter 6 — Reasoning-Relevant Retrieval Architecture

This is the core implementation challenge of the HLD. If this chapter is weak, the architecture reduces to ordinary RAG with extra metadata. The paper's central implementation claim is that reasoning-relevant retrieval is technically and architecturally harder than ordinary semantic retrieval. This chapter must substantiate that claim.

---

#### How Reasoning-Relevant Retrieval Differs from Semantic Document Retrieval

| Dimension | Ordinary Semantic Retrieval | Reasoning-Relevant Retrieval |
|---|---|---|
| **Question asked** | What documents sound similar to this request? | What prior reasoning is relevant to this decision? |
| **Match basis** | Text similarity (embedding distance) | Goal, policy scope, premise, confidence, applicability, provenance, workflow context, outcome history |
| **Returns** | Document chunks or passages | Reasoning objects with structured metadata about why they matter |
| **Ranking** | Similarity score | Reasoning relevance: how closely the prior decision context matches the current one |
| **Human role** | User reads and interprets results | System presents match rationale; human confirms applicability before reuse |
| **Reuse tracking** | None | Tracks whether reused reasoning improved the next cycle |
| **Status awareness** | None (all documents are equally current) | Lifecycle status distinguishes Draft, Provisional, Validated, Deprecated, Superseded |

---

#### Retrieval Inputs

When a retrieval request is made (during the Retrieve step of RIPC), the following inputs shape the query:

- **Current workflow context** — workflow type, domain, requester, stage
- **Current Optimizer State** — even as a Draft, the inferred goal and interpretation constrain what prior reasoning is relevant
- **Request text** — natural language query for semantic matching
- **Structured filters** — goal keywords, policy scope, audience segment, workflow type
- **Negative filters** — exclude reasoning whose non-applicability boundaries match the current context

---

#### Indexable Fields

Every reasoning object must carry structured metadata that supports retrieval beyond text similarity.

| Field | Purpose | Object(s) |
|---|---|---|
| `goal` / working objective | Find prior reasoning with similar objectives | Optimizer State |
| `policy_scope` | Find prior reasoning governed by similar constraints | Optimizer State |
| `premise_statements` | Find prior reasoning that shared similar working assumptions | Premise Stack |
| `confidence_level` | Filter by how confident the prior reasoning was | All objects |
| `evidence_basis` | Find prior reasoning supported by similar or overlapping evidence | Premise Stack, Learning Event, MUO |
| `applicability_boundary` | Filter by where the prior reasoning claims to apply | Premise Stack, MUO |
| `non_applicability_boundary` | Exclude prior reasoning that explicitly does not apply here | MUO |
| `workflow_context` | Find prior reasoning from the same or similar workflow type | Optimizer State |
| `audience` / segment | Find prior reasoning about similar audiences or operating conditions | Optimizer State |
| `outcome` (if available) | Find prior reasoning where the outcome is known | Learning Event |
| `status` | Filter by lifecycle status | All objects |
| `provenance` (created_by, confirmed_by, reviewed_by) | Show who created and confirmed the reasoning | All objects |
| `reuse_history` (future) | Show whether the reasoning has been reused before and whether reuse improved outcomes | MUO |
| `prediction_error_category` (future) | Find prior reasoning that failed in a similar way | Learning Event |

---

#### Metadata Filters

The retrieval system must support queries that combine:

1. **Semantic search** — find reasoning objects whose text is similar to the current request
2. **Structured metadata filters** — narrow results by goal, policy scope, applicability boundary, confidence, status, workflow type, audience, and provenance
3. **Negative filters** — exclude reasoning objects whose non-applicability boundaries match the current context
4. **Status filters** — distinguish Draft, Provisional, Validated, Deprecated, Superseded, and Rejected reasoning. Default: surface only Provisional and Validated. Flag Deprecated if surfaced for context.
5. **Recency and staleness weighting** — weight more recent reasoning higher; flag reasoning that has not been validated since its last review period

**MVP retrieval:** Semantic search + metadata filters on goal keywords, workflow type, and lifecycle status. Negative filtering on non-applicability boundaries. This is simpler than the full specification but architecturally distinct from pure semantic retrieval because it uses structured metadata, not just embeddings.

---

#### Applicability and Non-Applicability Boundaries in Retrieval

Applicability boundaries are the primary mechanism for preventing false-analogy reuse. When the system retrieves a prior reasoning object:

1. The system checks whether the current context falls within the object's applicability boundary.
2. The system checks whether the current context matches any non-applicability boundary.
3. If there is a non-applicability match, the object is either excluded from results or surfaced with a visible warning: "This reasoning explicitly excludes your current context."
4. If there is an applicability match, the object is surfaced with its boundary displayed so the human can confirm fit.
5. If neither boundary matches (the current context is ambiguous), the object is surfaced with a flag: "Applicability to your current context is uncertain — confirm before use."

---

#### Confidence and Provenance Display

When reasoning objects are surfaced during retrieval, the user must see:

- **Content** — what the prior reasoning says
- **Match rationale** — why the system thinks it is relevant ("matched on similar goal and same workflow type"; "prior campaign targeted the same audience segment")
- **Confidence** — how confident the prior reasoning was (Low / Medium / High)
- **Provenance** — who created it, who confirmed it, when
- **Applicability boundaries** — where it claims to apply and where it does not
- **Lifecycle status** — Draft, Provisional, Validated, Deprecated, Superseded
- **Reuse history** (future) — whether it has been reused before and whether reuse improved outcomes

---

#### False-Analogy Prevention

| Failure Mode | Architectural Prevention |
|---|---|
| System retrieves semantically similar text that is not reasoning | Reasoning objects are stored with structured metadata. Retrieval from the reasoning-state store returns objects with metadata, not text chunks. |
| System retrieves relevant reasoning but does not show why it matters | Every retrieved reasoning object must be presented with its match rationale, not just its content. |
| System reuses prior reasoning without human confirmation | Human confirmation is required before prior reasoning shapes the current decision (Principle 4). |
| System treats all retrieved reasoning as equally authoritative | Lifecycle status and confidence levels distinguish Draft from Validated, high-confidence from low-confidence, recent from stale. |
| System retrieves deprecated or superseded reasoning | Status filters exclude deprecated/superseded by default. If surfaced for context, they must be visibly marked. |
| System applies a lesson beyond its applicability boundary | Applicability boundaries are displayed. The human confirms boundary match. Non-applicability boundaries trigger exclusion or warning. |
| System treats a single-instance lesson as a universal rule | MUO confidence and reuse history indicate how many cycles have validated the lesson. A single-instance MUO (confidence: Low or Medium, reuse_count: 0) must be flagged as untested. |

---

#### When Not to Retrieve or Reuse Prior Reasoning

- When the workflow is genuinely novel and no prior reasoning applies
- When all relevant prior reasoning is Deprecated or Superseded
- When the applicability boundary of prior reasoning does not match the current context
- When the prior reasoning was created under different policy constraints that no longer apply
- When the human explicitly rejects the relevance of prior reasoning
- When retrieval would anchor the system toward a prior interpretation that constrains fresh investigation (the "anchoring trap" — a strong prior may prevent the team from seeing a new problem)

---

#### Relationship to Ordinary RAG

Reasoning-relevant retrieval does not replace ordinary RAG. It operates alongside it.

| Layer | What it retrieves | Example |
|---|---|---|
| **Document retrieval (RAG)** | Documents, policies, reports, data, artifacts | "Find the approved claims list for healthcare campaigns" |
| **Reasoning-state retrieval** | Prior reasoning objects — goals, premises, decisions, sufficiency rationale, investigation traces, learning events, model updates | "Find prior reasoning about campaigns targeting cardiology administrators where the sufficiency rationale involved evidence boundaries" |

Both retrieval layers feed into the Discovery loop. Document retrieval provides information surfaces. Reasoning-state retrieval provides prior reasoning state. The Infer step uses both to construct a provisional reasoning state.

---

#### Relationship to Martin / Co-Worker Retrieval

Co-worker indexes enterprise data — what happened in Salesforce, what's in Zendesk tickets, what's in Slack threads. This is information surface retrieval, not reasoning-state retrieval.

The relationship:

- Co-worker data feeds into the reasoning-state layer as **information surfaces** — inputs to reasoning, not reasoning itself.
- A co-worker result ("customer X had 4 support tickets about billing in the last month") may inform a premise ("this customer is likely frustrated with billing") but it is not itself a premise. The premise requires interpretation, confidence, and confirmation.
- Retrieval queries from the reasoning-state layer could route through the model router for cost optimization (retrieval queries on cheaper models, generation on more capable models).
- The two retrieval systems should be composable: a single Discovery loop can draw from both co-worker data and the reasoning-state store.

---

### Chapter 7 — Learning-Loop Architecture

Learning is the mechanism by which outcomes change future reasoning. Without it, the system produces output but never improves. The learning loop is not a post-campaign retrospective or a lessons-learned document. It is a structured pipeline that moves from outcome through prediction error, investigation, evidence-supported explanation, and reusable model change.

The critical distinction: **learning is not reaction.** Reaction says "it didn't work, try something different." Learning says "we expected X, got Y, investigated why, and identified an evidence-supported explanation that should change how future reasoning handles this situation." The architecture must enforce this distinction.

---

#### Learning-Loop Pipeline

```text
Outcome Capture → Prediction-Error Detection → Investigation →
Evidence-Supported Explanation → Learning Event → MUO Creation →
MUO Retrieval in Next Cycle → Human Confirms Applicability →
Modified Optimizer State
```

---

#### Stage 1: Outcome Capture

**Service responsibility:** Record what happened after the decision was executed.

**Inputs:** Decision State (what was decided), workflow completion signal, outcome data from analytics, CRM, sales feedback, user behavior, or other observable sources.

**Outputs:** Outcome Record (see Chapter 4) linked to the Decision State.

**MVP implementation:** Manual outcome capture. A human records the outcome after the workflow completes. The system provides a structured form with the Decision State's prediction visible for comparison.

**Future implementation:** Semi-automated outcome capture. Analytics systems push outcome data. The system compares the outcome to the prediction and flags potential prediction errors for human review.

**Governance requirement:** The outcome record must capture who recorded it, when, and what data source it came from. Outcome records are not reasoning objects — they are inputs to reasoning. They do not require the same lifecycle governance as reasoning objects, but they must be traceable.

---

#### Stage 2: Prediction-Error Detection

**Service responsibility:** Compare the expected outcome (from the Decision State's prediction/sufficiency rationale and the Premise Stack) to the actual outcome. Identify the gap.

**Inputs:** Outcome Record, Decision State (what was expected), Premise Stack (what assumptions supported the expectation).

**Outputs:** Prediction-error assessment: whether the gap is significant enough to warrant investigation.

**MVP implementation:** Manual comparison. The system displays the outcome alongside the prediction and premises. The human decides whether the gap is material.

**Future implementation:** Automated detection. The system compares structured outcome metrics to expected ranges derived from the Premise Stack and flags significant deviations.

**Key design rule:** Not every outcome gets a Learning Event. Only outcomes that materially contradict expectations warrant the investigation overhead. A campaign that performs within expected ranges does not need a Learning Event, even if performance was mediocre. The trigger is prediction error — the gap between what was expected and what occurred — not dissatisfaction.

---

#### Stage 3: Investigation

**Service responsibility:** Support the team in moving from prediction error to explanation. Why did the outcome differ from the prediction? Which premise failed? Was the goal misaligned? Was information missing? Did external conditions change?

**Inputs:** Prediction-error assessment, Decision State, Premise Stack, Investigation Trace (from the original decision), relevant information surfaces.

**Outputs:** Evidence gathered, premises tested, candidate explanations developed.

**MVP implementation:** Human-driven investigation. The system surfaces the original Premise Stack and Investigation Trace so the team can identify which assumption failed. The system may assist by retrieving additional information surfaces.

**Future implementation:** System-assisted investigation. The system proposes candidate explanations based on the Premise Stack ("Premise 2 appears contradicted by sales feedback — workflow burden did not predict buying readiness"), and the human confirms, corrects, or rejects the explanation.

**Governance requirement:** Investigation must be contemporaneous, not reconstructed after the fact. The architecture must make it easy to record investigative steps incrementally. After-the-fact rationalization is the primary failure mode of organizational learning.

---

#### Stage 4: Evidence-Supported Explanation

**Service responsibility:** Formalize the explanation. The explanation must identify which premise or assumption failed, what evidence supports the explanation, and what should change.

**What a good explanation contains:**
- Which premise was wrong or incomplete
- What evidence contradicts the premise
- Whether the failure was local (this instance only) or structural (likely to recur)
- What the explanation implies for future reasoning

**What a weak explanation looks like:**
- "It didn't work." (No premise identified, no evidence cited.)
- "We need better targeting." (Action recommendation without diagnostic.)
- "The market changed." (Untested attribution without evidence.)

**MVP implementation:** The human writes the explanation as a text field in the Learning Event, linking to specific premises by ID. The system enforces that at least one premise is linked.

**Future implementation:** The system proposes a structured explanation template based on the Premise Stack and prediction error. The human confirms, corrects, or replaces.

---

#### Stage 5: Learning Event Creation

**Service responsibility:** Create a formal Learning Event record that preserves the prediction, outcome, prediction error, and evidence-supported explanation. (See Chapter 3, Object 5 for full specification.)

**Governance requirement:** Learning Events start as Draft. They require human review before promotion to Provisional or Validated. A validated Learning Event is one where the explanation has been confirmed by evidence and reviewed by a domain expert.

---

#### Stage 6: MUO Creation

**Service responsibility:** If the learning is reusable — it applies beyond the single instance — create a Model Update Object. (See Chapter 3, Object 6 for full specification.)

**Not every Learning Event produces an MUO.** A Learning Event may identify a local anomaly (a one-time external event, a data error, an unusual customer) that does not warrant a reusable model change. An MUO is created only when the team identifies a structural lesson that should shape future reasoning for similar decisions.

**Governance requirement:** MUOs must be human-created and human-reviewed before they can be applied to future cycles. An unreviewed system-generated lesson must not become policy by default. This is the primary protection against policy laundering (Risk 8 in Chapter 14).

---

#### Stage 7: MUO Retrieval and Reuse

**Service responsibility:** When the workflow repeats, the Retrieve step of RIPC surfaces relevant MUOs. (See Chapter 6 for retrieval architecture.)

The human must see the MUO's applicability boundary, non-applicability boundary, confidence, provenance, and status, then provide lightweight applicability acknowledgment before the MUO shapes the current cycle's reasoning (per Principle 4 and the confirmation-fatigue correction in Chapter 5).

---

#### Stage 8: Effectiveness Tracking

**Service responsibility:** After the MUO has been applied and the next cycle completes, compare: did the next cycle avoid the prior failure? Did the preserved reasoning reach the right moment? Did the outcome improve?

**MVP implementation:** Manual comparison. The team assesses whether the MUO made a difference.

**Future implementation:** Structured effectiveness tracking. The system records which MUOs were applied to which cycles and whether outcomes improved, remained neutral, or degraded. Over time, this data informs retrieval ranking (MUOs with strong effectiveness evidence rank higher).

---

#### Open Questions

- When is a prediction error significant enough to warrant a Learning Event vs. noise?
- How is "effectiveness" measured without controlled experiments? (Direction: before/after comparison across cycles with the same workflow type, not formal A/B testing.)
- What prevents MUO accumulation without review? (Direction: governance — MUOs require human review; staleness detection flags unreused MUOs; retirement policy for MUOs that have never been reused.)

**Martin compatibility notes:** If Beacon skills produce outputs with observable outcomes, those outcomes could feed the learning loop through the Outcome Record interface. The outcome-capture interface should be generic — not coupled to a specific skill framework or analytics platform.

---

## Part IV: Governance and Operations

### Chapter 8 — State Lifecycle Model

The lifecycle model governs how reasoning objects move through states, who can trigger transitions, and what evidence is required. Without lifecycle governance, reasoning objects become permanent truths or invisible assumptions. Both are dangerous.

---

#### Lifecycle States

**MVP (three states):**

| State | Definition | Who can create | Evidence required |
|---|---|---|---|
| **Draft** | System-inferred or human-initiated reasoning that has not been confirmed. May be wrong. Must be visibly marked as unconfirmed. | System (via inference) or any user | None — automatic on creation |
| **Provisional** | Reasoning that has been proposed and confirmed by a human but has not yet been validated by outcome evidence or authoritative review. | N/A (transition only) | Human confirmation of plausibility. Confirmation record required: who confirmed, what they confirmed, what they changed. |
| **Validated** | Reasoning that has been confirmed by an authorized human and, where applicable, supported by outcome evidence. | N/A (transition only) | Outcome evidence or authoritative review. Reviewer identity and evidence cited must be recorded. |

**Future (full seven states):**

| State | Definition | Transition trigger |
|---|---|---|
| **Draft** | Unconfirmed reasoning | Automatic on creation |
| **Provisional** | Human-confirmed but not outcome-validated | Human confirms during RIPC |
| **Validated** | Outcome-supported or authority-confirmed | Reviewer validates with evidence |
| **Deprecated** | Once valid, no longer current. World changed, policy changed, or assumption contradicted. | Evidence of changed conditions. Retained for audit; not surfaced as active guidance. |
| **Superseded** | Explicitly replaced by newer reasoning. The superseding object must link to the superseded one. | New reasoning object created with supersession link. |
| **Rejected** | Proposed but found incorrect, overgeneralized, or unsupported. | Reviewer rejects with reason. Retained for audit; not surfaced as guidance. |
| **Archived** | Aged past relevance window. Retained for compliance and historical analysis. | Retention period elapsed or manual archive decision. |

---

#### Allowed Transitions

```text
Draft → Provisional       (human confirms)
Draft → Rejected          (human or reviewer rejects)
Provisional → Validated   (reviewer validates with evidence)
Provisional → Rejected    (reviewer rejects)
Provisional → Draft       (confirmer withdraws confirmation — rare but allowed)
Validated → Deprecated    (evidence of changed conditions)
Validated → Superseded    (new reasoning object replaces it)
Deprecated → Archived     (retention period elapsed)
Superseded → Archived     (retention period elapsed)
Rejected → Archived       (retention period elapsed)
```

**Transitions that are NOT allowed:**

- Deprecated → Validated (deprecated reasoning cannot be re-validated without creating a new object)
- Rejected → Validated (rejected reasoning cannot be promoted without creating a new object)
- Any state → Draft (once reasoning has been confirmed, it cannot revert to Draft — corrections create new versions)

---

#### Who Can Transition Objects

| Transition | Authorized roles (MVP) | Authorized roles (Future) |
|---|---|---|
| Draft → Provisional | Requester (own workflow), Domain Expert | + Reviewer |
| Draft → Rejected | Domain Expert, Governance Owner | + Reviewer |
| Provisional → Validated | Domain Expert, Governance Owner | + Reviewer with authority scope |
| Provisional → Rejected | Domain Expert, Governance Owner | + Reviewer |
| Validated → Deprecated | Domain Expert, Governance Owner | + System (via staleness detection) |
| Validated → Superseded | Domain Expert, Governance Owner | + Author of superseding reasoning |
| Any → Archived | Governance Owner | + System (via retention policy) |

---

#### Evidence Required for Transitions

| Transition | Evidence requirement |
|---|---|
| Draft → Provisional | Human confirmation. The confirmation record must capture: who, what, when, what authority, what scope. |
| Provisional → Validated | Outcome evidence OR authoritative review. The validation record must capture: what evidence, who reviewed, what scope of validation. |
| Validated → Deprecated | Evidence of changed conditions: contradicting outcome, policy change, market shift, or new information. The deprecation record must capture: why, who, what triggered it. |
| Validated → Superseded | The superseding reasoning object must exist and be at least Provisional. The supersession record must link old and new objects. |
| → Rejected | Explanation of why the reasoning is incorrect or unsupported. The rejection record must capture: why, who, what evidence. |

---

#### Staleness Triggers

The architecture must detect stale reasoning. Stale reasoning should be flagged for review, not automatically deprecated.

| Indicator | What it means |
|---|---|
| Time since last validation exceeds the workflow's review period | The reasoning has not been checked recently |
| Policy or regulatory context has changed since creation | External conditions may invalidate the reasoning |
| Reasoning has been reused but outcomes have not been tracked | The system is relying on the reasoning without knowing if it still works |
| Reasoning references information surfaces that have been updated since creation | The evidence basis may have changed |
| Reasoning has not been accessed or retrieved in a defined period | The reasoning may no longer be relevant |

**MVP implementation:** Manual staleness review. The system flags reasoning objects older than the workflow's review period (configurable). A human reviews and decides whether to revalidate, deprecate, or update.

**Future implementation:** Automated staleness detection with notification to the governance owner or domain expert.

---

#### Supersession Behavior

When reasoning is superseded:

1. The superseding object must reference the superseded object (explicit link).
2. The superseded object remains in the store, marked Superseded.
3. Retrieval defaults to surfacing the superseding object. The superseded object may be surfaced for historical context if requested.
4. During the transition period, both objects may be visible so the human can compare.
5. If the superseding object is later Rejected, the superseded object does not automatically revert to Validated — a new assessment is required.

---

#### How Sufficiency Gates Relate to Lifecycle Transitions

Sufficiency is the moment where investigation stops and action begins. In lifecycle terms:

- **Before sufficiency:** The system is in the RIPC loop. Reasoning objects are being created, refined, and confirmed (Draft → Provisional transitions).
- **At sufficiency:** The Decision State is created with a sufficiency rationale. The system commits to action. This is a lifecycle event — the workflow moves from "reasoning formation" to "action."
- **After action:** Outcomes are observed. If outcomes contradict expectations, a Learning Event is created. This may trigger Deprecated transitions on premises that failed and Superseded transitions on MUOs that are replaced.

Sufficiency gates are the system's mechanism for making premature sufficiency harder:

| Gate | What it checks | What happens if the check fails |
|---|---|---|
| Unsupported-claim check | Are there claims in the decision artifact that are not supported by evidence in the Premise Stack? | System flags the claim and blocks the sufficiency transition until the claim is either supported, qualified, or removed. |
| Missing-information check | Are there identified gaps from the Retrieve step that have not been addressed? | System surfaces the gaps and asks whether they are material to the decision. If material, sufficiency is blocked. |
| Low-confidence check | Are any key premises marked as Low confidence? | System flags the low-confidence premises and asks whether additional investigation is warranted before action. |
| Policy-boundary check | Does the decision artifact cross a policy boundary identified in the Optimizer State? | System flags the boundary crossing and requires explicit human authorization. |
| Prior-failure check | Has a prior Learning Event identified a failure mode that matches the current decision pattern? | System surfaces the prior failure and asks whether the current decision has addressed the identified risk. |

**MVP implementation:** Sufficiency rationale is a required field on Decision State. The system displays the Premise Stack and asks the human to confirm sufficiency. Automated gate checks are a future-phase concern, but the data model must support them from the start.

---

### Chapter 9 — Human Roles and Permissions

The reasoning-state layer requires explicit authority definitions because reasoning objects carry different governance weight depending on who created, confirmed, validated, or deprecated them. A system-inferred premise confirmed by a junior marketer carries different weight than one validated by a domain expert with outcome evidence. The role model makes that distinction architectural, not implicit.

---

#### Role Definitions

**MVP roles (three):**

| Role | Description | Typical organizational title |
|---|---|---|
| **Requester / Operator** | The person who initiates a workflow and interacts with Discovery. Creates Draft reasoning objects. Confirms proposed reasoning within their own workflow. | Marketer, support agent, analyst, campaign manager, product manager |
| **Domain Expert** | The person with subject-matter authority over the decision domain. Confirms premises, validates evidence, assesses applicability boundaries, and promotes reasoning from Provisional to Validated. | Senior marketer, product lead, compliance reviewer, sales leader, subject-matter expert |
| **Governance Owner** | The person responsible for the overall health of the reasoning-state layer. Manages lifecycle policies, resolves disputes between conflicting reasoning, configures retention and staleness rules, and ensures governance controls are operating. | VP of marketing operations, AI enablement lead, knowledge manager, platform owner |

**Future roles (five additional):**

| Role | Description |
|---|---|
| **Reviewer / Approver** | Reviews reasoning objects before promotion to Validated. May be a manager, compliance reviewer, or quality lead. Distinct from Domain Expert when review authority is separate from subject-matter authority. |
| **System Steward** | Manages the technical health of the reasoning-state system. Monitors retrieval quality, staleness, volume, integration, and metadata quality. |
| **Architect / Platform Owner** | Designs and maintains the reasoning-state architecture. Makes schema, retrieval, and integration decisions. |
| **Auditor** | Reviews the reasoning-state layer for compliance, provenance, and appropriate use. May be internal or external. Read-only access to reasoning objects and audit trails. |
| **Executive Sponsor** | Funds and prioritizes reasoning-state architecture work. Needs visibility into value and risk dashboards, not implementation detail. |

---

#### Permissions Matrix

**MVP permissions:**

| Action | Requester | Domain Expert | Governance Owner |
|---|---|---|---|
| Create Draft reasoning | Yes | Yes | No |
| Confirm proposed reasoning (Draft → Provisional) | Yes (own workflow only) | Yes | Yes |
| Validate reasoning (Provisional → Validated) | No | Yes | Yes |
| Reject reasoning | No | Yes | Yes |
| Modify reasoning (creates new version) | Yes (own workflow only) | Yes | Yes |
| Deprecate reasoning | No | Yes | Yes |
| Supersede reasoning (with new MUO) | No | Yes | Yes |
| Archive reasoning | No | No | Yes |
| View audit trail | Own workflow only | Yes | Yes |
| Configure retention policies | No | No | Yes |

**Future permissions** add Reviewer, System Steward, Architect, Auditor, and Executive Sponsor columns with granular distinctions (see blueprint Section 8 for full matrix).

---

#### Authority Scope

A confirmation is only valid when the confirmer has authority over the domain being confirmed. The architecture must track:

- **Who confirmed** — identity
- **What role they held** — at the time of confirmation
- **What scope their authority covers** — by workflow type, domain, content category, or organizational unit
- **What they actually confirmed** — which specific elements of the reasoning state

**MVP implementation:** Authority scope is implicit. The application enforces role-based permissions. The confirmation record logs who confirmed and what role they held. Authority-scope tracking (e.g., "this person has authority over cardiology campaigns but not oncology") is a future-phase concern.

**Future implementation:** Structured authority-scope records. Each role assignment includes a scope definition. The system validates that the confirmer's authority scope covers the reasoning being confirmed.

---

#### Multiple Roles

A single person may hold multiple roles. In a small team, the campaign owner may be both Requester and Domain Expert. In a solo operation, one person may hold all three MVP roles. The architecture must support this without creating governance theater — a person confirming their own reasoning should be logged as such, and the system should flag when the same person both creates and validates a reasoning object (self-validation warning).

**Martin compatibility notes:** Beacon likely has its own role model (skill authors, skill consumers, administrators). The PTF role model does not need to replace Beacon's roles. It operates alongside them. The mapping question is: when a Beacon skill output enters the reasoning-state layer, what PTF role does the skill consumer hold? The default should be Requester — skill outputs are inputs to reasoning, not confirmed reasoning.

---

### Chapter 10 — Governance and Observability

Governance in this architecture is not post-hoc review. It operates at three points: when reasoning is formed (during Discovery), when reasoning is reused (during retrieval), and when reasoning changes status (during lifecycle transitions). Without governance at all three points, the reasoning-state layer can create false confidence, policy laundering, or unauditable decision chains.

---

#### Governance Operating Points

| Point | What governance does | When it happens |
|---|---|---|
| **Formation** | Ensures system-inferred reasoning is marked Draft. Ensures human confirmation happens before reasoning shapes action. | During RIPC Infer and Confirm steps |
| **Reuse** | Ensures prior reasoning is surfaced with status, applicability boundary, confidence, and provenance. Ensures human acknowledges applicability before reuse. | During RIPC Retrieve and Propose steps |
| **Transition** | Ensures lifecycle state changes are authorized, evidenced, and logged. | During lifecycle transitions (Chapter 8) |

---

#### Role-Based Access Control

**MVP implementation:** Application-level enforcement of three-role permissions (Chapter 9). No fine-grained attribute-based access control.

**Future implementation:** Attribute-based access control where role permissions are scoped by workflow type, domain, and content category. Example: a Domain Expert may validate cardiology campaign reasoning but not oncology campaign reasoning unless their authority scope includes both.

---

#### Review and Approval Workflows

**MVP workflow:**

1. System creates Draft reasoning during RIPC Infer step.
2. Human reviews and confirms during RIPC Propose/Confirm steps (Draft → Provisional).
3. Domain Expert or Governance Owner reviews with evidence (Provisional → Validated).
4. All transitions logged in Governance Audit Records (Chapter 4).

**Future workflow additions:**

- Multi-reviewer approval for high-consequence reasoning
- Conditional approval ("approved for this campaign only; requires re-review for next campaign")
- Escalation path when reviewers disagree (both positions preserved with attribution; Governance Owner resolves)
- Time-bounded approval (approval expires after a defined period, triggering re-review)

---

#### Audit Logging

Every governance-relevant action must be logged. Audit records are immutable — they are never modified or deleted. (See Chapter 4, Governance Audit Record for schema.)

**What must be logged:**

- Reasoning object creation (who, when, what type, what workflow)
- Status transitions (from-status, to-status, who, when, why, evidence cited)
- Confirmation actions (who confirmed, what they confirmed, what they changed, what role, what authority scope)
- Retrieval events (what was retrieved, what was surfaced to the user, what was excluded)
- Reuse acknowledgments (human confirmed applicability of prior reasoning)
- Rejection actions (what was rejected, why, by whom)
- Modification actions (what was changed, who, why — old version retained)

**MVP implementation:** Basic audit logging — who, what, when, from-status, to-status. Stored as append-only records.

**Future implementation:** Full audit chain with evidence citations, authority-scope verification, and retrieval event logging. Audit query interface for compliance review.

---

#### Governance Dashboards

**MVP implementation:** No dashboards. Governance health is assessed manually.

**Future implementation:** Dashboards showing:

- **Staleness indicators** — how many reasoning objects exceed their review period
- **Volume metrics** — reasoning objects by status, workflow type, and age
- **Reuse metrics** — how often prior reasoning is retrieved, acknowledged, and applied
- **Conflict indicators** — reasoning objects with conflicting applicability boundaries or contradictory MUOs
- **Confirmation quality** — average confirmation time, correction rate, rejection rate (indicators of whether confirmation is meaningful or rubber-stamped)
- **Coverage gaps** — workflows that produce decisions without reasoning-state capture

---

#### Exception Handling

| Exception | MVP handling | Future handling |
|---|---|---|
| Governance rules conflict (two valid rules point to different actions) | Escalate to Governance Owner for manual resolution | Surface both rules with attribution; route to structured conflict resolution |
| Authority is disputed (two people claim authority over the same reasoning domain) | Governance Owner decides | Authority-scope registry resolves; escalation path if registry is ambiguous |
| Escalation fails (Governance Owner is unavailable or the dispute cannot be resolved) | Reasoning remains at current status; no silent promotion | Time-bounded escalation with automatic hold — reasoning cannot advance until resolved |
| Self-validation detected (same person creates and validates a reasoning object) | Log warning in audit trail | Configurable policy — allow for solo operations, require second reviewer for team operations |

---

#### Governance Overhead Proportionality

Not all reasoning needs the same governance depth. The architecture must support governance proportional to consequence.

**Direction (not fully specified in MVP):** Future versions should support a consequence-level field on Decision States that determines governance requirements. Low-consequence decisions may require only Draft → Provisional with basic logging. High-consequence decisions may require multi-reviewer validation, evidence documentation, and time-bounded re-review.

*Grounding note: The RapidSOS Marketing Context Layer demonstrated a coaching model for governance — flag and suggest, not reject. Brand voice violations were flagged with specific coaching suggestions ("use 'augment responders' instead of 'surveillance'"), not blocked. This pattern is worth evaluating for the PTF HLD as a design option for formation-time governance: the system proposes corrections to inferred reasoning rather than blocking workflow progress. However, this is a UI/UX pattern, not an architectural constraint — the PTF HLD must support both coaching and blocking governance models.*

**Martin compatibility notes:** Martin's Beacon and co-worker systems likely have their own governance models. The PTF governance layer operates on reasoning objects, not on skill execution or data access. The two governance layers are complementary — Beacon governs who can use which skills; PTF governs how reasoning produced by those skills is confirmed, validated, and reused.

---

## Part V: Integration and Implementation

### Chapter 11 — Integration Patterns

The reasoning-state layer is not a replacement for existing systems. It sits alongside them. It adds a reasoning layer on top of context, document, workflow, analytics, and governance systems that already exist. The integration principle is: the reasoning-state layer consumes information surfaces from existing systems and produces reasoning objects that existing systems can reference.

---

#### Integration Architecture

The reasoning-state layer has three integration surfaces:

1. **Inbound (information surfaces):** Existing systems provide documents, data, policies, and outcomes that the reasoning-state layer consumes as information surfaces during the Retrieve step.
2. **Event (workflow triggers):** Existing workflow tools emit events that trigger reasoning-state operations — workflow start triggers Discovery, workflow completion triggers outcome capture, workflow repetition triggers prior-reasoning retrieval.
3. **Outbound (reasoning references):** The reasoning-state layer produces reasoning objects that existing systems can reference — audit systems can link to reasoning chains, approval systems can reference confirmation records, agent frameworks can consume confirmed Optimizer States.

---

#### Integration Patterns by System Type

| System Type | Integration Pattern | What flows in | What flows out | MVP / Future |
|---|---|---|---|---|
| **RAG systems** | Parallel retrieval source. RAG retrieves documents; reasoning-state layer retrieves reasoning objects. Both feed the Discovery loop. | Document chunks (information surfaces) | Reasoning objects with metadata | Future (MVP operates standalone) |
| **Document repositories** | Documents are information surfaces. Reasoning-state layer records which documents supported which premises, which were consulted during investigation, which were cited in sufficiency rationale. | Documents, policies, briefs, reports | Usage metadata (which reasoning referenced this document) | MVP: document repository as Retrieve source. Future: bidirectional usage tracking. |
| **Workflow tools** | Event-driven hooks. Workflow start → Discovery trigger. Workflow completion → outcome capture trigger. Workflow repetition → prior-reasoning retrieval trigger. | Workflow events (start, complete, repeat) | Reasoning-state records associated with workflow instances | MVP: one workflow tool integration. Future: multi-workflow. |
| **CRM / marketing platforms** | CRM records provide audience, account, and campaign context as information surfaces. | Customer data, campaign data, account history | Reasoning about targeting assumptions, qualification signals, audience premises | Future |
| **Analytics systems** | Analytics provide outcome data that the reasoning-state layer uses for prediction-error detection. Without the prediction (from Decision State), the outcome is just a number. | Outcome metrics, performance data | Prediction-error assessments, learning event triggers | MVP: manual outcome capture from analytics. Future: automated outcome ingestion. |
| **Policy repositories** | Policy documents are information surfaces. Reasoning-state layer connects specific policies to specific decisions — which policy was consulted, which was relevant but not retrieved, which was overridden. | Policy documents, compliance guidelines | Policy-decision links in reasoning objects | Future |
| **Agent orchestration frameworks** | Agent frameworks consume confirmed Optimizer States, active Premise Stacks, sufficiency criteria, and governance gates as reasoning context. The integration point is the agent's context window or state management. | Reasoning objects (confirmed goal, premises, boundaries) | Agent actions and outputs (information surfaces for future cycles) | Future (OAD-12 must be resolved) |
| **Approval / governance systems** | Existing approval systems handle permissions. Reasoning-state layer adds reasoning provenance — not just "who approved" but "what reasoning did they approve, with what confidence and boundaries." | Approval decisions | Reasoning provenance in approval records | Future |
| **Audit systems** | Existing audit systems log actions. Reasoning-state layer adds reasoning audit — what reasoning objects were used, by whom, whether confirmed or overridden. | Action logs | Reasoning audit records | Future (MVP has basic audit logging internally) |

---

#### API Design Principles

The HLD must remain platform-agnostic. It specifies integration patterns (what data flows between the reasoning-state layer and existing systems), not product integrations (how to connect to Salesforce, Jira, LangChain, or Beacon specifically).

- **Capability-based:** Specify what the integration must do, not how it is implemented.
- **Event-driven where possible:** Workflow events trigger reasoning-state operations. Pull-based integration is acceptable when push is not available.
- **Protocol-agnostic:** The reasoning-state layer should expose via standard protocols (REST, MCP, webhooks). The protocol is a deployment decision, not an architecture decision.

---

#### Open Questions

- OAD-12: How do reasoning objects relate to the agent's context window? (Options: injected in full, referenced by ID with key fields injected, hybrid. Depends on agent framework and reasoning-object size.)
- What is the minimum integration surface for v1? (Direction: one workflow tool for event triggering, one document repository as information surface source.)
- How does the reasoning-state layer handle systems that cannot push events? (Direction: polling with configurable interval, or manual triggers.)

**Martin compatibility notes:** See Appendix C for dedicated Martin compatibility analysis. Key points: MCP is the likely integration protocol. Co-worker data enters as information surfaces. Beacon skills register alongside reasoning-state services. The model router is transparent infrastructure.

---

### Chapter 12 — Volume Management and Retention

If every workflow cycle produces reasoning objects, volume will grow. Unchecked growth degrades retrieval quality (more noise in results), increases storage costs, and makes governance harder (more objects to review). The architecture must manage volume without destroying provenance.

---

#### Retention Principles

1. **Retain provenance, not detail.** Full reasoning objects are valuable during active use. After their relevance window, a summary with provenance links may be sufficient.
2. **Lifecycle status drives retention.** Validated reasoning is retained longer than Draft reasoning. Rejected reasoning is retained for audit but not actively retrieved.
3. **Reuse frequency signals value.** Reasoning objects that are frequently retrieved and applied are more valuable than reasoning objects that are never accessed.
4. **Compliance overrides convenience.** Some industries require full retention of decision reasoning for regulatory periods regardless of retrieval value.

---

#### Retention Tiers

| Tier | Reasoning State | Retention Policy | Retrieval Behavior |
|---|---|---|---|
| **Active** | Draft, Provisional, Validated | Full retention. All fields preserved. Actively retrievable. | Default retrieval target |
| **Stale** | Validated but exceeds review period | Flagged for review. Full retention until reviewed. Retrievable with staleness warning. | Retrieved with "stale — review recommended" flag |
| **Archived** | Deprecated, Superseded, Rejected, or aged past relevance window | Summary retained with provenance links. Full detail available on request. Not actively retrieved. | Excluded from default retrieval. Available via explicit archive query. |
| **Compliance hold** | Any status, subject to regulatory retention | Full retention regardless of lifecycle status. Duration set by compliance policy. | Same as Active, but cannot be archived until hold expires. |

---

#### Archival Process

When a reasoning object moves to Archived:

1. A summary record is created preserving: object type, key fields (goal, update target, applicability boundary), status, provenance (who created, who confirmed), and links to related objects.
2. The full record is moved to cold storage (not deleted).
3. The summary remains in the active store for audit queries and historical context.
4. Provenance links in the reasoning chain are preserved — a chain from Optimizer State through MUO must remain navigable even if individual objects are archived.

---

#### Cross-Workflow Reasoning-Object Governance

**MVP:** Single-workflow operation. No cross-workflow governance needed.

**Future:** When multiple workflows share reasoning objects (e.g., an MUO from a cardiology campaign is surfaced during an oncology campaign), cross-workflow governance must address:

- Who has authority to validate reasoning that spans workflows?
- How are applicability boundaries enforced when reasoning crosses workflow boundaries?
- Who owns reasoning objects that are shared across teams?
- How are conflicts between workflow-specific MUOs and cross-workflow MUOs resolved?

---

#### Multi-Team Access Patterns

**MVP:** Single-team operation. All reasoning objects are visible to all team members.

**Future:** When multiple teams use the reasoning-state layer:

- **Reading should be open.** Any team can retrieve reasoning from any other team's workflows (unless restricted by compliance or sensitivity).
- **Writing stays governed.** Each team owns its own reasoning objects. Governance Owner permissions are scoped by team/domain.
- **Cross-team MUOs require explicit applicability assessment.** An MUO from Team A's workflow must not automatically shape Team B's decisions. Cross-team reuse requires applicability acknowledgment from Team B's Domain Expert.

---

#### Open Questions

- OAD-9: What should be retained vs. summarized? (Direction: retain full detail for 6-12 months of active use, then summarize with provenance links. Compliance requirements may override.)
- At what volume does reasoning-object accumulation degrade retrieval quality? (Direction: monitor retrieval precision and recall as volume grows. Degradation is an empirical question, not a theoretical one.)

**Martin compatibility notes:** If the organization has enterprise data governance policies that apply to reasoning objects (retention periods, data residency, access controls), the reasoning-state layer must comply. This is an organizational policy question, not an architecture question — the architecture must support configurable retention.

---

### Chapter 13 — Minimal Viable Implementation

The MVP is not a reduced version of the full architecture. It is a bounded first implementation that proves the core claim: preserving reasoning state across repeated decision cycles changes future behavior in ways that context alone does not.

---

#### First Workflow Selection Criteria

Select a workflow where:

1. **Decisions recur.** The same type of decision happens at least monthly.
2. **The team can articulate "better."** They can describe what a good outcome looks like and what a bad outcome looks like.
3. **Outcomes are observable.** After the decision, there is a measurable or assessable result (campaign performance, customer response, policy outcome, tool action consequence).
4. **Reasoning currently disappears.** The team recognizes that they re-explain the same goals, repeat the same premise failures, rediscover the same boundaries, or restart from a cold prompt each cycle.
5. **The team is willing to participate.** Discovery requires human engagement. If the team views it as overhead, the implementation will fail.

*Grounding example: A marketing campaign workflow where each campaign starts from a brief, targets a buyer persona, uses approved messaging, and produces measurable results (engagement, conversion, pipeline). The RapidSOS healthcare campaign is one instance. But the criteria are domain-agnostic — they apply equally to support ticket escalation, policy exception review, product requirement specification, or recurring compliance assessment.*

---

#### MVP Inclusions

| Component | MVP Specification |
|---|---|
| **Reasoning objects** | Optimizer State, Premise Stack (3-5 entries), Decision State (with required sufficiency rationale), Outcome Record. Investigation Trace captured if investigation occurs. Learning Event and MUO captured only when outcome contradicts expectations and team can identify evidence-supported explanation. |
| **Schema** | Minimal fields per object as specified in Chapter 3 MVP fields. No full schema. |
| **RIPC loop** | Four-step Retrieve → Infer → Propose → Confirm. Manual Discovery Patterns (static questions per workflow type). |
| **Retrieval** | Semantic search + metadata filters on goal keywords, workflow type, lifecycle status. Match rationale displayed. |
| **Governance** | Three lifecycle states (Draft → Provisional → Validated). System-inferred reasoning marked as Draft. Human confirmation required before reuse. Basic audit logging (who, what, when). |
| **Roles** | Requester (initiates workflow, confirms own reasoning), Domain Expert (validates premises, confirms applicability), Governance Owner (manages lifecycle policy). |
| **Learning** | Manual outcome capture. Manual Learning Event and MUO creation. Basic MUO retrieval during next cycle's Discovery. |
| **Sufficiency** | Sufficiency rationale is required on Decision State. Premise Stack displayed at sufficiency point for human review. |
| **Integration** | One workflow tool (workflow start triggers Discovery; workflow completion triggers outcome capture). One document repository (as information surface source for Retrieve step). |

---

#### Explicit Exclusions (What NOT to Build in v1)

| Excluded | Why |
|---|---|
| Full seven-state lifecycle governance | Too much process for a first cycle. Three states are sufficient to prove the concept. |
| Automated staleness detection | Requires enough reasoning objects to measure staleness patterns. Manual review is sufficient initially. |
| Multi-workflow reasoning-object governance | Start with one workflow. Cross-workflow governance is a maturity concern. |
| Integration with agent orchestration frameworks | Start with a standalone reasoning-state store. Agent integration is a second-phase concern. |
| Automated MUO creation | MUOs must be human-created and human-reviewed in the first cycle. Automated creation risks noise and policy laundering. |
| Complex retrieval ranking | Start with simple semantic + metadata filters. Sophisticated ranking requires enough data to tune. |
| Full audit and compliance infrastructure | Start with basic provenance tracking. Full audit is a maturity concern. |
| Reasoning-object versioning UI | Start with append-only storage. A version-comparison interface is not needed until reasoning objects are frequently updated. |
| Dynamic Discovery Patterns | Start with static question sets per workflow type. Dynamic patterns require enough usage data to learn from. |
| Automated sufficiency gates | Start with human-reviewed sufficiency. Automated gates require validated rules and enough examples to calibrate. |
| Confirmation fatigue detection | Requires baseline data on confirmation behavior that does not exist in the first cycle. |

---

#### Minimal Object Schema Summary

| Object | MVP Fields |
|---|---|
| **Optimizer State** | id, workflow_id, goal, interpretation, policy_scope, requester, status, confidence, source_type, confirmed_by, created_at, version |
| **Premise Stack entry** | id, optimizer_state_id, statement, confidence, evidence_basis, assumption_type, status, source_type, applicability_boundary, created_at |
| **Decision State** | id, optimizer_state_id, chosen_action, rejected_alternatives, sufficiency_rationale (required), confidence_at_decision, unresolved_uncertainties, status, created_at |
| **Investigation Trace** | id, decision_state_id, questions_asked, sources_checked, contradictions_found, evidence_accepted, evidence_rejected, status, created_at |
| **Learning Event** | id, decision_state_id, prediction, outcome, prediction_error, evidence_supported_explanation, linked_premise_ids, status, confidence, created_at |
| **MUO** | id, learning_event_id, update_target, update_content, evidence_basis, confidence, applicability_boundary, non_applicability_boundary, status, created_by, reviewed_by, created_at |
| **Outcome Record** | id, decision_state_id, outcome_description, outcome_data_source, recorded_by, created_at |

---

#### Minimal Retrieval Implementation

- **Semantic search** over reasoning objects (embed goal, interpretation, premise statements, update content)
- **Metadata filters** on: workflow type, lifecycle status, goal keywords, audience/segment
- **Negative filters** on: non-applicability boundaries
- **Match rationale** displayed for every surfaced result (even if simple: "same workflow type, similar goal")
- **Status display** on every surfaced result
- **No complex ranking** — filter and display, let the human judge

---

#### Minimal Governance Model

- **Three states:** Draft → Provisional → Validated
- **System-inferred reasoning** always starts as Draft
- **Human confirmation** moves Draft → Provisional (during RIPC Confirm step)
- **Validation** moves Provisional → Validated (domain expert or governance owner reviews with evidence)
- **Audit log:** every state transition logged with who, what, when, from-state, to-state
- **No automated governance workflows** in v1 — all governance is human-initiated

---

#### Minimal RIPC Flow

1. **Retrieve:** Semantic search + metadata filters over reasoning-state store and information surfaces. Log what was retrieved.
2. **Infer:** System constructs Draft Optimizer State and Draft Premise Stack. All elements marked system-inferred.
3. **Propose:** System presents Draft reasoning state to human with confidence levels, uncertainties, and prior reasoning (if any). Human can confirm, correct, reject, qualify, or bound.
4. **Confirm:** System records human response. Updates reasoning objects from Draft to Provisional. Logs confirmation record. If human rejects or identifies new uncertainty, re-enter the loop.

---

#### Minimal Learning Loop

1. **Outcome capture:** After the workflow completes, a human records the outcome. Manual entry.
2. **Prediction-error identification:** The human compares the outcome to the prediction (what the Optimizer State and Decision State expected). If the outcome contradicts expectations, a Draft Learning Event is created.
3. **Investigation:** The human investigates why the prediction was wrong. The system may assist by surfacing relevant information surfaces and prior reasoning.
4. **Explanation:** The human writes an evidence-supported explanation, not a narrative. Links to specific premises that failed.
5. **MUO creation:** If the learning is reusable (applies beyond the single instance), the human creates a Model Update Object with applicability boundary, non-applicability boundary, and confidence. Status: Draft. Requires review before it can be applied to future cycles.
6. **MUO retrieval in next cycle:** When the workflow repeats, the Retrieve step surfaces the MUO. The human confirms whether it applies to the current context before it shapes the current cycle.

---

#### Success Criteria for the First Cycle

The first cycle succeeds if:

1. **Reasoning was captured.** The workflow produced at least an Optimizer State, Premise Stack, Decision State, and outcome record that were not previously preserved.
2. **The next cycle started differently.** When the workflow repeated, prior reasoning was retrieved and the starting state was richer than a cold prompt.
3. **A human confirmed applicability.** Prior reasoning was not blindly applied. A human assessed whether prior reasoning applied to the new context.
4. **The sufficiency rationale was explicit.** The Decision State recorded why investigation stopped, not just what was decided.
5. **If a prediction error occurred, it was explained.** A Learning Event was created with an evidence-supported explanation, not just a note that "it didn't work."

The first cycle does NOT need to produce a Model Update Object, automated sufficiency gates, cross-workflow reasoning reuse, or evidence of measurable improvement. Those are second-cycle and later concerns.

---

#### Evidence to Preserve for Future Case-Study Learning

While running the first cycle, capture baseline observations as natural byproducts (not as a separate research protocol):

- What reasoning currently disappears between cycles?
- Where does premature sufficiency currently occur?
- What artifacts exist today, and what reasoning do they fail to preserve?
- How do decisions currently become "good enough"?
- What outcomes does the team expect to improve?
- What evidence would show the next cycle got smarter?

These observations are for Path 2 (academic paper) if the formal academic track needs baseline data. They do not change the build.

---

#### What Must Remain Deferred

| Deferred concern | Why | When to revisit |
|---|---|---|
| Multi-workflow reasoning | Scope discipline. Prove the pattern with one workflow first. | After 2-3 successful single-workflow cycles. |
| Automated MUO creation | Risk of noise and policy laundering. | After enough human-created MUOs exist to establish quality patterns. |
| Dynamic Discovery Patterns | Requires usage data that does not exist yet. | After 5+ cycles with static patterns. |
| Agent orchestration integration | The reasoning-state layer must be stable before agents consume it. | After the data model and retrieval are validated. |
| Automated governance workflows | Governance must be understood before it can be automated. | After manual governance patterns are established. |
| Effectiveness metrics | Requires controlled comparison that the first cycle cannot provide. | After 3+ cycles where reasoning state was preserved and reused. |
| Martin / Beacon integration | Requires answers to open integration questions (Appendix C). | After the PTF reasoning-state layer is independently validated. |

---

## Part VI: Forward-Looking

### Chapter 14 — Risks and Mitigations

A reasoning-state architecture creates new risks because it makes reasoning durable, retrievable, and behaviorally influential. That power can be misused, can degrade, or can produce the opposite of its intended effect. Each risk below includes the HLD chapter(s) that must address it and whether it is an MVP concern or a maturity concern.

| # | Risk | Why It Matters | Mitigation Direction | HLD Chapter | MVP or Future |
|---|---|---|---|---|---|
| 1 | **State explosion** — volume of reasoning objects becomes unmanageable | Volume degrades retrieval quality, increases costs, makes governance harder | Selective capture (Principle 8). Retention policies (Ch 12). Archive reasoning past relevance window. Not every workflow needs full capture. | Ch 8, Ch 12, Ch 13 | Future (MVP operates on one workflow with low volume) |
| 2 | **Stale reasoning** — prior reasoning becomes outdated as conditions change | Stale reasoning reused without flagging causes worse outcomes than no reasoning | Staleness detection (Ch 8). Lifecycle status management. Periodic review triggered by configurable thresholds. Stale reasoning flagged, not silently retrieved. | Ch 8, Ch 6 | MVP (basic staleness flagging) |
| 3 | **False analogy / false reuse** — prior reasoning applied to situations where it does not actually apply | False reuse creates false confidence from prior experience — worse than no reuse | Applicability boundaries on every object (Principle 6). Non-applicability boundaries as negative retrieval filters (Ch 6). Human confirmation before reuse (Principle 4). | Ch 6, Ch 5, Ch 3 | MVP (applicability boundaries required from day one) |
| 4 | **Confirmation fatigue** — humans rubber-stamp without meaningful review | Creates false audit trail of human oversight. Undermines the human-in-the-loop design. | Minimize confirmation to material decisions. Reduce burden for validated reasoning (lightweight acknowledgment, not full re-review). Track confirmation behavior to detect rubber-stamping (future). | Ch 5, Ch 10 | MVP (lightweight acknowledgment design) |
| 5 | **Automation bias** — humans defer to system-generated reasoning because it appears authoritative | System proposal becomes decision by default. Undermines genuine human judgment. | Expose uncertainty and inferential basis. Make correction and rejection as easy as confirmation. Do not present proposals as conclusions. Design proposals to invite challenge. | Ch 5 | MVP (confidence and source_type display) |
| 6 | **Overcapture / surveillance** — reasoning capture becomes worker monitoring | Workers resist, game inputs, or refuse to express genuine uncertainty | Selective capture (Principle 8). Capture reasoning for the decision, not about the person. Give humans control over what is recorded. Do not record reasoning the human has not chosen to share. | Ch 2, Ch 13 | Both (design constraint from day one; monitoring concern grows with scale) |
| 7 | **Political misuse** — preserved reasoning used for blame rather than learning | People stop sharing genuine reasoning. System captures political reasoning instead of honest reasoning. | Governance norms distinguishing learning from blame. Access controls limiting individual-reasoning visibility. Aggregate learning from patterns, not individual attribution. | Ch 9, Ch 10 | Future (governance norm, not architectural control in MVP) |
| 8 | **Policy laundering** — system-inferred reasoning silently becomes organizational policy | Unreviewed reasoning accumulates authority it was never granted | All system-inferred reasoning marked Draft (Principle 9). Promotion requires human review. Track origin of every object (system-generated vs. human-created). MUOs require human review before shaping future cycles. | Ch 3, Ch 8, Ch 7 | MVP (Draft marking and review requirement) |
| 9 | **Audit overhead** — provenance tracking creates administrative burden | Teams avoid the system or game inputs if overhead is too high | Automate as much audit as possible (timestamps, identity, version tracking). Manual audit proportional to consequence. Not every object needs the same audit depth. | Ch 10 | MVP (basic automated audit) |
| 10 | **Metadata quality** — incomplete or inaccurate metadata degrades retrieval | Retrieval by reasoning relevance becomes unreliable if metadata is wrong | Metadata defaults and templates. Validation at creation time. Flag objects with incomplete metadata. Require minimum viable metadata, not perfect metadata. | Ch 3, Ch 6 | MVP (minimum required fields enforced) |
| 11 | **Broken provenance** — reasoning-object chain is not maintained | System becomes unauditable and ungovernable | Referential integrity enforcement. No orphaned objects. Version links rather than breaking them. | Ch 3 | MVP (referential integrity from day one) |
| 12 | **Workflow integration burden** — reasoning-state capture creates friction | Teams reject the system if burden exceeds value | Start with one workflow. Minimize required fields. Use Discovery to reduce burden (infer, confirm only what matters). Do not require capture for routine, low-consequence work. | Ch 13, Ch 5 | MVP (minimized by design) |
| 13 | **Human escalation bottlenecks** — too many decisions require human confirmation | Humans become the bottleneck; system cannot operate at useful speed | Escalation proportional to consequence and uncertainty. Validated reasoning earns reduced confirmation burden. Escalation thresholds increase with system maturity. | Ch 5, Ch 8 | Both (MVP addresses through lightweight acknowledgment; future adds adaptive thresholds) |
| 14 | **Generic RAG drift** — architecture silently collapses into ordinary semantic retrieval with extra metadata | The system loses its distinguishing value. Prior reasoning is retrieved by text similarity, not reasoning relevance. Governance becomes post-generation review. Sufficiency becomes implicit. | HLD Review Checklist (Appendix D) enforces drift detection. Chapter 6 explicitly distinguishes reasoning-relevant retrieval from semantic retrieval. Governance operates at formation and reuse time, not only post-hoc. Sufficiency is a required field. | Ch 6, Ch 2, Appendix D | Both (design constraint; ongoing vigilance required) |

**Martin compatibility notes:** Risk 3 (false analogy) is relevant if co-worker data is treated as reasoning without confirmation — co-worker data is an information surface, not a reasoning object. Risk 7 (policy laundering) is relevant if Beacon skill outputs accumulate reasoning-like authority without lifecycle governance.

---

### Chapter 15 — Open Architecture Questions

These are not gaps in the HLD. They are decisions that require implementation experience to resolve. Each question has been surfaced during the architecture process and carries enough context for the implementation team to make an informed choice when the time comes.

---

| # | Decision | Options | HLD Default (if any) | Dependencies | Must Resolve for MVP? |
|---|---|---|---|---|---|
| OAD-1 | **Separate reasoning-state store vs. metadata layer vs. hybrid** | (a) Dedicated reasoning-state store; (b) Metadata layer on existing document store; (c) Hybrid — dedicated store with links to documents | Separate store recommended (cleaner query patterns, independent lifecycle management) | Existing infrastructure, retrieval architecture, storage budget | Yes — determines storage architecture |
| OAD-2 | **Minimum metadata schema for v1** | (a) Full schema from Ch 3; (b) Reduced: goal, interpretation, premises (3-5), sufficiency rationale, confidence, status | Reduced for MVP (Ch 3 MVP fields) | Implementation team capacity, first workflow complexity | Yes — determines data model |
| OAD-3 | **Lifecycle states for v1** | (a) Full seven states; (b) Minimal three (Draft → Provisional → Validated) | Three states for MVP (Ch 8) | Governance maturity, first workflow requirements | Yes — determines governance scope |
| OAD-4 | **What counts as "validated" reasoning** | (a) Any human confirmation; (b) Authorized domain expert; (c) Confirmation plus outcome evidence; (d) Consequence-proportional | Policy decision. HLD specifies capability; organization defines policy. | Authority structures, governance requirements | Partially — need at least a working definition for MVP |
| OAD-5 | **Who can supersede an MUO** | (a) Original creator; (b) Any domain expert; (c) Governance owner only; (d) Anyone with stronger evidence | Default: domain expert or governance owner (Ch 8) | Authority structures | No — supersession is a future-phase concern |
| OAD-6 | **Confidence representation** | (a) Numeric (0-1 or 1-5); (b) Categorical (Low/Medium/High); (c) Evidence-linked; (d) Multi-dimensional | Categorical for MVP (Ch 3). Simpler to use; sufficient for initial cycles. | UI design, retrieval ranking | Yes — determines display and filtering |
| OAD-7 | **Applicability boundary expression** | (a) Free text; (b) Structured tags; (c) Both; (d) Learned from reuse patterns | Free text for MVP (Ch 3). Structured tags added in future. | Retrieval architecture, metadata schema | Yes — free text is the minimum |
| OAD-8 | **Reasoning reuse audit level** | (a) Log every retrieval + confirmation; (b) Log only incorporation events; (c) Full effectiveness tracking | Level (b) for MVP. Add (a) and (c) as system matures. | Audit requirements, storage | Partially — (b) is sufficient for MVP |
| OAD-9 | **Retention vs. summarization policy** | (a) Retain indefinitely; (b) Time-based (N months full, then summarize); (c) Status-based; (d) Reuse-frequency-based | Direction: 6-12 months full detail, then summarize with provenance (Ch 12). Compliance overrides. | Storage costs, compliance, retrieval quality | No — manual retention is sufficient for MVP |
| OAD-10 | **Discovery Patterns: static or dynamic** | (a) Static configuration per workflow; (b) Dynamic patterns that update; (c) Start static, enable dynamic | Static for MVP. Dynamic is Stage 3+ maturity. | Learning-loop maturity, usage data volume | Yes — static is the MVP answer |
| OAD-11 | **Conflicting reasoning objects** | (a) Surface both with attribution; (b) Escalate to governance owner; (c) Recency tiebreaker; (d) Confidence tiebreaker; (e) Human resolves | Default: (e) present conflict, let human resolve. System must not resolve conflicts silently. | Governance workflows, UI | No — conflicts are unlikely in single-workflow MVP |
| OAD-12 | **Reasoning objects and agent context window** | (a) Inject full objects; (b) Store externally, reference by ID; (c) Hybrid — inject key fields, link full objects | Depends on agent framework and object size. Hybrid likely. | Agent framework constraints, context window limits | No — agent integration is future phase |

---

#### Questions Surfaced by This HLD That Are Not in the Blueprint

| # | Question | Context |
|---|---|---|
| OAD-13 | **How does RIPC operate in multi-agent orchestration?** | When an agent calls RIPC on behalf of a human, who is the "confirmer"? The agent cannot hold authority. The human must still confirm, but the interaction pattern changes. |
| OAD-14 | **What is the minimum viable Propose interface?** | Chapter 5 specifies what must be proposed but not how. A command-line interface, a web form, a conversational exchange, or an IDE plugin are all valid. The interface must support confirm/correct/reject/qualify/bound. |
| OAD-15 | **How does the architecture handle reasoning about reasoning?** | When a governance decision is made (e.g., deprecating an MUO), should that decision itself be captured as a reasoning object? This risks infinite regress but may be necessary for high-consequence governance. |

**Martin compatibility notes:** OAD-1 and OAD-12 are the most relevant to Martin integration. If Beacon or co-worker already stores reasoning-like objects, the separate-vs-hybrid decision (OAD-1) is constrained. If agent context windows are limited by the model router's cost optimization, injection (OAD-12) may not be viable for large reasoning objects.

---

### Chapter 16 — Appendices

#### Appendix A: Build Discovery Guide Categories → HLD Components Mapping

| # | Guide Category | Build Output Produced | Primary HLD Chapter(s) | MVP Priority | Future Enhancement |
|---|---|---|---|---|---|
| 1 | Workflow Boundary | Workflow scope, entry/exit conditions, repetition pattern | Ch 13 (MVP), Ch 1 (Scope) | High | Multi-workflow boundary definitions |
| 2 | Campaign Brief Structure | Decision State fields, Optimizer State fields | Ch 3 (Data Model) | High | Full decision-artifact schema |
| 3 | KB / Information Surfaces | Information Surface inventory, categories, authority, recency | Ch 4 (Supporting Objects), Ch 6 (Retrieval) | Medium | Automated information surface discovery |
| 4 | Trust, Evidence, Confidence | Confidence metadata, evidence standards, trust display | Ch 6 (Retrieval), Ch 3 (Data Model) | Medium | Multi-dimensional confidence scoring |
| 5 | Assumptions / Premises | Premise Stack schema, staleness flags, re-examination triggers | Ch 3 (Data Model), Ch 6 (Retrieval), Ch 7 (Learning) | Medium | Automated premise-falsification detection |
| 6 | Policy / Governance Boundaries | Policy engine, governance scoring, review gates, approval workflows | Ch 10 (Governance), Ch 5 (RIPC), Ch 8 (Lifecycle) | High | Multi-vertical governance, automated policy updates |
| 7 | Sufficiency and Stopping | Sufficiency gates, stop/ask/escalate logic, quality-gate scoring | Ch 8 (Lifecycle), Ch 5 (RIPC), Ch 10 (Governance) | High | Adaptive sufficiency thresholds |
| 8 | Reasoning to Preserve | Six reasoning objects: Optimizer State, Premise Stack, Decision State, Investigation Trace, Learning Event, MUO | Ch 3 (Data Model), Ch 5 (RIPC), Ch 8 (Lifecycle) | High | Full six-object capture, cross-workflow reasoning links |
| 9 | Learning Loop | Learning Event creation, MUO lifecycle, prediction-error detection, outcome-to-reasoning routing | Ch 7 (Learning Loop), Ch 3 (Data Model), Ch 6 (Retrieval) | Medium | Automated prediction-error detection, multi-campaign aggregation |
| 10 | Retrieval Relevance | Reasoning-relevant retrieval engine, applicability matching, match-rationale generation | Ch 6 (Retrieval), Ch 5 (RIPC), Ch 14 (Risks) | Medium | Cross-workflow retrieval, automated relevance scoring |
| 11 | Human Confirmation | Confirmation workflow, review UI, correction propagation, override logic | Ch 5 (RIPC), Ch 10 (Governance), Ch 14 (Risks) | High | Adaptive confirmation frequency, learning from confirmation patterns |
| 12 | Ownership / Lifecycle | Lifecycle state machine, staleness notification, ownership registry, archival logic | Ch 8 (Lifecycle), Ch 10 (Governance), Ch 12 (Volume) | Medium | Automated ownership-transfer detection, cross-system lifecycle sync |
| 13 | Build Translation | Architecture-landing summary — all discovery outputs organized by system component | All chapters | High | — |

#### Appendix B: Concept-to-Component Mapping

| PTF Concept | Buildable System Component(s) | HLD Chapter |
|---|---|---|
| Perceived topography | Information-surface registry + retrieval/governance visibility layer. The system's "topography" is what the human-agent system can see, retrieve, and trust. | Ch 4, Ch 6, Ch 10 |
| Gradients | Governance rules, confidence signals, authority weighting, UI prompts, escalation paths. Gradients are the pressures that shape which reasoning surfaces receive attention. | Ch 10, Ch 8, Ch 5 |
| Sufficiency | Stop / ask / proceed / escalate / abstain gates. Explicit stopping conditions that replace "the draft sounds professional." | Ch 8, Ch 5 |
| Premature sufficiency | Risk checks: unsupported-claim blocks, missing-information checks, grounding checks, low-confidence warnings. The system makes it harder to act before reasoning is sufficient. | Ch 8, Ch 5, Ch 14 |
| Reasoning state | Six-object data model: Optimizer State, Premise Stack, Decision State, Investigation Trace, Learning Event, Model Update Object. | Ch 3 |
| RIPC / Discovery | Service flow: Retrieve → Infer → Propose → Confirm. Multi-step interaction pattern, not single API call. | Ch 5 |
| Learning | Learning Events (prediction error + evidence-supported explanation), Model Update Objects (reusable lessons with applicability boundaries), outcome capture, review/apply workflow. | Ch 7 |
| Governance | Rule engine (policy constraints at decision time), approval gates (lifecycle transitions), audit trail (who did what to which reasoning object), ownership model (who maintains which reasoning). | Ch 10, Ch 8, Ch 9 |
| Trust | Source authority metadata, evidence standards, confidence/provenance display, lifecycle status as trust signal. | Ch 3, Ch 4, Ch 6 |
| Retrieval relevance | Applicability logic (goal, policy, audience, workflow match), metadata filters (status, confidence, recency), match rationale display, prior reasoning reuse confirmation, false-analogy prevention. | Ch 6 |

#### Appendix C: Compatibility With Existing / Martin Implementation Work

**Purpose:** This section treats Martin's implementation work (Beacon skill registry, model router, co-worker integration) as a compatibility and interface surface. Martin's work is not conceptual authority for the PTF HLD unless explicitly promoted. It is a practical constraint and a potential integration target.

**Known Implementation Artifacts:**

| Artifact | What We Know | Source |
|---|---|---|
| **Beacon** (Skill Registry) | MCP-based skill distribution system. Ships "little AI avatars" (skills) across the organization. Known skills: Security Review, Feature Alignment, Weekly Log. Uses MCP protocol for discovery and connection. | Martin interview, Architecture Cheat Sheet, Rapid deliverables |
| **Model Router** | Routes queries to cost-appropriate models (Claude for complex, DeepSeek/MiniMax/Moonshot for simple). 20x cheaper inference on easy queries. Under active development. | Martin interview, Architecture Cheat Sheet |
| **Co-Worker MCP** | Third-party enterprise data indexer (Salesforce, Zendesk, JIRA, Slack, email). Provides MCP interface into Claude. Not built by Martin. | Martin interview, Architecture Cheat Sheet |
| **Semantic Layers** | Martin referenced "other semantic layers being built" — details unknown. | Deliverable 4 (Martin Reply 2) |

**Reusable Components:**

| Component | Reuse Potential | Notes |
|---|---|---|
| MCP protocol | High | PTF reasoning-state services could expose as MCP tools, compatible with Beacon's discovery mechanism |
| Beacon discovery | Medium | If reasoning-state services register as Beacon skills, existing infrastructure handles discovery and access |
| Model router | Medium | Retrieval queries could route to cheaper models; generation stays on higher-quality models |
| Co-worker data | High | Enterprise data from co-worker is a natural information surface for the reasoning-state layer |

**Alignment With PTF Concepts:**

| Martin Component | PTF Concept | Alignment Assessment |
|---|---|---|
| Beacon skills | Information surfaces / tools | Skills provide information and capabilities. In PTF terms, skill outputs are information surfaces that shape the optimizer's perceived topography. Alignment is natural but not direct — skills are action-oriented, information surfaces are perception-oriented. |
| Model router | Retrieval architecture (cost optimization) | Compatible. The model router is an infrastructure concern; it does not affect the conceptual architecture. Retrieval queries can route through it. |
| Co-worker data | Information surfaces | Strong alignment. Co-worker indexes what happened (enterprise data). PTF adds how to reason about it (reasoning state). Complementary, not competing. |
| Semantic layers | Unclear | Insufficient information to assess alignment. |

**Interface Assumptions:**

1. MCP is the integration protocol. Both Beacon and the PTF reasoning-state layer would expose via MCP.
2. Co-worker data is consumed as information surfaces, not as reasoning objects. The PTF layer adds reasoning on top of co-worker's data layer.
3. The model router is transparent to the reasoning-state layer. Routing decisions are infrastructure, not architecture.
4. Beacon's skill discovery mechanism is a registration concern, not a conceptual concern. The PTF reasoning-state layer registers as a skill; Beacon handles distribution.

**Potential Conflicts or Drift:**

| Concern | Risk | Mitigation |
|---|---|---|
| Beacon skills may accumulate reasoning-like outputs that are not governed as reasoning objects | Medium — skill outputs could become de facto policy without lifecycle governance | Define interface: when a skill output should be captured as a reasoning object vs. consumed as transient information |
| Model router may prioritize cost over reasoning quality for retrieval | Low — retrieval quality is measurable | Define minimum quality thresholds for reasoning-relevant retrieval queries |
| Co-worker data may be treated as confirmed reasoning rather than information surfaces | Medium — enterprise data has authority but not PTF-style confidence/provenance metadata | Define the boundary: co-worker data is input to reasoning, not reasoning itself |
| "Other semantic layers" may overlap with reasoning-state storage | Unknown — insufficient information | Flag for discovery during integration planning |

**Open Integration Questions:**

1. How does Beacon discover and register MCP skills? (Registration mechanism unknown.)
2. What metadata does Beacon attach to skills? (Relevance to reasoning-object metadata unknown.)
3. Does co-worker provide confidence or provenance metadata, or only raw data?
4. What are the "other semantic layers" Martin referenced?
5. Does any existing system store anything resembling reasoning objects (decisions, assumptions, lessons)?
6. What are the latency requirements for Beacon skill calls? (RIPC's multi-step loop may exceed single-call expectations.)

**MVP Decision:**

| Option | Assessment |
|---|---|
| **Integrate now** | Not recommended for MVP. Integration requires answers to the open questions above. Premature integration risks designing the PTF architecture around Beacon's constraints rather than PTF's concepts. |
| **Design for later** | Recommended. The HLD should specify MCP-compatible interfaces and define information-surface ingestion patterns that can accept co-worker data. This keeps the door open without coupling. |
| **Defer entirely** | Acceptable if the first implementation slice targets a non-RapidSOS organization. |

---

#### Appendix D: HLD Review Checklist

Use this checklist to verify that each HLD chapter maintains alignment with the framework and avoids common drift patterns.

| # | Check | Pass Criteria |
|---|---|---|
| 1 | Preserves keystone logic | Every architectural decision traces back to a paper concept. No invented concepts without paper grounding. |
| 2 | Maps cleanly from the Build Discovery Guide | Every guide category has a named HLD landing point. No guide outputs are orphaned. |
| 3 | Avoids generic RAG drift | The retrieval architecture explicitly distinguishes reasoning-relevant retrieval from semantic document retrieval. If the architecture can be reduced to "vector DB + top-K chunks," it has failed. |
| 4 | Keeps RapidSOS as grounding, not center | RapidSOS examples illustrate patterns; they do not constrain the architecture. The HLD must work for any repeated-decision workflow, not only marketing. |
| 5 | Separates MVP from future phases | Every section names what is MVP and what is deferred. No section assumes full implementation in v1. |
| 6 | Distinguishes Path 1 actual build from Path 2 academic paper | The HLD is a Path 1 artifact. It does not need to satisfy academic review criteria. It may capture baseline observations for Path 2, but this is a byproduct, not a goal. |
| 7 | Turns PTF concepts into buildable system components | Every PTF concept maps to at least one named system component. No concept is left abstract. |
| 8 | Keeps reasoning-state preservation central | The architecture's organizing principle is "preserve and surface reasoning at the moment it matters." If reasoning-state preservation is a secondary concern, the architecture has drifted. |
| 9 | Makes governance active at decision time | Governance is not only post-hoc review. It operates at the moment reasoning is formed, confirmed, and reused. |
| 10 | Makes sufficiency explicit | Sufficiency is a required field, not optional. The system records why investigation stopped, not just what was decided. |
| 11 | Preserves learning-loop evidence | Learning Events and MUOs require evidence-supported explanations, not just narratives. The architecture distinguishes reaction from learning. |
| 12 | Identifies Martin implementation interfaces without overfitting | Martin's work defines compatibility surfaces, not architectural constraints. The HLD can integrate with Beacon/co-worker/model router without being designed around them. |

---

## No-Edit Confirmation

- Frozen paper (`PAPER_v1.0_WORKING.md`) edited: **No**
- Figure 8 modified: **No**
- Figures modified: **No**
- References modified: **No**
- Executive Brief edited: **No**
- Build Discovery Guide v1.0 edited: **No**
- Freeze records modified: **No**
- Full HLD drafted: **Yes** (v0.3 — all 16 chapters drafted. Spine chapters from v0.2; remaining chapters expanded in v0.3.)
