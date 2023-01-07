# Week 1

## 1. Setting up

### a. Train/Dev/Test sets

<p align="center">
  <img src="../res/img/img1.png" width="600"/>
</p>

### b. Bias/Variance

+ Overfitting: high variance
+ Underfitting: high bias
+ Bias可以看作对training set的描述，bias越低模型越fit数据；Variance可以看作对Dev/test sets的描述，variance越低模型越fit dev/test sets

<p align="center">
  <img src="../res/img/img2.png" width="500"/>
  <img src="../res/img/img3.png" width="500"/>
</p>

### c. Basic Recipe for Machine Learning

+ Bias可以通过改进模型（bigger network）；Variance可以通过增多数据（more data）来改变

<p align="center">
  <img src="../res/img/img4.png" width="600"/>
</p>

## 2. Regularization

### a. Introduction

#### i. Logistic regression

通常使用L2 regularization

<p align="center">
  <img src="../res/img/img5.png" width="600"/>
</p>

#### ii. Neural network 

Frobenius norm：panel

<p align="center">
  <img src="../res/img/img6.png" width="600"/>
</p>

### b. Dropout Regularization

Dropout：每个node会有一定几率drop掉

<p align="center">
  <img src="../res/img/img7.png" width="600"/>
</p>

Intuition：分散权重（每层拥有不同权重）
缺点：cost function J is not always well defined (hard to calculate) -> 先关闭drop-out，观察gradient descent是否正常工作，然后再重新训练

<p align="center">
  <img src="../res/img/img8.png" width="600"/>
</p>

### c. Other Regularization Methods

#### i. Data augmentation

<p align="center">
  <img src="../res/img/img9.png" width="600"/>
</p>

#### ii. Early stopping

在evaluation的图中，绘制training error和dev error；然后stop half way -> 普遍意义上不如L2 regularization

<p align="center">
  <img src="../res/img/img10.png" width="600"/>
</p>

## 2. Optimization Problems

### a. Normalizing Inputs

+ Normal training and test sets together
+ normalization可以让gradient descent过程快一些

<p align="center">
  <img src="../res/img/img11.png" width="500"/>
  <img src="../res/img/img12.png" width="500"/>
</p>

### b. Vanishing / Exploding Gradients

梯度爆炸：权重太大/初始值（大于一）有关

<p align="center">
  <img src="../res/img/img13.png" width="600"/>
</p>

### c. Weight Initialization for Deep Networks

<p align="center">
  <img src="../res/img/img14.png" width="600"/>
</p>

### d. Gradient Checking

#### i. Numerical approximation of gradients

<p align="center">
  <img src="../res/img/img15.png" width="600"/>
</p>

#### ii. Gradient check

1. Take W[1], b[1], ... , W[L], b[L] and reshape into a big vector theta.
    + J(W[1], b[1], ... , W[L], b[L]) -> J(theta)
2. Take dW[1], db[1], ... , dW[L], db[L] and reshape into a big vector dtheta.

<p align="center">
  <img src="../res/img/img16.png" width="600"/>
</p>

#### iii. Notes

<p align="center">
  <img src="../res/img/img17.png" width="600"/>
</p>