# v1.0 Section 7 Source Packet

## Discovery Turns Human Intent Into Reusable Reasoning

---

## Section Purpose

Section 7 must explain why preserved reasoning cannot depend only on post-hoc learning. Organizations also need a way to capture reasoning before action: intent, assumptions, confidence, boundaries, constraints, decision logic, tacit knowledge, and unresolved questions.

Section 6 defined learning as an evidence-supported model update triggered by prediction error. But learning happens after reality answers back. Discovery happens before — and during — action. It converts the reasoning that lives inside conversations, assumptions, habits, and expert judgment into something that future systems and humans can use.

The controlling insight:

Discovery is not a formality before work begins. It is the process by which human intent, assumptions, boundaries, and decision logic become available to future reasoning.

---

## Narrative Position

Sections 1-6 now establish:

- Landscape design (S1)
- Context versus reasoning state (S2)
- Optimizer state and perceived topography (S3)
- Gradients, attention, attraction, investigation, sufficiency, and action (S4)
- Healthcare campaign stress test (S5)
- Learning requires preserved reasoning (S6)

Section 7 must answer the next question:

If preserved reasoning is necessary, how does the organization capture it before it disappears?

---

## Reader Realization

After reading Section 7, the reader should be able to say:

"Most organizational reasoning is not missing because nobody knows it. It is missing because it remains unstructured, unconfirmed, and unavailable at the moment future systems need it. Discovery converts tacit reasoning into reusable reasoning surfaces by retrieving existing context, inferring likely assumptions, proposing a candidate reasoning state, and requiring human confirmation where the answer would materially change action."

---

## Opening Bridge from Section 6

Section 6 ends with:

> "If learning depends on preserved reasoning, then organizations need a way to capture reasoning before it disappears into conversation, memory, intuition, or one-off correction."
>
> "That problem is Discovery."

Section 7 should take that handoff and immediately show what kind of reasoning disappears and why.

Do not replay the learning loop. Do not re-define Model Update Objects. Begin from the gap: what reasoning exists before action but does not survive into reusable form?

---

## Source Files and Line Ranges

| Source | File | Relevant sections | Line ranges |
| --- | --- | --- | --- |
| v0.2 Discovery section | PAPER_v0.2.md | S11: Discovery Turns Requests Into Usable Reasoning | Lines 2217-2480 |
| v0.1 Discovery section | PAPER_v0.1.md | S11: Discovery Framework: From Messy Intent to Reasoning State | Lines 2353-2616 |
| Concept architecture | CURRENT_STATE.md | Discovery Framework (Phase 4.4) | Lines 107-122 |
| v1.0 S6 ending | PAPER_v1.0_WORKING.md | "That problem is Discovery." | Lines 1262-1268 |
| v1.0 S5 campaign | PAPER_v1.0_WORKING.md | Reasoning-state path, human question, bounded campaign | Lines 669-773 |
| Reviewer synthesis | V0_2_REVIEW_SYNTHESIS_MEMO.md | KM graveyard risk, user burden | Lines 43-45 |
| Rewrite doctrine | V1_0_REWRITE_DOCTRINE_AND_WORKPLAN.md | KM graveyard objection response | Section 11 (lines ~462) |
| S6 source-packet review | V1_0_SECTION_06_SOURCE_PACKET_REVIEW.md | KM graveyard allocation: S6 names problem, S7 delivers solution | Reviewer 3 and Reviewer 4 |

---

## Inherited Claims from Sections 1-6

### Landscape Design

S1 established that safer behavior comes from shaping the landscape. Discovery shapes the landscape by making tacit reasoning visible before action.

### Context Versus Reasoning State

S2 established that context does not preserve why. Discovery is the process that produces reusable reasoning from context that would otherwise remain passive.

### Optimizer State and Perceived Topography

S3 defined Goal, Policy, Interpretation, and the five topography dimensions. Discovery elicits and confirms these: what is the goal? What policy applies? How is the situation interpreted? What is visible, accessible, represented, trusted, and connected?

### Motion, Sufficiency, and Failure

S4 defined how gradients create motion and how premature sufficiency produces failure. Discovery can change what becomes sufficient by surfacing unresolved questions, evidence boundaries, and confidence gaps before action.

### Healthcare Campaign Stress Test

S5 showed the reasoning-state path asking a targeted question ("Are we targeting practices already evaluating RPM, or creating demand among problem-aware but not-yet-shopping buyers?"). That question is Discovery in action.

### Learning Requires Preserved Reasoning

