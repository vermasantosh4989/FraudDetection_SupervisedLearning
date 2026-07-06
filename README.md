# Credit Card Fraud Detection using Supervised Machine Learning


This project focuses on detecting fraudulent credit card transactions using supervised machine learning techniques. Since fraudulent transactions represent only a very small portion of the dataset, the project applies feature engineering, data preprocessing, imbalance handling, model training, hyperparameter tuning, and threshold optimization to improve fraud detection performance.

---
# Dataset creditcard.csv Online Link

https://drive.google.com/file/d/1zyuGKeYMwIswUMyZv8pQQM26b4kMN8Ne/view?usp=sharing

# Dataset clean_data.csv Online Link

https://drive.google.com/file/d/1grHeWB4VJL9BjWdh83X2jYHQ78vxcV9J/view?usp=sharing

---
# Dataset Overview

- Dataset Name: creditcard.csv
- Total Features: 31
- Target Column: Class
- Total Records: 284,807
- Legitimate Transactions (Class = 0): 284,315
- Fraudulent Transactions (Class = 1): 492

### Feature Description

| Feature | Description |
|----------|-------------|
| Time | Seconds elapsed between transactions |
| V1-V28 | PCA transformed confidential features |
| Amount | Transaction amount |
| Class | Target (0 = Legitimate, 1 = Fraud) |

---

# Data Preprocessing

The following preprocessing steps were performed:

- Loaded dataset
- Checked missing values
- Checked class distribution
- Created stratified sample
- Feature Engineering
  - Amount_log = log1p(Amount)
  - Hour extracted from Time
- Dropped original Time and Amount columns
- StandardScaler applied on Amount_log and Hour
- Train-Test Split (80:20)
- Class imbalance handling using:
  - Original Data
  - SMOTE
  - Random Under Sampling

---

# Exploratory Data Analysis (EDA)

The following analysis was performed:

- Dataset shape
- Summary statistics
- Class distribution
- Fraud vs Legitimate comparison
- Amount distribution
- Time distribution
- Correlation heatmap
- Feature importance analysis

### Key Findings

- The dataset is highly imbalanced.
- Fraud transactions represent only about 0.17% of all transactions.
- Fraudulent transactions generally have smaller transaction amounts.
- Some PCA features show strong correlation with fraudulent transactions.

---

# Machine Learning Models

The following models were implemented:

- Logistic Regression
- Random Forest
- XGBoost

---

# Model Performance

| Model | Accuracy | Precision | Recall | F1 Score | PR-AUC |
|--------|---------:|----------:|--------:|---------:|--------:|
| Logistic Regression | 99.78% | 0.30 | 0.94 | 0.45 | 0.75 |
| Random Forest | 99.95% | 0.45 | 0.94 | 0.61 | 0.87 |
| XGBoost | 99.97% | 0.64 | 0.94 | 0.76 | 0.94 |

>  The table is sorted in descending order of Recall, as Recall is the most important metric for customer churn prediction.



---

# Hyperparameter Tuning

RandomizedSearchCV was used for:

- Logistic Regression
- Random Forest
- XGBoost

Best hyperparameters were selected using **Average Precision (PR-AUC)**.

---

# Threshold Optimization

Threshold optimization was performed using the Precision-Recall Curve.

The following thresholds were evaluated:

- Default Threshold (0.5)
- Best F1 Threshold
- Recall ≥ 0.90 Threshold

This improved the balance between fraud detection and false alarms.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- XGBoost
- Joblib

---

# Project Structure

```
Credit-Fraud-Detection/
│
├── FraudDetection.ipynb
├── creditcard.csv
├── fraud_detection_model.pkl
├── README.md
├── requirements.txt
└── summary_report.md
```

---

# How to Run

1. Clone the Drive.
2. Install the required libraries:

```
pip install -r requirements.txt
```

3. Place `creditcard.csv` in the project folder.
4. Open the notebook.
5. Run all cells.

---

# Conclusion

The project successfully developed machine learning models for detecting fraudulent credit card transactions. Among the tested models, the best-performing model achieved the highest PR-AUC and F1 Score after hyperparameter tuning and threshold optimization. The results demonstrate that handling class imbalance and optimizing the decision threshold significantly improve fraud detection performance while reducing missed fraudulent transactions.

---

# Author

**Santosh Verma**

---

# License

This project is developed for educational and academic purposes.

