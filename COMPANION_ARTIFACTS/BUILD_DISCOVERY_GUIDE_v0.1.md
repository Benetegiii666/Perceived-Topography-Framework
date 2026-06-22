# Decision Topography Build Discovery Guide

## Questions That Become Build Inputs

---

## What This Guide Is

This guide is a build-discovery instrument. It helps a team translate organizational knowledge, decision patterns, governance rules, and workflow behavior into concrete system specifications.

Every question in this guide has a build target. The answers become campaign brief schemas, KB taxonomies, metadata fields, governance rules, retrieval configurations, sufficiency checks, reasoning-state objects, learning-loop specifications, and HLD inputs.

The guide is organized by build-input category, not by calendar time, session agenda, or facilitation theory. Each category maps to a system component that must be specified before the build can proceed.

---

## What This Guide Is Not

- It is not a workshop facilitation script. It does not tell you who should be in the room or how to manage stakeholder disagreement.
- It is not a calendar plan. It does not prescribe Day 1, Week 1, or 30-60-90 timelines.
- It is not a replacement for the paper. It operationalizes the paper's concepts; it does not re-teach them.
- It is not RapidSOS-specific documentation. RapidSOS examples ground the questions in practice; the guide works for any organization running repeated decision workflows.
- It is not a research instrument. It captures observations that may later support academic study, but its purpose is build discovery.

---

## How This Guide Relates to the Keystone Paper

The paper (*The Perceived Topography Framework: A Reasoning-State Architecture for Human-Agent Systems*) is the keystone. It provides:

- perceived topography as the design surface
- gradients as directional pressures
- sufficiency as the stopping condition
- premature sufficiency as the shared failure pattern
- reasoning state as the unit of preservation
- the six-object reasoning architecture
- Discovery / RIPC as the capture loop
- learning as evidence-supported model change
- Appendix A as the conceptual interview shape

This guide takes those concepts and turns them into build questions. The paper says "preserve reasoning state." This guide asks: "What fields does the campaign brief schema need? What metadata must each KB chunk carry? What governance rule prevents an unsupported claim from becoming sufficient?"

---

## How This Guide Relates to Appendix A

Appendix A is the conceptual seed. It asks the right questions at the right level of abstraction:

- Phase 1: Map the Decision Topography
- Phase 2: Shape the Motion
- Phase 3: Preserve the Reasoning
- Phase 4: Make the Next Cycle Smarter

This guide is Appendix A made operational.

Appendix A asks: "What kind of work keeps coming back?" This guide asks: "What are the required fields in the campaign brief schema, and which ones must be present before the system drafts?"

Appendix A asks: "What rules can change the answer?" This guide asks: "What claim types require approved evidence? What restricted terms must be flagged? What approval gates exist before publish?"

Appendix A asks: "Did the next run actually get smarter?" This guide asks: "What outcome data feeds back through governance? What fields does a Learning Event require? How does a Model Update Object get scoped, reviewed, and applied?"

---

## How This Guide Relates to the Executive Brief

The Executive Brief tells leaders why this matters and what to fund. It ends with eight questions and a recommendation: "Start with one repeated decision workflow."

This guide picks up where the Executive Brief leaves off. The leader chose the workflow. Now the team needs to discover what to build.

---

## How This Guide Feeds the HLD / Reference Architecture

Every answer in this guide produces a build specification. Those specifications become inputs to the HLD / Reference Architecture:

| Guide output | HLD input |
| --- | --- |
| Campaign brief schema | Decision-artifact data model |
| KB taxonomy and source inventory | Information-surface registry, retrieval configuration |
| Governance rules | Policy-retrieval linkages, approval gates, brand/compliance scoring |
| Sufficiency criteria | Sufficiency-gate specifications, escalation rules |
| Reasoning-preservation scope | Six-object schema: which objects are captured for this workflow |
| Learning-loop requirements | Outcome capture, prediction-error detection, MUO creation |
| Retrieval-relevance rules | Reasoning-relevant retrieval architecture, metadata indexing |
| Human-confirmation points | RIPC service pattern, review workflows |
| Ownership model | Lifecycle management, staleness detection, review cadence |

The guide discovers the requirements. The HLD designs the system that implements them.

---

## Design Rule: Every Question Must Have a Build Target

Questions should not be included merely because they are interesting.

Each question in this guide should produce one or more of:

