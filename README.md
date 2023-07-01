# Project Name: Avengers Image Classification

This hobby project focuses on classifying images of Avengers characters into their respective classes. Initially, the project scraped images and processed them by resizing them to 64x64 pixels. The initial model was trained using a simple architecture with two convolutional layers, a flatten layer, and a fully connected layer. The model was initially trained to classify images into two classes: Iron Man and Black Widow.

## Table of Contents
1. [Introduction](#introduction)
2. [Data Collection and Preprocessing](#data-collection-and-preprocessing)
3. [Model Architecture](#model-architecture)
4. [Model Performance](#model-performance)

## Introduction

Image classification is an exciting field in computer vision, and this project focuses specifically on classifying Avengers images. By leveraging image processing techniques and machine learning models, the project aims to accurately identify the characters present in the images.

## Data Collection and Preprocessing

The project initially scraped images of Avengers characters from various sources. These images were processed by resizing them to a standardized size of 64x64 pixels. The image preprocessing step helps ensure consistency in the dataset and provides a suitable input size for the model.

## Model Architecture

The model used for this project has a simple architecture consisting of two convolutional layers, a flatten layer, and a fully connected layer. The model architecture is as follows:

```
Layer (type:depth-idx)                   Output Shape              Param #
==========================================================================================
CNN                                      [1, 2]                    --
├─Conv2d: 1-1                            [1, 10, 64, 64]           280
├─MaxPool2d: 1-2                         [1, 10, 32, 32]           --
├─Conv2d: 1-3                            [1, 10, 32, 32]           910
├─MaxPool2d: 1-4                         [1, 10, 16, 16]           --
├─Linear: 1-5                            [1, 2]                    5,122
```

The model consists of two convolutional layers followed by max-pooling layers to extract relevant features from the images. The output from the convolutional layers is flattened and passed through a fully connected layer to make the final predictions.

## Model Performance

The initial model achieved an accuracy of 62.5% on the test dataset, even with a simple architecture and a limited dataset. It's important to note that the accuracy of the model heavily depends on the quality and diversity of the training data. In this hobby project, the dataset might not be ideal, and there is room for improvement.

