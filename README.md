# Bank-Churn-Analysis
## Background
## Objective
The primary objective of this analysis is to identify patterns and correlations between customer features and churn. 
 - Does a lower credit score correlate with higher churn?
 - Is there a geographical factor influencing churn?
 - Does having multiple banking products decrease the likelihood of churn?
 - Do customers with credit cards have higher churn rates than those without?
## Data Overview
The dataset comprises 10,000 rows with 18 columns including customer profiles, including demographic details (age, gender, geography), financial metrics (balance, credit score, salary), and behavioral attributes (activity status, product usage, credit card ownership). Data Source: [LINK]()
## Data Preparation

## Key Insights and Findings
**1. Credit Score with Exit Variable:** The distribution of credit scores for both retained and churned customers tends to be similar, mainly clustered between scores of 600 - 700. \
    _Key Insight:_ Low credit score customers are more likely to churn, as all low credit score customers (below 600) fall under the churned category. \
    
**2. Age with Exited Variable:** Churned customers are concentrated in the age group of 40-55 years. \

**3. Balance with Exited Variable:** Churned customers have account balances primarily ranging from 40k to 130k, while retained customers show more variation and lower concentration in balances, at zero.\
    _Key Insight:_ Surprisingly, churned customers with medium to high balances are exiting, which might suggest dissatisfaction with the products or services offered.\
    
**4. Estimated Salary with Exited Variable:** No significant difference in salary distribution between churned and retained customers, with both groups concentrated around 50k to 100k. \

**5. Geography with Exited:** The number of churned customer in France and Germany is similar, around 810 customers, while in Spain, it is lower at 410. However, the churn rate in Germany should be approximately 40%, which is about double the rate in France, which is around 20%.\

**6. Gender with Exited:** Females exhibit a higher churn rate (11.4%) compared to males (9%). \

**7. Credit Card User with Exited:**  Credit card users exhibit a higher churn rate (14.2%) compared to non-credit card users (6.1%). \
   _Key Insight:_ Credit card users may be experiencing dissatisfaction with credit-related products or services. \
   
**8. Product Usage with Exited:** Approximately 14.1% of customers using only one product have churned, which is higher compared to other groups. Notably, customers using three or four products have a retention rate close to zero, with almost no retained customers in those groups. \

**9. Customer Status with Exited:** Inactive customers have a higher churn rate (13.0%) compared to active customers (7.3%).\
**10. 
## Recommendation
- The bank should consider introducing typical products for customers who are approaching retirement age.
- Nearly all customers with three or more products have churned, highlighting a potential failure in the bank's product diversification strategy. Stakeholders should prioritize investigating the root causes and focus on improving service quality while adopting a more targeted and customer-centric approach to product offerings.
