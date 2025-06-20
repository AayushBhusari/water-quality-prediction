# Multi-Output Regression for Water Quality Prediction

This project uses supervised machine learning to predict multiple water quality parameters using environmental sensor data. It leverages a `MultiOutputRegressor` wrapped around a `RandomForestRegressor` to simultaneously predict several dependent variables based on the rest.

---

## 📌 Problem Statement

Water quality monitoring involves measuring multiple chemical and physical parameters such as NH₄⁺, NO₃⁻, dissolved oxygen (O₂), and biochemical oxygen demand (BSK5). However, some of these parameters may be unavailable or hard to measure in real time.

This project aims to:

- Use the available parameters to **predict the missing ones**
- Build a robust machine learning pipeline for **multi-target regression**
- Allow flexible prediction of **any one or more parameters** using the remaining values

---

## 📊 Dataset

The dataset contains the following **9 parameters**:

```

['NH4', 'BSK5', 'Suspended', 'O2', 'NO3', 'NO2', 'SO4', 'PO4', 'CL']

```

At any time, **8 of these parameters can be used as input** to predict the remaining one.

---

## 🧠 Approach

- Used **MultiOutputRegressor** from `sklearn` with **RandomForestRegressor** as the base model
- Built a flexible system to:
  - Train a single model to predict all parameters
  - Train individual models for each parameter to allow modular deployment
- Evaluated using **R² score** and **RMSE** (Root Mean Squared Error)

---

## ⚙️ Tech Stack

- Python
- pandas, numpy
- scikit-learn
- matplotlib, seaborn (for visualization)
- joblib (for model persistence)

---

## 🔮 Future Work

- Add deep learning model for comparison
- Incorporate temporal data (if available)
- Build a user-friendly web dashboard using Streamlit or FastAPI

---
