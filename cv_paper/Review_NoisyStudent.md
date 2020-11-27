# This is my review of [Noisy Student](https://arxiv.org/abs/1911.04252)

# Abstract 

The paper presents a semi-supervised learning approach, **Noisy Student Training**, that works well even though when labeled data is abundant. Noisy Student Training extends the idea of self-training and distillation with the use of equal-or-larger student models and noise added to the student during learning. On ImageNet, (1) a teacher EfficientNet model is training with labeled data, (2) after that it is used to generate pseudo labels for unlabeled images. (3) Then, a larger EfficientNet model is training as student on the combination of labeled and pseudo labeled images. (4) Iterating this process by putting the student as the teacher. During the training of student, noise is injected such as **dropout**, **stochastic depth**, and data augmentation via **RandAugment**. 

# Two Key Improvements 

### 1 Noise added 

Noise is added when training the student and the teacher to make them consistent. It is, however, not added when the teacher predicts pseudo labels. Two types of noises are introduced in this paper, input noise and model noise. 

### 2 Student model is larger-or-equal than teacher model

The student model is given much lager capacity to be better than the teacher. Thus, the method can be also called Knowledge Expansion. 

### 3 Other techniques used 

Data filtering and balancing. Images are filtered out if they have low confidence from the predictions by the teacher. To ensure the distribution of unlabeled data, images are duplicated if they do not have enough samples in a class, otherwise, they are removed if they have too many in a classe based on the confidence from the teacher predictions. 
  
