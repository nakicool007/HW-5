# Homework 5 - Decision Trees and Regression

**Name:** Nakul Kumbria  
**GitHub:** nakicool007

This notebook contains my solutions for decision trees on the Acute Inflammations data and regression on the Communities and Crime data.

## Files

- `notebook/Kumbria_Nakul_HW5.ipynb`: code, explanations, plots, and saved outputs.
- `data/diagnosis.data` and `data/diagnosis.names`: Acute Inflammations data and description.
- `data/communities.data` and `data/communities.names`: Communities and Crime data and description.
- `docs/jupyter-notebook/Kumbria_Nakul_HW5.pdf`: exported notebook.
- `requirements.txt`: Python packages needed to run the notebook.

## What I did

1. Fit a decision tree on all 120 Acute Inflammations records, plotted it, wrote IF-THEN rules, and applied cost-complexity pruning.
2. Split Communities and Crime into the first 1495 rows for training and the remaining 499 for testing. I removed five nonpredictive columns and filled missing predictors with training-set medians.
3. Plotted feature correlations and the 11 features with the highest coefficient of variation.
4. Fit least squares, ridge, LASSO with and without standardization, PCR, and L1-regularized XGBoost. I used five-fold cross-validation for tuning and test MSE to compare the models. Preprocessing was fitted inside each tuning fold.

## Running the notebook

Use Python 3.10 or newer. From the project folder, run:

```powershell
python -m venv .venv
.venv\Scripts\python -m pip install -r requirements.txt
.venv\Scripts\python -m jupyterlab
```

Open `notebook/Kumbria_Nakul_HW5.ipynb` and run all cells in order. The data is already included, and all imports are in the first code cell. Cross-validation may take a few minutes.

To run it from the terminal and save the outputs:

```powershell
.venv\Scripts\python -m nbconvert --to notebook --execute --inplace --ExecutePreprocessor.timeout=600 notebook/Kumbria_Nakul_HW5.ipynb
```

## Data sources

- [Acute Inflammations - UCI](https://archive.ics.uci.edu/ml/datasets/Acute+Inflammations)
- [Communities and Crime - UCI](https://archive.ics.uci.edu/ml/datasets/Communities+and+Crime)

The `.names` files contain the feature descriptions. Keep the data, notebook, and PDF in the repository; local environments and caches are ignored.
