# Customer Churn Prediction

## Overview
An end-to-end machine learning project to predict customer churn for a 
travel/airline company. Covers the full pipeline — EDA, preprocessing, 
model comparison, and SHAP-based interpretation.
A machine learning project to predict customer churn for a travel/airline 
company. The goal is to identify customers likely to leave.

(Still a work in progress. Therefore, **this repo still has the previous model files** which will be removed once completed.)

## Dataset
Airline customer dataset with  ~950 rows and 8 features.

**Target:** Whether a customer churned or not (binary — 76.5% No Churn, 23.5% Churn)

**Features:** FrequentFlyer, AnnualIncomeClass, AccountSyncedToSocialMedia,
BookedHotelOrNot, ServicesOpted, Age

## Results
| Model | AUC-ROC | F1 (Class 1) | Recall (Class 1) | Log Loss |
|---|---|---|---|---|
| XGBoost (Final) | 0.9632 | 0.8052 | 0.9118 | 0.2274 |
| Random Forest | 0.9590 | 0.8205 | 0.9412 | 0.4716 |
| Logistic Regression | 0.8612 | 0.6667 | 0.8235 | 0.4762 |

XGBoost selected as final model based on highest AUC-ROC and lowest Log Loss.

## Key Findings
- **FrequentFlyer** and **AnnualIncomeClass** are the strongest churn drivers according to SHAP analysis
- Middle income customers are strongly pushed towards no churn (SHAP: -2.21)
- Frequent flyers push strongly toward churn (SHAP: +1.54)
- Model blind spot: young middle-income customers with high service usage 
  fall outside the usual churn profile

## Setup
```bash
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
```
Run notebooks in order: EDA -> PREPROCESS -> MODEL -> SHAP
[Will be updated once notebooks are complete]

## Tech Stack
Python, Pandas, NumPy, Scikit-learn, XGBoost, SHAP,
Matplotlib, Seaborn, Imbalanced-learn

*Will update with model results and key findings once modeling is complete.*
