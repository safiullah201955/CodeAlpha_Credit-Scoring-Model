# CodeAlpha_Credit-Scoring-Model

# Overview
This project aims to predict the likelihood of credit default (Serious Delinquency in 2 years) using a real-world credit scoring dataset. It uses a Random Forest Classifier, enhanced by SMOTE (Synthetic Minority Oversampling Technique) to handle class imbalance, and includes threshold tuning based on F1-score optimization for better classification performance.
# Problem Statement
Financial institutions need accurate credit risk models to determine whether a customer is likely to default on a loan. The target variable SeriousDlqin2yrs indicates whether a person experienced serious delinquency in the following 2 years. This is a binary classification problem with a highly imbalanced dataset.
# Dataset
The dataset includes features such as:

Age

Monthly Income

Debt Ratio

Number of Dependents

Credit history indicators (e.g., late payments)
# Additional Feature Engineering
TotalPastDue: Sum of 30-59, 60-89, and 90+ days past due accounts.

NumberOfLoans: Total number of credit lines and real estate loans.

# Imbalance Handling
Applied SMOTE to synthetically oversample the minority class (default cases) in training data.

# Model Training
Used RandomForestClassifier with optimized hyperparameters.

Enabled class_weight='balanced' to further address imbalance.

# Threshold Tuning
Used Precision-Recall Curve to identify the threshold that maximizes the F1-score.

Applied the optimal threshold to convert probabilities into binary class predictions.

# Evaluation Metrics
Classification Report (Precision, Recall, F1-score)

ROC AUC Score