- campaign brief structure
- KB structure
- metadata field
- reasoning object specification
- governance rule
- retrieval rule
- confidence / provenance requirement
- lifecycle requirement
- HLD input
- future case-study observation

If a question does not produce a build target, it does not belong in this guide.

---

## Category Map

| Guide category | General PTF purpose | RapidSOS grounding example | What system thing this informs |
| --- | --- | --- | --- |
| Workflow boundary | Scope the first implementation slice | Healthcare campaign brief workflow | Workflow definition, first build scope |
| Campaign brief structure | Define the decision artifact | What must a campaign brief contain before AI drafts? | Campaign brief schema, required fields, missing-info checks, draft-generation inputs |
| KB / information surfaces | Define what the system can see and trust | Brand voice, ICPs, messaging, playbooks, competitive intel | KB taxonomy, source types, chunking strategy, metadata model, retrieval filters |
| Trust, evidence, and confidence | Map what the team trusts, doubts, or argues about | Which sources carry weight? Which ones get worked around? | Confidence-display rules, retrieval weighting, evidence-requirement flags |
| Assumptions / premises | Surface working beliefs that shape the decision | "Workflow burden is a buying signal" | Premise Stack schema, assumption capture, confidence markers |
| Policy / governance boundaries | Shape gradients away from unsafe claims | Approved claims, restricted language, evidence requirements | Policy rules, claim validation, approval gates, brand/compliance scoring |
| Sufficiency and stopping conditions | Define when the system can act or must pause | When is a draft "good enough" vs. needing review? | Stop/ask/escalate logic, confidence thresholds, quality gates |
| Reasoning to preserve | Keep "why" from disappearing | What assumption shaped this campaign? What evidence was missing? | Optimizer State, Premise Stack, Decision State, Investigation Trace |
| Learning loop | Make the next run smarter | What campaign result should change future briefs? | Learning Event, Model Update Object, analytics feedback loop |
| Retrieval relevance | Retrieve prior reasoning, not just similar text | Which prior campaign lesson applies here, and why? | Reasoning-relevant retrieval, applicability rules, confidence/provenance display |
| Human confirmation | Keep humans in the correction loop | Who confirms whether a prior lesson applies? | RIPC flow, review UI, confirmation records, override logic |
| Ownership / lifecycle | Keep knowledge current and governed | Who owns brand voice, ICPs, playbooks, claims, competitive intel? | Ownership model, review cadence, staleness detection, notification workflow |
| Build translation | Turn all answers into HLD / architecture inputs | How do the answers above become data objects, services, and workflows? | HLD input packet, architecture-landing summary |

---

## Category 1: Workflow Boundary

*Intent: Scope the first implementation slice. Choose one repeated decision workflow where AI output matters, mistakes recur, and one cycle should make the next cycle smarter. This category produces the workflow definition that bounds everything else in the guide.*

### Category purpose

Identify the single repeated workflow that the build will target first.

### Build output produced

Workflow scope definition, recurrence pattern, decision type, outcome observability, team involvement.

### Core questions — placeholder

*(To be fully drafted in a future version.)*

### What this informs in the system

First implementation slice. Every other category is scoped to this workflow.

### What this feeds in the HLD

Workflow-scope record, first-implementation criteria (Section 13 of the HLD blueprint).

---

## Category 2: Campaign Brief Structure

### Category purpose

Discover the structure of the campaign brief — or whatever the repeated decision artifact is. The campaign brief is the decision artifact: the document, form, or structured output that commits the team to a direction. Understanding its structure tells you what the system must produce, what it must check before producing, and what reasoning must survive the production.

### Build output produced

- Campaign brief schema (required fields, optional fields, conditional fields)
- Missing-information checks (what must be present before drafting)
- Evidence-backed fields (which fields require supporting evidence)
- Review-gated fields (which fields require human review before use)
- Sufficiency criteria for a usable brief
- Draft-generation inputs (what the AI needs before it can begin)
- Downstream dependency map (what breaks later when the brief is weak)

### Core questions

**Q2.1 — What decision or action does this brief enable?**

Ask this because the brief is not the end product. It enables downstream work: creative execution, channel production, sales enablement, compliance review, budget allocation. The system needs to know what the brief is for, not just what it contains.

Listen for: "The brief is what the team works from for the next 6 weeks." "Nothing moves until the brief is approved." "The brief is mostly for the AI to draft from."

