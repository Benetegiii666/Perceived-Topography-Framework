## 7. Discovery Turns Human Intent Into Reusable Reasoning

Learning changes reasoning after reality answers back. Discovery works earlier. It captures the human reasoning that should shape the landscape before the system acts.

That before-action moment matters because many failures do not begin with missing data. They begin with compressed intent.

A stakeholder asks for a campaign, but the real goal is not "campaign." It is qualified pipeline, executive education, sales learning, partner enablement, compliance-safe positioning, or some blend of those. A manager asks for a customer update, but the hidden boundary is that one field change may trigger billing, eligibility, legal notice, or account access. A product lead asks for a summary, but the important distinction is whether the summary should preserve uncertainty, recommend action, or simply report what is known. A security reviewer asks for an approval path, but the real reasoning may depend on consequence severity, reversibility, and who has authority to accept risk.

The request is small. The reasoning behind it is not.

A human may not arrive with a fully formed reasoning state. People often know what matters without having already organized it into goals, assumptions, evidence, confidence, boundaries, unresolved questions, and sufficiency conditions. Some of that reasoning is tacit. Some is contested. Some becomes clear only when a system proposes the wrong interpretation and the human sees what needs correction.

The problem is therefore not simply that important reasoning is missing. Often, the organization already contains the necessary judgment. It lives in stakeholder intent, expert memory, sales intuition, compliance caution, product nuance, executive priority, team habit, and half-spoken assumption. The problem is that this reasoning remains unstructured, unconfirmed, and unavailable at the moment future systems need it.

Discovery turns messy intent into reusable reasoning state.

More precisely, Discovery turns tacit or compressed human reasoning into reusable reasoning surfaces: confirmed and bounded representations of intent, assumptions, confidence, evidence, constraints, unresolved questions, and sufficiency conditions. These surfaces are not merely notes. They become features of the future landscape. They give later humans and agents something to see, trust, question, connect, investigate, or treat as insufficient.

Discovery is therefore not better intake. It is pre-action topography design.

It asks:

> What reasoning should shape the landscape before action becomes sufficient?

That question changes the role of the user. The user is not merely assigning a task. The user is helping shape the conditions under which the task should be understood, bounded, and completed.

### Most requests are compressed reasoning

Most work begins with compressed language.

"Create a campaign."

"Summarize this issue."

"Reach out to the customer."

"Approve the exception."

"Update the record."

"Find the best answer."

"Generate the brief."

Each request carries hidden structure. It implies a goal, an audience, a risk boundary, a definition of success, a confidence level, a policy context, a set of assumptions, and a stopping condition. But the request rarely states all of that. It asks for action while leaving much of the action-shaping reasoning implicit.

A system can complete the request anyway.

That is the danger.

The path can become sufficient before the hidden reasoning becomes visible. The system may produce a fluent campaign, a confident summary, a completed tool action, or a polished recommendation while moving through a landscape built from unconfirmed inference.

Discovery exists to surface that inference before it hardens into action.

It does not ask every possible question. That would fail. It asks for the reasoning whose absence could materially change the goal, boundary, investigation, sufficiency condition, or action.

### Discovery runs on infer-confirm, not blank forms

A blank form asks the human to formalize everything from scratch. That creates burden. People will avoid it, rush through it, or answer at the wrong level of abstraction.

Silent inference creates the opposite failure. The system infers intent from context, treats that inference as if it were confirmed, and preserves a reasoning state that may never have been true.

Both failure modes are predictable.

Blank forms create burden.

Silent inference creates false confidence.

Discovery needs a middle path.

The system should do the reasoning work before asking the user to do it. It should infer what it can from existing information surfaces, expose the inference, and ask humans to confirm only what matters.

The core loop is:

```text
Retrieve
→ Infer
→ Propose
→ Confirm
```

**Figure 6. Runtime Discovery Loop**

```text
Existing information surfaces
        ↓
Retrieve relevant artifacts, policies, examples, and prior reasoning
        ↓
Infer provisional reasoning
        ↓
Propose a candidate reasoning state
        ↓
Human confirms, corrects, rejects, qualifies, or bounds
        ↓
Reusable reasoning surface
        ↓
Future topography
```

The center of Discovery is the infer-confirm loop:

```text
Retrieve → Infer → Propose → Confirm
```

