# This is my review of [EfficientNet: Rethinking Model Scaling for Convolutional Neural Networks](https://arxiv.org/pdf/1905.11946.pdf) 

This paper systematically studied model scaling and identified that carefully balancing network depth, width and resolution can lead to better performance. It proposes a new simple but effective compound coefficient that can be used to uniformly scale all dimensions of depth, width, and resolution. To go even further, a baseline model is designed and scaled up to obtain a family of models, called EfficientNets. EfficientNets achieve better accuracy and efficiency (fewer parameters and FLOPS) than previous ConvNets. 

## Outline: 

* 1. Motivation 

Previous studies have shown that scaling up the network dimensions can improve model accuracy. However, most of them only tried to scale one of the dimensions, either depth, width or resolution, others tried to arbitrarily scale two or three dimensions, which require tediout manual tuning and often yield sub-optimal accuracy and efficient. The this paper aimed to rethink the scaling process and investigate if there is a principled method to scale up Convnets that can achieve better accuracy and efficient.  
 
* 2. Compounding Scaling

Two observations about scaling up the dimensions. First, scaling up any dimensions of network depth, width, or resolution improves accuracy, but the accuracy gain diminishes for bigger model. Second, it is critical to balance all dimensions of network width, depth, and resolution during ConvNet scaling. 

Compound scaling method uniformly scales network width, depth, and resolution in a principled way. 

![constrait](/images/) 

Because convolution ops usually dominate the computation cost in ConvNets, alpha is not squared by 2 here. φ is a user-specified coefficient that controls how many more resources are available. 

* Architecture 

In order to better demonstrate the effectiveness of the scaling method, a new mobile-size baseline model was developed, call EfficientNet by leveraging a multi-objective neural architecture search that optimizes both accuracy and FLOPS. The baseline architecture is similar to MnasNet, whose building block is mobile inverted bottleneck **MBConv** (increase dimension first and reduce it back to input size). Also, squeeze-and-excitation optimization is added to the buidling block. 

![EfficnetNet-B0](/images/) 


* Advantages 

* Experiments 

* Conclusion 

## 1. Motivation 






Understand how they propose the compound coefficient. 

FLOPS? 





