# Probability of Default (PD) Model – Credit Risk

## Project Overview

This project develops a Probability of Default (PD) model to estimate
the likelihood that a borrower will default on a loan.

The model uses traditional credit risk modelling techniques including:

- Optimal Binning
- Weight of Evidence (WOE)
- Information Value (IV)
- Logistic Regression
- AUC / Gini
- KS Statistic
- PD Calibration
- Decile Analysis

## Objective

The objective is to develop a transparent and interpretable PD model
suitable for credit risk analysis.

## Dataset

The dataset contains approximately 10,000 loan records with borrower,
credit and loan characteristics.

The target variable is:

- 0 = Non-default
- 1 = Default

Default is defined using delinquent and charged-off loan statuses.

## Methodology

### 1. Data Preparation
- Data cleaning
- Missing-value treatment
- Data type conversion
- Feature engineering
- Exploratory data analysis

### 2. Train-Test Split

The dataset was split into:

- 80% Training
- 20% Testing

Stratified sampling was used to preserve the default rate.

### 3. Optimal Binning

Optimal Binning was applied to numerical and categorical variables.

Information Value (IV) was used to assess predictive strength.

### 4. WOE Transformation

Variables were transformed using Weight of Evidence (WOE).

Binning was fitted only on the training dataset and the same
binning rules were applied to the test dataset.

### 5. Logistic Regression

A logistic regression model was developed using selected WOE-transformed
variables.

### 6. Model Validation

The model was evaluated using:

- AUC
- Gini
- KS Statistic
- Decile Analysis
- Calibration Plot

## Final Model Performance

| Metric | Train | Test |
|---|---:|---:|
| AUC | 0.820 | 0.795 |
| Gini | 0.640 | 0.590 |
| KS | 0.50 | 0.46 |

## Calibration

The calibration analysis showed that predicted PDs were broadly aligned
with observed default rates across risk deciles.

The highest-risk decile showed some underprediction of observed defaults.

## Key Features

The final model included variables such as:

- Credit Score
- DTI
- Delinquencies
- Credit Utilization
- Annual Income
- Credit History
- Interest Rate
- Employment Years
- Recent Inquiries
- Loan Amount
- Open Accounts
- Age

## Conclusion

The final PD model demonstrated good discrimination and reasonably good
calibration on the test dataset.

The relatively small difference between training and testing performance
suggests limited overfitting.
- Model monitoring
- Population Stability Index (PSI)
- Calibration monitoring
