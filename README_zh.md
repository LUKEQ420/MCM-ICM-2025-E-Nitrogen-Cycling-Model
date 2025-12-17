# 从森林到农场：可持续农业中的氮动力学建模

<div align="center">
<p>
    <img src="https://img.shields.io/badge/MCM/ICM-2025-blue" alt="竞赛徽章">
    <img src="https://img.shields.io/badge/Award-Finalist-brightgreen" alt="奖项徽章">
    <img src="https://img.shields.io/badge/License-MIT-yellow" alt="许可证徽章">
</p>
</div>
<div align="left">

Available in: **[English Version](./README.md)** 

</div>

> 🏆 特等奖提名奖 (Finalist Award | 全球27,456支队伍中排名前1.8%)
> -  本仓库包含了我们为 **[2025年MCM/ICM竞赛E题](https://www.contest.comap.com/undergraduate/contests/mcm/contests/2025/problems/2025_ICM_Problem_E.pdf)** 提交的完整解决方案。
> -  我们采用基于改进Lotka-Volterra方程的动态建模方法，模拟了森林与农业生态系统中的氮循环过程，并深入分析了从森林到可持续性农田的生态系统转变。
> -  本项目中包含了论文的**tex源文档**以及**所有代码**。
> -  对于我们论文思路，以及正文讲解，请见 **[本人博客文章](https://www.cnblogs.com/JQ-Luke/p/18858431)**。
> - 推荐阅读顺序：
>   1. 阅读[模型一的jupyter笔记本](./notebooks/1_model_1.ipynb)，包含我对欧拉法与微分方程模型的理解，如何调参，以及相应的求解代码；
>   2. 阅读[中文博客](https://www.cnblogs.com/JQ-Luke/p/18858431)中的思路讲解，我们建立模型解决问题的过程，强烈建议在读之前 **[先读一遍赛题](https://www.contest.comap.com/undergraduate/contests/mcm/contests/2025/problems/2025_ICM_Problem_E.pdf)**，先理解问题能够更容易读懂我们解决问题的思路；
>   3. 阅读我们的英文版参赛论文和后续代码（尽信书不如无书，希望大家对我们论文**批判性阅读**，取长补短，在博客里赛后复盘我其实感觉我们有很多点没做好，希望后来者能够吸取我们的经验教训做得更好）；
>   4. 拓展阅读，读完我们文章之后建议再去找一下本题的o奖论文，横向对比一下其他人的解决方案。以及往年的微分方程题目（通常是A题）相应的o奖论文，从而以本项目为起点学会微分方程这一类问题的解决方法。
> - **本项目内容仍在不定期更新中**，建议时不时来看看有没有新内容。此外有任何改进的意见（或是错误）欢迎在本项目中提issue，让我们一起让这个项目变好吧！
---

## 📖 摘要

将森林转变为农田会极大地改变生态系统的结构与功能。本研究聚焦于作为生态系统健康关键指标的**氮循环**，以探究这些生态后果。我们采用动态建模方法来模拟氮元素在森林和农业食物网中的流动，为人类农业活动带来的影响提供量化分析。

---

## 🔬 核心模型

本研究基于三个递进的核心模型构建：

* **FENCM (森林生态系统氮循环模型):** 一个基础模型，使用改进的Lotka-Volterra方法模拟自然森林食物网中的氮流动，为健康的生态系统建立基准。
* **AENCM (农业生态系统氮循环模型):** FENCM的扩展，该模型纳入了种植、收获、施肥和农药使用等人类干预活动，从而能够模拟不同的耕作策略。
* **AE-FW-NCM (农业生态系统-食物网-氮循环模型):** 最全面的模型，包含一个具有多个营养级的复杂食物网结构，反映了随着时间的推移，一个更加成熟和稳定的农业生态系统。

---

## 📁 仓库结构

为了确保清晰性和可复现性，本仓库按以下结构组织：

```plaintext
MCM-ICM-2025-E-Nitrogen-Cycling-Model/
│
├── .gitignore               # Git忽略配置文件
├── LICENSE                  # MIT许可证文件
├── README.md                # 本文档的英文版
├── README_zh.md             # 本文档（中文版）
├── requirements.txt         # Python项目依赖列表
│
├── notebooks/               # 存放所有的代码与可视化结果
│   ├── 1_model_1.ipynb      # 模型一求解代码，以及我对于微分方程的讲解
│   ├── 2_model_2.ipynb      # 模型二 (AENCM) 求解代码
│   ├── 3_model_3.ipynb      # 模型三 (AE-FW-NCM) 求解代码
│   └── 4_sensitivity_anlysis.ipynb # 灵敏度分析求解代码
│
└── paper/                   # 存放完整的学术论文
    ├── main.tex             # LaTeX源文件
    ├── references.bib       # 参考文献
    ├── figures/             # 图片
    └── 2515324.pdf          # 最终的PDF版本论文
```

## 🚀 开始使用

本项目依赖 **Python** (用于数据分析和模型求解) 和 **LaTeX** (用于论文排版)。为了帮助你顺利运行本项目，我们提供了以下三种配置方法，请根据你的熟悉程度选择（**如遇到任何问题，建议复制本文件所有内容，在大模型的指导下进行**）：

**环境要求:**
* **Python:** 建议使用 Python 3.8 或更高版本。
* **Pip:** Python 的包管理器，通常随 Python 一起安装。
* **代码编辑器:** 推荐使用 [VS Code](https://code.visualstudio.com/)，并安装 [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) 和 [Jupyter](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter) 扩展。
* **(可选) Git:** 版本控制工具，用于方法二。[点此下载](https://git-scm.com/downloads)。
* **(可选) Anaconda:** 对于初学者，[Anaconda](https://www.anaconda.com/download) 是一个更简单的 Python 环境管理工具，它自带了 Python, Pip, Jupyter 等常用库。

---

### 开始方法一（云端运行：使用 GitHub Codespaces）

这是对于新手**最推荐**的方式。它不需要你在本地安装任何软件（Python, Git, VS Code 都不需要），一切都在你的浏览器中完成，并且能保持最新。

> *优点：无需本地配置，环境纯净，可随时随地跨设备访问。如果你 Fork 了项目，你所做的任何修改都会保存在你自己的仓库中。*

1.  **注册 GitHub 账户**
    如果你还没有 GitHub 账户，请先注册一个。

2.  **(可选，但推荐) Fork 本项目**
    * 在项目主页右上角，点击 **`Fork`** 按钮。
    * 这会把本仓库复制一份到你自己的 GitHub 账户下。这样做的好处是，你可以在你自己的版本上自由修改、运行和保存代码，而不用担心“弄乱”原项目。

3.  **启动 Codespace**
    * 在你 **Fork 后的仓库**（或原仓库）页面，点击绿色的 **`<> Code`** 按钮。
    * 切换到 **`Codespaces`** 标签页。
    * 点击 **`Create codespace on main`** (或你 Fork 后的分支名)。

4.  **等待环境配置**
    * 请耐心等待 1-2 分钟。GitHub 会在云端为你创建一个虚拟电脑，并自动执行安装依赖、配置环境等所有步骤。
    * *注：GitHub 为学生提供每月免费的 Codespaces 使用额度，通常足够用于课程学习和项目探索。*

5.  **开始使用！**
    * 配置完成后，你的浏览器会打开一个完整的“在线 VS Code”界面。
    * 所有文件和依赖都已准备就绪。你只需在左侧文件浏览器中进入 `notebooks/` 目录，打开 `1_model_1.ipynb` 即可开始运行和学习。

---

### 开始方法二（使用 Git 克隆到本地）

这种方法最适合希望长期跟进项目更新、或者未来可能想学习使用 Git 的同学。它能让你通过简单的命令获取项目的最新版本。

1.  **安装 Git**
    如果你电脑上还没有 Git，请先[下载并安装它](https://git-scm.com/downloads)。

2.  **克隆仓库**
    打开你的终端（在 Windows 上可能是 "命令提示符"、"PowerShell" 或 "Git Bash"；在 macOS/Linux 上是 "终端"）。先使用`cd + 绝对路径`打开你希望克隆到的文件夹，输入以下命令将项目复制（克隆）到你的电脑上：

    ```bash
    # 将项目克隆到你当前所在的文件夹
    git clone https://github.com/LUKEQ420/MCM-ICM-2025-E-Nitrogen-Cycling-Model.git
    ```

3.  **进入项目目录**
    ```bash
    cd MCM-ICM-2025-E-Nitrogen-Cycling-Model
    ```

4.  **创建并激活虚拟环境 (强烈推荐)**
    为了避免和你电脑上其他 Python 项目的依赖包产生冲突，我们强烈建议创建一个“隔离”的虚拟环境：

    ```bash
    # 1. 创建一个名为 .venv 的虚拟环境文件夹
    python -m venv .venv
    
    # 2. 激活这个环境
    #    在 Windows (CMD/PowerShell) 上:
    .\.venv\Scripts\activate
    #    在 macOS / Linux (Bash) 上:
    source .venv/bin/activate
    ```
    *激活成功后，你会在终端提示符的开头看到 `(.venv)` 字样。*

5.  **安装项目依赖**
    确保你处于已激活虚拟环境的终端中，运行：

    ```bash
    # pip 会自动读取 requirements.txt 文件，并安装所有必需的库
    pip install -r requirements.txt
    ```

6.  **启动 Jupyter Lab**
    所有代码都在 Jupyter Notebook 中。安装完依赖后，运行：

    ```bash
    # 这将在你的默认浏览器中打开一个新标签页
    jupyter lab
    ```

7.  **开始探索！**
    在浏览器打开的 JupyterLab 界面中，从左侧文件浏览器进入 `notebooks/` 目录，点击 `1_model_1.ipynb` 开始你的探索之旅。

---

### 开始方法三（最简单：下载 ZIP 压缩包）

如果你不熟悉 Git，只想快速查看一下代码和论文，这是一个最直接且**最简单**的方法。
> *注：这种方法非常简单，但缺点是无法通过 `git pull` 快速获取项目更新。如果项目有重要更新，你需要重新下载 ZIP 包。*

1.  **下载压缩包**
    在项目的 GitHub 主页 (确保是英文版 [README.md](https://github.com/LUKEQ420/MCM-ICM-2025-E-Nitrogen-Cycling-Model) 所在的页面)，点击右上角绿色的 **`<> Code`** 按钮，然后点击 **`Download ZIP`**。

2.  **解压文件**
    将下载的 `MCM-ICM-2025-E-Nitrogen-Cycling-Model-main.zip` 文件解压到你希望存放项目的文件夹。

3.  **安装 VS Code (如果尚未安装)**
    [下载并安装 VS Code](https://code.visualstudio.com/)。它是一个功能强大的免费代码编辑器。

4.  **在 VS Code 中打开项目**
    启动 VS Code，点击左上角“文件 (File)” > “打开文件夹 (Open Folder)”，然后选择你刚才**解压后的文件夹**。

5.  **安装推荐的扩展**
    打开文件夹后，VS Code 可能会在右下角弹窗，推荐你本项目所需的扩展。请务必安装 **Python** 和 **Jupyter** 这两个扩展（均由 Microsoft 发布）。

6.  **安装 Python 依赖库**
    * 在 VS Code 中，打开一个新终端 (点击顶部菜单“终端 (Terminal)” > “新建终端 (New Terminal)”)。
    * **建议：** 同样如“方法二”的第4步，在终端中创建并激活一个虚拟环境。
    * 在（已激活虚拟环境的）终端中，运行 `pip install -r requirements.txt` 来安装依赖。

7.  **运行 Notebook**
    在 VS Code 左侧的文件浏览器中，进入 `notebooks/` 目录，点击 `1_model_1.ipynb`。VS Code 将在编辑器窗口中打开它，你可以直接在 VS Code 中运行和修改代码。

8.  **查看论文 (三种方式)**
    * **(最简单) 直接阅读PDF：** 对于初学者，最快的方式是直接打开 `paper/` 目录下的 `2515324.pdf` 最终版论文。
    * **(在线编译) 使用 Overleaf：** 如果你想在线查看或修改 `.tex` 源文件，这是一个很好的免安装选项：
        1.  将你解压项目中的 `paper/` 文件夹单独压缩成一个 `.zip` 文件 (例如 `paper.zip`)。
        2.  访问 [Overleaf (www.overleaf.com)](https://www.overleaf.com/) 并注册一个免费账户。
        3.  在 Overleaf 项目面板，点击 "New Project" (新建项目)，然后选择 "Upload Project" (上传项目)。
        4.  上传你刚刚创建的 `paper.zip` 文件。Overleaf 会自动打开项目，你可以在线编译和查看 PDF。
    * **(本地编译) 使用 VS Code：** 如果你想在本地编译 `.tex` 论文源文件，你需要：
        1.  安装一个 LaTeX 发行版（例如 [TeX Live](https://www.tug.org/texlive/) 或 [MiKTeX](https://miktex.org/)）。
        2.  在 VS Code 中安装 [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) 扩展。



## ⚖️ 许可证
本项目采用 MIT 许可证发行。更多信息请参见 `LICENSE` 文件。
