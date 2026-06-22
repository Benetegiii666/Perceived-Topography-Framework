# v1.0 HLD / Reference Architecture Planning Blueprint

**Date:** 2026-06-21
**Status:** Planning blueprint only. No full HLD drafted.
**Source:** PAPER_v1.0_WORKING.md (Sections 7, 8, 11, Appendix A), V1_0_COMPANION_ARTIFACT_OUTLINES.md, HLD_REFERENCE_ARCHITECTURE_NOTES.md, ARCHITECTURAL_PRESSURE_REPORT.md, V1_0_STAGE_2_AGENT_PEER_REVIEW.md.

---

## 1. HLD / Reference Architecture Purpose

### What this artifact is for

The HLD / Reference Architecture translates the Perceived Topography Framework from a design theory into an implementable system design. It answers the question that the paper deliberately defers:

> How do you build a system that preserves reasoning state across repeated decision cycles?

The paper teaches how to think about human-agent systems. The Practitioner Workbook teaches how to discover what the organization knows, believes, and needs. The HLD teaches what to build.

### Who it serves

| Audience | What they need from the HLD |
|---|---|
| Enterprise architects | Data model, service patterns, integration points, governance workflows |
| Platform teams | Schema specifications, retrieval architecture, lifecycle management, API design principles |
| Product engineers | Discovery interaction patterns, sufficiency-gate design, learning-loop implementation |
| Governance and compliance teams | Audit requirements, role-based access, review workflows, provenance tracking |
| AI enablement teams | Integration with existing RAG, agentic frameworks, and knowledge systems |
| Technical program leads | Minimal viable implementation, maturity staging, implementation risks |

### How it relates to the other artifacts

```
Paper (teaches the framework)
        ↓
Practitioner Workbook (discovers the reasoning)
        ↓
HLD / Reference Architecture (builds the system)
```

The Workbook produces structured interview outputs. The HLD translates those outputs into architecture. Neither artifact replaces the other: the Workbook produces the *what* and *why*; the HLD produces the *how*.

---

## 2. Scope and Non-Scope

### What the HLD must cover

| Domain | Scope |
|---|---|
| Reasoning-state preservation | How the six reasoning objects are captured, stored, versioned, and retrieved |
| Discovery / RIPC | How Retrieve → Infer → Propose → Confirm operates as a service pattern |
| Reasoning-relevant retrieval | How prior reasoning is found by goal, policy, confidence, applicability, provenance — not just semantic similarity |
| Governance and lifecycle | How reasoning objects move through draft → provisional → validated → deprecated → superseded, with permissions and audit |
| Confidence and provenance | How metadata about evidence quality, authority, source, and scope is captured and surfaced |
| Applicability boundaries | How the system represents where a reasoning object applies and where it does not |
| Human confirmation and review | How the architecture prevents blind reuse and ensures human authority over reasoning surfaces |
| Integration with RAG and agentic systems | How the reasoning-state layer sits alongside existing retrieval, orchestration, and knowledge systems |
| Audit and observability | How the system tracks what reasoning was used, by whom, and with what effect |
| Minimal viable implementation | How an organization begins with one workflow and a small schema |

### What the HLD must not become

| Anti-pattern | Why it fails |
|---|---|
| A vendor-specific architecture | The HLD must remain platform-agnostic. It should specify capabilities, not products. |
| A product pitch | The HLD is a design guide, not a sales document. |
| A full implementation manual | The HLD specifies what must exist and how components relate. It does not specify code, database DDL, or deployment scripts. |
| A universal enterprise AI platform | The HLD addresses reasoning-state preservation for repeated decision workflows. It does not attempt to solve all of enterprise AI. |
| A generic RAG pattern | The HLD must explicitly distinguish reasoning-relevant retrieval from ordinary semantic document retrieval. If the architecture can be reduced to "store everything in a vector database and retrieve the top 10 similar chunks," it has failed. |

---

## 3. Architecture Principles

The following principles govern the HLD. They are derived from the paper's conceptual architecture and should be treated as design constraints, not aspirations.

### Principle 1: Preserve reasoning, not just artifacts

The unit of organizational reasoning is the optimizer state transition, not the document. The architecture must preserve what the system was trying to do, what it believed, why the available information felt sufficient, what reality later contradicted, and what should change.

### Principle 2: Retrieve by reasoning relevance, not just semantic similarity

The most important prior reasoning may not use similar language. It may be relevant because it shares a goal, policy boundary, audience assumption, unresolved uncertainty, confidence limit, or failure pattern. Retrieval must combine semantic search with structured metadata filtering.

### Principle 3: Make prior reasoning behaviorally available at the moment it matters

A reasoning surface is behaviorally available when it can appear at the moment it matters, with enough confidence, provenance, scope, and status for the system and human to know how to use it. Storage without behavioral availability is a knowledge-management graveyard.

### Principle 4: Require human confirmation of applicability before reuse

Prior reasoning must not be silently applied to new decisions. The system must surface prior reasoning with its confidence, provenance, applicability boundaries, and status. A human must confirm that the prior reasoning applies to the current situation before the system treats it as part of the current landscape.

### Principle 5: Treat confidence and provenance as first-class metadata

Every reasoning object must carry information about how confident the system or human is, where the reasoning came from, who confirmed it, and what evidence supports it. Without this metadata, all prior reasoning becomes equally authoritative and equally misleading.

### Principle 6: Preserve applicability boundaries

A lesson learned about cardiology campaign targeting should not automatically reshape oncology outreach or partner enablement. Every reasoning object must carry explicit boundaries about where it applies and where it does not.

### Principle 7: Support lifecycle states

Reasoning objects are not permanent truths. They may be drafts, provisional interpretations, validated lessons, deprecated assumptions, or superseded rules. The architecture must track lifecycle status so that future systems and humans know how much weight to give each reasoning surface.

### Principle 8: Design for selective capture, not total capture

The goal is not to turn every human thought into a field. The goal is to preserve the minimum reasoning structure required for future action, learning, and governance. If the system tries to capture everything, it becomes bureaucracy.

### Principle 9: Govern reuse, not merely storage

The critical governance question is not whether reasoning is stored. It is whether reasoning is reused appropriately. Governance must address who can create, confirm, reject, modify, deprecate, supersede, and audit reasoning objects — and under what conditions prior reasoning can shape future action.

---

## 4. Six-Object Data Model Planning

### Source

Table 7 from the paper defines the minimum viable reasoning objects. The chain is:

```
Optimizer State → Premise Stack → Decision State → Investigation Trace → Learning Event → Model Update Object → Modified Optimizer State
```

### Object 1: Optimizer State

| Dimension | Specification |
|---|---|
| **Purpose** | Preserves what the system was trying to do, under what interpretation, goal, and constraints. |
| **Core fields** | goal (working objective), policy_scope (governing constraints), interpretation (how the situation was understood), requester, workflow_id, timestamp, version |
| **Relationships** | Parent of Premise Stack and Decision State. Referenced by Learning Event and MUO. Links to workflow definition. |
| **Lifecycle status needs** | Draft (inferred by system), Provisional (proposed to human), Validated (confirmed by human with authority) |
| **Provenance requirements** | Who created it, who confirmed it, what Discovery interaction produced it, what information surfaces informed the interpretation |
| **Retrieval needs** | Retrievable by goal, policy domain, workflow type, audience, and operating context. Must be findable when a similar decision arises. |
| **Governance needs** | Only authorized humans should confirm the goal and interpretation. System-inferred optimizer states must be visibly provisional. |
| **Healthcare campaign example** | Goal: generate qualified demo requests from cardiology practice administrators. Policy: no direct clinical-outcome claims without approved evidence. Interpretation: workflow burden is an attention hook, not a qualification signal. |
| **Implementation risks** | Goal may be poorly specified or politically contested. Multiple stakeholders may disagree on interpretation. System-inferred goals may anchor humans toward accepting an incorrect frame. |

