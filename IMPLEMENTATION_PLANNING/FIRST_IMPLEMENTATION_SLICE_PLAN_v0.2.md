# First Implementation Slice Plan v0.2

**Date:** 2026-06-22
**Status:** v0.2 Planning Draft. Component lanes, governance posture, learning classification, and demo shape integrated from Rapid Component Capability Map. Ready for ChatGPT / Benet review before build.
**Primary source:** `REFERENCE_ARCHITECTURE/HLD_REFERENCE_ARCHITECTURE_v1.0.md`, Chapter 13.
**Companion:** `IMPLEMENTATION_PLANNING/RAPID_COMPONENT_CAPABILITY_MAP_v0.1.md`

---

## 1. Purpose

This artifact is the planning bridge between the accepted HLD v1.0 and actual build work. It defines the first bounded implementation slice — one repeated workflow, minimal reasoning-object schema, minimal RIPC, minimal retrieval, minimal governance, manual learning.

### What this is

- A scope definition for the first implementation cycle
- A workflow boundary specification
- A set of success criteria
- A list of questions to resolve before build begins

### What this is not

- Not implementation code
- Not a database schema or DDL
- Not a deployment architecture
- Not a vendor selection
- Not a product pitch
- Not an expansion of HLD Chapter 13

---

## 2. Source Hierarchy

| Priority | Source | Role in this plan |
|---|---|---|
| 1 | HLD v1.0 (`REFERENCE_ARCHITECTURE/HLD_REFERENCE_ARCHITECTURE_v1.0.md`) | Active build reference. Chapter 13 defines the MVP scope. Chapter 3 defines the data model. |
| 2 | Build Discovery Guide v1.0 (`COMPANION_ARTIFACTS/BUILD_DISCOVERY_GUIDE_v1.0.md`) | Provides discovery question structure. Category 1 (Workflow Boundary) shapes Section 4 of this plan. |
| 3 | Executive Brief v1.0 (`COMPANION_ARTIFACTS/EXECUTIVE_BRIEF_v1.0.md`) | Leadership framing. Defines the organizational language for communicating the implementation. |
| 4 | RapidSOS Marketing Context Layer (`Rapid/`) | Grounding example only. Illustrates what a marketing campaign workflow looks like in practice. Does not set architecture. |
| 5 | Martin / Beacon / co-worker | Compatibility surfaces only. Not MVP dependencies. |

---

## 3. Candidate First Workflow

### Recommended: Marketing Campaign Brief Workflow

**Why this workflow meets HLD Chapter 13 criteria:**

| Criterion | Assessment |
|---|---|
| **Decisions recur** | Campaign briefs are produced repeatedly — at least monthly, often more frequently. Each brief targets a buyer persona, uses approved messaging, and makes claims that may or may not be evidence-supported. |
| **Team can articulate "better"** | Better means: qualified pipeline (not just engagement), brand-compliant messaging, evidence-supported claims, correct audience targeting, and learning that carries to the next campaign. |
| **Outcomes are observable** | Campaign performance is measurable: engagement metrics, conversion rates, qualified pipeline generation, sales feedback on lead quality. |
| **Reasoning currently disappears** | Teams re-explain the same goals, rediscover the same claim boundaries, repeat the same premise failures (e.g., treating engagement as buying readiness), and restart from cold prompts each cycle. |
| **Team is willing to participate** | Requires confirmation during Build Discovery. The workflow is a natural fit because marketers already produce briefs and review performance — the system adds structured reasoning preservation, not a new workflow. |

**Important framing:** This marketing campaign brief workflow is the first grounding case for the Perceived Topography Framework's implementation. It is not the framework center. The architecture is domain-agnostic. The same implementation pattern applies to support ticket escalation, policy exception review, product requirement specification, or recurring compliance assessment. The marketing workflow is selected because it has observable outcomes, recurring decisions, and documented grounding material — not because the framework is a marketing tool.

---

## 4. Workflow Boundary

### Workflow Start Trigger

A new campaign brief is requested. The request may come from:

- A campaign owner initiating a new campaign
- A recurring campaign cycle reaching its next iteration
- A stakeholder requesting content for a specific audience/vertical

The start trigger initiates the RIPC loop — the system retrieves prior reasoning and information surfaces, infers a draft reasoning state, and proposes it to the human.

### Workflow End Condition

