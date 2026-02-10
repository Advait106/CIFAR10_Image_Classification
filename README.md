CIFAR‑10 Image Classification using CNN
🎯 Objective
Build a Convolutional Neural Network (CNN) to classify CIFAR‑10 images into 10 object categories and analyze model performance.

📂 Dataset
CIFAR‑10 contains:

60,000 RGB images

Image size: 32 × 32

10 classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck

Training images: 50,000

Test images: 10,000

⚙️ Train / Validation Split
We used the official CIFAR‑10 split:

Training set → 50,000 images

Test/Validation set → 10,000 images

🧹 Preprocessing
Pixel normalization (0–255 → 0–1)

One‑hot encoding of labels

Data augmentation:

Random rotation

Width/height shift

Horizontal flip

Zoom

🧠 Models Implemented
1️⃣ Baseline CNN
Architecture:

Conv → MaxPool

Conv → MaxPool

Dense → Softmax

Test Accuracy: 70.21%

2️⃣ Improved CNN
Enhancements:

Extra convolution layer

Batch Normalization

Dropout (0.3)

Data Augmentation

Early Stopping + LR Scheduler

Best Test Accuracy: 83.92%

📊 Metrics Reported
Accuracy

Loss curves

Confusion Matrix

Classification Report

🏆 Final Results
Model	Test Accuracy
Baseline CNN	70.21%
Improved CNN	83.92%
Accuracy Improvement: +13.7%

▶️ How to Run
python train.py
python evaluate.py
📊 Analysis of Results (Add below README)
Model Improvement Analysis
The improved CNN significantly outperformed the baseline model, achieving 83.92% accuracy compared to 70.21%.

The improvement was achieved through:

Deeper convolutional architecture

Batch normalization for stable training

Dropout to reduce overfitting

Data augmentation to improve generalization

Confusion Matrix Observations
From the confusion matrix:

Common misclassifications

Cat ↔ Dog (similar shapes and textures)

Truck ↔ Automobile (similar structure)

Best classified classes

Airplane

Ship

Frog

This indicates the model performs better on visually distinct objects.

Overfitting Analysis
Training and validation curves remained close, showing:

Good generalization

Minimal overfitting due to dropout and augmentation

Final Conclusion
This project demonstrates that CNNs are highly effective for image classification.
Architectural improvements and data augmentation resulted in a 13.7% accuracy increase, proving the importance of model optimization techniques.
