# Customer Churn Prediction Project

**End-to-End Data Science Portfolio Project**

---

# Project Overview

Customer churn is one of the most critical business challenges in subscription-based industries such as telecommunications, SaaS, and financial services. Retaining existing customers is significantly more cost-effective than acquiring new ones.

This project analyzes telecom customer data to:

* Understand churn behavior
* Identify key churn drivers
* Quantify revenue at risk
* Prepare features for predictive modeling
* Build a deployable churn prediction system

This repository documents the complete workflow from data cleaning through exploratory data analysis (EDA), with modeling and deployment to follow.

---

## Data Source

**Dataset:** Telecom Customer Churn Dataset
**Type:** Customer-level subscription and behavioral data
**Records:** 6,920 customers
**Scope:** Multi-feature telecom dataset containing demographic, geographic, financial, and service usage information.

The dataset includes real-world structured customer data commonly seen in telecom churn modeling projects. It was cleaned and transformed to prepare it for analysis and machine learning modeling.

Processed dataset location:

```
data/cleaned/cleaned_telecom_customer_churn.csv
```

---

## Business Objective

The primary business goals of this project are:

1. Identify factors that influence customer churn.
2. Detect high-risk customer segments.
3. Estimate revenue lost due to churn.
4. Prepare engineered features for predictive modeling.
5. Enable data-driven retention strategies.

---

## Dataset Description

The dataset contains the following categories of information:

### Demographics

* Age
* Gender
* Married
* Number of Dependents

### Geographic Information

* City
* Zip Code
* Latitude / Longitude

### Service Usage
* Phone service
* Multiple lines
* Internet Service
* Internet Type
* Streaming TV / Movies / Music
* Online Security / Backup
* Device Protection Plan
* Premium Tech Support
* Unlimited Data
* Average Monthly GB Download

### Financial Information

* Monthly Charge
* Total Charges
* Total Revenue
* Refunds
* Contract Type
* Payment Method

### Target Variable

* Customer Status (Stayed / Churned)

---

## Data Cleaning (Completed)

The dataset was thoroughly cleaned before analysis to ensure quality and reliability.

### Cleaning Steps Performed:

* Removed duplicate customer records
* Standardized categorical values
* Validated logical consistency
   - Verified revenue alignment with tenure × monthly charges
   - Checked service dependency logic (internet & streaming)
   - Identified zero-tenure billing inconsistencies
   - Confirmed contract-duration consistency
   - Validated no negative or impossible numeric values
* Checked for invalid or unrealistic values
   - checked for and removed outliers in revenue 
* Ensured no remaining critical missing data

This process transformed raw structured data into a modeling-ready dataset.

---

##  Exploratory Data Analysis (Completed)

EDA was conducted in a structured, business-driven manner.

---

### 1️⃣ Dataset Overview

* Confirmed dataset dimensions and structure
* Analyzed churn distribution
* Identified class imbalance considerations

---

### 2️⃣ Target Variable Analysis

* Overall churn rate calculated
* Breakdown of churn categories
* Top churn reasons identified
* Revenue lost due to churn estimated

Key Insight:
Churned customers represent a measurable portion of total revenue at risk.

---

### 3️⃣ Demographic Insights

Analyzed churn patterns by:

* Age
* Marital status
* Number of dependents

Findings indicate demographic characteristics influence retention behavior.

---

### 4️⃣ Financial Analysis

Explored:

* Monthly Charge distribution
* Total Revenue patterns
* Refund behavior
* Revenue concentration

Key Observations:

* Contract length strongly impacts churn probability.
* Customers with higher monthly charges show slightly elevated churn risk.
* Revenue contribution varies significantly across tenure groups.

---

### 5️⃣ Contract & Payment Behavior

* Month-to-month contracts exhibit higher churn rates.
* Long-term contracts improve retention.
* Auto-payment methods correlate with lower churn risk.

---

### 6️⃣ Service Engagement Patterns

Created analytical features to measure service engagement (e.g., total subscribed services).

Insight:

Customers subscribed to multiple services demonstrate lower churn probability, suggesting stronger product integration reduces churn risk.

---

### 7️⃣ Correlation Analysis

* Converted churn to binary for numeric correlation analysis.
* Identified preliminary predictive drivers such as contract type, tenure-related metrics, and service engagement.

---

## 🛠 Tools & Technologies Used

* Python
* Pandas
* NumPy
* Plotly (interactive visualizations)
* Seaborn / Matplotlib
* Jupyter Notebook

---

## 📁 Repository Structure

```
customer-churn-project/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   └── 02_exploratory_data_analysis.ipynb
│
├── requirements.txt
└── README.md
```

---

## 🚀 Next Steps

Upcoming stages of the project:

* Feature Engineering
* Class Imbalance Handling
* Baseline Model (Logistic Regression)
* Advanced Models (Random Forest, XGBoost)
* Model Evaluation (ROC-AUC, Precision-Recall)
* SHAP Explainability
* Optional Deployment (Streamlit Dashboard)

---

## 👤 Author

**Daniel Inioluwa**
Entry-Level Data Scientist
B.Eng. Civil Engineering

Focused on building end-to-end, business-oriented machine learning systems.

---

## 🎓 Project Purpose

This project demonstrates:

* Real-world data wrangling
* Structured exploratory data analysis
* Business-focused insight extraction
* Proper repository organization
* Preparation for production-ready modeling

This README will be updated progressively as the project advances through modeling, evaluation, and deployment stages.
