# EMS_PREDICTIONS

## The Data
The Data for this project was collected from multiple sources. Firstly a dataset of all 8.5 million NYC EMS calls between the years 2013 and 2018 was downloaded from NYC Open Data (https://opendata.cityofnewyork.us/). NYC Open Data is a government website that provides various datasets about NYC ranging from EMS calls to Political campaign contributions. In addition various weather features were scraped from (https://www.wunderground.com/) using selenium. 

## The Goal
The goal of this project was to be able to predict how many EMS calls, in each borough, will occur so resources can be better made availbile.

## Exploritory Data Analysis 
While analysing this data a few interesting occurances poped out. Manhattan and Bronx both have the most EMS calls per capita per day. This makes sense for Manhattan Thousands of people commute to the city for work, so while the Medical Emergencies get counted towards Manhattan dispatches, their per capita are counted at their residences. 

Call Per Population by Borough

![Call Per Population](https://github.com/kmcnicoll/EMS_PREDICTIONS/blob/master/Final_Project/download.png)


In addition, Two Sample T-Tests, showed that while rainfall equaling 2 inches or less does not have a statistically signifigant effect on the number of EMS calls, as well as the fact that days considered to be US federal holidays do signifigantly reduce the amount of Medical Emergency calls that day.


Holiday Distributions
![US Holiday](https://github.com/kmcnicoll/EMS_PREDICTIONS/blob/master/Final_Project/download-1.png)

Anova tests showed that there is a reduction of calls on weekends opposed to weekdays. While there is seasonality, the seasons themselves have very little effect on the variance in the EMS calls, (in terms of being summer or spring, AKA. School seasons) but that it is the tempeture itself that is responsible for the variance in calls. 


Days of the Week Boxplot
![day of week boxplot](https://github.com/kmcnicoll/EMS_PREDICTIONS/blob/master/Final_Project/download-2.png)



Another interesting discovery was that while decompositioning the data, it was discovered that there was an upwards trend of about 600 calls since 2013. This is slightly concering as the population of NYC has stayed stagnant over the years.

Decomposition for Trend, and Seasons
![decomposition graph, unscaled](https://github.com/kmcnicoll/EMS_PREDICTIONS/blob/master/Final_Project/download-3.png)

## The Models

Six Facebook Prophet Models were made. One for overall NYC as well as one for each Borough. Interestingly overall NYC model, during testing, preformed with and MSE of 2%, while individual Boroughs were between 4-8% MSE. Testing for these models were done by removing dates from the fitting and testing the proceding week to the data input.


## Future Applicaitons and Diving Deeper
Going forward this model can be used to prepare the nessicary resources in advance of the calls so enough Medical Providers and Ambulances are availible before each shift. Future depths of this project would be to predict the severity of the calls, as well as the number so the properly trained professionals can be made availible per location.
