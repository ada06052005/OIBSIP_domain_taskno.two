# OIBSIP_domain_taskno.two

# objectives
Practical experience with clustering algorithms.

Data cleaning and exploration skills.

Visualization techniques for conveying insights.

# Project Summary: Customer Segmentation Analysis
This project performs a customer segmentation analysis using the iFood dataset to identify distinct customer groups based on their purchasing behavior and demographic information. The goal is to provide data-driven recommendations for targeted marketing strategies. The analysis was carried out in the following steps:

1. Data Cleaning and Feature Engineering
The initial dataset was cleaned by handling a few key issues:

Missing Income Values: Missing values in the 'Income' column were imputed by replacing them with the mean income to ensure all data could be used for analysis.

Outlier Age Value: A single outlier with an age of 123 years was removed to prevent it from skewing the results of the analysis.

Creating New Features: New, more informative features were created to better capture customer behavior:

Total_Mnt_Spent: The total amount spent across all product categories (wines, fruits, meat, fish, sweets, and gold products) was calculated to get a single, comprehensive spending metric.

Total_Num_Purchases: The total number of purchases made through different channels (deals, web, catalog, and in-store) was calculated to understand purchase frequency.

Removing Unnecessary Columns: Columns with constant values (Z_CostContact and Z_Revenue) were dropped as they provide no useful information for clustering or segmentation.

2. Descriptive Statistics
A summary of descriptive statistics was generated for key numerical features to provide a foundational understanding of the dataset.

Income: The average income was approximately \$51,622, with a wide standard deviation, suggesting a diverse income range among customers.

Age: The average age of customers was around 51 years old, indicating a relatively mature customer base.

Total_Mnt_Spent: On average, customers spent \$606, but the high standard deviation shows that spending habits vary significantly across the customer base.

Total_Num_Purchases: Customers made an average of 15 purchases, but this metric also had a large standard deviation, highlighting different levels of engagement.

3. Customer Segmentation with K-Means Clustering
To segment the customers, K-Means clustering was applied using a set of relevant features including Income, Total_Mnt_Spent, Total_Num_Purchases, Age, Recency, and AcceptedCmpOverall.

Data Scaling: The features were standardized using StandardScaler to ensure that each feature contributes equally to the clustering process, preventing features with larger scales (like income) from dominating the results.

Elbow Method: An elbow method plot was used to determine the optimal number of clusters. Based on the plot, a value of k=3 was selected as the ideal number of segments.

Clustering: The K-Means algorithm was then run with 3 clusters, and the resulting segment labels were added to the original DataFrame. The customer count for each segment was printed to show the distribution.

4. Visualization and Recommendations
A scatter plot was created to visualize the customer segments based on their total spending and purchase frequency.
This visualization clearly separated the customers into three distinct groups. The analysis of these segments leads to the following strategic recommendations:

Engage Low-Spending Customers: Offer targeted discounts and loyalty programs to the low-spending segment to increase their purchase frequency and average transaction value.

Strengthen Relationships with Frequent Buyers: Retain frequent buyers with personalized offers and cross-selling campaigns to encourage them to explore different product categories.

Retain Premium Customers: Acknowledge and reward the high-spending segment with exclusive VIP offers, personalized services, and early access to new products to build brand loyalty.

Optimize Marketing Efforts: Tailor marketing campaigns for each segment to maximize effectiveness and return on investment.

# Tools Used
This project utilized the following Python libraries:

Pandas for data manipulation and cleaning.

NumPy for numerical operations.

Scikit-learn for machine learning, specifically StandardScaler for data preprocessing and K-Means for clustering.

Matplotlib.pyplot and Seaborn for data visualization.

