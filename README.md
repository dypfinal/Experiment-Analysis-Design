# Optimizing Skin Cancer Detection Neural Networks: SVD for Storage Reduction and Model Pruning for Compute Efficiency

## Introduction

This project aims to optimize neural networks for skin cancer detection by leveraging Singular Value Decomposition (SVD) for image compression and model pruning techniques to enhance compute efficiency. The methodology involves compressing images using SVD, analyzing image quality metrics at various values of `k`, selecting the best reconstruction value, and subsequently proposing and training multiple neural network architectures. These models are pruned iteratively to minimize model size and learnable parameters, making them suitable for deployment in resource-constrained environments.

## Methodology

### 1. Singular Value Decomposition (SVD) for Image Compression

#### Algorithm
1. **Convert Images to Grayscale**: Images are converted to grayscale to simplify the processing and reduce computational complexity.
   
2. **Apply SVD**: SVD is applied to the grayscale images to decompose them into singular vectors and singular values.

3. **Select `k` Components**: Varying numbers of singular values (`k`) are selected to reconstruct the images.

4. **Reconstruct Images**: Images are reconstructed using the selected `k` components.

5. **Evaluate Image Quality Metrics**: Metrics such as RMSE, PSNR, SSIM, VOI, and others are calculated to evaluate the quality of reconstructed images.

6. **Select Optimal `k`**: The `k` value yielding the best trade-off between compression rate and image quality is chosen.

### 2. Neural Network Architecture Proposal and Training

#### Architecture Selection
- Multiple neural network architectures are proposed and trained using the reconstructed images from SVD.

#### Baseline Model
- A baseline model is established to benchmark the performance of subsequent pruned models.

### 3. Model Pruning for Compute Efficiency

#### Pruning Methodology
- **Iterative Pruning**: Filters in convolutional layers and dense layers connected to them are pruned iteratively.
- **Pruning Factors**: Models are pruned by factors such as 50%, 33.33%, 16.5%, until a minimal model with optimized efficiency is achieved.

#### Benefits of Pruning
- Reduces the number of learnable parameters and model size.
- Enhances computational efficiency, making the models suitable for deployment in small-scale environments.

## Conclusion

By combining SVD for image compression and model pruning for compute efficiency, this project aims to optimize skin cancer detection neural networks. The approach not only improves storage and computational efficiency but also maintains or enhances model performance. The findings and methodologies presented here are crucial for deploying effective and efficient skin cancer detection systems in real-world scenarios.

