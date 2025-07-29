# 🏦 Bank Customer Deposit Prediction - Data Quest 2025

> This project aims to build a predictive model to classify whether a bank customer will subscribe to a term deposit product. It was developed as part of the **Data Quest 2025 Competition** by Data Science Indonesia.

All steps are performed in one notebook: `Modeling_Notebook_All.ipynb`

---

## 🧭 Project Roadmap

| Step              | Content                                       |
|-------------------|-----------------------------------------------|
| **01 - EDA**       | Exploratory Data Analysis (light only)       |
| **02 - Preprocess**| Cleaning & Feature Engineering               |
| **03 - Modeling**  | Model Training & Tuning                      |
| **04 - Evaluate**  | Metrics, ROC Curve, Learning Curve           |
| **05 - Ensemble**  | Voting Ensemble from all tuned models        |
| **06 - Evaluate**  | Final Comparison & AUC Summary               |

---

## 🧹 Data Cleaning & Feature Engineering

- Replaced `999` with `-1` in `hari_sejak_kontak_sebelumnya`
- One-hot encoded **low-cardinality categorical columns**
- Mapped ordinal & binary categorical columns to numeric
- Used **CatBoostEncoder** for `pekerjaan` (high cardinality)
- Ordinal encoded `bulan_kontak_terakhir` and `hari_kontak_terakhir`
- Performed **feature engineering**
- Dropped **highly correlated features**
- Selected **top 20 features** based on feature importance

---

## ⚖️ Imbalanced Target Handling

The target variable is imbalanced. To address this, we applied `class_weight='balanced'` in model training.

![Imbalanced Target](https://github.com/user-attachments/assets/a06743e9-68f4-4ae9-971e-4c0f16c3281d)

---

## ⚙️ Modeling & Evaluation

Models Trained:
- **XGBoost**
- **LightGBM**
- **Gradient Boosting Classifier**
- **CatBoost**

Each model was tuned using Optuna search, and performance was evaluated using AUC, ROC curve, and learning curve.
<img width="989" height="690" alt="image" src="https://github.com/user-attachments/assets/e2619ba1-df5c-46cb-b240-5b2f183ac90d" />
<img width="1389" height="990" alt="image" src="https://github.com/user-attachments/assets/d7510aa3-c0a0-494a-9b9d-b6c3ecfcee30" />

---

## 📊 Model Comparison

Performance comparison of all individual models:

![Model Comparison](https://github.com/user-attachments/assets/f86ac8cb-caec-4b54-bd20-4e54e104c66d)

---

## 🔗 Ensemble Voting

The best performance was achieved using a **Soft Voting Ensemble** combining all four models.

<img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/d1722020-d872-464d-a54e-acf54ce08815" />

---

## 📁 How to Use

- Open `Modeling_Notebook_All.ipynb`
- No extra setup needed. All steps from preprocessing to evaluation are included.
- Competition: **Data Quest 2025 - Data Science Indonesia**

---

## 📌 Notes

- Focused on building strong models, less emphasis on in-depth EDA.
- Notebook-based workflow for reproducibility and clarity.

