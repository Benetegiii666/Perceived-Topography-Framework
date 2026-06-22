# Campaign Brief Workflow Discovery v0.1

**Date:** 2026-06-22
**Status:** Discovery worksheet — Categories 1-3 only. Awaiting Benet review and input.
**Primary source:** `COMPANION_ARTIFACTS/BUILD_DISCOVERY_GUIDE_v1.0.md`, Categories 1-3.
**Companion:** `IMPLEMENTATION_PLANNING/FIRST_IMPLEMENTATION_SLICE_PLAN_v0.2.md`

---

## 1. Purpose

This worksheet collects concrete implementation inputs for the first campaign brief workflow. It translates Build Discovery Guide Categories 1-3 into specific questions, answer slots, and output tables that feed directly into data model sketches and build backlog.

### What this is

- A structured discovery instrument for the selected first workflow
- A bridge between planning artifacts and implementation specifications
- A set of questions that must be answered before schemas or code

### What this is not

- Not a schema or data model (that comes after discovery)
- Not a build backlog (that comes after the data model)
- Not Categories 4-13 (those come after Categories 1-3 are filled)
- Not an academic interview (this produces build inputs)

---

## 2. Selected Workflow

**Workflow:** Marketing Campaign Brief Workflow
**Role:** First grounding case for PTF implementation. Not the framework center.
**Current status:** Selected for discovery. Not yet build-ready.

The campaign brief workflow was selected because it meets HLD Chapter 13 criteria: decisions recur, the team can articulate "better," outcomes are observable, reasoning currently disappears, and the workflow has documented grounding material from the RapidSOS case study.

---

## 3. Category 1 — Workflow Boundary

*Build Discovery Guide Category 1 asks: "What kind of work keeps coming back?"*

### Questions

**3.1 What starts the workflow?**

What triggers the creation of a new campaign brief? Is it a calendar cycle, a stakeholder request, a product launch, a market event, or something else?

> **Answer:** `TBD`

**3.2 Who requests the brief?**

Who initiates the workflow? What is their role? Do they always have the same goal, or does the goal vary by campaign type?

> **Answer:** `TBD`

**3.3 What decision is being made?**

What is the core decision the brief represents? (e.g., "what messaging, audience, and claims should this campaign use?") Is it a single decision or a bundle of related decisions?

> **Answer:** `TBD`

**3.4 What ends the workflow?**

When is the brief "done"? Is there a formal approval step? Who signs off? What happens after sign-off?

> **Answer:** `TBD`

**3.5 What is the decision artifact?**

What does the brief look like? Is it a document, a form, a structured template, a slide deck, or something else? Does the format vary?

> **Answer:** `TBD`

**3.6 Who confirms the reasoning?**

Who reviews the brief's reasoning — not just the text, but the targeting logic, claim choices, audience assumptions, and evidence basis? Is this the same person who requests it?

> **Answer:** `TBD`

**3.7 Who validates domain/policy/evidence claims?**

Who has authority to say "this claim is approved," "this audience assumption is valid," or "this evidence is sufficient"? Is it the same person as 3.6?

> **Answer:** `TBD`

**3.8 What is explicitly out of scope?**

What does this workflow NOT decide? (e.g., creative production, channel execution, budget allocation, sales follow-up strategy)

> **Answer:** `TBD`

**3.9 What outcome will be observed later?**

After the campaign runs, what data will tell us whether the brief's decisions were good? How long after execution does this data become available?

> **Answer:** `TBD`

**3.10 How often does this workflow repeat?**

Weekly? Monthly? Per product launch? Per vertical? What determines the cadence?

> **Answer:** `TBD`

### Workflow Boundary Output Table

| Field | Value |
|---|---|
| `workflow_start_trigger` | `TBD` |
| `workflow_end_condition` | `TBD` |
| `decision_artifact` | `TBD` |
| `requester` (PTF: Requester role) | `TBD` |
| `domain_expert` (PTF: Domain Expert role) | `TBD` |
| `governance_owner` (PTF: Governance Owner role) | `TBD` |
| `outcome_signal` | `TBD` |
| `outcome_availability_delay` | `TBD` |
| `workflow_cadence` | `TBD` |
| `explicit_exclusions` | `TBD` |

---

## 4. Category 2 — Campaign Brief Structure

*Build Discovery Guide Category 2 asks: "What does the actual decision artifact contain?"*

### Questions

**4.1 What fields belong in the campaign brief?**

List every field or section in a typical campaign brief. Include both formal fields and informal sections that "everyone knows should be there."

> **Answer:** `TBD`

**4.2 Which fields are required vs. optional?**

For each field, is it required for the brief to be considered complete, or is it optional/nice-to-have?

> **Answer:** `TBD`

**4.3 Which fields are generated vs. human-authored?**

Which fields could the system draft from information surfaces and prior reasoning? Which fields must the human write from scratch?

> **Answer:** `TBD`

