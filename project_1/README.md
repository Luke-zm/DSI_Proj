# Analysis of Singapore monthly weather on PV Generation

---

### Problem Statement

> * Singapore is trying to decarbonize the electrical grid. Solar energy plays a major role in this initiative. Unfortunately, solar energy can be intermittent, due to cloud coverage and rainfall. Therefore, this project aims to analyse trends in Singapore weather to identify if rainny seasons in Singapore adversely affect the generation of energy using photovoltaic (PV) panels. This analysis can then help stakeholders, such as PV system owners, decide if they need to include other sources of energy.   

---

### Background

---

### Data Used

#### Provided Data

There are 6 datasets included in the [`data`](./data/) folder for this project. These correponds to rainfall information and PV Generation. 

* 1 [`rainfall-monthly-number-of-rain-days.csv`](./data/rainfall-monthly-number-of-rain-days.csv): Monthly number of rain days from 1982 to 2022. A day is considered to have “rained” if the total rainfall for that day is 0.2mm or more.
* 2 [`rainfall-monthly-total.csv`](./data/rainfall-monthly-total.csv): Monthly total rain recorded in mm(millimeters) from 1982 to 2022
* 3 [`sunshine-monthly-mean.csv`](./data/sunshine-monthly-mean.csv): Monthly data of daily mean sunshine hours in hours from 1982 to 2022
* 4 [`monthly_electricity_generated.csv`](./data/monthly_electricity_generated.csv): Monthly data of electricity generated in GWh from Jan 2009 to Sep 2022
* 5 [`monthly-plant-mix.csv`](./data/monthly-plant-mix.csv): Monthly percentage (%) of electricty generated using various sources.
* 6 [`quaterly-mwp-solar.xls`](./data/quaterly-mwp-solar.xls): Quaterly data on Mega Watt Peak (MWp) capacity of Singapore's PV systems connected to gird from 2009 to 2022 Q1.

Sources:
1 to 3 from [Data.goc.sg](https://data.gov.sg/):
* 1 [rainfall-monthly-number-of-rain-days](https://data.gov.sg/dataset/rainfall-monthly-number-of-rain-days)
* 2 [rainfall-monthly-total](https://data.gov.sg/dataset/rainfall-monthly-maximum-daily-total)
* 3 [sunshine-monthly-mean](https://data.gov.sg/dataset/sunshine-duration-monthly-mean-daily-duration)

4 to 6 from [EMA Statistics](https://www.ema.gov.sg/Statistics.aspx):
* 4 [monthly_electricity_generated](https://www.ema.gov.sg/TemStatistic.aspx?pagesid=20210218Z0Z6JYV1gayG&pagemode=live&sta_sid=20140802apItNJRIa9Pa)
* 5 [monthly-plant-mix](https://www.ema.gov.sg/statistic.aspx?sta_sid=20140802NEeM2zyMguvz)
* 6 [quaterly-mwp-solar](https://www.ema.gov.sg/statistic.aspx?sta_sid=20170711hc85chOLVvWp)

---

### Thank you
