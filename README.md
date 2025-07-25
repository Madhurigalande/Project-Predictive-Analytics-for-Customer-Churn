🏦 Bank Customer Churn Prediction 
📌 Problem Statement
Predict whether a customer will exit the bank (churn) based on their demographic, account, and transaction-related data.

🎯 Objectives
Predict customer churn using machine learning models.
Analyze key factors that influence customer churn.
Evaluate and compare models using accuracy, precision, recall, and F1-score.
Recommend actions for proactive customer retention.

📊 Dataset Overview
Features include age, balance, tenure, salary, geography, credit card status, and more.
Contains class imbalance (more non-churn than churn).
Includes both categorical and numerical data.

🧹 Data Preprocessing
Handled missing values (mode for categorical, 0 for numerical).
Encoded categorical variables using one-hot encoding.
Split into training and test datasets (80/20).

📈 Exploratory Data Analysis (EDA)
Most customers are from France.
Majority have 1–2 products, are aged 30–40, and have similar salary distribution across gender.

Higher churn observed in:
Inactive members
Customers with short tenure
Customers aged above 50
Customers with 4 products and low salary

🤖 Models Used
Logistic Regression
Decision Tree
Random Forest
Naive Bayes
K-Nearest Neighbors (KNN)

🏁 Model Performance
All models reached ~79% accuracy.
Random Forest offered balanced precision-recall and is suitable for deployment.
Decision Tree is interpretable but prone to overfitting.
Naive Bayes is fast but makes naive assumptions.
KNN accuracy was ~76% and needs tuning.

🚀 Future Improvements
Try advanced models (e.g., XGBoost, LightGBM).

Apply PCA/LDA for feature engineering.

Handle class imbalance with SMOTE or weighted loss.

📌 Final Recommendation
Use Random Forest for deployment due to its performance, interpretability, and generalization ability.

