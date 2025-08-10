@@
## Bulldozer Price Predictor (Regression)

This project builds a machine learning model to predict bulldozer sale prices using the Kaggle Bluebook for Bulldozers dataset.

- **Notebook**: `bulldozer-price-predictor-regression.ipynb`
- **Data source**: Kaggle Bluebook for Bulldozers competition
  ([overview](https://www.kaggle.com/competitions/bluebook-for-bulldozers/overview))

### Setup

1) Create and activate a Python virtual environment (Windows PowerShell):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2) Install dependencies:

```bash
pip install -r requirements.txt
```

### Data

- Download the dataset from Kaggle and place the CSV files under the `data/` directory.
- Note: Large datasets can make the repository very big and may exceed GitHub limits. Consider keeping large files out of the repo (e.g., upload a small sample only or host data elsewhere).

### Run

Open the notebook and run cells top-to-bottom:

```bash
jupyter notebook bulldozer-price-predictor-regression.ipynb
```

The notebook:
- Parses dates and engineers time-based features
- Encodes categorical features and imputes missing values
- Trains and tunes a `RandomForestRegressor`
- Generates predictions for the Kaggle test set (saved to `data/test_predictions.csv`)

### Notes

- Training can be computationally intensive. Consider reducing sample size or estimator count if needed.
- To reproduce results, ensure the same dataset versions and random seeds.
- If you want to exclude large files or local environments later, you can add a `.gitignore` file tailored to your needs.


