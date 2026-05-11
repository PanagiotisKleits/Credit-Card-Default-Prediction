# Credit Card Default Prediction

Binary classification on the UCI Credit Card Dataset using a Hybrid CNN, XGBoost and Logistic Regression with 5-fold Cross-Validation.

## Dataset

[UCI Credit Card Dataset](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset) — 30,000 credit card clients from a Taiwanese bank (April– September 2005).

Features are split into two categories:
- **Static**: LIMIT_BAL, SEX, EDUCATION, MARRIAGE, AGE
- **Temporal**: Payment status, bill amounts and payment amounts over 6 months

**Target**: Whether the client will default next month (1) or not (0) — 22.1% default rate.

## Models

| Model | Description 

| Logistic Regression | Linear baseline 
| XGBoost | Ensemble baseline (500 estimators, early stopping) 
| Hybrid CNN | Conv1D for temporal features + Dense for static features

## Results

**5-fold Cross-Validation:**

| Model | CV Mean AUC | Std 

| Logistic Regression | 0.726 | ±0.012 
| Hybrid CNN | 0.774 | ±0.011 
| XGBoost | 0.783 | ±0.012

**Test Set:**

| Model | AUC | Somer's D 

| Logistic Regression | 0.709 | 0.419
| Hybrid CNN | 0.770 | 0.540 
| XGBoost | 0.783 | 0.566 

## Usage

1. Download the dataset from the link above and place it as `UCI_Credit_Card.csv`
2. Open `CNN_.ipynb` in Google Colab or Jupyter Notebook
3. Run all cells sequentially
