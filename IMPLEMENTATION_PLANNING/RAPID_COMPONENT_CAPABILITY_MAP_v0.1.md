# Rapid Component Capability Map v0.1

**Date:** 2026-06-22
**Status:** v0.1 Planning Draft. Companion to First Implementation Slice Plan v0.1.
**Purpose:** Map Rapid-style implementation components to MVP / MVP-adjacent / future phases before locking the first build slice.

---

## 1. Purpose

This artifact maps candidate Rapid-style components against the PTF implementation slice. It exists because the RapidSOS Marketing Context Layer demonstrated concrete agent patterns (Research Agent, Brand Voice Agent, ICP Agent, Composition Agent, Quality Agent, governance scoring, KB ingestion, gap detection) that are relevant to the first PTF build — but not all of them belong in the first cycle.

This map classifies each candidate component so that the first build slice stays narrow while the team knows where each component fits in the maturity progression.

---

## 2. Relationship to Slice Plan v0.1

### Slice Plan v0.1 remains valid

The existing slice plan correctly defines: workflow boundary, reasoning objects, RIPC flow, retrieval, governance, learning loop, exclusions, and success criteria. It does not need to be replaced.

### What the slice plan already covers well

- Reasoning-object capture (Optimizer State, Premise Stack, Decision State, Outcome Record)
- RIPC as a four-step service pattern
- Three-state governance model
- Manual learning loop
- MVP/future separation
- Explicit exclusions
- Success criteria

### What the slice plan under-specifies

- **Component decomposition:** The plan describes what the system must do but does not decompose it into named components or agents. This map fills that gap.
- **KB refresh and information surface maintenance:** The plan assumes information surfaces are registered and available but does not specify how they are ingested, updated, or governed.
- **The relationship between KB updates and reasoning-state changes:** The plan correctly separates information surfaces from reasoning objects but does not trace the boundary through specific agent behaviors.
- **Agent topology:** The plan does not specify whether the RIPC loop is one agent, multiple agents, or a service orchestration. This map proposes a topology.

---

## 3. Component Inventory

### Critical Distinction: KB Update vs. MUO

Before mapping components, one distinction must be clear in every row:

**A KB update changes the information surface.** It adds, revises, or removes content from the knowledge base. It changes what the system can see and retrieve.

**A Model Update Object changes future reasoning.** It records an evidence-supported lesson with applicability boundaries, confidence, and governance lifecycle. It changes how the system interprets, trusts, and acts on what it retrieves.

These are not the same operation. The architecture must not allow information refresh, agent output, or campaign results to silently become reusable reasoning without human review, applicability boundaries, evidence basis, confidence, lifecycle status, and governance.

---

