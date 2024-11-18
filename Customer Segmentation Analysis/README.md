# Customer Segmentation Analysis for E-Commerce Business

## INTRODUCTION

In the fast-paced world of e-commerce, understanding customer behavior is vital for driving business growth and achieving customer satisfaction. Customer segmentation allows businesses to categorize their customers into distinct groups based on shared characteristics and behaviors. These insights enable the development of targeted marketing campaigns, personalized experiences, and efficient resource allocation. This report presents the findings of a customer segmentation analysis performed on an e-commerce dataset to inform strategic decision-making and enhance overall business performance.

## Objectives
The primary goal of this project is to analyze customer behavior and purchase patterns to create meaningful customer segments. These segments can help the company:
- Design targeted marketing strategies.
- Improve customer satisfaction by tailoring services.
- Enhance resource allocation for better business outcomes.

## Data Sources

This dataset was gotten from oasis infobyte internship as part of the required tasks.

# Data Collection and Columns Overview

The dataset used for this analysis includes a wide range of customer demographic and behavioral data. Below is a detailed list and explanation of all the columns in the dataset:

## Columns in the Dataset:

### 1. **Income**
- Represents the annual income of the customer. This can help analyze spending power and purchasing patterns.

### 2. **Kidhome**
- The number of children in the customer's household. This influences buying behavior, particularly for family-related products.

### 3. **Teenhome**
- The number of teenagers in the customer's household. This affects product preferences, such as items for teenagers.

### 4. **Recency**
- A measure of how recently the customer made a purchase. This is an indicator of customer engagement.

### 5. **MntWines**
- The total spending on wine products by the customer.

### 6. **MntFruits**
- The total spending on fruit products by the customer.

### 7. **MntMeatProducts**
- The total spending on meat products by the customer.

### 8. **MntFishProducts**
- The total spending on fish products by the customer.

### 9. **MntSweetProducts**
- The total spending on sweet products by the customer.

### 10. **MntGoldProds**
- The total spending on gold-related products by the customer.

### 11. **NumDealsPurchases**
- The number of purchases made using promotional deals or discounts.

### 12. **NumWebPurchases**
- The number of purchases made online through the company's website.

### 13. **NumCatalogPurchases**
- The number of purchases made through catalogs or direct mail offers.

### 14. **NumStorePurchases**
- The number of purchases made in physical stores.

### 15. **NumWebVisitsMonth**
- The number of times the customer visited the company's website in a given month.

### 16. **AcceptedCmp3**
- Whether the customer accepted marketing campaign 3 (1 for accepted, 0 for not).

### 17. **AcceptedCmp4**
- Whether the customer accepted marketing campaign 4 (1 for accepted, 0 for not).

### 18. **AcceptedCmp5**
- Whether the customer accepted marketing campaign 5 (1 for accepted, 0 for not).

### 19. **AcceptedCmp1**
- Whether the customer accepted marketing campaign 1 (1 for accepted, 0 for not).

### 20. **AcceptedCmp2**
- Whether the customer accepted marketing campaign 2 (1 for accepted, 0 for not).

### 21. **Complain**
- The number of complaints filed by the customer, indicating their level of dissatisfaction.

### 22. **Z_CostContact**
- The standardized cost of contacting the customer, which can help assess the efficiency of marketing outreach.

### 23. **Z_Revenue**
- The standardized revenue generated from the customer, indicating their contribution to overall revenue.

### 24. **Response**
- Whether the customer responded to a marketing campaign (1 for responded, 0 for not).

### 25. **Age**
- The age of the customer, which can be useful for demographic segmentation.

### 26. **Customer_Days**
- The number of days since the customer made their first purchase, indicating the length of their relationship with the company.

### 27. **marital_Divorced**
- Whether the customer is divorced (1 for divorced, 0 for not).

### 28. **marital_Married**
- Whether the customer is married (1 for married, 0 for not).

### 29. **marital_Single**
- Whether the customer is single (1 for single, 0 for not).

### 30. **marital_Together**
- Whether the customer lives with a partner (1 for living together, 0 for not).

### 31. **marital_Widow**
- Whether the customer is widowed (1 for widow, 0 for not).

### 32. **education_2n Cycle**
- Whether the customer has completed a secondary education cycle (1 for completed, 0 for not).

### 33. **education_Basic**
- Whether the customer has a basic level of education (1 for basic, 0 for not).

### 34. **education_Graduation**
- Whether the customer has completed a graduate-level education (1 for graduated, 0 for not).

### 35. **education_Master**
- Whether the customer has completed a master's degree (1 for master's, 0 for not).

### 36. **education_PhD**
- Whether the customer has a PhD (1 for PhD, 0 for not).

### 37. **MntTotal**
- The total amount spent by the customer across all categories.

### 38. **MntRegularProds**
- The total spending on regular products, excluding premium items.

### 39. **AcceptedCmpOverall**
- The total number of marketing campaigns accepted by the customer.


## TOOLS
- Analysis - jupyter notebook
- Visualization - jupyter notebook

# Methodology

### Data Cleaning and Preparation

Before analyzing the data, several steps were taken to clean and prepare the dataset for analysis. This phase ensures that the data is consistent, accurate, and ready for statistical modeling or segmentation.

## Data Quality Assessment

- A thorough check revealed 184 duplicate records in the dataset, Which was removed.
- No missing values were found in the dataset
- Each record was verified to ensure data completeness and consistency
- After completing these steps, the dataset was ready for exploratory analysis, segmentation, and building machine learning models to uncover valuable insights about customer behavior.

