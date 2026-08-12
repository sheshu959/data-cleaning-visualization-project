# Data Cleaning & Visualization Project

Intern task: work on a raw dataset to clean, process, and visualize insights.

## Overview

A synthetic retail sales dataset (1,225 raw records) was cleaned and analyzed using
Pandas, Matplotlib, and Seaborn. The raw data intentionally contains the kind of
issues real exports have: missing values, duplicate rows, inconsistent text
formatting, mixed date formats, and price/quantity outliers.

## Repo structure

```
data/
  raw_sales_data.csv          # original raw dataset (1,225 rows)
  cleaned_sales_data.csv      # cleaned, analysis-ready dataset (1,200 rows)
notebook/
  Data_Cleaning_Visualization_Project.ipynb   # full, executed notebook
report/
  Data_Cleaning_Visualization_Report.docx     # written report / summary
dashboard/
  dashboard.png               # final 6-panel visualization dashboard
cleaning_log.txt              # step-by-step log of cleaning operations
```

## What was done

- **Standardized text fields** — normalized inconsistent Category casing/spacing
- **Parsed mixed date formats** (`YYYY-MM-DD`, `DD/MM/YYYY`, `MM-DD-YYYY`) into one consistent format
- **Removed duplicates** — 25 exact duplicate order records
- **Handled missing values** — 204 values imputed (median-per-category for price, mode/median/"Unknown" for the rest)
- **Handled outliers** — IQR method, computed **per category** for price (categories have very different natural price ranges)
- **Visualized** monthly revenue trend, revenue by category, order share by region, price distribution, payment method breakdown, and ratings by category

## Key findings

- Electronics drives the largest share of revenue despite not having the most orders
- North and South regions each account for ~26% of orders
- Cash on Delivery and Credit Card are the most common payment methods
- Median customer rating sits around 4.0/5 across all categories

## Tools

Python · Pandas · NumPy · Matplotlib · Seaborn · Jupyter
