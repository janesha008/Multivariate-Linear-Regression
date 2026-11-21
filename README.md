# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:

1. Start the program and import the required Pandas and Scikit-learn libraries.

2. Read the dataset carsemission.csv using pd.read_csv() and select Weight and Volume as independent variables (X) and CO2 as the dependent variable (y).

3. Create a Linear Regression model using LinearRegression() and train the model using regr.fit(X, y). Display the regression coefficients and intercept.

4. Give the weight as 3300 and volume as 1300 as input, predict the CO2 emission using regr.predict(), display the predicted CO2 value, and Stop the program.

## Program:
```
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)
```
## Output:

<img width="793" height="605" alt="image" src="https://github.com/user-attachments/assets/42e7ff6d-4dd1-412a-a355-f6b367d01622" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
