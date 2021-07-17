---
title: "Week 1 Lecture 2: Different Types of Learning"
date: 2021-07-14 00:00:00 +0000
katex: true
---
# Week 1 Lecture 2: Different Types of Learning
* Supervised Learning
  - Has (X, Y) given as data, where X was input, Y was output, and model tries to find out Y for a new X and compare with the given Y
  - Give a label to X (ie find Y)
- UnSupervised Learning
  - Only X is given  
  - Given X, Cluster or Summarise them, ie organise them into meaningful groups
- Reinforcement Learning
  - Given an "agent" Determine what to do based on rewards and punishments
  - Agent takes an action which impacts the enviornment, based on which it is rewarded ( rewards can  be [-1, 0, 1])
  - The agent tries to optimise longterm rewards
- SemiSupervised Learning //Not defined in Andrew Ng's course, who put it in supervised learning only
  - Combo
  - Given labelled training data, and a even larger unlabelled data, come up with algo to process the unlabelled data
  - Most common for now

## Supervised Learning
We have a set of input features given X<sub>1</sub>, X<sub>2</sub>, ... , X<sub>n</sub>, with respect to which the instances are described. We also have a target feature Y.
  
  | S.No | \\( X_1, X_2, ... , X_n \\) | Y |
  | -- |------------------------------------------- | -- |
  | 1. | \\( A_1, A_2, ... , A_n \\) | \\( Y_1\\) |
  | 2. | \\( B_1, B_2, ... , B_n \\) | \\( Y_2\\) |
  | . | . | . |
  | . | . |.|
  | . | . |.|
  | . | . |.|
  
  So the values of Y<sub>i</sub> are given. Along with this a test instance is given, containing only X<sub>i</sub>.
  
  * If Y is discrete valued, [eg Will it rain, or not rain] it is known as **Classification**.
  * If Y is continious valued, [eg Given a location, predict price of house per sq inches], it is known as **Regression**.
    * Most common example - linear regression

### Features

Individual observations are analysed into a set of **quantifiable** properties which are called features
eg Type of blood group, or Ordinal [small, medium or large] etc
#### To Summarise **Supervised Learning**

| | Traning Set | |
|--|-------------|--|
| | Learning Algo | |
| **X** | Hypothesis | Predicted Y |

## Classification Learning

- Task T is given
  - Input: Set of Instances  \\( d_1, d_2, ... , d_n \\)
    * Each instance  has a set of features
    * So d can be represented as a vector **d** = < \\( X_1, X_2, ... , X_n \\)>
  - Output: A set of predictions as one of a fixed set of constant values 
- Performance Metric P 
  - Probability of a prediction being wrong
- Experience E
  - It is the data, ie a given set of correctly labelled examples (X,Y), ```coming from a fixed distribution``` (ideally)


## TLDR

* **Features:** Distinct traits that is used to describe a particular instance quantitatively
* **Feature Vector:** n - dimentional vector of   numerical features
* **Instance space X:** Set of all possible objects describeable by features
* **Example (x, y):** Instance x with label f(x) = y
* **Concept c:** Subset of objects from X [eg given a group of images, those images that are of a bicycle are under a concept c that contains images of bicycles]
* **Target Function:** Maps each instance x ε X to target label y ε Y
* **Training Data:** Collection of examples observed by learning algorithm, used to potentially predict relationships [in the Computer Science sense ;) ]

