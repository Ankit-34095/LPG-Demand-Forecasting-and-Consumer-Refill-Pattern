📌 Overview
This project addresses two problems:
- Demand Forecasting: Predict weekly LPG demand using historical data  
- Refill Prediction: Predict whether a customer will refill within the next "N" days where N can be any number. Here the value of N is 25 days.

The solution uses statistical, machine learning, and deep learning models.

🎯 Objectives
- Analyze LPG consumption patterns  
- Build forecasting models for demand prediction  
- Model customer refill behavior  
- Compare multiple algorithms for performance  

📁 Dataset
- File: Refill_Data_30L.csv  
- Description: LPG refill transaction dataset  

Key Features:
- OrderDate – Date of order  
- OrderQuantity – Quantity ordered  
- DistributorId – Distributor identifier  
- UniqueConsumerId – Customer identifier  

🧹 Data Preprocessing
- Handled missing values  
- Converted OrderDate to datetime format  
- Sorted data chronologically  
- Aggregated data for weekly analysis  

## ⚙️ Feature Engineering

Time Series Features
- Lag features: lag_1, lag_2, lag_4  
- Rolling mean: roll_4  
- Week-based features  

Customer Features
- Days since last refill  
- Previous refill gaps (Lag1, Lag2, Lag3)  
- Average refill interval  

🤖 Models Used

Regression (Demand Forecasting)
- Linear Regression  
- Random Forest Regressor  
- LightGBM Regressor  
- LSTM (Deep Learning)

Classification (Refill Prediction)
- Random Forest Classifier  
- Feed Forward Neural Network  

📊 Evaluation Metrics

Regression
- MAE (Mean Absolute Error)  
- RMSE (Root Mean Squared Error)  

Classification
- Accuracy  
- Precision  
- Recall  
- F1 Score  

📈 Results
- Tree-based models (Random Forest, LightGBM) perform better than baseline  
- LSTM captures temporal patterns but requires tuning  
- Lag-based features significantly improve prediction accuracy  

🛠️ Tech Stack
- Python  
- Pandas, NumPy  
- Scikit-learn  
- LightGBM  
- TensorFlow / Keras  
- Matplotlib  

📂 Project Structure
├── data/
├── notebooks/
│   └── demand_forecasting.ipynb
├── models/
├── README.md

🚀 Installation & Setup

1. Clone Repository

2. Install Dependencies
pip install pandas numpy scikit-learn lightgbm tensorflow matplotlib

3. Run Project
jupyter notebook

▶️ Usage
- Open the notebook  
- Run cells sequentially  
- View model outputs and evaluation metrics  

📌 Assumptions
- Historical patterns are indicative of future demand  
- No external factors (weather, holidays) included  
- Data is clean after preprocessing  

⚠️ Limitations
- Limited dataset size  
- No real-time deployment  
- Deep learning model not extensively tuned  

Future Work
- Hyperparameter tuning  
- Add external features (seasonality, weather)  
- Model deployment (Flask/FastAPI)  
- Real-time prediction pipeline  
