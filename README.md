# Loan Default Prediction

This project aims to predict whether a loan will default based on various borrower attributes and loan details. Using advanced machine learning techniques, the project provides insights into the factors contributing to loan default and evaluates the performance of different models.

---

## Table of Contents
1. [Overview](#overview)
2. [Dataset](#dataset)
3. [Methodology](#methodology)
4. [Machine Learning Models](#machine-learning-models)
5. [Results](#results)
6. [Key Insights](#key-insights)
7. [Technologies Used](#technologies-used)
8. [How to Run](#how-to-run)
9. [Acknowledgments](#acknowledgments)

---

## Overview
Loan default prediction is a critical task in the financial industry to mitigate risks and improve decision-making. This project leverages a dataset with borrower and loan attributes to build predictive models that classify loans as default (`1`) or non-default (`0`).

---

## Dataset
- **Number of Records**: 255,347
- **Features**:
  - Numerical: Age, Income, Loan Amount, Credit Score, Debt-to-Income Ratio, etc.
  - Categorical: Education Level, Employment Type, Marital Status, Loan Purpose, etc.
- **Target Variable**: `Default` (`0` = Non-Default, `1` = Default)

### Data Preprocessing
1. Handled missing values (none in the dataset).
2. Removed duplicates.
3. Applied one-hot encoding for categorical variables.
4. Created new features:
   - **Income-to-Loan Ratio**
   - **Debt-to-Income Ratio**
5. Scaled numerical features using `StandardScaler`.
6. Addressed class imbalance using **SMOTE** (Synthetic Minority Oversampling Technique).

---

## Methodology
1. **Exploratory Data Analysis (EDA)**:
   - Visualized distributions of numerical and categorical variables.
   - Analyzed correlations between features.
   - Examined the class imbalance in the target variable.

2. **Feature Engineering**:
   - Created new features to enhance predictive power.
   - Standardized numerical columns for better model performance.

3. **Model Training**:
   - Split the data into training (70%) and testing (30%) sets.
   - Implemented and evaluated three machine learning models.

---

## Machine Learning Models
1. **Logistic Regression**
2. **Random Forest Classifier**
3. **XGBoost Classifier**

### Model Evaluation Metrics:
- Classification Report (Precision, Recall, F1-Score)
- Confusion Matrix
- ROC-AUC Score

---

## Results
| Model                 | ROC-AUC Score |
|-----------------------|---------------|
| Logistic Regression   | 0.8286        |
| Random Forest         | 0.9765        |
| XGBoost               | 0.9574        |

- **Random Forest** performed the best, achieving the highest ROC-AUC score.
- **XGBoost** also showed strong performance.

---

## Key Insights
1. **Class Imbalance**: The dataset was highly imbalanced (88.39% non-default, 11.61% default). Addressing this with SMOTE improved model performance.
2. **Important Features**:
   - Credit Score
   - Debt-to-Income Ratio
   - Income-to-Loan Ratio
3. **Model Performance**:
   - Ensemble methods (Random Forest, XGBoost) significantly outperformed Logistic Regression.

---

## Technologies Used
- **Programming Language**: Python
- **Data Analysis and Visualization**: Pandas, NumPy, Matplotlib, Seaborn
- **Machine Learning**: Scikit-learn, XGBoost
- **Imbalanced Data Handling**: SMOTE (imbalanced-learn)
- **Version Control**: Git and GitHub

---

## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/fernandes-s/loan_default_prediction.git
   cd loan_default_prediction
