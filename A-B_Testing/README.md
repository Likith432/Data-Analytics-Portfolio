# 📊 A/B Testing Report – Facebook vs AdWords Campaign Analysis

## 📌 Project Overview

This project evaluates the performance of two digital advertising campaigns — **Facebook Ads** and **Google AdWords** — using statistical analysis and hypothesis testing.

The goal is to determine which platform delivers better performance in terms of:

* Clicks
* Conversions
* Cost-effectiveness
* Return on Investment (ROI)

The findings help optimize marketing budget allocation and improve advertising strategy.

---

## 🎯 Business Problem

* As a marketing agency, our objective is to maximize ROI for clients.
* We conducted parallel campaigns on Facebook and AdWords and needed to determine:
* Which platform is more effective in driving conversions and delivering cost efficiency?

---

## ❓ Research Question

Which ad platform performs better in terms of conversions, clicks, and overall cost-effectiveness?**

---

# 🔬 Methodology

The analysis was performed using daily campaign data for 2019 and included:

### 1️⃣ Data Cleaning & Preparation

* Converted `Date`, `Cost`, and numerical fields to appropriate formats
* Checked for inconsistencies and missing values


### 2️⃣ Distribution Analysis

Analyzed daily clicks and conversions using histograms to understand spread and variability.

<p align="center">
<img src="https://github.com/user-attachments/assets/2a6babb1-885b-4907-bcbd-0d6a7e34d2cc" width="600">
</p>

<p align="center">
<img src="https://github.com/user-attachments/assets/19d35e3b-3025-47b0-a2c6-a158b142e08e" width="600">
</p>


### 3️⃣ Conversion Category Comparison

Grouped daily conversions into categories:

* Less than 6
* 6–10
* 10–15
* More than 15

Facebook showed significantly more high-conversion days.

<p align="center">
<img src="https://github.com/user-attachments/assets/ed0adb19-05d3-474c-8035-718f6e0b0762" width="600">
</p>


### 4️⃣ Correlation Analysis

Measured relationship between clicks and conversions.

| Platform     | Correlation                |
| ------------ | -------------------------- |
| **Facebook** | **0.87 (Strong Positive)** |
| AdWords      | 0.45 (Moderate Positive)   |

Facebook shows a much stronger click-to-conversion relationship.

<p align="center">
<img src="https://github.com/user-attachments/assets/f3a8b606-e58e-4b8f-bb53-7e3004e914d4" width="600">
</p>


### 5️⃣ Hypothesis Testing (Two-Sample t-test)

* **Facebook Mean Conversions:** 11.74
* **AdWords Mean Conversions:** 5.98
* **T-statistic:** 32.88
* **P-value:** 9.35e-134

Since p-value < 0.05:

✅ **Reject Null Hypothesis**
Facebook produces significantly higher conversions than AdWords.


### 6️⃣ Linear Regression (Facebook)

Built regression model to predict conversions from clicks.

* **R² Score:** 76.35%
* **MSE:** 2.02

This shows strong predictive power.

Example:

* 50 clicks → ~13 conversions
* 80 clicks → ~19 conversions

<p align="center">
<img src="https://github.com/user-attachments/assets/ab572eee-71da-436d-8663-c754b9860eab" width="500">
</p>


### 7️⃣ Time-Based Analysis

#### Weekly Trends

* Highest conversions on **Monday & Tuesday**

<p align="center">
<img src="https://github.com/user-attachments/assets/b7c4c217-18a7-40e2-b5da-ff7b18f3051e" width="500">
</p>


#### Monthly Trends

* Overall upward trend
* Drops observed in:

  * February
  * April
  * May
  * June
  * August
  * November

<p align="center">
<img src="https://github.com/user-attachments/assets/1ab51ff6-8af1-4e60-9e10-08a8802363f7" width="500">
</p>


### 8️⃣ Cost Per Conversion (CPC)

* Lowest CPC: **May & November**
* Highest CPC: **February**

<p align="center">
<img src="https://github.com/user-attachments/assets/c25221ad-da2f-4db9-b5cd-e3f0eebb2f20" width="500">
</p>


### 9️⃣ Cointegration Test

* **Score:** -14.755
* **P-value:** 2.13e-26

Result:

✅ Long-term equilibrium relationship between Facebook spend and conversions.

This indicates stable ROI behavior.

---

# 📊 Key Findings

### 🔥 Facebook Outperforms AdWords

* Higher average daily conversions
* More high-conversion days
* Stronger click-to-conversion relationship
* Better predictive modeling performance

---

# 💡 Final Recommendations

1. Allocate higher budget to **Facebook campaigns**
2. Increase spend during **low CPC months (May, November)**
3. Focus campaigns early in the week (Mon–Tue)
4. Use regression model for forecasting conversion targets
5. Maintain stable Facebook investment for long-term ROI

What should we finalize next? 🚀