Preservation, generation, action, observation, and learning are downstream consequences. They matter, but they are not additional Discovery stages. Discovery is the process by which a provisional interpretation becomes confirmed, corrected, rejected, qualified, or bounded reasoning.

### Retrieve

Discovery begins by using what already exists.

The system retrieves relevant information surfaces: documents, policies, prior decisions, examples, reports, tickets, transcripts, customer notes, campaign data, approved claims, tool histories, and previous model updates. Retrieval reduces burden because the human does not have to restate everything the organization has already made available.

But retrieval does not equal understanding.

A retrieved artifact may be stale, incomplete, politically shaped, context-dependent, or irrelevant to the current decision. A prior campaign may show that workflow-burden language generated engagement. It may not reveal whether the current team wants awareness, qualified pipeline, executive education, partner enablement, sales learning, or compliance-safe experimentation. An approved-claims repository may show what can be said. It may not explain how close to the claim boundary the team wants to operate. Sales notes may show buyer pain. They may not establish whether that pain indicates readiness to buy.

Retrieval provides surfaces.

Discovery asks what those surfaces mean for the decision at hand.

The point of retrieval is not to avoid human judgment. It is to prepare a better question.

### Infer

The system then infers a possible reasoning state.

It may infer the apparent goal, likely audience, hidden premise, policy boundary, confidence level, unresolved question, or decision condition. That inference is useful because it turns scattered context into a candidate structure.

It is also dangerous because the candidate structure may be wrong.

Inferred reasoning must remain visibly provisional. The system should not hide the inferential step. It should not treat its interpretation as the user's intent. It should not treat non-response as confirmation.

A useful inference sounds like:

> I think this campaign is treating workflow burden as the primary attention hook, but not yet as proof of buying readiness. Is that right?

A dangerous inference sounds like:

> The audience has workflow burden, so they are qualified buyers.

Discovery depends on making the first kind of inference explicit before it becomes the second kind of action.

### Propose

The system should then propose a candidate reasoning state.

A proposal is not merely a question. It is a visible draft of the reasoning the system is about to use.

For the healthcare campaign, the proposal might be:

> I am reading the objective as qualified demo generation, not broad awareness. I am treating workflow burden as an attention signal, not a sufficient qualification signal. I am treating "reduces readmissions" as a direct clinical-outcome claim that requires approved evidence. I am not assuming that engagement equals buying readiness. The main unresolved question is which signals distinguish active RPM evaluation from general concern about workflow burden.

That proposal gives the human something to correct.

The stakeholder may say:

> No, this campaign is actually top-of-funnel awareness, so qualified demo conversion is not the immediate goal.

Or:

> Yes, but practices with existing remote-monitoring reimbursement workflows are higher priority.

Or:

> We do have an approved readmissions claim, but only in a qualified form and only for a specific population.

Or:

> Workflow burden is the hook, but sales only wants leads from organizations actively evaluating RPM this quarter.

The same pattern applies outside marketing.

For a customer-account action, the proposal might be:

> I am reading this as a routine account update, but the field being changed appears connected to billing eligibility. Should this action require approval before downstream notification?

For a support summary, the proposal might be:

> I am treating the unresolved customer issue as a product defect hypothesis, not yet a confirmed defect. Should the summary preserve that uncertainty or recommend escalation?

For an internal policy question, the proposal might be:

> I found prior guidance, but it appears to apply to contractors rather than full-time employees. Should I treat it as analogous background or as binding policy?

In each case, the proposal creates a surface for alignment. It lets the human adjust the reasoning before the system commits to action.

### Confirm

Confirmation is not a yes/no approval click.

The human must be able to confirm, correct, reject, qualify, or bound the proposed reasoning. Confirmation may also reveal that the system needs to re-enter the loop: retrieve more context, infer again, propose a narrower reasoning state, and ask a better question.

Confirmation establishes that a human accepts or bounds the represented reasoning for the current decision. It does not establish that the reasoning is objectively true, universally applicable, politically neutral, or permanently valid.

That humility matters.

The person confirming may not have authority over every boundary. Different stakeholders may disagree. A product lead, marketer, sales leader, compliance reviewer, and executive sponsor may each see a different part of the situation. A system-generated proposal may anchor the human toward accepting a frame they would otherwise challenge. A confirmed reasoning state can still be local, incomplete, or wrong.