| # | Component | Purpose | PTF Concept | Input | Output | Human Confirmation Required | Phase | Risk if Automated Too Early | Modifies |
|---|---|---|---|---|---|---|---|---|---|
| 1 | **Information Surface Registry** | Register and manage what information sources exist, their type, authority, recency, and accessibility | Information surfaces, perceived topography | Document inventory, source metadata | Registered surfaces with authority level (binding/advisory/background/anecdotal) | Initial registration: yes. Authority classification: yes. | **MVP** | Low — registry is metadata, not reasoning | KB metadata only |
| 2 | **KB Ingestion / Refresh Agent** | Monitor topics, detect stale content, propose KB updates from new sources | Information surfaces, topography maintenance | External sources, staleness triggers, topic monitoring rules | Proposed KB additions or revisions — flagged for human review | **Yes — always.** KB changes affect what the system can see. Unreviewed additions change the retrieval landscape. | **Future** (autonomous monitoring). **MVP-adjacent** (manual-triggered ingestion). | High — autonomous ingestion changes retrieval results without governance. Stale or biased sources silently shape future campaigns. | KB only |
| 3 | **Human-Requested Search-to-KB Update Flow** | Human requests research on a topic → system searches → human reviews → approved content enters KB | Information surfaces, retrieval | Human research request, external/internal sources | Reviewed and approved KB content with metadata | **Yes.** Human requests the search, reviews results, approves what enters the KB. | **MVP-adjacent** | Medium — the human is in the loop, but the system's search framing can anchor what gets found | KB only |
| 4 | **Campaign Brief Orchestrator / RIPC Agent** | Execute the Retrieve → Infer → Propose → Confirm loop for campaign brief creation | RIPC / Discovery, optimizer state, premise stack | Workflow trigger, request text, information surfaces, prior reasoning objects | Draft Optimizer State, Draft Premise Stack, confirmed reasoning state after human review | **Yes — this is the primary human interaction point.** The orchestrator proposes; the human confirms, corrects, rejects, qualifies, or bounds. | **MVP** | Low if designed as propose-confirm. High if designed as auto-complete. The difference is whether the system presents a draft reasoning state or a finished brief. | Reasoning objects (Draft → Provisional) |
| 5 | **Campaign Brief Generator** | Generate the decision artifact (the brief itself) from confirmed reasoning state | Decision artifact, sufficiency | Confirmed Optimizer State, Premise Stack, retrieved information surfaces, governance constraints | Draft campaign brief with source citations | **Yes.** The brief is reviewed before execution. Sufficiency rationale captured in Decision State. | **MVP** | Medium — a fluent brief can mask weak reasoning. The governance check (Component 6) must operate before the brief is treated as sufficient. | Decision artifact only |
| 6 | **Governance / Policy / Sufficiency Agent** | Check the draft brief and reasoning state against governance rules, policy boundaries, claim restrictions, and sufficiency criteria | Governance, sufficiency, premature sufficiency prevention | Draft brief, confirmed reasoning state, policy repository, approved claims | Governance assessment: policy compliance, claim validation, sufficiency check, flagged issues | **Advisory output — human decides.** The agent flags issues; it does not block or approve autonomously in MVP. | **MVP** | Medium — if it blocks autonomously, it creates friction. If it approves silently, it creates false compliance confidence. Coaching model (flag + suggest) is the right MVP posture. | Nothing directly. Advisory only. Flags may trigger Decision State updates. |
| 7 | **Outcome Capture Assistant** | Help the campaign owner record outcomes after execution, displaying the Decision State's predictions for comparison | Learning loop, outcome capture | Campaign performance data, Decision State predictions | Structured Outcome Record linked to Decision State | **Yes.** Human records and validates the outcome. | **MVP** | Low — the assistant structures the capture; the human provides the data. | Outcome Record only |
| 8 | **Results-to-Learning Agent** | Analyze campaign outcomes against predictions, identify potential prediction errors, propose draft Learning Events | Learning loop, prediction-error detection | Outcome Record, Decision State, Premise Stack | Draft Learning Event proposals (prediction error identified, candidate premises flagged) | **Yes — always.** Agent proposes; human confirms whether the prediction error is real and which premise failed. | **MVP-adjacent** | High — automated prediction-error attribution can be wrong. If the agent identifies the wrong premise as the failure point, the resulting MUO misdirects future reasoning. Human investigation is essential. | Reasoning objects (Draft Learning Events only — never auto-promoted) |
| 9 | **Learning Event / MUO Assistant** | Help the human formalize a Learning Event into a Model Update Object with applicability boundaries, evidence, and confidence | Learning loop, model update objects | Validated Learning Event, human investigation results | Draft MUO with required fields (update target, content, evidence, applicability, non-applicability, confidence) | **Yes — always.** MUOs require human creation and review. The assistant structures; the human authors. | **MVP-adjacent** | High — automated MUO creation risks noise and policy laundering. Every MUO must be human-authored and human-reviewed before it can shape future reasoning. | Reasoning objects (Draft MUOs only — never auto-promoted) |
| 10 | **Beacon / MCP Interface** | Expose reasoning-state services as MCP tools compatible with Beacon's skill discovery | Integration, compatibility | Reasoning-state API | MCP-compatible tool endpoints (search_reasoning_objects, get_optimizer_state, etc.) | Registration: yes. Runtime: depends on calling context. | **Future** | Low risk but premature — the reasoning-state layer must be independently validated before external systems consume it. | Nothing (interface layer) |
| 11 | **Co-Worker Information Surface Connector** | Register co-worker-accessible enterprise data systems as information surfaces in the PTF registry | Information surfaces, integration | Co-worker API / MCP endpoints | Information Surface Records with authority level (typically background or anecdotal) | Registration: yes (authority classification requires human judgment). | **Future** | Medium — co-worker data may be treated as confirmed reasoning rather than information surfaces. The boundary must be explicit: co-worker data is input to reasoning, not reasoning itself. | KB metadata only |
| 12 | **Model Router Integration** | Route retrieval queries to cost-appropriate models via Martin's model router | Integration, cost optimization | Retrieval queries | Routed queries with model selection | No — infrastructure concern, not reasoning governance. | **Future** | Low — routing does not affect reasoning quality if minimum quality thresholds are defined. | Nothing (infrastructure) |

