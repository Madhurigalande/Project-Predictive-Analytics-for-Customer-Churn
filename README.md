# 🏦 Customer Churn Prediction

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Scikit-learn](https://img.shields.io/badge/ML-ScikitLearn-orange.svg)
![Tableau](https://img.shields.io/badge/Dashboard-Tableau%20%7C%20PowerBI-green.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)

---

## 📌 Problem Statement
Banks face significant financial loss when customers exit (churn).  
This project builds a **predictive machine learning model** to identify customers likely to churn, enabling proactive retention strategies.

---

## 🎯 Objectives
- Build ML models to **predict customer churn**.  
- Identify **key churn drivers** (demographic, account, and transaction factors).  
- Compare models using **Accuracy, Precision, Recall, and F1-score**.  
- Recommend **business actions** for customer retention.  

---

## 📊 Dataset Overview
- Features include:  
  - `Age`, `Balance`, `Tenure`, `EstimatedSalary`, `Geography`, `Gender`,  
  - `HasCrCard`, `IsActiveMember`, `NumOfProducts`, etc.  
- **Class imbalance**: More non-churned customers than churned.  
- Mix of **categorical** and **numerical** variables.  

---

## 🧹 Data Preprocessing
- **Missing Values**  
  - Numerical → Imputed with mean/0.  
  - Categorical → Mode imputation.  
- **Categorical Encoding** → One-Hot Encoding (`Geography`, `Gender`).  
- **Train-Test Split** → 80% training / 20% testing.  

---

## 📈 Exploratory Data Analysis
- Majority of customers are from **France**.  
- Most hold **1–2 products**, aged **30–40**.  
- Salary distribution is **similar across genders**.  

### 🔑 Key Findings
- Higher churn among:
  - **Inactive members**  
  - **Tenure < 3 years**  
  - **Age > 50 years**  
  - **4 products customers**  
  - **Low salary group**  
- Germany shows **highest churn rate**.  

---

## 🤖 Models Implemented
| Model                | Notes                                    |
|-----------------------|------------------------------------------|
| Logistic Regression   | Baseline, interpretable results          |
| Decision Tree         | Clear paths, prone to overfitting        |
| Random Forest         | ⭐ Best trade-off, strong performance     |
| Naive Bayes           | Very fast, weaker assumptions            |
| KNN                   | Needs tuning, sensitive to scaling       |

---

## 🏁 Model Performance
- **Accuracy**: ~79% (across models)  
- **Random Forest (chosen)**:  
  - Accuracy = **79%**  
  - Recall = **72%** ✅ (fewer missed churners)  
  - Precision = **65%** ⚠️ (some false positives, acceptable)  

✔️ **Random Forest chosen for deployment** due to best recall–precision trade-off.  

---

## 📊 Dashboard Insights
1. **Overall Churn Rate**: ~20% (higher than industry avg of 10–15%).  
2. **Churn by Segment**:  
   - Age > 50 → Highest churn.  
   - Inactive members → 2x more churn.  
   - Germany → Regional hotspot.  
   - 4 products → High dissatisfaction.  
3. **Financial Risk**:  
   - Avg balance per churned customer = **$80K**.  
   - If 2,000 churn → **$160M deposits at risk**.  
4. **Retention Strategy KPI**:  
   - 2,500 high-risk customers flagged.  
   - If 30% retained → **$48M+ savings**.  

---

## 📝 Business Storyline
- **Problem**: Churn (20%) puts ~$160M deposits at risk.  
- **Key Drivers**: Age > 50, inactivity, high products, Germany region.  
- **Solution**: Random Forest model predicts churn with strong recall.  
- **Action Plan**:  
  - Retention campaigns for high-risk customers.  
  - Engage inactive members via loyalty/benefits.  
  - Review cross-sell strategy to avoid dissatisfaction.  
- **Monitoring**: Track churn monthly in Tableau/PowerBI, measure ROI.  

---

## 🚀 Future Improvements
- Explore **XGBoost / LightGBM**.  
- Use **SMOTE / class-weighting** for imbalance handling.  
- Apply **PCA/LDA** for dimensionality reduction.  
- Deploy as **Flask / FastAPI API** for real-time scoring.  

---


