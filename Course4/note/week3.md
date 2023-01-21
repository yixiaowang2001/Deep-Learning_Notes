# Week 3

## 1. Detection Algorithm

### a. Object Localization

Classification with Localization

<p align="center">
  <img src="../res/img/img52.png" width="600"/>
</p>

Defining the target label y

<p align="center">
  <img src="../res/img/img53.png" width="600"/>
</p>

### b. Landmark Detection

标记点，每个点的位置作为ground truth

<p align="center">
  <img src="../res/img/img54.png" width="600"/>
</p>

### c. Object Detection

#### i. Sliding windows detection

小方块一步一步找，然后将size变大 -> Computational cost太大

<p align="center">
  <img src="../res/img/img55.png" width="600"/>
</p>

#### ii. Turning FC to Conv layers

<p align="center">
  <img src="../res/img/img56.png" width="600"/>
</p>

#### iii. Conv implementation of sliding windows

<p align="center">
  <img src="../res/img/img57.png" width="600"/>
</p>

#### iv. Bounding Box Algorithm

YOLO algorithm：将一张图平等分为nxn大小，然后对每个部分prediction得到一个output

<p align="center">
  <img src="../res/img/img58.png" width="500"/>
  <img src="../res/img/img59.png" width="500"/>
</p>