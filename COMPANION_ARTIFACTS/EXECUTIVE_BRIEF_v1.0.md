# Executive Brief: Shaping Better AI Decisions with the Perceived Topography Framework

---

## One-Sentence Thesis

AI systems do not fail only because they lack information. They fail because the landscape around them makes the wrong path visible, easy, trusted, or sufficient.

---

## The Problem

Your teams are doing the right things. They are building prompt libraries, adding documents to retrieval systems, connecting data sources, and refining instructions. The AI gets more context with every iteration. It produces fluent, confident, professional-sounding output.

And it keeps making the same kind of mistake.

A marketing agent drafts a campaign with an unsupported clinical claim. A support system gives a confident answer based on stale policy. An operations tool takes an action before checking whether it should. A planning agent produces a recommendation that sounds right but rests on an assumption nobody examined.

The outputs are polished. The reasoning is shallow.

The usual diagnosis is that the system needs more context, better prompts, or tighter guardrails. Those responses are useful. They are also incomplete.

The missing layer is not more information. It is preserved reasoning.

Organizations routinely store what happened — the final brief, the campaign report, the postmortem, the dashboard — without preserving why decisions were made. The goal that shaped the action. The assumptions that made it feel reasonable. The evidence that was missing. The confidence that was asserted without basis. The stopping condition that let the system act before the reasoning was actually sufficient.

When the next cycle begins, the system inherits the artifacts without inheriting the judgment. It starts confident. It stays wrong. The same failure returns in a different form.

---

## The Core Reframe

The usual question after an AI failure is: *What is wrong with the model?*

That question matters. But it is often not the most useful question.

The more useful question is: *What landscape did we ask the system to move through?*

An AI agent does not act in a vacuum. It acts inside an environment of visible options, accessible tools, represented goals, trusted signals, and connected consequences. Some paths through that environment are easy to find. Others are buried, disconnected, or invisible. Some actions feel sufficient long before the reasoning actually warrants them.

That difference in felt ease is a gradient — a directional pressure within the environment. A persuasive but unsupported claim has a strong gradient because it pulls attention toward action. A disconnected policy has a weak gradient because it exists without shaping the decision. Gradients explain why "more context" often does not help: a retrieved source does not automatically constrain a claim if the claim already feels easier, more available, and more sufficient than the evidence check.

The Perceived Topography Framework treats this environment as a design surface. The landscape — what the system can see, reach, understand, trust, and connect — is not fixed. It can be shaped.

When the desired path is also the easiest sufficient path, better behavior becomes the natural result. When the landscape makes the wrong path easier than the right one, no amount of instruction reliably compensates.

Build better landscapes. Not as a slogan, but as an operating principle: design the environment so that grounded, policy-aware, human-beneficial action is easier to reach than the confident shortcut.

---

## Key Concepts in Plain Language

**Perceived topography** is the information-and-action environment as the system experiences it. Not the world as it objectively is, but the world as it has been made available — what the system can see, reach, understand, trust, and connect to the decision at hand.

**Sufficiency** is the point at which the system treats its current reasoning as enough to stop investigating and act. Sufficiency is not certainty. It is the stopping condition. Many failures begin not when a system decides to be wrong, but when the system reaches sufficiency too soon.

**Premature sufficiency** is what happens when the system acts before the reasoning warrants it. The answer sounds good. The draft looks complete. The tool call seems routine. But the evidence has not been checked, the policy has not been connected, the assumptions have not been examined, or the prior lesson has not been retrieved. The easy path felt sufficient before the careful path became visible.

**Reasoning state** is the structured condition from which a system acts: the active goal, governing constraints, interpretation of the situation, working assumptions, confidence levels, uncertainty signals, and the rationale for why the available information felt sufficient. Context tells the system what information is available. Reasoning state tells the system why that information matters and what should change when outcomes arrive.

---

## Why Prompt Libraries and Context Stuffing Are Not Enough

Prompt libraries and RAG (retrieval-augmented generation) are useful infrastructure, but they do not solve the core problem by themselves: they do not preserve the reasoning transition from one decision cycle to the next.

A better prompt does not automatically preserve why a prior decision worked, why it failed, or what should change the next time. A system can retrieve a prior campaign brief without knowing which premise was tested, which assumption failed, which evidence boundary mattered, or whether the prior lesson applies to the current situation.

