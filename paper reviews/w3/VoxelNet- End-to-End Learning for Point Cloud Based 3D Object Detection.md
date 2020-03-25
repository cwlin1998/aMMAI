# VoxelNet: End-to-End Learning for Point Cloud Based 3D Object Detection

Yin Zhou	Oncel Tuzel



## Introduction

VoxelNet is a generic 3D detection framework that simultaneously learns a dicriminative feature representation from point clouds and predicts accurate 3D bounding boxes, in an end-to-end fashion.

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w3/img/voxelnet_intro.png)

## Method

### Overall Architecture

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w3/img/voxelnet_overall_arcitecture.png)

#### Feature Learning Network

1. Voxel Partition

   subdivide the 3D space into equally spaced voxels

2. Grouping

   group the points according to the voxel they reside in

3. Random Sampling

   random sample a fixed number , T, of points from those voxels containing more than T points

4. Stacked Voxel Feature Encoding

   ![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w3/img/voxelnet_voxel_feature_encoding_layer.png)

5. Sparse Tensor Representation

   represent non-empty voxel features as a sparse tensor

#### Convolutional Middle Layers

Converts voxel feature to feature maps, using three Conv+BN+ReLU blocks

#### Region Proposal Network (RPN)

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w3/img/voxelnet_rpn.png)

### Loss Function

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w3/img/voxelnet_loss.png)

## Experiment

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w3/img/voxelnet_experiment.png)