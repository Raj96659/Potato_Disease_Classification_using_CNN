
# 🥔 Crop Potato Disease Classification using CNN & Flask

## 📘 Overview
This project is a **Deep Learning–based web application** that classifies potato leaf images into three categories:
- **Potato — Early Blight**
- **Potato — Late Blight**
- **Potato — Healthy**

It uses a **Convolutional Neural Network (CNN)** trained on a potato leaf disease dataset and deployed using **Flask**.  
Users can upload images of potato leaves to instantly get disease predictions along with confidence levels.

---

## 🎯 Objective
To assist farmers and researchers by providing an automated system that identifies potato plant diseases early —  
reducing manual inspection effort and improving crop yield.

---

## ⚙️ Tech Stack

| Component | Technology Used |
|------------|-----------------|
| **Language** | Python |
| **Framework** | Flask |
| **Deep Learning** | TensorFlow / Keras |
| **Frontend** | HTML, CSS, Bootstrap |
| **IDE / Tools** | VS Code / Jupyter Notebook |
| **Deployment (optional)** | Render / Heroku / Localhost |

---

## 🧩 System Workflow

### 1️⃣ Model Training (TensorFlow)
- The dataset is split into **Train**, **Validation**, and **Test** sets.
- Images are resized to a consistent shape (`255x255x3`).
- A **CNN** model is trained for **20–70 epochs** with **Early Stopping** to prevent overfitting.
- The model is compiled using:
  ```python
  model.compile(optimizer='adam',
                loss='sparse_categorical_crossentropy',
                metrics=['accuracy'])

  ## 🧠 Model Architecture

| Parameter | Value |
|------------|--------|
| **Model Type** | Convolutional Neural Network (CNN) |
| **Input Image Size** | 255×255×3 |
| **Output Classes** | Early Blight, Late Blight, Healthy |
| **Optimizer** | Adam |
| **Loss Function** | Sparse Categorical Crossentropy |
| **Batch Size** | 32 |
| **Epochs** | 20 (with EarlyStopping) |

---

## 🧩 Model Training
Trained model is saved as:
- Crop_Disease_Classification.h5

---

## 2️⃣ Flask Backend

Flask handles image uploads and prediction requests.

When a user uploads an image:
1. The image is stored in the `static/` folder.  
2. TensorFlow preprocesses and reshapes the image.  
3. The CNN model predicts the class and confidence.  
4. Flask renders results on the web page.

---

## 3️⃣ Frontend (HTML + Bootstrap)

A simple and clean UI that includes:
- Image upload box  
- Display of uploaded image  
- Predicted label and confidence percentage  
- Error handling messages (e.g., “No file selected”)  

Styled using **Bootstrap 5** and CSS gradients for a modern appearance.

---

## 🖥️ Flask Application Explanation

### 🔹 Model Loading
```python
model = tf.keras.models.load_model('Crop_Disease_Classification.h5')

