# Human Activity Recognition (HAR) using CNN & MobileNetV2

A deep learning-based **Human Activity Recognition (HAR)** system that classifies human activities from video frames into three categories:

- 🏃 Running
- 🚶 Walking
- 🧍 Standing

The project uses **Convolutional Neural Network (CNN)** with **Transfer Learning** based on **MobileNetV2** for efficient human activity classification.

---

## 📌 Project Overview

Human Activity Recognition (HAR) is useful for intelligent surveillance, healthcare, human-computer interaction, and real-time monitoring.

In this project, video clips are converted into image frames and processed using a MobileNetV2-based deep learning model.

The model achieved a **validation accuracy of 81.5%** and was also tested on unseen video data.

---

## 🎯 Objectives

- Detect human activities from video data.
- Extract frames from video sequences.
- Preprocess images for deep learning.
- Apply Transfer Learning using MobileNetV2.
- Classify Running, Walking, and Standing activities.
- Develop an efficient model for real-time applications.

---

## 🗂️ Dataset & Preprocessing

The dataset contains **more than 2,300 frames** extracted from video sequences.

### Frame Extraction

Using OpenCV, every **10th frame** was extracted from the videos.

### Image Processing

- Image Size: **128 × 128 pixels**
- Pixel Normalization: **[0, 255] → [0, 1]**

### Data Augmentation

To improve model robustness and reduce overfitting:

- Rotation
- Shifting
- Flipping

---

## 🧠 Model Architecture

The project uses **MobileNetV2 with Transfer Learning**.

```text
Input Image
128 × 128
     │
     ▼
MobileNetV2
ImageNet Pre-trained Weights
     │
     ▼
Global Average Pooling
     │
     ▼
Dense Layer
512 Neurons
     │
     ▼
ReLU Activation
     │
     ▼
Dropout
0.5
     │
     ▼
Softmax Output
     │
     ├── Running
     ├── Walking
     └── Standing
