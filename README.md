# # 🚗 Real-Time Vehicle Detection using YOLOv8 & YOLOv9 (Google Colab)

A computer vision project for real-time vehicle detection and classification using YOLOv8 and YOLOv9, implemented entirely in **Google Colab**. The project includes training, testing, and performance evaluation of both models on a custom dataset annotated via Roboflow.

---

## 📌 Features

- ✅ Google Colab–based implementation (no local setup needed)
- 🚀 Real-time inference with YOLOv8 and YOLOv9
- 🔍 Comparison of detection accuracy and speed
- 📦 Roboflow-integrated dataset pipeline
- 📊 mAP-based performance evaluation

---

## 🧠 Models Used

| Model   | Framework    | Version | Performance |
|---------|--------------|---------|-------------|
| YOLOv8s | Ultralytics  | v8.1    | Fast + accurate |
| YOLOv9s | Ultralytics  | v9.0    | Better mAP, handles occlusion |

---

## 📁 Dataset

- **Source**: Roboflow (exported in YOLO format)
- **Classes**: Car, Truck, Bus, Motorcycle, Bicycle
- **Augmentations**: Rotation, flip, blur, mosaic

---

## 🛠️ Google Colab Setup

1. Open the notebook in Colab:  
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/azeem-aslam-ch/Real-time-Vehicle-detection/blob/main/Vehicle_Detection_YOLOv8_YOLOv9.ipynb)

2. Run all cells to:
   - Install dependencies
   - Clone YOLOv8/YOLOv9 repos
   - Load dataset from Roboflow
   - Train and test models

---

## 🚀 Quick Commands

```python
# Train YOLOv8
!yolo task=detect mode=train model=yolov8s.pt data=data.yaml epochs=100 imgsz=640

# Train YOLOv9
!yolo task=detect mode=train model=yolov9s.pt data=data.yaml epochs=100 imgsz=640

# Inference
!yolo task=detect mode=predict model=runs/detect/train/weights/best.pt source="test.mp4"
