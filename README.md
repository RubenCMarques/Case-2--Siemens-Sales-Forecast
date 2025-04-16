# Siemens Sales Forecast

## Introduction  
This project focuses on improving sales forecasting accuracy for Siemens' Smart Infrastructure division in Germany using data science techniques. The objective is to develop a monthly sales forecasting model per product category, integrating macroeconomic variables to enhance accuracy, reduce bias, and support data-driven decision-making. Siemens previously relied on manual and judgment-based forecasts, which lacked scalability and consistency in volatile market conditions.

By applying machine learning and time series forecasting methods, we analyzed historical sales trends, macroeconomic indicators, and seasonal behaviors. XGBoost with hyperparameter optimization proved to be the most effective approach, outperforming classical time series models and delivering robust predictive performance.

---

## Table of Contents  
- [Project Overview](#project-overview)  
- [Dataset](#dataset)  
- [Methodology](#methodology)   
- [Results](#results)  
- [Deployment and Maintenance](#deployment-and-maintenance)  
- [Future Improvements](#future-improvements)  

---

## Project Overview  
Siemens aims to leverage artificial intelligence in its internal operations to improve forecast accuracy, reduce operational inefficiencies, and enhance planning decisions. The Smart Infrastructure business unit is an ideal use case, where product-level monthly sales predictions are essential for managing working capital and supply chain demands.

The key goals were:  
- Create an automated and scalable forecasting pipeline  
- Incorporate external economic indicators  
- Evaluate performance using RMSE and responsiveness  
- Reduce human intervention in forecasting  

---

## Dataset  
**Sales Data**  
- Source: Siemens Smart Infrastructure (Germany)  
- Period: October 2018 to April 2022  
- Features: Date, product category (14 total), and sales revenue per transaction  

**Macroeconomic Data**  
- Source: Public economic indicators  
- Period: February 2004 to April 2022  
- Features: Industrial indices, commodity prices, producer prices across countries (e.g., Germany, US, China)

---

## Methodology  
**Exploratory Data Analysis (EDA):**  
- Identified seasonality and cyclic trends  
- Revenue skewed towards top-performing products  
- Applied seasonal decomposition  

**Feature Engineering:**  
- Lag values (last month, last year)  
- Moving averages  
- Temporal indicators (month, quarter)  
- Macroeconomic feature deltas  
- Top 10 features per product selected using XGBoost  

**Modeling:**  
- SARIMA for macroeconomic forecasts  
- Prophet for baseline time series forecasting  
- XGBoost with and without hyperparameter tuning  
- Evaluation based on RMSE across 14 product categories  

---

## Results  
| Model                  | Average RMSE        |
|------------------------|---------------------|
| Prophet Vanilla        | 931,954.35          |
| Prophet + Features     | 2,698,845.85        |
| XGBoost                | 709,405.58          |
| **XGBoost Tuned**      | **703,202.77**      |

XGBoost with hyperparameter tuning was the most effective model overall. It handled nonlinearity, feature interaction, and external variables better than the alternatives.

---

## Deployment and Maintenance  
**Deployment Strategy:**  
- Batch deployment on a monthly basis  
- Integrated into Siemens’ internal systems  
- Forecasts delivered to BI tools for planning  

**Monitoring:**  
- Monthly RMSE evaluation  
- Retraining scheduled quarterly  
- Alerts for performance drops  
- Full version control for all deployments  

---

## Future Improvements  
- Finalize preprocessing and automate the pipeline   
- Expand feature set (e.g., marketing events, customer data)  
- Build visual dashboards for scenario planning  
