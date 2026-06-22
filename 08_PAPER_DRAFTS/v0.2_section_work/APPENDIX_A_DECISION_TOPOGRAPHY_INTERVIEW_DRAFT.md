# Appendix A: The Decision Topography Interview

## A Starter Kit for Preserving Reasoning

This interview is a practical way to begin using the Perceived Topography Framework.

It is not a normal requirements questionnaire. A normal questionnaire often starts by asking what the organization has: reports, dashboards, data sources, documents, workflows, systems, and tools. Those questions are useful, but they mostly inventory artifacts.

This interview starts somewhere else.

It asks how the organization decides.

The goal is to understand the repeated decisions, signals, assumptions, constraints, failure paths, and learning moments that shape a workflow. The purpose is not only to improve one output. The purpose is to preserve the reasoning that should make the next cycle smarter.

Each question has three parts:

**What are we asking?**
The plain-language question to ask during discovery.

**Why are we asking?**
The reason this question matters in the framework.

**What will we do with the answer?**
How the answer becomes part of the workflow design, reasoning record, topography map, sufficiency threshold, model update, or future discovery pattern.

The interview can be used in a workshop, design session, product discovery meeting, governance review, or AI implementation planning session. It does not require the participants to know the theory. They only need to answer the questions.

## Old Approach: Artifact Inventory

A traditional discovery process often begins with questions like:

What reports exist?

What dashboards exist?

What data exists?

What documents exist?

What systems are connected?

Those questions map what the organization has. They do not necessarily map how the organization decides.

An organization can have many artifacts and still lose the reasoning that connects one decision to the next. It can preserve the report but lose why the report mattered. It can preserve the dashboard but lose which signals changed the decision. It can preserve the final action but lose the assumptions, constraints, uncertainty, and evidence that made the action seem sufficient.

## New Approach: Decision Topography Discovery

Decision topography discovery begins with different questions:

What decisions repeat?

What outcomes matter?

What signals influence the decision?

What information is trusted?

What information is hard to reach?

What assumptions drive action?

What evidence changes the model?

What causes the system to stop too early?

What should be preserved so the next cycle starts smarter?

These questions map how the organization perceives, decides, acts, fails, and learns.

That is the shift.

The point is not to collect more context. The point is to identify the reasoning that should survive the moment of action.

## How to Use This Interview

Begin with one repeated workflow. Do not start with the whole organization.

Choose a workflow where decisions recur, outcomes matter, and one case should help the next case improve. The first use case should be small enough to understand but important enough that better reasoning would matter.

Use the questions in order, but do not treat them as a rigid script. The interview is meant to reveal the shape of the work: what the system is trying to do, what information shapes behavior, where motion goes wrong, what should be preserved, and how the next cycle should improve.

Some questions intentionally return to earlier themes at a deeper level: first to discover how the workflow operates, later to decide what reasoning must be preserved.

# Phase 1: Map the Decision Topography

The first phase maps the decision environment before any system is built. The goal is to understand the repeated decision, the outcome that matters, the signals people use, the information they trust, the gaps that surprise them, the assumptions they carry, and the constraints that govern the work.

## 1. What decisions repeat?

**What are we asking?**

Which workflow produces a recurring decision, recommendation, output, escalation, or action?

Where does the organization make a similar judgment again and again?

**Why are we asking?**

The framework works best where learning can accumulate. A one-time task may need a good answer, but a repeated workflow needs better starting conditions for the next cycle.

If the same kind of decision happens repeatedly, the organization should not have to relearn the same lesson every time.

**What will we do with the answer?**

We use this answer to choose the first workflow to model.

This becomes the scope boundary for the first implementation. It tells us where reasoning should be preserved, where learning should accumulate, and where future work should start smarter.

## 2. What outcomes matter most?

**What are we asking?**

What is this workflow trying to accomplish?

What would count as a good result?

What outcome would make the work worth improving?

**Why are we asking?**

A system cannot know what is relevant unless it knows what outcome matters.

The goal is not just the task label. "Create a campaign," "review a case," or "answer a customer" is not enough. We need to know what success means in context.

**What will we do with the answer?**

We use this answer to define the active goal for the workflow.

The goal shapes which information matters, which paths become attractive, and what "good enough" means before the system acts.

## 3. What signals influence those decisions?

**What are we asking?**

What information currently shapes the decision?

What do people look at before acting?

