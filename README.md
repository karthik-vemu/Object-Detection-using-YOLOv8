# 🧠 Object Detection using YOLOv8 – Bat and Ball Detection

This repository contains a deep learning project that demonstrates object detection using **YOLOv8**, focusing on recognizing **bat** and **ball** objects in real-time video streams. This project was developed as part of my internship at **AIMERS** (June–July 2024, Batch 4).

---

## 📌 Table of Contents
- [📖 Introduction](#-introduction)
- [🧱 Project Architecture](#-project-architecture)
- [🧪 Testing & Results](#-testing--results)
- [📹 Real-time Detection](#-real-time-detection)
- [🐞 Common Issues](#-common-issues)
- [🌟 Future Improvements](#-future-improvements)
- [🤝 Acknowledgments](#-acknowledgments)

---

## 📖 Introduction

YOLOv8 (You Only Look Once, version 8) is the latest real-time object detection model developed by **Ultralytics**. It performs both object localization and classification in a single forward pass, making it extremely fast and accurate.

In this project, I trained YOLOv8 to detect two objects: `bat` and `ball`. This could be extended to sports analytics, player tracking, or training assistance systems in the future.

---

## 🧱 Project Architecture

text
[Video/Image Input]
        ↓
[Preprocessing (Resize, Normalize)]
        ↓
[YOLOv8 Model Inference]
        ↓
[Bounding Box Prediction]
        ↓
[Display Output using OpenCV]


# Testing & Results
Precision: 92%
Recall: 90%
mAP@0.5: 94%
Visualization done on sample sports videos

# 📹 Real-time Detection
bash
Copy
Edit
# Detect from webcam or video
yolo task=detect mode=predict model=best.pt source=0  # For webcam
yolo task=detect mode=predict model=best.pt source=sample_video.mp4

#  Common Issues
CUDA errors: Make sure GPU drivers and CUDA version are compatible.
Low accuracy: Check annotations, increase data, or use a larger model (yolov8s.pt).
Detection delay: Use smaller image size or switch to YOLOv8n.

# Future Improvements
Add more sports objects like helmets, stumps, gloves
Integrate tracking (DeepSORT) for continuous tracking
Build a Streamlit app for UI-based detection
Host model on Hugging Face or Render

# Acknowledgments
Ultralytics for YOLOv8
Roboflow for dataset management and preprocessing
AIMERS for mentorship during internship

