# machine_learning_project-unsupervised-learning

## Project Outcomes
- Unsupervised Learning: perform unsupervised learning techniques on a wholesale data dataset. The project involves four main parts: exploratory data analysis and pre-processing, KMeans clustering, hierarchical clustering, and PCA.

## Process
### 1. Exploratory data analysis and pre-processing:
#### Relationships/Correlations Among Features
- There was some correlation between a few of the features - namely between "Milk", "Grocery", and "Detergents_Paper"

#### Missing Values and Outliers
- There were no missing values, but the outliers needed to be addressed since some of the unsupervised algorithms can be sensitive to these.
- Decided to make any outliers equal to either Q1 - 1.5*IQR if it was less than that value, or Q3 + 1.5*IQR if it was more than that value.

### 2. Pre-processing
#### Scaling and Normalization
- Used a PowerTransform() scaler with box-cox method in order to scale the data, paired with a min/max scaler afterwards.

### 3. Model Training
Unsupervised learning: We performed k-means clustering, hierarchical clustering, and principal component analysis (PCA) to identify patterns and to group similar data points together. We hoped to determine the optimal number of clusters and communicate the insights gained through data visualization.

## Conclusion
1. We saw that the most correlated features were "Milk", "Grocery", and "Detergents_Paper" with a correlation of:
    - 0.92 for "Grocery" and "Detergents_Paper"
    - 0.73 for "Milk" and "Grocery"
    - 0.66 for "Milk" and "Detergents_Paper"
2. By combining both K-means and Hierarchical Clustering methods, we were able to deduce that 2 - 4 clusters was an appropriate choice.  K-means particularly yeilded an elbow at k=2, whereas Hierarchical methods showed some promise for that 2 - 4 cluster range.
3. Using PCA we discovered that at least 70% of explained variability is reached when we reduced our dimensionality to 2 components, and 90% of explained variability was reached when we used 4 components. In other words, the data might inherently lie in a lower-dimensional space, and the first two principal components retain the most essential information about the variability in the data.
4. The clearest separation was seen when reducing our dimensions to 2 and clustering into 2 groups.  The fact that a small number of principal components and clusters provide a clear separation implies that the original features may have some level of redundancy or correlation. The principal components and clusters offer a more concise and interpretable representation of the data.