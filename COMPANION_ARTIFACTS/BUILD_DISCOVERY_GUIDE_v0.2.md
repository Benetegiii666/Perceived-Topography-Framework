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

### Category 1 — Purpose

Define the repeated decision workflow the first build will target. This category bounds the entire discovery effort. Every later category is scoped to this workflow. If you get this wrong, you build the right system around the wrong problem.

### Category 1 — Build output produced

- Workflow name and definition
- Workflow boundary (start point, end point, what is in scope, what is out)
- Trigger event (what starts the workflow)
- Primary users (who produces the decision artifact)
- Downstream users (who consumes the output)
- Decision owner (who is accountable for the action)
- Recurrence pattern (how often this workflow repeats)
- Recurring failure modes (what goes wrong, how often, with what consequence)
- Success criteria (what "better" means for this workflow)
- First implementation slice (what the build will include)
- Explicit exclusions (what the build will intentionally leave out)

### Category 1 — Core questions

**Q1.1 — What repeated work are we trying to improve?**

Ask this because the system should not be built around a one-time project. It should be built around a workflow that repeats often enough that preserving reasoning pays off. If the workflow only happens once a year, the overhead of reasoning-state capture may exceed the benefit.

Listen for: "Campaign briefs — we do 15–20 a quarter." "Customer escalation responses — daily." "Compliance review of marketing claims — every launch." "Product launch messaging — every release cycle."

This becomes: Workflow name. Recurrence frequency. The first sentence of the workflow definition.

**Q1.2 — What event starts this workflow?**

Ask this because the trigger event defines the system's entry point. Discovery begins here. The system must know what initiates the cycle: a request, a calendar event, a market signal, a product release, a customer action.

Listen for: "Cassidy asks for a campaign." "A new product feature ships." "A customer complaint escalates." "The quarterly competitive review starts." "IACP conference registration opens."

This becomes: Trigger-event definition. Discovery entry point. The first step in the workflow specification.

**Q1.3 — What output ends the workflow?**

Ask this because the end point defines what the system must produce and when the workflow is complete. It also defines where reasoning-state capture should occur — at the moment the team commits to an action.

Listen for: "An approved campaign brief." "A set of channel assets ready for launch." "A compliance-reviewed messaging package." "A customer response that's been sent."

This becomes: Decision-artifact definition. The output schema. The point at which the Decision State is captured.

**Q1.4 — Who produces the output, and who consumes it?**

Ask this because primary users and downstream users have different needs. The person who drafts the brief needs retrieval, governance, and sufficiency checks. The person who executes the campaign needs a complete, unambiguous, approved artifact.

Listen for: "Marketing produces the brief. Creative executes the assets. Sales uses the messaging. Compliance reviews the claims." "I write it, but three other teams depend on it."

This becomes: User-role definitions. Downstream dependency map. Review-gate assignments.

**Q1.5 — What goes wrong often enough to justify system design?**

Ask this because this question surfaces the recurring failure modes that make the build worthwhile. If the team cannot name specific, repeated failures, the workflow may not need reasoning-state architecture.

Listen for: "We keep making unsupported claims." "The brief is always vague on audience." "We copy forward old messaging without checking if it still holds." "Every campaign starts cold — nobody remembers what worked last quarter." "Compliance catches problems after launch, not before."

This becomes: Failure-mode inventory. Premature-sufficiency risk map. The specific design targets for governance, sufficiency, and learning.

**Q1.6 — What does "better" mean for this workflow?**

Ask this because the team's success criteria determine what the system should optimize for and how effectiveness will be measured. "Better" is not "faster." It might be: fewer compliance flags, stronger qualified pipeline, less rework, better evidence grounding, or learning that actually changes the next cycle.

Listen for: "Fewer compliance rejections." "Campaigns that convert, not just engage." "Briefs that downstream teams can actually use without asking questions." "The second campaign for a vertical should be better than the first."

This becomes: Success criteria. Effectiveness signal. The outcome comparison that drives the learning loop.

**Q1.7 — What should the first build include?**

Ask this because scope discipline is critical. The first build should cover one workflow, a small reasoning-object schema, and enough governance to be useful. It should not attempt to model the whole organization.

Listen for: "Just the campaign brief workflow." "Just healthcare campaigns." "Just the brief and one channel — not the full execution pipeline yet." "Just brand and compliance governance, not competitive intel yet."

This becomes: First implementation slice. The scope constraint that prevents the build from becoming unmanageable.

