# ☀️ Solar Challenge Week 0

A Python-based project for the Solar Challenge Week 0 task.  
This repository contains all code, dependencies, and setup instructions needed to reproduce and run the environment locally.

---

## 📦 Project Overview

This project is part of the **Solar Challenge** initiative.  
It demonstrates environment setup, dependency management, and reproducible development practices using Python virtual environments.

---

## 🧩 Tasks Description

### Task 1: Git & Environment Setup

The goal of Task 1 was to establish a reproducible and collaborative development environment before starting data analysis.  
Key accomplishments include:

- Created the GitHub repository `solar-challenge-week0`.
- Set up the Python virtual environment (`venv`) and automated dependency management with `requirements.txt`.
- Added `.gitignore` to exclude data files and temporary files.
- Developed a GitHub Actions CI workflow to automate environment setup checks on pushes and pull requests.
- Implemented a clean folder structure separating source code, notebooks, tests, and scripts.
- Documented the environment setup and usage in `README.md`.
- Completed multiple meaningful commits following conventional commit messages.
- Successfully merged `setup-task` branch into `main`, ensuring code review and integrity.

### Task 2: Data Profiling, Cleaning & Exploratory Data Analysis (EDA)

Task 2 focused on comprehensive profiling and cleaning of solar datasets for each country, preparing them for comparative analysis. Highlights include:

- Created dedicated branches and notebooks for country-specific EDA (e.g., `eda-benin`).
- Generated summary statistics and missing value reports for numeric solar variables (GHI, DNI, DHI, ModA, ModB, WS, WSgust, Tamb, RH).
- Detected outliers statistically via Z-score computations, flagging records with |Z| > 3.
- Cleaned data by imputing median values for missing data and removing extreme outliers.
- Planned and initiated time-series visualizations, correlation heatmaps, wind rose plots, and bubble charts for detailed insights.
- Ensured cleaned data export to `.gitignore`d folders to maintain repository cleanliness.

### Task 3: Cross-Country Solar Potential Comparison

This task synthesizes results for impactful cross-country insights. Main points include:

- Created `compare-countries` branch with `compare_countries.ipynb` notebook.
- Loaded cleaned datasets from Benin, Sierra Leone, and Togo.
- Compared key solar irradiance metrics (GHI, DNI, DHI) visually using side-by-side boxplots colored by country.
- Compiled statistical summaries (mean, median, standard deviation) for comparative evaluation.
- Performed statistical significance tests (one-way ANOVA, Kruskal–Wallis) on GHI values and reported p-values.
- Highlighted key observations such as highest solar potential and variability differences.
- Visualized ranked countries by average GHI, providing actionable insights for solar energy prospects.

---

Thank you for your interest in the Solar Challenge project.  
Please feel free to explore the notebooks and scripts to further your understanding and contribute improvements.




