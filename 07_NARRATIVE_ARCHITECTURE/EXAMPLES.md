# EXAMPLES

Concrete examples that illustrate the framework in action. Each example should demonstrate at least one core concept and be grounded in a real domain.

---

## Marketing Knowledge Platform Example

**Illustrates:** Information Surfaces, Perception Construction, FL_007 Independent Variability

### Observation

A marketer building a campaign brief will optimize against the reality exposed through the knowledge platform. The platform is the information surface. The brief is the behavioral output.

### Scenario A

The knowledge platform exposes:
- Prior campaign briefs
- Brand guidelines
- Product descriptions

Produces one perception of the market. The marketer builds a campaign around internal messaging and product features.

### Scenario B

The knowledge platform exposes:
- Prior campaign briefs
- Brand guidelines
- Product descriptions
- **Customer complaints**
- **Lost deals**
- **NPS feedback**
- **Competitor analysis**

Produces a different perception of the market. The marketer builds a campaign that addresses pain points, competitive positioning, and customer sentiment.

### Implication

The retrieval architecture influences the situational model available to the marketer and therefore influences campaign decisions. Same marketer. Same analytical capability. Different information surface. Different perception construction. Different behavior.

### Framework Mapping

| Component | In This Example |
|-----------|----------------|
| Reality | The actual market: customers, competitors, sentiment, product fit |
| Information Surface | The knowledge platform and what it exposes |
| Perception Construction | The marketer's situational model of the market |
| Optimization | Campaign brief creation |
| Behavior | The campaign itself |

### Why This Example Matters

This is a business-native example that avoids AI jargon. It demonstrates that Information Surfaces are not a technical concept — they exist in every domain where an optimizer makes decisions based on curated information. It also provides a clean instance of the FL_007 independence test: the information surface changed while the perception construction capability remained constant, and behavior followed the surface change.

---

## VP Marketing Visibility Interview

**Illustrates:** Gradient/Visibility/Perception distinction, FL_007 failure modes (Hidden Risk, Misread Signal, Attention Failure), D011 (Differential Intervention Principle), operational application of framework

### Objective

Most discovery engagements begin by asking: What systems do you use? What reports do you have? What KPIs do you track?

This framework begins somewhere else:

> **What reality is currently visible to the organization?**

The goal is to map Known, Visible, Invisible, Misread, and Ignored Gradients — **before** proposing technology, retrieval, dashboards, or AI.

---

### Phase 1: Known Gradients

*Identify what the VP currently believes matters.*

**Q: What are the three to five things that occupy most of your attention today?**
Follow-up: Why those?

Example response: Pipeline generation, conversion rate, campaign ROI.

Signal: The perceived gradients already driving behavior. Not whether they're correct — only what currently has attention.

**Q: If your team exceeded expectations this quarter, what would be true?**

Example response: More qualified leads, better campaign performance, higher conversion.

Signal: Reveals the success landscape currently being optimized.

---

### Phase 2: Visibility Mapping

*Identify what reality is actually visible.*

**Q: What information do you review every week?**

Example response: Salesforce dashboards, marketing analytics, campaign reports, executive scorecards.

Signal: Maps current information surfaces.

**Q: What information do your direct reports review that you do not?**

Example response: Customer support tickets, social sentiment, campaign creative feedback.

Signal: Reveals visibility asymmetry.

**Q: What information exists somewhere in the company but rarely reaches you?**

Example response: Win/loss interviews, product usage data, customer complaints.

Signal: Potential hidden gradients.

---

### Phase 3: Hidden Gradient Discovery

*Identify risks that may exist but remain unseen.*

**Q: What surprises the organization most often?**

Example response: Unexpected churn, competitor wins, campaign failures.

Signal: Surprises frequently indicate hidden gradients.

**Q: What problems tend to become obvious only after they are already expensive?**

Example response: Customer dissatisfaction, pipeline quality issues, product-market fit concerns.

Signal: Areas where visibility arrives too late.

**Q: If you could have one source of truth tomorrow that doesn't currently exist, what would it be?**

Example response: Real customer sentiment, lost deal intelligence, competitive positioning.

Signal: The VP is identifying perceived blind spots.

---

### Phase 4: Misread Gradient Discovery

*Identify areas where information exists but interpretation differs.*

**Q: What metrics generate the most debate?**

Example response:
- Marketing: "Campaigns are performing well."
- Sales: "Lead quality is declining."

Signal: Same visibility. Different perception. Classic Misread Signal candidate.

**Q: Where do leadership teams consistently disagree about root causes?**

Example response: Why customers churn, why opportunities stall, why campaigns succeed.

Signal: Potential perception-construction failure.

**Q: What information does everyone see but interpret differently?**

Example response: Pipeline reports, conversion metrics, NPS scores.

Signal: Visibility exists. Shared understanding does not.

---

### Phase 5: Ignored Gradient Discovery

*Identify areas where the organization understands the issue but does not act.*

**Q: What problems does everyone agree exist but never seem to get fixed?**

Example response: Poor onboarding, weak lead handoff, brand inconsistency.

Signal: Attention Failure candidate.

**Q: If resources were unlimited, what would you fix first?**

Example response: Customer onboarding, product adoption, retention programs.

Signal: Known gradients being deprioritized.

**Q: What issue keeps appearing in quarterly reviews without meaningful progress?**

Example response: Customer retention, campaign attribution, lead quality.

Signal: Visible. Understood. Not acted upon.

---

### Diagnostic Summary

After the interview, classify findings:

