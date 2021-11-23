# Clustering Techniques

## Hierarchical-clustering
Is a method of cluster analysis which seeks to build a hierarchy of clusters without having fixed number of cluster.
- Agglomerative methods begin with ‘n’ clusters and sequentially combine similar clusters until only one cluster is obtained.
- Divisive methods work in the opposite direction, beginning with one cluster that includes all the records and Hierarchical methods are especially useful when the target is to arrange the clusters into a natural hierarchy.
  ## Pros
    - Ease of handling of any forms of similarity or distance.
    - Consequently, applicability to any attributes types.
  ## Cons
    - Hierarchical clustering requires the computation and storage of an n×n  distance matrix. For very large datasets, this can be expensive and slow.

## K-Means
Is method of cluster analysis using a pre-specified no. of clusters. It requires advance knowledge of ‘K’.
- First, we initialize k points, called means, randomly.
- We categorize each item to its closest mean and we update the mean’s coordinates, which are the averages of the items categorized in that mean so far.
- We repeat the process for a given number of iterations and at the end, we have our clusters.
  ## Pros
    - Scales well on large dataset.
    - Generalizes to clusters of different shapes and sizes, such as elliptical clusters.
    - Can warm-start the positions of centroids.
  ## Cons
    - k-means has trouble clustering data where clusters are of varying sizes and density.
    - Centroids can be dragged by outliers, or outliers might get their own cluster instead of being ignored.

## Gaussian Mixture clustering
- This clustering approach assumes data is composed of distributions. As distance from the distribution's center increases, the probability that a point belongs to the distribution decreases
  ## Pros
    - These models is that they can handle a greater variety of shapes, primarily clusters that form ellipsis shapes.
    - Another positive is that these models allow for soft classification. K-Means is a hard classification model where each data point is assigned to a single cluster. The Gaussian Mixture method, however, calculates probabilities of data points belonging to clusters
  ## Cons
    - Takes more computation time than K-means.
    
## Density Based clustering
Is a method that divides the data points into a number of specific batches or groups, such that the data points in the same groups have similar properties and data points in different groups have different properties in some sense.
- Find all the neighbor points within eps and identify the core points or visited with more than MinPts neighbors.
- For each core point if it is not already assigned to a cluster, create a new cluster.
- Find recursively all its density connected points and assign them to the same cluster as the core point. 
- A point a and b are said to be density connected if there exist a point c which has a sufficient number of points in its neighbors and both the points a and b are within the eps distance. This is a chaining process. So, if b is neighbor of c, c is neighbor of d, d is neighbor of e, which in turn is neighbor of a implies that b is neighbor of a.
- Iterate through the remaining unvisited points in the dataset. Those points that do not belong to any cluster are noise.

**DBSCAN algorithm overcomes all the above-mentioned drawbacks of K-Means algorithm. DBSCAN algorithm identifies the dense region by grouping together data points that are closed to each other based on distance measurement.**


