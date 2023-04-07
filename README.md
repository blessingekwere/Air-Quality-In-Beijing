# Air-Quality-In-Beijing
### Impact of weather Conditions on Air Quality

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/Beijing_Picture_2.jpg)
###### photo Source: Google

## Introduction
Beijing is the capital city of the People's Republic of China and was formerly known as Peking. It is the world's most populous city with an estimated population of over 21 million residents. The city is located in the northern part of China and covers an area of 16,500 square kilometers.
In the past few years, air pollution problem in China, especially Beijing, has been so severe that it has received widespread attention from all over the world. Cities are dense areas of economic activities, and therefore, populations, and Beijing is the political and economic center of China. After a stage of radical pursuit of economic growth, improving air quality and overall living environment is the current focus of China's realization of green development. Therefore, it is important to study Beijing's air quality issues to find ways to tackle air pollution problems and provide a reference for other cities.

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/Into_Pics2.jpg)
###### photo Source: Google

## Air quality basics
Air quality refers to the degree to which the air is suitable or clean enough for humans or the environment.
Good air quality means the air is free of harmful substances. Air quality is rated using air quality categories (AQC) which rate the amount of pollution in the air based on airborne concentrations of major pollutants - the higher the AQC rating, the poorer the air quality.

It has been reported that air quality categories (AQC) based on visibility and 6 major airborne pollutants:
* ground-level ozone
* carbon monoxide
* sulfur dioxide
* nitrogen dioxide
* particulate matter as PM10 and PM2.5.

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/Into_Pics1.jpg)
###### photo Source: Google


## Data Sourcing
The data was downloaded in a comma separated value (csv) format from a website. It is made up of 13 columns and 43,824 rows. The link to the dataset can be found here. The columns are
. No - Row Number
. Year - Year of the data in the row
. Month - Month of the data in the row
. Day - Day of the data in the row
. Hour - Hour of the data in the row
. pm2.5 - pm2.5 concentration
. DEWP - Dew Point
. TEMP - Temperature
. PRES - Pressure (hpa)
. cbwd - Combined Wind Direction
. Iws - Cumulated wind speed (m/s)
. Is - Cumulated hours of snow (hours)
. Ir - Cumulated hours of rain (hours)
The link to the dataset can be found [here](https://archive.ics.uci.edu/ml/datasets/Beijing+PM2.5+Data)

## Problem Statement
The air quality in Beijing is a major concern due to high levels of particulate matter 2.5 (PM 2.5) pollution, which poses serious health risks to the population. Despite efforts to reduce emissions and improve air quality, PM2.5 levels in Beijing remain consistently high, particularly during winter months when coal burning increases. To better understand the sources and drivers of PM2.5 pollution in Beijing, there is need for an analysis of the air quality data and identification of key factors contributing to the persistent high level of pollution

Having known all of these, let's now take a look at the air quality data in Beijing to draw insights and help make informed decisions. Amonst the questions to be answered in this project are:
* What is the total pm2.5 of combined wind direction (cbwd)
* What the total hours of rainfall of combined wind direction (cbwd)
* What is the prediction on pm2.5 value in air quality in the next five years?
* What is likely to be the total hours of rainfall in the next five years?
* Which season, month and year recorded the highest Pm2.5?

## Tools Used: Power BI and Power Query Editor

## Skills Demonstrated
The skills recorded in the course of carrying out this project are
* Data Cleaning, Transformation and manipulation
* Data Analysis Expression (DAX)
* Data Visualization

## Data Transformation
* To begin the data transformation, I launched the Power BI interface and used the get data command to import the data as a Text/CSV file.

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/Picture_1_Lauching_PowerBI.png)
#### Getting Data as Text/ CSV

* I then clicked the transform button to load the data into power query editor.

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/Picture_2_Loading_Into_PowerQuery.png)
###### Loading the data into power query editor

* I used the first rows as headers.

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/Picture_3.png)
###### Before setting first rows as headers

* I then selected the year, month, and day columns, clicked on merge columns, used hyphen as a delimiter to separate the values and then I renamed the column to full date and formatted it to date type.

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/Picture_4.png)
###### Merging Year, Month and Day column to full date column

* I noticed that the pm2.5 column had "N/A" as values, which I replaced with Zero(0) using the replace value command.

* The NE in cbwd column was replaced with North-East, while the NW and SE were replaced with North-West and South-East respectively. I then replaced the "cv" in cbwd column to South-West, since it might have been a data entry error.

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/Picture_6.png)
###### Replacing the values in cbwd column


* I then proceeded to convert the pressure column from hectopascal (hpa) to atmospheric pressure (atm) using the custom column command.

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/Picture_9.png)
###### Converting the values of pressure from hpa to atm

