# machine_learning_project-unsupervised-learning

## Project Outcomes
- Unsupervised Learning: perform unsupervised learning techniques on a wholesale data dataset. The project involves four main parts: exploratory data analysis and pre-processing, KMeans clustering, hierarchical clustering, and PCA.
### Duration:
Approximately 1 hour and 40 minutes
### Project Description:
In this project, we will apply unsupervised learning techniques to a real-world data set and use data visualization tools to communicate the insights gained from the analysis.

The data set for this project is the "Wholesale Data" dataset containing information about various products sold by a grocery store.
The project will involve the following tasks:

-	Exploratory data analysis and pre-processing: We will import and clean the data sets, analyze and visualize the relationships between the different variables, handle missing values and outliers, and perform feature engineering as needed.
-	Unsupervised learning: We will use the Wholesale Data dataset to perform k-means clustering, hierarchical clustering, and principal component analysis (PCA) to identify patterns and group similar data points together. We will determine the optimal number of clusters and communicate the insights gained through data visualization.

The ultimate goal of the project is to gain insights from the data sets and communicate these insights to stakeholders using appropriate visualizations and metrics to make informed decisions based on the business questions asked."

# Goals
To perform:
- exploratory data analysis and pre-processing on the Wholesale Customers Data Set
- K Means clustering, determine optimal value for K, and converge on cluster centroids
- Hierarchical clustering, and confirm optimal value for K
- Principal Component Analysis and determine how to best reduce the number of features

# EDA
- No zeros or null values
- Viewed feature distribution and strip plots
- Removed outliers
- Built correlation heatmap and pair plots for features

# K Means Clustering
- Chose to only use Fresh and Frozen features as they had relatively low correlation, and 3 somewhat visable clusters on their pair plot
- Manually converged on cluster centroids
- Used KMeans function to confirm these centroids
- Optimized the value for K by building inertia and silhouette score plots

# Hierarchical
- Built a dendrogram for all discrete features (removed Channel and Region) which showed that 2 clusters was optimal
- Built a dendrogram for just the Fresh and Frozen features, which showed that 2 or 3 clusters would be optimal
- With the Fresh and Frozen features, compared using different linkage methods for clustering. Complete linkage worked the best, but the results were not as good as using KMeans.

# PCA
- Using all discrete features, built a scree plot to determine the number of PC's to use
- Found that by using PC's 1 and 2, we can account for ~55% of the explained variance
- Built a KMeans model using all discrete features, and colour coded the PCA results by the KMeans labelling.  A K value of 2 gave us the best results.
- Colour coded the PCA results by Channel and Region.  Coding the results by Region gave 2 noticable clusters.

# Conclusions

1. The optimal value for K when only looking at features Fresh and Frozen is 3.  If we assume that each row is a grocery store (customers of a wholesaler), these three clusters could be "healthy" grocery stores that specialize in fresh food, big chains like Walmart and No Frills that make large selections of frozen food, and grocery stores that sell a variety of both fresh and frozen.

2. When using all of the discrete features, the optimal value of K is either 2 or 3.  Based on the Dendrogram, K = 2 is better.

3. The discrete values can be used to fairly accurately estimate the Channel.

4. Reducing the discrete features to 2 principle components can still produce an accurate clustering model.



