1:# The Perceived Topography Framework
3:## A Reasoning-State Architecture for Human-Agent Systems
5:### Draft Status
13:# 1. Introduction: From Agent Fear to Topography Design
101:# 2. A Note on Terms
107:## Optimizer
115:## Agent
121:## Goal
127:## Policy
133:## Interpretation
141:## Reasoning State
147:## Topography
155:## Perceived Topography
161:## Information Surface
169:## Gradient
177:## Visibility
183:## Accessibility
189:## Representation
197:## Confidence
205:## Connectivity
213:## Attraction
219:## Investigation
225:## Sufficiency
233:## Action
239:## Prediction Error
245:## Learning
253:## Premise Stack
261:## Model Update Object
267:## Discovery
281:## Alignment
289:## Governance
295:## Hallucination
303:## Summary of Usage
346:# 3. The Problem: Context Is Not Reasoning State
374:## Documents Preserve Artifacts, Not State Transitions
402:## Context Without Reasoning Can Increase Risk
429:## Reasoning State Is the Missing Unit
447:## The Healthcare Campaign Example
491:## Why This Matters for Safety
511:## The Paper's Design Claim
563:# 4. Optimizers: Goal, Policy, Interpretation
593:## 4.1 Goal
630:## 4.2 Policy
673:## 4.3 Interpretation
705:## 4.4 Optimizer State
747:## 4.5 Why These Three Primitives Are Enough
785:## 4.6 Why This Matters for Agent Safety
824:## 4.7 Transition to Information Topography
876:# 5. Information Topography: What the Optimizer Navigates
902:## 5.1 The Five Dimensions of Information Topography
930:## 5.2 Visibility
952:## 5.3 Accessibility
970:## 5.4 Representation
986:## 5.5 Confidence
1017:## 5.6 Connectivity
1043:## 5.7 Why Goal Relevance Is Relational
1067:## 5.8 Policy as Boundary Condition, Not Dimension
1093:## 5.9 Topography and Affordances
1107:## 5.10 Information Topography in the Healthcare Campaign Example
1143:## 5.11 Information Topography and Safety
1161:## 5.12 Transition to Motion
1210:# 6. Gradients and Motion: How Behavior Emerges
1240:## 6.1 Gradients
1262:## 6.2 Attraction
1278:### Action Attraction
1284:### Exploration Attraction
1296:## 6.3 Investigation
1322:## 6.4 Task Spawning
1344:## 6.5 Sufficiency
1376:## 6.6 Action
1398:## 6.7 Motion in the Healthcare Campaign Example
1422:## 6.8 Motion in Safety Failures
1426:### Hallucination
1434:### Unsafe Tool Use
1442:### Constraint Circumvention
1454:## 6.9 Motion and Design
1470:## 6.10 Transition to Learning
1525:# 7. Hallucination and Harmful Action as Related Failures
1545:## 7.1 Hallucination as Premature Sufficiency
1565:## 7.2 Harmful Action as Premature Sufficiency
1587:## 7.3 The Shared Failure Grammar
1607:## 7.4 Why More Context Is Not Enough
1627:## 7.5 Two Cases: Unsupported Claims and Unsafe Actions
1631:### Case A: Unsupported Claim
1651:### Case B: Unsafe Tool Action
1671:## 7.6 The Role of "I Don't Know" and "I Should Not Act Yet"
1691:## 7.7 Same Pattern, Different Severity
1713:## 7.8 Implications for Evaluation
1729:## 7.9 Transition to Learning
1776:# 8. Learning: When Reality Pushes Back
1804:## 8.1 Expectation
1824:## 8.2 Action
1840:## 8.3 Outcome
1854:## 8.4 Prediction Error
1880:## 8.5 Investigation
1898:## 8.6 Evidence-Supported Explanation
1923:## 8.7 Model Update
1933:### Goal Update
1937:### Policy Update
1941:### Interpretation Update
1951:## 8.8 Reaction Is Not Learning
1971:## 8.9 Postmortem Is Not Learning
1989:## 8.10 Learning in the Healthcare Campaign Example
1991:### Prior Expectation
1994:### Action
1997:### Outcome
2000:### Prediction Error
2003:### Investigation
2006:### Evidence-Supported Explanation
2009:### Model Update
2020:## 8.11 Learning in Agent Safety
2022:### Prior Expectation
2025:### Action
2028:### Outcome
2031:### Prediction Error
2034:### Investigation
2037:### Evidence-Supported Explanation
2040:### Model Update
2047:## 8.12 Learning Changes the Topography
2067:## 8.13 The Learning Loop
2119:# 9. Model Update Objects: Making Learning Durable
2139:## 9.1 Why Ordinary Documentation Is Not Enough
2155:## 9.2 The Three-Layer Structure
2165:## 9.3 Core Learning Payload
2209:## 9.4 Observability Envelope
2223:## 9.5 Human-Ready View
2242:## 9.6 Example Model Update Object
2278:## 9.7 Failure Modes Model Update Objects Prevent
2295:## 9.8 Model Update Objects Reshape Topography
2313:## 9.9 Transition to Reasoning Architecture
2362:# 10. Reasoning Architecture: Preserving State Transitions
2380:## 10.1 Why Documents Are Not Enough
2394:## 10.2 Six Minimum Viable Reasoning Objects
2411:## 10.3 Optimizer State
2425:## 10.4 Premise Stack
2439:## 10.5 Decision State
2455:## 10.6 Investigation Trace
2467:## 10.7 Learning Event
2479:## 10.8 Model Update Object
2487:## 10.9 Supporting Concerns, Not New Objects
2504:## 10.10 The Objects as a State-Transition Chain
2516:## 10.11 Healthcare Campaign Example
2534:## 10.12 Agent Safety Example
2550:## 10.13 Relationship to Knowledge Management
2562:## 10.14 Relationship to AI Agents
2576:## 10.15 Transition to Discovery
2633:# 11. Discovery Framework: From Messy Intent to Reasoning State
2667:## 11.1 Why Discovery Matters
2691:## 11.2 Initial Discovery and Runtime Discovery
2693:### Initial Discovery
2701:### Runtime Discovery
2711:## 11.3 Retrieve
2721:## 11.4 Infer
2733:## 11.5 Propose
2743:## 11.6 Confirm
2757:## 11.7 Generate
2767:## 11.8 Preserve
2777:## 11.9 Learn
2787:## 11.10 Discovery Pattern Updates
2799:## 11.11 The Low-Friction Principle
2811:## 11.12 Discovery and Human Control
2825:## 11.13 Discovery and Safety
2837:## 11.14 Discovery in the Healthcare Campaign Example
2859:## 11.15 Discovery as the Front Door to Reasoning Architecture
2875:## 11.16 Transition to the Running Example
2923:# 12. Running Example: Adaptive Campaign Reasoning Studio
2935:## 12.1 Messy Human Intent
2949:## 12.2 Retrieve
2961:## 12.3 Infer
2973:## 12.4 Propose
2981:## 12.5 Confirm
2993:## 12.6 Sufficiency
3001:## 12.7 Generate
3021:## 12.8 Preserve
3039:## 12.9 Outcome
3047:## 12.10 Learning Event
3059:## 12.11 Model Update Object
3075:## 12.12 Discovery Pattern Update
3087:## 12.13 The Next Campaign Starts Smarter
3103:## 12.14 What This Example Demonstrates
3117:## 12.15 Transition to Implementation
3157:# 13. Implementation Bridge: From Context Layer to Reasoning-State Layer
3173:## 13.1 Layer 1: Context Layer
3187:## 13.2 Layer 2: Reasoning-State Layer
3201:## 13.3 Layer 3: Learning Layer
3214:## 13.4 Layer 4: Adaptive Workflow Studio
3226:## 13.5 Minimal Viable Implementation
3247:## 13.6 Suggested System Components
3265:## 13.7 Data Model Sketch
3285:## 13.8 Retrieval Requirements
3299:## 13.9 Human Review and Governance
3311:## 13.10 Implementation Maturity Model
3325:## 13.11 What Not to Build First
3335:## 13.12 Implementation Risks
3352:## 13.13 Implementation Success Criteria
3362:## 13.14 Transition to Validation
3409:# 14. Validation and Falsifiability: Keeping the Framework in Contact With Reality
3425:## 14.1 Testable Claims
3443:## 14.2 What Would Falsify the Framework?
3461:## 14.3 Levels of Validation
3477:## 14.4 Conceptual Validation
3487:## 14.5 Operational Validation
3497:## 14.6 Comparative Validation
3507:## 14.7 Adversarial Validation
3515:## 14.8 Longitudinal Validation
3525:## 14.9 Human Validation
3533:## 14.10 Outcome Validation
3543:## 14.11 Assumption Verification
3555:## 14.12 Evaluation of the Six Reasoning Objects
3570:## 14.13 Evaluation of the Five Topography Dimensions
3586:## 14.14 Validation in the Healthcare Campaign MVP
3596:## 14.15 The Framework Should Update Itself
3608:## 14.16 Transition to Related Work
3658:# 15. Related Work and Intellectual Lineage
3674:## 15.1 Bounded Rationality and Satisficing
3684:## 15.2 Organizational Decision-Making
3692:## 15.3 Behavioral Theory of the Firm
3700:## 15.4 Organizational Learning
3708:## 15.5 Sensemaking
3716:## 15.6 Affordances and Action Possibilities
3724:## 15.7 Reward Shaping and Environment Design
3732:## 15.8 Retrieval-Augmented Generation and Grounding
3742:## 15.9 AI Safety, Alignment, and Agentic Misalignment
3752:## 15.10 Anti-Anthropomorphism and Behavioral Description
3760:## 15.11 Knowledge Management and Organizational Memory
3768:## 15.12 Decision Provenance, Design Rationale, and Workflow Traceability
3776:## 15.13 Human-AI Collaboration and Mixed-Initiative Systems
3784:## 15.14 Case-Based Reasoning
3792:## 15.15 Uncertainty, Abstention, and Calibration
3800:## 15.16 What the Framework Adds
3814:## 15.17 Boundaries of the Contribution
3826:## 15.18 Citation Posture
3838:## 15.19 Transition to Implications
3862:# 16. Implications: What Changes If the Framework Is Useful
3872:## 16.1 Implication for AI Safety: Safety Is Also Topography Design
3886:## 16.2 Implication for Alignment: Alignment Is Distributed Across the System
3896:## 16.3 Implication for Enterprise AI: Context Layers Are Only the Beginning
3906:## 16.4 Implication for Knowledge Management: Preserve the State Transition
3916:## 16.5 Implication for Governance: Rules Must Exert Force
3926:## 16.6 Implication for Product Design: Build for Sufficiency, Not Just Completion
3936:## 16.7 Implication for Human-AI Collaboration: Ask Better, Not More
3946:## 16.8 Implication for Evaluation: Evaluate State Transitions, Not Only Outputs
3956:## 16.9 Implication for Organizational Learning: Postmortems Are Not the End
3964:## 16.10 Implication for Agent Memory: Memory Should Include Model Change
3972:## 16.11 Implication for Research: Study the Interaction Layer
3980:## 16.12 Implication for Builders: Start Small, Preserve the Loop
3988:## 16.13 The Deeper Shift
4000:## 16.14 Transition to Conclusion
4044:# 17. Conclusion: Build Better Landscapes
4070:## 17.1 The Core Aha
4084:## 17.2 Failure Has Shape
4098:## 17.3 Learning Is Not Memory
4110:## 17.4 Discovery Is the Front Door
4128:## 17.5 What Changes
4146:## 17.6 The Responsibility of the Landscape
4160:## 17.7 The Framework Must Remain Testable
4174:## 17.8 Build Better Landscapes
