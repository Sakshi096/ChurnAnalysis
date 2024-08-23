# ChurnAnalysis
This document outlines the steps involved in building a predictive model for telecom customer churn. The goal is to identify customers who are likely to churn and understand the factors influencing their decisions.

## 1. Exploratory Data Analysis (EDA)

The first step is to perform an exploratory data analysis to understand the structure of the dataset.

- **Data Overview:**
  - Import necessary libraries and read the dataset.
  - Print the number of rows, columns, missing values, unique values in each column, and feature values.
  - This helps in analyzing the categorical and numerical values and deciding which features to move forward with.

## 2. Exploring the Target Variable

The target variable, customer churn, is explored to understand its distribution.

- **Objective:**
  - Visualize the distribution of churned vs. non-churned customers using a pie chart.
  - Understand the balance in the dataset, which is crucial for model building.

## 3. Exploring Categorical Values

Next, categorical features are analyzed to gain insights into customer demographics and their relationship with churn.

- **Demographic Insights:**
  - Gender and partner status are evenly distributed.
  - Higher churn is observed among younger customers, those without partners, and those without dependents.
  - The data highlights non-senior citizens with no partners and dependents as a segment more likely to churn.

## 4. Analyzing Customer Subscription to Services

The services customers have signed up for are explored to see how they relate to churn.

- **Service Insights:**
  - Customers with more complex service setups (e.g., internet and streaming services) are more likely to churn.
  - Understanding these patterns helps in identifying which services might be associated with higher churn rates.

## 5. Exploring Payment Features

Payment-related features are analyzed to understand their impact on churn.

- **Payment Insights:**
  - Customers with shorter contracts and those who opted for paperless billing have higher churn rates.
  - Electronic check payments are associated with higher churn, highlighting a need for different payment options.

## 6. Exploring Numeric Data Types

Numeric features like tenure, monthly charges, and total charges are analyzed to identify patterns related to churn.

## 7. Binning Numerical Data

Numeric features are binned into categories (low, medium, high) to gain more detailed insights.

- **Binning Insights:**
  - Low tenure and high monthly charge bins have higher churn rates.
  - The low total charge bin also shows a higher churn rate, suggesting these customers are more likely to leave.

## 8. Data Preprocessing

Data preprocessing is performed to prepare the dataset for modeling.

- **Steps:**
  - Drop unnecessary columns.
  - Encode categorical features to convert them into a suitable format for machine learning algorithms.

## 9. Correlation Analysis

A correlation matrix is generated to identify and handle correlated features.

- **Insights:**
  - High correlations are identified and managed to reduce multicollinearity, ensuring that the model is built on independent features.

## 10. Churn Prediction Problem Definition

Churn prediction is defined as a binary classification problem.

- **Key Questions:**
  1. Which features influence churn?
  2. What are the most important features for model training?
  
- **Approach:**
  - Use the Generalized Linear Model (GLM) to analyze features and their importance using exponential coefficients.

## 11. Baseline Model Creation and Model Comparison

A baseline model is created using Logistic Regression and compared with other models.

- **Models Used:**
  - Support Vector Classifier (SVC)
  - Random Forest Classifier
  - Decision-Tree Classifier
  - Naive-Bayes Classifier
  
- **Objective:**
  - Compare each model's performance against the baseline to identify the best model for predicting churn.

## 12. Feature Selection to Improve Model Building

Feature selection is performed to enhance model performance.

- **Method:**
  - Recursive Feature Elimination with Cross-Validation (RFECV) is used with Logistic Regression to identify the most relevant features.
  - This step reduces model complexity, speeds up training, and can potentially improve accuracy.

## Conclusion

This workflow outlines the process of analyzing customer data, preparing it for machine learning, and building a predictive model for telecom churn. By following these steps, you can effectively identify churn drivers and build a model that helps retain customers.
