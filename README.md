# Surfs Up Analysis


## Overview of the analysis: Explain the purpose of this analysis.

After finishing the weather analysis, W. Avy needs further anaylis to determine temperature trends prior opening the shop. He is keen on analysing and understaning temperature data for the months of June and December in Oahu, in order to determine if the surf and ice cream shop business is sustainable year-round.

**Data exploration** includes writing queries for precipitation analysis, most active stations anlysis, temperature analysis, rainfall per weather station and daily noramls.

The purpose of our analysis is to see temperature statistics for June and December to see if running a surf shop is sustainable year around. The way we get the temperature data is by running two seperate queries, one being for June and the other being December. Once we run our queries we store the temperatures in a list then convert them to a dataframe. Once our dataframe is created we are able to get our summary statistics by using the **.describe() method**. 

**Resoucres Used for Analysis:** Python Pandas, SqlAlchemy, Matplotlib and Flask (VS Code editor), and Jupyter Notebook for presentation.

## Results:

For this analysis, W. Any needs to analyse the tredns in months of June and December. To enbale the analysis we will be utilizing climate analysis and data exploration of Hawaii climate sqlite database(Resources/hawaii.sqlite). 

![June Data](https://github.com/div1085/surfs_up./blob/c27816f67699afcfe45f1917a91e61d5ad3a7bf2/Resources/june%20temp.png). : ![Dec Data](https://github.com/div1085/surfs_up./blob/c27816f67699afcfe45f1917a91e61d5ad3a7bf2/Resources/dec%20temp%20.png).

1. The average temperature in Oahu during the month of June and December is almost similar (+/- 3°only)
2. The maximum temprerature in both the cities during June and December doesnt exceed 85°F historically.
3. However, the temprarture in December can go as low as 56°.

## Summary: Provide a high-level summary of the results and two additional queries that you would perform to gather more weather data for June and December.

According to the anaylsis above, the weather does not change significantly from June to Decemeber. These two additional queries are helpful to see how much rain they get in June and in Decemember:

As per the analysis above, the temprature during the months of June and December doesnt change that much, however, another consideration for the tourist will be the amount of rainfall receivied during those two months. We can insert queries on overview the presicipation recevied by the city speficifically in those months.

### As per the images below we can determine that 

  `June_prcp = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()
  list(June_prcp)`

##

  ``Dec_prcp = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()
  list(Dec_prcp)``


![June Data](https://github.com/div1085/surfs_up./blob/580b7339c692092baf5c6c599794e6e19f8e28cd/Resources/Screen%20Shot%202021-11-01%20at%208.52.47%20AM.png).: ![Dec Data](https://github.com/div1085/surfs_up./blob/6adf41820cf4d38eab0314b74d131ad3f5d2c753/Resources/Screen%20Shot%202021-11-01%20at%209.04.17%20AM.png).
