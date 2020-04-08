# A Survey on Learning to Hash

Jingdong Wang	Ting Zhang	Jingkuan Song	Nicu Sebe	Heng Tao Shen



## Introduction

There are two categories of hashing algorithm: Locality Sensitie Hashing(data-independent) and Learning to Hash(data-dependent). 

This survey categories the algorithm according to the simalarity preserving manner into:

1. pairwise similarity preserving
2. multiwise similarity preserving
3. implicit similarity preserving
4. quantization (a form of pairwise similarity preserving, as well as an end-to-end hash learning strategy)

This paper focuses more on lerninng to hash and discusses more on quantization-based solutions.



## Methods

![table](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w5/img/table.png)

#### Pairwise Similarity Preserving

- Similarity-distance product minimization (SDPM) 
  - Spectral hashing
  - ICA hashing
  - Linear discriminant analysis (LDA) hashing
- Similarity-similarity product maximization (SSPM)
  - Semi-supervised hashing
- Distance-distance product maximization (DDPM)
  - Topology preserving hashing
- Distance-similarity product minimization (DSPM) 
- Distance-distance difference minimization (DDDM) 
  - Binary reconstructive embedding
- Similarity-similarity difference minimization (SSDM)
  - Supervised hashing with kernels
  - Kernel reconstructive hashing
  - Scalable graph hashing
  - Binary hashing
- Normalized similarity-similarity divergence minimization (NSSDM) 
  - Spec hashing

#### Multiwise Similarity Preserving

- Order preserving hashing
- Triplet loss hashing
- Listwise supervision hashing

#### Implicit Similarity Preserving

- Random maximum margin hashing
- Complementary projection hashing
- Spherical hashing

#### Quantization

- Hypercubic Quantization
  - Iterative quantization
  - Harmonious hashing
  - Isotropic hashing
- Cartesian Quantization
  - Product Quantization
  - Cartesian k-means
  - Composite Quantization