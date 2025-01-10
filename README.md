# Bank Customer Churn Analysis
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
  ![image](https://github.com/user-attachments/assets/60b79058-a95e-4823-ac7f-0aefaa8292de)

- Dataset Imbalance: The dataset is imbalanced, with the majority of customers being retained (79.6%). This imbalance highlights the need for strategies focused on retaining the minority group (churned customers) - the target variable.

**2. Credit Score with Exit Variable:** The distribution of credit scores for both retained and churned customers tends to be similar, mainly clustered between scores of 600 - 700. \
![image](https://github.com/user-attachments/assets/47c2ef20-62a2-4921-8627-5c7eea645801)

   _Key Insight:_ Low credit score customers are more likely to churn, as all low credit score customers (below 400) fall under the churned category. 
    
**3. Age with Exited Variable:** Churned customers are concentrated in the age group of 40-55 years. 
![image](https://github.com/user-attachments/assets/390e49f2-9087-436d-82ba-9a17cb14842f)


**4. Balance with Exited Variable:** Churned customers have account balances primarily ranging from 40k to 130k, while retained customers show more variation and lower concentration in balances, at zero.\
![image](https://github.com/user-attachments/assets/fbf53cb3-4bb5-41d6-83f5-ad1b7ec4fff1)

    _Key Insight:_ Surprisingly, churned customers with medium to high balances are exiting, which might suggest dissatisfaction with the products or services offered.
    
**5. Estimated Salary with Exited Variable:** No significant difference in salary distribution between churned and retained customers, with both groups concentrated around 50k to 100k. 
![image](https://github.com/user-attachments/assets/aebba98f-b1ba-4a9d-9941-601dbfc894cc)


**6. Geography with Exited:** The number of churned customer in France and Germany is similar, around 810 customers, while in Spain, it is lower at 410. However, the churn rate in Germany should be approximately 40%, which is about double the rate in France, which is around 20%.
![image](https://github.com/user-attachments/assets/9203a4c2-e29c-4bca-9b1f-7dcda6437e7a) ![image](https://github.com/user-attachments/assets/8b63487d-b7c8-4c95-b6a8-b9ba71e728af)


**7. Gender with Exited:** Females exhibit a higher churn rate (11.4%) compared to males (9%). 
![image](https://github.com/user-attachments/assets/e829dd12-2a45-4906-a646-2e358ba876ce)


**8. Credit Card User with Exited:**  Credit card users exhibit a higher churn rate (14.2%) compared to non-credit card users (6.1%). \

   ![image](https://github.com/user-attachments/assets/c10daa05-cff9-4a5a-9f63-4fe141f2d1e8)
_Key Insight:_ Credit card users may be experiencing dissatisfaction with credit-related products or services. 
   
**9. Product Usage with Exited:** Approximately 14.1% of customers using only one product have churned, which is higher compared to other groups. Notably, customers using three or four products have a retention rate close to zero, with almost no retained customers in those groups. 
![image](https://github.com/user-attachments/assets/4739a118-e68b-4b69-a2b8-2faa14b5f8a2)

**10. Customer Status with Exited:** Inactive customers have a higher churn rate (13.0%) compared to active customers (7.3%).
![image](https://github.com/user-attachments/assets/4c71ddcf-0b59-41d4-904a-bd75afb5081f)


**11. Heatmap Findings:** The heatmap indicates that there is non-linear relationship between all features with the target variable (Exit). \
![image](https://github.com/user-attachments/assets/6c8a94ad-db0d-418f-9841-e3543f47dbc6)
## Dashboard
I used Power BI to perform visualisation. At first, I 
### 1. Column Operations
- There is no significant difference in churn rate between income groups (found out by Python). So, EstimatedSalary have been removed.
- Column Rename: Columns have been renamed for clarity. For example, rename "HasCrCard" to "Credit Card", "NumOfProducts" to "No.Products" and so on.
- Value Replacement: For clarity, I replace all binary values (0 vs 1 ) with suitable values. For example, replace 0 to  "Inactive" and 1 to "Active" in "Active Member" column, replace 0 to "Retained" and 1 to "Churned" in "Exited" column and so on.
![image](https://github.com/user-attachments/assets/ec12c0d8-b354-4ace-ba28-cedd627c1821)

Power Bi Dashboard [Link](https://github.com/thinlh07/Bank-Churn-Analysis/blob/main/Bank%20Churn%20Report.pbix)
### 2. Data Normalisation


#### 2.1. Separation of Fact and Dimension Attributes
The dataset was divided into a fact table and multiple dimension tables:

- Fact Table: A fact_churn table was created to contain transactional and measurable data, including CustomerID, ChurnStatus, JoinDate, and foreign keys linking to the dimension tables.
- Dimension Tables: Descriptive tables were designed to represent entities like country, account balance, age, credit score
#### 2.2. Creation of Tables
The fact_churn table was populated with churn-related metrics and references to dimension tables.
A Customer Dimension table was created to store demographic details such as age and gender.
A Plan Dimension table captured information about subscription plans, including PlanType and pricing.
A Location Dimension table recorded geographical details such as country and region.
Establishing Relationships



Primary and foreign key relationships were established between the fact_churn table and the dimension tables. This ensured a clear and efficient star schema structure, which optimized data queries and supported robust data analysis in Power BI.
Next step, I applied data normalization to restructure the dataset for churn analysis, organizing it into a star schema for improved efficiency and analysis. The process involved the following steps:
#### 1. Table Creations:
- Fact_churn table: Included alls and references to dimensions.
- Dim_CreditScore: Stored Credit Score Range, Credit Score Level and CreditScoreID.
- Dim_Country: Captured CountryID and Country.
- Dim_Age: Stored Age Range and AgeID.
- Dim_Balance: Stored Balance Range and BalanceRangeID.
![image](https://github.com/user-attachments/assets/b9071eb0-7c27-4972-b6f0-117af97e2f76)



## Recommendation
**1.** The bank should consider retirement-focused financial products, investment planning tools, or age-targeted advisory services to retain customers in this age group.\
**2.** The bank should revisit its product bundling strategy, making sure that customers with multiple products feel they are receiving sufficient value. Alternatively, it may be useful to personalize bundles and create more flexible options.\
**3.** A thorough investigation into customer satisfaction and service quality in Germany should be conducted. The bank should focus on improving its customer support and perhaps reconsider its product offerings in Germany to align with local needs and expectations.\
**4.** The bank should develop re-engagement strategies to target inactive customers, such as personalized outreach, special offers, or financial consultations, to re-engage them and reduce churn.

