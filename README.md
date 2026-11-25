# Telco Customer Churn Prediction

## Overview

This project focuses on predicting customer churn using machine learning classification algorithms. It explores customer data to identify patterns and factors associated with customer churn and builds classification models to predict whether a customer is likely to leave the service.

The project covers the complete machine learning workflow, from exploratory data analysis and data preprocessing to model training and evaluation.

## Dataset

- **Dataset:** IBM Telco Customer Churn
- **Total Records:** 7,043
- **Target Variable:** `Churn`
- **Problem Type:** Binary Classification

The dataset contains customer information, including demographics, subscribed services, contract details, payment methods, tenure, and monthly charges.

## Technologies & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn

## Project Workflow

### 1. Exploratory Data Analysis (EDA)
- Understanding dataset dimensions and structure.
- Checking missing values and duplicate records.
- Analyzing categorical variables and unique values.
- Examining target variable distribution.
- Visualizing churn patterns across contract types, tenure, and monthly charges.

### 2. Data Cleaning & Preprocessing
- Removing irrelevant customer identifiers.
- Separating independent and dependent variables.
- Splitting data into training and testing sets.
- Using stratified sampling to maintain target class distribution.
- Applying StandardScaler to numerical features.
- Applying One-Hot Encoding to categorical features.

### 3. Handling Class Imbalance
- Applying SMOTE (Synthetic Minority Over-sampling Technique) to balance the training dataset.

### 4. Feature Selection
- Examining feature correlations with the target variable.
- Selecting relevant features for model training.

### 5. Model Building
The following classification algorithms were implemented:

- Logistic Regression
- K-Nearest Neighbors (KNN)

### 6. Model Evaluation
Models were evaluated using:

- Accuracy Score
- Confusion Matrix
- Classification Report
- Precision
- Recall
- F1-Score

## Model Results

| Model | Training Accuracy | Testing Accuracy |
|---|---:|---:|
| Logistic Regression | 74.98% | 71.68% |
| KNN | 57.13% | 73.46% |

**Note:** Although KNN achieved higher test accuracy, its churn recall was 0.00%, meaning it failed to identify any actual churn customers. Logistic Regression performed better at identifying churn cases, achieving a churn recall of 0.78.

Accuracy alone is therefore insufficient to determine the better model for this classification problem.

## Key Learnings

- Understanding and performing exploratory data analysis.
- Handling numerical and categorical features.
- Implementing feature scaling and encoding.
- Understanding class imbalance and applying SMOTE.
- Performing feature selection.
- Building and evaluating classification models.
- Interpreting confusion matrices and classification reports.
- Comparing models using multiple evaluation metrics.

## Future Improvements

- Experiment with additional classification algorithms.
- Perform hyperparameter tuning using GridSearchCV.
- Explore alternative feature selection techniques.
- Experiment with different class imbalance handling methods.
- Improve model performance using additional relevant features.

## Project Status

Completed initial preprocessing, exploratory data analysis, and baseline classification model implementation. Further experimentation and model improvements are possible.

---

**Author:** Harisanker S Paleri
