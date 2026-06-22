# 9. Lessons Need Objects

The previous section defined learning as an evidence-supported model update triggered by prediction error.

That definition creates a practical problem.

Where does the learning go?

If learning remains in a meeting, it becomes memory. If it remains in a postmortem, it becomes documentation. If it remains in a Slack thread, it becomes searchable residue. If it remains in one person's head, it becomes expertise. If it is summarized vaguely, it becomes folklore.

None of these are sufficient for human-agent systems that must reuse learning across time, teams, workflows, and agents.

This section introduces the **Model Update Object**.

A Model Update Object is a bounded, reusable record of learning. It preserves the prior expectation, the premise stack that produced that expectation, the observed outcome, the prediction error, the evidence-supported explanation, the model update, the applicability boundary, and the confidence level.

Its purpose is not simply to store what happened. Its purpose is to change future reasoning.

---

## 9.1 Ordinary Documentation Does Not Carry the Change

Organizations already document many things. They write briefs, reports, incident reviews, campaign analyses, product requirements, sales notes, meeting summaries, dashboards, and postmortems. These artifacts matter. The framework does not replace them.

But ordinary documentation often fails to preserve the exact structure needed for future learning.

A campaign report may say: "Workflow messaging performed well." But a future system needs to know: Performed well against which goal? With which audience? Compared to what expectation? Under what channel conditions? With what offer? At what buying stage? What did performance mean? What should change next time?

An incident postmortem may say: "Restarting the service caused downstream data loss." But a future system needs to know: Under what system state? What prior expectation made restart seem safe? What signal was misread? Which policy failed? Which future trigger should block or escalate restart?

Ordinary documentation often preserves conclusions without preserving the reasoning transition that produced them.

The Model Update Object is designed to preserve that transition.

---

## 9.2 A Lesson Needs Three Layers

A Model Update Object has three layers:

```
Model Update Object = Core Learning Payload + Observability Envelope + Human-Ready View
```

---

## 9.3 The Core Payload Holds the Source of Truth

The first layer is the **Core Learning Payload** — the source-of-truth layer.

It contains eleven fields:

| # | Field | Prevents |
|---|-------|---------|
| 1 | Prior Expectation | No learning delta |
| 2 | Prior Basis / Premise Stack | Premise-blind learning |
| 3 | Triggering Context / Action | Context collapse |
| 4 | Observed Outcome | Vague outcome memory |
| 5 | Prediction Error | Outcome mistaken for learning |
| 6 | Evidence / Investigation Trace | Rationalized learning |
| 7 | Explanation | Raw evidence without model change |
| 8 | Update Target | Unlocated learning |
| 9 | Model Update | Lesson too vague to guide action |
| 10 | Applicability Boundary | Overgeneralized learning |
| 11 | Confidence | False certainty |

**Prior Expectation** records what the optimizer believed would happen before action. Without it, the system cannot know what changed.

**Prior Basis / Premise Stack** records why the expectation seemed reasonable. Without it, the system may learn the wrong lesson from the right evidence. The premise stack answers: *Why did we expect this to work?*

**Triggering Context / Action** records what was done and under what conditions. Without it, a future system may overgeneralize from one context to all contexts.

**Observed Outcome** records what happened with enough specificity to support investigation.

**Prediction Error** records the mismatch between expectation and outcome. This is the hinge of learning.

**Evidence / Investigation Trace** records what evidence was examined. Without it, learning becomes rationalization.

**Explanation** states why the prediction error occurred based on evidence. Without it, evidence remains raw data without meaning.

**Update Target** identifies which part of the optimizer model should change (Goal, Policy, or Interpretation). Without it, learning is vague.

**Model Update** states the reusable change to future reasoning. A good model update is specific enough to change behavior but bounded enough to avoid overgeneralization.

**Applicability Boundary** states when the update should and should not apply. Without it, useful learning can become harmful dogma.

**Confidence** records how strongly the system should trust the update. Without it, weakly supported lessons become false certainty.

The Confidence field in a Model Update Object records how strongly the learning should shape future behavior. It is related to the topography dimension Confidence, but it is not identical: the topography dimension concerns perceived trustworthiness during reasoning, while the Model Update Object field concerns the reliability of a completed learning update.

---

## 9.4 The Envelope Makes the Update Governable

The second layer is the **Observability Envelope** — the trust, audit, and lifecycle layer.

It may include: Object ID, Source Learning Event, Created Date, Created By, Owner/Steward, Source Artifact References, Evidence References, Version, Status, Confidence History, Supersedes/Superseded By, Usage Log, Validation Log, Last Reviewed Date, Related Updates / Conflict Flags.

Recommended status values: Provisional, Validated, Deprecated, Superseded, Rejected.

This layer matters because model updates should not become permanent doctrine by default. They need lifecycle. A model update may be provisional. It may later be validated. It may be superseded by stronger evidence. It may be deprecated when conditions change. It may conflict with another update and require investigation.

