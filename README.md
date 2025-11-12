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

The primary goal is to handle solar datasets across several countries, perform exploratory data analysis, and compare solar potential across regions to inform energy strategies.

---

## 🛠 Features

- Python virtual environment setup and dependency management  
- Data profiling, cleaning, and exploratory data analysis (EDA) for multiple countries  
- Cross-country solar data comparison with statistical testing  
- Continuous integration with GitHub Actions for automated environment validation

---

## Time Series Analysis
- Plot line or bar charts of `GHI`, `DNI`, `DHI`, `Tamb` versus `Timestamp`.
- Observe:
  - Monthly patterns
  - Daily trends
  - Anomalies, e.g., peaks in solar irradiance or temperature fluctuations.

---

## Cleaning Impact
- Compare pre/post-cleaning averages for sensors:
```python
df_cleaned.groupby('cleaning_flag')[['ModA', 'ModB']].mean().plot()
```

---

## Correlation & Relationship Analysis
- Heatmap of correlations between solar and sensor data:
```python
import seaborn as sns
sns.heatmap(df_cleaned[['GHI', 'DNI', 'DHI', 'TModA', 'TModB']].corr(), annot=True)
```
- Scatter plots for relationships:
  - `WS`, `WSgust`, `WD` vs. `GHI`
  - `RH` vs. `Tamb`
  - `RH` vs. `GHI`

---

## Wind & Distribution Analysis
- Wind rose or radial bar plot for `WS` / `WD`.
- Histograms for `GHI` and another variable (e.g., `WS`):
```python
df_cleaned['GHI'].hist(bins=20)
df_cleaned['WS'].hist(bins=20)
```

---

## Temperature Analysis
- Examine how `RH` influences temperature (`Tamb`) and solar radiation (`GHI`).

---

## Bubble Chart
- Plot `GHI` vs. `Tamb` with bubble size representing `RH` or `BP`:
```python
import matplotlib.pyplot as plt

plt.scatter(df_cleaned['Tamb'], df_cleaned['GHI'], 
            s=df_cleaned['RH']*0.5, alpha=0.5)
plt.xlabel('Tamb')
plt.ylabel('GHI')
plt.title('GHI vs Tamb (Bubble size = RH)')
plt.show()
```

---

**Notes**
- All data processing and cleaning should be reproducible using the provided scripts.
- Avoid committing raw or cleaned CSV files; keep `data/
