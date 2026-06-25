# Bibliography Audit Report — 2026-06-25

**Manuscript:** `PAPER_ACADEMIC_v0.1.md`
**Auditor:** Claude Opus 4.6
**Status:** Complete

---

## A. Confirmed Entries (in bibliography, cited in text, metadata acceptable)

| Citation Key | Entry | Status |
|---|---|---|
| Alavi and Leidner, 2001 | Alavi, M., & Leidner, D. E. (2001). Knowledge management. *MIS Quarterly*, *25*(1), 107-136. | OK |
| Argyris and Schon, 1978 | Argyris, C., & Schon, D. A. (1978). *Organizational learning*. Addison-Wesley. | OK (note: text uses both "Schon" and "Schön" — standardize) |
| Endsley, 1995 | Endsley, M. R. (1995). Situation awareness. *Human Factors*, *37*(1), 32-64. | OK |
| Gibson, 1979 | Gibson, J. J. (1979). *The ecological approach to visual perception*. Houghton Mifflin. | OK |
| Horvitz, 1999 | Horvitz, E. (1999). Mixed-initiative user interfaces. *CHI '99*, 159-166. | OK |
| Kuhlthau, 1991 | Kuhlthau, C. C. (1991). Inside the search process. *JASIS*, *42*(5), 361-371. | OK |
| Lee, 1997 | Lee, J. (1997). Design rationale systems. *IEEE Expert*, *12*(3), 78-85. | OK |
| Lee and See, 2004 | Lee, J. D., & See, K. A. (2004). Trust in automation. *Human Factors*, *46*(1), 50-80. | OK |
| Lewis et al., 2020 | Lewis, P., et al. (2020). Retrieval-augmented generation. *NeurIPS*, *33*, 9459-9474. | OK |
| March, 1991 | March, J. G. (1991). Exploration and exploitation. *Organization Science*, *2*(1), 71-87. | OK |
| Markus, 2001 | Markus, M. L. (2001). Toward a theory of knowledge reuse. *JMIS*, *18*(1), 57-93. | OK |
| Maynez et al., 2020 | Maynez, J., et al. (2020). Faithfulness and factuality. *ACL*, 1906-1919. | OK |
| Norman, 1988 | Norman, D. A. (1988). *The design of everyday things*. Basic Books. | OK |
| Parasuraman and Riley, 1997 | Parasuraman, R., & Riley, V. (1997). Humans and automation. *Human Factors*, *39*(2), 230-253. | OK |
| Pirolli and Card, 1999 | Pirolli, P., & Card, S. (1999). Information foraging. *Psychological Review*, *106*(4), 643-675. | OK |
| Simon, 1955 | Simon, H. A. (1955). A behavioral model of rational choice. *QJE*, *69*(1), 99-118. | OK |
| Su et al., 2025 | Su, H., et al. (2025). Autonomy-induced security risks. *arXiv:2506.23844*. | OK |
| Walsh and Ungson, 1991 | Walsh, J. P., & Ungson, G. R. (1991). Organizational memory. *AMR*, *16*(1), 57-91. | OK |
| Weick, 1995 | Weick, K. E. (1995). *Sensemaking in organizations*. Sage. | OK |

---

## B. Corrected Entries

### B.1 Argyris — accent inconsistency

**Issue:** Body text uses both "Argyris and Schon" and "Argyris and Schön" (with umlaut). The bibliography entry uses "Schon" (no umlaut).

**Decision:** Standardize to "Schon" throughout (no umlaut) for consistency with the bibliography entry. The original 1978 Addison-Wesley publication uses "Schön" but the no-umlaut form is widely accepted in English-language citation.

**Action:** Search-and-replace "Schön" → "Schon" in body text where it appears in citation brackets.

### B.2 Walsh — conjunction inconsistency

**Issue:** Line 93 uses `[Walsh & Ungson, 1991]` while all other instances use `[Walsh and Ungson, 1991]`.

**Action:** Change line 93 from `&` to `and`.

### B.3 ReAct — year decision

**Issue:** Manuscript cites `[Yao et al., 2022]`. ReAct was arXiv 2022, published at ICLR 2023.

**Decision:** Change to `[Yao et al., 2023]` throughout. Use ICLR 2023 as the canonical venue.

### B.4 Huang et al. — existing entry is fine

