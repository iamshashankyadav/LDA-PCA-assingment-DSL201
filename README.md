# DSL201 - Assignment - Linear Discriminant Analysis (LDA) and Principal Component Analysis (PCA)

## Project Overview
This repository contains the implementation and analysis of **Linear Discriminant Analysis (LDA)** and **Principal Component Analysis (PCA)** as part of Assignment for DSL201.

---

## Objectives
This assignment covers the following:

1. **LDA for Classification and dimensionality reduction**:
   - Using the MNIST dataset to implement a one-vs-rest classification with Linear Discriminant Analysis.
   - Comparing the performance of the k-Nearest Neighbors (k-NN) classifier before and after LDA to the original data set.
2. **PCA for Dimensionality Reduction**:
   - Applying PCA (Karhunen-Loève Transform) to reconstruct face images from the faces94 dataset.
   - Illustrating the impact of varying the number of principal components on image quality.

---

## Contents
1. **LDA Analysis**: Implementing LDA for dimensionality reduction and k-NN accuracy comparison on MNIST data.
2. **PCA Analysis**: Using PCA to compress and reconstruct face images, visualizing reconstructed images with different numbers of principal components.

---

## LDA Experimentation
### Given Dataset
- A subset of the MNIST dataset containing digits 0-4.

### Preprocessing steps
- Images are flattened and normalized.

### LDA Transformation
- One-vs-Rest LDA is applied to enhance class separability.

### k-NN Comparison
- **Baseline k-NN accuracy**: 98.03%
- **Accuracy after LDA**: 95.80%

### Key Findings
-: LDA effectively reduces the dimensionality of the MNIST dataset while retaining the most important discriminatory features.
- k-NN performance did not improve after applying LDA, possibly due to the complexity of MNIST data and limitations of LDA for non-linear patterns.

---

## PCA Experimentation
### Dataset
- Faces from the faces94 dataset.

### Preprocessing
- Images converted to grayscale, resized to 100x100 pixels, and flattened.

### Reconstruction Quality
- Images reconstructed using 5, 6, 7, 8, 9, and 10 principal components.

#### Reconstruction Observations
- The key insight here is that PCA can effectively reduce the dimensionality of
face images while still preserving most of the essential information needed for
recognizing or understanding the faces. Even with only a few principal
components. As the number of components increases, the quality of the
reconstruction improves. However, it is clear that even with only a
handful of components, PCA can recover the general structure of the
face, though finer details are lost.
---

## Conclusion
1. **LDA**:
   - Effective for visualizing class separability but may not always improve classifier performance on complex datasets.
2. **PCA**:
   - Provides significant compression potential while preserving key image features, making it ideal for storage and computational efficiency.

---

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/iamshashankyadav/LDA-PCA-assingment-DSL201
   ```
2. Run the ipynb files to execute the experiments for both LDA and PCA.

---

## Requirements
- Python 3.x
- Required libraries:
  - `sci-kit-learn`
  - `matplotlib`
  - `numpy`
  - `cv2`
