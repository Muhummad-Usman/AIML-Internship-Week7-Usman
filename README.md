# 🧠 AI/ML Internship — Week 7: Deep Learning Model Comparison (CIFAR-10)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3+-orange?logo=scikit-learn)
![Week](https://img.shields.io/badge/Week-7%20of%208-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 👤 Student Information

- **Name:** Usman Asif  
- **Date:** 14th June, 2026  
- **Program:** AI/ML Internship — Digitech Offerings  
- **Instructor:** Zain Ul Abideen  

---

# 📌 Project Overview

This project focuses on **image classification using deep learning** on the CIFAR-10 dataset. The main objective is to build, train, and compare three different deep learning approaches to understand how architecture complexity impacts performance.

Three models were implemented:

1. Dense Neural Network (Baseline Model)
2. Convolutional Neural Network (CNN from scratch)
3. MobileNetV2 (Transfer Learning)

The project includes full pipeline development: data preprocessing, exploratory data analysis (EDA), model training, regularization techniques, data augmentation, transfer learning, evaluation metrics, and final deployment comparison.

---

# 📊 Dataset Information

| Property | Detail |
|---|---|
| Dataset | CIFAR-10 Image Dataset |
| Source | TensorFlow / Keras Built-in |
| Samples | 60,000 images |
| Train/Test Split | 50,000 / 10,000 |
| Image Size | 32 × 32 × 3 (RGB) |
| Classes | 10 object categories |

### Classes:
airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck

---

# ⚙️ Data Preprocessing & EDA

- Normalized pixel values to range [0, 1]
- Flattened images for Dense Network (3072 features)
- Resized images to 96×96 for MobileNetV2
- Converted labels into categorical format
- Visualized sample images for each class
- Analyzed class distribution (balanced dataset)
- Computed channel-wise mean and standard deviation
- Applied histogram analysis for RGB channels

---

# 🤖 Models Implemented

## 1️⃣ Dense Neural Network (Baseline)
- Input: Flattened 3072 features
- Layers: Dense → Dropout → Dense → Output Softmax
- Limitation: No spatial feature learning

## 2️⃣ CNN (Custom Architecture)
- Conv2D + MaxPooling layers
- Batch Normalization applied
- Dropout regularization
- Learns spatial patterns (edges, textures, shapes)

## 3️⃣ MobileNetV2 (Transfer Learning)
- Pretrained on ImageNet
- Feature extractor frozen in Phase 1
- Fine-tuned last 30 layers in Phase 2
- Uses Global Average Pooling + Dense classifier

---

# 🏆 Best Model Performance

Best Model: **MobileNetV2 (Fine-Tuned)**

- Test Accuracy: **~93%**
- Macro F1 Score: **~0.93**
- ROC-AUC: **~0.99**
- Fast convergence with transfer learning

### Final Comparison:

| Model | Accuracy | Macro F1 | ROC-AUC | Params |
|------|---------|----------|--------|--------|
| Dense Network | ~55% | 0.54 | 0.82 | ~1.7M |
| CNN (Regularized) | ~86% | 0.85 | 0.96 | ~2.5M |
| MobileNetV2 | ~93% | 0.93 | 0.99 | ~2.6M |

---

# 📉 Regularization & Optimization Techniques

- Dropout (0.25–0.5)
- Batch Normalization
- EarlyStopping
- ReduceLROnPlateau
- Data Augmentation:
  - Rotation (15°)
  - Width/Height Shift
  - Zoom
  - Horizontal Flip

---

# 📁 Repository Structure

AIML-Internship-Week7-UsmanAsif/

- Week7_Final_Notebook.ipynb
- week7_dashboard.png
- week7_best_model.keras
- README.md

---

# 📊 Project Dashboard

The dashboard includes:

- Training & validation accuracy curves
- Confusion matrix heatmap
- Per-class accuracy comparison
- ROC curves for all models
- Misclassified image visualization
- Final model comparison charts

📌 Dashboard Screenshot:

<img width="5370" height="6483" alt="week7_dashboard" src="https://github.com/user-attachments/assets/ce8206c2-5de1-4861-99f3-5bbab82e7ca2" />


---

# 📈 Key Findings

- CNN significantly outperforms Dense Network due to spatial feature learning
- Batch Normalization stabilizes and speeds up training
- Data augmentation reduces overfitting and improves generalization
- Transfer learning provides the highest performance with minimal training
- Fine-tuning improves accuracy further by adapting pretrained features

---

# 🧠 Key Insights

- Flattening images destroys spatial relationships → poor Dense performance
- CNN learns hierarchical patterns (edges → textures → objects)
- MobileNetV2 transfers knowledge from large-scale ImageNet dataset
- Regularization is essential for avoiding overfitting in CNNs
- Learning rate must be reduced during fine-tuning

---

# 🛠 Tools & Technologies

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

# 📊 Evaluation Metrics

- Accuracy
- Macro F1 Score
- ROC-AUC (One-vs-Rest)
- Confusion Matrix
- Classification Report
- Training Time Comparison

---

# 🚀 Deployment Recommendation

**MobileNetV2 is recommended for deployment because:**

- Highest accuracy (~93%)
- Best generalization performance
- Strong transfer learning capability
- Efficient inference for production systems
- Balanced tradeoff between speed and accuracy

---

# 🔍 Key Learnings

- CNNs are essential for image data
- Transfer learning dramatically improves performance
- Regularization prevents overfitting
- Data augmentation improves robustness
- Fine-tuning pretrained models boosts accuracy

---

# 🚀 Future Improvements

- Experiment with EfficientNet or ResNet
- Hyperparameter optimization (Optuna / Keras Tuner)
- Real-time deployment using Streamlit
- Model compression (quantization)
- API deployment using Flask/FastAPI

---

# 👤 Author

**Usman Asif**  
AI/ML Internship — Digitech Offerings  

Instructor: Zain Ul Abideen  

---

# ⭐ Final Conclusion

This project demonstrates a complete deep learning workflow from baseline modeling to advanced transfer learning. The results clearly show that **MobileNetV2 with fine-tuning provides the best performance**, making it the most suitable model for real-world deployment in image classification tasks.
