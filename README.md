# Part 2: CNN Computer Vision Project

## Problem Statement

The given dataset contains product surface images with different types of defects.  
The objective of this project is to build a CNN (Convolutional Neural Network) model that can classify images into different defect categories.

The project demonstrates how CNN models learn visual patterns from image data using convolution layers, pooling layers, activation functions, and dense layers.

---

# Task 1: Problem Identification

This dataset represents an **Image Classification** problem.

Reason:
- Each image belongs to only one category
- The goal is to classify the image into a single class
- No bounding boxes or pixel-level masks are provided

The four classes in the dataset are:
- dent
- normal
- scratch
- stain

---

# Task 2: Dataset Exploration

## Number of Classes

The dataset contains 4 classes:
- dent
- normal
- scratch
- stain

## Number of Images Per Class

- dent: 120 images
- normal: 120 images
- scratch: 120 images
- stain: 120 images

The dataset is balanced because all classes contain equal number of images.

## Image Dimensions

All images have dimensions:
- 96 × 96 pixels

## Sample Images

Sample images from each class were visualized in the notebook.

---

# Task 3: Image Preprocessing

The following preprocessing steps were performed:

- Resized all images to 96 × 96
- Normalized pixel values using ImageDataGenerator
- Split dataset into training and validation sets
- Applied image augmentation such as:
  - rotation
  - zoom
  - horizontal flip

These preprocessing steps help improve model generalization.

---

# Task 4: CNN Model Creation

A CNN model was built using TensorFlow/Keras.

The model contains:
- Convolution layers
- ReLU activation functions
- MaxPooling layers
- Flatten layer
- Dense layer
- Dropout layer
- Softmax output layer

The model was trained using categorical crossentropy loss and Adam optimizer.

---

# Task 5: Model Training and Evaluation

The CNN model was trained for 20 epochs.

## Final Performance

- Test Accuracy: 93.75%
- Test Loss: 0.168

## Evaluation Methods

The following evaluation methods were used:
- Accuracy and loss curves
- Confusion matrix
- Classification report
- Sample predictions

The model achieved strong performance on the dataset and correctly classified most images.

---

# Task 6: CNN Concept Explanation

## What is Convolution?

Convolution is a process where small filters scan the image to detect important features such as edges, shapes, and textures.

## Why is Pooling Used?

Pooling reduces the size of feature maps and helps reduce computation.  
It also helps the model focus on important features.

## Why is ReLU Commonly Used?

ReLU helps the model learn non-linear patterns and improves training speed.

## Why are CNNs Better Than Regular Feed-Forward Networks for Images?

CNNs are better for image data because they automatically learn visual features from images while preserving spatial relationships between pixels.

---

# Task 7: Business Use Case Mapping

This type of computer vision solution can be used in manufacturing industries for quality inspection.

Example:
- Detect dents
- Detect scratches
- Identify stained products
- Separate defective products from normal products automatically

This can reduce manual inspection effort and improve production quality.

---

# Project Structure

part-2-cnn-computer-vision/

├── README.md  
├── notebook.ipynb  
├── requirements.txt  

├── sample_predictions/  
│   └── prediction_outputs.png  

└── results/  
    ├── accuracy_loss_curves.png  
    └── confusion_matrix.png
