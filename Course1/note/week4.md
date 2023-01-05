# Week 4

## 1. Deep L-layer Neural Network

### a. Matrix dimensions

+ Z[l]: (n[l], 1)
+ W[l]: (n[l], n[l-1])
+ b[l]: (n[l], 1)
+ dW[l]: W[l]
+ db[l]: b[l]

<p align="center">
  <img src="../res/img/img34.png" width="500"/>
  <img src="../res/img/img35.png" width="500"/>
</p>

### b. Why depp representations

<p align="center">
  <img src="../res/img/img36.png" width="600"/>
</p>

### c. Blocks of deep neurak networks

<p align="center">
  <img src="../res/img/img37.png" width="600"/>
</p>

### d. Forward and backward propagation

#### i. Forward propagation

<p align="center">
  <img src="../res/img/img38.png" width="600"/>
</p>

#### ii. Backward propagation

<p align="center">
  <img src="../res/img/img39.png" width="600"/>
</p>

#### iii. Summary

<p align="center">
  <img src="../res/img/img40.png" width="600"/>
</p>

## 2. Parameters vs Hyperparameters

Hpyerparamters用于control parameters（Hpyerparamters determine parameters）

+ Parameters: W[1], b[1], W[2], b[2], W[3], b[3], ...
+ Hyperparameters
    + Learning rate: alpha
    + Number of iterations
    + Number of hidden layers: L
    + Number of hidden units: n[1], n[2], n[3], ...
    + Choice of activation function