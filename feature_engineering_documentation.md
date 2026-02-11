# Feature Engineering Documentation – Customer Churn

## 1. Encoding Strategy

### One-Hot Encoding
Applied to:
- Contract
- PaymentMethod
- PaperlessBilling

Reason:
No natural ordering between categories.

Example:
Contract_Month-to-Month
Contract_One Year
Contract_Two Year

---

## 2. Removed Features

### CustomerID
Reason:
Unique identifier, no predictive meaning.

---

## 3. Feature Scaling

Applied StandardScaler:
- Tenure
- MonthlyCharges
- TotalCharges
- SeniorCitizen

Reason:
Ensures all features contribute equally to model learning.

---

## 4. Model Comparison

Models Used:
- Logistic Regression
- Decision Tree
- Random Forest

Reason:
To compare linear vs non-linear performance.

---

## 5. Key Insights

- Model achieves ~94% accuracy.
- Recall for churn class improved using class_weight="balanced".
- Random Forest showed strong performance in detecting churn customers.