### Object 2: Premise Stack

| Dimension | Specification |
|---|---|
| **Purpose** | Preserves why the system expected this action or decision to work. |
| **Core fields** | premise_id, statement, confidence_level, evidence_basis, source, assumption_type (explicit/tacit/inferred), status, applicability_boundary, linked_optimizer_state_id |
| **Relationships** | Child of Optimizer State. Referenced by Learning Event (to identify which premise failed). |
| **Lifecycle status needs** | Draft, Provisional, Validated, Deprecated (when evidence contradicts), Superseded (when replaced by updated premise) |
| **Provenance requirements** | Who stated or confirmed each premise, what evidence supports it, when it was last validated |
| **Retrieval needs** | Retrievable by topic, confidence, status, and linked goal. Must surface when a similar assumption appears in a future decision. |
| **Governance needs** | Premises with low confidence must be visibly marked. Premises that have been contradicted by outcomes must be deprecated, not silently retained. |
| **Healthcare campaign example** | Premise: "Workflow burden is a useful attention hook for cardiology administrators." Confidence: Medium. Evidence: prior campaign engagement data. Assumption type: Explicit. Boundary: does not establish buying readiness. |
| **Implementation risks** | Premises may be too vague to be useful. Teams may resist making tacit assumptions explicit. Confidence may be asserted without evidence. Premise volume may grow without review. |

### Object 3: Decision State

