# 🧪 Experimental and Machine Learning-Based Prediction of Properties in Bi Off-Stoichiometric NBT–7BT Ceramics

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-DeepLearning-orange)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-green)
![Domain](https://img.shields.io/badge/Domain-Electroceramics-purple)
![Status](https://img.shields.io/badge/Status-Active-success)

This repository contains the complete **experimental + machine learning (ML) + deep learning (DL) workflow** for studying and predicting the **structural, dielectric, ferroelectric, and piezoelectric properties of Bi off-stoichiometric NBT–7BT ceramics**.

**Author:** Srishty Mangutte  
**Department:** Ceramic Engineering, NIT Rourkela  
**Guide:** Prof. Anupam Mishra

---

## 📌 Project Overview

Lead-free piezoelectric ceramics such as **NBT–BT (Na₀.₅Bi₀.₅TiO₃–BaTiO₃)** are promising alternatives to lead-based materials. However, **Bi volatility during high-temperature sintering leads to A-site off-stoichiometry**, which strongly affects:

- Crystal structure
- Microstructure
- Dielectric behavior
- Ferroelectric response
- Piezoelectric performance

To **reduce experimental trial-and-error**, this project integrates:

- **Experimental electroceramics characterization**
- **Machine Learning for composition → property prediction**
- **Deep Learning for SEM microstructure → grain size prediction**

---

## 🏗️ System Architecture

**Pipeline:**

1. Experimental synthesis of Bi-deficient & stoichiometric NBT–7BT
2. Structural & electrical characterization
3. Data extraction from plots and SEM images
4. ML model training for property prediction
5. DL model training for microstructure-based grain size prediction

---

## 🧫 Experimental Work

The following experimental techniques are used:

- **XRD** → Phase identification and structural analysis
- **SEM** → Microstructure & grain size analysis
- **Archimedes Method** → Density & porosity
- **LCR Meter** → Dielectric measurements
- **Ferroelectric Loop Tracer** → P–E hysteresis loops
- **Strain Measurement System** → S–E butterfly loops
- **Piezometer** → d₃₃ measurement

> Add these images here:
> images/xrd_pattern.png
> images/sem_microstructure.png
> images/dielectric_vs_temp.png
> images/pe_loop.png
> images/se_butterfly_loop.png

---

## 🤖 Machine Learning Model – Property Prediction

### Objective

Predict the following properties:

- d₃₃
- Dielectric constant (εᵣ)
- Coercive field (E𝒸)
- Grain size

### Input Features

- SEM images
- Bi off-stoichiometry (Biₓ)
- Ba content
- Sintering temperature
- Bulk density

### Model Details

- Algorithm: **Random Forest Regressor**
- Framework: **Scikit-learn**
- Data Split: **80% Training / 20% Testing**
- Evaluation Metrics: **R², MAE, RMSE**

> Add ML output plots here:
> images/ml_true_vs_predicted.png
> images/ml_feature_importance.png
> images/ml_error_plot.png

---

## 🧠 Deep Learning Model – SEM Image → Grain Size

### Objective

Predict **average grain size directly from SEM microstructure images**.

### Dataset

- 2–3 SEM images per experimental sample
- Grain size labels extracted from Excel data (mean of `Length` column)

### Model Details

- Framework: **TensorFlow (Keras API)**
- Architecture: **ResNet-50**
- Training: **Transfer learning with fine-tuning**
- Optimizer: **Adam**
- Loss Function: **Mean Squared Error (MSE)**

> Add DL images here:
> images/sem_sample.png
> images/dl_training_loss.png
> images/dl_true_vs_predicted.png

---

## ⚙️ Setup Instructions

```bash
git clone <your-repo-link>
cd <repo-name>
pip install -r requirements.txt

```

### Run DL notebook:

jupyter notebook notebooks/dl_sem_grain_size_prediction.ipynb

## 📊 Key Outcomes

- ML successfully predicts electromechanical properties from composition.

- DL model estimates grain size directly from SEM images.

- Integration of ML + DL reduces experimental trial cycles.

- Demonstrates data-driven electroceramics design.

## 📚 Data Source & Credibility

- Experimental data obtained from NBT–7BT Bi off-stoichiometric ceramic synthesis and characterization under Prof. Anupam Mishra.

- Grain size labels extracted from experimental SEM image analysis.

- ML datasets constructed using:

- Experimental trends

- Peer-reviewed electroceramics literature ranges

- ML and DL models are used as proof-of-concept predictive tools.
