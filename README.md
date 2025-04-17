# Fraud Detection and Financial Transaction Analysis Using Snowflake, Machine Learning, and Tableau

## Overview

This project leverages **Snowflake**, **Machine Learning**, and **Tableau** to uncover valuable insights from financial transaction data. Key focus areas include **customer segmentation**, **fraud risk analysis**, and **transaction behavior patterns**. This analysis provides actionable intelligence to support **marketing strategy**, **fraud prevention**, and **revenue optimization**.

---

## Data Analysis for Transaction Insights

The dataset includes critical variables such as:

- `Transaction_Amount`
- `Customer_ID`
- `Merchant_ID`
- `Transaction_Type`
- `Is_Fraud`
- `Fraud_Risk_Score`

Key analysis sections:

- **Customer Spending Insights**
- **Fraud Prediction Counts**
- **Transaction Type and Amount Analysis**

---

## Data Analysis using Snowflake

### **Customer Spending Insights Query**

![Customer Spending Insights Query](https://github.com/lewis-hue/Fraud-Detection-Financial-Transaction-Analysis-Snowflake-/blob/main/Customer%20Spending%20Insights%20Data.png)

**Query Output Table:**

| AMOUNT_RANGE | NUM_CUSTOMERS |
|--------------|---------------|
| 50–100       | 10            |
| 101–200      | 18            |
| 201–300      | 24            |
| 301–400      | 18            |
| 401–500      | 21            |

#### 🔍 Analysis:

- The highest concentration of customers (24) falls within the $201–$300 range.
- High-value customers (spending $401–$500) account for **24% of total customers**, indicating a strong upper-tier.
- Customers spending below $200 represent only 28 individuals, a smaller and lower-yielding segment.

#### 💼 Business Implications:

- **High-value segmentation**: Launch exclusive campaigns targeting the 21 top spenders with premium incentives or loyalty programs.
- **Upselling Opportunity**: Customers in the $201–$300 range could be incentivized to move up tiers via bundled offers or cashback campaigns.
- **ROI-Driven Marketing**: Targeted marketing towards high-LTV segments improves acquisition cost efficiency and overall customer retention.

---

### **Fraud Prediction Count Query**

![Fraud Prediction Count Query](https://github.com/lewis-hue/Fraud-Detection-Financial-Transaction-Analysis-Snowflake-/blob/main/Fraud%20Prediction.png)

**Query Output Table:**

| FRAUD_RISK_SCORE | COUNT_OF_TRANSACTIONS |
|------------------|-----------------------|
| 0                | 150                   |
| 1                | 45                    |
| 2                | 20                    |
| 3                | 5                     |

#### 🔍 Analysis:

- **68%** of transactions are low-risk (score 0), while **11.4%** fall into high-risk brackets (score 2–3).
- Score 3 transactions, although rare (5 total), require **immediate attention** for fraud prevention.
- Score 1 transactions (45) are low priority but still warrant trend monitoring.

#### 💼 Business Implications:

- **Operational Efficiency**: Focus human review on just 25 high-risk transactions out of 220—maximizing fraud prevention efforts while reducing false positives.
- **Real-Time Monitoring**: Implement dynamic dashboards that alert fraud teams of any sudden increase in Score 2–3 activity.
- **Cost Control**: Automate low-risk transactions (Score 0) to reduce overhead from unnecessary manual checks.

---

### **Transaction Type and Amount Query**

![Transaction Type and Amount Query](https://github.com/lewis-hue/Fraud-Detection-Financial-Transaction-Analysis-Snowflake-/blob/main/Staging%20the%20Raw%20Transaction%20Data.png)

**Query Output Table:**

| TRANSACTION_TYPE | TOTAL_AMOUNT |
|------------------|--------------|
| Purchase         | $150,000     |
| Refund           | $20,000      |
| Exchange         | $5,000       |

#### 🔍 Analysis:

- Purchases account for **85.7%** of transaction volume, indicating strong sales conversion.
- Refunds and exchanges contribute to **14.3%**, which may point to **product dissatisfaction** or **policy abuse**.

#### 💼 Business Implications:

- **Revenue Protection**: High refunds ($20,000) suggest reviewing return policies and product QA for recurring issues.
- **Customer Experience Strategy**: Analyze exchange data by product/merchant to improve satisfaction and reduce costly reversals.
- **Margin Optimization**: Reducing refunds/exchanges to under 10% could recover an estimated **$7,500** in potential revenue.

---

## Data Visualization by Tableau

### **Customer Spending Insights**

![Customer Spending Insights](https://github.com/lewis-hue/Fraud-Detection-Financial-Transaction-Analysis-Snowflake-/blob/main/Customer%20Spending%20insights%20Dashboard.png)

- The dashboard highlights dominant customer segments and their spending ranges.
- Enables filtering and targeted cohort analysis for marketing strategy development.

---

### **Fraud Prediction Count**

![Fraud Prediction Count](https://github.com/lewis-hue/Fraud-Detection-Financial-Transaction-Analysis-Snowflake-/blob/main/Fraud%20Prediction%20count%20Dashboard.png)

- Real-time visibility into fraud score distributions.
- Designed for fraud analysts to prioritize resources effectively.

---

### **Transaction Type and Amount**

![Transaction Type and Amount](https://github.com/lewis-hue/Fraud-Detection-Financial-Transaction-Analysis-Snowflake-/blob/main/Transaction%20Type%20and%20Amount%20dashboard.png)

- Compares volume of purchases vs refunds/exchanges.
- Spot trends and anomalies in transaction behaviors to support business decision-making.

---

## 📌 Summary of Key Takeaways

| Insight Area             | Key Finding                                                             | Recommended Action                                                              |
|--------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Customer Segmentation    | 21 customers in $401–$500 bracket (24%)                                  | Launch premium loyalty programs to boost retention and LTV                      |
| Fraud Risk Monitoring    | 11.4% of transactions flagged as medium/high risk                        | Prioritize manual review of Score 2–3 transactions                              |
| Refund/Exchange Analysis | Refunds and exchanges total $25,000 (14.3% of total volume)              | Optimize return policies and improve product quality to reduce lost revenue     |

---

## Conclusion

This project demonstrates how a modern data stack—powered by **Snowflake**, **machine learning**, and **Tableau**—can provide deep operational and strategic insights into transactional behavior. It supports proactive fraud detection, refined customer segmentation, and smarter business decisions.

Let me know if you'd like to explore more advanced features like:

- Real-time fraud alert systems
- Predictive modeling of customer spend
- Merchant-level risk profiling
- Time-series forecasting of transactional patterns

---
