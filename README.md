# 🚦 Traffic Sign Detection for Self-Driving Cars

![Model](https://img.shields.io/badge/model-YOLOv11s-green)
![Platform](https://img.shields.io/badge/platform-Raspberry%20Pi-lightgrey)
![Framework](https://img.shields.io/badge/inference-NCNN-blue)

A real-time traffic sign detection system using **YOLOv11s**, optimized for deployment on **Raspberry Pi**. This project processes **dashcam footage or live camera feed** to detect and classify traffic signs, enhancing the perception module of self-driving cars.

---

## 🚀 Features

- 📦 **YOLOv11s-based** object detection optimized for edge devices  
- 🎥 Real-time detection from **live video** using Raspberry Pi Camera  
- ⚡ **NCNN**-based inference for high-speed performance on Raspberry Pi  
- 📋 Recognizes multiple traffic sign types with bounding boxes and labels  
- 🧠 Lightweight deep learning model suitable for embedded deployment  
- 🌐 Fully offline and cloud-independent for autonomous vehicles  

---

## 🎬 Demo

[![Watch the demo](https://github.com/user-attachments/assets/60762d69-ba5c-4209-8d29-89f140b5299b)](https://youtu.be/bhc6ccFv0Xg)

> *Real-time detection of traffic signs from dashcam footage using Pi camera and NCNN backend*

---

## 📂 Dataset

This project uses the **German Traffic Sign Detection Benchmark (GTSDB)** for training the YOLOv11s model.

🔗 [Download GTSDB Dataset (Google Drive)](https://drive.google.com/file/d/1AudgxEPmgsP-0HrYzBKzAV0Gn2tyAJjI/view?usp=drive_link)

The GTSDB dataset consists of **~900 annotated images** in **PPM format** and includes **42 distinct traffic sign classes**, including speed limits, warnings, and prohibitions.

---

## 🧹 Data Preprocessing

- 🔄 **Image Conversion**: Original PPM images were converted to JPG format for compatibility with training pipelines.
- 🗂 **Label Conversion**: Original annotations were converted to YOLO format (`class_id x_center y_center width height`) normalized with respect to image dimensions.
- 🧪 **Train/Validation Split**: Dataset was split into 80% training and 20% validation.
- 🧰 **Augmentation Techniques**:
  - Random brightness and contrast adjustments
  - Horizontal flipping
  - Random scaling and translation
  - Gaussian blur

These augmentations helped increase data diversity and robustness of the model to real-world scenarios.

---

## 🧠 Model Training

- 🧩 Framework: YOLOv11s (Ultralytics-based custom fork)
- ⚙️ Configuration:
  - Input Size: `640x640`
  - Batch Size: `16`
  - Epochs: `100`
- 🛠 Loss Function: Combination of objectness loss, classification loss, and bounding box regression loss

Training was done using a GPU-enabled system (e.g., Google Colab or local CUDA GPU), and the best model was selected based on validation mAP.

<img width="1096" height="530" alt="image" src="https://github.com/user-attachments/assets/4bb37545-2abb-458c-82e8-7d456abcba4e" />


---

## 📈 Evaluation

- 📊 Metrics:
  - mAP@0.5: ~91%
  - Precision: ~89%
  - Recall: ~92%
- 🔎 The model was tested on unseen validation images with cluttered backgrounds and varying lighting conditions.
- 🎯 High detection accuracy was maintained across small, occluded, and angled traffic signs.

---

## ⚙️ Deployment Details

- 📦 The final YOLOv11s weights were converted into NCNN format using ONNX as intermediate.
- 🖥 Inference runs at ~15-20 FPS on Raspberry Pi 4 with NCNN backend.
- 📷 Integrated with Pi Camera for live detection.
- 🖼 Real-time visualization includes bounding boxes and class labels overlaid on live video.

---

## 🧰 Hardware Requirements

- Raspberry Pi 4 Model B (or compatible board)  
- Pi Camera Module v2 (or USB webcam)  
- MicroSD card with Raspbian OS  
- Monitor + keyboard/mouse for setup  
- Optional: Portable power supply for mobile testing  

---
