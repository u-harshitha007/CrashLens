#  CrashLens — Road Accident Data Analysis

> **A real-world Data Science project that analyzes road accident patterns to uncover insights that could save lives.**

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-orange?logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-red)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-purple)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)

---

## Project Overview

**CrashLens** is a beginner-to-intermediate Data Science project that dives into real-world road accident data.  
The goal is to identify **accident patterns**, **contributing factors**, and **actionable insights** that could help improve road safety.

This project is built **step-by-step** as part of a Data Science learning journey, focusing on:
- Data loading and exploration with **Pandas**
- Numerical analysis with **NumPy**
- Data visualization with **Matplotlib** and **Seaborn**

---

##  Project Structure

```
CrashLens/
│
├── data/
│   ├── raw/              ← Original, untouched dataset
│   └── processed/        ← Cleaned & transformed data
│
├── notebooks/            ← Jupyter Notebooks (step-by-step analysis)
│
├── src/                  ← Reusable Python scripts/modules
│
├── visualizations/       ← Saved charts and plots
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

##  Dataset

- **Source:** [UK Road Safety — Road Accidents Dataset (Kaggle)](https://www.kaggle.com/datasets/silicon99/dft-accident-data)
- **Size:** ~1.8 million accident records (2005–2017)
- **Key Features:** Location, severity, weather, road conditions, vehicle types, casualties

>  Raw data files are excluded from version control (see `.gitignore`).  
> Download the dataset from Kaggle and place it in `data/raw/`.

---

##  Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/u-harshitha007/CrashLens.git
cd CrashLens
```

### 2. Create a virtual environment (recommended)
```bash
python -m venv venv
venv\Scripts\activate        # Windows
# source venv/bin/activate   # Mac/Linux
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook
```bash
jupyter notebook
```

---

## 📈 Milestones

| # | Milestone | Status |
|---|-----------|--------|
| 1 | Project setup & folder structure |  Done |
| 2 | Dataset loading & first look | In Progress |
| 3 | Data cleaning & handling missing values |  Upcoming |
| 4 | Exploratory Data Analysis (EDA) |  Upcoming |
| 5 | Visualizations & insights | Upcoming |

---

##  Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.10+ | Core programming language |
| Pandas | Data loading, cleaning, analysis |
| NumPy | Numerical computations |
| Matplotlib | Plotting and charting |
| Seaborn | Statistical visualizations |
| Jupyter Notebook | Interactive analysis environment |

---

 
