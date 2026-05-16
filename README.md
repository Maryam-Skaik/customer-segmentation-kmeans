# 🧠 Customer Segmentation using KMeans Clustering

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Machine Learning](https://img.shields.io/badge/ML-KMeans-orange)
![Scikit--Learn](https://img.shields.io/badge/Scikit--Learn-Used-green)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

---

## 📌 Project Overview

This project focuses on **customer segmentation using KMeans Clustering**, an unsupervised machine learning algorithm.

The goal is to group customers into meaningful segments based on their financial and personal attributes. These segments help a credit card company better understand customer behavior and improve marketing strategies.

---

## 📊 Dataset Description

The dataset contains information about **850 customers**, including:

* Age 👤
* Education level 🎓
* Years of employment 💼
* Income 💰
* Credit card debt 💳
* Default history ⚠️
* Debt-to-income ratio 📉

Each row represents a single customer and their financial profile.

---

## 💡 Key Financial Terms (Simple Meaning)

* **Credit Card Debt** → Money the customer still owes to the bank
* **Defaulted** → Whether the customer failed to repay loans (1 = yes, 0 = no)
* **Debt-to-Income Ratio** → How much debt a customer has compared to their income

---

## ⚙️ Project Workflow

### 1. Data Cleaning 🧹

* Removed unnecessary columns (Customer ID, index column)
* Handled missing values in `Defaulted` column using median

### 2. Feature Selection 🎯

Selected important features for clustering:

* Age
* Education
* Years Employed
* Income
* Card Debt
* Defaulted
* Debt-Income Ratio

### 3. Data Scaling 📏

Applied `StandardScaler` to normalize all features so that no variable dominates others.

---

## 📈 Finding the Best Number of Clusters (K)

To choose the optimal number of clusters:

### 📉 Elbow Method

* Plotted inertia values for different K values
* Looked for the “elbow point” where improvement slows down

### 📊 Silhouette Score

* Measured how well-separated clusters are
* Higher score = better clustering quality

👉 Based on both methods, **K = 3** was selected.

---

## 🤖 Model Building

* Applied **KMeans Clustering** with `k = 3`
* Assigned each customer to a cluster
* Added cluster labels to the dataset

---

## 📊 Cluster Analysis Results

### 🟢 Cluster 0: High-Earning Stable Customers

* High income and long work experience
* Low risk of default
* Financially stable and reliable

### 🟡 Cluster 1: Low-Risk Regular Customers

* Lower income but controlled spending behavior
* Very low debt levels
* Safe but lower-value customers

### 🔴 Cluster 2: High-Risk Customers

* Low experience and high debt pressure
* Highest default rate
* Financially unstable group

---

## 🔍 Key Insights

* Income alone does NOT determine risk level
* Work experience strongly affects financial stability
* Debt-to-income ratio is a key indicator of risk
* Customers naturally fall into 3 distinct financial behaviors

---

## 📌 Marketing Recommendations

### 🟢 Cluster 0

* Offer premium credit cards
* Provide travel rewards and high limits
* Focus on loyalty programs

### 🟡 Cluster 1

* Offer standard credit cards with low fees
* Provide cashback on daily spending
* Gradually increase credit limits

### 🔴 Cluster 2

* Offer secured or low-limit cards only
* Apply strict approval policies
* Focus on financial stability improvement

---

## 🧠 Conclusion

KMeans clustering helped uncover hidden customer groups based on financial behavior. These insights allow the company to make better credit decisions and targeted marketing strategies.

---

## 🛠️ Technologies Used

* Python 🐍
* Pandas & NumPy
* Scikit-learn
* Matplotlib

---

## 📂 Project Outcome

A complete customer segmentation model that:

* Identifies customer groups automatically
* Helps reduce credit risk
* Improves marketing strategy efficiency