---

## 4. Recommended MVP Component Set

The smallest component set that proves the core claim: preserving reasoning state across repeated decision cycles changes future behavior.

| # | Component | Role in MVP |
|---|---|---|
| 1 | **Information Surface Registry** | Register the initial set of information surfaces (brand voice, ICPs, messaging, playbooks, approved claims). Manual registration. |
| 4 | **Campaign Brief Orchestrator / RIPC Agent** | The core. Executes Retrieve → Infer → Propose → Confirm. Creates Draft reasoning objects; human confirms. |
| 5 | **Campaign Brief Generator** | Produces the decision artifact from confirmed reasoning state. Human reviews before execution. |
| 6 | **Governance / Policy / Sufficiency Agent** | Advisory mode. Flags policy violations, unsupported claims, and sufficiency concerns. Coaching posture — flag and suggest, not block. |
| 7 | **Outcome Capture Assistant** | Structures outcome recording after campaign execution. Displays predictions for comparison. |

**Total MVP agents/services: 5**

This set covers the full first-cycle arc: register surfaces → RIPC Discovery → generate brief → governance check → capture outcome. It does not include KB refresh or learning automation — those are manual in the first cycle.

---

## 5. MVP-Adjacent Components

These components may be lightly represented in the first build but should not be fully automated. They operate as human-assisted workflows, not autonomous agents.

| # | Component | MVP-Adjacent Implementation | Why Not Full MVP |
|---|---|---|---|
| 3 | **Human-Requested Search-to-KB Update** | Human requests a topic search. System searches external/internal sources. Human reviews results and manually adds approved content to the KB. No autonomous ingestion. | KB changes affect retrieval. Changes must be human-reviewed and intentional. |
| 8 | **Results-to-Learning Agent** | After outcome capture, the system highlights where the outcome diverges from predictions and flags which premises may have failed. Human investigates and confirms. | Automated prediction-error attribution can be wrong. The human must identify the actual failure point, not accept the system's first guess. |
| 9 | **Learning Event / MUO Assistant** | If the human confirms a prediction error and identifies an evidence-supported explanation, the system helps structure the Learning Event and draft a MUO with required fields. Human authors the content; system provides the template. | MUOs require human creation, applicability boundaries, evidence basis, and review. Automated MUO creation is the primary policy-laundering risk. |

**MVP-adjacent means:** the system provides structure and prompts; the human does the reasoning work. The system never creates, promotes, or applies these objects without human action.

---

## 6. Future-Phase Components

These should not be built in the first cycle. They require validated reasoning-state data, established governance patterns, or external system integration that is premature.

| # | Component | Why Future | When to Revisit |
|---|---|---|---|
| 2 | **KB Ingestion / Refresh Agent** (autonomous) | Autonomous topic monitoring changes the retrieval landscape without governance. Must understand what information surfaces matter before automating refresh. | After 3+ cycles with stable KB and established governance patterns. |
| 10 | **Beacon / MCP Interface** | The reasoning-state layer must be independently validated before external systems consume it. MCP integration requires answers to open questions (HLD Appendix C). | After the data model and RIPC flow are validated with real usage. |
| 11 | **Co-Worker Information Surface Connector** | Co-worker data must enter as information surfaces, not reasoning objects. The boundary must be proven with manual classification first. | After the authority taxonomy is validated and the team understands which co-worker data sources are binding vs. anecdotal. |
| 12 | **Model Router Integration** | Infrastructure optimization. No reasoning impact. Premature until retrieval volume justifies cost optimization. | After retrieval volume exceeds manual cost management. |
| — | **Autonomous MUO creation** | Policy laundering risk. MUOs must be human-created until enough human-authored MUOs establish quality patterns. | After 10+ human-created MUOs exist and governance patterns are mature. |
| — | **Dynamic Discovery Patterns** | Requires 5+ cycles of static pattern data to learn from. | After enough RIPC cycles to measure which questions produce valuable confirmations. |
| — | **Governance dashboards** | Requires reasoning-object volume and governance event data. | After 3+ cycles produce enough data to visualize. |
| — | **Confirmation fatigue detection** | Requires baseline confirmation behavior data. | After multiple cycles with human confirmation events logged. |
| — | **Automated sufficiency gates** | Requires validated rules and calibrated thresholds. | After manual sufficiency review produces enough examples to define automated rules. |

---

## 7. Governance Rules by Component

