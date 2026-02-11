# Preprocessing Report – Customer Churn Prediction

## 1. Data Overview
Dataset contains 500 customer records with churn labels (0 = No, 1 = Yes).

## 2. Data Cleaning
- Removed CustomerID column (identifier, no predictive value)
- Verified no missing values
- Checked data types and converted boolean columns to integers

## 3. Categorical Encoding
Applied One-Hot Encoding to:
- Contract
- PaymentMethod
- PaperlessBilling

Reason:
Machine learning models require numerical input.

Used:
pd.get_dummies(drop_first=True)

## 4. Feature Scaling
Applied StandardScaler to all numerical features.

Reason:
Logistic Regression performs better when features are standardized.

## 5. Train-Test Split
Split data:
- 80% Training
- 20% Testing
Random State = 42 for reproducibility

## 6. Class Imbalance Handling
Used class_weight="balanced" in Logistic Regression to handle minority churn class.
