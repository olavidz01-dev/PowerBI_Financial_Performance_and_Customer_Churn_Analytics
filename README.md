# PowerBI_Financial_Performance_Customer_Churn_Analytics
<p align="center">
  <img src="assets/Overview.jpg" width="1000" />
</p>


---


## Business Overview
**Unity Bank** is a financial services institution operating across multiple European markets, including France, Germany, and Spain. The bank serves a diverse customer base with varying financial profiles, credit quality, and engagement levels. It also offers a variety of banking products across consumer and business segments. As part of its digital transformation and customer-centric strategy, the bank aims to strengthen data-driven decision-making across customer engagement, financial performance, and operational risk management.

To support data‑driven decision-making, Unity Bank implemented a PowerBI analytics solution focused on **customer behavior, churn risk, financial exposure, and portfolio performance**. The dashboards enable stakeholders to monitor customer retention, identify high-risk and high-value customers, analyze churn drivers, and evaluate how customer demographics, credit profiles, and product usage influence churn.


---


## Business Problem 
As competition in the banking sector intensifies and customer switching costs increase, **Unity Bank** faces growing pressure to retain customers, protect high-value balances, and proactively manage churn risk.

**1. High Customer Churn with Significant Financial Impact**
- The bank is experiencing a churn rate of over 20%, resulting in the loss of 2,037 customers.
- Churned customers account for approximately $186M in lost balances, posing a serious threat to revenue stability.

**2. Loss of High-Value Customers**
- The high-value churn rate (~25%) indicates that customers with substantial balances are leaving at a disproportionate rate.
- Average churned balances are higher than retained balances, increasing financial exposure.

**3. Inactivity as a Major Churn Driver**
- A large share of churn originates from inactive customers, highlighting poor engagement and weak lifecycle management.
- The bank lacks early-warning indicators to intervene before customers disengage.

**4. Geographic Concentration of Churn Risk**
- Certain regions (notably Germany) show significantly higher churn rates and churned balances.
- Regional performance disparities make it difficult to deploy uniform retention strategies.

**5. Low Product Penetration and Weak Customer Stickiness**
- Most customers hold only one product, increasing churn susceptibility.
- Customers with fewer products show higher churn likelihood compared to multi-product customers.

**6. Underestimated Risk in Medium-Risk Customers**
- The majority of churned balances come from customers classified as Medium Risk, not High Risk.
- This indicates gaps in the bank’s churn risk classification and prioritization logic.


---


## Project Objectives
The PowerBI project was designed to achieve the following objectives:

**1. Provide a Unified View of Customer Churn and Risk**
- Develop interactive dashboards that track churn rate, churned balances, risk tiers, and customer activity status in real time.

**2. Identify High-Risk and High-Value Customers**
- Enable business users to quickly isolate customers who combine high balances with elevated churn risk for proactive intervention.

**3. Analyze Churn Drivers Across Key Dimensions**

Assess churn patterns by:
- Geography
- Age group
- Credit score band
- Product usage
- Active vs. inactive status

**4. Support Targeted Retention Strategies**

Equip relationship managers and marketing teams with insights to design segment-specific retention actions, especially for:
- Medium-risk customers
- Inactive customers
- Single-product customers
- Older age segments (45+)

**5. Improve Financial Risk Visibility**
- Quantify the financial exposure of churn by risk tier and customer segment.
- Shift focus from churn volume alone to churn value impact.

**6. Enable Customer-Level Monitoring**
- Provide a customer portfolio view to track individual balances, credit scores, risk tiers, and churn status.
- Support operational decision-making at both strategic and tactical levels.


---


