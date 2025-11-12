# Benin Dataset Analysis

## Summary Statistics & Missing-Value Report
- Compute descriptive statistics for all numeric columns:
```python
df.describe()
```
- Count missing values per column:
```python
df.isna().sum()
```
- Identify columns with more than 5% null values and flag them for cleaning.

---

## Outlier Detection & Basic Cleaning
- Inspect missing values, outliers, or incorrect entries, especially in:
  - Solar radiation: `GHI`, `DNI`, `DHI`
  - Sensor readings: `ModA`, `ModB`
  - Wind data: `WS`, `WSgust`
- Compute Z-scores for key columns:
```python
from scipy.stats import zscore

columns = ['GHI', 'DNI', 'DHI', 'ModA', 'ModB', 'WS', 'WSgust']
df_outliers = flag_outliers_zscore(df, columns, threshold=3)
```
- Flag rows where `|Z| > 3` as outliers.
- Drop or impute missing values (e.g., median) in key columns:
```python
df_cleaned = clean_missing_values(df_outliers, columns)
```
- Export cleaned DataFrame (ensure `data/` is in `.gitignore`):
```python
df_cleaned.to_csv('data/benin_clean.csv', index=False)
```

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
