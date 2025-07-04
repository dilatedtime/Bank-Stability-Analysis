# Bank Stability Analysis (2005–2024)

A panel-data framework for assessing financial stability of Indian Scheduled Commercial Banks using Z-score, NPAs, liquidity measures, and key risk indicators.

## Overview

This repository implements a comprehensive stability analysis pipeline for Indian banks (2005–2024). It covers data collection from RBI and annual reports, metric construction (Z-score, NPAs, CAR, LDR, ALM Gap, income diversification), fixed-effects panel regression, and visual trend analysis.

## Key Features

* **Data Preparation**: Scripts to compile, clean, and merge RBI STRBI and bank annual-report datasets.
* **Metric Construction**: Functions to compute Z-score, Net & Gross NPA ratios, Capital Adequacy Ratio, Loan-to-Deposit Ratio, ALM Gap, ROA, and Non-Interest Income Ratio.
* **Econometric Modeling**: Fixed-effects panel regression notebooks quantifying impacts of asset quality, capitalization, funding structure, and income diversification on stability.
* **Visualization & Diagnostics**: Notebooks for trend plots, cross-bank comparisons (public/private/foreign), and tests for heteroskedasticity and autocorrelation.

## Data Description

* **Source**: RBI Statistical Tables Relating to Banks in India (STRBI), RBI DBIE, and bank annual reports.
* **Coverage**: Scheduled Commercial Banks’ annual balance sheets and ratios (2005–2024).
* **Variables**: Net Profit, Total Assets, Equity, Net & Gross NPAs, CAR, NIM, ROA, LDR, ALM Gap, Non-Interest Income.

## Data Preprocessing

1. **Compile**: Aggregate key fields from RBI Excel tables and PDF reports.
2. **Clean**: Handle missing values, standardize definitions, adjust monetary units to constant rupees.
3. **Merge**: Create unified panel dataset indexed by bank and financial year.

## Modeling Approaches & Hyperparameters

* **Dependent Variable**: Z-score = ln((ROA + Equity/Total Assets) / SD(ROA)).
* **Independent Variables**: Net NPA Ratio, CAR, LDR, ALM Gap, Non-Interest Income Ratio.
* **Model**: Fixed-effects panel regression controlling for bank-specific time-invariant effects.

## Evaluation Metrics

* **Regression Coefficients**: Significance, sign, and magnitude of explanatory variables.
* **Diagnostics**: Heteroskedasticity (Breusch-Pagan), autocorrelation (Durbin-Watson), and goodness-of-fit (R²).

## Execution

```bash
git clone https://github.com/your-org/bank-stability-analysis.git
cd bank-stability-analysis
pip install -r requirements.txt
jupyter notebook 01_data_prep.ipynb 02_metrics.ipynb 03_panel_model.ipynb 04_visualization.ipynb
```

## Results & Conclusion

* Identified key drivers of bank stability: capital buffers, asset quality, funding structure, and income diversification.
* Documented temporal trends and cross-bank variations in resilience.
* Insights support macroprudential policy and bank risk-management strategies.
