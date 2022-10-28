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

## 2. Logistic Regression

### a. 本质
将常规的线性回归公式套入Sigmoid function中，得到Logistic Regression。

<p align="center">
  <img src="res/img/img4.png" width="600"/>
</p>

### b. Logistic Regression cost function

+ 如果使用最小二乘法（1/2(y_hat - y)^2）来作为Logistic Regression的Loss function，会导致梯度下降无法达到Local optimum。
+ 定义Logistic Regression的loss function：

<p align="center">
  <img src="res/img/img5.png" width="800"/>
</p>

+ Cost function：

<p align="center">
  <img src="res/img/img6.png" width="800"/>
</p>

### c. Gradient Descent

Update gradient based on (w, b):

<p align="center">
  <img src="res/img/img7.png" width="400"/>
</p>

## 3. Computation Graph

+ Example

<p align="center">
  <img src="res/img/img8.png" width="600"/>
</p>

+ 相比正向推导，在计算微分的时候，我们会反向来看整个流程（chain rule）

<p align="center">
  <img src="res/img/img8.png" width="500"/>
  <img src="res/img/img8.png" width="500"/>
</p>