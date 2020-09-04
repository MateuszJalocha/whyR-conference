# Forecasting Rental Prices in Kraków

After the data was collected to my undergraduated thesis i realized that there is a possibility to check how location affects rental price of apartment. In the next step informations about objects and areas surrounding the dwellings were extracted from google API and OpenSteetMaps. All these informations made it possible to carry out the study on the most accurate forecasting rental prices using geospatial variables and the distances between apartments and selected objects.

<p align="center">

<img align = "center" src ="Images/whyR_additionalObjects.png" /> 
<img align = "center" src="Images/whyR_pricesPredictions.png" />

</p>

## Data

Due to not enough observations in some of 18 Cracow districts I decided to take into account four main delegations: Krowodrza, Śródmieście, Nowa Huta and Podgórze. The study used two and three room flats with less than eighty square meters and these where we have to pay less than sixty PLN per square meter.

From the objects surrounding the apartments, the following have been taken into account: "university", "shopping center", "kindergarten", "small shop", "bus stop", "supermarket", "city center", "park". Based on their coordinates, the distance from the nearest facility of each type was calculated and the average distance to the nearest five representatives of each type except for the "city centre" and the "park". Also, due to the significantly higher number of students at universities such as "AGH University of Science and Technology" and "Jagiellonian University", a weight was imposed on the distance between the apartment and the university building. The formula for the weights is: one minus the number of students at university divided by number of students in Cracow and it is multiplied by the distanc

## Models

Two approaches to prediction were used in the study, in the first case only one model was created based on all observations.  In the second case, separate models were created for each of the districts, based on observations located only in these districts and then predictions were combined. Methods used to create models are:

- **Multiple regression** - the best model was selected using Akaike Information Criterion.
- **Bagging**
- **GBM**
- **Random Forest**
- **XGBoost**


## Main libraries

- **randomForest**, **pracma**, **gbm**, **e1071**, **xgboost**, **caret**, **MLmetrics**- Machine Learning

- **ggmap**, **osmdata**, **geosphere**, **googleway**, **gmapsdistance** - Coordinates of objects

- **rvest**, **rlang**, **RCurl** - Webscrapping

- **tidyverse**, **dbplyr**, **dplyr**, **XML*, **stringr**, **caTools** - Generally useful libraries

## Contributors

- **Mateusz Jałocha** (mat.jalocha@gmail.com, https://www.linkedin.com/in/mateusz-jałocha-8942701b6/)

