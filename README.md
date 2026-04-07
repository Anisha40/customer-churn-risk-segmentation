# Customer Churn Prediction, Risk Segmentation, and Retention Strategy

## Project Overview
This project analyzes customer churn using the Telco Customer Churn dataset and goes beyond standard churn prediction by translating model results into business action.

Instead of only predicting which customers are likely to churn, this project also:
- identifies the main drivers of churn
- segments customers into risk tiers
- estimates revenue at risk
- creates customer retention personas
- recommends next-best actions for intervention

  
## Business Goal
The goal of this project is to predict which customers are likely to churn and turn those predictions into practical retention decisions.

The analysis focuses on answering four key business questions:
1. Which customers are most likely to churn?
2. What factors are driving churn?
3. Which customer groups represent the highest business risk?
4. What actions should the company take to reduce churn?

   
## Dataset
- **Dataset:** Telco Customer Churn
- **Source:** Kaggle
- **Records:** 7,043 customers

The dataset includes customer demographics, subscription details, billing information, service usage, and churn status.


## Tools and Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook


## Project Workflow
The project followed this workflow:

1. Data cleaning and preprocessing  
2. Exploratory data analysis  
3. Feature engineering  
4. Predictive modeling  
5. Feature importance analysis  
6. Risk segmentation  
7. Revenue-at-risk estimation  
8. Retention persona creation  
9. Intervention recommendation  


## Modeling Approach
Two models were tested:
- Logistic Regression
- Random Forest

Logistic Regression was selected as the final model because it produced stronger recall for churners and remained highly interpretable for business use.

### Final Model Performance
- **Model:** Logistic Regression
- **ROC-AUC:** 0.842
- **Churn Recall:** 0.79

This made the model effective for identifying at-risk customers while still allowing business interpretation of churn drivers.


## Key Findings

### Main churn drivers
The strongest churn signals included:
- Month-to-month contracts
- Fiber optic internet
- Electronic check payment method
- No online security
- No tech support
- Early customer tenure

### Retention signals
The strongest retention indicators included:
- Longer tenure
- Two-year contracts
- DSL service
- More stable customer profiles

### Risk segmentation results
Customers were grouped into four risk tiers:
- **Low**
- **Medium**
- **High**
- **Critical**

Observed churn increased consistently across segments:

- **Low:** 3.9%
- **Medium:** 18.7%
- **High:** 36.8%
- **Critical:** 68.0%

This validated that the model was effective in separating the customer base into meaningful business risk groups.


## Revenue at Risk
To make the analysis more actionable, predicted churn probabilities were translated into expected revenue at risk.

### Expected revenue at risk by segment
- **Low:** \$192K
- **Medium:** \$380K
- **High:** \$843K
- **Critical:** \$1.13M

This showed that most financial exposure is concentrated in the **High** and **Critical** segments, meaning retention resources should be prioritized there.


## Retention Personas
To make intervention more practical, customers were grouped into business-friendly personas:

- **New customer shock**
- **Price-sensitive fiber user**
- **Unprotected / unsupported user**
- **Payment friction risk**
- **General risk**

### Most important personas
- **New customer shock** had the highest average churn probability and the highest actual churn rate
- **Price-sensitive fiber user** combined elevated churn risk with very high monthly charges
- **Unprotected / unsupported user** highlighted the role of support-related services in retention


## Recommended Intervention Strategy

### 1. New customer shock
**Recommended actions:**
- onboarding campaigns
- 30/60/90-day check-ins
- product education
- early-life retention outreach

### 2. Price-sensitive fiber user
**Recommended actions:**
- plan optimization
- bundle review
- limited-time discount
- value-based messaging

### 3. Unprotected / unsupported user
**Recommended actions:**
- free trial of tech support
- free trial of online security
- support feature education

### 4. Payment friction risk
**Recommended actions:**
- autopay incentives
- billing simplification
- better payment reminders

This intervention layer is what turns the project from a churn model into a business decision-support tool.


## Project Files
- `customer_churn_analysis.ipynb` - full notebook
- `scored_telco_customers.csv` - scored customer output with churn probabilities, risk segments, personas, and actions
- `README.md` - project summary and findings


## Business Impact
This project demonstrates how churn modeling can be made more valuable by connecting prediction to action.

Rather than ending with a probability score, the project helps answer:
- where churn risk is highest
- which customers should be prioritized
- how financial exposure is distributed
- what retention teams should do next


## Future Improvements
Possible next steps for this project include:
- threshold tuning based on retention cost
- probability calibration
- uplift modeling for offer targeting
- A/B testing of intervention strategies
- dashboard deployment for business users


## Created by
**Anisha Shrestha**

If you found this project interesting, feel free to connect with me on LinkedIn or explore my other analytics projects.
