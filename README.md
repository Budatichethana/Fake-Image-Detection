# AI Generated Image Detection Using Deep Learning

## 📌 Project Overview

This project focuses on detecting **AI-generated and Deepfake images** using multiple deep learning architectures and feature fusion techniques.

The objective is to compare different CNN architectures and evaluate their effectiveness in distinguishing **Real Images** from **AI Generated Images**.

---

## 🚀 Models Implemented

### 1️⃣ ResNet50
- Pretrained on ImageNet
- Used as deep feature extractor
- Extracted 2048-dimensional feature vectors

### 2️⃣ EfficientNet-B3
- Efficient CNN architecture
- Better parameter utilization
- Captures texture and structural information

### 3️⃣ ConvNeXt
- Modern CNN architecture
- Inspired by Vision Transformer design
- Achieved the best overall performance

### 4️⃣ Fusion Model
- Combines ResNet50 and EfficientNet-B3 features
- Produces richer feature representation
- Improves classification performance

---

## 📂 Datasets Used

### Dataset 1: AI Generated Images vs Real Images

🔗 Dataset Link:

https://www.kaggle.com/datasets/cashbowman/ai-generated-images-vs-real-images

**Description**
- Real Images
- AI Generated Images
- Used for benchmarking deep learning models

#### Structure

```text
train/
├── real/
└── fake/

test/
├── real/
└── fake/
```

### Dataset 2: CIFAKE Dataset

🔗 Dataset Link:

https://www.kaggle.com/datasets/birdy654/cifake-real-and-ai-generated-synthetic-images

**Description**
- REAL images
- FAKE images
- More challenging due to blur and compression artifacts

#### Structure

```text
train/
├── REAL/
└── FAKE/

test/
├── REAL/
└── FAKE/
```


## ⚙️ Methodology

### Image Preprocessing
- Image resizing
- Normalization
- Patch extraction

### Handcrafted Features
- GLCM Features
- LBP Features
- FFT Features

### Deep Features
- ResNet50
- EfficientNet-B3
- ConvNeXt

### Classification
- XGBoost Classifier

### Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1 Score
- AUC Score

## 🧪 Experimental Setup

| Parameter | Value |
|------------|---------|
| Image Size | 224 × 224 |
| Deep Models | ResNet50, EfficientNet-B3, ConvNeXt |
| Classifier | XGBoost |
| Framework | PyTorch |
| Metrics | Accuracy, Precision, Recall, F1, AUC |
| Platform | Kaggle Notebook |

---

## 📊 Results Summary

### AI Generated Images vs Real Images Dataset

| Model | AUC |
|--------|------|
| ResNet50 | 0.95 |
| EfficientNet-B3 | 0.94 |
| ConvNeXt | 0.98 |
| Fusion | 0.97 |

### CIFAKE Dataset

| Model | AUC |
|--------|------|
| ResNet50 | 0.83 |
| EfficientNet-B3 | 0.86 |
| Fusion | 0.90 |
| ConvNeXt | 0.97 |

---

## 🔍 Key Observations

- ConvNeXt achieved the highest AUC across both datasets.
- Fusion outperformed individual ResNet50 and EfficientNet-B3 models.
- Dataset quality significantly affects model performance.
- Compression and blur artifacts reduce detection accuracy.

---

## 🎯 Explainability

Grad-CAM was used to visualize image regions influencing model predictions.

### Benefits
- Improves interpretability
- Highlights important regions
- Validates learned features

---

## 🔮 Future Work

- End-to-end ConvNeXt training
- Larger datasets
- Improved feature fusion
- Ensemble learning
- Real-time deepfake detection
- Explainable AI techniques

---

## 📁 Repository Structure

```text
Fake-Image-Detection/
│
├── resnet50.ipynb
├── resnet50-deep.ipynb
├── efficientnet-b3.ipynb
├── efficientnet-b3-deep.ipynb
├── convnext.ipynb
├── convnext-deep.ipynb
├── fusion.ipynb
├── fusion-deep.ipynb
└── README.md
```

---

## Acknowledgements

- PyTorch
- XGBoost
- OpenCV
- Scikit-Learn
- Kaggle Datasets
- ImageNet Pretrained Models
