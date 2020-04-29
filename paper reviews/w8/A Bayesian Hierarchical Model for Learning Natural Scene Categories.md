# A Bayesian Hierarchical Model for Learning Natural Scene Categories

Li Fei-Fei	Pietro Perona



## Introduction

Main contributions:

1. leaning relevant intermediate representations of scenes automatically and without supervision
2. probabilistic framework for learning models of textures via codewords (or textons)
3. be able to group categories of images into a sensible hierarchy, similar to humans would do



## Method

### Algorithm

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w8/img/algorithm_flow_chart.png)

### Model Structure

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w8/img/model_structure.png)

#### Theme Models

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w8/img/theme_model.png)

Choosing words by repeating following four steps:

1. Choose a distribution of topics from distributions of topics
2. Choose a topic from the distribution
3. Choose one of the distributions of words from the topic
4. Choose a word from the distribution of words



#### Bayesian Decision

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w8/img/bayesian_decision1.png)

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w8/img/bayesian_decision2.png)

####  Learning: Variational Inference

**log likelihood:**

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w8/img/log_likelihood.png)

**EM algorithm:**

E step:

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w8/img/e_step.png)

M step:

Maximize the reuslting lower bound on the log likelihood with respect to the model parameters θ and β



## Experiment

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w8/img/confusion_matrix.png)

Confusion table of Theme Model 1 using 100 training and 50 test examples from each category.

The average performance is 64.0%.