## Data Dictionary and Modelling
- **CustomerID:** Unique customer identifier
- **Surname:** Customer full name (for identification in the portfolio view)
- **CreditScore:** Actual credit score used for segmentation 
- **Geography:** Country of customer (France, Germany, Spain)
- **Gender:** Customer gender (Male, Female)
- **Age:** Exact age of customer
- **Tenure:** How long they have been using the banking service(s)
- **Balance:** Current total account balance held by the customer
- **NumOfProducts:** Number of bank products held by the customer (1–4)
- **HasCrCard:** Indicates if the customer has a credit card (Yes/No)
- **IsActiveMembers:** Indicates if the customer is currently active or inactive
- **EstimatedSalary:** Customer's annual salary
- **Exited:** Indicates if the customer has churned (Yes/No)
- **Age Group:** Customer age category (<25, 25–34, 35–44, 45–54, 55+)
- **CreditScore Band:** Customer credit score range (Poor, Fair, Good, Very Good, Excellent)
- **Churn Risk Score:** Scored risk level (e.g., 0–4 scale) for finer segmentation
- **Balance Band:** Categorized balance ranges (e.g., Low < $50K, Medium $50K–100K, etc.)
- **Churn Risk Tier:** Risk level assigned based on customer behavior or model (Low, Medium, High)
<p align="center">
  <img src="assets/Data_Modelling.png" width="1000" />
</p>


---


## Approach & Methodology
This project was developed entirely using **Microsoft PowerBI**, covering the full analytics workflow — from data cleaning and transformation to modeling, analysis, and visualization. The objective was to analyze customer behavior, churn risk, and portfolio insights using an integrated and interactive PowerBI dashboard solution.
### 1️⃣ Data Cleaning & Transformation (Power BI Power Query)
- Imported raw customer data into **Power BI** using Power Query Editor
- Performed data cleaning and transformation directly in Power BI:
  - Removed duplicates and filtered invalid or missing entries
  - Renamed columns and standardized field formats (e.g., text, numeric, dates)
  - Created **calculated columns** for:
    - `Age Group` (e.g., <25, 25–34, 35–44, etc.)
    - `Credit Score Band` (e.g., Poor, Fair, Good, etc.)
    - `Balance Band` (e.g., Low < $50K, Medium, High, Very High)
    - `Churn Risk Tier` (Low, Medium, High)
    - `Churn Risk Score` (0,1,2,3,4,5)
  - Ensured consistency and data quality for downstream modeling

### 2️⃣ DAX Measures (Power BI)
- Created **custom DAX measures** to support key metrics and business logic, including:
  - `Churn Rate`, `Total Customers`, `Churned Balance`, `Average Churned Balance`, `Average Retained Balance`, etc
- Used **DAX functions** such as:
  - `CALCULATE`, `FILTER`, `DIVIDE`, `AVERAGEX`, `IF`, `VAR`, `COUNTROWS`, `DISTINCTCOUNT`, etc
- Applied calculated measures to support dynamic and filter-aware analysis across customer segments

### 3️⃣ Interactive Visualization & Dashboard Design (Power BI)
Developed a comprehensive suite of interactive dashboards using **Power BI Desktop**

**Visualization Techniques:**
- Used card visuals, bar/column charts, donut charts, heatmaps, and filters/slicers
- Enabled interactive drill-downs by age, region, churn status, and risk score

### 4️⃣ Insight Generation & Business Alignment
- Identified key customer behavior patterns
- Translated findings into **actionable business recommendations**


---


## 🔢 Customer Overview

<p align="center">
  <img src="assets/CustomerDash.png" width="1000" />
</p>

### Top KPIs (Key Performance Indicators)
- Total Customers: 10,000
- Average Balance: $76,486
- Products per Customer: 1.53 on average
- Active Customers: 51.51%
- Median Credit Score: 652

### 📊 Customer Segmentation: Analysis & Insights
**1. By Location**
- France has 50% (5,014) of the total customers.
- Germany and Spain are almost equally represented (~25% each).

**2. By Age Group & Gender**
- Largest age segments:
   - 35–44: 3,981 customers
   - 25–34: 3,222 customers
- Younger segment (<25) is the smallest: only 457 customers
- Gender distribution is balanced across all age groups

**3. By Credit Score Band**
- Majority of customers have fair to poor credit:
   - Fair (580–669): 3,331 customers
   - Poor (<580): 2,362 customers
   - Good (670–739): 2,428 customers
