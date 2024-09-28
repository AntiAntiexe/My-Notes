# Multiple Regression

- Multiple regression is like linear regression, but with more than one independent value, meaning that we try to predict a value based on two or more variables.

## Example of Data Set

| Car | Model | Volume | Weight | CO2 |
| --- | --- | --- | --- | --- |
| Toyota | Aygo | 1000 | 790 | 99 |
| Mitsubishi | Space Star | 1200 | 1160 | 95 |
| Skoda | Citigo | 1000 | 929 | 95 |
| Fiat | 500 | 900 | 865 | 90 |
| Mini | Cooper | 1500 | 1140 | 105 |
| VW | Up! | 1000 | 929 | 105 |
| Skoda | Fabia | 1400 | 1109 | 90 |
| Mercedes | A-Class | 1500 | 1365 | 92 |
| Ford | Fiesta | 1500 | 1112 | 98 |
| Audi | A1 | 1600 | 1150 | 99 |
| Hyundai | I20 | 1100 | 980 | 99 |
| Suzuki | Swift | 1300 | 990 | 101 |
| Ford | Fiesta | 1000 | 1112 | 99 |
| Honda | Civic | 1600 | 1252 | 94 |
| Hundai | I30 | 1600 | 1326 | 97 |
| Opel | Astra | 1600 | 1330 | 97 |
| BMW | 1 | 1600 | 1365 | 99 |
| Mazda | 3 | 2200 | 1280 | 104 |
| Skoda | Rapid | 1600 | 1119 | 104 |
| Ford | Focus | 2000 | 1328 | 105 |
| Ford | Mondeo | 1600 | 1584 | 94 |
| Opel | Insignia | 2000 | 1428 | 99 |
| Mercedes | C-Class | 2100 | 1365 | 99 |
| Skoda | Octavia | 1600 | 1415 | 99 |
| Volvo | S60 | 2000 | 1415 | 99 |
| Mercedes | CLA | 1500 | 1465 | 102 |
| Audi | A4 | 2000 | 1490 | 104 |
| Audi | A6 | 2000 | 1725 | 114 |
| Volvo | V70 | 1600 | 1523 | 109 |
| BMW | 5 | 2000 | 1705 | 114 |
| Mercedes | E-Class | 2100 | 1605 | 115 |
| Volvo | XC70 | 2000 | 1746 | 117 |
| Ford | B-Max | 1600 | 1235 | 104 |
| BMW | 2 | 1600 | 1390 | 108 |
| Opel | Zafira | 1600 | 1405 | 109 |
| Mercedes | SLK | 2500 | 1395 | 120 |
- We can predict the CO2 emission of a car based on the size of the engine, but with the multiple regression we can use more variables to help us predict the CO2. Such as, the weight of the car to make the prediction more accurate.

## Example

- In python there are modules that can do the calculations for use. Start by importing the Pandas module.

```python
import pandas
```

- The pandas module can read csv files and return a DataFrame object. The example files is data.csv:

```python
# Read the csv file
df = pandas.read_csv('data.csv')
```

- Read the CSV file and store it in a variable

```python
#create the independant and dependant variables
X = df[['Weight', 'Volume']]
y = df['CO2']
```

- Create a list of the independent variable and the dependent variable. Usually, the independent variable is store in an uppercase X and the dependant in a lower case y.

```python
from sklearn import linear_model
```

- We also need some methods from sklearn for linear regression.
- From the sklearn module we will use the LinearRegression() method to create the linear regression object.
- This object has a method called fit() that takes the independent and the dependent values as parameters and fills the regression object with data that describes the relationship.

```python
#creates the linear regression object
regr = linear_model.LinearRegression()

#fits it with the two x and y parameters
regr.fit(X, y)
```

- Now we have a regression object that is ready to predict CO2 values based on a car’s weight and volume.

```python
# Predict the CO2 emission of a car where the weight is 2300 kg, and the volume is 1300cm3
preictiedCO2 = regr.predict([[2300, 1300]])
```

## The whole code:

```python
import pandas
from sklearn import linear_model # Import the modules

# Read the csv file
df = pandas.read_csv('data.csv')

# Create the independant and dependant variables
X = df[['Weight', 'Volume']]
y = df['CO2']

# Creates the linear regression object
regr = linear_model.LinearRegression()
# Fits it with the two x and y parameters
regr.fit(X, y)

# Predict the CO2 emission of a car where the weight is 2300 kg, and the volume is 1300cm3
preictiedCO2 = regr.predict([[2300, 1300]])

# Prints the predicted CO2 value
print(preictiedCO2)
```

```python
[107.2087328]
```

- We have predicted that a car with a 1.3 litre engine, and a weight of 2300kg will release approximately 107 grams of CO2 for every kilometre it drives.

## The Coefficient

- The coefficient is a factor that describes the relationship with an unknown variable.
- Example:
    - If 𝑥 is a variable, then 2𝑥 is 𝑥 two times. 𝑥 is the unknown variable, and the number 2 is the coefficient.
    - In this case, we can ask for the coefficient value of weight against CO2, and or volume against CO2. Answer(s) we get tells us what would happen if we increase, or decrease one of the independent variables.

```python
import pandas
from sklearn import linear_model # Import the modules

# Read the csv file
df = pandas.read_csv('data.csv')

# Create the independant and dependant variables
X = df[['Weight', 'Volume']]
y = df['CO2']

# Creates the linear regression object
regr = linear_model.LinearRegression()
# Fits it with the two x and y parameters
regr.fit(X, y)

# Prints the coefficient of the regression object
print(regr.coef_)
```

```python
[0.00755095 0.00780526]
```

- The result array represents the coefficient values of weight and volume.
- Weight: 0.00755095
- Volume: 0.00780526
- These values tell us that if the weight increase by 1kg, the CO2 emission increases by 0.00780526
- And if the engine size (volume) increases by 1 cm^3, the CO2 emission increases by 0.00780526
- It seems to be a fair guess, but we can test it.
- We have already predicted that if a car with 1300cm^3 engine weighs 2300kg, the CO2 emission will be approximately 107g.
- What if we increase the weight with 100kg.

```python
import pandas
from sklearn import linear_model

# Stores the csv data in variable
df = pandas.read_csv('data.csv')

# Creates independant and dependant variable
X = df[['Weight', 'Volume']]
y = df['CO2']

# Create the regression model
regr = linear_model.LinearRegression()
# Fit the model with the x and y values
regr.fit(X, y)

# Add our specific independent variables for the prediction
predictedCO2 = regr.predict([[3300, 1300]])

# Print the predicted result
print(predictedCO2)
```

```python
[114.75968007]
```

- We now have predicted that acra with a 1.3 litre engine and a weight of 3300kg, will produce 114.76 grams of CO2 for every kilometre it drives.
- This proves that the coefficient is correct:
- 107.2087328 + (1000 *0.00755095) = 114.75.968