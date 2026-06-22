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

### Category 4 — Purpose

Map what the team trusts, doubts, argues about, treats as evidence, and treats as merely suggestive. This category defines how the system distinguishes authoritative sources from weak signals, how it displays confidence, and what evidence standards must be met before a claim can be used. Without this category, the system treats all retrieved information as equally trustworthy — which means a sales anecdote carries the same weight as an approved clinical study.

### Category 4 — Build output produced

- Confidence map (what the team is confident about, uncertain about, and actively debating)
- Source-trust hierarchy (which sources are authoritative, which are advisory, which are anecdotal)
- Evidence-quality levels (what counts as strong evidence, weak evidence, and mere signal)
- Evidence-requirement rules (what evidence standard must be met per claim type)
- Confidence-display requirements (how the system shows certainty and uncertainty to users)
- Retrieval-weighting specifications (how source authority affects retrieval ranking)
- Provenance requirements (what source information must accompany generated content)
- Uncertainty markers (how the system flags low-confidence content)
- Source-conflict handling (what happens when trusted sources disagree)
- Confidence thresholds by content type (different evidence bars for different claim types)

### Category 4 — Core questions

**Q4.1 — What sources does the team trust most, and why?**

Ask this because trust is not uniform. The team trusts some sources because they have been vetted, some because they are recent, some because a specific person produced them, and some out of habit. The system needs to know which sources carry governing weight and which are merely familiar.

Listen for: "The approved claims list — it's been through legal." "Product marketing's ICPs — they do the research." "The brand guide — it's what we agreed to." "Sarah's competitive notes — she's always right." "The analytics dashboard — numbers don't lie."

This becomes: Source-trust hierarchy. Authority-level metadata per source. Retrieval-weighting rules that rank authoritative sources above anecdotal ones.

**Q4.2 — What sources does the team use but not fully trust?**

Ask this because many workflows run on sources the team knows are imperfect. Competitive intel that is three months old. An ICP built from intuition rather than research. Customer anecdotes that are vivid but not representative. The system should surface these sources but mark them as advisory, not governing.

Listen for: "The competitive battlecard is useful but probably out of date." "We use last quarter's campaign results but the sample was small." "The sales team's win/loss notes are helpful but not systematic." "The industry report is from an analyst we half-agree with."

This becomes: Advisory-source classification. Confidence markers on retrieved content. Uncertainty flags that distinguish "we have this" from "we trust this."

**Q4.3 — What evidence is required before a claim can be used in output?**

Ask this because some claims require formal evidence and some do not. A clinical-outcome claim requires an approved study. An ROI claim requires finance-validated data. A brand-voice statement requires the approved guide. A general product description may require only product documentation. The system needs claim-type-specific evidence bars.

Listen for: "Clinical outcomes need the approved study." "ROI claims need finance sign-off." "Customer quotes need a signed release." "Product capabilities need the current feature sheet." "General positioning just needs the messaging doc."

This becomes: Evidence-requirement rules per claim type. Pre-draft blocking conditions for claims that lack required evidence. The link between claim taxonomy and evidence taxonomy.

**Q4.4 — What signals are useful but should not be treated as authoritative?**

Ask this because signals inform strategy without governing claims. A spike in webinar registrations suggests interest but does not confirm buying intent. A customer anecdote suggests a pain point but does not validate a market trend. A competitor's press release signals direction but does not confirm capability. The system should retrieve these signals without promoting them to evidence.

Listen for: "Webinar attendance tells us something but it's not pipeline." "A customer said they love the integration, but that's one account." "The competitor announced a feature but we don't know if it ships." "Social engagement is a signal, not a result."

This becomes: Signal-type classification. Retrieval rules that surface signals as context without citing them as evidence. Confidence-display rules that show signals differently from evidence.

**Q4.5 — Where do people disagree about what evidence means?**

Ask this because disagreement about evidence is where the team's reasoning is most fragile. Marketing reads a case study as proof of product-market fit; product reads it as an outlier. Sales interprets engagement as buying intent; marketing interprets it as awareness. These disagreements should be surfaced and preserved, not silently resolved by the system.

Listen for: "Marketing thinks the webinar proves demand. Sales thinks it proves curiosity." "Product marketing says the case study is representative. The data team says the sample is too small." "We disagree about whether compliance-led messaging works better or just feels safer."

This becomes: Confidence-dispute inventory. Fields where the system should display competing interpretations rather than a single answer. Premise Stack candidates (assumptions that shape how evidence is read).

**Q4.6 — How should the system show confidence to the human reviewer?**

Ask this because confidence display shapes human behavior. If the system presents all output with equal confidence, the reviewer cannot prioritize what to check. If the system shows confidence scores without explanation, the reviewer cannot evaluate whether the score is meaningful. The display must be honest, interpretable, and actionable.

Listen for: "Show me where the evidence is strong and where it's thin." "Don't just give me a number — tell me why." "Flag the parts that are based on assumptions versus the parts based on data." "I want to see the sources, not just the output."

This becomes: Confidence-display requirements. Source-citation display format. Uncertainty-marker design. The difference between "the system is confident" and "the evidence supports this."

**Q4.7 — What should lower the system's confidence in a piece of content?**

Ask this because confidence should degrade under known conditions. Staleness lowers confidence: a source reviewed six months ago is less trustworthy than one reviewed last week. Anecdotal sourcing lowers confidence: a single customer story is not a market trend. Conflicting evidence lowers confidence: two authoritative sources that disagree should not produce a high-confidence output.

Listen for: "If the source is more than 90 days old, flag it." "If it's based on one customer, say so." "If two sources disagree, don't just pick one." "If the claim has no citation, it should show low confidence."

This becomes: Confidence-degradation rules. Staleness-based confidence adjustments. Source-count thresholds. Conflict-detection triggers.

**Q4.8 — What should happen when trusted sources disagree with each other?**

Ask this because source conflict is where premature sufficiency is most tempting. The system will want to pick one source and proceed. But if the approved claims list says one thing and the product documentation says another, the system should surface the conflict rather than resolve it silently.

Listen for: "If the brand guide and the product sheet disagree, flag it for brand." "If the ICP says one thing and the sales team says another, show both." "If two approved claims contradict each other, route to compliance." "Never silently pick one over the other."

This becomes: Source-conflict handling rules. Escalation triggers for conflicting authoritative sources. Display rules that show both sides rather than resolving silently.

**Q4.9 — What evidence should be visible to the human reviewer at decision time?**

Ask this because reviewers cannot govern what they cannot see. If the system drafts a claim and the reviewer cannot see what evidence supported it, the reviewer is approving based on fluency, not grounding. The system must make evidence visible, not just available.

Listen for: "I need to see which approved claim was used." "Show me the ICP it's targeting." "Show me the competitive source it's referencing." "I want to see what's cited and what's not cited."

This becomes: Evidence-display requirements at review time. Citation-visibility rules. The reviewer's information surface — what must be shown, not just stored.

**Q4.10 — How should evidence standards differ by content type?**

Ask this because not all content carries equal risk. A healthcare campaign brief requires clinical-grade evidence for outcome claims. An internal sales enablement doc requires accurate product information but not regulatory-grade sourcing. A social media post requires brand-voice compliance but not legal review of every sentence. The evidence bar should match the content risk.

Listen for: "Healthcare content needs the highest evidence bar." "Internal docs need accuracy but not legal sign-off." "Social posts need brand compliance but not clinical review." "Competitive content needs current data but not the same rigor as a regulatory claim."

This becomes: Evidence-requirement tiers by content type. Risk-weighted governance levels. Different confidence thresholds for different output categories.

### Category 4 — Follow-up probes

- "Walk me through a recent disagreement about whether evidence was strong enough. How was it resolved?"
- "What source has the team relied on that turned out to be wrong? What happened?"
- "If the system showed you a confidence score of 0.6, what would you do with that information?"
- "What would make you distrust something the system produced?"

### Category 4 — What good answers contain

- Named sources with trust levels and reasons for trust
- Specific claim types with specific evidence requirements
- Concrete examples of evidence disagreements within the team
- Clear preferences for how confidence should be displayed
- Named conditions that should lower confidence
- Stories about when the team trusted something it should not have

### Category 4 — What weak answers look like

