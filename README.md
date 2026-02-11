# CIFAR-10 Image Classification using Convolutional Neural Networks

## Project Overview
This project builds and evaluates Convolutional Neural Network (CNN) models for image classification on the CIFAR-10 dataset.

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

<img width="700" height="470" alt="download" src="https://github.com/user-attachments/assets/e05e72a0-6615-41c9-ad08-b6582e0d028f" />
<img width="691" height="470" alt="download" src="https://github.com/user-attachments/assets/59fd9546-a04e-4b7c-80dd-e5650542723e" />


### Improved CNN
- Additional convolution layer
- Batch Normalization
- Dropout
- Data augmentation
- Early stopping + LR scheduler  
Test Accuracy: 83.92%

#Confusion Matrix
<img width="853" height="766" alt="download" src="https://github.com/user-attachments/assets/8c2da185-aaf5-4f66-964d-36950863fcc5" />

---

## Results

| Model | Accuracy |
|-------|-----------|
| Baseline | 70.21% |
| Improved | 83.92% |

Accuracy Improvement: +13.7%

---

## How to Run
python train.py
python evaluate.py



---

## Conclusion
The improved CNN significantly increased performance through deeper architecture, regularization, and augmentation, achieving strong generalization on unseen data.



