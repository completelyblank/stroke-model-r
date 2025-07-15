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

