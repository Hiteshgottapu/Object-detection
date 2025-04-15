# Object Detection Pipeline

This repository contains a complete pipeline for object detection, including dataset preparation, image augmentation, model training, evaluation, and prediction. The pipeline is implemented in Python using TensorFlow and OpenCV.
## Dataset Link: https://public.roboflow.com/object-detection/self-driving-car/2
## Table of Contents
- [Overview](#overview)
- [Dataset Preparation](#dataset-preparation)
- [Image Augmentation](#image-augmentation)
- [Model Training](#model-training)
- [Evaluation](#evaluation)
- [Prediction](#prediction)
- [Requirements](#requirements)
- [Usage](#usage)

## Overview
The pipeline processes an object detection dataset, applies data augmentation techniques, trains a Convolutional Neural Network (CNN) for binary classification, and evaluates the model's performance. The trained model can also be used for predictions on new images.

## Dataset Preparation
1. **Dataset Splitting**: A subset of the dataset is selected (95% of the images) and copied to a new directory.
2. **Directory Structure**:
   - Original dataset: `/kaggle/input/object-de/export`
   - Subset dataset: `/kaggle/working/95_percent_data`

## Image Augmentation
The pipeline uses `ImageDataGenerator` from TensorFlow for real-time data augmentation. Augmentation techniques include:
- Random rotation
- Width and height shifts
- Shear and zoom transformations
- Horizontal flips
- Normalization

## Model Training
A simple CNN model is built and trained using the augmented dataset. The architecture includes:
- Convolutional layers with ReLU activation
- MaxPooling layers
- Fully connected layers with dropout
- Sigmoid activation for binary classification

The model is trained for 10 epochs with an 80-10-10 split for training, validation, and testing.

## Evaluation
The model is evaluated on the test set using:
- Accuracy
- Confusion Matrix
- Classification Report (Precision, Recall, F1-Score)

## Prediction
The trained model is used to predict the class of new images. Images are preprocessed (resized and normalized) before prediction.

## Requirements
- Python 3.7+
- TensorFlow
- OpenCV
- NumPy
- Matplotlib
- Scikit-learn
- Seaborn

## Usage
1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-repo/object-detection.git
   cd object-detection
