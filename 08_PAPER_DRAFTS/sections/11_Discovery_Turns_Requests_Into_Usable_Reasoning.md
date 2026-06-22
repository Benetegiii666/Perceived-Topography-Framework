# 11. Discovery Turns Requests Into Usable Reasoning

The previous section defined the reasoning architecture: the set of objects required to preserve optimizer state transitions across human-agent systems.

That architecture creates a practical problem.

If every user had to manually create an Optimizer State, Premise Stack, Decision State, Investigation Trace, Learning Event, and Model Update Object, the system would fail in practice. The reasoning architecture would be theoretically complete but operationally unusable.

People do not begin work by filling out reasoning schemas.

They say things like: "I want to do a healthcare campaign." Or: "Can you draft a customer follow-up?" Or: "Help me respond to this incident." Or: "Build a launch plan."

The human intent is often partial, ambiguous, compressed, and context-dependent. Asking the user to supply all of that up front creates friction and often produces worse reasoning because the system shifts the work of structure onto the person least prepared to do it at that moment.

This section introduces the **Discovery Framework**.

Discovery is the process by which messy human intent and organizational artifacts are converted into structured reasoning objects with the lowest necessary human burden.

The basic loop is:

```
Retrieve → Infer → Propose → Confirm → Generate → Preserve → Learn
```

Discovery is not a questionnaire. Discovery is not simply requirements gathering. Discovery is not asking the user to fill in every missing field.

Discovery is the adaptive process of turning unclear intent into usable reasoning state.

The principle is:

> Do the reasoning work before asking the user to do it.

---

## 11.1 Discovery Matters Because Structure Is Not Given

Discovery is where the human-agent system first determines what work is actually being requested.

This step matters because the same user request may imply different optimizer states.

Consider: "I want to do a healthcare campaign."

This could mean: brand awareness, qualified demo generation, conference activation, sales enablement, patient education, executive thought leadership, retention campaign, or partner campaign. Each implied goal changes the reasoning state.

A weak system asks blank-form questions: Who is your audience? What is your goal? What channel do you want? What message do you want? What assets do you need?

Those questions are not wrong. But they force the user to construct the reasoning state manually.

A stronger system retrieves existing context, infers likely candidates, proposes a strawman, and asks only the questions that materially affect the decision.

It might say:

> Based on existing materials, I think this is likely an RPM campaign for cardiology practice administrators, optimized for qualified demo requests. Prior learning suggests workflow burden is a strong attention driver, but buying-stage readiness determines demo quality. Should we target organizations already evaluating RPM, or problem-aware operators who are not yet shopping?

That is Discovery.

---

## 11.2 Discovery Happens Before and During the Work

### Initial Discovery Establishes the Pattern

Initial Discovery maps the existing reasoning environment of a team, department, or organization.

It asks: What artifacts already exist? Where do decisions happen? What policies govern work? What prior lessons are stored? Where does learning currently disappear? Which workflows repeatedly start cold? Which assumptions keep recurring? Which handoffs create ambiguity? Which systems contain evidence? Which people hold tacit knowledge?

Initial Discovery is useful when designing a reasoning architecture for a team or workflow.

### Runtime Discovery Builds the Moment

Runtime Discovery happens inside the work. It begins when a user brings a new objective, request, or proposal into the system.

Runtime Discovery converts that messy input into reasoning objects. It is the ongoing process by which the system retrieves, infers, proposes, confirms, generates, preserves, and learns.

Initial Discovery designs the map. Runtime Discovery uses and updates the map.

---

At runtime, Discovery turns messy human intent into preserved reasoning state through a structured loop:

![Runtime Discovery Loop](paper_assets/svg/fig7_runtime_discovery_loop.svg)

*Figure 7 — Runtime Discovery Loop.*

## 11.3 Retrieval Brings Prior Knowledge Into View

The first runtime step is **Retrieve**. The system should retrieve relevant artifacts before asking the user to manually supply what the organization already knows.

