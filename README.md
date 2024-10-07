# Credit Card Fraud Detection

This repository contains the code and analysis for our credit card fraud detection project, using the **Credit Card Fraud Detection Dataset 2023** from Kaggle. Our objective is to identify fraudulent transactions using machine learning techniques.

## Introduction

Credit card fraud is a significant issue in the financial industry, with sophisticated methods used by fraudsters to exploit vulnerabilities. Our project aims to improve fraud detection mechanisms using a dataset of 550,000 transactions. We explore key characteristics of fraudulent transactions and assess whether machine learning models can effectively distinguish between legitimate and fraudulent activity.

## Dataset

- **Source**: Kaggle - Credit Card Fraud Detection Dataset 2023
- **Size**: 550,000 transaction records
- **Features**:
  - **ID**: Unique identifier for each transaction
  - **V1-V28**: Anonymized attributes representing transaction details
  - **Amount**: Transaction amount
  - **Class**: Binary label (1 = Fraudulent, 0 = Non-fraudulent)

## Data Preprocessing

1. **No Null Values**: The dataset contains no missing values.
2. **Duplicate Removal**: We removed any duplicate records to ensure data integrity.
3. **Class Balance**: The dataset is balanced, with an equal split of fraudulent and non-fraudulent transactions.
4. **Outliers**: Outliers were retained due to their potential relevance in fraud detection.

## Machine Learning Models

### K-Nearest Neighbors (KNN)
- **k-values tested**: 5, 10, 20, 100
- **Best k-value**: 5
- **Accuracy**: 93.49%

### Decision Tree
- **Method**: Recursive binary splitting
- **Accuracy**: 99.83%
- **Key Features**: V14, V4, and V10 show the strongest correlations with fraudulent transactions.

### Regularized Regression (Ridge & Lasso)
- **Objective**: Assist with feature selection by shrinking coefficients of less important features.

## Results

- **KNN Classifier**: The highest accuracy was achieved with k=5 (93.49%).
- **Decision Tree Classifier**: Achieved an accuracy of 99.83% on the test set.
- **Feature Importance**: 
  - Through the Decision Tree model, we identified several key features that played a crucial role in predicting fraud:
    - **V14**: This feature had the highest importance, indicating a strong influence on whether a transaction was fraudulent.
    - **V4**: Another highly relevant feature, showing significant correlation with fraudulent transactions.
    - **V10**: This feature also demonstrated a strong impact in distinguishing between legitimate and fraudulent activities.
  - These features provide valuable insights into the patterns and characteristics of fraud, helping improve the detection accuracy of machine learning models.

## Conclusion

- Our models demonstrate high accuracy, particularly the Decision Tree classifier, which achieved near-perfect results.
- By focusing on key features such as V14, V4, and V10, we can improve detection mechanisms and help mitigate credit card fraud.

## What We Can Do
- Enhance fraud detection accuracy.
- Reduce financial risks through automated fraud detection.
- Improve efficiency by reducing manual reviews of transactions.