| Dimension | Specification |
|---|---|
| **Purpose** | Preserves what was chosen, what was rejected, and why the available information felt sufficient. |
| **Core fields** | decision_id, chosen_action, rejected_alternatives, sufficiency_rationale, confidence_at_decision, unresolved_uncertainties, linked_optimizer_state_id, linked_premise_stack_ids, timestamp |
| **Relationships** | Child of Optimizer State. References Premise Stack. Referenced by Investigation Trace (what investigation supported the decision). Referenced by Learning Event (what the decision's outcome revealed). |
| **Lifecycle status needs** | Active (current decision), Archived (after outcome captured), Superseded (if a later decision replaced it) |
| **Provenance requirements** | Who made the decision, what authority they held, what investigation preceded it, what sufficiency criteria were met |
| **Retrieval needs** | Retrievable by decision type, outcome, sufficiency rationale, and linked goal. Must surface when a similar decision arises so that prior stopping conditions are visible. |
| **Governance needs** | The sufficiency rationale is the most important governance surface. It is the record of why the system stopped investigating. Future reviewers must be able to inspect and challenge it. |
| **Healthcare campaign example** | Chosen: use workflow-burden messaging without direct readmissions claim. Rejected: direct clinical-outcome language (insufficient evidence). Sufficiency: approved operational claims available; clinical claims require evidence review. |
| **Implementation risks** | Teams may record the decision without the sufficiency rationale. "We decided X" is common; "we stopped investigating because Y" is rare. The architecture must make sufficiency rationale a required field, not optional. |

### Object 4: Investigation Trace

| Dimension | Specification |
|---|---|
| **Purpose** | Preserves how uncertainty was reduced before action. |
| **Core fields** | trace_id, questions_asked, sources_checked, contradictions_found, evidence_accepted, evidence_rejected, investigation_path, linked_decision_state_id, timestamp |
| **Relationships** | Supports Decision State. May trigger re-entry into Discovery if investigation reveals new uncertainty. |
| **Lifecycle status needs** | In Progress, Complete, Reopened (if new evidence requires re-investigation) |
| **Provenance requirements** | What sources were consulted, what tools were used, what human judgment was applied, how long the investigation took |
| **Retrieval needs** | Retrievable by investigation topic, sources used, and linked decision. Must surface when a similar uncertainty appears so that prior investigation paths are visible. |
| **Governance needs** | Must distinguish genuine investigation from after-the-fact rationalization. The trace must be created during investigation, not reconstructed after the decision. |
| **Healthcare campaign example** | Investigated: whether "reduces readmissions" is an approved claim. Sources checked: approved-claims repository, compliance guidelines, prior campaign reviews. Finding: no approved evidence for direct readmissions claim in this population. |
| **Implementation risks** | Investigation traces may be too detailed to be useful or too sparse to be meaningful. Teams may skip investigation and rationalize after the fact. The architecture must make it easy to record investigation steps incrementally, not retroactively. |

### Object 5: Learning Event

| Dimension | Specification |
|---|---|
| **Purpose** | Preserves where reality contradicted, qualified, or sharpened the model. |
| **Core fields** | event_id, prediction (what was expected), outcome (what happened), prediction_error (the gap), evidence_supported_explanation, linked_decision_state_id, linked_premise_stack_ids, timestamp |
| **Relationships** | References Decision State and Premise Stack. Parent of Model Update Object. |
| **Lifecycle status needs** | Draft (outcome recorded, explanation pending), Provisional (explanation proposed), Validated (explanation confirmed with evidence), Rejected (explanation found insufficient) |
| **Provenance requirements** | What outcome data was used, who identified the prediction error, who proposed the explanation, what evidence supports the explanation |
| **Retrieval needs** | Retrievable by outcome type, prediction-error category, linked premises, and workflow context. Must surface when similar decisions are forming so that prior failures are visible. |
| **Governance needs** | The explanation must be evidence-supported, not merely plausible. A convenient narrative is not a learning event. Governance must verify that the explanation identifies which premise or assumption failed, not just that the outcome was bad. |
| **Healthcare campaign example** | Prediction: workflow-burden messaging will generate qualified demo requests. Outcome: high engagement but low qualified conversion. Prediction error: engagement ≠ buying readiness. Explanation: workflow burden attracted attention but did not distinguish organizations actively evaluating RPM from those with general frustration. |
| **Implementation risks** | Teams may record outcomes without identifying prediction errors. The explanation may be political rather than evidence-supported. The learning event may be created for every outcome, not just outcomes that contradict expectations — leading to noise. |

### Object 6: Model Update Object (MUO)

| Dimension | Specification |
|---|---|
| **Purpose** | Preserves what reusable change should shape future reasoning. |
| **Core fields** | muo_id, update_target (what should change), update_content (the specific change), evidence_basis, confidence_level, applicability_boundary (where it applies), non_applicability_boundary (where it does not apply), linked_learning_event_id, status, created_by, reviewed_by, timestamp |
| **Relationships** | Child of Learning Event. When applied, modifies a future Optimizer State. |
| **Lifecycle status needs** | Draft (proposed), Provisional (under review), Validated (approved for reuse), Deprecated (no longer applicable), Superseded (replaced by a newer MUO), Rejected (found to be incorrect or overgeneralized) |
| **Provenance requirements** | Who created it, who reviewed it, what evidence supports it, what learning event produced it, when it was last validated, how many times it has been reused, whether reuse improved outcomes |
| **Retrieval needs** | Retrievable by update target, applicability boundary, confidence, status, and workflow context. This is the most important retrieval challenge: a relevant MUO must surface when a future decision matches its applicability boundary, not merely when the text is similar. |
| **Governance needs** | MUOs must be reviewed before they shape future reasoning. An unreviewed system-generated lesson must not become policy by default. Governance must track who approved the MUO, whether it has been tested, and whether it should be retired. |
| **Healthcare campaign example** | Update target: campaign qualification logic. Update content: future campaigns should distinguish workflow-burden attention from active RPM evaluation readiness. Applicability: cardiology practice administrator campaigns. Non-applicability: does not apply to partner enablement or executive education campaigns without further validation. Confidence: Medium (one cycle of evidence). |
| **Implementation risks** | MUOs may be too broad (overgeneralized) or too narrow (useless beyond one situation). Unreviewed MUOs may accumulate and silently shape system behavior. Political pressure may produce MUOs that reflect blame assignment rather than evidence-supported learning. The applicability boundary is the hardest field to get right. |

### Object 7: Modified Optimizer State

| Dimension | Specification |
|---|---|
| **Purpose** | Represents the changed conditions from which the next cycle begins. |
| **Storage decision** | Modified Optimizer State is not a separate stored object. It is the resulting condition when one or more MUOs are applied to a new Optimizer State. The architecture should store the MUOs and the new Optimizer State separately, with explicit links showing which MUOs were applied. |
| **Rationale** | Storing Modified Optimizer State as a separate object would create redundancy and version-control complexity. The important thing to preserve is the link: "This Optimizer State was created with knowledge of MUO-42 and MUO-78." That link is sufficient for audit, governance, and provenance. |
| **Healthcare campaign example** | The next cardiology campaign begins with an Optimizer State that includes: "Prior campaigns showed that workflow burden drives attention but not qualification. Distinguish attention from evaluation readiness." That knowledge is present because MUO-12 was retrieved, confirmed as applicable, and applied during Discovery. |
| **Implementation risks** | If the link between MUOs and the new Optimizer State is not explicit, the system cannot explain why the next cycle started differently. If the link is implicit (baked into the text of the new Optimizer State), provenance is lost. |

### Cross-Object Relationships

```
Optimizer State (1) ──→ (many) Premise Stack
Optimizer State (1) ──→ (1) Decision State
Decision State (1) ──→ (1) Investigation Trace
Decision State (1) ──→ (many) Learning Events
Learning Event (1) ──→ (many) Model Update Objects
Model Update Object ──→ (applied to) Future Optimizer State
```

### Versioning and Immutability

- Reasoning objects should be append-only once created. Corrections are new versions, not overwrites.
- Each version carries a timestamp, author, and reason for revision.
- The chain from Optimizer State through MUO must remain intact for audit. Breaking the chain breaks provenance.

---

## 5. Discovery / RIPC Service Pattern

### Overview

Discovery implements the Retrieve → Infer → Propose → Confirm loop as a service pattern. It is not a single API call. It is a multi-step interaction that moves from existing information surfaces through system inference to human-confirmed reasoning state.

### Step 1: Retrieve

| Dimension | Specification |
|---|---|
| **Service function** | Gather relevant information surfaces and prior reasoning objects for the current decision context. |
| **Inputs** | Workflow context (type, requester, domain), initial request text, workflow history |
| **Outputs** | Retrieved information surfaces, prior reasoning objects (Optimizer States, Premise Stacks, Decision States, MUOs), relevance scores, applicability assessments |
| **Data objects read** | Information Surface Registry, Reasoning-State Store (all six object types), Discovery Pattern records |
| **Data objects written** | Retrieval log (what was retrieved, what was omitted, why) |
| **Human interaction point** | None at this step (system-only). However, the retrieval log must be inspectable by humans. |
| **Failure modes** | Retrieval misses relevant prior reasoning (false negative). Retrieval surfaces irrelevant reasoning that anchors the system (false positive). Retrieval returns too many results, creating cognitive overload. Prior reasoning is stale but retrieved as current. |
| **Governance controls** | Retrieval must respect lifecycle status (do not retrieve deprecated or rejected reasoning without flagging it). Retrieval must surface provenance so the next step can assess trustworthiness. |

### Step 2: Infer

| Dimension | Specification |
|---|---|
| **Service function** | Construct a provisional reasoning state from the retrieved information and the current request. |
| **Inputs** | Retrieved information surfaces and prior reasoning objects, current request, workflow context |
| **Outputs** | Provisional Optimizer State (inferred goal, policy scope, interpretation), provisional Premise Stack (inferred assumptions), provisional confidence levels, identified uncertainties, identified gaps |
| **Data objects read** | Retrieved results from Step 1, Discovery Pattern records (how to ask better questions in this workflow type) |
| **Data objects written** | Draft Optimizer State, Draft Premise Stack (both marked as system-inferred, not human-confirmed) |
| **Human interaction point** | None at this step. Inference is system-only. The critical requirement is that inferred reasoning remains visibly provisional. |
| **Failure modes** | System infers a plausible-but-wrong goal. System treats its interpretation as confirmed. System anchors toward a prior reasoning object that does not apply. System fails to flag low-confidence inferences. System treats non-response as confirmation. |
| **Governance controls** | All inferred reasoning must be marked as Draft status. The system must not act on inferred reasoning without human confirmation. Inference must surface uncertainty, not hide it. |

### Step 3: Propose

| Dimension | Specification |
|---|---|
| **Service function** | Present the candidate reasoning state to the human in a form that supports confirmation, correction, rejection, qualification, or bounding. |
| **Inputs** | Draft Optimizer State, Draft Premise Stack, identified uncertainties, identified gaps, relevant prior reasoning with provenance |
| **Outputs** | A human-readable proposal that includes: inferred goal, inferred interpretation, inferred assumptions, confidence levels, prior reasoning being reused (with applicability assessment), identified uncertainties, specific questions for the human |
| **Data objects read** | Draft reasoning objects from Step 2 |
| **Data objects written** | Proposal record (what was proposed, when, to whom) |
| **Human interaction point** | **This is the primary human interaction point.** The human must be able to: confirm the reasoning, correct specific elements, reject the entire interpretation, qualify with additional boundaries, bound the applicability, add information the system does not have, and identify that the proposal is asking the wrong question. |
| **Failure modes** | Proposal is too complex for the human to evaluate. Proposal uses framework jargon instead of plain language. Proposal anchors the human toward accepting the system's interpretation. Proposal does not expose enough uncertainty for the human to make an informed judgment. Confirmation fatigue leads to rubber-stamping. |
| **Governance controls** | The proposal must expose inference, uncertainty, confidence, and provenance. It must not bury important qualifications in long text. It must be designed to make correction and rejection easy, not just confirmation. Confirmation fatigue is a design problem, not a user problem. |

### Step 4: Confirm

| Dimension | Specification |
|---|---|
| **Service function** | Record the human's response and update reasoning objects accordingly. |
| **Inputs** | Human response (confirmation, correction, rejection, qualification, bounding, re-entry request) |
| **Outputs** | Updated reasoning objects with status changed from Draft to Provisional or Validated. Re-entry signal if the human's response reveals new uncertainty that requires another Retrieve → Infer → Propose cycle. |
| **Data objects read** | Draft reasoning objects from Steps 2–3, human response |
| **Data objects written** | Updated Optimizer State (status: Provisional or Validated), updated Premise Stack (status: Provisional or Validated), confirmation record (who confirmed, what they confirmed, what they changed, what authority they held) |
| **Human interaction point** | This step records the human's judgment. The human has already interacted in Step 3. |
| **Failure modes** | Human confirms without reading (confirmation fatigue / automation bias). Human lacks authority to confirm the reasoning (wrong person in the loop). Confirmation is recorded but not linked to the reasoning objects it governs. Human correction is lost because the system overwrites rather than versions. |
| **Governance controls** | Confirmation must be linked to a specific human with traceable authority. Confirmation must be version-preserving (the Draft version is retained; the Provisional version is a new record). Re-entry must be supported: if confirmation reveals that the proposal was asking the wrong question, the system must be able to restart the loop rather than forcing a yes/no. |

### Re-Entry Logic

Confirmation may reveal that the system needs to re-enter the loop. This happens when:

- The human provides information that changes the goal or interpretation fundamentally
- The human identifies that a critical information surface was not retrieved
- The human rejects the entire framing and the system needs to start from a different premise
- The human's correction creates a new uncertainty that was not previously visible

Re-entry is not failure. It is the system learning from human feedback within the current decision cycle.

### Confirmation Fatigue and Automation Bias

These are first-class design concerns, not edge cases.

| Risk | Mitigation direction |
|---|---|
| Confirmation fatigue | Minimize confirmation requests to those that materially affect the decision. Do not ask humans to confirm reasoning that is already validated and unchanged. Use Discovery Patterns to learn which confirmations matter most for each workflow type. |
| Automation bias | Expose the system's uncertainty and the inferential basis for its proposal. Do not present proposals as conclusions. Make correction and rejection as easy as confirmation. Track whether humans are confirming without meaningful review (e.g., confirmation time < reading time). |

---

## 6. Reasoning-Relevant Retrieval Architecture

### Why this is a first-class section

This is the core implementation challenge of the HLD.

The paper states: "Retrieval must be by reasoning relevance, not just semantic similarity." The Stage 2 Systems Architecture reviewer identified this as the most technically underspecified part of the framework. The HLD planning notes state: "Reasoning-relevant retrieval is not semantic document retrieval."

If the HLD does not address this challenge explicitly, the architecture reduces to ordinary RAG with extra metadata — which does not solve the problem the framework identifies.

### How reasoning-relevant retrieval differs from semantic document retrieval

| Ordinary semantic retrieval | Reasoning-relevant retrieval |
|---|---|
| Asks: what documents sound similar to this request? | Asks: what prior reasoning is relevant to this decision? |
| Matches by text similarity | Matches by goal, policy scope, premise, confidence, applicability, provenance, workflow context, and outcome history |
| Returns documents | Returns reasoning objects with metadata about why they matter |
| Ranks by similarity score | Ranks by reasoning relevance: how closely the prior decision context matches the current one |
| Does not require human confirmation of reuse | Requires human confirmation that the prior reasoning applies to the current situation |
| Does not track reuse effectiveness | Tracks whether reused reasoning improved the next cycle |

### What must be indexed

Every reasoning object must carry structured metadata that supports retrieval. The minimum indexable fields are:

| Field | Purpose |
|---|---|
| goal / working objective | Find prior reasoning with similar objectives |
| policy_scope | Find prior reasoning governed by similar constraints |
| assumptions / premise statements | Find prior reasoning that shared similar working assumptions |
| confidence_level | Filter by how confident the prior reasoning was |
| evidence_basis | Find prior reasoning supported by similar or overlapping evidence |
| applicability_boundary | Filter by where the prior reasoning claims to apply |
| non_applicability_boundary | Filter out prior reasoning that explicitly does not apply to the current context |
| workflow_context | Find prior reasoning from the same or similar workflow type |
| audience / segment / operating context | Find prior reasoning about similar audiences or operating conditions |
| outcome (if available) | Find prior reasoning where the outcome is known |
| validation_status | Filter by lifecycle status (do not treat Draft reasoning the same as Validated reasoning) |
| deprecated / superseded status | Exclude or flag reasoning that has been replaced |
| human_confirmation_history | Show whether prior reasoning was confirmed, corrected, rejected, or bounded by a human |
| provenance | Show who created the reasoning, when, and under what authority |
| reuse_history | Show whether the reasoning has been reused before, and whether reuse improved outcomes |

### What must be searchable

The retrieval system must support queries that combine:

1. **Semantic search** — find reasoning objects whose text is similar to the current request
2. **Structured metadata filters** — narrow results by goal, policy scope, applicability boundary, confidence, status, workflow type, audience, and provenance
3. **Negative filters** — exclude reasoning objects whose non-applicability boundaries match the current context
4. **Status filters** — distinguish Draft, Provisional, Validated, Deprecated, Superseded, and Rejected reasoning
5. **Recency and staleness** — weight more recent reasoning higher, flag reasoning that has not been validated recently

### What must be visible to the user at retrieval time

When reasoning objects are surfaced, the user must see:

- What the prior reasoning says (the content)
- Why the system thinks it is relevant (the match rationale)
- How confident the prior reasoning was (confidence level)
- Who confirmed it and when (provenance)
- Where it claims to apply and where it does not (applicability boundaries)
- What its current status is (lifecycle state)
- Whether it has been reused before and whether reuse was successful (reuse history)

### How the architecture prevents "top 10 similar chunks" from being mistaken for reasoning reuse

| Failure mode | Architectural prevention |
|---|---|
| System retrieves semantically similar text that is not reasoning | Reasoning objects are stored separately from documents. Retrieval from the reasoning-state store returns objects with structured metadata, not text chunks. |
| System retrieves relevant reasoning but does not show why it matters | Every retrieved reasoning object must be presented with its match rationale, not just its content. |
| System reuses prior reasoning without human confirmation | Human confirmation is required before prior reasoning shapes the current decision. The system proposes; the human confirms. |
| System treats all retrieved reasoning as equally authoritative | Lifecycle status and confidence levels distinguish Draft from Validated, high-confidence from low-confidence, recent from stale. |
| System retrieves deprecated or superseded reasoning | Status filters exclude deprecated/superseded reasoning by default. If surfaced for context, these must be visibly marked. |
| System applies a lesson beyond its applicability boundary | Applicability boundaries are displayed with the retrieved reasoning. The human confirms that the boundary matches the current context. |

### When not to retrieve or reuse prior reasoning

- When the workflow is genuinely novel and no prior reasoning applies
- When all relevant prior reasoning is deprecated or superseded
- When the applicability boundary of prior reasoning does not match the current context
- When the prior reasoning was created under different policy constraints that no longer apply
- When the human explicitly rejects the relevance of prior reasoning
- When retrieval would anchor the system toward a prior interpretation that constrains fresh investigation

---

## 7. Governance and Lifecycle Planning

### Lifecycle States

| State | Definition |
|---|---|
| **Draft** | System-inferred or human-initiated reasoning that has not been confirmed. May be wrong. Must be visibly marked as unconfirmed. |
| **Provisional** | Reasoning that has been proposed and partially confirmed but has not yet been validated by outcome or authoritative review. |
| **Validated** | Reasoning that has been confirmed by an authorized human and, where applicable, supported by outcome evidence. |
| **Deprecated** | Reasoning that was once valid but is no longer current. The world changed, the policy changed, or the assumption was contradicted. Retained for audit; not surfaced as active guidance. |
| **Superseded** | Reasoning that has been explicitly replaced by newer reasoning. The superseding object must link to the superseded one. |
| **Rejected** | Reasoning that was proposed but found to be incorrect, overgeneralized, or unsupported. Retained for audit; not surfaced as guidance. |
| **Archived** | Reasoning that has aged past its relevance window. Retained for compliance and historical analysis; not actively retrieved. |

### Governance Rules by Lifecycle State

| State | Who can create | Who can transition to this state | Evidence required | Audit trail | Conflict resolution |
|---|---|---|---|---|---|
| **Draft** | System (via inference) or any user | Automatic on creation | None | Creation timestamp, creator, source information | N/A |
| **Provisional** | System (via proposal) or user | Human who received the proposal, or domain expert | Human confirmation of plausibility | Confirmation timestamp, confirmer identity, what was confirmed vs. changed | If multiple humans disagree, both positions are preserved with attribution |
| **Validated** | N/A (transition only) | Authorized reviewer, domain expert, or governance owner | Outcome evidence or authoritative review | Review timestamp, reviewer identity, evidence cited, scope of validation | Escalation to governance owner if reviewers disagree |
| **Deprecated** | N/A (transition only) | Domain expert, governance owner, or system (via staleness detection) | Evidence of changed conditions, contradicting outcome, or policy change | Deprecation reason, deprecator identity, timestamp | If contested, retain as Provisional with a dispute flag |
| **Superseded** | N/A (transition only) | Author of the superseding reasoning, or governance owner | The superseding reasoning object must exist and be at least Provisional | Link to superseding object, supersession reason, timestamp | The superseded object is retained; both are visible during the transition period |
| **Rejected** | N/A (transition only) | Reviewer, governance owner, or the confirming human | Explanation of why the reasoning is incorrect or unsupported | Rejection reason, rejector identity, timestamp | If the rejector and creator disagree, escalate to governance owner |
| **Archived** | N/A (transition only) | System (via retention policy) or governance owner | Retention period elapsed, or manual archive decision | Archive timestamp, retention policy reference | N/A |

### Staleness Detection

The architecture must detect stale reasoning. Staleness indicators include:

- Time since last validation exceeds the workflow's review period
- The policy or regulatory context has changed since the reasoning was created
- The reasoning has been reused but outcomes have not been tracked
- The reasoning references information surfaces that have been updated since creation
- The reasoning has not been accessed or retrieved in a defined period

Stale reasoning should be flagged for review, not automatically deprecated.

---

## 8. Human Roles and Permissions

### Role Definitions

| Role | Description |
|---|---|
| **Requester / Operator** | The person who initiates a workflow and interacts with Discovery. May be a marketer, support agent, analyst, or any workflow participant. |
| **Domain Expert** | The person with subject-matter authority over the decision domain. May confirm premises, validate evidence, and assess applicability boundaries. |
| **Reviewer / Approver** | The person who reviews reasoning objects before they are promoted to Validated status. May be a manager, compliance reviewer, or quality lead. |
| **Governance Owner** | The person responsible for the overall health of the reasoning-state layer. Manages lifecycle policies, resolves disputes, and ensures that governance controls are operating. |
| **System Steward** | The person who manages the technical health of the reasoning-state system. Monitors retrieval quality, staleness, volume, and integration. |
| **Architect / Platform Owner** | The person who designs and maintains the reasoning-state architecture. Makes schema, retrieval, and integration decisions. |
| **Auditor** | The person who reviews the reasoning-state layer for compliance, provenance, and appropriate use. May be internal or external. |
| **Executive Sponsor** | The person who funds and prioritizes reasoning-state architecture work. Needs visibility into value and risk, not implementation detail. |

### Permissions Matrix

| Action | Requester | Domain Expert | Reviewer | Governance Owner | System Steward | Architect | Auditor | Exec Sponsor |
|---|---|---|---|---|---|---|---|---|
| Create Draft reasoning | Yes | Yes | No | No | No | No | No | No |
| Confirm proposed reasoning (Draft → Provisional) | Yes (own workflow) | Yes | Yes | Yes | No | No | No | No |
| Validate reasoning (Provisional → Validated) | No | Yes | Yes | Yes | No | No | No | No |
| Reject reasoning | No | Yes | Yes | Yes | No | No | No | No |
| Modify reasoning (creates new version) | Yes (own workflow) | Yes | Yes | Yes | No | No | No | No |
| Deprecate reasoning | No | Yes | No | Yes | No | No | No | No |
| Supersede reasoning (with new MUO) | No | Yes | Yes | Yes | No | No | No | No |
| Archive reasoning | No | No | No | Yes | Yes | No | No | No |
| Audit reasoning trail | No | No | No | Yes | No | No | Yes | No |
| Configure retention policies | No | No | No | Yes | Yes | Yes | No | No |
| View governance dashboards | No | No | Yes | Yes | Yes | Yes | Yes | Yes |

---

## 9. Workbook-to-HLD Translation

### How Appendix A / Practitioner Workbook outputs become HLD inputs

The Decision Topography Interview produces structured answers. Each answer category maps to a specific architecture requirement.

| Interview output | Architecture requirement | HLD component |
|---|---|---|
| "What kind of work keeps coming back?" → repeated workflow | Workflow boundary definition | First implementation slice; workflow-scope record |
| "What result would make this worth improving?" → actual goal | Working objective for the optimizer state | Goal field in Optimizer State record |
| "What do people actually check before deciding?" → information sources | Information-surface registry | Retrieval configuration; information-surface records |
| "What information do people trust, ignore, or argue about?" → confidence landscape | Confidence-display and retrieval-weighting rules | Confidence metadata on retrieved surfaces; trust-level indicators |
| "What do people keep finding out too late?" → repeated surprises | Retrieval priorities; prediction-error triggers | Retrieval rules that surface this information earlier; Learning Event triggers |
| "What are we acting as though we already know?" → hidden assumptions | Premise Stack records | Premise Stack schema; assumption-capture in Discovery |
| "What rules can change the answer?" → policy constraints | Policy-retrieval linkages; escalation conditions; governance gates | Policy-scope field in Optimizer State; governance-gate specifications |
| "Where does the team move too fast?" → premature-sufficiency patterns | Sufficiency-gate design targets | Sufficiency-condition specification; investigation triggers |
| "When should the system stop and ask a person?" → escalation triggers | Escalation rules; approval gates; human-confirmation triggers | Escalation-service configuration; abstention conditions |
| "What would make us say 'we know enough to act'?" → sufficiency criteria | Sufficiency-condition specification | Structured stopping criteria that replace "the draft sounds good" |
| "What mistake should have changed the next run?" → prior lessons | Model Update Object records | MUO schema; MUO retrieval; MUO reuse governance |
| "Six weeks from now, what would someone need to know?" → reasoning preservation scope | Reasoning-state preservation scope for this workflow | Which reasoning objects are captured for this workflow type |
| "What was the system trying to accomplish?" → working frame | Optimizer State record | Optimizer State schema (goal, policy, interpretation) |
| "What belief made this choice seem reasonable?" → working assumptions | Premise Stack record | Premise Stack schema (statement, confidence, evidence, boundary) |
| "What did we choose, reject, and why did we stop looking?" → decision rationale | Decision State record | Decision State schema (chosen, rejected, sufficiency rationale) |
| "How did we get from uncertainty to confidence?" → investigation path | Investigation Trace record | Investigation Trace schema (questions, sources, contradictions, evidence) |
| "What should the system know to ask next time?" → Discovery patterns | Discovery Pattern record | Discovery Pattern schema; RIPC configuration per workflow type |
| "What actually happened?" → outcome | Outcome record | Outcome-capture service; prediction-error detection |
| "What turned out differently than expected?" → prediction error | Learning Event trigger | Prediction-error record; Learning Event schema |
| "What did we learn was actually going on?" → evidence-supported explanation | Learning Event record | Evidence-supported-explanation field in Learning Event |
| "What should change next time?" → reusable lesson | Model Update Object | MUO schema (update target, content, applicability, confidence) |
| "Where should this lesson apply and not apply?" → applicability boundaries | MUO applicability and non-applicability boundaries | Applicability-boundary and non-applicability-boundary fields |
| "Did the next run actually get smarter?" → effectiveness signal | Effectiveness tracking | Reuse-outcome comparison; effectiveness metric |

---

## 10. Minimal Viable Implementation

### Shape

A narrow first implementation follows this sequence:

1. **Choose one repeated decision workflow.** Select a workflow where decisions recur, outcomes matter, and one cycle should help the next cycle improve. Criteria: the workflow repeats at least monthly, the team can articulate what "better" looks like, outcomes are observable, and the team is willing to participate in Discovery.

2. **Define a small schema for reasoning-state objects.** Implement the six reasoning objects with minimal fields. Do not attempt to capture every possible metadata field. Start with: goal, interpretation, key premises (3–5), sufficiency rationale, and outcome. Add fields as implementation experience reveals what matters.

3. **Capture reasoning in one workflow cycle.** Run Discovery on one instance of the chosen workflow. Capture an Optimizer State, Premise Stack, and Decision State. This is manual-heavy in the first cycle. That is expected.

4. **Retrieve prior reasoning with semantic + metadata search.** When the workflow repeats, retrieve the prior cycle's reasoning objects. Combine semantic search (find textually similar reasoning) with structured metadata filters (match by goal, workflow type, audience, policy scope). Start with simple filters; do not attempt full reasoning-relevant retrieval in v1.

5. **Present applicability boundaries and confidence.** When surfacing prior reasoning, show the user: what the prior reasoning says, how confident it was, where it applies, and where it does not. Do not present prior reasoning as established truth.

6. **Require human confirmation before reuse.** The human must confirm that the prior reasoning applies to the current situation before the system incorporates it into the current cycle's reasoning state.

7. **Capture outcome.** After the workflow completes, record the outcome. Compare the outcome to the prediction (what was expected).

8. **Create Learning Event and MUO only when evidence supports it.** Do not create a Model Update Object for every outcome. Create one only when the outcome contradicts expectations and the team can identify an evidence-supported explanation for the gap.

9. **Apply MUO to the next cycle.** When the workflow repeats again, retrieve the MUO during Discovery. Present it with its applicability boundary and confidence. The human confirms whether it applies.

10. **Observe whether the next cycle changes.** Track whether the system started from a better place. Did it avoid the prior mistake? Did the preserved reasoning reach the right moment? This is the effectiveness signal.

### What should NOT be built in the first implementation

| Not yet | Why |
|---|---|
| Full lifecycle governance workflow | Too much process for a first cycle. Start with Draft → Provisional → Validated only. |
| Automated staleness detection | Requires enough reasoning objects to measure staleness patterns. Manual review is sufficient initially. |
| Multi-workflow reasoning-object governance | Start with one workflow. Cross-workflow governance is a maturity concern. |
| Integration with existing agentic frameworks | Start with a standalone reasoning-state store. Integration is a second-phase concern. |
| Automated MUO creation | MUOs should be human-created and human-reviewed in the first implementation. Automated creation risks creating noise. |
| Complex retrieval ranking | Start with simple semantic + metadata filters. Sophisticated ranking requires enough data to tune. |
| Full audit and compliance infrastructure | Start with basic provenance tracking (who, when, what). Full audit is a maturity concern. |
| Reasoning-object versioning system | Start with append-only storage. Versioning becomes important when reasoning objects are frequently updated. |

---

## 11. Integration with Existing Systems

### Integration Principles

The reasoning-state layer is not a replacement for existing systems. It sits alongside them. It adds a reasoning layer on top of the context, document, workflow, analytics, and governance systems that already exist.

### Integration Points

| Existing system type | Integration pattern |
|---|---|
| **RAG systems** | The reasoning-state store is a new retrieval source alongside existing document stores. RAG retrieval continues to work for document-level context. Reasoning-state retrieval adds goal-scoped, policy-scoped, confidence-weighted reasoning objects. The two retrieval paths feed into the same Discovery loop. |
| **Document repositories** | Documents remain the primary information surfaces. The reasoning-state layer adds metadata about how documents were used in prior decisions — which document supported which premise, which was consulted during investigation, which was cited in the sufficiency rationale. |
| **Workflow tools** | Workflow tools (project management, ticketing, task systems) define the workflow boundary. The reasoning-state layer hooks into workflow events: workflow start triggers Discovery; workflow completion triggers outcome capture; workflow repetition triggers prior-reasoning retrieval. |
| **CRM / marketing platforms** | CRM records provide audience, account, and campaign context. The reasoning-state layer adds reasoning about why specific audiences were targeted, what assumptions shaped the segmentation, and what prior campaigns taught about qualification signals. |
| **Analytics systems** | Analytics provide outcome data. The reasoning-state layer adds the prediction (what was expected) that makes the outcome interpretable as a prediction error. Without the prediction, the outcome is just a number. |
| **Policy repositories** | Policy repositories provide the constraints. The reasoning-state layer connects specific policies to specific decisions — which policy was consulted, which was relevant but not retrieved, which was overridden and by whom. |
| **Agent orchestration frameworks** | Agent frameworks (LangChain, CrewAI, AutoGen, etc.) orchestrate agent behavior. The reasoning-state layer provides the reasoning context that shapes agent action: the confirmed Optimizer State, the active Premise Stack, the sufficiency criteria, and the governance gates. The integration point is the agent's context window or state management system. |
| **Approval / governance systems** | Existing approval systems handle permissions and sign-offs. The reasoning-state layer adds reasoning provenance to the approval chain: not just "who approved" but "what reasoning did they approve, with what confidence, and with what boundaries." |
| **Audit systems** | Existing audit systems log actions. The reasoning-state layer adds reasoning audit: what reasoning objects were used, by whom, with what effect, and whether the reasoning was confirmed, overridden, or ignored. |

### No vendor-specific claims

The HLD must remain platform-agnostic. It should specify integration patterns (what data flows between the reasoning-state layer and existing systems), not product integrations (how to connect to Salesforce, Jira, or LangChain specifically).

---

## 12. Risks and Mitigations

| # | Risk | Description | Why it matters | Likely mitigation | HLD must address directly? |
|---|---|---|---|---|---|
| 1 | **State explosion** | If every workflow cycle produces six reasoning objects, the volume of preserved reasoning becomes unmanageable over time. | Volume degrades retrieval quality, increases storage costs, and makes governance harder. | Retention policies. Not every workflow needs full reasoning capture. Start with selective capture of high-value workflows. Archive reasoning that has aged past its relevance window. Summarize rather than retain at full detail after a defined period. | Yes |
| 2 | **Stale reasoning** | Prior reasoning may become outdated as policies change, markets shift, or organizational context evolves. | Stale reasoning reused without flagging can cause worse outcomes than no reasoning at all. | Staleness detection based on time since validation, policy changes, and outcome tracking. Periodic review cycles. Lifecycle status management. | Yes |
| 3 | **False analogy / false reuse** | Prior reasoning may be retrieved and applied to a situation where it does not actually apply, because the match was surface-level rather than structural. | False reuse is worse than no reuse — it creates false confidence from prior experience. | Applicability boundaries on every reasoning object. Human confirmation of applicability before reuse. Non-applicability boundaries that explicitly exclude certain contexts. | Yes |
| 4 | **Confirmation fatigue** | Humans asked to confirm reasoning too frequently will rubber-stamp without meaningful review. | Confirmation without review is worse than no confirmation — it creates a false audit trail of human oversight. | Minimize confirmation requests to those that materially affect the decision. Learn which confirmations matter most per workflow. Track confirmation behavior (time, pattern) to detect rubber-stamping. | Yes |
| 5 | **Automation bias** | Humans may defer to system-generated reasoning because it appears authoritative, even when it is inferred and unconfirmed. | Automation bias undermines the human-in-the-loop design. The system's proposal becomes the decision by default. | Expose uncertainty and inferential basis. Make correction and rejection as easy as confirmation. Do not present proposals as conclusions. Design proposals to invite challenge, not agreement. | Yes |
| 6 | **Overcapture / surveillance** | If the system captures reasoning too aggressively, it becomes a surveillance tool that records every human thought, judgment, and uncertainty. | Workers may resist the system, game the inputs, or become unwilling to express genuine uncertainty. | Selective capture. Capture reasoning for the decision, not reasoning about everything. Give humans control over what is recorded. Do not capture reasoning that the human has not chosen to share with the system. | Yes |
| 7 | **Political misuse** | Preserved reasoning may be used to assign blame rather than improve future reasoning. A manager may use the Premise Stack to prove that a subordinate made a bad assumption, rather than to improve the system's landscape. | If the system is used as a blame tool, people will stop sharing genuine reasoning. The system will capture political reasoning instead of honest reasoning. | Governance norms that distinguish learning from blame. Access controls that limit who can see individual reasoning and under what circumstances. Aggregate learning from reasoning patterns, not individual attribution. | Yes |
| 8 | **Policy laundering** | A system-generated inference may become organizational policy by default because nobody marked it as unconfirmed and it was reused enough times. | Unreviewed system-generated reasoning can accumulate authority it was never granted. | All system-generated reasoning must be visibly marked as Draft. Promotion to Provisional or Validated requires human review. Track the origin of every reasoning object (system-generated vs. human-created). | Yes |
| 9 | **Audit overhead** | Comprehensive provenance and lifecycle tracking creates administrative burden. | If the audit overhead is too high, teams will avoid the system or game the inputs. | Automate as much audit as possible (timestamps, user identity, version tracking). Manual audit requirements should be proportional to the consequence of the reasoning. Not every reasoning object needs the same audit depth. | Yes |
| 10 | **Poor metadata quality** | Reasoning objects with incomplete, inaccurate, or inconsistent metadata degrade retrieval quality. | If metadata is wrong, retrieval by reasoning relevance becomes unreliable. | Provide metadata defaults and templates. Validate metadata at creation time. Flag reasoning objects with incomplete metadata for review. Do not require perfect metadata — require minimum viable metadata. | Yes |
| 11 | **Broken provenance** | If the chain from Optimizer State through MUO is not maintained, the system cannot explain why a decision was made or why a lesson was learned. | Broken provenance makes the system unauditable and ungovernable. | Enforce referential integrity in the reasoning-object chain. Do not allow orphaned reasoning objects. Version links rather than breaking them. | Yes |
| 12 | **Workflow integration burden** | Adding reasoning-state capture to existing workflows creates friction and slows down work. | If the burden is too high, teams will reject the system. | Start with one workflow. Minimize required fields. Use Discovery to reduce burden (infer what you can, confirm only what matters). Do not require reasoning capture for routine, low-consequence work. | Yes |
| 13 | **Human escalation bottlenecks** | If too many decisions require human confirmation, the humans become the bottleneck and the system cannot operate at useful speed. | Escalation bottlenecks defeat the purpose of AI-augmented workflows. | Escalation should be proportional to consequence and uncertainty. Routine, validated reasoning should not require re-confirmation. Build escalation thresholds that increase with system maturity and trust. | Yes |

---

## 13. Open Architecture Decisions

The following decisions must be resolved before drafting the full HLD. Some require implementation experience; others require organizational input.

| # | Decision | Options | Dependencies | Notes |
|---|---|---|---|---|
| 1 | Should reasoning objects be stored separately from documents? | (a) Separate reasoning-state store; (b) Metadata layer on top of existing document store; (c) Hybrid — separate store with links to documents | Existing infrastructure, retrieval architecture | Separate store is cleaner but requires a new system. Metadata layer reuses existing infrastructure but may not support the required query patterns. |
| 2 | What is the minimum metadata schema for v1? | Full schema from Section 4 vs. reduced schema with only goal, interpretation, key premises, sufficiency rationale, confidence, and status | Implementation team capacity, first workflow complexity | Start minimal. Add fields as implementation experience reveals what matters. |
| 3 | What lifecycle states are required for v1? | Full lifecycle (Draft → Provisional → Validated → Deprecated → Superseded → Rejected → Archived) vs. minimal (Draft → Provisional → Validated) | Governance maturity, first workflow requirements | Start with three states. Add others as the organization develops governance practices. |
| 4 | What counts as "validated" reasoning? | (a) Any human confirmation; (b) Confirmation by an authorized domain expert; (c) Confirmation plus outcome evidence; (d) Depends on consequence level | Organizational authority structures, governance requirements | This is a policy decision as much as an architecture decision. The HLD should specify the capability; the organization should define the policy. |
| 5 | Who can supersede a Model Update Object? | (a) The original creator; (b) Any domain expert; (c) Only the governance owner; (d) Anyone who creates a new MUO with stronger evidence | Organizational authority structures | Supersession is a governance question. The architecture must support it; the policy must define it. |
| 6 | How should confidence be represented? | (a) Numeric (0–1 or 1–5 scale); (b) Categorical (Low / Medium / High); (c) Evidence-linked (confidence is a function of the evidence cited); (d) Multi-dimensional (confidence in the premise vs. confidence in the applicability) | User interface design, retrieval ranking requirements | Categorical is simpler. Numeric enables ranking. Evidence-linked is most rigorous but most complex. |
| 7 | How should applicability boundaries be expressed? | (a) Free-text description; (b) Structured tags (workflow type, audience, domain, policy scope); (c) Both; (d) Learned from reuse patterns | Retrieval architecture, metadata schema | Free text is flexible but hard to match. Structured tags enable filtering but may be too rigid. Both is likely the right answer. |
| 8 | How should reasoning reuse be audited? | (a) Log every retrieval + confirmation event; (b) Log only when reasoning objects are incorporated into a decision; (c) Log retrieval, confirmation, and outcome for effectiveness tracking | Audit requirements, storage constraints | Level (c) is the most useful but also the most expensive. Start with (b) and add (a) and (c) as the system matures. |
| 9 | What should be retained versus summarized? | (a) Retain full reasoning objects indefinitely; (b) Retain full objects for N months, then summarize; (c) Retain based on lifecycle status (Validated retained longer than Draft); (d) Retain based on reuse frequency | Storage costs, retrieval quality, compliance requirements | This is a retention-policy decision. The architecture must support flexible retention; the organization must define the policy. |
| 10 | Should Discovery Patterns be stored and improved? | (a) Static configuration per workflow type; (b) Dynamic patterns that update based on which questions produced the most valuable confirmations; (c) Both — start static, enable dynamic improvement over time | Learning-loop maturity, implementation complexity | Start static. Dynamic patterns are a maturity-stage-3+ capability. |
| 11 | How does the system handle conflicting reasoning objects? | (a) Surface both with attribution; (b) Escalate to governance owner; (c) Use recency as tiebreaker; (d) Use confidence as tiebreaker; (e) Present conflict to the human and let them resolve | Governance workflows, user interface design | (e) is the default. The system should not resolve conflicts silently. |
| 12 | What is the relationship between reasoning objects and the agent's context window? | (a) Reasoning objects are injected into the context window at retrieval time; (b) Reasoning objects are stored externally and referenced by the agent; (c) Hybrid — key fields are injected, full objects are linked | Agent framework constraints, context-window limits | This is a critical integration question. The answer depends on the agent framework and the size of reasoning objects. |

---

## 14. Proposed HLD Table of Contents

### Part I: Foundation

1. **Introduction**
   - 1.1 Purpose of the HLD / Reference Architecture
   - 1.2 Relationship to the paper and Practitioner Workbook
   - 1.3 Scope and non-scope
   - 1.4 How to read this document

2. **Architecture Principles**
   - 2.1 Preserve reasoning, not just artifacts
   - 2.2 Retrieve by reasoning relevance
   - 2.3 Behavioral availability
   - 2.4 Human confirmation of applicability
   - 2.5 Confidence and provenance as first-class metadata
   - 2.6 Applicability boundaries
   - 2.7 Lifecycle status
   - 2.8 Selective capture
   - 2.9 Govern reuse, not merely storage

### Part II: Data Architecture

3. **Six-Object Reasoning-State Data Model**
   - 3.1 Optimizer State
   - 3.2 Premise Stack
   - 3.3 Decision State
   - 3.4 Investigation Trace
   - 3.5 Learning Event
   - 3.6 Model Update Object
   - 3.7 Modified Optimizer State (derived, not stored)
   - 3.8 Cross-object relationships and chain integrity
   - 3.9 Versioning and immutability model

4. **Supporting Data Objects**
   - 4.1 Information Surface records
   - 4.2 Discovery Pattern records
   - 4.3 Governance audit records
   - 4.4 Outcome records
   - 4.5 Retrieval-relevance metadata

### Part III: Service Architecture

5. **Discovery / RIPC Service Pattern**
   - 5.1 Retrieve service
   - 5.2 Infer service
   - 5.3 Propose service
   - 5.4 Confirm service
   - 5.5 Re-entry logic
   - 5.6 Discovery Pattern updates
   - 5.7 Confirmation fatigue and automation bias mitigation

6. **Reasoning-Relevant Retrieval Architecture**
   - 6.1 Why semantic retrieval is not sufficient
   - 6.2 Metadata requirements for reasoning objects
   - 6.3 Indexing strategy
   - 6.4 Query patterns: goal-based, policy-scoped, applicability-filtered
   - 6.5 Ranking and filtering
   - 6.6 Human confirmation of applicability before reuse
   - 6.7 Integration with existing vector databases and RAG systems
   - 6.8 When not to retrieve or reuse prior reasoning

7. **Learning-Loop Architecture**
   - 7.1 Outcome capture service
   - 7.2 Prediction-error detection
   - 7.3 Investigation support
   - 7.4 Evidence-supported explanation workflow
   - 7.5 Model Update Object creation
   - 7.6 MUO retrieval and reuse
   - 7.7 Effectiveness tracking

### Part IV: Governance and Operations

8. **State Lifecycle Model**
   - 8.1 Lifecycle states and definitions
   - 8.2 Transition triggers and permissions
   - 8.3 Review workflows
   - 8.4 Audit trail requirements
   - 8.5 Conflict resolution
   - 8.6 Staleness detection and expiration

9. **Human Roles and Permissions**
   - 9.1 Role definitions
   - 9.2 Permissions matrix
   - 9.3 Authority scope and provenance tracking

10. **Governance and Observability**
    - 10.1 Role-based access control
    - 10.2 Review and approval workflows
    - 10.3 Audit logging
    - 10.4 Governance dashboards
    - 10.5 Exception handling

### Part V: Integration and Implementation

11. **Integration Patterns**
    - 11.1 Integration with RAG systems
    - 11.2 Integration with document repositories
    - 11.3 Integration with workflow tools
    - 11.4 Integration with agent orchestration frameworks
    - 11.5 Integration with governance and audit systems
    - 11.6 API design principles

12. **Volume Management and Retention**
    - 12.1 Retention policies
    - 12.2 Archival and cleanup
    - 12.3 Cross-workflow reasoning-object governance
    - 12.4 Multi-team access patterns

13. **Minimal Viable Implementation**
    - 13.1 First workflow selection criteria
    - 13.2 Minimal reasoning-object schema
    - 13.3 Minimal retrieval implementation
    - 13.4 Minimal governance workflow
    - 13.5 Success criteria for the first cycle
    - 13.6 What not to build in v1
    - 13.7 Maturity model mapping (Table 8 from the paper)

### Part VI: Forward-Looking

14. **Risks and Mitigations**
    - 14.1 State explosion
    - 14.2 Stale reasoning
    - 14.3 False analogy / false reuse
    - 14.4 Confirmation fatigue and automation bias
    - 14.5 Overcapture and surveillance
    - 14.6 Political misuse
    - 14.7 Policy laundering
    - 14.8 Audit overhead
    - 14.9 Metadata quality
    - 14.10 Broken provenance
    - 14.11 Workflow integration burden
    - 14.12 Human escalation bottlenecks

15. **Open Architecture Questions**
    - Questions requiring implementation experience to resolve

16. **Appendix: Workbook-to-HLD Translation Table**
    - Full mapping from interview outputs to architecture requirements

---

## 15. Recommended Next HLD Drafting Task

### Recommendation: Draft the Reasoning-Relevant Retrieval section first (Section 6 in the proposed ToC)

### Rationale

1. **It is the hardest problem.** The Stage 2 Systems Architecture reviewer identified reasoning-relevant retrieval as the most technically underspecified part of the framework. If this section cannot be specified concretely, the rest of the HLD is weakened.

2. **It forces the data model to be real.** You cannot specify retrieval without specifying what is being retrieved. Drafting the retrieval section will force concrete decisions about the six-object data model, metadata schema, and indexing strategy.

3. **It is the section most likely to expose architectural surprises.** The gap between "retrieve by reasoning relevance" and an actual query architecture is where the hardest design decisions live. Drafting this section early surfaces those decisions before the rest of the HLD is committed.

4. **It is the section that distinguishes this architecture from generic RAG.** If the retrieval section is weak, the HLD reads like "ordinary RAG with more metadata." If it is strong, the HLD demonstrates a genuinely different approach to information architecture.

5. **It validates the core claim.** The paper's central implementation claim is that reasoning-relevant retrieval is technically and architecturally harder than ordinary semantic retrieval. The retrieval section either substantiates that claim or reveals that the claim was overstated.

### Alternative options (ranked)

| Rank | Option | Rationale |
|---|---|---|
| 1 | **Reasoning-relevant retrieval** (recommended) | Hardest problem, forces data-model concreteness, distinguishes from generic RAG |
| 2 | **Six-object data model** | Foundation for everything else; could be drafted in parallel with retrieval |
| 3 | **Minimal viable implementation** | Most directly actionable; but needs the data model and retrieval to be at least sketched |
| 4 | **Workbook-to-HLD translation** | Bridges the two companion artifacts; but the translation table in this blueprint may be sufficient for now |
| 5 | **Full HLD v0.1** | Comprehensive but risks being shallow everywhere rather than deep where it matters |

---

## No-Edit Confirmation

- Manuscript edited: No
- Figures modified: No
- Figure 8 modified: No
- References modified: No
- Full HLD drafted: No (planning blueprint only)
- Practitioner Workbook drafted: No
- Executive Summary drafted: No
- Stage 3 run: No