S6 defined learning as model change after prediction error. It ended by noting that learning cannot happen without preserved reasoning, and that reasoning must also be captured before action.

---

## Original Discovery / Reasoning-Capture Material Inventory

### Preserved Concepts

| Concept | v0.2 location | Status for v1.0 |
| --- | --- | --- |
| "Discovery is the process by which messy human intent and organizational artifacts are converted into structured reasoning objects" | v0.2 S11 line 2233 | **Preserve — refine to emphasize human reasoning capture, not just artifact conversion** |
| "Do the reasoning work before asking the user to do it" | v0.2 S11 line 2247 | **Preserve as the primary design principle** |
| Retrieve → Infer → Propose → Confirm loop | v0.2 S11 line 2238; CURRENT_STATE.md line 115 | **Preserve as the central loop. Evaluate whether Generate, Preserve, Learn should remain in S7 or be treated as natural consequences.** |
| Discovery is not a questionnaire | v0.2 S11 line 2241 | **Preserve** |
| Correctable inference over blank interrogation | v0.2 S11 line 2319 | **Preserve** |
| Ask only where uncertainty materially affects the result | v0.2 S11 line 2341; CURRENT_STATE.md line 120 | **Preserve** |
| Discovery Pattern Update | v0.2 S11.10 lines 2377-2385 | **Preserve — the system learns how to ask better** |
| Initial Discovery vs. Runtime Discovery | v0.2 S11.2 lines 2275-2292 | **Compress — the distinction is useful but does not need a full subsection** |
| Human control comes through correction | v0.2 S11.12 lines 2401-2412 | **Preserve** |
| Discovery shapes the starting optimizer state | v0.2 S11.13 lines 2415-2424 | **Preserve — connects Discovery to safety** |

### Strong Original Formulations

These should be preserved or closely paraphrased:

1. "Do the reasoning work before asking the user to do it." (v0.2 S11 line 2247)
2. "Discovery is not a questionnaire." (v0.2 S11 line 2241)
3. "The system should prefer correctable inference over blank interrogation." (v0.2 S11 line 2319)
4. "Ask only where uncertainty could materially change the action." (v0.2 S11 line 2341)
5. "The system should learn not only what strategies work, but how to ask better questions." (v0.2 S11.10 line 2385)
6. "Discovery shapes the starting optimizer state. Because starting state shapes motion, discovery shapes safety." (v0.2 S11.13 lines 2423-2424)

### Material Requiring Refinement

- The seven-step loop (Retrieve → Infer → Propose → Confirm → Generate → Preserve → Learn) may be too long for Section 7. The core is Retrieve → Infer → Propose → Confirm. Generate, Preserve, and Learn are natural consequences rather than Discovery-specific steps. Consider presenting the core four and noting that generation, preservation, and learning follow.

### Material to Compress

- v0.2 S11.1 (Discovery Matters Because Structure Is Not Given): can be folded into the opening.
- v0.2 S11.2 (Initial vs. Runtime Discovery): compress to one paragraph. The distinction matters but does not need two subsections.
- v0.2 S11.3-S11.6 (Retrieve, Infer, Propose, Confirm as separate subsections): can be presented as a continuous narrative with the loop steps as bolded inline terms.
- v0.2 S11.7-S11.8 (Generate, Preserve): these are consequences of Discovery, not Discovery itself. Compress to a paragraph or defer to S8.
- v0.2 S11.14 (Campaign shows Discovery in practice): S5 already carries this. Compact callback only.

### Material to Defer

- Full Discovery Pattern Update specification → brief mention in S7; detailed treatment in S8 or Appendix A
- Full reasoning-object creation workflow → S8
- Schema for Discovery artifacts → S8
- Governance of inferred reasoning → S8 and S9

### Material to Retire

- v0.2 S11.15 (Discovery Is the Front Door to Reasoning) and S11.16 (From Discovery to a Running Example): these were transition paragraphs to S12, which no longer exists as a separate section. The transitions are no longer needed.

---

## Canonical Definitions

### Discovery

The process by which human intent, tacit assumptions, boundaries, and decision logic are converted into reusable reasoning state. Discovery captures reasoning before it disappears.

### Human Intent

What the human wants to accomplish, including goals, assumptions, constraints, preferences, quality standards, audience expectations, success criteria, confidence, evidence basis, decision logic, tradeoffs, and unresolved questions — often expressed partially, ambiguously, or implicitly.

### Tacit Reasoning

Reasoning that exists inside human judgment, experience, habit, and expertise but has not been made explicit, structured, or available to systems.