**Q1.8 — What should the first build intentionally exclude?**

Ask this because explicit exclusions prevent scope creep. If the team knows what is out of scope, they will not try to force it in during the first cycle.

Listen for: "Not the full execution pipeline." "Not the sales enablement handoff." "Not multi-region or multi-language." "Not the research agent — just the context layer first."

This becomes: Exclusion list. Scope boundary. Future-phase candidates.

**Q1.9 — What evidence would show the next cycle got smarter?**

Ask this because this is the meta-question. If the system does not improve the next time the workflow runs, the reasoning-state architecture is not earning its place. The team should define what improvement looks like before the first cycle completes.

Listen for: "The second healthcare campaign brief should not re-make the readmissions claim mistake." "Next quarter, the brief should start with the lessons from this quarter." "Compliance should flag fewer issues because the system already knows the boundaries."

This becomes: Effectiveness signal. The prediction against which the next cycle is measured. The test of whether the build is working.

### Category 1 — Follow-up probes

- "Walk me through the last time this workflow ran. What happened step by step?"
- "If you could fix one thing about how this workflow operates today, what would it be?"
- "What would make you say, after 60 days, that the system is working?"
- "What is the simplest version of this build that would still be useful?"

### Category 1 — What good answers contain

- A named workflow with clear boundaries
- A concrete trigger event and end-point artifact
- Named users and downstream consumers
- Specific, repeated failure modes with examples
- Measurable or observable success criteria
- A narrow first scope with explicit exclusions

### Category 1 — What weak answers look like

- "We want to improve all our marketing." (Too broad. Which workflow?)
- "Everything should be AI-powered." (Not a workflow. A wish.)
- "We'll know it when we see it." (Success criteria must be stated before the build, not after.)
- "Let's just start and see what happens." (The guide exists because this approach produces premature sufficiency at the system-design level.)

### Category 1 — What this informs in the system

- Workflow definition and scope boundary
- Trigger-event and entry-point logic
- Decision-artifact output schema
- User-role definitions and downstream dependency map
- Failure-mode inventory and premature-sufficiency risk map
- Success criteria and effectiveness signal
- First implementation slice and exclusion list

### Category 1 — What this feeds in the HLD

- Section 13: Minimal viable implementation — first workflow selection, scope, success criteria
- Section 3: Six-object data model — workflow-scoped reasoning objects
- Section 8: State lifecycle — workflow-specific governance requirements

### Category 1 — Case-study observations to preserve

While asking these questions, note:

- How clearly can the team define the workflow boundary? (Fuzzy boundaries indicate the workflow may not be well understood.)
- How many failure modes does the team name spontaneously versus with prompting?
- Does the team have observable success criteria, or only vague aspirations?
- How narrow is the team willing to scope the first build? (Resistance to narrow scope often predicts scope creep.)

---

## Category 2: Campaign Brief Structure

### Category 2 — Purpose

Discover the structure of the campaign brief — or whatever the repeated decision artifact is. The campaign brief is the decision artifact: the document, form, or structured output that commits the team to a direction. Understanding its structure tells you what the system must produce, what it must check before producing, and what reasoning must survive the production.

### Category 2 — Build output produced

- Campaign brief schema (required fields, optional fields, conditional fields)
- Missing-information checks (what must be present before drafting)
- Evidence-backed fields (which fields require supporting evidence)
- Review-gated fields (which fields require human review before use)
- Sufficiency criteria for a usable brief
- Draft-generation inputs (what the AI needs before it can begin)
- Downstream dependency map (what breaks later when the brief is weak)

### Category 2 — Core questions

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

### Category 2 — Follow-up probes

- "Show me the last brief that worked well. What made it work?"
- "Show me one that caused problems downstream. What was missing?"
- "If you could add one required field that doesn't exist today, what would it be?"
- "What does the AI currently produce that you always have to fix?"

### Category 2 — What good answers contain

- Specific section names and field names
- Clear distinction between required and optional
- Named review gates with owners
- Concrete examples of vague-but-accepted content
- Stories about downstream failures caused by weak briefs

### Category 2 — What weak answers look like

- "We need a good brief." (Too vague. What makes it good?)
- "The AI should just know." (Know what? From where?)
- "It depends on the campaign." (Which parts depend? Which parts are always the same?)
- "We'll figure it out as we go." (The guide exists because this approach produces premature sufficiency.)

