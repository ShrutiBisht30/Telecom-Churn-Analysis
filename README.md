# 📊 Telecom Churn Analysis

## Project Overview
This project analyzes customer churn for a telecom company to identify key drivers of attrition and provide actionable insights for retention strategies.  
It evaluates metrics such as **Churn Rate**, **ARPU**, **CLV**, **MRR**, and **Revenue Impact**, while leveraging a predictive model and an interactive **Power BI dashboard** for executives and teams.

---

## 🎯 Objective
- Evaluate current performance metrics and KPIs.  
- Identify the primary factors driving customer churn.  
- Understand the direction of impact for key variables.  
- Enable targeted retention strategies to improve **Customer Lifetime Value (CLV)**.

---

## 📌 Project Scope
- Analyzes customer demographics, services, tenure, payment mode, and contract duration.  
- Uses **logistic regression** to identify top churn factors.  
- Builds an interactive **Power BI dashboard** for stakeholders.  
- Excludes real-time streaming data and predictive churn scoring (out of scope).

---

## 👥 Key Stakeholders / Audience
- **Executive Leadership:** Strategic decision-making & business impact assessment.  
- **Customer Experience Team:** Design initiatives to enhance satisfaction and retention.  
- **Marketing Team:** Develop targeted campaigns to reduce churn and increase engagement.  
- **Sales Team:** Tailor offerings, strengthen relationships, and support long-term contracts.

---

## 🗂️ Data / Requirements

### Data Source
CSV flat file containing customer churn information and associated variables.

### Key Columns

| Column            | Description |
|------------------|-------------|
| customerID        | Unique ID for each customer |
| gender            | Male/Female |
| SeniorCitizen     | 1 = Yes, 0 = No |
| Partner           | Yes/No |
| Dependents        | Yes/No |
| tenure            | Months with company (0–72) |
| PhoneService      | Yes/No |
| MultipleLines     | Yes/No/No phone service |
| InternetService   | DSL/Fiber optic/No |
| OnlineSecurity    | Yes/No/No internet service |
| OnlineBackup      | Yes/No/No internet service |
| DeviceProtection  | Yes/No/No internet service |
| TechSupport       | Yes/No/No internet service |
| StreamingTV       | Yes/No/No internet service |
| StreamingMovies   | Yes/No/No internet service |
| Contract          | Month-to-month / One year / Two year |
| PaperlessBilling  | Yes/No |
| PaymentMethod     | Electronic check / Mailed check / Bank transfer / Credit card |
| MonthlyCharges    | Monthly charge amount |
| TotalCharges      | Total amount charged |
| Churn             | Yes/No |

---

## 🛠️ Tools & Technologies
- **Power BI:** Data prep, visualization, dashboard development  
- **Power Query:** Data cleaning & transformation  
- **R Integration:** Logistic regression modeling via R Visuals  

---

## ⚙️ Methodology

### Data Preparation
- Imported data into **Power Query** and standardized query names.  
- Removed ~1% missing values in *TotalCharges* (new customers not billed yet).  
- Standardized categorical columns (e.g., “No internet service” → “No”).  
- Converted *SeniorCitizen* column from 1/0 to Yes/No for clarity.

### Data Modeling / Calculations
- Single consolidated table for modeling.  
- Key **DAX Measures**:
  - **Churn Rate (%)**  
  - **ARPU**  
  - **Average Revenue**  
  - **Average Tenure**  
  - **Customer Lifetime Value (CLV)**  
  - **Revenue Impact (%)**

### Predictive Modeling
- **Logistic Regression** implemented via **R Visual** in Power BI.  
- Top 10 factors driving churn identified based on **p-values**.  
- Coefficient signs used to interpret direction of effect (positive = increases churn, negative = reduces churn).  

---

## 📈 Visualization / Dashboard

### Executive Summary
- **Card visuals** for key metrics: Churn %, MRR, CLV, ARPU.  
- **R Visual/Table visual** showing top 10 churn factors with positive/negative impact.  
- **Bar/Column charts**: Churn % across tenure groups & payment modes.  
- **Pie charts**: Contract type contribution to churn.  

### Services Page
- **Bar/Column charts**: Churn % & Revenue Impact % across service categories.  
- **Bookmarks**: App-like interactivity to toggle between variables.  

### Demographics Page
- **Bar/Column charts**: Churn % & Revenue Impact % across demographic factors.  
- **Bookmarks**: Interactive exploration of demographic variables.

### Model Performance 
- **Dedicated page** for reviewing model metrics.

---

## 💡 Key Insights & Recommendations
- **Tenure**: Customers in the first 0–6 months have highest churn. Focus retention campaigns here. Reward long-term customers with discounts or benefits.  
- **Monthly Charges**: Higher charges increase churn. Consider bundled offerings or value-added perks.  
- **Contract Type**: Longer-term contracts reduce churn. Incentivize 12- or 24-month commitments.  
- **Add-on Services**: Streaming & other add-ons reduce churn. Cross-selling can improve retention.

---

## 📝 Conclusion
This analysis provides a detailed understanding of telecom customer churn and its key drivers.  
The combination of **logistic regression modeling** and an **interactive Power BI dashboard** equips stakeholders to:  
- Proactively reduce churn  
- Optimize revenue  
- Improve customer lifetime value  
- Design targeted retention initiatives and data-driven strategies  
