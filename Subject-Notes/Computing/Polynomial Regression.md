# Polynomial Regression

- If the data points clearly will not fit a linear regression (a straight line through all data points), it might be ideal for polynomial regression.
- Polynomial regression, like linear regression, uses the relationship between the x and y to find the best way to draw a line through the data points.

![image.png](Subject-Notes/Computing/Polynomial%20Regression/image.png)

## Example

- 8 cars were registered as they passed a certain tollbooth. The car’s speed and the time of day (hour) we recorded.
- The x-axis represents the hours of the day and the y-axis represents the speed.

Start by creating a scatter plot

```python
import matplotlib.pyplot as plt

x = [1,2,3,5,6,7,8,9,10,12,13,14,15,16,18,19,21,22]
y = [100,90,80,60,60,55,60,65,70,70,75,76,78,79,90,99,99,100]

plt.scatter(x, y)
plt.show()
```

![image.png](Subject-Notes/Computing/Polynomial%20Regression/image%201.png)

Then import NumPy and then draw the line of polynomial:

```python
import matplotlib.pyplot as plt # Import the correct modules
import numpy

# Create the arrays
x = [1,2,3,5,6,7,8,9,10,12,13,14,15,16,18,19,21,22]
y = [100,90,80,60,60,55,60,65,70,70,75,76,78,79,90,99,99,100]

# Numpy's method of creating a polynomial model
mymodel = numpy.poly1d(numpy.polyfit(x, y, 3))

# Specify how the line will display, it starts at x pos 1 and finishes at x pos 22
myline = numpy.linspace(1, 22, 100)

plt.scatter(x, y)# Draw the original scatter plot
plt.plot(myline, mymodel(myline))# Draw the line of polynomial regression
plt.show()# Display the diagram

```

![image.png](Subject-Notes/Computing/Polynomial%20Regression/image%202.png)

# R-Squared

- It is important to know how well the relationship between the values of the x- and y-axis is, if there is no relationship the polynomial regression can not be used to predict anything.
- The relationship is measured with a value called the r-squared.
- The r-squared value ranges from 0 to 1, where 0 means no relationship and 1 means 100% related.
- Python and the SkLearn module will compute the value for you, all you have to do is feed it with the x and y arrays.

```python
import numpy
from sklearn.metrics import r2_score# Import sklearn and numpy

# Create data set
x = [1,2,3,5,6,7,8,9,10,12,13,14,15,16,18,19,21,22]
y = [100,90,80,60,60,55,60,65,70,70,75,76,78,79,90,99,99,100]

# Create the polynomial line of regression
mymodel = numpy.poly1d(numpy.polyfit(x, y, 3))

# Find how well it can use polynomial regression by using r2_score
print(r2_score(y,mymodel(x)))
```

```python
0.9432150416451027
```

- This output of .94 is really good which shows it can be used for polynomial regression.

# Predict Future Values

- We can use the information from before to predict future values.

## Example

- Try and predict the speed of a car that passes the tollbooth at around the time 1700.
- To do so, we need the same mymodel array from the example above.

```python
import numpy
from sklearn.metrics import r2_score # Import sklearn and numpy

# Create data set
x = [1,2,3,5,6,7,8,9,10,12,13,14,15,16,18,19,21,22]
y = [100,90,80,60,60,55,60,65,70,70,75,76,78,79,90,99,99,100]

# Create the polynomial line of regression
mymodel = numpy.poly1d(numpy.polyfit(x, y, 3))

# Input the desired x value
speed = mymodel(17)
print(speed)
```

```python
88.87331269697978
```

- This can also be read from the diagram:

![image.png](Subject-Notes/Computing/Polynomial%20Regression/image%203.png)