A reasoning-state architecture does something different. It preserves what the system was trying to do, what it believed, why the action felt sufficient, what reality later contradicted, and what should change. It retrieves prior reasoning by relevance to the current decision — not just by text similarity. It requires human confirmation before prior reasoning is reused.

The difference is not "more context." The difference is a system that can remember why, not just what.

---

## Mini Example: Healthcare Campaign

A marketing team asks an AI agent to draft a campaign for a remote patient monitoring product targeting cardiology practice administrators. Both paths start with the same organizational materials: product documents, audience research, prior campaigns, compliance guidance, and an approved-claims repository.

**The context-only path.** The agent retrieves relevant materials. It finds that readmissions are mentioned in prior documents, that administrators care about workload, and that remote monitoring offers operational benefits. It synthesizes a compelling message: *"Our platform helps cardiology teams reduce readmissions."*

The phrase is concise, persuasive, and aligned with the business goal. It is also a direct clinical-outcome claim for which the organization has no approved evidence.

The compliance guidance exists in the system. But it is not connected to the specific sentence being produced. The absence of an approved claim is easy to interpret as missing content rather than as a reason to stop. The fluent answer becomes sufficient before the evidence boundary exerts force.

That is premature sufficiency. The system acted before its reasoning warranted the claim.

**The reasoning-state path.** The agent starts with the same materials. The attractive claim is still visible. But the system also carries an explicit goal (qualified demo requests, not broad awareness), a connected policy boundary (clinical-outcome claims require approved evidence), and a confidence-bounded audience interpretation (workflow burden is an attention signal, not necessarily a buying-readiness signal).

When the readmissions claim surfaces, the system checks: is there approved evidence? There is not. The claim is set aside. The agent produces a campaign around operational value — workflow visibility, care-team coordination, monitoring between visits — and flags the clinical-outcome claim for compliance review.

The same information. A different landscape. A different result.

---

## What Changes Operationally

When a team adopts this framework, the work changes in specific ways:

- **Capture assumptions, not just final outputs.** Before a campaign, recommendation, or decision goes out, preserve what the team believed and why. If the premise turns out to be wrong, the organization can identify which part of the reasoning failed — not just that the result was disappointing.

- **Preserve why a decision felt sufficient.** The most important thing to record is not the answer but the stopping condition. Why did the team act when it did? What evidence was considered enough? What uncertainty was left unresolved?

- **Track what changed after outcomes arrive — and make it specific.** When reality contradicts expectations, the organization should produce a bounded update, not a vague lesson. "Improve targeting" is not learning. "Workflow pain attracts attention but does not reliably indicate buying readiness — distinguish attention from qualification" is learning. Learning means the reasoning that would otherwise reproduce the same error actually changes.

- **Reuse prior reasoning only when it applies.** Prior lessons should not be silently applied to new decisions. They should be surfaced with their confidence, scope, and boundaries. A human should confirm that the prior reasoning applies before the system treats it as guidance.

- **Make confidence, provenance, and applicability boundaries visible.** When the system retrieves prior reasoning, the user should see how confident it was, who confirmed it, where it applies, and where it does not.

- **Design AI workflows around repeated decisions, not isolated prompts.** The highest value comes from workflows where decisions recur, outcomes matter, and one cycle should help the next cycle improve. Single-use prompts do not need this architecture. Repeated decision workflows do.

---

## What Leaders Should Ask For

If you lead a team that uses AI for repeated decision work, these questions will surface where reasoning disappears:

1. **What repeated decisions should we improve first?** Not every workflow needs reasoning-state architecture. Start where mistakes recur, outcomes matter, and one cycle should make the next cycle smarter.

2. **What reasoning disappears between cycles?** When the workflow repeats, does the system start from what was learned last time — or does it start cold from the same prompt and the same documents?

3. **What assumptions should survive into the next run?** Not the final output, but the working beliefs that shaped it. If those assumptions turn out to be wrong, can the organization trace which one failed?

4. **What counts as enough evidence before action?** Has the team defined what "sufficient" looks like — or is sufficiency whatever the AI produces when the draft sounds good?

5. **Where are we letting fluent outputs feel sufficient too soon?** Fluency is not evidence. A plausible-sounding answer may be an unsupported one. Where is the team most vulnerable to confident-but-wrong?

6. **How will we know whether the next cycle got smarter?** If the system cannot show that the second run started from a better place than the first, the organization has memory but not learning.

---

## Companion Artifacts

The Perceived Topography Framework is delivered through three companion artifacts. Each serves a different audience and answers a different question.

