# Bangalore_city_home_price_prediction
Data Cleaning:
1. Drop column which are not required.
2. Applied lambda function to extract integer from column having int + text values like 3 from 3 bhk.
3. Finding values from "total_sqft" column that are not in correct integer form (2433-3422, 34sq mt) and filling with appropriate values.

Feature Engineering:
1. Finding categorical data having lesser data and removing them as less data will not give accurate result.

Outlier Detection:
1. Finding houses with sqft per bhk less than 300 and removing it.
2. Dealing with data having price per bhk that are too higher or lower than mean +- standard deviation.
3. Dealing with case in which price of 2 BHK is higher than 3 BHK in same region and similar.
4. Finding data with house having bathroom much greater than total rooms using scatter plot and removing it.

Choosing Best Model: 
1. Used k-fold cross validation to get score on multiple fold of datasets on linear regression.
2. Used grid search cv to compare regression, lasso and decision tree alogorithm and get the best score out of that.
3. Made pickle and Json file to upload model to file directory. 

Deployment:
1. Made flask server to get names of all locations from json file.
2. Used model to predict price using local web server. ("app.html" file in "BHP_web_server" folder)
