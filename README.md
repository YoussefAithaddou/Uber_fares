# Uber_fares

Uber is a common commuting tool, I used Linear regression to estimate Uber ride costs fares based on trip distances, number of passengers and time and date of the ride.

* Cleaned data from corrupted and void entries using Pandas.
* Calculated ride distances using the Haversine formula.
* Created a location variable by clustering pickup locations using KMeans.
* Achieved an R^2 of 85.6%.


# Resources Used
* Python Version: 3.7
* CUDA Toolkit 11.5.119 
* Packages and Libraries: pandas, numpy, matplotlib, seaborn, sklearn, datetime.
# Data used
* Uber Fares Dataset from Kaggle (https://www.kaggle.com/datasets/yasserh/uber-fares-dataset).

# Data preparation
* Converted four videos to pictures frame by frame.
* Uploaded and resized the pictures for uniformity.
* Created separate training and testing sets.

# Linear regression model:
* The linear regression model is as follows:  5.18e-02 * passenger_count + 2.66 * distance , 0.0 * Locations , 8.68e-02 * Months + 2.12e-03 * Days + 2.73e-02 * Hours

![image 1](https://github.com/YoussefAithaddou/CNN-to-predict-locations-of-my-previous-trips/blob/main/model%20info.PNG)


# Model Evaluation:
* R^2 = 85.6% 
* 85.6% of variation of a the ride fares are explained by trip distances, number of passengers and time and date of the ride 


![image 2](https://github.com/YoussefAithaddou/CNN-to-predict-locations-of-my-previous-trips/blob/main/result%20sample.png)

* This model achieved a decent accuracy rate. However, we see that the model underestimate values above 75$. This can be explained by a possibility of corrupt data as we have foind unrealistic data ponts (such as a number of passegngers above 50, or distances of 0 Kms). This can be seen as extreme outliers as the cost of a typial 11 minutes ride is between $8 and $37 according to the following article https://www.ridesharingdriver.com/how-much-does-uber-cost-uber-fare-estimator/. Moreover, this underestimation of high prices can be caused also by the lack of ride details such as the ride option for example.
