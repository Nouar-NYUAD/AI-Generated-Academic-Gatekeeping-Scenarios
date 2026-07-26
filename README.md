# Who Gets Access? Global Region and Academic Status Bias in AI-Generated Academic Gatekeeping Scenarios

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)

This repository contains the dataset, experiment code, and evaluation logs for the paper:

> **Who Gets Access? Global Region and Academic Status Bias in AI-Generated Academic Gatekeeping Scenarios**

---

## 📌 Overview

As Large Language Models (LLMs) are increasingly integrated into administrative and evaluative workflows, understanding their decision-making biases in academic gatekeeping scenarios is critical. This study investigates whether popular open-weight and proprietary LLMs exhibit systemic biases based on **geographic region** (Global North vs. Global South) and **academic status** (e.g., Professor, Postdoc, PhD candidate, Independent Scholar) when making resource access and gatekeeping choices.

### Evaluated Models
- **Meta:** LLaMA 3 / 3.1 (8B)
- **Google:** Gemini, Gemma 3
- **Anthropic:** Claude Series
- **OpenAI:** GPT Models (e.g., GPT-4o, GPT-3.5)

---

## 📂 Repository Structure

```text
.
├── data/
│   ├── country_classification/
│   │   └── global_north_south.zip   # Country classifications into Global North vs. Global South by LLMs
│   │
│   ├── llm_selections/
│   │   ├── access_scenarios.zip     # LLM selection of countries for each access scenario
│   │   └── academic_status.zip      # LLM selections across different academic status levels
│   │
│   └── prompts/                     # Prompt templates used for gatekeeping decision experiments
│
├── notebooks/                       # Exploratory data analysis & plot generation
├── src/                             # Processing, execution, and evaluation scripts
├── README.md
└── requirements.txt
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
git clone https://github.com/your-username/academic-gatekeeping-llm-bias.git
cd academic-gatekeeping-llm-bias
pip install -r requirements.txt
```

### Unpacking Datasets

You can unpack all dataset archives automatically using Python:

```python
import zipfile
import glob
import os

zip_files = glob.glob("data/**/*.zip", recursive=True)
for zip_path in zip_files:
    extract_dir = os.path.splitext(zip_path)[0]
    with zipfile.ZipFile(zip_path, 'r') as zip_ref:
        zip_ref.extractall(extract_dir)
    print(f"Extracted: {zip_path} -> {extract_dir}")
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
