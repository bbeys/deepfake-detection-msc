# Deepfake Detection MSc Project

**Evaluating the Reliability of Deepfake Detection Models Against Modern AI-Generated Identity Images**

Beyza Saglam - MSc Computing, University of Roehampton

---

## Overview

This repository contains the Google Colaboratory notebook for the experimental component of my MSc Computing dissertation. The experiment evaluates four CNN-based deepfake detection models trained on FaceForensics++ and tested across three generalisation conditions, including JPEG compression simulation.


---

## Models

- XceptionNet
- EfficientNet-B4
- ResNet50
- DenseNet121

---

## Datasets

| Dataset | Purpose |
|---------|---------|
| FaceForensics++ | Training + within-dataset evaluation |
| CelebDF-v2 | Cross-dataset evaluation |
| GenImage (Stable Diffusion v1.4) | Cross-generation evaluation |

---

## Experiment Pipeline

1. Dataset acquisition and frame extraction
2. Model training on FaceForensics++ (10 epochs, Adam optimiser, ImageNet pretrained weights)
3. Evaluation across three conditions (within-dataset, cross-dataset, cross-generation)
4. JPEG compression simulation (q=90, q=70, q=50, q=30)
5. Results visualisation (Figures 3-14)

---

## Requirements

- Google Colaboratory (T4 GPU)
- PyTorch
- timm
- scikit-learn
- OpenCV
- matplotlib / seaborn

---

## Results Summary 

| Model | FF++ (Within) | CelebDF (Cross) | GenImage (Cross-Gen) |
|-------|--------------|-----------------|----------------------|
| XceptionNet | 0.642 | 0.589 | 0.495 |
| EfficientNet-B4 | 0.552 | 0.507 | 0.575 |
| ResNet50 | 0.706 | 0.524 | 0.488 |
| DenseNet121 | 0.748 | 0.571 | 0.527 |



---


## Repository Structure

```
deepfake-detection-msc/
├── deepfake_detection_experiment.ipynb  # Main experiment notebook
└── README.md  #Project documentation
```