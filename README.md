# 📦 Time Series Demand Forecasting using SARIMAX

## 📌 Project Overview
This project focuses on forecasting **monthly product demand** using **time series analysis**.  
Accurate demand forecasting is critical for **inventory planning, cost optimization, and supply chain efficiency**.

We implement a **SARIMAX (Seasonal ARIMA with Exogenous Variables)** model to capture:
- Trend
- Seasonality
- Temporal dependencies in demand data

This project is designed to reflect **real-world industry practices** used in retail and supply-chain analytics.

---

## 🎯 Business Problem
In real-world retail and supply-chain systems:
- Overstocking increases holding and storage costs
- Understocking leads to lost sales and poor customer experience

📉 **Objective:**  
Predict future demand accurately to enable **data-driven inventory decisions**.

---

## 🗂 Dataset Description
The dataset contains historical order demand data with the following attributes:

| Column | Description |
|------|------------|
| Product_ID | Unique product identifier |
| Product_Code | Product reference code |
| Warehouse | Warehouse location |
| Product_Category | Category of product |
| Date | Order date |
| Order_Demand | Quantity demanded |

📌 The data is **aggregated to monthly frequency** to enable time-series modeling.

---

## 🧹 Data Preprocessing
Key preprocessing steps:
- Converted date column to datetime format
- Aggregated order demand at **monthly level**
- Created a **synthetic monthly time index** (dataset had no native index)
- Applied **log transformation** to stabilize variance
- Ensured **time-aware train–test split** (80% train, 20% test)

---

## 🧠 Feature Engineering
- Monthly time index creation
- Variance stabilization using log transformation
- Preservation of temporal order (no random shuffling)

---

## 📈 Model Selection
### Why SARIMAX?
- Captures **trend and seasonality**
- Handles non-stationary data
- Widely used in **industry demand forecasting**

**Model Configuration:**
- ARIMA order: `(1,1,1)`
- Seasonal order: `(1,1,1,12)`
- Frequency: Monthly

---

## 📊 Model Evaluation
Model performance is evaluated using:

- **RMSE (Root Mean Squared Error)**
- Comparison against a **Naive Baseline Forecast**
- Visual inspection of forecast vs actual demand

📉 The SARIMAX model **outperforms the baseline**, indicating effective learning of demand patterns.

---

## 📉 Results Visualization
The following series are visualized:
- Last portion of training data (context)
- Actual test demand
- SARIMAX forecast

This provides a **clear aligned comparison** between actual demand and model predictions.

---

## 🚀 Business Impact
✔ Improved inventory planning  
✔ Reduced stockouts and excess inventory  
✔ Scalable forecasting framework  

This framework can be extended to:
- Product-level forecasting
- Warehouse-level forecasting
- Promotion-aware or holiday-aware demand forecasting

---

## 🛠 Tech Stack
- Python
- Pandas, NumPy
- Statsmodels (SARIMAX)
- Scikit-learn
- Matplotlib
- Jupyter Notebook

---

## ▶ How to Run
```bash
git clone https://github.com/<your-username>/project-4-time-series-demand-forecasting.git
cd project-4-time-series-demand-forecasting
pip install -r requirements.txt
jupyter notebook
open demand_forecasting_sarimax.ipynb

📌 Project Structure

project-4-time-series-demand-forecasting/
│
├── data/
│   └── demand_data.csv
│
├── notebooks/
│   └── demand_forecasting_sarimax.ipynb
│
├── README.md
├── requirements.txt

📌 Future Improvements
Walk-forward (rolling) validation
Incorporation of exogenous variables (promotions, holidays)
Model deployment as API or dashboard
Multi-product and multi-warehouse forecasting

⭐ Project Status
✅ Completed
🚀 Actively improving for production readiness


Author
Venkata Sandeep Kumar Reddy
Aspiring Data Scientist / Machine Learning Engineer
