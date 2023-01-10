# Week 2

## 1. Mini-batch Gradient Descent

### a. Comparison

Idea: 把大的数据集分为几个大部分，对每个部分进行gradient descent，然后再把前部分graident descent的结果作为后一个部分的输入

<p align="center">
  <img src="../res/img/img18.png" width="600"/>
</p>

### b. Mini-batch Gradient Descent

<p align="center">
  <img src="../res/img/img19.png" width="600"/>
</p>

### c. Undestanding

在batch gradient descent中，cost在每次iteration的时候都下降；但在mini-batch中，cost应该是波动的

<p align="center">
  <img src="../res/img/img20.png" width="600"/>
</p>

+ Stochastic / In-between / Batch comparison
+ How to choose size? -> 
    + 大于2000再使用，一般选择64/512
    + 2的次方数
    + mini-batch不能超过CPU/GPU容量
    + mini-batch也可以作为hyperparameter，通过尝试不同的值来看哪个值让cost function J下降最快

<p align="center">
  <img src="../res/img/img21.png" width="600"/>
</p>


## 2. Exponentially Weighted Averages

### a. Implementation

Moving average:
+ V0 = 0
+ V1 = 0.9 * V0 + 0.1 * theta1
+ V2 = 0.9 * V1 + 0.1 * theta2
+ ...
+ Vn = beta * Vt-1 + (1-beta) * thetat

<p align="center">
  <img src="../res/img/img22.png" width="600"/>
</p>

+ Legend
    + 红：0.9
    + 绿：0.98
    + 黄：0.5
+ Vt -> an approximate average over 1/(1-beta) days temperature

<p align="center">
  <img src="../res/img/img23.png" width="500"/>
  <img src="../res/img/img24.png" width="500"/>
</p>

### b. Understanding

Why weighted average?

<p align="center">
  <img src="../res/img/img25.png" width="600"/>
</p>

### c. Bias Correction

紫线和绿线在后面重合

<p align="center">
  <img src="../res/img/img26.png" width="600"/>
</p>

## 3. Gradient Descent with Momentum

目的：让梯度下降变得平滑

<p align="center">
  <img src="../res/img/img27.png" width="500"/>
  <img src="../res/img/img28.png" width="500"/>
</p>

## 4. RMSprop

+ 在垂直方向上震荡更小
+ 可以使用更大的learning rate

<p align="center">
  <img src="../res/img/img29.png" width="600"/>
</p>

## 5. Adam Optimization ALgorithm

<p align="center">
  <img src="../res/img/img30.png" width="500"/>
  <img src="../res/img/img31.png" width="500"/>
</p>

## 6. Learning Rate Decay

+ 开始的时候learning rate较大，之后在靠近converge点的时候慢慢减小
+ Hyperparameter: alpha_0

+ epoch -> learning rate
    + 1 -> 0.1
    + 2 -> 0.067
    + 3 -> 0.05
    + 4 -> 0.04

<p align="center">
  <img src="../res/img/img32.png" width="500"/>
  <img src="../res/img/img33.png" width="500"/>
</p>

## 7. The Problem of Local Optima

<p align="center">
  <img src="../res/img/img34.png" width="500"/>
  <img src="../res/img/img35.png" width="500"/>
</p>