Discovery therefore needs scope, confidence, and provenance.

A confirmed statement should preserve not only what was accepted, but who accepted it, under what conditions, with what confidence, and where authority or uncertainty remains unresolved.

A weak confirmation record says:

> User confirmed workflow burden matters.

That is too vague. It can easily become a misleading memory.

A stronger confirmation record says:

> Confirmed by campaign owner for current RPM demand-generation campaign: workflow burden should be used as an attention hook, not as a qualification signal. Qualified demo requests require evidence of active evaluation or operational readiness. Compliance approval still required for any clinical-outcome language. Confidence: moderate because prior engagement data supports attention value, but sales feedback does not yet support buying-readiness value. Applicability: current cardiology administrator campaign.

This record is more useful because it preserves a confidence marker and a reason for that confidence. "Moderate" is not decorative. It tells future reasoning how strongly to rely on the premise.

A stronger tool-action confirmation might say:

> Confirmed by operations lead for customer-status updates: changing this field from pending to approved can trigger downstream customer notification and account-access changes. Human approval is required before execution. Confidence: high for current workflow. Applicability: customer-status update process only; does not apply to internal notes.

That record does not merely store an answer. It preserves a bounded reasoning surface that can shape future action.

### Ordinary intake and Discovery ask different questions

Discovery can look like questioning, but the purpose is not to collect more form fields. The purpose is to expose the reasoning that changes future action.

**Table 6. Ordinary Intake and Discovery Ask Different Questions**

| Ordinary intake asks              | Discovery additionally asks                                                       | Why the answer changes future reasoning                                           |
| --------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| What do you want produced?        | What decision or action should this output support?                               | The system can distinguish completion from usefulness.                            |
| Who is the audience?              | What do we believe about this audience, and how confident are we?                 | Audience claims become bounded interpretations rather than invisible assumptions. |
| What message should we emphasize? | What evidence supports that message, and what boundary does it cross?             | The system can separate supported positioning from unsupported claims.            |
| What constraints apply?           | Which constraints must interrupt action if they are unresolved?                   | Policy becomes behaviorally meaningful rather than merely present.                |
| What does success look like?      | What outcome would prove our premise wrong or incomplete?                         | Later learning has an expectation to compare against.                             |
| What examples should we use?      | Which examples are reusable, and where do they stop applying?                     | Future systems inherit scope rather than copying patterns blindly.                |
| What should be remembered?        | What reasoning would future work need in order to avoid repeating this ambiguity? | Memory becomes reasoning support rather than artifact storage.                    |

The table should not be read as a checklist. Most situations will not require every question. Discovery asks when the answer could materially change the goal, boundary, investigation, sufficiency condition, or action.

### Discovery creates reusable reasoning surfaces

Once reasoning is confirmed and bounded, it can become part of the future landscape.

A reusable reasoning surface is not just a stored answer. It is a structured surface through which future humans and agents can encounter prior reasoning. To be reusable, it should preserve enough scope, confidence, provenance, and applicability boundary to prevent blind copying.

Discovery can create surfaces such as:

* confirmed goals;
* premise stacks;
* audience interpretations;
* confidence notes;
* claim boundaries;
* policy links;
* evidence requirements;
* unresolved questions;
* escalation triggers;
* examples and counterexamples;
* sufficiency conditions;
* decision rationale;
* applicability boundaries.

These surfaces change future topography.

They can make a prior assumption visible. They can make an evidence boundary easier to encounter. They can make a weak confidence signal less likely to be overused. They can connect a policy to a specific action type. They can make an unresolved question attractive enough to investigate before action. They can make escalation easier than unsupported completion.

The healthcare campaign shows the mechanism.

Without Discovery, the instruction "generate qualified demo requests" may remain compressed. The system may infer that workflow pain is enough to identify qualified buyers. The team may not realize that assumption is active until after the campaign runs.

With Discovery, the system can surface the hidden premise earlier:

> What makes a demo request qualified?

The answer might be:

> A qualified request comes from an organization that is actively evaluating RPM, has operational ownership for patient monitoring, and has a near-term workflow or budget reason to act.

That answer changes the landscape.

