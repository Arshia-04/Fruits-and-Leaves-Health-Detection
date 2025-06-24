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

---

## ⚠️ Model Limitations

- **Background Detection**:  
  The model struggles to properly identify and distinguish the background from the objects in the image. This leads to **misclassifications** where the model may incorrectly classify parts of the background as objects. The confusion matrix shows the model has difficulty predicting the background class, with low classification scores (especially in the 'background' row).
  
- **Confusion Between Fruits and Leaves**:  
  Fruits and leaves often have **similar shapes** (e.g., round shapes, elongated forms), which makes it hard for the model to distinguish between them. This results in some misclassifications, especially when the objects are very similar in appearance.
  
- **Class Imbalance**:  
  The model was trained on a dataset that may not be fully representative of real-world scenarios. As a result, it might perform well on some classes (e.g., 'Healthy') but struggle with others, especially when there is a significant class imbalance.
  
---

## ✅ Suggestions for Future Work

- **Improve background segmentation** using techniques like adding more training data or background subtraction.
- **Enhance data augmentation** to improve model robustness to similar-looking classes, such as fruits and vegetables with similar shapes.
- **Fine-tune the model** on additional data to improve the ability to distinguish between fruits and leaves.