Retrieval should consider not only topical similarity but reasoning-state relevance: active or inferred goal, policy domain, audience, workflow type, prior premise stacks, decision history, model updates, applicability boundaries, and confidence levels.

The system should retrieve not only documents, but reasoning objects when they exist.

---

## 11.4 Inference Builds a Correctable Frame

After retrieval, the system should **Infer** the likely reasoning state: probable goal, likely audience, relevant policy, current interpretation, premise stack, applicable model updates, decision options, confidence gaps, and sufficiency threshold.

Inference is not guessing carelessly. It is structured hypothesis formation. The system should make its inference visible and provisional.

Example: "I am inferring that your goal is qualified demo requests, not general awareness, because the recent campaign brief and prior performance review both emphasize pipeline quality."

Inference lets the system build a strawman reasoning state. It also lets the user correct the system efficiently. The system should prefer correctable inference over blank interrogation.

---

## 11.5 Proposals Make the Frame Visible

After inference, the system should **Propose** a strawman — a provisional reasoning state or work direction offered for confirmation.

A good strawman is specific enough to be useful and humble enough to be corrected. A strong proposal includes confidence markers: high confidence (practice-level operators care about workflow burden), medium confidence (cardiology administrators are the right audience), low confidence / needs confirmation (buying-stage readiness).

The proposal gives the user something to react to. That reaction is more informative than a blank form.

---

## 11.6 Confirmation Asks Only What Matters

After proposing, the system should **Confirm** only the uncertainties that materially affect the outcome.

The system asks the smallest number of questions needed to reach sufficiency.

Example: "Before I generate the campaign package, confirm one thing: are we targeting organizations already evaluating RPM, or creating demand among problem-aware but not-yet-shopping buyers?"

The discovery rule is: *Ask only where uncertainty could materially change the action.*

This creates low-friction collaboration. The human remains in control, but the system carries more of the reasoning burden.

---

## 11.7 Generation Begins After Sufficiency

After confirmation, the system can **Generate** the requested artifacts. But generation should not be treated as the only output.

In a reasoning-state system, generated artifacts are accompanied by preserved reasoning objects. The user may see only the useful artifact. The system should preserve the reasoning beneath it.

This is the difference between producing content and producing adaptive work.

---

## 11.8 Preservation Makes the Work Reusable

After generation, the system should **Preserve** the relevant reasoning objects. Preservation is not an afterthought. It is how the system avoids starting cold next time.

Not every task requires full preservation. The amount of preservation should match the stakes, repeatability, and learning value of the workflow.

The design question is: *What reasoning state must future humans or agents recover to act better next time?*

---

## 11.9 Learning Changes the Next Discovery

Discovery does not end when the artifact is generated.

If the resulting action produces an outcome, the system should compare outcome against expectation. If reality contradicts expectation, the system should create a Learning Event and, where evidence supports it, a Model Update Object.

But Discovery itself can also learn.

---

## 11.10 Discovery Patterns Can Update Too

A **Discovery Pattern Update** is a specialized Model Update Object that records how the discovery process itself should change.

It answers: *Which interaction pattern produced better reasoning, better artifacts, lower user burden, or better outcomes?*

Example: Prior discovery pattern: ask for audience, goal, channel, and message from the user. Observed outcome: users provided inconsistent answers, often omitting buying-stage readiness. Model Update: for healthcare demo-generation campaigns, retrieve and infer ICP first, then ask one material question about buying-stage readiness.

This matters because the system should learn not only what strategies work, but how to ask better questions. A mature human-agent system improves its interaction patterns over time. Discovery Pattern Updates make that improvement durable.

---

## 11.11 Low Friction Keeps the System Usable

> The user should not have to supply information the system can responsibly retrieve, infer, or propose.

This does not mean the system should hide assumptions. It means the system should surface assumptions in a correctable form.

Bad discovery makes the user do structure. Better discovery provides structure and asks for correction.

