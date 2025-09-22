# Predicting Customer Spend and Subscription

## 📌 Project Overview  
This project focuses on predicting two key outcomes for an e-book subscription business:  

1. **Average Monthly Spend** (Regression)  
2. **Subscription Flag** (Classification)  

The analysis was conducted using a real-world styled customer dataset, applying advanced **machine learning models**, **EDA techniques**, and **business intelligence visualizations** to uncover actionable insights.  

The ultimate goal is to support strategic decision-making around **customer acquisition, retention, and revenue growth**.

---

## 🎯 Business Problem  
E-book companies often face two challenges:  
- **Understanding customer spend behavior** to identify high-value segments.  
- **Predicting subscription likelihood** to increase conversion and retention.  

By modeling customer spend and subscription probability, this project provides data-driven recommendations for **marketing, pricing, and product strategy**.

---

## 📊 Dataset Description  
- **Rows:** 16,519  
- **Original Features:** 21  
- **Final Features (after cleaning):** 15  

### Key preprocessing steps:
- Removed personal identifiers (names, addresses, IDs).  
- Engineered new features from `City-ZipCode-State`.  
- Converted `Birth Date` into **Age**.  
- Handled missing values and irrelevant columns.  

**Final dataset includes variables such as:**  
- Demographics: Age, Gender, Marital Status, Education, Occupation.  
- Household: Home Ownership, Number of Cars, Number of Children.  
- Financials: Annual Income, Average Monthly Spend.  
- Subscription: eBook Subscriber Flag.  

---

## 🔬 Methodology / Pipeline  
1. **Data Cleaning & Preprocessing**  
   - Feature engineering (age, city/state split).  
   - Removal of non-informative variables.  

2. **Exploratory Data Analysis (EDA)**  
   - Profiling with *JData Profiling*.  
   - Correlation analysis (Dictum, Autovis).  
   - Tableau dashboards for business storytelling.  

3. **Modeling (PyCaret)**  
   - Regression for *Average Monthly Spend*.  
   - Classification for *Subscription Flag*.  
   - Hyperparameter tuning and performance evaluation.  

4. **Evaluation & Visualization**  
   - Metrics reporting (MAE, RMSE, R², Accuracy, AUC, etc.).  
   - Business insights visualized with Tableau & Autovis.  

---

## 🤖 Models & Results  

### **Average Monthly Spend (Regression – LightGBM)**  
- MAE: **2.51**  
- MSE: **10.12**  
- RMSE: **3.18**  
- R²: **0.98**  

✅ Very strong predictive power, showing that monthly spend can be reliably estimated from demographic and financial features.  

---

### **Subscription Flag (Classification – Gradient Boosting Classifier)**  
- Accuracy: **0.79**  
- AUC: **0.85**  
- Recall: **0.58**  
- Precision: **0.75**  
- F1 Score: **0.65**  

✅ Solid performance with balanced metrics, demonstrating that customer subscription likelihood can be predicted with high confidence.  

---

## 📈 Key Insights  

- **Top correlations with Spend:**  
  - Number of Children at Home (0.73)  
  - Annual Income (0.61)  
  - Gender (0.57)  
  - Total Number of Children (0.50)  

- **Top correlations with Subscription:**  
  - Occupation, Marital Status, Car Ownership.  
  - Subscribers tend to be **aged 44–66**, own **~2 cars**, and are more likely to be homeowners.  
  - Higher subscription rates among **Professionals** and **Management** occupations.  

---

## 📊 Visualizations (Tableau & Autovis)  
- **Spend vs. Children & Home Ownership** – families with more children show higher spend.  
- **Subscription Rate by Occupation & Education** – professionals and college-educated customers dominate subscriptions.  
- **Spend Distribution by Annual Income** – highest spenders earn between $90K–$160K.  
- **Age vs. Subscription Status** – older cohorts more likely to subscribe.  
- **Overall Subscription Rate** – 33% subscribed vs 66% non-subscribed.  

---

## 📂 Project Structure  

```
e-book-data-project/
│
├── Data/                         # Original & cleaned datasets
├── Models/                       # Cluster profiling, anomalies, final models
│   ├── Best Model Training Performance/
│   ├── Average Spend - LightGBM
│   └── Subscription - GBC
│
├── Notebooks/                    # Jupyter notebooks (EDA, ML)
├── Report/                       # PDF & HTML reports
│   ├── Customer Data eBook 2025 (HTML Profiling)
│   └── Predicting Customer Spend & Subscription 2024-25 (PDF)
│
├── SRC/                          # Python scripts version of notebooks
├── Visuals/                      # Tableau dashboards
├── Requirements/                 # requirements.txt
└── README.md                     # This file
```

---

## ⚙️ How to Run  

1. Clone the repository:  
   ```bash
   git clone https://github.com/yourusername/e-book-data-project.git
   cd e-book-data-project
   ```

2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```

3. Run notebooks inside `/Notebooks` for full workflow.  

---

## 🏆 Business Value  

- **Customer Spend Prediction** → supports pricing strategies, identifies high-value segments.  
- **Subscription Prediction** → improves targeting and marketing ROI.  
- **Actionable Insights** → clear drivers of spend & subscription provide guidance for business growth.  

---

✨ This project demonstrates how **machine learning, data analytics, and visualization** can generate strategic insights for a digital subscription business.  