Workflow burden remains useful, but it no longer becomes sufficient by itself. Readiness indicators become more visible. Sales notes become more connected to targeting. The call to action can be framed around workflow fit rather than broad clinical transformation. The next agent does not need to rediscover the distinction from scattered artifacts.

The confirmed reasoning becomes a future surface.

Discovery can also improve its own patterns over time. If repeated confirmations show that a certain kind of request almost always hides the same missing premise, boundary, or confidence question, that pattern should shape future Discovery. The system should not ask every user everything; it should learn which reasoning gaps are likely to matter for a given class of work, while still treating each inferred gap as provisional until confirmed.

### Discovery makes policy and consequence visible before action

Discovery also matters for tool use.

A user may ask an agent to perform an action that appears straightforward:

> Update the customer record.
>
> Send the notice.
>
> Cancel the account.
>
> Change the routing.
>
> Trigger the workflow.
>
> Approve the exception.

The task may be clear while the consequence boundary remains hidden.

Discovery asks:

> When this action succeeds, what downstream consequence should still block, require approval, or trigger escalation?

That question can surface reasoning that is obvious to a human expert but invisible to the system. The human may know that a change affects billing, compliance status, customer access, patient communication, contract terms, legal notice, or operational routing. The system may see only a tool that completes the requested action.

Discovery makes the consequence part of the perceived topography before the tool path becomes sufficient.

A confirmed reasoning surface might say:

> Updating this field changes customer eligibility. If the field changes from pending to approved, human review is required before downstream notification. The action is operationally simple but materially consequential.

That is not implementation architecture. It does not specify permissions, storage, API design, or lifecycle management. It preserves the reasoning needed to avoid treating a consequential action as a routine edit.

### Discovery does not replace human judgment

Discovery does not remove human judgment. It depends on it.

The system can retrieve context, infer a candidate reasoning state, propose the interpretation, and ask focused questions. But it cannot assume that its inference is authoritative. It cannot treat silence as agreement. It cannot convert one stakeholder's answer into universal policy. It cannot know that a confirmed boundary applies forever.

Human judgment remains necessary because organizational reasoning is often contested, local, political, evolving, and incomplete.

Discovery makes that reality more explicit.

It allows the system to say:

> I have inferred the likely reasoning, but these parts need confirmation.

It allows a human to say:

> That is right for this campaign, but not for enterprise accounts.

Or:

> That was true last quarter, but the compliance guidance changed.

Or:

> Sales believes this, but product does not have evidence yet.

Or:

> That is my working assumption, not an approved policy.

These qualifications are not noise. They are part of the reasoning state. Without them, future systems may inherit conclusions without scope.

A reasoning surface is more useful when it says less with better boundaries.

### Discovery as governance

The governance value of Discovery is not that it produces perfect understanding. It does not.

Discovery makes reasoning available for inspection before action. It reduces the chance that hidden assumptions become invisible gradients. It gives humans a way to correct the system's interpretation before fluency hardens into sufficiency. It gives future systems more than artifacts to retrieve.

A governed human-agent system should be able to represent:

* what goal it believes it is serving;
* what assumptions it is using;
* what confidence it has in those assumptions;
* what evidence supports them;
* what boundaries constrain action;
* what uncertainty could change the path;
* what human confirmation has been obtained;
* what remains unresolved;
* what should be preserved for future reasoning.

Without Discovery, the system may still perform tasks. But it will often act from an inferred landscape whose most important features were never confirmed.

With Discovery, the organization can shape the landscape before the system moves.

Discovery shapes the starting optimizer state. Because starting state shapes motion, Discovery shapes safety. It changes what the system believes it is doing, which boundaries appear relevant, which uncertainties become visible, and what must be confirmed before action becomes sufficient.

The easiest sufficient path can become the path that preserves intent, checks assumptions, exposes boundaries, and asks when the answer would change action.

Learning shows why preserved reasoning matters after outcomes. Discovery shows how reasoning can be captured before it is lost.

Discovery gives architecture something worth carrying. Architecture gives Discovery somewhere durable to go. Without Discovery, architecture risks becoming an empty container for reasoning that was never captured. Without architecture, Discovery risks becoming another good conversation that cannot reliably shape the next action.

The remaining problem is structural: what kind of system can hold these reasoning surfaces, retrieve them at the right time, update them when reality contradicts them, and govern their use across human-agent workflows?