- "We trust everything in the KB." (No you don't. Some of it is stale, some is anecdotal, some is disputed.)
- "The AI should figure out what's trustworthy." (The AI cannot determine trust without authority metadata and evidence-requirement rules.)
- "Confidence scores will confuse people." (Then design the display differently. The absence of confidence information is not the same as the absence of uncertainty.)
- "We don't have disagreements about evidence." (Then you have not looked closely enough. Every team has evidence disputes — they are often just unspoken.)

### Category 4 — What this informs in the system

- Source-trust hierarchy and authority-level metadata
- Evidence-requirement rules per claim type
- Confidence-display design (what the reviewer sees)
- Retrieval-weighting rules (how authority affects ranking)
- Uncertainty markers and confidence-degradation rules
- Source-conflict detection and escalation logic
- Provenance and citation-visibility requirements
- Evidence-standard tiers by content type

### Category 4 — What this feeds in the HLD

- Section 6: Reasoning-relevant retrieval — confidence weighting, authority ranking, source-conflict detection
- Section 3: Six-object data model — confidence fields on Premise Stack, Decision State, and Investigation Trace
- Section 10: Governance and observability — evidence-requirement enforcement, provenance audit, confidence-display rules

### Category 4 — Case-study observations to preserve

While asking these questions, note:

- How many distinct trust levels does the team actually use? (Often fewer than they think — "trusted" and "not trusted" with little in between.)
- What sources does the team rely on despite knowing they are imperfect? (This reveals where the workflow tolerates uncertainty.)
- How does the team currently resolve evidence disagreements? (Often: the loudest voice wins, or the question is deferred indefinitely.)
- Has the team ever been harmed by trusting a source that was stale or wrong? (Capture the story — it grounds the evidence-requirement rules.)
- Does the team currently see evidence when reviewing AI output, or only the output itself? (Usually: only the output.)

---

## Category 5: Assumptions / Premises

### Category 5 — Purpose

Surface working beliefs that shape the decision but are often unstated, copied forward, or treated as obvious. Every workflow runs on assumptions — about the audience, the market, the product, the competition, the evidence, and the organization itself. Most of these assumptions are never written down. Many are inherited from prior campaigns without re-examination. Some are risky if wrong. This category produces the inputs for the Premise Stack: the structured record of what was assumed, why, by whom, with what confidence, and under what conditions the assumption should be re-examined.

### Category 5 — Build output produced

- Premise inventory (all assumptions currently shaping the workflow)
- Premise Stack schema inputs (fields, types, required metadata)
- Assumption-capture logic (when and how assumptions are recorded)
- Confidence markers (how confident the team is in each assumption)
- Evidence links (what evidence supports or contradicts each assumption)
- Premise source (where the assumption came from — data, experience, inheritance, convention)
- Premise owner (who stated or confirmed the assumption)
- Re-examination triggers (what should cause the team to revisit an assumption)
- Premise expiry / review conditions (when an assumption should be rechecked or retired)
- Assumption-risk map (which assumptions create the most risk if wrong)

### Category 5 — Core questions

**Q5.1 — What are we acting as though we already know?**

Ask this because the most dangerous assumptions are the ones that feel like facts. The team "knows" who the buyer is, "knows" what messaging works, "knows" what the competition cannot do. These beliefs shape every downstream decision. If they are wrong, every downstream decision inherits the error — and the system will reproduce it unless the assumptions are surfaced and marked.

Listen for: "We know healthcare buyers care about compliance." "We know workflow burden is the top pain point." "We know our main competitor can't do real-time data." "We know engagement-driven CTAs outperform feature-driven ones."

This becomes: Premise inventory. The first pass at the Premise Stack. Each statement becomes a candidate premise with a confidence marker.

**Q5.2 — Which assumptions shape this brief or workflow right now?**

Ask this because assumptions are often invisible until you trace the reasoning backward. The brief targets a specific audience — why that audience? The messaging leads with compliance — why compliance? The CTA uses "see a demo" — why not "read the case study"? Each of these choices rests on an assumption that may or may not be examined.

Listen for: "We target IT directors because that's who we've always targeted." "We lead with compliance because healthcare buyers are risk-averse." "We use demo CTAs because the sales team wants meetings." "We avoid mentioning price because the product is expensive."

This becomes: Per-brief assumption list. Links between brief fields and the assumptions behind them. Premise Stack entries that tie to specific decision points.

**Q5.3 — Which assumptions came from evidence, and which from experience or convention?**

Ask this because evidence-backed assumptions and experience-backed assumptions deserve different confidence levels. "Compliance-led messaging converts better" backed by A/B test data is different from "compliance-led messaging converts better" backed by "that's what the VP said last year." Both may be correct, but the system should mark the difference.

Listen for: "We tested that — compliance-led outperformed by 15%." "That's what the sales team tells us." "We've always done it that way." "There was a study but I'm not sure it's still relevant." "That came from the industry report."

This becomes: Evidence-link field in the Premise Stack. Confidence markers differentiated by source type (tested / observed / reported / inherited / assumed).

**Q5.4 — Which assumptions are copied from prior work without being re-examined?**

Ask this because copied-forward assumptions are where stale reasoning enters the current cycle disguised as current knowledge. The audience section from last quarter's brief becomes this quarter's starting point. The competitive positioning from six months ago becomes today's differentiation. The assumption that "workflow burden is a buying signal" persists because nobody has asked whether it is still true.

Listen for: "We copied the audience section from the last campaign." "The competitive positioning hasn't been updated since Q1." "We've been using the same ICP for two years." "That messaging framework came from the old marketing lead."

This becomes: Staleness flags on inherited premises. Re-examination prompts in the Discovery flow. Premise Stack entries with an "inherited" source marker and a review trigger.

**Q5.5 — Which assumptions are risky if wrong?**

Ask this because not all assumptions carry equal risk. Assuming the wrong audience for an internal enablement doc wastes time. Assuming the wrong evidence standard for a healthcare campaign creates regulatory exposure. The system should know which assumptions are high-stakes and treat them with more scrutiny.

Listen for: "If the compliance assumption is wrong, we could get flagged by legal." "If the audience assumption is wrong, the campaign just underperforms." "If the competitive claim is wrong, we could damage a partner relationship." "If we assume the ICP is current but it's not, we target the wrong buyers for a quarter."

This becomes: Assumption-risk map. Risk-weighted review priorities. Premises that require evidence before the system uses them versus premises that can proceed with lower confidence.

**Q5.6 — Which assumptions should be tested before the team acts on them?**

Ask this because some assumptions are testable and should be tested before they shape a campaign. "Compliance-led messaging outperforms feature-led messaging" is testable. "Healthcare buyers respond to ROI arguments" is testable. If the assumption is testable and the stakes are high, the system should flag it as a test candidate rather than treating it as settled.

Listen for: "We should probably A/B test that." "We've never actually validated that assumption." "The data might exist but nobody's looked." "We could run a small test before committing the full campaign."

This becomes: Test-candidate flags on high-stakes premises. Pre-campaign validation requirements. Links between Premise Stack entries and potential Learning Events.

**Q5.7 — Which assumptions should be preserved into the next cycle?**

Ask this because not all assumptions are temporary. Some represent hard-won organizational knowledge that should persist across campaigns: "In healthcare, always lead with compliance before features." "In K-12, avoid fear-based messaging about school safety." These are durable premises that should be available to the next cycle without being re-discovered.

Listen for: "That's a lesson we learned the hard way." "That assumption has been validated across multiple campaigns." "That's our positioning — it shouldn't change campaign to campaign." "The compliance boundary is stable — it doesn't need re-examination every time."

This becomes: Premise durability classification (durable / campaign-specific / experimental). Durable premises that persist in the KB. Campaign-specific premises that are captured but not generalized.

**Q5.8 — Which assumptions should expire or be rechecked on a schedule?**

Ask this because assumptions age. A competitive positioning assumption that was accurate six months ago may not hold after a competitor's product launch. An ICP assumption validated by last year's data may not reflect this year's market. The system should know which assumptions need periodic re-examination and trigger review when they age past their window.

Listen for: "The competitive positioning should be rechecked every quarter." "The ICP should be reviewed annually." "The messaging framework should be revisited after every major product release." "The compliance boundaries should be rechecked when regulations change."

This becomes: Premise expiry / review conditions. Review-cadence specifications per premise type. Staleness-triggered re-examination prompts.

**Q5.9 — What would change if a key assumption turned out to be false?**

Ask this because this question reveals the downstream impact of each assumption. If "workflow burden is a buying signal" turns out to be wrong, every campaign targeting that pain point is misaligned. If "healthcare buyers are compliance-first" turns out to be wrong, the entire messaging hierarchy needs restructuring. The system should know which assumptions, if falsified, would require the largest course corrections.

Listen for: "If that's wrong, we've been targeting the wrong pain point for a year." "If compliance isn't the top concern, our whole healthcare approach changes." "If the ICP is wrong, the last three campaigns were aimed at the wrong people." "If that competitive claim is wrong, we need to pull the battlecard."

This becomes: Impact-assessment field in the Premise Stack. High-impact premises that receive more scrutiny. The link between premise falsification and Learning Events.

**Q5.10 — Who stated or confirmed each key assumption?**

Ask this because ownership matters for accountability and re-examination. An assumption stated by the VP of Product Marketing carries different weight than one inherited from a departed employee. An assumption confirmed by data analysis carries different weight than one confirmed by "everyone just knows." The system should record who owns each premise so that re-examination has a responsible party.

Listen for: "That came from the CMO." "The data team validated that." "I think the old marketing lead said that." "Nobody specifically — it's just how we do things." "The sales team insists on that assumption."

This becomes: Premise-owner field in the Premise Stack. Ownership-based review routing. Orphaned-premise detection (assumptions with no current owner).

### Category 5 — Follow-up probes

- "If I asked the team to list their top five assumptions about this workflow, would they agree?"
- "What assumption has the team been wrong about before? What happened?"
- "What would you need to see to change your mind about a core assumption?"
- "Which assumptions would a new team member question that the current team takes for granted?"

### Category 5 — What good answers contain

- Named assumptions with stated confidence levels
- Clear distinction between evidence-backed and experience-backed beliefs
- Specific examples of assumptions that were copied forward without re-examination
- Named owners or explicit gaps ("nobody owns that assumption")
- Concrete impact statements ("if this is wrong, then X changes")
- Identified assumptions that are testable but untested

### Category 5 — What weak answers look like

- "We don't have assumptions — we have data." (Every team has assumptions. Data is interpreted through assumptions.)
- "Our assumptions are all validated." (By whom? When? Under what conditions? Validation has a shelf life.)
- "We don't need to write them down — everyone knows them." (If everyone knows them, they should be easy to write down. If they are not easy to write down, everyone does not actually agree.)
- "Assumptions don't change." (They do. Markets shift. Products evolve. Competitors move. Assumptions that do not change are assumptions that have not been re-examined.)

### Category 5 — What this informs in the system

- Premise Stack schema (fields, types, confidence markers, evidence links, owners)
- Assumption-capture logic (when and how premises are recorded during Discovery)
- Confidence differentiation by source type (tested / observed / reported / inherited / assumed)
- Staleness flags and re-examination triggers for inherited premises
- Assumption-risk map and risk-weighted review priorities
- Premise durability classification (durable / campaign-specific / experimental)
- Premise expiry and review-cadence specifications
- Orphaned-premise detection

### Category 5 — What this feeds in the HLD

- Section 3: Six-object data model — Premise Stack schema, confidence fields, evidence links, owner fields, expiry conditions
- Section 6: Reasoning-relevant retrieval — premise-relevant retrieval, surfacing prior premises that apply to the current decision
- Section 7: Learning-loop architecture — which premise failed, linking Learning Events to Premise Stack entries

### Category 5 — Case-study observations to preserve

While asking these questions, note:

- How many assumptions can the team name without prompting? (Usually fewer than are actually operating.)
- How many assumptions are inherited from prior work versus generated fresh for this cycle?
- Does the team distinguish between evidence-backed and experience-backed assumptions? (Often they do not.)
- What assumptions has the team been wrong about before, and did the lesson persist? (This is the learning-loop question applied to premises.)
- How does the team currently record or communicate assumptions? (Usually: they don't. The assumption lives in someone's head or in the structure of the brief itself.)

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

### Category 8 — Purpose

Identify what reasoning must survive from one cycle to the next. Every decision rests on goals, constraints, assumptions, evidence, alternatives, and judgments — and in most workflows, all of this disappears the moment the decision is made. The brief is approved. The campaign launches. The reasoning behind it evaporates. When the next cycle starts, the team rebuilds from scratch because the system preserved the output but not the thinking.

This category translates workflow discovery into the six-object reasoning architecture. It defines which reasoning objects are captured, with what fields, at what granularity, and under what conditions. It produces the reasoning-state preservation scope for the workflow.

### Category 8 — Build output produced

- Reasoning-state preservation scope (which of the six reasoning objects are captured for this workflow)
- Minimum viable reasoning record (the smallest useful reasoning capture per decision)
- Optimizer State fields (goal, policy, interpretation snapshot at decision time)
- Premise Stack fields (assumptions, confidence, evidence links, owners)
- Decision State fields (chosen action, alternatives considered, sufficiency justification)
- Investigation Trace fields (what was retrieved, what was checked, what was missing)
- Learning Event links (what outcome data connects back to this decision)
- MUO links (what prior lessons were applied to this decision)
- Capture triggers (when reasoning-state capture occurs in the workflow)
- Preservation boundaries (what is worth preserving versus what is transient)
- Retention requirements (how long reasoning records must be kept)
- Reasoning-state display requirements (what the next cycle's user should see)

### Category 8 — Core questions

**Q8.1 — What should someone understand later about why this decision was made?**

Ask this because this is the meta-question for reasoning preservation. If someone reviews this campaign brief six months from now — or if the system starts the next campaign in the same vertical — what must they understand about the reasoning behind this one? Not what was decided, but why.

Listen for: "They should know why we chose compliance-led messaging over feature-led." "They should know we avoided the readmissions claim because of evidence gaps." "They should know the audience was narrowed to IT directors based on the sales team's input." "They should know we rejected the competitive comparison because the data was stale."

This becomes: The scope of the reasoning record. The fields that matter most. The difference between preserving the decision and preserving the reasoning.

**Q8.2 — What goal shaped this decision?**

Ask this because the goal is the first element of the Optimizer State. Without the goal, later reviewers cannot tell whether the decision was good or bad — only whether the output existed. "Increase qualified pipeline in healthcare" produces different reasoning than "raise brand awareness in K-12." The goal must be preserved alongside the decision.

Listen for: "The goal was to generate qualified demo requests from healthcare IT directors." "The goal was to position the product as compliance-first for HIPAA-sensitive buyers." "The goal was to re-engage lapsed accounts in the enterprise segment."

This becomes: Goal field in the Optimizer State record. The anchor against which the decision's reasoning is evaluated.

**Q8.3 — What constraints shaped the decision?**

Ask this because constraints explain why the decision took the shape it did. Budget limits, timeline pressure, compliance boundaries, brand rules, channel restrictions, and resource availability all shape the output. If the constraints are not preserved, later reviewers will wonder why the team did not do something that was, in fact, impossible at the time.

Listen for: "We had two weeks, so we couldn't do original research." "Compliance said no clinical-outcome claims without the study." "Budget only covered email and social — no events." "The product team said the feature wouldn't ship until Q3." "Brand said no fear-based messaging for K-12."

This becomes: Constraint fields in the Optimizer State. Policy references in the reasoning record. The link between governance rules and the specific decisions they shaped.

**Q8.4 — What assumptions shaped the decision?**

Ask this because assumptions are the most fragile part of the reasoning. The team assumed the ICP was current. The team assumed compliance-led messaging converts better. The team assumed the competitor's product does not support real-time data. If any of these assumptions turns out to be wrong, the decision needs to be revisited — but only if the assumptions were recorded.

Listen for: "We assumed the healthcare ICP was still accurate." "We assumed compliance-first messaging would outperform feature-first." "We assumed the competitive battlecard was current." "We assumed demo requests are a better signal than whitepaper downloads."

This becomes: Premise Stack entries linked to the Decision State. The connection between what was assumed and what was decided. The foundation for learning when an assumption is falsified.

**Q8.5 — What evidence was checked before the decision was made?**

Ask this because the evidence trail distinguishes a grounded decision from a fluent guess. If the team checked the approved claims list, retrieved the current ICP, reviewed the competitive battlecard, and consulted the prior campaign's results, that trail should be preserved. If they did not, that absence should also be visible.

Listen for: "We checked the approved claims list." "We pulled the healthcare ICP." "We reviewed last quarter's campaign performance." "We looked at the competitive positioning but it was outdated." "We didn't check anything — we just drafted."

This becomes: Investigation Trace fields. The record of what was retrieved, what was consulted, and what was available but not used. The evidence surface at decision time.

**Q8.6 — What evidence was missing or unavailable?**

Ask this because missing evidence is as important as present evidence. If the team could not find an approved claim for a specific outcome, that gap shaped the decision. If the competitive intelligence was stale, that absence constrained the positioning. Missing evidence should be recorded so the next cycle knows what to look for.

Listen for: "We didn't have an approved study for the readmissions claim." "The competitive data was six months old." "We had no campaign performance data for K-12." "The ICP for the new vertical hasn't been built yet." "We couldn't find the customer quote release."

This becomes: Evidence-gap fields in the Investigation Trace. Missing-information records. Inputs to the learning loop (what should be available next time that was not available this time).

**Q8.7 — What alternatives were considered or rejected?**

Ask this because rejected alternatives carry reasoning that is valuable for the next cycle. The team considered a feature-led approach and rejected it because of compliance risk. The team considered targeting CIOs and rejected it because the sales team said IT directors hold budget authority. These rejected paths prevent the next cycle from re-exploring options that were already evaluated.

Listen for: "We considered leading with ROI but couldn't support the claim." "We thought about targeting CIOs but sales said IT directors are the buyers." "We looked at a fear-based angle for K-12 but brand rejected it." "We considered a competitive comparison but the data was too stale."

This becomes: Alternatives-considered fields in the Decision State. Rejection reasons. The reasoning record that prevents the next cycle from repeating the same exploration.

**Q8.8 — What made the answer feel sufficient?**

Ask this because this is the sufficiency record — the reasoning behind the stopping decision. The team decided the brief was good enough. Why? Because all required fields were present? Because compliance reviewed the claims? Because the deadline arrived? Because the draft sounded professional? The sufficiency justification should be preserved so the next cycle can evaluate whether the stopping condition was appropriate.

Listen for: "Compliance signed off on the claims." "All the required sections were filled in." "We ran out of time." "It matched the template." "The draft sounded good and nobody objected." "We hit all the quality-gate thresholds."

This becomes: Sufficiency-justification field in the Decision State. The distinction between evidence-grounded sufficiency and time-pressured sufficiency. An input to the learning loop (was the stopping condition appropriate given the outcome?).

**Q8.9 — What human judgment changed the system's interpretation or output?**

Ask this because human overrides, corrections, and refinements are reasoning that the system cannot generate on its own. When a compliance officer changes a claim, when a brand lead adjusts the tone, when a campaign manager narrows the audience — these human interventions carry reasoning that should be preserved. Otherwise, the system will reproduce the pre-correction version next time.

Listen for: "Compliance changed the claim language." "Cassidy narrowed the audience from the system's suggestion." "The brand team softened the CTA." "The sales team added context the system didn't have." "I rewrote the positioning because the AI version was generic."

This becomes: Human-override records. Correction traces. The link between system output and human refinement. Training signal for the next cycle's Discovery flow.

**Q8.10 — What should be available to the next cycle that is not available today?**

Ask this because this question defines the preservation target. If the next campaign in this vertical should start with the current campaign's reasoning — the goal, the constraints, the assumptions, the evidence gaps, the rejected alternatives, the sufficiency justification — then those are the fields that must survive.

Listen for: "Next time, the team should know we avoided the readmissions claim and why." "Next time, the system should start with this campaign's lessons." "Next time, the brief should know which assumptions were tested and which were inherited." "Next time, the ICP should reflect what we learned from this campaign's results."

This becomes: Reasoning-state preservation scope. The minimum viable reasoning record. The fields, objects, and links that must persist from this cycle to the next.

### Category 8 — Follow-up probes

- "Walk me through a decision from last quarter. If you had to explain why you made it today, could you? Where would you look?"
- "What reasoning has been lost when a team member left or a project ended?"
- "If the system showed you the reasoning behind a prior campaign's brief, what would you want to see?"
- "What would change about the next campaign if the reasoning from this one were fully preserved?"

### Category 8 — What good answers contain

- Specific examples of reasoning that has been lost ("we don't know why we avoided that claim last time")
- Named fields or sections where reasoning currently disappears
- Clear statements about what the next cycle should inherit
- Concrete examples of human judgment that changed the output
- Distinction between output preservation (we kept the brief) and reasoning preservation (we kept the why)

### Category 8 — What weak answers look like

- "We keep all our briefs in Google Drive." (Preserving the output is not preserving the reasoning. The brief records what was decided, not why.)
- "The team remembers." (The team changes. Memory is not architecture.)
- "We'll just re-derive it." (Re-derivation is expensive, error-prone, and produces different reasoning each time. That is why the same mistakes recur.)
- "We don't need to preserve reasoning — the AI will figure it out." (The AI has no memory of prior reasoning unless the system preserves it. Without preservation, every cycle starts cold.)

### Category 8 — What this informs in the system

- Reasoning-state preservation scope (which objects, which fields, which granularity)
- Minimum viable reasoning record per decision
- Optimizer State schema (goal, policy, interpretation)
- Premise Stack schema (assumptions, confidence, evidence links, owners)
- Decision State schema (chosen action, alternatives, sufficiency justification)
- Investigation Trace schema (retrieved sources, checked evidence, missing evidence)
- Learning Event and MUO links
- Capture triggers (when in the workflow reasoning is recorded)
- Retention and versioning requirements
- Reasoning-state display for next-cycle users

### Category 8 — What this feeds in the HLD

- Section 3: Six-object data model — all objects (Optimizer State, Premise Stack, Decision State, Investigation Trace, Learning Event, Model Update Object)
- Section 5: Discovery / RIPC — what reasoning is captured during the confirmation stage of the loop
- Section 8: State lifecycle — retention rules, versioning, reasoning-state transitions

### Category 8 — Case-study observations to preserve

While asking these questions, note:

- What reasoning currently survives from one cycle to the next? (Usually: almost none. The output survives. The reasoning does not.)
- How does the team currently reconstruct prior reasoning? (Usually: they ask the person who was involved, if that person is still available.)
- What decisions have been revisited because nobody remembered the original reasoning?
- What human corrections have been made that the system should learn from but currently cannot?
- How much of the current workflow's reasoning lives in someone's head versus in a persistent record?

---

## Category 9: Learning Loop

### Category 9 — Purpose

Define how outcomes become learning and how learning changes future reasoning. Most organizations believe they learn from experience. They run retrospectives, store campaign analytics, and write postmortems. But storing a postmortem is not learning. Storing campaign analytics is not learning. These are records of what happened — not instructions that change what happens next.

Learning occurs when a bounded outcome changes the reasoning that would otherwise reproduce the same mistake. The output of learning should be specific enough to become a Model Update Object candidate: a scoped, evidence-backed change to the system's knowledge, premises, or governance rules that applies under defined conditions and does not apply outside them.

This category prevents "lessons learned" from being vague, disconnected summaries that nobody retrieves. It produces Learning Event and MUO specifications that connect outcomes to the reasoning they should change.

### Category 9 — Build output produced

- Learning Event schema (what fields a learning record must contain)
- MUO candidate schema (what fields a Model Update Object must contain)
- Outcome-capture requirements (what outcome data must be recorded for this workflow)
- Prediction-error triggers (what results indicate a premise or assumption was wrong)
- Applicability-boundary fields (where the lesson applies and where it does not)
- Confidence-update rules (how new evidence changes confidence in existing premises)
- Review / confirmation workflow (who confirms the lesson is valid before it enters the system)
- Learning-to-KB workflow (how a confirmed lesson updates the knowledge base)
- Learning-to-reasoning-state workflow (how a confirmed lesson changes future Premise Stacks, Optimizer States, or governance rules)
- Effectiveness signal (how the system knows the next cycle actually started smarter)

### Category 9 — Core questions

**Q9.1 — What outcome data matters for this workflow?**

Ask this because learning requires outcome data, and outcome data must be defined before the campaign runs — not after. If the team does not decide in advance what results to track, the learning loop has nothing to process. The relevant outcomes depend on the workflow: campaign performance, compliance flags, downstream rework, pipeline contribution, audience engagement by segment, or content reuse rates.

Listen for: "Click-through rates by segment." "Qualified pipeline generated." "Compliance rejection rate." "Time from brief to approved assets." "How often downstream teams asked for clarification." "Which proof points outperformed which product descriptions."

This becomes: Outcome-capture requirements. The data fields that must be recorded at workflow completion. The input to the Learning Event schema.

**Q9.2 — What result would tell us an assumption was wrong?**

Ask this because this question turns assumptions into testable predictions. If the team assumed "compliance-led messaging converts better than feature-led," a campaign where feature-led messaging outperforms compliance-led messaging is a prediction error. The system should detect these errors automatically when the outcome data arrives.

Listen for: "If feature-led outperforms compliance-led, our messaging hierarchy is wrong." "If IT directors don't convert, our ICP assumption is wrong." "If the competitive comparison gets no engagement, the positioning is stale." "If the demo CTA underperforms the whitepaper CTA, our funnel assumption is wrong."

This becomes: Prediction-error triggers. Links between Premise Stack entries and the outcomes that would falsify them. Automatic detection of assumptions that need re-examination.

**Q9.3 — What did the team expect to happen?**

Ask this because learning requires a prediction to compare against. If the team expected a 2% CTR and got 4%, that is a positive surprise worth understanding. If the team expected compliance-led messaging to win and feature-led messaging won instead, that is a premise falsification worth recording. Without the prediction, the outcome is just a number — it cannot become learning.

Listen for: "We expected about a 2% CTR based on the last healthcare campaign." "We expected compliance-led to outperform feature-led." "We expected IT directors to convert at a higher rate than CIOs." "We expected the proof-point-led version to win."

This becomes: Pre-campaign prediction records. The baseline against which outcomes are measured. The foundation for prediction-error detection.

**Q9.4 — What actually happened, and how does it compare to the prediction?**

Ask this because the comparison between prediction and outcome is where learning begins. A campaign that met expectations confirms current reasoning. A campaign that exceeded or fell short of expectations signals that something in the reasoning — the ICP, the messaging hierarchy, the evidence, the governance rules — may need updating.

Listen for: "The CTR was 3.5% — higher than expected." "Compliance-led and feature-led performed about the same." "IT directors converted but CIOs actually had higher deal sizes." "The proof-point version outperformed the product-description version by 40%."

This becomes: Outcome-versus-prediction comparison. The raw material for Learning Event creation. The evidence that supports or challenges current premises.

**Q9.5 — What should change next time based on what happened?**

Ask this because this is the moment where an outcome becomes a lesson. The question is not "what happened?" but "what should be different?" If proof points outperformed product descriptions, the next brief should lead with proof points. If compliance-led and feature-led performed equally, the team's messaging hierarchy assumption needs re-examination. The answer to this question becomes a MUO candidate.

Listen for: "Next time, lead with proof points, not product descriptions." "Next time, test both messaging approaches instead of assuming compliance-led wins." "Next time, include CIOs in the targeting — they convert at higher deal sizes." "Next time, use the updated competitive positioning — the old one got no engagement."

This becomes: MUO candidate content. The specific, bounded change to reasoning that should persist. The lesson that must be scoped, confirmed, and applied.

**Q9.6 — What should NOT be generalized beyond this case?**

Ask this because over-generalization is the most common failure mode of learning. A lesson that worked for healthcare may not apply to K-12. A messaging approach that worked for one product may not work for another. A competitive positioning that worked against one competitor may not work against a different one. Every lesson needs an applicability boundary.

Listen for: "That worked for healthcare but probably doesn't apply to enterprise." "That was specific to the compliance buyer — the IT buyer is different." "That competitive positioning only applies to Carbyne, not to the other competitors." "That CTR is from email only — we can't assume it applies to social."

This becomes: Applicability-boundary fields in the MUO schema. Scope constraints on learning. The difference between "this worked" and "this works everywhere."

**Q9.7 — Who confirms that the lesson is valid before it enters the system?**

Ask this because unconfirmed lessons are dangerous. A single campaign result is not a validated lesson. A team's interpretation of why something worked may be wrong. A lesson based on a small sample may not generalize. Someone with authority and context must confirm the lesson before it changes the system's reasoning.

Listen for: "The campaign manager confirms the interpretation." "Product marketing validates the ICP change." "Compliance reviews any change to claim rules." "The data team confirms the analytics are statistically meaningful." "Nobody confirms anything — we just remember it."

This becomes: Confirmation workflow in the MUO schema. Review-gate specifications for learning. The authority model for lesson validation.

**Q9.8 — Where should the confirmed lesson live in the system?**

Ask this because a lesson that lives in a postmortem document is a lesson nobody retrieves. A lesson that updates the Premise Stack is a lesson that shapes the next decision. A lesson that updates a governance rule is a lesson that changes the system's behavior. The question is: where does the lesson land so that it actually reaches the next cycle?

Listen for: "It should update the ICP." "It should change the messaging hierarchy." "It should add a new approved claim." "It should update the competitive battlecard." "It should change the sufficiency criteria for the next brief." "It should update the KB."

This becomes: Learning-to-KB workflow. Learning-to-reasoning-state workflow. The routing rules that determine where a confirmed lesson is applied. MUO target specification.

**Q9.9 — How does the lesson reach the next cycle?**

Ask this because the gap between "lesson exists" and "lesson is applied" is where most organizational learning fails. The lesson may be stored, but if the system does not retrieve it at the right moment in the next workflow, it might as well not exist. The lesson must be connected to the retrieval architecture so that it surfaces when the next relevant decision is being made.

Listen for: "The next healthcare brief should see this lesson automatically." "The system should surface the MUO when the same vertical comes up." "The next campaign targeting IT directors should know this." "It should be part of the retrieval context, not a separate document."

This becomes: MUO retrieval specifications. Applicability-matching rules. The connection between learning-loop output and reasoning-relevant retrieval. The mechanism that ensures the next cycle starts with the lesson, not without it.

**Q9.10 — How will we know the next cycle actually started smarter?**

Ask this because this is the effectiveness signal — the test of whether the learning loop works. If the next healthcare campaign avoids the readmissions-claim mistake, the lesson was applied. If the next brief leads with proof points instead of product descriptions, the MUO reached the system. If compliance flags fewer issues, the governance update worked. Without this signal, the team cannot distinguish a working learning loop from a learning loop that stores lessons nobody uses.

Listen for: "The next healthcare brief should not repeat the readmissions-claim error." "The next campaign should start with the proof-point lesson already loaded." "Compliance flags should decrease because the system already knows the boundaries." "The brief should be faster to produce because the system remembers what worked."

This becomes: Effectiveness signal. The prediction that makes the learning loop testable. The metric or observation that shows whether the next cycle improved.

### Category 9 — Follow-up probes

- "Tell me about a lesson your team learned from a campaign. Did it change the next campaign, or did the team re-learn it?"
- "Where do campaign learnings currently live? Who retrieves them?"
- "If the system said 'this lesson from the last healthcare campaign applies here — do you want to use it?', would that be helpful or annoying?"
- "What is the difference between a campaign analytics report and a lesson that changes behavior?"

### Category 9 — What good answers contain

- Named outcomes with prediction comparisons ("we expected X, got Y")
- Specific lessons with applicability boundaries ("this applies to healthcare but not enterprise")
- Named confirmation authorities ("product marketing validates ICP changes")
- Concrete examples of lessons that were learned but not applied in the next cycle
- Clear destination for where the lesson should live (KB, Premise Stack, governance rule)
- Observable effectiveness signals ("the next brief should not repeat this mistake")

### Category 9 — What weak answers look like

- "We do retrospectives." (Retrospectives are not learning. Learning is when the next cycle starts differently. Does it?)
- "We have campaign analytics." (Analytics are outcome data, not lessons. The data must be interpreted, scoped, confirmed, and routed before it becomes learning.)
- "The team remembers what worked." (Memory is not architecture. The team changes. Memory fades. The system must remember, not the people.)
- "We store everything in Confluence." (Storage is not retrieval. A lesson stored in Confluence that is not surfaced at the next decision point is a lesson that does not exist for the system.)
- "Lessons are obvious — we don't need a process." (If lessons were obvious, the same mistakes would not recur. They recur because the lesson is not connected to the next cycle's reasoning.)

### Category 9 — What this informs in the system

- Learning Event schema (outcome data, prediction comparison, premise links, interpretation)
- MUO candidate schema (lesson content, applicability boundary, confidence, confirmation status, target)
- Outcome-capture requirements (what data is recorded at workflow completion)
- Prediction-error detection logic (automatic comparison of outcome versus prediction)
- Applicability-boundary specifications (where a lesson applies and where it does not)
- Confirmation workflow (who validates the lesson before it enters the system)
- Learning-to-KB routing (how a confirmed lesson updates knowledge)
- Learning-to-reasoning-state routing (how a confirmed lesson changes Premise Stacks, governance, or sufficiency)
- Effectiveness signal (the test of whether the learning loop works)

### Category 9 — What this feeds in the HLD

- Section 7: Learning-loop architecture — Learning Event creation, MUO lifecycle, confirmation workflow, evidence-supported model change
- Section 3: Six-object data model — Learning Event schema, MUO schema, links to Premise Stack and Decision State
- Section 6: Reasoning-relevant retrieval — MUO retrieval, applicability matching, surfacing prior lessons at decision time
- Section 13: Minimal viable implementation — learning-loop scope for the first build, minimum viable MUO

### Category 9 — Case-study observations to preserve

While asking these questions, note:

- Does the team currently distinguish between outcome data and lessons? (Usually: they don't. Campaign analytics are treated as learning, but they are not connected to future reasoning.)
- How many lessons from the last cycle actually changed the next cycle's behavior? (Usually: very few. The lesson was "learned" but not applied.)
- Where do lessons currently live? (Postmortems, slide decks, someone's memory, a Confluence page nobody reads.)
- Has the team ever re-made a mistake that a prior cycle had already identified? (Capture the story — it is the strongest argument for the learning loop.)
- Does anyone currently confirm whether a lesson is valid before it is generalized? (Usually: no. The loudest interpretation wins.)

---

## Category 10: Retrieval Relevance

### Category 10 — Purpose

Define how the system retrieves prior reasoning, not just similar text. Reasoning-relevant retrieval is not the same as semantic document retrieval. The most important prior reasoning may not use similar language — it may be relevant because it shares a goal, a policy boundary, an audience assumption, an unresolved uncertainty, a confidence limit, or a failure pattern. A prior healthcare campaign lesson about compliance-led CTAs underperforming may use completely different vocabulary than the current brief, yet it is the single most important piece of context the system should surface. If retrieval is limited to semantic similarity, the system will retrieve text that sounds like the current task while missing reasoning that matters for the current task.

### Category 10 — Build output produced

- Reasoning-relevance criteria (what makes prior reasoning relevant to a current decision)
- Retrieval metadata requirements (what fields must be indexed for reasoning-relevant retrieval)
- Applicability-boundary fields (what conditions must match before prior reasoning is surfaced)
- Match-rationale display (how the system explains why it retrieved something)
- Prior-reasoning surfacing logic (when and how the system surfaces prior reasoning during the workflow)
- Confidence/provenance display (how the system shows the origin, age, and confidence of retrieved reasoning)
- Retrieval filter requirements (how the system narrows retrieval beyond semantic similarity)
- False-analogy prevention rules (what should prevent the system from treating superficially similar reasoning as applicable)
- Reuse-confirmation requirements (what the human must confirm before prior reasoning is applied)
- Retrieval miss/gap logging requirements (what happens when the system finds no relevant prior reasoning)

### Category 10 — Core questions

**Q10.1 — What prior decisions should be retrievable for this workflow?**

Ask this because the system needs to know what counts as a prior decision worth surfacing. Not every past action is relevant. The system should retrieve prior decisions that share the current workflow's vertical, audience, goal type, or constraint profile — not just prior decisions that used similar words.

Listen for: "The last healthcare campaign brief." "Any campaign that targeted IT directors." "The brief where we dropped the readmissions claim." "Any campaign where compliance flagged something." "The last time we ran a competitive positioning campaign against Carbyne."

This becomes: Retrievable-decision scope. The types of prior reasoning records the system indexes for surfacing. The link between workflow attributes and retrieval targets.

**Q10.2 — What makes a prior decision relevant to a current decision?**

Ask this because relevance is not similarity. A prior campaign is relevant when it shares a goal (qualified pipeline in healthcare), an audience (IT directors at mid-market health systems), a constraint (compliance-restricted clinical claims), a failure pattern (premature sufficiency on audience assumptions), or a lesson (proof points outperformed product descriptions). The system must match on these reasoning dimensions, not just on text overlap.

Listen for: "It's relevant if it targeted the same buyer." "It's relevant if it ran into the same compliance issue." "It's relevant if it tested a similar messaging approach." "It's relevant if the same assumption was in play." "It's relevant because the same governance rules applied."

This becomes: Reasoning-relevance criteria. The matching dimensions the retrieval system uses beyond semantic similarity: goal type, audience, vertical, constraint profile, premise overlap, failure-pattern match, lesson applicability.

**Q10.3 — What metadata is needed to retrieve prior reasoning safely?**

Ask this because retrieval without metadata produces false matches. A prior campaign that looks relevant because it mentions "healthcare" may have targeted a different buyer, operated under different compliance rules, or been run before a major product change. The metadata must carry enough context to let the system — and the human — evaluate whether the match is genuine.

Listen for: "I need to know when it ran." "I need to know which vertical and audience." "I need to know what the goal was." "I need to know whether it was successful." "I need to know which compliance rules applied." "I need to know who owned the decision."

This becomes: Retrieval metadata requirements. The minimum metadata fields that must be indexed alongside reasoning records: date, vertical, audience, goal, outcome, compliance context, owner, confidence, lifecycle status.

**Q10.4 — What applicability boundaries should travel with prior reasoning?**

Ask this because a lesson without a boundary is a lesson that will be over-applied. "Proof points outperform product descriptions" may hold for healthcare email campaigns but not for enterprise webinar promotions. "Compliance-led CTAs underperform feature-led CTAs" may hold for mid-market health systems but not for large academic medical centers. The boundary must be part of the retrieval record, not a separate document the user must find.

Listen for: "That lesson was specific to healthcare." "That only applies to email, not social." "That was about the old product — the new one is different." "That worked for mid-market but enterprise is a different buyer." "That result was from a small sample — we're not sure it generalizes."

This becomes: Applicability-boundary fields on reasoning records and MUOs. Boundary-matching logic in the retrieval system. Display requirements that show the boundary alongside the retrieved reasoning.

**Q10.5 — What would make a prior lesson not apply to the current decision?**

Ask this because the system must know when to withhold, not just when to surface. A prior lesson may share the vertical but differ on audience. It may share the goal but differ on constraints. It may be from a period before a major product change, a market shift, or a regulatory update. The system should be able to identify and communicate non-applicability, not just applicability.

Listen for: "The product has changed since then." "The competitive landscape is different now." "That was before the compliance rules tightened." "The audience was different even though the vertical was the same." "That campaign had a much larger budget — the constraints were different."

This becomes: Non-applicability rules. Staleness-based retrieval suppression. Constraint-mismatch detection. The conditions under which the system retrieves a prior record but marks it as potentially non-applicable.

**Q10.6 — What should the system show when it retrieves prior reasoning?**

Ask this because the display determines whether retrieval is useful or disruptive. If the system shows only the prior decision without the reasoning behind it, the user cannot evaluate whether it applies. If the system shows the full reasoning record without summarizing why it was retrieved, the user drowns in context. The display must be: what was decided, why it was decided, why the system thinks it is relevant now, and what conditions might make it not apply.

Listen for: "Show me the lesson and why it was retrieved." "Show me what the prior campaign concluded and what evidence supported it." "Show me the applicability boundary." "Don't just dump the old brief — tell me what's relevant about it." "Show me where the conditions match and where they differ."

This becomes: Match-rationale display requirements. Prior-reasoning summary format. The retrieval-display pattern: decision + reasoning + match rationale + applicability boundary + confidence/provenance.

**Q10.7 — How should the system explain why it retrieved something?**

Ask this because opaque retrieval erodes trust. If the system surfaces a prior lesson without explaining why, the user cannot tell whether the match is genuine or accidental. "Retrieved because this campaign shares the same vertical, audience segment, and compliance constraints as the prior campaign that found proof-point-led messaging outperformed product-description-led messaging by 40%" is useful. "Here is a related campaign" is not.

Listen for: "Tell me why you're showing me this." "I need to know what the connection is." "Don't just show me something similar — explain the relevance." "If you can't explain why it's relevant, don't show it."

This becomes: Match-rationale generation requirements. Explanation fields in the retrieval display. The difference between "similar text found" and "relevant reasoning found because of shared goal, audience, and constraint profile."

**Q10.8 — What should happen when no relevant prior reasoning is found?**

Ask this because a retrieval miss is information, not a failure. If the system has no prior reasoning for a new vertical, a new audience, or a new campaign type, the user should know. "No prior campaigns targeting this audience were found" is useful because it tells the user that the current decision is being made without the benefit of prior reasoning — and that the current decision's reasoning should be preserved especially carefully for the next cycle.

Listen for: "Tell me if this is the first time we've done this." "I want to know if there's no prior data." "If nothing comes up, that's useful — it means we're starting from scratch." "Log the gap so we can fill it next time."

This becomes: Retrieval miss/gap logging requirements. Gap-notification display. The link between retrieval misses and reasoning-preservation priority (first-time decisions should have their reasoning captured with extra care).

**Q10.9 — What should happen when retrieved reasoning is similar but not applicable?**

Ask this because false analogy is the retrieval equivalent of premature sufficiency. The system finds a prior campaign that looks relevant but differs in a way that changes the conclusion. A healthcare campaign lesson about compliance-led CTAs may not apply to a government campaign with different regulatory constraints. If the system surfaces the prior reasoning without flagging the mismatch, the user may apply a lesson that does not hold.

Listen for: "The last campaign was healthcare but this one is government — different rules." "The prior lesson was for email but this is a webinar funnel." "The old competitive positioning was against Carbyne but this is against a new entrant." "The prior audience was mid-market but this is enterprise."

This becomes: False-analogy prevention rules. Boundary-mismatch detection and display. The distinction between "this was retrieved because it is similar" and "this was retrieved because it is applicable." Mismatch warnings that surface alongside retrieved reasoning.

**Q10.10 — What should the human confirm before prior reasoning is reused?**

Ask this because reuse without confirmation is inheritance without examination. The RIPC pattern requires a Confirm step: the human reviews the retrieved reasoning, evaluates whether it applies, and confirms or rejects before the system incorporates it into the current decision. Without this step, the system copies forward prior reasoning the same way teams copy forward prior briefs — without checking whether the assumptions still hold.

Listen for: "I should confirm that the lesson still applies." "I need to check whether the conditions match before it gets used." "Don't auto-apply prior reasoning — show it to me and let me decide." "I want to see the match rationale and then confirm or reject."

This becomes: Reuse-confirmation requirements. RIPC Confirm-stage specification for retrieval. The workflow step where the human reviews retrieved reasoning, sees the match rationale and applicability boundary, and confirms, modifies, or rejects before the system proceeds.

### Category 10 — Follow-up probes

- "Tell me about a time the team applied a lesson from a prior campaign that turned out not to apply. What went wrong?"
- "If the system showed you three prior campaign lessons ranked by relevance, with match rationale for each, would that change how you start a brief?"
- "What is the difference between finding a similar document and finding a relevant decision?"
- "What prior reasoning do you wish the system could surface automatically that you currently have to remember or look up manually?"

### Category 10 — What good answers contain

- Specific examples of prior reasoning that should have been retrieved but was not ("we repeated the readmissions mistake because nobody remembered the prior campaign")
- Named dimensions of relevance beyond text similarity (same goal, same audience, same constraint, same failure pattern)
- Clear statements about what the retrieval display should include (decision + reasoning + match rationale + boundary)
- Concrete examples of false analogies — prior reasoning that was applied but should not have been
- Named conditions under which prior reasoning should be suppressed or flagged as non-applicable

### Category 10 — What weak answers look like

- "Just search for similar campaigns." (Semantic search finds similar text, not relevant reasoning. A campaign that uses similar words but targets a different audience with different constraints is a false match.)
- "The team will remember what's relevant." (Memory is not retrieval. The team changes. Memory fades. The system must retrieve, not the people.)
- "Show everything and let me filter." (Showing everything is showing nothing. The system must rank by reasoning relevance, not dump results.)
- "Prior campaigns aren't relevant — every campaign is different." (Every campaign is different. But many share goals, audiences, constraints, and failure patterns. Retrieval surfaces the reasoning that transfers, not the campaign that repeats.)

### Category 10 — What this informs in the system

- Reasoning-relevance criteria and matching dimensions
- Retrieval metadata requirements (indexed fields beyond text content)
- Applicability-boundary fields and boundary-matching logic
- Match-rationale display format
- Prior-reasoning surfacing logic (when, where, and how in the workflow)
- Confidence/provenance display at retrieval time
- Retrieval filter specifications (vertical, audience, goal, constraint, outcome)
- False-analogy prevention and boundary-mismatch detection
- Reuse-confirmation workflow (RIPC Confirm stage for retrieval)
- Retrieval miss/gap logging and notification

### Category 10 — What this feeds in the HLD

- Section 6: Reasoning-relevant retrieval architecture — matching dimensions, metadata indexing, applicability-boundary matching, match-rationale generation, false-analogy prevention
- Section 5: Discovery / RIPC — retrieval stage configuration, reuse-confirmation step, prior-reasoning surfacing during Discovery
- Section 14: Risks and mitigations — false analogy, stale reasoning reuse, over-generalization of prior lessons

### Category 10 — Case-study observations to preserve

While asking these questions, note:

- How does the team currently find prior reasoning? (Usually: they ask a colleague, search a shared drive, or start from scratch.)
- Has the team ever applied a prior lesson that turned out not to hold? (Capture the story — it grounds the false-analogy prevention rules.)
- What dimensions of relevance does the team use intuitively that the system should formalize? (Goal match, audience match, constraint match, failure-pattern match.)
- How often does the team start a decision without any prior reasoning, when prior reasoning actually exists somewhere? (This is the retrieval-miss frequency.)
- Does the team currently distinguish between "similar prior work" and "applicable prior reasoning"? (Usually: they do not. Similarity is treated as relevance.)

---

## Category 11: Human Confirmation

### Category 11 — Purpose

Define how humans confirm, correct, reject, bound, or override system interpretations without creating ritual approval or confirmation fatigue. The RIPC pattern — Retrieve, Infer, Propose, Confirm — places human judgment at the end of each reasoning cycle, not at the beginning and not nowhere. But confirmation is useful only when the human is confirming something specific, with enough context to make a real judgment. If the system asks for confirmation too often, the human rubber-stamps. If it asks with too little context, the human confirms based on fluency rather than grounding. If it never asks, the system acts without accountability. This category operationalizes the Confirm step so that it produces genuine human judgment, not bureaucratic approval.

### Category 11 — Build output produced

- Confirmation-point map (where in the workflow the system asks for human confirmation)
- RIPC stage specifications (what happens at each stage of Retrieve, Infer, Propose, Confirm)
- Confirmation record schema (what is recorded when a human confirms, corrects, rejects, or overrides)
- Review UI requirements (what the human must see to confirm meaningfully)
- Correction capture requirements (how corrections are recorded and fed back into the system)
- Override logic (what happens when a human overrides a system recommendation)
- Escalation rules (when confirmation must be routed to a higher authority)
- Re-entry logic after correction (how the system proceeds after a human changes its interpretation)
- Confirmation fatigue mitigations (how the system keeps review meaningful without making it exhausting)
- Accountability/audit requirements (who confirmed what, when, and with what information)

### Category 11 — Core questions

**Q11.1 — Where should the system ask for human confirmation?**

Ask this because confirmation points must be designed, not assumed. The system should ask for confirmation at moments where its interpretation could materially change the output: after retrieving prior reasoning, after inferring an audience interpretation, after proposing a messaging approach, after selecting which governance rules apply. Not every step needs confirmation. The question is: which steps carry enough risk that proceeding without human judgment creates premature sufficiency?

Listen for: "Before it drafts clinical language." "After it retrieves the ICP and before it interprets the audience." "When it proposes which prior campaign lessons to apply." "After it selects the messaging approach but before it drafts." "When it encounters a compliance boundary it hasn't seen before."

This becomes: Confirmation-point map. The specific workflow steps where the system pauses for human judgment. The RIPC Confirm stage locations.

**Q11.2 — What exactly should the human be confirming?**

Ask this because vague confirmation is rubber-stamping. "Does this look right?" invites a glance and an approval. "The system inferred that the primary audience is IT directors at mid-market health systems, based on the current ICP and the prior campaign's results. The prior campaign targeted the same segment and achieved a 3.5% CTR. Do you want to proceed with this audience interpretation, modify it, or reject it?" invites a judgment. The confirmation prompt must be specific enough that the human is confirming a named interpretation, not approving a feeling.

Listen for: "I should be confirming the audience interpretation, not the whole brief." "I should be confirming whether the prior lesson applies, not whether the system found something." "I should be confirming the claim-evidence pairing, not the entire messaging approach." "I need to confirm specific things, not everything at once."

This becomes: Confirmation-prompt specifications. The named interpretation or proposal the human evaluates at each confirmation point. The difference between "approve this" and "confirm this interpretation given this evidence."

**Q11.3 — What should the human be able to correct, reject, or bound?**

Ask this because confirmation is not binary. The human may confirm the interpretation as-is. Or the human may correct it ("the audience is right but add CIOs"), reject it ("that prior lesson doesn't apply here — the competitive landscape has changed"), or bound it ("use this approach but only for the email channel, not social"). The system must support all four actions, not just confirm/reject.

Listen for: "I should be able to narrow the audience." "I should be able to say the lesson applies but only for this vertical." "I should be able to override the messaging approach." "I should be able to add a constraint the system didn't know about." "I should be able to reject the interpretation and provide my own."

This becomes: Correction, rejection, and bounding actions in the confirmation workflow. The response options available to the human at each confirmation point. The system's ability to incorporate partial corrections, not just full approvals or rejections.

**Q11.4 — What should be recorded when a human confirms?**

Ask this because the confirmation record is part of the reasoning state. It captures who confirmed, what they confirmed, what information was available at confirmation time, and whether they modified the interpretation. Without this record, the system cannot audit its decisions, the next cycle cannot learn from prior confirmations, and accountability is invisible.

Listen for: "Who confirmed it." "When they confirmed it." "What they saw when they confirmed." "Whether they changed anything." "What the system proposed versus what the human approved."

This becomes: Confirmation record schema. Fields: confirmer identity, timestamp, system proposal, human action (confirm / correct / reject / bound), modification details, information surface at confirmation time (what the human could see). Links to the Decision State and Investigation Trace.

**Q11.5 — What should happen after a correction?**

Ask this because a correction changes the reasoning state. If the human narrows the audience, the system must re-evaluate downstream steps that depend on the audience interpretation. If the human rejects a prior lesson, the system must proceed without it. If the human adds a constraint, the system must incorporate it into governance. The correction must propagate, not just be logged.

Listen for: "If I change the audience, the messaging should change too." "If I reject the prior lesson, the system should draft without it." "If I add a compliance constraint, the system should check against it." "The correction should flow through — it shouldn't just be noted and ignored."

This becomes: Re-entry logic after correction. The propagation rules that ensure a human correction changes downstream system behavior, not just the confirmation record. The link between correction and re-inference.

**Q11.6 — What should happen after an override?**

Ask this because an override is a correction that goes against the system's recommendation, and it carries special weight. If a brand lead overrides the system's governance flag to allow a restricted term for a specific campaign, that override must be recorded with the rationale, scoped to the specific instance, and not silently generalized. Overrides are legitimate — but they must be auditable, bounded, and non-precedent-setting unless explicitly promoted.

Listen for: "If compliance approves an exception, record why." "If I override a governance flag, it should apply to this campaign only." "Overrides should not automatically become new rules." "There should be an audit trail for every override." "The next campaign should not inherit the override unless someone explicitly says so."

This becomes: Override logic. Override record schema: who overrode, what was overridden, rationale, scope (this instance only / this vertical / permanent), audit trail. Override-scope rules that prevent accidental generalization.

**Q11.7 — Where is confirmation likely to become rubber-stamping?**

Ask this because confirmation fatigue is the operational enemy of meaningful review. If the system asks for confirmation at every step, the human will stop reading. If the system presents the same type of confirmation repeatedly, the human will develop a "click yes" reflex. If the confirmation prompt is too long or too vague, the human will skim. The system must be designed to resist the drift toward ritual approval.

Listen for: "If it asks too often, I'll just approve everything." "I already rubber-stamp half the reviews in our current workflow." "The compliance review is supposed to be thorough but everyone just checks the box." "I stop reading after the third prompt." "If the confirmation is always the same, I stop thinking about it."

This becomes: Confirmation fatigue mitigations. Frequency limits on confirmation prompts. Variability in confirmation format. Escalation for high-stakes confirmations that must not be rubber-stamped. The distinction between routine confirmations (which can be batched or simplified) and high-stakes confirmations (which must be presented with full context).

**Q11.8 — How should the system make review meaningful without slowing everything down?**

Ask this because the tension between thoroughness and speed is real. A system that requires full-context review at every step will be abandoned. A system that requires no review will produce unaccountable output. The design must find the points where review adds the most value and make those review moments efficient, contextual, and useful — not ritualistic.

Listen for: "Show me only what changed since my last review." "Highlight the parts that are new or risky — don't make me re-read everything." "Let me confirm the high-stakes parts and auto-approve the routine parts." "Batch the low-risk confirmations." "Make the review screen show me exactly what I need to judge, nothing more."

This becomes: Review UI requirements. Context-efficient review design. Differential review (show what changed). Risk-weighted review depth (full context for high-stakes, summary for routine). Batch-confirmation logic for low-risk steps.

**Q11.9 — What confirmation points are essential versus optional?**

Ask this because not all confirmations carry equal weight. Confirming a clinical claim before it enters a healthcare brief is essential. Confirming a brand-voice suggestion for an internal doc is optional. The system should have a tiered confirmation model: essential confirmations that block progress, recommended confirmations that prompt but do not block, and optional confirmations that are available but not triggered.

Listen for: "Compliance confirmation is non-negotiable." "Brand voice confirmation is nice to have but shouldn't block." "Audience confirmation should always happen." "Prior-lesson confirmation depends on the stakes." "For internal docs, most confirmations can be skipped."

This becomes: Confirmation tier classification (essential / recommended / optional). Blocking versus non-blocking confirmation points. The configuration that determines which confirmations are required for which content types and risk levels.

**Q11.10 — Who has authority for which types of confirmation?**

Ask this because confirmation by the wrong person is not confirmation. A marketer confirming a clinical claim is not the same as a compliance officer confirming a clinical claim. A junior team member confirming a competitive positioning is not the same as the product marketing lead confirming it. Authority must be mapped to confirmation type.

Listen for: "Compliance confirms clinical claims." "Brand confirms voice and positioning." "The campaign manager confirms audience interpretation." "Product marketing confirms ICP changes." "Legal confirms competitive comparisons in regulated verticals." "The campaign owner confirms everything else."

This becomes: Confirmation-authority model. The mapping between confirmation type and authorized confirmer. Role-based confirmation routing. Escalation rules when the authorized confirmer is unavailable.

### Category 11 — Follow-up probes

- "Walk me through the last time you reviewed something the AI produced. What did you actually check? What did you skip?"
- "If the system asked for your confirmation five times during a single brief, would you read each prompt carefully or start clicking 'approve'?"
- "What is the difference between a review that adds value and a review that is just a checkbox?"
- "What confirmation would you want to see that does not exist in the current workflow?"

### Category 11 — What good answers contain

- Named confirmation points with specific interpretations being confirmed
- Clear distinction between essential and optional confirmations
- Named authorities for each confirmation type
- Concrete examples of rubber-stamping in the current workflow
- Specific ideas for making review efficient without making it superficial
- Correction and override scenarios with propagation requirements

### Category 11 — What weak answers look like

- "Everything should go through review." (Everything reviewed is nothing reviewed. Which reviews matter most?)
- "The team will review it." (Which team member? For what specific judgment? With what authority?)
- "We don't need confirmation — the AI should get it right." (The AI will be wrong sometimes. The question is whether the human catches it before it matters.)
- "We'll add approval workflows later." (Approval workflows added after the system is running are approval workflows that missed the first batch of errors.)
- "Just put an 'approve' button on everything." (An approve button without context is a rubber stamp. Confirmation requires showing the human what they are confirming and why it matters.)

### Category 11 — What this informs in the system

- Confirmation-point map and RIPC stage specifications
- Confirmation record schema (who, what, when, with what information, what action)
- Review UI design (context-efficient, risk-weighted, differential)
- Correction capture and propagation logic
- Override logic and override-scope rules
- Escalation rules and authority routing
- Confirmation fatigue mitigations (frequency, variability, batching)
- Confirmation tier classification (essential / recommended / optional)
- Confirmation-authority model (who confirms what)
- Accountability and audit trail

### Category 11 — What this feeds in the HLD

- Section 5: Discovery / RIPC service pattern — Confirm stage specification, re-entry logic, confirmation-point map
- Section 10: Governance and observability — confirmation records, audit trail, override logging, accountability model
- Section 14: Risks and mitigations — confirmation fatigue, automation bias, rubber-stamping, accountability gaps

### Category 11 — Case-study observations to preserve

While asking these questions, note:

- How many confirmation points exist in the current workflow? How many are meaningful versus ritualistic?
- Where does rubber-stamping already occur? (This predicts where the system's confirmation will also become ritualistic unless designed differently.)
- How does the team currently record confirmations? (Usually: they don't. Approval is assumed, not documented.)
- What corrections has a human made that the system should have learned from? (This links confirmation to the learning loop.)
- Does the team currently distinguish between "I confirmed this" and "I approved this without reading it"? (Usually: they do not. Both look the same in the audit trail.)

---

## Category 12: Ownership / Lifecycle

### Category 12 — Purpose

Define who owns the knowledge, reasoning objects, policies, updates, review cadences, and lifecycle transitions that keep the system current. Without ownership, knowledge decays silently. Without lifecycle management, the system accumulates stale reasoning, outdated policies, expired premises, and orphaned records that no one reviews, updates, or retires. The system becomes a knowledge-management graveyard with better UX — everything looks current because nothing is marked as old. This category prevents that outcome by producing the ownership model, lifecycle states, staleness-detection rules, review cadences, and governance responsibilities that keep the system's knowledge surface honest.

### Category 12 — Build output produced

- Ownership model per knowledge category (who creates, reviews, updates, and retires each type of content)
- Ownership model per reasoning object (who is responsible for each of the six reasoning objects)
- Review cadence (how often each knowledge category and reasoning object must be reviewed)
- Lifecycle states (draft / provisional / validated / deprecated / superseded / archived)
- Staleness detection rules (what conditions trigger a staleness warning)
- Notification workflow (who is notified when content becomes stale, requires review, or has been flagged)
- Deprecation rules (what happens when content is no longer current but may still be referenced)
- Archival/retention rules (what is kept, for how long, and in what form)
- Update authority (who can modify each knowledge category and reasoning object)
- Governance responsibility matrix (who is accountable when the system uses stale or wrong knowledge)

### Category 12 — Core questions

**Q12.1 — Who owns each knowledge category?**

Ask this because knowledge without an owner is knowledge nobody updates. The brand guide may exist, but if nobody is responsible for reviewing it, it ages silently. The competitive battlecard may exist, but if nobody owns it, it reflects last quarter's landscape. Ownership means a named person or role is accountable for creating, reviewing, and updating each category — and for flagging when it is no longer current.

Listen for: "Product marketing owns the ICPs." "The brand team owns voice guidelines." "Nobody owns competitive intel right now." "Compliance owns the approved claims list." "Demand gen owns the playbooks." "The analytics team owns campaign performance data."

This becomes: Ownership model per knowledge category. Named owners or roles for each KB category. Identified gaps where ownership is missing or informal.

**Q12.2 — Who owns each policy or rule?**

Ask this because policies without owners become zombie rules — enforced by the system but reviewed by nobody. A restricted-term list must have an owner who can add, remove, or modify terms. An evidence-requirement rule must have an owner who can update the standard when regulations change. If no one owns the policy, no one can update it when reality shifts.

Listen for: "Legal owns the restricted-language list." "Compliance owns the evidence requirements for clinical claims." "Brand owns the voice guidelines." "Nobody has formally owned the governance rules — they were set up once and left." "The CMO is accountable for brand policy but delegates updates to the brand team."

This becomes: Ownership model per policy or rule. Named owners for governance artifacts. Escalation path when a policy needs updating but the owner is unclear.

**Q12.3 — Who approves learning updates?**

Ask this because learning updates change the system's reasoning, and unapproved changes to reasoning are unapproved changes to future decisions. When a Learning Event produces a MUO candidate, someone must confirm the lesson is valid, scope it appropriately, and approve its entry into the system. Without an approval authority, lessons enter the system based on whoever interpreted the results, which may be wrong.

Listen for: "The campaign manager interprets the results but product marketing should approve ICP changes." "Compliance must approve any change to the approved claims." "The data team should validate that the analytics support the conclusion." "The demand gen lead confirms playbook updates." "Nobody formally approves lessons — they just get remembered or forgotten."

This becomes: Learning-update approval authority. The mapping between lesson type and approver role. Review-gate specifications for MUOs. The gap between "lesson interpreted" and "lesson validated and applied."

**Q12.4 — How often should each source be reviewed?**

Ask this because review cadence is how the system prevents silent staleness. Competitive intelligence may need monthly review because the market moves fast. ICPs may need quarterly review because buyer behavior changes seasonally. Brand voice may need annual review because positioning is relatively stable. Approved claims may need review whenever regulations change, not on a calendar.

Listen for: "Competitive intel should be reviewed monthly." "ICPs should be reviewed quarterly." "Brand voice gets reviewed annually." "Compliance rules get reviewed when regulations change." "Playbooks should be reviewed after every major campaign cycle." "Campaign performance data is reviewed after every campaign."

This becomes: Review-cadence specifications per knowledge category. Calendar-based review triggers (monthly, quarterly, annual). Event-based review triggers (regulation change, product release, competitive launch). The schedule that feeds the staleness-detection system.

**Q12.5 — What makes a source stale?**

Ask this because staleness is not just age. A competitive battlecard is stale when the competitor launches a new product, regardless of when the battlecard was last reviewed. An ICP is stale when the target market restructures, regardless of the calendar. A campaign lesson is stale when the product it referenced has changed. The system needs both time-based and event-based staleness triggers.

Listen for: "It's stale when the competitor releases a new product." "It's stale when the review window passes." "It's stale when the product changes." "It's stale when the team using it says it's wrong." "It's stale when the regulations change." "It's stale when the market shifts and nobody updates the source."

This becomes: Staleness detection rules. Time-based triggers (exceeded review cadence). Event-based triggers (competitor launch, product change, regulation update, market shift). User-reported staleness (the team flags a source as outdated). The conditions that cause the system to mark content as stale and notify the owner.

**Q12.6 — What happens when a source expires?**

Ask this because expiration must produce a visible action, not silent decay. When a competitive battlecard passes its review window, the system should notify the owner and flag the content for review. When an approved claim is withdrawn, the system should mark it as deprecated and prevent it from being cited. When an ICP is superseded by a new version, the old version should be archived, not deleted — because prior reasoning that referenced the old ICP must remain traceable.

Listen for: "Notify the owner." "Flag it for review." "Stop using it in drafts until it's updated." "Archive it but keep it accessible for audit." "Deprecate it but don't delete it — we might need the history." "Replace it with the new version and link them."

This becomes: Expiration-action rules. Notification workflow for expired content. Retrieval suppression for expired content (surface with warning, not without context). Deprecation versus deletion rules. Version linking between superseded and superseding content.

**Q12.7 — What should be archived, deprecated, or retained?**

Ask this because the system needs clear rules for content that is no longer current but still has value. Archived content is no longer active but remains accessible for reference and audit. Deprecated content is marked as outdated and should not be used in new decisions but may be needed to understand prior ones. Retained content is kept for regulatory, legal, or organizational requirements.

Listen for: "Keep old ICPs so we can trace why prior campaigns targeted who they did." "Archive old playbooks — they're useful for history but not for current work." "Deprecated claims should be flagged if someone tries to use them." "Regulatory requires us to keep all compliance-reviewed content for five years." "Prior reasoning records should never be deleted — they're the audit trail."

This becomes: Archival rules per content type. Deprecation behavior (flag, warn, suppress, but do not delete). Retention requirements (regulatory, legal, organizational). The lifecycle states that content passes through: draft, provisional, validated, deprecated, superseded, archived.

**Q12.8 — Who is accountable when the system uses stale or wrong knowledge?**

Ask this because accountability without ownership is blame without remedy. When the system produces output based on an outdated ICP, who is responsible? The owner who failed to update it? The system that failed to flag it? The reviewer who approved the output? The answer depends on the ownership model, the staleness-detection rules, and the review workflow. Clear accountability prevents the "nobody's fault" failure mode.

Listen for: "The owner should have updated it." "The system should have flagged it." "The reviewer should have caught it." "Nobody is accountable — that's the problem." "If the system used stale data and nobody was notified, that's a system failure, not a person failure."

This becomes: Governance responsibility matrix. The mapping between failure type and accountable party. The link between ownership, staleness detection, and accountability. The expectation that if the owner was notified and did not act, accountability is different than if the system failed to notify.

**Q12.9 — What lifecycle states does the team need?**

Ask this because lifecycle states make knowledge status visible. A source in "draft" status should not be cited as evidence. A source in "validated" status carries full authority. A source in "deprecated" status should trigger a warning if retrieved. A source in "superseded" status should link to its replacement. Without visible lifecycle states, the system treats everything as equally current.

Listen for: "We need draft and approved at minimum." "We need a way to mark something as outdated but still accessible." "We need a superseded state that points to the replacement." "We need an archived state for things we keep for compliance but don't use." "We need provisional — good enough to use but not fully validated yet."

This becomes: Lifecycle-state taxonomy. State definitions (draft / provisional / validated / deprecated / superseded / archived). State-transition rules (what triggers a move from one state to another). State-dependent system behavior (retrieval rules, citation rules, display rules per state).

**Q12.10 — How should handoffs work when ownership changes?**

Ask this because ownership changes are inevitable — people leave, roles change, teams restructure — and every ownership change is a moment where knowledge can become orphaned. The departing owner's knowledge, context, and judgment about the content's current state should transfer to the new owner. Without a handoff process, the new owner inherits the content without inheriting the understanding.

Listen for: "When someone leaves, their KB categories need a new owner." "We've lost knowledge when people changed roles." "The handoff should include what's current, what's stale, and what's under review." "There should be a notification when ownership transfers." "The new owner should know what review cadence applies and when the last review happened."

This becomes: Ownership-transfer workflow. Handoff requirements (content inventory, staleness status, review history, pending reviews). Notification rules for ownership changes. Orphaned-content detection (content whose owner has changed without a handoff).

### Category 12 — Follow-up probes

- "What knowledge has become stale without anyone noticing? How was it discovered?"
- "What happened the last time someone left and their knowledge responsibilities were not transferred?"
- "If you could see the lifecycle status of every piece of content the system uses, what statuses would you need?"
- "What content should the system stop using automatically versus what should require a human decision to retire?"

### Category 12 — What good answers contain

- Named owners per knowledge category with explicit accountability
- Specific review cadences with both calendar-based and event-based triggers
- Concrete examples of staleness that went undetected and caused problems
- Clear lifecycle states with defined transitions
- Named accountability when stale knowledge produces bad output
- Handoff scenarios with specific requirements for what must transfer

### Category 12 — What weak answers look like

- "Everyone owns everything." (If everyone owns it, nobody owns it. Shared ownership without named accountability is no ownership.)
- "We review things when we have time." (Review without cadence is review that does not happen. Staleness is the default state of unreviewed knowledge.)
- "Nothing gets outdated that quickly." (It does. Competitive intel, campaign performance, regulatory changes, and product updates all create staleness faster than most teams recognize.)
- "We don't need lifecycle states — everything is current." (If everything is current, the team has not looked closely enough. Every knowledge base contains content that is outdated, orphaned, or superseded.)
- "We'll figure out ownership later." (Ownership defined after the system is running is ownership defined after the first round of stale knowledge has already produced bad output.)

### Category 12 — What this informs in the system

- Ownership model per knowledge category and per reasoning object
- Review-cadence specifications (calendar-based and event-based)
- Staleness-detection rules and notification workflow
- Lifecycle-state taxonomy and state-transition rules
- Deprecation, archival, and retention rules
- Governance responsibility matrix
- Update-authority model (who can modify what)
- Ownership-transfer workflow and orphaned-content detection
- State-dependent retrieval and citation behavior

### Category 12 — What this feeds in the HLD

- Section 8: State lifecycle model — lifecycle states, state transitions, staleness detection, review triggers, retention rules
- Section 10: Governance and observability — ownership model, accountability matrix, audit logging, notification workflow
- Section 12: Volume management and retention — archival rules, retention requirements, deprecation behavior

### Category 12 — Case-study observations to preserve

While asking these questions, note:

- How many knowledge categories have a named owner today? (Usually: fewer than the team thinks.)
- How many sources have a defined review cadence? (Usually: almost none. Review happens when someone notices a problem, not on a schedule.)
- Has the team experienced a failure caused by stale knowledge? (Capture the story — it grounds the staleness-detection rules.)
- What happened the last time someone left the team? Was their knowledge responsibility transferred? (Usually: no. The content became orphaned.)
- Does the team currently have any lifecycle-state visibility? (Usually: no. Everything looks equally current because nothing is marked as old.)

---

## Category 13: Build Translation

### Category 13 — Purpose

Turn all discovery answers from categories 1 through 12 into a usable HLD input packet. This is not a discovery category — it is a translation step. It does not generate new insights about the organization or its workflows. It maps what has already been discovered into the architecture components the build team needs: data objects, metadata fields, services, retrieval rules, governance rules, UI/workflow requirements, lifecycle requirements, and scope decisions. The output of this category is the bridge between "what we learned about the organization" and "what the system must contain."

### Category 13 — Build output produced

- Architecture-landing summary (a structured summary of all discovery outputs, organized by system component)
- HLD input packet (the complete set of specifications the HLD/reference architecture needs)
- Data object requirements (what objects the system must store, with fields and relationships)
- Metadata requirements (what metadata fields must be captured, indexed, and displayed)
- Service requirements (what services the system must provide: retrieval, governance, sufficiency, learning)
- Retrieval requirements (what must be retrievable, by what dimensions, with what display)
- Governance requirements (what rules must be enforced, at what severity, with what audit trail)
- UI/workflow requirements (what the human must see and do at each step)
- Lifecycle requirements (what states, transitions, review cadences, and retention rules apply)
- MVP scope (the smallest useful build from these inputs)
- Future-phase backlog (what is important but not included in the MVP)

### Category 13 — Core questions

**Q13.1 — What build inputs have we produced from each category?**

Ask this because this is the inventory step. Before translation begins, the team must see what discovery produced. Each category generated build outputs: schemas, rules, criteria, workflows, and specifications. This question produces a category-by-category summary of what was discovered and what build artifacts it produced.

Listen for: This is an internal review question, not a stakeholder interview question. The answers come from the discovery records, not from a conversation. The facilitator or build lead reviews the outputs from categories 1 through 12 and summarizes them.

This becomes: Architecture-landing summary. The single document that shows the build team what discovery produced and where each output lands in the system.

**Q13.2 — Which answers become data objects?**

Ask this because data objects are the things the system stores. The campaign brief schema (Category 2) becomes a data object. The Premise Stack (Category 5) becomes a data object. The Learning Event (Category 9) becomes a data object. The MUO (Category 9) becomes a data object. The Investigation Trace (Category 8) becomes a data object. Each of these must be defined with fields, types, relationships, and constraints.

Listen for: Review the build outputs from each category. Any output that says "schema," "record," "fields," or "object" is likely a data object candidate.

This becomes: Data object requirements. The list of objects the system must store, with field definitions drawn from discovery. The six reasoning objects plus the campaign brief, KB chunks, policy rules, and confirmation records.

**Q13.3 — Which answers become metadata fields?**

Ask this because metadata fields are what make data objects retrievable, filterable, governable, and traceable. Category, vertical, owner, updated date, review cadence, authority level, confidence, applicability boundary, lifecycle state — these are not content fields; they are metadata that travels with content and determines how the system treats it.

Listen for: Review the build outputs from Categories 3, 4, 10, and 12 especially. Any output that says "metadata," "filter," "index," or "display at retrieval time" is a metadata field candidate.

This becomes: Metadata requirements. The minimum metadata schema that must be captured at content creation, indexed for retrieval, and displayed at retrieval time. The fields that turn raw content into governed, traceable knowledge.

**Q13.4 — Which answers become governance rules?**

Ask this because governance rules are the constraints the system enforces. Evidence-requirement rules (Category 4), policy rules (Category 6), sufficiency conditions (Category 7), and confirmation requirements (Category 11) all translate into governance logic: what the system must check, flag, block, or route for review.

Listen for: Review the build outputs from Categories 4, 6, 7, and 11. Any output that says "rule," "constraint," "gate," "block," "flag," "escalate," or "require" is a governance rule candidate.

This becomes: Governance requirements. The complete set of rules the system enforces, classified by severity (blocking / flagging / coaching) and by type (evidence, policy, sufficiency, confirmation).

**Q13.5 — Which answers become retrieval rules?**

Ask this because retrieval rules determine what the system surfaces, when, ranked by what criteria, with what display. Reasoning-relevance criteria (Category 10), authority-based ranking (Category 4), applicability-boundary matching (Category 10), and metadata-filtered search (Category 3) all translate into retrieval architecture.

Listen for: Review the build outputs from Categories 3, 4, 10, and 6. Any output that says "retrieval," "matching," "ranking," "filter," "surface," or "citation" is a retrieval rule candidate.

This becomes: Retrieval requirements. The matching dimensions, ranking rules, filter specifications, and display requirements that define what the system retrieves and how it presents it.

**Q13.6 — Which answers become UI/review workflow requirements?**

Ask this because the human interface determines whether governance, confirmation, and review actually work. Confidence-display requirements (Category 4), review UI requirements (Category 11), match-rationale display (Category 10), and evidence-visibility requirements (Category 4) all translate into what the human sees and does at each workflow step.

Listen for: Review the build outputs from Categories 4, 7, 10, and 11. Any output that says "display," "show," "review," "confirm," or "interface" is a UI/workflow requirement candidate.

This becomes: UI/workflow requirements. The specifications for what the human sees at each confirmation point, review gate, and retrieval moment. The design requirements that make governance visible and confirmation meaningful.

**Q13.7 — Which answers become sufficiency gates?**

Ask this because sufficiency gates are the system's stopping conditions — the checks that must pass before the system proceeds. Pre-draft blocking conditions (Category 7), evidence requirements (Category 4), missing-information checks (Category 2), and essential confirmation points (Category 11) all translate into sufficiency-gate specifications.

Listen for: Review the build outputs from Categories 2, 4, 7, and 11. Any output that says "must be present," "blocks," "required before," "cannot proceed without," or "must confirm" is a sufficiency-gate candidate.

This becomes: Sufficiency-gate specifications. The complete set of checks the system performs before proceeding at each workflow step. The operational translation of "what must be true before the system acts."

**Q13.8 — Which answers become reasoning-state objects?**

Ask this because reasoning-state objects are what the system preserves for the next cycle. The Optimizer State, Premise Stack, Decision State, Investigation Trace, Learning Event, and Model Update Object (Category 8) are the six reasoning objects. Discovery determines which fields each object contains, when each is captured, and how each is displayed to the next cycle's user.

Listen for: Review the build outputs from Categories 5, 8, and 9 especially. Any output that says "preserve," "capture," "record for next cycle," "reasoning record," or "what the next cycle needs" is a reasoning-state object specification.

This becomes: Reasoning-state object specifications. The six-object schema with fields, capture triggers, retention rules, and display requirements drawn from discovery.

**Q13.9 — Which answers become learning-loop requirements?**

Ask this because learning-loop requirements define how outcomes become lessons and how lessons reach the next cycle. Outcome-capture requirements, prediction-error triggers, MUO schemas, confirmation workflows for learning, and MUO retrieval specifications (Category 9) all translate into learning-loop architecture.

Listen for: Review the build outputs from Categories 9 and 10. Any output that says "learning," "outcome," "prediction error," "MUO," "lesson," or "next cycle" is a learning-loop requirement candidate.

This becomes: Learning-loop requirements. The specifications for outcome capture, prediction-error detection, MUO creation, MUO confirmation, MUO routing, and MUO retrieval that make the learning loop operational.

**Q13.10 — What is the smallest useful build from these inputs?**

Ask this because MVP scope prevents the build from becoming unmanageable. Not everything discovered in categories 1 through 12 belongs in the first build. The smallest useful build should include: the workflow boundary (Category 1), the decision-artifact schema (Category 2), the core KB categories with metadata (Category 3), the highest-priority governance rules (Category 6), the minimum viable sufficiency conditions (Category 7), the minimum viable reasoning-state capture (Category 8), and enough retrieval to surface prior reasoning at decision time (Category 10). Everything else becomes a future-phase candidate.

Listen for: This is a scoping decision, not a discovery question. The build lead reviews all discovery outputs and determines what can be deferred.

This becomes: MVP scope. The first-build specification. Future-phase backlog. The boundary between "must have for the system to be useful" and "important but not first."

### BUILD TRANSLATION TABLE

| Guide category | Primary artifact produced | System component | HLD section | MVP priority | Future phase |
| --- | --- | --- | --- | --- | --- |
| 1. Workflow Boundary | Workflow definition, scope, success criteria | Workflow configuration, entry-point logic | Section 13: Minimal viable implementation | High | Multi-workflow support |
| 2. Campaign Brief Structure | Campaign brief schema, required fields, draft-generation inputs | Decision-artifact data model, sufficiency checks | Section 3: Six-object data model; Section 8: State lifecycle | High | Conditional fields, multi-artifact types |
| 3. KB / Information Surfaces | KB taxonomy, source inventory, metadata schema | Information-surface registry, retrieval filters, citation logic | Section 4: Supporting data objects; Section 6: Retrieval; Section 12: Volume management | High | Full source integration, advanced chunking |
| 4. Trust, Evidence, and Confidence | Source-trust hierarchy, evidence-requirement rules, confidence-display rules | Confidence scoring, authority-weighted retrieval, provenance display | Section 6: Retrieval; Section 3: Data model; Section 10: Governance | Medium | Multi-signal conflict resolution, confidence calibration |
| 5. Assumptions / Premises | Premise inventory, Premise Stack schema, assumption-risk map | Premise Stack data object, staleness flags, re-examination triggers | Section 3: Six-object data model; Section 6: Retrieval; Section 7: Learning loop | Medium | Automated premise-falsification detection |
| 6. Policy / Governance Boundaries | Policy-rule inventory, DO/DON'T lists, claim-type taxonomy | Policy engine, governance scoring, review gates, approval workflows | Section 10: Governance; Section 5: RIPC; Section 8: State lifecycle | High | Multi-vertical governance, automated policy updates |
| 7. Sufficiency and Stopping Conditions | Sufficiency criteria, pre-draft blocking conditions, abstention rules | Sufficiency gates, stop/ask/escalate logic, quality-gate scoring | Section 8: State lifecycle; Section 5: RIPC; Section 10: Governance | High | Adaptive sufficiency thresholds |
| 8. Reasoning to Preserve | Reasoning-state preservation scope, six-object field definitions, capture triggers | Six reasoning objects (Optimizer State, Premise Stack, Decision State, Investigation Trace, Learning Event, MUO) | Section 3: Six-object data model; Section 5: RIPC; Section 8: State lifecycle | High | Full six-object capture, cross-workflow reasoning links |
| 9. Learning Loop | Learning Event schema, MUO schema, outcome-capture requirements, effectiveness signal | Learning Event creation, MUO lifecycle, prediction-error detection, outcome-to-reasoning routing | Section 7: Learning-loop architecture; Section 3: Data model; Section 6: Retrieval | Medium | Automated prediction-error detection, multi-campaign learning aggregation |
| 10. Retrieval Relevance | Reasoning-relevance criteria, retrieval metadata, match-rationale display, false-analogy prevention | Reasoning-relevant retrieval engine, applicability matching, match-rationale generation | Section 6: Retrieval; Section 5: RIPC; Section 14: Risks | Medium | Cross-workflow retrieval, automated relevance scoring |
| 11. Human Confirmation | Confirmation-point map, RIPC Confirm specifications, confirmation-fatigue mitigations | Confirmation workflow, review UI, correction propagation, override logic | Section 5: RIPC; Section 10: Governance; Section 14: Risks | High | Adaptive confirmation frequency, learning from confirmation patterns |
| 12. Ownership / Lifecycle | Ownership model, review cadence, lifecycle states, staleness-detection rules | Lifecycle state machine, staleness notification, ownership registry, archival logic | Section 8: State lifecycle; Section 10: Governance; Section 12: Volume management | Medium | Automated ownership-transfer detection, cross-system lifecycle sync |

### Category 13 — Follow-up probes

- "Looking at the full set of discovery outputs, what is the single most important thing the system must do on day one?"
- "What can be deferred to a second phase without making the first phase useless?"
- "Where are the gaps — what did discovery not cover that the build team will need?"
- "If you had to cut half the scope, what stays?"

### Category 13 — What good answers contain

- A complete mapping from discovery outputs to system components
- Clear MVP scope with named inclusions and exclusions
- Data object definitions with fields drawn from discovery
- Governance rules classified by severity and mapped to system behavior
- Retrieval specifications drawn from Category 10 and Category 3
- A future-phase backlog with priority ordering

### Category 13 — What weak answers look like

- "Build everything we discovered." (Scope discipline is critical. Not everything belongs in the first build.)
- "The architecture team will figure it out." (The architecture team needs inputs. This category produces those inputs.)
- "We'll prioritize later." (Prioritization is part of this category. MVP scope must be defined before the build begins.)
- "Everything is high priority." (If everything is high priority, nothing is. The translation table exists to force scope decisions.)

### Category 13 — What this informs in the system

- Architecture-landing summary (all discovery outputs organized by system component)
- Data object specifications (six reasoning objects plus supporting objects)
- Metadata schema (fields, indexing, display rules)
- Governance rule inventory (classified by severity and type)
- Retrieval architecture specifications (matching, ranking, display)
- UI/workflow specifications (what the human sees and does)
- Sufficiency-gate specifications (what must be true before action)
- Learning-loop specifications (outcome capture, MUO lifecycle, retrieval)
- Lifecycle specifications (states, transitions, staleness, retention)
- MVP scope and future-phase backlog

### Category 13 — What this feeds in the HLD

- All HLD sections — this category produces the architecture-landing summary that feeds the entire HLD / reference architecture

### Category 13 — Case-study observations to preserve

While asking these questions, note:

- How much of what was discovered in categories 1 through 12 is genuinely new to the team versus already known but never formalized? (This reveals the discovery process's value beyond the system build.)
- Where do discovery outputs conflict with each other? (These conflicts must be resolved before the build, not during it.)
- What did the team learn about their own workflow that they did not know before? (This is the meta-observation: discovery as organizational learning.)
- How willing is the team to accept a narrow MVP scope? (Resistance to narrow scope predicts scope creep in the build.)
- What gaps remain after discovery? (No discovery process is complete. Naming the gaps is part of honest translation.)

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

*Draft status: v0.4 full companion artifact draft. All thirteen build-discovery categories are fully drafted. Derived from PAPER_v1.0_WORKING.md, the accepted Executive Brief, the Keystone / Two-Track Strategy note, and prior Build Discovery Guide drafts. Not a replacement for the full paper or the HLD.*
