# Week 1

## 1. RNN

### a. Introduction

Examples of sequence data

<p align="center">
  <img src="../res/img/img1.png" width="600"/>
</p>

### b. Notations

T指的是input text（字符串）的长度

<p align="center">
  <img src="../res/img/img2.png" width="600"/>
</p>

根据词典对input进行one-hot编码，然后让模型去output一个y

<p align="center">
  <img src="../res/img/img3.png" width="600"/>
</p>

### c. Structure

<p align="center">
  <img src="../res/img/img4.png" width="600"/>
</p>

#### i. Forward Propagation

<p align="center">
  <img src="../res/img/img5.png" width="500"/>
  <img src="../res/img/img6.png" width="500"/>
</p>

#### ii. Backward Propagtion

<p align="center">
  <img src="../res/img/img7.png" width="600"/>
</p>

### d. Different Types of RNN

+ One-one
+ Many-many
+ Many-one
+ One-many

<p align="center">
  <img src="../res/img/img8.png" width="500"/>
  <img src="../res/img/img9.png" width="500"/>
</p>

Summary

<p align="center">
  <img src="../res/img/img10.png" width="600"/>
</p>

### e. What Is Language Modeling?

<p align="center">
  <img src="../res/img/img11.png" width="600"/>
</p>

EOS and UNK

<p align="center">
  <img src="../res/img/img12.png" width="600"/>
</p>

output就是根据dict给出下个可能的单词的probability

<p align="center">
  <img src="../res/img/img13.png" width="600"/>
</p>

### f. Sampling Novel Sequences

<p align="center">
  <img src="../res/img/img14.png" width="600"/>
</p>

Character-level language model

<p align="center">
  <img src="../res/img/img15.png" width="600"/>
</p>

### g. Vanishing Gradients with RNNs

Vanishing gradients with RNNs：output会被附近的output所影响，比如y3会被y2和y4影响，但是远距离的output很难被影响，比如last y很难被y1影响

<p align="center">
  <img src="../res/img/img16.png" width="600"/>
</p>

### h. Gated Recurrent Unit (GRU)

RNN unit

<p align="center">
  <img src="../res/img/img17.png" width="600"/>
</p>

GRU simplified

<p align="center">
  <img src="../res/img/img18.png" width="600"/>
</p>

Full GRU

<p align="center">
  <img src="../res/img/img19.png" width="600"/>
</p>

### i. LSTM

<p align="center">
  <img src="../res/img/img20.png" width="600"/>
</p>

Picture

<p align="center">
  <img src="../res/img/img21.png" width="600"/>
</p>

### j. Bidirectional RNN

Blocks can still be GRU/LSTM block

<p align="center">
  <img src="../res/img/img22.png" width="600"/>
</p>

### k. Deep RNN

<p align="center">
  <img src="../res/img/img23.png" width="600"/>
</p>
