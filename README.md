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
## Week 2: Building ML Models

### Project Overview

In Week 2, I built and evaluated different machine learning models for Telco Customer Churn Prediction. I worked with Logistic Regression, Decision Tree, Random Forest, class balancing, threshold selection, and feature engineering.

### Dataset & Preprocessing

* Total customers: **7,043**
* Features after encoding: **30**
* Training samples: **5,634**
* Testing samples: **1,409**
* Churn rate: **26.5%**
* Missing values after cleaning: **0**

### Baseline Model

The baseline always predicted that customers would stay.

* Accuracy: **73.5%**
* Churners caught: **0**

This showed that accuracy alone can be misleading for an imbalanced dataset.

### Logistic Regression

At threshold **0.50**:

* Accuracy: **0.807**
* Precision: **0.658**
* Recall: **0.567**
* F1: **0.609**
* AUC: **0.842**

Top churn risk factors included **Fiber optic, TotalCharges, and StreamingMovies**. Important protective factors included **tenure, MonthlyCharges, and Two-year contracts**.

### Confusion Matrix

* TN: **925**
* FP: **110**
* FN: **162**
* TP: **212**

The model missed **162 churners**, showing why recall is important.

### Threshold Analysis

The business costs were:

* Missed churner: **PKR 6,000**
* Unnecessary retention offer: **PKR 1,000**

Theoretical threshold: **0.14**
Empirical best threshold: **0.15**

At threshold **0.15**, the model caught **344 churners** compared with **212** at threshold 0.50. This means **132 more churners** were caught, with **327 additional false alarms**.

### Decision Tree & Random Forest

The Decision Tree showed overfitting as depth increased.

Random Forest results:

* OOB accuracy: **0.803**
* Test accuracy: **0.807**
* Test AUC: **0.842**

Top features by permutation importance were **tenure, TotalCharges, and Contract_Two year**.

### Class Balancing

| Model       | Precision | Recall |    F1 |
| ----------- | --------: | -----: | ----: |
| LR Default  |     0.658 |  0.567 | 0.609 |
| LR Balanced |     0.505 |  0.781 | 0.613 |

Balanced weights increased recall but reduced precision.

### Feature Engineering

Engineered features:

* `n_services`
* `is_new`
* `charge_per_mo`
* `price_jump`

Random Forest AUC:

**Before:** 0.8422
**After:** 0.8420

The engineered features did not improve the AUC.

### What I Learned

I learned that accuracy alone is not enough for an imbalanced classification problem. I learned how to interpret Logistic Regression using odds ratios, evaluate models using precision, recall, F1 and AUC, select a threshold using business costs, identify overfitting in Decision Trees, and use Random Forest and feature engineering for comparison.

### Biggest Lesson

The biggest lesson was that **model evaluation should consider both technical performance and business costs**, rather than relying only on accuracy.
### Kaggle Notebook

[Week 2 - Building ML Models]((https://www.kaggle.com/code/abuzarbhatti068/week-2-building-ml-models))
