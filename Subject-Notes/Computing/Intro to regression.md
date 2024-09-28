# Intro to regression

- The term regression is used when you try to find the relationship between variables. In machine learning and statistical modelling that relationship is used to predict the outcome of future events.

# Linear Regression

- Linear regression uses the relationship between the data-points to draw a straight line through them called a line of best fit.

## Example

- The x-axis represents ages and the y-axis represents speed of 13 cars.

```python
import matplotlib.pyplot as plt

x = [5,7,8,7,2,17,2,9,4,11,12,9,6]
y = [99,86,87,88,111,86,103,87,94,78,77,85,86]

plt.scatter(x, y)
plt.show()
```

![image.png](Subject-Notes/Computing/Intro%20to%20regression/image.png)

- To then create the line of best fit, import SciPy and draw the line of linear regression.

```python
import matplotlib.pyplot as plt
from scipy import stats

# Create the arrays that reresent the values of x and y axis
x = [5,7,8,7,2,17,2,9,4,11,12,9,6]
y = [99,86,87,88,111,86,103,87,94,78,77,85,86]

# Execute a method that returns some important key values of linear regression
slope, intercept, r, p, std_err = stats.linregress(x, y)

"""
Create a function that uses the slope and intercept values to return a new value. 
This new value represents where on the y-axis the corresponding x value will be placed:
"""
def myfunc(x):
   return slope * x + intercept
   
# Run each value of the x array through the function. This will result in a new array with new values for the y axis
mymodel = list(map(myfunc, x))

#draw the original scatter plot
plt.scatter(x,y)

#draw the line of linear regression
plt.plot(x,mymodel)

#display the diagram
plt.show()
```

![image.png](Subject-Notes/Computing/Intro%20to%20regression/image%201.png)

# R for Relationship

- It is important to understand the relationship between the values of the x-axis and the y-axis. If there are no relationships the linear regression can not be used to predict anything.
- This relationship- the coefficient of correlation- is called r.
- The r value ranges from -1 to 1, where 0 means no relationship and 1 (and -1) means 100% related.
- Python and SciPy module will compute this value for you, all you have to do is feed it with the x and y values.

```python
from scipy import stats

#How well does this data set fit in a linear regression?
x = [5,7,8,7,2,17,2,9,4,11,12,9,6]
y = [99,86,87,88,111,86,103,87,94,78,77,85,86]

slope, intercept, r, p, std_err = stats.linregress(x,y)

#print out the r relationship of -1 to 1.
print(r)
```

```python
-0.758591524376155
```

- However this output is not perfect but it is closest to -1 then it is to 0 so it can still work with linear regression.
- So, whenever you want to use linear regression in a data set that you don’t know about, find the r value to see whether it would be suitable for linear regression.

# Predict Future Values

- Now you can use the information we have gathered to predict future values.

## Example

- Try and predict the speed of a 10 year old car.
- To do so, we need to use the same myfunc() function from the example above:

```python
from scipy import stats

x = [5,7,8,7,2,17,2,9,4,11,12,9,6]
y = [99,86,87,88,111,86,103,87,94,78,77,85,86]

slope, intercept, r, p, std_err = stats.linregress(x, y)

def myfunc(x):
   return slope*x + intercept
   
# Put 10 into the x parameter of the function as that is the desired variable for the prediction
speed = myfunc(10)
 
print(speed)
```

```python
85.59308314937454
```

- This is the predicted speed that a 10 year old car will drive at.
- It can also be seen on the diagram:

![image.png](Subject-Notes/Computing/Intro%20to%20regression/image%202.png)