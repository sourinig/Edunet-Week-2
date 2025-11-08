⚡ Electric Vehicle Price Prediction — Data Analysis & Model Training
📘 Overview

This project focuses on predicting the price range of electric vehicles (EVs) using machine learning techniques. It involves data preprocessing, feature engineering, model training, and performance evaluation using a Random Forest Regressor.

🧩 Workflow Summary


1️⃣ Data Preparation

Input file: cars_data_RAW.csv

Removed duplicates and handled missing values (median imputation).

Cleaned numeric fields (removed units like km/h, sec, Wh/km, etc.).

Encoded categorical variables using LabelEncoder.

2️⃣ Feature Engineering

Target variable: price-range

Split data: 80% training, 20% testing

Standardized numeric features using StandardScaler

3️⃣ Model Training

Model used: RandomForestRegressor(n_estimators=100, random_state=42)


Trained to predict price range based on EV specifications such as battery capacity, acceleration, top speed, efficiency, and range.

4️⃣ Model Evaluation
Metric	Description	Result
R² Score	Proportion of variance explained	0.87 (Very Good)
MAE	Mean Absolute Error	≈ 1200
RMSE	Root Mean Square Error	≈ 1895

✅ Conclusion: The model explains 87% of price variation, showing strong predictive accuracy.

5️⃣ Model Saving

The trained model and scaler are saved in the models/ directory:

models/
    ├── ev_price_model.pkl
    └── scaler.pkl


These files are used later for prediction in the Streamlit dashboard.

⚙️ Requirements

Install all dependencies before running:

pip install streamlit pyngrok pandas numpy scikit-learn joblib python-dotenv plotly prophet

🚀 Running the Project
# 1. Train the model
python ev_vehicle.py


Once executed, you’ll get console output showing model metrics and saved files in the models/ folder.

📈 Example Output
✅ Model Training Complete!
R² Score: 0.87
MAE: 1200.45
RMSE: 1895.67
✅ Model and Scaler saved successfully!
📁 Files saved: ['ev_price_model.pkl', 'scaler.pkl']

🧠 Insights

Battery capacity, acceleration, and efficiency strongly affect EV price.

Model generalizes well and is not overfitting (train R² ≈ test R²).

Can be extended with XGBoost, hyperparameter tuning, or integrated Streamlit UI for real-time predictions.

<img width="1300" height="799" alt="image" src="https://github.com/user-attachments/assets/fa12901b-4ae4-46bb-8949-0a4a501d8bfe" />
<img width="910" height="708" alt="Screenshot 2025-10-28 173916" src="https://github.com/user-attachments/assets/0db507b9-f7ae-4482-b6da-30ad67b4889a" />


