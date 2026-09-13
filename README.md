# Customer Churn Prediction
## Week 1: Exploratory Data Analysis
### Dataset
- Source: Telco Customer Churn (Kaggle)
- Size: 7,043 customers, 21 features
- Target: Predict customer churn (Yes/No)
### Key Findings
* **Overall Churn Rate:** 26.54% (1,869 of 7,043 customers).
* **Contract Type:** Month-to-month contracts are the strongest churn driver, churning at ~42% compared to ~11% for one-year and ~3% for two-year contracts.
* **Customer Tenure:** Customers with shorter tenure are far more likely to leave, with most churn happening early in the relationship.
* **Internet Service:** Fiber optic subscribers churn at ~42%, notably higher than DSL (~19%) or customers with no internet service (~7%).
* **Payment Method:** Electronic check users have the highest churn rate (~45%), nearly three times that of automatic payment methods like bank transfers or credit cards.
### Setup
Open the Kaggle notebook or run locally:
pip install pandas numpy matplotlib seaborn
