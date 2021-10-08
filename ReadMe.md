# Predicting Bicycle Traffic

### Tags

Library used are : Pandas, Visualization, RollingMean, GroupBy, PivotTable, TimeSeries, LinearRegression

### Goal

To Understand Bicylers habits and Predict the bicycle traffic on the given day



### DataSets Source

* [Seattle Gov - Data](https://data.seattle.gov)
  * [Transportation : Fremont Bridge - Hourly Bicycle Counts by the  month of October 2012 to present](https://data.seattle.gov/Transportation/Fremont-Bridge-Hourly-Bicycle-Counts-by-Month-Octo/65db-xm6k)
    * The Fremont Bridge Bicycle Counter records the number of bikes that cross the bridge using the pedestrian/bicycle pathways. Inductive loops on the east and west pathways count the passing of bicycles regardless of travel direction. The data consists of a date/time field: Date, east pathway count field: Fremont Bridge NB, and west pathway count field: Fremont Bridge SB. The count fields represent the total bicycles detected during the specified one hour period. Direction of travel is not specified, but in general most traffic in the Fremont Bridge NB field is travelling northbound and most traffic in the Fremont Bridge SB field is travelling southbound.
    * The data we will use here are the hourly bicycle counts on [Seattle's Fremont Bridge](https://www.openstreetmap.org/#map=17/47.64813/-122.34965). These data come from an [automated bicycle counter](http://www.seattle.gov/transportation/projects-and-programs/programs/bike-program/bike-counters/fremont-bike-counters), installed in late 2012, which has inductive sensors under the sidewalks on either side of the bridge. The daily or hourly bicycle counts can be downloaded from http://data.seattle.gov/; here is the direct link to the hourly dataset. 
* [NOAA - Climate Data Online Search](https://www.ncdc.noaa.gov/cdo-web/search?datasetid=GHCND)
  
