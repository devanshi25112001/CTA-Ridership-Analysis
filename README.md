# CTA Ridership Analysis

## 📌 Project Overview

This project analyzes the impact of **COVID-19 on Chicago Transit Authority (CTA) ridership** and develops forecasting models to predict ridership recovery post-pandemic. Using **time series models**, the project assesses ridership patterns and provides insights to help in **capacity planning and resource allocation**.

## 🔍 Problem Statement

The **COVID-19 pandemic** significantly reduced public transit ridership, affecting **operational planning** for CTA. As ridership trends recover, accurate forecasting models are needed to **optimize resources** and maintain efficiency.

## 👥 Team Members

- **Devanshi Ledwani**
- **Nethra Subramanian**
- **Devon Delgado**
- **Karan Mehta**
- 
- 
## 📊 Dataset Information

- **Source:** [City of Chicago Data Portal](https://data.cityofchicago.org/Transportation/CTA-Ridership-Daily-Boarding-Totals/6iiy-9s97/about_data)
- **Time Period:** January 2001 – March 2024
- **Key Features:**
  - `Service Date`: Date of operation
  - `Total Boardings`: Combined bus and rail ridership
  - `Bus Boardings`: Daily CTA bus boardings
  - `Rail Boardings`: Daily CTA rail boardings
  - `Day Type`: Weekday, Saturday, or Sunday/Holiday

## 🛠 Data Preprocessing

- **Removed 62 duplicate rows**
- **Ensured chronological ordering** for accurate analysis
- **Handled missing values and outliers appropriately**
- **Future Feature Engineering:**
  - Hourly breakdowns for **rush-hour analysis**
  - Incorporating **external factors** like weather and major events

## 🎯 Hypotheses & Assumptions

1. **COVID-19 significantly impacted ridership**, causing a steep decline.
2. **Post-pandemic recovery will be gradual**, with changes in commuter behavior.
3. **Weekdays have the highest ridership**, followed by Saturdays, then Sundays/Holidays.
4. **Ridership exhibits strong seasonality**, including daily, weekly, and yearly patterns.

## 📈 Models Implemented

### 🔹 **Causal Impact Model**
- Assesses **statistical significance of COVID-19’s impact** on ridership.
- Finds a **52% decrease in ridership** post-pandemic.
- Rides started declining as early as **May 2013**, coinciding with the rise of **Lyft** and **Uber**.

### 🔹 **Holt-Winters Model**
- Captures **trend, level, and seasonality** for post-COVID forecasts.
- Shows a **gradual ridership recovery with seasonal fluctuations**.

### 🔹 **Prophet Model**
- **Pre-COVID:** Steady increase in ridership until **2015**, followed by a decline.
- **Post-COVID:** **Sharp drop in 2020**, then gradual recovery with lower weekday peaks.

### 🔹 **TBATS Model** (⏫ Best Performing Model)
- Captures **multiple seasonal patterns** (weekly, monthly, yearly).
- Handles **changing seasonal amplitudes** over time.
- **Outperforms other models in accuracy**.

### 🔹 **ARIMAX Model with Fourier Multi-Seasonality**
- Models **weekly and annual seasonality** using Fourier series.
- Uses **intervention regressor** to model COVID-19 effects.
- Captures **logarithmic decay of pandemic impact** on ridership.

## 🔬 Model Performance (First Two Months of 2024)

| Model       | RMSE       | MAE        | MAPE (%) |
|------------|------------|------------|------------|
| **Holt-Winters** | 196,500  | 154,658  | 26.33% |
| **Prophet** | 123,438  | 103,872  | 19.4% |
| **TBATS** | **136,913**  | **112,943**  | **16.74%** |
| **ARIMAX** | 171,792  | 126,585  | 23.5% |

✅ **TBATS Model performed the best** due to its **robust multi-seasonality handling** and **trend adaptability**.

## 🔑 Key Findings

- **CTA ridership will take years to fully recover**, with fluctuations due to external factors.
- **TBATS model provided the most accurate forecasts** for CTA ridership trends.
- **Future improvements can include external regressors** like weather, fuel prices, and major events.

## 🚀 Future Work

- **Enhance feature engineering** (hourly aggregates, external factors).
- **Improve intervention analysis** by refining regressor selection.
- **Explore deep learning models** (LSTMs, Transformers) for advanced forecasting.



---

