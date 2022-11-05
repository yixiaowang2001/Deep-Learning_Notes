# Week 3

## 1. Neural Networks Overview

<p align="center">
  <img src="../res/img/img25.png" width="600"/>
</p>

## 2. Neural Network Representation

### a. Notation

<p align="center">
  <img src="../res/img/img26.png" width="500"/>
  <img src="../res/img/img27.png" width="500"/>
</p>

### b. Matrix transform

+ 对于每一层，z与b的shape一致
+ 对于每一层，w.shape[0] = b.shape[0]，x.shape[1] = b.shape[1]
+ 对于第n层和n+1层，b_n.shape[0] = b_n1.shape[0]

<p align="center">
  <img src="../res/img/img28.png" width="600"/>
</p>

## 3. Vectorizing Across Multiple Examples

<p align="center">
  <img src="../res/img/img29.png" width="600"/>
</p>

## 4. Activation Functions

### a. Activation functions
+ 不管是对于Sigmoid还是tanh function，当z很小或是很大的时候，斜率都会很低，某些程度上降低了gradient descent的速度。
+ 神经网络中每一层的Activation function都可以不一样，通常来说，隐藏层会选择Relu function。
+ 对于Relu来说，当z是负的时候，a = 0。
+ Leaky ReLU是一种变体，当z是负的时候，a不为0.

<p align="center">
  <img src="../res/img/img30.png" width="600"/>
</p>

### b. Why we need a non-linear activation function?

+ 如果没有activation function或者activation function是linear的，那么y hat的结果只会是input的一个linear的结果。
+ 线性激活函数通常都出现在输出层，隐藏层很少出现

<p align="center">
  <img src="../res/img/img31.png" width="600"/>
</p>

## 5. Derivatives of Activation Functions