| # | Component | Can Modify KB | Can Modify Reasoning Objects | Can Modify Decision Artifact | Can Modify Lifecycle Status | Can Modify Governance State | Human Confirmation Required |
|---|---|---|---|---|---|---|---|
| 1 | Information Surface Registry | Metadata only | No | No | No | No | Yes (registration and authority classification) |
| 2 | KB Ingestion / Refresh Agent | Yes (proposed) | No | No | No | No | Yes — always. Proposed additions reviewed before entry. |
| 3 | Search-to-KB Update Flow | Yes (after review) | No | No | No | No | Yes — human reviews and approves. |
| 4 | RIPC Orchestrator | No | Yes (creates Drafts) | No | Yes (Draft → Provisional via human confirm) | No | Yes — primary human interaction point. |
| 5 | Brief Generator | No | No | Yes (creates draft brief) | No | No | Yes — brief reviewed before execution. |
| 6 | Governance / Sufficiency Agent | No | No | No | No | No | Advisory only — flags issues, does not decide. |
| 7 | Outcome Capture Assistant | No | No | No | No | No | Yes — human records the outcome. |
| 8 | Results-to-Learning Agent | No | Yes (proposes Draft Learning Events) | No | No | No | Yes — human confirms prediction error and explanation. |
| 9 | MUO Assistant | No | Yes (helps structure Draft MUOs) | No | No | No | Yes — human authors MUO content and fields. |
| 10 | Beacon / MCP Interface | No | No | No | No | No | Registration only. |
| 11 | Co-Worker Connector | Metadata only | No | No | No | No | Yes (authority classification). |
| 12 | Model Router | No | No | No | No | No | No (infrastructure). |

**Key rule:** No component may promote a reasoning object from Draft to Provisional or Validated without human action. No component may create a Validated MUO. No component may silently change what the system retrieves, trusts, or treats as sufficient.

---

## 8. Proposed Agent / Service Topology

```text
                    ┌─────────────────────────┐
                    │  Information Surface     │
                    │  Registry                │
                    │  (MVP: manual register)  │
                    └────────────┬────────────┘
                                 │
            ┌────────────────────┼────────────────────┐
            │                    │                     │
     ┌──────▼──────┐    ┌───────▼───────┐    ┌───────▼───────┐
     │ Brand Voice  │    │ ICPs /        │    │ Playbooks /   │
     │ Guidelines   │    │ Messaging     │    │ Approved      │
     │ (binding)    │    │ (advisory)    │    │ Claims        │
     └──────┬──────┘    └───────┬───────┘    └───────┬───────┘
            │                    │                     │
            └────────────────────┼─────────────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │  Campaign Brief         │
                    │  Orchestrator / RIPC    │
                    │  (MVP core)             │
                    │                         │
                    │  Retrieve → Infer →     │
                    │  Propose → Confirm      │
                    └────────────┬────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │  Governance / Policy /  │
                    │  Sufficiency Agent      │
                    │  (advisory — flag +     │
                    │   suggest, not block)   │
                    └────────────┬────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │  Campaign Brief         │
                    │  Generator              │
                    │  (decision artifact)    │
                    └────────────┬────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │  Decision State         │
                    │  (sufficiency rationale │
                    │   captured — required)  │
                    └────────────┬────────────┘
                                 │
                          [campaign executes]
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │  Outcome Capture        │
                    │  Assistant              │
                    │  (manual — human        │
                    │   records outcome)      │
                    └────────────┬────────────┘
                                 │
                                 ▼
              ┌──────────────────────────────────┐
              │  Results-to-Learning Agent       │
              │  (MVP-adjacent — highlights      │
              │   prediction errors, human       │
              │   investigates and confirms)     │
              └──────────────────┬───────────────┘
                                 │
                                 ▼
              ┌──────────────────────────────────┐
              │  Learning Event / MUO Assistant  │
              │  (MVP-adjacent — structures      │
              │   human-authored learning)       │
              └──────────────────┬───────────────┘
                                 │
                                 ▼
              ┌──────────────────────────────────┐
              │  Future Campaign Reasoning       │
              │  (next cycle retrieves prior     │
              │   reasoning + MUOs during RIPC)  │
              └──────────────────────────────────┘
```

**Topology notes:**

- The flow is sequential, not parallel. Each component feeds the next.
- The RIPC Orchestrator is the core. Everything before it provides input; everything after it captures outcomes and learning.
- Governance operates between RIPC confirmation and brief generation — it checks before sufficiency, not after.
- The learning path (Outcome → Results-to-Learning → MUO) feeds back into the next cycle's RIPC Retrieve step.

