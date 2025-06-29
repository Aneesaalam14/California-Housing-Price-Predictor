# 🏠 California Housing Price Predictor

This project predicts median house values in California using machine learning models trained on the California Housing dataset.

---

## 📁 Dataset

- **Source**: [Downloaded from Kaggle](https://www.kaggle.com/)
- **File**: `housing.csv` (extracted from `archive.zip`)
- **Features**: 
  - `longitude`, `latitude`, `housing_median_age`, `total_rooms`, `total_bedrooms`, `population`, `households`, `median_income`, `ocean_proximity`
- **Target**: 
  - `median_house_value`

---

## 🔍 Workflow

### 1. Data Loading
- Loaded directly from ZIP using `zipfile` and `pandas`.

### 2. Data Exploration & Visualization
- Used `pandas`, `matplotlib`, and `seaborn`.
- Histograms, scatter plots, and correlation matrices created.

### 3. Data Preprocessing
- Handled missing values with `SimpleImputer`.
- Created new features: `rooms_per_household`, `population_per_household`, etc.
- Categorical encoding and feature scaling done with `StandardScaler`.

### 4. Model Training
- Models used:
  - Linear Regression
  - Decision Tree Regressor
  - ✅ Random Forest Regressor (best performance)

### 5. Evaluation
- Metrics: 
  - RMSE (Root Mean Squared Error)
  - MAE (Mean Absolute Error)

### 6. Deployment
- Built and deployed using **Streamlit**.
- Saved model and scaler with `joblib`:
  - `best_model.pkl`
  - `scaler.pkl`
- Streamlit app takes user inputs and predicts house price.

---

## ▶️ Running the Project
 Make sure you're in the project folder:

Install dependencies:
pip install -r requirements.txt

Run the app:

streamlit run app.py
