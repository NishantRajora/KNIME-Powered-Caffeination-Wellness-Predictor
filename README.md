# Coffee and Health Analytics: A KNIME Predictive Modeling Project

## Overview

This project leverages the KNIME Analytics Platform to perform a comprehensive predictive analysis using the Global Coffee Health Dataset.  

The primary objective is to investigate the relationship between coffee consumption, demographic characteristics, and health and sleep outcomes using both classification and regression techniques.

The workflow integrates:

- Data preprocessing and feature preparation  
- Supervised learning (classification and regression)  
- Model comparison and evaluation  
- Unsupervised learning for behavioral segmentation  
- Exploratory data visualization  

The project demonstrates the practical implementation of end-to-end analytics workflows within a visual data science environment.

---

## Project Objectives

- Predict health severity categories using demographic and lifestyle variables  
- Classify sleep quality based on coffee intake and related features  
- Predict numerical outcomes such as sleeping hours and coffee intake  
- Identify behavioral clusters using unsupervised learning  
- Compare performance of multiple machine learning algorithms  

---

## Dataset

Source: Kaggle (Global Coffee Health Dataset)  

The dataset includes demographic, lifestyle, and health-related attributes such as:

- Age  
- Gender  
- Coffee intake (cups per day)  
- Sleep duration  
- Sleep quality rating  
- Health issue category  
- Additional lifestyle variables  

The dataset enables both categorical prediction tasks and continuous outcome modeling.

---

## Workflow Architecture

The KNIME workflow is divided into parallel modeling paths for different predictive objectives.

### 1. Classification Tasks

These models predict categorical outcomes such as health severity and sleep quality.

| Target Variable | Model Used | Reported Accuracy | Model Type |
|-----------------|------------|------------------|------------|
| Health Issue | Random Forest | ~99.65% | Classification |
| Health Issue | Decision Tree | ~99.8% | Classification |
| Sleep Quality | Random Forest | ~98.95% | Classification |
| Sleep Quality | Decision Tree | ~99% | Classification |
| Sleep Quality | Logistic Regression | ~56.4% | Baseline Classification |

Interpretation:

- Tree-based models significantly outperformed Logistic Regression.  
- The high accuracy suggests strong separability in feature space.  
- Random Forest provided stable performance across both targets.  

---

### 2. Regression Tasks

Linear Regression was implemented for predicting continuous variables.

| Target Variable | Model Used | Evaluation Method | Objective |
|-----------------|------------|------------------|----------|
| Sleeping Hours | Linear Regression | Numeric Scorer (R², MAE, etc.) | Estimate daily sleep duration |
| Coffee Intake | Linear Regression | Numeric Scorer (R², MAE, etc.) | Estimate number of cups consumed |

Insights:

- Regression performance depends on feature correlation strength.  
- Linear models provide interpretable relationships between predictors and outcomes.  

---

### 3. Exploratory Data Analysis (EDA)

Unsupervised learning techniques were applied to explore behavioral segmentation.

Technique Used:
- K-Means Clustering  

Analysis Focus:
- Age vs Coffee Intake relationship  
- Identification of distinct consumption patterns  
- Visualization through scatter plots  

Outcome:

- Distinct clusters revealed differences in coffee consumption habits across age groups.  
- Segmentation highlights lifestyle variability within demographic segments.  

---

## Tools and Technologies

- KNIME Analytics Platform  
- Decision Tree  
- Random Forest  
- Logistic Regression  
- Linear Regression  
- K-Means Clustering  
- Numeric Scorer and Confusion Matrix Nodes  
- Data preprocessing and transformation nodes  

---

## Key Observations

- Tree-based models achieved extremely high accuracy, suggesting structured feature relationships.  
- Logistic Regression underperformed, indicating possible non-linear decision boundaries.  
- Regression models demonstrated moderate predictive power for numerical targets.  
- Clustering revealed interpretable lifestyle segments.  
- KNIME’s workflow-based modeling enables parallel experimentation and evaluation.  

---

## Learning Outcomes

- Hands-on experience with workflow-based machine learning  
- Implementation of classification and regression pipelines  
- Comparative evaluation of multiple algorithms  
- Application of unsupervised clustering techniques  
- Interpretation of model metrics within a visual analytics environment  

---

## Limitations

- Synthetic or simplified dataset structure may inflate classification accuracy  
- Potential overfitting in tree-based models  
- Further cross-validation and hyperparameter tuning required for production-level reliability  

---

## Future Improvements

- Implement cross-validation loops in KNIME  
- Perform hyperparameter tuning  
- Add feature importance analysis  
- Deploy workflow via KNIME WebPortal  
- Integrate advanced ensemble or boosting techniques  
- Conduct fairness or bias analysis  

---

## Repository Structure

```
Coffee-and-Health-Analytics/
│
├── data/
├── workflow.knwf
├── results/
├── screenshots/
└── README.md
```

---

## Author

Nishant Rajora   
Focused on predictive modeling, structured analytics workflows, and practical data science implementation
