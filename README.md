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
📊 Dashboard Insights & Interpretation
1. Overall Churn Rate

Suppose churn rate is 20% → This means 1 in 5 customers leave the bank.

Insight: This is a red flag compared to the industry average (normally 10–15%).

2. Churn by Segment

Age Group:

Highest churn in customers >50 years old.

Younger customers (20–30) show lower churn.

Action: Design loyalty benefits for senior customers.

Activity Status:

Inactive members churn 2x more than active ones.

Action: Run engagement campaigns, personalized offers, or push app usage.

Geography:

If Germany has the highest churn, explore regional service gaps.

Products Held:

Customers with 4 products show very high churn (possible dissatisfaction).

Action: Review cross-sell strategy, ensure not overloading customers.

3. Financial Risk (Revenue at Risk)

Example: If churned customers hold an average balance of $80,000, and 2,000 customers churn →
Revenue at Risk = $160M

Action: Prioritize high-balance churn-prone customers for retention.

4. Model KPIs (Random Forest Chosen)

Accuracy = 79%

Recall = 72% (good, since recall ensures fewer missed churners)

Precision = 65% (means some false alarms exist, but that’s okay if recall is high).

Action: Use the model to identify high-risk customers and trigger retention offers.

5. Retention Strategy KPI

High-Risk Customers Identified = 2,500 (e.g., inactive, >50 years, 4 products).

Potential savings: If even 30% of them are retained, the bank saves $48M+ in balances.

📝 Storyline for Presentation (Executive Style)

Problem: Customer churn is high (20%), risking millions in deposits.

Key Findings:

Older, inactive, and high-product customers are at highest risk.

Germany shows regional churn concentration.

Model Results: Random Forest predicts churn with 79% accuracy, recall is strong.

Business Impact: ~$160M deposits at risk.

Action Plan:

Target high-risk customers with retention campaigns.

Improve engagement for inactive members.

Review cross-sell strategy to reduce dissatisfaction.

Future Monitoring: Track churn rate monthly, compare with campaign ROI in Tableau.

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

