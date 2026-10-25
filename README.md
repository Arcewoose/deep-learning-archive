# Applied Deep Learning & Computer Vision Engineering Repository

This repository contains research implementations, benchmark experiments, and domain-specific engineering projects across Computer Vision, Deep Tabular Learning, NLP, and Recommendation Systems.

<p align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch" />
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow" />
  <img src="https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white" alt="Keras" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-Learn" />
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy" />
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
</p>

---

## Program Introduction

<div align="center">
  <a href="https://sesac.seoul.kr/">
    <img src="https://sesac.seoul.kr/static/img/sub/img_pursue_01.png" width="600" alt="Seoul Software Academy (SeSAC)" />
  </a>
  <p><b>Seoul Software Academy (SeSAC / 서울청년취업사관학교)</b></p>
</div>

- **Affiliation**: Supported by Seoul Metropolitan Government and Seoul Business Agency (SBA).
- **Official Website**: [https://sesac.seoul.kr/](https://sesac.seoul.kr/)
- **Curriculum Scope**: Intensive training program focused on Deep Learning pipeline engineering, Computer Vision architectures, Machine Learning optimization, and production deployment workflows.

---

## Featured Projects

### 1. [Satellite Multispectral Volcanic Eruption Detection](projects/module_01_volcano_classification/)
- **Objective**: On-board automated eruption detection from multispectral satellite imagery under extreme class imbalance.
- **Key Challenges**: Imbalanced dataset (260 eruption vs. 1,500 non-eruption instances).
- **Methods**:
  - Custom 7-layer CNN backbone combined with Global Average Pooling (GAP) to reduce parameter overhead.
  - Class-weighted oversampling and augmentation pipeline (`ai4eo.preprocessing`).
- **Results**: Achieved **85.0% classification accuracy** on test set with 0.5 decision thresholding.

### 2. [Deep Neural Architectures for Tabular Classification](projects/module_02_diabetes_classification/)
- **Objective**: Surpass tree-based baseline (XGBoost) on tabular benchmark data (Pima Indians Diabetes dataset).
- **Methods**:
  - **Tabular-to-Tensor Transformation**: Mapped structured feature vectors into multi-channel tensor structures (`[batch_size, channels, 32, 32]`) to leverage CNN inductive bias.
  - **Feature Stretching**: Min-max normalization scaled to $[-1, 1]$ interval.
  - **Optimization**: Systematic Grid Search, Cosine Annealing learning rate schedule, and customized FC layers.
- **Results**: Reached **84.38% accuracy**, outperforming standard ResNet adaptations and the XGBoost baseline.

---

## Repository Layout

```text
├── projects/
│   ├── module_01_volcano_classification/   # Satellite multispectral CV project
│   └── module_02_diabetes_classification/  # Tabular deep learning & optimization
├── notebooks/
│   ├── cv/                                 # YOLO detection, transfer learning
│   ├── nlp/                                # BERT sentiment & comment analysis
│   └── recsys/                             # Matrix factorization & SVD engines
├── assignments/                            # Selected technical task reports
└── daily_lectures/                         # Progressive implementation logs (Dec - Mar)
```

---

## Core Competencies & Toolstack

- **Computer Vision**: CNN backbones, Object Detection (YOLO), Satellite/Multispectral preprocessing, Transfer Learning.
- **Deep Tabular Modeling**: Feature embedding, tensor mapping, hyperparameter optimization.
- **NLP & RecSys**: BERT fine-tuning, Tokenization, Latent Factor SVD recommendation.
