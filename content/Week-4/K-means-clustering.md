---
title: "K-means Clustering: My Own Insights"
date: 2021-09-06 00:00:00 +0000
katex: true
---
# K-means-clustering

A cluster refers to a collection of data points aggregated together because of certain similarities.

K-Means clustering is used to clump unsupervised data into K different subgroups / clusters, in which each observation belongs to the cluster with the nearest mean (cluster centers or cluster centroid), serving as a prototype of the cluster. 

The K-means algorithm identifies k number of centroids, and then allocates every data point to the nearest cluster, while keeping the centroids as small as possible. K-**means** clustering is called so, cause it finds the mean (ie trhe centroid).

## K means algorithm:

### Classify Clusters

### Move older centroid to new centroid of Data Points

### Stopping iterations:
- The centroids have stabilized — there is no change in their values because the clustering has been successful.
- The defined number of iterations has been achieved.



# My Idea, and How can this be improved:



### K-Means - Difference in pattern recognition by a Computer and our Brain

What I observed is to find correlation between points in data, we look out for the gaps between clusters of data points.
i e if we inverted the colors, we look for holes in the graph (where the data was more dense).
So my idea of the algorithm is

1. Randomly **"seed"** the data with noise (say . s) [while the data is denoted by X], such that there is less noise where there is more data. i.e. each data point has a sort of radius around which there occurs no noise.
2. Next we get rid of the data points (X)on the graph. 
3. Get rid of the random noise in less dense areas and put the centroid there.

This is computationally a little bit more resourceful, but it may well be much more acurate.


