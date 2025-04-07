# DCGAN on MNIST

This project implements a **Deep Convolutional Generative Adversarial Network (DCGAN)** using **PyTorch** to generate handwritten digit images based on the MNIST dataset. The training is designed to run on **Google Colab** with data stored on **Google Drive**.


## Development setup

Local run without google colab

1. Install uv:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

2. Install dependencies:

```bash
uv sync
```



## Features

- Implements a custom **Generator** and **Discriminator** using PyTorch
- Trains on the **MNIST dataset** with normalized grayscale images
- Uses **Adam optimizer** and **Binary Cross Entropy loss**
- Saves generated image samples during training
- Includes visualization of generated digits

## Model Architecture

### Generator
- Transposed Convolutions (a.k.a. Deconvolutions)
- Batch Normalization and ReLU activations
- Outputs 28×28x1 grayscale images

### Discriminator
- Convolutional layers
- LeakyReLU activations
- Ends with a Sigmoid output for binary classification (real vs. fake)

## Training

- Batch Size: 32
- Learning rate: 0.0002
- Epochs: 20
- Optimizer: Adam
- Loss Function: Binary Cross Entropy
- Training images are logged every 5 epochs for visual inspection


Images are normalized to the [-1, 1] range for stability during GAN training.

## Output

The notebook generates sample outputs showing the evolution of generated digits over epochs. These are saved to image files and optionally displayed using `matplotlib`.
