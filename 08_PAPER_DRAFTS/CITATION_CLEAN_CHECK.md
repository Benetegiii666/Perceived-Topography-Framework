# Body Citation Clean Check and Reference Ledger Sync Prep

**Date:** 2026-06-12
**Auditor:** Claude

---

## Part 1 — Body Citation Clean Check

| Location | Unresolved Placeholders |
|----------|----------------------|
| Body prose | **0** |
| Citation-debt checklists | 152 (65 unique) |
| Total | 152 |

**Body prose is citation-clean.** All in-text citations now use real author-year references. Zero unresolved placeholders appear outside checklist/debt sections.

---

## Part 2 — Actual In-Text Citation Inventory

**33 unique real citations** now appear in body prose.

| # | Citation | Frequency | Sections | Claim Family | In Ledger? | Needs Bib? |
|---|---------|-----------|----------|-------------|-----------|-----------|
| 1 | Simon, 1955 | 12 | S2, S6, S15 | Bounded rationality, sufficiency | Partial | No (known) |
| 2 | Argyris & Schön, 1978 | 10 | S2, S8, S15 | Organizational learning, double-loop | Partial | No (known) |
| 3 | Cyert & March, 1963 | 11 | S2, S3, S8, S15 | Behavioral theory of the firm | Partial | No (known) |
| 4 | March & Simon, 1958 | 7 | S3, S15 | Organizational decision-making | Partial | No (known) |
| 5 | Weick, 1995 | 9 | S2, S4, S15 | Sensemaking, interpretation | Partial | No (known) |
| 6 | Gibson, 1979 | 8 | S5, S6, S15 | Affordances (ecological) | Partial | No (known) |
| 7 | Norman, 1988 | 8 | S5, S6, S15 | Affordances (design) | Partial | No (known) |
| 8 | Ng et al., 1999 | 8 | S2, S6, S15 | Reward shaping | Partial | No (known) |
| 9 | Lewis et al., 2020 | 11 | S2, S7, S15 | RAG | Partial | No (known) |
| 10 | Menick et al., 2022 | 10 | S1, S2, S7, S15 | GopherCite, grounding | Partial | **Yes** (verify venue) |
| 11 | Dennett, 1987 | 2 | S4 | Intentional stance | No | No (known) |
| 12 | Russell & Norvig, 2020 | 3 | S4 | AI agents foundational | No | No (known) |
| 13 | Lynch et al., 2025 | 5 | S1, S15 | Agentic misalignment | No | **Yes** |
| 14 | OpenAI, 2025 | 5 | S1, S15 | Preparedness Framework | No | **Yes** (verify URL/format) |
| 15 | Google DeepMind, 2024 | 5 | S1, S15 | Frontier Safety Framework | No | **Yes** (verify URL/format) |
| 16 | Shanahan et al., 2023 | 4 | S1, S15 | Role-play, anti-anthropomorphism | No | **Yes** (verify venue) |
| 17 | Shanahan, 2022 | 2 | S15 | Anthropomorphism caution | No | **Yes** (verify venue) |
| 18 | Ji et al., 2023 | 3 | S2, S15 | AI alignment survey | No | **Yes** |
| 19 | Walsh & Ungson, 1991 | 3 | S3, S15 | Organizational memory | No | **Yes** |
| 20 | Alavi & Leidner, 2001 | 3 | S3, S15 | Knowledge management | No | **Yes** |
| 21 | Pirolli & Card, 1999 | 1 | S6 | Information foraging | No | **Yes** |
| 22 | Howard, 1966 | 1 | S6 | Value of information | No | **Yes** |
| 23 | Russell & Wefald, 1991 | 1 | S6 | Rational metareasoning | No | **Yes** |
| 24 | de Clippel & Rozen, 2024 | 2 | S15 | Bounded rationality survey | No | **Yes** |
| 25 | Yu et al., 2024 | 2 | S15 | RAG evaluation survey | No | **Yes** |
| 26 | Moreau et al., 2013 | 2 | S15 | Decision/workflow provenance | No | **Yes** |
| 27 | Lee, 1997 | 2 | S15 | Design rationale | No | **Yes** |
| 28 | Amershi et al., 2019 | 2 | S15 | Human-AI interaction guidelines | No | **Yes** |
| 29 | Horvitz, 1999 | 2 | S15 | Mixed-initiative systems | No | **Yes** |
| 30 | Johnson et al., 2014 | 2 | S15 | Coactive design | No | **Yes** |
| 31 | Aamodt & Plaza, 1994 | 6 | S15 | Case-based reasoning | No | **Yes** |
| 32 | Guo et al., 2017 | 2 | S15 | Uncertainty calibration | No | **Yes** |
| 33 | Kadavath et al., 2022 | 2 | S15 | LLM abstention/calibration | No | **Yes** |

**Note:** The grep also captured figure alt-text (e.g., `[From Agent Fear to Landscape Design]`, `[Context Is Not Reasoning State]`) — these are markdown image labels, not citations. They are correctly excluded from the citation count above.

---

