# 🌀 Mini Diffusion Model for Text-to-MNIST Generation

A lightweight diffusion model that generates **MNIST digits** (0–9) from **text prompts** like `"zero"`, `"one"`, etc.  
Built with **PyTorch**, optimized for **Google Colab (CPU/GPU T4)**.

---

## 🚀 Overview

This project implements a **Mini Diffusion Model** (DDPM-style) that learns to generate handwritten MNIST digits conditioned on text labels.  
It’s designed for simplicity, clarity, and full trainability within **10–15 minutes on a Colab T4 GPU**.

---

## ✨ Key Features

### 📊 Architecture
- **Mini U-Net** with encoder–decoder structure  
- **Sinusoidal position embeddings** for timestep encoding  
- **Text conditioning** via one-hot vectors (digits 0–9)  
- **Skip connections** for stable training and better gradient flow  

### 🔧 Training
- **Forward Diffusion:** Linear noise schedule (β from `1e-4` → `0.02`)  
- **1000 diffusion timesteps**  
- **Loss:** Mean Squared Error (MSE) between predicted and true noise  
- **Optimizer:** Adam  
- **Fully Colab-optimized** (runs on CPU or T4 GPU)

### 🎯 Sampling
- **Reverse diffusion** using DDPM formulation  
- Generate digits directly from text prompts like `"seven"` or `"three"`  
- **Iterative denoising** across 1000 steps for each sample  

---

## 🧠 What It Does
✅ Loads and preprocesses MNIST dataset  
✅ Creates mappings between text labels and digit indices  
✅ Implements forward diffusion (adds noise progressively)  
✅ Trains U-Net to predict the added noise  
✅ Uses reverse diffusion to generate clean samples  
✅ Visualizes generated digits and training loss curves  
✅ Saves the trained model  

---

## 💻 Usage (in Google Colab)

```python
# Clone or upload your script to Colab and run all cells.
```
---
(kid like notebook just run it .. its too easy)