The campaign brief is finalized and approved for execution. The decision artifact (the brief itself) has been produced, and the sufficiency rationale has been captured in the Decision State.

### Decision Artifact Produced

The **campaign brief** — the output of the workflow. This is not a reasoning object. It is the artifact that the reasoning objects explain. The brief includes targeting decisions, messaging choices, claim selections, audience framing, and channel strategy.

The six reasoning objects explain how and why that brief became sufficient.

### Human Participants

| Role | PTF Role | Responsibility |
|---|---|---|
| Campaign owner / marketer | Requester | Initiates workflow, interacts with RIPC, confirms intent and local context |
| Senior marketer or product marketing lead | Domain Expert | Validates premises about audience, messaging, and claim boundaries |
| Marketing operations or knowledge manager | Governance Owner | Manages lifecycle policy, resolves conflicts, configures review periods |

### Information Surfaces Involved

| Surface | Type | Authority | Content |
|---|---|---|---|
| Brand voice guidelines | Document | Binding | DO/DON'T rules, vertical adaptations, restricted terms |
| Ideal Customer Profiles (ICPs) | Document | Advisory | Buyer personas, pain points, buying signals, decision process |
| Messaging frameworks | Document | Advisory | Product positioning, value propositions per vertical |
| Competitive positioning | Document | Advisory | Competitor comparison, differentiation language |
| Campaign playbooks | Document | Advisory | Workflow templates, channel strategy, timing guidance |
| Approved claims repository | Document | Binding | What claims can be made, with what evidence, for which audiences |
| Prior campaign performance data | Data source | Background | Engagement, conversion, pipeline metrics from past campaigns |
| Sales feedback | Data source | Anecdotal | Qualitative feedback on lead quality, buyer readiness, objections |
| Prior reasoning objects (if any exist) | Reasoning-state store | Varies by status | Prior Optimizer States, Premise Stacks, Decision States, MUOs from earlier cycles |

### Outcome Signal

After campaign execution:

- Engagement metrics (click-through, asset downloads, event attendance)
- Conversion metrics (demo requests, qualified pipeline generated)
- Sales feedback (lead quality assessment, buyer readiness signals)
- Comparison to prediction (what the Decision State expected vs. what occurred)

### Explicitly Out of Scope

- Campaign execution (the build does not run campaigns — it preserves reasoning about campaign decisions)
- Multi-channel orchestration (the build captures reasoning about the brief, not the multi-channel execution pipeline)
- Creative production (copy, design, video — these are downstream of the brief)
- CRM integration (Salesforce data may inform premises but is not ingested automatically in MVP)
- Cross-campaign reasoning (reasoning from one campaign type does not automatically shape another in the first cycle)

---

## 5. Minimal Reasoning Objects

### Always Captured

| Object | MVP Fields | Capture Trigger |
|---|---|---|
| **Optimizer State** | id, workflow_id, goal, interpretation, policy_scope, requester, status, confidence, source_type, confirmed_by, created_at, version | Created at RIPC start. System infers Draft; human confirms to Provisional. |
| **Premise Stack** (3-5 entries) | id, optimizer_state_id, statement, confidence, evidence_basis, assumption_type, status, source_type, applicability_boundary, created_at | Created during RIPC Infer. System proposes key assumptions; human confirms, corrects, or adds. |
| **Decision State** | id, optimizer_state_id, chosen_action, rejected_alternatives, sufficiency_rationale (required), confidence_at_decision, unresolved_uncertainties, reasoning_status, decision_status, created_at | Created when the brief is finalized. Sufficiency rationale is required — "why did we stop investigating?" |
| **Outcome Record** | id, decision_state_id, outcome_description, outcome_data_source, recorded_by, created_at | Created after campaign execution. Manual entry by campaign owner. |

### Conditionally Captured

| Object | MVP Fields | Capture Trigger |
|---|---|---|
| **Investigation Trace** | id, decision_state_id, questions_asked, sources_checked, contradictions_found, evidence_accepted, evidence_rejected, status, created_at | Only if the team investigates a specific uncertainty before finalizing the brief (e.g., "Is this claim approved?" → check claims repository). |
| **Learning Event** | id, decision_state_id, prediction, outcome, prediction_error, evidence_supported_explanation, linked_premise_ids, status, confidence, created_at | Only if the outcome materially contradicts expectations AND the team can identify an evidence-supported explanation. |
| **Model Update Object** | id, learning_event_id, update_target, update_content, evidence_basis, confidence, applicability_boundary, non_applicability_boundary, status, created_by, reviewed_by, created_at | Only if the learning is reusable — applies beyond the single campaign instance. Requires human creation and review. |

