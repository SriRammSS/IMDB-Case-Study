<div align="center">

# 🎬 IMDB Movies — Data Analysis Case Study

### Structured Task-Based EDA: Profitability, Directors, Genre, and Actor Analysis

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Statistical_Viz-4C72B0?style=for-the-badge)](https://seaborn.pydata.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)](LICENSE)

<br/>

> A structured 7-task analysis of the IMDB movies dataset covering data cleaning, profitability ranking, IMDb Top 250 construction, director performance, genre revenue, and actor comparison — with detailed markdown explanations at every step.

</div>

---

## Overview

This case study follows a guided analytical framework — each task builds on the cleaned output of the previous one — making it a complete end-to-end data analysis project rather than a loose collection of charts. The notebook is annotated throughout with findings and interpretations.

| Dimension | Value |
|-----------|-------|
| Cells | 54 |
| Dataset | `IMDB_Movies.csv` |
| Tasks | 7 structured analytical tasks |
| Rows retained after cleaning | ~77% |

---

## Analysis Tasks

| Task | Focus | Key Technique |
|------|-------|---------------|
| **Task 1** | Data loading and inspection | `.shape`, `.columns`, `.dtypes` |
| **Task 2** | Data cleaning | Drop 15 columns, row null filtering, language imputation |
| **Task 3.1** | Unit conversion | Budget & gross → million $ |
| **Task 3.2** | Profitability | `profit = gross - budget`, scatter plot, top 10 ranking |
| **Task 3.3** | Duplicate handling | Drop, re-rank (James Cameron appears twice) |
| **Task 3.4** | IMDb Top 250 | Filter `num_voted_users > 25,000`, sort by score, extract non-English films |
| **Task 3.5** | Director analysis | `groupby director → mean IMDb score` → top 10 directors |
| **Task 3.6** | Genre revenue | Split `genres` by `\|`, group by genre pair → **Family+Sci-Fi tops gross** |
| **Task 3.7** | Actor comparison | Meryl Streep vs DiCaprio vs Pitt — mean critic vs user reviews |

---

## Key Findings

| Finding | Detail |
|---------|--------|
| **Most profitable director** | James Cameron (appears in top 10 twice before deduplication) |
| **Highest-grossing genre combo** | Family + Sci-Fi |
| **Top actor (critics + users)** | Leonardo DiCaprio leads both critic and user review counts |
| **Non-English Top 250** | Veer-Zaara is a notable entry in the non-English IMDb Top 250 |
| **Most active decade** | Volume of voted users peaks in the 2000s (log-scale bar chart) |
| **Top director by IMDb score** | Damien Chazelle (La La Land era) in top 10 by average score |

---

## Tech Stack

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading, cleaning, groupby, merging |
| `numpy` | Numerical operations |
| `matplotlib` | Scatter plots, bar charts |
| `seaborn` | Statistical visualizations |

---

## How to Run

```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook "IMDB Case Study Question (1).ipynb"
```

> **Note:** Place `IMDB_Movies.csv` in the same directory before running.
