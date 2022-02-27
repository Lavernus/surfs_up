# Analysis of Oahu Temperature Trends
## Overview
The client has provided an SQLite database containing weather data on the island Oahu. Using this data, they want an analysis on the weather data of the June and December months. This will determine the year-round sustainability of a business that relies heavily on the pleasantness of the weather, and affect the client's decision on whether to invest in such a business.
### Purpose

Utilizing python, this analysis will generate summary statistics on the weather of all June and December months contained within the SQLite database. This will be used to compare the two months and predict the success of a business tied to pleasant weather. 

## Results
Generating summary statistics using the **.describe()** function on June and December temperatures in degrees fahrenheit produced two tables. The table for June appeared as this:

![June_summ.png](https://github.com/Lavernus/surfs_up/blob/main/Add_Resources/June_summ.png)

and the table for December appeared as this:

![Dec_summ.png](https://github.com/Lavernus/surfs_up/blob/main/Add_Resources/Dec_summ.png)

While both of these tables are, overall, similar, it is important to address three key differences.
- Minimum and Maximum Temperatures
    - The minimum temperature for June is 64 degrees and the maximum temperature is 85 degrees. The December temperatures are at 56 degrees for the minimum and 83 degrees for the maximum.
- Lower and Upper Quartile
    - The lower quartile for June lies at 73 degrees, while its upper quartile is at 77 degrees. For December, the lower quartile is at 69 degrees and the upper quartile is at 74 degrees.
- Mean and Median
    - The mean for June is 74.94 degrees and the median is 75 degrees. For December, the mean is 71.04 degrees and the median is 71 degrees.

## Summary
The first area to address is the minimum and maximum temperatures. Obviously, the June minimum and maximum temperature lie within a range that is optimal for business success. The minimum temperature of December, however, is much lower than June's. Being in the 50's is not optimal weather for the success of the business. The maximum temperature of December is promising, however, at 83 degrees. This shows that the temperature in the winter is still capable of being balmy enough to encourage business success. 

The lower and upper quartile range are perhaps the most important in determining business success. While the min and max temperatures display the range of temperatures, the upper and lower quartiles display the spread of the temperatures within that range. The medians of the lower quartile and the upper quartile of June are very close together in the mid 70s, showing that while the minimum is in the 60s, most of the month is spent in a very pleasant range for business. December has a similar occurance that, while lower, its upper and lower quartile medians are around the low 70s, which is still pretty good for business. This also implies that the 56 degree minimum is not a regular occurance, which is promising.

Finally, the mean for June and its median are extremely close together, which shows an even distribution of temperatures across the month. This means that most of the time, the temperature is in the sweet spot for business being around 75 degrees. The mean and median for December are similarly almost identical and not that much lower than June's. This implies that we can expect weather to be similar if slightly lower between December and June, which could be extrapolated to mean that not much weather fluctuation occurs over the year.

### Additional Queries
Another area to explore is the precipitation occuring across June and December. Rainfall will most likely mean no business for those days, so knowing the daily rainfall for both June and December could give an idea of how many sunny days there actually are to conduct business. 

It would also be a good idea to observe the spread of temperatures and precipitation across the stations they are being measured in. It could be, due to geographical location and other environmental considerations, that some stations experience higher rainfall or lower temperatures than other stations. Creating a query that could average each stations temperature and precipitation could give an idea of an area of the island that would be better for business due to better weather. 