---

## 5.5 KB Update vs. MUO

A critical distinction that must remain clear across all components:

**A KB update changes the information surface.** It adds, revises, or removes content from the knowledge base. It changes what the system can see and retrieve. A KB update does not carry applicability boundaries, evidence basis, confidence, or lifecycle governance.

**A Model Update Object changes future reasoning.** It records an evidence-supported lesson with applicability boundaries, non-applicability boundaries, confidence, and governance lifecycle. It changes how the system interprets, trusts, and acts on what it retrieves.

**Rules:**

- A KB refresh must never silently become a MUO.
- A campaign result must never silently become reusable reasoning.
- Agent output must never become validated reasoning without human review, applicability boundaries, evidence basis, confidence, lifecycle status, and governance.
- Information refresh (new data, updated documents, refreshed competitive positioning) enters through the Information Surface Registry. It does not create or modify reasoning objects.
- Learning enters through the Learning Event / MUO pipeline. It requires prediction error, evidence-supported explanation, human authorship, and human review.

---

## 5.6 MVP Component Lanes

The first build decomposes into five MVP core components. (See `RAPID_COMPONENT_CAPABILITY_MAP_v0.1.md` for full inventory including MVP-adjacent and future components.)

| # | Component | Role | What It Modifies |
|---|---|---|---|
| 1 | **Information Surface Registry** | Register and manage information sources (brand voice, ICPs, messaging, playbooks, approved claims). Manual registration in MVP. | KB metadata only |
| 2 | **Campaign Brief Orchestrator / RIPC Agent** | Execute Retrieve → Infer → Propose → Confirm. Create Draft reasoning objects; human confirms. This is the core component. | Reasoning objects (Draft → Provisional via human confirm) |
| 3 | **Campaign Brief Generator** | Produce the decision artifact (the campaign brief) from confirmed reasoning state. Human reviews before execution. | Decision artifact only |
| 4 | **Governance / Policy / Sufficiency Agent** | Advisory mode. Flag policy violations, unsupported claims, and sufficiency concerns. Coaching posture — flag and suggest, not block. | Nothing directly. Advisory only. |
| 5 | **Outcome Capture Assistant** | Structure outcome recording after campaign execution. Display Decision State predictions for comparison. | Outcome Record only |

**MVP-adjacent components** (lightly represented, not fully automated):

| # | Component | MVP-Adjacent Posture |
|---|---|---|
| A | Human-Requested Search-to-KB Update | Human requests topic search; system searches; human reviews and manually approves what enters KB. No autonomous ingestion. |
| B | Results-to-Learning Agent | After outcome capture, highlights where outcomes diverge from predictions and flags which premises may have failed. Human investigates and confirms. |
| C | Learning Event / MUO Assistant | If human confirms a prediction error, helps structure the Learning Event and draft MUO with required fields. Human authors content; system provides template. |

**What the first build proves:** Reasoning preservation changes the next campaign cycle. The brief is the visible artifact; the reasoning objects are the proof. The core question is: when the workflow repeats, does the system start from preserved reasoning rather than a cold prompt?

---

## 6. Minimal RIPC Flow

### Step 1: Retrieve

**What Retrieve pulls:**

- Information surfaces: brand voice guidelines, relevant ICP, messaging framework for the target vertical, approved claims, relevant playbook
- Prior reasoning objects (if they exist from a prior cycle): Optimizer States, Premise Stacks, Decision States, MUOs with matching workflow type and audience
- Retrieval log: what was found, what was not found, match rationale for each surfaced item

**What is not retrieved in MVP:** Cross-workflow reasoning, deprecated reasoning (unless explicitly requested), reasoning from other teams.

### Step 2: Infer

**What Infer drafts:**

- Draft Optimizer State: inferred goal (e.g., "generate qualified demo requests from cardiology administrators"), inferred interpretation (e.g., "workflow burden as attention hook, not qualification signal"), inferred policy scope (e.g., "no direct clinical-outcome claims without approved evidence")
- Draft Premise Stack (3-5 entries): key assumptions the system identified from the request and retrieved context
- Identified uncertainties: where confidence is low or information is missing
- Identified gaps: what information surfaces are missing or stale

