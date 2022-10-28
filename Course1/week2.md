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
  <img src="res/img/img9.png" width="500"/>
  <img src="res/img/img10.png" width="500"/>
</p>

## 4. Logistic Regression Derivatives

+ Simplified formula for the derivative of the losswith respect to z: a - y

<p align="center">
  <img src="res/img/img11.png" width="600"/>
</p>

+ Logistic regression on m examples（如果按照右图的写法的话，需要两个for loop（i和num of features），所以我们通常使用Vectorization）

<p align="center">
  <img src="res/img/img12.png" width="500"/>
  <img src="res/img/img13.png" width="500"/>
</p>

## 5. Vectorization

### a. Comparison

<p align="center">
  <img src="res/img/img14.png" width="600"/>
</p>

### b. Code

[week2.ipynb](https://github.com/yixiaowang2001/Deep-Learning_Notes/blob/main/Course1/week2.ipynb)

## 6. Logistic Regression

### a. Pseudocode

#### i. For loop version

<p align="center">
  <img src="res/img/img15.png" width="500"/>
</p>

#### ii. Vectorization version

<p align="center">
  <img src="res/img/img16.png" width="600"/>
</p>

### b. Process

<p align="center">
  <img src="res/img/img17.png" width="600"/>
</p>

