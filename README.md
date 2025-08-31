# Introduction

This project investigates whether fusing multiple views improves shape classification with LeNet-5.
Each sample contains three 32×32 views (gradient, noise, spotlight) of one shape (circle, square,
triangle, pentagon).

The task is organized into four main steps:
1) Dataset Overview — understand the three aligned views per sample.
2) Step 1: Change LeNet-5 Architecture — adjust a compact backbone used across all experiments.
3) Step 2: Train & Evaluate Without Fusion — train three single-view models (img1, img2, img3) and report confusion matrices.
4) Step 3: Implement Fusion Strategy — apply low-level (avg/max/min) and high-level (majority voting) fusion, then compare to baselines.

Finally, we compare accuracies and visualize results with confusion matrices.


# Dataset Overview :

Image 1 - Gradient background

Image 2 - Noise background

Image 3 - Spotlight background

# Step 1: Change LeNet5 Architecture
![LeNet5 Comparison](https://github.com/user-attachments/assets/255e6c14-4bd1-4f8c-aa58-adcf8df4a693)


# Step 2: Train and Evaluate LeNet without Fusion
Dataset Preparation:

Training:

Evaluation:
![Confusion matrix for each model](https://github.com/user-attachments/assets/0561569b-5481-4dd7-bfab-b96525fbd83d)

# Step 3: Implementing fusion Strategy
1. Low-Level Fusion:

a. Pixel-based Average Fusion: It involves directly combining the pixel values of the three images and take average value to create a new, fused image.

b. Pixel-based Maximum Fusion: It involves directly combining the pixel values of the three images and take maximum value to create a new, fused image.

c. Pixel-based Minimum Fusion: It involves directly combining the pixel values of the three images and take minimum value to create a new, fused image.

![Low_level_fusion](https://github.com/user-attachments/assets/1cdf2c16-b48d-4e64-b826-dbdf7760794b)

2. High Level Fusion : • Majority Voting : Among all four models, the final classification is decided by majority vote. In this method, the predicted class that receives the most votes from the individual models is selected as the final prediction.

# Results
![Results with confusion matrix](https://github.com/user-attachments/assets/98f2dd6e-a350-47dc-a23d-1a2ee7e347e3)


