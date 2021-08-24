---
title: "KNN"
date: 2021-08-24 00:00:00 +0000
katex: true
---

## Feature Reduction For K-Nearest Neighbours

More features reduce accuracy. More info != more discriminative power!

This is because, some features are irrelevant, and introduce noise, and fool the algorithm (especially a lazy algo like Knn)
Moreover they may have redundant features, as we have limited computational resources.

So we use 2 methods to reduce this:

1. Feature Selection: F is fiven, find a subset F' which has elements less than F, such that it optimises cetrain aspects
2. Feature Extraction: Transforms or projects the existing features to a dimention m < n (original no. of dimentions)

Both cases we try to improve or maintain classification accuracy while simplifying it.

For **1**, we have \\( 2^n \\) possible subsets
so finding F' can use

- Optimised algo
- Heuristic / Greedy algo
- Randomised algo

For evaluation we have 2 methods: **Unsupervised** (Filter methods) that looks only at the input and outputs the one with most information and **Supervised methods** (Wrapper methods) that actually uses it on the learning algo and estimates error on validation set.

Strategies
- Use uncorrelated features [eg Age may be directly related to one's weight when we consider children, so we consider only one of those features]
  - Forward Selection: Start from an empty set of features
  - Try each remaining feature
  - Estimate regression/classification error for each feature
  - Select feature which gives best improvement and continue this one by one, until it doesnt improve any more
- Backward Selection:
  - Start with full feature set
  - Try removing features as see how accuracy improves for a particular feature
  - Drop the feature whose removal gives least improvement / impact on error

Feature Selection can be **univariate** (looking at each feature one at a time) or **multivariate**

### Univariate

- Pearson correlation coefficient r \\( -1 < r < +1 \\) r = 0 implies no correlation, r = +1 or -1 implies good correlation
- F-Score
- Chi-Square Test
- Signal to noise ratio: \\( \frac{Difference in means}{Difference in std dev in two classes} \\). Large values = good correlation 
- Mutual Information
- etc

#### We then rank the features

### Multivariate

- Considers all features simultaneously
- Consider \\( \vec w \\) for any linear classifier
- Classifiaction of a point X is given by \\( w^T x + w_0 \\)
- W is basically the weights given to each feature, and the indices can be ranked based on the weights
- In recursive feature elimination, this is used, where features with least w are recursively removed till a reduction in accuracy is observed.
#### Here -ve or +ve val doesnt matter. Only the abs val determine the rank.