What signals tend to change the direction of the work?

**Why are we asking?**

Signals reveal the visible part of the decision topography.

If a signal influences the decision, it has behavioral force. If a signal should influence the decision but does not, that may reveal a visibility gap, representation problem, trust problem, or connectivity problem.

**What will we do with the answer?**

We use this answer to map which information is already shaping behavior.

We also identify signals that should be made more visible, easier to reach, better represented, more trusted, or more clearly connected to the decision.

## 4. What information do you trust — and what do you not trust?

**What are we asking?**

Which sources, signals, people, systems, reports, or prior lessons carry weight?

Which ones are ignored, doubted, delayed, or treated as unreliable?

**Why are we asking?**

Information does not shape behavior just because it exists. It shapes behavior when the system or team trusts it enough to use it.

Confidence is part of the topography. High-confidence information can pull action forward. Low-confidence information may be ignored even when it matters.

**What will we do with the answer?**

We use this answer to map confidence.

We look for places where the system is over-trusting weak information, under-trusting useful information, or treating important uncertainty as if it were settled.

## 5. What information is difficult to access or repeatedly surprises you?

**What are we asking?**

What relevant information exists but is hard to find, slow to retrieve, fragmented, buried, or trapped in someone's head?

What keeps surprising the team after the decision has already been made?

**Why are we asking?**

Accessibility and visibility are different problems.

Sometimes the information exists, but the system cannot reach it at the moment of action. Sometimes the organization only discovers the important signal after reality pushes back.

Repeated surprise is a clue. It often means the workflow is missing something that should have been visible earlier.

**What will we do with the answer?**

We use this answer to identify access problems and visibility gaps.

Hard-to-access information becomes a candidate for better retrieval or representation. Repeated surprises become candidates for prediction-error investigation later in the workflow.

## 6. What assumptions drive your actions?

**What are we asking?**

What does the team believe is true when this work begins?

What prior experience, causal model, rule of thumb, or "everyone knows" belief shapes the decision?

What has the team stopped questioning?

**Why are we asking?**

Assumptions often make an action seem reasonable before evidence confirms it.

When assumptions are wrong, the action may still look coherent. The problem may not appear until the outcome contradicts the premise.

If assumptions are not preserved, future learning becomes premise-blind. The organization may remember what happened but forget what it believed when it acted.

**What will we do with the answer?**

We use this answer to build the premise stack.

These assumptions become part of the reasoning record. They also become expectations that can be tested against future outcomes.

## 7. What constraints govern the work?

**What are we asking?**

What rules, policies, approvals, compliance boundaries, ethical commitments, safety limits, or escalation requirements apply?

What must the system do?

What must it not do?

When must it involve a person?

**Why are we asking?**

A constraint does not govern behavior merely because it exists in a document.

For a constraint to shape action, it must be visible, reachable, understandable, trusted, and connected to the moment of decision.

**What will we do with the answer?**

We use this answer to define the policy field for the workflow.

We also test whether the constraint currently has force. If the rule exists but does not shape the path of action, the topography must change.

# Phase 2: Shape the Motion

The second phase identifies how the workflow moves. The goal is to understand what the current process makes easy, what it makes hard, where it tends to stop too early, and what conditions should cause the system to pause, ask, escalate, or refuse to act.

## 8. What makes the easiest path dangerous?

**What are we asking?**

Where does the current workflow make it easy to move too quickly?

Where might the system skip evidence, ignore uncertainty, bypass a constraint, or act before the situation is understood?

What is the tempting shortcut?

**Why are we asking?**

Systems do not only follow instructions. They follow paths.

If the easiest path is also the risky path, then the system is being shaped toward failure. A bad outcome may not come from a bad goal. It may come from a path that made the wrong action feel available, useful, or sufficient.

**What will we do with the answer?**

We use this answer to identify dangerous gradients.

Then we decide how the workflow should be reshaped: what should become harder, what should become more visible, what should require evidence, and what safer path should be easier to follow.

## 9. What would make the system stop, ask, or escalate?

**What are we asking?**

When should the system say, "I do not know yet"?

When should it say, "I should not act yet"?

When should it ask a person, escalate, or refuse to proceed?

**Why are we asking?**

A system needs a path for not acting.

If the only available path is to answer, recommend, generate, or act, then the system will keep moving even when it should pause. Many failures happen because stopping was not designed as a real option.

