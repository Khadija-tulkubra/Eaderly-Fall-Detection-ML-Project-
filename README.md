# Detecting Falls with AI  
### A Comparative Study of Machine Learning & Deep Learning Approaches

## 📖 Project Overview
This project focuses on **Elderly Activity Recognition and Fall Detection** using wearable sensor data from the **MobiFall Dataset v2.0**.  
The goal is to compare **classical machine learning** techniques with **deep learning models** to analyze how different approaches handle **time-series accelerometer data**.

Fall detection is a critical real-world problem, especially for elderly care, where **missing a fall can have serious consequences**.

---

## 🎯 Objectives
- Analyze raw accelerometer time-series data
- Compare feature-based ML models with deep learning approaches
- Evaluate models using **accuracy and macro F1-score**
- Understand the importance of temporal modeling for sensor data

---

## 📊 Dataset
- **Dataset:** MobiFall Dataset v2.0  
- **Data Type:** Accelerometer sensor readings  
- **Activities:** Daily activities + Fall events  
- **Challenge:** Class imbalance (fewer fall samples)

---

## 🧠 Approaches Used

### 1️⃣ Feature Engineering + Classical Machine Learning
Statistical features were extracted from raw accelerometer signals:
- Mean
- Standard Deviation
- Minimum
- Maximum

**Models Used:**
- Logistic Regression  
- Support Vector Machine (SVM)  
- Decision Tree  
- Random Forest / XGBoost  

**Results:**
- Accuracy: **98.31%**
- Macro F1-Score: **0.96**

➡️ High accuracy but strong dependency on manual feature engineering.

---

### 2️⃣ Fully Connected Deep Neural Network (FC-DNN)
- Raw sensor data used directly
- No manual feature extraction

**Results:**
- Accuracy: **90.05%**
- Macro F1-Score: **0.73**

➡️ Reduced manual effort but weak at capturing temporal dependencies.

---

### 3️⃣ Sequence-Based Deep Learning (LSTM)
- Sensor data converted into fixed-length sequences
- Temporal information preserved

**Results:**
- Accuracy: **96.48%**
- Macro F1-Score: **0.9165**

➡️ Best balanced performance, especially for fall-related activities.

---

## ⚠️ Challenges Faced
- Class imbalance (falls vs daily activities)
- Parsing raw sensor files with inconsistent formatting
- Selecting optimal window size and sequence length
- Improving macro F1-score instead of accuracy only
- Low recall for minority fall classes in ML models

---

## 🌱 Key Learnings
- Time-series data requires temporal modeling
- Accuracy alone can be misleading
- Macro F1-score is crucial for imbalanced datasets
- Sequence-based models are more suitable for HAR tasks
- Proper preprocessing significantly impacts results

---

## 🔮 Future Work
- Implement Attention Mechanisms
- Explore Transformer-based models
- Improve recall for fall detection in real-world scenarios

---

## 👩‍💻 Contributors
- **Khadija Tul Kubra**
- **Alina Idrees**

---

## 📌 Technologies Used
- Python  
- NumPy, Pandas  
- Scikit-learn  
- TensorFlow / Keras  
- Matplotlib  

---

## 📄 License
This project is developed for **academic and learning purposes**.
