# 🔍 CrashLens — Road Accident Data Analysis

> **A real-world Data Science project that analyzes road accident patterns to uncover insights that could save lives.**

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-orange?logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-red)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-purple)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)

---

## 📌 Project Overview

**CrashLens** is a beginner-to-intermediate Data Science project that dives into real-world road accident data.
The goal is to identify **accident patterns**, **contributing factors**, and **actionable insights** that could help improve road safety.

This project is built **step-by-step** as part of a Data Science learning journey, focusing on:
- Data loading and exploration with **Pandas**
- Numerical analysis with **NumPy**
- Data visualization with **Matplotlib** and **Seaborn**

---

## 🎯 Project Objectives

By the end of this project, we aim to:

1. **Understand the data** — Load, inspect, and describe the dataset using Pandas
2. **Clean the data** — Handle missing values, fix data types, and prepare data for analysis
3. **Explore patterns** — Discover trends in accident severity, time of day, weather, and road types
4. **Visualize findings** — Create meaningful charts that communicate insights clearly
5. **Build ML-readiness** — Lay the groundwork for future machine learning (predicting accident severity)

---

## 📦 Dataset

### 🗂️ Dataset Source

| Field | Details |
|-------|---------|
| **Name** | UK Road Safety — Road Collision Statistics 2023 |
| **Publisher** | UK Department for Transport (DfT) |
| **Portal** | [data.gov.uk — Road Accidents Safety Data](https://data.gov.uk/dataset/cb7ae6f0-4be6-4935-9277-47e5ce24a11f/road-accidents-safety-data) |
| **Licence** | [Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/) — free to use |
| **Format** | CSV (Comma-Separated Values) |
| **Direct URL** | https://data.dft.gov.uk/road-accidents-safety-data/dft-road-casualty-statistics-collision-2023.csv |

---

### 📊 Dataset Description

The dataset contains **~104,000 real road accident records** from across the United Kingdom for the year **2023**, recorded by police forces under the STATS19 reporting system.

| Property | Value |
|----------|-------|
| **Rows (Accidents)** | ~104,000 |
| **Columns (Features)** | 44 |
| **Time Period** | January 2023 – December 2023 |
| **Geographic Coverage** | England, Wales, and Scotland |
| **File Size** | ~20 MB |

**Key columns we will use:**

| Column | What it tells us |
|--------|-----------------|
| `collision_severity` | How serious was the accident? (1=Fatal, 2=Serious, 3=Slight) |
| `date` | The date the accident occurred |
| `time` | Time of day (24-hour format) |
| `day_of_week` | Day of the week (1=Sunday … 7=Saturday) |
| `weather_conditions` | Weather at the time of the accident |
| `road_surface_conditions` | Road surface state (dry, wet, icy, etc.) |
| `speed_limit` | Speed limit on the road in mph |
| `light_conditions` | Daylight, darkness, street lighting, etc. |
| `urban_or_rural_area` | City (urban) vs. countryside (rural) |
| `latitude` / `longitude` | Exact GPS coordinates of the accident |
| `number_of_vehicles` | How many vehicles were involved |
| `number_of_casualties` | How many people were injured or killed |

---

### ✅ Why This Dataset Was Chosen

This dataset was selected over other popular options (e.g., Kaggle datasets requiring login) for the following reasons:

1. **Official & Trustworthy** — Published by the UK government. Verified, real-world data.
2. **No account required** — Direct CSV download via URL. No Kaggle login or API key needed.
3. **Beginner-friendly size** — ~104,000 rows loads in seconds on a laptop. Not too big, not too small.
4. **Rich real-world features** — Weather, time, severity, GPS, road type — perfect for meaningful EDA.
5. **Open licence** — Free to use in personal projects, portfolios, and academic submissions.
6. **ML-ready target column** — `collision_severity` is a clean, 3-class classification target for future ML work.
7. **Internationally recognised** — UK STATS19 data is used in research papers and university courses worldwide.

---

### ⬇️ How to Download the Dataset

> ⚠️ Raw data files are **not included** in this repository (excluded via `.gitignore`).
> You must download the dataset and place it in the correct folder before running any notebooks.

**Step 1 — Download the file**

**Option A:** Click the direct link to download in your browser:
👉 [Download road_accidents_uk_2023.csv](https://data.dft.gov.uk/road-accidents-safety-data/dft-road-casualty-statistics-collision-2023.csv)

**Option B:** Use Python:
```python
import urllib.request
url = "https://data.dft.gov.uk/road-accidents-safety-data/dft-road-casualty-statistics-collision-2023.csv"
urllib.request.urlretrieve(url, "data/raw/road_accidents_uk_2023.csv")
print("Download complete!")
```

**Option C:** Use PowerShell (Windows):
```powershell
Invoke-WebRequest -Uri "https://data.dft.gov.uk/road-accidents-safety-data/dft-road-casualty-statistics-collision-2023.csv" -OutFile "data\raw\road_accidents_uk_2023.csv"
```

**Step 2 — Place the file here:**
```
CrashLens/
└── data/
    └── raw/
        └── road_accidents_uk_2023.csv   ← file goes here
```

---

## 🗂️ Project Structure

```
CrashLens/
│
├── data/
│   ├── raw/              ← Original, untouched dataset (not in Git)
│   └── processed/        ← Cleaned & transformed data (not in Git)
│
├── notebooks/            ← Jupyter Notebooks (step-by-step analysis)
│   └── 01_data_loading.ipynb
│
├── src/                  ← Reusable Python scripts/modules
│   └── __init__.py
│
├── reports/              ← Written summaries and EDA findings
│
├── visualizations/       ← Saved charts and plots
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## 🚀 Getting Started

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

### 4. Download the dataset
Follow the **How to Download the Dataset** section above and place the file in `data/raw/`.

### 5. Launch Jupyter Notebook
```bash
jupyter notebook
```

---

## 📈 Current Progress & Milestones

| # | Milestone | Status |
|---|-----------|--------|
| 1 | Project setup & folder structure | ✅ Done |
| 2 | Dataset research & documentation | ✅ Done |
| 3 | Data loading & first look (`01_data_loading.ipynb`) | 🔄 In Progress |
| 4 | Data cleaning & handling missing values | ⏳ Upcoming |
| 5 | Exploratory Data Analysis (EDA) | ⏳ Upcoming |
| 6 | Visualizations & insights | ⏳ Upcoming |

### 🔜 Next Steps
- Complete `notebooks/01_data_loading.ipynb` — load dataset, inspect shape, columns, and data types
- Create `notebooks/02_data_cleaning.ipynb` — handle nulls, fix types, drop irrelevant columns
- Create `notebooks/03_eda.ipynb` — explore patterns by time, weather, severity, and location

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.10+ | Core programming language |
| Pandas | Data loading, cleaning, analysis |
| NumPy | Numerical computations |
| Matplotlib | Plotting and charting |
| Seaborn | Statistical visualizations |
| Jupyter Notebook | Interactive analysis environment |

---

## 👩‍💻 Author

**Harshitha**
📍 Aspiring Data Scientist | Learning by Building
🔗 [GitHub](https://github.com/u-harshitha007)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
