# The Credit Risk Analysis Challenge

# credit-risk-classification
This analysis aims to build and evaluate a machine learning model that predicts the creditworthiness of borrowers based on historical lending data from a peer-to-peer lending services company. The goal is to determine the credit risk of borrowers by classifying loans as healthy (0) or high-risk (1).

# Credit Risk Analysis Overview

### Financial Information
The dataset contains financial information such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt.

### Methods Used
- **Logistic Regression**: A statistical model used for binary classification to predict the probability of a binary outcome based on one or more predictor variables.


## Overview of the Analysis

* **Purpose of the Analysis**: The purpose of this analysis was to use machine learning techniques to predict the creditworthiness of borrowers by classifying loans as either healthy (low-risk) or high-risk. This helps lenders make informed decisions and manage their risk exposure effectively.

* **Financial Information and Prediction Goal**: The data contains financial information about loan applicants, including:
  - Loan size
  - Interest rate
  - Borrower income
  - Debt-to-income ratio
  - Number of accounts
  - Derogatory marks
  - Total debt
  
  The goal is to predict the 'loan_status' column, which indicates whether a loan is healthy (low-risk, represented as 0) or high-risk (represented as 1).

* **Basic Information about Variables**: 
  - The target variable is 'loan_status', with values:
    - 0: Healthy loan
    - 1: High-risk loan
  - Example value counts:
    ```python
    y.value_counts()
    ```
    ```
    0    75036
    1     2500
    Name: loan_status, dtype: int64
    ```

* **Stages of the Machine Learning Process**:
  1. **Data Preparation**: Loaded and preprocessed the data, separating features (X) and labels (y).
  2. **Data Splitting**: Split the data into training and testing sets using `train_test_split`.
  3. **Model Training**: Trained a logistic regression model using the training data (`X_train` and `y_train`).
  4. **Model Evaluation**: Evaluated the model's performance on the testing data (`X_test` and `y_test`).
  5. **Analysis and Reporting**: Analyzed the results and reported the findings.

* **Methods Used**:
  - **Logistic Regression**: A statistical model used for binary classification to predict the probability of a binary outcome based on one or more predictor variables.

## Results

* **Machine Learning Model 1** (Logistic Regression):
  - **Accuracy Score**: 0.99
  - **Precision Score**: 
    - Healthy Loan (0): 1.00
    - High-Risk Loan (1): 0.84
  - **Recall Score**: 
    - Healthy Loan (0): 0.99
    - High-Risk Loan (1): 0.94

* **Confusion Matrix Interpretation**:
  - The confusion matrix is as follows:
    ```
    array([[18655,   110],
           [   36,   583]])
    ```
  - **True Positives (TP)**: 583 (High-risk loans correctly identified as high-risk)
  - **True Negatives (TN)**: 18655 (Healthy loans correctly identified as healthy)
  - **False Positives (FP)**: 110 (Healthy loans incorrectly identified as high-risk)
  - **False Negatives (FN)**: 36 (High-risk loans incorrectly identified as healthy)

  The high number of true positives and true negatives indicates that the model is highly effective in correctly classifying both healthy and high-risk loans. The relatively low number of false positives and false negatives shows that the model has a low rate of misclassification, which is crucial for making reliable credit risk assessments.

* Further highlights of these results are found in the accompanying markdown file called `report-template` in the same root directory as this file.

## Summary

* **Model Performance**:
  - The logistic regression model performs exceptionally well, with an overall accuracy of 99%. 
  - It shows high precision and recall for predicting healthy loans, with precision and recall scores of 1.00 and 0.99, respectively.
  - For high-risk loans, the model also performs well, with precision and recall scores of 0.84 and 0.94, respectively.

* **Recommendation**:
  - Based on the results, the logistic regression model is recommended for predicting loan risk. It demonstrates balanced performance in predicting both healthy and high-risk loans, making it a suitable choice for identifying credit risk in borrowers.
  - The high precision and recall scores for both loan statuses ensure that the model can accurately classify loans, minimizing the risk of misclassification and helping lenders make informed decisions.

# Conclusion
By following this structured approach, the analysis provides insights into the creditworthiness of borrowers, aiding in better decision-making for loan approvals and risk management.

