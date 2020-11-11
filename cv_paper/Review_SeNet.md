# This is my review of [Squeeze-and-Excitation Networks](https://arxiv.org/abs/1709.01507) 

A broad of range of prior research has investigated the spatial component of ........
In this paper, they focused on the channel relationship and proprosed a novel architectural unit, "Sequeeze-and-Excitation" (SE) block, that adaptively recalibrates channnel-wise feature responses by explicitly modeling interdependencies between channels. (???) 
The SENet architecture has been proven to generalize extremly effectively across different datasets. Moreover, SE blocks can bring significant improvements in performance for existing STOAs at slight additional computational cost. 
SENet won the ILSVRC 2017 with top-5 error of 2.251%. 

1. Squeeze-and-Excitation Blocks 

Squeeze: Global Information Embedding 

To mitigate the problem of ... 

add channel descriptor, using global average pooling. In detail, 

Excitation: Adaptive Recalibration 

Which aims to fully capture channel-wise dependencies. 

