# Keystone-to-Academic Literature Coverage Audit — 2026-06-25

## A. Citation Count Comparison

| Metric | Keystone | Academic |
|---|---|---|
| Unique in-text citations | 36 | 41 |
| Bibliography entries | 36 | 41 |
| Sources retained | — | 21 |
| Sources removed | — | 15 |
| Sources added | — | 20 |

The academic manuscript has more citations AND broader coverage despite removing 15 keystone sources.

## B. Removed Sources — Safe to Leave Removed (13)

| Source | Rationale |
|---|---|
| Shanahan et al., 2023 | Point restated from framework's own voice, not requiring external attribution |
| March & Simon, 1958 | Bounded rationality carried by Simon 1955 |
| Russell & Norvig, 2020 | Academic defines "optimizer-like" from scratch |
| Dennett, 1987 | Same — intentional stance not invoked |
| Ng et al., 1999 | Gradient introduced as topography concept, not reward shaping |
| Howard, 1966 | Information value theory not used in academic |
| Russell & Wefald, 1991 | Investigation grounded through Pirolli & Card instead |
| Cyert & March, 1963 | Behavioral theory of firm not directly invoked |
| Menick et al., 2022 | RAG grounding carried by Lewis et al., 2020 |
| Moreau et al., 2013 | PROV-DM is implementation-level; Lee 1997 covers design rationale |
| Guo et al., 2017 | Model calibration not discussed at that specificity |
| Kadavath et al., 2022 | Self-knowledge not discussed at that specificity |
| Aamodt & Plaza, 1994 | Case-based reasoning not invoked as a tradition |

## C. Removed Sources — May Need Restoration (2)

| Source | Concept | Academic still uses? | Recommendation |
|---|---|---|---|
| Wilson, 1999 | Information behavior models | S4 says "information-seeking behavior" but cites only Kuhlthau | **Restore** — add to S4 opening citation cluster |
| Bates, 1989 | Berrypicking / exploratory search | Not directly invoked | Leave removed |

## D. Literature Coverage Matrix

| # | Tradition | Keystone | Academic | Adequate? |
|---|---|---|---|---|
| 1 | Bounded rationality | Strong | Strong | Yes |
| 2 | Affordance theory | Strong | Strong | Yes |
| 3 | Situation awareness | Adequate | Adequate | Yes |
| 4 | Information seeking/foraging | Strong (4 sources) | Reduced (2 sources) | **Minor gap** — Wilson recommended |
| 5 | Sensemaking | Adequate | Adequate | Yes |
| 6 | Organizational memory | Strong | Strong | Yes |
| 7 | Organizational learning | Strong | Adequate | Yes |
| 8 | Knowledge reuse | Adequate | Adequate | Yes |
| 9 | Design rationale | Adequate | Adequate | Yes |
| 10 | Mixed-initiative interaction | Strong | Strong | Yes |
| 11 | Automation bias / trust | Strong | Strong | Yes |
| 12 | Human-AI interaction | Adequate | Strong | **Improved** |
| 13 | RAG / retrieval | Adequate | Adequate | Yes |
| 14 | Agent architectures | **Absent** | Strong (5 sources) | **Major improvement** |
| 15 | Agent memory / reflection | **Absent** | Adequate (3 sources) | **Major improvement** |
| 16 | Agent benchmarks | **Absent** | Strong (5 sources) | **Major improvement** |
| 17 | Hallucination / factuality | Adequate | Adequate | Yes |
| 18 | AI safety / alignment | Adequate (2) | Strong (6 sources) | **Major improvement** |
| 19 | Design science / falsifiability | **Absent** | Strong (5 sources) | **Major improvement** |
| 20 | Case-study methodology | Absent | Adequate | Improved |

**5 major improvements, 1 minor gap, 0 regressions.**

## E. Under-Cited Claims

None significant. All major claims are properly grounded.

## F. Properly Original Claims

All correctly framed as synthesis: perceived topography, premature sufficiency, five dimensions, optimizer state, reasoning-state architecture, Discovery, Model Update Objects, context/reasoning-state distinction, gradient as topography concept, adjacent truth.

## G. Recommended Patch

**One patch:**

Section 4, opening paragraph citation cluster.

Current: `[Gibson, 1979; Norman, 1988; Kuhlthau, 1991; Simon, 1955]`

Change to: `[Gibson, 1979; Norman, 1988; Wilson, 1999; Kuhlthau, 1991; Simon, 1955]`

Add bibliography entry:
`Wilson, T. D. (1999). Models in information behaviour research. Journal of Documentation, 55(3), 249-270.`

Reason: The phrase "information-seeking behavior" is explicitly used in the sentence but only Kuhlthau is cited. Wilson is the broader model-of-models reference.

## Pass Criteria

All 6 criteria met:
1. Every major keystone intellectual dependency accounted for ✓
2. Removed citations justified ✓
3. No uncited original-claim accidents ✓
4. No major grounding lost ✓
5. Citation density appropriate ✓
6. Synthesis remains original but visibly grounded ✓
