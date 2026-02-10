# Telecom-Churn-Case-Study
# Predicting Customer Churn in the Telecom Industry (Team 1A)

## What this project is📲
This project predicts customer churn (whether a customer leaves) for a telecom company using a real customer dataset. The goal is to identify high-risk customers early so the business can take action (discounts, service outreach, contract offers) before they cancel.

## Why it matters
Churn is expensive. Retaining existing customers is typically cheaper than acquiring new ones. A model that flags likely churners helps the company focus retention efforts where they matter most.

## Data📈
- Source: Public Kaggle telecom churn dataset
- Size: 7,043 customers
- Target: `Churn` (Yes/No)
- Features include:
  - Demographics (e.g., senior citizen, dependents)
  - Account info (contract type, payment method, tenure, charges)
  - Services (internet type, add-ons like tech support, streaming)

## Tools used ⚙️
- Python
- Jupyter Notebook
- pandas (data cleaning and transformation)
- numpy (numeric operations)
- matplotlib / seaborn (visualizations)
- scikit-learn (train/test split, preprocessing, modeling, metrics)
- imbalanced-learn (SMOTE oversampling)
- statsmodels (optional analysis / checks)

## What we did
1. Cleaned and prepared the dataset (handled missing/invalid values and converted data types).
2. Encoded categorical variables (one-hot encoding) and prepared the final modeling table.
3. Split data into training/testing sets (stratified split).
4. Built two classification models:
   - Logistic Regression (interpretable baseline)
   - Decision Tree Classifier (non-linear model)
5. Evaluated using accuracy, precision, recall, ROC-AUC, and confusion matrices.
6. Addressed class imbalance using SMOTE (trained models before and after SMOTE to compare tradeoffs).

## Results (high level)📚
- Logistic Regression performed best overall on the original dataset, with strong accuracy and ROC-AUC.
- Decision Tree captured non-linear patterns but tended to trade off precision/accuracy depending on balancing.
- After SMOTE, recall for churners improved significantly (the models caught more true churners), but accuracy dropped due to more false positives.

## Key insights
The strongest churn signals were:
- Tenure (short-tenure customers churn more)
- Contract type (month-to-month customers churn the most)
- Monthly charges / total charges
- Payment method (electronic check showed higher churn)
- Internet type (fiber optic showed higher churn)

## Recommendations
- Target month-to-month customers with incentives to switch to 1-year or 2-year contracts.
- Focus retention programs on customers with tenure < 12 months (highest-risk period).
- Investigate fiber optic customer experience and pricing (higher churn segment).
- Encourage auto-pay methods to reduce churn linked to payment friction.

## Files
- `Telecom Final Slides.pdf` — final presentation slides (compressed under 25MB)
- `ML Project Report (1).pdf` — full written report
- `Machine_learning_final_code.ipynb` — notebook (cleaning, EDA, modeling, evaluation)

## How to run⚡
1. Open `Machine_learning_final_code.ipynb` in Jupyter / VS Code.
2. Install dependencies (example):
   pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn statsmodels
3. Run cells top to bottom to reproduce preprocessing, models, and evaluation outputs.

## Notes / limitations
- The dataset is a snapshot (not time-series), so it doesn’t capture changes in customer behavior over time.
- The dataset lacks real operational variables like support-call history, complaint logs, or service outages.
- The project focuses on model performance metrics and business interpretation, not full cost/benefit or customer lifetime value optimization.

