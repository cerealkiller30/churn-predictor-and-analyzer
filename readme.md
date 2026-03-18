# Customer Churn Prediction and Analysis

## Overview
An end-to-end machine learning project to predict customer churn for a 
travel/airline company. Covers the full pipeline — EDA, preprocessing, 
model comparison, and SHAP-based interpretation.

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
pip install -r requirements.txt
```
Run notebooks in order: EDA -> PREPROCESS -> MODEL -> SHAP

## Tech Stack
Python, Pandas, NumPy, Scikit-learn, XGBoost, SHAP,
Matplotlib, Seaborn, Imbalanced-learn