### Inferred Reasoning

A candidate reasoning state constructed by the system from available artifacts, context, and prior learning. Inferred reasoning must be surfaced and confirmed, not silently adopted.

### Confirmed Reasoning

Reasoning that has been reviewed, corrected, or accepted by a human. Confirmed reasoning is the output of the Propose → Confirm step.

### Reusable Reasoning Surface

A structured representation of confirmed reasoning that can be retrieved, inspected, and used by future systems and humans. A reasoning surface is reusable — rather than merely stored — when it carries scope, confidence, provenance, and applicability boundary: enough structure to be retrieved and applied in a future decision, not merely archived and forgotten. Reusable reasoning surfaces become part of future topography.

### Preserved Reasoning

The structured reasoning state (goal, policy, interpretation, premises, confidence, sufficiency rationale, decision, unresolved questions) that must survive action so that learning becomes possible.

---

## Required Conceptual Distinctions

### Discovery Versus Retrieval

Retrieval finds existing artifacts. Discovery elicits reasoning that may not yet exist in explicit form.

### Discovery Versus Prompting

Prompting asks for a task. Discovery uncovers why the task matters, what assumptions shape it, what boundaries constrain it, and what would make the result sufficient.

### Discovery Versus Requirements Gathering

Requirements gathering often captures desired outputs and constraints. Discovery must also capture the reasoning behind them: confidence, tradeoffs, unknowns, evidence basis, and decision logic.

### Discovery Versus Memory

Memory stores what was said or done. Discovery structures what must be preserved so future reasoning can use it.

### Discovery Versus Model Update Object

A Model Update Object preserves a learning transition after prediction error and investigation. Discovery can create reusable reasoning before an outcome exists.

### Discovery Versus Human Replacement

Discovery does not replace human judgment. It makes human judgment available to systems and future humans.

---

## Discovery Loop

### Core Loop: Retrieve → Infer → Propose → Confirm

**Retrieve:** Gather existing artifacts, prior decisions, policies, examples, performance data, and context. Retrieval should consider not only topical similarity but reasoning-state relevance.

**Infer:** Identify likely goals, assumptions, constraints, confidence levels, unresolved questions, and decision boundaries from the retrieved material. Inference is structured hypothesis formation, not guessing.

**Propose:** Offer a candidate reasoning state or interpretation for human review. A good proposal is specific enough to be useful and humble enough to be corrected. It should include confidence markers.

**Confirm:** Require the human to correct, accept, bound, or reject the inferred reasoning. Ask only where the answer could materially change the goal, boundary, investigation, sufficiency condition, or action. The loop re-enters when confirmation reveals new uncertainty or when correction changes the scope of what must be inferred. The system must not treat non-response or silence as confirmation.

### Natural Consequences: Generate → Preserve → Learn

After confirmation, the system can generate artifacts, preserve the reasoning state, and later learn from outcomes. These are consequences of Discovery rather than Discovery-specific steps. They are already covered by Sections 5, 6, and 8.

### Design Principle

"Do the reasoning work before asking the user to do it."

The system should not ask users to fill out a massive form. It should use available context to propose likely reasoning, then ask focused confirmation questions where the answer would materially change action.

---

## Five-Movement Narrative Plan

### Movement 1: Missing Reasoning Often Exists in People

Open from Section 6's handoff (~200 words).

The problem is not only that systems fail to learn after outcomes. It is also that key reasoning exists before action but remains inside conversations, assumptions, habits, and expert judgment.

A marketer knows which audience matters and why. A product manager knows which constraints are real and which are inherited. A compliance lead knows which claims require evidence. A sales team knows which objections recur. An operations lead knows which incidents have misleading symptoms.

This reasoning exists. It is not preserved in a form that future systems can use.

### Movement 2: Discovery Is Reasoning Capture, Not Intake

Distinguish Discovery from generic task intake, requirements gathering, prompting, and retrieval (~250 words).

Discovery is not "What do you want?" It is "What must be true for action to be justified?"

The system should not ask blank-form questions. It should not force the human to construct the reasoning state manually.

Show the contrast: blank form ("Who is your audience? What is your goal? What channel do you want?") vs. Discovery ("Based on existing materials, I think this is likely an RPM campaign for cardiology practice administrators optimized for qualified demo requests. Prior learning suggests workflow burden attracts attention but buying-stage readiness determines demo quality. Should we target organizations already evaluating RPM, or problem-aware operators who are not yet shopping?").

