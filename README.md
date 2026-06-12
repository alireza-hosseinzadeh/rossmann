# Rossmann Stores Sales and Customer Prediction

This repository contains a Python/Jupyter workflow for predicting Rossmann store sales and customer numbers. The project covers data cleaning, feature engineering, exploratory data analysis, and predictive modelling using classical regression models, tree-based models, boosting models, and an LSTM model.

## Project summary

Rossmann operates thousands of stores across several countries. Accurate forecasts of sales and customer numbers support staffing, inventory planning, promotion planning, and broader operational decisions.

The analysis uses Rossmann sales records and store-level information, supplemented with state mapping and weather data. The original sales data contain roughly one million records from 1,115 stores in Germany, covering 1 January 2013 to 31 July 2015.

## Repository structure

```text
rossmann-sales-prediction/
├── README.md
├── LICENSE
├── .gitignore
├── requirements.txt
├── environment.yml
├── notebooks/
│   └── Rossmann_Final.ipynb
├── reports/
│   └── Rossmann_report.pdf
└── data/
    ├── README.md
    ├── raw/
    │   └── .gitkeep
    └── processed/
        └── .gitkeep
```

## Data

The raw data are not included in this repository because they come from Kaggle and supplementary external sources. Download the data manually and place the files in `data/raw/`.

Expected data sources:

- Kaggle Rossmann Store Sales competition data
- Store-to-state mapping data
- German state-level weather data

The notebook may need small path edits if your local file names differ from those used in the original analysis.

## Methods

The workflow includes:

- missing-value and incorrect-record treatment;
- log transformation and feature engineering;
- sales-per-customer feature construction;
- time-based and event-based exploratory data analysis;
- categorical encoding and memory optimisation;
- model comparison using RMSE;
- models including Linear Regression, LASSO, Ridge, Elastic Net, Regression Tree, Random Forest, AdaBoost, XGBoost, LightGBM, and LSTM.

## Main findings

The report identifies promotions, holidays, competition-related features, store type, assortment, and temporal patterns as important drivers of Rossmann sales behaviour. XGBoost and LSTM are reported as strong predictive approaches, although the LSTM uses a different train/test setup and is less interpretable than the classical and tree-based models.

## Setup

### Option 1: Conda

```bash
conda env create -f environment.yml
conda activate rossmann-sales
python -m ipykernel install --user --name rossmann-sales --display-name "Python (rossmann-sales)"
jupyter lab
```

### Option 2: pip

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate

pip install -r requirements.txt
python -m ipykernel install --user --name rossmann-sales --display-name "Python (rossmann-sales)"
jupyter lab
```

## How to run

1. Clone the repository.
2. Download the raw datasets and place them in `data/raw/`.
3. Create the Python environment using either `environment.yml` or `requirements.txt`.
4. Open `notebooks/Rossmann_Final.ipynb` in JupyterLab.
5. Run the notebook cells in order.

## Notes

- Large raw data files, generated model files, cache folders, and notebook checkpoints are intentionally ignored by Git.
- The PDF report is included as a static summary of the analysis.
- The notebook was prepared as an applied data-science project and may require path adjustments depending on the local data layout.

## Suggested citation

Hosseinzadeh, A. Rossmann Stores Sales and Customer Prediction. Jupyter notebook and project report.
