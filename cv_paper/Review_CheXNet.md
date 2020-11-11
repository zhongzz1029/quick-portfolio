# The is my review of [CheXNet](https://stanfordmlgroup.github.io/projects/chexnet/)

CheXNet can detect pneumonia from chest X-rays at a level exceeding practicing radiologists. CheXNet is a 121-layer CNN trained on ChestX-ray14, which is the largest pubilicly availiable chest X-ray dataset. CheXNet also outperform best published results on detecting all 14 diseases in the dataset.


## 1 Model Architecture    

CheXNet is a 121-layer Dense Covolutional Network. DenseNets improve flow of information and gradients through the network. The final fully connected layer is replaced with one that has sigle output, sigmoid layer. 

The weights of the network are initialized with weights from a model pretrained on ImageNet (? which network). Some details on training the model: 
	
	- Adam optimizer is used to train the network.  

	- Mini batch size is 16. 

	- learning rate is set to 0.001, reduced by a factor of 10 when validataion loss plateaus. 

## 2 Data 

ChestX-ray14 dataset is used to train CheXNet and compare this network results with those by expert radiologist. For pneumonia detection task, the dataset is randomly split into training (28744 patients, 98637 total images), validation (1672 patients, 6351 images), test (389 patients, 420 images). 

The images are downscaled (?) into 224x224 and normalized based on the mean and standard deviation of images in the ImageNet training set. Random hrizontal flipping also is applied to the images.

## 3 CheXnet vs Radiologist 

F1 score is used as metric to compare the performance. 

Boostrap is adopted too, 10,000 samples, sampled with replacement from the test set (412 images) is used to test both the CheXNet and 4 different expert radiologists to construct 95% bootstrap confidence intervals, calculating the average F1 scores. (bootstrap?)  

CheXNet achieves an F1 score of 0.435, higher than the radiologists average of 0.387. 

![tablel1](/images/CheXNet/table1.png) 


#### A few limitations 

## 4 CheXNet vs Previous STOA on ChestX-ray14 

Modifications on CheXNet. 

	- extend the network to classify multiple pathologies. 

	- Replace sigmoid layer with softmax layer. 

	- Cross entropy loss is used.  

CheXNet ahieves state-of-the-art AUROC results on all 14 pathologies compared with previous SOTAs.

![table2](/images/CheXNet/table2.png)

## 5 Model Interpretation

To interpret the network, heatmaps also are produced to visualize the areas of the image most indicative of the disease using class activation mappings (CAM). 

![figure2](/images/CheXNet/figure2.png) 
 






