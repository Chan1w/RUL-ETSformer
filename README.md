# 🚀 RUL-Prediction  
## Exponential Transformer for Interpretable Remaining Useful Life Prediction of Lithium-Ion Batteries

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)]()
[![PyTorch](https://img.shields.io/badge/PyTorch-1.10+-red.svg)]()
[![IEEE TTE](https://img.shields.io/badge/Published-IEEE%20Transactions%20on%20Transportation%20Electrification-005BAC.svg)]()
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()

---

## 📖 Paper

**An Exponential Transformer for Learning Interpretable Temporal Information in Remaining Useful Life Prediction of Lithium-Ion Battery**

Chenhan Wang, Zhengyi Bao, Huipin Lin, Zhiwei He, Mingyu Gao  

Published in **IEEE Transactions on Transportation Electrification (TTE), 2025**  
DOI: 10.1109/TTE.2025.3534146  

This repository provides the official implementation of the proposed **Exponential Transformer (ETSformer)** for lithium-ion battery Remaining Useful Life (RUL) prediction.

---

## 🔬 Background & Motivation

Accurate RUL prediction is essential for:

- Electric vehicle safety assurance  
- Intelligent battery health management  
- Predictive maintenance planning  

Although Transformer-based architectures demonstrate strong sequence modeling capabilities, their application in battery RUL prediction faces three key challenges:

1. Lack of interpretable temporal decomposition  
2. Underutilization of degradation trend information  
3. High computational cost in long-sequence prediction  

Battery capacity degradation exhibits:

- Long-term monotonic decline (trend component)
- Short-term regeneration and fluctuation patterns
- Strong temporal dependency structure

Conventional self-attention mechanisms fail to explicitly separate and interpret these characteristics.

---

## 🧠 Proposed Method: Exponential Transformer (ETSformer)

The proposed framework integrates interpretable decomposition with an efficient attention mechanism.

### 1️⃣ Interpretable Temporal Decomposition

The raw capacity sequence is decomposed into:

- **Level Component** – representing long-term degradation trend  
- **Fluctuation Component** – representing short-term dynamic variations  

This decomposition enables interpretable feature extraction and improves RUL learning stability.

### 2️⃣ Exponential Attention Mechanism

Standard self-attention is replaced with **Exponential Attention**, which:

- Introduces exponential decay weighting
- Emphasizes temporally relevant features
- Suppresses irrelevant long-distance interactions
- Reduces computational redundancy
- Enhances both efficiency and prediction accuracy

Mathematically, similarity weights are modulated through exponential decay based on temporal distance, allowing the model to better capture degradation continuity.

### 3️⃣ Unified Prediction Framework

The network supports:

- Single-step RUL prediction
- Multi-step RUL forecasting
- Robust generalization across aging datasets

---
## 💻 Environment
- torch==2.0.0+cu118
- numpy==1.22.4
- pandas==1.4.2
- matplotlib==3.6.0

```
pip install -r requirement.txt
```

---

## 🏃 Training & Testing
```
python main.py
```
---

##  📌 Citation
If you find ETSformer useful, please consider citing:
```javascript
@ARTICLE{wang2025exponential,
  author={Wang, Chenhan and Bao, Zhengyi and Lin, Huipin and He, Zhiwei and Gao, Mingyu},
  journal={IEEE Transactions on Transportation Electrification}, 
  title={An Exponential Transformer for Learning Interpretable Temporal Information in Remaining Useful Life Prediction of Lithium-Ion Battery}, 
  year={2025},
  pages={1-12},
  doi={10.1109/TTE.2025.3534146}
}
```
