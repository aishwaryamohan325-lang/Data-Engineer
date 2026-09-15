# Sales Data Analysis

Exploratory analysis of **1,000 sales orders** using Python, Pandas, Matplotlib and Seaborn.

## Objective

Clean inconsistent sales records and explore category revenue, city order volume, payment methods and average order value.

## Files

- [Analysis notebook](Sales-Data-Analysis.ipynb): cleaning steps, seven visualizations and findings.
- [Source dataset](salesdataset.csv): the 12-column input used by the notebook.
- [Dependencies](requirements.txt): packages for running locally.

## Approach

1. Inspect column types, missing values and sample records.
2. Standardize age values and parse mixed date formats.
3. Fill missing prices with the median within each category; label missing categorical values as `Unknown` and retain missing ratings.
4. Check exact duplicates and derive `Total_Sale` and `Order_Month`.
5. Compare revenue, order volume, payment preferences and distributions.

## Findings in the notebook

- Clothing has the highest calculated category revenue.
- Lahore has the highest order count: 191.
- Cash and Card account for 33.4% and 32.9% of orders; 16.6% have unknown payment methods.

These findings describe the supplied dataset. Price imputation affects revenue estimates, and product/category mismatches remain a data-quality limitation. The dataset's source and currency are not documented in this repository.

## Run locally

From this folder:

```bash
python -m pip install -r requirements.txt
jupyter notebook Sales-Data-Analysis.ipynb
```

Keep `salesdataset.csv` beside the notebook and run the cells in order. For Google Colab, open the notebook and upload the CSV into the runtime first.

## Discussion points

- Why use a category-level median for missing prices?
- How does retaining missing ratings affect interpretation?
- How would validating product/category mappings change the analysis?
- How could the derived month column support a time-series extension?

[Back to portfolio](../README.md)
