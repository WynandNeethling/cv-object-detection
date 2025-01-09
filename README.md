
# Computer Vision 842: Assignment 2

This repository contains solutions which focuses on input masking, evaluating object detection models, and building fully convolutional networks for image denoising.

## Task Overview

### 1. Input Masking

- **Approach**:
  - Use a pre-trained network on ImageNet.
  - Generate **saliency maps** for random images by systematically occluding portions of a correctly classified image.
  - Record how the network’s output probability of the correct class changes as the occluded square moves across the image.
- **Reference**: Zeiler and Fergus (2013) ([Paper link](https://arxiv.org/abs/1311.2901))

### 3. Fully Convolutional Networks for Image Denoising

- **Approach**:
  - Split the dataset into training, validation, and test sets.
  - Add zero-mean Gaussian noise with a standard deviation of 10% of the maximum possible pixel value to every pixel in the images.
  - Train a relatively small network (3 to 5 convolutional and pooling layers in the encoder).
  - Specify the loss function used for training.
  - Evaluate the performance of the final model on a handful of noisy test images.

## Results and Discussion

- Visualizations of saliency maps for input masking.
- mAP calculation and detection results for object detection models.
- Noisy image reconstructions and denoising performance for fully convolutional networks.
