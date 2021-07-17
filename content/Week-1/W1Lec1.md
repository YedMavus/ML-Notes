---
title: "Introduction"
date: 2021-07-13 00:00:00 +0000
katex: true
---
# Introduction
Definition of **Learning**: The ability to improve behaviour or a prediction based on experience.

  Building comp sys that improve with experience
  
### Machine Learning 
- Explores algorithms
    - learn from data and build models from data
    - Models can be used for some tasks, eg prediction, decision making or solving
    - 
  Formal definition of ML _(Mitchell)_: A computer program **(machine)** is said to **learn** from experience E, with respect to some class of tasks T, and performance measure P, if its performance on task T as measured by P improves with experience E.
### Components of a Learning Algo
  - Tasks T <sub>i</sub>
    - Prediction
    - Classification
    - Acting in an environment
    - et cetera
  - Experience E, also called Data
  - Measure of improvement or P
 ### Components of an ML Model
A ML model consists of a **learner** and a **reasoner**
- Learner
  - Takes up Experience Data and backgreound knowledge, and creates one or more predictive model(s) and provides it to the reasoner
- Reasoner
  - Takes up the task, applies the model it was provided to by the Learner to give a result/answer/performance

## Learner
1. Choose the **traning Experience** or Data
2. Choose the target function [how to represent the model] that needs to be learned
3. Choose the class of Function [**How to reperesent the target func**] or the hypothesis language
4. Choose a learning algorithm to infer the target function

[Note to 2: Richer a representation is, tougher to learn the model]
