# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) # Project 1 - Harnessing Weather Patterns to Identify Means to Optimise Households Energy Consumption by Town

## Project Objectives

Singapore’s climate is characterised by two main monsoon seasons separated by inter-monsoonal periods.  The **Northeast Monsoon** occurs from December to early March, and the **Southwest Monsoon** from June to September.

Weather can potentially impact energy consumption as usage patterns in response to weather conditions. 
By analysing the **relationship** between rainy days and energy consumption, we can identify opportunities to promote more efficient practices and optimise energy usage.


## Methodology

Step 1 : Analyse Monthly weather **pattern** in Singapore
Step 2 : Analyse **Relationship** between various monthly weather data
Step 3 : Analyse Energy consumption **pattern** per month across town in Singapore
Step 4 : Analyse **Relationship** between various monthly weather data
Step 5 : Analyse **Relationship** between various monthly weather data and energy consumption across town
Conclusion: Sharing **insights** that assists in decision making process for approach

---

## Data Used

* [`rainfall-monthly-number-of-rain-days.csv`](./data/rainfall-monthly-number-of-rain-days.csv): Monthly number of rain days from 1982 to 2022. A day is considered to have “rained” if the total rainfall for that day is 0.2mm or more.
* [`rainfall-monthly-total.csv`](./data/rainfall-monthly-total.csv): Monthly total rain recorded in mm(millimeters) from 1982 to 2022
* [Relative Humidity](https://data.gov.sg/dataset/relative-humidity-monthly-mean)
* [Monthly Maximum Daily Rainfall](https://data.gov.sg/dataset/rainfall-monthly-maximum-daily-total)
* [Hourly wet buld temperature](https://data.gov.sg/dataset/wet-bulb-temperature-hourly)
* [Monthly mean sunshine hours](https://data.gov.sg/dataset/sunshine-duration-monthly-mean-daily-duration)
* [Surface Air Temperature](https://data.gov.sg/dataset/surface-air-temperature-mean-daily-minimum)
* [`electricity_consumption_by_area_monthly.csv`](./data/electricity_consumption_by_area_monthly.csv): the csv file contains the Overall (both Public and Private Housing) Average Monthly Household Town Electricity Consumption by Planning Area from Jan 2005 to June 2022. Some of the more prominent areas are like Woodlands, Bishan, Tampines and Jurong West. 
* [`gas_consumption_by_area_monthly.csv`](./data/gas_consumption_by_area_monthly.csv): the csv file contains the Overall (both Public and Private Housing) Average Monthly Household Town Gas Consumption by Planning Area from Jan 2005 to June 2022. Some of the more prominent areas are like Woodlands, Bishan, Tampines and Jurong West.

The data above are abstracted from [Energy Market Authority (EMA)](https://www.ema.gov.sg/statistic.aspx?sta_sid=20140617E32XNb1d0Iqa).


## Data Dictionary

|Feature|Type|Dataset|Description|
|:---|:---|:---|:---|
|maximum_rainfall_in_a_day|float|df_max_dayrain|Maximum rainfall in a day in mm|
|no_of_rainy_days|Integer|df_num_days_rain|Total number of rainy days in a month|
|total_rainfall|float|df_sum_rain|Total rainfall in mm|
|mean_rh|float|df_humidity|Relative Humidity|
|mean_sunshine_hrs|float|df_sunshine|Mean number of hours Sun is out|
|mean_temp|float|df_mean_temperature|Mean temperature of the day in degree Celcius|
|wet_bulb_temperature|float|df_month_wet_bulb|Mean temperature indicated by a moistened thermometer bulb exposed to the air flow|
|Bishan|float|df_econsumption|Electricity Consumption in a month in kWh in Bishan Town|
|Bishan|float|df_gconsumption|Natural Gas Consumption in a month in kWh in Bishan Town|

---

## Key Takeaways from the Analysis

1. Total rainfall in a month and maximum rainfall in a day have strong positive correlation (r = 0.81).
2. Mean temperature and wet bulb temperature have strong positive correlation (0.775680).
3. 70% of the Towns in Singapore has high correlation in energy consumption behaviours, supported by its high correlations. (See the heatmap and correlation coefficients table in the code)
4. Selected Towns like Bukit Timah, Newton, Orchard, Paya Lebar, Seletar, Southern Islands, Tanglin and Sungei Kadut has unusually high average household consumptions.
5. Weather and Energy Consumption by Household does not have any significant relationship.

---

## Recommendations

#### 1. The recommendations from us will not be weather-dependent.
#### 2. Bukit Timah, Newton, Orchard, Tanglin and Southern Islands are
    - top target audience for energy consumption campaign
    - the campaign will be electricity consumption focused
#### 3. If a energy conservation strategy works in this area, due to the high correlation between energy consumption patterns across areas, the campaign can expand to island-wide.

---
### Citations

Source 1: https://www.ema.gov.sg/singapore-energy-statistics/Ch03/index3

Source 2: https://www.ema.gov.sg/Electricity.aspx

Source 3: https://www.coolgeography.co.uk/A-level/AQA/Year%2013/Weather%20and%20climate/Climate%20controls/Insolation%20and%20the%20atmosphere.htm#:~:text=The%20Northern%20Hemisphere%20receives%20its,receive%20no%20Insolation%20at%20all.

Source 4: https://en.wikipedia.org/wiki/Southern_Islands

Source 5: https://en.wikipedia.org/wiki/Seletar

Source 6: https://www.inspirecleanenergy.com/blog/sustainable-living/how-much-electricity-does-air-conditioning-use

Source 7: https://www.candy-home.com/en_GB/blog/how-much-electricity-does-a-washer-drier-consume/#:~:text=The%20average%20estimate%20is%20around,cycle%20(around%2090%20cents).

Source 8: https://news.energysage.com/how-many-watts-does-a-refrigerator-use/#:~:text=A%20home%20refrigerator's%20power%20consumption,and%20off%20throughout%20the%20day.