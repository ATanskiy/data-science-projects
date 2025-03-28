# 🚗 Israeli Private and Business Vehicles – EDA Project

An Exploratory Data Analysis (EDA) project focused on official vehicle data in Israel, using Pandas to uncover trends in vehicle types, import patterns, emission levels, fuel types, and more.

## 📁 Project Structure

```
📂 Israeli_Vehicles_EDA/
├── vehicles_eda_project.ipynb               # EDA notebook with code and charts
├── vehicles_eda_project_presentation.pptx   # Project summary presentation
└── README.md                                # This file
```

---

## 📦 Dataset Information

- 📍 Source: [data.gov.il – Private & Commercial Vehicles](https://data.gov.il/dataset/private-and-commercial-vehicles)
- 📅 Coverage:
  - Private vehicles: manufactured from 1996 onward
  - Commercial vehicles (≤ 3,500 kg): from 1998 onward
- 🧮 Size: Two CSV files with **3.8 million rows** each
- 🔤 Challenges:
  - Many Hebrew-named columns
  - Needed external tools to make data readable for Pandas
  - Some columns had up to 67% missing values (e.g., `safety_upgrade_status`)

---

## 📊 Key Exploratory Findings

### 🧍 Vehicle Ownership
- 85% of all vehicles are privately owned
- Majority have automatic (P) or mechanical (M) transmission

### 📈 Emissions & Environmental Insight
- Cars with higher emissions are declining (esp. post-2016)
- Cleaner models (1.0–5.0 group) are slowly increasing

### 📆 Import & Usage Trends
- 25% of all vehicles are between 1–4 years old
- Sharp import drop in 2020 (COVID-19), bounce back in 2021
- January is consistently the peak month for registering new vehicles

### 🎨 Vehicle Colors
- Top 3: White Ivory (38.5%), Silver (16.5%), Black (12%)
- These top 10 colors account for 82% of all vehicles

### ⚡ Fuel Type Trends
- Electric and Hybrid cars on the rise 🚘⚡
- Diesel vehicles slowly decreasing
- Gasoline remains dominant

### 🌍 Import Countries
- 🇯🇵 Japan led imports historically but declining
- 🇨🇳 China is rising rapidly post-2020
- 🇰🇷 South Korea has shown steady growth since 2010

### 🚘 Brand & Model
- Top 10 brands dominate the market
- Analysis includes most polluting brands by model count

---

## 🛠️ Tools Used

- Python 🐍
- Pandas & NumPy
- Matplotlib & Seaborn
- Jupyter Notebook
- Excel / Hebrew file format tools for preprocessing

---

## 👤 Author

**Aleksander Tanskii**  
---

## 📄 License

This project uses data from the Israeli government portal [data.gov.il](https://data.gov.il), available for public use.

---

Love digging through large datasets with real-world implications?  
Explore, fork, or reach out!
