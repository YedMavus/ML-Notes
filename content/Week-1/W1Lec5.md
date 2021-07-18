---
title: "Week 1 Lecture 5: Tutorial 1"
date: 2021-07-16 18:00:00 +0000
katex: true
---
# Week 1 Lecture 5: Tutorial 1
## Agenda
* Supervised vs Unsupervised Learning
* Different types of Features: Categorical vs Contiious Features
* Supervised Learning
  * Regression vs Classification
* Bias vs Varience  
* Generalisation Performance of A Learning Algorithm


## Supervised vs Unsupervised Learning
Basic algorithms to follow
Suppose we have a huge number of images (1 Million, say)
1. Clustering Done -> Get a broad idea about what are the different kinds of images
2. Classifier is run for each of these clusters to discover intricacies in this data 


So step 1 is unsupervised, while step 2 may be supervised or unsupervised.

## Categorical vs Continious

### Categorical
Finite number of Values, or indicating presence and absence of something

//Imp for exam purpose these categories

### Continious

Can theoretically take infinie number of values, eg Height, weight, price, etc

## Types of Supervised Learning Algo

##### Dependent on type of output variable
(Check if its discrete or continious)

- Regression
 - Given certain features of car, predict price of car
- Classification
 - Is it categorical or discrete?
 - examples 
  - given images of animals predict species of animal
  - given CT Scans, predict malignant tumor

## Bias vs Variance

#### Bias
- Set of erroneous **assumptions** in the learning algorithm
- This is only due to the learning algo, and not the training examples

#### Variance

- Due to sensitivity of learning towards noise as opposed to the features and relationship of input/output
- Happens if too many features are being considered
- Happens if too less training data
|  | Number of Features | Number of Parameters | Number of Training Examples |
| ---- | ---- | ---- | ---- |
| **Bias** | Decreases | Decreases | Remains the same |
| **Variance** | Increases | Increases | Decreases |
<incomplete>
