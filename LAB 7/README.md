# 🎨 Neural Style Transfer (NST)

> **Course:** CSET419 – Introduction to Generative AI  
> **Lab 7 Implementation using VGG19**

---

## 📌 Project Overview

This project implements **Neural Style Transfer (NST)** using a pretrained VGG19 convolutional neural network.

The goal is to generate a new image by combining:

- 🖼 **Content** from one image  
- 🎨 **Style** from another image  

The model extracts deep features from both images and optimizes a new image that preserves content structure while transferring artistic texture.

---

## 🎯 Objectives

- Load one content image and one style image  
- Use pretrained VGG19 (weights frozen)  
- Extract content and style features  
- Define content loss and style loss  
- Combine them into total loss  
- Optimize image pixels to generate stylized output  

---

## 🧠 How Neural Style Transfer Works

### 1️⃣ Feature Extraction

We use pretrained **VGG19** (trained on ImageNet) as a feature extractor.

- **Content Layer:** `conv4_2`
- **Style Layers:**
  - `conv1_1`
  - `conv2_1`
  - `conv3_1`
  - `conv4_1`
  - `conv5_1`

---

### 2️⃣ Content Loss

Measures structural similarity between:

- Generated image features  
- Content image features  

Implemented using **Mean Squared Error (MSE)**.

---

### 3️⃣ Style Loss

Style is represented using a **Gram Matrix**, which captures correlations between feature maps.

Style Loss = MSE(Gram_generated, Gram_style)

---

### 4️⃣ Total Loss

Total Loss = (Content Weight × Content Loss) + (Style Weight × Style Loss)

- Content Weight = `1e4`
- Style Weight = `1e2`

These weights control the balance between structure preservation and artistic transformation.

---

## ⚙️ Implementation Details

| Component        | Value |
|------------------|--------|
| Framework        | PyTorch |
| Model            | VGG19 (Pretrained) |
| Optimizer        | Adam |
| Iterations       | 2000 |
| Device           | GPU / CPU |

---

## 📊 Results

The generated image:

- ✅ Preserves content structure  
- ✅ Transfers artistic texture  
- ✅ Produces visually stylized output  

A side-by-side comparison includes:

- Content Image  
- Style Image  
- Stylized Output  

---

### image output
<img width="1656" height="597" alt="Screenshot 2026-03-01 132023" src="https://github.com/user-attachments/assets/5f6069c8-bf30-4355-b256-7191e9ecf240" />

## 🚀 How to Run

```bash
git clone <repo-url>
cd <repo-name>
pip install torch torchvision matplotlib pillow
jupyter notebook


