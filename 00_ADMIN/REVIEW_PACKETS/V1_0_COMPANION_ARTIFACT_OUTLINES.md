# v1.0 Companion Artifact Outlines

**Date:** 2026-06-21
**Status:** Outline-level plans only. No full drafts created.
**Source:** PAPER_v1.0_WORKING.md, Appendix A, Stage 2 Agent Peer Review, HLD Reference Architecture Notes.

---

## 1. Overall Companion Artifact Strategy

### Why these three artifacts exist

The paper introduces the Perceived Topography Framework as a design theory. It teaches the reader how to think about human-agent systems. But thinking is not enough. Practitioners need to know how to start, architects need to know what to build, and leaders need to know what to fund.

Three companion artifacts close those gaps:

| Artifact | Answers | Audience |
| --- | --- | --- |
| Practitioner Workbook | "How do we start?" | Facilitators, transformation leads, product owners, AI enablement teams |
| HLD / Reference Architecture | "What do we build?" | Enterprise architects, platform teams, product engineers, governance leads |
| Executive Summary / Decision Brief | "Why should we care and what should we fund?" | Executives, sponsors, business stakeholders, funding decision-makers |

### How they relate to each other

```
Paper (teaches the framework)
        ↓
Executive Summary (sells the why)
        ↓
Practitioner Workbook (runs the discovery)
        ↓
HLD / Reference Architecture (translates answers into system design)
```

The Workbook takes inputs from the paper's Appendix A and produces structured outputs. The HLD takes those outputs and translates them into architecture. The Executive Summary gives leaders enough to fund the Workbook + HLD work.

### Recommended drafting order

1. **Executive Summary / Decision Brief** — fastest to draft; needed for external sharing; enables buy-in for the other two
2. **Practitioner Workbook** — next because it expands Appendix A (which already exists) and produces the inputs the HLD needs
3. **HLD / Reference Architecture** — last because it requires workbook outputs as input and the reasoning-relevant retrieval design is the most technically complex

---

## 2. Practitioner Workbook Outline

### Proposed Title

*The Perceived Topography Practitioner Workbook: A Facilitation Guide for Designing Human-Agent Reasoning Systems*

### Audience

- Transformation leaders running AI enablement programs
- Product leaders designing AI-augmented workflows
- Marketing operations leaders building knowledge platforms
- AI enablement teams implementing reasoning-state systems
- Facilitators running discovery sessions with cross-functional teams
- Knowledge-platform owners designing for reasoning reuse

### Purpose

Turn the paper's Appendix A into a complete facilitation tool. A team should be able to pick up the workbook, run a discovery session, and produce structured outputs that feed directly into system design.

### Table of Contents

1. **Introduction: What This Workbook Does**
   - Relationship to the paper
   - Relationship to Appendix A
   - Relationship to the HLD / Reference Architecture
   - Who should use this
   - When to use this
   - What not to use this for

2. **Before You Start**
   - Choose one repeated workflow
   - Identify who should be in the room
   - Prepare the materials
   - Set expectations: this is reasoning discovery, not requirements gathering

3. **The Full Decision Topography Interview**
   - Phase 1: Map the Decision Topography (Questions 1–7)
   - Phase 2: Shape the Motion (Questions 8–11)
   - Phase 3: Preserve the Reasoning (Questions 12–17)
   - Phase 4: Make the Next Cycle Smarter (Questions 18–23)
   - For each question:
     - Facilitator script (how to ask it)
     - Expected answer types
     - Common pitfalls
     - How to record the answer
     - What the answer becomes (architecture implications)
     - Worked example from a healthcare campaign

4. **The Minimal Interview Variant**
   - 8-question subset for one-hour sessions
   - When to use the short version
   - How to decide when to go deeper

5. **Recording and Structuring Answers**
   - Answer templates for each phase
   - How to capture assumptions, confidence, boundaries, and unresolved questions
   - How to distinguish artifacts from reasoning

6. **From Interview to Design Requirements**
   - How answers map to the six reasoning objects
   - How answers map to Discovery patterns
   - How answers map to sufficiency gates and escalation conditions
   - How answers map to learning-loop requirements
   - Architecture-landing table (expanded from Appendix A)

7. **Running the Session**
   - Suggested agenda (half-day and full-day formats)
   - Facilitation tips
   - Managing stakeholder disagreement
   - What to do when answers conflict
   - What to do when the team does not know the answer

