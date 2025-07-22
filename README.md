# 🍽️ Food-101 Image Classification using EfficientNetB0

This project implements an image classification pipeline on the [Food-101 dataset](https://www.tensorflow.org/datasets/catalog/food101) using transfer learning with **EfficientNetB0** in TensorFlow and Keras. The model is fine-tuned to achieve over **78% accuracy** on the validation set.

---

## 📚 About the Dataset

The [Food-101](https://data.vision.ee.ethz.ch/cvl/datasets_extra/food-101/) dataset consists of:

- **101 food categories**
- **101,000 images total**  
  - 75,750 training images  
  - 25,250 testing images  

📝 **Original Research Paper**:  
Bossard, Lukas, Matthieu Guillaumin, and Luc Van Gool.  
**"Food-101 – Mining Discriminative Components with Random Forests"**, ECCV 2014.  
[Read it here](https://link.springer.com/chapter/10.1007/978-3-319-10599-4_29)

---

## 🧠 Model Overview

- **Base model**: `EfficientNetB0` (pretrained on ImageNet)
- **Training Strategy**:
  - Phase 1: Feature extraction (top layers only)
  - Phase 2: Fine-tuning (unfreezing bottom layers)
- **Additional Techniques**:
  - Data augmentation
  - Learning rate tuning
  - TensorBoard for training visualization
  - Checkpointing best model

---

## 📈 Results

| Phase          | Accuracy |
|----------------|----------|
| Feature Extraction | ~74%     |
| Fine-tuned (15 layers, LR = 5e-5) | **~78%**     |

---

## 📊 Visualizations

- Class-wise prediction distribution using **Seaborn**
- Manual test accuracy calculation with custom loops

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/food101-efficientnet.git
   cd food101-efficientnet
