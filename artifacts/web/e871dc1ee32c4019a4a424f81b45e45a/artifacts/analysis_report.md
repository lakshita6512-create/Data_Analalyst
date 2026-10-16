# Exploratory Data Analysis

- Rows: 5 before, 5 after transformations.
- Columns: 5.
- Exact duplicate rows removed: 0.

## Dashboard

Open [the interactive dashboard](analysis_dashboard.html) for summary cards, the full column profile, and cross-filtering charts.

## Findings

- Column 'id' is a unique identifier with no missing values.
- Column 'name' is categorical with all unique values, no missing.
- Column 'age' has 20% missing; numeric range 25-40, no outliers.
- Column 'city' has 20% missing; categorical, all unique, no outliers.
- Column 'salary' numeric, no missing, range 50000-90000.

## Transformations applied

- **age** — Impute missing ages with median to preserve distribution. (conversion: numeric; missing values: median; outliers: keep; rows removed: 0).
- **city** — Impute missing city with most frequent value. (conversion: category; missing values: mode; outliers: keep; rows removed: 0).
- **id** — Keep identifier as numeric. (conversion: numeric; missing values: keep; outliers: keep; rows removed: 0).
- **name** — Treat names as categorical for analysis. (conversion: category; missing values: keep; outliers: keep; rows removed: 0).
- **salary** — Ensure salary is numeric for calculations. (conversion: numeric; missing values: keep; outliers: keep; rows removed: 0).
- Duplicate handling: No duplicate rows detected in the sample.

## Chart downloads

- [What is the distribution of employee ages after imputation? (SVG)](charts/chart_01_histogram.svg) — Age is a key numeric variable; histogram shows spread.
- [Are there any salary outliers? (SVG)](charts/chart_02_box.svg) — Box plot visualizes salary range and potential outliers.
- [How many employees are in each city? (SVG)](charts/chart_03_bar.svg) — Bar chart summarizes categorical city counts.
- [Is there a relationship between age and salary? (SVG)](charts/chart_04_scatter.svg) — Scatter plot reveals correlation between age and salary.

No model was trained and no train/test split was created.
