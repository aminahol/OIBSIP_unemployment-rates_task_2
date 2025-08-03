# Unemployment Rate Forecasting in India During COVID-19

A time series analysis project investigating the impact of COVID-19 pandemic on employment patterns across Indian states and regions, with forecasting using Facebook Prophet algorithm.

**[View Interactive Notebook](https://nbviewer.org/github/aminahol/OIBSIP_unemployment-rates_task_2/blob/fb74e27f62e08866c5cde1c358a92dd1eedb575d/Unemployment_%20Analysis%20_%20Task2.ipynb)**

## Objectives

- Analyze the impact of COVID-19 lockdowns on employment trends across India
- Quantify the magnitude and temporal progression of unemployment during pandemic peak
- Identify regional patterns in unemployment rates before and after COVID-19
- Develop time series forecasting model to predict future unemployment trends

## Dataset

The analysis combines two unemployment datasets covering Indian states from May 2019 to June 2020:
- **728 samples** across multiple states and regions after removing duplicates
- **Key features**: Unemployment Rate (%), Employed population, Labour Participation Rate (%)
- **Time periods**: Pre-COVID (May 2019 - March 2020) and Post-COVID (April 2020 - June 2020)
- **Geographic coverage**: All major Indian states grouped by regions (North, South, East, West)

## Methodology

### Data Preparation
- Merged two datasets to create comprehensive unemployment database
- Created binary COVID impact indicator using April 1, 2020 as threshold
- Calculated employment growth rates and categorized unemployment levels
- Cleaned data by removing duplicates and standardizing column names

### Exploratory Analysis
- **Temporal trends**: Line graphs showing unemployment evolution over time
- **Impact comparison**: Boxplots comparing pre and post COVID unemployment rates
- **Regional analysis**: Bar charts showing state and region-wise unemployment patterns
- **Employment dynamics**: Growth rate analysis across different time periods

### Time Series Forecasting
Used Facebook Prophet algorithm for unemployment rate prediction:
- **Changepoint identification**: Selected April 30, May 31, and June 30, 2020 as changepoints based on observed trend breaks in the line graph
- **External regressor**: Added Post-COVID binary variable to capture pandemic impact
- **Model validation**: Applied cross-validation with 180-day initial training period

## Results

### COVID-19 Impact
- **Unemployment doubled**: Average rate increased from 9.5% (pre-COVID) to 20.3% (post-COVID)
- **Sharp spike observed**: Peak unemployment occurred during April-May 2020 lockdown
- **Labour force reduction**: Participation rate dropped from 43.9% to 38.1%
- **Recovery pattern**: Employment growth resumed in most states post-lockdown

### Regional Findings
- **Universal impact**: All regions experienced significant unemployment increases
- **State variations**: Different recovery patterns observed across states
- **North region**: Showed highest average unemployment rates
- **Employment paradox**: Rising employment growth despite higher unemployment due to shrinking labour force

### Forecasting Performance
- **Model accuracy**: MAE of 7.03%, RMSE of 9.67%
- **Short-term reliability**: Best performance for 28-29 day forecasts
- **Limitation**: Model struggled with extreme volatility during acute pandemic phase
- **Trend capture**: Successfully identified overall recovery trajectory

## Key Insights

1. **Systematic Impact**: COVID-19 affected employment across all Indian states, not just specific regions
2. **Sharp Recovery**: Despite severe initial impact, employment showed signs of recovery by June 2020
3. **Changepoint Importance**: The line graph clearly revealed three critical transition periods that improved forecast accuracy
4. **Labour Market Dynamics**: Rising employment alongside higher unemployment indicates complex workforce participation changes

## Conclusion

The analysis successfully quantified COVID-19's severe impact on Indian employment markets. The Prophet forecasting model, enhanced with changepoints identified from temporal trend analysis, provides reasonable short-term unemployment predictions. 

The study reveals that while the pandemic created unprecedented job losses, the labour market showed resilience with recovery beginning within months. However, the reduced labour participation rate suggests lasting structural changes requiring continued monitoring.

The forecasting framework demonstrates how visual trend analysis can inform model design, with changepoints derived from line graph observations significantly improving prediction accuracy.
