# Classification
Classify flights as delayed or not



![flightsbalance.jfif](./images/3NumOnTimeDelayedbyCarrier.png?raw=true)

## Overview

This project encapsulates using Classification with Machine Learning for modeling 2018 Domestic Airline Flight Delays.

## Business Problem

We are consulting with Southwest Airlines for Domestic Flights Analysis by looking at industry delays and routes for improvement opportunities.
Which Airlines are usually late/early?
Which routes are late/early?

## Data

Airline and Cancellation Dataset on Kaggle by Yuanyu 'Wendy' Mu     

All Records from United States Department of Transportation

2018 data containing 7.21M records 851MB
Initial Features included: 

FL_DATE - Date of Flight<br>
OP_CARRIER - Flight Carrier<br>
OP_CARRIER_FL_NUM - Flight Carrier Identifier<br>
ORIGIN- Start Airport<br>
DEST- Destination Airport<br>
CRS_DEP_TIME - Computer Reservation System (CRS) Departure Time<br>
DEP_TIME - Actual Departure Time<br>
DEP_DELAY - Dep Time minus CRS Dep Time in Min<br>
TAXI_OUT - Time To taxi<br>
WHEELS_OFF - Time Wheels in Air<br>
WHEELS_ON - Time Wheels on Ground<br>
TAXI_IN - Time To taxi<br>
CRS_ARR_TIME - Computer Reservation System (CRS) Arrival Time<br>
ARR_TIME - Actual Arrival Time<br>
ARR_DELAY - ARR_Time minus CRS_ARR_TIME in Min<br>
CANCELLED - Flight Cancelled or not<br>
CANCELLATION_CODE - Cancel Code<br>
DIVERTED - Flight Was diverted or Not<br>
CRS_ELAPSED_TIME -CRS scheduled Flight Time<br>
ACTUAL_ELAPSED_TIME - Actual Flight Time<br>
AIR_TIME - Time in the Air<br>
DISTANCE - Distance of Flight<br>
CARRIER_DELAY - Carrier Delay in Min<br>
WEATHER_DELAY - Weather Delay in Min<br>
CANCELLATION_CODE - Cancelled Code<br>
NAS_DELAY - National Air Service Delay in Min<br>
SECURITY_DELAY - Sec Delay in Min<br>
LATE_AIRCRAFT_DELAY - Delay due to late Aircraft in Min<br>

## Methods

We performed Inferential Analysis of 7M+ recs looking at Airlines, Destinations of Flights, Delays, Times,
We then reduced the Data set to just the Top 5 Airlines by numner of flights.
We reduced the number of Origins and Destinations to the top 30 instead of the 358.

We also performed Classification Analysis with Machine Learning Algorithms
	Logistic Regression, Decision Trees, Random Forests, XGBoost
	
With GridSearch narrowing down the most optimal Hyperparameters to predict delayed flights and assess the strength and relationship and importance of the different features and their relation to delayed flight.


## Results

![1TotalFlightsbyCarrier.png](./images/1TotalFlightsbyCarrier.png?raw=true)

![2BusiestCitiesbyFlights.png](./images/2BusiestCitiesbyFlights.png?raw=true)

Modeling with continuous features Distance, Flight Time, 
Categoricals Weekdays, Months, Top 5 Airlines, Top 30 Origins and Destinations
To Classify if Delayed or not.  Delays are on Arrival Delays and >=15 mins



![6delayedSplit.png](./images/6delayedSplit.png?raw=true)

Best Predictive Results were found with the XGBoost algorithm
With a Recall of 59%, Accuracy 66% , F1 value of .59

MODEL
RECALL
ACCURACY
F1
XGBoost
59%
66%
59%
Random Forest
59%
65%
57%
Decision Tree
39%
68%
55%
Logistic Regression
DNF


![10AircraftLate.png](./images/10AircraftLate.png?raw=true)<br>


## Conclusions

We predicted 59% of Delayed flights but Recall needs to be more accurate.<br>
SouthWest Airlines should focus on Reducing Backup Delays as that is 50% of All Delays<br>

Challenges<br>
Large Dataset and finding an appropriate model for the complexity of the data was a challenge.<br>


## Next Steps

Reduction of origins and destinations: Top 20, Top 10<br>
Try PCA analysis<br>
<br>

## For More Information

See the full analysis in the [Jupyter Notebook](https://github.com/SunTzuLombardi/FlightsClassification/blob/main/code/Classification.ipynb) or review this [presentation](https://github.com/SunTzuLombardi/FlightsClassification/blob/main/presentation.pdf)

For additional info, contact Daniel M. Smith at danielmsmith1@gmail.com

## Repository Structure

├── code<br>
│   ├── __init__.py<br>
│   ├── __.py<br>
├── data<br>
├── images<br>
├── __init__.py<br>
├── README.md<br>
├── presentation.pdf<br>
├── gitbhub.pdf<br>
├── notebook_Classification.pdf<br>
├── Classification.ipynb<br>




