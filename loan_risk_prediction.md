# Capstone Project: Forecast Loan Default Risk Using Past Records

## Project Overview
In this capstone project, you will build a **loan default risk prediction model** using a simple, beginner-friendly dataset.  
The project is designed to help you understand how credit risk models work in practice, without overwhelming data complexity.

This is a **binary classification** problem focused on clarity, correctness, and explainability.

---

## Problem Statement
Given historical loan application data, predict whether a borrower is **high risk or low risk**.

This task simulates a real-world credit decision problem commonly used in banks and fintech companies.

---

## Recommended Dataset (Easy & Clean)

**Dataset link:**  
https://www.kaggle.com/datasets/altruistdelhite04/loan-prediction-problem-dataset

**Why this dataset is recommended**
- Small dataset (~600 records)
- Simple and intuitive features
- Minimal preprocessing required
- Ideal for first-time credit risk projects

---

## Dataset Structure

### Input Features

**Demographics**
- Gender  
- Marital Status  
- Education  
- Number of Dependents  

**Financial Information**
- Applicant Income  
- Coapplicant Income  
- Loan Amount  
- Loan Amount Term  

**Credit Behavior**
- Credit History (0 = bad, 1 = good)  

---

### Target Variable
- `Loan_Status = Y` → Low risk (loan approved)  
- `Loan_Status = N` → High risk (loan rejected)  

> Note: In this educational project, loan rejection is treated as a **proxy for default risk**, which is common in teaching and practice.

---

## Project Workflow

### 1. Data Understanding
- Load and inspect the dataset  
- Identify missing values  
- Check class balance  
- Understand the meaning of each feature  

---

### 2. Data Preprocessing
- Handle missing values (median or mode)  
- Encode categorical variables  
- Scale numerical features (optional)  

---

### 3. Feature Engineering
- Total income (applicant + coapplicant)  
- Income-to-loan ratio  
- Loan amount per dependent  

---

### 4. Modeling

**Baseline Model**
- Logistic Regression (highly interpretable)

**Optional Models**
- Decision Tree  
- Random Forest  

---

### 5. Model Evaluation
- Accuracy  
- Precision and Recall  
- Confusion Matrix  
- ROC-AUC  

---

### 6. Interpretation
- Feature coefficients (Logistic Regression)  
- Feature importance (Tree-based models)  
- Business interpretation of risk factors  

---

## Final Deliverables
- Cleaned dataset  
- Jupyter Notebook with full ML pipeline  
- Model evaluation results  
- Clear explanation of credit risk drivers  

---

## Learning Outcomes
By completing this project, you will learn how to:
- Work with real-world financial data  
- Build and evaluate binary classification models  
- Interpret credit risk predictions  
- Communicate results in simple business terms  

This project is an excellent **starting point for credit risk modeling** before moving to larger datasets.
