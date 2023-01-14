# Week 1

## 1. Orthogonalization

TV tuning example:

<p align="center">
  <img src="../res/img/img1.png" width="600"/>
</p>

Chain of assumptions in ML:

<p align="center">
  <img src="../res/img/img2.png" width="600"/>
</p>

## 2. Setting Up Your Goal

### a. Single Evaluation Metric

有两个evaluation metrics的时候，快速的找出好的模型会很困难 -> 使用F1分数：2 / (1/P + 1/R)

<p align="center">
  <img src="../res/img/img3.png" width="600"/>
</p>

在多种类别的情况下：Compute the average

<p align="center">
  <img src="../res/img/img4.png" width="600"/>
</p>

### b. Satisficing and Optimizing Metric

+ Satisficing metric: 锦上添花，比如运行时间
+ Optimizing metric: 雪中送炭，比如模型精确度
+ cost = Sm - b*Om

<p align="center">
  <img src="../res/img/img5.png" width="600"/>
</p>

### c. Train/Dev/Test Distributions

+ 选择一个能反应data所有方面部分的数据作为dev set
+ dev set和test set必须要来自于same distribution

<p align="center">
  <img src="../res/img/img6.png" width="600"/>
</p>

### d. Splitting data

+ Old way vs. new way
+ Size of test set: set your test set to be big enough to give high confidence in the overall performance of your system

<p align="center">
  <img src="../res/img/img7.png" width="600"/>
</p>

### e. When to Change Dev/Test Sets And Metrics?

Example 1: 添加W[i] -> 如果不是porn，那么W[i] = 1；如果是，那么W[i] = 10

<p align="center">
  <img src="../res/img/img8.png" width="600"/>
</p>

Example 2: 更清晰的图片和不清晰（用户自己上传的） -> 用户可能更prefer自己上传的模糊图片

<p align="center">
  <img src="../res/img/img9.png" width="600"/>
</p>

## 3. Comparing to Human-level Performance


