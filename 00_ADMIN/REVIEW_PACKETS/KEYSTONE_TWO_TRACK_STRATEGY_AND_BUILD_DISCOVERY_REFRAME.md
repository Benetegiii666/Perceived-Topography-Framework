# Keystone, Two-Track Strategy, and Build Discovery Guide Reframe

**Date:** 2026-06-22
**Status:** Strategy note. No artifacts drafted.

---

## 1. Current Status

- `PAPER_v1.0_WORKING.md` is frozen as the internal v1.0 working paper (2,583 lines, 31,387 words, 36 references, 8 figures, 23-question Appendix A).
- `COMPANION_ARTIFACTS/EXECUTIVE_BRIEF_v1.0.md` is accepted as the first completed companion artifact.
- The next companion artifact should not be treated as a generic "Practitioner Workbook." A workbook implies facilitation scripts, session agendas, and workshop patterns — useful, but not what the build path needs next.
- The next artifact should be reframed as a **build-discovery guide**: a question-driven instrument organized by build-input categories, where every question produces a concrete system specification.

---

## 2. The Keystone Framing

The paper is the keystone. It holds the core conceptual structure stable:

- Perceived topography — the information-and-action environment as the system experiences it
- Gradients — directional pressures that make some paths easier, more available, or more sufficient than others
- Sufficiency — the stopping condition where the system treats its current reasoning as enough to act
- Premature sufficiency — acting before the reasoning warrants it
- Reasoning state — the structured condition from which a system acts (goal, policy, interpretation, premises, confidence, sufficiency rationale)
- Learning as model change — evidence-supported updates to the reasoning that would otherwise reproduce the same error
- The six-object reasoning architecture — Optimizer State, Premise Stack, Decision State, Investigation Trace, Learning Event, Model Update Object
- Appendix A — the conceptual interview shape (23 questions across 4 phases)

The keystone paper should not try to do everything itself. It provides the conceptual foundation that downstream artifacts operationalize, build from, and eventually pressure-test with real evidence.

---

## 3. The Two Paths

From the keystone, the work forks into two connected paths.

### Path 1 — Actual Build

**Purpose:** Turn the framework into something usable inside a real organization.

This path produces:

- Build discovery guide (the next companion artifact)
- Campaign brief structure
- KB / context-layer structure
- Metadata model
- Source hierarchy
- Governance and evidence rules
- Retrieval requirements
- Sufficiency checks
- Reasoning-state objects
- Learning loop
- HLD / reference architecture
- Demo / prototype / first 30–60 day usable system

**Path 1 is the evidence engine.** It is how the framework eventually produces real data, case-study evidence, implementation failures, design constraints, and observed practice. Without a build, the framework remains a conceptual argument. With a build, it becomes testable.

### Path 2 — Formal Academic Paper

**Purpose:** Turn the framework into an academically legible and defensible scholarly contribution.

This path produces:

- Formal academic paper version
- Literature positioning
- Research questions
- Falsifiability plan
- Empirical validation plan
- Case-study structure
- Theoretical contribution
- Study design
- Publication-quality argument

**Path 2 should remain more formal, careful, cited, and claim-disciplined than the build path.** The build path can move fast, experiment, and tolerate ambiguity. The academic path must be precise about what is claimed, what is assumed, what is borrowed, and what is original.

---

## 4. How the Paths Feed Each Other

The loop:

```
Keystone paper
    → companion docs
    → actual build
    → practical learning / observed evidence
    → case-study data
    → formal academic paper
    → refined framework
    → updated companion docs
```

- The build path gives observations, artifacts, implementation failures, design constraints, and data. It produces the evidence the academic path needs to move from pre-empirical to empirical.
- The academic path gives rigor, testable claims, literature grounding, and conceptual discipline. It prevents the build path from losing the framework's distinctions in the rush to ship.
- Both paths should remain connected but not collapsed into each other. A build discovery guide is not a research instrument. A formal paper is not a product spec. But each should be aware of what the other needs.

---

## 5. Role of the RapidSOS Demo/Context

The RapidSOS Marketing Context Layer demo and case-study context provides practical grounding for the build path.

**Important framing:**

The RapidSOS work does not replace the framework. It does not replace the companion docs. It does not turn the next artifact into RapidSOS documentation.