## Data Standardization
The following features were scaled using StandardScaler from sklearn.preprocessing:

- Income
- MntTotal (Total Amount Spent)
- NumWebPurchases
- NumStorePurchases

This standardization transforms the features to have a mean of 0 and standard deviation of 1, making them comparable and suitable for various machine learning algorithms. The scaled features were stored in a new DataFrame called scaled_clas.

## Customer Segmentation
K-Means clustering was used to group customers based on their behavioral patterns. The elbow method was applied to identify the optimal number of clusters by evaluating distortion scores for different values of k. The final segmentation resulted in four distinct customer groups.

## Visualization
Using Python libraries such as matplotlib and seaborn, visualizations were created to illustrate the results of the analysis. Scatter plots were used to depict cluster separation, while bar charts and histograms highlighted key characteristics of each segment.

## Insights and Recommendations
The characteristics of each cluster were analyzed to derive actionable insights, including spending behavior, purchasing preferences, and potential for targeted marketing.

# Results and Analysis
## Optimal Number of Clusters
Our customer segmentation analysis leveraged K-means clustering to identify distinct customer groups, with the optimal number of clusters determined through rigorous elbow method analysis. The implementation of StandardScaler on key features including Income, Total Purchase Amount (MntTotal), Web Purchases, and Store Purchases ensured normalized data distribution for accurate clustering.
The elbow curve visualization reveals a clear inflection point at k=4, indicating this as the optimal number of clusters. 
Beyond this point, the decrease in within-cluster sum of squares (inertia) becomes marginal, confirming that four segments provide the most efficient balance between cluster complexity and explanatory power.

## Cluster Characteristics

Cluster 0: Premium
- Customers with high income and high spending.
- Represent the most affluent segment, with frequent purchases and high transaction values.

Cluster 1: Budget Conscious
- Customers with low income and low spending.
- Display price-sensitive behavior, often purchasing lower-priced items.

Cluster 2: High-Value
- Customers with above-average income and spending.
- Consistent buyers with strong spending patterns, making them highly valuable.

Cluster 3: Mid-Market
- Customers with average income and low spending.
- Balanced purchasing behavior, with opportunities for increased engagement.

## Segment Insights
### 1. Premium Customers (Cluster 0)

- Exhibit exceptional spending levels and frequent purchases.
- Represent the most valuable segment in terms of revenue contribution.
- Require strategies focused on exclusivity and high-value services.

### 2. Budget Conscious Customers (Cluster 1)

- Show price-sensitive behavior and lower transaction values.
- Despite lower spending, their large segment size offers significant potential.
- Best approached with value-oriented promotions and incentives.

### 3. High-Value Customers (Cluster 2)

- Above-average spending and income, with consistent engagement.
- Represent a key growth segment with strong potential for retention and upselling.
- Targeted recommendations and premium service offerings are effective here.

### Mid-Market Customers (Cluster 3)

- Average income with relatively low spending patterns.
- Offer opportunities for targeted campaigns to increase purchase frequency.
- Focus on enhancing their perceived value through personalized communication.

## Key Insights

The standardized feature analysis reveals:

- Income correlation: A strong differentiator between Premium, High-Value, and Budget Conscious segments.
- Web purchase frequency: A consistent predictor of segment membership.
- Store purchases: Variations across segments suggest opportunities for omnichannel engagement.
- Spending patterns: Significant differences between clusters, providing actionable insights for marketing strategies.

## Strategic Recommendations
#### Premium Customers (Cluster 0)
- Retention: Implement exclusive benefits, premium service offerings, and loyalty programs.
- Engagement: Provide early access to products or events to deepen brand loyalty.

#### Budget Conscious Customers (Cluster 1)
- Activation: Offer value-oriented promotions and bundling strategies to increase basket size.
- Engagement: Use personalized communication to highlight discounts and value deals.

#### High-Value Customers (Cluster 2)
- Upselling: Develop tailored recommendations to increase spending.
- Retention: Strengthen loyalty with premium perks and proactive engagement strategies.

#### Mid-Market Customers (Cluster 3)
- Frequency Boost: Create campaigns encouraging regular purchases through rewards.
- Perceived Value: Focus on providing additional value through targeted messaging and incentives.


## Implementation Framework
#### 1. Automated Segmentation Pipeline

- Regularly update customer data and execute clustering algorithms for dynamic segment membership updates.
- Preprocessing with StandardScaler and consistent feature engineering ensures reliable results.

#### 2. Real-Time Classification

- Develop a classification model for immediate assignment of new customers to clusters.
- Enable personalized customer journeys from the first interaction.

#### 3. Monitoring and Optimization

- Implement tracking systems for segment migration and performance metrics.
- Refine strategies based on segment behavior and key performance indicators.

# Conclusions
This analysis confirms the presence of four distinct customer segments, each requiring tailored engagement strategies. The segmentation approach highlights the importance of income, spending patterns, and purchase frequency in understanding customer behavior.

Key findings include:

- The Premium cluster is the most affluent and requires high-touch retention strategies.
- The High-Value cluster offers significant growth potential through targeted upselling.
- The Budget Conscious cluster benefits from value-driven campaigns, given their price sensitivity.
- The Mid-Market cluster shows promise for increased engagement through personalized communication.

By implementing these recommendations and leveraging dynamic segmentation pipelines, businesses can enhance customer satisfaction and drive sustained revenue growth. Future enhancements should focus on incorporating additional behavioral data and expanding feature sets to refine segmentation further.
