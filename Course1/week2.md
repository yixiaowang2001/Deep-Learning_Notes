# Week 2

## 1. Binary Classification

### a. Images Store

64 * 64 * 3 -> 12288 * 1

<p align="center">
  <img src="res/img/img2.png" width="600"/>
</p>

### b. Notation

<p align="center">
  <img src="res/img/img3.png" width="600"/>
</p>

### c. Logistic Regression

#### i. 本质
将常规的线性回归公式套入Sigmoid function中，得到Logistic Regression。

<p align="center">
  <img src="res/img/img4.png" width="600"/>
</p>

#### ii. Logistic Regression cost function

+ 如果使用最小二乘法（1/2(y_hat - y)^2）来作为Logistic Regression的Loss function，会导致梯度下降无法达到Local optimum。
+ 定义Logistic Regression的loss function：

<p align="center">
  <img src="res/img/img5.png" width="400"/>
</p>