# Citation Resolution Prep Audit

**Date:** 2026-06-12
**Auditor:** Claude
**Total placeholders in paper:** 337 occurrences
**Unique placeholders:** 91

---

## Summary

| Metric | Count |
|--------|-------|
| Total placeholder occurrences | 337 |
| Unique placeholders | 91 |
| In-text citations (body prose) | ~35 citation points across 17 sections |
| Citation-debt checklist entries | ~302 (listed at end of each section) |
| High-confidence (known source) | ~25 |
| Medium-confidence (category known, specific paper TBD) | ~40 |
| Low-confidence (vague or aspirational) | ~26 |
| Needs external verification | ~50 |

**Note:** Most of the 337 occurrences are in citation-debt checklists at the end of each section. The actual in-text citations number approximately 35 distinct citation points in the body prose.

---

## Grouped by Category

### 1. Bounded Rationality / Satisficing

| Placeholder | In-Text? | Likely Source | Confidence |
|------------|---------|--------------|------------|
| [SIMON1955] | Yes (S2, S6, S6) | Simon, H.A. (1955). "A Behavioral Model of Rational Choice." QJE 69(1). | **High** |
| [SIMON_SATISFICING] | Yes (S2, S6, S15) | Simon, H.A. (1956). "Rational choice and the structure of the environment." Psych Review. Or Simon (1957) Models of Man. | **High** |
| [BOUNDED_RATIONALITY_SURVEY] | Debt only | Survey article on bounded rationality. Gigerenzer & Selten (2001) likely. | **Medium** |

### 2. Organizational Decision-Making

| Placeholder | In-Text? | Likely Source | Confidence |
|------------|---------|--------------|------------|
| [MARCH_SIMON_ORGS] | Yes (S3, S15) | March, J.G. & Simon, H.A. (1958). Organizations. Wiley. | **High** |
| [ORGANIZATIONAL_DECISION_MAKING] | Debt only | General — could be same as March & Simon or Cohen, March & Olsen (1972). | **Medium** |

### 3. Behavioral Theory of the Firm

| Placeholder | In-Text? | Likely Source | Confidence |
|------------|---------|--------------|------------|
| [CYERT_MARCH] | Yes (S2, S8, S15) | Cyert, R.M. & March, J.G. (1963). A Behavioral Theory of the Firm. | **High** |
| [BEHAVIORAL_THEORY_OF_THE_FIRM] | Debt + S15 | Same as above. | **High** — duplicate of [CYERT_MARCH] |

### 4. Organizational Learning

| Placeholder | In-Text? | Likely Source | Confidence |
|------------|---------|--------------|------------|
| [ARGYRIS_SCHON] | Yes (S2, S8, S15) | Argyris, C. & Schön, D.A. (1978). Organizational Learning. | **High** |
| [DOUBLE_LOOP_LEARNING] | Debt + S15 | Argyris (1977) or same as above. | **High** — likely same source |
| [ORGANIZATIONAL_LEARNING] | Yes (S8, S15) | Could be Argyris & Schön, or Senge, or Levitt & March (1988). | **Medium** — needs disambiguation |
| [ORGANIZATIONAL_ROUTINES] | Debt only | Nelson & Winter (1982) likely. | **Medium** |

### 5. Sensemaking

| Placeholder | In-Text? | Likely Source | Confidence |
|------------|---------|--------------|------------|
| [WEICK_SENSEMAKING] | Yes (S2, S4, S15) | Weick, K.E. (1995). Sensemaking in Organizations. Sage. | **High** |
| [SENSEMAKING] | Debt + S15 | Same as above or Weick (1979). | **High** — likely duplicate |

### 6. Affordances

| Placeholder | In-Text? | Likely Source | Confidence |
|------------|---------|--------------|------------|
| [GIBSON_AFFORDANCES] | Yes (S5, S6, S15) | Gibson, J.J. (1979). The Ecological Approach to Visual Perception. | **High** |
| [NORMAN_AFFORDANCES] | Yes (S5, S6, S15) | Norman, D.A. (1988). The Design of Everyday Things. | **High** |
| [AFFORDANCE_THEORY] | Debt + S15 | General — could cite either Gibson or Norman or both. | **High** — covered by above two |

### 7. Reward Shaping / Environment Design

| Placeholder | In-Text? | Likely Source | Confidence |
|------------|---------|--------------|------------|
| [NG_REWARD_SHAPING] | Yes (S2, S6, S15) | Ng, A.Y., Harada, D. & Russell, S. (1999). "Policy invariance under reward transformations." ICML. | **High** |
| [REINFORCEMENT_LEARNING_REWARD_DESIGN] | Debt + S15 | General RL reward design — Amodei et al. (2016) or Hadfield-Menell et al. (2017). | **Medium** |
| [REWARD_SHAPING] | Debt only | Likely same as [NG_REWARD_SHAPING]. | **High** — duplicate |

