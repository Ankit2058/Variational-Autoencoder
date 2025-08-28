# Variational Autoencoder on MNIST

This repository contains a Variational Autoencoder (VAE) implementation trained on the MNIST dataset. The project demonstrates how probability can be used to model data through latent variables and generative sampling. 

## Understanding

Now let’s technically explain it. In the field of AI, when you want to know what the model wants, just look at its loss function. In a VAE, the loss function gives a penalty when you generate an inaccurate result. That loss denotes that the encoder didn’t correctly encode the input into the correct region, or the decoder didn’t correctly decode the encoded value, or both. So the accuracy part of the loss wants to make the model correctly encode and decode.  

Then comes KL divergence into the loss function: the difference in probability distribution between the one predicted by the encoder for the input and the probability distribution of the latent space. Basically, it wants to align the encoder-outputted probability distribution of input with the latent distribution, which is N(0, I).  

But why force the neural network to confine itself to a limited space? Because we want to make that confined space meaningful. We want the meaning of the entire dataset to be captured in the concise latent distribution space. We don’t want some random distribution of encoded values to generate accurate results just by neural network magic, we have seen this before in RNN, LSTM, etc. We want the distribution to have meaning, not just the capability to output correct results.  

The entire reason VAEs exist is to give meaning and structure to the encoded input: to define a space where every meaning in this universe exists. We defined that space as N(0, I), and we want to punish the model if it doesn’t encode its findings of this world into that space.  

## Overview

The workflow of this project is as follows:

1. **Encoding**: The MNIST dataset is encoded into a latent space using the encoder network, which outputs the mean and variance parameters of the approximate posterior distribution p(z|x).  
2. **Decoding**: The latent representations are decoded back into samples, reconstructing the original images.  
3. **Training**: The model is trained using the VAE objective, which combines reconstruction loss with a KL divergence regularizer.  
4. **Sampling**: After training, random latent vectors are sampled from the prior distribution p(z) and decoded into new image samples.  
5. **Visualization**: The latent space is visualized to show the structure learned by the model.

## Files

- `Variational-Autoencoder.ipynb`: Main Kaggle notebook containing training, visualization, and sampling code.  
- `README.md`: Project description and documentation.  

## Results

- Latent space visualization of the encoded dataset.  
- Reconstructions of MNIST digits from the latent space.  
- Randomly generated digit samples from latent vectors drawn from the prior distribution.  

## How to Run

1. Clone this repository:  
   ```bash
   git clone https://github.com/Ankit2058/Variational-Autoencoder.git
   cd vae-mnist-latent-visualization
