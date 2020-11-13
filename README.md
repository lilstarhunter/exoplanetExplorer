# Exoplanet Explorer

![exoplanets.jpg](Images/exoplanets.jpg)


## Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, I created multiple machine learning models capable of classifying candidate exoplanets from the raw dataset.

## Workflow


### 1. Preprocessing the Data

* Data was preprocess prior to fitting the model.
* Removed unnecesary features and performed feature selection
* Use `MinMaxScaler` to scale the numerical data.
* Applied `LabelEncoder` to the categorical labels (__koi_disposition__) for future Neural Network
* Split the data into a training and testing data subset.

### 2. Create a SVM Model & Tune Model Parameters

* The first model used is a Support Vector Machine Linear Classifier from `sklearn.svm` library
* Use `GridSearch` to tune model parameters.
* Tune and compare at least two different classifiers.

### Reporting

* Create a README that reports a comparison of each model's performance as well as a summary about your findings and any assumptions you can make based on your model (is your model good enough to predict new exoplanets? Why or why not? What would make your model be better at predicting new exoplanets?).

- - -

## Summary

* 

## Data Source

* [Exoplanet Data Source](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)


- - -