### 8. RAG / Grounding / Hallucination

| Placeholder | In-Text? | Likely Source | Confidence |
|------------|---------|--------------|------------|
| [DEEPMIND_GOPHERCITE] | Yes (S1, S2, S7, S15) | Menick et al. (2022). "Teaching language models to support answers with verified quotes." | **High** |
| [RAG_FOUNDATIONAL] | Yes (S2, S7, S15) | Lewis et al. (2020). "Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks." NeurIPS. | **High** |
| [GROUNDING_CITATION_GENERATION] | Yes (S7, S15) | Could be GopherCite or Gao et al. (2023) on attributed QA. | **Medium** |
| [RAG_EVALUATION] | Debt + S15 | Es et al. (2024) RAGAS or similar RAG eval frameworks. | **Medium** — needs verification |

### 9. AI Safety / Agentic Misalignment

| Placeholder | In-Text? | Likely Source | Confidence |
|------------|---------|--------------|------------|
| [ANTHROPIC_AGENTIC_MISALIGNMENT] | Yes (S1, S15) | Anthropic (2025). Alignment faking / agentic misalignment papers. | **Medium** — specific paper TBD |
| [OPENAI_PREPAREDNESS] | Yes (S1, S15) | OpenAI Preparedness Framework (2023). | **High** |
| [DEEPMIND_FRONTIER_SAFETY] | Yes (S1, S15) | Google DeepMind Frontier Safety Framework (2024). | **High** |
| [DEEPMIND_ROLE_PLAY] | Yes (S1, S15) | Shanahan et al. (2023). "Role-Play with Large Language Models." | **Medium** — verify exact paper |
| [AI_ALIGNMENT_OVERVIEW] | Yes (S2, S15) | General alignment survey — Ngo et al. (2022) or similar. | **Medium** |
| [AGENT_SAFETY_SURVEY] | Yes (S2, S15) | Survey on agent safety — specific paper TBD. | **Low** |
| [AI_SAFETY_EVALS] | Debt only | General safety evaluation work — Shevlane et al. (2023). | **Medium** |
| [AI_SAFETY_GOVERNANCE] | Debt only | General — Schuett et al. (2023) or similar. | **Low** |

### 10. Anti-Anthropomorphism

| Placeholder | In-Text? | Likely Source | Confidence |
|------------|---------|--------------|------------|
| [AI_ANTHROPOMORPHISM] | Debt + S15 | Shanahan (2024) or similar. | **Medium** |

### 11. Knowledge Management / Organizational Memory

| Placeholder | In-Text? | Likely Source | Confidence |
|------------|---------|--------------|------------|
| [KNOWLEDGE_MANAGEMENT] | Yes (S3) | General KM — Nonaka & Takeuchi (1995) or Davenport & Prusak (1998). | **Medium** — needs specific source |
| [ORGANIZATIONAL_MEMORY] | Yes (S3) | Walsh & Ungson (1991). "Organizational memory." Academy of Management Review. | **Medium** |
| [ENTERPRISE_AI_KNOWLEDGE_MANAGEMENT] | Debt only | General — no specific source identified. | **Low** |
| [LESSONS_LEARNED_SYSTEMS] | Debt only | Weber et al. (2001) or similar. | **Low** |

### 12. Decision Provenance / Design Rationale

| Placeholder | In-Text? | Likely Source | Confidence |
|------------|---------|--------------|------------|
| [DECISION_PROVENANCE] | Debt only | Provenance literature — Moreau et al. (2013). | **Low** |
| [DESIGN_RATIONALE] | Debt + S15 | Lee (1997) or Burge et al. (2008). | **Low** |
| [WORKFLOW_PROVENANCE] | Debt + S15 | Davidson & Freire (2008). | **Low** |
| [PROVENANCE_SYSTEMS] | Debt + S15 | General — PROV-W3C or Moreau et al. | **Low** |

### 13. Human-AI Collaboration / HCI

