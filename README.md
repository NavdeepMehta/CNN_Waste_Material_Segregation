# 🧠 CNN Waste Material Segregation

A Convolutional Neural Network (CNN)-based image classification project that categorizes waste into **7 distinct classes**:  
**Cardboard, Food Waste, Glass, Metal, Paper, Plastic, Other**.

---

## 📌 Project Overview

This project addresses the challenge of classifying real-world waste images using a custom-built CNN trained on images of size **128×128×3**. The goal is to aid efficient waste sorting and recycling processes by automating the recognition of different waste types.

The dataset is **highly imbalanced**, with *Plastic* being the most frequent and *Cardboard* the least. To overcome this, **real-time data augmentation** was applied to enrich the dataset and improve model generalization.

---

## 🧰 Tech Stack

- **Language**: Python  
- **Libraries**: TensorFlow, Keras, NumPy, Matplotlib, scikit-learn  
- **Model Type**: CNN (built using Keras Sequential API)

---

## 📁 Dataset Details

- Images resized to: `128x128x3`  
- Class labels extracted from folder names  
- Classes:  
  `['Cardboard', 'Food Waste', 'Glass', 'Metal', 'Paper', 'Plastic', 'Other']`

---

## ⚙️ Model Architecture

- **Convolutional Layers**: 3 layers with ReLU activation
- **Normalization**: BatchNormalization
- **Regularization**: Dropout
- **Output**: Softmax activation (multi-class classification)
- **Loss Function**: Categorical Crossentropy
- **Optimizer**: Adam

---

## 🔄 Data Augmentation

Applied using `ImageDataGenerator`:

- Rotation
- Width/Height Shift
- Shearing
- Zooming
- Horizontal Flipping

---

## 📊 Performance Metrics

| Metric              | Result (Post-Augmentation) |
|---------------------|----------------------------|
| Training Accuracy   | ~95%                        |
| Validation Accuracy | Improved from ~64% to ~69% |

Also evaluated using:

- Precision, Recall, F1-Score
- Confusion Matrix

---

## 🚧 Challenges & Solutions

- **Problem**: Severe class imbalance  
  **Solution**: Data augmentation and plans for class weighting or oversampling

- **Problem**: Visually similar classes (e.g., Plastic vs. Food Waste)  
  **Solution**: Regularization, and exploration of more advanced models

---

## 🔮 Future Work

- Integrate **transfer learning** (e.g., ResNet, MobileNet)
- Apply **class weighting** or **SMOTE-based oversampling**
- Experiment with **focal loss** to improve handling of hard examples
- Use **AutoAugment** for optimized augmentation strategies

---

## 🧪 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/CNN_Waste_Material_Segregation.git
   cd CNN_Waste_Material_Segregation