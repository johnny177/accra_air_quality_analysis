# Accra, Ghana Air Quality Data Exploration and AR Modelling
## by John Ametepe Agboku

## Dataset
The Accra Air Quality data was accessed from openDataAfrica. Each month's data from Nov 2019 to March 2021 was  accessed via the download urls from the openDataAfrica site. The data was concantenated into one dataframe using the pandas library. The total number of entries are 23,528. With 7 features that is 
1. sensor_id
2. sensor_type
3. location
4. lat
5. lon
6. value_type
7. value
8. timestamp

The value and timestamp are the features that are relevant for this analysis and modelling. Thus the other features except for lon and lat were dropped. The value column was renamed to P2 beacuse it is more descriptive. The timestamp column was converted into datime dtype and was then converted to Africa/Accra timezone. Then the data was resampled to 1 hour average window.


## Summary of Findings
From my investigations, i found out that, during the periods of the COVID pandemic were locked down was imposed, the PM2.5 readings decreased drastically and by rule of thumb, is due to the low emission of gases and other industrial and commercial activities that leads to the pollution the air were being halted or decreased. Thus, during the periods of March 2020 to June 2020, there was low PM2.5 readings. 
However, as activities begun to resume from early December 2020, the PM2.5 spiked showing that, the industrial and commercial activities can be the major causes of the decrease in air quality in Accra Ghana because it has most of the production companies situated there and there are alot of commercial activities that go on there and this is due to tehe fact that it is the Capital city of Ghana.

## Key Insights 
There is only one feature in this data set that was relevant to this analysis.
So i focused on finding periods where there are spikes or downturns in the PM2.5 readings.
By visualizing the PM2.5 readings, i found out that the periods of low Pm2.5 readings coincide with the periods of COVID pandemic. To get a clear insight of the trend, i rolled the data into a weekly average. 


