# Review Report: Skeptical Practitioner

## Thesis Playback

The paper argues that AI agents should be understood not as moral actors but as optimizer-like systems moving through perceived information landscapes, and that safer, more reliable human-agent systems require designing those landscapes -- not just building stronger boxes. It proposes a set of reasoning objects (Goal, Policy, Interpretation, topography dimensions, Model Update Objects, etc.) that organizations should preserve so that future workflows start smarter instead of cold.

The practical payoff claim is that if you preserve the *why* behind decisions -- not just the documents -- you get systems that learn, avoid repeated mistakes, and produce better work over time.

## What Works

1. **The marble analogy and the fence-vs-landscape distinction** (Section 1). This is the single best moment in the paper. It is concrete, immediately graspable, and earns the rest of the argument. A practitioner reads that and thinks: yes, I have seen this. I have watched people blame the marble.

2. **The "reduces readmissions" example** (Section 7.5, Case A). This is a real problem that real marketers face. The system catching a clinical outcome claim and offering softer language -- that is something I would actually want built. It does not feel theoretical. It feels like a Tuesday.

3. **The distinction between reaction and learning** (Section 8.8). This is genuinely useful. The examples -- "Campaign underperformed, reaction: stop targeting healthcare" vs. the more precise investigation -- land because every practitioner has sat in a meeting where that exact wrong lesson was drawn.

4. **Sufficiency vs. certainty** (Section 6.5). The low-confidence-high-sufficiency and high-confidence-low-sufficiency examples are clear and immediately applicable. This is the kind of distinction practitioners can use without adopting the entire framework.

5. **The "do the reasoning work before asking the user to do it" principle** (Section 11). This is the most practically important sentence in the paper, and it does not need the framework to be true. It stands on its own as a design principle. Good.

6. **Appendix A, especially Phase 1 questions 5 and 6.** "What information is difficult to access or repeatedly surprises you?" and "What assumptions drive your actions?" -- these are questions a consultant could use in a real workshop tomorrow morning.

## Where the Paper Loses the Reader

1. **The healthcare campaign example does not stop.** It appears at least ten times across the paper. By Section 12, I have read essentially the same RPM-cardiology-workflow-pain-buying-stage scenario so many times that the repetition has gone from helpful to numbing. The example was effective in Sections 3-4. By Section 12 it feels like the paper has only one example and is riding it to death. A practitioner will wonder: does this framework work for anything besides healthcare campaigns?

2. **Sections 4-6 are slow and over-scaffolded.** The paper defines each concept, then explains why it is not a different concept, then explains why it was not promoted to a primitive, then demonstrates it with the same campaign example. The intellectual hygiene is admirable but the reader experience is a lecture. A practitioner will skim or bail. The paper takes roughly 2,500 words to say "Goal, Policy, Interpretation" and another 2,500 to say "Visibility, Accessibility, Representation, Confidence, Connectivity." That is 5,000 words of vocabulary with the same illustration repeated.

3. **Section 10 (Reasoning Architecture) is where the paper becomes a framework-for-frameworks.** Six objects, each with a table, each with a campaign example, each with a safety example. By the time the reader hits "Optimizer State -> Premise Stack -> Decision State -> Investigation Trace -> Learning Event -> Model Update Object," the paper has produced a taxonomy that feels heavy. A practitioner will ask: who is going to create all of these objects? Section 11 answers that question, but the damage is done. The heavy schema appears before the relief valve.

4. **Section 13 (Implementation Bridge) provides a component table and a data schema but no evidence that anyone has built this.** The maturity model (Stage 0 through Stage 4) is the kind of thing consultants put in slide decks. Without a single case study, prototype, or even a sketch of a working system, this section reads as aspirational architecture, not implementation guidance.

5. **Section 15 (Related Work) is 18 subsections of "we were influenced by X."** This is intellectually honest but operationally dead weight. A practitioner will not care that the framework is downstream of Gibson 1979 or Cyert and March 1963. The lineage section could be compressed to a single table and a paragraph.

## Strongest Contribution