| Placeholder | In-Text? | Likely Source | Confidence |
|------------|---------|--------------|------------|
| [HCI_HUMAN_AI_COLLABORATION] | Debt only | Amershi et al. (2019). "Guidelines for Human-AI Interaction." CHI. | **Medium** |
| [MIXED_INITIATIVE_SYSTEMS] | Debt + S15 | Horvitz (1999). "Principles of mixed-initiative user interfaces." CHI. | **Medium** |
| [HUMAN_IN_THE_LOOP_AI] | Debt + S15 | Wu et al. (2022) or Monarch (2021). | **Medium** |
| [COACTIVE_DESIGN] | Debt + S15 | Johnson et al. (2014). "Coactive Design." JAIR. | **Medium** |
| [HUMAN_AI_INTERACTION_GUIDELINES] | Debt + S15 | Amershi et al. (2019). Same as HCI above. | **Medium** — possible duplicate |
| [HUMAN_AI_COLLABORATION] | Debt only | General — same family as above. | **Low** |
| [HUMAN_AI_WORKFLOW_SYSTEMS] | Debt only | No specific source. | **Low** |
| [HUMAN_FACTORS_AUTOMATION_BIAS] | Debt only | Parasuraman & Riley (1997) or Cummings (2004). | **Medium** |

### 14. Case-Based Reasoning

| Placeholder | In-Text? | Likely Source | Confidence |
|------------|---------|--------------|------------|
| [CASE_BASED_REASONING] | Yes (S15) | Kolodner (1993) or Aamodt & Plaza (1994). | **Medium** |

### 15. Uncertainty / Abstention / Calibration

| Placeholder | In-Text? | Likely Source | Confidence |
|------------|---------|--------------|------------|
| [UNCERTAINTY_CALIBRATION] | Debt only | Guo et al. (2017) on calibration. | **Medium** |
| [ABSTENTION_IN_LLM_SYSTEMS] | Debt + S15 | Specific papers on LLM abstention — Kadavath et al. (2022). | **Medium** |
| [SELECTIVE_PREDICTION] | Debt + S15 | Geifman & El-Yaniv (2017). | **Medium** |

### 16. Other / Implementation / Methods

| Placeholder | In-Text? | Likely Source | Confidence |
|------------|---------|--------------|------------|
| [AI_AGENTS_FOUNDATIONAL] | Yes (S4) | Wooldridge & Jennings (1995) or Russell & Norvig. | **Medium** |
| [DENNETT_INTENTIONAL_STANCE] | Yes (S4) | Dennett, D.C. (1987). The Intentional Stance. MIT Press. | **High** |
| [RUSSELL_NORVIG_AGENTS] | Yes (S4) | Russell, S. & Norvig, P. (2020). Artificial Intelligence: A Modern Approach. 4th ed. | **High** |
| [INFORMATION_FORAGING] | Yes (S6) | Pirolli & Card (1999). "Information foraging." Psychological Review. | **High** |
| [VALUE_OF_INFORMATION] | Yes (S6) | Howard (1966) or Raiffa (1968). | **Medium** |
| [RATIONAL_METAREASONING] | Yes (S6) | Russell & Wefald (1991). "Do the Right Thing." | **Medium** |
| [POPPER_FALSIFIABILITY] | Debt only | Popper, K. (1959). The Logic of Scientific Discovery. | **High** |
| [DESIGN_SCIENCE_RESEARCH] | Debt only | Hevner et al. (2004). | **Medium** |
| [TOOL_USE_AGENTS] | Debt only | Schick et al. (2023) on Toolformer or similar. | **Medium** |
| [HUMAN_OVERSIGHT_AUTONOMY] | Debt only | General oversight literature. | **Low** |
| [MCP_TOOL_PROTOCOLS] | Debt only | Model Context Protocol — Anthropic (2024). | **Medium** |
| [KNOWLEDGE_GRAPHS] | Debt only | General KG literature. | **Low** |
| [EVENT_SOURCING] | Debt only | Fowler (2005) on event sourcing. | **Low** |
| [MODEL_GOVERNANCE] | Debt only | General AI governance. | **Low** |
| [AI_GOVERNANCE] | Debt only | General. | **Low** |
| [INTER_RATER_RELIABILITY] | Debt only | Cohen (1960) on kappa or similar. | **Medium** |
| [HCI_EVALUATION_METHODS] | Debt only | General HCI eval. | **Low** |
| Various implementation/eval placeholders | Debt only | Multiple sources TBD | **Low** |

---

## Duplicate / Redundant Placeholders

