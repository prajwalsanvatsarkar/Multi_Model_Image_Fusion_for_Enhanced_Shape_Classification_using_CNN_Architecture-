# Introduction

In this task, a low and high level fusion strategy is used to improve the classification performance of a synthetic dataset. There are 1000 images in the dataset, each have three 32x32 images that represent one of the four geometric shapes (pentagon, circle, square, or triangle). Three distinct background types gradient, noise, and spotlight are used to create the images. To classify these shapes, a convolutional neural network called LeNet 5 is implemented. To compare performance improvements, 3 LeNet5 models are trained and evaluated on the images without fusion at first and then another LeNet5 model is trained and evaluated on fused image dataset obtained from the defined fusion strategy. Finally the increased accuracy of the CNN model is achieved for the shape classification task. At the end confusion matrices are plot to demonstrate these accuracies.

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

b. Pixel-based Maximum Fusion: It involves directly selecting the maximum pixel value amoung the pixel values of the all three images to create a new, fused image.

c. Pixel-based Minimum Fusion: It involves directly selecting the minimum pixel value amoung the pixel values of the all three images to create a new, fused image.

![Low_level_fusion](https://github.com/user-attachments/assets/1cdf2c16-b48d-4e64-b826-dbdf7760794b)

2. High Level Fusion (Majority Voting) : Among all four models, the final classification is decided by majority vote. In this method, the predicted class that receives the most votes from the individual models is selected as the final prediction.

# Results
![Results with confusion matrix](https://github.com/user-attachments/assets/98f2dd6e-a350-47dc-a23d-1a2ee7e347e3)


