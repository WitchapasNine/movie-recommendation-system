# 🎬 Movie Recommendation System (DES431 Project)

## 📌 Overview
This project implements a **hybrid movie recommendation system** that predicts user ratings by combining two collaborative filtering methods:  
1. **Bias-Aware Matrix Factorization (Bias-MF)**  
2. **Item-Based Collaborative Filtering (Item-CF)**  

The final predictions are made using an **ensemble** (weighted average of MF and Item-CF), which improves accuracy over either model alone.

---

## 🚀 Features
- **Bias-Aware Matrix Factorization**
  - Models global average, user bias, item bias, and latent factors.
  - Learned via **Stochastic Gradient Descent (SGD)** with regularization.
- **Item-Based Collaborative Filtering**
  - Computes **cosine similarity** between movies.
  - Predicts ratings using top-k (k=20) nearest neighbors.
- **Ensemble Model**
  - Weighted combination of MF and Item-CF predictions.
  - Optimal weight chosen by minimizing RMSE on validation data.

---

## 📊 Results
Validation Root Mean Squared Error (RMSE):

| Model               | RMSE   |
|---------------------|--------|
| Baseline (mean)     | 1.007  |
| Bias-MF             | 0.870  |
| Item-CF             | 0.839  |
| **Ensemble (w=0.4)**| **0.811** |

✅ The ensemble reduced RMSE by ~20% compared to baseline.

---

## 🛠️ Tech Stack
- **Language:** Python  
- **Libraries:** NumPy, Pandas, Scikit-learn, Matplotlib  
- **Data:** Movie ratings CSVs (`ratings_train.csv`, `ratings_valid.csv`, `movies.csv`)

---

## 👥 Authors

Kanapitch Khamjorn

Witchapas Chotichaiyon

Kueakul Jongpermponwattana
