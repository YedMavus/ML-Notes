---
title: "Week1 Lecture 3: Hypothesis Space and Inductive Bias"
date: 2021-07-15 00:00:00 +0000
katex: true
---
# Week1 Lecture 3: Hypothesis Space and Inductive Bias

## Inductive Learing or Prediction
- Given examples or data of form (x , y) or (x, f(x))
  - **Classification Problems:** f(x) is discrete
  - **Regression Problems**: f(x) is continuous
  - **Probability Estimation:** f(x) is the probability of x

**Why inductive learning**: Given data, use induction, as opposed to deduction, to try and identify a function that predicts the data.

Features: Properties that describe each instance

If multiple features, use feature vector.

### Feature Space

Recall Vector Space

For n features, we define a n fimentional "feature" space, similar to vector spaces. Each instance becomes a point in the feature space.

Take a 2 class classification problem.
We have 2 types of instances.
Training set has subset of instances - some marked class 1{denoted by +1} , others 2{denoted by -1}.

We can map different points in the feature set. We want a function to predict, for a new instance, whether it is a + or - . 
It could be a curve or line that seperates an area in the feature space (2D, so area). This is what inductive learning is. Points to the left of this line is positive, to the right are negative, for example. The line is a hypothesis that we use to do the prediction. 
It needn't be a linear function. It could be a polynomial curve, or even a decision tree. These are just representations. Neural Networks are also another representation.


**Hypothesis space**: Class of functions that can in principle be output by the learning algorithm. It is represented by H. Output of a learning algo produces h ∈ H.
- Supervised learning methods kind of explores the hypothesis space.

The Hypothesis h can be biased, ie restricts the hypothesis using
- Constraints
- Preferences

#### If there are N input features, there are 2<sup>N</sup> possible boolean functions, each of which is iterated by the learner to figure out the best possible approach.
{Derived from simple combinatorics}
  
### Inductive Bias
  
 - Restrictive: Limit on Hypothesis space - specifying the form of the function [eg we state that we only look at linear funtions]
 - Preferencial: Ordering is imposed on Hyp space - eg we specify that we prefer a function of lower degree, even though we consider all possible functions
  
Inductive learning comes up with a general fucntion from the training examples.
  - Constructs hypothesis h to agree on c - the training example
  - h is said to be consistent if it agrees with all training examples [not always possible, or may be more than one]
  - If it works on unseen data as well is said to generalise well.
  
 Inductive learning is also, quite ill posed - wastes resources by looking at mostly wrong hypotheses. 
  
  
  
## Errors

Bias errrors [preference in choosing a hyp thaqt was incorrect] and Varience errors [ wehn we have a small test set, so the model is inconsistent with other training set hypotheses...will be discussed later] These two are basically stating overfitting and under fitting with lot of gargantuan words

# TLDR

<i am too tired>

