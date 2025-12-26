# Time Series Demand Forecasting using SARIMA

## 📌 Project Overview
This project builds an end-to-end time series forecasting pipeline to predict monthly product demand using classical statistical models.

The workflow covers:
- Data cleaning & aggregation
- Time index engineering
- Train-test split (time-aware)
- Baseline comparison
- ARIMA / SARIMA modeling
- Model evaluation using RMSE
- Business-ready visualization

## 🧠 Key Concepts Used
- Time Series Analysis
- ARIMA / SARIMA
- Stationarity & transformations
- Forecast evaluation (RMSE)
- Time-aware train-test split

## 📊 Dataset
Transactional demand data aggregated into monthly demand per warehouse.

## 🏗️ Workflow
1. Load & clean data  
2. Aggregate demand monthly  
3. Create time index  
4. Baseline forecasting  
5. ARIMA / SARIMA modeling  
6. Forecast evaluation  
7. Visualization & insights  

## 📈 Results
- SARIMA model captures seasonality better than baseline
- Clear comparison between actual vs forecasted demand
- Ready for real-world supply chain planning

## 🛠️ Tech Stack
- Python
- Pandas, NumPy
- Matplotlib
- Statsmodels
- Scikit-learn

## 🚀 Future Improvements
- Auto-SARIMA tuning
- External regressors (promotions, holidays)
- Rolling-window forecasting
- Deployment as API

---