# Bank-Churn-Analysis
![image](https://github.com/user-attachments/assets/ad8e3904-2abe-457a-8931-e118c6d1a61c)

## Background
The bank is facing a high customer churn rate, which indicates a significant portion of its customers are discontinuing their relationships with the institution. This churn threatens the bank’s growth, profitability, and long-term customer loyalty. Understanding the key drivers of churn is essential for developing targeted strategies to improve customer retention and overall satisfaction.
### Objective
The main goal of this analysis is to uncover patterns and correlations between customer features and churn behavior. By analyzing diverse datasets encompassing transactions, demographics, customer activity, and interactions, the study aims to identify the root causes of the high churn rate. These insights will enable the bank to develop and implement suitable, targeted strategies to improve customer retention, optimize product offerings, and enhance overall customer satisfaction.
 ### Questions:
 - Does a lower credit score correlate with higher churn?
 - Is there a geographical factor influencing churn?
 - Does having multiple banking products decrease the likelihood of churn?
 - Do customers with credit cards have higher churn rates than those without?
## Data Overview
The dataset comprises 10,000 rows with customer profiles, including demographic details (age, gender, geography), financial metrics (balance, credit score, salary), and behavioral attributes (activity status, product usage, credit card ownership). Data Source: [LINK](https://www.kaggle.com/datasets/santoshd3/bank-customers)
## Data Preparation
- Data duplication & missing values: There are no duplicate data and missing values in the dataset.
![image](https://github.com/user-attachments/assets/cb9a7fee-d2d9-49cb-98bc-8cc113d90062)


- Feature Engineering: Extracting age group features, and transforming the data into desired form.
- Encoding: The encoding method used is ordinal encoding to convert categorical data (geography) in numerical.

## Key Insights and Findings
**1. Exit Distribution:** 
- Churned Customers: 20.4% of customers are labeled as "exited" or "churned."
- Dataset Imbalance: The dataset is imbalanced, with the majority of customers being retained (79.6%). This imbalance highlights the need for strategies focused on retaining the minority group (churned customers) - the target variable.

**2. Credit Score with Exit Variable:** The distribution of credit scores for both retained and churned customers tends to be similar, mainly clustered between scores of 600 - 700. \
    _Key Insight:_ Low credit score customers are more likely to churn, as all low credit score customers (below 400) fall under the churned category. 
    
**3. Age with Exited Variable:** Churned customers are concentrated in the age group of 40-55 years. 

**4. Balance with Exited Variable:** Churned customers have account balances primarily ranging from 40k to 130k, while retained customers show more variation and lower concentration in balances, at zero.\
    _Key Insight:_ Surprisingly, churned customers with medium to high balances are exiting, which might suggest dissatisfaction with the products or services offered.
    
**5. Estimated Salary with Exited Variable:** No significant difference in salary distribution between churned and retained customers, with both groups concentrated around 50k to 100k. 

**6. Geography with Exited:** The number of churned customer in France and Germany is similar, around 810 customers, while in Spain, it is lower at 410. However, the churn rate in Germany should be approximately 40%, which is about double the rate in France, which is around 20%.

**7. Gender with Exited:** Females exhibit a higher churn rate (11.4%) compared to males (9%). 

**8. Credit Card User with Exited:**  Credit card users exhibit a higher churn rate (14.2%) compared to non-credit card users (6.1%). \
   _Key Insight:_ Credit card users may be experiencing dissatisfaction with credit-related products or services. 
   
**9. Product Usage with Exited:** Approximately 14.1% of customers using only one product have churned, which is higher compared to other groups. Notably, customers using three or four products have a retention rate close to zero, with almost no retained customers in those groups. 

**10. Customer Status with Exited:** Inactive customers have a higher churn rate (13.0%) compared to active customers (7.3%).

**11. Heatmap Findings:** The heatmap indicates that there is non-linear relationship between all features with the target variable (Exit). \
![image](https://github.com/user-attachments/assets/6c8a94ad-db0d-418f-9841-e3543f47dbc6)
## Dashboard
![image](https://github.com/user-attachments/assets/ec12c0d8-b354-4ace-ba28-cedd627c1821)


## Recommendation
**1.** The bank should consider retirement-focused financial products, investment planning tools, or age-targeted advisory services to retain customers in this age group.\
**2.** The bank should revisit its product bundling strategy, making sure that customers with multiple products feel they are receiving sufficient value. Alternatively, it may be useful to personalize bundles and create more flexible options.\
**3.** A thorough investigation into customer satisfaction and service quality in Germany should be conducted. The bank should focus on improving its customer support and perhaps reconsider its product offerings in Germany to align with local needs and expectations.\
**4.** The bank should develop re-engagement strategies to target inactive customers, such as personalized outreach, special offers, or financial consultations, to re-engage them and reduce churn.

