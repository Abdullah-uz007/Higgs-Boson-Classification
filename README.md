# Higgs Boson Classification ⚛️

[![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python)](https://www.python.org/)  
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)](https://www.tensorflow.org/)  
[![Validation Accuracy](https://img.shields.io/badge/Validation%20Accuracy-84.5%25-brightgreen)]()  

---

## 📌 Project Summary
This portfolio project by **AtomCamp** focuses on **classifying Higgs boson events** using deep learning. The dataset contains features extracted from particle collisions, and the goal is to predict the occurrence of Higgs boson events with high accuracy.  

The project demonstrates a **complete ML workflow**, including data preprocessing, feature engineering, model training, and evaluation.

---

## 📊 Dataset
- Source: [Kaggle Higgs Boson Challenge](https://www.kaggle.com/c/higgs-boson)  
- Features include: `DER_mass_MMC`, `DER_mass_transverse_met_lep`, `DER_mass_vis`, etc.  

---

## 🛠️ Approach
### 1️⃣ Data Preprocessing
- Handle missing values and normalize features  
- Perform **EDA** to understand feature distributions  

### 2️⃣ Model Building
- Deep learning models using **TensorFlow / Keras**  
- Tested multiple **architectures, activations, and layers**  

### 3️⃣ Evaluation
- Metrics: **Accuracy**, **AUC**, **Confusion Matrix**  
- Visualizations to interpret predictions  

---

## ✨ Key Highlights
- Achieved **~84.5% validation accuracy**  
- Modular code structure for **data, modeling, and evaluation**  
- Deep learning insights applied to **real-world particle physics data**  

---

## 🧠 Reflection

### 🔹 Model Depth & Activation
Adding layers improved learning but only up to three. Beyond that, **exploding gradients** caused NaN losses.  
- **Batch Normalization** stabilized deep models  
- **ReLU activations** avoided vanishing gradients  

### 🔹 Mitigating Overfitting
Techniques that improved generalization:  
- **L2 Regularization**  
- **Dropout (0.3–0.4)**  
- **Batch Normalization**  
- **Early Stopping**  

### 🔹 Learning Rate & Optimizer
- Initial **0.001 LR** caused NaN losses  
- Reduced to **1e-5** with **ReduceLROnPlateau** for stable convergence  
- Used **Adam**, later **AdamW** for improved generalization  

### 🔹 Future Improvements
- Automate hyperparameter search with **Keras Tuner**  
- Better handling of missing data (-999.0)  
- Ensemble learning with **Deep Learning + XGBoost**  

### 🔹 Final Thoughts
This project taught the realities of deep learning: handling NaNs, tuning hyperparameters, and stabilizing training. Achieving stable performance was rewarding and provided hands-on experience translating theory into practice.

---

## 🗂️ Project Structure


## 🗂️ Project Structure
Higgs-Boson-Classification/
│
├── data/ # Dataset or download link
├── notebooks/ # Jupyter Notebooks
├── requirements.txt # Python dependencies
└── README.md
