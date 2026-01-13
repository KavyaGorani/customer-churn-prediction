# Customer Churn Prediction using Machine Learning

## Project Overview
Customer churn refers to customers who stop using a company’s service.  
This project uses machine learning to predict whether a customer will churn based on demographic, service, and billing information. The goal is to help businesses identify high-risk customers and take proactive steps to reduce customer loss.

---

## Dataset
The dataset contains customer information including:
- Demographics (gender, senior citizen, partner, dependents)
- Services used (internet, streaming, tech support, etc.)
- Account information (tenure, contract type, billing method, charges)
- Target variable: **Churn** (Yes / No)

---

## Exploratory Data Analysis (EDA)
Exploratory Data Analysis was performed to understand customer behavior and churn patterns.

### Contract vs Churn
![Contract vs Churn](images/contract_vs_churn.png)

### Tenure vs Churn
![Tenure vs Churn](images/tenure_vs_churn.png)

### Monthly Charges vs Churn
![Monthly Charges vs Churn](images/monthlycharges_vs_churn.png)

### Payment Method vs Churn
![Payment Method vs Churn](images/paymentmethod_vs_churn.png)

### Internet Service vs Churn
![Internet Service vs Churn](images/internetservice_vs_churn.png)

### Paperless Billing vs Churn
![Paperless Billing vs Churn](images/paperlessbilling_vs_churn.png)

---

## Key EDA Insights
- Customers on **month-to-month contracts** are more likely to churn.
- Customers with **shorter tenure** have a higher churn rate.
- **Higher monthly charges** are associated with increased churn.
- **Fiber optic** internet users show higher churn compared to other services.
- **Electronic check** users have higher churn than automatic payment users.
- Most customers use **paperless billing**.

---

## Data Preprocessing
The following steps were applied:
- Dropped irrelevant columns such as `customerID`
- Converted `TotalCharges` to numeric
- Handled missing values
- Converted binary columns (Yes/No, Male/Female) into 0 and 1
- Converted "No internet service" to "No"
- Applied one-hot encoding to multi-category features
- Split data into training and testing sets

---

## Models Used

### Logistic Regression
Used as a baseline model because it is simple, fast, and interpretable.

### Random Forest Classifier
Used to test whether a more complex model could improve performance.

---

## Model Performance Comparison

| Model | Accuracy | Precision (Churn) | Recall (Churn) |
|--------|----------|------------------|----------------|
| Logistic Regression | 0.82 | 0.69 | 0.60 |
| Random Forest | 0.79 | 0.65 | 0.46 |

---

## Final Model Selection
Although Random Forest is more complex, **Logistic Regression performed better** in identifying churned customers, especially in recall. Since detecting churned customers is more important for business decision-making, Logistic Regression was selected as the final model.

---

## Business Impact
This model allows businesses to identify customers who are likely to churn so they can:
- Offer targeted discounts
- Improve customer support
- Provide personalized plans
- Reduce revenue loss

---

## Tools and Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Conclusion
This project demonstrates a complete data science workflow including data cleaning, exploratory data analysis, feature engineering, model training, evaluation, and business interpretation. It shows how machine learning can be applied to solve a real-world business problem such as customer churn prediction.
