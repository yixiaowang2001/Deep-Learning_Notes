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

### d. Bounding Box Algorithm

YOLO algorithm：将一张图平等分为nxn大小，然后对每个部分prediction得到一个output

<p align="center">
  <img src="../res/img/img58.png" width="500"/>
  <img src="../res/img/img59.png" width="500"/>
</p>

### e. Intersection with Union

Motivation：检验检测效果如何 -> 比率

<p align="center">
  <img src="../res/img/img60.png" width="600"/>
</p>

### f. Non-max Suppression

Motivation：判断是否算法对同一目标有多次检测 -> 几个选中的目标中选择概率最高的

<p align="center">
  <img src="../res/img/img61.png" width="500"/>
  <img src="../res/img/img62.png" width="500"/>
</p>

Implement：

<p align="center">
  <img src="../res/img/img63.png" width="600"/>
</p>

### g. Anchor Box

Motivation：detect multiple objects

<p align="center">
  <img src="../res/img/img64.png" width="600"/>
</p>

Implement

<p align="center">
  <img src="../res/img/img65.png" width="600"/>
</p>

Example

<p align="center">
  <img src="../res/img/img66.png" width="600"/>
</p>

### h. YOLO Algorithm

Training

<p align="center">
  <img src="../res/img/img67.png" width="600"/>
</p>

Making predictions

<p align="center">
  <img src="../res/img/img68.png" width="600"/>
</p>

Outputting the non-max suppressed outputs

<p align="center">
  <img src="../res/img/img69.png" width="600"/>
</p>


### i. Region Proposol

Procedure：将图片变成最右边的样式，然后对每个色块来运行YOLO（是一种segment algorithm）

<p align="center">
  <img src="../res/img/img70.png" width="600"/>
</p>

### j. Semantic Segementation

<p align="center">
  <img src="../res/img/img71.png" width="500"/>
  <img src="../res/img/img72.png" width="500"/>
</p>

Deep learning architure for semantic segementation

<p align="center">
  <img src="../res/img/img73.png" width="600"/>
</p>