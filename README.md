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

### Images here:


  
<img src="https://github.com/user-attachments/assets/bd1cd0ec-4d63-487f-8772-8cd8c809656a" width="48%"/>

 <img src="https://github.com/user-attachments/assets/7cf9c136-310c-4696-8804-47f694eab8f2" width="48%"/>
<br/>


<table>
<tr>
<td> <img src="https://github.com/user-attachments/assets/ba47cc15-fa30-4783-982d-0fcc1e84c6e3"/> </td>

<td> <img src="https://github.com/user-attachments/assets/dbb17ce2-c6a7-4da6-bc83-eac7379e3c95"/> </td>

<td> <img src="https://github.com/user-attachments/assets/e72e9451-4c29-4c28-b0cc-f0fe383e0173"/> </td>
</tr>
</table>

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

> ML output plots:
<img width="65%" alt="Screenshot 2025-12-01 153727" src="https://github.com/user-attachments/assets/93fc6b10-1a76-4bc3-9a31-b1e230d38123" />

<img width="1832" height="763" alt="Screenshot 2025-12-01 153905" src="https://github.com/user-attachments/assets/f9031b4a-361f-4cf8-9424-f111725a40d5" />


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

> DL images:
<img width="1255" height="606" alt="Screenshot 2025-12-03 060559" src="https://github.com/user-attachments/assets/682b3118-0180-4571-b964-8491a063ba5f" />
<img width="514" height="605" alt="Screenshot 2025-12-03 055549" src="https://github.com/user-attachments/assets/8a08f0a8-6d35-42ee-966f-bfa4ce5acc89" />


<img width="370" height="150" alt="Screenshot 2025-12-03 061319" src="https://github.com/user-attachments/assets/5c085c56-b53a-45e2-adb4-5fd06492fa6d" />
<img width="352" height="118" alt="Screenshot 2025-12-03 061358" src="https://github.com/user-attachments/assets/a6bc1320-7272-4e76-82ec-f2392657d842" />

<img width="353" height="108" alt="Screenshot 2025-12-03 061527" src="https://github.com/user-attachments/assets/e6041d55-6439-4c2c-8683-9cce9a1b7d76" />
<img width="351" height="129" alt="Screenshot 2025-12-03 061647" src="https://github.com/user-attachments/assets/eb4bc595-0319-45c4-a224-505d85d5be92" />


---

## ⚙️ Setup Instructions

```bash
git clone https://github.com/Srish-ty/resnet-SEM-microstructure-predictor
cd resnet-SEM-microstructure-predictor
pip install -r requirements.txt

```

### Run DL notebook:

jupyter notebook notebooks/dl_sem_grain_size_prediction.ipynb

## 📊 Key Outcomes

- ML successfully predicts electromechanical properties from composition.

- DL model estimates grain size directly from SEM es.

- Integration of ML + DL reduces experimental trial cycles.

- Demonstrates data-driven electroceramics design.

## 📚 Data Source & Credibility

- Experimental data obtained from NBT–7BT Bi off-stoichiometric ceramic synthesis and characterization under Prof. Anupam Mishra.

- Grain size labels extracted from experimental SEM e analysis.

- ML datasets constructed using:

- Experimental trends

- Peer-reviewed electroceramics literature ranges

- ML and DL models are used as proof-of-concept predictive tools.
