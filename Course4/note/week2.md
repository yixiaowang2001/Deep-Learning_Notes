# Week 2

## 1. Case Studies

### a. Classic networks

+ LeNet-5
+ AlexNet
+ VGG

#### i. LeNet-5

<p align="center">
  <img src="../res/img/img18.png" width="600"/>
</p>

#### ii. AlexNet

<p align="center">
  <img src="../res/img/img19.png" width="600"/>
</p>

#### iii. VGG-16

<p align="center">
  <img src="../res/img/img20.png" width="600"/>
</p>

### b. ResNets

#### i. Residual block

<p align="center">
  <img src="../res/img/img21.png" width="600"/>
</p>

#### ii.Residual Network

"plain network"

<p align="center">
  <img src="../res/img/img22.png" width="600"/>
</p>

#### iii. Why ResNets work

Identity function is easy for Residual block to learn -> will not hurt the performance 

<p align="center">
  <img src="../res/img/img23.png" width="600"/>
</p>

#### iv. Image

<p align="center">
  <img src="../res/img/img24.png" width="600"/>
</p>

### c. 1X1 Convolutions

Network in network

<p align="center">
  <img src="../res/img/img25.png" width="600"/>
</p>

Shrink networks

<p align="center">
  <img src="../res/img/img26.png" width="600"/>
</p>

### d. Inception Network

#### i. Motivation

<p align="center">
  <img src="../res/img/img27.png" width="600"/>
</p>

+ The problem of computational cost
+ Different structure: using 1X1 convolution -> bottleneck layer

<p align="center">
  <img src="../res/img/img28.png" width="500"/>
  <img src="../res/img/img29.png" width="500"/>
</p>

#### ii. Inception Network

<p align="center">
  <img src="../res/img/img30.png" width="500"/>
  <img src="../res/img/img31.png" width="500"/>
</p>

Paper还cite了inception

<p align="center">
  <img src="../res/img/img32.png" width="600"/>
</p>

### e. MobileNets

#### i. Motivation

Designed for low compute environment

<p align="center">
  <img src="../res/img/img33.png" width="600"/>
</p>

#### ii. Comparison

Normal Conv

<p align="center">
  <img src="../res/img/img34.png" width="600"/>
</p>

Depthwise Separable Conv

+ filter每层对应每层：红对红，绿对绿，蓝对蓝
+ 最终得到一个intermediate value

<p align="center">
  <img src="../res/img/img35.png" width="600"/>
</p>

Pointwise Conv：DSC的下一步

<p align="center">
  <img src="../res/img/img36.png" width="600"/>
</p>

#### iii. Cost summary

<p align="center">
  <img src="../res/img/img37.png" width="600"/>
</p>

#### iv. Architecture

MobileNet v1 vs. MobileNet v2

<p align="center">
  <img src="../res/img/img38.png" width="600"/>
</p>

Expansion -> Depthwise -> Pointwise (projection)

<p align="center">
  <img src="../res/img/img39.png" width="600"/>
</p>

### f. EfficientNet

Motivation: Scale a particular network up/down

Ways to change scale:

+ Higher resolution image
+ Deeper
+ Wider
+ Compound scaling（前三个合并一起改变）

<p align="center">
  <img src="../res/img/img40.png" width="600"/>
  <img src="../res/img/img41.png" width="600"/>
  <img src="../res/img/img42.png" width="600"/>
  <img src="../res/img/img43.png" width="600"/>
</p>

## 2. Advices for Using Conv

### a. Transfer Learning

Use pre-trained parameters (imageNet, coco, ...)

#### i. Small training set：
+ Method 1（蓝色）
  1. Freeze parameters of layers
  2. Change softmax layer (depends on real problems)
+ Method 2（紫色）
  1. 将input放入pre-trained model，得到output
  2. 对output搭建一个shallow network

<p align="center">
  <img src="../res/img/img44.png" width="600"/>
</p>

#### ii. Larger training set：
1. Freeze some layers
2. Train others

<p align="center">
  <img src="../res/img/img45.png" width="600"/>
</p>

#### iii. Lots of data:
1. 用开源神经网络的权重作为初始值（replace随机值初始化）
2. 重新训练整个网络

<p align="center">
  <img src="../res/img/img46.png" width="600"/>
</p>

### b. Data Augmentation

#### i. Common Augmentation Methods

+ Mirroring
+ Random cropping
+ Rotation
+ Shearing
+ Local warping

<p align="center">
  <img src="../res/img/img47.png" width="600"/>
</p>

#### ii. Color Shifting

PCA color augmentation -> 如果图片主要是紫色（红+蓝），那么这个算法会对红色和蓝色的改变多，绿色相对少

<p align="center">
  <img src="../res/img/img48.png" width="600"/>
</p>

#### iii. Implementation

Can be done in parallel
+ One thread: loading data and augmenting
+ The other thread: training

<p align="center">
  <img src="../res/img/img49.png" width="600"/>
</p>

### c. Computer Vision

#### i. Introduction

<p align="center">
  <img src="../res/img/img50.png" width="600"/>
</p>

#### ii. Tips

<p align="center">
  <img src="../res/img/img51.png" width="600"/>
</p>