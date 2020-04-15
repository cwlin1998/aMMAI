# Graph Embedding and Extensions: A General Framework for Dimensionality Reduction

Shuicheng Yan	Dong Xu	Benyu Zhang	Hong-Jiang Zhang	Qiang Yang	Stephen Lin



## Introduction

- Presents graph embedding, along with its linearization, kernelization, and tensorization, to offer a unified view for understanding and explaining many of the popular dimensionality reduction algorithms.
- Develop Marginal Fisher Analysis (MFA) to overcome limitations of LDA.



## Method

### Graph Embedding

(Mapping Function) F : x → y, x ∈ IR<sup>m</sup>, y ∈ IR<sup>m'</sup>, m >> m'

(Dataset) X = [x<sub>1</sub>, x<sub>2</sub>, ... , x<sub>N</sub>], x<sub>i</sub> ∈ IR<sup>m</sup>

(Weighted Graph) G = {X, W}, W ∈ IR<sup>NxN</sup>

The diagonal matrix D and the Laplacian matrix L of a graph G are defined as L = D - W, D<sub>ii</sub> = ∑<sub>j≠1</sub> W<sub>ij</sub>, ∀i

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w6/img/graph_embedding.gif)

#### General Framework for Dimentionality Reduction

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w6/img/graph_embedding_general.gif)

### Marginal Fisher Analysis (MFA)

1. PCA projection

   - project the data set into the PCA subspace by retaining N−N<sub>c</sub> dimensions or a certain energy

2. Constructing the intraclass compactness and interclass separability graphs

   - In the intraclass compactness graph, for each sample x<sub>i</sub>, set the adjacency matrix W<sub>ij</sub>=W<sub>ji</sub>=1 if x<sub>i</sub> is among the k<sub>1</sub>-nearest neighbors of x<sub>j</sub> in the same class. In the interclass separability graph, for each class c, set the similarity matrix W<sub>ij</sub><sup>p</sup> =1 if the pair (i,j) is among the k<sub>2</sub> shortest pairs among the set { (i,j), i∈π<sub>c</sub>, j∉π<sub>c</sub> }

3. Marginal Fisher Criterion

   - From the linearization of the graph embedding framework, we have the Marginal Fisher Criterion

   ![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w6/img/marginal_fisher_criterion.png)

4. Output the final linear projection direction

   ![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w6/img/output.png)



## Experiment

Table: Face Recognition Accuracies of PCA, Fisherface, LPP, MFA, Bayesian Face, PCA + LDA, MFA + LDA, KDA and KMFA, DATER, and TMFA on the PIE-1 Subdatabase

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w6/img/experiment.gif)