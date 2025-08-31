# 1. Introduction

This project tests whether combining multiple images (image fusion) can improve
shape classification. Each sample has three 32×32 views of the same object
(circle, square, triangle, or pentagon). We:

- Train a LeNet-5 CNN on each single view (img1, img2, img3)
- Do early (pixel-level) fusion (avg/max/min, Laplacian pyramid, PCA) and train a CNN on the fused images
- Do late (decision-level) fusion via majority voting across the three single-view models
- Compare accuracies and show a confusion matrix

Idea: each view carries different cues; fusing them can keep useful edges and reduce noise,
often giving better results than any single view alone.
