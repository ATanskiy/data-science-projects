# 🚗 Car Insurance Fraud Detection

This project aims to detect **fraudulent car insurance claims** using classical and ensemble machine learning classification techniques. The project walks through all the major steps in a real-world data science pipeline: from EDA to preprocessing, modeling, and evaluation.

---

## 📁 Project Structure

```
📂 Car_Fraud_Classification/
├── EDA_car_claims.ipynb             # Exploratory Data Analysis
├── Modeling_Car_Claims.ipynb        # ML model development and evaluation
├── fraud_vihecles.csv               # Raw dataset
├── DS Project - Classfication Tanskii Alexander.pptx  # Project presentation
└── README.md                        # Project summary and instructions
```

---

## 📊 Project Overview

Insurance fraud is a growing challenge, with nearly 1 in 10 Americans admitting they would commit fraud if they could get away with it. This results in billions in losses and higher premiums for honest customers. Detecting fraud early can significantly reduce operational costs and improve service quality.

This project uses **supervised machine learning** to detect fraud in a real dataset of car insurance claims.

---

## 📌 Dataset Info

- 📂 Source: [Kaggle Dataset](https://www.kaggle.com)
- 📅 Years: 1994-1996
- 📈 15,420 records and 33 features
- 🎯 Target variable: `FraudFound_P` (1 = fraud, 0 = not fraud)
- 🔢 9 numeric and 24 categorical columns (many encoded as numeric but are actually categorical)

---

## 🔎 Exploratory Data Analysis Highlights

- Fraud cases make up **5.99%** of all claims
- **Gender, marital status, vehicle type**, and **age of policy holder** show strong associations with fraudulent behavior
- Heatmaps reveal high fraud patterns in:
  - Males aged 31–35
  - Vehicles priced $20K–$30K
  - Policyholders with older vehicles
  - Specific makes (Pontiac, Toyota, Honda)

---

## 🛠️ Preprocessing and Feature Engineering

- Dropped: `PolicyNumber`, `Age`
- One-hot encoding for categorical features
- Feature creation (e.g., Season) explored but not used
- SMOTE and downsampling applied to address class imbalance

---

## 🤖 Models and Strategy

- Models Used:
  - Logistic Regression
  - Decision Tree
  - Random Forest
  - XGBoost
  - CatBoost
  - Voting Classifier (ensemble of above)
  - KNN and SVM (tested, discarded)

- Pipeline:
  - Custom pipeline per model
  - GridSearchCV for hyperparameter tuning
  - Evaluation with F1 and F-beta metrics
  - Nested loops with SMOTE and CV splits to optimize parameters

---

## 🧪 Final Results

- Tree-based models (XGBoost & CatBoost) outperformed others
- Logistic Regression, Random Forest, and Decision Tree underperformed
- VotingClassifier did not improve results
- Overfitted model with label encoding performed the best (not production safe)

---

## 📉 Limitations & Challenges

- Severe class imbalance despite SMOTE
- Difficulty finding optimal hyperparameters
- Overfitting models produced better results, indicating data/model limitations

---

## 📌 Conclusions

- Detecting insurance fraud is **non-trivial** and requires careful handling of imbalanced data
- XGBoost and CatBoost are promising but **still insufficient for reliable deployment**
- More data and domain-specific features might improve performance

---

## 👤 Author

**Aleksander Tanskii**  

---

🚨 If you're working on fraud detection in insurance or similar domains, this project might be a helpful reference. Feel free to fork, modify, or reach out with suggestions!
