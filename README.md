# Bank Stability Analysis

This repository studies liquidity and financial stability across Indian scheduled commercial banks. The notebooks combine balance-sheet, earnings, maturity-profile, off-balance-sheet, and ratio data, then test how liquidity measures relate to bank stability.

The analysis covers public, private, foreign, and aggregate bank groups. It uses panel regressions and measures such as the loan-to-deposit ratio, asset-liability maturity gaps, non-interest income, equity-to-assets ratio, return on assets, capital adequacy, non-performing assets, and a Z-score for stability.

## Files

| Path | Purpose |
| --- | --- |
| `LDR_ALM_NIIR_EAR_Ananlysis.ipynb` | Builds financial-stability measures and compares pooled, fixed-effects, and random-effects models |
| `LiquidityAnalysis.ipynb` | Constructs liquidity measures and tests their relationship with Z-scores and bank ratios |
| `Cleaned Dataset/Balance_Sheet.xlsx` | Cleaned balance-sheet data |
| `Cleaned Dataset/Earnings_Expenses.xlsx` | Earnings and expense data |
| `Cleaned Dataset/Maturity_Profile.xlsx` | Asset and liability maturity buckets |
| `Cleaned Dataset/OBS.xlsx` | Off-balance-sheet data |
| `Cleaned Dataset/Ratios_of_SCBs.xlsx` | Published banking ratios |

The notebooks use `pandas`, `numpy`, `matplotlib`, `seaborn`, `statsmodels`, `linearmodels`, `scipy`, and `scikit-learn`.

## Run the analysis

```bash
git clone https://github.com/dilatedtime/Bank-Stability-Analysis.git
cd Bank-Stability-Analysis
python -m venv .venv
python -m pip install jupyter pandas numpy matplotlib seaborn openpyxl statsmodels linearmodels scipy scikit-learn
jupyter notebook
```

Open either notebook and run the cells in order.

The notebooks still contain absolute Windows paths from the original working environment and refer to intermediate CSV files created during that work. The cleaned Excel files are included, but you will need to point the loading cells at `Cleaned Dataset/` and rerun the data-building cells before the full analysis can be reproduced on another computer.

This is an exploratory academic analysis. The saved regression output reflects the data preparation and model choices in the notebooks and should not be read as a current assessment of any bank.