This becomes: The goal field in the optimizer-state record. The purpose statement in the brief schema.

**Q2.2 — What sections must exist before work can begin?**

Ask this because a brief with missing sections will produce downstream work that has to be redone. If the system can draft without an audience definition, it will — and the draft will be wrong in ways that are expensive to fix later.

Listen for: section names, required fields, "we always need X before we can start," "last time we skipped Y and it cost us two weeks."

This becomes: Required-fields list in the brief schema. Missing-information check logic.

**Q2.3 — Which sections are factual, which are strategic, and which are evidence-dependent?**

Ask this because different sections have different sufficiency conditions. A factual section (product capabilities) needs accuracy. A strategic section (audience interpretation) needs judgment. An evidence-dependent section (clinical claims) needs approved support. The system should treat them differently.

Listen for: "Product features are straightforward." "Audience targeting is where the judgment lives." "Anything about outcomes needs compliance."

This becomes: Field-type classification in the brief schema (factual / strategic / evidence-dependent). Different governance rules per field type.

**Q2.4 — Which sections require policy, legal, clinical, compliance, or brand review?**

Ask this because review-gated fields must not become sufficient before review. If a clinical-outcome claim can enter the brief without triggering a review gate, the system has a premature-sufficiency vulnerability.

Listen for: "Claims need legal." "Anything mentioning patient outcomes goes through compliance." "Brand reviews the headline and CTA." "Nobody reviews the audience section."

This becomes: Review-gate specifications per field. Approval-workflow requirements in the HLD.

**Q2.5 — Which parts are usually copied forward without being rethought?**

Ask this because copied-forward content is where stale reasoning hides. If the audience section from the last campaign is pasted into the next campaign without re-examination, the system inherits assumptions that may no longer hold.

Listen for: "We usually start from the last brief." "The audience section hasn't changed in a year." "We copy the positioning and update the product name."

This becomes: Staleness flags on copied-forward content. Re-examination prompts in the Discovery flow. Premise Stack candidates (what was assumed without being re-tested).

**Q2.6 — Which parts are most often vague but still treated as good enough?**

Ask this because this is where premature sufficiency lives in the current workflow. The team knows the section is weak but proceeds anyway because the draft sounds professional or because nobody owns that section.

Listen for: "The 'why now' section is always thin." "We never really define what 'qualified' means." "The evidence section just says 'see approved claims.'"

This becomes: Sufficiency-condition specification for the brief. Fields that the system should flag as insufficient before drafting proceeds.

**Q2.7 — What must the AI know before it begins drafting?**

Ask this because this is the input specification for the composition agent. If the AI needs the goal, audience, policy constraints, approved claims, and prior campaign lessons before it drafts, those are the retrieval and Discovery requirements.

Listen for: "It needs the ICP." "It needs to know what we can and can't say." "It should know what worked last time." "It needs the product messaging."

This becomes: Draft-generation input specification. Retrieval requirements. Discovery / RIPC configuration for this workflow.

**Q2.8 — What should make the system pause before drafting?**

Ask this because some conditions should prevent the system from producing output at all. Missing compliance review. Missing audience definition. Missing evidence for a claim type. The system should recognize these as blocking conditions, not optional context.

Listen for: "If there's no approved claims list, it shouldn't draft clinical language." "If we don't have the ICP, it's guessing." "It should never draft without knowing the goal."

This becomes: Pre-draft blocking conditions. Escalation triggers. Abstention logic.

**Q2.9 — What would make a brief unsafe, misleading, low-quality, or unusable?**

Ask this because this question surfaces the failure modes the team already knows about. An unsafe brief makes an unsupported claim. A misleading brief implies something the product cannot deliver. A low-quality brief sounds generic. An unusable brief is missing sections that downstream teams need.

Listen for: "An unsupported clinical claim." "Generic messaging that could be any product." "No differentiation from Carbyne." "Missing the call-to-action." "Wrong audience assumptions."

This becomes: Quality-scoring dimensions. Brand compliance rules. Grounding checks. Competitive-differentiation requirements.

**Q2.10 — What does a strong campaign brief make easier for downstream work?**

Ask this because the brief's value is measured by what it enables. A strong brief makes creative execution faster, sales enablement clearer, compliance review smoother, and cross-channel consistency automatic.

Listen for: "When the brief is tight, the emails write themselves." "A good brief means compliance has nothing to flag." "The sales team actually reads it when the audience section is specific."

