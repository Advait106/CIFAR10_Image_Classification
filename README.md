# CIFAR-10 Image Classification using Convolutional Neural Networks
## Project Overview
This project builds and evaluates Convolutional Neural Network (CNN) models for image classification on the CIFAR-10 dataset.
CNN based image classification on CIFAR-10.
    A baseline model is built first, followed by an improved
    architecture using batch normalization, dropout,
    and data augmentation for higher accuracy.
---
## Dataset
- 60,000 RGB images
- 32 × 32 resolution
- 10 classes
- Training set: 50,000
- Test set: 10,000
---
## Preprocessing
- Pixel normalization (0–1 scaling)
- One-hot encoding of labels
- Data augmentation
  - rotation
  - width/height shift
  - horizontal flip
  - zoom
---
## Models
### Baseline CNN
- Two convolution layers
- Max pooling
- Dense classifier  
Test Accuracy: 70.21%


<img width="700" height="470" alt="download" src="https://github.com/user-attachments/assets/825d4aaa-f3c3-4c5f-bd41-11013b3e410f" />
<img width="691" height="470" alt="download" src="https://github.com/user-attachments/assets/02f1b68f-d403-4060-8afd-369fe293b505" />


### Improved CNN
- Additional convolution layer
- Batch Normalization
- Dropout
- Data augmentation
- Early stopping + LR scheduler  
Test Accuracy: 83.92%


<img width="691" height="470" alt="download" src="https://github.com/user-attachments/assets/880cfe2f-1c20-49db-8822-1006667c6112" />
<img width="691" height="470" alt="download" src="https://github.com/user-attachments/assets/5eaa104c-3240-4e76-8fbd-1879bfee1844" />


##Confusion Matrix


Diagonal values indicate correct predictions. Off-diagonal values show misclassifications. Minor confusion exists between visually similar classes such as cats vs dogs and trucks vs automobiles.



<img width="853" height="766" alt="download" src="https://github.com/user-attachments/assets/3c5ea2ac-fa1b-4bc6-85dc-208ec6958b5f" />


---
## Results
| Model | Accuracy |
|-------|-----------|
| Baseline | 70.21% |
| Improved | 83.92% |
Accuracy Improvement: +13.7%
---
## How to Run
#To train the model
python train.py
#To evaluate model
python evaluate.py


## Analysis
Improvements due to
- deeper feature extraction
- batch normalization stabilizing training
- dropout reducing overfitting
- augmentation improving robustness
- early stopping preventing overtraining



---
## Conclusion


The improved CNN significantly outperforms the baseline model achieving better generalization and higher classification accuracy.Future enhancements may include transfer learning and hyperparameter tuning.
