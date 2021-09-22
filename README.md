# DStest
Data Science Test for Junior position

## Instructions
- This test includes 3 tasks, it is not necessarely expected from you to complete all the tasks
- You time limit is **xxx h and xxx min**.
- Results should be provided as a R or Python script. You can also provide a Rmarkdown or Jupyter notebook.

### Note
- The main criteria for evaluation may not be the answer per se but how you manage to obtain this answer. 
- Any suitable method can be used, and there are no restrictions on online resources or packages. However, the objective of the test is to see your own work. 
- It is important to provide a commented code that can be read by anyone.
- Questions are welcome.

## Problematic
In order to take decisions on the management of a coastal barrage, we need to be able to anticipate the variations of sea level in the coming 2 hours. 
Sea level is mainly determined by tides , with a correction coming from meteorological effects (mostly atmospheric pressure and wind).
To anticipate sea level, complex wave models coupled with atmospheric models can be built, however we are only interested in a short term forecast and in the sea level at a single location. We will propose instead to develop a forecasting algorithm based on the analysis of the gap between the measured sea level and the forecasted astronomical tide. 

The final objective of this assignment is to provide a module that is able to **forecast the observed tide over the next two hours**, preferably providing values **every 5 minutes** on this two hours window.

## Datasets
All datasets are located in the folder *dataset*:
- *astronomicalTide.csv* – astronomical tide over June to August 2017
- *observedTide.csv* – observed sea level over June to August 2017 (raw data)

## Tasks
Not all tasks are mandatory to complete the assignment but some of them will be useful for the following ones. 
Note that the analysis should be carried out in Singapore Time (SGT = UTC+8) 

### Task 1 - Astronomical tide
1. Read the file _astronomicalTide.csv_: this file contains 2 columns, the time and the tide value. Time is expressed in UTC. 
2. Plot the astronomical tide according to time.
3. Can you extract some pattern on the astronomical tide?

### Task 2 - Observed tide
1. Read the file _observedTide.csv_: this file contains 2 columns, the time and the tide value. Time is already expressed in SGT
2. Plot the observed tide according to time. Can you identify and remove some outliers?
3. The observed tide is available every 5 minutes, whereas the astronomical tide is available every minute. Join the two tables with a common timeline, without leaving any gap.
You can either use linear interpolation to fill the gap between 1 and 5 minutes or extract the value every 5 minutes (remember the final objective of this assignment).
4. What is the correlation between the astromical and the observed tide? Use this relationship to fill the missing data?

### Task 3 - Forecast
Build a function that will forecast the *observed tide* for the next 2 hours, using as input:
- the past *observed tide* 
- the past *astromical tide*
- the *astronomical tide* over the next two hours.
There is no contrains on the selection of historical data. The forecast however is constrained to 2 hours and should preferably (not mandatory) provide a value every 5 minutes 
(forecasted value for the next 5 minutes, 10 minutes, ..., 120 minutes)