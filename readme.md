# Performance Analysis of YOLO Algorithms in Skin Cancer Diagnosis

This project comparatively analyzes the performance of the most recent deep learning architectures in object detection—YOLOv5, YOLOv8, YOLOv9, and YOLOv11—to optimize clinical decision support systems for the early diagnosis of skin cancer.

## 🎯 Project Overview
In dermatological clinical practice, the diagnosis of skin lesions relies heavily on visual examination based on expert experience; however, the scarcity of specialists and morphological similarities can limit diagnostic accuracy. This study was developed to create a reliable digital assistant capable of minimizing error margins and accelerating diagnostic speed during pre-biopsy screening processes.

* **Models Used:** YOLOv5, YOLOv8, YOLOv9, and YOLOv11.
* **Hardware & Training Parameters:** The training and testing processes were conducted on an Nvidia A100 GPU infrastructure. Images were optimized to a resolution of 800x800 pixels, and the training phase was configured for 25 epochs with a batch size of 8.
* **Key Findings:** The YOLOv11 architecture achieved the highest overall diagnostic accuracy (0.879 mAP@.5 and 0.705 mAP@.5:.95). The YOLOv9 model reached the most sensitive results in capturing cancerous cases (Recall: 0.893), while YOLOv5 and YOLOv8 provided the most efficient performance for real-time applications with an inference time of 2.0 ms.

## 📊 Dataset Distribution
The dataset utilized in this research was acquired from the open-source platform Roboflow Universe ([Dataset Link](https://app.roboflow.com/cem-yujfy/skin-cancer-vczfq-rvakt/1)). It comprises a total of 2,000 dermatological images.
* **Malignant:** Melanoma (mel), Basal Cell Carcinoma (bcc), and Actinic Keratosis (akiec) representing potential malignancy.
* **Benign:** Melanocytic nevi (nv), Benign keratosis (bkl), Vascular lesions (vasc), and Dermatofibroma (df).

| Dataset Split | Total Images | Malignant | Benign | 
| :--- | :--- | :--- | :--- | 
| **Train** | 1401 | 701 | 700 |
| **Validation** | 400 | 200 | 200 | 
| **Test** | 199 | 100 | 99 | 
| **TOTAL** | **2000** | **1001** | **999** | 

## 📈 Comparative Performance Analysis
The quantitative success, parameter size, and speed metrics of the four different YOLO architectures are summarized in the table below.

| Model | Parameters | GFLOPs | Precision (P) | Recall (R) | mAP50 | mAP50-95 | Inference Time | 
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | 
| **YOLOv5** | 7.0 M | 15.8 | 0.644 | 0.856 | 0.789 | 0.605 | 2.0 ms | 
| **YOLOv8** | 11.1 M | 28.4 | 0.787 | 0.843 | 0.876 | 0.696 | 2.0 ms | 
| **YOLOv9** | 25.3 M | 102.3| 0.729 | 0.893 | 0.868 | 0.691 | 24.5 ms| 
| **YOLOv11**| 9.4 M | 21.3 | 0.765 | 0.850 | 0.879 | 0.705 | 8.0 ms | 

### Model Evaluations
* **YOLOv11:** Provides the most optimized balance in terms of accuracy and parameter efficiency. Despite having roughly one-third of the parameters compared to the YOLOv9 architecture, it achieved a higher mAP50-95 score (0.705), proving its geometric precision in determining lesion boundaries.
* **YOLOv9:** Minimized the risk of missing critical cases (false negatives) with an 0.893 recall rate, providing maximum sensitivity in capturing cancerous lesions.
* **YOLOv5 & YOLOv8:** With an inference time of 2.0 ms, these models offered the most efficient performance for real-time applications and rapid clinical screenings requiring high speed.

## 🖼️ Project Visualizations

*(Developer Note: Drag and drop your images into the GitHub editor to replace these placeholders)*

* `[Insert Dataset - Malignant and Benign Samples Image Here]` 
* `[Insert YOLOv11 Inference and Validation Samples Image Here]` 
* `[Insert YOLO Models Training (Epoch) Graphs Here]` 
* `[Insert YOLOv11 Confusion Matrix Here]` 

## 👨‍💻 Author & Contact
This academic research was conducted as part of the Master's Degree Program (with Thesis) in Computer Engineering at Bandırma Onyedi Eylül University, Faculty of Engineering and Natural Sciences.

* **Author:** Cem Er
* **Contact:** 2515514026@ogr.bandirma.edu.tr