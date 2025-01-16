# Object Detection Using YOLOv8 and YOLOv11

## Overview
This project implements object detection using state-of-the-art pre-trained models **YOLOv8** and **YOLOv11**. These models are optimized for speed and accuracy, making them ideal for real-time applications such as autonomous driving, traffic monitoring, and surveillance. The project explores their performance on a dataset of road signs and provides a comparison of their results.

---

## Features
- **Pre-trained YOLO Models**: YOLOv8 and YOLOv11 for robust object detection.
- **High Accuracy and Speed**: Suitable for real-time applications.
- **Comprehensive Evaluation**: Metrics such as IoU, mAP, and class-wise performance.
- **Dataset Insights**: Analysis of the results on various classes of road signs.

---

## Table of Contents
1. [Background](#background)
2. [Dataset](#dataset)
3. [YOLOv8 and YOLOv11 Models](#yolov8-and-yolov11-models)
4. [Evaluation Metrics](#evaluation-metrics)
5. [Results](#results)
6. [Setup and Usage](#setup-and-usage)
7. [Future Work](#future-work)
8. [Contributors](#contributors)

---

## Background
YOLO (You Only Look Once) is a real-time object detection system that treats object detection as a regression problem. It predicts bounding boxes and class probabilities directly from full images in a single evaluation, making it both fast and efficient.

---

## Dataset
The dataset comprises 623 annotated images of road signs with:
- **Class Labels**: Types of road signs (e.g., "Stop", "Speed Limit").
- **Bounding Boxes**: Coordinates indicating the location of the objects.

### Data Source
The dataset was loaded directly from Kaggle for training and validation.

---

## YOLOv8 and YOLOv11 Models
### YOLOv8
- **Parameters**: ~3 million
- **Layers**: 168
- **Inference Time**: 3.8 ms/image
- **Features**: Optimized for real-time applications with a focus on both speed and accuracy.

### YOLOv11
- **Enhanced Architecture**: Improved feature extraction and better performance at high IoU thresholds.
- **Parameters**: Similar to YOLOv8 but optimized further for robustness in detecting smaller objects.

Both models were pre-trained on large datasets and fine-tuned on the road sign dataset.

---

## Evaluation Metrics
1. **Intersection over Union (IoU)**: Measures the overlap between predicted and ground-truth bounding boxes.
2. **Mean Average Precision (mAP)**: Evaluates detection accuracy across all classes.
3. **Class-wise IoU and mAP**: Provides insights into the performance for individual road sign categories.

---

## Results
### YOLOv8 Performance
- **IoU**: Mean IoU of 0.802
- **mAP**: 0.957
- **Best Class**: "Attention Please" with mAP of 0.995
- **Challenges**: Struggles with the "Dangerous Left Curve Ahead" class (mAP: 0.813).

### YOLOv11 Performance
- **IoU**: Mean IoU of 0.960
- **mAP**: 0.960
- **Best Class**: "Attention Please" with mAP of 0.998
- **Improvements**: Higher accuracy for challenging classes like "Dangerous Left Curve Ahead".

---

## Setup and Usage
### Prerequisites
- Python 3.7 or higher
- PyTorch 1.10+
- Required libraries: ultralytics, matplotlib, numpy, pandas.

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/yolo-object-detection.git