**4.4 Which fields require evidence?**

Which fields make claims that must be supported by evidence (e.g., "reduces readmissions" requires approved evidence; "workflow burden is common" may not)?

> **Answer:** `TBD`

**4.5 Which fields require governance review?**

Which fields cross policy or compliance boundaries? Which fields should the Governance / Sufficiency Agent flag for review?

> **Answer:** `TBD`

**4.6 Which fields depend on audience/vertical?**

Which fields change depending on the target audience or vertical (e.g., healthcare vs. enterprise vs. K-12)? How does the brief adapt?

> **Answer:** `TBD`

**4.7 Which fields should cite information surfaces?**

Which fields should trace back to a specific information surface (e.g., "this claim comes from the approved claims repository," "this audience insight comes from ICP documentation")?

> **Answer:** `TBD`

**4.8 Which fields should link to reasoning objects?**

Which fields represent reasoning that should be preserved as Optimizer State, Premise Stack, or Decision State fields? (This is the connection between the decision artifact and the reasoning-state objects.)

> **Answer:** `TBD`

### Campaign Brief Field Output Table

| # | brief_field | purpose | required / optional | generated / human-confirmed | evidence_required | governance_review_required | linked_reasoning_object | source_surface |
|---|---|---|---|---|---|---|---|---|
| 1 | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` |
| 2 | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` |
| 3 | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` |
| ... | | | | | | | | |

*Rows will be populated during discovery. Start with the fields from the RapidSOS grounding material if applicable, then generalize.*

---

## 5. Category 3 — KB / Information Surfaces

*Build Discovery Guide Category 3 asks: "What does the team actually check before deciding?"*

### Questions

**5.1 What information surfaces are needed for the first workflow?**

List every document, data source, repository, or reference the team consults (or should consult) when creating a campaign brief.

> **Answer:** `TBD`

**5.2 Where do they live?**

For each surface, where is it stored? (e.g., Google Drive, Notion, internal wiki, CRM, analytics dashboard, shared folder, someone's head)

> **Answer:** `TBD`

**5.3 Who owns them?**

For each surface, who is responsible for keeping it current? Who should be notified if the content is stale?

> **Answer:** `TBD`

**5.4 What authority level do they carry?**

For each surface, is it binding (must follow), advisory (useful but not governing), background (context only), or anecdotal (signal only)?

> **Answer:** `TBD`

**5.5 Are they current?**

For each surface, when was it last updated? Is there a review cadence? Has the content been validated recently?

> **Answer:** `TBD`

**5.6 Are they accessible?**

For each surface, can the system access it directly, or does it require a human to retrieve and provide the content?

> **Answer:** `TBD`

**5.7 Are any critical surfaces missing?**

Are there information sources the team knows should exist but don't? Topics where the team improvises because no documented source exists?

> **Answer:** `TBD`

**5.8 Which surfaces should be manually registered for MVP?**

Which surfaces are essential for the first RIPC cycle? The system cannot retrieve what is not registered.

> **Answer:** `TBD`

### Information Surface Output Table

| # | surface_name | type | owner | location | authority_level | last_updated | accessibility | MVP_required | notes |
|---|---|---|---|---|---|---|---|---|---|
| 1 | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` |
| 2 | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` |
| 3 | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` | `TBD` |
| ... | | | | | | | | | |

*Rows will be populated during discovery.*

---

## 6. Initial Information Surface Registry Draft

Based on the Slice Plan v0.2 and RapidSOS grounding material, the following surfaces are expected candidates for the first workflow. All values marked `TBD` require Benet's input.

| # | Surface Name | Type | Owner | Location | Authority | Last Updated | Accessibility | MVP Required | Notes |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Brand voice guidelines | document | `TBD` | `TBD` | binding | `TBD` | `TBD` | Yes | DO/DON'T rules, vertical adaptations, restricted terms. RapidSOS grounding: `seed_data/brand_voice.md` |
| 2 | ICP: primary buyer persona | document | `TBD` | `TBD` | advisory | `TBD` | `TBD` | Yes | Pain points, buying signals, decision process. RapidSOS grounding: `seed_data/icp_*.md` |
| 3 | Messaging frameworks | document | `TBD` | `TBD` | advisory | `TBD` | `TBD` | Yes | Product positioning per vertical. RapidSOS grounding: `seed_data/messaging_*.md` |
| 4 | Competitive positioning | document | `TBD` | `TBD` | advisory | `TBD` | `TBD` | Recommended | Differentiation language. RapidSOS grounding: `seed_data/competitive_*.md` |
| 5 | Campaign playbooks | document | `TBD` | `TBD` | advisory | `TBD` | `TBD` | Recommended | Workflow templates, channel strategy. RapidSOS grounding: `seed_data/playbook_*.md` |
| 6 | Approved claims repository | document / policy | `TBD` | `TBD` | binding | `TBD` | `TBD` | Yes | What claims can be made, with what evidence, for which audiences |
| 7 | Prior campaign performance data | data source | `TBD` | `TBD` | background | `TBD` | `TBD` | Recommended | Engagement, conversion, pipeline metrics from past campaigns |
| 8 | Sales feedback | data source | `TBD` | `TBD` | anecdotal | `TBD` | `TBD` | Recommended | Qualitative feedback on lead quality, buyer readiness |
| 9 | Prior reasoning objects | reasoning-state store | System | Reasoning-state store | Varies by status | N/A (first cycle) | Direct | Yes (empty on first cycle) | Prior Optimizer States, Premise Stacks, Decision States, MUOs |

