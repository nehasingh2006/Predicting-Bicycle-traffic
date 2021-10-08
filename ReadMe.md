# Predicting Bicycle Traffic

### Tags

Pandas, Visualization, RollingMean, GroupBy, PivotTable, TimeSeries, LinearRegression

### Credits

* [Python Data Science Handbook by Jake Vanderplas](https://amzn.to/2uApdah)  -- Key Source
  * [Section "Example: Visualizing Seattle Bicycle Counts" in Chapter 3](https://www.safaribooksonline.com/library/view/python-data-science/9781491912126/ch03.html#example-visualizing-seattle-bicycle-counts)
  * [Section "Example: Predicting Bicycle Traffic" in Chapter 5](https://www.safaribooksonline.com/library/view/python-data-science/9781491912126/ch05.html#example-predicting-bicycle-traffic)
* [A statistical analysis of biking on the Fremont Bridge - A 4 part series](https://www.seattlebikeblog.com/tag/a-statistical-analysis-of-biking-on-the-fremont-bridge/)  
* [(Blog by Jake Vanderplas) Is Seattle Really Seeing an Uptick In Cycling?](https://jakevdp.github.io/blog/2014/06/10/is-seattle-really-seeing-an-uptick-in-cycling/) 
* [(Blog by Jake Vanderplas) Learning Seattle's Work Habits from Bicycle Counts](https://jakevdp.github.io/blog/2015/07/23/learning-seattles-work-habits-from-bicycle-counts/)
* [How Does that Bike Counter work at the Fremont Bridge (and who named Fremont)?](http://sdotblog.seattle.gov/2016/02/25/how-does-that-bike-counter-work-at-the-fremont-bridge-and-who-named-fremont/)



### Objective

Understand Bicylers habits and make predictions



### DataSets Source

* [Seattle Gov - Data](https://data.seattle.gov)
  * [Transportation : Fremont Bridge - Hourly Bicycle Counts by the  month of October 2012 to present](https://data.seattle.gov/Transportation/Fremont-Bridge-Hourly-Bicycle-Counts-by-Month-Octo/65db-xm6k)
    * The Fremont Bridge Bicycle Counter records the number of bikes that cross the bridge using the pedestrian/bicycle pathways. Inductive loops on the east and west pathways count the passing of bicycles regardless of travel direction. The data consists of a date/time field: Date, east pathway count field: Fremont Bridge NB, and west pathway count field: Fremont Bridge SB. The count fields represent the total bicycles detected during the specified one hour period. Direction of travel is not specified, but in general most traffic in the Fremont Bridge NB field is travelling northbound and most traffic in the Fremont Bridge SB field is travelling southbound.
    * The data we will use here are the hourly bicycle counts on [Seattle's Fremont Bridge](https://www.openstreetmap.org/#map=17/47.64813/-122.34965). These data come from an [automated bicycle counter](http://www.seattle.gov/transportation/projects-and-programs/programs/bike-program/bike-counters/fremont-bike-counters), installed in late 2012, which has inductive sensors under the sidewalks on either side of the bridge. The daily or hourly bicycle counts can be downloaded from http://data.seattle.gov/; here is the direct link to the hourly dataset. To download the data directly, you can uncomment the following curl command:
    * Code: `!curl -o FremontBridge.csv# https://data.seattle.gov/api/views/65db-xm6k/rows.csv?accessType=DOWNLOAD`
* [NOAA - Climate Data Online Search](https://www.ncdc.noaa.gov/cdo-web/search?datasetid=GHCND)
  * While the datasets are free, the way you obtain data from this site is by submitting your email-id and as if you are making an online purchase for free.
  * NOAA makes available their daily [weather station data](http://www.ncdc.noaa.gov/cdo-web/search?datasetid=GHCND) (I used station ID USW00024233) and we can easily use Pandas to join the two data sources. 

### Lessons

* Learn how to play with Time-Series data.