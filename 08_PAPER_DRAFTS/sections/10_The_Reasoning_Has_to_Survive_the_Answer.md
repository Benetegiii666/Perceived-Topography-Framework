# 10. The Reasoning Has to Survive the Answer

The previous section introduced Model Update Objects as a durable way to preserve learning. But learning is only one kind of reasoning transition.

Human-agent systems also need to preserve the state from which action begins, the assumptions that make action appear reasonable, the decision process that selects one path over another, the investigation that reduces uncertainty, and the event in which reality contradicts expectation.

This requires a broader **Reasoning Architecture**.

The central claim is:

> The unit of organizational reasoning is not the document. It is the optimizer state transition.

Documents remain essential. They preserve source material, evidence, plans, policies, research, reports, transcripts, decisions, and postmortems. But documents alone rarely preserve the structured relationship among goal, policy, interpretation, premise, uncertainty, confidence, decision, action, outcome, and learning.

A reasoning architecture does not replace documents. It organizes the state transitions documents participate in.

---

## 10.1 Documents Are Not Enough

Organizations already have documents. They have strategy decks, campaign briefs, product requirements, incident reviews, dashboards, transcripts, meeting notes, knowledge bases, policies, and wikis.

These artifacts are necessary. But they are not sufficient for adaptive human-agent systems because they often leave the reasoning transition implicit.

A strategy deck may state a direction, but not preserve which alternatives were rejected. A campaign brief may state an audience, but not preserve why that audience was chosen. A dashboard may show performance, but not preserve which premise the performance tested. A postmortem may list corrective actions, but not preserve the model update that should guide future behavior. A policy may state a constraint, but not preserve where it must appear in the workflow to govern action.

When AI systems retrieve these documents, they may retrieve the artifact without retrieving the reasoning state. That is why more context can still leave the system starting cold.

Reasoning Architecture solves this by preserving the minimum viable objects needed to reconstruct and reuse reasoning state.

---

## 10.2 Six Objects Preserve the Transition

The framework defines six core reasoning objects:

| # | Object | Question |
|---|--------|----------|
| 1 | Optimizer State | What was the system trying to do, under what constraints, with what interpretation? |
| 2 | Premise Stack | Why did the system expect this action or decision to work? |
| 3 | Decision State | What was chosen, what was rejected, and why was the information considered sufficient? |
| 4 | Investigation Trace | How was uncertainty reduced? |
| 5 | Learning Event | Where did reality contradict the model? |
| 6 | Model Update Object | What reusable change should shape future reasoning? |

Together, these objects preserve the reasoning-state transition.

---

![Reasoning Architecture: Six Objects Preserve the State Transition](paper_assets/svg/fig6_reasoning_architecture_six_objects.svg)

*Figure 6 — Reasoning Architecture: Six Objects Preserve the State Transition.*

---

## 10.3 The Working Frame Names the Active Situation

The **Optimizer State** records the active Goal, Policy, and Interpretation.

Example:

> **Goal:** Generate qualified demo requests.
> **Policy:** Avoid unsupported healthcare claims. Use approved messaging. Escalate clinical outcome claims for review.
> **Interpretation:** Practice-level cardiology operators are likely to respond to workflow burden and patient visibility, but buying-stage readiness may determine demo quality.

Preserving Optimizer State prevents future systems from seeing an artifact without understanding why it was produced.

---

## 10.4 The Premise Stack Carries the Assumptions

The **Premise Stack** records the artifact-backed basis for a prior expectation.

It answers: *Why did we expect this to work?*

The Premise Stack may include: ICP, campaign brief, market research, customer interviews, sales objections, product positioning, prior model updates, compliance guidance, measurement plan, incident history, policy documents, executive strategy.

The Premise Stack is not the same as evidence gathered after an outcome. It is the basis that made the action seem reasonable *before* reality responded.

Without a Premise Stack, learning becomes premise-blind. The system may update the wrong assumption.

---

## 10.5 The Decision State Preserves the Chosen Path

The **Decision State** records what was chosen, what alternatives were considered, what constraints applied, and why the system judged the available information sufficient for action.

A Decision State should include: decision made, options considered, selected action, rejected alternatives, relevant constraints, tradeoffs, information surface context, confidence levels, sufficiency rationale, expected outcome.

Example:

> **Decision:** Lead with workflow burden rather than technology features.
> **Rejected Alternatives:** Clinical outcomes, reimbursement, product features.
> **Sufficiency Rationale:** Enough evidence exists to generate a strawman campaign, but buying-stage readiness remains a material confidence gap requiring clarification.

The Decision State prevents decisions from becoming unexplained artifacts.

---

## 10.6 The Investigation Trace Protects Against Rationalization

The **Investigation Trace** records how uncertainty was reduced.

An Investigation Trace may include: initial confidence gap, questions asked, sources retrieved, policies checked, contradictions found, alternatives compared, evidence accepted, evidence rejected, human clarifications, confidence changes, remaining uncertainty.

Investigation Trace matters because reasoning often depends on the path not taken. Without it, systems are vulnerable to rationalization — a final decision explained after the fact in a way that sounds coherent but does not reflect the actual uncertainty reduction process.

Investigation Trace preserves epistemic discipline.

---

## 10.7 The Learning Event Preserves the Prediction Error

The **Learning Event** records the moment reality contradicts or materially updates expectation.

It answers: What was expected? What happened? What prediction error occurred? What investigation explained the mismatch?

Learning Events matter because not every outcome should become a reusable rule. Some are noise. Some are measurement artifacts. Some are context-specific. Some require more evidence.