This becomes: Downstream dependency map. Quality criteria that go beyond "the brief sounds good" to "the brief enables the next step."

### Follow-up probes

- "Show me the last brief that worked well. What made it work?"
- "Show me one that caused problems downstream. What was missing?"
- "If you could add one required field that doesn't exist today, what would it be?"
- "What does the AI currently produce that you always have to fix?"

### What good answers contain

- Specific section names and field names
- Clear distinction between required and optional
- Named review gates with owners
- Concrete examples of vague-but-accepted content
- Stories about downstream failures caused by weak briefs

### What weak answers look like

- "We need a good brief." (Too vague. What makes it good?)
- "The AI should just know." (Know what? From where?)
- "It depends on the campaign." (Which parts depend? Which parts are always the same?)
- "We'll figure it out as we go." (The guide exists because this approach produces premature sufficiency.)

### What this informs in the system

- Campaign brief schema (required fields, optional fields, conditional fields)
- Missing-information check logic (what blocks drafting)
- Evidence-requirement flags (which fields need approved evidence)
- Review-gate specifications (which fields need human approval)
- Sufficiency criteria (when is the brief "good enough" to proceed?)
- Draft-generation input specification (what the composition agent needs)
- Quality-scoring dimensions (brand, grounding, citation, completeness)
- Downstream dependency map (what the brief enables)

### What this feeds in the HLD

- Decision-artifact data model (Section 3 of the HLD blueprint)
- Discovery / RIPC configuration for this workflow (Section 5)
- Sufficiency-gate specifications (Section 8)
- Governance workflow for review-gated fields (Section 9)

### Case-study observations to preserve

While asking these questions, note:

- What does the current brief look like? (Capture a baseline artifact.)
- How long does it take to produce today?
- How often does the team copy forward without re-examining?
- What downstream failures have occurred because of brief quality?
- What does the team expect to improve?

---

## Category 3: KB / Information Surfaces

### Category purpose

Discover what the system must be able to see, retrieve, trust, cite, compare, or ignore. Information surfaces are the raw material of the perceived topography. If a source is not in the KB, it cannot create a gradient. If it is in the KB but poorly structured, it may be retrieved without being useful. If it is authoritative but unmarked, the system cannot distinguish it from opinion.

### Build output produced

- KB category candidates (the taxonomy)
- Source inventory (what exists today, where it lives, who owns it)
- Authority hierarchy (which sources are binding, which are advisory, which are background)
- Information-surface map (what the system can see for each decision type)
- Metadata fields (what each KB chunk must carry)
- Retrieval filters (how the system narrows search)
- Citation requirements (what the system must cite when drafting)
- Ownership model (who creates, reviews, and retires each category)
- Staleness / review cadence requirements (how often each category must be refreshed)
- Known knowledge gaps (what the team knows is missing)

### Core questions

**Q3.1 — What source materials do people actually rely on today?**

Ask this because the system will copy whatever the team actually uses, not what the process document says they use. If people rely on a Slack thread from six months ago instead of the official messaging doc, the system needs to know.

Listen for: "I always check the approved claims list." "I look at what the last campaign did." "I ask Sarah — she knows the ICPs." "There's a Google Doc somewhere." "I use the competitive battlecard, but it's from Q1."

This becomes: Source inventory. The first pass at KB categories. The gap between "what exists" and "what is used."

**Q3.2 — Which sources are authoritative — meaning the system should treat them as governing?**

Ask this because not all sources carry equal weight. An approved-claims repository is binding. A competitive battlecard is useful context. A Slack message from a sales rep is a signal, not a source of truth. The system must know the difference.

Listen for: "The approved claims list is the law." "Brand guidelines are non-negotiable." "The ICPs are pretty solid but they're from last year." "Sales notes are useful but anecdotal."

This becomes: Authority hierarchy. Source-type classification (binding / advisory / background / anecdotal). Confidence-display rules per source type.

**Q3.3 — Which sources are outdated but still being reused?**

Ask this because stale knowledge is worse than missing knowledge. Missing knowledge triggers a gap. Stale knowledge fills the gap with yesterday's answer and makes it feel sufficient today.

Listen for: "The healthcare ICP hasn't been updated since the reorg." "We're still using competitive positioning from before Carbyne's APEX launch." "The webinar playbook assumes the old event platform."

This becomes: Staleness detection requirements. Review-cadence specifications per source. Flags on knowledge that has aged past its review window.

