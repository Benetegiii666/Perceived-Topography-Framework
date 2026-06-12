# Discovery Framework — Phase 4.4 Complete

**Status:** Foundational — validated through healthcare campaign simulation
**Date:** 2026-06-12

---

## Core Finding

> Discovery is the adaptive process of converting messy human intent and organizational artifacts into structured reasoning objects with the lowest necessary human burden.

More compactly: **Discovery converts human intent into reasoning state.**

Discovery is not a static questionnaire. It is an adaptive process that should:

```
Retrieve → Infer → Propose → Confirm → Generate → Preserve → Learn
```

---

## Two Discovery Modes

### 1. Initial Discovery

Used when entering a new team, department, organization, or agent ecosystem.

**Purpose:** Map how the team currently reasons.

**Identifies:**
- Active goals
- Policies and constraints
- Key decisions
- Existing premise artifacts
- Trusted information surfaces
- Confidence gaps
- Recurring investigations
- Failure modes
- Existing folklore / bad lessons
- Learning loops
- Model update opportunities

May use interviews, workshops, artifacts, physical cards, UI flows, and structured discovery canvases.

### 2. Runtime Discovery

Used when new work enters the system (campaign request, feature proposal, agent workflow, automation proposal).

**Purpose:** Convert a new proposal or user objective into structured reasoning objects with minimal human burden.

**Prefers:** Retrieve → Infer → Propose → Confirm (over blank-form questions).

---

## Strawman-First Principle

**Bad pattern:**
> "Who is your audience? What is your goal? What channels? What message? What proof points?"

**Better pattern:**
> "Based on existing materials and prior learning, here is my recommended direction. Here is why. Here is my confidence. Here is the one clarification that materially affects the result."

This reduces user burden while increasing reasoning quality.

## Low-Friction Discovery Principle

> Do the reasoning work before asking the user to do it.

Operational version: Infer first. Offer a strawman. Ask only where uncertainty materially affects the result.

The system should not behave like a smarter intake form. It should behave like a strategist that arrives with a strong first draft.

---

## Runtime Discovery Output

Runtime Discovery produces or updates the six reasoning architecture objects:

1. **Optimizer State** — active goal, relevant policies, current interpretation
2. **Premise Stack** — artifacts and assumptions producing the expectation
3. **Decision State** — selected direction, alternatives, constraints, sufficiency
4. **Investigation Trace** — what was checked, what contradictions were found
5. **Learning Event** — where reality contradicts expectation (post-outcome)
6. **Model Update Object** — reusable learning (post-outcome)

---

## Discovery Pattern Learning

A mature discovery system learns not only what strategies work, but which interaction patterns produce:
- Lower necessary user friction
- Better reasoning-object quality
- Better generated artifacts
- Better downstream outcomes

### Discovery Pattern Update

A specialized Model Update Object that records which discovery interaction pattern produced better results for a class of work.

**Definition:**
> A Discovery Pattern Update is a Model Update Object that records which discovery interaction pattern produced lower necessary user friction, better reasoning-object quality, better generated artifacts, or better downstream outcomes for a class of work.

### Why This Is Architecture-Level

Discovery is how messy human intent becomes structured reasoning state. If the discovery pattern is bad, the system produces weak reasoning objects → weak artifacts → ambiguous outcomes → unreliable learning. Therefore Discovery Pattern Learning affects reasoning quality itself.

---

## Validation: Healthcare Campaign Simulation

**User input:** "I want to do a healthcare campaign."

**System inference from existing artifacts:** Product (RPM for cardiology), likely ICP (practice administrators), prior sales objections, prior model update (provider campaigns underperform when feature-led).

**Minimal clarification:** "Are we targeting practice-level operators or health-system executives?"

**Generated:** Campaign brief, ICP summary, messaging pillars, LinkedIn posts, email drip, signage concepts, commercial concepts, compliance watchlist, measurement plan, prediction error triggers.

**Post-campaign learning:** Workflow-pain messaging attracted attention but didn't reliably produce qualified demo intent. Model Update: workflow burden is an attention signal, not evidence of buying intent. Future campaigns should combine with readiness filters.

**Discovery Pattern Learning:** The low-friction flow worked for artifacts but missed a readiness variable. Update: for healthcare demo campaigns, add one readiness question after ICP strawman.

---

## Complete Discovery Framework

```
Discovery Framework
    = Initial Discovery (map existing reasoning environment)
    + Runtime Discovery (process new work as it enters)
    + Discovery Pattern Learning (improve discovery itself over time)
```

### Runtime Discovery Loop

```
New user objective or proposal
    ↓
Retrieve existing artifacts and prior learning
    ↓
Infer optimizer state and premise stack
    ↓
Propose strawman
    ↓
Ask only high-impact clarifying questions
    ↓
Generate artifacts
    ↓
Preserve reasoning objects
    ↓
Track outcome
    ↓
Create Learning Event / Model Update Object if needed
    ↓
Create Discovery Pattern Update if interaction pattern should change
```

### Key Principle

> Discovery should minimize human burden by converting available artifacts into proposed reasoning objects before asking for clarification.

Or: **Do the work first. Ask only where uncertainty matters.**

---

## Cross-References
- `REASONING_ARCHITECTURE.md` (the six objects discovery produces)
- `MODEL_UPDATE_OBJECTS.md` (Discovery Pattern Updates are a specialization)
- `LEARNING.md` (discovery feeds the learning loop)
- `OPTIMIZER_MOTION.md` (discovery is how the system encounters new work)
- OP_001 (Decision Topography Discovery — the earlier, less refined version)
- VP Marketing Visibility Interview (07_NARRATIVE_ARCHITECTURE/EXAMPLES.md — the interview predecessor)
