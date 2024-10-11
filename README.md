# GST Analytics Predictive Model

This repository contains the solution developed for the GSTN analytics challenge by undergraduate students of Netaji Subhas University of Technology. The project focuses on building a predictive model for GST analytics, overcoming challenges such as imbalanced data, missing values, and selecting the best performing model.

## Team Information
- **Team ID**: GSTN_821
- **University**: Netaji Subhas University of Technology

## Problem Statement
The objective of this project is to develop a predictive model for GST analytics. Key challenges include:

- **Imbalanced Target Class**: The target class is dominated by zeros, making it difficult to accurately predict class 1.
- **Missing Data**: Some features contain missing values, which required careful imputation to maintain data consistency.
- **Model Selection**: Evaluated multiple models based on their accuracy, efficiency, and ability to handle large datasets.

## Dataset Overview
- **X_train**: 785,133 records with 21 features + ID.
- **Y_train**: 785,133 records with a boolean target variable + ID.
- **Data Imputation**: Addressed missing data using various imputation techniques:
  - **Median Imputation**: Applied to Columns 5, 6, 9, 14, and 15.
  - **Iterative Imputation**: Applied to Columns 3 and 4.
  - **KNN Imputation**: Applied to Column 8 (k=5).
- **Standard Scaling**: Data was standardized before model training to ensure consistency.

## Data Visualization
- **Null Values Bar Chart**: Displays the proportion of missing data across features.
- **Correlation Matrix Heatmap**: Shows relationships between numeric features.

## Model Training & Performance
We compared various models and selected the best performing ones based on metrics such as accuracy, precision, recall, F1 score, AUC-ROC, log loss, and balanced accuracy.

### CatBoost Model
- **Accuracy**: 0.9783
- **Precision**: 0.8485
- **Recall**: 0.9369
- **F1 Score**: 0.8905
- **AUC-ROC**: 0.9947
- **Confusion Matrix**: [[232902 4130] [ 1556 23122]]
- **Log Loss**: 0.0501
- **Balanced Accuracy**: 0.9598

### KNN Model
- **Accuracy**: 0.9729
- **Precision**: 0.8301
- **Recall**: 0.8958
- **F1 Score**: 0.8617
- **AUC-ROC**: 0.9867
- **Confusion Matrix**: [[232506 4526] [ 2572 22106]]
- **Log Loss**: 0.2525
- **Balanced Accuracy**: 0.9383

## Results & Conclusion
The CatBoost model achieved the highest accuracy and AUC-ROC score, making it the best choice for the given problem. Our approach effectively handled the class imbalance and missing data, resulting in a reliable predictive model.