**Q3.4 — What knowledge categories exist today, and what is missing?**

Ask this because the taxonomy defines what the system can see. If "competitive intelligence" is not a category, competitive context will not be retrieved. If "approved claims" is not a category, claim governance has no source to check against.

Listen for existing categories (brand voice, ICPs, messaging, playbooks, competitive intel, case studies, product docs, compliance rules, campaign performance). Listen for gaps ("We don't have a formal approved-claims list." "Nobody owns competitive intel." "There's no playbook for events.").

This becomes: KB taxonomy (category list). Gap inventory (what must be created before the system can operate). Priority order for knowledge creation.

**Q3.5 — What knowledge should be structured before it enters the system?**

Ask this because unstructured knowledge is hard to retrieve, hard to cite, and hard to govern. A 40-page brand guide is less useful than structured DO/DON'T rules with vertical adaptations. A narrative ICP is less useful than structured sections (pain points, buying signals, objections, decision process).

Listen for: "The brand guide exists but nobody reads the whole thing." "Our ICPs are in a slide deck." "The playbooks are in someone's head."

This becomes: Chunking strategy. Structured-input templates per category. Metadata requirements that must be captured at upload time (category, title, vertical, owner, date).

**Q3.6 — What should be searchable, and what should be filterable?**

Ask this because semantic search alone is not enough. The system should be able to filter by category (show me only competitive intel), by vertical (show me only healthcare), by owner (show me what product marketing governs), and by recency (show me what was updated in the last 90 days).

Listen for: "I need to find all the healthcare messaging." "I want to see what's changed since last quarter." "I need to check if we have anything on K-12." "Show me everything the brand team owns."

This becomes: Metadata fields (category, vertical, owner, updated date, review cadence). Retrieval filter specifications. Search-interface requirements.

**Q3.7 — What should the system cite when it drafts?**

Ask this because citation is how governance becomes visible. If the system drafts without citing sources, a reviewer cannot tell whether the language came from approved claims, product docs, competitive positioning, or the model's training data.

Listen for: "We need to know where the language came from." "If it's making a clinical claim, it better cite the approved claims list." "The brand voice rules should be traceable."

This becomes: Citation requirements per content type. Source-tracing specifications. Quality-scoring rules for citation coverage.

**Q3.8 — What should never be treated as a source of truth?**

Ask this because some information should inform the system without governing it. A sales rep's anecdote about a prospect should not become a positioning statement. A blog post about the industry should not become a product claim. A prior campaign draft should not become messaging doctrine.

Listen for: "Sales notes are useful context but not positioning." "Industry articles are background, not our voice." "Old drafts should not be reused as approved content."

This becomes: Source-type restrictions. Authority-level metadata. Retrieval rules that surface background context without treating it as governing.

**Q3.9 — What needs an owner, and what needs a review cadence?**

Ask this because knowledge without ownership becomes stale without anyone noticing. The team that created it moves on. The market changes. The product evolves. Nobody updates the source because nobody is responsible.

Listen for: "Product marketing owns ICPs." "The brand team owns voice guidelines." "Nobody owns competitive intel right now." "The playbooks were written by someone who left."

This becomes: Ownership model per KB category. Review cadence per category (30 days for competitive, 90 days for ICPs, 120 days for playbooks). Staleness-notification workflow.

**Q3.10 — What metadata would make retrieval safer or more useful?**

Ask this because metadata is what makes retrieval reasoning-relevant rather than merely semantic. Category, vertical, owner, updated date, review status, authority level, confidence, and applicability boundary — these fields turn a text chunk into a governed knowledge surface.

Listen for: "I need to know when it was last reviewed." "I need to know if it's approved or draft." "I need to know which vertical it applies to." "I need to know who signed off."

This becomes: Metadata schema per KB chunk. Minimum required metadata at upload. Metadata-display rules at retrieval time.

### Follow-up probes

- "Walk me through where you go when you start a new campaign. What do you open first?"
- "What source have you relied on that turned out to be wrong?"
- "If you had to hand this workflow to a new hire, what sources would you point them to? Which ones would you warn them about?"
- "What knowledge exists in someone's head that has never been written down?"

### What good answers contain