### Movement 3: Infer-Confirm Reduces Burden Without Pretending Omniscience

Introduce Retrieve → Infer → Propose → Confirm (~400 words).

This is the section's core explanatory movement.

Each step does distinct work:

- Retrieve: what does the organization already know?
- Infer: what can the system responsibly hypothesize from available material?
- Propose: make the inference visible and correctable.
- Confirm: let the human correct, accept, or bound the proposal. Ask only where uncertainty would change action.

The key insight: "The system should prefer correctable inference over blank interrogation."

Show why this matters for adoption: if the system asks too much, people will not use it. If the system infers silently, it may preserve false reasoning. The infer-confirm loop balances the two.

Acknowledge the risk: inferred reasoning can be wrong. Confirmation does not guarantee truth. Confirmed reasoning may still be stale, local, or biased. Confirmation reflects the confirmer's judgment at that moment, not organizational consensus or permanent truth. Because the system's proposal frames the space of correction, confirmed reasoning may carry anchoring bias. The purpose is not to eliminate error but to make assumptions visible, correctable, and reusable.

### Movement 4: Discovery Creates Reusable Reasoning Surfaces

Show how confirmed reasoning becomes future topography (~300 words).

Discovery can create or strengthen:

- confirmed goals;
- premise stacks;
- confidence notes;
- decision boundaries;
- applicability boundaries;
- unresolved questions;
- evidence requirements;
- policy links;
- escalation triggers;
- sufficiency conditions.

These are not mere notes. They are future landscape features. They change what becomes visible, accessible, represented, trusted, and connected in the next decision.

Connect to the five topography dimensions. Show that Discovery is topography design.

### Movement 5: Discovery Makes Human-Agent Systems Governable

Discovery helps future agents know what question they are answering, what boundaries apply, what assumptions are uncertain, and when to ask rather than act (~250 words).

Discovery also learns. The system can learn which interaction patterns produce lower friction, better reasoning objects, better artifacts, and better outcomes (Discovery Pattern Update). This makes the discovery process itself adaptive.

End by creating the need for Section 8:

If Discovery produces reusable reasoning, what system would be required to hold, retrieve, update, and govern it?

---

## Healthcare Campaign Callback

Use as a compact callback (~100 words), not a replay.

| Element | Content |
| --- | --- |
| What Discovery would ask | When you say the campaign should generate qualified demo requests, what makes a demo request qualified? Are we targeting active evaluators or problem-aware operators? |
| What it would infer | The team may be treating workflow burden as evidence of buying readiness. Prior learning suggests this assumption has limited support. |
| What it would require confirmation for | Buying-stage readiness as a qualification criterion. Whether the audience includes active evaluators or only problem-aware operators. |
| What would become reusable | A confirmed goal, audience interpretation with confidence boundary, evidence boundary on clinical claims, and unresolved question about readiness indicators. |

The reader already holds the campaign from S5. Do not re-derive it.

---

## Unsafe Tool-Action Callback

Use sparingly (~50 words) if helpful.

| Element | Content |
| --- | --- |
| What Discovery would ask | When this tool action succeeds, what downstream consequences should still block or require approval? |
| What it would preserve | Consequence boundaries and approval conditions before the tool is used. |
| What must remain for Section 8 | Implementation of consequence checks and approval gates. |

---

## Human Burden and Adoption

### Why Blank Forms Fail

If users must fill out every field manually, they will not do it. The reasoning architecture becomes theoretically complete but operationally dead.

### Why Silent Inference Fails

If the system infers intent without confirmation, it may preserve wrong reasoning. Confident-but-wrong reasoning objects can be worse than no reasoning objects.

### How Infer-Confirm Balances the Two

The system does the reasoning work first. It proposes. The human corrects. Friction is low because the human reviews rather than authors.

### Knowledge-Management Graveyard Risk

Section 6 acknowledged that structured learning repositories have historically failed to achieve reuse. Section 7 delivers the design response:

- Discovery shifts the creation burden from human authoring to system inference plus human confirmation.
- The system proposes reasoning objects from available artifacts and asks focused questions.
- The result is more complete, more structured, and less burdensome than manual creation.

This does not guarantee adoption. Confirmed reasoning can still be ignored, become stale, or be retrieved incorrectly. But the creation friction — the primary barrier to knowledge-management adoption — is structurally reduced.

Acknowledge the secondary risk: AI-inferred reasoning objects may be inaccurate, and trust in them must be earned rather than assumed.

---

## Boundary with Section 6

Section 6 owns:

- Learning after prediction error
- Model update
- Model Update Object
- Why learning must survive

Section 7 owns:

- Capturing reasoning before or during action
- Eliciting human intent
- Infer-confirm loop
- Reducing burden
- Making tacit reasoning reusable

Do not re-define learning. Do not re-explain MUOs except where Discovery may produce reasoning that later becomes part of them.

---

## Boundary with Section 8

Section 8: What It Would Take to Build This

Section 7 should not specify:

- Storage architecture
- APIs
- Schemas
- Permissions
- Object lifecycle
- Validation workflows
- Retrieval architecture
- Observability systems
- Complete product design

Section 7 may say these are required. Section 8 explains how to build them.

---

## Boundary with Section 9

Section 9: Boundaries, Objections, and Falsifiability

Section 7 should not fully litigate:

- Whether Discovery always works
- Whether humans will comply
- Whether inferred intent can be trusted
- Whether reasoning capture can be gamed
- Whether this creates surveillance or bureaucracy risks

It should acknowledge enough humility to avoid overclaiming and leave fuller objections for Section 9.

---

## Visual Plan

### Figure 7: Discovery Loop

Legacy SVG: `fig7_runtime_discovery_loop.svg` (shows the seven-step loop; superseded for v1.0).

v1.0 SVG: `fig7_discovery_loop.svg` (shows only the four-step canonical Discovery loop).

The displayed manuscript figure number is **Figure 7** because `fig6_reasoning_architecture_six_objects.svg` is allocated to Section 6 as Figure 6. The current manuscript contains Figures 1–5 displayed; Figure 6 is planned for Section 6.

Argumentative job: Show that Discovery is a specific, repeatable process — not a formality, not a one-shot intake — that converts tacit reasoning into structured, confirmed reasoning surfaces.

The figure shows:

```
Existing information surfaces + tacit human reasoning
  → Retrieve
  → Infer (provisional hypothesis)
  → Propose (visible, correctable)
  → Confirm (correct · reject · qualify · bound; re-entry on new uncertainty)
  → Reusable reasoning surface (scope, confidence, provenance, applicability boundary)
  → Future topography
```

Generate, Preserve, and Learn appear as muted downstream consequences, not loop stages.

Place Figure 7 after the Retrieve → Infer → Propose → Confirm loop is introduced (Movement 3).

### Optional Table

Possible table role: contrast ordinary intake with Discovery.

| Ordinary intake asks | Discovery asks | Why it matters for future reasoning |
| --- | --- | --- |
| What do you want? | What goal does this serve, and what would make the result sufficient? | Captures the sufficiency condition, not just the task. |
| Who is the audience? | Which audience interpretation are we using, and at what confidence? | Preserves the premise and its boundary. |
| What evidence do you have? | Which claims require evidence that we do not yet have? | Identifies evidence gaps before they become premature sufficiency. |
| What constraints apply? | Which policy must be connected to this task to prevent a compliance or safety failure? | Makes policy behaviorally effective. |
| What happened last time? | Which prior premise held, which failed, and what should change? | Connects prior learning to the current decision. |
| What do you need? | What reasoning must survive this task so the next cycle starts smarter? | Shifts from artifact production to reasoning preservation. |

**Recommendation:** Include this table. It has a distinct argumentative job from Figure 7. Figure 7 shows the process; the table shows how Discovery questions differ from ordinary questions. Both add comprehension.

Place the table after Movement 2 (Discovery Is Reasoning Capture, Not Intake), before Movement 3 (the loop itself). This placement lets the reader feel the difference before learning the mechanism.

---

## Citation Inventory

### Existing Citations

- Horvitz, 1999 — mixed-initiative interaction (cited in v0.2 S15)
- Amershi et al., 2019 — human-AI interaction guidelines (cited in v0.2 S15)

### Missing Citation Needs

Per the citation workstream (doctrine Section 12):

- **Mixed-initiative interaction:** Horvitz 1999 — should be cited inline in S7 where the infer-confirm loop is introduced. Currently only in S15.
- **Cognitive load:** Sweller 1988 — "Do the reasoning work before asking the user to do it" is essentially a cognitive load argument.
- **Naturalistic decision-making:** Klein 1998 — recognition-primed decisions are relevant to how Discovery surfaces expert reasoning.
- **Tacit knowledge:** Nonaka & Takeuchi 1995 — canonical reference for tacit-to-explicit knowledge conversion. Relevant to the claim that Discovery makes tacit reasoning available.
- **KM failure:** Markus 2001, Weber et al. 2001 — directly addresses the graveyard risk.