The Observability Envelope prevents: *Stale learning treated as current truth.*

---

## 9.5 The Human View Makes the Lesson Usable

The third layer is the **Human-Ready View** — the usability layer.

It may include: Title, One-Line So What, What Changed, Assumption Changed, Use This When, Do Not Use This When, Confidence/Caveat, Recommended Future Check.

Example:

> **Title:** Workflow Pain Drives Attention, Not Qualified Demo Intent
> **One-Line So What:** For cardiology RPM campaigns, workflow-burden messaging gets attention, but qualified-demo campaigns need buying-stage filters.
> **Use This When:** Building practice-level cardiology RPM campaigns optimized for qualified demo requests.
> **Do Not Use This When:** The campaign goal is awareness, education, or executive thought leadership.

The Human-Ready View is not the source of truth. It is a usability layer. The Core Learning Payload remains authoritative.

This distinction matters because human-readable summaries can drift. A short "so what" may be useful, but future systems should still be able to inspect the underlying expectation, evidence, explanation, boundary, and confidence.

---

## 9.6 A Model Update Shows the Shape of Learning

Below is an example from the healthcare campaign scenario.

> **Title:** Workflow Pain Drives Attention, Not Qualified Demo Intent
>
> **Prior Expectation:** Workflow-pain-led messaging will generate qualified demo requests from cardiology practice administrators.
>
> **Premise Stack:** ICP (cardiology practice administrators), prior campaign learning (feature-led underperformance), sales objections ("another dashboard"), product positioning (earlier visibility without staff burden), goal (qualified demo requests).
>
> **Triggering Context:** Launched workflow-pain-led RPM campaign targeting practice-level cardiology operators.
>
> **Observed Outcome:** Strong engagement and moderate demo requests, but lower-than-expected qualified-demo rate.
>
> **Prediction Error:** Workflow pain attracted attention but did not reliably indicate buying readiness.
>
> **Evidence:** Engagement above benchmark; sales feedback indicated problem-aware but not-shopping leads; demo qualification showed weak evaluation readiness; message-level performance favored workflow burden language; prior feature-led comparison supported attention benefit.
>
> **Explanation:** Practice-level operators resonated with workflow burden, but the message reached many problem-aware prospects not yet actively evaluating RPM.
>
> **Update Target:** Interpretation / Action Model
>
> **Model Update:** For cardiology RPM campaigns, workflow burden should be treated as an attention signal, not sufficient buying intent. Campaigns optimized for qualified demos should include buying-stage readiness filters.
>
> **Applicability Boundary:** Applies to practice-level cardiology RPM campaigns optimized for qualified demo requests. Does not automatically apply to awareness campaigns, executive campaigns, or other specialties without validation.
>
> **Confidence:** Medium-high. Needs validation in at least one additional campaign.
>
> **Status:** Provisional

This object can now shape future discovery. When the next marketer says "I want to do a healthcare campaign," the system can retrieve the model update and ask: "Are we targeting organizations already evaluating RPM, or creating demand among problem-aware but not-yet-shopping buyers?"

The system is not merely retrieving an old campaign. It is reusing learning.

---

## 9.7 Objects Prevent Learning From Becoming Folklore

Model Update Objects are designed to prevent several common failure modes:

1. **Folklore Update** — a story accepted as truth without evidence
2. **Premise-Blind Update** — learning from outcome without identifying which assumption failed
3. **Overgeneralized Update** — a lesson from one context applied everywhere
4. **Stale Update** — an old lesson active after conditions change
5. **Confidence Inflation** — a weakly supported lesson becomes doctrine
6. **Misclassified Update Target** — the system changes the wrong part of the model
7. **Policy Laundering** — a preference disguised as a rule
8. **Human-Ready Drift** — a simplified summary changes the meaning
9. **Retrieval Bias** — the system retrieves a topically similar update that does not actually apply
10. **Contradiction Suppression** — a new outcome conflicts with a prior update, but the conflict is ignored

---

## 9.8 Model Updates Reshape the Landscape

Model Update Objects are not just records. They reshape future topography.

They make prior learning visible. They make failed premises accessible. They represent learning in reusable form. They assign confidence. They connect past outcomes to future decisions.

Before the update:

> Healthcare campaign → retrieve old campaign → copy workflow-pain message → generate assets.

After the update:

> Healthcare campaign → retrieve prior model update → infer workflow pain as attention signal → detect buying-stage confidence gap → ask readiness question → generate better campaign.

The object changes motion. This is why Model Update Objects are a structural component of the framework.

---

## 9.9 From Lessons to Architecture

A Model Update Object preserves one kind of reasoning transition: learning.

But human-agent systems need more than learning records. They also need to preserve optimizer state, premise stacks, decision states, investigation traces, and learning events.

Together, these objects form a broader reasoning architecture.

The next section introduces that architecture.

Its central claim:

> The unit of organizational reasoning is not the document. It is the optimizer state transition.

---
