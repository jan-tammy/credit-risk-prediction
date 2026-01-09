# 📊 Credit Risk Prediction – German Credit Dataset
Janhavi Tamhankar

## Project Overview
This project implements an end-to-end machine learning workflow for **credit risk classification** using the German Credit dataset from the UCI Machine Learning Repository. The objective is to predict whether a loan applicant represents a **high credit risk (bad credit)** or **low credit risk (good credit)** while addressing key challenges common in real-world financial modeling, such as class imbalance, skewed financial variables, and business-aligned evaluation.

The project is designed to reflect how credit risk models are structured, evaluated, and interpreted in industry settings.

---

## Business Problem
In lending, approving a high-risk applicant can lead to significant financial losses, while rejecting a low-risk applicant results in lost revenue and customer dissatisfaction. These errors have **asymmetric costs**, making accuracy alone an unreliable evaluation metric. This project focuses on metrics that better capture business risk and decision-making quality.

---

## Dataset
- **Source:** UCI Machine Learning Repository  
- **Dataset:** German Credit Dataset  
- **Target Variable:** Credit risk classification (good vs bad credit)  
- **Features:** Demographic, financial, and behavioral attributes of loan applicants  

---

## Machine Learning Models Evaluated
- Logistic Regression  
- K-Nearest Neighbors (KNN)  
- Decision Tree  
- Random Forest  
- XGBoost  

All models were evaluated using **Stratified K-Fold Cross Validation** to ensure stable and unbiased performance estimates under class imbalance.

---

## Feature Engineering & Preprocessing
- Applied **log transformations** to highly skewed numeric variables such as credit amount, credit duration, and age.
- Standardized numeric features to support linear and distance-based models.
- One-hot encoded categorical variables.
- Ensured all preprocessing steps were applied without data leakage.

**Impact:**  
Log-transformed features improved model stability and resulted in higher ROC-AUC scores, indicating better risk ranking.

---

## Hyperparameter Tuning
Hyperparameter tuning was performed for Decision Tree, Random Forest, and XGBoost models. Adjusting parameters such as tree depth, number of estimators, and learning rate:

- Reduced overfitting  
- Improved recall and model stability  
- **Increased ROC-AUC compared to baseline models**

This improvement demonstrates enhanced ability to distinguish risky applicants from safe ones.

---

## Model Evaluation Metrics (Business Interpretation)

- **ROC-AUC:** Measures how well the model ranks risky applicants above safe ones; the most important metric for credit screening.
- **Recall (Bad Credit):** Indicates how many high-risk applicants are correctly identified; critical for minimizing financial losses.
- **Precision:** Reflects how many predicted risky applicants are truly risky; important for operational efficiency.
- **Specificity:** Measures correct approval of low-risk applicants; supports revenue and customer experience.
- **Accuracy:** Reported for completeness but not relied upon due to class imbalance.

---

## Key Results & Conclusions
- Logistic Regression achieved the most balanced performance and the highest ROC-AUC.
- Decision Trees provided the highest recall, effectively identifying high-risk applicants.
- KNN achieved high accuracy and specificity but performed poorly in recall.
- Random Forest and XGBoost showed strong precision and accuracy but lagged in minority-class detection.
- Feature engineering and hyperparameter tuning significantly improved ranking performance and reliability.

---

## Future Work
- Incorporate cost-sensitive learning or expected loss optimization
- Explore oversampling methods such as SMOTE
- Apply probability calibration for threshold-based decision systems
- Conduct deeper fairness and bias analysis
- Deploy the model with monitoring for data and performance drift

---

## Repository Contents
- Jupyter notebook with EDA, modeling, and evaluation
- Model comparison tables and performance metrics
- Feature importance visualizations
- Clean, reproducible machine learning workflow

---

📌 *This project demonstrates how machine learning models can be aligned with real-world financial decision-making and risk management.*
