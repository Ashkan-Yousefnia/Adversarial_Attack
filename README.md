# 🛡️ Adversarial Attacks on Deep Learning Models

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://python.org)
[![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-EE4C2C.svg)](https://pytorch.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This repository contains implementations of various adversarial attack techniques against deep learning models, focusing on both vision and speech domains[cite: 3]. It explores the vulnerability of Deep Neural Networks (DNNs) to carefully crafted perturbations and demonstrates methods to expose these failure modes[cite: 3].

## 📌 Project Overview

Deep Neural Networks excel at recognizing patterns, often achieving human-level performance in tasks like image classification[cite: 3]. However, research has shown that these models can be easily fooled by adding salient but carefully constructed, imperceptible noise to the input data[cite: 3]. This project investigates these vulnerabilities by implementing custom adversarial attack strategies to trick trained networks[cite: 3]. The consequences of such attacks can be severe, especially in critical applications like autonomous driving, where an attack could make a pedestrian "invisible" to the network's image understanding system[cite: 3].

## ✨ Key Features

*   **White-box & Black-box Attacks:** Implements both white-box and black-box adversarial attacks, including Fast Gradient Sign Method (FGSM) and Projected Gradient Descent (PGD).
*   **High Misclassification Rates:** Achieves up to 93.7% misclassification on target models using imperceptible noise.
*   **Cross-Domain Application:** Attacks are developed and evaluated on both vision (image classification) and speech models.
*   **Adversarial Patches:** Includes the training of adversarial patches designed to disrupt object detection. These patches successfully reduced detection accuracy by 70% under varied lighting conditions and viewing angles.
*   **Pre-trained Model Evaluation:** Utilizes common CNN architectures, such as ResNet34, trained on the ImageNet dataset (provided via PyTorch's `torchvision` package) for testing and evaluation[cite: 3].
*   **Performance Metrics:** Evaluates model performance and attack success using standard metrics like "Top-1 Error Rate" and "Top-5 Error Rate", which are crucial for assessing models on datasets with many classes like ImageNet[cite: 3].

## 🚀 Getting Started

### Prerequisites

*   Python 3.x
*   PyTorch
*   Torchvision[cite: 3]
*   Matplotlib (for plotting and visualization)[cite: 3]
*   Seaborn[cite: 3]
*   SciPy[cite: 3]
*   Tqdm (for progress bars)[cite: 3]
*   PyTorch Lightning (optional, for advanced training workflows)[cite: 3]

### Installation

1.  Clone the repository:
    ```bash
    git clone [https://github.com/yourusername/adversarial-attacks-dl.git](https://github.com/yourusername/adversarial-attacks-dl.git)
    cd adversarial-attacks-dl
    ```
2.  Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```
    *(Note: You may need to create a `requirements.txt` file based on the imports listed in the notebook.)*

### Data and Pre-trained Models

The project uses pre-processed data from the ImageNet dataset for evaluating the attacks[cite: 3]. The notebook includes code to automatically download the necessary dataset samples and pre-trained model checkpoints (e.g., pre-trained patches)[cite: 3].

*   **Dataset:** A small subset of ImageNet (5 images for each of the 1000 labels) is used for fair evaluation[cite: 3].
*   **Models:** By default, a pre-trained ResNet34 model from `torchvision.models` is utilized[cite: 3].

## 📊 Visualizations

The project includes functionality to visualize the predictions of the model, showing the original image alongside the adversarial example and the applied noise perturbation[cite: 3]. It also provides bar charts displaying the confidence of the top-k predictions before and after the attack[cite: 3].

## 📚 Acknowledgments

*   The concepts and examples in this project draw inspiration from foundational papers in adversarial machine learning, such as Goodfellow et al. (2014) and J.H. Metzen et al. (2017)[cite: 3].
