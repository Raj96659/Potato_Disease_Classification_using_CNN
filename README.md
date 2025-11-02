<h1 align="center">🥔 Potato Disease Classification using CNN & Flask</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Language-Python-yellow?style=for-the-badge&logo=python&logoColor=white" alt="Python Badge">
  <img src="https://img.shields.io/badge/Framework-Flask-black?style=for-the-badge&logo=flask&logoColor=white" alt="Flask Badge">
  <img src="https://img.shields.io/badge/Deep%20Learning-TensorFlow-orange?style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow Badge">
  <img src="https://img.shields.io/badge/Library-Keras-red?style=for-the-badge&logo=keras&logoColor=white" alt="Keras Badge">
  <img src="https://img.shields.io/badge/Library-Pandas-teal?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas Badge">
  <img src="https://img.shields.io/badge/Library-NumPy-blue?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy Badge">
  <img src="https://img.shields.io/badge/Library-Matplotlib-lightblue?style=for-the-badge&logo=plotly&logoColor=white" alt="Matplotlib Badge">
  <img src="https://img.shields.io/badge/Model-CNN-green?style=for-the-badge" alt="CNN Badge">
</p>


A deep learning web app that classifies **potato leaf diseases** — *Early Blight*, *Late Blight*, or *Healthy* — using a **Convolutional Neural Network (CNN)** trained in TensorFlow and deployed with Flask.

---

## 📘 Project Overview
This project helps **farmers and researchers** detect potato leaf diseases quickly and accurately.  
The CNN model is trained on the *Potato Leaf Disease Dataset* from Kaggle and integrated with a Flask web app for **real-time image-based predictions**.

---

## 🧠 Model Details

### 📊 Dataset
**Source:** [Potato Leaf Disease Dataset (Kaggle)](https://www.kaggle.com/datasets/muhammadardiputra/potato-leaf-disease-dataset)  
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
- Predicted Label: Potato — Early Blight
- Confidence: 92.4%

<h2>📸 Preview</h2>
<p align="center">
  <img src="https://github.com/Raj96659/Potato_Disease_Classification_using_CNN/blob/main/Screenshot%202025-11-02%20093737.png" width="500">
</p>
<p align="center">
  <img src="https://github.com/Raj96659/Potato_Disease_Classification_using_CNN/blob/main/Screenshot%202025-11-02%20093813.png" width="500">
</p>

## 🚀 Future Improvements

- Extend support for multiple crops (e.g., tomato, corn, etc.)
- Deploy on Render, Vercel, or Hugging Face Spaces
- Add database logging for predictions
- Introduce voice-based output

## 🙌 Acknowledgements

- Dataset: Potato Leaf Disease Dataset – Kaggle
- Frameworks: TensorFlow, Flask
- Developer: Raj Sonawane