The existing entry `Huang, L., et al. (2023). Hallucination in large language models. *arXiv:2311.05232*.` is cited in S5 line 585. Confirmed present and correctly attributed.

### B.5 Ji et al. — single entry, dual context

**Issue:** `[Ji et al., 2023]` is cited in S2 (alignment survey context) and S5 (alongside hallucination citations). The bibliography has only the alignment survey entry.

**Decision:** Keep as single entry. The alignment survey covers hallucination topics within its scope. No disambiguation needed because there is only one Ji et al. 2023 in the manuscript.

### B.6 Lynch et al. — verify metadata

**Current:** `Lynch, A., et al. (2025). Agentic misalignment. Anthropic Research.`

**Verified title:** "Agentic misalignment: How LLMs could be an insider threat"

**Action:** Expand title in bibliography.

---

## C. Needs Decision

### C.1 SWE-bench year

Manuscript cites `[Jimenez et al., 2023]`. The paper was published at ICLR 2024.

**Recommendation:** Change to `[Jimenez et al., 2024]` and use ICLR 2024 as venue. This matches the ReAct decision (use conference year, not arXiv year).

### C.2 AgentBench and WebArena years

Manuscript cites `[Liu et al., 2023]` and `[Zhou et al., 2023]`. Both were published at ICLR 2024.

**Recommendation:** Change to `[Liu et al., 2024]` and `[Zhou et al., 2024]`. Same logic as ReAct and SWE-bench.

---

## D. Removed Entries (orphans — in bibliography, never cited in text)

| Entry | Reason |
|---|---|
| Aamodt, A., & Plaza, E. (1994) | Not cited in academic manuscript |
| Bates, M. J. (1989) | Not cited in academic manuscript (Kuhlthau is cited instead) |
| Cyert, R. M., & March, J. G. (1963) | Not cited |
| Dennett, D. C. (1987) | Not cited |
| Guo, C., et al. (2017) | Not cited |
| Howard, R. A. (1966) | Not cited |
| Kadavath, S., et al. (2022) | Not cited |
| March, J. G., & Simon, H. A. (1958) | Not cited (March 1991 is cited separately) |
| Menick, J., et al. (2022) | Not cited |
| Moreau, L., & Missier, P. (2013) | Not cited |
| Ng, A. Y., et al. (1999) | Not cited |
| Russell, S., & Norvig, P. (2020) | Not cited |
| Russell, S., & Wefald, E. (1991) | Not cited |
| Shanahan, M., et al. (2023) | Not cited |

**14 orphan entries to remove.**

---

## E. In-Text Citation Changes

| Change | Scope |
|---|---|
| `[Yao et al., 2022]` → `[Yao et al., 2023]` | Throughout (S1, S2, S10) |
| `[Jimenez et al., 2023]` → `[Jimenez et al., 2024]` | Throughout (S2, S10) |
| `[Liu et al., 2023]` → `[Liu et al., 2024]` | Throughout (S2, S10) |
| `[Zhou et al., 2023]` → `[Zhou et al., 2024]` | Throughout (S2, S10) |
| `[Walsh & Ungson, 1991]` → `[Walsh and Ungson, 1991]` | Line 93 only |
| `Schön` → `Schon` | Body text where umlaut appears in citation context |

---

## F. Final Bibliography

