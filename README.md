# From Forest to Farm: Modeling Nitrogen Dynamics for Sustainable Agriculture

<div align="center">
<p>
    <img src="https://img.shields.io/badge/MCM/ICM-2025-blue" alt="Contest Badge">
    <img src="https://img.shields.io/badge/Award-Finalist-brightgreen" alt="Award Badge">
    <img src="https://img.shields.io/github/stars/LUKEQ420/MCM-ICM-2025-E-Nitrogen-Cycling-Model?style=social" alt="GitHub stars">
    <img src="https://img.shields.io/badge/License-MIT-yellow" alt="License Badge">
</p>

<div align="left">

Available in: **[简体中文 (Chinese)](./README_zh.md) <- 点击切换中文版** 

> 🏆 **Finalist Award (Top 1.8% of 27,456 teams worldwide)**
> - This repository contains our complete solution for the **[MCM/ICM 2025 Problem E](https://www.contest.comap.com/undergraduate/contests/mcm/contests/2025/problems/2025_ICM_Problem_E.pdf)**.
> - We developed a dynamic model using modified Lotka-Volterra equations to simulate the nitrogen cycle in forest and agricultural ecosystems, analyzing the ecological transition from forest to sustainable farmland.
> - This project includes the **TeX source document** of the paper as well as **all the code**.
</div>


<div align="center">
  <img src="./paper/figures/our%20work.jpg" alt="Our Work Workflow" width="85%">
  <p><em>Figure 1: The overall workflow and logical framework of our study.</em></p>
</div>
</div>

---

## 📖 Abstract

The conversion of forests to farmland significantly alters ecosystem structure and function. This study investigates these ecological consequences by focusing on **nitrogen cycling** as a key indicator of ecosystem health. We employ a dynamic modeling approach to simulate nitrogen flow through forest and agricultural food webs, providing quantitative insights into the impacts of human agricultural practices.

---

## 🔬 Core Models Developed

This study is built upon a progressive sequence of three core models. Below are the schematic representations of the ecological dynamics we modeled.

### 1. FENCM (Forest Ecosystem Nitrogen Cycle Model)
A foundational model using a modified Lotka-Volterra approach to simulate the nitrogen flow through a natural forest food web. It accounts for the decomposition process where organic nitrogen transforms back into inorganic forms, establishing a baseline for a healthy ecosystem.

<div align="center">
  <img src="./paper/figures/forest%20ecosystem.jpg" alt="Forest Ecosystem Model" width="70%">
  <p><em>Figure 2: The nitrogen flux dynamics within a natural forest ecosystem.</em></p>
</div>

### 2. AENCM (Agricultural Ecosystem Nitrogen Cycle Model)
An extension of FENCM that incorporates human interventions. The model explicitly simulates the **Agricultural Cycle** (as shown below), quantifying the impact of sowing, harvesting, fertilization, and pesticide use on the nitrogen dynamics between crops and weeds.

<div align="center">
  <img src="./paper/figures/Agriculture%20cycle.jpg" alt="Agriculture Cycle" width="60%">
  <p><em>Figure 3: The modeled agricultural cycle stages affecting nitrogen inputs and outputs.</em></p>
</div>

### 3. AE-FW-NCM (Agricultural Ecosystem-Food Web-Nitrogen Cycle Model)
The most comprehensive model, reflecting a stabilized agricultural ecosystem. We expanded the food chain into a complex **Food Web** involving 7 species (including bats and biological control agents) to analyze stability and biodiversity recovery.

<div align="center">
  <img src="./paper/figures/food%20web.jpg" alt="Agricultural Food Web" width="75%">
  <p><em>Figure 4: The complex agricultural food web structure incorporating biological controls.</em></p>
</div>

---

## 📁 Repository Structure

The repository is organized as follows to ensure clarity and reproducibility:

```plaintext
MCM-ICM-2025-E-Nitrogen-Cycling-Model/
│
├── .gitignore               # Git ignore configuration
├── LICENSE                  # MIT License file
├── README.md                # This file (English version)
├── README_zh.md             # Chinese version of the README
├── requirements.txt         # Python dependency list
│
├── notebooks/               # All code, models, and visualizations
│   ├── 1_model_1.ipynb      # Model 1 (FENCM)
│   ├── 2_model_2.ipynb      # Model 2 (AENCM)
│   ├── 3_model_3.ipynb      # Model 3 (AE-FW-NCM)
│   └── 4_sensitivity_analysis.ipynb # Sensitivity analysis
│
└── paper/                   # The complete academic paper
    ├── main.tex             # LaTeX source file
    ├── references.bib       # Bibliography file
    ├── figures/             # Image assets
    └── 2515324.pdf          # Final PDF version of our paper
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

## ⭐ Star History
<div align="center">
  <a href="https://star-history.com/#LUKEQ420/MCM-ICM-2025-E-Nitrogen-Cycling-Model&Date">
    <img src="https://api.star-history.com/svg?repos=LUKEQ420/MCM-ICM-2025-E-Nitrogen-Cycling-Model&type=Date" alt="Star History Chart" width="70%">
  </a>
</div>

## ⚖️ License
This project is distributed under the MIT License. See the `LICENSE` file for more information.

---
