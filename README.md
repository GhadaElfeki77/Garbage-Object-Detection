# Garbage-Object-Detection

# Garbage Object Detection: YOLOv8 vs YOLOv5 vs Faster R-CNN

## 📌 Project Overview

This project implements and compares three popular deep learning object detection models on a real-world garbage/waste detection dataset:

* **YOLOv8**
* **YOLOv5**
* **Faster R-CNN**

The objective is to evaluate the models not only according to detection performance, but also according to computational efficiency and inference speed.

---

## 🎯 Project Objectives

The project aims to:

* Train multiple object detection architectures on the same dataset.
* Detect different types of garbage objects.
* Compare model performance using standard object detection metrics.
* Measure inference time and FPS.
* Analyze the trade-off between accuracy and speed.
* Save the trained models and evaluation results.

---

## 🗂️ Dataset

**Dataset:** Garbage Classification 3

**Source:** Roboflow Universe

The dataset contains seven garbage categories:

1. Paper
2. Plastic
3. Glass
4. Metal
5. Cardboard
6. Cloth
7. Biodegradable

The dataset is provided in YOLO-compatible annotation format.

---

## 🤖 Models

### 1. YOLOv8

A modern YOLO architecture designed for fast and accurate object detection.

Configuration used:

* Model: YOLOv8n
* Image size: 416 × 416
* Transfer learning using pretrained weights

### 2. YOLOv5

A widely used YOLO object detection architecture.

Configuration used:

* Model: YOLOv5s
* Image size: 416 × 416
* Transfer learning using pretrained weights

### 3. Faster R-CNN

A two-stage object detection architecture implemented using TorchVision.

Configuration used:

* Backbone: ResNet-50 + FPN
* Pretrained weights
* Custom detection head for the 7 garbage classes
* Image size: 416 × 416

---

## 📊 Evaluation Metrics

The models are compared using:

| Metric         | Description                                        |
| -------------- | -------------------------------------------------- |
| Precision      | Percentage of detected objects that are correct    |
| Recall         | Percentage of actual objects successfully detected |
| mAP@50         | Mean Average Precision at IoU 0.50                 |
| mAP@50:95      | Mean Average Precision across IoU 0.50–0.95        |
| Inference Time | Time required to process an image                  |
| FPS            | Frames/images processed per second                 |
| Parameters     | Number of trainable model parameters               |

> For object detection, mAP, Precision, and Recall are more meaningful than ordinary classification accuracy.

---

## 🛠️ Technologies

* Python
* PyTorch
* TorchVision
* Ultralytics
* YOLOv5
* YOLOv8
* Faster R-CNN
* OpenCV
* Roboflow
* NumPy
* Pandas
* Matplotlib
* Scikit-learn

---

## 🔄 Project Workflow

```text
Roboflow Dataset
       ↓
Data Download
       ↓
Data Preparation
       ↓
YOLO Annotations
       ↓
 ┌──────────┬──────────┬──────────────┐
 ↓          ↓          ↓
YOLOv8    YOLOv5    Faster R-CNN
 ↓          ↓          ↓
Training   Training   Fine-tuning
 └──────────┴──────────┴──────────────┘
              ↓
       Model Evaluation
              ↓
 ┌──────────────────────────────┐
 │ Precision                    │
 │ Recall                       │
 │ mAP@50                       │
 │ mAP@50:95                    │
 │ Inference Time               │
 │ FPS                          │
 └──────────────────────────────┘
              ↓
       Model Comparison
```

---

## 📈 Results

The final comparison is saved automatically in:

```text
results/
├── model_comparison.csv
├── model_comparison.json
├── mAP_comparison.png
├── inference_time_comparison.png
└── FPS_comparison.png
```

Example comparison structure:

| Model        | Precision | Recall | mAP@50 | mAP@50:95 | Inference Time | FPS |
| ------------ | --------: | -----: | -----: | --------: | -------------: | --: |
| YOLOv8n      |         — |      — |      — |         — |              — |   — |
| YOLOv5s      |         — |      — |      — |         — |              — |   — |
| Faster R-CNN |         — |      — |      — |         — |              — |   — |

The values will be filled automatically after training and evaluation.

---

## 📁 Project Structure

```text
Garbage-Object-Detection/
│
├── notebook/
│   └── garbage_object_detection.ipynb
│
├── models/
│   ├── yolov8/
│   ├── yolov5/
│   └── faster_rcnn/
│
├── results/
│   ├── model_comparison.csv
│   ├── model_comparison.json
│   ├── mAP_comparison.png
│   ├── inference_time_comparison.png
│   └── FPS_comparison.png
│
├── predictions/
│   └── sample_predictions.png
│
├── README.md
└── requirements.txt
```

---

## 💡 Key Learning Outcomes

Through this project, I developed practical experience in:

* Object detection using deep learning.
* Preparing YOLO-format datasets.
* Working with bounding-box annotations.
* Transfer learning and pretrained models.
* Fine-tuning Faster R-CNN.
* Evaluating object detection models.
* Measuring inference performance.
* Comparing accuracy and computational efficiency.
* Building reproducible Computer Vision workflows.

---

## 🚀 Future Improvements

Possible future improvements include:

* Data augmentation.
* Hyperparameter optimization.
* Larger YOLO models such as YOLOv8s/m.
* Different Faster R-CNN backbones.
* ROC/PR analysis.
* Class-wise mAP analysis.
* Confusion analysis of visually similar waste categories.
* Model deployment using Streamlit or Gradio.
* Real-time garbage detection using webcam/video.

---

## 📚 Dataset

Garbage Classification 3 dataset from Roboflow Universe.

Dataset license: **CC BY 4.0**

---

## 👩‍🔬 About Me

**Dr. Ghada Elfeki**

PhD in Biochemistry | Molecular Biology | Data Analysis | Machine Learning | Deep Learning | Computer Vision

I am developing my expertise at the intersection of **scientific research, data analysis, machine learning, and artificial intelligence**, with a particular interest in applying AI and Computer Vision to real-world problems.

