# Uber_fares

Uber is a common commuting tool, I used Linear regression to estimate Uber ride costs fares based on trip distances, number of passengers, time and date of the ride.

* Prepared raw data by introducing timedata and trip distances using the Haversine formula.
* Cleaned data from corrupted and void entries using Pandas.
* Detected and removed errors and inconsistencies to improve regression accuracy.
* Achieved a significant 76.08% decrease in MSE after the data cleaning.

# Resources Used
* Python Version: 3.7
* CUDA Toolkit 11.5.119 
* Packages and Libraries: pandas, numpy, matplotlib, seaborn, sklearn, datetime.
# Data used
* Uber Fares Dataset from Kaggle (https://www.kaggle.com/datasets/yasserh/uber-fares-dataset).

# Data Analysis
* Detected and removed unrealistic data points and corrupt entries.
* Fetched new columns to gain more insights about data: Location, Day of the week and Distance.
* Calculated correlation between variables.

![image 1](https://github.com/YoussefAithaddou/Uber_fares/blob/main/Correlation%20Matrix.png)

# Linear regression model:
* MSE using raw data: 93.08
* After analysis we see that distance is the most important variable.
* MSE using cleaned data: 22.26
* We achieved a significant 76.08% decrease in MSE after cleansing the data.


![image 2](https://github.com/YoussefAithaddou/Uber_fares/blob/main/Regression%20Result.png)

* This model achieved a decent accuracy rate. However, we see that the model underestimate values above 75$. This can be explained by a possibility of corrupt data as we have found unrealistic data points (such as a number of passengers above 50, or distances of 0 Kms). This can be seen as extreme outliers as the cost of a typical 11 minutes ride is between $8 and $37 according to the following article https://www.ridesharingdriver.com/how-much-does-uber-cost-uber-fare-estimator/. Moreover, this underestimation of high prices can be caused also by the lack of ride details such as the ride option for example.