*  I also used the conditional column command to add a column named "season". I also used the conditional column command to add a column named "season".

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/Picture_7.png)
###### Using conditional column command to add a new column called season

* The season column was grouped as follows:

December to February was called winter.

March to May was called Spring.

June to August was called Summer.

September to November was called Autumn.

* After this, the data was then loaded into Power BI for further analysis and Power query was 

## Analysis and Visualization

* Looking at all combined wind direction and the total amount of pm2.5, it is observed that South East had the highest average of PM2.5 with a total of 120.20 µg/m3, followed by South West with a total of 105.623 µg/m3, North West and North East had a total of 85.83 µg/m3 and 63.83 µg/m3 respectively.

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/Pics_1.png)
###### Total Hours of Rain by Combined Wind Direction

* Comparing the four combined wind directions, it can be seen that North West had the highest number of hours of rainfall with a total of 3755 hours, followed by South East with a total of 1792 and North East and South West had a total of 1642 and 1353 hours of rainfall respectively.

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/pics_3.png)
###### Average PM2.5 by Combined Wind Direction

* Comparing the total amount of PM2.5 across the years, January 2013 had the highest amount of PM2.5 with about 191.97 µg/m3 and January 2011 recorded the lowest amount of pm2.5 with 40.55 µg/m3.

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/Pics_2.png)
#### Average PM2.5 by Month and Year

* Considering pm2.5 across all seasons, the analysis showed that PM2.5 was highest in winter season with 28.44% followed by Autumn with 26.35%.

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/pics_6.png)
#### Percentage of PM2.5 across all seasons

* I carried out a prediction of pm2.5 for the next five years which is from 2015 to 2019, and the analysis 2015 will have a pm2.5 of 96.10 µg/m3, 2016 will have a pm2.5 of 90.84 µg/m3, while 2017, 2018 and 2019 will have a pm2.5 value of 85.51 µg/m3, 100.76 µg/m3 and 96.63 µg/m3 respectively.

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/pics_4.png)
###### Prediction of Average PM2.5 for the next five years

* I also carried out a prediction of the total hours of rainfall for the five years and it showed that in 2015 the total hours will be 2347, in 2016 the total hours will be 1231, in 2017 the total hours will be 2366 and in 2018 and 2019 the hours of rainfall will be 1410 and 1188 hours respectively.

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/pics_5.png)
###### Prediction of the total hours of rainfall for the next five years


* From the analysis, it showed that as the hours of snow increased, there was also an increase in the average amount PM2.5 though not a steady increase, the number of hours it rained remained zero when the number of hours it snowed increased except for the increase in hours that it rained when it only snowed for two hours. This means that there is likely to be an increase in PM2.5 after it rains than during the rain. This is because rain can help wash out PM2.5 particles from the atmosphere effectively removing them from the air we breathe because rain captures the particles and pulls them down to the ground.

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/pics_7.png)
###### Analysis of how snow hours and average rainfall hours affects PM2.5

* The analysis also showed that pm2.5 kept increasing with temperature though not on a steady increase, while dew point kept reducing until the temperature got to 10 degrees Celsius then the dew point began to increase. This is likely because higher temperatures can accelerate chemical reactions that produce PM2.5 particles. Also, when dew point is high, it can help trap PM2.5 particles in the air rather than being dispersed and this is because water droplets can act as a surface for particles to adhere to.

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/pics_8.png)
###### Analysis of how Dew Point and Temperature affects Pm2.5

![](https://github.com/blessingekwere/Air-Quality-In-Beijing/blob/main/Air%20Quality_page-0001.jpg)
###### Air Quality In Beijing Dashboard


## Conclusion and Recommendation
In conclusion, Beijing has been known to face severe air quality problems due to various activities such as industrial activities, transportation and coal-based energy production. To address these problems a few recommendations I will make are:
* Enforcing stricter regulations on industrial emissions, and incentivizing companies to adopt cleaner production methods.
 
* Raising Public awareness of the health risks associated with air pollution and encouraging individuals to take steps to reduce their own emissions.

* Collaborating with other countries and international organizations to share best practices and technologies for improving air quality.

* Promoting renewable energy sources and phasing out coal-based energy production.

Finally, while there have been some positive developments in improving air quality in Beijing, there is still much work to be done to address the issue. It will require the commitment and cooperation of stakeholders, from government and industry to individuals, to make a meaningful difference in reducing air pollution and improving the health and well being of the city's residents.

Kindly find the link to the Power BI report [here](https://drive.google.com/file/d/1uxzMhN4wOh4V_5_slGPOB_PZ7uqQWCDk/view?usp=share_link)

Thank you for reading this article. I sincerely appreciate

Kindly share your thoughts, recommendations and comments.
💜









