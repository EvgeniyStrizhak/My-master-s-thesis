## Stock Price Prediction Using Macro Indicators with Machine Learning and Deep Learning Models
**(Project In Progress)**

This project aims to predict the monthly closing price of the Frankfurt Stock Exchange (GDAXI) index using a range of macroeconomic indicators. The prediction task is performed using several machine learning and deep learning models.

Project Structure
### [1. Data_Pre_Processing.ipynb](https://github.com/EvgeniyStrizhak/My-master-s-thesis/blob/main/Data_pre_processing.ipynb)
Composes the dataset from multiple sources, including Yahoo Finance and the Deutsche Bundesbank.

Downloads macroeconomic indicators from the Bundesbank database and the GDAXI index from Yahoo Finance.

Processes, cleans, and merges all datasets into a unified DataFrame.

Saves the output into the row_datasets/ folder for further use.

The [row_datasets folder](https://github.com/EvgeniyStrizhak/My-master-s-thesis/tree/main/row_datasets) contains the raw data sources used for model development.

### [2. Data_Analysis.ipynb ](https://github.com/EvgeniyStrizhak/My-master-s-thesis/blob/main/Data_Analysis.ipynb)
Performs exploratory data analysis (EDA) on the raw data.

Identifies key trends, correlations, and transformations required for model readiness.

Assesses the stationarity and seasonality of the GDAXI time series.

### [3. Data_Processing_and_Feature_Selection.ipynb](https://github.com/EvgeniyStrizhak/My-master-s-thesis/blob/main/Data_Processing_and_Features_Selection.ipynb)
Applies all necessary transformations identified in the EDA phase:

Trend removal

Differencing for stationarity

Scaling

Feature engineering (e.g., adding lagged values)

Performs feature selection using:

SelectKBest for top 15 features

PCA to reduce dimensionality to 10 components

Saves data in [processed_datasets foulder](https://github.com/EvgeniyStrizhak/My-master-s-thesis/tree/main/processed_datasets)

### [4. Model_Training.ipynb](https://github.com/EvgeniyStrizhak/My-master-s-thesis/blob/main/Model_Training.ipynb)
Trains and evaluates multiple models using Root Mean Squared Error (RMSE) as the performance metric:

Linear Regression – Baseline model

Random Forest – Outperforms baseline

XGBoost – Best-performing model overall

LSTM Neural Network – Suffers from overfitting due to limited data

ARIMA (ARIMAX) – Includes macro indicators, but performs poorly

### 5. Model Testing and Final Conclusion
The best performance was achieved by XGBoost, with an RMSE of 721.0 on the test set.

In comparison, Linear Regression resulted in a higher RMSE of 771.7, confirming the added value of nonlinear modeling.
