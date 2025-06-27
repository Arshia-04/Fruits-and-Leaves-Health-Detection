# 🍎🍃Health Detection of Fruits and Leaves

This repository contains a custom-trained YOLOv5 model to detect **healthy and diseased fruits and leaves**.  
It was trained on a custom dataset in Roboflow (images were taken from various sources, including Roboflow, Google images, annotated using bounding box labeling, and data augmentation and data versioning at the end) using YOLOv5 in a Kaggle Notebook.


## ✅ **Model**

- **File:** `best.pt`
- **Framework:** YOLOv5 (PyTorch)
- **Classes:** Healthy, Diseased


## ✅ **Outputs**

This repo includes:
- `best.pt` — trained weights
- `/outputs/` — sample images (with bounding boxes already drawn)
- `/metrics/` — training curves and confusion matrix
