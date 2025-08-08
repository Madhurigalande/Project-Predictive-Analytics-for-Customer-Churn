# Predictive Analysis for Customer Churn

## 📌 Problem Statement
Predict whether a customer will exit the bank (churn) based on their demographic, account, and transaction-related data.

---

## 🎯 Objectives

- Predict customer churn using machine learning models.
- Analyze key factors that influence customer churn.
- Evaluate and compare models using **Accuracy**, **Precision**, **Recall**, and **F1-score**.
- Recommend actions for proactive customer retention.

---

## 📊 Dataset Overview

- Includes **demographic**, **account**, and **transactional** features:
  - `Age`, `Balance`, `Tenure`, `EstimatedSalary`, `Geography`, `Gender`, `HasCrCard`, `IsActiveMember`, `NumOfProducts`, etc.
- Dataset contains **class imbalance** (more non-churned than churned customers).
- Mix of **categorical** and **numerical** variables.

---

## 🧹 Data Preprocessing

- **Missing Values**:
  - Categorical: Imputed using **mode**.
  - Numerical: Imputed using **0** or appropriate statistical values.
- **Categorical Encoding**:
  - Applied **One-Hot Encoding** for `Geography` and `Gender`.
- **Data Splitting**:
  - Split into **training (80%)** and **testing (20%)** sets.

---

## 📈 Exploratory Data Analysis (EDA)

- Most customers are from **France**.
- Majority have **1–2 products**, aged **30–40**, and **similar salary distribution** across genders.
  
### Churn is higher among:
- **Inactive members**
- Customers with **short tenure**
- Customers aged **above 50**
- Customers with **4 products** and **low salary**

---

## 🤖 Models Used

| Model              | Notes                                                 |
|-------------------|--------------------------------------------------------|
| Logistic Regression | Simple baseline, interpretable results               |
| Decision Tree       | Clear decision paths, prone to **overfitting**       |
| Random Forest       | **Best performance**, good generalization            |
| Naive Bayes         | Very fast, assumes feature independence              |
| K-Nearest Neighbors | Sensitive to feature scaling, needs parameter tuning |

---

## 🏁 Model Performance

- **Overall Accuracy**: ~**79%** for most models.
- **Random Forest**:
  - **Best trade-off** between **precision** and **recall**.
  - Chosen for **deployment**.
- **Decision Tree**:
  - Interpretable but may **overfit** on training data.
- **Naive Bayes**:
  - Fast and simple, but **naive assumptions** may hurt performance.
- **KNN**:
  - Accuracy ~**76%**, sensitive to `K` and distance metrics.

---

## 🚀 Future Improvements

- Use advanced models like **XGBoost**, **LightGBM** for better performance.
- Apply **PCA** or **LDA** for **feature engineering** and **dimensionality reduction**.
- Handle **class imbalance** with:
  - **SMOTE (Synthetic Minority Over-sampling Technique)**
  - **Class-weighted loss functions**

---

## 📌 Final Recommendation

Deploy the **Random Forest** model due to:
- Strong and balanced performance.
- Good generalization on unseen data.
- Better interpretability compared to black-box models.

---

