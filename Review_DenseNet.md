This is my review of Denset. [Densely Connected Convolutional Networks](https://arxiv.org/pdf/1608.06993v5.pdf) 

DenseNet is a followup of ResNet, because it further extends the idea of shortcut connections between layers in the network. In DenseNet, each layer is connected to all the subsequent layers in a feedfoward fashion with the same feature map size. With this dense connection, DenseNet can achieve high performance with better computation and parameter efficiency. Densenet also alleviate the vanishing gradient problem and encourage feature reuse. 

Architecture, what is new? 

The biggest difference of Dense compared to ResNet is that for each layer in DenseNet, all the feature maps from preceding layers are used as input, and its own feature maps are used as input into all subsequent layer with the same feature map size. The authors claimed that for network with L layers, there should be L(L+1)/2 connections. (understand?) 

Advantages? 




