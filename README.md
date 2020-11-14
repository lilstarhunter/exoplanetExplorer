# Exoplanet Explorer

![exoplanets.jpg](Images/exoplanets.jpg)


## Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, I created multiple machine learning models capable of classifying candidate exoplanets from the raw dataset.


## Exploring and Selecting the Data

This dataset is a cumulative record of all observed Kepler "objects of interest" and contains an extensive data directory. 

**Exoplanet Achive Information**: The disposition or label in the literature for the exoplanet candidate. One of CANDIDATE, FALSE POSITIVE, NOT DISPOSITIONED or CONFIRMED. (**koi_disposition**)

**Project Disposition Columns**: NASA flags used to identify or assign the foreign body.

**Transit Properties**: Calculated parameters of the object such as  Orbital Period, Transit Epoch, Planet-Star Radius Ratio, Planet-Star Distance over Star Radius and Impact Parameter. _Transit properties contain uncertainty values and are identified with a suffix _err. The margin of error is NOT included in the model_

**Stellar Parameters**: Stellar parameters are observational data used to determine stellar physics. These include effective temperature, surface gravity, metallicity, radius, mass, and ageCalculated parameters of the object such as  Orbital Period, Transit Epoch, Planet-Star Radius Ratio, Planet-Star Distance over Star Radius and Impact Parameter. _Stellar properties contain uncertainty values and are identified with a suffix _err. The margin of error is NOT included in the model_

**KIC Parameters**: Physical properties and target identifier.

[Full Directory of Data Columns Definitions](https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html)


## Pipeline


### 1. Preprocessing the Data

* Data was preprocess prior to fitting the model.
* Removed unnecesary features and performed feature selection
* Use `MinMaxScaler` to scale the numerical data.
* Applied `LabelEncoder` to the categorical labels (__koi_disposition__) for future Neural Network
* Split the data into a training and testing data subset.

### 2. Create Models

* Support Vector Machine Linear Classifier from `sklearn.svm` library
* Logistic Regression from `sklearn.linear_mode` library
* Random Forest from `sklearn.ensemble` library
* kNN Model from `sklearn.neighbors` library
* Neural Networks from `tensorflow.keras.models` library


### 3. Hypertune Model
* Idenitified parameters using `.get_params().keys()`
* Use `GridSearch` to tune model parameters.


### Reporting

* Create a README that reports a comparison of each model's performance as well as a summary about your findings and any assumptions you can make based on your model (is your model good enough to predict new exoplanets? Why or why not? What would make your model be better at predicting new exoplanets?).

- - -

## Summary

* 

## Data Source

* [Exoplanet Data Source](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)


- - -

