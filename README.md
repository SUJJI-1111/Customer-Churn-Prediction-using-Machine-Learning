# Customer Churn Prediction using Machine Learning

## Project Overview

Customer churn is one of the most significant challenges faced by subscription-based businesses, particularly in the telecommunications industry. Losing existing customers results in revenue loss, increased acquisition costs, and reduced customer lifetime value.

This project develops a machine learning-based customer churn prediction system for AlphaCom, a telecommunications company. The objective is to identify customers who are likely to discontinue services and provide actionable business insights to support proactive retention strategies.

The project combines Exploratory Data Analysis (EDA), data preprocessing, machine learning model development, hyperparameter tuning, threshold optimization, and business recommendations to create a practical churn prediction solution.

---

## Business Problem

AlphaCom has experienced increasing customer attrition despite offering multiple service plans and competitive pricing.

Key challenges include:

* Inability to identify customers likely to churn
* Revenue loss due to customer attrition
* Increased customer acquisition costs
* Ineffective retention strategies
* Reduced customer lifetime value

The goal of this project is to predict customer churn and identify the major factors contributing to customer attrition.

---

## Dataset Information

The dataset contains customer-level information including:

### Demographic Information

* Gender
* Senior Citizen
* Partner
* Dependents

### Service Information

* Phone Service
* Internet Service
* Online Security
* Online Backup
* Device Protection
* Tech Support
* Streaming Services

### Account Information

* Contract Type
* Payment Method
* Paperless Billing
* Tenure

### Financial Information

* Monthly Charges
* Total Charges

### Target Variable

* Churn (Yes / No)

---

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

Performed detailed analysis to identify customer behavior patterns and churn drivers.

Key analyses included:

* Univariate Analysis
* Bivariate Analysis
* Multivariate Analysis
* Correlation Analysis

### 2. Data Preprocessing

The following preprocessing steps were performed:

* Duplicate value verification
* Data type correction
* Missing value treatment
* Outlier analysis
* Feature engineering
* One-hot encoding
* Feature scaling
* Class imbalance handling
* Data leakage prevention

### 3. Machine Learning Model Development

The following models were implemented and evaluated:

* Logistic Regression (Baseline)
* Decision Tree
* Random Forest
* Random Forest (Tuned)
* Gradient Boosting
* Gradient Boosting (Tuned)
* AdaBoost
* XGBoost
* XGBoost (Tuned)

### 4. Hyperparameter Tuning

Hyperparameter optimization was performed on:

* Random Forest
* Gradient Boosting
* XGBoost

to improve predictive performance and model generalization.

---

## Model Evaluation Metrics

Models were evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* AUC (Area Under ROC Curve)

Since the business objective is to identify customers likely to churn, Recall was prioritized during model selection.

---

## Final Model Performance

### Selected Model: Random Forest (Tuned)

The final model was selected based on business requirements emphasizing churn detection capability.

| Metric    | Score |
| --------- | ----- |
| Accuracy  | 73.5% |
| Precision | 51.9% |
| Recall    | 80.6% |
| F1 Score  | 63.2% |
| AUC       | 0.835 |

Random Forest (Tuned) achieved the highest recall while maintaining a balanced F1-score, making it the most suitable model for proactive customer retention initiatives.

---

## Threshold Optimization

Threshold tuning was performed to align the model with business objectives.

### Default Threshold (0.5)

* Recall: 80.6%
* Precision: 51.9%
* F1 Score: 63.2%

### Optimized Threshold (0.3)

* Recall: 94.6%
* Precision: 40.3%
* F1 Score: 56.5%

Lowering the threshold significantly improved churn detection by identifying nearly all at-risk customers.

Although precision decreased, this trade-off is acceptable because the cost of losing a churn customer is substantially higher than the cost of targeting a non-churn customer.

---

## Key Business Insights

The analysis identified several major churn drivers:

### Contract Type

Customers with month-to-month contracts exhibit significantly higher churn compared to customers on long-term contracts.

### Customer Tenure

Customers with low tenure are more likely to leave, indicating that early-stage engagement is critical.

### Monthly Charges

Higher monthly charges are associated with increased churn probability, suggesting pricing sensitivity among customers.

### Technical Support

Customers without technical support services show considerably higher churn rates.

### Internet Service

Fiber optic customers demonstrate higher churn compared to other service segments, indicating opportunities for service improvement and value enhancement.

---

## Business Recommendations

Based on project findings:

* Promote long-term contracts through incentives and loyalty benefits.
* Strengthen onboarding programs for new customers.
* Develop targeted retention campaigns for high-risk customers.
* Improve technical support accessibility and service quality.
* Review pricing strategies for premium customer segments.
* Integrate churn prediction into CRM systems for proactive intervention.

---

## Business Impact

The proposed churn prediction framework enables:

* Early identification of at-risk customers
* Reduced customer attrition
* Improved customer retention
* Better allocation of marketing resources
* Enhanced customer lifetime value
* Increased profitability through proactive decision-making

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* XGBoost
* Jupyter Notebook

---

## Repository Contents

* AlphaCom-Final-GL.ipynb
* Customer-Churn-Report-GL.pdf
* Model-comparison.png
* ROC-CURVE-Customer-Churn.png
* Confusion-matrix-customer-churn.png
* requirements.txt

---

## Conclusion

This project demonstrates how machine learning can be leveraged to address customer churn challenges through predictive analytics. By combining advanced ensemble learning techniques, threshold optimization, and business-focused evaluation, the solution provides a practical framework for identifying at-risk customers and supporting data-driven retention strategies.

The final Random Forest (Tuned) model successfully balances predictive performance with business value, making it suitable for real-world churn management applications.
