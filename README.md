# Feature-examination-using-regression-models.-Determining-demand-for-a-bike-share-scheme

Bike sharing systems are a means of renting bicycles where the process of obtaining membership, rental, and bike return is automated via a network of kiosk locations throughout a city. Using these systems, people are able rent a bike from a one location and return it to a different place on an as-needed basis. Currently, there are over 500 bike-sharing programs around the world.

I intend to reveal what is driving demand for bike hires. Machine learning models will be used to determine which features in the dataset are encouraging people to hire these bikes. Finally we will examine if it is necessary to examine “casual” users and “registered” users separately instead of the overall count of bikes hired.

Data source: https://www.kaggle.com/c/bike-sharing-demand/data

This investigation is composed of 3 parts split between 3 Jupyter notebooks.
Part 1 is an exploratory analysis of the data.
Part 2 is a section on feature engineering.
Part 3 is the modelling section that seeks to determine which features are driving demand.

Summary:
Demand for bikes is mostly determined by the time of day. Though that depends on which day it is. Most days are working days. On these days bikes are mostly being used around typical commuting times (7am to 9am and 5pm to 7pm). When its not a working day then time is less important unless its late night/early morning.

People prefer cycling when it feels warmer. High temperatures and humidity levels encourage more bike hires. This is why our models showed that summer was a significant factor.

There did not seem to be a linear relationship between the features and the number of bikes hired. Box-cox and log transformations were not sufficient. As a result tree based models were superior to linear regression models. Sklearn’s gradient boosting regressor returned the most accurate results. The final part of the modelling section indicated that it was better to model counts by type of user rather than consider all users at once.
