# Bank Marketing Machine Learning Project

## Overview

This project builds machine learning models to predict whether a client will subscribe to a term deposit using bank marketing data. The goal is to improve targeting and support better decision-making in marketing campaigns.

## Dataset

The dataset contains 41,188 records with 14 features and 1 target variable (Subscribed).
It is highly imbalanced, with approximately 89% of clients not subscribing and 11% subscribing.
Features include demographic, financial, and campaign-related information such as age, job, education, loan status, and call duration.

## Data Preparation

The data was cleaned by handling "unknown" values and applying imputation.
Median imputation was used for numerical features, while the most frequent values were used for categorical features.
Categorical variables were converted using one-hot encoding.
Numerical features were standardized for Logistic Regression.
The dataset was split into training and testing sets using a 70/30 split.

## Models Used

Logistic Regression and Random Forest models were implemented to compare performance.

## Results

Both models achieved approximately 14% accuracy, with recall reaching 100% and precision around 12%.
This indicates that the models predicted almost all observations as “Yes”, resulting in poor overall performance despite perfect recall.

## Key Insights

The strong class imbalance significantly impacted model performance.
Accuracy alone was not a reliable metric in this case.
The models showed bias toward predicting the minority class, leading to overprediction.

## Recommendations

To improve performance, class imbalance techniques such as SMOTE or resampling should be applied.
Hyperparameter tuning should be performed to optimize model performance.
More advanced models like XGBoost or Gradient Boosting should be tested.
Potential data leakage features should be reviewed and removed if necessary.
Evaluation should focus more on precision, recall, and F1 score rather than accuracy.

## Tools Used

Python, pandas, scikit-learn, matplotlib, seaborn

## Author

Collins Ezenwelu
