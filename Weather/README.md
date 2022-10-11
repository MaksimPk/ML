# Prediction of the temperature.
## Purpose and essence of the project
In this project, we set out to predict the temperature for every day of the year.
The project was done in JupiterLab.
We used the archive of weather data at Sheremetyevo airport (Moscow, Russia) for several years.
In the course of the work, we tested an optimal model using the trigonometric transformation of the number of days in the year (cos and sin functions) for linear regression. We considered models with a simplified structure (cosine only) and a more complex structure (cos, sin and a number of weather characteristics).
Also, we've made a visualization of each model and basic data.
## The results
Here we use the coefficient of determination and mean absolute error as R2 and MAE (on test sample).
The best model is the one using day features, but this leads to an intraday prediction only (R2 = 0.99-1.0, MAE = 0.56).
The model using sin and cos has performed in exactly the same way as the model with additional features averaged with the median by month (R2 = 0.76, MAE = 4.25-4.29).
The model with only one cos feature performed slightly worse (R2 = 0.71, MAE = 4.57).
So, the model with both cos and sin features proved to be the best model for long-run prediction.
## Libraries and technologies
1) urllib.request
2) pandas
3) matplotlib.pyplot
4) numpy
5) statsmodels.api
6) sklearn.linear_model (LinearRegression)
7) sklearn.metrics (mean_absolute_error)
## Links
URLs: 
- to dowload the file:
http://37.9.3.250/download/files.synop/27/27514.01.01.2016.01.01.2022.1.0.0.ru.utf8.00000000.csv.gz
- to see the website: https://rp5.ru/%D0%90%D1%80%D1%85%D0%B8%D0%B2_%D0%BF%D0%BE%D0%B3%D0%BE%D0%B4%D1%8B_%D0%B2_%D0%A8%D0%B5%D1%80%D0%B5%D0%BC%D0%B5%D1%82%D1%8C%D0%B5%D0%B2%D0%BE,_%D0%B8%D0%BC._%D0%90._%D0%A1._%D0%9F%D1%83%D1%88%D0%BA%D0%B8%D0%BD%D0%B0_(%D0%B0%D1%8D%D1%80%D0%BE%D0%BF%D0%BE%D1%80%D1%82)
