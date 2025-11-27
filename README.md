# 🌾 Rice Leaf Disease Classification using Deep Learning

### Using **EfficientNetB0**, **DenseNet121**, and **ResNet50**

---

## 📌 Overview
This repository contains Jupyter notebooks and scripts for classifying **rice leaf diseases** using modern **Transfer Learning** architectures.

The models detect the following three diseases:
- **Bacterial Blight**
- **Brown Spot**
- **Leaf Smut**

The dataset is loaded automatically using `image_dataset_from_directory()` and split into:
- **80% Training**
- **20% Validation**

---

## 📁 Repository Structure
```
📦 Rice-Leaf-Disease-Classification
│
├── rice_disease_densenet121.ipynb
├── rice_disease_efficientnet.ipynb
├── rice_disease_resnet50.ipynb
│
├── images/                 # Optional: confusion matrices, accuracy curves
└── README.md
```

---

## 🚀 Models Implemented

### 🔹 **1. DenseNet121**
- Pretrained on ImageNet
- Initial frozen layers + custom classifier
- **Validation Accuracy:** ~96%

### 🔹 **2. EfficientNetB0**
- Lightweight and highly efficient
- Excellent performance on small datasets
- **Validation Accuracy:** **99.57%**

### 🔹 **3. ResNet50**
- Deep residual network
- Best performing model in this project
- **Validation Accuracy:** **100%**

---

## 📊 Results

### ✔️ **Confusion Matrix (ResNet50)**
```
[[309   0   0]
 [  0 348   0]
 [  0   1 278]]
```

### ✔️ **Classification Report**
```
Accuracy       : 1.00
Precision      : 1.00
Recall         : 1.00
F1-score       : 1.00
```

---

## 📦 Dataset Format
```
dataset/
 ├── Bacterialblight/
 ├── Brownspot/
 └── Leafsmut/
```

Loaded using:
```python
tf.keras.preprocessing.image_dataset_from_directory(
    DATA_DIR,
    validation_split=0.2,
    subset="training",
    seed=42,
    image_size=(224, 224)
)
```

---

## ⚙️ Installation

### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/<your-username>/Rice-Leaf-Disease-Classification.git
cd Rice-Leaf-Disease-Classification
```

### **2️⃣ Install Dependencies**
```bash
pip install tensorflow numpy matplotlib scikit-learn
```

### **3️⃣ Run the Jupyter Notebooks**
```bash
jupyter notebook
```

---

## 🧠 Features
- ✔ Transfer learning with ImageNet models
- ✔ Real-time data augmentation
- ✔ Training curves (Loss & Accuracy)
- ✔ Confusion matrix & classification report
- ✔ ModelCheckpoint + EarlyStopping
- ✔ Final trained `.h5` models saved automatically

---

## 📈 Training Curves
Each notebook generates:
- 📉 **Loss vs Epochs**
- 📈 **Accuracy vs Epochs**

(You may place the figures inside the `images/` folder.)

---

## 🔮 Future Improvements
- Add Grad-CAM heatmaps
- Deploy model using Streamlit / Flask
- Train Vision Transformers (ViT, Swin)
- Add balanced dataset or synthetic augmentation

---

## 🤝 Contributing
Contributions, suggestions, and pull requests are welcome.

---

## 📜 License
This project is licensed under the **MIT License**.