**What will we do with the answer?**

We use this answer to define stop, ask, escalate, and refusal conditions.

These conditions become part of the workflow design. They tell the system when motion should pause instead of continuing toward a premature answer or unsafe action.

## 10. How will you know when enough is enough?

**What are we asking?**

What must be true before the system can act?

What evidence is required?

What uncertainty would change the decision?

What uncertainty can be tolerated?

**Why are we asking?**

Good decisions do not require knowing everything. They require knowing enough for the action being taken.

The important question is not, "Do we have all possible information?" The important question is, "Would more information change what we should do?"

**What will we do with the answer?**

We use this answer to define sufficiency.

The sufficiency rationale becomes part of the decision record. It explains why the system had enough to proceed, what uncertainty remained, and why that uncertainty did or did not block action.

## 11. Where has this workflow failed before?

**What are we asking?**

Where has this workflow produced a poor result, a risky action, a bad recommendation, rework, delay, or surprise?

What did the team think was true at the time?

What later proved different?

**Why are we asking?**

Prior failures are often remembered as stories but not preserved as reusable learning.

A failure can be useful if the organization knows what expectation failed, what evidence explained the mismatch, and what should change next time. Without that structure, the lesson becomes folklore.

**What will we do with the answer?**

We use this answer to identify candidate learning events.

Some prior failures may become model updates. Others may reveal missing signals, weak constraints, bad assumptions, or places where the system stopped too early.

# Phase 3: Preserve the Reasoning

The third phase defines what must survive after the system acts. The goal is to preserve the reasoning trail, not just the output. A future person, agent, reviewer, or workflow should be able to understand why the action made sense at the time.

## 12. What must survive the action?

**What are we asking?**

After the system acts, what should still be recoverable?

What would a future person or agent need to understand why the decision, recommendation, output, or action happened?

**Why are we asking?**

Most systems preserve outputs better than reasoning.

They remember the email, campaign, report, decision, ticket, or action. But they often lose the goal, assumptions, evidence, uncertainty, constraints, and sufficiency rationale that shaped it.

**What will we do with the answer?**

We use this answer to decide which reasoning objects must be preserved.

At minimum, this may include the working frame, premise stack, decision state, investigation trace, and any learning event that should affect future work.

## 13. What goal, policy, and interpretation should be recorded?

**What are we asking?**

What was the system trying to accomplish?

What rules or constraints governed the work?

How did the system interpret the situation?

**Why are we asking?**

A decision is hard to evaluate if the working frame is missing.

The same action can be reasonable under one goal and wrong under another. The same output can be safe under one policy and unsafe under another. The same signal can mean different things depending on the interpretation.

**What will we do with the answer?**

We use this answer to preserve the working frame.

This gives future users and systems a way to understand the action in context instead of judging it only from the final output.

## 14. What assumptions made this action seem reasonable?

**What are we asking?**

What did the team or system believe when it acted?

What prior evidence, experience, pattern, lesson, or belief made this path seem right?

What was assumed but not fully proven?

**Why are we asking?**

Assumptions are often invisible until they fail.

If the premise is not preserved, the organization may learn the wrong lesson later. It may blame the output, the user, the data, or the tool while missing the belief that actually drove the action.

**What will we do with the answer?**

We use this answer to build the premise stack.

The premise stack helps future investigation ask, "Which belief was wrong?" instead of merely asking, "Which output was bad?"

## 15. What was chosen, what was rejected, and why was it sufficient?

**What are we asking?**

What action, answer, recommendation, or output was chosen?

What alternatives were considered?

Why was the chosen path considered good enough?

**Why are we asking?**

A final action without its alternatives is hard to understand.

The organization needs to know not only what happened, but why that path beat the other possible paths. It also needs to know why the available evidence was considered sufficient at the time.

**What will we do with the answer?**

We use this answer to preserve the decision state.

The decision state records the chosen path, rejected alternatives, tradeoffs, evidence, uncertainty, and sufficiency rationale.

## 16. How was uncertainty reduced?

**What are we asking?**

What questions were asked?

What evidence was checked?

What contradictions were found?

What information was accepted, rejected, or left unresolved?

**Why are we asking?**

Investigation is part of reasoning.

If the investigation disappears, the final explanation may become a story told after the fact. That makes the system vulnerable to rationalization: a clean explanation that sounds reasonable but does not reflect the actual path of inquiry.

