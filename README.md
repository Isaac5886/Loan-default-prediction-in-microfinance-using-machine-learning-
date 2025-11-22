# 🔍 Loan Default Prediction In Microfinance using Machine Learning

# 📌 Introduction
Loan default is a major risk in the financial industry. This project aims to build a machine learning model that predicts whether a loan applicant is likely to default, based on historical loan data. The goal is to help financial institutions make informed credit decisions.

# 📊 Dataset
- Source: [Kaggle - Loan Default Dataset](https://www.kaggle.com/datasets/nikhil1e9/loan-default)
- Contains demographic, financial, and loan-related information for applicants.

# 🎯 Objective
- Predict if a borrower will default on a loan.
- Create meaningful new features to improve prediction accuracy.
- Deploy the model using Streamlit for easy use.

---

# 🧠 Features & Feature Engineering

*Original Features:*  
- Loan ID, Age, Income, Loan Amount, Loan Term, etc.

*New Features Created:*  
1. *Loan to Income Ratio* = `LoanAmount / MonthlyIncome`  
2. *EMI (Estimated Monthly Installment)* = `(LoanAmount * InterestRate / 100) / LoanTerm_Months`  
3. *Loan Age Ratio* = `LoanAmount / Age`  
4. *Employment Duration* = `CurrentYear - YearOfEmploymentStart`
5. *Family Burden Index* = `Dependents / MonthlyIncome`

*Dropped Features:*  
- Loan ID (not useful for prediction)

---

# 📌 Feature Selection
- Used 5 methods:
  - L1 (Lasso)
  - RFE
  - Mutual Information
  - Random Forest Importance
  - SelectKBest

---

# 🤖 Models Used
- Logistic Regression  
- Decision Tree  
- Random Forest  
- XGBoost  
- CatBoost  
- LightGBM  
- SVM  
- K-Nearest Neighbors (KNN)

---

# ⚙️ Model Training & Evaluation
- Applied cross-validation
- Used GridSearchCV for hyperparameter tuning
- Evaluation Metrics: Accuracy, Precision, Recall, F1 Score

---

# 📈 Results
- XGBoost gave the best recall on Mutual Information features.
- Logistic Regression gave the best F1 on L1 feature set.
- Final model was chosen based on the business need (e.g., recall for reducing defaults).

---

# 🚀 Deployment
- Deployed with *Streamlit*.
- Users can input applicant details and get a prediction in real-time.

---

# 📚 Conclusion
This project demonstrates the application of machine learning in risk prediction for microfinance/loan institutions. With meaningful feature engineering and proper evaluation, the model can aid in minimizing loan default risks.

---

