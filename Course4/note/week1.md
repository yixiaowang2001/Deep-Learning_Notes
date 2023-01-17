# Week 1

## 1. Computer Vision

### a. Introduction

Image recognition问题：input会变的特别大

### b. Edge Detection Example

+ Python: conv-forward
+ Tensorflow: tf.nn.conv2d
+ keras: Conv2d

<p align="center">
  <img src="../res/img/img1.png" width="500"/>
  <img src="../res/img/img2.png" width="500"/>
</p>

More edge detection

<p align="center">
  <img src="../res/img/img3.png" width="600"/>
</p>

## 2. CNN
### a. Padding

+ 缺点
  + 每使用一次卷积，图像都会变小一点；每次想检测边界或者其他的特征时，都缩小图片
  + 边界上的点每次都只会被使用一次
+ 解决方案
  + 在最外圈增加一圈或n圈 -> Padding

<p align="center">
  <img src="../res/img/img4.png" width="500"/>
  <img src="../res/img/img5.png" width="500"/>
</p>

### b. Strided Convolution

Stirde -> 跳步 

<p align="center">
  <img src="../res/img/img6.png" width="500"/>
  <img src="../res/img/img7.png" width="500"/>
</p>

### c. Convolutions over Volume

<p align="center">
  <img src="../res/img/img8.png" width="600"/>
</p>

### d. One Layer of a Convolutional Network

If you have 10 filters that are 3*3*3 in one layer of a neural network, hwo many parameters does that layer have? -> 3*3*3+1 = 28; 28*10 = 280

Summary of notation:

<p align="center">
  <img src="../res/img/img9.png" width="600"/>
</p>

Example of ConvNet:

+ Convolution (CONV)
+ Pooling (POOL)
+ Fully connected (FC)

<p align="center">
  <img src="../res/img/img10.png" width="600"/>
</p>

### e. Pooling Layers

#### i. Max pooling

No parameters to learn

<p align="center">
  <img src="../res/img/img11.png" width="500"/>
  <img src="../res/img/img12.png" width="500"/>
</p>

#### ii. Average pooling

<p align="center">
  <img src="../res/img/img13.png" width="600"/>
</p>

#### iii. Summary

<p align="center">
  <img src="../res/img/img14.png" width="600"/>
</p>

### f. CNN Example

<p align="center">
  <img src="../res/img/img15.png" width="600"/>
</p>

Shape:

<p align="center">
  <img src="../res/img/img16.png" width="600"/>
</p>

### g. Why Convolutions?

1. Parameter sharing
2. Sparsity of connections

<p align="center">
  <img src="../res/img/img17.png" width="600"/>
</p>