Instead, it gives concrete grounding so the Build Discovery Guide is not vague or theoretical.

**What the RapidSOS context provides:**

- **Original practical question:** "What is a marketing context layer?" — the same question the framework answers at a deeper level.
- **Working demo:** A governed KB with brand voice, ICPs, messaging, playbooks, competitive intel. Retrieval with confidence thresholding. Brand and ICP governance on intake. Quality scoring on output. Gap logging and knowledge lifecycle. Campaign execution with cross-channel chaining. Analytics feedback with learnings that flow back through governance.
- **Audience validation:** Cassidy and the team responded because it made the abstract idea tangible. The demo was the answer to "what does this actually look like on Tuesday morning?"
- **Practical baseline:** The RapidSOS build is now a concrete arena where guide questions and examples can be grounded — not hypothetically, but in terms of actual KB categories, actual governance rules, actual retrieval behavior, and actual quality scoring.

---

## 6. Correct Relationship Among the Three Efforts

| Effort | Role |
| --- | --- |
| Keystone paper | Gives the conceptual foundation — the vocabulary, the architecture, the diagnostic structure, the learning model, the falsifiability conditions. |
| Companion docs | Operationalize the foundation — the executive brief sells the why; the build discovery guide discovers the what; the HLD designs the how. |
| RapidSOS build | Gives practical learning by seeing the ideas in action — a concrete system where the framework's distinctions either hold up or need revision. |

**Rules:**

- Do not let the RapidSOS context hijack the companion artifact structure. The guide must work for any organization running repeated decision workflows, not only for marketing teams using ChromaDB.
- Do not let the companion docs become abstract theory. Every question must have a build target. Every category must produce system specifications.
- Use RapidSOS as the concrete arena where the guide can hang exercises and examples — but keep the guide's structure general enough that a healthcare operations team, a compliance team, or a support triage team could also use it.

---

## 7. Reframe of the Next Companion Artifact

The next artifact should not be called "Practitioner Workbook." That name implies facilitation scripts, session agendas, "who should be in the room" sections, and workshop logistics. Those are useful but secondary.

The next artifact should be framed as a build-discovery guide: a question-driven instrument organized by build-input categories, where every question produces a concrete system specification.

**Recommended title:**

> **Decision Topography Build Discovery Guide: Questions That Become System Inputs**

**Why this title:**

- "Decision Topography" connects to Appendix A and the paper's vocabulary.
- "Build Discovery" signals that the purpose is to discover what must be built, not to facilitate a workshop.
- "Questions That Become System Inputs" states the design rule directly: every question must have a build target.

**What the artifact should answer:**

> What do I need to ask the team, category by category, to get the concrete details required to build the campaign brief structure, KB structure, metadata, governance rules, reasoning-state objects, retrieval behavior, sufficiency checks, learning loop, and HLD inputs?

**What it should not be organized by:**

- Calendar time (Day 1, Week 1, Week 2)
- Generic facilitation theory
- "Who should be in the room" as a major section
- "When to use the interview" as a major section

**What it should be organized by:**

Build-input categories. Each category is a system component that the guide helps the team specify.

---

## 8. Required Guide Table Pattern

The core organizing device for the Build Discovery Guide is a four-column table that maps each guide category to its general purpose, a concrete grounding example, and the system component it informs.

| Guide category | General PTF purpose | RapidSOS grounding example | What system thing this informs |
| --- | --- | --- | --- |
| Campaign brief structure | Define the decision artifact | What must a campaign brief contain before AI drafts? | Campaign brief schema, required fields, missing-info checks, draft-generation inputs |
| KB / information surfaces | Define what the system can see and trust | Brand voice, ICPs, messaging, playbooks, competitive intel | KB taxonomy, source types, chunking strategy, metadata model, retrieval filters |
| Governance boundaries | Shape gradients away from unsafe claims | Approved claims, restricted language, evidence requirements | Policy rules, claim validation, approval gates, brand/compliance scoring |
| Sufficiency rules | Define when the system can act or must pause | When is a draft "good enough" vs. needing review? | Stop/ask/escalate logic, confidence thresholds, quality gates |
| Reasoning preservation | Keep "why" from disappearing | What assumption shaped this campaign? What evidence was missing? | Optimizer State, Premise Stack, Decision State, Investigation Trace |
| Learning loop | Make the next run smarter | What campaign result should change future briefs? | Learning Event, Model Update Object, analytics feedback loop |
| Retrieval relevance | Retrieve prior reasoning, not just similar text | Which prior campaign lesson applies here, and why? | Reasoning-relevant retrieval, applicability rules, confidence/provenance display |
| Human confirmation | Keep humans in the correction loop | Who confirms whether a prior lesson applies? | RIPC flow, review UI, confirmation records, override logic |
| Ownership / lifecycle | Keep knowledge current and governed | Who owns brand voice, ICPs, playbooks, claims, competitive intel? | Ownership model, review cadence, staleness detection, notification workflow |

