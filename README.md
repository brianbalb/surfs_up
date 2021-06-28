# Temperature Trends for Surfs Up

### Project request from Oahu Surf Shop

## Project Overview

The purpose of this project is to analyze the temperature trends in Oahu, Hawaii for my client who is interested in open a surf shop. Specifically, the temperature trends during the months of June and December are analyzed so that the client can make a more informed decision for the surfing season.

Additonally coming from the mainland USA, the weather can vary in the summer and winter months. 

## Ultimate Objective
Your investors want to ensure that there are enough customers between seasons to sustainable business throughout the year. 

## Resources

Data File: hawaii.sqlite (provided)
Software: Python, SQLAlchemy 

# Results

* The average temperature in Oahu during December is only 3.9°F cooler than June.
* The lowest temperature in December is 8°F colder than the lowest temperature in June.
* There are 10.7% less data points in December than June.

# Summary and Recommendations 

Based on the results above, it can be expected that a surf shop in Oahu will have less customers in December than in June due to the slight decrease in average daily temperature.

It is important to have the most relevant results when conducting analysis on a potential business venture. For this reason, I would perform two additional queries on June and December to obatin more weather data about precipitation during these two months.

1. This query will find precipitation scores in June:

**session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()**

2. This query below will find precipitation scores in December:

**session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()**
