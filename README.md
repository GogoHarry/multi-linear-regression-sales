# 📊 Sales Prediction using Multiple Linear Regression

### 📌 Overview
This project leverages Multiple Linear Regression to analyze and predict sales performance based on various marketing promotion strategies, including TV ads, radio, social media, and influencer marketing. It walks through the complete data science workflow — from data acquisition and exploration to modeling and evaluation — to deliver actionable insights for marketing optimization.

### 🎯 Objective
To build a predictive model that estimates sales using multiple independent variables representing different marketing strategies. The aim is to:

- Quantify the impact of each promotional channel on sales.
- Identify which channels significantly influence revenue.
- Provide insights to help businesses allocate marketing budgets more effectively.

### 🧠 Learning Outcomes
By the end of this project, you will:

- Understand and apply multiple linear regression techniques.
- Preprocess and explore real-world marketing data.
- Evaluate model performance and check regression assumptions.
- Interpret model coefficients and communicate findings to stakeholders.

## 📊 Dataset
The dataset contains 572 records with the following features:
| Feature        | Description                             |
| -------------- | --------------------------------------- |
| `TV`           | Categorical variable: High, Medium, Low |
| `Radio`        | Continuous radio promotion spend        |
| `Social Media` | Continuous social media promotion spend |
| `Influencer`   | Categorical: Mega, Micro, Nano          |
| `Sales`        | Target variable: sales figures          |


## 🔍 Exploratory Data Analysis (EDA)
- Visualized relationships using pair plots
- Identified potential correlations among features
- Detected and handled missing values
- Encoded categorical variables using one-hot encoding

## 🧹 Data Preprocessing
- Removed null values with df.dropna()
- Converted categorical features using pd.get_dummies(drop_first=True)
- Prepared features for regression analysis

## 🧮 Model Building

Used statsmodels.ols to build the multiple linear regression model with the formula:
```python
Sales ~ Radio + Q("Social Media") + Q("TV_Low") + Q("TV_Medium") + Q("Influencer_Mega") + Q("Influencer_Micro") + Q("Influencer_Nano")
```python
