# EMS_PREDICTIONS

## The Data
The Data for this project was collected from multiple sources. Firstly a dataset of all 8.5 million NYC EMS calls between the years 2013 and 2018 was downloaded from NYC Open Data (https://opendata.cityofnewyork.us/). NYC Open Data is a government website that provides various datasets about NYC ranging from EMS calls to Political campaign contributions. In addition various weather features were scraped from (https://www.wunderground.com/) using selenium. 

## The Goal
The goal of this project was to be able to predict how many EMS calls, in each borough, will occur so resources can be better made availbile.

## Exploritory Data Analysis 
While analysing this data a few interesting occurances poped out. Manhattan and Bronx both have the most EMS calls per capita per day. This makes sense for Manhattan Thousands of people commute to the city for work, so while the Medical Emergencies get counted towards Manhattan dispatches, their per capita are counted at their residences. 


In addition, Two Sample T-Tests, showed that while rainfall equaling 2 inches or less does not have a statistically signifigant effect on the number of EMS calls, as well as the fact that days considered to be US federal holidays do signifigantly reduce the amount of Medical Emergency calls that day.



Anova tests showed that there is a reduction of calls on weekends opposed to weekdays. While there is seasonality, the seasons themselves have very little effect on the variance in the EMS calls, (in terms of being summer or spring, AKA. School seasons) but that it is the tempeture itself that is responsible for the variance in calls. 

## The Models
