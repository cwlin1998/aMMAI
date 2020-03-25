# PointNet: Deep Learning on Point Sets for 3D Classification and Segmentation

Charles R. Qi	Hao Su	Kaichun Mo	Leonidas J. Guibas



## Introduction

A deep net architecture consuming unordered point sets in 3D and perform 3d shape classification, shape part segmentation and scene semantic parsing tasks.



## Method

### Overall Architecture

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w3/img/pointnet_overall_architecture.png)

#### Symmetry Function for Unordered Input

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w3/img/pointnet_symmetric_function.png)

approximate h by a multi-layer perception(mlp) network and g by a composition of single variable function and a max pooling function

#### Local and Global Information Aggregation

Concatenate the global feature with per point feature in order to satisfy the segmentation problems

#### Joint Alignment Network

constrain the feature transformation matrix to be close to orthogonal matrix:

![pointnet_joint_alignment](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w3/img/pointnet_joint_alignment.png)

where A is the feature alignment matrix predicted by a mini-network(T-net)

### Theoretical Analysis

#### Universal approximation

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w3/img/pointnet_theorem1.png)

#### Bottleneck dimention and stability

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w3/img/pointnet_theorem2.png)



## Experiment

### 3D Object classification

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w3/img/pointnet_experiment_classification.png)

### 3D Object Part Segmentation

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w3/img/pointnet_experiment_segmentation.png)

### Sementic Segmentation in Scences

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w3/img/pointnet_experiment_samentic_segmentation.png)