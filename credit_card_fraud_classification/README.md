# 💳 Credit Card Fraud Detection

A classification project focused on detecting fraudulent credit card transactions using advanced machine learning models including XGBoost, LightGBM, CatBoost, and an ensemble Voting Classifier. This project handles real-world challenges such as highly imbalanced data and high-cardinality categorical features.

---

## 📁 Project Structure

```
📂 Credit_Card_Fraud_Detection/
├── Credit Card Fraud Detection Project EDA.ipynb       # EDA and insights
├── 1. Credit Card Fraud Detection Modeling XGBoost.ipynb
├── 2. Credit Card Fraud Detection Modeling LightGBM.ipynb
├── 3. Credit Card Fraud Detection Modeling CatBoost.ipynb
├── 4. Credit Card Fraud Detection Modeling with Voting.ipynb
├── DS Project - Credit Card Fraud Detection.pptx       # Final presentation
└── README.md                                           # This file
```

---

## 🔍 Project Overview

Credit card fraud costs billions annually. Common fraud tactics include:

- Phishing attacks via email/SMS
- Breaches of retailer databases
- Disputing legitimate charges (friendly fraud)

Visa and Mastercard apply **strict fraud thresholds**, imposing **fines** if exceeded. For example, Visa fines start at **$10,000/month** once fraud exceeds 0.65–1.80% of total monthly volume.

This project tackles fraud detection using supervised learning on a real-world style dataset.

---

## 🧾 Dataset Info

- 📂 Source: Kaggle (simulated dataset)
- 📆 Period: 2020–2022
- 🧮 Size: 1.3M rows (train), 0.5M (test), 23 columns
- 🎯 Target: `is_fraud` (1 = fraud, 0 = not fraud)
- ⚠️ Imbalance: Only **0.58%** of transactions are fraud

Columns include transaction details, customer demographics, merchant info, etc.

---

## 📊 Key EDA Highlights

- Fraud is more likely in transactions between **$500–$1000**
- Night-time (22:00–03:00) has the highest fraud activity
- **Shopping_net** and **Shopping_pos** are top fraud categories
- Top 3 categories account for **58% of fraud** but only **23% of all transactions**
- City population, gender, and job features had low predictive power
- Feature engineering created `age`, `hour`, `day_of_week`, and `month`

---

## ⚙️ Preprocessing & Feature Engineering

- Dropped columns: `trans_date_trans_time`, `cc_num`, `first`, `last`, `street`, `zip`, `dob`, `trans_num`, `lat`, `long`, `merch_lat`, `merch_long`
- One-hot encoding used for all categorical features → expanded to **2151 columns**
- Data saved as Parquet for memory efficiency
- Downsampling performed to address class imbalance

---

## 🤖 Models Used

- XGBoost
- LightGBM
- CatBoost
- VotingClassifier (ensemble)

### Strategy

- Custom hyperparameter tuning for each model
- Metrics focused on **precision and recall**
- **50% downsampling** yielded best results
- `shap` used for interpretability and feature importance
- Manual tuning due to memory limits

---

## 📈 Final Results

- All models performed similarly
- **LightGBM** was significantly faster and most balanced
- Top features included: `category`, `amount`, `hour`, `merchant`, and engineered features

---

## 🚧 Challenges

- **Memory issues** due to large one-hot encoded dataset
- LightGBM required sanitizing column names with special characters
- Kernel restarts needed frequently during tuning

---

## ✅ Conclusion

- Fraud detection on highly imbalanced data is complex but solvable with careful preprocessing and model tuning
- **LightGBM** is the preferred model for this dataset
- Ensemble models did not outperform single best models
- Precision/recall trade-off is critical for real-world fraud prevention

---

## 👤 Author

**Aleksander Tanskii**  

---

If you’re working on a fraud detection system, feel free to explore, fork, or contribute. Let’s catch those fraudsters! 🕵️‍♂️💸