**What will we do with the answer?**

We use this answer to preserve the investigation trace.

The trace shows how uncertainty was reduced, what evidence mattered, what was checked, and what remained uncertain when action occurred.

## 17. How should the system discover this next time?

**What are we asking?**

If a similar request came in tomorrow, what should the system retrieve first?

What should it infer?

What should it propose?

What should it ask before acting?

**Why are we asking?**

Discovery should improve over time.

If the system asks the same generic questions every time, it is not learning how the workflow works. A better system should begin the next cycle with better questions, better assumptions, and better retrieval.

**What will we do with the answer?**

We use this answer to define or update the discovery pattern.

The next time this kind of work begins, the system should start with a better frame instead of starting cold.

# Phase 4: Make the Next Cycle Smarter

The fourth phase connects the action to reality. The goal is to capture what happened, compare it to what was expected, identify what changed, and make sure the next cycle begins with better reasoning.

## 18. What happened after the system acted?

**What are we asking?**

What was the outcome?

What happened after the decision, recommendation, output, campaign, escalation, or action?

What evidence shows the result?

**Why are we asking?**

Learning needs contact with reality.

If the system acts but the outcome is not observed, there is no way to know whether the reasoning held up. Without an outcome, there is no prediction error. Without prediction error, there is no learning.

**What will we do with the answer?**

We use this answer to record the observed outcome.

The observed outcome is compared against the prior expectation so the system can identify where reality agreed, disagreed, or added nuance.

## 19. Where did reality differ from what was expected?

**What are we asking?**

What surprised you?

What went differently than expected?

Which assumption, signal, constraint, or prediction did reality challenge?

**Why are we asking?**

A bad outcome is not automatically learning.

Learning begins when the system can name the mismatch between what it expected and what actually happened. That mismatch is the prediction error.

**What will we do with the answer?**

We use this answer to identify prediction error.

The prediction error tells us what needs investigation. It focuses learning on the gap between expectation and reality.

## 20. What evidence explains the gap?

**What are we asking?**

Why did the outcome differ from the expectation?

What evidence supports that explanation?

What alternative explanations were considered?

What explanation should not be accepted yet?

**Why are we asking?**

A surprise can produce learning, but it can also produce rationalization.

The organization may react quickly and update the wrong belief. Evidence-supported explanation slows that down. It asks what actually explains the mismatch.

**What will we do with the answer?**

We use this answer to support or reject a model update.

The evidence becomes part of the learning record. It explains why the system should change, and why the change is justified.

## 21. What should change for next time?

**What are we asking?**

What should the system do differently next time?

Should the goal change?

Should the policy change?

Should the interpretation change?

Should the information topography change?

**Why are we asking?**

A lesson is not durable unless it changes future reasoning.

If the organization only remembers what happened, it has memory. If it changes what future work sees, asks, trusts, checks, or preserves, it has learning.

**What will we do with the answer?**

We use this answer to create a model update.

The model update records what changed, why it changed, what evidence supports the change, and how it should shape future work.

## 22. Where does this lesson apply — and where does it not?

**What are we asking?**

When should this lesson be used again?

Where should it not be used?

What conditions define its boundary?

**Why are we asking?**

Lessons can become dangerous when they are over-applied.

A lesson from one campaign, customer segment, market, risk pattern, or workflow may not apply everywhere. Without boundaries, learning can become dogma.

**What will we do with the answer?**

We use this answer to define the applicability boundary.

The boundary tells future systems when to retrieve the lesson, when to question it, and when not to use it.

## 23. Did preserved reasoning actually improve the next cycle?

**What are we asking?**

Did the next cycle start smarter?

Did the system ask better questions?

Did it avoid the prior failure?

Did the model update change future behavior?

Did the workflow improve in a way that matters?

**Why are we asking?**

The framework should be tested by its own standard.

If preserving reasoning does not improve the next cycle, then the implementation needs to change. The interview is not successful because it was completed. It is successful if it improves future motion.

**What will we do with the answer?**

We use this answer to validate the framework application.

If the answer is yes, the workflow has evidence that preserved reasoning is helping. If the answer is no, the workflow itself needs a model update.

## Closing Note

The interview begins by asking how the organization decides. It ends by asking whether preserved reasoning improved the next decision. That is the practical test of the framework: not whether the system produced one better answer, but whether the next cycle started with better reasoning.
