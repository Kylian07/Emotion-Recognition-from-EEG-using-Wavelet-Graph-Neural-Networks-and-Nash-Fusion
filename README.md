# 🧠 Emotion Recognition from EEG using Wavelet Graph Neural Networks and Nash Fusion  

[![Conference](https://img.shields.io/badge/Conference-IEEE%20ICME%20Workshop%202025-blue.svg)](https://www.ieee.org/)

📄 **Accepted at ICME Workshop:**  
**Embodied Multimedia: When Multimodal Signal Processing Meets Embodied Intelligence**

---

## 📝 Overview  

This repository contains the **official PyTorch implementation** of our paper:

**Emotion Recognition from EEG Signals using Wavelet Graph Convolutions and Nash Bargaining-based Feature Fusion**

We propose a **novel dual-branch Graph Neural Network (GNN)** framework for EEG-based emotion recognition that jointly models:

- **Localized frequency dynamics** using wavelet-based graph convolutions  
- **Global spatial dependencies** using Graph Convolutional Networks (GCN)  

To effectively integrate these complementary representations, we introduce a **Nash Bargaining-based Fusion mechanism**, inspired by **game theory**, enabling adaptive and context-aware feature fusion.

The proposed approach achieves **state-of-the-art performance across multiple EEG datasets**, demonstrating strong generalization and robustness.

---

## 🚀 Key Contributions  

- Dual-branch **Wavelet + Spatial GNN architecture**  
- Novel **Haar Wavelet Graph Convolution** for frequency-aware feature extraction  
- **Nash Bargaining-based Fusion** for adaptive embedding integration  
- End-to-end framework for **graph-based EEG modeling**  
- State-of-the-art results on multiple benchmark datasets  

---

## 🏗️ Model Architecture  

<p align="center">
  <img src="assets/model_architecture.png" alt="Model Architecture" width="700"/>
</p>

The architecture consists of two parallel branches:

- **Wavelet GNN Branch** → captures fine-grained temporal-frequency variations  
- **Spatial GCN Branch** → models inter-channel relationships  

These are fused using **Nash Bargaining Fusion**, followed by global pooling and classification.

---

## 🧠 Nash Bargaining-based Fusion  

We introduce a **game-theoretic fusion strategy** inspired by the **Nash Bargaining Solution**:

- Compute **Cosine Similarity** between embeddings  
- Adaptive fusion:
  - ✔ High agreement → **Geometric Mean (cooperative fusion)**  
  - ✔ Low agreement → **Arithmetic Mean (fallback strategy)**  

This ensures:
- Preservation of **complementary information**  
- Suppression of noisy or conflicting features  
- Robust and stable feature representation  

<p align="center">
  <img src="assets/fusion_flow.png" alt="Fusion Flow" width="650"/>
</p>

---

## 📂 Datasets  

We evaluate our model on **four benchmark EEG datasets**:

### 🔹 SEED  
- 62-channel EEG recordings  
- Emotion classes: Positive, Neutral, Negative  

### 🔹 WESAD  
- Multimodal physiological dataset  
- Stress and affect detection  

### 🔹 SWELL  
- Office stress dataset  
- Multi-sensor physiological signals  

### 🔹 Brainwave EEG  
- Frequency-band based EEG signals  
- Delta, Theta, Alpha, Beta, Gamma bands  

---

## 📈 Performance  

| Dataset        | Accuracy |
|---------------|---------|
| SEED          | **99.99%** |
| WESAD         | **99.99%** |
| SWELL         | **99.99%** |
| Brainwave EEG | **99.00%** |

✔ Consistent **near-perfect performance** across datasets  
✔ Strong **generalization across modalities**  

---

## 🔬 Ablation Study  

| Configuration                         | Accuracy |
|--------------------------------------|---------|
| Spatial GCN                          | Low–Moderate |
| Wavelet GNN                          | High |
| Combined (No Fusion)                 | Improved |
| + Nash Fusion (Proposed)             | **Best (≥99.9%)** |

👉 Demonstrates the **critical role of Nash Fusion** in boosting performance  

---

## ⚙️ Experimental Setup  

- Framework: **PyTorch**  
- GPU: **NVIDIA Tesla T4**  
- Epochs: **150**  
- Batch Size: **8**  
- Learning Rate: **0.01**  
- Optimizer: **Adam**  

---

## 📊 Visualization  

<p align="center">
  <img src="assets/saliency_maps.png" alt="Saliency Maps" width="700"/>
</p>

Saliency maps highlight **important EEG channels**, showing how the model focuses on discriminative brain regions across datasets.

---

## ✍️ Authors  

- **Rajdeep Pal** – Department of Artificial Intelligence and Machine Learning, St. Thomas College of Engineering and Technology, India  
- *(Add co-authors here if needed)*  

---

## ⚠️ Disclaimer  

This repository is released for **academic research purposes only**.

- Not intended for **clinical or medical diagnosis**  
- Results depend on **dataset-specific characteristics**  
- Real-world deployment requires **extensive validation**  

---

## 📄 Paper  

📌 *Emotion Recognition from EEG Signals using Wavelet Graph Convolutions and Nash Bargaining-based Feature Fusion*  

(Add PDF / arXiv link here)

---

## ⭐ Citation  