### Framework Propositions Rather Than Empirical Claims

- "Discovery reduces user burden while improving reasoning capture" — testable claim, not yet validated
- "Infer-confirm produces better reasoning objects than blank interrogation" — testable claim
- "Discovery Pattern Updates improve interaction quality over time" — testable claim

---

## Theory Risks

### Discovery as Bureaucracy

If Discovery becomes too heavy, users will bypass or ignore it. The infer-confirm loop is the design response: the system does most of the work.

### Discovery as False Inference

If the system infers intent without confirmation, it may preserve wrong reasoning. Confirmed reasoning may still be wrong, but it is at least visible and correctable.

### Discovery as User Interrogation

If the system asks too many questions, users will abandon it. The rule: ask only where uncertainty would materially change action.

### Discovery as Memory

If Discovery only stores answers, it misses reasoning. It must capture premises, confidence, boundaries, and decision logic — not just outputs.

### Discovery as Surveillance

Capturing reasoning can feel like monitoring people rather than supporting work. The framing should be: Discovery makes human judgment available to future systems, not monitored by current systems.

### Discovery as Overconfidence

Confirmed reasoning may still be wrong, stale, or local. The MUO confidence and applicability-boundary fields are protections, but they are not guarantees.

### Discovery as Hidden Governance

If Discovery encodes constraints invisibly, it can shape behavior without accountability. The infer-confirm loop requires that inferred reasoning be visible and correctable.

### Discovery as Implementation Architecture

The section must not turn into product design. Architecture belongs in Section 8.

---

## Drafting Constraints

- Do not re-explain Section 6's learning loop.
- Do not turn Discovery into a requirements-gathering checklist.
- Do not make Discovery sound like a form.
- Do not let the system infer intent without human confirmation.
- Do not overburden the user.
- Do not claim Discovery eliminates ambiguity.
- Do not imply captured reasoning is always true.
- Keep human judgment visible.
- Show Discovery as topography design.
- Keep Discovery distinct from MUOs.
- Keep implementation details for Section 8.
- End by creating the need for build architecture.
- Avoid manuscript self-reference ("this section," "the prior section").
- Let the reader feel why Discovery matters before naming the loop.

---

## Transition into Section 8

The closing bridge should be conceptually:

If Discovery produces reusable reasoning and learning preserves model updates, the next question is: what would it take to build a system that holds, retrieves, updates, and governs these reasoning objects?

Do not draft as final prose. Treat as the closing conceptual move.

---

## Recommended Section Length

~1,500-2,500 words.

v0.2 S11 is ~2,700 words. v1.0 S7 should be somewhat shorter because S5 already demonstrates Discovery in action (the reasoning-state path is Discovery operating). The section should focus on explaining why Discovery is necessary and how the infer-confirm loop works, without replaying the full campaign walkthrough.

Reader comprehension governs.

---

## Readiness Assessment

The source packet answers all twelve readiness questions:

1. **What is Discovery?** The process by which human intent, tacit assumptions, boundaries, and decision logic are converted into reusable reasoning state.
2. **Why is Discovery necessary after Section 6?** Learning captures reasoning after outcomes. Discovery captures reasoning before it disappears.
3. **What human reasoning disappears without Discovery?** Intent, assumptions, confidence, boundaries, constraints, decision logic, tacit knowledge, and unresolved questions.
4. **How is Discovery different from retrieval?** Retrieval finds existing artifacts. Discovery elicits reasoning that may not yet exist in explicit form.
5. **How is Discovery different from prompting?** Prompting asks for a task. Discovery uncovers why the task matters.
6. **How is Discovery different from requirements gathering?** Requirements capture desired outputs. Discovery captures the reasoning behind them.
7. **Why is confirmation necessary?** Without it, the system may preserve false inferences. Infer-confirm makes assumptions visible and correctable.
8. **How does Discovery reduce user burden?** The system retrieves, infers, and proposes first. The human reviews and corrects rather than authoring from scratch.
9. **How does Discovery create reusable reasoning surfaces?** Confirmed goals, premises, boundaries, confidence, and unresolved questions become future landscape features.
10. **How does Discovery shape future topography?** By making tacit reasoning visible, accessible, represented, confidence-bearing, and connected.
11. **What remains for Section 8?** Implementation architecture: storage, retrieval, governance, lifecycle, and system design.
12. **What objections remain for Section 9?** Whether Discovery always works, whether humans comply, whether inferred intent can be trusted, whether this creates surveillance risks.
