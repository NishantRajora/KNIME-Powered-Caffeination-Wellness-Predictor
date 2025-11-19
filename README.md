# ☕ Coffee and Health Analytics: A KNIME Predictive Project

## 📜 Project Overview

This project utilizes the **KNIME Analytics Platform** to conduct a comprehensive analysis and predictive modeling study using the **Global Coffee Health Dataset**. The primary goal is to explore the complex relationship between coffee consumption, demographic factors, and various health and sleep outcomes.

The workflow is structured to address both **classification** (predicting categories) and **regression** (predicting numerical values) problems, alongside basic exploratory data analysis (EDA).

---

## ⚙️ Workflow Segments & Model Performance

The KNIME workflow is partitioned into multiple concurrent paths to train and evaluate distinct models for various targets.

### 1. Classification Tasks (Predicting Quality/Status)

These models predict categorical outcomes like health severity and sleep rating.

| Target Variable | Model Used | Reported Accuracy | Model Type |
| :--- | :--- | :--- | :--- |
| **Health Issue** | Random Forest | $\approx 99.65\%$ | Classification |
| **Health Issue** | Decision Tree | $\approx 99.8\%$ | Classification |
| **Sleep Quality** | Random Forest | $\approx 98.95\%$ | Classification |
| **Sleep Quality** | Decision Tree | $\approx 99\%$ | Classification |
| **Sleep Quality** | Logistic Regression | $\approx 56.4\%$ | Classification (Baseline) |

*The high accuracy observed in the tree-based models (Random Forest and Decision Tree) suggests a strong, easily separable pattern exists in the data linking lifestyle features to the classified outcomes.*

### 2. Regression Tasks (Predicting Numerical Values)

These models predict continuous, quantitative values using **Linear Regression**.

| Target Variable | Model Used | Evaluation Metric (Numeric Scorer) | Goal |
| :--- | :--- | :--- | :--- |
| **Sleeping Hours** | Linear Regression | *Evaluated via Numeric Scorer (e.g., R-squared)* | Predict the average hours of sleep per night. |
| **Coffee Intake** | Linear Regression | *Evaluated via Numeric Scorer (e.g., R-squared)* | Predict the daily coffee intake (in cups). |

### 3. Exploratory Data Analysis (EDA)

* **Objective:** To visually segment the population and identify patterns.
* **Techniques:** K-Means Clustering for segmentation and Scatter Plot visualization.
* **Analysis:** Investigating the relationship between **Age vs. Coffee Intake** using K-Means to identify clusters with distinct consumption habits.

---

## 🛠️ Tools & Technologies

* **Primary Tool:** KNIME Analytics Platform
* **Dataset:** Global Coffee Health Dataset (Kaggle)
* **Modeling Techniques Used:**
    * Decision Tree
    * Random Forest
    * Logistic Regression
    * Linear Regression
    * K-Means Clustering
