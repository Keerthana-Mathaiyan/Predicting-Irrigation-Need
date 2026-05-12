
# 🌱 Irrigation Need Prediction using Machine Learning

A machine learning project to predict **irrigation requirements (Low, Medium, High)** using soil, crop, and environmental data. This project uses **XGBoost** for multi-class classification and applies feature engineering to improve predictive performance.

## 📌 Project Overview

Efficient irrigation management is essential for sustainable agriculture. This project predicts the level of irrigation needed based on factors such as:

- Soil characteristics
- Weather conditions
- Crop information
- Previous irrigation history

The goal is to help optimize water usage and support smart farming decisions.

---

## 📂 Dataset

Dataset used from Kaggle:

**Playground Series - Season 6, Episode 4**  
Irrigation Need Prediction Competition

### Features Included

#### Soil Data
- Soil_Type
- Soil_pH
- Soil_Moisture
- Organic_Carbon
- Electrical_Conductivity

#### Environmental Data
- Temperature_C
- Humidity
- Rainfall_mm
- Sunlight_Hours
- Wind_Speed_kmh

#### Crop & Farm Data
- Crop_Type
- Crop_Growth_Stage
- Season
- Irrigation_Type
- Water_Source
- Field_Area_hectare
- Mulching_Used
- Previous_Irrigation_mm
- Region

### Target Variable
- **Irrigation_Need**
  - Low
  - Medium
  - High

---

## ⚙️ Methodology

### 1. Data Preprocessing
- Removed unnecessary `id` column
- Encoded categorical variables using **One-Hot Encoding**
- Encoded target labels using **LabelEncoder**

### 2. Feature Engineering
Created additional features to improve model learning:

- **Water_Balance**  
  `Rainfall_mm + Previous_Irrigation_mm`

- **Temp_Humidity**  
  `Temperature_C × Humidity`

- **Moisture_Index**  
  `Soil_Moisture × Humidity`

### 3. Train-Validation Split
- 80% training
- 20% validation
- Stratified split to preserve class balance

### 4. Model Training
Used **XGBoost Classifier** for multi-class prediction.

### 5. Model Evaluation
Evaluated using:

- Accuracy Score
- Precision
- Recall
- F1 Score
- Classification Report

### 6. Feature Importance Analysis
Visualized the most influential features affecting irrigation prediction.

---

## 🛠 Technologies Used

- Python
- Pandas
- Scikit-learn
- XGBoost
- Matplotlib
- Kaggle Notebook

---

## 📈 Results

The model successfully predicts irrigation requirements with strong validation performance and identifies key agricultural factors influencing irrigation demand.

---

## 🚀 How to Run

```bash
git clone <your-repository-link>
cd irrigation-prediction
pip install -r requirements.txt
python irrigation_prediction.py
```

---

## 📁 Output

The script generates:

- Model evaluation metrics
- Feature importance graph
- `submission.csv` for Kaggle competition submission

---

## 🌍 Future Improvements

- Hyperparameter tuning
- Ensemble learning
- Streamlit web application
- Real-time weather API integration
- Smart irrigation recommendation dashboard

---

## 👩‍💻 Author

Keerthana 

Machine Learning Project | Smart Agriculture | Irrigation Prediction

Kaggle project - ([S6E4-irrigation needed](https://www.kaggle.com/code/keerthanamathaiyan/s6e4-irrigation-needed
))
