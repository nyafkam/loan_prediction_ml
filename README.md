
# 🏦 Loan Approval Prediction Project

## 🎯 Objective
This project aims to build a machine learning model that predicts whether a loan will be **approved (`loan_status = 1`)** or **denied (`loan_status = 0`)** based on applicant information.

---

## 📊 Dataset Overview

The dataset includes 13 columns:
- **Demographics**: `gender`, `married`, `dependents`, `education`
- **Financial info**: `applicant_income`, `coapplicant_income`, `loan_amount`, `loan_amount_term`, `credit_history`
- **Other context**: `self_employed`, `property_area`
- **Target variable**: `loan_status`

---

## 🛠️ Feature Engineering

New features were created to enhance model learning:

- `total_income`: Sum of applicant and coapplicant incomes
- `loan_to_income_ratio`: Ratio of loan amount to total income
- `log_loan_amount`: Log-transformed loan amount to reduce skew
- `income_per_person`: Adjusted income based on number of dependents
- `is_self_employed_or_low_credit`: Risk flag combining employment and credit history

---

## 🧪 Preprocessing Strategy

- **Log1p Transformations**: Applied to skewed features to compress large values
- **Lower Clipping**: Used after log-transform to suppress artificial low-end outliers
- **RobustScaler**: Used for features like `loan_amount_term` that aren’t highly skewed
- **Missing Values**: Handled appropriately per column using domain-aware strategies

---

## 🤖 Modeling Approach

- Multiple classification models were explored
- Evaluation metrics: accuracy, precision, recall, F1-score
- Final model selected based on its performance and ability to generalize

---

## 📈 Conclusion

This project balanced **real-world complexity** (like valid but extreme incomes) with **model robustness**, resulting in a thoughtful and effective prediction tool for loan approval decisions.

