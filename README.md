# Stroke Prediction Model Findings

## Dataset Summary

- **Total Observations**: 5110
- **Features**: 12 (including target)
- **Target Variable**: `stroke` (Binary: 0 = No Stroke, 1 = Stroke)
- **Class Imbalance**:
  - Stroke = 1: 249 instances
  - Stroke = 0: 4861 instances

## Feature Overview

- **Gender**: Female (2994), Male (2115), Other (1)
- **Age**: Range 0.08 to 82 (Mean ≈ 43.23)
- **Hypertension**: 9.7% positive cases
- **Heart Disease**: 5.4% positive cases
- **Ever Married**: Yes (3353), No (1757)
- **Work Type**: 
  - Private: 2925  
  - Self-employed: 819  
  - Govt_job: 657  
  - Children: 687  
  - Never_worked: 22
- **Residence Type**: Urban (2596), Rural (2514)
- **Average Glucose Level**: Mean ≈ 106.15
- **BMI**: Mean ≈ 28.89
- **Smoking Status**:
  - Formerly Smoked: 885  
  - Never Smoked: 1892  
  - Smokes: 789  
  - Unknown: 1544

---

## Model Evaluation Results

### Logistic Regression / Random Forest / SVM

All three models resulted in **identical confusion matrices** when tested on the dataset (before applying balancing techniques).

#### Confusion Matrix:

# Prediction 0 1
# 0 972 49
# 1 0 0


#### Metrics:

- **Accuracy**: 95.2%
- **95% CI**: (93.7%, 96.43%)
- **No Information Rate (NIR)**: 95.2%
- **P-Value [Acc > NIR]**: 0.5379
- **Kappa**: 0
- **McNemar’s Test P-Value**: 7.025e-12

#### Class-wise Performance:

- **Sensitivity (Recall for Class 0)**: 1.000
- **Specificity (Recall for Class 1)**: 0.000
- **Positive Predictive Value (Precision for Class 0)**: 0.952
- **Negative Predictive Value (Class 1)**: NaN (none predicted as class 1)
- **Balanced Accuracy**: 0.500
- **Detection Rate**: 0.952
- **Detection Prevalence**: 1.000

---

## ⚠️ Key Observations

- The model **always predicts stroke = 0** (majority class).
- **No true positives** or **true negatives** for stroke = 1.
- **Perfect recall for class 0**, **zero recall for class 1**.
- **Kappa = 0** → The model performs no better than chance when accounting for imbalance.
- **Balanced accuracy is 0.5**, indicating the model is biased due to class imbalance.

---
