# ☀️ Solar Challenge Week 0

A Python-based project for the Solar Challenge Week 0 task.  
This repository contains all code, dependencies, and setup instructions needed to reproduce and run the environment locally.

---

## 📦 Project Overview

This project is part of the **Solar Challenge** initiative.  
It demonstrates environment setup, dependency management, and reproducible development practices using Python virtual environments.

The primary goal is to handle solar datasets across several countries, perform exploratory data analysis, and compare solar potential across regions to inform energy strategies.

---

## 🛠 Features

- Python virtual environment setup and dependency management  
- Data profiling, cleaning, and exploratory data analysis (EDA) for multiple countries  
- Cross-country solar data comparison with statistical testing  
- Continuous integration with GitHub Actions for automated environment validation

---

## 🧩 Steps to Reproduce the Environment

1. **Clone the repository**  
```bash git clone https://github.com/msultan001/solar-challenge-week0```

2. **Navigate into the project directory**  
```bash cd solar-challenge-week0```

3. **Create a Python virtual environment**  
```bash python -m venv venv```

4. **Activate the virtual environment**  
- On **Windows**:  
  ```
  env\Scripts\activate
  ```  
- On **macOS/Linux**:  
  ```
  source env/bin/activate
  ```

5. **Install the required dependencies**  
```bash pip install -r requirements.txt```


---

## 📓 Task 1 & 2: Environment Setup, EDA, and Cleaning

- Initialize the repository with `.gitignore` and GitHub Actions CI for environment consistency.  
- Profile, clean, and analyze solar datasets from each country independently using the EDA notebooks.  
- Generate reports of missing data, outliers, time series patterns, and correlations.

---

## 📊 Task 3: Cross-Country Solar Potential Comparison

**Branch:** `compare-countries`  
**Notebook:** `compare_countries.ipynb`

- Objective: Synthesize cleaned datasets from Benin, Sierra Leone, and Togo.  
- Load cleaned CSVs from `data/benin_clean.csv`, `data/sierra_leone_clean.csv`, and `data/togo_clean.csv`.  
- Visualize boxplots of GHI, DNI, and DHI side-by-side, colored by country for comparison.  
- Summarize statistical metrics (mean, median, standard deviation) across countries.  
- Perform one-way ANOVA or Kruskal-Wallis tests on GHI values to assess significance; report p-values.  
- Highlight key findings on solar irradiance potential and country variations.  
- Provide a visual ranking of countries by average GHI.  

---

## ⚙️ Continuous Integration (CI)

- Automated GitHub Actions workflows install dependencies and validate the environment on every push and pull request.  
- Includes unit test runs and static code checks (if implemented).

---

## 🚀 Getting Help

For any issues or questions, please open an issue on the GitHub repository or contact the maintainer via project emails or discussions.

---


Thank you for exploring the Solar Challenge Week 0 project! 🌞
