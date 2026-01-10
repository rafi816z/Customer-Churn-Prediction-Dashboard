# Customer Churn Prediction Dashboard (Power BI + ML)

## 🧩 Business Problem

Telecom companies face high customer churn, which directly impacts recurring revenue and profitability. With a churn rate of ~26%, the business lacks a proactive, data-driven way to identify customers who are likely to leave, understand the key drivers behind churn, and estimate the revenue at risk.

Current retention strategies are largely reactive and applied broadly, leading to inefficient use of discounts and missed opportunities to retain high-value customers.

This project addresses the problem by using Machine Learning and Power BI to predict customer churn, identify high-risk segments, explain why customers churn, and support data-driven retention and revenue optimization decisions.

---

## 🎯 Business Objective

The objective of this project is to:
- Predict customer churn probability using Machine Learning  
- Identify high-risk customers early in their lifecycle  
- Understand key churn drivers across contracts, tenure, pricing, and services  
- Estimate revenue at risk due to potential churn  
- Enable scenario-based retention and discount optimization  

This enables the business to shift from reactive churn analysis to proactive, targeted customer retention.


## ⭐ Project Overview
This project integrates **Power BI** with **Machine Learning** to predict customer churn, identify high-risk segments, and assess potential revenue loss. Using a Kaggle telecom dataset, an ML model was trained to generate churn probabilities, which were then incorporated into Power BI for interactive visual insights.

The dashboard provides:

- Churn Summary Overview  
- ML-based Churn Drivers & Feature Importance  
- Predictive Retention & Revenue Optimization  

---

## 📂 Dataset
- **Source:** [Kaggle – Telecom Customer Churn Dataset](https://www.kaggle.com/blastchar/telco-customer-churn)  
- **Rows:** ~7,000 customers  
- **Features:** demographics, service usage, contract type, payment method, charges, tenure  

**Data Cleaning Steps:**
- Handled missing values  
- Encoded categorical variables  
- Scaled numeric features  
- Split into train and test sets for model evaluation  

---

## 🔧 Tech Stack
- **Data Analysis & ML:** Python (pandas, scikit-learn, NumPy)  
- **Dashboard & Visualization:** Power BI  
- **Data Source:** Kaggle Telecom Customer Churn Dataset  

---

## 🤖 Machine Learning Model
- **Model Used:** Random Forest Classifier  
- **Why Random Forest?**
  - Captures nonlinear patterns effectively  
  - Handles both categorical and numerical features  
  - Provides interpretable feature importance  
  - High accuracy for churn classification  

**Model Outputs for Power BI Integration:**
- Churn Probability  
- Predicted Churn (Yes/No)  
- Feature Importance Values  

**Integration Method:**  
The ML model was trained in Python, and scoring results were exported as a CSV for use in Power BI.

---

## 📊 Dashboard Breakdown

### 🟦 Page 1 — Telecom Churn Summary Dashboard
**Key Metrics:**
- Total Customers: 7,043  
- Customers Churned: 1,869  
- Churn Rate: 26.54%  
- Avg. Monthly Charges: $64.76  

**Visual Highlights:**
- **Donut Chart – User Status Overview:** Split between active and churned users  
- **Phone Service vs Churn Rate:** Higher churn among multiple lines or certain phone services  
- **Contract Type Analysis:** Month-to-month customers show significantly higher churn  
- **Customer Loyalty with Tenure:** Churn probability decreases with tenure  
- **Churn Distribution Across Online Services:** Treemap showing correlations with churn  

---

### 🟦 Page 2 — Customer Risk & Churn Drivers
**Key KPIs:**
- High-Risk Customers: 26.17%  
- Average Churn Probability: 34.29%  
- Total Revenue at Risk: ~$145.09K  

**Visual Highlights:**
- **Customer Distribution by Risk Level:** Low, medium, and high churn probability segments  
- **Churn Drivers by Customer Attributes:** Decomposition tree to identify drivers by gender, contract, service type, and tenure  
- **Top 10 Features (ML Output):**
  - TotalCharges
  - tenure
  - MonthlyCharges
  - Contract_Two year
  - InternetService_Fiber optic
  - PaymentMethod_Electronic check
  - Contract_One year
  - gender_Male
  - OnlineSecurity_Yes
  - TechSupport_Yes
- **Revenue at Risk Across Contract Types:** Month-to-month contracts contribute most to potential revenue loss  

---

### 🟦 Page 3 — Predictive Retention & Revenue Optimization Dashboard
**Key Metrics:**
- Average Customer Lifetime Value (CLV): $2.10K  

**Visual Highlights:**
- **Discount-Adjusted Churn Probability:** Slider to simulate discount % and see churn decrease by tenure group  
- **Churn Probability by Tenure Groups:** Most vulnerable are 0–12 months  
- **Churn Probability vs Lifetime Value:** Prioritize customers with highest ROI potential  
- **Churn Probability After Discount (by Contract & Tenure):** Shows combined effect of discounts on predicted churn  

**Purpose:** Scenario planning and simulation tool for optimizing retention strategies  

---

## 💼 Business Impact
- **Identify High-Risk Customers:** Targeted retention strategies for customers likely to churn  
- **Revenue Optimization:** Understand revenue at risk for smarter campaigns  
- **Understand Why Customers Leave:** Insights from feature importance and churn drivers (e.g., higher monthly charges, shorter tenure, month-to-month contracts, fiber optic complaints)  
- **Improve Customer Lifetime Value:** Simulation tools test discounts and retention incentives for maximum ROI  

---
## 🔍 Overall Insights

- **Churn is heavily concentrated among month-to-month customers**, making contract type the strongest churn driver. Customers on long-term contracts show significantly lower churn probability and higher loyalty.
- **Early-tenure customers (0–12 months) have the highest churn probability**, indicating that the onboarding and initial service experience play a critical role in customer retention.
- **Higher Monthly Charges and Total Charges strongly correlate with churn**, suggesting price sensitivity among customers with higher billing amounts—especially those using fiber optic services.
- **Electronic Check payment method users exhibit the highest churn**, pointing to potential billing friction, convenience issues, or demographic differences influencing payment behavior.
- **Fiber optic internet users churn more frequently than DSL users**, which may indicate dissatisfaction related to service quality, reliability, or cost.
- **Approximately 26% of customers fall into the high-risk category, but they account for nearly 40% of total revenue at risk**, underscoring the need for targeted retention efforts for this segment.
- **Revenue at Risk is highest for month-to-month customers**, reinforcing the importance of offering loyalty incentives, discounts, or contract upgrade offers to prevent churn.
- **Discount simulation analysis shows the greatest reduction in churn probability for customers with high charges and low tenure**, demonstrating that targeted, data-driven retention incentives provide the highest ROI.
- **Long-tenure customers show strong stability**, suggesting that improving early customer experience could significantly reduce overall churn rates.

