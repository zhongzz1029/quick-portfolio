# Semantic Segmentation 

### 2015 
---

[FCN]()

[DeconvNet]

[DeepLabV1 & V2]

[CRF-RNN]

[SegNet]

[DPN] 

### 2016 
---

[ENet] 

[ParseNet]

[DilatedNet]

### 2017
---

[DRN]

[RefineNet]

[ERFNet]

[GCN]
 
[PSPNet]

[DeepLabV3]

[LC] 

[FC-DenseNet]

[IDW-CNN]

[DIS]

[SDN]

### 2018 
---

[ESPNet] 

[ResNet-DUC-HDC]

[DeepLabV3+]

### 2019 
---

[ResNet-38]

[C3]

[ESPNetv2]

### 2020 
---

[DRRN Zhang JNCA20] 

--- 

Two types of image segmentation 

Semantic Segmentation and Instance Segmentation 

**FCN**:one of the fisrt proposed models for end-to-end semantic segmentation. SOTA cnns are converted to fully convolutional by making FC layers 1x1 convolutions. **Transposed** convolutions are used to upsample. skip connections are used. 


SegNet: encoder-decoder framework. encodrer and decoder are symmetrical to each other. 

UNet: encoder-decoder framework with skip connections. It was built for medical purposes to find tumours in lungs and brains. 

UNet for medical domain, FCN & SegNet for small dataset. 

DeepLab: 1. Atrous (Dilated?) Convolutions. 2. Atrous Spatial Pyramidal Pooling 3. Conditional Random Fields Usage for Improving Final Output. 

	Bilinear up sampling. 

PSPNet: Pyramid scene Parsing Network. Kind of like SPPNet, pool feature into different sizes, and combine them together. 






