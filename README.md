# Boat_Image_Classification_Model
Added image classification notebook comparing scratch vs pretrained CNNs

# Boat Image Classification Project

This project explores image classification using **Convolutional Neural Networks (CNNs)** to identify boat types.  
Two models were trained and compared:
1. A **baseline model built from scratch**
2. A **transfer learning model using a pre-trained CNN (MobileNetV2)**

---

## Overview

The goal was to understand how starting from scratch compares to leveraging pre-trained knowledge on real-world image data.  
By analyzing both models’ learning behavior, we identified how pre-trained models can generalize better with less overfitting.

---

## Model 1 — Built from Scratch

- **Training Accuracy:** ~95%  
- **Validation Accuracy:** ~82%  
- **Observation:** The model learned fast but started memorizing training data early.  
- **Problem:** Overfitting after around 10 epochs, validation loss started rising.  
- **Fix:** Add data augmentation, batch normalization, and early stopping.

---

## Model 2 — Pre-trained CNN

- **Training Accuracy:** ~98%  
- **Validation Accuracy:** ~91%  
- **Observation:** Learned efficiently and generalized better.  
- **Behavior:** Validation loss remained stable, showing mild overfitting but strong generalization.  
- **Fix:** A bit of extra dropout and L2 regularization could help refine stability.

---

## Comparison

| Feature | From Scratch | Pre-trained |
|----------|---------------|-------------|
| Starting Point | Random weights | Pre-learned features |
| Training Speed | Slow | Fast |
| Accuracy | 82% (val) | 91% (val) |
| Overfitting | High | Mild |
| Generalization | Weak | Strong |
| Real-world Readiness | Low | High |

---

## Results Summary

The pre-trained model clearly outperformed the scratch model. It learned faster, generalized better, and stayed stable throughout training.  
It proves that **transfer learning is a practical, time-saving strategy** for image based tasks with limited data.

---

## Lessons Learned

- Don’t train from scratch unless you have huge data.  
- Early stopping and dropout save your model from memorizing.  
- Transfer learning gives better accuracy and faster convergence.  
- Regularization (L2) keeps your model grounded and fair.

---

## 🗂️ Repository Structure

