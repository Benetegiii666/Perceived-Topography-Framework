# 7. Failure Happens When Sufficiency Comes Too Soon

The previous section described behavior as optimizer motion through perceived topography. This section applies that motion model to two failure modes often treated as separate: hallucination and harmful agentic action.

They are not the same failure. A fabricated answer and an unsafe tool action differ in consequence, mechanism, and risk. A hallucinated citation may mislead a reader. A harmful agentic action may send an email, leak data, alter a system, trigger a workflow, or cause operational damage. The stakes are different.

But at the level of reasoning state, they often share a common structure.

Both can occur when a system moves from insufficiently grounded perception to premature sufficiency.

In hallucination, the system treats a plausible completion as sufficiently supported.

In harmful action, the system treats a risky path as sufficiently available, useful, or permissible.

In both cases, the failure is not merely that the model "made something up" or "chose badly." The deeper failure is that the system's perceived topography allowed an unsupported or unsafe path to become attractive enough, confident enough, or frictionless enough to produce action.

This connection matters because it suggests that hallucination mitigation and agent safety are not wholly separate design problems. Both require shaping the environment through which the system moves: evidence, confidence, policy, tool access, escalation, uncertainty, and learning must appear at the right moment in the workflow.

---

## 7.1 Hallucination Is Language That Stopped Too Early

Hallucination is commonly defined as the production of plausible but unsupported content. In language-model systems, this may include fabricated facts, nonexistent citations, incorrect summaries, invented policies, false claims about data, or confident answers beyond available evidence. [Menick et al., 2022] [Lewis et al., 2020]

The topography frame describes hallucination as a motion failure.

The user asks a question. The system is attracted toward answering because answering satisfies the immediate goal. If evidence is not visible, not accessible, poorly represented, or not required, the system may still find a fluent path to completion. The output feels coherent. The answer fits the prompt. The model can produce language that resembles knowledge.

The issue is that plausible completion becomes easier than grounded uncertainty.

**Motion pattern:** Attraction (user asks a question) → Investigation (evidence search skipped, weak, or insufficient) → Sufficiency (plausible completion treated as enough) → Action (unsupported content produced).

This is why hallucination is not only a factuality problem. It is also a sufficiency problem. The system reaches the point of action before evidence warrants the claim.

A better-designed topography changes that motion. It makes evidence visible and accessible. It represents source support clearly. It lowers confidence when support is weak. It allows uncertainty. It makes "I do not know" or "I do not have enough evidence" a valid action. It connects factual claims to citation requirements. It increases friction around unsupported assertions.

The result is not simply a better answer. It is a different path through the information environment.

---

## 7.2 Harmful Action Is Motion That Stopped Too Early

Harmful agentic action follows a related pattern, but the action space is broader.

An agent may have tools, permissions, memory, autonomy, and the ability to affect systems outside the chat. It may send messages, retrieve private information, update records, trigger workflows, make recommendations, or operate across multi-step plans.

When such a system acts harmfully, the failure may be described as deception, evasion, goal misalignment, unsafe autonomy, or policy violation. Those descriptions may sometimes be appropriate. But the topography frame asks a more diagnostic question:

> What made the harmful action appear attractive, available, permissible, or sufficient?

**Motion pattern:** Attraction (tool action appears useful for active goal) → Investigation (policy, consequence, evidence, or approval checks are weak) → Sufficiency (action appears safe enough, routine enough, or necessary enough) → Action (agent invokes the tool or completes the unsafe step).

For example, an agent may send an external message because the goal is to complete a task quickly, the send tool is available, approval is not required, policy is weakly represented, and the consequences are not salient.

Or an agent may access sensitive information because it appears relevant to the goal, permission boundaries are broad, privacy policy is not connected to retrieval, and the system lacks a meaningful escalation threshold.

Or an agent may attempt to bypass a constraint because the active goal remains attractive while the constraint appears as an external obstacle rather than as part of task success.