- Only 655 customers have Excellent (800+) scores - just 6.5% of the base

**4. By Number of Products**
- Over 50% have only 1 product
  - 5,084 (1 product)
  - 4,590 (2 products)
- Very few are using 3+ products

**5. By Balance Band**
- High Balance (100k–150k): 3,830 customers
- Low Balance (<50k): 3,692 customers
- Medium (50k-100k): 1,509 customers
- Very High Balance (150k+): 969 customers
- Most balances are clustered at the extremes - either low or high, suggesting a bimodal distribution


### ⚠️ Key Challenges Identified
**1. Low Active Engagement**
- With only 51.51% active customers, nearly half of the customer base is disengaged or dormant.
  - This may contribute significantly to the 20.37% churn rate.

**2. Low Cross-Sell Penetration**
- Over 95% of customers have 1–2 products
  - Suggests missed opportunities for upselling/cross-selling additional financial services (loans, credit cards, investments, etc.)

**3. Weak Credit Quality**
- With a median credit score of 652 and 5,693 customers in Fair or Poor segments, the bank may be carrying higher credit risk.
  - Could impact loan default rates and profitability if not managed


---


## 📊 Churn & Risk Overview

<p align="right">
  <img src="assets/churn1.png" width="1000" />
</p>

### Top KPIs (Key Performance Indicators)
- Churn Rate: 20.37%
- No. of Customers churned: 2.037
- Churned Balance: $186M
- High-Risk Customers: 174
- High-Value Churn Rate: 24.98%
  - Key Risk: Nearly 25% of high-value customers churned, representing a significant financial loss and a priority focus area.

### 🌍 Churn by Location

| Country         | Churn Rate   | Churned Balance    | Key Insight                               |
|-----------------|--------------|--------------------|-------------------------------------------|
| **Germany**     |     32%      |       $97.9M       | Highest churn rate and balance loss       |
| **Spain**       |     17%      |       $29.9M       | Moderate churn, lower financial exposure  |
| **France**      |     16%      |       $57.7M       | Lower churn rate, but large value impact  |

⚠ Germany is a high-risk churn zone, both in terms of volume and financial value.

### Churn by Customer Type
**1. Active vs. Inactive**
- Inactive customers account for 65% of churn, which is only 48% of the base.
- Active customer churn rate = 35%, indicating even active users aren't fully engaged.

**Actionable Insight:** Inactivity is a major churn predictor. There is a need to consider stronger lifecycle management.

### Churn by Product Usage
| No. of Products    | Churn Rate    | No. of Churned     |
|--------------------|-------------- |--------------------|
|   1                |     28%       |        1,409       | 
|   2                |     8%        |        348         |
|   3                |     83%       |        220         | 
|   4                |     100%      |        60          |

Customers with only 1 product are the largest churn group (1,409 customers).

**Caution**

The dataset shows a 100% churn rate for customers with four products. On investigation, this segment has a very small sample size, and all instances are labelled as churned. This appears to be a dataset artifact rather than a realistic banking behavior, so insights from this segment should be interpreted with caution. Strategic focus should remain on 1–3 product customers, where both volume and churn impact are material.

### Churn by Age Group
| Age Group       | Churn Rate    | No. of Churned                        |
|-----------------|-------------- |---------------------------------------|
|   45-54         |     48%       |  Extremely high churn risk            |
|   55+           |     39%       |  Aging segment disengaging            |
|   35-44         |     18%       |  Moderate risk                        | 
|   <25           |     9%        |  Lower churn, oppourtunity to grow    |
|   25-34         |     8%        |   Best-performing segment             |

**Insight:** Mid-to-senior age customers are churning at 2-5x the rate of younger ones.

### Churn by Credit Score Band
| Credit Score Band       |  Churn Rate    |
|-------------------------|----------------|
|  Poor (<580)            |     22%        |
|  Fair (580-669)         |     21%        |
|  very Good (740-799)    |     21%        |
|  Excellent (800+)       |     20%        |
|  Good (670-739)         |     19%        |

