# HLD / Reference Architecture v0.1 — Skeleton and Architecture Charter

**Date:** 2026-06-22
**Status:** v0.1 Skeleton / Architecture Charter. Not a complete HLD.
**Classification:** HLD v0.1 Skeleton / Architecture Charter

---

## Architecture Charter

### What This Document Is

This is the structural skeleton and architecture charter for the Perceived Topography Framework HLD / Reference Architecture. It establishes the design posture, source hierarchy, concept-to-component mapping, section structure, and review criteria before deep technical drafting begins.

### What This Document Is Not

- Not a complete HLD. Sections contain purpose, inputs, expected outputs, and open questions — not full technical specifications.
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

This skeleton preserves the 16-chapter structure from `V1_0_HLD_REFERENCE_ARCHITECTURE_PLANNING_BLUEPRINT.md` (dated 2026-06-21). The task specification's 23 required sections are mapped into this structure — additional concerns appear as subsections rather than replacements.

### Relationship to Keystone Paper and Companion Artifacts

```
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

**Section purpose:** Establish the design constraints that govern every subsequent chapter. These are derived from the paper's conceptual architecture and are non-negotiable.

**Inputs from Build Discovery Guide:** All 13 categories inform these principles, but they are sourced from the paper.

**Expected technical outputs:**
The nine principles from the blueprint, each with a one-paragraph explanation and a testable design constraint:

1. **Preserve reasoning, not just artifacts.** The unit of organizational reasoning is the optimizer state transition, not the document.
2. **Retrieve by reasoning relevance, not just semantic similarity.** Prior reasoning may be relevant because it shares a goal, policy boundary, audience assumption, or failure pattern — not because it uses similar words.
3. **Behavioral availability.** A reasoning surface is behaviorally available when it can appear at the moment it matters, with enough confidence, provenance, scope, and status for the human-agent system to know how to use it.
4. **Human confirmation of applicability before reuse.** Prior reasoning must not be silently applied to new decisions.
5. **Confidence and provenance as first-class metadata.** Every reasoning object must carry information about confidence, source, confirmation history, and evidence basis.
6. **Applicability boundaries.** Every reasoning object must carry explicit boundaries about where it applies and where it does not.
7. **Lifecycle status.** Reasoning objects are not permanent truths. They may be drafts, provisional, validated, deprecated, superseded, or rejected.
8. **Selective capture, not total capture.** Preserve the minimum reasoning structure required for future action, learning, and governance.
9. **Govern reuse, not merely storage.** The critical governance question is whether reasoning is reused appropriately, not whether it is stored.

**MVP / Future Phase:** Foundation — applies to all phases.

**Open questions:**
- Are there principles missing that implementation experience will reveal?
- Should principles be ranked or are they all co-equal constraints?

**Martin compatibility notes:** Principle 4 (human confirmation before reuse) may create friction with fully automated agent pipelines. The HLD must specify how confirmation works in agent-to-agent scenarios.

---

## Part II: Data Architecture

### Chapter 3 — Six-Object Reasoning-State Data Model

**Section purpose:** Define the data model that makes reasoning-state preservation concrete. This is the foundation for everything else — retrieval, governance, lifecycle, and learning all operate on these objects.

**Inputs from Build Discovery Guide:**
- Category 2 (Campaign Brief Structure) → Optimizer State, Decision State fields
- Category 5 (Assumptions / Premises) → Premise Stack schema
- Category 8 (Reasoning to Preserve) → all six objects, field definitions, capture triggers

**Expected technical outputs:**
- Object specifications for all six reasoning objects (from blueprint Section 4):
  1. **Optimizer State** — goal, policy_scope, interpretation, requester, workflow_id, timestamp, version
  2. **Premise Stack** — premise_id, statement, confidence_level, evidence_basis, source, assumption_type, status, applicability_boundary
  3. **Decision State** — decision_id, chosen_action, rejected_alternatives, sufficiency_rationale, confidence_at_decision, unresolved_uncertainties
  4. **Investigation Trace** — trace_id, questions_asked, sources_checked, contradictions_found, evidence_accepted/rejected, investigation_path
  5. **Learning Event** — event_id, prediction, outcome, prediction_error, evidence_supported_explanation
  6. **Model Update Object** — muo_id, update_target, update_content, evidence_basis, confidence_level, applicability_boundary, non_applicability_boundary, status
- Modified Optimizer State (derived, not stored — link between applied MUOs and new Optimizer State)
- Cross-object relationship chain and referential integrity rules
- Versioning and immutability model (append-only, version-linked)

**MVP / Future Phase:**
- MVP: minimal schema (goal, interpretation, key premises 3-5, sufficiency rationale, outcome, confidence, status)
- Future: full schema with all fields from blueprint Section 4

**Open questions (from blueprint Section 13):**
- OAD-1: Should reasoning objects be stored separately from documents, as metadata on documents, or hybrid?
- OAD-2: What is the minimum metadata schema for v1?
- OAD-6: How should confidence be represented (numeric, categorical, evidence-linked, multi-dimensional)?
- OAD-7: How should applicability boundaries be expressed (free text, structured tags, both, learned)?

**Martin compatibility notes:** If Beacon or co-worker stores reasoning-like objects, the schema must either align or provide explicit translation. The six-object model is PTF-native — it is not required to match external schemas, but interface surfaces must be defined.

---

### Chapter 4 — Supporting Data Objects

**Section purpose:** Define data objects that support the six core reasoning objects but are not reasoning objects themselves.

**Inputs from Build Discovery Guide:**
- Category 3 (KB / Information Surfaces) → Information Surface records
- Category 4 (Trust, Evidence, Confidence) → confidence and provenance metadata
- Category 10 (Retrieval Relevance) → retrieval metadata

**Expected technical outputs:**
- Information Surface records (what information sources exist, their type, authority, recency, accessibility)
- Discovery Pattern records (what interaction patterns produce valuable confirmations per workflow type)
- Governance audit records (who did what, when, to which reasoning object)
- Outcome records (what happened after the decision)
- Retrieval-relevance metadata (match rationale, applicability assessment, reuse history)

**MVP / Future Phase:**
- MVP: Information Surface records, basic governance audit, outcome records
- Future: Discovery Pattern records, full retrieval-relevance metadata

**Open questions:**
- OAD-10: Should Discovery Patterns be static configuration or dynamic patterns that update?
- What is the minimum information surface record for v1?

**Martin compatibility notes:** Co-worker indexes enterprise data (Salesforce, Zendesk, JIRA, Slack). These are information surfaces in PTF terms. The HLD must define how external information surfaces are registered without requiring them to conform to the PTF schema.

---

## Part III: Service Architecture

### Chapter 5 — Discovery / RIPC Service Pattern

**Section purpose:** Define how Retrieve → Infer → Propose → Confirm operates as a service pattern — the primary interaction loop between the system and humans.

**Inputs from Build Discovery Guide:**
- Category 11 (Human Confirmation) → confirmation-point map, RIPC Confirm specifications, confirmation-fatigue mitigations
- Category 7 (Sufficiency and Stopping) → sufficiency criteria, pre-draft blocking conditions, abstention rules
- Category 1 (Workflow Boundary) → workflow scope and entry conditions

**Expected technical outputs (from blueprint Section 5):**
- **Retrieve service:** gather relevant information surfaces and prior reasoning objects for the current decision context
- **Infer service:** construct provisional reasoning state from retrieved information and current request
- **Propose service:** present candidate reasoning state to human for confirmation, correction, rejection, qualification, or bounding
- **Confirm service:** record human response and update reasoning objects accordingly
- **Re-entry logic:** when confirmation reveals new uncertainty, restart the loop
- **Discovery Pattern updates:** learn which interaction patterns produce the most valuable confirmations
- **Confirmation fatigue and automation bias mitigation:** minimize confirmation to what materially affects the decision; track rubber-stamping signals

**MVP / Future Phase:**
- MVP: four-step RIPC loop with manual Discovery Patterns
- Future: dynamic Discovery Patterns, adaptive confirmation frequency, confirmation-fatigue detection

**Open questions:**
- How does RIPC operate in multi-agent orchestration (agent calls RIPC on behalf of human)?
- What is the minimum viable Propose interface?
- How is re-entry distinguished from a new workflow instance?

**Martin compatibility notes:** Beacon skills appear to operate as single-call tools (query → response). RIPC is a multi-step interaction. The HLD must define whether RIPC wraps around a Beacon skill call, operates alongside it, or operates at a different layer entirely.

---

### Chapter 6 — Reasoning-Relevant Retrieval Architecture

**Section purpose:** Define how prior reasoning is found by goal, policy, confidence, applicability, provenance — not just semantic similarity. This is the core implementation challenge. If this section is weak, the HLD reduces to ordinary RAG with extra metadata.

**Inputs from Build Discovery Guide:**
- Category 10 (Retrieval Relevance) → reasoning-relevance criteria, retrieval metadata, match-rationale display, false-analogy prevention
- Category 4 (Trust, Evidence, Confidence) → confidence weighting in retrieval
- Category 5 (Assumptions / Premises) → premise-based retrieval

**Expected technical outputs (from blueprint Section 6):**
- Comparison table: ordinary semantic retrieval vs. reasoning-relevant retrieval
- Minimum indexable fields for reasoning objects (goal, policy_scope, assumptions, confidence, evidence_basis, applicability_boundary, non_applicability_boundary, workflow_context, audience, outcome, validation_status, provenance, reuse_history)
- Query architecture: semantic search + structured metadata filters + negative filters + status filters + recency/staleness weighting
- User-visible retrieval metadata: content, match rationale, confidence, provenance, applicability boundaries, lifecycle status, reuse history
- Architectural prevention table for "top 10 similar chunks" failure modes
- When-not-to-retrieve criteria

**MVP / Future Phase:**
- MVP: semantic search + basic metadata filters (goal, workflow type, status). Match rationale displayed. Human confirmation before reuse.
- Future: full reasoning-relevant retrieval with multi-dimensional filtering, learned relevance ranking, cross-workflow retrieval

**Open questions:**
- OAD-12: What is the relationship between reasoning objects and the agent's context window (injected, referenced, hybrid)?
- How does reasoning-relevant retrieval scale with reasoning-object volume?
- What retrieval latency is acceptable for interactive Discovery?
- How does false-analogy prevention work in practice (beyond applicability boundaries)?

**Martin compatibility notes:** Co-worker provides enterprise data retrieval. The model router routes queries to cost-appropriate models. The HLD must define how reasoning-relevant retrieval interacts with both:
- Does reasoning-relevant retrieval run alongside co-worker retrieval, or does it consume co-worker results as information surfaces?
- Can retrieval queries route through the model router for cost optimization?

---

### Chapter 7 — Learning-Loop Architecture

**Section purpose:** Define how outcomes are captured, prediction errors are detected, learning events are created, MUOs are produced, and MUOs feed back into future cycles.

**Inputs from Build Discovery Guide:**
- Category 9 (Learning Loop) → Learning Event schema, MUO schema, outcome-capture requirements, effectiveness signal
- Category 4 (Trust, Evidence, Confidence) → evidence standards for learning

**Expected technical outputs (from blueprint Section 7 equivalent):**
- Outcome capture service (what happened after the decision)
- Prediction-error detection (comparison of expected vs. actual outcome)
- Investigation support (how the team moves from prediction error to explanation)
- Evidence-supported explanation workflow (not narrative — evidence-linked)
- MUO creation (reusable lesson with applicability boundary, confidence, evidence basis)
- MUO retrieval and reuse (surface MUOs during Discovery; human confirms applicability)
- Effectiveness tracking (did the next cycle actually improve?)

**MVP / Future Phase:**
- MVP: manual outcome capture, manual MUO creation, basic MUO retrieval during Discovery
- Future: automated prediction-error detection, multi-campaign learning aggregation, effectiveness metrics

**Open questions:**
- When is a prediction error significant enough to warrant a Learning Event (vs. noise)?
- How is "effectiveness" measured without controlled experiments?
- What prevents MUO accumulation without review (policy laundering)?

**Martin compatibility notes:** If Beacon skills produce outputs with observable outcomes, those outcomes could feed the learning loop. The HLD should define the outcome-capture interface generically, not coupled to a specific skill framework.

---

## Part IV: Governance and Operations

### Chapter 8 — State Lifecycle Model

**Section purpose:** Define how reasoning objects move through lifecycle states, who can trigger transitions, and what evidence is required.

**Inputs from Build Discovery Guide:**
- Category 12 (Ownership / Lifecycle) → lifecycle states, staleness-detection rules, review cadence
- Category 6 (Policy / Governance Boundaries) → governance rules by lifecycle state
- Category 7 (Sufficiency and Stopping) → sufficiency gates as lifecycle transitions

**Expected technical outputs (from blueprint Section 7–8):**
- Seven lifecycle states: Draft → Provisional → Validated → Deprecated → Superseded → Rejected → Archived
- Governance rules by state (who can create, who can transition, evidence required, audit trail, conflict resolution)
- Staleness detection indicators (time since validation, policy changes, unretrieved reasoning, updated source information surfaces)
- Sufficiency and stopping architecture:
  - Stop / ask / proceed / escalate / abstain gates
  - Premature sufficiency risk checks: unsupported-claim blocks, missing-info checks, grounding checks
  - Sufficiency criteria as required fields (not optional)

**MVP / Future Phase:**
- MVP: three states (Draft → Provisional → Validated), basic staleness flagging, manual sufficiency assessment
- Future: full seven-state lifecycle, automated staleness detection, adaptive sufficiency thresholds

**Open questions:**
- OAD-3: What lifecycle states are required for v1 (full seven vs. minimal three)?
- OAD-4: What counts as "validated" reasoning (any human, authorized expert, outcome evidence, consequence-proportional)?
- OAD-5: Who can supersede a Model Update Object?

**Martin compatibility notes:** If Beacon skills have their own lifecycle (versioning, deprecation), the HLD must define whether reasoning objects tied to a skill version inherit the skill's lifecycle or maintain their own.

---

### Chapter 9 — Human Roles and Permissions

**Section purpose:** Define who can do what to reasoning objects and under what authority.

**Inputs from Build Discovery Guide:**
- Category 11 (Human Confirmation) → confirmation-point map, authority requirements
- Category 12 (Ownership / Lifecycle) → ownership model, review cadence

**Expected technical outputs (from blueprint Section 8):**
- Eight role definitions: Requester/Operator, Domain Expert, Reviewer/Approver, Governance Owner, System Steward, Architect/Platform Owner, Auditor, Executive Sponsor
- Permissions matrix (who can create, confirm, validate, reject, modify, deprecate, supersede, archive, audit, configure, view)
- Authority scope and provenance tracking (confirmation is only valid from someone with the right authority)

**MVP / Future Phase:**
- MVP: two-three roles (Requester, Domain Expert, Governance Owner). Permissions enforced at the application level.
- Future: full eight-role model with granular permissions and authority-scope tracking.

**Open questions:**
- How do roles map to existing organizational titles?
- Can a single person hold multiple roles?
- How is authority scope defined (by workflow type, by domain, by content category)?

**Martin compatibility notes:** Beacon likely has its own role model (skill authors, skill consumers, administrators). The HLD must define how PTF roles map to or coexist with Beacon roles without creating conflicting authority hierarchies.

---

### Chapter 10 — Governance and Observability

**Section purpose:** Define the governance infrastructure that makes reasoning-state preservation trustworthy — access control, review workflows, audit logging, governance dashboards, and exception handling.

**Inputs from Build Discovery Guide:**
- Category 6 (Policy / Governance Boundaries) → policy-rule inventory, DO/DON'T lists, claim-type taxonomy, review gates, approval workflows
- Category 4 (Trust, Evidence, Confidence) → evidence standards, confidence display

**Expected technical outputs (from blueprint Section 10):**
- Role-based access control specifications
- Review and approval workflows (governance gates at key transitions)
- Audit logging requirements (who, what, when, to which reasoning object, with what effect)
- Governance dashboards (health of the reasoning-state layer: staleness, volume, reuse, conflicts)
- Exception handling (what happens when governance rules conflict, when authority is disputed, when escalation fails)

**MVP / Future Phase:**
- MVP: basic audit logging, simple approval gates for Draft → Validated transitions
- Future: governance dashboards, automated exception routing, governance analytics

**Open questions:**
- How is governance overhead kept proportional to consequence (not all reasoning needs the same governance depth)?
- How does governance interact with speed-of-decision requirements?

**Martin compatibility notes:** RapidSOS Marketing Context Layer demonstrated governance on intake (brand voice checking, ICP fit evaluation) and on output (brand consistency, factual grounding, source citation). The coaching model (flag and suggest, not reject) is a design pattern worth evaluating for the HLD, but it is a grounding example, not an architectural requirement.

---

## Part V: Integration and Implementation

### Chapter 11 — Integration Patterns

**Section purpose:** Define how the reasoning-state layer integrates with existing systems without replacing them.

**Inputs from Build Discovery Guide:**
- Category 3 (KB / Information Surfaces) → existing knowledge sources as information surfaces
- Category 13 (Build Translation) → integration requirements from discovery

**Expected technical outputs (from blueprint Section 11):**
- Integration patterns for nine system types:
  1. RAG systems (reasoning-state store as additional retrieval source)
  2. Document repositories (documents as information surfaces, reasoning as usage metadata)
  3. Workflow tools (workflow events trigger Discovery, outcome capture, prior-reasoning retrieval)
  4. CRM / marketing platforms (audience context as information surface)
  5. Analytics systems (outcome data that makes predictions interpretable)
  6. Policy repositories (constraints linked to specific decisions)
  7. Agent orchestration frameworks (reasoning context shapes agent action)
  8. Approval / governance systems (reasoning provenance in approval chains)
  9. Audit systems (reasoning audit alongside action audit)
- API design principles (platform-agnostic; specify capabilities, not products)

**MVP / Future Phase:**
- MVP: integration with one workflow tool and one document repository
- Future: multi-system integration, agent orchestration integration, enterprise-wide reasoning audit

**Open questions:**
- OAD-12: How do reasoning objects relate to the agent's context window?
- What is the minimum integration surface for v1?
- How does the reasoning-state layer handle systems that cannot push events (pull-based integration)?

**Martin compatibility notes:** See Chapter 18 for dedicated Martin compatibility analysis.

---

### Chapter 12 — Volume Management and Retention

**Section purpose:** Define how reasoning-object volume is managed over time so the system remains useful, not buried.

**Inputs from Build Discovery Guide:**
- Category 12 (Ownership / Lifecycle) → staleness-detection rules, review cadence, archival logic

**Expected technical outputs (from blueprint Section 12):**
- Retention policies (how long reasoning objects are actively retained vs. summarized vs. archived)
- Archival and cleanup (what triggers archival, what is preserved for compliance)
- Cross-workflow reasoning-object governance (when reasoning is shared across workflows)
- Multi-team access patterns (who can see reasoning from other teams)

**MVP / Future Phase:**
- MVP: manual retention review, basic archival by lifecycle status
- Future: automated retention policies, cross-workflow governance, summarization-before-archival

**Open questions:**
- OAD-9: What should be retained vs. summarized (indefinite, N months, by status, by reuse frequency)?
- At what volume does reasoning-object accumulation degrade retrieval quality?

**Martin compatibility notes:** N/A for this section unless enterprise data governance policies apply.

---

### Chapter 13 — Minimal Viable Implementation

**Section purpose:** Define what to build first, what to defer, and how to know if the first cycle worked.

**Inputs from Build Discovery Guide:**
- Category 1 (Workflow Boundary) → first workflow selection criteria
- Category 13 (Build Translation) → MVP scope, named inclusions and exclusions

**Expected technical outputs (from blueprint Section 13):**
- First workflow selection criteria (repeats monthly, team can articulate "better," outcomes observable, team willing to participate)
- Minimal reasoning-object schema (from blueprint: goal, interpretation, key premises 3-5, sufficiency rationale, outcome)
- Minimal retrieval implementation (semantic + basic metadata filters)
- Minimal governance workflow (Draft → Provisional → Validated only)
- Success criteria for the first cycle (did the next cycle start from a better place?)
- What NOT to build in v1 (from blueprint): full lifecycle governance, automated staleness detection, multi-workflow governance, agentic framework integration, automated MUO creation, complex retrieval ranking, full audit infrastructure, reasoning-object versioning
- Maturity model mapping (from paper Table 8, if applicable)
- 10-step implementation sequence from blueprint Section 10

**MVP / Future Phase:** This section defines MVP. Future phases are addressed in Chapter 15.

**Open questions:**
- How long should the first cycle run before evaluating effectiveness?
- What is the minimum team size for a meaningful first implementation?
- How much Discovery overhead is acceptable in the first cycle (manual-heavy is expected)?

**Martin compatibility notes:** The first implementation slice could target a marketing workflow (familiar from RapidSOS grounding) or a different domain. If the first slice is at RapidSOS or a similar organization, Beacon integration would be a natural second-phase concern — not an MVP requirement.

---

## Part VI: Forward-Looking

### Chapter 14 — Risks and Mitigations

**Section purpose:** Surface risks that could undermine the architecture and specify mitigation directions.

**Inputs from Build Discovery Guide:**
- Category 7 (Sufficiency and Stopping) → premature sufficiency risks
- Category 11 (Human Confirmation) → confirmation fatigue risks
- Category 6 (Policy / Governance) → policy laundering risks

**Expected technical outputs (from blueprint Section 12):**
13 risks with description, why-it-matters, likely mitigation, and HLD-relevance:

1. State explosion
2. Stale reasoning
3. False analogy / false reuse
4. Confirmation fatigue and automation bias
5. Overcapture and surveillance
6. Political misuse
7. Policy laundering
8. Audit overhead
9. Metadata quality
10. Broken provenance
11. Workflow integration burden
12. Human escalation bottlenecks
13. *(Additional from task spec)* Generic RAG drift — the architecture silently collapses into ordinary semantic retrieval with extra metadata

**MVP / Future Phase:** Both — some risks are MVP concerns (confirmation fatigue, workflow burden, metadata quality), others are maturity concerns (state explosion, political misuse, policy laundering).

**Open questions:**
- Which risks should have automated detection in the system vs. governance-policy mitigation?
- Are there risks missing that implementation experience will reveal?

**Martin compatibility notes:** Risk 3 (false analogy) is relevant if co-worker data is treated as reasoning without confirmation. Risk 7 (policy laundering) is relevant if Beacon skill outputs become de facto policy.

---

### Chapter 15 — Open Architecture Questions

**Section purpose:** Preserve questions that require implementation experience to resolve. These are not gaps in the HLD — they are explicitly deferred decisions.

**Inputs from Build Discovery Guide:** All 13 categories — open questions surfaced during build-input discovery.

**Expected technical outputs (from blueprint Section 13):**
12 open architecture decisions:

| # | Decision | Key Options |
|---|---|---|
| OAD-1 | Separate reasoning-state store vs. metadata layer vs. hybrid | Separate is cleaner; metadata reuses infrastructure |
| OAD-2 | Minimum metadata schema for v1 | Full schema vs. reduced (goal, interpretation, premises, sufficiency, confidence, status) |
| OAD-3 | Lifecycle states for v1 | Full seven vs. minimal three (Draft → Provisional → Validated) |
| OAD-4 | What counts as "validated" | Any human, authorized expert, outcome evidence, consequence-proportional |
| OAD-5 | Who can supersede an MUO | Original creator, domain expert, governance owner, anyone with stronger evidence |
| OAD-6 | Confidence representation | Numeric, categorical, evidence-linked, multi-dimensional |
| OAD-7 | Applicability boundary expression | Free text, structured tags, both, learned |
| OAD-8 | Reasoning reuse audit level | Every retrieval, only incorporation, full effectiveness tracking |
| OAD-9 | Retention vs. summarization policy | Indefinite, time-based, status-based, reuse-based |
| OAD-10 | Discovery Patterns: static or dynamic | Static config, dynamic learning, start static → enable dynamic |
| OAD-11 | Conflicting reasoning objects | Surface both, escalate, recency tiebreaker, confidence tiebreaker, human resolves |
| OAD-12 | Reasoning objects and agent context window | Injected, referenced externally, hybrid |

**MVP / Future Phase:** Both — some decisions must be resolved for MVP, others can be deferred.

**Open questions:** These are the open questions.

**Martin compatibility notes:** OAD-1 and OAD-12 are the most relevant to Martin integration. If Beacon or co-worker already has a reasoning-like store, the separate-vs-hybrid decision is constrained. If agent context windows are limited, injection may not be viable for large reasoning objects.

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
- Full HLD drafted: **No** (skeleton / charter only)
