# 🥔 Potato Disease Classification using CNN & Flask

A deep learning web app that classifies **potato leaf diseases** — *Early Blight*, *Late Blight*, or *Healthy* — using a **Convolutional Neural Network (CNN)** trained in TensorFlow and deployed with Flask.

---

## 📘 Project Overview
This project helps **farmers and researchers** detect potato leaf diseases quickly and accurately.  
The CNN model is trained on the *Potato Leaf Disease Dataset* from Kaggle and integrated with a Flask web app for **real-time image-based predictions**.

---

## 🧠 Model Details

### 📊 Dataset
**Source:** [Potato Leaf Disease Dataset (Kaggle)](https://www.kaggle.com/datasets)  
**Classes:**
- Potato — Early Blight  
- Potato — Late Blight  
- Potato — Healthy  

---

### 🧩 CNN Architecture
A custom **Convolutional Neural Network** built using **TensorFlow**:

- Convolutional + MaxPooling layers for feature extraction  
- Dense layers for classification  
- ReLU activation & Softmax output layer  

| Parameter | Value |
|------------|--------|
| **Model Type** | Convolutional Neural Network (CNN) |
| **Input Image Size** | 255 × 255 × 3 |
| **Output Classes** | Early Blight, Late Blight, Healthy |
| **Optimizer** | Adam |
| **Loss Function** | Sparse Categorical Crossentropy |
| **Batch Size** | 32 |
| **Epochs** | 70 (with EarlyStopping) |

---

## ⚙️ Flask Backend

### 🔹 Model Loading
The trained CNN model **`Crop_Disease_Classification.h5`** is loaded for inference.

### 🔹 Prediction Function
✅ Converts uploaded image into a tensor  
✅ Feeds it to the CNN model  
✅ Returns the predicted **class label** and **confidence score**

### 🔹 Routes
- `'/'` → Handles image upload and prediction display  
- Validates allowed file types (`jpg`, `jpeg`, `png`)  

---

## 🌐 Frontend (index.html)
A clean, responsive **Bootstrap 5** interface displays:

- Image upload section  
- Uploaded image preview  
- Predicted label and confidence percentage  

**Example Output:**
