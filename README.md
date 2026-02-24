# 🚀 RUL-Prediction (Exponential Transformer)

## An Exponential Transformer for Learning Interpretable Temporal Information in Remaining Useful Life Prediction of Lithium-Ion Batteries

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)]()
[![PyTorch](https://img.shields.io/badge/PyTorch-1.10+-red.svg)]()
[![License](https://img.shields.io/badge/License-MIT-green.svg)]()
[![IEEE TTE](https://img.shields.io/badge/Published-IEEE%20TTE-005BAC.svg)]()
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()

---

## 📖 Paper Information

**Title:**  
*An Exponential Transformer for Learning Interpretable Temporal Information in Remaining Useful Life Prediction of Lithium-Ion Battery*

**Journal:** IEEE Transactions on Transportation Electrification  
**Year:** 2025  
**DOI:** 10.1109/TTE.2025.3534146  

**Authors:**  
Chenhan Wang, Zhengyi Bao, Huipin Lin, Zhiwei He, Mingyu Gao

This repository provides the official implementation of the proposed **Exponential Transformer (ETSformer)** for battery Remaining Useful Life (RUL) prediction.

---

## 🧠 Motivation

Accurate RUL prediction of lithium-ion batteries is essential for:

- 🚗 Electric vehicle safety  
- 🔋 Battery health management  
- ⚡ Intelligent maintenance scheduling  

Although conventional Transformer architectures have demonstrated strong modeling capacity, they suffer from:

- ❌ Limited interpretability of temporal decomposition  
- ❌ Inability to explicitly model trend & fluctuation components  
- ❌ High computational overhead in long-sequence prediction  

---

## 🔬 Proposed Method

We introduce **Exponential Transformer (ETSformer)** to address these challenges.

### 🔹 1. Interpretable Time-Series Decomposition

The raw battery capacity sequence is decomposed into:

- **Level Component** (long-term degradation trend)
- **Fluctuation Component** (short-term variations)

This decomposition improves interpretability and enhances feature utilization.

---

### 🔹 2. Exponential Attention Mechanism

We replace standard self-attention with **Exponential Attention**, which:

- Applies exponential decay weighting
- Emphasizes temporally similar patterns
- Reduces irrelevant long-range interactions
- Improves both prediction accuracy and computational efficiency

---

### 🔹 3. Single-step & Multi-step Prediction Capability

The framework supports:

- One-step ahead prediction
- Multi-step forecasting
- Robust performance across different aging datasets

---

## 🏗 Model Architecture Overview

---

## 📊 Experimental Highlights

- ✔ Superior RUL prediction accuracy  
- ✔ Improved interpretability compared to standard Transformer  
- ✔ Efficient long-sequence modeling  
- ✔ Strong generalization across datasets  

---

## 📁 Project Structure

---

## ⚙️ Installation

### 1️⃣ Create Environment

```bash
conda create --name etsformer python=3.8
conda activate etsformer

pip install -r requirement.txt

python main.py

@ARTICLE{wang2025exponential,
  author={Wang, Chenhan and Bao, Zhengyi and Lin, Huipin and He, Zhiwei and Gao, Mingyu},
  journal={IEEE Transactions on Transportation Electrification}, 
  title={An Exponential Transformer for Learning Interpretable Temporal Information in Remaining Useful Life Prediction of Lithium-Ion Battery}, 
  year={2025},
  pages={1-12},
  doi={10.1109/TTE.2025.3534146}
}
