# Model Compression and Acceleration for Deep Neural Networks: The Principles, Progress, and Challenges

Yu Cheng	Duo Wang	Pan Zhou	Tao Zhang



## Introduction

This paper surveys different appraoches for model compression and acceleration, which can mainly  be classified into four categories:

1. Parameter pruning and sharing
2. Low-rank factorization
3. Transferred/compact convolutional filters
4. Knowledge distillation (KD)

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w11/img/summary.png)



## Methodology

### Parameter pruning and sharing

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w11/img/pruning.png)

#### Quantization and binarization

Drawback:

- The accuracy of such binary nets is significantly lowered when dealing with large CNNs such as GoogleNet.
- These binary nets is that existing binarization schemes are based on simple matrix approximations and ignore the effect of binarization on the accuracy loss.

#### Pruning and Sharing

Drawback:

- Pruning with L1 or L2 regularization requires more iterations to converge.
- All pruning criteria require manual setup of sensitivity for layers, which demands fine-tuning of the parameters and could be cumbersome for some applications.

#### Designing the strctural matrix

Drawback:

- The structural constraint will cause loss in accuracy since the constraint might bring bias to the model.
- How to find a proper structural matrix is difficult since there is no theoretical way from which to derive it.



### Low-rank factorization and sparsity

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w11/img/low-rank.png)

Drawback: 

- The implementation is not that easy since it involves a decomposition operation, which is computationally expensive.
- Current methods perform low-rank approximation layer by layer, and thus cannot perform global parameter compression, which is important as different layers hold different information.
- Factorization requires extensive model retraining to achieve convergence when compared to the original model.



### Transferred/compact convolutional filters

Drawback:

- These methods can achieve competitive performance for wide/flat architectures (like VGGNet) but not narrow/special ones (like GoogleNet and ResNet).
- The transfer assumptions sometimes are too strong to guide the algorithm, making the results unstable on some data sets.



### KD

Drawback:

- Can only be applied to classification tasks with softmax loss function, which hinders its usage.
- The model assumptions sometimes are too strict to make the performance competitive with other types of approaches.