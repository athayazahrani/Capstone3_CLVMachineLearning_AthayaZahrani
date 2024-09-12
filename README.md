# Athaya Zahrani Irmansyah - Capstone Project Module 3 - Predistion of Customer Lifetime Value (CLV) using Machine Learning Algorithm (in Bahasa)
_Athaya Zahrani Irmansyah as a Purwadhika JCDS-0408 Student On Site Bandung 2024 / Capstone Project Module 2 Data Analysis with Case Study NEW YORK CITY TAXIS AND LIMOUSINES COMMISSION (NYC TLC) TRIP RECORD_

## Context
For companies, acquiring new customers requires significantly more effort than retaining existing ones. Therefore, customer retention becomes crucial for maintaining stable revenue, as repeat purchases from existing customers allow the business to continue operating smoothly. For this reason, companies need to measure how valuable customers are to their business. One metric that can be used to assess this is the 1Customer Lifetime Value (CLV)1.

`CLV is a highly important metric in modern business management1. By helping companies understand the long-term value of their customers, CLV enables them to make smarter and more strategic decisions regarding marketing, retention, and product development. Improving CLV is directly linked to increasing profitability and business stability, making it a valuable tool in managing customer relationships.

`CLV represents the total amount of money a customer spends on a company during the duration of their business relationship1. Simply put, 1CLV is an estimate of the total revenue a customer can generate1. In practice, the CLV metric is often used by companies that rely on repeat sales (such as food or household product companies) and businesses with a subscription model (such as insurance or telecommunications companies).

## Problem Statement
The dataset used in this analysis is `'data_customer_lifetime_value.csv'`. Based on this data, a problem statement can be identified regarding `a car insurance company facing challenges in increasing its revenue`. One of the possible main causes is an ineffective marketing strategy, where the company allocates the same budget to all types of customers. As a result, the company spends more money on low-value customers while losing high-value customers.

To address this issue, the company has tasked the data science team with using the CLV metric to determine how valuable each customer is and adjust the marketing strategy based on that value. However, the company currently lacks a system that can quickly and accurately predict CLV, which causes delays in marketing strategy decisions as they are still made manually. Therefore, `a faster and more accurate CLV prediction (using machine learning algorithms) is crucial to support more effective and precise marketing decision-making.`

## Goals
Based on the explanation of the problem statement in point 2, it would be highly beneficial for the car insurance company (particularly the marketing division) to have a tool that can predict CLV using customer demographic data and car insurance data, as reflected in the dataset columns: `'Vehicle Class', 'Coverage', 'Renew Offer Type', 'EmploymentStatus', 'Marital Status', 'Education', 'Number of Policies', 'Monthly Premium Auto', 'Total Claim Amount', 'Income', and 'Customer Lifetime Value'`. With the implementation of machine learning algorithms as this tool, the manual processing of CLV data can be eliminated, speeding up the decision-making process for marketing strategies. The importance of CLV can be realized through several key aspects, such as:

1. **Marketing Spend Optimization**: By understanding CLV, the company can determine how much to spend on acquiring new customers without sacrificing profitability. CLV helps identify whether marketing campaigns are efficient and successful in attracting high-value customers.
2. **Customer Retention Strategy**: CLV provides insights into the importance of retaining existing customers. By focusing on improving customer retention, companies can increase their CLV and thereby enhance total revenue. Loyal customers are more likely to make repeat purchases, offer recommendations, and remain longer with the company.
3. **Customer Segmentation**:: Companies can use CLV to categorize customers based on their value. This enables them to give special attention to the most profitable customer segments and create tailored offers to retain and enhance their value.
4. **Budget and Resource Planning**:: Understanding CLV helps companies plan budgets and allocate resources more efficiently. By focusing on high-CLV customers, the company can prioritize initiatives that yield the best return on investment.
5. **Product and Service Development**:: CLV can also guide the development of new products and services. By knowing what keeps valuable customers loyal, companies can tailor their products and services to meet those customers' needs, increasing satisfaction and extending the customer relationship duration.

## Analytic Approach
The steps that will be taken involve analyzing the data to identify patterns from the various features that distinguish CLV for each customer. A regression model will be used to help the company provide a CLV prediction tool with the aid of machine learning algorithms. The detailed analysis steps are as follows:
- Conduct Exploratory Data Analysis (EDA) on the dataset.
- Perform Preprocessing on the dataset.
- Benchmark several regression models to select the most suitable model for the dataset.
- Perform Hyperparameter Tuning on the selected model to achieve lower error rates.
These steps aim to ensure accurate CLV predictions and optimize the company's marketing strategy.

## Metric Evaluation
The evaluation metrics that will be used are `RMSE, MAE, and MAPE`. These metrics will help evaluate the performance of the regression models used in predicting CLV, with the following descriptions:
- `RMSE`: Root Mean Square Error – This metric measures the square root of the average squared differences between predicted and actual values. It gives a higher weight to large errors.
- `MAE`: Mean Absolute Error – This is the average of the absolute differences between predicted and actual values. It provides a straightforward measure of prediction accuracy.
- `MAPE`: Mean Absolute Percentage Error – This calculates the average percentage difference between predicted and actual values, giving a sense of the error in percentage terms.

From the calculations obtained later, we will verify that `the smaller the values of RMSE, MAE, and MAPE, the more accurate the model is in predicting CLV`, according to the feature limitations used. This will serve as an indicator of the model's performance and its suitability for the given dataset. 

---

_Unlock the potential of your customer data! Discover how accurately predicting Customer Lifetime Value (CLV) can revolutionize your marketing strategy and drive higher profitability. Learn how leveraging machine learning models can provide faster, more precise insights, helping you focus on what truly matters—your most valuable customers._

- Open the "AthayaZahrani_Capstone3_ML-CLV_done.ipynb" file.

Thank You - Athaya Zahrani Irmansyah
