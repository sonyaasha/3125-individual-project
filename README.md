# Global Climate Change
#### 3125 Individual Project
#### Sofia Toropova

## Introduction

The project was undertaken to analyze the impacts of temperatures rising on the sea ice extent levels. Also, it was interesting to see how the public support of climate change actions impact the contributions of each country to environmental initiatives. 

The objecticve of the project is to examine the impact of global temperature change on various aspects of natural life. For example, the melting down of sea ice. However, other impact include the change in economics and social influence. 

Three questions were taken into consideration and answered to further the objective analysis of the global climate change:

1. How have the anomalies in temperature impacted the sea ice extent?
2. What effect has flooding have on the economy in China? And how drastic was that effect?
3. What countries have showcased over 70% of support for climate emergency action? And did that support result in action? 

## Selection of Data

Most data comes from Statista datasets from the following sources:
-  [Sea Ice Extent](https://www.statista.com/statistics/1299082/northern-hemisphere-sea-ice-extent/)
-  [Temperature Anomalies](https://www.statista.com/statistics/224893/land-and-ocean-temperature-anomalies-based-on-temperature-departure/)
- [Economic Loss from Floods in China 2022](https://www.statista.com/statistics/1118042/china-economic-loss-from-natural-disasters/)
- [Weather Catastrophes Causing Economic Losses Globally](https://www.statista.com/statistics/818411/weather-catastrophes-causing-economic-losses-globally/)
-  [Public Support](https://www.statista.com/statistics/1201071/climate-emergency-public-support-globally-by-country/)
- [Green Bonds](https://www.statista.com/statistics/1090928/green-bonds-issuance-volume-europe/#statisticContainer)

The data includes the calculated statistics from 1900s to 2023. 

Before utilizing the data, the excel files were modified for ease of use in the analysis. For example, overview pages were eliminated and some columns were shifted to provide a more comprehensive view of the data. Some features for the unnecessery years were modified to fit requirements of the analysis.

For the dataset [Economic Loss from Floods in China 2022](https://www.statista.com/statistics/1118042/china-economic-loss-from-natural-disasters/), the yuan data was converted to usd, so that the losses could be used in camparison with other datasets that are in usd. Used conversion rates as of April 1, 2023.

#### Data access preview

Data excel files are loaded to the Jupyter system, located in the same folder as the notebook, so that Panda's function read_excel() could be used to read in the files.

`sea_ice_extent_data = pd.read_excel("northern-hemisphere-sea-ice-extent-per-month-1980-2023.xlsx")`

The code snippet above demonstrates a way how the data files were accessed within the Jupyter Notebook.

`data_1980 = sea_ice_extent_data.loc[year]` 

The example above is the way to access data by year. By running the following snippet, we can see the month and the corresponding value of sea ice extent in million square kilometers.

To answer some questions, it is required to combine the data from [Sea Ice Extent](https://www.statista.com/statistics/1299082/northern-hemisphere-sea-ice-extent/) and [Temperature Anomalies](https://www.statista.com/statistics/224893/land-and-ocean-temperature-anomalies-based-on-temperature-departure/), therefore, we create lists to store the necessary information, and then parse the data into a Pandas DataFrame:

```
model_year.append(year)
model_temp_anomaly.append(temp_anom_2023)
model_average_sea_extent.append(average_sea_ice_extent_2023)
data = pd.DataFrame({'Year': model_year, 'Temperature Anomaly': model_temp_anomaly, 'Sea Ice Extent': model_average_sea_extent})
```

Other ways used to combine the datasets:

```
merged_df = pd.merge(green_bonds_data, public_support_data, on='Country', how='inner')
```
This way the two datasets are merged into one dataframe, and therefore, it makes it easier to visualize the data with plots.

## Methods
#### Tools:
- NumPy, Pandas for data analysis and inference
- Seaborn and Matplotlib.pyplot for data visualization
- GitHub for version control
- VS Code as IDE

#### Inference methods:
- best line fit on combined temperature anomaly and sea ice extent data to predict the trend for year 2030

## Results

## Discussion