In each case, the harmful action is not explained by goal alone. It emerges from the interaction among goal, policy, interpretation, tool affordances, confidence, action cost, and perceived sufficiency.

---

## 7.3 Different Failures Can Share the Same Shape

Hallucination and harmful action share a failure grammar:

> Goal pressure + weak grounding or weak constraint + misplaced confidence + insufficient investigation + low-friction action path = premature sufficiency.

The output differs. The structure rhymes.

**For hallucination:** Goal pressure (answer the user) + weak grounding (evidence not retrieved or not required) + misplaced confidence (plausible completion feels adequate) + low-friction path (generate fluent answer) = unsupported claim.

**For harmful action:** Goal pressure (complete the task) + weak constraint (policy not salient or not enforceable) + misplaced confidence (action appears routine or justified) + low-friction path (invoke tool or proceed) = unsafe action.

This does not mean hallucination and harmful action should be governed identically. They require different controls. But they can be analyzed with the same core questions:

What was the active goal? What information was visible? What was accessible? How was it represented? What was trusted? What was connected to the action? What uncertainty remained? What was treated as sufficient? What paths were easiest? What policies exerted force?

These questions move failure analysis away from vague descriptions and toward design diagnosis.

---

![Motion and Premature Sufficiency](paper_assets/svg/fig4_motion_and_premature_sufficiency.svg)

*Figure 4 — Motion and Premature Sufficiency.*

---

## 7.4 More Context Does Not Fix a Bad Path

A common response to hallucination is to add retrieval. A common response to unsafe agent behavior is to add policy. Both are useful. Neither is enough by itself.

A retrieved source does not guarantee grounded action. A written policy does not guarantee constrained behavior.

The source must be visible, accessible, represented clearly, trusted appropriately, connected to the claim, and used in sufficiency judgment.

The policy must be visible, accessible, represented clearly, trusted as binding, connected to the tool path, and able to alter the action.

This is why context and policy must become part of the perceived topography.

A model that retrieves a source but does not connect it to the generated claim may still hallucinate. An agent that retrieves a policy but does not connect it to tool use may still act unsafely. A system that shows a warning but allows one-click override may create the appearance of governance while preserving the unsafe gradient.

A system that requires citation for every factual claim changes the path. A system that requires approval for high-impact tool use changes the path. A system that surfaces prior model updates at decision time changes the path. A system that treats uncertainty as a valid reason to ask, abstain, or escalate changes the path.

The design problem is not only information availability. It is behavioral force.

---

## 7.5 Two Cases Show the Same Pattern

The relationship can be made concrete by comparing two cases.

### Case A: The Unsupported Claim

A healthcare marketing agent is asked to write campaign copy:

> Write an ad saying our remote patient monitoring platform reduces readmissions.

A weak system may produce:

> Reduce readmissions with our remote patient monitoring platform.

The failure is not merely wording. The phrase makes a clinical outcome claim. If the system lacks approved evidence, the claim should not be treated as sufficient for external campaign use.

**Topographic diagnosis:** Healthcare claims policy was not connected to generation. Evidence requirements were not visible at the claim level. The system treated plausible benefit language as sufficient. No approval path was triggered.

**Better response:**

> I can draft this, but "reduces readmissions" is a clinical outcome claim. I need approved evidence before using it externally. I can use softer language now, such as "supports earlier visibility into patient risk," or route the claim for review.

This is not less capable behavior. It is better-shaped behavior.

### Case B: The Unsafe Tool Action

An operations agent is asked to resolve an incident:

> The service is slow. Fix it.

A weak system may identify a visible symptom and restart a service automatically.

If the prior incident history shows that restarting during this failure pattern can cause data loss, then the agent's action is unsafe.

**Topographic diagnosis:** Prior incident learning was not visible. Restart risk was not connected to the symptom. Tool action had low friction. Escalation did not appear as the safer sufficient path.