**All elements marked `source_type: system-inferred` and `status: Draft`.**

### Step 3: Propose

**What Propose shows the human:**

- The inferred goal and interpretation — "I think this campaign is doing X, targeting Y, under constraint Z. Is that right?"
- The inferred premises with confidence levels — "I'm assuming A (Medium confidence), B (High confidence), C (Low confidence)"
- Prior reasoning if any exists — with applicability boundary, status, confidence, and provenance displayed
- Identified uncertainties and gaps
- Specific questions for the human — focused on reasoning whose absence could materially change the brief

**The human can:** confirm, correct, reject, qualify, bound, or add information the system does not have.

### Step 4: Confirm

**What Confirm records:**

- Updated Optimizer State: status moves from Draft to Provisional
- Updated Premise Stack: status moves from Draft to Provisional
- Confirmation record: who confirmed, what they confirmed, what they changed, what role they held
- If prior MUOs were surfaced: lightweight applicability acknowledgment (human saw the MUO's boundary, confidence, and provenance and acknowledged it applies)
- If human rejects or identifies new uncertainty: re-enter the loop

### When Re-Entry Happens

- Human provides information that fundamentally changes the goal or interpretation
- Human identifies a critical missing information surface
- Human rejects the entire framing ("you're asking the wrong question")
- Human's correction creates new uncertainty not previously visible

---

## 7. Minimal Retrieval

### Document / Information-Surface Retrieval

- Semantic search over registered information surfaces (brand voice, ICPs, messaging, playbooks, approved claims)
- Category filtering where applicable (e.g., retrieve only healthcare-vertical messaging)
- Authority level displayed on each surfaced document (binding / advisory / background / anecdotal)

### Reasoning-State Retrieval

- Semantic search over prior reasoning objects (embed goal, interpretation, premise statements, MUO update content)
- Metadata filters on: workflow type (campaign brief), lifecycle status (Provisional, Validated only by default), goal keywords, audience/segment
- Negative filters on: non-applicability boundaries (exclude MUOs that explicitly do not apply to the current context)
- Match rationale displayed for every surfaced result ("same workflow type and audience segment"; "prior campaign with similar goal")
- Lifecycle status displayed on every surfaced result

### Applicability Acknowledgment

- When prior reasoning is surfaced, the human must acknowledge applicability before it shapes the current cycle
- For Validated MUOs: lightweight acknowledgment (see the boundary, confidence, provenance, status — then confirm it applies)
- For Provisional reasoning: full review (the reasoning has not been outcome-validated)

### What Is Not Included Yet

- Complex retrieval ranking (filter and display; let the human judge)
- Cross-workflow retrieval
- Automated relevance scoring
- Reuse-outcome tracking (did applying this MUO improve the next cycle?)

---

## 8. Minimal Governance

### Lifecycle States

Three states only: **Draft → Provisional → Validated**

- System-inferred reasoning always starts as Draft
- Human confirmation moves Draft → Provisional (during RIPC Confirm)
- Domain Expert or Governance Owner validates Provisional → Validated (with evidence or authoritative review)

### Requester Authority Scope

Requester confirmation is valid for:

- Their own intent, goal interpretation, local workflow context
- Whether the system understood the request correctly

Requester confirmation is **not sufficient** to validate:

- Domain claims, compliance/policy claims, evidence strength
- Cross-workflow applicability, reusable MUOs, high-consequence premises

Unless the Requester also holds Domain Expert or Governance Owner role.

### Roles

| Role | Who | What they can do |
|---|---|---|
| Requester | Campaign owner / marketer | Create Draft reasoning, confirm own intent (Draft → Provisional for own workflow) |
| Domain Expert | Senior marketer, product marketing, compliance | Validate premises, confirm applicability, promote Provisional → Validated |
| Governance Owner | Marketing operations, knowledge manager | Manage lifecycle policy, resolve conflicts, configure review periods |

### Confirmation Requirements

- Prior reasoning cannot silently shape a new decision
- Even Validated MUOs require lightweight applicability acknowledgment
- System-inferred reasoning must be visibly marked as Draft
- All state transitions logged (who, what, when, from-state, to-state)

### What Cannot Be Silently Reused

- Any reasoning object, regardless of status
- Validated MUOs (reduced review burden, not silent application)
- System-inferred premises (must remain Draft until human confirms)

### MVP Governance Posture

The Governance / Policy / Sufficiency Agent operates in **advisory mode** in the first cycle:

- **Flag and suggest.** When the agent detects a policy violation, unsupported claim, missing evidence, or insufficiently justified sufficiency rationale, it flags the issue and suggests a correction. It does not autonomously block the workflow or silently approve.
- **Expose, don't decide.** The agent surfaces policy/evidence/sufficiency issues to the human. The human decides whether to address them, override them, or accept the risk.
- **Coaching, not gating.** The pattern follows the RapidSOS Marketing Context Layer's brand voice model — coaching suggestions ("use 'augment responders' instead of 'surveillance'") rather than rejection. This is a grounding pattern, not an architectural requirement.
- **No autonomous approval.** The governance agent does not mark reasoning as compliant. It flags concerns. The human's decision to proceed (or not) is captured in the Decision State's sufficiency rationale.

Autonomous governance gating (blocking workflows, requiring approval before proceeding) is a future-phase capability that requires validated governance rules and calibrated thresholds.

---

## 9. Minimal Learning Loop

### 1. Outcome Capture

After campaign execution, the campaign owner records the outcome manually. The system displays the Decision State's prediction/expectations for comparison.

### 2. Prediction-Error Check

The human compares: what was expected (from the Optimizer State, Premise Stack, and Decision State) vs. what occurred (from the Outcome Record).

If the outcome materially contradicts expectations, proceed to step 3. If the outcome is within expected ranges, no Learning Event is needed.

### 3. Learning Event Trigger

A Draft Learning Event is created when:

- The prediction error is significant enough to change future behavior
- The team can begin to identify why the gap occurred

The Learning Event must link to specific premises that appear to have failed.

### 4. MUO Trigger

A Model Update Object is created when:

- The Learning Event has been investigated and an evidence-supported explanation exists
- The learning is reusable (applies beyond the single campaign instance)
- The update can be stated with a clear applicability boundary and non-applicability boundary

### 5. Evidence Requirement

- Explanations must be evidence-supported, not narrative ("it didn't work")
- At least one premise must be linked as the failure point
- Evidence must be cited (sales feedback, performance data, investigation findings)

### 6. Manual Review Requirement

- MUOs start as Draft
- MUOs require Domain Expert or Governance Owner review before they can shape future cycles
- An unreviewed MUO must not become policy by default

### Learning Component Classification

| Component | MVP Classification | Posture |
|---|---|---|
| **Outcome Capture Assistant** | MVP core | Structures outcome recording. Human provides the data. |
| **Results-to-Learning Agent** | MVP-adjacent | May highlight possible prediction errors and flag which premises may have failed. Human investigates and confirms. The agent proposes; it does not conclude. |
| **Learning Event / MUO Assistant** | MVP-adjacent | May structure draft Learning Events or draft MUOs with required fields (applicability boundary, evidence, confidence). Human authors the content and reviews before any reasoning object is created. |

MVP-adjacent means: the system provides prompts, highlights, and templates. The human does the reasoning work. No Learning Event or MUO is created, promoted, or applied without explicit human action.

---

## 10. MVP Explicit Exclusions

Carried forward from HLD Chapter 13:

| Excluded | Why |
|---|---|
| Full seven-state lifecycle governance | Three states sufficient for first cycle |
| Automated staleness detection | Requires enough reasoning objects to measure patterns |
| Multi-workflow reasoning-object governance | Start with one workflow |
| Integration with agent orchestration frameworks | Standalone reasoning-state store first |
| Automated MUO creation | Risk of noise and policy laundering |
| Complex retrieval ranking | Simple filters sufficient; ranking requires data to tune |
| Full audit and compliance infrastructure | Basic provenance tracking sufficient initially |
| Reasoning-object versioning UI | Append-only storage; version comparison not needed yet |
| Dynamic Discovery Patterns | Static question sets; dynamic requires usage data |
| Automated sufficiency gates | Human-reviewed sufficiency; automated requires calibration |
| Confirmation fatigue detection | Requires baseline data from multiple cycles |
| Autonomous KB ingestion / topic monitoring | Changes retrieval landscape without governance. Must understand what information surfaces matter before automating refresh. Revisit after 3+ cycles with stable KB. |
| Automatic KB refresh cycles | Same as above — KB changes must be human-reviewed in MVP. |

---

## 11. Martin / Beacon / Co-Worker Interface Notes

### MVP Status: Not integrated. Design for later.

Martin / Beacon / co-worker are compatibility surfaces, not MVP dependencies. The first implementation slice operates as a standalone reasoning-state system.

### What May Later Interface Through MCP

- The reasoning-state layer could expose as an MCP server (compatible with Beacon's skill discovery)
- MCP tools: `search_reasoning_objects`, `get_optimizer_state`, `get_premise_stack`, `compose_with_reasoning`

### What Co-Worker Could Provide as Information Surfaces

- Enterprise data (Salesforce deal history, Zendesk support tickets, Slack conversations)
- These would be registered as information surfaces with authority level `background` or `anecdotal`
- Co-worker data is input to reasoning, not reasoning itself

### What Beacon Could Later Expose as Skills

- The reasoning-state layer registered as a Beacon skill, discoverable by other MCP clients
- Other Beacon skills (Security Review, Feature Alignment) could produce outputs that become information surfaces for the reasoning-state layer

### Why These Are Not MVP Dependencies

- Integration requires answers to open integration questions (HLD Appendix C, OAD-1, OAD-12)
- Premature integration risks designing the PTF architecture around Beacon's constraints
- The reasoning-state layer must be independently validated before external systems consume it
- MCP-compatible interfaces can be added later without re-architecting

---

## 12. Success Criteria for First Cycle

The first cycle succeeds if:

| # | Criterion | How to assess |
|---|---|---|
| 1 | **Reasoning was captured** | The workflow produced at least an Optimizer State, Premise Stack, Decision State, and Outcome Record that were not previously preserved. |
| 2 | **The next cycle started differently** | When the workflow repeated, prior reasoning was retrieved and the starting state was richer than a cold prompt. The system proposed a draft reasoning state from prior context. |
| 3 | **Prior reasoning was behaviorally available** | Prior reasoning appeared at the moment it mattered — during brief creation — not only when explicitly searched. |
| 4 | **Sufficiency rationale was captured** | The Decision State recorded why investigation stopped, not just what was decided. |
| 5 | **Premises were visible** | The Premise Stack was displayed at the sufficiency point so the human could review which assumptions were active. |
| 6 | **A human confirmed applicability** | Prior reasoning was not blindly applied. A human assessed whether prior reasoning applied to the new context. |
| 7 | **Prediction error was detectable** | If the outcome contradicted expectations, the system made the gap visible by comparing the outcome to the Decision State's prediction. |
| 8 | **The team avoided re-explaining** | The team did not need to re-state the same goals, re-discover the same claim boundaries, or re-learn the same premise failures from scratch. |

The first cycle does **NOT** need to produce:

- A Model Update Object
- Automated sufficiency gates
- Cross-workflow reasoning reuse
- Quantitative evidence of measurable improvement
- Integration with external systems

---

## 13. Open Questions Before Build

### Must Answer Before Build

| # | Question | Why it blocks |
|---|---|---|
| 1 | **Storage: separate reasoning-state store or metadata layer?** (OAD-1) | Determines storage architecture and retrieval implementation. Recommendation: separate store for cleaner query patterns. |
| 2 | **What is the initial information-surface inventory?** | The Retrieve step needs registered surfaces to search. Must identify and register the first set of documents (brand voice, ICPs, messaging, playbooks, approved claims). |
| 3 | **Who fills the three MVP roles for the first cycle?** | Requester, Domain Expert, and Governance Owner must be named people with availability. |
| 4 | **Which specific campaign is the first cycle?** | Must select one upcoming campaign to run the first cycle on. Criteria: recurring type, observable outcome, team willing to participate. |
| 5 | **What is the interaction medium for RIPC?** (OAD-14) | Command-line, web form, conversational exchange, IDE plugin? The Propose step must support confirm/correct/reject/qualify/bound. |

### Can Answer During Build

| # | Question | When it becomes relevant |
|---|---|---|
| 6 | How should confidence be displayed? (OAD-6) | During Propose UI implementation. Start with categorical (Low/Medium/High). |
| 7 | What static Discovery Pattern questions work for this workflow? | During RIPC implementation. Start with Build Discovery Guide Category 1-2 questions adapted for campaign briefs. |
| 8 | How much reasoning capture overhead is acceptable? | After the first RIPC run. Adjust based on team feedback. |
| 9 | What outcome data is available and when? | After the first campaign executes. Depends on analytics infrastructure. |

### Defer Until Future Phase

| # | Question | Why it can wait |
|---|---|---|
| 10 | How does reasoning-relevant retrieval scale? | Volume is negligible in the first cycle. |
| 11 | How should applicability boundaries be structured? (OAD-7) | Free text is sufficient for MVP. Structured tags require enough data to define categories. |
| 12 | When should Discovery Patterns become dynamic? (OAD-10) | After 5+ cycles with static patterns. |
| 13 | How does the reasoning-state layer integrate with agent orchestration? (OAD-12) | After the data model and retrieval are validated. |
| 14 | How do PTF roles map to Beacon roles? | After the PTF layer is independently validated and Martin integration is planned. |

---

## 14. Recommended Next Repository Action

### Option A (Recommended): Run Build Discovery Guide against the selected workflow

Use Build Discovery Guide v1.0, Categories 1-3 (Workflow Boundary, Campaign Brief Structure, KB/Information Surfaces) against the selected first campaign. This produces:

- Concrete workflow boundary specification
- Campaign brief field inventory
- Information surface registry

This is the highest-value next step because it grounds the plan in real organizational content rather than theoretical structure.

### Option B: Review this slice plan with ChatGPT / Benet

If the candidate workflow needs conceptual validation before discovery, review this plan first. Confirm the workflow selection, role assignments, and scope boundaries.

### Option C: Create a data model sketch

Translate HLD Chapter 3 MVP fields into a concrete schema sketch (not DDL, not implementation code — a structured specification that the build team can implement). This is useful if the build team wants to validate the data model before running Discovery.

### Option D: Create a build backlog

Convert this plan's sections into a sequenced build backlog (tasks, dependencies, acceptance criteria). This is useful if the build team wants a structured work plan.

**Recommended sequence:** B → A → C → D. Review the plan, then run discovery, then sketch the data model, then create the backlog.

### Component Decomposition Reference

For the full component inventory (MVP, MVP-adjacent, and future), governance rules by component, and proposed agent topology, see:

`IMPLEMENTATION_PLANNING/RAPID_COMPONENT_CAPABILITY_MAP_v0.1.md`

---

## 15. Demo Shape

The first demo should present **one orchestrated flow with visible stages**, not multiple independent autonomous agents. Each stage corresponds to a component in the MVP topology. The human sees the system's work at each stage and can intervene.

### Suggested Stage Sequence

```text
1. Register / select information surfaces
   → Information Surface Registry shows available sources and their authority levels

2. Retrieve
   → System searches information surfaces and prior reasoning objects
   → Retrieval log visible: what was found, what was not found, match rationale

3. Infer
   → System constructs Draft Optimizer State and Draft Premise Stack
   → All elements marked system-inferred, confidence levels visible

4. Propose
   → System presents the draft reasoning state to the human
   → Human can confirm, correct, reject, qualify, or bound

5. Confirm
   → Human response recorded
   → Reasoning objects updated (Draft → Provisional)
   → Prior MUOs acknowledged if applicable

6. Governance / sufficiency check
   → Governance agent flags policy issues, unsupported claims, sufficiency concerns
   → Advisory: flag + suggest, not block

7. Generate brief
   → Brief Generator produces the decision artifact from confirmed reasoning state
   → Human reviews before execution

8. Capture sufficiency rationale
   → Decision State records why investigation stopped
   → Premise Stack visible at sufficiency point

9. [Campaign executes — outside system scope]

10. Capture outcome
    → Outcome Capture Assistant displays predictions for comparison
    → Human records outcome

11. Optionally: prompt for learning review
    → Results-to-Learning Agent highlights prediction errors (if any)
    → Human investigates, confirms, and optionally authors Learning Event / MUO
```

**Why one orchestrated flow:** The Rapid demo showed five independent agents streaming results in sequence (Research → Brand Voice → ICP → Composition → Quality). For the PTF implementation, these agents are reconceived as stages of the RIPC + governance + outcome loop. The visible stages make the system's reasoning work transparent. The human is in the loop at stages 4, 5, 7, 10, and 11 — not only at the end.

---

## No-Edit Confirmation

- Frozen paper (`PAPER_v1.0_WORKING.md`) edited: **No**
- Figure 8 modified: **No**
- Figures modified: **No**
- References modified: **No**
- Executive Brief v1.0 edited: **No**
- Build Discovery Guide v1.0 edited: **No**
- HLD v1.0 content edited: **No**
- Scope expanded beyond HLD Chapter 13: **No**
