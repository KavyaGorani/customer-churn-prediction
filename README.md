# Customer Churn Prediction using Machine Learning
## Project Overview
### Customer churn refers to customers who stop using a company’s service.This project aims to predict whether a customer will churn using machine learning based on demographic, service, and billing information.The objective is to help businesses identify high-risk customers and take proactive actions to improve retention.


# Dataset
## The dataset contains customer details including:
### Demographics (gender, senior citizen, partner, dependents)
### Services used (internet, streaming, tech support, etc.)
### Account information (tenure, contract, billing, charges)
### Target variable: Churn (Yes / No)


# Exploratory Data Analysis (EDA)
## EDA was performed to understand patterns related to customer churn.
## Key insights:
### Customers with month-to-month contracts churn more & Customers with shorter tenure have higher churn.

![Tenure](/assets/Tenure.png)

### Higher monthly charges are associated with increased churn.

![MonthlyCharges](/assets/MonthlyCharges.png)

### Fiber optic users show higher churn compared to other services.

![InternetService](/assets/InternetServices.png)

### Electronic check users churn more than automatic payment users.

![PaymentMethod](/assets/PaymentMethod.png)

### Most customers use paperless billing.

![PaperlessBilling](/assets/PaperlessBilling.png)


# Data Preprocessing

## The following steps were applied:

### Dropped irrelevant columns such as customerID
### Converted TotalCharges to numeric format
### Handled missing values
### Converted binary values (Yes/No) into 0 and 1
### Converted “No internet service” into “No”
### Applied one-hot encoding to multi-category features
### Split the dataset into training and testing sets


# Models Used
## Logistic Regression
### A simple and interpretable model used as the baseline.

## Random Forest Classifier
### A more complex ensemble model used for comparison.


# Model Performance Comparison
## Model	Accuracy	Precision (Churn)	Recall (Churn)
## Logistic Regression	0.82	0.69	0.60
## Random Forest	0.79	0.65	0.46


# Final Model Selection

## Although Random Forest is more complex, Logistic Regression performed better in detecting churned customers, especially in recall, which is crucial for customer retention.
## Therefore, Logistic Regression was selected as the final model.


# Business Insight
## The model helps identify customers who are likely to churn so businesses can:
### Offer targeted discounts
### Improve customer service
### Provide personalized plans
### Reduce revenue loss


# Tools and Technologies
## Python
## Pandas, NumPy
## Matplotlib && Seaborn
## Scikit-learn
## Jupyter Notebook


# Conclusion
## This project demonstrates a complete data science workflow including data cleaning, exploratory data analysis, feature engineering, model training, evaluation, and business interpretation.

## It shows how machine learning can be applied to solve a real-world business problem such as customer churn.