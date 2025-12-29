## 🔗 Related Repository

This frontend consumes a live forecasting API deployed separately.

- **Backend API Repository:**  
  [https://github.com/SOUJITH-JADI/yellowstone-visitation-api](https://github.com/JADI-SOUJITH/yellowstone-visitation-api)

  # Yellowstone National Park Visitor Forecaster

An end-to-end machine learning project that predicts monthly visitor counts for Yellowstone National Park using historical data from the U.S. National Park Service.

The project demonstrates a complete ML workflow — from data modeling and API deployment to a live, production-ready web interface.

---

## 🔍 Problem Statement

National parks experience strong seasonal variation in visitor demand.  
Accurately forecasting future visitation helps with:

- Staffing and resource planning
- Infrastructure and maintenance scheduling
- Managing environmental pressure during peak months

This project forecasts **future monthly visitor counts** based purely on historical visitation patterns.

---

## 📊 Data Source

- **Dataset:** U.S. National Park Service – Monthly Recreation Visits  
- **Period:** 1979–2024  
- **Granularity:** Monthly  
- **Park:** Yellowstone National Park  

---

## 🤖 Model & Approach

- **Model:** Holt-Winters Exponential Smoothing (ETS)
- **Seasonality:** 12 months
- **Why ETS?**
  - Captures trend + strong seasonality
  - Interpretable and well-suited for time-series forecasting
  - Outperformed naïve baselines using MAE and RMSE

The model learns repeating seasonal patterns and long-term trends directly from historical data.

---

## 🌐 System Architecture

[ Frontend (HTML/CSS/JS) ]
↓
Fetch API (JSON)
↓
[ FastAPI Backend (Render) ]
↓
[ Trained ETS Model ]


---

## 🖥️ Live Demo

- **Frontend:** Deployed on Netlify  
- **Backend API:** Deployed on Render  

Users can:
- Select a forecast horizon (1–12 months)
- View live forecast results instantly
- See derived insights such as peak month and average demand

---

## 📈 Output & Insights

From the forecasted values, the application derives:
- Peak predicted month
- Lowest predicted month
- Average monthly visitors
- Peak vs average percentage increase

These insights are computed directly from model output.

---

## ⚠️ Limitations

- Forecasts rely only on historical visitation data
- External factors (weather, wildfires, policy changes) are not included
- Sudden structural changes cannot be predicted

---

## 🚀 Future Improvements

- Include weather and economic indicators as exogenous variables
- Add confidence intervals around forecasts
- Support multiple national parks

---

## 🛠️ Tech Stack

- **Modeling:** Python, statsmodels
- **Backend:** FastAPI
- **Frontend:** HTML, CSS, JavaScript, Chart.js
- **Deployment:** Render + Netlify
