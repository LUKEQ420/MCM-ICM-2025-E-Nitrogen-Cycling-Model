

# From Forest to Farm: Modeling Nitrogen Dynamics for Sustainable Agriculture

<div align="center">
<p>
    <img src="https://img.shields.io/badge/MCM/ICM-2025-blue" alt="Contest Badge">
    <img src="https://img.shields.io/badge/Award-Finalist-brightgreen" alt="Award Badge">
    <img src="https://img.shields.io/badge/License-MIT-yellow" alt="License Badge">
</p>
</div>
<div align="left">

点击切换为中文版☞ **[简体中文](./README_zh.md)**

</div>

> 🏆 **Finalist Award (Top 1.8% of 27,456 teams worldwide)**.
> - This repository contains our complete solution for the **MCM/ICM 2025 Problem E**.
> - We developed a dynamic model using modified Lotka-Volterra equations to simulate the nitrogen cycle in forest and agricultural ecosystems, analyzing the ecological transition from forest to sustainable farmland.
> - This project includes the **TeX source document** of the thesis as well as **all the codes**.
> - In addition, for the Chinese version of the paper and the personal journey, please refer to the blog post **[2025 MCM E Problem F Award Winning Paper Sharing](https://www.cnblogs.com/JQ-Luke/p/18858431)**.
---

## 📖 Abstract

The conversion of forests to farmland significantly alters ecosystem structure and function. This study investigates these ecological consequences by focusing on **nitrogen cycling** as a key indicator of ecosystem health. We employ a dynamic modeling approach to simulate nitrogen flow through forest and agricultural food webs, providing quantitative insights into the impacts of human agricultural practices.

## 🔬 Core Models Developed

This study is built upon a progressive sequence of three core models:

* **FENCM (Forest Ecosystem Nitrogen Cycle Model):** A foundational model using a modified Lotka-Volterra approach to simulate the nitrogen flow through a natural forest food web, establishing a baseline for a healthy ecosystem.
* **AENCM (Agricultural Ecosystem Nitrogen Cycle Model):** An extension of FENCM that incorporates human interventions such as planting, harvesting, fertilization, and pesticide use, allowing for the simulation of different farming strategies.
* **AE-FW-NCM (Agricultural Ecosystem-Food Web-Nitrogen Cycle Model):** The most comprehensive model, which includes a complex food web structure with multiple trophic levels, reflecting a more mature and stabilized agricultural ecosystem over time.

## 📁 Repository Structure

The repository is organized as follows to ensure clarity and reproducibility:

```plaintext
MCM-ICM-2025-E-Nitrogen-Cycling-Model/
│
├── .gitignore               # Git ignore configuration
├── LICENSE                  # MIT License file
├── README.md                # This file (English version)
├── README_zh.md             # Chinese version of the README
├── requirements.txt         # Python dependency list
│
├── notebooks/               # All code and visualizations
│   ├── 1_model_1.ipynb      # Model 1 (FENCM)
│   ├── 2_model_2.ipynb      # Model 2 (AENCM)
│   ├── 3_model_3.ipynb      # Model 3 (AE-FW-NCM)
│   └── 4_sensitivity_anlysis.ipynb # sensitivity anlysis
│
└── paper/                   # The complete academic paper
    ├── main.tex             # LaTeX source file
    ├── references.bib       # references
    ├── figures/             # figures
    └── 2515324.pdf          # Final PDF version of our paper
```

## 🚀 Getting Started

To get a local copy up and running, follow these simple steps.

Prerequisites
- Python 3.8 or higher
- Pip package manager

Installation
1. **Clone the repository and install dependencies.** The following commands will set up the project in one go.

```Bash
git clone https://github.com/LUKEQ420/MCM-ICM-2025-E-Nitrogen-Cycling-Model.git
cd MCM-ICM-2025-E-Nitrogen-Cycling-Model
pip install -r requirements.txt
```

2. **Run the analysis.** Our entire workflow is contained within the Jupyter Notebooks. Launch JupyterLab and run them in sequential order to replicate the results.

```Bash
# Launch Jupyter Lab to open the notebooks
jupyter lab
```
Once JupyterLab opens, navigate to the `notebooks/` directory and run the files starting with `1_model_1.ipynb`.

## 📄 Paper & Citation
Our complete methodology, analysis, and findings are detailed in the academic paper located in the `paper/` directory. If you find our work useful in your research, we would appreciate a citation.

```Code snippet
@inproceedings{Lu2025,
  title     = {From Forest to Farm: Modeling Nitrogen Dynamics for Sustainable Agriculture},
  author    = {Lu, Junqi and Wu, Yuejiao and Peng, Linjing},
  booktitle = {The Mathematical Contest in Modeling (MCM/ICM)},
  year      = {2025},
  publisher = {COMAP, Inc.},
  note      = {Team 2515324, Finalist Award}
}
```

## ⚖️ License
This project is distributed under the MIT License. See the `LICENSE` file for more information.

---