8. **After the Session**
   - How to package outputs for the architecture team
   - How to package outputs for leadership
   - How to identify the next workflow to assess
   - How to track whether preserved reasoning improved the next cycle

9. **Appendix: Blank Templates**
   - Phase 1–4 answer sheets
   - Architecture-landing summary
   - Reasoning-object capture template
   - Discovery pattern template
   - Sufficiency-condition template
   - Learning-event template

### Key Templates / Worksheets

- Decision Topography Interview answer sheet (per phase)
- Reasoning-object capture form (per object type)
- Sufficiency-condition specification
- Discovery pattern specification
- Architecture-landing summary (from interview to system components)
- Maturity self-assessment (Table 8 from the paper)

### Inputs

- Appendix A (23 questions + 8-question minimal variant)
- Table 7 (six reasoning objects)
- Table 8 (maturity model)
- Appendix A architecture-landing table

### Outputs

- Structured interview answers
- Workflow scope definition
- Reasoning-preservation requirements
- Sufficiency-gate specifications
- Discovery-pattern requirements
- Learning-loop requirements
- Architecture-landing summary for HLD team

### Relationship to Appendix A

Appendix A is the bridge. The Workbook is the full road. Appendix A introduces the 23 questions and shows how answers begin to land in architecture. The Workbook provides facilitation scripts, templates, worked examples, and session-management guidance that Appendix A does not carry.

### Drafting Risks

- Becoming too long — the workbook should be usable, not encyclopedic
- Becoming too theoretical — it should use plain-language throughout
- Duplicating the paper — it should reference the paper, not re-teach it
- Assuming facilitator expertise — it should be usable by someone who has read Appendix A but not the full paper

---

## 3. HLD / Reference Architecture Outline

### Proposed Title

*The Perceived Topography HLD / Reference Architecture: A System Design Guide for Reasoning-State Preservation in Human-Agent Systems*

### Audience

- Enterprise architects designing AI-augmented platforms
- Platform teams building reasoning-state systems
- Product engineers implementing Discovery, learning loops, and governance
- AI system designers integrating with agentic frameworks
- Governance and compliance teams designing oversight mechanisms
- Technical program leads planning implementation roadmaps

### Purpose

Translate the paper's conceptual architecture into implementable system design. A platform team should be able to read the HLD and begin designing data objects, services, workflows, retrieval systems, governance gates, and integration patterns.

### Table of Contents

1. **Introduction**
   - Relationship to the paper
   - Relationship to the Practitioner Workbook
   - Scope: what this HLD covers and does not cover
   - Design principles

2. **Core Architecture Principles**
   - Reasoning-state preservation, not just artifact storage
   - Behavioral availability, not just retrieval
   - Reasoning-relevant retrieval, not just semantic similarity
   - Human confirmation before reuse
   - Start small; earn maturity
   - Governance as design requirement, not afterthought

3. **Six-Object Reasoning-State Data Model**
   - Optimizer State: schema, fields, relationships
   - Premise Stack: schema, fields, relationships
   - Decision State: schema, fields, relationships
   - Investigation Trace: schema, fields, relationships
   - Learning Event: schema, fields, relationships
   - Model Update Object: schema, fields, relationships
   - Cross-object relationships and chain integrity
   - Versioning and immutability model

4. **Discovery / RIPC Service Pattern**
   - Service architecture for Retrieve → Infer → Propose → Confirm
   - Retrieval service: information-surface registry, reasoning-object retrieval
   - Inference service: candidate reasoning-state construction
   - Proposal service: human-readable reasoning-state presentation
   - Confirmation service: human review, correction, bounding, rejection
   - Re-entry logic: when confirmation reveals new uncertainty
   - Discovery Pattern Updates: how the system learns to ask better

5. **Reasoning-Relevant Retrieval Architecture**
   - Why semantic retrieval is not sufficient
   - Metadata requirements for reasoning objects
   - Indexing strategy: structured metadata + semantic search
   - Query patterns: goal-based, policy-scoped, applicability-filtered
   - Ranking and filtering by confidence, status, provenance, and applicability
   - Human confirmation of applicability before reuse
   - Integration with existing vector databases and RAG systems

