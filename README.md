# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
1. Import necessary modules,pandas for data manipulation and linear_model from sklearn for performing linear regression.

### Step2
2. Use pandas.read_csv() to load the CSV file containing the dataset into a DataFrame

### Step3
3. Define the independent variables(x) as the columns "Volume" and "Weight"

### Step4
4. Define the dependent variable (y) as the "CO2" column

### Step5
5. Create a linear regression object and fit the model using the x and y data. Print the coefficients and intercept of the trained model.

### Step6
6. Use the trained model to predict the CO2 emission for a given input(e.g.,Volume=3300, Weight=1300).Print the predicted value.

## Program:
```
Developed by : Monika V
Reg no: 212225100028

```
```


import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemmision.csv")
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
<img width="610" height="401" alt="image" src="https://github.com/user-attachments/assets/c27f4172-dad7-4c5d-826e-9ae9ccd9fd42" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