### The Paper

*The Perceived Topography Framework: A Reasoning-State Architecture for Human-Agent Systems.*

The paper teaches the framework. It provides the full conceptual architecture, the healthcare stress test, the six-object reasoning architecture, the learning model, the Discovery loop, the falsifiability conditions, and the intellectual lineage. It is written for practitioners and researchers who want to understand why the framework works the way it does. The paper presents a pre-empirical design framework with falsifiable claims, not an empirical study.

### The Practitioner Workbook

*The Perceived Topography Practitioner Workbook.*

The workbook helps teams discover the reasoning that should shape their AI systems. It expands the paper's Decision Topography Interview (23 questions across four phases) into facilitation scripts, worksheets, worked examples, and workshop patterns. A team should be able to pick up the workbook, run a discovery session on one repeated workflow, and produce structured outputs that feed directly into system design.

### The HLD / Reference Architecture

*The Perceived Topography HLD / Reference Architecture.*

The HLD translates the framework into implementable system design. It specifies the six reasoning-state objects, the Discovery service pattern (Retrieve → Infer → Propose → Confirm), reasoning-relevant retrieval architecture, governance and lifecycle management, confidence and provenance tracking, human confirmation workflows, and a minimal viable implementation path. A platform team should be able to read the HLD and begin designing data objects, services, workflows, and retrieval systems.

**The relationship is simple:**

- The paper explains how to think about the problem.
- The workbook discovers what the organization knows, believes, and needs.
- The HLD designs what to build.

---

## Recommended First Move

Do not begin by building a larger prompt library. Do not begin by adding more documents to the retrieval system. Do not begin by buying a new platform.

Begin by mapping the landscape.

Choose one repeated decision workflow where AI output matters, mistakes recur, and one cycle should make the next cycle smarter. A campaign brief. A customer escalation. A compliance review. A content approval. A pricing decision. A support triage.

Sit down with the people who make that workflow work. Ask them eight questions:

1. What kind of work keeps coming back, and what result matters?
2. What are we acting as though we already know?
3. What rules should shape the action but often do not?
4. Where does the team move too fast and regret it later?
5. When should the system stop and ask a person?
6. Six weeks from now, what would someone need to know about why we chose this?
7. What mistake should have changed the next run but did not?
8. Did the next run actually get smarter?

One hour. One workflow. Eight questions.

By the end, the team will not have merely gathered requirements. They will have mapped the operating landscape their system moves through. Every answer is a design specification — for what the system should see, what should make it pause, what reasoning must survive, and how the next cycle should begin differently.

The answers tell you what to build.

---

## One-Page Version

### The Problem

AI systems retrieve context but lose reasoning. They produce confident-but-wrong work because the landscape makes the easy path feel sufficient too soon. Organizations preserve artifacts — campaign briefs, postmortems, reports — without preserving why decisions were made. The next cycle inherits the output without inheriting the judgment.

### The Core Insight

The issue is not only the model's capability. It is the information landscape the model moves through — and that landscape can be designed. When the desired path is also the easiest sufficient path, better behavior becomes the natural result. The Perceived Topography Framework shapes what the system can see, trust, investigate, stop on, preserve, and learn from.

### What Changes

- Systems preserve why, not just what.
- Instead of blank-form intake, the system infers a draft interpretation, proposes it, and the human confirms, corrects, or bounds it.
- Sufficiency becomes a designed stopping condition, not whatever feels complete.
- Learning changes future reasoning, not just future storage.
- Prior reasoning is retrieved by relevance to the current decision, not just by text similarity.
- Human confirmation is required before prior reasoning is reused.

### What Leaders Should Ask For

- What repeated decisions should we improve first?
- What reasoning disappears between cycles?
- What assumptions should survive into the next run?
- What counts as enough evidence before action?
- Where are we letting fluent outputs feel sufficient too soon?
- How will we know whether the next cycle got smarter?

### The Recommended First Move

Start with one repeated decision workflow where AI output matters, mistakes recur, and one cycle should make the next cycle smarter. Run the Decision Topography Interview: eight questions, one hour, one workflow. The answers become design specifications for what the system should see, what should make it pause, what reasoning must survive, and how the next cycle should begin differently.

---

*Status: v1.0 companion artifact. Accepted executive-facing brief derived from PAPER_v1.0_WORKING.md and companion artifact planning notes. Not a replacement for the full paper.*
