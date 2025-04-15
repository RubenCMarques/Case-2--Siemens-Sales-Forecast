# Case-2 Siemens Sales Forecast

## Introduction  
This project focuses on developing a sales forecasting model for Siemens using historical sales data. By leveraging data science techniques, we aim to create a predictive model that provides accurate sales estimates, helping Siemens optimize decision-making and resource allocation. The dataset spans 2.5 years of sales records, and our approach involves exploratory data analysis (EDA), feature engineering, and the application of machine learning models to enhance forecast accuracy.  

## Project Overview  
In a complex and data-driven world, accurate forecasting of sales is essential to ensure operational efficiency, resource allocation, and strategic decision-making. Being a global leader in technology and innovation, Siemens wants to introduce artificial intelligence into the heart of its business. To this end, the present project seeks to develop a sales forecasting model for Siemens' Smart Infrastructure business unit in Germany based on past sales data and macroeconomic variables to improve forecast accuracy and business performance.
The main objectives were to create a robust, automated forecasting pipeline capable of delivering monthly sales predictions per product category, include external economic variables, and evaluate model performance using RMSE, time efficiency, and responsiveness. The project aimed to reduce human bias and enhance Siemens' forecasting processes with scalable machine learning approaches.
Through a systematic CRISP-DM process, the team preprocessed and cleaned historical sales data and macroeconomic factors. SARIMA was applied to forecast economic factors, while various algorithms were tried for sales forecasting. Among these, XGBoost with hyperparameter optimization achieved the lowest average RMSE across categories and was therefore the better performing model overall. However, inconsistencies in preprocessing, especially missing values between the training and test sets, highlighted the need for further refinement before the model can be reliably deployed.
To move forward, it is recommended to finalize and standardize the preprocessing pipeline, automate data integration and retraining processes, and deploy the forecasting model into Siemens' internal environment using a batch deployment strategy. 
In short, the project has immense potential for AI application in sales forecasting at Siemens. With certain improvements, the model can be a useful tool, facilitating data-driven decision-making, optimizing resource allocation, and assisting Siemens in realizing its broader digital transformation goals.

## Dataset  
- **Source**: Sales data provided by Siemens.
- **Time Period**: 2.5 years  
- **Features**: 1) date records which are daily transactions in dd.mm.yyyy format, 2)  the product category for each transaction, and 3) sales revenue in euro per transaction
