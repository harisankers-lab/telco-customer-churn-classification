# Telco Customer Churn Classification

## Overview

This project focuses on predicting customer churn using machine learning classification algorithms. The objective is to analyze customer information, identify patterns associated with churn, and build models to predict whether a customer is likely to discontinue a service.

The project follows a machine learning workflow covering exploratory data analysis, data cleaning, preprocessing, class imbalance handling, feature selection, model training, and evaluation.

## Dataset

- **Dataset:** IBM Telco Customer Churn
- **Original Records:** 7,043
- **Features:** Customer demographics, subscribed services, account information, and billing details.
- **Target Variable:** `Churn`
- **Problem Type:** Binary Classification

The `TotalCharges` column was converted into numeric format, and 11 rows containing missing values in this column were removed.

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

- Understanding dataset structure and dimensions.
- Checking missing values and duplicate records.
- Exploring categorical features and unique values.
- Analyzing the distribution of the target variable.
- Visualizing churn patterns across contract types, tenure, and monthly charges.

### 2. Data Cleaning

- Converting `TotalCharges` into numeric format.
- Handling missing values.
- Removing the customer ID column.
- Converting `SeniorCitizen` into a categorical feature.

### 3. Data Preprocessing

- Separating independent and dependent variables.
- Performing stratified train-test splitting.
- Applying StandardScaler to numerical features.
- Applying One-Hot Encoding to categorical features.
- Maintaining consistent transformations between training and testing data.

### 4. Handling Class Imbalance

- Identifying class imbalance in the target variable.
- Applying SMOTE (Synthetic Minority Over-sampling Technique) to the training data.

### 5. Feature Selection

- Analyzing feature correlations with the target variable.
- Selecting three features for model training:
  - `Contract_Month-to-month`
  - `OnlineSecurity_No`
  - `OnlineBackup_No`

### 6. Model Building

Three classification algorithms were implemented:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree Classifier

### 7. Hyperparameter Selection and Threshold Analysis

- Splitting training data into training and validation sets for KNN.
- Experimenting with odd values of K from 1 to 31.
- Selecting the best K using validation F1-score.
- Exploring different classification probability thresholds (0.3, 0.5, and 0.7).

### 8. Model Evaluation

Models were evaluated using:

- Accuracy Score
- Confusion Matrix
- Precision
- Recall
- F1-Score
- Classification Report

## Model Performance

The following results were obtained from the implemented models:

| Model | Training Accuracy | Testing Accuracy |
|---|---:|---:|
| Logistic Regression | 75.99% | 70.79% |
| KNN (k=5) | 52.34% | 68.66% |
| Decision Tree | 77.97% | 72.85% |

### Evaluation Insights

**Logistic Regression**

Achieved a churn recall of 0.78 and an F1-score of 0.59, making it the strongest of the evaluated models in identifying churn customers.

**K-Nearest Neighbors**

The optimal K was selected as 5 using validation F1-score. However, its test performance showed poor churn identification, with a recall of 0.0428.

**Decision Tree**

Achieved the highest test accuracy among the three implemented models at 72.85%. Further evaluation using class-specific precision, recall, and F1-score is needed for a complete comparison.

## Key Learnings

- Performing exploratory data analysis.
- Handling missing values and data type conversion.
- Understanding numerical scaling and categorical encoding.
- Applying SMOTE to address class imbalance.
- Exploring feature correlation and feature selection.
- Implementing classification algorithms.
- Selecting hyperparameters using validation data.
- Understanding probability thresholds.
- Evaluating classification models using multiple metrics.

## Future Improvements

- Explore additional feature selection techniques.
- Experiment with alternative sampling methods.
- Perform hyperparameter tuning using GridSearchCV.
- Improve KNN performance through feature and parameter experimentation.
- Evaluate Decision Tree using additional classification metrics.
- Compare models using precision, recall, and F1-score.
- Explore ensemble learning algorithms.

## Project Status

Initial EDA, data preprocessing, feature selection, and baseline classification models have been implemented. Further model evaluation and optimization are possible.

---

**Author:** Harisanker
