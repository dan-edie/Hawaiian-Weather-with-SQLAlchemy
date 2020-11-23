# Hawaiian Weather with SQLAlchemy

Using data from 9 separate NWS weather stations in Hawaii, an analysis of trends in precipitation and temperature were performed to determine if there was a meaningful difference in tempereatures in Hawaii between June and December. In addition, a specific date range was chosen, and a look at the normals in temperature and precipitation was made. 

The data was pulled and queried using SQLAlchemy. The data consisted of a full year of NWS data from specific Hawaiian stations.

Looking at an entire years worth of precipiation data, we see a few spikes in September, February, and March. We see several days where little to no precipitation occured. 
![The Precipitation levels measured in Hawaii over the course of an entire year.](https://github.com/dan-edie/Hawaiian-Weather-with-SQLAlchemy/blob/master/hawaii_precip_12_mo.png)

Querying the data, station USC00519281 was found to have the most data on record, with some 2772 data points. Using this station, the lowest temperature recorded was 51 degrees F, the average was 71.7 degrees F, and the highest temperature recorded was 85 degrees F, giving a range of 34 degrees F. 
![Temperatures recorded at the most active station](https://github.com/dan-edie/Hawaiian-Weather-with-SQLAlchemy/blob/master/temp_obvs.png)

Is there any meaningful difference in average temperatures in the summer and winter in Hawaii? Because two independent systems were used, an unpaired t-test was used to calculate the p-value. The p-value was essentially zero, thus the null hypothesis was rejected.

Next, a date range from 3 October to 17 October was chosen to examine the normal temperatures for this range. To do so, a few Python functions were written that used the date range to query and calculate the requested data. The results are givin in the table below.

| date  | tmin |   tavg    | tmax |
|-------|------|-----------|------|
| 10-03 |	66.0 | 76.730769 | 84.0 |	
| 10-04 |	67.0 | 75.862745 | 82.0	|
| 10-05 |	67.0 | 76.166667 | 84.0	|
| 10-06 |	70.0 | 75.420000 | 81.0	|
| 10-07 |	68.0 | 75.607843 | 81.0	|
| 10-08 |	66.0 | 76.326531 | 86.0	|
| 10-09 |	69.0 | 76.113636 | 84.0	|
| 10-10 |	69.0 | 75.854167 | 83.0	|
| 10-11 |	69.0 | 76.571429 | 84.0	|
| 10-12 |	65.0 | 75.755102 | 82.0	|
| 10-13 |	65.0 | 75.980392 | 84.0	|
| 10-14 |	67.0 | 75.192308 | 82.0	|
| 10-15 |	67.0 | 75.634615 | 82.0	|
| 10-16 |	67.0 | 75.591837 | 81.0	|
| 10-17 |	65.0 | 75.078431 | 83.0	|
|10-18	| 65.0 | 75.000000 | 83.0	|

The average temperature held steady, around 75 degrees F. The maximum was in the mid to low 80s, and the low temperatures mid to high 60s.
![The daily normal temperatures over a period of 14 days in October](https://github.com/dan-edie/Hawaiian-Weather-with-SQLAlchemy/blob/master/daily_normals.png)

The date range can be easily changed in the code to any other time and length. If one were to try and plan for a time to visit Hawaii, this would be useful to find the range of dates and times where temperatures are in averaged to a persons wants, and amount of precipitation is at a level where outdoor activities are possible.
