CIFAR‑10 Image Classification using Convolutional Neural Networks
Project Overview
This project focuses on building and evaluating Convolutional Neural Network (CNN) models for image classification on the CIFAR‑10 dataset. The goal is to design a baseline model, improve its performance using deep learning techniques, and analyze the results.

Dataset
The CIFAR‑10 dataset contains:

60,000 RGB images

Image size: 32 × 32 pixels

10 object classes:

Airplane

Automobile

Bird

Cat

Deer

Dog

Frog

Horse

Ship

Truck

Dataset split:

Training set: 50,000 images

Test set: 10,000 images

The official dataset split was used as the train/validation split.

Preprocessing
The following preprocessing steps were applied:

Pixel normalization (values scaled from 0–255 to 0–1)

One‑hot encoding of class labels

Data augmentation applied to the training set:

Random rotation

Width and height shifting

Horizontal flipping

Random zoom

Data augmentation was used to improve model generalization and reduce overfitting.

Models Implemented
Baseline CNN
Architecture:

Convolution layer → MaxPooling

Convolution layer → MaxPooling

Fully connected layer → Softmax output

Baseline Test Accuracy: 70.21%

Improved CNN
Enhancements introduced:

Additional convolution layer

Batch Normalization after convolution layers

Dropout regularization (0.3)

Data augmentation during training

Early stopping and learning rate scheduling

Improved Test Accuracy: 83.92%

Evaluation Metrics
The models were evaluated using:

Test Accuracy

Training and validation loss curves

Training and validation accuracy curves

Confusion Matrix

Classification Report (precision, recall, F1‑score)

Results Summary
Model	Test Accuracy
Baseline CNN	70.21%
Improved CNN	83.92%
Accuracy improvement achieved: 13.7%

Analysis of Results
Model Improvement
The improved CNN significantly outperformed the baseline model. The increase in accuracy is attributed to:

Deeper feature extraction through additional convolution layers

Stabilized training via batch normalization

Reduced overfitting using dropout

Better generalization from data augmentation

Confusion Matrix Observations
Key observations from the confusion matrix:

Common misclassifications:

Cats and dogs were frequently confused due to similar visual features.

Trucks and automobiles were sometimes misclassified because of similar shapes.

Classes with strong performance:

Airplanes

Ships

Frogs

These classes are visually more distinct, making them easier for the model to classify.

Overfitting Analysis
Training and validation curves remained close throughout training, indicating:

Minimal overfitting

Effective use of regularization and augmentation

Good generalization on unseen data

How to Run the Project
Train the model:

python train.py
Evaluate the model:

python evaluate.py
Conclusion
This project demonstrates the effectiveness of convolutional neural networks for image classification. By improving the network architecture and applying data augmentation and regularization techniques, the model achieved a significant performance improvement on the CIFAR‑10 dataset.
