# 🐶 Canine Bone Cancer Detection using Thermographic Imaging

This project implements a deep learning pipeline for detecting **canine bone cancer** from thermographic images using a **hybrid CNN + Vision Transformer (ViT)** architecture. It compares traditional feature-based methods with a modern AI-based approach for robust and scalable veterinary diagnostics.

---

## 📄 Project Summary

Based on our SPIE conference paper titled:  
**"Comparative Analysis of Traditional Thermographic Image Processing and Deep Learning Models for Canine Bone Cancer Detection"**

The project explores:
- Traditional classification using handcrafted features
- Deep learning with transfer learning (CNN + ViT)
- Data balancing with SMOTE
- Preprocessing and image enhancement tailored for thermographic imaging

---

## 🧠 Key Features

- 📷 Thermographic preprocessing (Gaussian filtering, AHE, edge detection)
- 🔍 Feature extraction: CNN (ResNet50) + Vision Transformer
- ⚖️ Dataset balancing using **SMOTE**
- 📊 Classification metrics: Accuracy, Precision, Recall, F1-Score
- 📈 Evaluation: Classification report + Confusion matrix

---

## 🗂️ Project Structure

```
📦 Canine_Cancer_Detection
 ┣ 📁 features/                # Precomputed CSV features
 ┣ 📁 model/                   # Folder for model file (excluded from GitHub)
 ┣ 📁 notebooks/               # Jupyter notebooks (optional analysis)
 ┣ 📄 vit_test_eval.py         # Evaluation script
 ┣ 📄 requirements.txt         # Dependencies
 ┗ 📄 README.md
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/RedHood316/Canine-Cancer-Detection.git
cd Canine-Cancer-Detection
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run evaluation script

Update paths in `vit_test_eval.py` as needed:

```python
model_save_path = r"C:\your_path\Model\vit_feature_classifier.pth"
test_csv_path = r"C:\your_path\features\test_features_hybrid.csv"
```

Then run:

```bash
python vit_test_eval.py
```

---

## 🔎 Sample Output

```
Classification Report:
              precision    recall  f1-score   support
   No Cancer       0.94      0.96      0.95        69
      Cancer       0.97      0.96      0.97       104

Accuracy: 96%
```

Confusion matrix is also visualized using Seaborn.

---

## 📊 Performance Comparison

| Model                     | Accuracy | Precision | Recall | F1-Score |
|--------------------------|----------|-----------|--------|----------|
| Traditional (CVIPtools)  | 85.59%   | 81.59%    | 90.00% | 85.59%   |
| Deep Learning (CNN + ViT)| 96.0%    | 97.0%     | 96.0%  | 97.0%    |

---


## 🧠 Citation

> Md Sami Ul Hoque, Al Mahmud, Thien Huu Nguyen, Syed Muhammad M Raza, Robert Leander, and Scott Umbaugh.  
> _Comparative Analysis of Traditional Thermographic Image Processing and Deep Learning Models for Canine Bone Cancer Detection_,  
> SPIE Defense + Commercial Sensing, 2024.

---

## 🙏 Acknowledgments

Special thanks to **Dr. Scott Umbaugh** and the **CVIP Lab** at Southern Illinois University Edwardsville for guidance and support throughout this research.

---
