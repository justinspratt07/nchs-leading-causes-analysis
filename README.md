# NCHS Leading Causes of Death Analysis

This project applies a supervised machine-learning workflow to the CDC's
**NCHS - Leading Causes of Death: United States** dataset. A Decision Tree
classifier predicts the cause-of-death category from year, state, number of
deaths, and age-adjusted death rate.

## Analysis workflow

- Inspect dataset structure, class distributions, and missing values.
- Remove the aggregate `All causes` category from the prediction target.
- One-hot encode state while passing numeric features through the pipeline.
- Preserve class balance with a stratified train/test split.
- Train a Decision Tree classifier using Gini impurity.
- Evaluate training and test accuracy, the classification report, confusion
  matrix, feature importance, and the model's top decision levels.

## Repository structure

```text
notebooks/
  nchs_decision_tree_analysis.ipynb
requirements.txt
```

## Dataset

Download the CSV from the
[CDC data portal](https://data.cdc.gov/National-Center-for-Health-Statistics/NCHS-Leading-Causes-of-Death-United-States/bi63-dtpu)
and save it as:

```text
NCHS_-_Leading_Causes_of_Death__United_States.csv
```

Place the CSV in the repository root before running the notebook. The dataset
is not duplicated in this repository; it remains subject to the source's terms
and documentation.

## Setup

```bash
python -m venv .venv
python -m pip install -r requirements.txt
jupyter notebook notebooks/nchs_decision_tree_analysis.ipynb
```

## Tools

Python, pandas, scikit-learn, Matplotlib, and Jupyter Notebook.

## Author

[Justin Spratt](https://github.com/justinspratt07)
