# Unemployment Forecasting in India During COVID19
Oasis InfoByte Internship | Task 2

## Overview

This project analyzes and forecasts the unemployment rate in India, focusing on the impact of the COVID19 pandemic. Using time series modeling and exploratory data analysis (EDA), it highlights how lockdown measures and socioeconomic shifts contributed to employment fluctuations. The Prophet library was used for forecasting, enhanced with a custom `Post_covid` regressor and changepoints to better capture the pandemic's disruptive effects.

## Objectives

* Understand how COVID19 affected unemployment trends in India
* Measure changes in unemployment before and after lockdown periods
* Build a forecasting model that accounts for real-world disruptions
* Evaluate the accuracy of short- vs long-term forecasts

## Process Summary

* Cleaned and merged national and regional unemployment datasets into a monthly time series
* Introduced a binary `Post_covid` variable to reflect structural shifts caused by lockdown
* Performed exploratory data analysis to identify temporal unemployment trends
* Built and fine-tuned a Prophet model with changepoints and custom regressors
* Evaluated forecasting performance using cross-validation and key error metrics

## Key Insights

**Unemployment Spike**: The unemployment rate surged sharply in April 2020, coinciding with the first COVID19 lockdown. This marked the most significant disruption in the time series.

**Peak and Dip**: The rate peaked in May 2020, then began to decline around June, with a more noticeable drop by September. This suggests the job market was hit hard but started recovering within a few months.

**Sustained High Levels**: Even months after restrictions eased, unemployment did not return to pre-pandemic levels. This indicates lasting economic disruption and an incomplete recovery.

**Participation Drop**: Labour force participation declined from 43.9 percent before COVID to 38.1 percent after. Although job growth resumed, fewer people remained in the workforce, reflecting a shrinking labour base.

**National Impact**: The rise in unemployment post-COVID affected nearly all regions, showing that the economic shock was widespread.

These findings justified the use of changepoints and the `Post_covid` regressor in the forecasting model to capture the structural break in the data.

## Forecasting and Model Performance

We used Facebook Prophet to forecast unemployment, taking advantage of its ability to handle seasonality, changepoints, and custom regressors.

### Model Accuracy Metrics

* Mean Absolute Error (MAE): 7.03 – On average, predictions deviated from actual values by 7 percentage points
* Root Mean Squared Error (RMSE): 9.67 – Indicates larger errors have more impact, showing moderate volatility in forecasts

### Cross-Validation Findings

* Forecasts for short horizons around 28–29 days were the most accurate, with MAE between 6.1 and 9.4 and RMSE as low as 7.7
* Forecasts for longer horizons (e.g., 90 days) had higher errors, with MAE reaching 11.4 and RMSE rising to 16.57

## Tools and Libraries Used

Python (Pandas, Seaborn, Matplotlib, Prophet)
Jupyter Notebook
nbviewer.org for notebook presentation

## Conclusion

Overall, the model demonstrates reasonable accuracy for short-term unemployment rate forecasts, with lower errors at 28–29 day horizons. However, as the forecast horizon increases, the model’s performance declines, with higher MAE and RMSE values indicating reduced reliability for long-term predictions.

Additionally, the model struggled to capture sharp spikes during the COVID-19 period, due to:

* Limited dataset size, especially for pre- and post-COVID periods.

