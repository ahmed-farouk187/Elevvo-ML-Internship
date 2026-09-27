# Task 2 - Customer Segmentation

In this task I grouped mall customers into segments based on their annual income and spending score using K-Means clustering.

Dataset: Mall Customer Segmentation Data from Kaggle
https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python

Libraries used: pandas, numpy, matplotlib, scikit-learn

## What I did

- Loaded the data and checked it (200 customers, no missing values or duplicates)
- Plotted income vs spending score and the distributions of age, income and spending
- Scaled income and spending with StandardScaler
- Used the elbow method and silhouette score to choose the number of clusters
- Ran K-Means with 5 clusters and plotted the groups
- Made a summary of each cluster and a chart of average spending per cluster
- Bonus: tried DBSCAN and compared it with K-Means

## Results

The elbow method and silhouette score both pointed to 5 clusters (silhouette = 0.555).

The 5 groups:

- Average income, average spending - 81 customers
- High income, high spending - 39 customers
- Low income, high spending - 22 customers
- High income, low spending - 35 customers
- Low income, low spending - 23 customers

The high income / low spending group is the biggest opportunity for the mall.

DBSCAN found 6 clusters and marked 23 customers as noise. K-Means worked better for this data because it puts every customer in a group.

## How to run

Download Mall_Customers.csv from Kaggle, put it in the same folder as the notebook (or upload it in Colab), and run all the cells.
