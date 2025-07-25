# RFM
Recency-Frequency-Monetary  This project performs an in-depth RFM (Recency, Frequency, Monetary) analysis and customer segmentation on the [UCI Online Retail dataset](https://archive.ics.uci.edu/ml/datasets/online+retail). 
# 📊 RFM-Based Customer Segmentation | Online Retail Analysis

This project leverages **RFM (Recency, Frequency, Monetary)** analysis to segment customers based on their purchasing behavior using the **UCI Online Retail Dataset**. The objective is to identify customer segments that can inform targeted marketing, retention strategies, and business insights.

---

## 🧠 Project Objective

To apply RFM-based segmentation on retail transaction data to:
- Understand customer value and engagement
- Segment customers for personalized marketing
- Enable business teams to make data-driven decisions

---

## 📦 Dataset Overview

- **Source**: [UCI Machine Learning Repository – Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)
- **Size**: ~500,000 transactions
- **Period**: One year of e-commerce transactions for a UK-based online retailer
- **Features**: `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

---

## 🧾 Methodology

### 1. **Data Cleaning & Preprocessing**
- Removed cancellations (invoices starting with 'C')
- Filtered out null `CustomerID` values
- For remaining missing values, assigned logical `GuestID` using session-based grouping
- Calculated `TotalAmount = Quantity × UnitPrice`

### 2. **RFM Feature Engineering**
- **Recency**: Days since last purchase (from a fixed reference date)
- **Frequency**: Number of unique purchase invoices
- **Monetary**: Total spending across all transactions

### 3. **Scoring & Segmentation**
- Scaled Recency, Frequency, and Monetary using quintile-based scoring (1–5)
- Combined individual scores into a single `RFM Score`
- Mapped scores to business-relevant customer segments (e.g., **Champions**, **Hibernating**, **At Risk**)

### 4. **Clustering (Optional Layer)**
- Standardized RFM values
- Applied **KMeans Clustering**
- Determined optimal number of clusters using the **Elbow Method** and **Silhouette Score**

### 5. **Visualization & Interpretation**
- Distribution of RFM metrics
- Segment-based heatmaps
- Cluster profiling and business interpretation

---

## 🛠️ Tech Stack

| Category        | Tools & Libraries                    |
|----------------|---------------------------------------|
| Language        | Python                               |
| Analysis        | Pandas, NumPy                        |
| Modeling        | Scikit-learn (KMeans)                |
| Visualization   | Matplotlib, Seaborn                  |
| Notebook        | Jupyter                              |

---

## 📊 Key Insights

- Identified top 15% customers contributing to over 50% of total revenue
- Segmented customers into high-value, loyal, and at-risk buckets
- Derived actionable strategies for retention and reactivation
- Created a clean, ready-to-use dataset for dashboarding in Tableau/Power BI

---

## 💡 Use Cases

- 🎯 **Targeted Marketing**: Tailor campaigns for loyal vs. inactive users
- 📉 **Churn Prevention**: Identify and re-engage “at risk” customers
- 📈 **Sales Strategy**: Allocate resources to high-value segments

---




