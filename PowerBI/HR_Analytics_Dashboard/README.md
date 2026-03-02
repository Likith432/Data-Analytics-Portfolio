# 👥 HR Analytics Dashboard

## 📌 Project Overview

This Power BI dashboard analyzes employee attrition patterns and workforce demographics to help HR teams identify turnover drivers and improve employee retention strategies.

The dashboard provides insights into attrition trends by age, salary, job role, education, and years at company.

---

## 🎯 Business Objective

The purpose of this dashboard is to:

* Monitor overall employee attrition
* Identify high-risk employee groups
* Analyze job satisfaction impact on turnover
* Understand salary and tenure-based attrition patterns
* Support data-driven HR decision making

---

## 🗂 Dataset Information

Dataset Used: `HR_Analytics.csv`

The dataset contains:

* Employee demographics (Age, Gender, Education)
* Job details (Job Role, Department, Salary Slab)
* Years at Company
* Attrition status
* Job Satisfaction levels

This is a **single structured employee dataset**, suitable for direct aggregation modeling.

---

## 📈 Key KPIs

| KPI                      | Value |
| ------------------------ | ----- |
| Employee Count           | 1.47K |
| Attrition Count          | 237   |
| Attrition Rate           | 16.1% |
| Average Age              | 37    |
| Average Salary           | 6.5K  |
| Average Years at Company | 7     |

These KPIs provide a snapshot of workforce health.

---

## 📊 Dashboard Analysis & Insights

### 🔹 Attrition by Gender

* Male attrition higher than female.
* Indicates possible job-role or department concentration among male employees.


### 🔹 Attrition by Age Group

* Highest attrition in 26–35 age group.
* Young professionals show higher turnover.

📌 Suggests early-career retention strategies needed.


### 🔹 Attrition by Education

* Life Sciences (38%) highest attrition
* Medical (27%)
* Marketing & Technical follow

📌 Skill-based role pressure may influence turnover.


### 🔹 Attrition by Salary Slab

* Majority attrition in salary ≤ 5K
* Significant drop as salary increases

📌 Compensation strongly influences retention.


### 🔹 Attrition by Years at Company

* Peak attrition at early tenure (1–3 years)
* Declines with longer tenure

📌 Critical retention window: First 2–3 years.


### 🔹 Attrition by Job Role

Highest attrition observed in:

* Laboratory Technician
* Sales Executive
* Research Scientist

📌 Operational & sales roles face higher turnover pressure.


### 🔹 Job Satisfaction Analysis

Matrix analysis shows lower satisfaction levels correlate with higher attrition.

📌 Employee engagement programs may reduce churn.

---

## 💡 Key Business Insights

1. Attrition Rate is 16.1% – moderate but improvable.
2. Early-career employees (26–35) are most vulnerable.
3. Low salary slab employees drive majority of exits.
4. Technical and Sales roles face higher churn.
5. Employee satisfaction plays a major role in retention.

---

## 🛠 Tools & Technologies

* Power BI Desktop
* DAX Measures
* Calculated Columns
* Interactive slicers & department filters
* Matrix & trend visualizations
