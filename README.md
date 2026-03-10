## 🔋 Energy-Efficient Appliance Demand Forecasting

## 📌 Project Overview
Accurate demand forecasting is essential for optimizing inventory allocation and long-term product strategy in the energy-efficient appliance market.
This project analyzes 30+ years of historical demand data and compares multiple time-series forecasting models — ARIMA, SARIMA, SARIMAX, and Prophet — to determine the most reliable approach for balancing operational forecasting precision with strategic business insights.
The analysis highlights how model selection and external business drivers influence forecasting accuracy and strategic decision-making.

--- 

## 🔍 Problem
Existing demand forecasting systems face a critical challenge:
- Simplistic models lack predictive accuracy.
- Complex models may fail to produce actionable business insights.

This creates a forecasting paradox:
⚖️ Balancing short-term operational precision (inventory planning) with long-term strategic insight (product and market strategy) is difficult.

As a result, organizations risk:
- Inventory inefficiencies
- Stock-outs or overstocking
- Missed opportunities for strategic product planning

---

## ⚙️ Methodology

1️⃣ Strategic Forecast Model Design
Developed a demand forecasting pipeline using 30+ years of monthly demand data, designed to support both:
- Operational forecasting accuracy
- Long-term strategic planning

2️⃣ Data Preparation & Exploratory Analysis
- Cleaned and processed 30+ years of historical demand data.

Performed time series decomposition to analyze:
 - Long-term trend
 - Seasonal patterns
 - Residual noise

--- 

📊 Historical demand visualization revealed clear seasonality and trend components.

--- 
📈 Historical Demand Analysis

<p align="center"> <img src="HISTORICAL_DEMAND_PLOT.png" width="700"> </p>

Figure 01: Time Series Forecast with Trend and Seasonality (1990–2023)

--- 

3️⃣ Baseline & Seasonal Modeling (ARIMA / SARIMA)
- Built baseline statistical models to capture temporal dependencies.

Models tested:
 - ARIMA(1,1,1)
 - SARIMA(1,1,1)(1,1,1,12)

Model evaluation:
 - SARIMA AIC: 2824.8
 - SARIMA BIC: 2844.7
 - SARIMA provided stronger performance by capturing seasonal demand cycles.
   
4️⃣ Strategic Feature Integration (SARIMAX)
Tested external variables to evaluate their influence on demand forecasts.
 - Implemented SARIMAX models with dummy sine proxies
 - External variable results:
   - Coefficient ≈ 0
   - p-value ≈ 1.0
  
💡 Key Insight:
Artificial proxies were statistically insignificant, highlighting the importance of real business-relevant external drivers (e.g., energy policy incentives, seasonal promotions, weather patterns).

--- 
📊 SARIMAX Forecast Visualization

<p align="center"> <img src="SARIMAX_FORECAST.png" width="700"> </p>

<p align="center"> Figure 02: SARIMA(1,1,1)(1,1,1,12) Forecast with Exogenous Variable</p>

---

5️⃣ Comparative Modeling (Prophet)
Evaluated Prophet to assess its ability to capture complex trend and seasonality patterns.
Comparison showed that while Prophet provides flexible modeling capabilities, SARIMA achieved significantly better predictive accuracy for this dataset.

---
## 📈 Results

📊 Forecast Performance Benchmark
| Model                              | MAE   | RMSE  |
| ---------------------------------- | ----- | ----- |
| SARIMA                             | 7.71  | 8.51  |
| SARIMAX (dummy exogenous variable) | 7.71  | 8.51  |
| Prophet                            | 22.83 | 23.77 |

---
## 📏 Quantified Performance Benchmarks
- Established clear evaluation benchmarks using MAE and RMSE metrics, enabling structured comparison across forecasting approaches.
- These benchmarks support future model optimization and performance tracking.

## 🧠 Strategic Business Insights
The analysis revealed that:
- External variables must represent real business drivers to improve forecast accuracy.
- Dummy proxies provide no meaningful predictive improvement.

This insight highlights the importance of incorporating variables such as:
- Energy efficiency incentives
- Market policy changes
- Seasonal promotion cycles
- Economic indicators
  
## 🏗 Scalable Forecasting Framework
Delivered a modular and scalable forecasting pipeline capable of:
- Integrating new external variables
- Updating models with new demand data
- Supporting inventory planning and strategic forecasting
- The framework is adaptable for multiple product categories and long-term demand planning.

---

## 🛠 Tech Stack

### 🐍 Python
| Category               | Tools                                         |
| ---------------------- | --------------------------------------------- |
| Data Processing        | pandas, numpy                                 |
| Time Series Modeling   | statsmodels (ARIMA, SARIMA, SARIMAX), Prophet |
| Visualization          | matplotlib                                    |
| Performance Evaluation | sklearn.metrics (MAE, RMSE)                   |

---

## 🚀 Key Skills Demonstrated
- Time Series Forecasting
- ARIMA / SARIMA / SARIMAX Modeling
- Forecast Model Evaluation
- Demand Forecasting Strategy
- Statistical Modeling
- Business-Driven Data Science
- Inventory Optimization Analytics
