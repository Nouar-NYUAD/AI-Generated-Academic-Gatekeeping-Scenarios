# Global North–South and Status Biases in AI-Generated Academic Gatekeeping Scenarios

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)

This repository contains the experiment dataset for the paper:

> **Global North–South and Status Biases in AI-Generated Academic Gatekeeping Scenarios**

---

## 📌 Overview

As Large Language Models (LLMs) are increasingly integrated into administrative and evaluative workflows, understanding their decision-making biases in academic gatekeeping scenarios (CVs sharing, Paywalled Articles, nonpublic Data) is critical. This study investigates whether popular open-weight and proprietary LLMs exhibit systemic biases based on **geographic region** (Global North vs. Global South) and **academic status** (e.g., Tenured Professor, Postdoc Researcher, PhD candidate, Undergraduate Students) when making resource access and gatekeeping choices.

### Evaluated Models
- **Meta:**  Llama 3.1-8B
- **Google:** Gemini 2.5 Pro, Gemma-3n-2B
- **Anthropic:** Claude Sonnet 4.6.
- **OpenAI:** GPT-4o 

---

## 📂 Repository Structure

```text
.
├── llama8b.zip               # LlaMa selection of countries belonging to Global South or Global North for each access scenario and academic status.
│── gemma3.zip                # Gemma-3 selection of countries belonging to Global South or Global North for each access scenario and academic status.
│── claude.zip                # Claude selection of countries belonging to Global South or Global North for each access scenario and academic status.    
│── gemini.zip                # Gemini selection of countries belonging to Global South or Global North for each access scenario and academic status.
│── gpt.zip                   # GPT selection of countries belonging to Global South or Global North for each access scenario and academic status.
│── academic_status_files.zip       # LLMs selection of academic status for each access scenario and country.
├── classify_country_files.zip      # Country classifications by LLMs into Global North vs. Global South by LLMs
└── README.md
```

---

## 📊 Datasets

1. **Country Classification**
   - Contains zipped data mapping how each LLM categorizes countries into Global South and Global North classifications.

2. **Access Scenarios Selections**
   - Records of LLM selection choices across various academic gatekeeping scenarios (e.g., CVs sharing, Paywalled Articles, nonpublic Data).

3. **Academic Status Selections**
    - Records of LLM selection choices across various academic seniorities (e.g.,  Tenured Professor, Postdoc Researcher, PhD candidate, Undergraduate Students).
  
3. **Global Region Selections**
    - Records of LLM selection choices across various countries belonging to Global South or Global North.

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
@article{aldahoul2026gets,
  title={Who Gets Access? Global Region and Academic Status Bias in AI-Generated Academic Gatekeeping Scenarios},
  author={AlDahoul, Nouar and Karim, Hezerul Abdul and Tan, Myles Joshua Toledo},
  journal={arXiv preprint arXiv:2608.05178},
  year={2026}
}
```

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
