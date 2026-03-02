# 📊 Meta Ad Performance Dashboard
---
## 📌 Project Overview

This Power BI dashboard analyzes Meta (Facebook & Instagram) advertising performance across the complete marketing funnel — from impressions to purchases.

The solution provides actionable insights into campaign effectiveness, audience behavior, ad format performance, geographic trends, and budget utilization to support data-driven marketing decisions.

---

## 🎯 Business Objective

The objective of this analysis is to:

* Monitor campaign reach and engagement
* Evaluate conversion efficiency across the funnel
* Identify high-performing ad formats
* Understand demographic and geographic behavior
* Optimize budget allocation for improved ROI
  
---

## 🗂 Data Model & Architecture

The data model follows a **Hybrid Star Schema Design**.

### ⭐ Fact Table

**`ad_events`**

* Stores event-level interactions (Impression, Click, Share, Comment, Purchase)
* Used to derive all KPIs


### 🌟 Dimension Tables

* **`ads`** – Platform, ad type, targeting information
* **`campaigns`** – Budget, duration, campaign metadata
* **`users`** – Demographics, age, gender, location, interests
* **Calendar Table** – Date hierarchy for time-based analysis


### 🔎 Modeling Approach

* `ad_events` acts as the central fact table
* `ads`, `users`, and `Calendar` connect directly to the fact table
* `campaigns` connects to `ads`, forming a slight snowflake structure
* One-to-many relationships ensure proper filter propagation

This structure enables scalable, efficient KPI computation and dimensional analysis.

---

## 📈 Key KPIs Implemented (Using DAX)

| KPI                     | Formula Logic                           |
| ----------------------- | --------------------------------------- |
| Impressions             | COUNT where `event_type = "Impression"` |
| Clicks                  | COUNT where `event_type = "Click"`      |
| Engagements             | Clicks + Shares + Comments              |
| CTR                     | Clicks ÷ Impressions                    |
| Engagement Rate         | Engagements ÷ Impressions               |
| Conversion Rate         | Purchases ÷ Clicks                      |
| Purchase Rate           | Purchases ÷ Impressions                 |
| Total Budget            | SUM(campaigns.total_budget)             |
| Avg Budget per Campaign | Total Budget ÷ Campaign Count           |

Dynamic KPI selection is implemented using a **parameter table**.

---

## 📊 Dashboard Components

### 🔹 Funnel Overview

* **216K Impressions**
* **25.4K Clicks**
* **1.3K Purchases**
* High **CTR (11.76%)**
* Low **Purchase Rate (0.61%)** → Funnel drop-off identified


### 🔹 Audience Analysis

* Female audience contributes **43%** engagement
* Core age group: **18–30**
* Strong youth segment responsiveness


### 🔹 Geographic Insights

* High engagement: **India, US, Brazil**
* Higher purchasing power markets: **Germany, UK**
* Enables geo-based budget optimization


### 🔹 Time-Based Analysis

* Peak engagement during **afternoon & evening**
* Stable weekly performance
* Calendar heatmap highlights campaign-driven spikes


### 🔹 Ad Format Performance

| Ad Type        | Insight                         |
| -------------- | ------------------------------- |
| Video          | Highest CTR & Conversion Rate   |
| Stories        | Strong impressions & engagement |
| Image/Carousel | Moderate performance            |


---

## 💡 Key Business Insights

* Strong top-funnel performance (awareness & engagement)
* Significant drop in purchase conversion
* Target segment: **Females aged 18–30**
* Best-performing formats: **Video & Stories**
* Optimize landing pages and retargeting to improve purchase rate

---

## 🛠 Tools & Technologies

* Power BI Desktop
* DAX Measures
* Schema Modeling
* Data Transformation (Power Query)
* Interactive Slicers & Dynamic KPI Parameters
