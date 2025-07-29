# 🛡️ Fraud Detection using Machine Learning

This project implements a fraud detection system using a dataset of 6.3 million financial transactions. The goal is to identify fraudulent behavior and extract actionable business insights.

## 📂 Project Overview

- **Problem**: Identify and prevent fraudulent transactions in financial systems.
- **Data**: 6,362,620 records with features like transaction type, amount, and account balances.
- **Goal**: Train a model to predict fraud and recommend prevention strategies.

## 🔧 Technologies Used

- Python (3.9)
- Jupyter Notebook
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn

## 🧠 Key Steps

1. Data Cleaning
2. Exploratory Data Analysis (EDA)
3. Feature Engineering
4. Encoding Categorical Variables
5. Train-Test Split
6. Model Building (Random Forest Classifier)
7. Model Evaluation
8. Feature Importance
9. Business Insights

## 📊 Model Performance

- **Model**: Random Forest Classifier
- **F1 Score (Fraud)**: 0.84
- **Precision (Fraud)**: 0.95
- **Recall (Fraud)**: 0.75
- **ROC-AUC Score**: 0.97

## 🔍 Feature Importance

Top predictors of fraud:
- Transaction Type (`TRANSFER`, `CASH_OUT`)
- Amount
- Balance Difference (before and after)
- Original Account Balance

## 📌 Business Insights (Step 9)

### 1. Data Cleaning
- No missing values; engineered `balanceDiffOrig` and `balanceDiffDest` to capture transaction shifts.

### 2. Model Description
- Random Forest with `class_weight=balanced` to address class imbalance.
- Trained on ~5M rows; evaluated on 1.3M test samples.

### 3. Feature Selection
- Selected numerical and encoded categorical features.
- Created meaningful derived features from balances.

### 4. Model Evaluation
- Achieved strong fraud detection with high precision and recall.

### 5. Key Predictors
- `type_encoded`, `amount`, `oldbalanceOrg`, and balance differences.

### 6. Do the Factors Make Sense?
- Yes — fraudulent transactions tend to involve large transfers or withdrawals from accounts with high balances.

### 7. Recommended Prevention
- Real-time ML fraud detection
- Alerts for suspicious balance drops
- Multi-factor authentication for large transfers

### 8. Measuring Effectiveness
- Monitor fraud rate post-implementation
- Track detection precision and recall
- Use A/B testing with flagged transactions

## 📁 Files Included

- `Fraud_Detection_Analysis.ipynb` – Full notebook with code and analysis
- `README.md` – Project summary