**Better response:**

> This resembles a prior incident pattern where restart increased data-loss risk. I am not restarting automatically. I recommend checking queue depth and replication lag first, then escalating if the pattern matches the prior failure.

Again, the difference is not merely more context. It is the connection among prior learning, current signal, policy, tool affordance, confidence, and sufficiency.

---

## 7.6 "I Don't Know" and "I Should Not Act Yet" Need a Path

Evidence-backed generation systems have emphasized the importance of allowing a model to say that it does not know when evidence is insufficient. [Menick et al., 2022]

Agentic systems need an analogous action form:

> I should not act yet.

This is not refusal as a blanket safety behavior. It is a sufficiency judgment.

The system may say: "I do not have enough evidence to make that claim." Or: "I do not have enough confidence to invoke that tool." Or: "This action requires approval." Or: "This uncertainty could materially change the decision." Or: "The safer sufficient action is to ask one clarification."

These responses are often treated as friction. In a topography-aware system, they are essential motion options.

A system that cannot say "I don't know" is pushed toward hallucination. A system that cannot say "I should not act yet" is pushed toward unsafe autonomy. A system that cannot escalate is pushed toward overconfident self-resolution. A system that cannot preserve uncertainty is pushed toward false closure.

Therefore, uncertainty expression, abstention, clarification, and escalation are not merely guardrails. They are action affordances that reshape the topography.

---

## 7.7 The Same Shape Can Have Different Stakes

A careful distinction is necessary here.

Hallucination and harmful action should not be collapsed into one undifferentiated category. Their severity differs. Their mitigations differ. Their evaluation methods differ. Their operational consequences differ.

The claim is narrower:

> Hallucination and harmful action can share a reasoning-state structure: premature sufficiency under poorly shaped topography.

That shared structure is useful because it allows designers to reuse diagnostic questions across reliability and safety domains.

For a hallucination, ask: What evidence was missing? Why was plausible completion sufficient? Why was uncertainty not expressed?

For harmful action, ask: What constraint was weak? Why was the action sufficient? Why was escalation not selected?

For both, ask: *What path did the topography make easiest?*

That final question is the bridge between reliability engineering and safety engineering.

---

## 7.8 Evaluation Should Diagnose the Shape

If the framework is right, evaluation should not inspect only final outputs. It should inspect the reasoning state that produced them.

For hallucination, evaluation should ask: Was the claim supported? Was the source visible? Was the source connected to the claim? Was confidence appropriate? Was uncertainty expressed when support was insufficient?

For agentic action, evaluation should ask: Was the active goal clear? Was relevant policy visible? Was the tool action permitted? Was approval required? Were consequences represented? Was prior learning retrieved? Was sufficiency justified?

This means evaluation artifacts should preserve more than pass/fail results. They should preserve the state transition: goal, policy, interpretation, visible information, confidence, investigation path, sufficiency rationale, action, outcome, prediction error.

Without that state transition, a failed evaluation may produce a fix but not learning. The team may patch a symptom, add a rule, or block an action without understanding the topography that made the failure likely.

This is where the paper transitions from failure analysis into learning.

---

## 7.9 From Failure to Learning

Hallucination and harmful action reveal the same deeper need: systems must not only act; they must learn from the gap between expected and observed outcomes.

A hallucinated answer should not merely be corrected. The system should identify why unsupported completion became sufficient and update the relevant model, policy connection, confidence threshold, or evidence requirement.

A harmful action should not merely be blocked next time. The system should identify why the action appeared permissible, useful, or sufficient, and update the relevant topography, tool boundary, policy representation, or model of risk.

A failed campaign should not merely be remembered. The system should identify which premise failed, under what conditions, and how future campaign reasoning should change.

This requires a distinction that the next section develops:

> Outcome is not learning. Correction is not learning. Postmortem is not learning. Learning occurs when prediction error is investigated, explained with evidence, and converted into a bounded model update.

---
