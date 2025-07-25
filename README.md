
# 🏦 Loan Approval Prediction – Jupyter Notebook Summary

## 📘 Project Title
**Loans_ML_Project**

---

## 🎯 Objective
Build a machine learning model to predict whether a loan will be approved or denied (`loan_status`), using various applicant and financial information.

---

## 📊 Dataset Overview

### 📑 Data Dictionary

| Column               | Description                                |
|----------------------|--------------------------------------------|
| `loan_id`            | Unique loan ID                             |
| `gender`             | Applicant gender (Male/Female)             |
| `married`            | Marital status (Yes/No)                    |
| `dependents`         | Number of dependents (0,1,2,3+)            |
| `education`          | Graduate/Not Graduate                      |
| `self_employed`      | Employment type                            |
| `applicant_income`   | Applicant’s monthly income                 |
| `coapplicant_income` | Coapplicant’s income                       |
| `loan_amount`        | Requested loan amount                      |
| `loan_amount_term`   | Term (duration) of loan in months          |
| `credit_history`     | Credit history meets guidelines (1 = Yes)  |
| `property_area`      | Urban/Semiurban/Rural                      |
| `loan_status`        | Target variable: 1 = Approved, 0 = Denied  |

---

## 🧰 Workflow Steps

### 1. 📦 Importing Packages & Loading Data
- Used libraries like `pandas`, `numpy`, `matplotlib`, `seaborn`, `sklearn`.

### 2. 🔍 Data Exploration & Cleaning
- Checked for missing values, null counts, and inconsistencies.
- Visualized distributions and relationships (e.g., loan approval vs income).

### 3. 🧠 Feature Engineering
- Created new features:
  - `total_income` = applicant + coapplicant
  - `loan_to_income_ratio`
  - `income_per_person` = total_income / (1 + dependents)
  - `log_loan_amount` (to reduce skew)
- Applied log transformation and clipping to handle extreme values.

### 4. ⚙️ Preprocessing
- Imputed missing values
- Encoded categorical variables
- Scaled numeric features using `RobustScaler`
- Split dataset into training and testing sets

### 5. 🤖 Model Training
- Tried multiple models (e.g., Logistic Regression, Random Forest, etc.)
- Evaluated with metrics: Accuracy, Precision, Recall, F1-score
- Selected best-performing model

### 6. 📈 Evaluation
- Plotted confusion matrix and ROC curves
- Analyzed feature importances and error cases

---

## ✅ Key Learnings

- Real-world outliers (e.g., high incomes) may not be data errors but still hurt models.
- Log transforms + clipping are helpful for managing extreme values.
- Tree models (Random Forest) handle non-scaled data well; linear models (Logistic) need preprocessing.

---

## 🗂 File Structure

- `loan_prediction.ipynb` → Full notebook with analysis and model
- `README.md` → Project summary

---

## 🙋‍♂️ Author
Created by a data science learner working toward understanding real-world loan risk and model interpretability.

