Customer Segmentation Project
This is my project 3 for Data Science internship (Unsupervised Learning).

What is this project about
In this project I had to group mall customers into segments based on how they behave, but there was no labels telling me what the correct groups are, thats why its called unsupervised learning. Dataset has 200 customers with columns Age, Annual Income, Gender and Spending Score.

What i did
Only used Age, Income and Spending Score for the clustering. I removed CustomerID because its just a random number and doesnt mean anything, and i kept Gender separate to describe the clusters later, not to actually cluster on it
Scaled the data using StandardScaler because Income and Age have very different ranges and that would mess up the distance calculation if not scaled
Used PCA to reduce everything to 2 components, this kept about 78% of the variance
To find best number of clusters i used Elbow Method and Silhouette Score. Elbow method showed K=4 was good, Silhouette score was actually a tiny bit higher at K=2 but almost same as K=4. I picked K=4 because 2 clusters is too simple for real business use and K=4 also matches what this dataset is known for
Ran K-Means with K=4 and checked the average age/income/spending in each cluster to understand what type of customer each group actually is
Results - the 4 customer types i found
Cluster	Age	Income	Spending Score	Count	% Female
0 - Older Moderate Spenders	52.1	$46.3k	40.1	69	58.0%
1 - High Value Trendsetters	30.0	$79.1k	70.8	58	58.6%
2 - Budget Conscious Explorers	25.6	$32.6k	67.5	38	60.5%
3 - Affluent Conservatives	41.7	$88.2k	17.3	35	42.9%
The most interesting group is Cluster 3, they have the highest income but spend the least. This is actually useful for a business because it means these people have money but for some reason arent spending, so they could be targeted with better offers.

How to run
Install these:
Get the dataset from Kaggle (search "Mall Customer Segmentation Data") and put Mall_Customers.csv in the same folder
Open customer_segmentation.ipynb and run all the cells
Tools used
Python, Pandas, Scikit-learn, Matplotlib, Kneed, Jupyter Notebook

By
Urwa-til-Wosqa