**Notes:**

- Surfaces 1-6 are the minimum set for the first RIPC Retrieve step.
- Surfaces 7-8 are valuable for premise formation but may be harder to structure for MVP.
- Surface 9 is empty on the first cycle — it becomes populated after the first cycle completes.
- RapidSOS grounding references point to existing Rapid seed data files that demonstrate the content structure. These are examples, not the actual surfaces for the first implementation.

---

## 7. Open Questions for Benet

### Must answer to complete Categories 1-3

| # | Question | Why it matters |
|---|---|---|
| 1 | **Which specific campaign is the first campaign?** | Determines the concrete workflow boundary, audience, vertical, and information surfaces. Without a specific campaign, discovery stays abstract. |
| 2 | **Which existing Rapid/RapidSOS assets should be treated as initial information surfaces?** | The Rapid seed data (brand_voice.md, icp_*.md, messaging_*.md, etc.) could bootstrap the information surface registry. Are they the actual first surfaces, or should new ones be created? |
| 3 | **Who plays Requester / Domain Expert / Governance Owner?** | Named people with availability. In a solo or small-team operation, one person may hold multiple roles — but the architecture should still log which role they are acting in for each confirmation. |
| 4 | **What brief format should be treated as the decision artifact?** | Is there an existing brief template? A Google Doc? A structured form? A slide? Or should the system define the brief format as part of the build? |
| 5 | **Which information surfaces are binding vs. advisory vs. background vs. anecdotal?** | Authority classification affects retrieval weighting, governance rules, and premise confidence. The team's judgment is needed — the system cannot infer authority levels. |
| 6 | **What outcome signal matters most for the first cycle?** | Engagement? Qualified pipeline? Sales feedback on lead quality? Conversion rate? The outcome signal determines what the Outcome Record captures and what prediction errors look like. |
| 7 | **Is the RapidSOS healthcare campaign (cardiology RPM) the specific first campaign, or is a different campaign better suited?** | The healthcare campaign is well-documented in the paper and Rapid materials, but a different campaign may be more practical for the first build cycle. |
| 8 | **What information surfaces are missing?** | Are there critical sources the team consults informally but has never documented? Topics where the team improvises because no structured source exists? These gaps are valuable discovery — they reveal where reasoning currently disappears. |

### Can wait until after Categories 1-3

| # | Question | When needed |
|---|---|---|
| 9 | What static Discovery Pattern questions work best for this workflow? | During RIPC implementation (Category 7 territory) |
| 10 | What governance rules apply to which claim types? | During governance implementation (Category 6 territory) |
| 11 | What sufficiency criteria should the system check? | During sufficiency gate design (Category 7 territory) |

---

## 8. Recommended Next Action

### Step 1: Review this worksheet with Benet

Walk through Categories 1-3. Fill in the TBD slots. The open questions in Section 7 are the priority — especially questions 1-4.

### Step 2: Fill in the output tables

Once Benet provides input, populate:

- Workflow Boundary Output Table (Section 3)
- Campaign Brief Field Output Table (Section 4)
- Information Surface Output Table (Section 5)

### Step 3: Create a data model sketch

Translate the filled worksheet into a concrete schema sketch (not DDL, not code — a structured specification). The schema draws from:

- HLD Chapter 3 MVP fields (reasoning objects)
- Category 2 output (brief fields)
- Category 3 output (information surface registry)

### Step 4: Create build backlog

Convert the slice plan + filled worksheet + schema sketch into a sequenced build backlog with tasks, dependencies, and acceptance criteria.

**Recommended sequence:** 1 → 2 → 3 → 4. Discovery before schemas. Schemas before backlog.

---

## No-Edit Confirmation

- Frozen paper (`PAPER_v1.0_WORKING.md`) edited: **No**
- Figure 8 modified: **No**
- Figures modified: **No**
- References modified: **No**
- Executive Brief v1.0 edited: **No**
- Build Discovery Guide v1.0 edited: **No**
- HLD v1.0 content edited: **No**
- Slice Plan v0.2 edited: **No**
- Capability Map v0.1 edited: **No**
- Categories 4-13 included: **No** (only 1-3)
- Schemas created: **No**
- Backlog created: **No**
- Implementation code created: **No**
