# Week 3

## 1. Sequence to Sequence Architectures

### a. Basic Models

<p align="center">
  <img src="../res/img/img47.png" width="600"/>
</p>

### b. Beam Search

#### i. Motivation

给出一个given x（某种语言版本），得到y（翻译版本）的概率，而不是直接给出y的概率

<p align="center">
  <img src="../res/img/img48.png" width="600"/>
</p>

结果是要寻找argmax（最大值），而不是randomly selected的

<p align="center">
  <img src="../res/img/img49.png" width="600"/>
</p>

使用beam search而不是greedy search，why？
+ Greedy search：对于每一个y<1>，output可能性最大的那个
+ Greedy search可能达到局部最优解，但不可能达到全局最优

<p align="center">
  <img src="../res/img/img50.png" width="600"/>
</p>

#### ii. Procedure

Beam search：
+ Step 1: output B个可能的words，
+ Step 2: 然后根据这三个words来找下一个可能的word，然后再找出可能行最大的B个pair
+ 如果 B = 1，那么beam search就和greedy search一样了

<p align="center">
  <img src="../res/img/img51.png" width="500"/>
  <img src="../res/img/img52.png" width="500"/>
</p>

#### iii. Refinements to beam search

Length normalization：介于full normalization和null normalization中的一种，调整alpha的权重来获得更好的效果

<p align="center">
  <img src="../res/img/img53.png" width="600"/>
</p>

#### iv. Disucssions

<p align="center">
  <img src="../res/img/img54.png" width="600"/>
</p>

#### v. Error analysis

比较两个outputs的概率（真实值和预测值）

<p align="center">
  <img src="../res/img/img55.png" width="600"/>
</p>

Logic: 如果是case 1，那么output有问题；如果是case 2，那么神经网络有问题

<p align="center">
  <img src="../res/img/img56.png" width="600"/>
</p>

Procedure:

<p align="center">
  <img src="../res/img/img57.png" width="600"/>
</p>

### c. Bleu Score

比较output和reference，

<p align="center">
  <img src="../res/img/img58.png" width="500"/>
  <img src="../res/img/img59.png" width="500"/>
</p>

使用n-bigrams（n个words合并在一起，然后step by step）

<p align="center">
  <img src="../res/img/img60.png" width="600"/>
</p>

### d. Attention Model

#### i. Intuition

Look at the part of the sentence at a time

<p align="center">
  <img src="../res/img/img61.png" width="600"/>
</p>

#### ii. Implementation

Computing attention

<p align="center">
  <img src="../res/img/img62.png" width="600"/>
</p>

Examples

<p align="center">
  <img src="../res/img/img63.png" width="600"/>
</p>

## 2. Speech Recognition

### a. CTC Cost

<p align="center">
  <img src="../res/img/img64.png" width="600"/>
</p>

### b. Trigger Word Detection

What is trigger word detection system?
+ Amazon Echo -> Alexa
+ Baidu DuerOS -> 小度你好
+ Siri -> Hey Siri
+ Google Home -> Okay Google

Algorithm

<p align="center">
  <img src="../res/img/img65.png" width="600"/>
</p>

