# DStest
Data Science Test for Junior position

### Guideline
* This test includes 3 sections: basic, intermediate, and advanced
* You time limit is xxx h and xxx min; it is not expected from you to finish the test entirely, you can select the sections you want to complete.
* Any suitable method can be used, and there are no restrictions on online resources or packages. However, the objective of the test is to see your own work. 
* Results should be provided as a R or Python script. You can also provide a Rmarkdown or Jupyter notebook.
* Comment your code(?)
* Questions are welcome.

## Section 3 - Tide forecasting (advanced)
### ETL
* xxx

### xxx
In order to take decisions on the management of a coastal barrage, we need to be able to anticipate the variations of sea level in the coming 2 hours. Sea level is mainly determined by tides , with a correction coming from meteorological effects  (mostly atmospheric pressure and wind).
In order to anticipate sea level, complex wave models coupled with atmospheric models can be built, however we are only interested in a short term forecast and in the sea level at a single location. We will propose instead to develop a forecasting algorithm based on the analysis of the gap between the measured sea level and the forecasted astronomical tide. 


The objective of the assignment is to write a function taking as an input the astronomical tide data and the observed sea level data on a given time window, as well as the astronomical tide data in the next two hours, and giving as an output the forecast on the next two hours of the sea level. 
There is no constraint on the selection of the historical data window, but the idea is to have this algorithm run every 5 minutes in a real-time application context.

Data to work with:
In Documents/TideForecasting/

* astronomicalTide.csv – astronomical tide over June to August 2017
*	observedTide.csv – observed sea level over June to August 2017 (raw data)