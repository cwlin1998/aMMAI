# ArcFace: Additive Angular Margin Loss for Deep Face Recognition

Jiankang Deng, Jia Guo, Niannan Xue, Stefanos Zafeiriou

Imperial College London, InsightFace, FaceSoft



## Introduction

This paper introduces a new loss function, Additive Angular Margin Loss (ArcFace), to learn highly discriminative features for face recognition. The advantages of ArcFace can be summarized as follows:

- **Engaging.** Directly optimises the geodesic distance margin.
- **Effective.** Achieves state-of-the-art performance.
- **Easy.** Extremely easy to implement.
- **Efficient.** Only adds negliable computational complexity during training.



## ArcFace

1. Softmax

   ![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w2/L1.png)

2. Weight normalization

   ![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w2/L2.png)

3. Add additive angular margin penalty

   ![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w2/L3.png)

### Algorithm

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w2/Algo.png)



## Experiment

**Verification performance (%) for different loss functions**

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w2/verification_results_loss.png)

**Verification performance (%) for different method on LFW and YTF**

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w2/verification_results_method.png)

**Face identification and verification evaluation of different methods on MegaFace Challenge1**

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w2/MegaFace_challenge.png)