The reframe from "what is wrong with the agent?" to "what landscape did we ask it to move through?" is the paper's strongest and most exportable idea. It changes how a practitioner thinks about failure diagnosis. It is also the idea that survives even if the full framework is too heavy to adopt. A team could use this reframe without ever creating a single Model Update Object.

The second strongest contribution is the concept of premature sufficiency (Section 7) as a unifying explanation for hallucination and harmful action. That is a genuinely useful diagnostic lens.

## Weakest or Least-Supported Claim

**"Model Update Objects reduce repeated mistakes more effectively than ordinary postmortems"** (Claim 5, Section 14.1).

This is the paper's central operational claim, and it has zero evidence behind it. No case study, no prototype, no pilot, no user test. The paper acknowledges this in Section 14 by listing it as a testable claim, but the gap is still large. The entire learning architecture (Sections 8-10) rests on the assumption that structured reasoning objects are better than narrative memory. That assumption is plausible but undemonstrated.

A skeptical reader will note that organizations have tried structured knowledge management before (lessons-learned databases, case repositories, decision logs). Many of those systems failed not because the schema was wrong but because nobody wanted to fill them out, nobody trusted the entries, and nobody retrieved them. The paper partially addresses this with Discovery (Section 11) but does not confront the graveyard of prior knowledge-management initiatives that looked exactly like this.

## Usefulness Assessment

**What would I actually use?**

- The fence-vs-landscape reframe. Immediately usable in any design review or incident postmortem.
- The premature sufficiency diagnosis. Usable for hallucination triage and unsafe-action analysis.
- The sufficiency-vs-certainty distinction. Usable for calibrating when systems should act vs. investigate.
- The "do the reasoning work before asking the user" principle. Usable for any AI product design.
- Appendix A, Phase 1 (Questions 1-7). Usable as a workshop tool for scoping an AI implementation.
- The "reduces readmissions" compliance example. Usable as a pattern for claims-sensitive generation.

**What would I not use?**

- The full six-object reasoning architecture as described. Too heavy for most teams without significant tooling support.
- The eleven-field Core Learning Payload. The fields are individually defensible, but the schema as a whole is intimidating. Most organizations will not fill out eleven fields per learning event.
- The maturity model (Section 13.10). It does not tell me anything I could not infer from the rest of the paper.
- The lineage section in its current form. I would skip it entirely.

**What would make me use more of it?**

Evidence. A single case study showing: we used the framework, here is the before, here is the after, here is what happened on the second cycle. Without that, the framework remains a compelling vocabulary, not a demonstrated method.

## Appendix A Assessment

Appendix A partially rescues the paper from abstraction. The Decision Topography Interview is the most practically usable section of the entire paper. The three-part structure (What are we asking? / Why are we asking? / What will we do with the answer?) is well designed and would work in a real workshop setting.

However, Appendix A also reveals a tension. The interview is good enough to stand alone as a practical tool without the full framework behind it. A practitioner could use these 23 questions without ever reading Sections 4-10. That is both a strength (the interview is genuinely useful) and a weakness (it suggests the framework machinery may be heavier than the practical payoff requires).

Phase 1 is the strongest. Phases 2-3 are solid. Phase 4 starts to feel like the framework is asking the practitioner to do the framework's homework.

Question 23 ("Did preserved reasoning actually improve the next cycle?") is the right question to end on. It grounds the entire interview in outcome accountability.

## Credibility / Evidence Assessment

The paper cites well and from relevant traditions. The intellectual lineage is real. Simon, Weick, Argyris, Gibson, Norman -- these are serious sources and they do support the conceptual moves the paper makes.

But the paper has a credibility gap between its theoretical apparatus and its empirical base. The framework makes strong operational claims -- that Model Update Objects are better than postmortems, that reasoning-state preservation improves future work, that Discovery reduces burden while increasing quality -- and supports none of them with empirical evidence.

Section 14 is honest about this. It lists testable claims and falsifiers. That intellectual honesty is valuable. But it does not substitute for evidence.

The paper also relies on a single domain example (healthcare marketing campaigns) for virtually all of its illustrations. This creates a risk: the reader cannot tell whether the framework generalizes or whether it was designed around the example. Adding even one worked example from a different domain (incident response, customer support, compliance review) would substantially increase credibility.

