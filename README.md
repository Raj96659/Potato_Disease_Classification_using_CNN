<h1 align="center">🌾 
Real-Time Crop Disease Detection Web App (CNN, VGG16 + Flask)</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Python-yellow?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Flask-black?style=for-the-badge&logo=flask&logoColor=white" alt="Flask">
  <img src="https://img.shields.io/badge/TensorFlow-orange?style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow">
  <img src="https://img.shields.io/badge/Keras-red?style=for-the-badge&logo=keras&logoColor=white" alt="Keras">
  <img src="https://img.shields.io/badge/VGG16-purple?style=for-the-badge" alt="VGG16">
  <img src="https://img.shields.io/badge/Pandas-teal?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/NumPy-blue?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy">
  <img src="https://img.shields.io/badge/Matplotlib-lightblue?style=for-the-badge&logo=plotly&logoColor=white" alt="Matplotlib">
  <img src="https://img.shields.io/badge/CNN-green?style=for-the-badge" alt="CNN">
</p>


A deep learning web application that classifies **crop leaf diseases** — *Early Blight*, *Late Blight*, or *Healthy* — using  **Custom CNN** and **Transfer Learning with VGG16** trained in TensorFlow and deployed with Flask.

---

## 📘 Project Overview
This project assists **farmers and agricultural researchers** in diagnosing crop leaf diseases quickly and accurately.  
Two deep learning models were experimented with:
- **Custom CNN model** built from scratch
- **VGG16 transfer learning model** with ImageNet weights

The best-performing model is integrated into a Flask web app for **real-time predictions** using uploaded crop leaf images.


---

## 🧠 Model Details

### 🧩 Models Used
| Model | Technique | Status |
|--------|------------|---------|
| Custom CNN | Developed from scratch | Used for baseline |
| VGG16 Transfer Learning | Fine-tuned on crop dataset | Selected for deployment |

### 📊 Dataset
Source: Crop Leaf Disease Dataset (Kaggle)


**Classes:**
- Early Blight  
- Late Blight  
- Healthy  

---

### 🧩 Model Architecture — VGG16 Transfer Learning
A **VGG16-based CNN** model built using TensorFlow and fine-tuned for crop disease classification.

| Parameter | Value |
|------------|--------|
| **Model Type** | Transfer Learning (VGG16 + Custom Layers) |
| **Input Image Size** | 255 × 255 × 3 |
| **Output Classes** | Early Blight, Late Blight, Healthy |
| **Optimizer** | Adam |
| **Loss Function** | Sparse Categorical Crossentropy |
| **Batch Size** | 32 |
| **Epochs** | 70 (with EarlyStopping) |
| **Pre-trained Weights** | ImageNet |

---

## ⚙️ Flask Backend

### 🔹 Model Loading
The trained model **`Crop_Disease_Classification_VGG16.h5`** is loaded for inference.

### 🔹 Prediction Workflow
- Preprocess uploaded image
- Convert to tensor
- Run through VGG16 model
- Predict **class label** + **confidence score**

### 🔹 Flask Routes
- `'/'` → Image upload & prediction display  
- Supports: `jpg`, `jpeg`, `png` formats  

---

## 🌐 Frontend (index.html)
A **Bootstrap 5 responsive interface** featuring:
- Image upload panel
- Preview of uploaded leaf image
- Predicted disease + confidence %

**Example Output:**
- Predicted Label: Early Blight  
- Confidence: 92.4%

---

## 🚀 Future Improvements
- Support additional crops (tomato, corn, rice, etc.)
- Deploy on Render / Vercel / HuggingFace Spaces
- Integrate prediction logging database
- Add voice-based output

---

## 🙌 Acknowledgements
- Dataset: Crop Disease Dataset – Kaggle
- Frameworks: TensorFlow, Flask
- Developer: Raj Sonawane
