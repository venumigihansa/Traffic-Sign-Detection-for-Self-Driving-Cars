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

<img src="https://user-images.githubusercontent.com/your-demo.png" width="480"/>

> *Real-time detection of traffic signs from dashcam footage using Pi camera and NCNN backend*

---

## 🧰 Hardware Requirements

- Raspberry Pi 4 Model B (or compatible board)  
- Pi Camera Module v2 (or any compatible CSI/USB camera)  
- MicroSD card with Raspbian OS  
- Monitor + keyboard/mouse for setup  
- Optional: Portable power supply for mobile testing  

---
---

## 📂 Dataset

This project uses the **German Traffic Sign Detection Benchmark (GTSDB)** for training the YOLOv11s model.

🔗 [Download GTSDB Dataset (Google Drive)](https://drive.google.com/file/d/1AudgxEPmgsP-0HrYzBKzAV0Gn2tyAJjI/view?usp=drive_link)

The dataset contains annotated dashcam images of traffic signs in realistic driving conditions, ideal for training object detection models used in autonomous vehicles.