## Strongest Objection

**The framework solves a real problem but may reproduce the failure mode of every structured knowledge-management initiative of the last 30 years: high-quality schema, low adoption.**

The paper implicitly assumes that if you build the right reasoning objects and the right discovery process, people will create, maintain, retrieve, and trust these objects. History suggests otherwise. Lotus Notes had structured knowledge bases. SharePoint had lessons-learned libraries. ITIL had post-incident review templates. Most of these became graveyards.

The paper's answer is Discovery -- the system fills in the objects so the human does not have to. That is a reasonable answer, but it shifts the problem: now the question is whether AI-inferred reasoning objects will be accurate enough to be trusted, maintained, and retrieved. If they are wrong 20% of the time, will users learn to ignore them? If they are right but never retrieved, do they matter?

The paper needs to confront this objection directly rather than deferring it to future validation.

## Recommended Changes for v1.0

### Blocking

1. **Add at least one non-marketing worked example.** The paper currently runs on a single healthcare campaign scenario repeated across 12+ sections. One additional domain -- incident response, customer support triage, compliance review, or sales enablement -- would demonstrate that the framework generalizes. Without this, the paper reads as a theory built around one use case.

2. **Confront the knowledge-management graveyard.** Add a direct discussion (in Section 9, Section 13, or the Related Work) acknowledging that structured organizational learning repositories have failed before and explaining specifically what is different this time. "Discovery" is the answer, but the paper needs to say so explicitly and honestly.

3. **Compress Sections 4-6.** These sections can be cut by 30-40% without losing any conceptual content. The pattern of "define term, explain what it is not, show campaign example, show safety example" is repeated too many times. State the concepts, illustrate them once, move on.

### Important but Non-Blocking

4. **Vary the running example.** Even within healthcare marketing, the paper could show a different scenario for some sections (e.g., a failed compliance review, a mistargeted campaign in a different specialty, or an agent that over-escalates). Using the same RPM-cardiology-workflow-pain-buying-stage sequence twelve times makes the framework feel narrow.

5. **Compress Section 15 (Related Work).** Convert the 18 subsections into a single table mapping framework component to intellectual tradition, with one paragraph of prose explaining the synthesis claim. The current format is respectful but exhausting.

6. **Move the Model Update Object example (Section 9.6) earlier.** The reader encounters the eleven-field schema (Section 9.3) before seeing what a filled-out object looks like. Show the example first, then explain the fields. This is a basic pedagogical fix.

7. **Acknowledge automation bias more directly.** Section 13.12 mentions it in a risk table, but the paper should address head-on: if the system infers reasoning state and proposes strawmen, users may anchor on wrong inferences. This is a known HCI problem and the paper should say more about when inference helps vs. when it misleads.

### Optional Polish

8. **Cut the word count by 15-20% overall.** The paper is approximately 18,000 words of body text plus a substantial appendix. For the audience the paper wants to reach (practitioners, builders, applied researchers), this is too long. The ideas are strong enough to survive compression.

9. **Remove or shorten Section 5.7 (Goal Relevance) and 5.8 (Policy as non-dimension).** These are internal architecture decisions that matter to the authors but not to the reader. A footnote or a single paragraph would suffice.

10. **Add a one-page "Framework at a Glance" summary** after Section 2 or before the Conclusion. A single diagram showing the full loop (Optimizer State -> Topography -> Motion -> Action -> Outcome -> Learning -> Model Update -> updated Topography) with one-line definitions would help practitioners who want the shape before the detail.

### Future Work

- A prototype implementation in one workflow, with before/after comparison.
- User testing of the Decision Topography Interview (Appendix A) in a real organizational setting.
- Inter-rater reliability testing on the five topography dimensions and the six reasoning objects.
- A second domain example developed to full depth (not marketing).
- Empirical comparison: context-only vs. reasoning-state workflow on repeated decision quality.

## One-Sentence Verdict

The paper contains a genuinely useful reframe (landscape, not box) and several practical ideas worth stealing, but it is currently 40% longer than its evidence base can support and needs a second worked domain, a confrontation with the knowledge-management graveyard, and significant compression before it will hold a practitioner's attention through to the end.