The difference is not just user experience. It changes the quality of reasoning state captured. When the system retrieves, infers, proposes, and confirms, the resulting reasoning objects are more complete, more grounded, and more reusable.

---

## 11.12 Human Control Comes Through Correction

Low-friction discovery should not remove human control. The framework does not recommend that systems silently infer goals and act without confirmation in high-stakes or ambiguous settings.

Instead, it recommends visible inference. The system should show: what it inferred, why it inferred it, how confident it is, what uncertainty remains, which question matters, what action it proposes.

This makes discovery collaborative. Both human and system participate in constructing a better reasoning state.

In domains involving policy, compliance, safety, customer communication, medical claims, financial claims, legal claims, or operational risk, discovery should favor: transparent assumptions, confidence labels, approval gates, policy checks, escalation paths, trace preservation.

Human control is strongest when the system makes its reasoning state inspectable.

---

## 11.13 Safety Improves When Discovery Surfaces Risk

Discovery is also a safety mechanism. Many failures begin with a bad initial framing.

If the system infers the wrong goal, retrieves the wrong context, ignores the relevant policy, or fails to identify the material uncertainty, later safeguards may be too late.

A healthcare campaign framed as "write persuasive copy" may produce risky claims. The same campaign framed as "generate compliant, evidence-bounded external healthcare messaging for qualified demo conversion" produces a different path.

Discovery shapes the starting optimizer state. Because starting state shapes motion, discovery shapes safety.

---

## 11.14 The Campaign Shows Discovery in Practice

**Human Intent:** "I want to do a healthcare campaign."

**Retrieve:** Healthcare messaging, cardiology ICP, prior campaign performance, sales objections, product positioning, claims policy, prior model updates, measurement guidance.

**Infer:** Likely goal (qualified demo requests), likely audience (cardiology practice administrators), relevant policy (avoid unsupported clinical claims), relevant prior learning (workflow pain attracts attention; feature-led underperforms), material confidence gap (buying-stage readiness).

**Propose:** Workflow-pain-led RPM campaign for cardiology practice administrators, optimized for qualified demo requests. Avoid unsupported clinical claims. Include measurement plan.

**Confirm:** "Are we targeting practices already evaluating RPM, or creating demand among problem-aware but not-yet-shopping buyers?"

**Generate:** Campaign brief, ICP summary, messaging pillars, LinkedIn posts, email drip, event signage, commercial concepts, compliance watchlist, measurement plan, prediction-error triggers.

**Preserve:** Optimizer State, Premise Stack, Decision State, Investigation Trace, Sufficiency Rationale.

**Learn:** After performance data: Learning Event, Model Update Object, Discovery Pattern Update.

The important point is that the generated campaign is not the only product. The reusable reasoning state is also a product.

---

## 11.15 Discovery Is the Front Door to Reasoning

Reasoning Architecture defines what the system should preserve. Discovery defines how those objects are created naturally during work.

Without Discovery, the reasoning architecture becomes too heavy. Without Reasoning Architecture, Discovery becomes a better conversation but not a durable learning system.

They need each other.

The pieces now connect:

> **Optimizer State:** what the system brings. **Information Topography:** what the system navigates. **Optimizer Motion:** how behavior emerges. **Learning:** how reality updates the system. **Model Update Objects:** how learning persists. **Reasoning Architecture:** how state transitions persist. **Discovery:** how messy intent becomes structured reasoning.

This completes the framework's operational loop.

---

## 11.16 From Discovery to a Running Example

The next section brings the framework together in a single running example.

The healthcare campaign scenario will be treated not as a casual illustration, but as a complete workflow: messy request, retrieval, inference, strawman, confirmation, generation, decision state, measurement, outcome, prediction error, learning event, model update, discovery pattern update.

This example shows what the framework looks like when applied end to end.

It also demonstrates the paper's practical claim:

> The value of the framework is not only better AI outputs. The value is a system that helps people and agents reason, act, preserve, and learn together.

---
