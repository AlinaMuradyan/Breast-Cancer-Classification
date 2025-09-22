# 🧠 Breast Cancer Classification with Neural Networks

This project uses the **Breast Cancer dataset** from `sklearn.datasets` to build and train a **Neural Network** for binary classification (Malignant vs. Benign tumors).  
The goal is to demonstrate deep learning for medical data analysis and provide model evaluation through metrics and visualizations.

---

## 📊 Dataset
- Source: `sklearn.datasets.load_breast_cancer()`
- Features: 30 numeric features describing tumor characteristics
- Target classes:
  - **0 → Malignant**
  - **1 → Benign**

---

## ⚙️ Model Architecture
The neural network was built using **TensorFlow/Keras**:

- Dense(32, ReLU) + BatchNormalization  
- Dense(16, ReLU)  
- Dense(8, ReLU)  
- Dense(2, Softmax)

---

## 📈 Results

### Confusion Matrix
|               | Predicted Malignant | Predicted Benign |
|---------------|----------------------|------------------|
| **Malignant** | 50                   | 0                |
| **Benign**    | 13                   | 68               |

- ✅ Correctly classified malignant tumors: **50**
- ✅ Correctly classified benign tumors: **68**
- ❌ Misclassified benign tumors: **13**
- ⚠️ No malignant tumors were misclassified

---

## 🔎 Evaluation
- **High sensitivity** (no malignant cases missed) → great for medical use  
- Some benign cases were misclassified as malignant (false positives), which is safer than false negatives in cancer detection.

---

## 🚀 How to Run
```bash
# Clone the repository
git clone https://github.com/AlinaMuradyan/Breast-Cancer-Classification.git
cd Breast-Cancer-Classification

# Install dependencies
pip install -r requirements.txt

# Run Jupyter Notebook
jupyter notebook
