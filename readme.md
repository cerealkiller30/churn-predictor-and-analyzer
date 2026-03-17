# Customer Churn Prediction (wip)

## Overview
A machine learning project to predict customer churn for a travel/airline 
company. The goal is to identify customers likely to leave.

(Still a work in progress. Therefore, **this repo still has the previous model files** which will be removed once completed.)

## Dataset
Airline customer dataset with ~950 rows and 8 features.
**Target:** Whether a customer churned or not (binary)

## What's Been Done So Far
- x Exploratory Data Analysis
- x Preprocessing (encoding...(wip))

## Observations from EDA
- Dataset has a **23.5% churn rate** — (which needs to be handled likely by SMOTE or CrossValidation to overcome class imbalance)
- **FrequentFlyer** and **AnnualIncomeClass** appear to be the strongest 
  predictors from class vs churn analysis

## Setup 
pip install -r requirements.txt
[Will be updated once notebooks are complete]

## Tech Stack
Python, Pandas, NumPy, Scikit-learn, XGBoost, 
Matplotlib, Seaborn, Imbalanced-learn

*Will update with model results and key findings once modeling is complete.*
