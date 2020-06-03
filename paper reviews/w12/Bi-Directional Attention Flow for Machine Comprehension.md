# Bi-Directional Attention Flow for Machine Comprehension

Minjoon Seo	Aniruddha Kembhavi	Ali Farhadi	Hananneh Hajishirzi



## Introduction

This paper offers improvements on attention via three parts:

1. The attention layer is not used to summarize the context paragraph into a fixed-size vector but computed for every time step, and the attended vector at each time step, along with the representations from previous layers, is allowed to *flow* through to the subsequent modeling layer.

   This reduces the information loss caused by early summarization.

2. Using a memory-*less* attention mechanism. That is, while we iteratively compute attention through time, the attention at each time step is a function of only the query and the context paragraph at the current time step and does not directly depend on the attention at the previous time step. 

   It forces the attention layer to focus on learning the attention between the query and the context, and enables the modeling layer to focus on learning the interaction within the query-aware context representation (the output of the attention layer). It also allows the attention at each time step to be unaffected from incorrect attendances at previous time steps.

3. Using attention mechanisms in both directions, query-to-context and context-to-query, which provide complimentary information to each other.



## Model Architecture

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w12/img/model.png)

### Character Embedding Layer

maps each word to a vector space using character-level CNNs

### Word Embedding Layer

maps each word to a vector space using a pre-trained word embedding model

### Contextual Embedding Layer

utilizes contextual cues from surrounding words to refine the embedding of the word by Bi-LSTM network

### Attention Flow Layer

C2Q and Q2C Attention

### Context-to-query Attention

 employs a Recurrent Neural Network to scan the context

### Query-to-context Attention

provides an answer to the query



## Experiment

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w12/img/experiment1.png)

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w12/img/experiment2.png)