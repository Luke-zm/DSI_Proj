# Analysis of Singapore monthly weather on PV Generation

---

### Problem Statement

> * Weather is an important part of our daily lives. The rainfall, sun shine hours, temperature etc., both reflects what we did to the environment and also affects how we go about our daily lives. Some seemingly unconnected things may seem correlated. Some correlation may happen by pure chance.  
So looking at the weather data of Singapore, as a data analyst, I am interested to know:  
- Does the Straits Time Index (STI) value at the end of every month have any correlations at all?  
- If so, did they happen by pure chance?  

---

### Background

STI value and weather may seem very far fecthed, but they might actually be correlated.  
This is because of 3 points:  
 - Firstly, [economic activities and energy consumption are very closely tied together](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9328951/).  
 - Secondly, [energy consumptions/ transports are very closely tied to carbon/ greenhouse gas production](https://www.epa.gov/ghgemissions/sources-greenhouse-gas-emissions#:~:text=Human%20activities%20are%20responsible%20for,over%20the%20last%20150%20years.&text=The%20largest%20source%20of%20greenhouse,electricity%2C%20heat%2C%20and%20transportation.).  
 - Thridly, [greenhouse gases causes climate change, which causes extreme weather patterns](https://earthjustice.org/features/how-climate-change-is-fueling-extreme-weather).  

My goal for this project it to examine the weather features, and if they have any possible, none random relationship with the STI value.  


---

### Data Used

|Feature|Type|Dataset|Description|
|---|---|---|---|
|year|int64|all data source|The year the data is captured|
|month_in_yr|int64|all data source|The month the data is captured|
|open|float64|[Historical data: Straits Times Index - Singapore](https://stooq.com/q/d/?s=%5Esti&c=0&d1=19821228&d2=20230130&l=11&i=m)|Opening price of STI on the last day of the month
|high|float64|[Historical data: Straits Times Index - Singapore](https://stooq.com/q/d/?s=%5Esti&c=0&d1=19821228&d2=20230130&l=11&i=m)|Closing price of STI on the last day of the month
|low|float64|[Historical data: Straits Times Index - Singapore](https://stooq.com/q/d/?s=%5Esti&c=0&d1=19821228&d2=20230130&l=11&i=m)|Lowest price of STI on the last day of the month
|close|float64|[Historical data: Straits Times Index - Singapore](https://stooq.com/q/d/?s=%5Esti&c=0&d1=19821228&d2=20230130&l=11&i=m)|Highest price of STI on the last day of the month
|no_of_rainy_days|int64|[rainfall-monthly-number-of-rain-days](https://data.gov.sg/dataset/rainfall-monthly-number-of-rain-days)|Number of rainy days in month with rainfall >= 0.2mm|
|total_rainfall|float64|[rainfall-monthly-total](https://data.gov.sg/dataset/rainfall-monthly-total)|Total rainfall in a month in mm| 
|mean_sunshine_hrs|float64|[sunshine-monthly-mean](https://data.gov.sg/dataset/sunshine-duration-monthly-mean-daily-duration)|Mean daily sunshine hrs in a month|
|mean_temp|float64|[monthly-surafce-air-temp-mean](https://data.gov.sg/dataset/surface-air-temperature-monthly-mean)|The monthly mean air temperature in Degree Celsius|
  
    
*For detailed description, check the source via hyperlink  
**Datasets from hyperlink might be updated  

#### Provided Data

There are 5 datasets included in the [`data`](./data/) folder for this project. These correponds to weather information and STI information. 

* 1 [`rainfall-monthly-number-of-rain-days.csv`](./data/rainfall-monthly-number-of-rain-days.csv): Monthly number of rain days from 1982 to 2022. A day is considered to have “rained” if the total rainfall for that day is 0.2mm or more.
* 2 [`rainfall-monthly-total.csv`](./data/rainfall-monthly-total.csv): Monthly total rain recorded in mm(millimeters) from 1982 to 2022.
* 3 [`sunshine-monthly-mean.csv`](./data/sunshine-monthly-mean.csv): Monthly data of daily mean sunshine hours in hours from 1982 to 2022.
* 4 [`monthly-surafce-air-temp-mean.csv`](./data/monthly-surafce-air-temp-mean.csv): Monthly average of surface air temperature.
* 5 [`sti_m.csv`](./data/sti_m.csv): The value of Striats Time Index on the last day of the month. (https://stooq.com/q/d/?s=%5Esti&c=0&d1=19821228&d2=20230130&l=11&i=m)

Sources:
1 to 4 from [Data.gov.sg](https://data.gov.sg/)
5 from [website](https://stooq.com/q/d/?s=%5Esti&c=0&d1=19821228&d2=20230130&l=11&i=m)

---

### Results and conclusions

The data quality from the various sources are very clean, with no missing data located in the datasets themselves.  
There ammount of data avaliable is limited by the ammount of STI values obtained from online sources.   
A total of 419 data point, starting from Dec 1987, ending at Pct 2022 is generated.  
This dataset contains a 4 weather features, as well as 4 features indicating how the STI performed at the very last day of the month.  

Most of these features shows a large degree of normal distribution amongst values for that feature.  
Number of rainy days per month, sunshine hours and mean daily temperature for the month showed distinct characteristics for each month.  
For example, hottest months are May and June, coldest months are Nov, Dec.   
This trend also happens to correspond with the rain datas.   


Also, perhaps the most interesting finding in this project is the correlation between `mean_temp` and `sti_end_month`.  
They have a pearson's r value of 0.18, and a p value of less than 0.05 for both 2 tailed and 1 tailed test.  
This proves that they are somewhat correlated. The possible explanations were ellaborated in the additional analysis section.

Other possible relationships were also throughly examined and visual display of the results can be found in datat visualisation section.  

---
### Thank you