**Insight:**

Churn is fairly consistent across credit bands, and no strong correlation between score and churn.

### Churn Balance by Risk Tier

| Risk Tier       |  Churned Balance  |
|-----------------|-------------------|
|  Medium         |     $106M         |
|  low            |     $79.4M        |
|  High           |     $0.2M         |

**Insight:**
- My analysis showed that customers at the highest churn risk tend to have lower balances, meaning they contribute less to direct financial loss.
- The majority of revenue loss actually comes from medium-risk, higher-value customers.
- This highlights the need for differentiated retention strategies.


---


## Financial Performance Summary

<p align="right">
  <img src="assets/Summary.png" width="1000" />
</p>

### KPIs Overview
- Total Customers: 10,000
- Churn Rate: 20.37% (2,037 customers churned)
- Average Retain Balance: $72,745
- Average Churn Balance: $91,109
- Total Balance: $765M
- Geographies: France, Germany, Spain

**Key Insights**
**1. High Churn Rate**
- A churn rate of 20.37% is relatively high, indicating a potential issue in customer retention.
- The average balance of churned customers ($91,109) is higher than that of retained customers ($72,745), suggesting that higher-value customers are churning.

**2. Geographical Distribution**

- Majority of customers are from:
  - France: 5,014 (50.1%)
  - Germany: 2,509 (25.1%)
  - Spain: 2,477 (24.8%)

However, a filtered drill-down shows:
- In Germany, customers under 25 years old, with medium churn risk, are notably present (96 customers).
- Within this filtered segment, gender is almost equally split: 41 males, 36 females.

**3. Age Group Analysis**
- Most customers fall into 35-44 and 25-34 age groups:
  - 35-44: 3,278 retained
  - 25-34: 2,972 retained

- However, <25 age group has the lowest retention (417) and churn (40) proportionally.
- Suggests younger customers are more likely to churn.

**4. Churn Risk Tiers**

- Within the Germany/<25/Medium Risk segment:
  - Most are in Medium Risk tier (77 out of 96).
  - Low (14) and High (5) are negligible.









---

### Department-specific Recommendations
1. **Engineering (critical attention needed)**
- Address causes of 150% turnover: conduct workload audits, enhance leadership support, and improve team morale.
- Offer technical training and recognition programs to boost satisfaction.
2. **Marketing & HR (high turnover areas)**
- Strengthen employee support and engagement.
- Clarify role expectations, career paths, and growth opportunities.
- Reassess workload distribution and team structure.
3. **Sales (strong retention & stability)**
- Analyze and document sales’ successful retention strategies, leadership style, incentives, onboarding, and replicate what works across other departments.
4. **Company-wide**
- Ensure each department receives a tailored retention and performance plan based on turnover rate and average performance score.

---

## Executive Summary
This report analyzes employee performance, compensation, and turnover trends at NextGen Corp to identify risks and opportunities impacting workforce stability and organizational growth. The findings highlight significant retention challenges in Engineering, HR, and Marketing, contrasted with strong stability in Sales. While performance levels are generally consistent across departments, no team has yet reached top-tier performance, indicating opportunities to strengthen performance management and employee development.

Compensation analysis reveals uneven salary distribution across roles, suggesting the need for better alignment with responsibilities, performance, and market benchmarks. Based on these insights, the report recommends targeted retention initiatives, standardized performance evaluation, competitive and equitable pay structures, and stronger employee support programs.

Implementing these actions will help NextGen Corp improve retention, boost productivity, and build a more resilient, high-performing workforce.

---

## Disclaimer
This project is for portfolio and educational display only.

No content may be reused without permission.

---

## Connect With Me
- 💼 **LinkedIn:** (https://www.linkedin.com/in/david-okeleye001/)
- 📧 **Email:** okeleyedavid2021@gmail.com
- 🌐 **Portfolio:** https://bit.ly/3N5c1p7
- 🐙 **GitHub:** https://github.com/olavidz01-dev
