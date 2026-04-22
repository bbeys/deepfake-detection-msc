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

## Results Summary (v6 baseline)

| Model | FF++ (Within) | CelebDF (Cross) | GenImage (Cross-Gen) |
|-------|--------------|-----------------|----------------------|
| XceptionNet | 0.652 | 0.593 | 0.493 |
| EfficientNet-B4 | 0.557 | 0.499 | 0.493 |
| ResNet50 | 0.705 | 0.567 | 0.487 |
| DenseNet121 | 0.748 | 0.553 | 0.527 |



---


## Repository Structure

```
deepfake-detection-msc/
├── deepfake_detection_experiment.ipynb  # Main experiment notebook
└── README.md  #Project documentation
```