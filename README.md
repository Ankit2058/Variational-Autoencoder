# Variational Autoencoder on MNIST

This repository contains a Variational Autoencoder (VAE) implementation trained on the MNIST dataset. The project demonstrates how probability can be used to model data through latent variables and generative sampling.

## Overview

The workflow of this project is as follows:

1. **Encoding**: The MNIST dataset is encoded into a latent space using the encoder network, which outputs the mean and variance parameters of the approximate posterior distribution.  
2. **Decoding**: The latent representations are decoded back into samples, reconstructing the original images.  
3. **Training**: The model is trained using the VAE objective, which combines reconstruction loss with a KL divergence regularizer.  
4. **Sampling**: After training, random latent vectors are sampled from the prior distribution and decoded into new image samples.  
5. **Visualization**: The latent space is visualized to show the structure learned by the model.

## Files

- `notebook.ipynb`: Main Kaggle notebook containing training, visualization, and sampling code.  
- `README.md`: Project description and documentation.  

## Results

- Latent space visualization of the encoded dataset.  
- Reconstructions of MNIST digits from the latent space.  
- Randomly generated digit samples from latent vectors drawn from the prior distribution.  

## How to Run

1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/vae-mnist-latent-visualization.git
   cd vae-mnist-latent-visualization
   ```
2. Open the notebook in Jupyter or upload it to [Kaggle](https://www.kaggle.com/) to run.  
3. Ensure you have `torch`, `torchvision`, `matplotlib`, and `scikit-learn` installed.  

## Requirements

- Python 3.x  
- PyTorch  
- Torchvision  
- Matplotlib  
- scikit-learn  
