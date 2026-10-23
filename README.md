# Need or Reputation? Region, National Income, and Academic Status in LLM Gatekeeping Decisions
# Generous with Papers, Guarded with Data: Auditing the Jev Decision Model in Academic Gatekeeping

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)

This repository contains the experiment dataset for the paper:

> **Need or Reputation? Region, National Income, and Academic Status in LLM Gatekeeping Decisions
> Generous with Papers, Guarded with Data: Auditing the Jev Decision Model in Academic Gatekeeping**

---

## 📌 Overview

As Large Language Models (LLMs) and Decision Models (DMs) are increasingly integrated into administrative and evaluative workflows, understanding their decision-making biases in academic gatekeeping scenarios (CVs sharing, Paywalled Articles, nonpublic Data) is critical. This study investigates whether popular open-weight LLMs, proprietary LLMs, or DMs exhibit systemic biases based on **geographic region** (Global North vs. Global South) and **academic status** (e.g., Tenured Professor, Postdoc Researcher, PhD candidate, Undergraduate Students) when making resource access and gatekeeping choices.

### Evaluated Models
- **Meta:**  Llama 3.1-8B
- **Google:** Gemini 2.5 Pro, Gemma-3n-E2B
- **Anthropic:** Claude Sonnet 4.6.
- **OpenAI:** GPT-4o 
- **TypeSafe:** Jev 1.13 decision model

---

## 📂 Repository Structure

```text
.
├── study1_origin_data.zip       # Study 1: Global North vs. Global South selections by each LLM
├── Academic_status_files.zip    # Study 2: academic status selections by each LLM
├── classify_country_files.zip   # Each LLM's Global North / Global South country classification
├── gdp_per_capita_2023.csv      # 2023 GDP per capita (World Bank) used in the income analysis
├── jev_gatekeeping_files.zip    # Jev decision model: decisions, probabilities, and country classifications
└── README.md
```

## 📊 Datasets

1. **Country Classification**
   - Contains zipped data mapping how each LLM categorizes countries into Global South and Global North classifications.

2. **Access Scenarios Selections**
   - Records of LLM selection choices across various academic gatekeeping scenarios (e.g., CVs sharing, Paywalled Articles, nonpublic Data).

3. **Academic Status Selections**
    - Records of LLM selection choices across various academic seniorities (e.g.,  Tenured Professor, Postdoc Researcher, PhD candidate, Undergraduate Students).
  
4. **Global Region Selections**
    - Records of LLM selection choices across various countries belonging to Global South or Global North.

5. **Jev Decision Model** (`jev_gatekeeping_files.zip`)
    - Data for the paper *Generous with Papers, Guarded with Data: Auditing the Jev Decision Model in Academic Gatekeeping*, which repeats both studies with TypeSafe's Jev decision model (`typesafe/jev-1.13`, queried through OpenRouter's Decisions API in October 2026) using the same prompts, countries, academic statuses, and option orders.
    - `study1_run1.csv`: Study 1, all 61,440 decisions (32 Global North × 80 Global South countries × 3 resources × 4 academic statuses × 2 option orders), with Jev's choice and its probability for each requester.
    - `study1_run2.csv`, `study1_run3.csv`: two repetitions of 300 randomly drawn country pairs (7,200 decisions each), used to assess stability.
    - `study2.csv`: Study 2, all 1,680 decisions (112 countries × 3 resources × 5 option orderings), with Jev's probability for each academic status.
    - `classify.csv`: Jev's Global North / Global South classification of the 112 countries.
    - `reasons_study1.csv`, `reasons_study2.csv`: the reasons experiment, in which Jev also chose the main reason for each decision from nine fixed options (Study 1: 100 country pairs spanning the income gap × 3 resources × 4 statuses, 1,200 decisions; Study 2: 40 countries spanning GDP per capita × 3 resources, 120 decisions), with its probability for each reason.

---

## 🚀 Getting Started

### Prerequisites

Clone the repository:

```bash
git clone https://github.com/Nouar-NYUAD/AI-Generated-Academic-Gatekeeping-Scenarios.git
cd AI-Generated-Academic-Gatekeeping-Scenarios
```


---

## 📜 Citation

If you use this repository or dataset in your research, please cite our paper:

```bibtex
@article{aldahoul2026need,
  title={Need or Reputation? {Region}, National Income, and Academic Status in {LLM} Gatekeeping Decisions},
  author={AlDahoul, Nouar and Karim, Hezerul Abdul and Tan, Myles Joshua Toledo},
  journal={arXiv preprint arXiv:2608.05178},
  year={2026}
}
```

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
