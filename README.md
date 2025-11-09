# Higgs Boson Classification

## Project Summary
This is a portfolio project by **AtomCamp**, focusing on **classifying Higgs boson events** using deep learning. The project leverages particle physics data to predict the occurrence of Higgs boson events.

The goal is to implement a full machine learning workflow: from data preprocessing and feature engineering to model training and evaluation.

---

## Dataset
- The dataset contains features extracted from particle collisions.  
- Source: [Kaggle Higgs Boson Challenge](https://www.kaggle.com/c/higgs-boson)  
- Key features include: `DER_mass_MMC`, `DER_mass_transverse_met_lep`, `DER_mass_vis`, etc.

---

## Approach
1. **Data Preprocessing**
   - Handling missing values and feature normalization
   - Exploratory Data Analysis (EDA) to understand feature distributions

2. **Model Building**
   - Deep learning models using **TensorFlow / Keras**
   - Explored different architectures, layers, and activation functions

3. **Evaluation**
   - Metrics: Accuracy, AUC, and confusion matrix
   - Visualizations for interpreting model predictions

---

## Key Highlights
- Achieved **~84.5% validation accuracy**  
- Modular code structure for data, modeling, and evaluation  
- Visualized model training and results for better insights  

---





---

## 🧠 Reflection

### How did model depth and activation affect performance?
Experimenting with model depth taught me that adding more layers improves the model’s ability to learn complex relationships — but only to a point. When I increased the depth beyond three layers, training initially broke due to exploding gradients (loss: nan).  

Techniques that helped:
- **Batch Normalization** stabilized deeper models.  
- **ReLU activations** enabled efficient training, avoiding vanishing gradients common with sigmoid or tanh.  

---

### What helped mitigate overfitting?
Overfitting was a challenge, especially with high-capacity models. Key techniques that improved generalization:  
- **L2 Regularization**: kept weights small  
- **Dropout (0.3–0.4)**: prevented memorization of training data  
- **Batch Normalization**: acted as a soft regularizer  
- **Early Stopping**: saved the model at its best validation performance  

---

### How did learning rate and optimizer affect convergence?
- Initial learning rate (0.001) caused NaN losses. Gradually reducing it to 1e-5 and using **ReduceLROnPlateau** enabled smooth convergence.  
- **Adam optimizer** worked well, while **AdamW** slightly improved generalization by decoupling weight decay.  
- Achieved ~**84.5% validation accuracy** after 150 epochs.

---

### What would I improve with more time or compute?
- **Automate Hyperparameter Search**: Use Keras Tuner to optimize learning rate, dropout, and regularization.  
- **Handle Missing Data Better**: Replace -999.0 values using Iterative Imputer or encode them as categorical.  
- **Try Ensemble Learning**: Combine multiple models (Deep Learning + XGBoost) for higher accuracy and robustness.

---

### Final Thoughts
This project was more than just building a classifier — it was a journey through the realities of deep learning. Fixing NaN losses, experimenting with optimizers, and tuning hyperparameters taught me the importance of patience and experimentation. Reaching stable performance was genuinely rewarding and gave me a deeper understanding of applying theory to real-world results.

---

## License
This project is **open-source** under the MIT License.






