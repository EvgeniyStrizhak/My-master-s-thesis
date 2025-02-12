# Development of a Machine Learning Model for Predicting the Frankfurt Stock Exchange (GDAXI) Index Using Macro-Economic Indicators

**(The project is still in progress)**

This project predicts future month price of the Frankfurt Stock Exchange (GDAXI) index by using some machine learning models.

**Project structure:**

- Row_datasets folder contains sources of data which is used by machine learining models
- Data_pre_processing.ipynb downloads macroeconomic indicators from Bundesbank [database](https://www.bundesbank.de/) and GDAXI index, process them and merge into one dataframe and upload into row_datasets folder
- The_project.ipynb contains data analysis and model training

**The result**:

The random forest regression model has shown the best result so far. The average error of 577\$ is 5.8% of the average price of 9941\$ per share in this period. This result is possibly unsatisfactory and requires improvement.