6. **State Lifecycle Model**
   - States: Draft → Provisional → Validated → Deprecated → Superseded
   - Transition triggers and permissions
   - Review workflows
   - Audit trail requirements
   - Conflict resolution (when reasoning objects disagree)
   - Staleness detection and expiration

7. **Learning-Loop Architecture**
   - Outcome capture service
   - Prediction-error detection
   - Investigation support
   - Evidence-supported explanation workflow
   - Model Update Object creation
   - MUO retrieval and reuse
   - Effectiveness tracking (did the update improve the next cycle?)

8. **Governance and Observability**
   - Role-based access control for reasoning objects
   - Review and approval workflows
   - Authority scope and provenance tracking
   - Audit logging
   - Governance dashboards
   - Exception handling

9. **Integration Patterns**
   - Integration with existing agentic frameworks (LangChain, CrewAI, AutoGen)
   - Integration with existing RAG systems
   - Integration with existing knowledge-management systems
   - Integration with existing compliance and governance tools
   - API design principles

10. **Volume Management and Retention**
    - Retention policies for reasoning objects
    - Archival and cleanup
    - Cross-workflow reasoning-object governance
    - Multi-team access patterns

11. **Minimal Viable Implementation**
    - First workflow selection criteria
    - Minimal reasoning-object schema
    - Minimal retrieval implementation
    - Minimal governance workflow
    - Success criteria for the first cycle
    - Maturity model mapping (Table 8 from the paper)

12. **Open Architecture Questions**
    - Questions that require implementation experience to resolve

### Core Architecture Components

| Component | Purpose |
| --- | --- |
| Reasoning-State Store | Persist the six reasoning objects with metadata |
| Information-Surface Registry | Index and manage available information surfaces |
| Discovery Service | Implement RIPC (Retrieve → Infer → Propose → Confirm) |
| Reasoning-Relevant Retrieval | Find prior reasoning by goal, policy, applicability, confidence, status |
| Learning-Loop Service | Capture outcomes, detect prediction errors, create MUOs |
| Governance Service | Manage status, permissions, review, audit |
| Sufficiency Gate | Evaluate whether current reasoning state warrants action |
| Escalation Service | Route decisions that need human authority |

### Required Data Objects

The six reasoning objects from Table 7, plus:

- Information Surface records
- Discovery Pattern records
- Governance audit records
- Outcome records
- Retrieval-relevance metadata

### Reasoning-Relevant Retrieval Section Plan

This is the first-class section identified in the HLD planning notes. It must specify:

1. How reasoning objects are captured with structured metadata
2. How the system indexes by goal, policy scope, assumptions, confidence, applicability, provenance, status
3. How queries combine semantic search with structured metadata filters
4. How ranking reflects reasoning relevance, not just textual similarity
5. How human confirmation gates prevent blind reuse
6. How the system tracks whether reused reasoning improved outcomes

### Inputs from Workbook

- Interview answers structured by phase
- Architecture-landing summary
- Sufficiency-gate specifications
- Discovery-pattern requirements
- Learning-loop requirements

### Outputs

- Implementable system design
- Data model specifications
- Service architecture
- Integration patterns
- Governance workflow design
- Minimal viable implementation plan

### Drafting Risks

- Becoming a product spec for a specific platform — should remain reference architecture
- Over-specifying before implementation experience — should leave room for learning
- Under-specifying reasoning-relevant retrieval — the hardest technical problem
- Ignoring existing tooling — should show integration, not replacement
- State explosion without retention policy — must address volume from the start

---

## 4. Executive Summary / Decision Brief Outline

### Proposed Title

*Perceived Topography: Why Your AI Systems Keep Starting Confident and Staying Wrong — and What to Build Instead*

### Audience

- Executives and transformation sponsors
- AI program leaders
- Business stakeholders
- Funding and prioritization decision-makers
- Leadership teams evaluating AI strategy

### Purpose

Give a leader enough to understand the framework, see the practical stakes, and know what to fund — in 1–2 pages. The leader should not need to read the full paper.

### One-Page Version Structure

1. **The problem** (3 sentences): AI systems retrieve context but lose reasoning. They produce confident-but-wrong work because the landscape makes the easy path feel sufficient too soon.
2. **The reframe** (2 sentences): The issue is not the AI's capability. It is the information landscape the AI moves through — and that landscape can be designed.
3. **The framework in one sentence**: The Perceived Topography Framework shapes what the system can see, trust, investigate, stop on, preserve, and learn from.
4. **What changes operationally** (bullet list):
   - Systems preserve why, not just what
   - Discovery replaces blank-form intake
   - Sufficiency becomes a designed stopping condition
   - Learning changes future reasoning, not just future storage
