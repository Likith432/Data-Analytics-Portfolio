# 🧠 Customer Segmentation Analysis – Machine Learning (K-Means)

## 📌 Project Overview

This project performs **customer segmentation using Unsupervised Machine Learning (K-Means Clustering)** on a marketing dataset.

The objective is to identify distinct customer groups based on purchasing behavior, demographics, and campaign responses. These insights enable businesses to design targeted marketing strategies, improve retention, and enhance customer relationship management (CRM).

---

## 🎯 Business Objective

* Identify high-value and at-risk customers
* Understand purchasing patterns across demographics
* Improve campaign targeting efficiency
* Support personalized marketing strategies
* Enhance customer lifetime value (CLV)

---

## 🗂 Dataset

**File Used:** `customer_segmentation.csv`

The dataset includes:

* Demographics (Age, Income, Marital Status, Education)
* Campaign response data
* Product category spending
* Purchase frequency (Web & Store)
* Recency (Days since last purchase)

---

## 🔬 Methodology

The project follows a structured Data Science workflow:

### 1️⃣ Data Loading & Exploration

* Loaded dataset using Pandas
* Performed initial inspection using:

  * `head()`
  * `info()`
  * `describe()`

---

### 2️⃣ Data Cleaning

* Removed rows with missing `Income`
* Converted `Dt_Customer` to datetime format

---

### 3️⃣ Feature Engineering

Created meaningful derived features:

* **Age** → Calculated from `Year_Birth`
* **Total_Children** → `Kidhome + Teenhome`
* **Total_Spending** → Sum of all product category spending
* **Customer_Since** → Days since enrollment
* **AcceptedAny** → Binary campaign response indicator
* **AgeGroup** → Age segmentation buckets

---

### 4️⃣ Exploratory Data Analysis (EDA)

* Distribution analysis (Age, Income, Spending)
* Box plots for demographic comparisons
* Correlation heatmap for numerical features
* Campaign response pattern analysis

---

### 5️⃣ Customer Segmentation (K-Means Clustering)

#### 🔹 Feature Selection

Selected key clustering features:

* Age
* Income
* Total_Spending
* NumWebPurchases
* NumStorePurchases
* NumWebVisitsMonth
* Recency

#### 🔹 Data Scaling

Applied **StandardScaler** to normalize feature ranges.

#### 🔹 Optimal Cluster Selection

Used **Elbow Method (WCSS)** to determine optimal `k`.
<p> <img src="https://github.com/user-attachments/assets/4448fa0d-0ac8-49a2-af5d-ff6bdb760815" width="500"> </p>


#### 🔹 Model Training

Applied **K-Means Clustering (k=6)**.

#### 🔹 Dimensionality Reduction

Used **PCA (Principal Component Analysis)** to visualize clusters in 2D space.
<p> <img src="https://github.com/user-attachments/assets/45c4e48d-a1d0-4c40-83c2-5b157ec1bc00" width="500"> </p>

---

### 6️⃣ Model Deployment Preparation

Saved trained components:

* `kmeans_model.pkl`
* `scaler.pkl`

These are used in the Streamlit web application for real-time customer prediction.

---

## 📊 Key Findings – Identified Customer Segments (k = 6)

### 🟢 Cluster 0: Senior High-Spending Traditional Customers

* Older age group
* Very high income & spending
* High store purchases
* Higher recency (less frequent recently)


### 🟡 Cluster 1: Low-Income Browsers (Low Converters)

* Lower income & spending
* High web visits
* Low conversion value
* Recent but low-value purchases


### 🔵 Cluster 2: Active Multi-Channel Shoppers

* Medium-high income
* Strong web engagement
* Consistent purchases
* Balanced recency


### 🟣 Cluster 3: Young High-Value Premium Customers

* Youngest age group
* Highest income & spending
* High store purchases
* Medium recency


### 🔴 Cluster 4: At-Risk Low-Value Customers

* Low income & spending
* Low purchase frequency
* High recency (disengaged customers)


### 🟠 Cluster 5: Loyal High-Value Store Customers

* High income & spending
* Very frequent store purchases
* Very low recency (recent buyers)

---

## 💡 Business Impact

This segmentation enables:

* Personalized marketing campaigns
* Retention strategies for at-risk customers
* Premium targeting for high-value segments
* Budget optimization across customer groups
* Improved campaign conversion rates
