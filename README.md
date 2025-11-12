# ☀️ Solar Challenge Week 0

A Python-based project for the Solar Challenge Week 0 task.  
This repository contains all code, dependencies, and setup instructions needed to reproduce and run the environment locally.

---

## 📦 Project Overview

This project is part of the **Solar Challenge** initiative.  
It demonstrates environment setup, dependency management, and reproducible development practices using Python virtual environments.

---

## 🧩 Steps to Reproduce the Environment

1. **Clone the repository**
   ```bash
   git clone https://github.com/msultan001/solar-challenge-week0.git
   ```

2. **Navigate into the project directory**
   ```bash
   cd solar-challenge-week0
   ```

3. **Create a virtual environment**
   ```bash
   python -m venv env
   ```

4. **Activate the virtual environment**
   - **Windows**
     ```bash
     env\Scripts\activate
     ```
   - **macOS/Linux**
     ```bash
     source env/bin/activate
     ```

5. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```


---

## 📓 Notebooks Description

- **Benin, Sierra Leone, Togo EDA notebooks** (`benin_eda.ipynb`, etc.): Perform exploratory data analysis, cleaning, and visualization on country-specific solar datasets.
- **compare_countries.ipynb**: Synthesizes cleaned datasets from Benin, Sierra Leone, and Togo to analyze and compare solar potential across countries. Includes visualizations (boxplots, summary tables, and bar charts), statistical testing (ANOVA, Kruskal-Wallis), and key observations to highlight significant differences in solar metrics.


## 📁 Data Handling Notes

- The `data/` folder and all `.csv` files are excluded from version control via `.gitignore`.
- Cleaned CSV data files should never be committed to the repo.
- This keeps the repo lightweight and secure.

---

## 📝 Running Tests and Scripts

(Include instructions here for running any scripts or tests if applicable)

---

Thank you for participating in the Solar Challenge. 🚀



