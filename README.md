# ADAB / أدب — Arabic Dataset for Automated Politeness Benchmarking

> **A Large-Scale Resource for Computational Sociopragmatics**
> 
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Dataset Size](https://img.shields.io/badge/Dataset-10%2C000%20texts-blue)]()
[![Languages](https://img.shields.io/badge/Language-Arabic%20(MSA%20%2B%204%20dialects)-green)]()
[![Paper](https://img.shields.io/badge/Paper-LREC%202026-red)](https://arxiv.org/abs/2602.13870)

---

## Overview

**ADAB** (*Arabic Politeness Dataset*) is the first large-scale Arabic dataset for automated politeness detection. It contains **10,000 annotated Arabic texts** collected from four diverse online platforms, covering both Modern Standard Arabic (MSA) and four major dialectal varieties: Gulf, Egyptian, Levantine, and Maghrebi.

The dataset supports a **three-way politeness classification** task (Polite / Neutral / Impolite) with fine-grained annotations across **16 linguistic politeness and impoliteness categories**.

---

## Authors

| Name | Affiliation |
|------|-------------|
| Hend Al-Khalifa | King Saud University, Riyadh, Saudi Arabia |
| Nadia Ghezaiel | University of Hail, Hail, Saudi Arabia |
| Maria Bounnit | Cadi Ayyad University, Marrakesh, Morocco |
| Hend Hamed Alhazmi | Saudi Center of Philosophy and Ethics, Jeddah, Saudi Arabia |
| Noof Abdullah Alfear | King Saud University, Riyadh, Saudi Arabia |
| Reem Fahad Alqifari | King Saud University, Riyadh, Saudi Arabia |
| Ameera Masoud Almasoud | King Saud University, Riyadh, Saudi Arabia |
| Sharefah Al-Ghamdi | King Saud University, Riyadh, Saudi Arabia |

---

## Dataset

### Statistics

| Property | Value |
|----------|-------|
| Total texts | 10,000 |
| Source domains | 4 (2,500 per domain) |
| Politeness classes | 3 (Polite, Neutral, Impolite) |
| Annotation categories | 16 |
| Average text length | 13.90 words |
| Inter-annotator agreement | κ = 0.703 (substantial) |
| Class distribution | Polite 19.12% · Neutral 70.72% · Impolite 10.16% |

### Data Sources

| Source | Size Available | Domain |
|--------|---------------|--------|
| YouTube Comments | ~70K | Informal reactions, multi-dialect |
| Product Reviews (Shein) | ~6K | E-commerce, customer feedback |
| Twitter/X (ArSAS) | ~20K | Social, cultural, political discourse |
| Banking App Reviews | ~67K | Customer-to-business communication |

### Politeness Categories

**Politeness (7):** Appreciation & Admiration, Permission & Courtliness, Congratulations, Greetings, Hospitality & Generosity, Gratitude & Thanks, Respect

**Impoliteness (8):** Accusation, Harsh Criticism, Discrimination & Racism, Disparagement, Insult, Demeaning Sarcasm, Threat, Verbal Violence

**Both:** Prayers — *Du'ā' Lak* (blessing) vs. *Du'ā' 'Alayk* (curse), same linguistic form with dual intent

---

## Benchmarks

We evaluated **40 model configurations** across three paradigms:

### Top-5 Models

| Model | Accuracy | Macro-F1 | F1 Impolite | F1 Neutral | F1 Polite |
|-------|----------|----------|-------------|------------|-----------|
| **MARBERT** | **0.9119** | **0.8582** | **0.81** | 0.94 | 0.82 |
| AraBERTv02 | 0.8984 | 0.8296 | 0.74 | 0.93 | 0.82 |
| mDeBERTa v3 | 0.8959 | 0.8252 | 0.72 | 0.93 | 0.82 |
| CAMeLBERT-mix | 0.8929 | 0.8193 | 0.73 | 0.93 | 0.80 |
| XLM-RoBERTa large | 0.8889 | 0.8150 | 0.71 | 0.93 | 0.81 |

### Models Evaluated

**Traditional ML (12):** Logistic Regression, SVM, XGBoost × {TF-IDF, FastText, GloVe, Word2Vec}

**Transformers (10):** AraBERTv02, MARBERT, CAMeLBERT-mix, mBERT (cased/uncased), XLM-RoBERTa (base/large), mDeBERTa v3, InfoXLM, RemBERT

**LLMs (18 configs):** GPT-4 mini, Claude Sonnet 4.5, DeepSeek V3, GPT OSS 20B, Fanar-1-9B, ALLaM-7B-Instruct × {0-shot, 1-shot, 3-shot}

---

## Citation

If you use ADAB in your research, please cite:

```bibtex
@inproceedings{alkhalifa2026adab,
  title     = {{ADAB}: Arabic Dataset for Automated Politeness Benchmarking --
               A Large-Scale Resource for Computational Sociopragmatics},
  author    = {Al-Khalifa, Hend and Ghezaiel, Nadia and Bounnit, Maria and
               Alhazmi, Hend Hamed and Alfear, Noof Abdullah and
               Alqifari, Reem Fahad and Almasoud, Ameera Masoud and
               Al-Ghamdi, Sharefah},
  booktitle = {Proceedings of the The Fifteenth biennial Language 
               Resources and Evaluation (LREC 2026)},
  year      = {2026}
}
```

---

## License

The ADAB dataset is released under the [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). It is intended for **research and educational purposes only**.