## Part 3 — Ledger Sync Recommendation

### Entries already aligned (partial — old placeholder names, same sources)

The RELATED_WORK_LEDGER.md has entries for 11 categories that map to Batch 1 sources. However, the ledger still uses **old placeholder names** (e.g., `[SIMON1955]`, `[ARGYRIS_SCHON]`, `[DEEPMIND_GOPHERCITE]`) — 13 old-style placeholders remain in the ledger. These need renaming to match the real citations now in the paper.

| Ledger Category | Old Placeholder | New Citation | Action |
|----------------|----------------|-------------|--------|
| 1. Bounded Rationality | [SIMON1955] | [Simon, 1955] | Rename |
| 2. Org Decision-Making | [MARCH_SIMON_ORGS] | [March & Simon, 1958] | Rename |
| 3. Behavioral Theory | [CYERT_MARCH] | [Cyert & March, 1963] | Rename |
| 4. Org Learning | [ARGYRIS_SCHON] | [Argyris & Schön, 1978] | Rename |
| 5. Sensemaking | [WEICK_SENSEMAKING] | [Weick, 1995] | Rename |
| 6. Affordances | [GIBSON_AFFORDANCES] [NORMAN_AFFORDANCES] | [Gibson, 1979] [Norman, 1988] | Rename |
| 7. Reward Shaping | [NG_REWARD_SHAPING] | [Ng et al., 1999] | Rename |
| 8. AI Safety | [ANTHROPIC_...] [OPENAI_...] [DEEPMIND_...] | [Lynch et al., 2025] etc. | Rename |
| 9. Hallucination | [DEEPMIND_GOPHERCITE] [RAG_FOUNDATIONAL] | [Menick et al., 2022] [Lewis et al., 2020] | Rename |
| 10. Knowledge Mgmt | (placeholder only) | [Walsh & Ungson, 1991] [Alavi & Leidner, 2001] | **Add** |
| 11. HCI | (placeholder only) | [Amershi et al., 2019] [Horvitz, 1999] [Johnson et al., 2014] | **Add** |

### Entries missing from the ledger

These citations now appear in body prose but have no ledger entry:

| Citation | Category | Action |
|----------|----------|--------|
| Dennett, 1987 | Philosophy of mind / anti-anthropomorphism | Add entry |
| Russell & Norvig, 2020 | AI agents foundational | Add entry |
| Ji et al., 2023 | AI alignment survey | Add entry |
| Walsh & Ungson, 1991 | Organizational memory | Add to Category 10 |
| Alavi & Leidner, 2001 | Knowledge management | Add to Category 10 |
| Pirolli & Card, 1999 | Information foraging | Add new category or subcategory |
| Howard, 1966 | Value of information | Add new category or subcategory |
| Russell & Wefald, 1991 | Rational metareasoning | Add new category or subcategory |
| de Clippel & Rozen, 2024 | Bounded rationality survey | Add to Category 1 |
| Yu et al., 2024 | RAG evaluation | Add to Category 9 |
| Shanahan, 2022 | Anthropomorphism | Add to Category 10 (anti-anthropomorphism) |
| Moreau et al., 2013 | Provenance | Add new category or Category 12 |
| Lee, 1997 | Design rationale | Add new category or Category 12 |
| Amershi et al., 2019 | HCI guidelines | Add to Category 11 |
| Horvitz, 1999 | Mixed-initiative | Add to Category 11 |
| Johnson et al., 2014 | Coactive design | Add to Category 11 |
| Aamodt & Plaza, 1994 | Case-based reasoning | Add new category (14) |
| Guo et al., 2017 | Calibration | Add new category (15) |
| Kadavath et al., 2022 | LLM abstention | Add new category (15) |

### Entries in ledger no longer cited in body prose

The ledger's "Citation Placeholders for Drafting" section lists 14 old-style placeholder names. All 14 have been resolved and should be **retired or renamed** in the ledger.

### Sources needing full bibliographic metadata

**20 of 33 citations** need full bibliography entries (title, venue, volume, pages, DOI/URL). The 13 foundational sources (Simon, Argyris, Cyert, March, Weick, Gibson, Norman, Ng, Lewis, Dennett, Russell & Norvig) have well-known metadata in the ledger. The remaining 20 need verification.

---

## Part 4 — Summary

| Metric | Count |
|--------|-------|
| Body prose citation-clean? | **Yes — zero unresolved** |
| Real author-year citations in body prose | **33** |
| Ledger entries needing rename | **11** |
| Ledger entries needing addition | **19** |
| Citations needing bibliography metadata | **20** |
| Checklist placeholders remaining (untouched) | **152** |

### Recommended Next Action

1. **Update RELATED_WORK_LEDGER.md** — rename 11 placeholder entries, add 19 new citation entries, retire old placeholder list.
2. **Create BIBLIOGRAPHY.md** — compile full metadata for all 33 citations.
3. **Optionally clean citation-debt checklists** — decide whether to resolve, simplify, or remove the 152 checklist placeholders (they are not visible to readers unless the draft notes are kept).
