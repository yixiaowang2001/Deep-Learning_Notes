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