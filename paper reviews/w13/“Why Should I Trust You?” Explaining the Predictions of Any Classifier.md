

# “Why Should I Trust You?” Explaining the Predictions of Any Classifier

Marco Tulio Ribeiro	Sameer Singh	Carlos Guestrin



## Introduction

In this work, they propose LIME (Local Interpretable Model-agnostic Explanations), a novel explanation technique that explains the predictions of any classifier in an interpretable and faithful manner, by learning an interpretable model locally around the prediction.



## Why explain

There exist posibilities that a model reaches high accuracy but actually having attention on features that are not strongly realated to, such as algorithm 2 in the following figure.

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w13/img/why_explain.png)



## Desired Characteristics for Explanations

- **Interpretable**
  - provide qualitative understanding between the input variables and the response
- **Local Fidelity**
  - correspond to how the model behaves in the vicinity of the instance being predicted.
- **Model Agnostic**
  - treat the original model as a black box
- **Global Perspective**
  - select a few explanations that represent the model



## LIME (Local Interpretable Model-agnostic Explanations)

- **Interpretable Data Representations**

  - denote x ∈ R<sup>d</sup> be the original representation of an instance being explained, and use x′ ∈ {0, 1}<sup>d′</sup> to denote a binary vector for its interpretable representation

- **Fidelity-Interpretability Trade-off**

  ![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w13/img/equation_lime.png)

  - define an explanation as a model g ∈ G, where G is a class of potentially interpretable models
  - let Ω(g) be a measure of complexity (as opposed to interpretability) of the explanation g ∈ G
  - let the model being explained be denoted f : R<sup>d</sup> → R
  - use π<sub>x</sub>(z) as a proximity measure between an instance z to x, so as to define locality around x
  - let L(f,g,π<sub>x</sub>) be a measure of how unfaithful g is in approximating f in the locality defined by π<sub>x</sub>

- **Sampling for Local Exploration**

  - approximate L(f,g,π<sub>x</sub>) by drawing samples, weighted by π<sub>x</sub>
  - sample instances around x′ by drawing nonzero elements of x′ uniformly at random (where the number of such draws is also uniformly sampled)
  - recover the sample in the original repre- sentation z ∈ R<sup>d</sup> and obtain f(z), which is used as a label for the explanation model

- **Sparse Linear Explanations**

  ![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w13/img/algorithm.png)



## Submodular Pick for Explaning Models

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w13/img/algorithm2.png)

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w13/img/equation_c.png)

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w13/img/sp.png)