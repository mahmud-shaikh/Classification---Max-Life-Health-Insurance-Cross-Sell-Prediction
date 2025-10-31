# 🧠 Max Life Health Insurance Cross-Sell Prediction

### 📘 Project Overview

This project focuses on predicting whether existing **health insurance customers** are likely to purchase **vehicle insurance**, helping the company improve cross-selling strategies and optimize marketing costs through data-driven targeting.

### 🎯 Objective

To build a **supervised classification model** that identifies high-potential customers for vehicle insurance using demographic, policy, and behavioral data.

### 🧩 Dataset

**Source:** Provided by Max Life Insurance (Sampled Dataset)
**Size:** 381,109 records, 12 columns
**Target Variable:** `Response` → (1 = Interested, 0 = Not Interested)

**Key Features:**

* `Gender`, `Age`, `Driving_License`, `Region_Code`
* `Previously_Insured`, `Vehicle_Age`, `Vehicle_Damage`
* `Annual_Premium`, `Policy_Sales_Channel`, `Vintage`

### ⚙️ Data Preprocessing

* No missing or duplicate values
* Outlier treatment using **log transformation** and **IQR capping** on `Annual_Premium`
* **Label Encoding** for binary features (`Gender`, `Vehicle_Damage`)
* Created new engineered features:

  * `Age_Bin` – grouped age ranges
  * `Risk_Profile` – combined `Vehicle_Damage` & `Previously_Insured`
  * `Premium_per_Day` – premium divided by `Vintage`
  * `Age_Premium_Interaction` – captures effect of age on premium

### 🔍 Exploratory Insights

* Customers with **vehicle damage** are more likely to cross-buy.
* **Older vehicles** and **uninsured customers** showed higher interest in cross-sell offers.
* Policy channels 43 and 123 had the **highest conversion rates**.

### 🤖 Model Building

**Algorithms Tested:** Logistic Regression, Random Forest, XGBoost
**Best Model:** Tuned Logistic Regression (GridSearchCV)
**ROC-AUC:** ≈ 0.63

**Evaluation Metrics:** Accuracy, Precision, Recall, F1-Score, ROC-AUC

### 💡 Key Results

* Model effectively identified high-probability customers.
* Reduced marketing costs by improving targeting efficiency.
* Highlighted data-driven strategies for optimized cross-selling.

### 🏢 Business Impact

* Enabled **targeted marketing** and improved **conversion rate**.
* Demonstrated value of predictive analytics in the **insurance industry**.
* Reduced campaign waste by focusing on **likely buyers**.

### 🛠️ Tools & Libraries

Python • Pandas • NumPy • Scikit-learn • Matplotlib • Seaborn

### 📈 Future Improvements

* Handle imbalance using SMOTE or class weights
* Test ensemble stacking or gradient boosting
* Incorporate customer engagement and claim history data

---
