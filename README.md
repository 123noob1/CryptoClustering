# CryptoClustering
For this module challenge, use unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

## Requirements
### Find the Best Value for k Using Original Data
1) Prepare the data using <code>StandardScaler()</code> from <code>scikit-learn</code> to normalize the data from the data.
2) Create a DataFrame using the scaled data.
3) Determine the best <code>k</code> value by plotting an <code>Elbow Curve</code> chart.

Answer the following question:<br/>
<b>What is the best value for k using the original data?</b><br/>
- 4 looks like the optimal value for k where the inertia starts decreasing linearly. However, 3 can also be tested to see the difference as well.

### Cluster Cryptocurrencies with K-means Using the Original Scaled Data
1) Fit the <code>K-means</code> model using the <code>k</code> determined from above.
2) Predict the clusters to group the cryptocurrencies using the scaled DataFrame.
3) Create a scatter plot using <code>hvPlot</code> with the predicted clusters.

### Optimize Clusters with Principal Component Analysis
1) Use the original scaled DataFrame and perform the Principal Component Analysis (PCA) and reduce the features (or columns) to three components.
2) Retrieve the explained variance to determine how much information can be attributed to each principal component.
3) Create a new DataFrame using the PCA data.

Answer the following question:<br/>
<b>What is the total explained variance of the three principal components?</b><br/>
- 0.895031657030984 ratio or 89.50%.

### Find the Best Value for k Using the PCA Data
Refer to the steps above in finding the <code>k</code> value for the original data and apply it to the PCA data.

Answer the following questions:<br/>
<b>What is the best value for k using the PCA data?</b><br/>
- 4

<b>Does it differ from the best k value found using the original data?</b><br/>
- No, even though there are differences in the inertia between the two data, the k value of 4 is still the best optimal value to use to test with.

### Cluster Cryptocurrencies with K-means Using the PCA Data
Refer to the steps above in creating the scatter plot for the predicted clusters on the original data and apply it to the PCA data.

Answer the following question:<br/>
<b>What is the impact of using fewer features to cluster the data using K-Means?</b><br/>
- Although both the Elbow Curves from the original and PCA data suggested the same k value (k = 4), the PCA model is better for machine learning with this dataset where the PCA's scatter plot allowed for a better clustering of the groups with each cluster being more distinct from another versus that in the original data's scatter plot.
