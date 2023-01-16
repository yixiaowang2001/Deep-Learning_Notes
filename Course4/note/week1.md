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

### c. Padding

+ 缺点
  + 每使用一次卷积，图像都会变小一点；每次想检测边界或者其他的特征时，都缩小图片
  + 边界上的点每次都只会被使用一次
+ 解决方案
  + 在最外圈增加一圈或n圈

<p align="center">
  <img src="../res/img/img4.png" width="500"/>
  <img src="../res/img/img5.png" width="500"/>
</p>

### d. Strided Convolution

Stirde -> 跳步 

<p align="center">
  <img src="../res/img/img6.png" width="500"/>
  <img src="../res/img/img7.png" width="500"/>
</p>

### e. Convolutions Over Volume

<p align="center">
  <img src="../res/img/img8.png" width="600"/>
</p>

### f. One Layer of a Convolutional Network

<p align="center">
  <img src="../res/img/img9.png" width="600"/>
</p>

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