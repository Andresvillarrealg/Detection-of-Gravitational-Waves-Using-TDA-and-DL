# Detection of Gravitational Waves Using Topological Data Analysis and Deep Learning

## Team

This project was developed by students from **Tecnológico de Monterrey**:

- **Gerardo Juárez Hernández** – A01732799
- **Andrés Villarreal González** – A00833915
- **Salvador Vidal Torres** – A01732983

**June 4, 2024**

---

## Project Overview

Detecting gravitational waves has revolutionized astrophysics, revealing new insights into massive cosmic events. However, identifying these faint signals amidst noise is challenging. This project enhances gravitational wave detection by integrating **Topological Data Analysis (TDA)** with **Convolutional Neural Networks (CNN)**. We use persistent homology to extract topological features from sliding window embeddings of time-series data, combining them with raw signals for CNN input vectors. Our approach aims to improve robustness and accuracy for low signal-to-noise scenarios in gravitational wave astronomy.

---

## Methodology

1. **Synthetic Data Generation**
   - Gravitational wave signals were obtained from a base dataset and downsampled.
   - Realistic noise was generated and added to signals to simulate various signal-to-noise ratios.
   - Datasets included both "signal-present" (wave + noise) and "signal-absent" (noise only) samples.

2. **Data Preprocessing**
   - **Sliding Window Embedding**: Transform signals into higher-dimensional point clouds.
   - **Principal Component Analysis (PCA)**: Dimensionality reduction for better visualization and analysis.

3. **Topological Feature Extraction (TDA)**
   - Persistent homology is computed from the point clouds.
   - **Persistence diagrams** summarize the lifetime of topological features (connected components, loops).
   - Features such as **persistence entropy** are extracted as input for machine learning.

4. **Deep Learning (CNN)**
   - Input to the CNN combines raw signals and topological features.
   - Model hyperparameters were carefully chosen for optimal classification.
   - **Permutation tests** are used to statistically validate the model's predictions.

5. **Mapper Classification (optional)**
   - Mapper is used for unsupervised dimensionality reduction and data visualization.

---

## Project Structure

- **data/** – Directory containing gravitational wave signals and synthetic datasets.
- **notebooks/** – Jupyter notebooks for each stage (data prep, TDA, model training).
- **tda/** – Scripts for persistence diagram generation and feature extraction.
- **cnn/** – Code for CNN model definition, training, and evaluation.
- **mapper/** – Optional scripts for Mapper analysis and visualization.
- **results/** – Generated figures and performance metrics.
- **Detection of Gravitational Waves Using TDA and DL.pdf** – Final report.

---

## Main Results

- The CNN achieved a **test accuracy of 83%** on synthetic data with variable noise, demonstrating the effectiveness of combining TDA features with deep learning.
- Permutation test gave a **p-value of 0.02**, indicating statistical significance.
- Visualizations (persistence diagrams, embeddings) illustrate the discriminative power of topological features for gravitational wave detection.

---

## References
- See the report for a complete list of references.

---


**Tecnológico de Monterrey – June 2024**
