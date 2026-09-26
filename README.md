# Customer Churn Prediction
## Week 1: Exploratory Data Analysis
### Dataset
- Source: Telco Customer Churn (Kaggle)
- Size: 7,043 customers, 21 features
- Target: Predict customer churn (Yes/No)
### Key Findings
The analysis of the Telco Customer Churn dataset revealed the following important findings:

### 1. Overall Churn Rate

* The overall churn rate is **26.54%**.
* Out of **7,043 customers**, **1,869 customers** have churned.

### 2. Contract Type

* **Month-to-month contracts** have the highest churn rate at approximately **42%**.
* Customers with **one-year contracts** have a churn rate of approximately **11%**.
* Customers with **two-year contracts** have the lowest churn rate at approximately **3%**.
* This shows a strong relationship between contract type and customer churn.

### 3. Customer Tenure

* Customers with **shorter tenure** are much more likely to leave.
* Most churn occurs during the **early stages of the customer relationship**.
* Customers who stay with the company for a longer period generally show greater loyalty.

### 4. Monthly Charges

* Customers with **higher monthly charges** are more likely to churn.
* Higher costs appear to be associated with an increased risk of customer cancellation.

### 5. Internet Service

* **Fiber optic customers** have a churn rate of approximately **42%**.
* **DSL customers** have a churn rate of approximately **19%**.
* Customers with **no internet service** have a churn rate of approximately **7%**.
* Fiber optic customers therefore represent an important high-churn group in this dataset.

### 6. Payment Method

* Customers using **electronic checks** have the highest churn rate at approximately **45%**.
* Customers using automatic payment methods, such as **bank transfers and credit cards**, have considerably lower churn rates.
* This indicates that payment method is an important factor associated with customer churn.

### 7. High-Risk Customer Characteristics

The analysis shows that customers are particularly associated with higher churn when they have:

* Month-to-month contracts
* Short customer tenure
* Higher monthly charges
* Fiber optic internet service
* Electronic check payment method

### 8. Overall Conclusion

The analysis shows that **contract type, customer tenure, monthly charges, internet service, and payment method** are important factors associated with customer churn. New customers, month-to-month customers, fiber optic users, customers with higher monthly charges, and electronic check users represent important groups for further analysis and customer-retention efforts.

### Setup
Open the Kaggle notebook or run locally:
pip install pandas numpy matplotlib seaborn