### Category 2 — What this informs in the system

- Campaign brief schema (required fields, optional fields, conditional fields)
- Missing-information check logic (what blocks drafting)
- Evidence-requirement flags (which fields need approved evidence)
- Review-gate specifications (which fields need human approval)
- Sufficiency criteria (when is the brief "good enough" to proceed?)
- Draft-generation input specification (what the composition agent needs)
- Quality-scoring dimensions (brand, grounding, citation, completeness)
- Downstream dependency map (what the brief enables)

### Category 2 — What this feeds in the HLD

- Decision-artifact data model (Section 3 of the HLD blueprint)
- Discovery / RIPC configuration for this workflow (Section 5)
- Sufficiency-gate specifications (Section 8)
- Governance workflow for review-gated fields (Section 9)

### Category 2 — Case-study observations to preserve

While asking these questions, note:

- What does the current brief look like? (Capture a baseline artifact.)
- How long does it take to produce today?
- How often does the team copy forward without re-examining?
- What downstream failures have occurred because of brief quality?
- What does the team expect to improve?

---

## Category 3: KB / Information Surfaces

### Category 3 — Purpose

Discover what the system must be able to see, retrieve, trust, cite, compare, or ignore. Information surfaces are the raw material of the perceived topography. If a source is not in the KB, it cannot create a gradient. If it is in the KB but poorly structured, it may be retrieved without being useful. If it is authoritative but unmarked, the system cannot distinguish it from opinion.

### Category 3 — Build output produced

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

### Category 3 — Core questions

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

### Category 3 — Follow-up probes

- "Walk me through where you go when you start a new campaign. What do you open first?"
- "What source have you relied on that turned out to be wrong?"
- "If you had to hand this workflow to a new hire, what sources would you point them to? Which ones would you warn them about?"
- "What knowledge exists in someone's head that has never been written down?"

### Category 3 — What good answers contain