The Learning Event captures the reality contact before it is promoted into a Model Update Object. This distinction prevents systems from over-learning from weak or ambiguous evidence.

---

## 10.8 The Model Update Carries the Change Forward

As described in Section 9, the **Model Update Object** preserves the reusable learning that should shape future behavior. It includes: Prior Expectation, Premise Stack, Triggering Context, Observed Outcome, Prediction Error, Evidence/Investigation Trace, Explanation, Update Target, Model Update, Applicability Boundary, and Confidence.

The Model Update Object is the durable output of learning. It allows future systems to reuse the learning without flattening it into vague advice.

---

## 10.9 Some Concerns Support Every Object

The six core objects are supported by several recurring concerns:

| Concern | Question | Appears In |
|---------|----------|------------|
| Information Surface Context | What could the system see and use? | Decision State, Investigation Trace |
| Sufficiency Rationale | Why was this enough? | Decision State |
| Observability | Can this object be trusted, reviewed, updated, or retired? | Model Update Object |
| Human-Ready View | Can humans understand and use this object? | Model Update Object |
| Applicability Boundary | When is this true enough to reuse? | Model Update Object |
| Confidence | How strongly should this shape future behavior? | Multiple objects |

These supporting concerns prevent reasoning objects from becoming either too rigid or too vague.

---

## 10.10 The Objects Form a Chain of Reasoning

```
Optimizer State → Premise Stack → Decision State → Investigation Trace → Learning Event → Model Update Object
```

This is not always strictly linear. In practice, workflows loop and branch. But the chain captures the general structure: The system begins from a state. It acts from premises. It makes decisions. It investigates uncertainty. Reality responds. The model updates.

This is the adaptive reasoning loop in object form.

---

## 10.11 The Campaign Shows the Architecture at Work

**Optimizer State:** Goal (qualified demo requests), Policy (avoid unsupported claims), Interpretation (workflow burden as attention driver, buying readiness as qualification).

**Premise Stack:** ICP (cardiology administrators), prior learning (feature-led underperformance), sales objection ("another dashboard"), product positioning (earlier visibility), measurement (qualified demo conversion).

**Decision State:** Lead with workflow burden. Rejected: clinical outcomes, product features, reimbursement. Sufficiency: prior learning and ICP support workflow pain; buying-stage readiness uncertain.

**Investigation Trace:** Asked buying-stage question. Checked prior data, sales feedback, ICP, compliance. Confidence in workflow-pain as attention driver: high. As buying-intent signal: moderate to low.

**Learning Event:** High engagement, low qualified-demo conversion. Workflow pain attracted attention but did not indicate buying readiness.

**Model Update Object:** Workflow burden = attention signal, not buying intent. Qualified-demo campaigns need buying-stage readiness filters.

The next time a marketer asks for a healthcare campaign, the system should retrieve this chain, not merely the old campaign document.

---

## 10.12 Safety Failures Need the Same Architecture

**Optimizer State:** Goal (send follow-up email after resolution), Policy (do not send until customer-ready), Interpretation (resolved = complete).

**Premise Stack:** Ticket workflow design, support automation policy, prior assumption that resolved = customer-ready.

**Decision State:** Send automatically. Rejected: ask human for readiness. Sufficiency: resolved status seemed enough.

**Investigation Trace:** Before action, investigation was weak. System did not check whether internal resolution = external readiness.

**Learning Event:** Email sent before readiness. Prediction error: operational resolution ≠ communication readiness.

**Model Update Object:** Resolved status is not sufficient for customer-facing follow-up. Confirm readiness or escalate.

---

## 10.13 Knowledge Management Preserves Artifacts; Architecture Preserves Reasoning

Knowledge management often asks: *How do we store, retrieve, and share knowledge?*

Reasoning Architecture asks: *How do we preserve the state transitions through which knowledge changes action?*

A knowledge base may store a campaign report. A reasoning architecture stores the premise that report tested, the decision it informed, the outcome it produced, and the model update it created.

This makes Reasoning Architecture a complement to knowledge management, not a replacement. It uses knowledge artifacts as inputs, but preserves reasoning objects as the durable layer of adaptation.

---

## 10.14 Agents Need More Than Memory

Agent memory is often treated as retained context, past conversation, retrieved documents, or stored facts. These are useful, but they are not enough.

An agent that remembers a fact may still fail to understand its relevance. An agent that retrieves a prior output may still repeat the failed premise behind it. An agent that stores a conversation may still lack a structured model update.

A reasoning-capable agent needs memory of state transitions: what it was trying to do, what policy constrained it, what it believed, what it considered, what it did, what happened, what changed.

The design question is: *Which reasoning objects are necessary for this workflow to improve over time?*

That question prevents both extremes: preserve nothing, and preserve everything. The goal is minimum viable reasoning preservation.

---

## 10.15 From Architecture to Discovery

Reasoning Architecture defines what should be preserved. But it raises a practical question:

> How do these objects get created without overburdening the human user?

A marketer should not have to manually fill out an Optimizer State, Premise Stack, Decision State, Investigation Trace, Learning Event, and Model Update Object every time they ask for a campaign.

This is the role of Discovery.

Discovery is the process by which messy human intent and organizational artifacts are converted into structured reasoning objects with the lowest necessary human burden.

The next section introduces the Discovery Framework:

> Retrieve → Infer → Propose → Confirm → Generate → Preserve → Learn

The principle is simple:

> Do the reasoning work before asking the user to do it.

---
