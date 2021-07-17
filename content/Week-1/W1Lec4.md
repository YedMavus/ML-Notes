---
title: "Week 1 Lecture 4: Evaluation and Cross Validation"
date: 2021-07-16 00:00:00 +0000
katex: true
---
# Week 1 Lecture 4: Evaluation and Cross Validation

Given a hypothesis space H and training data S, the learning algo comes up with a function h. To understand how good the h is, we need to evaluate it using experimental evaluation, ie having a metric using which we evaluate, eg 
- error metric
- accuracy
- precision and recall

These evaluations are done on the training set or even better a seperate test set.

Given y' = h(x) is a prediction on x and y is the actual value. If y' differs from y, we have an error.

#### Types of errors:
- Absoloute error: 1/n &sum;{|h(x) - y|}
- Sum of Square Method: 1/n &sum;(h(x) - y)<sup>2</sup>
- Classification error: 1/n &sum; &delta; (h(x),y)

In classification, we define a confusion matrix

| Hyp Class\True Class | Positive | Negative |
| -- | -- | -- |
| Positive | True Positive[TP] | False Positive[FP] |
| Negative | False Negative[FN] | True Negative[TN] |
| | &sum; = P | &sum; = N |


Obviously the diagonal elements are either all true or all false

#### Accuracy = (TP + TN) / (P + N)

\\How many are correctly predicted

#### Precision = TP/ (TP + FP)

\\Answers how many are correctly positive

#### Recall = TP / P


How many of the positive examples are retrieved as positive, also called true positive rate. False positive rate also exists.

Error Got on Sample is called **sample error**. The actual error is called the **true error**.

We split the example dataset, using a part for training the learner, and a disjoint dataset for testing the learner. 

If testset is small, the varience increases.

#### How to test with limited data

- Divide the examples into training set and test sets. 
  - The size of training set incerases, then overfitting occurs, so we prefer to give max of the data for training.
- During traning, a small part of the training data can be used as validation set, if training is sort of ok. The validation set is used to do minor tweaks, so to say.

### K - Fold cross validation

1. Split Data into K Equal subsets
2. Perform K Rounds of learning. On each round
  - 1/k of the data is held out as test set
  - Remaining examples used as training data 
3. Compute average test set score of K Rounds 

Final accuracy is given by average of each of these K Subsets

## Trade off [TLDR]

- Always a tradeoff between complex hyp that fits training data well
- Simpler hypothesis that generalise better
  - As data amount increases, generalisation error increases