| Category | Definition | FL_007 Failure Mode |
|----------|-----------|-------------------|
| **Known Gradients** | What the organization currently believes matters | — (baseline) |
| **Visible Gradients** | Reality regularly exposed through dashboards, reports, meetings, systems | — (functioning surfaces) |
| **Invisible Gradients** | Important forces believed to exist but not adequately visible | Hidden Risk |
| **Misread Gradients** | Visibility exists but interpretation differs | Misread Signal |
| **Ignored Gradients** | Visibility and understanding exist but action does not | Attention Failure |

### Design Implications

Only after this map exists should retrieval, dashboards, AI assistants, or knowledge platforms be designed.

The goal is not: *"Retrieve relevant documents."*

The goal is: **"Improve visibility of important gradients, reduce misinterpretation, and surface information capable of changing decisions."**

### Why This Example Matters

This is the framework's first operational tool — a structured interview that applies the gradient/visibility/perception distinction to real organizational diagnosis. It demonstrates:

1. The framework produces **actionable methodology**, not just theory
2. FL_007's failure modes map directly to diagnostic categories
3. D011 (Differential Intervention Principle) is embedded: each category implies a different intervention class
4. The interview itself is an information surface designed to make organizational gradients visible to the consultant

---

## Agent Governance Through Visibility

**Illustrates:** Information Surfaces as governance mechanism, FL_007 (5-layer chain), ST-3 (Governance as Environmental Design)

### Core Observation

Agent behavior may be influenced not only by goals and optimization, but also by which gradients are visible through the information surfaces available to the agent. Governance is not just goal design — it is also **visibility design**.

### Scenario

Two AI agents with identical goals: "maximize customer engagement."

**Agent A — Narrow Visibility:**
Information surfaces expose:
- Click-through rates
- Session duration
- Conversion metrics

Agent A optimizes for engagement patterns that maximize clicks and time-on-site. It may produce increasingly aggressive notification strategies, dark patterns, or addictive loops — because those gradients slope toward its goal given what it can see.

**Agent B — Broad Visibility:**
Information surfaces expose:
- Click-through rates
- Session duration
- Conversion metrics
- **Customer trust scores**
- **Churn indicators**
- **Support ticket volume**
- **Long-term retention data**

Agent B, with the same goal, perceives a different landscape. Aggressive engagement tactics now have visible costs — trust erosion, churn risk, support load. The optimization settles on a different strategy: sustainable engagement that balances short-term metrics against long-term consequences.

### Implication

Same agent. Same goal. Same optimization capability. Different information surface. Different behavior.

Governance involves both:
1. **Goal Design** — what the agent is told to optimize
2. **Visibility Design** — which gradients the agent can perceive while optimizing

Most AI governance conversations focus exclusively on goal design (alignment, reward specification, guardrails). The framework argues that visibility design may be equally powerful — and in some cases more practical, because it doesn't require changing the agent's objectives. It changes the landscape the agent sees.

### Framework Mapping

| Component | Agent A | Agent B |
|-----------|---------|---------|
| Reality | Full customer relationship | Full customer relationship |
| Real Gradients | Engagement, trust, churn, satisfaction | Same |
| Information Surface | Narrow: clicks, duration, conversion | Broad: adds trust, churn, retention, support |
| Visible Gradients | Short-term engagement only | Short-term + long-term consequences |
| Perceived Gradients | "Aggressive engagement works" | "Sustainable engagement works" |
| Behavior | Dark patterns, notification spam | Balanced engagement strategy |

### Why This Example Matters

This is the framework's clearest AI governance example. It demonstrates that the alignment problem is partly an information surface design problem — not just a reward specification problem. It connects directly to ST-4 (Alignment as Environment Design) and provides a concrete instance of FL_007's 5-layer chain in an AI context.

---

## Decision Support vs Information Retrieval

**Illustrates:** Practical application pattern — how the framework changes system design

### Observation

The practical application of the framework is not maximizing visibility. It is improving decisions through the interaction of three design levers:

1. **Goal Specification** — What is the optimizer trying to achieve?
2. **Attention Direction** — Which visible gradients should receive focus?
3. **Visibility Design** — Which gradients from reality are made observable?

These three levers interact. Visibility without goal-aligned attention produces noise. Attention without adequate visibility produces blind spots. Goals without visibility design produce misalignment between intent and action.

### Key Principle

Traditional systems retrieve information:
> *"Here are documents relevant to your query."*

Framework-informed systems surface gradients capable of changing a decision:
> *"Here is information that, if seen, would alter what you do next."*

The difference is not volume or relevance. It is **decision impact**. A framework-informed system asks: does this information create a visible gradient strong enough to shift the optimizer's perceived landscape?

### Comparison

| Dimension | Information Retrieval | Decision Support (Framework) |
|-----------|----------------------|------------------------------|
| Goal | Return relevant information | Surface decision-changing gradients |
| Success metric | Recall, precision, relevance | Decision quality, outcome improvement |
| Design question | "What matches the query?" | "What would change the decision?" |
| Failure mode | Irrelevant results | Missing gradient that would have mattered |
| Information surface | Optimized for coverage | Optimized for gradient visibility |

### Example

A marketer asks a knowledge platform: "Show me campaign performance data."

**Information retrieval** returns: campaign metrics, historical performance, benchmarks.

**Decision support** returns: campaign metrics, historical performance, benchmarks — *plus* the three customer complaints that would change the campaign direction if seen, the competitor move that invalidates the current strategy, and the churn signal that makes the current target audience questionable.

The second system doesn't just answer the question. It surfaces gradients the marketer didn't know to ask about — gradients capable of changing the decision.

### Why This Matters

This is the framework's prescriptive contribution to product design. It reframes the purpose of retrieval, dashboards, and AI assistants from "deliver information" to "surface decision-changing gradients." That reframe is actionable — it changes what you build, how you evaluate it, and what success looks like.