- Named sources with locations (Google Drive, Confluence, Slack, someone's head)
- Clear authority distinctions ("the approved claims list is binding; the competitive doc is advisory")
- Named owners or explicit gaps ("nobody owns competitive intel right now")
- Concrete examples of stale or misused knowledge
- Metadata wish list ("I wish I could filter by vertical and recency")

### Category 3 — What weak answers look like

- "We have a lot of documents." (Which ones matter? Which ones are used?)
- "Everything is in Google Drive." (Existence is not structure. Structure is not governance.)
- "The AI should figure out what's relevant." (The AI cannot distinguish binding from advisory without metadata.)
- "We'll upload everything and see what works." (This produces the KB equivalent of a knowledge-management graveyard.)

### Category 3 — What this informs in the system

- KB taxonomy and category structure
- Source inventory and authority hierarchy
- Metadata schema per chunk (category, title, vertical, owner, updated, review cadence, authority level, status)
- Retrieval filter specifications
- Citation and source-tracing requirements
- Ownership model
- Staleness detection and notification workflow
- Known knowledge gaps and priority order for creation

### Category 3 — What this feeds in the HLD

- Information-surface registry (Section 4 of the HLD blueprint)
- Reasoning-relevant retrieval architecture: metadata indexing, filter design, authority weighting (Section 6)
- State lifecycle model: staleness detection, review cadence (Section 8)
- Governance workflow: ownership, review, approval (Section 9)
- Volume management and retention (Section 12)

### Category 3 — Case-study observations to preserve

While asking these questions, note:

- How many sources exist today? How many are actually used?
- What is the gap between "documented" and "relied upon"?
- Where does the team go when they cannot find what they need? (This reveals information-surface failures.)
- What knowledge has been lost when someone left?
- How does the team currently know when something is out of date? (Usually: they don't.)

---

## Category 4: Trust, Evidence, and Confidence

*Intent: Map what the team trusts, doubts, or argues about. This category produces confidence-display rules, retrieval weighting, and evidence-requirement flags. It answers Appendix A Question 4: "What information do people trust, ignore, or argue about?"*

### Category 4 — Build output produced

Confidence map, source-trust hierarchy, evidence-requirement rules, retrieval-weighting specifications.

### Category 4 — Core questions — placeholder

*(To be fully drafted in a future version.)*

---

## Category 5: Assumptions / Premises

*Intent: Surface working beliefs that shape the decision but are not examined. This category produces Premise Stack schema, assumption-capture logic, and confidence markers. It answers Appendix A Question 6: "What are we acting as though we already know?"*

### Category 5 — Build output produced

Premise Stack schema, assumption inventory, confidence markers, re-examination triggers.

### Category 5 — Core questions — placeholder

*(To be fully drafted in a future version.)*

---

## Category 6: Policy / Governance Boundaries

### Category 6 — Purpose

Discover the rules, approvals, brand promises, compliance constraints, evidence requirements, and escalation conditions that should shape system behavior. These are the forces that prevent the easy path from also being the unsafe path. In the framework's language, governance boundaries shape gradients: they make some actions harder, some claims require evidence, some language require review, and some paths require human approval before the system proceeds.

Without this category, the system may retrieve the right context and still produce an unsafe output — because the policy existed as a document but did not exert force at the moment of generation.

### Category 6 — Build output produced

- Policy-rule inventory (all rules that should constrain system output)
- Approved-claim rules (what claims require approved evidence, which claims are pre-approved)
- Restricted-language rules (terms that must be flagged or replaced)
- Preferred-language rules (terms the system should use)
- Evidence requirements (which claim types need supporting evidence before use)
- Compliance review gates (what must be reviewed before publish)
- Brand review gates (what must be reviewed for voice and positioning)
- Escalation triggers (what should be routed to a human with authority)
- Claim-validation logic (how the system checks whether a claim is supported)
- Governance scoring dimensions (how the system scores output for policy compliance)
- Human approval requirements (who must approve, for what types of content)
- Audit and provenance requirements (what must be traceable after the fact)

### Category 6 — Core questions

**Q6.1 — What claims require approved evidence before the system can use them?**

Ask this because this is the most direct premature-sufficiency prevention. A system that can generate clinical-outcome claims, ROI statements, or competitive superiority claims without checking for approved evidence has a strong gradient toward unsupported action.

Listen for: "Clinical outcomes need an approved study." "ROI claims need finance sign-off." "Competitive comparisons need the battlecard." "Customer quotes need legal release."

This becomes: Claim-type taxonomy. Evidence-requirement rules per claim type. Pre-draft blocking conditions for unsupported claims.

**Q6.2 — What language is approved, preferred, discouraged, or prohibited?**

Ask this because language rules are the most granular form of governance. "Surveillance" is prohibited; "augment responders" is preferred. "Automate 911" is prohibited; "enhance public safety" is approved. These rules must be machine-readable, not buried in a 40-page brand guide.

Listen for: "Never say 'replace dispatchers.'" "Always say 'augment responders.'" "Don't use 'cost-cutting through automation.'" "Use 'mission-critical' and 'evidence-based.'" "Healthcare content should lead with patient outcomes and HIPAA compliance."

This becomes: DO/DON'T word lists. Restricted-term detection rules. Replacement-suggestion logic. Vertical-specific adaptations (healthcare language differs from enterprise language differs from K-12 language).

**Q6.3 — Which rules are hard constraints versus guidance?**

Ask this because the system should treat hard constraints (never make an unsupported clinical claim) differently from guidance (prefer "augment responders" over "assist responders"). A hard constraint should block or flag. Guidance should coach and suggest.

Listen for: "The approved-claims boundary is a hard stop." "Brand voice is strongly preferred but not a blocker." "Compliance rules are non-negotiable." "The tone guidelines are aspirational."

This becomes: Rule-severity classification (blocking / flagging / coaching). Different governance behaviors per severity level.

**Q6.4 — Who can approve exceptions?**

Ask this because some rules should be breakable by someone with authority. A CMO may approve language that stretches the brand voice for a specific campaign. A compliance officer may approve a qualified clinical claim with appropriate caveats. The system should know who can override, not just what the rule says.

Listen for: "Compliance can approve a qualified claim." "Cassidy can override brand voice for a specific campaign." "Legal has final say on anything in regulated verticals." "Nobody overrides the restricted-terms list."

This becomes: Override-authority model. Exception-approval workflow. Audit trail for exceptions.

**Q6.5 — What must the system never say without supporting evidence?**

Ask this because this question produces the hardest governance rules — the ones where getting it wrong creates material risk. In healthcare: unsupported clinical outcomes. In enterprise: unsubstantiated ROI. In K-12: fear-based safety claims. In competitive positioning: unverifiable superiority claims.

Listen for: "Never claim the product reduces readmissions unless we have the study." "Never say we're the only platform that does X." "Never imply clinical efficacy without approved language." "Never use customer data without a signed release."

This becomes: Hard-constraint list. Pre-generation blocking rules. The highest-priority governance scoring dimensions.

**Q6.6 — What should be flagged but not blocked?**

Ask this because coaching is more effective than rejection. If the system flags "surveillance" and suggests "augment responders," the contributor learns the rule by using the system. If the system silently blocks the content, the contributor learns nothing.

Listen for: "Flag restricted terms but let them acknowledge and proceed." "Show the brand voice suggestions but don't reject the draft." "Flag when the ICP fit is weak but don't prevent submission."

This becomes: Coaching-mode governance behavior. Flag-and-suggest logic. Acknowledge-and-proceed workflow.

**Q6.7 — What should be blocked until reviewed?**

Ask this because some content should not be publishable without human review. A clinical-outcome claim should not pass through the system without compliance review. A competitive comparison should not go live without product marketing review.

Listen for: "Anything with clinical language goes through compliance before publish." "Competitive claims need product marketing sign-off." "Executive quotes need PR approval."

This becomes: Review-gate specifications. Publish-blocking conditions. Approval-workflow integration.

**Q6.8 — What needs citation or provenance after the fact?**

Ask this because audit requirements shape how governance records must be preserved. If a regulator or legal team later asks "where did this claim come from?", the system must be able to trace the language to its source.

Listen for: "We need to know which approved claim was used." "If a customer complains about a product statement, we need to trace it." "Compliance needs to audit what sources were cited in healthcare content."

This becomes: Citation and provenance requirements. Source-tracing specifications. Audit-trail design.

**Q6.9 — What creates the most risk if the system gets it wrong?**

Ask this because this question identifies the highest-stakes governance targets. The system should invest the most governance effort where failure is most consequential.

Listen for: "An unsupported clinical claim could trigger an FDA warning." "A false competitive claim could damage a partner relationship." "An insensitive school-safety message could go viral." "A data-privacy violation could mean litigation."

This becomes: Risk-weighted governance priorities. The governance dimensions that receive the most scoring weight. The escalation triggers that are most critical.

**Q6.10 — What governance exists today that the system should inherit?**

Ask this because the team may already have governance that works — it just is not connected to the AI system. An approved-claims list may exist but not be retrieved during drafting. A brand guide may exist but not be checked at generation time. The system should inherit existing governance, not reinvent it.

Listen for: "We have an approved-claims spreadsheet." "The brand guide has DO/DON'T lists." "Compliance has a review checklist." "There's an approval workflow in Asana."

This becomes: Existing governance inventory. Integration requirements. The gap between "governance exists" and "governance is connected to the generation pipeline."

### Category 6 — Follow-up probes

- "Show me the last time a governance rule prevented a mistake. How did it work?"
- "Show me the last time a governance rule failed to prevent a mistake. What was missing?"
- "If the system flagged 'surveillance' and suggested 'augment responders,' would the team accept that coaching?"
- "What governance rule does the team work around because it is too cumbersome?"

### Category 6 — What good answers contain

- Named rules with severity levels (blocking / flagging / coaching)
- Specific terms on DO/DON'T lists
- Named approvers with scope of authority
- Concrete examples of claims that require evidence
- Existing governance artifacts with locations
- Stories about governance failures and near-misses

### Category 6 — What weak answers look like

- "We follow brand guidelines." (Which ones? Are they connected to the generation pipeline?)
- "Compliance handles that." (Handles what? When? Before or after generation?)
- "The AI should be responsible." (The AI cannot enforce rules it does not know. Governance is a system property, not a model property.)
- "We'll add governance later." (Governance added after the system is running is governance added after the first mistakes have been made.)

### Category 6 — What this informs in the system

- Policy-rule inventory and severity classification
- DO/DON'T word lists with replacement suggestions
- Claim-type taxonomy and evidence-requirement rules
- Review-gate specifications and approval workflows
- Coaching-mode governance behavior (flag, suggest, acknowledge)
- Governance scoring dimensions (brand compliance, factual grounding, citation coverage)
- Override-authority model and exception workflow
- Audit and provenance requirements

### Category 6 — What this feeds in the HLD

- Section 10: Governance and observability — role-based access, review workflows, audit logging
- Section 5: Discovery / RIPC — policy retrieval during inference, claim-level governance during proposal
- Section 8: State lifecycle — governance status transitions, review triggers
- Section 14: Risks and mitigations — policy laundering, automation bias, false precision

### Category 6 — Case-study observations to preserve

While asking these questions, note:

- How many governance rules exist today? How many are actually enforced in the current workflow?
- What is the gap between "documented rules" and "behaviorally effective rules"?
- Does the team work around any governance because it is too cumbersome?
- What governance failures have occurred in the last 6 months?
- How does the team currently know whether generated content is compliant? (Usually: someone reads it after the fact.)

---

## Category 7: Sufficiency and Stopping Conditions

### Category 7 — Purpose

Define when the system should proceed, pause, ask, escalate, abstain, or require human confirmation. This category is central to the framework because premature sufficiency — acting before the reasoning warrants it — is the shared failure mode across hallucination, unsafe claims, weak strategy, and repeated organizational mistakes.

Most teams have never explicitly defined what "good enough" means. They know it when they see it, which means the system will default to whatever feels complete — usually fluency and familiarity, not evidence and grounding.

This category turns implicit stopping conditions into explicit, buildable specifications.

### Category 7 — Build output produced

- Sufficiency criteria (what must be true before the system acts)
- Pre-draft blocking conditions (what prevents the system from generating output)
- Stop / ask / proceed / escalate rules (decision tree for system behavior)
- Confidence thresholds (minimum confidence levels per field or claim type)
- Quality gates (scoring thresholds that must be met before output is usable)
- Missing-information checks (what gaps should block action)
- Unsupported-claim checks (what evidence gaps should flag or block)
- Uncertainty triggers (what should make the system ask rather than act)
- Abstention logic (what should make the system refuse to complete)
- Human-review triggers (what should route to a person with authority)
- Premature-sufficiency risk map (where the workflow is most vulnerable)

### Category 7 — Core questions

**Q7.1 — What makes a draft or decision feel "good enough" today?**

Ask this because the current sufficiency condition is almost always implicit. "It sounds right." "It looks professional." "It's what we've done before." "Nobody complained last time." These are the real stopping conditions — and they are the ones the system will inherit unless better ones are designed.

Listen for: "When it reads well." "When it covers the main points." "When it matches what we've done before." "When nobody pushes back." "When we're out of time."

This becomes: Current-state sufficiency baseline. The gap between what "good enough" means today and what it should mean with reasoning-state architecture.

**Q7.2 — Where does the team move too fast and regret it later?**

Ask this because this question directly surfaces premature-sufficiency patterns. The team already knows where they tend to produce confident-but-wrong work. They may not call it premature sufficiency, but they know the pattern: the draft sounded good, the claim seemed plausible, the audience section felt reasonable — and then it turned out to be wrong.

Listen for: "We rushed the messaging and compliance caught it." "The audience assumption was wrong but the brief looked fine." "We copied the positioning from last quarter and the market had changed." "The AI draft was polished so nobody questioned the claims."

This becomes: Premature-sufficiency risk map. The specific points in the workflow where the system needs stronger stopping conditions.

**Q7.3 — What information must be present before the system acts?**

Ask this because some gaps should be blocking. If the system does not have the ICP, it should not draft audience-specific messaging. If the system does not have the approved-claims list, it should not draft evidence-dependent claims. If the system does not know the goal, it should not draft anything.

Listen for: "Don't draft without the ICP." "Don't use clinical language without the claims list." "Don't start without the campaign objective." "Don't generate competitive content without the current battlecard."

This becomes: Pre-action required-information list. Missing-information check logic. Blocking conditions that prevent the system from generating output with insufficient input.

**Q7.4 — What uncertainty should force a pause?**

Ask this because some uncertainties are material — they could change the action. If the system is uncertain whether a claim is approved, it should not generate the claim and hope for the best. If the audience interpretation is low-confidence, the system should flag the interpretation before building a campaign around it.

Listen for: "If we're not sure whether the claim is approved, don't use it." "If the ICP is from last year, flag it." "If we don't know the buyer's readiness stage, ask." "If the competitive positioning is stale, say so."

This becomes: Uncertainty triggers. Flag-before-proceed conditions. Confidence thresholds that distinguish "proceed" from "flag" from "block."

**Q7.5 — What evidence gap should block action entirely?**

Ask this because some gaps are not merely inconvenient — they create material risk. Missing approved evidence for a clinical claim is not a gap to flag; it is a gap to block. Missing legal review for a competitive comparison is not a coaching opportunity; it is a stop condition.

Listen for: "No clinical claims without an approved study — period." "No competitive comparisons without product marketing sign-off." "No customer data without a signed release." "No content about school shootings without sensitivity review."

This becomes: Hard-block conditions. The most critical entries in the sufficiency specification. Pre-generation blocking rules.

**Q7.6 — What should trigger a human review?**

Ask this because some decisions should not be made by the system alone. The system can flag, suggest, and propose — but certain actions require a human with authority to confirm. The question is: which ones?

Listen for: "Compliance reviews all healthcare claims." "Brand reviews the headline." "The CMO signs off on competitive messaging." "Nobody reviews the audience section — maybe they should."

This becomes: Human-review trigger list. Review-gate assignments by field, claim type, or risk level.

**Q7.7 — What should the system ask before continuing?**

Ask this because asking is an action. "I don't have enough to draft this section — can you confirm the audience?" is not failure. It is the correct behavior when the reasoning state is insufficient. The system needs designed asking points, not just designed generation points.

Listen for: "It should ask whether the ICP is current." "It should ask who approved the claims list." "It should check whether the competitive positioning has been updated." "It should confirm the campaign objective before drafting."

This becomes: Discovery / RIPC configuration. The system's asking points. The questions the system poses before proceeding to generation.

**Q7.8 — What should the system refuse to complete?**

Ask this because abstention is a legitimate action. A system that cannot say "I should not do this" will default to completion. If the system does not have a way to refuse, it will produce unsafe, unsupported, or misleading output because the only exit is completion.

Listen for: "It should never draft a clinical claim without evidence." "It should refuse to generate if the goal is missing." "It should not produce content in a regulated vertical without the compliance checklist."

This becomes: Abstention rules. The conditions under which the system produces a "cannot proceed" response instead of a draft.

**Q7.9 — What are the signs that fluency is being mistaken for evidence?**

Ask this because this is the operational definition of premature sufficiency. The draft sounds good. The language is professional. The structure is complete. But the claims are unsupported, the audience is assumed, the evidence is missing, and the system produced a polished version of the wrong answer.

Listen for: "The draft reads well but the numbers aren't sourced." "It sounds like our voice but the claims are made up." "The audience section is plausible but it's not based on our ICP." "Compliance flagged it but the team had already started executing."

This becomes: Quality-scoring rules that check grounding, not just fluency. Citation requirements. Evidence-presence checks. The distinction between "sounds good" and "is grounded."

**Q7.10 — What does "sufficient to proceed" mean for each major field or step?**

Ask this because sufficiency is not one thing. The audience section is sufficient when it reflects a current, confirmed ICP. The claims section is sufficient when every claim has an approved evidence source. The messaging is sufficient when it passes brand voice review. The brief is sufficient when all required fields are present and all review gates have been cleared.

Listen for: field-by-field stopping criteria. "The audience section is done when it maps to a current ICP." "The claims are done when each one cites an approved source." "The brief is done when compliance has reviewed the healthcare sections."

This becomes: Per-field sufficiency conditions. The most granular level of the sufficiency specification. The foundation for quality-gate scoring.

### Category 7 — Follow-up probes

- "Tell me about the last time the team shipped something that turned out to be wrong. What made it feel sufficient at the time?"
- "If the system paused and said 'I don't have enough evidence to draft this claim,' would the team accept that?"
- "What is the difference between a draft that is good enough to share and a draft that is good enough to publish?"
- "How do you know when 'good enough' is actually good enough versus when you're just out of time?"

### Category 7 — What good answers contain

- Named stopping conditions per field or step
- Clear distinction between "flag" and "block" and "refuse"
- Concrete examples of premature sufficiency in the current workflow
- Named review gates with trigger conditions
- Stories about when fluency was mistaken for evidence
- Per-field definitions of what "sufficient" means

### Category 7 — What weak answers look like

- "We'll know it when we see it." (The system cannot "see it." It needs explicit conditions.)
- "The AI should use its judgment." (The AI's judgment is whatever feels most fluent. That is the problem.)
- "We don't want to slow things down." (Premature sufficiency is fast. Grounded sufficiency is reliable. The question is which one you want.)
- "Everything goes through review anyway." (After-the-fact review is not the same as designed sufficiency. Review catches mistakes. Sufficiency prevents them.)

### Category 7 — What this informs in the system

- Sufficiency-condition specification (per-field, per-step, per-claim-type)
- Pre-draft blocking conditions
- Stop / ask / proceed / escalate decision logic
- Confidence thresholds per field
- Quality-gate scoring thresholds
- Missing-information check logic
- Uncertainty triggers and flag-before-proceed conditions
- Abstention rules
- Human-review triggers
- Premature-sufficiency risk map

### Category 7 — What this feeds in the HLD

- Section 8: State lifecycle model — sufficiency gates, transition triggers
- Section 5: Discovery / RIPC — asking points, re-entry logic
- Section 10: Governance and observability — review workflows, escalation paths
- Section 13: Minimal viable implementation — first-build sufficiency criteria
- Section 14: Risks and mitigations — confirmation fatigue, automation bias

### Category 7 — Case-study observations to preserve

While asking these questions, note:

- What is the current implicit sufficiency condition? (Capture it in the team's own words.)
- How often does the team proceed when they know a section is weak? (This is the premature-sufficiency frequency.)
- What happens when the team is under time pressure? (Time pressure reliably degrades sufficiency.)
- What has been caught by downstream review that should have been caught earlier?
- Does the team have any explicit stopping criteria today, or is "good enough" always implicit?

---

## Category 8: Reasoning to Preserve

*Intent: Keep "why" from disappearing. This category produces the reasoning-state preservation scope for the workflow — which of the six reasoning objects are captured, with what fields, at what granularity. It answers Appendix A Questions 12–16.*

### Category 8 — Build output produced

Reasoning-state preservation scope, per-object field specifications, reasoning-capture triggers, minimum viable reasoning record.

### Category 8 — Core questions — placeholder

*(To be fully drafted in a future version.)*

---

## Category 9: Learning Loop

*Intent: Make the next run smarter. This category produces Learning Event and Model Update Object specifications, analytics feedback requirements, and effectiveness-tracking criteria. It answers Appendix A Questions 18–23.*

### Category 9 — Build output produced

Learning Event schema, MUO schema, outcome-capture requirements, prediction-error triggers, applicability-boundary specifications, effectiveness signal.

### Category 9 — Core questions — placeholder

*(To be fully drafted in a future version.)*

---

## Category 10: Retrieval Relevance

*Intent: Retrieve prior reasoning, not just similar text. This category produces reasoning-relevant retrieval specifications, applicability rules, and confidence/provenance display requirements. It draws on the HLD planning blueprint's first-class retrieval section.*

### Category 10 — Build output produced

Retrieval-relevance rules, match-rationale display, applicability-boundary matching, prior-reasoning surfacing logic, reuse-confirmation requirements.

### Category 10 — Core questions — placeholder

*(To be fully drafted in a future version.)*

---

## Category 11: Human Confirmation

*Intent: Keep humans in the correction loop without creating confirmation fatigue. This category produces RIPC flow specifications, review-UI requirements, confirmation records, and override logic. It draws on the paper's Discovery / RIPC architecture and the HLD blueprint's confirmation-fatigue mitigations.*

### Category 11 — Build output produced

Confirmation-point map, RIPC stage specifications, confirmation-record schema, fatigue-mitigation rules, override and re-entry logic.

### Category 11 — Core questions — placeholder

*(To be fully drafted in a future version.)*

---

## Category 12: Ownership / Lifecycle

*Intent: Keep knowledge current and governed. This category produces the ownership model, review cadence, staleness-detection rules, and notification workflow. It answers: who creates, reviews, updates, deprecates, and retires each knowledge category?*

### Category 12 — Build output produced

Ownership model per category, review-cadence specifications, staleness-detection rules, notification workflow, lifecycle-state transitions.

### Category 12 — Core questions — placeholder

*(To be fully drafted in a future version.)*

---

## Category 13: Build Translation

*Intent: Turn all answers from categories 1–12 into an HLD input packet. This category is not a discovery session — it is a translation step. It maps discovery outputs to architecture components.*

### Category 13 — Build output produced

Architecture-landing summary, HLD input packet, data-object specifications, service-pattern requirements, integration requirements.

### Category 13 — Core questions — placeholder

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

*Draft status: v0.2 companion artifact. Fully drafted categories: Workflow Boundary, Campaign Brief Structure, KB / Information Surfaces, Policy / Governance Boundaries, and Sufficiency and Stopping Conditions. Derived from PAPER_v1.0_WORKING.md, the accepted Executive Brief, the Keystone / Two-Track Strategy note, and Build Discovery Guide v0.1. Not a replacement for the full paper or the HLD.*