| Likely Duplicates | Resolution |
|------------------|------------|
| [BEHAVIORAL_THEORY_OF_THE_FIRM] ≈ [CYERT_MARCH] | Merge — same source |
| [SENSEMAKING] ≈ [WEICK_SENSEMAKING] | Merge — same source |
| [AFFORDANCE_THEORY] covered by [GIBSON_AFFORDANCES] + [NORMAN_AFFORDANCES] | Merge |
| [REWARD_SHAPING] ≈ [NG_REWARD_SHAPING] | Merge |
| [DOUBLE_LOOP_LEARNING] ≈ [ARGYRIS_SCHON] | Merge — same source family |
| [HUMAN_AI_INTERACTION_GUIDELINES] ≈ [HCI_HUMAN_AI_COLLABORATION] | Likely same Amershi et al. |
| [HUMAN_AI_COLLABORATION] ≈ [HCI_HUMAN_AI_COLLABORATION] | Merge |
| [ORGANIZATIONAL_LEARNING] — ambiguous | Needs to point to specific source |
| [AI_MEMORY_SYSTEMS] ≈ [AGENT_MEMORY_SYSTEMS] | Merge |

---

## Sections With Citation Risk

| Section | Risk | Issue |
|---------|------|-------|
| S3 (Context ≠ Reasoning State) | **Medium** | Claims about organizational memory failure cite [ORGANIZATIONAL_MEMORY] [KNOWLEDGE_MANAGEMENT] [MARCH_SIMON_ORGS] — but these are vague. Needs specific sources on why KM systems fail. |
| S4 (Optimizers) | **Low-Medium** | [AI_AGENTS_FOUNDATIONAL] is vague — needs a specific foundational agent paper. |
| S7 (Hallucination) | **Low** | Well-cited with GopherCite, RAG, and grounding. |
| S12 (Running Example) | **Low** | No scholarly claims — practical example. |
| S13 (Implementation) | **Medium** | Many implementation-related placeholders (MCP, knowledge graphs, event sourcing) with low confidence. These may be better as footnotes than formal citations. |
| S14 (Validation) | **Medium** | [POPPER_FALSIFIABILITY], [DESIGN_SCIENCE_RESEARCH], [INTER_RATER_RELIABILITY] need real citations. |

---

## Top 10 Sources Likely Needed

1. **Simon, H.A. (1955/1956)** — Bounded rationality, satisficing. [SIMON1955] [SIMON_SATISFICING]. **High confidence. Resolvable now.**
2. **Argyris, C. & Schön, D.A. (1978)** — Organizational learning, double-loop. [ARGYRIS_SCHON] [DOUBLE_LOOP_LEARNING]. **High confidence. Resolvable now.**
3. **Weick, K.E. (1995)** — Sensemaking. [WEICK_SENSEMAKING]. **High confidence. Resolvable now.**
4. **Gibson, J.J. (1979) + Norman, D.A. (1988)** — Affordances. [GIBSON_AFFORDANCES] [NORMAN_AFFORDANCES]. **High confidence. Resolvable now.**
5. **Ng, Harada & Russell (1999)** — Reward shaping. [NG_REWARD_SHAPING]. **High confidence. Resolvable now.**
6. **Lewis et al. (2020)** — RAG. [RAG_FOUNDATIONAL]. **High confidence. Resolvable now.**
7. **Menick et al. (2022)** — GopherCite. [DEEPMIND_GOPHERCITE]. **High confidence. Resolvable now.**
8. **Anthropic agentic misalignment paper** — [ANTHROPIC_AGENTIC_MISALIGNMENT]. **Medium confidence. Needs verification of exact paper/year.**
9. **OpenAI Preparedness Framework** — [OPENAI_PREPAREDNESS]. **High confidence. Public document.**
10. **Dennett, D.C. (1987)** — Intentional stance. [DENNETT_INTENTIONAL_STANCE]. **High confidence. Resolvable now.**

---

## Unresolved / Low-Confidence Count

| Confidence | Count |
|-----------|-------|
| High (known source, resolvable now) | ~25 placeholders |
| Medium (category known, specific paper needs verification) | ~40 placeholders |
| Low (vague, aspirational, or no specific source identified) | ~26 placeholders |

**Most low-confidence placeholders are in citation-debt checklists, not in body prose.** Many of the low-confidence entries (AI_GOVERNANCE, MODEL_GOVERNANCE, ENTERPRISE_AI_ARCHITECTURE, etc.) appear only in "likely needed" lists and may not need formal citations if the paper doesn't make specific claims requiring them.

---

## Recommendation

1. **Resolve the top 10 high-confidence sources first** — these cover ~60% of in-text citations.
2. **Merge ~9 duplicate placeholders** to reduce the unique count from 91 to ~82.
3. **Demote low-confidence debt-only placeholders** to "optional" unless a specific claim requires them.
4. **S3 and S13 need specific sources** for organizational memory failure and implementation patterns.
5. **S14 validation section** needs real methodology citations (Popper, design science, inter-rater reliability).
