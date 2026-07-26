# Who Gets Access? Global Region and Academic Status Bias in AI-Generated Academic Gatekeeping Scenarios

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)

This repository contains the experiment dataset for the paper:

> **Who Gets Access? Global Region and Academic Status Bias in AI-Generated Academic Gatekeeping Scenarios**

---

## 📌 Overview

As Large Language Models (LLMs) are increasingly integrated into administrative and evaluative workflows, understanding their decision-making biases in academic gatekeeping scenarios is critical. This study investigates whether popular open-weight and proprietary LLMs exhibit systemic biases based on **geographic region** (Global North vs. Global South) and **academic status** (e.g., Tenured Professor, Postdoc Researcher, PhD candidate, Undergraduate Students) when making resource access and gatekeeping choices.

### Evaluated Models
- **Meta:**  Llama 3.1-8B
- **Google:** Gemini 2.5 Pro, Gemma-3n-2B
- **Anthropic:** Claude Sonnet 3.
- **OpenAI:** GPT-4o 

---

## 📂 Repository Structure

```text
.
├── llama8b.zip     # LlaMa selection for each access scenario, academic status levels, and countries.
│── gemma3.zip      # Gemma-3 selection for each access scenario, academic status levels, and countries.
│── claude.zip      # Claude selection for each access scenario, academic status levels, and countries.    
│── gemini.zip      # Gemini selection for each access scenario, academic status levels, and countries.
│── gpt.zip         # GPT selection for each access scenario, academic status levels, and countries.
├── classify_country.zip      # Country classifications by LLMs into Global North vs. Global South by LLMs
└── README.md
```

---

## 📊 Datasets

1. **Country Classification (`data/country_classification/`)**
   - Contains zipped data mapping how each LLM categorizes countries into Global South and Global North classifications.

2. **Access Scenarios Selections (`data/llm_selections/access_scenarios.zip`)**
   - Records of LLM selection choices across various academic gatekeeping scenarios (e.g., funding grants, compute allocation, conference sponsorship, journal reviews).

3. **Academic Status Selections (`data/llm_selections/academic_status.zip`)**
   - Data detailing model selection outcomes conditioned on academic rank and institutional status (e.g., Senior Faculty vs. Early Career vs. Independent Researcher).

---

## 🚀 Getting Started

### Prerequisites

Clone the repository and install required Python packages:

```bash
git clone https://github.com/Nouar-NYUAD/AI-Generated-Academic-Gatekeeping-Scenarios.git
cd AI-Generated-Academic-Gatekeeping-Scenarios
```


---

## 📜 Citation

If you use this repository or dataset in your research, please cite our paper:

```bibtex
@article{gatekeeping_llm_bias_2026,
  title={Who Gets Access? Global Region and Academic Status Bias in AI-Generated Academic Gatekeeping Scenarios},
  author={Your Name and Co-authors},
  journal={arXiv preprint},
  year={2026}
}
```

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
