# TimeSeries-taxi
## Intro
Rusty Bargain is a used car sales service that is developing an app to attract new customers. In this app, you can quickly find out the market value of your car. You have access to historical data, technical specifications, trim versions and prices. You need to build the model to determine the value.
Rusty Bargain is interested in:
the quality of the prediction
the speed of prediction
the time required for training

### Notes:
- Use the REQM metric to evaluate the models.
- You can use a special command to find the execution time of the cell code in Jupyter Notebook.


### Data description
* DateCrawled - date on which the profile was downloaded from the database
* VehicleType - vehicle body type
* RegistrationYear - year the vehicle was registered
* Gearbox - type of transmission
* Power - power (hp)
* Model - vehicle model
* Mileage - mileage (measured in km due to the regional specificities of the dataset)
* RegistrationMonth - vehicle registration month
* FuelType - fuel type
* Brand - vehicle make
* NotRepaired - vehicle repaired or not
* DateCreated - profile creation date
* NumberOfPictures - number of photos of the vehicle
* PostalCode - postal code of the profile owner (user)
* LastSeen - date of the user's last activity

**Target**
* Price - (Euro)

## Libraries used

import pandas as pd

import numpy as np

import seaborn as sns

from matplotlib import pyplot as plt

from sklearn.model_selection import train_test_split 

import lightgbm as lgb

from sklearn import metrics

from sklearn.model_selection import cross_val_score

from sklearn.metrics import mean_squared_error

from sklearn.ensemble import RandomForestRegressor

from catboost import CatBoostRegressor

import xgboost as xgb

from sklearn.model_selection import GridSearchCV



