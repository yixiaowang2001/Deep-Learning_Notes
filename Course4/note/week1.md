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