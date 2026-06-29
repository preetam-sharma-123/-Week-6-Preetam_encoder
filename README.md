# Week 6 – Denoising Autoencoder on MNIST

## Celebal Technologies Data Science Internship

### Intern

**Preetam Sharma**

---

## Project Overview

This project implements a **Convolutional Denoising Autoencoder** using TensorFlow/Keras to reconstruct clean handwritten digit images from noisy MNIST images.

The model learns to map noisy inputs to their corresponding clean versions, effectively removing Gaussian noise while preserving digit structure and visual quality.

---

## Objectives

* Load and preprocess the MNIST dataset
* Add Gaussian noise to input images
* Build a Convolutional Denoising Autoencoder
* Train the model to reconstruct clean images
* Evaluate reconstruction quality using MSE and PSNR
* Analyze performance across digit classes
* Study robustness using different noise levels

---

## Dataset

**MNIST Handwritten Digits Dataset**

* Training Images: 60,000
* Testing Images: 10,000
* Image Size: 28 × 28 grayscale
* Classes: Digits 0–9

---

## Model Architecture

### Encoder

* Conv2D (32 filters)
* Conv2D (64 filters)
* Flatten Layer
* Dense Latent Vector (64 dimensions)

### Decoder

* Dense Layer
* Reshape Layer
* Conv2DTranspose (64 filters)
* Conv2DTranspose (32 filters)
* Conv2D Output Layer (Sigmoid)

---

## Features Implemented

* Gaussian Noise Injection
* Convolutional Autoencoder
* EarlyStopping Callback
* ReduceLROnPlateau Callback
* ModelCheckpoint Callback
* MSE Evaluation
* PSNR Evaluation
* Per-Digit Performance Analysis
* Noise-Level Ablation Study
* Architecture Visualization
* Model Saving and Loading

---

## Evaluation Metrics

### Mean Squared Error (MSE)

Measures the average squared difference between reconstructed and original images.

### Peak Signal-to-Noise Ratio (PSNR)

Measures reconstruction quality in decibels (dB). Higher values indicate better reconstruction.

---

## Results

The trained model successfully removed Gaussian noise from MNIST images while preserving digit shapes and stroke information.

Key observations:

* Significant reduction in reconstruction error
* Strong improvement in PSNR
* Consistent performance across digit classes
* Good robustness near the training noise level
* Graceful degradation as noise intensity increases

---

## Ablation Study

The model was evaluated on multiple noise levels:

* 0.1
* 0.2
* 0.3
* 0.4
* 0.5
* 0.6
* 0.7

Results demonstrate the model's ability to generalize across varying noise intensities while maintaining acceptable reconstruction quality.

---

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib

---

## Files Included

* `week6_preetam_CT.ipynb`
* `mnist_denoising_autoencoder.keras`
* `mnist_encoder.keras`
* `mnist_decoder.keras`
* Training and evaluation visualizations

---

## Future Improvements

* Variational Autoencoders (VAE)
* U-Net Based Denoisers
* SSIM Loss Functions
* Attention-Based Autoencoders
* Multi-Noise Training
* Real-World Image Denoising

---

## Conclusion

A Convolutional Denoising Autoencoder was successfully developed and trained on the MNIST dataset. The model effectively reconstructs clean handwritten digits from noisy inputs and demonstrates strong denoising capability, making it a solid foundation for more advanced image restoration systems.
