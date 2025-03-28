# 🏦 Loan Amount Prediction – Regression Project

This project tackles a regression problem involving **loan sanction amount prediction** based on applicant information such as income, expenses, credit score, employment status, and property type. The data cleaning, preprocessing, feature engineering, and model comparisons are all done to optimize prediction performance.


---

## 📁 Project Structure

```
📂 Loan_Amount_Regression/
├── Regression Project Aleksander Tanskii.ipynb   # Full analysis and modeling
├── train.csv                                     # Dataset (from Kaggle)
├── Regression Project Loan.pptx                  # Final presentation
└── README.md                                     # Project summary
```

---

## 🔍 Problem Statement

Predict the **Loan Sanction Amount (USD)** based on a dataset of loan applicants, originally designed for a HackerEarth ML competition.

---

## 🧾 Dataset Overview

- 📂 Source: [Kaggle Dataset](https://www.kaggle.com/datasets/phileinsophos/predict-loan-amount-data/data)
- 📊 Size: 30,000 rows, 24 columns
- 🎯 Target variable: `Loan Sanction Amount (USD)`
- 🏷️ Features: Age, Income, Expenses, Credit Score, Profession, Income Stability, Property Location, etc.
- ⚠️ Missing and anomalous values (e.g., -999) were found and handled during EDA

---

## 🧹 EDA and Preprocessing

- ✅ Removed outliers (loan amounts > $300K, negative expenses, age 18 anomalies)
- ✅ Imputed missing values using profession medians or property location modes
- ✅ Cleaned rows with -999 in the target column
- 🧼 Final dataset size: **28,044 records** (after ~6% cleanup)

---

## 🛠️ Feature Engineering

- Created `age_group` column to reflect age distribution effects
- Applied **log transforms** to skewed numerical variables
- Scaled numerical features
- Used `get_dummies()` for all categorical variables

---

## 🤖 Models Used

### Linear Regression

| Config | RMSE Train | RMSE Test |
|--------|-------------|-----------|
| All features, scaling/logs | 29,361 | 29,914 |
| Numerical only, no logs | 27,216 | 27,298 |
| Numerical only, log-transformed, 0s removed | 5,189 | 5,112 |

### Decision Trees

| Config | RMSE Train | RMSE Test |
|--------|-------------|-----------|
| All features, scaling/logs | 21,707 | 21,859 |
| Numerical only, log-transformed, 0s removed | 4,856 | 5,013 |

💡 The Decision Tree with minimal preprocessing gave the **best result** with the lowest RMSE.

---

## 📈 Insights & Learnings

- Removing 0s from the target and applying logs significantly improved model accuracy
- Simpler models (e.g., Decision Tree without full encoding) can outperform more complex ones
- Proper handling of outliers and missing values is critical in real-world regression problems

---

## 👤 Author

**Aleksander Tanskii**  

---

🔍 Interested in financial data, credit risk modeling, or practical regression use cases? Feel free to explore this project and reuse the workflow!
