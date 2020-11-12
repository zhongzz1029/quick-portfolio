# The is my review of [MobileNetV2, 2018 CVPR](https://arxiv.org/abs/1801.04381v4)

A new mobile architecture, **MobileNetV2** is introduced here. MobileNetV2 is based on inverted residual structure where the shortcut connections are between the thin bottleneck layers. The intermediate expansion layer inside the inverted residual block uses lightweight depthwise convolutions to filter features as a source of non-linearity. Additionally, the non-linearity of the output layer in the block is removed in order to retain representational power. 

This is a followup of the other architecture, [MobileNetV1](Review_MobileNet.md). Modern SOTAs require high computational resources beyond the capbilities of many mobile and embedded applicaitons, thus, MobileNetV2 is introduced to futher overcome this problem beyond MobileNetV1.    

## 1 Inverted residual with linear bottleneck

![figure4](/images/MobileNetV2/figure4.png) 

### 1x1 linear bottleneck layer with stride 1 

It was found that nonlinearity (ReLu) layer hurts destroy the information perserved from the input. Therefore, a 1x1 linear Conv layer is added at the end of each inverted residual block.

### BottleNeck block with stride 2 

The block is almost the same to the 1x1 linear bottleneck layer, except that it does not have residual connection and the stride is 2 on the depthwise 3x3 conv layer.  

### Basic bottleneck convolution

The basic structure of inverted residul is as follows: 

![table1](/images/MobileNetV2/table1.png)  

* t is the **expansion factor**, which is the ratio between the size of the input channel and that of the ouput after the first 1x1 conv. 

* The residual is the summation between the input of the first 1x1 layer and the output of the latter 1x1 conv layer.

* **ReLu6** is used here after each conv layer, y=min(max(x, 0), 6), because it is robust when used with low-precision computation. 

## 2 Overall architecture 

![table2](/images/MobileNetV2/table2.png)  

* where t is expansion factor, c is number of output channels, n is the repeating number, s is the stride. 3x3 is always used for spatial convolution. 

* 19 residual bottleneck layers (both stride 1 and stride 2). 

* Trade-off hyperparameter. width multiplier as in MobileNetV1. It is used for all layers except the very last conv layer. 

* t=6 for all main experiments. 

* BN after every layer(?)

## 3 Ablation Study 

## 4 Experiments

--- 

- [ ] Code 


