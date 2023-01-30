# Week 2

## 1. Word Embeddings

### a. Introduction

1-hot representation

<p align="center">
  <img src="../res/img/img24.png" width="600"/>
</p>

Featurized representation：找到Man、Woman、King等和Gender、Royal等的关系，如果关系密切那么绝对值就是1（三维空间中的距离 t-SNE）

<p align="center">
  <img src="../res/img/img25.png" width="600"/>
</p>

Visualization

<p align="center">
  <img src="../res/img/img26.png" width="600"/>
</p>

### b. Using Word Embeddings

Example

<p align="center">
  <img src="../res/img/img27.png" width="600"/>
</p>

Transfer learning and word embedding

<p align="center">
  <img src="../res/img/img28.png" width="600"/>
</p>

### c. Properties of Word Embeddings

Analogies：Man -> Woman; King -> ? (Queen)，通过Vector相减会发现最后剩下的就是Gender的差别

<p align="center">
  <img src="../res/img/img29.png" width="500"/>
  <img src="../res/img/img30.png" width="500"/>
</p>

Similarity functions: Cosine similarity

<p align="center">
  <img src="../res/img/img31.png" width="600"/>
</p>

### d. Embedding Matrix

<p align="center">
  <img src="../res/img/img32.png" width="600"/>
</p>

## 2. WOrd2vec & GloVe

### a. Learning Word Embeddings

#### i. Neural language model

<p align="center">
  <img src="../res/img/img33.png" width="600"/>
</p>

#### ii. Other context/target pairs

自己定义context
+ context可以是target word左右两边四个单词（Word embedding）
+ 最后四个单词（Language model）
+ 最后一个单词（Word embedding）
+ 最近的一个单词（Word embedding）

<p align="center">
  <img src="../res/img/img34.png" width="600"/>
</p>

### b. Word2Vec

#### i. Model

<p align="center">
  <img src="../res/img/img35.png" width="600"/>
</p>

#### ii. Problems with softmax classification

<p align="center">
  <img src="../res/img/img36.png" width="600"/>
</p>

### c. Negative Sampling

#### i. Defining a new learning problem

负抽样：有一个正面的例子，橘子和果汁，然后故意生成一堆负样本，因此得名负抽样，用它来训练四个以上的二进制分类器

<p align="center">
  <img src="../res/img/img37.png" width="500"/>
  <img src="../res/img/img38.png" width="500"/>
</p>

#### ii. Select sampling

<p align="center">
  <img src="../res/img/img39.png" width="600"/>
</p>

### d. GloVe Word Vectors

#### i. Notation

<p align="center">
  <img src="../res/img/img40.png" width="600"/>
</p>

#### ii. Model

<p align="center">
  <img src="../res/img/img41.png" width="600"/>
</p>

Note:

<p align="center">
  <img src="../res/img/img42.png" width="600"/>
</p>

## 3. Applications Using Word Embeddings

### a. Sentiment Classification

Then, many-to-one RNN

<p align="center">
  <img src="../res/img/img43.png" width="500"/>
  <img src="../res/img/img44.png" width="500"/>
</p>

### b. Debiasing Word Embeddings

Bias problem

<p align="center">
  <img src="../res/img/img45.png" width="600"/>
</p>

Addressing bias in word embeddings