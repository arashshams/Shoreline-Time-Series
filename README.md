# Shoreline-Time_Series

This repo hosts a Time Series modeling for prediction of the [Tairua Beach](https://www.findabeach.co.nz/beaches/tairua/about/) (located in New Zealand) shoreline.

The idea for this work stems from a modeling competition (The M4 Competition) where you can find more about in the paper by Makridakis et al. found [here](https://www.sciencedirect.com/science/article/pii/S0169207019301128#!).

For more details on the modeling, please refer to the [Kaggle Kernel](https://www.kaggle.com/arashshamseddini/forecasting-tairua-beach-shoreline).

## Dataset
The dataset in this study is the monthly records of the beach shoreline from a datum. The data are split into two part.

**Training data:** which covers a 15-year range (1999 - 2013, inclusive)  of the records. This is used to build and calibrate the Time Series model. Next, the model is used to make predictions for the next 3 years and these are compared with `Test data` (`True observations`).

Below is a sneak peek at the `Training data`.
![dataset](./Images/dataset.png)

**Test data:** aka **True observations** this covers the 3-year range (2014 - 2016, inclusive).

Below is a sneak peek at the `Test data`.
![dataset](./Images/dataset.png)

## Modeling

Several models have been built which include:

- Adjusted naive
- ETS (AAM) 
- ARIMA
- SARIMA
- RandomForest

As seen in the below plot, SARIMA model has the best performance compared to others. This model is next used to make predictions.
![dataset](./Images/dataset.png)

## Forecasting

The plot below, shows the predictions from SARIMA model and compares it with `True observations`.
![dataset](./Images/dataset.png)

Obviously, forecasts are close to `True observations` so that the lines are not practically distinguishable.

## Conclusions
- Several models including (`Adjusted naive`, `ETS (AAM)`, `ARIMA`, `SARIMA`, `RandomForest`) were built and their performances were evaluated using the 15-year data (1999 - 2013, inclusive) of which `SARIMA` model came out as the winner. 
- `SARIMA` model was used to make predictions for the next 3 years (2014 - 2016, inclusive) where predicted values were compared with the test data (true observations). Results show that the predictions are significantly close to the true observations of those 3 years. 
- There is always room for improvement in this analysis and while building a prefect model is not the intention of this work the main goal is to follow a solid workflow in building a Time-Series model.