This table is the spine of the guide. Each row becomes a section. Each section contains questions that produce system specifications.

---

## 9. Principle for the Build Discovery Guide

**Design rule: Every question must have a build target.**

Questions should not be included merely because they are interesting, conceptually important, or good for team conversation.

Each question should produce one or more of:

- Campaign brief structure specification
- KB structure specification
- Metadata field
- Reasoning object specification
- Governance rule
- Retrieval rule
- Confidence/provenance requirement
- Lifecycle requirement
- HLD input
- Future case-study observation

If a question does not produce a build target, it does not belong in the guide. It may belong in the paper, in the executive brief, or in a facilitation supplement — but not in the build discovery guide.

---

## 10. Appendix A Relationship

Appendix A remains the conceptual short version. It asks the right questions at the right level of abstraction:

- Phase 1: Map the Decision Topography
- Phase 2: Shape the Motion
- Phase 3: Preserve the Reasoning
- Phase 4: Make the Next Cycle Smarter

The Build Discovery Guide is Appendix A made operational.

Appendix A asks: "What kind of work keeps coming back?" The Build Discovery Guide asks: "What are the required fields in the campaign brief schema, and which ones must be present before the system drafts?"

Appendix A asks: "What rules can change the answer?" The Build Discovery Guide asks: "What claim types require approved evidence? What restricted terms must be flagged? What approval gates exist before publish?"

Appendix A asks: "Did the next run actually get smarter?" The Build Discovery Guide asks: "What outcome data feeds back through governance? What fields does a Learning Event require? How does a Model Update Object get scoped, reviewed, and applied?"

The relationship is clear: Appendix A is the conceptual seed. The Build Discovery Guide is the operational tree.

---

## 11. Case-Study / Academic Evidence Layer

Path 1 should also preserve research-relevant observations — not by turning the build guide into an academic instrument, but by quietly capturing the baseline data that the formal academic path will later need.

The build guide should capture, as natural byproducts of the discovery process:

- **Baseline workflow pain points** — what is broken today, before the framework is applied
- **Recurring failure modes** — where premature sufficiency, stale reasoning, or reasoning loss currently occurs
- **What reasoning currently disappears** — what the team knows but the system does not preserve
- **What artifacts currently exist** — what documents, templates, playbooks, and governance already live somewhere
- **How decisions currently become "good enough"** — what the current sufficiency condition is (often: "the draft sounds professional")
- **What outcomes are expected to improve** — what the team predicts will change
- **What evidence would show the next cycle got smarter** — the team's own success criteria

This is not to make the build guide feel academic. It is to avoid losing the observations that can later support the formal academic path. If the build runs for 60 days and produces real results, those results should be capturable as case-study data without having to reconstruct the baseline after the fact.

---

## 12. Recommended Next Action

**Draft the Build Discovery Guide v0.1 skeleton.**

Use the four-column table pattern (Section 8) as the structural spine. Fully draft two sample categories:

1. **Campaign Brief Structure** — the decision artifact itself
2. **KB / Information Surfaces** — what the system can see and trust

Do not draft the entire guide in one pass. The two sample categories will validate the format, question style, and build-target mapping before the remaining seven categories are drafted.

Save as: `COMPANION_ARTIFACTS/BUILD_DISCOVERY_GUIDE_v0.1.md`

---

## No-Edit Confirmation

- `PAPER_v1.0_WORKING.md` edited: No
- `COMPANION_ARTIFACTS/EXECUTIVE_BRIEF_v1.0.md` edited: No
- Figures modified: No
- Figure 8 modified: No
- References modified: No
- Build Discovery Guide drafted: No (strategy note only)
- HLD drafted: No
- Prior review packets overwritten: No
