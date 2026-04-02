# 🌍 World Happiness Report — EDA & Multi-Year Analysis

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?logo=pandas)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12-4c9be8)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7-orange)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter)
![Kaggle](https://img.shields.io/badge/Kaggle-Notebook-20BEFF?logo=kaggle)

> *What makes a country happy? Using 5 years of UN happiness data across 150+ countries, this project finds which factors drive national wellbeing — and which barely matter.*

---

## 📌 Project Overview

This project performs a complete **Exploratory Data Analysis (EDA)** on the [World Happiness Report](https://www.kaggle.com/datasets/unsdsn/world-happiness) dataset (2015–2019).

It covers data cleaning, correlation analysis, multi-year trend tracking, regional comparison, and visualization — structured as a Kaggle portfolio notebook.

🔗 **[View on Kaggle](https://www.kaggle.com/code/raunakgangwal/world-happiness-report-analysis)** 

---

## 🔍 Key Questions Answered

- Which country is the happiest in the world — and why?
- Which factor **most strongly** predicts happiness?
- Which factor has **almost no effect** on happiness? *(The answer is surprising)*
- How has **global happiness changed** from 2015 to 2019?
- Which country had the **biggest improvement** — and which had the **biggest decline**?

---

## 💡 Key Findings

| Finding | Detail |
|---|---|
| 🥇 Strongest happiness driver | GDP per capita (r = 0.79) |
| 🤝 Close second | Social support & Healthy life expectancy (both r = 0.78) |
| 😲 Weakest driver | Generosity — near-zero correlation (r = 0.076) |
| 🏆 Happiest country (2019) | Finland (7.769) |
| 😞 Unhappiest country (2019) | South Sudan (2.853) |
| 💰 Richest ≠ Happiest | Qatar has highest GDP but ranks only 29th |
| 📈 Biggest improvement (2015→2019) | Benin (+1.543) |
| 📉 Biggest decline (2015→2019) | Venezuela (−2.103) |
| 🌏 Happiest region | Australia & New Zealand (avg 7.27) |
| 😞 Unhappiest region | Sub-Saharan Africa (avg 4.31) |

---

## 📁 Project Structure

```
World-Happiness-Report-Analysis/
│
├── 2015.csv
├── 2016.csv
├── 2017.csv
├── 2018.csv
├── 2019.csv
│
├── world_happiness_portfolio.ipynb   ← Main analysis notebook
└── README.md
```

---

## 📊 Visualizations Included

| Chart | Key Insight |
|---|---|
| Horizontal bar — Top 15 happiest countries | Nordic dominance is undeniable |
| Scatter + regression — GDP vs Score | Strong positive relationship (r = 0.79) |
| Heatmap — Full correlation matrix | Generosity is surprisingly the weakest factor |
| Line chart — Global trend 2015–2019 | Stable globally, volatile at country level |
| Bar chart — Happiness by region | Nearly 3x gap between top and bottom regions |

---

## 🗂️ Analysis Sections

### 1. Data Loading & Exploration
- Shape, dtypes, missing values, descriptive statistics
- Dataset: 156 countries × 9 columns, zero nulls, zero duplicates
- Global average happiness score: **5.407** (range: 2.853 – 7.769)

### 2. Ranking & Filtering
- Top 10 and bottom 10 countries by happiness score
- Countries filtered by GDP threshold, Social Support, Life Expectancy

### 3. Correlation & Numeric Analysis
- Full correlation matrix computed and visualized
- Highest GDP country identified — checked if it's also the happiest
- Regional analysis via merge with 2015 dataset (only year with Region column)

### 4. Multi-Year Analysis (2015–2019)
- All 5 CSV files loaded with inconsistent column names — standardized and concatenated
- Global happiness tracked year by year
- Country-level trend: Finland (↑), Denmark (→), India (↓)
- Biggest improvement and decline computed via pivot table

### 5. Visualizations
- 5 charts with narrative interpretation after each plot

---

## 🚀 How to Run

**Option 1 — Kaggle (recommended, no setup needed)**
> Dataset is pre-attached on Kaggle. Just open and Run All.  
> 🔗 [View Notebook on Kaggle](https://www.kaggle.com/code/raunakgangwal/world-happiness-report-analysis)

**Option 2 — Run Locally**

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/world-happiness-eda.git
cd world-happiness-eda

# 2. Install dependencies
pip install pandas matplotlib seaborn jupyter

# 3. Download dataset from Kaggle
pip install kaggle
kaggle datasets download -d unsdsn/world-happiness
unzip world-happiness.zip -d data/

# 4. Launch the notebook
jupyter notebook world_happiness_portfolio.ipynb
```

> **Note:** Requires a free [Kaggle account](https://www.kaggle.com) and API token (`kaggle.json`) for CLI download.

---

## 🧠 Skills Demonstrated

| Skill | Used In |
|---|---|
| `pd.merge()` | Joining 2019 data with 2015 Region column |
| `pd.concat()` | Combining 5 years of data into one DataFrame |
| Column standardization | Renaming inconsistent column names across 5 files |
| `.corr()` + interpretation | Identifying strongest/weakest happiness drivers |
| `groupby()` + `pivot_table()` | Regional analysis, year-over-year trends |
| `sns.regplot()` | GDP vs Score scatter with regression line |
| Multi-file null handling | Fixing 2018's single missing value mid-pipeline |

---

## 📚 Dataset

- **Name:** World Happiness Report
- **Publisher:** UN Sustainable Development Solutions Network (SDSN)
- **Source:** [Kaggle — unsdsn/world-happiness](https://www.kaggle.com/datasets/unsdsn/world-happiness)
- **Years Covered:** 2015 · 2016 · 2017 · 2018 · 2019
- **License:** CC0 Public Domain

---

## 👤 Author

**Raunak Gangwal**  
Final Year Engineering Student — SNJB's College of Engineering, Nashik  

[![Kaggle](https://img.shields.io/badge/Kaggle-Profile-20BEFF?logo=kaggle)](https://www.kaggle.com/raunakgangwal)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?logo=linkedin)](https://www.linkedin.com/in/raunakgangwal/)

---
