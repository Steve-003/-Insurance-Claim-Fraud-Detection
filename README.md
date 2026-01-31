# -Insurance-Claim-Fraud-Detection
This project uses machine learning to detect fraudulent insurance claims

Overview
This project implements a comprehensive machine learning solution for detecting fraudulent insurance claims. The system analyzes historical claims data to classify claims as fraudulent or legitimate, helping insurance companies reduce financial losses and improve operational efficiency.

## Problem Statement

Insurance fraud results in significant financial losses. This project builds predictive models to identify suspicious claims.

## Dataset

The dataset contains insurance claims information in 39 columns, reduced to 25 through feature selection

Source: Historical insurance claims dataset (1000 samples)
Target Variable: fraud_reported (1 = Fraud, 0 = Legitimate)
2. Data Preprocessing & Feature Engineering
2.1 Feature Selection
Removed irrelevant columns including:
Personal identifiers (policy_number, insured_zip)
Demographic information (age, insured_sex)
Temporal features with minimal predictive value
Redundant location information

2.2 Data Cleaning
Missing value handling for categorical features
Encoding of categorical variables using One-Hot Encoding
Target variable transformation (Y→1, N→0)

2.3 Feature Analysis
25 final features (15 numerical, 9 categorical, 1 target)
Class imbalance observed: 75.3% legitimate vs 24.7% fraudulent claims

3.2 Key Insights
Authorities Contacted: Most common contacts are Police (54%) and Fire (25%)
Incident Severity: Significant relationship with fraud reporting
Categorical Features: 9 categorical variables with 3-39 unique values each

Handling Class Imbalance
Technique: RandomOverSampler
Approach: Oversampled minority class (fraudulent claims)
Result: Balanced dataset for training

Model Development
Algorithms Implemented
Logistic Regression - Baseline model
Random Forest - Ensemble method for non-linear relationships
Gradient Boosting (XGBoost, LightGBM) - State-of-the-art performance
Support Vector Machines - For high-dimensional space
Neural Networks - Deep learning approach

Model Training Strategy
Train-Test Split: 80-20 split with stratification
Cross-Validation: 5-fold stratified cross-validation
Hyperparameter Tuning: GridSearchCV for optimal parameters

Model Evaluation Metrics
Primary Metrics:
Accuracy: Overall prediction correctness
Precision: Fraud detection accuracy (minimizing false positives)
Recall: Capturing actual fraud cases (minimizing false negatives)
F1-Score: Harmonic mean of precision and recall
AUC-ROC: Model discrimination capability
Confusion Matrix: Detailed error analysis

Business-Centric Metrics:
Cost Savings Analysis: Estimated financial impact
False Positive Rate: Legitimate claims incorrectly flagged
Fraud Detection Rate: Percentage of actual fraud caught

## Technologies Used

-   Python
-   Pandas
-   Scikit-learn
-   Imbalanced-learn
-   Matplotlib
-   Seaborn

## Project Workflow

1.  Data Cleaning and Wrangling
2.  Exploratory Data Analysis
3.  Feature Engineering
4.  Handling Class Imbalance
5.  Model Building
6.  Model Evaluation
7.  Model Saving and Deployment

## Author:Steve

Steve
