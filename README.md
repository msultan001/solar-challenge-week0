## 📓 Notebooks Description

- **Benin, Sierra Leone, Togo EDA notebooks** (`benin_eda.ipynb`, etc.): Perform exploratory data analysis, cleaning, and visualization on country-specific solar datasets.

- **Task 3: Cross-Country Solar Potential Comparison (`compare_countries.ipynb`)**  
  **Branch:** `compare-countries`  

  **Objective:** Synthesize the cleaned datasets from Benin, Sierra Leone, and Togo to identify relative solar potential and key differences across countries.

  - Load cleaned CSVs from `data/benin_clean.csv`, `data/sierra_leone_clean.csv`, and `data/togo_clean.csv`.
  - Generate boxplots of GHI, DNI, and DHI side-by-side, colored by country.
  - Produce a summary table comparing mean, median, and standard deviation of GHI, DNI, and DHI.
  - Run statistical tests (one-way ANOVA or Kruskal–Wallis) on GHI values to assess significance; report p-values.
  - Summarize key observations highlighting countries with highest median GHI, variability, and statistical significance of differences.
  - Bonus: Visual summary bar chart ranking countries by average GHI.

