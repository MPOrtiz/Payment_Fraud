# 🛡️ Fraud Detection with Machine Learning

## 📌 Project Overview

This project focuses on detecting **fraudulent transactions** in e-commerce using **Machine Learning** techniques.
The dataset contains **38,000+ transactions**, labeled as either **normal behavior (0)** or **fraudulent activity (1)**.

The goal is to identify key behavioral patterns of fraud and evaluate different ML models to build a reliable fraud detection system.

---

## 📂 Dataset

* **Transactions:** 38,662
* **Features:**

  * `accountagedays` → Age of the account in days
  * `paymentmethodagedays` → Age of the payment method
  * `numitems` → Number of items purchased
  * `localtime` → Time of purchase (log-transformed)
  * `isweekend` → Weekend activity flag
  * `paymentmethod` → Payment channel (credit card, PayPal, store credit, etc.)
  * `category` → Purchase category (shopping, electronics, food, unidentified)
  * `label` → Target variable (0 = normal, 1 = fraud)

---

## 🔍 Exploratory Data Analysis (EDA)

Key insights from the dataset:

* Fraud is strongly linked to **new accounts (1 day old)** and **new payment methods**.
* Fraudulent activity occurs **almost exclusively on weekdays**, rarely on weekends.
* Fraudulent purchases involve **slightly larger item counts** and occur at **less common transaction times**.
* Normal transactions show **stable patterns across weekdays, weekends, and categories**.

---

## 🤖 Models Used

The following models were trained and evaluated:

* 🌳 **Decision Tree** → Achieved perfect accuracy but showed risks of **overfitting**.
* 🌲 **Random Forest** → Same as Decision Tree; suspiciously perfect metrics, potential memorization.
* 📈 **Logistic Regression** → More realistic baseline; achieved **100% Recall** (detected all fraud) but produced false positives.

**Evaluation Metrics:**

* Accuracy
* Precision, Recall, F1-Score
* ROC-AUC

---

## ⭐ Results

* **Most important features:** `accountagedays` and `paymentmethodagedays`.
* **Logistic Regression** → Best baseline model, ensuring **no fraud is missed** but with false positives.
* **Tree-based models** → Require careful tuning and validation to avoid overfitting.
* Recommended approach: **Gradient Boosting (LightGBM / XGBoost)** for production use.

---

## 📊 Business Value

* Fraud detection is essential to **reduce financial losses** and **protect customers**.
* Models can be integrated into e-commerce systems to **flag suspicious transactions** in real-time.
* Insights about **account and payment method age** help businesses design **preventive strategies**.

---

## 🚀 Next Steps

* Apply **hyperparameter tuning** and **cross-validation**.
* Experiment with **Gradient Boosting models (LightGBM, XGBoost, CatBoost)**.
* Use **SHAP values** for explainability.
* Deploy the model into a production pipeline for real-time fraud detection.

## ✨ Author

👩‍💻 Developed by **\[Martha Patricia]**
📍 Focus: Data Science | Machine Learning 
