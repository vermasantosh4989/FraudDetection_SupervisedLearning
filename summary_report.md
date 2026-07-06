# Project Summary Report

## Project Title

Credit Card Fraud Detection using Supervised Machine Learning

## Objective

The objective of this project is to build machine learning models that
can accurately identify fraudulent credit card transactions while
minimizing false alarms. Since the dataset is highly imbalanced,
different imbalance handling techniques were evaluated.

## Dataset

-   Dataset Name: creditcard.csv
-   Target Variable: Class
-   Legitimate Transactions: 0
-   Fraudulent Transactions: 1

## Project Steps

1.  Loaded and explored the dataset.
2.  Performed Exploratory Data Analysis (EDA).
3.  Engineered new features:
    -   Amount_log
    -   Hour
4.  Applied feature scaling using StandardScaler.
5.  Split the data into training and testing sets.
6.  Applied imbalance handling techniques:
    -   Original Data
    -   SMOTE
    -   Random Under Sampling
7.  Trained machine learning models:
    -   Logistic Regression
    -   Random Forest
    -   XGBoost
8.  Evaluated models using:
    -   Precision
    -   Recall
    -   F1 Score
    -   PR-AUC
9.  Performed hyperparameter tuning using RandomizedSearchCV.
10. Optimized the prediction threshold using the Precision-Recall curve.
11. Saved the best-performing model.

## Tools and Libraries

-   Python
-   Pandas
-   NumPy
-   Matplotlib
-   Seaborn
-   Scikit-learn
-   Imbalanced-learn
-   XGBoost
-   Joblib

## Results

The trained models were evaluated on unseen test data. Hyperparameter
tuning and threshold optimization improved fraud detection performance.
Precision-Recall analysis was used because it is more suitable than ROC
analysis for highly imbalanced datasets.

## Conclusion

This project demonstrates how supervised machine learning can
effectively detect fraudulent credit card transactions. By combining
preprocessing, imbalance handling, model optimization, and threshold
tuning, the system achieves better fraud detection performance and
provides a practical solution for real-world financial applications.

## Author

Santosh Verma
