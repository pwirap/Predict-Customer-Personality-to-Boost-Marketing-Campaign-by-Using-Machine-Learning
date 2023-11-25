# Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning
Predict Customer Personality using Clustering

# Background and Objective
A company can experience rapid growth by understanding the personality traits of its customers, allowing it to provide better services and benefits to potential loyal customers. By analyzing historical marketing campaign data to enhance performance and target the right customers for transactions on the company's platform, our focus is on creating a predictive clustering model. This will facilitate decision-making for the company based on insights derived from data.

# Scope of problem
The objective is to leverage historical marketing campaign data to create a predictive clustering model that enhances performance and targets the ideal customers for transactions on the company's platform. By understanding the personality traits of customers, the aim is to enable better services and benefits, fostering potential loyalty. This model will aid in decision-making for the company by deriving insights from data analysis, potentially driving rapid growth by catering to customer needs effectively.

# Data

# Data Analysis
## Conversion Rate Analysis Based on Age

![image](https://github.com/pwirap/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/99533745/de7051c8-6176-45ad-9cdf-5090bf37e809)

1. Elderly and young adults have a conversion rate of approximately 40%.
2. Adults exhibit the lowest conversion rate, which is around 31%.

## Conversion Rate Analysis Based on Total Children

![image](https://github.com/pwirap/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/99533745/69a5c8c8-1b7c-4e13-8d8b-d1caeb73bbcf)

1. Overall, there is a positive correlation between the number of children and the Conversion Rate (CVR), indicating that as the number of children increases, the CVR also tends to rise.
2. Customers with three children exhibit the highest CVR, approximately 55.25%.
3. Conversely, customers without any children demonstrate the lowest CVR, around 19.80%.

## Conversion Rate Analysis Based on Total Accepted Campaign

![image](https://github.com/pwirap/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/99533745/caaab6d6-2139-4d99-945a-43879b2cd36f)

1. In broad strokes, the fewer customers who accept the campaign, the higher the conversion rate (CVR).
2. This demonstrates that the likelihood of the existing campaign being less appealing is high.
3. Because the existing campaigns do not seem to enhance the current transaction volume.
4. The highest CVR is observed among customers who do not receive the campaign at all, reaching 39.49%.

## Conversion Rate Analysis Based on Academy Level

![image](https://github.com/pwirap/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/99533745/514d42ff-86f5-4a87-ae20-541dc6588349)

If looked at overall, the levels of education have the same conversion rate (CVR) except for high school (SMA), which has the highest CVR at 97.89%.

## Conversion Rate Analysis Based on Status

![image](https://github.com/pwirap/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/99533745/2ec07df9-fd33-4f89-92c6-8eb6ac1d1111)

1. Duda boasts the highest Conversion Rate (CVR) at an impressive 47.50%.
2. Janda, on the other hand, exhibits a lower CVR, standing at 29.24%.

## Conversion Rate Analysis Based on Years Since Join

![image](https://github.com/pwirap/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/99533745/e70cca12-6949-45b5-b5e8-7221fd6beff2)

1. The longer the customer has been a member, the higher the conversion rate (CVR), although the difference is not prominently noticeable.
2. The highest point is at 2 years, reaching 37.25%.
3. The lowest point is less than 1 year, around 35.20%.

## Conversion Rate Analysis Based on Years Since Join

![image](https://github.com/pwirap/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/99533745/3be1612d-de4e-44e6-bb5f-e94e6581c0de)

1. The lower the total transaction amount, the higher the Conversion Rate (CVR).
2. The majority of customers have a total transaction amount ranging from 500,000 to 1,000,000, with a corresponding CVR of approximately 0% to 50%.

# Data Preprocessing and Feature Engineering
1. Division of total purchases by total visitors.
2. new group for age :
- Less than 17 years = Child
- 19 - 44 years = Young Adult
- 45 - 74 years = Adult
- More than 75 years = Elderly

3. Since there is no information on when this data was collected, the last date in Dt_Customer is used to determine how long a customer has been a member to make a new feature called Feature days_since_join
4. Summing up all the total expenditures to make a new feature called Feature Total Transaksi
5. The number of children the customer has is a new feature called Feature Total Anak
6. The number of customers who received the campaign is a new feature called Feature Total Menerima Campaign
7. Fitur Dt_Customer could change into Date
8. There are 24 null values in the Income feature, and they will be filled with the median of the data.
9. There are no duplicate

# Feature Selection

To segment customers, there is a method known as RFM Analysis :

![image](https://github.com/pwirap/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/99533745/fade8b94-2d61-4bb7-862d-0954ea0843d4)


# Elbow Score & Silhouette score

In the provided Elbow Score below, it is evident that when the number of clusters is set to 5, the inertia score does not change significantly.

![image](https://github.com/pwirap/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/99533745/60ec5e99-72c4-485e-a43b-bfe5993deb51)

In the Silhouette score below, it is evident that when the number of clusters is set to 5, it exhibits the highest silhouette score compared to others, specifically at 0.35.

![image](https://github.com/pwirap/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/99533745/b3f643f1-cc4a-42ff-8bed-d3565f43b33e)

# 3-D Visualization of Customer Clusters

![image](https://github.com/pwirap/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/99533745/b1d45a7c-8af5-465d-82bb-df04a2ff3456)

The results of dividing customers based on characteristics produce 5 sections, which have been divided based on Recency, Total Purchases and Total Spents. Where the 5 parts are referred to as:
1. Low Valued Customers
2. Low-Medium Valued Customers
3. Medium Valued Customers
4. Medium-High Valued Customers
5. High Valued Customers

## Characteristics Each Group of Customers
![image](https://github.com/pwirap/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/99533745/615ec766-929c-4dbe-aa26-a16e9abcd63b)


# PCA
Because it is difficult to see the detailed division between the 5 groups because it uses 3 dimensions. So PCA is carried out to clearly see the division between each customer group

![image](https://github.com/pwirap/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/99533745/7f0dc2e0-2ba2-4895-bb5a-3907973bb380)

# Business Recommendation
1. Provide Premium Product and Service Offers to High-Value Customers in order to maintain a strong relationship with them, which can yield long-term benefits while maximizing revenue from this customer segment and ensuring a satisfying shopping experience.
2. For Low and Low-Medium Value customers with low income characteristics, they tend to visit the website but often do not engage in transactions. Furthermore, it appears that only a small percentage of them are responsive to the campaigns being offered. Therefore, it is essential to reevaluate the campaign strategy for this customer group, ensuring that it is better tailored to their needs, prompting them to not only visit the website but also complete transactions.

# Potential Impact
If we continue to focus on Customer Groups/Clusters and prevent them from churning, there is still a potential GMV of approximately IDR 1.3 billion per year. With the detail below.

![image](https://github.com/pwirap/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/99533745/de491412-02f7-423c-bd0f-aa8a95a8a408)
