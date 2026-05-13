# Bayesian Optimization of Deep Neural Networks for Finger Movement Classification from ECoG

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Institution: IPN-ESCOM](https://img.shields.io/badge/Institution-IPN--ESCOM-maroon.svg)](https://www.escom.ipn.mx/)

Official implementation of the **Technical Work (Trabajo Terminal) No. 2026-B145** from **Escuela Superior de Cómputo (IPN)**. This project decodes kinematic finger flexion from Electrocorticography (ECoG) signals using a 1D U-Net architecture optimized via Bayesian inference.



## 🎯 Project Overview
This research addresses the non-linear relationship between cortical activity and motor execution. By analyzing the **BCI Competition IV - Dataset 4**, we developed a pipeline that overcomes the limitations of traditional linear models, which show near-zero correlation with raw ECoG signals.

## 📚 Scientific Foundations
Our architectural framework and signal processing standards are informed by the following pioneering works:

* **Wang et al. (DTCNet):** We utilize the concept of **Deep Temporal Convolutional Networks** to capture multi-scale temporal features.
    * *Ref:* [DTCNet: Deep Temporal Convolutional Network for finger movement decoding](https://doi.org/10.48550/arXiv.2211.01960).
* **Lomtev et al. (FingerFlex):** Our preprocessing pipeline follows the standards for **High-Gamma Activity (HGA)** extraction.
    * *Ref:* [FingerFlex: Inferring finger trajectories from ECoG signals](doi: 10.3389/fncom.2025.1627819).

## ⚡ Original Contribution: Bayesian AutoML
The core innovation of this thesis is the **Bayesian Optimization (BO)** engine, designed to solve subject-variability in BCI systems by automatically discovering optimal subject-specific configurations.
## Authors & Roles

* **Valencia525 (Valencia San Roman Joel):**
    * Lead developer of the 1D Autoencoder/U-Net deep learning framework.
    * Development of the neural decoding and training pipeline.
    * Collaborative work on signal analysis, optimization integration, and evaluation.

* **SaulRodas (Rodas Bautista Saul):**
    * Lead developer of the Bayesian Optimization engine.
    * Implementation of Gaussian Processes (GP) and Expected Improvement (EI) acquisition functions.
    * Collaborative work on signal processing and feature exploration.

### Collaborative Contributions (Both Authors)
* **Development of the signal processing and feature exploration pipeline**, inspired by state-of-the-art techniques, including Continuous Wavelet Transform (CWT) and spatial/spectral filtering techniques.
* **Integration of deep learning, optimization, and signal processing modules.**
* **Research design, experimentation, and performance evaluation** using BCI Competition IV – Dataset 4.

### 🎓 Directors
* **Dra. Miriam Pescador Rojas**
* **M.C. Miguel Abel León Hernández**

## 📊 Performance Summary (Baseline)
| Subject | Thumb | Index | Middle | Ring | Pinky | Average |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **S1** | 0.62 | 0.82 | 0.51 | 0.64 | 0.54 | **0.62** |
| **S2** | 0.69 | 0.52 | 0.55 | 0.60 | 0.64 | **0.60** |
| **S3** | 0.87 | 0.78 | 0.65 | 0.76 | 0.69 | **0.75** |

## 📂 Repository Structure
```text
├── src/
│   ├── preprocessing.ipynb    # Signal cleaning and Spectrogram generation
│   ├── model.ipynb            # U-Net 1D Architecture
│   └── optimization.ipynb     # Bayesian Optimization logic
├── requirements.txt        # Project dependencies
└── README.md