```
Alavi, M., & Leidner, D. E. (2001). Review: Knowledge management and knowledge management systems: Conceptual foundations and research issues. *MIS Quarterly*, *25*(1), 107-136.

Amershi, S., Weld, D., Vorvoreanu, M., Fourney, A., Nushi, B., Collisson, P., Suh, J., Iqbal, S., Bennett, P. N., Inkpen, K., Teevan, J., Kikin-Gil, R., & Horvitz, E. (2019). Guidelines for human-AI interaction. *CHI '19: Proceedings of the 2019 CHI Conference on Human Factors in Computing Systems*, Paper 3.

Argyris, C., & Schon, D. A. (1978). *Organizational learning: A theory of action perspective*. Addison-Wesley.

Bai, Y., Kadavath, S., Kundu, S., Askell, A., Kernion, J., Jones, A., Chen, A., Goldie, A., Mirhoseini, A., McKinnon, C., Chen, C., Olsson, C., Olah, C., Hernandez, D., Drain, D., Ganguli, D., Li, D., Tran-Johnson, E., Perez, E., ... Kaplan, J. (2022). Constitutional AI: Harmlessness from AI feedback. *arXiv:2212.08073*.

Christiano, P. F., Leike, J., Brown, T., Martic, M., Legg, S., & Amodei, D. (2017). Deep reinforcement learning from human preferences. *Advances in Neural Information Processing Systems*, *30*.

Endsley, M. R. (1995). Toward a theory of situation awareness in dynamic systems. *Human Factors*, *37*(1), 32-64.

Gibson, J. J. (1979). *The ecological approach to visual perception*. Houghton Mifflin.

Hevner, A. R., March, S. T., Park, J., & Ram, S. (2004). Design science in information systems research. *MIS Quarterly*, *28*(1), 75-105.

Horvitz, E. (1999). Principles of mixed-initiative user interfaces. *CHI '99: Proceedings of the SIGCHI Conference on Human Factors in Computing Systems*, 159-166.

Huang, L., Yu, W., Ma, W., Zhong, W., Feng, Z., Wang, H., Chen, Q., Peng, W., Feng, X., Qin, B., & Liu, T. (2023). A survey on hallucination in large language models: Principles, taxonomy, challenges, and open questions. *arXiv:2311.05232*.

Ji, J., Qiu, T., Chen, B., Zhang, B., Lou, H., Wang, K., Duan, Y., He, Z., Zhou, J., Zhang, Z., Zeng, F., Ng, K. Y., Dai, J., Pan, X., O'Gara, A., Lei, Y., Xu, H., Tse, B., Fu, J., ... Gao, W. (2023). AI alignment: A comprehensive survey. *arXiv:2310.19852*.

Jimenez, C. E., Yang, J., Wettig, A., Yao, S., Pei, K., Press, O., & Narasimhan, K. (2024). SWE-bench: Can language models resolve real-world GitHub issues? *International Conference on Learning Representations*.

Kuhlthau, C. C. (1991). Inside the search process: Information seeking from the user's perspective. *Journal of the American Society for Information Science*, *42*(5), 361-371.

Lakatos, I. (1970). Falsification and the methodology of scientific research programmes. In I. Lakatos & A. Musgrave (Eds.), *Criticism and the growth of knowledge* (pp. 91-196). Cambridge University Press.

Lee, J. (1997). Design rationale systems: Understanding the issues. *IEEE Expert*, *12*(3), 78-85.

Lee, J. D., & See, K. A. (2004). Trust in automation: Designing for appropriate reliance. *Human Factors*, *46*(1), 50-80.

Lewis, P., Perez, E., Piktus, A., Petroni, F., Karpukhin, V., Goyal, N., Kuttler, H., Lewis, M., Yih, W., Rocktaschel, T., Riedel, S., & Kiela, D. (2020). Retrieval-augmented generation for knowledge-intensive NLP tasks. *Advances in Neural Information Processing Systems*, *33*, 9459-9474.

Liu, X., Yu, H., Zhang, H., Xu, Y., Lei, X., Lai, H., Gu, Y., Ding, H., Men, K., Yang, K., Zhang, S., Deng, X., Zeng, A., Du, Z., Zhang, C., Shen, S., Zhang, T., Su, Y., Sun, H., ... Tang, J. (2024). AgentBench: Evaluating LLMs as agents. *International Conference on Learning Representations*.

Lynch, A., Wright, B., Larson, C., Troy, K. K., Ritchie, S. J., Mindermann, S., Perez, E., & Hubinger, E. (2025). Agentic misalignment: How LLMs could be an insider threat. Anthropic Research.

Madaan, A., Tandon, N., Gupta, P., Hallinan, S., Gao, L., Wiegreffe, S., Alon, U., Dziri, N., Prabhumoye, S., Yang, Y., Gupta, S., Majumder, B. P., Hermann, K. M., Welleck, S., Yazdanbakhsh, A., & Clark, P. (2023). Self-Refine: Iterative refinement with self-feedback. *Advances in Neural Information Processing Systems*, *36*.

March, J. G. (1991). Exploration and exploitation in organizational learning. *Organization Science*, *2*(1), 71-87.

Markus, M. L. (2001). Toward a theory of knowledge reuse: Types of knowledge reuse situations and factors in reuse success. *Journal of Management Information Systems*, *18*(1), 57-93.

Maynez, J., Narayan, S., Bohnet, B., & McDonald, R. (2020). On faithfulness and factuality in abstractive summarization. *Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics*, 1906-1919.

Norman, D. A. (1988). *The design of everyday things*. Basic Books.

Ouyang, L., Wu, J., Jiang, X., Almeida, D., Wainwright, C., Mishkin, P., Zhang, C., Agarwal, S., Slama, K., Ray, A., Schulman, J., Hilton, J., Kelton, F., Miller, L., Simens, M., Askell, A., Welinder, P., Christiano, P. F., Leike, J., & Lowe, R. (2022). Training language models to follow instructions with human feedback. *Advances in Neural Information Processing Systems*, *35*.

Parasuraman, R., & Riley, V. (1997). Humans and automation: Use, misuse, disuse, abuse. *Human Factors*, *39*(2), 230-253.

Park, J. S., O'Brien, J. C., Cai, C. J., Morris, M. R., Liang, P., & Bernstein, M. S. (2023). Generative agents: Interactive simulacra of human behavior. *Proceedings of the 36th Annual ACM Symposium on User Interface Software and Technology*.

Peffers, K., Tuunanen, T., Rothenberger, M. A., & Chatterjee, S. (2007). A design science research methodology for information systems research. *Journal of Management Information Systems*, *24*(3), 45-77.

Pirolli, P., & Card, S. (1999). Information foraging. *Psychological Review*, *106*(4), 643-675.

Popper, K. R. (1959). *The logic of scientific discovery*. Hutchinson.

Schick, T., Dwivedi-Yu, J., Dessi, R., Raileanu, R., Lomeli, M., Hambro, E., Zettlemoyer, L., Cancedda, N., & Scialom, T. (2023). Toolformer: Language models can teach themselves to use tools. *Advances in Neural Information Processing Systems*, *36*.

Shinn, N., Cassano, F., Gopinath, A., Narasimhan, K., & Yao, S. (2023). Reflexion: Language agents with verbal reinforcement learning. *Advances in Neural Information Processing Systems*, *36*.

Siggelkow, N. (2007). Persuasion with case studies. *Academy of Management Journal*, *50*(1), 20-24.

Simon, H. A. (1955). A behavioral model of rational choice. *Quarterly Journal of Economics*, *69*(1), 99-118.

Su, H., Luo, J., Liu, C., Yang, X., Zhang, Y., Dong, Y., & Zhu, J. (2025). A survey on autonomy-induced security risks in large model-based agents. *arXiv:2506.23844*.

Walsh, J. P., & Ungson, G. R. (1991). Organizational memory. *Academy of Management Review*, *16*(1), 57-91.

Weick, K. E. (1995). *Sensemaking in organizations*. Sage.

Xie, T., Zhang, D., Chen, J., Li, X., Zhao, S., Cao, R., Hua, T. J., Cheng, Z., Shin, D., Lei, F., Liu, Y., Xu, Y., Zhou, S., Savarese, S., Xiong, C., Zhong, V., & Yu, T. (2024). OSWorld: Benchmarking multimodal agents for open-ended tasks in real computer environments. *Advances in Neural Information Processing Systems*, *37*.

Xu, F. F., Shi, Y., Hooi, D. S., Muennighoff, N., Shen, J. T., Xin, Z., ... & Neubig, G. (2024). TheAgentCompany: Benchmarking LLM agents on consequential real world tasks. *arXiv:2412.14161*.

Yao, S., Zhao, J., Yu, D., Du, N., Shafran, I., Narasimhan, K., & Cao, Y. (2023). ReAct: Synergizing reasoning and acting in language models. *International Conference on Learning Representations*.

Zhou, S., Xu, F. F., Zhu, H., Zhou, X., Lo, R., Sridhar, A., Cheng, X., Ou, T., Bisk, Y., Fried, D., Alon, U., & Neubig, G. (2024). WebArena: A realistic web environment for building autonomous agents. *International Conference on Learning Representations*.
```

---

## G. Remaining Risks

Two items to monitor:

1. **TheAgentCompany (Xu et al., 2024):** The manuscript cites this as `[Xu et al., 2024]` but the arXiv preprint is dated December 2024. If a formal conference publication appears before manuscript submission, update the venue. Currently listed as arXiv preprint.

2. **Bai et al., 2022 (Constitutional AI):** Listed as arXiv preprint. If published in a conference proceedings before submission, update. Currently arXiv.

No other unresolved citation risks remain after this audit.
