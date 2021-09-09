# Customer-Segmentation-by-using-K-means
This is my final project at dibimbing.id
## Executive Summary
- Focus on finding the most valuable customer segment 
- Reviewing the company's resources
- Get more ROI
- E-Commerce Data : frequency of orders - amount of money spent
- K-means clustering algorithm is a great tool
- EDA need before
## Data Introduction
[Source Data] (https://www.kaggle.com/carrie1/ecommerce-data)
## Exploratory Data Analysis
### - Handling NA values in the CustomerID
Customer ID is crutial for this analysis, so I will have to drop NA values there.
### - Changing the InvoiceDate Column to DateTime Format.
In order to prevent any issues with dates, I like to make sure all the data is in the appropriate format.
### - Filtering Negative (canceled) Orders.
If you look at the Quantity column, you notice some negative values there - canceled or returned orders. I need to remove those orders.
### - Removing Incomplete Data. 
December 2011 - not a full month in this data set.
### - Calculating The Sales Column 
Multiplying the Quantity and UnitPrice columns.
### - Transforming Data 
Each record represents the purchase history of individual customers.
## Data Standardization
Clustering algorithms (k-means clustering including) are highly affected by the scales of the data. So, We need to standardize the data to be on the same scale.
## Find The Best Number of Clustering
- Elbow Method
- Silhoutte Method
- Business Considering
## Model Clustering
K-means algorithm is an iterative algorithm that tries to partition the dataset into Kpre-defined distinct subgroups (clusters) where each data point belongs to only one group.
- Specify number of clusters K.
- Initialize centroids by first shuffling the dataset and then randomly selecting K data points for the centroids without replacement.
- Keep iterating until there is no change to the centroids. i.e assignment of data points to clusters isn’t changing.
## Recommendation
- 1st cluster has the lowest numbers for all three attributes - Total Sales, Order Count, and Average Order Value. It means that the 1st cluster contains customers with the lowest amount of sales, orders, and lowest average per-order value.
- 2nd cluster has the highest numbers for all attributes. The customers in the third cluster purchase expensive items and give the business the highest revenue. The company should focus on this cluster, as it will result in the highest ROI.
- The customers in the 3rd cluster have low numbers of orders and total sales, but their average per-order value is high. So these customers buy expensive items infrequently. It would be great to recommend expensive products to this segment group.
- Customers in the 4th cluster have a high value for OrderCount, but their AvgOrderValue is low. Basically, these customers make frequent purchases of low-value items. The business can make recommendations of low-value items to this segment, in order to get a high engagement rate.
