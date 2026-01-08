# 🧠 Machine Learning based Clinical Driven Support System(CDSS) for Skin Cancer Detection

This repository presents a **Machine Learning–Driven Clinical Decision Support System (CDSS)** for **skin cancer detection and classification**, developed as part of the **IEEE SPS GS Summer Internship 2025** under the guidance of **Dr. Ketki C. Pathak**.

The system integrates **deep learning–based feature extraction**, **traditional machine learning classifiers**, **patient metadata**, and **explainable AI (XAI)** techniques to assist dermatologists in early and accurate diagnosis of skin cancer.

---

## 📌 Project Highlights

- 🔍 **Multi-class Skin Cancer Classification** (7 lesion types)
- 🧠 **Deep Feature Extraction** using pre-trained **ResNet50**
- ⚖️ **Class Imbalance Handling** using **SMOTE**
- 📉 **Dimensionality Reduction** using **PCA**
- 🤖 **Machine Learning Models**:
  - Support Vector Machine (SVM)
  - Random Forest (RF)
  - Logistic Regression (LR)
- 🧩 **Metadata Integration**: Age, Sex, Lesion Location
- 🔎 **Explainable AI**:
  - Grad-CAM
  - SHAP
  - LIME
- 📊 **High Performance**:
  - Random Forest Accuracy: **98%**
  - SVM Accuracy: **97%**

---

## 🗂️ Dataset Used

⚠️ **Datasets are NOT included in this repository** due to size and licensing constraints.  
They are **downloaded dynamically using the Kaggle API**.

Primary dataset:
- **HAM10000 (Human Against Machine with 10000 training images)**  
  - 10,015 dermoscopic images  
  - 7 skin lesion classes:
    - Actinic keratoses (akiec)
    - Basal cell carcinoma (bcc)
    - Benign keratosis-like lesions (bkl)
    - Dermatofibroma (df)
    - Melanoma (mel)
    - Melanocytic nevi (nv)
    - Vascular lesions (vasc)

Additional datasets referenced for validation and research:
- ISIC Archive
- PH² Dataset
- Derm7pt
- BCN20000

---

## 🔑 Dataset Setup (Kaggle API)

### Step 1: Kaggle API Authentication
1. Create a Kaggle account: https://www.kaggle.com
2. Go to **Account → API → Create New API Token**
3. Download `kaggle.json`

### Step 2: Configure Kaggle API

#### Linux / macOS

mkdir ~/.kaggle
mv kaggle.json ~/.kaggle/
chmod 600 ~/.kaggle/kaggle.json

Step 3: Download Dataset Using Kaggle API

kaggle datasets download -d kmader/skin-cancer-mnist-ham10000
unzip the dataset:
unzip skin-cancer-mnist-ham10000.zip -d dataset/

Expected Structure
dataset/
├── HAM10000_images_part_1/
├── HAM10000_images_part_2/
└── HAM10000_metadata.csv

--

## 🧪 Methodology Pipeline

Input Images
↓
Image Preprocessing (Resize, Normalize)
↓
Deep Feature Extraction (ResNet50)
↓
Metadata Integration (Age, Sex, Location)
↓
Feature Scaling
↓
PCA (Dimensionality Reduction)
↓
SMOTE (Class Balancing)
↓
Model Training (SVM, RF, LR)
↓
Performance Evaluation
↓
Explainability (Grad-CAM, SHAP, LIME)


---

## 📈 Evaluation Metrics

- Accuracy
- Precision
- Recall (Sensitivity)
- F1-Score
- Confusion Matrix
- ROC-AUC (where applicable)

**Special focus:**  
✔ High **recall for melanoma** (early detection priority)

---

## 🧠 Explainable AI (XAI)

To improve **clinical trust and transparency**, the following techniques are implemented:

- **Grad-CAM** – Visual heatmaps highlighting lesion regions influencing predictions
- **SHAP** – Global feature importance using game theory
- **LIME** – Local explanation for individual predictions

---

## 🛠️ Tech Stack & Libraries

- **Programming Language:** Python
- **Deep Learning:** TensorFlow / Keras
- **Machine Learning:** Scikit-learn
- **Data Processing:** NumPy, Pandas
- **Image Processing:** OpenCV
- **Class Imbalance:** imbalanced-learn (SMOTE)
- **Explainability:** SHAP, LIME
- **Visualization:** Matplotlib, Seaborn

---


