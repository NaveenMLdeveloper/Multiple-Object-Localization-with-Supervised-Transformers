# 🧠 Multiple Object Localization with Supervised Transformers
![image](https://github.com/user-attachments/assets/4bc879e5-7ece-4dc7-b64d-c0ebe8c4a66b)

## 📘 Project Overview
This project focuses on detecting and localizing **multiple objects** within an image using **Transformer-based deep learning models** trained under **supervised learning** settings. Inspired by the DETR (DEtection TRansformer) architecture, this approach utilizes attention mechanisms to both classify and localize objects efficiently.

---

## 🎯 Objective
To build an accurate system capable of:
- 📍 Identifying the **type** of each object in an image
- 📦 Predicting their **bounding box coordinates**
- 🧠 Utilizing the power of **supervised transformers** to learn spatial and contextual relationships in images

---

## 🧪 Core Approach
We adapt the **DETR (Facebook AI)** architecture to:
- Use an **encoder-decoder transformer** for image representation
- Replace traditional CNN+RPN pipelines with **end-to-end attention**
- Perform **object classification** and **bounding box regression** in one step

![image](https://github.com/user-attachments/assets/aab4c214-23f1-4533-a5dd-e89940a84ea5)


---

## 🧠 Model Architecture
- 📷 Input image → CNN backbone (e.g., ResNet50)
- 🔁 Flattened features → Transformer encoder
- 📡 Decoder receives learnable object queries
- 🎯 Output: Object labels + bounding boxes (no need for NMS)

---

## 🔧 Implementation Steps
1️⃣ **Data Preprocessing**:
   - Parse and load COCO/VOC annotations
   - Normalize bounding boxes
   - Apply data augmentation

2️⃣ **Model Construction**:
   - CNN backbone (ResNet or EfficientNet)
   - Transformer encoder-decoder
   - Multi-head attention layers

3️⃣ **Training**:
   - Supervised training with loss = classification loss + box loss + GIoU loss
   - Evaluation using mAP, IoU, Precision, and Recall

4️⃣ **Prediction**:
   - Visualize object labels + bounding boxes on unseen images
   - Export detections to JSON for external use

---

## 📈 Evaluation Metrics
- ✅ **mAP (mean Average Precision)**
- 📦 **IoU (Intersection over Union)**
- 🧠 **Classification Accuracy**
- 🕒 Inference Speed

---

## 🛠️ Technologies Used
- 🐍 Python
- 🧱 PyTorch / TensorFlow
- 🧠 HuggingFace Transformers
- 📊 Matplotlib / Seaborn for visualizations
- 🔖 COCO API / Albumentations