- Named sources with locations (Google Drive, Confluence, Slack, someone's head)
- Clear authority distinctions ("the approved claims list is binding; the competitive doc is advisory")
- Named owners or explicit gaps ("nobody owns competitive intel right now")
- Concrete examples of stale or misused knowledge
- Metadata wish list ("I wish I could filter by vertical and recency")

### What weak answers look like

- "We have a lot of documents." (Which ones matter? Which ones are used?)
- "Everything is in Google Drive." (Existence is not structure. Structure is not governance.)
- "The AI should figure out what's relevant." (The AI cannot distinguish binding from advisory without metadata.)
- "We'll upload everything and see what works." (This produces the KB equivalent of a knowledge-management graveyard.)

### What this informs in the system

- KB taxonomy and category structure
- Source inventory and authority hierarchy
- Metadata schema per chunk (category, title, vertical, owner, updated, review cadence, authority level, status)
- Retrieval filter specifications
- Citation and source-tracing requirements
- Ownership model
- Staleness detection and notification workflow
- Known knowledge gaps and priority order for creation

### What this feeds in the HLD

- Information-surface registry (Section 4 of the HLD blueprint)
- Reasoning-relevant retrieval architecture: metadata indexing, filter design, authority weighting (Section 6)
- State lifecycle model: staleness detection, review cadence (Section 8)
- Governance workflow: ownership, review, approval (Section 9)
- Volume management and retention (Section 12)

### Case-study observations to preserve

While asking these questions, note:

- How many sources exist today? How many are actually used?
- What is the gap between "documented" and "relied upon"?
- Where does the team go when they cannot find what they need? (This reveals information-surface failures.)
- What knowledge has been lost when someone left?
- How does the team currently know when something is out of date? (Usually: they don't.)

---

## Category 4: Trust, Evidence, and Confidence

*Intent: Map what the team trusts, doubts, or argues about. This category produces confidence-display rules, retrieval weighting, and evidence-requirement flags. It answers Appendix A Question 4: "What information do people trust, ignore, or argue about?"*

### Build output produced

Confidence map, source-trust hierarchy, evidence-requirement rules, retrieval-weighting specifications.

### Core questions — placeholder

*(To be fully drafted in a future version.)*

---

## Category 5: Assumptions / Premises

*Intent: Surface working beliefs that shape the decision but are not examined. This category produces Premise Stack schema, assumption-capture logic, and confidence markers. It answers Appendix A Question 6: "What are we acting as though we already know?"*

### Build output produced

Premise Stack schema, assumption inventory, confidence markers, re-examination triggers.

### Core questions — placeholder

*(To be fully drafted in a future version.)*

---

## Category 6: Policy / Governance Boundaries

*Intent: Shape gradients away from unsafe claims. This category produces policy rules, claim-validation logic, approval gates, and brand/compliance scoring. It answers Appendix A Question 7: "What rules, approvals, brand promises, or 'don't mess this up' concerns can change the answer?"*

### Build output produced

Policy-rule specifications, claim-validation logic, restricted-term lists, approval-gate workflow, brand/compliance scoring dimensions.

### Core questions — placeholder

*(To be fully drafted in a future version.)*

---

## Category 7: Sufficiency and Stopping Conditions

*Intent: Define when the system can act or must pause. This category produces stop/ask/escalate logic, confidence thresholds, and quality gates. It answers Appendix A Questions 8–10: where the team moves too fast, when the system should stop, and what "enough" looks like.*

### Build output produced

Sufficiency-condition specification, escalation rules, blocking conditions, quality-gate thresholds, abstention logic.

### Core questions — placeholder

*(To be fully drafted in a future version.)*

---

## Category 8: Reasoning to Preserve

*Intent: Keep "why" from disappearing. This category produces the reasoning-state preservation scope for the workflow — which of the six reasoning objects are captured, with what fields, at what granularity. It answers Appendix A Questions 12–16.*

### Build output produced

Reasoning-state preservation scope, per-object field specifications, reasoning-capture triggers, minimum viable reasoning record.

### Core questions — placeholder

*(To be fully drafted in a future version.)*

---

## Category 9: Learning Loop

*Intent: Make the next run smarter. This category produces Learning Event and Model Update Object specifications, analytics feedback requirements, and effectiveness-tracking criteria. It answers Appendix A Questions 18–23.*

### Build output produced

Learning Event schema, MUO schema, outcome-capture requirements, prediction-error triggers, applicability-boundary specifications, effectiveness signal.

### Core questions — placeholder

*(To be fully drafted in a future version.)*

---

## Category 10: Retrieval Relevance

*Intent: Retrieve prior reasoning, not just similar text. This category produces reasoning-relevant retrieval specifications, applicability rules, and confidence/provenance display requirements. It draws on the HLD planning blueprint's first-class retrieval section.*

### Build output produced

Retrieval-relevance rules, match-rationale display, applicability-boundary matching, prior-reasoning surfacing logic, reuse-confirmation requirements.

### Core questions — placeholder

*(To be fully drafted in a future version.)*

---

## Category 11: Human Confirmation

*Intent: Keep humans in the correction loop without creating confirmation fatigue. This category produces RIPC flow specifications, review-UI requirements, confirmation records, and override logic. It draws on the paper's Discovery / RIPC architecture and the HLD blueprint's confirmation-fatigue mitigations.*

### Build output produced

Confirmation-point map, RIPC stage specifications, confirmation-record schema, fatigue-mitigation rules, override and re-entry logic.

### Core questions — placeholder

*(To be fully drafted in a future version.)*

---

## Category 12: Ownership / Lifecycle

*Intent: Keep knowledge current and governed. This category produces the ownership model, review cadence, staleness-detection rules, and notification workflow. It answers: who creates, reviews, updates, deprecates, and retires each knowledge category?*

### Build output produced

Ownership model per category, review-cadence specifications, staleness-detection rules, notification workflow, lifecycle-state transitions.

### Core questions — placeholder

*(To be fully drafted in a future version.)*

---

## Category 13: Build Translation

*Intent: Turn all answers from categories 1–12 into an HLD input packet. This category is not a discovery session — it is a translation step. It maps discovery outputs to architecture components.*

### Build output produced

Architecture-landing summary, HLD input packet, data-object specifications, service-pattern requirements, integration requirements.

### Core questions — placeholder

*(To be fully drafted in a future version. This category will include the translation table from Appendix A's "How the Interview Becomes Design" section.)*

---

## Appendix: How to Use the Answers as HLD Inputs

Each category produces specifications. Those specifications feed directly into the HLD / Reference Architecture.

| Category | HLD section it feeds |
| --- | --- |
| Workflow boundary | Section 13: Minimal viable implementation — first workflow scope |
| Campaign brief structure | Section 3: Six-object data model — Decision State, Optimizer State |
| KB / information surfaces | Section 4: Supporting data objects — Information Surface records |
| Trust, evidence, and confidence | Section 6: Reasoning-relevant retrieval — confidence weighting |
| Assumptions / premises | Section 3: Six-object data model — Premise Stack |
| Policy / governance boundaries | Section 10: Governance and observability |
| Sufficiency and stopping conditions | Section 8: State lifecycle — sufficiency gates |
| Reasoning to preserve | Section 3: Six-object data model — all six objects |
| Learning loop | Section 7: Learning-loop architecture |
| Retrieval relevance | Section 6: Reasoning-relevant retrieval architecture |
| Human confirmation | Section 5: Discovery / RIPC service pattern |
| Ownership / lifecycle | Section 8: State lifecycle model |
| Build translation | All sections — architecture-landing summary |

---

## Appendix: Case-Study Observations to Preserve

The build guide is not a research instrument. But Path 1 (the actual build) should capture baseline observations that Path 2 (the formal academic paper) will later need.

While running the guide, preserve:

- **Baseline workflow pain points.** What is broken today, before the framework is applied?
- **Recurring failure modes.** Where does premature sufficiency, stale reasoning, or reasoning loss currently occur?
- **What reasoning currently disappears.** What does the team know that the system does not preserve?
- **What artifacts currently exist.** What documents, templates, playbooks, and governance already live somewhere?
- **How decisions currently become "good enough."** What is the current sufficiency condition? (Often: "the draft sounds professional.")
- **What outcomes are expected to improve.** What does the team predict will change?
- **What evidence would show the next cycle got smarter.** The team's own success criteria.

These observations are captured as natural byproducts of build discovery. They do not require separate data-collection sessions. They do not turn the guide into an academic study. They simply ensure that when the formal academic path needs baseline data, it is available.

---

*Draft status: v0.1 companion artifact skeleton. Fully drafted sample categories: Campaign Brief Structure and KB / Information Surfaces. Derived from PAPER_v1.0_WORKING.md, the accepted Executive Brief, and the Keystone / Two-Track Strategy note. Not a replacement for the full paper or the HLD.*
