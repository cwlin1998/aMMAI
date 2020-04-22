# Robust Sparse Coding for Face Recognition

Meng Yang	Lei Zhang	Jian Yang	David Zhang



## Introduction

This paper proposed a model named robust sparse coding, which improved the robustness and effectiveness of sparse representation. The proposed RSC scheme utilizes the MLE (maximum likelihood estimation) principle to robustly regress the given signal with sparse regression coefficients, transforming the minimization problem into an iteratively reweighted sparse coding problem. 



## Method

### RSC model

With consideration of the sparsity constraint of $\alpha$, the MLE of $\alpha$, namely the RSC, can be formulated as the following minimization

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w7/img/minimization.png)

### The distribution induced weights

The RSC model above can be approximated by

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w7/img/weighted_minimization.png)

,where 

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w7/img/weight.png)

### Algorithm

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w7/img/algorithm.png)



## Experiment

### Face recognition without occlusion

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w7/img/FR_without_occlusion.png)

### Face recognition with occlusion

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w7/img/FR_with_occlusion.png)