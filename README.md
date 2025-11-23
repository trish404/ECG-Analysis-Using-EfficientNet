# 🩺 ECG Diagnostic AI  
Deep Learning-Based Myocardial Infarction Detection with Explainability  

> Research implementation for the paper:  
> **ECG Analysis for Myocardial Infarction Detection via Deep Learning**  
> 📄 Procedia Computer Science, International Conference on Machine Learning and Data Engineering, 2025  
> :contentReference[oaicite:0]{index=0}  

---

## 🔍 Project Overview

This repository contains a complete implementation of an explainable deep learning system designed to detect **Myocardial Infarction (MI)** and related cardiac abnormalities using ECG images. The system leverages:

- 🧠 **EfficientNet-B0 enhanced with Multi-Scale Attention (MSA)**
- 📊 **4-class ECG image classification**
- 🧬 **Explainable AI integration (Grad-CAM, Integrated Gradients)**
- 🖥 **Streamlit web interface for real-time diagnosis**

The model demonstrates strong performance with:  

| Metric | Result |
|--------|--------|
| **Accuracy** | **96%** |
| Precision | 94% |
| Recall | 97% |
| F1-Score | 0.95 |

---

## 📂 Dataset

Dataset used:

> **ECG Images Dataset of Cardiac Patients (Kaggle)**  
> 3,951 labeled ECG images across 4 diagnostic categories.  
:contentReference[oaicite:1]{index=1}

Classes include:

- Normal  
- Abnormal Heartbeat  
- History of MI  
- Myocardial Infarction (MI)

---

## 🏗 Methodology

Pipeline Summary:

ECG Image Input → Preprocessing → EfficientNet-B0 + MSA → Explainability → Diagnosis UI

Key components include:

- Preprocessing (224x224 resize, normalization, class encoding)
- Baseline model benchmarking (CNN, MobileNet, ResNet50, DenseNet121, ConvNeXt-Tiny)
- Final proposed architecture: **EfficientNet-B0 + Multi-Scale Attention**
- Explainability: Grad-CAM + Integrated Gradients + Textual reasoning
- Deployment: Streamlit UI with secure login and image upload  

---

## 🚀 Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/ECG-Analysis-Using-EfficientNet.git
cd ECG-Analysis-Using-EfficientNet
```
### 2️⃣ Install dependencies
``` bash

pip install -r requirements.txt
```

(For best performance, enable CUDA GPU acceleration if available.)
### 3️⃣ Launch the interface
```bash
streamlit run app.py

```
---
##🧪 Training Details
Setting	Configuration
Epochs	50 (with Early Stopping)
Batch Size	32
Optimizer	Adam
Learning Rate	1e-4
Loss	Weighted Cross-Entropy
Regularization	Dropout 0.3 + Weight Decay

Training was performed using GPU with mixed precision for efficiency.

---
## Baseline Model Performance
| Model                               | Accuracy  |
| ----------------------------------- | --------- |
| MobileNet                           | 48%       |
| ResNet-50                           | 68%       |
| DenseNet121                         | 90%       |
| **Proposed: EfficientNet-B0 + MSA** | ⭐ **96%** |
---
### 🧠 Explainability Support

The system generates:

🔥 Grad-CAM heatmaps

🌈 Integrated Gradients contribution maps

📝 Rule-based textual interpretations

These outputs validate whether the model attends to clinically relevant waveform segments like ST elevation, Q wave depth, or T-wave inversion.

### Citation
ECG Analysis for Myocardial Infarction Detection via Deep Learning. 
Procedia Computer Science — International Conference on Machine Learning and Data Engineering.