5. **The healthcare example** (2 sentences): A campaign brief generated an unsupported clinical claim because the evidence boundary was not behaviorally connected. The same system, with reasoning-state architecture, would have paused at the claim and asked for approved evidence.
6. **What to fund** (bullet list):
   - A Decision Topography Interview on one repeated workflow
   - A reasoning-state preservation pilot
   - Architecture planning for reasoning-relevant retrieval
7. **Where to start**: Appendix A of the paper. One hour. One repeated workflow. 8 questions.

### Two-Page Version Structure

Page 1: The one-page version above.

Page 2:
- **Why this is not just better prompting** (3 sentences)
- **Why this is not just better RAG** (3 sentences)
- **The three companion artifacts** (Workbook, HLD, Paper) — what each does
- **The maturity model** (compressed from Table 8 — 5 stages, one sentence each)
- **The disconfirmation standard** (compressed from Table 9 — what would make this framework wrong)
- **Call to action**: Run the interview. Design the landscape. Build better landscapes.

### Key Message Hierarchy

1. Your AI systems keep making the same kind of confident-but-wrong mistake.
2. The problem is not the model. It is the landscape the model moves through.
3. That landscape can be designed.
4. The framework gives you a vocabulary for diagnosing failures and a practical architecture for fixing them.
5. Start with one repeated workflow. Ask 8 questions. See where the reasoning disappears.
6. The answers become system design.

### Inputs from Paper

- Abstract
- Section 1 (fear-to-landscape reframe)
- Section 2 (context ≠ reasoning state)
- Section 5 (healthcare campaign — compressed)
- Section 11 (Build better landscapes — closing energy)
- Appendix A (minimal interview variant)

### Outputs

- A shareable 1–2 page brief
- A clear call to action
- A pointer to the Workbook and HLD for follow-up

### Drafting Risks

- Sounding like a pitch deck — should be serious and evidence-grounded
- Oversimplifying the framework — should preserve the "reasoning state, not just context" distinction
- Underspelling the practical value — should make the Monday-morning path visible
- Using too much framework jargon — should use Cassidy-accessible language

---

## 5. Dependencies Between Artifacts

| Artifact | Depends on... | Can start before... |
| --- | --- | --- |
| Executive Summary | Paper (complete) | Workbook and HLD |
| Practitioner Workbook | Paper + Appendix A (complete) | HLD |
| HLD / Reference Architecture | Paper + Workbook outputs + HLD planning notes | Nothing — final artifact |

### What must be decided before drafting each

| Artifact | Decisions needed |
| --- | --- |
| Executive Summary | Target audience (Cassidy's leadership? Advisors? Investors?), format (PDF? Slide? Markdown?), distribution plan |
| Practitioner Workbook | Session format (half-day vs. full-day?), template format (PDF? Digital?), whether to include a non-healthcare worked example |
| HLD / Reference Architecture | Target platform assumptions (cloud? On-prem? Framework-agnostic?), whether to specify a reference implementation or remain abstract, first-workflow selection criteria |

### What can be drafted in parallel

- Executive Summary and Workbook can be drafted in parallel (no dependency between them)
- HLD should begin outline-level work in parallel but full drafting should wait for at least one workbook session to produce real outputs

---

## 6. Recommended Next Action

**Draft the Executive Summary / Decision Brief first.**

Rationale:

1. It is the fastest to produce (~1–2 pages).
2. It is needed immediately for external sharing — Cassidy will not send the full 31,000-word paper to his leadership team.
3. It requires only the completed paper as input (no workbook or HLD outputs needed).
4. It validates the "so what?" message before investing in the longer companion artifacts.
5. It can be drafted and reviewed in a single session.

After the Executive Summary, draft the Practitioner Workbook (which expands the already-existing Appendix A). Then draft the HLD (which requires the most technical depth and benefits from having workbook outputs as input).

---

## No-Edit Confirmation

- Manuscript edited: No
- Figures modified: No
- Figure 8 modified: No
- References modified: No
- Full companion artifacts drafted: No (outlines only)