---

## 9. Recommended Update to Slice Plan

### Recommendation: Update to v0.2 with targeted additions

The existing `FIRST_IMPLEMENTATION_SLICE_PLAN_v0.1.md` should remain as-is. A v0.2 should incorporate:

| Change | What to add | Where in the slice plan |
|---|---|---|
| Component lanes | Name the five MVP components (Registry, RIPC Orchestrator, Brief Generator, Governance Agent, Outcome Capture) | New subsection in Section 6 (Minimal RIPC Flow) or new Section 6.5 |
| KB update vs. MUO distinction | Explicit statement that KB updates change information surfaces; MUOs change reasoning; they are not the same operation | Section 5 (Minimal Reasoning Objects) — add a note |
| Governance posture | Specify coaching model (flag + suggest, not block) for MVP governance | Section 8 (Minimal Governance) — add a note |
| Results-to-Learning classification | Classify as MVP-adjacent (system highlights; human investigates and confirms) | Section 9 (Minimal Learning Loop) — clarify |
| Autonomous KB monitoring as future | Explicitly exclude autonomous topic-monitoring agents from MVP | Section 10 (Explicit Exclusions) — add row |
| Agent topology reference | Reference this capability map for component decomposition | Section 14 (Recommended Next Action) — add reference |

**Do not rewrite the slice plan.** Add targeted clarifications only.

---

## 10. Open Questions for Benet

### Build focus

1. **What should the first build prove — brief generation, reasoning preservation, or KB refresh?**
   The slice plan prioritizes reasoning preservation. If Benet wants the first demo to show KB lifecycle (ingest → govern → retrieve → compose), the component priority shifts. If reasoning preservation is the goal, the RIPC orchestrator is the core. Both are valid — the question is what success looks like for the first cycle.

2. **Should KB refresh be part of MVP or manual setup?**
   The current plan assumes information surfaces are pre-registered (manual setup). If Benet wants KB ingestion as part of the first build, Component 3 (Human-Requested Search-to-KB Update) moves from MVP-adjacent to MVP. This adds scope but demonstrates a more complete loop.

3. **Should results-to-learning be included in the first cycle or wait until the second campaign cycle?**
   The learning loop requires an outcome. If the first campaign has not yet executed, results-to-learning cannot be tested in the first cycle. It may be better to build the capture infrastructure (Outcome Capture Assistant) in the first cycle and test results-to-learning in the second cycle when outcome data exists.

### Architecture decisions

4. **Should governance be a separate component or embedded in RIPC?**
   The Rapid demo embedded governance in the composition flow (brand voice checking during generation, quality scoring after generation). The PTF HLD positions governance as operating at three points (formation, reuse, transition). A separate governance component is cleaner architecturally but adds a step. An embedded approach is simpler but risks governance becoming post-hoc rather than pre-sufficiency.

5. **Should the first demo show one orchestrated flow or multiple visible agents?**
   The Rapid demo made each agent's work visible through SSE streaming (Research → Brand Voice → ICP → Composition → Quality). The PTF implementation could follow the same pattern (RIPC steps visible as sequential agent work) or present a single unified flow. Visible agent steps are more impressive in demos; a unified flow is simpler to build.

### Scope boundary

6. **Is the campaign brief the right first decision artifact, or should we start with something simpler?**
   A campaign brief involves multiple premises, governance constraints, audience targeting, and claim boundaries. It exercises the full framework. But a simpler artifact (e.g., a single-topic content piece, a research summary, or a customer response) would have fewer moving parts and reach the learning loop faster.

7. **How much of the Rapid Marketing Context Layer should be reused vs. rebuilt?**
   The Rapid prototype has working code: ChromaDB knowledge store, five-agent pipeline, governance scoring, SSE streaming, demo stage system. Some patterns are directly transferable (semantic search, category filtering, brand voice checking). Others need to be reconceived for PTF (the five-agent pipeline becomes RIPC; quality scoring becomes governance/sufficiency; gap detection becomes information surface registry). The question is where to draw the line between reuse and rebuild.

---

## No-Edit Confirmation

- Frozen paper (`PAPER_v1.0_WORKING.md`) edited: **No**
- Figure 8 modified: **No**
- Figures modified: **No**
- References modified: **No**
- Executive Brief v1.0 edited: **No**
- Build Discovery Guide v1.0 edited: **No**
- HLD v1.0 content edited: **No**
- First Implementation Slice Plan v0.1 edited: **No**
