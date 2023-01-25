# Week 4

## 1. Face Recognition

### a. Introduction

<p align="center">
  <img src="../res/img/img77.png" width="600"/>
</p>

### b. One-shot Learning

单样本学习问题 -> 对于每个人脸，深度学习然后output是不现实的 -> 所以选择比较两张脸是否相似 -> Learning a similarity function

<p align="center">
  <img src="../res/img/img78.png" width="600"/>
</p>

### c. Siamese Network

<p align="center">
  <img src="../res/img/img79.png" width="500"/>
  <img src="../res/img/img80.png" width="500"/>
</p>

### c. Triplet Loss

Objective

<p align="center">
  <img src="../res/img/img81.png" width="600"/>
</p>

Loss function

<p align="center">
  <img src="../res/img/img82.png" width="500"/>
  <img src="../res/img/img83.png" width="500"/>
</p>

### d. Binary Classification

Using different pairs to train a nerual network -> Same, y = 1; different, y = 0

<p align="center">
  <img src="../res/img/img84.png" width="600"/>
</p>

## 2. Neural Style Transfer

### a. Visualization of CNN

图片detect的物体是在逐渐变复杂的：从pattern到真正的物体

<p align="center">
  <img src="../res/img/img85.png" width="500"/>
  <img src="../res/img/img86.png" width="500"/>
</p>

### b. Cost Function

#### i. Procedure

<p align="center">
  <img src="../res/img/img87.png" width="500"/>
  <img src="../res/img/img88.png" width="500"/>
</p>

#### ii. Content Cost Function

<p align="center">
  <img src="../res/img/img89.png" width="600"/>
</p>

#### ii. Style Cost Function

<p align="center">
  <img src="../res/img/img90.png" width="500"/>
  <img src="../res/img/img91.png" width="500"/>
</p>

### c. Generalization for 1D and 3D

+ 1D & 3D examples
+ 3D可以是医学影像，也可以是电影（连续画面处理为3D）

<p align="center">
  <img src="../res/img/img92.png" width="500"/>
  <img src="../res/img/img93.png" width="500"/>
</p>