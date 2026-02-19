# Course Project Documentation
## Project Title
**Build a Basic Classifier for Patient Readmission**

---

## 1. Project Description

Hospital readmissions within 30 days are widely used as a quality indicator in healthcare systems. Predicting readmission risk helps hospitals allocate resources, improve follow-up care, and reduce avoidable costs.

In this project, students will build a **basic machine learning classifier** that predicts **30-day patient readmission** using a **public healthcare dataset from Kaggle**. The project focuses on correct problem formulation, clean data handling, interpretable modeling, and ethical awareness rather than model complexity.

---

## 2. Learning Outcomes

By completing this project, students will be able to:

- Understand EHR-style healthcare datasets  
- Define a clinical prediction problem correctly  
- Perform data cleaning and preprocessing  
- Engineer meaningful healthcare features  
- Train and evaluate a basic classifier  
- Interpret model outputs in clinical terms  
- Reflect on bias, privacy, and ethics  
- Design a realistic (conceptual) deployment plan  

---

## 3. Problem Statement

### Prediction Task

Predict whether a patient will be readmitted to the hospital **within 30 days after discharge**, using data available **before or at discharge time**.

### Problem Type
Binary classification

### Target Variable
- `readmitted_within_30_days`
  - 1 → Yes  
  - 0 → No  

---

## 4. Recommended Data Source

### Primary Dataset

**Diabetes 130-US Hospitals Dataset**

Platform: Kaggle  
Description:
- 100,000+ hospital encounters  
- Demographics, diagnoses, medications, procedures  
- Readmission outcome included  

Why this dataset:
- Realistic EHR-style structure  
- Widely used for healthcare analytics education  
- De-identified and safe for teaching  

---

## 5. Target Variable Construction

Original labels:
- `<30`
- `>30`
- `NO`

Mapping:
- `<30` → 1 (Readmitted within 30 days)  
- `>30`, `NO` → 0 (Not readmitted within 30 days)

---

## 6. Project Constraints

Students must:
- Use only features available before or at discharge  
- Avoid data leakage  
- Explain all preprocessing steps  
- Use interpretable models  

Students must not:
- Use patient identifiers as features  
- Optimize only for accuracy  
- Ignore class imbalance  

---

## 7. Project Tasks

### Task 1: Data Exploration
- Inspect dataset structure  
- Identify missing values  
- Analyze class distribution  

### Task 2: Data Cleaning & Preprocessing
- Handle missing values  
- Encode categorical features  
- Scale numeric features if needed  

### Task 3: Feature Engineering
Examples:
- Length of stay  
- Number of medications  
- Number of lab procedures  
- Prior inpatient visits  

Students must justify each feature.

### Task 4: Model Building
Required:
- Logistic Regression
- Decision Tree  
- Random Forest
- Gradient Boost(XGBoost)


### Task 5: Model Evaluation
Required metrics:
- Confusion matrix  
- Accuracy  
- Precision  
- Recall  
- F1-score  

### Task 6: Model Interpretation
- Analyze feature coefficients  
- Explain predictions in simple clinical terms
- Interpret feature importance with SHAP

### Task 7: Ethics, Bias & Privacy
- Discuss bias risks  
- Reflect on fairness  
- Address patient privacy  

---

## 8. Deployment Plan (Streamlit-Based)

The trained readmission prediction model will be deployed as a **Streamlit web application** to demonstrate practical usage in a clinical workflow. This deployment is educational and intended for visualization, interpretation, and decision support.

---

### 8.1 Objective

Allow users (clinicians or analysts) to:

- Input patient data available at discharge  
- Generate a 30-day readmission risk score  
- View a clear risk category (Low / Medium / High)  

---

### 8.2 System Architecture

Components of the Streamlit application:

1. **User Interface** – Web form for entering patient features  
2. **Preprocessing Layer** – Applies the same transformations as during training  
3. **Machine Learning Model** – Loads the trained classifier  
4. **Prediction Output** – Displays risk score and category  

---

### 8.3 Input Features

Include only features available **before or at discharge**:

- Age group  
- Length of stay  
- Number of medications  
- Number of lab procedures  
- Prior admissions  
- Comorbidity indicators  

Patient identifiers must **not** be used.

---

### 8.4 Output

- **Risk Score**: e.g., `0.72` (72% chance of readmission)  
- **Risk Category**: Low / Medium / High  
- Optional: Top contributing features for interpretability  

---

### 8.5 Human Oversight

The model provides **decision support only**. Clinical staff review predictions and take final decisions. The tool is **assistive, not authoritative**.

---

### 8.6 Implementation Notes

- Save and load the trained model using `joblib` or `pickle`  
- Reuse preprocessing pipelines from model training  
- Keep the interface simple and clear  

---

### 8.7 Deliverables

- `app.py` – Streamlit application  
- Trained model file (`.pkl` or `.joblib`)  
- Brief deployment description in the project report  

---

**Disclaimer:** This Streamlit deployment is for **educational purposes only** and is **not suitable for real clinical use**.
 

---

## 9. Final Submission

Students must submit:
1. Jupyter Notebook  
2. Project report (PDF or Markdown)  
3. Evaluation results  
4. Ethics reflection  
5. Deployment plan  

---

## 10. Evaluation Criteria

| Component | Weight |
|---------|--------|
| Data understanding & cleaning | 25% |
| Feature engineering | 20% |
| Modeling & evaluation | 20% |
| Interpretation | 20% |
| Ethics & deployment plan | 15% |

---

## Final Note to Students

This project is about doing the basics correctly.

A simple, transparent, and well-reasoned model is far more valuable than a complex model that cannot be trusted.
