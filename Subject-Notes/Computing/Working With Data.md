# Working With Data

# How to Get Big Data Sets?

- To create big data sets for testing, we use the Python module NumPy, which comes with a number of methods to create random data sets, of any size.

```python
import numpy

# Creates a data set of 250 floats from 0.0 to 5.0
data = numpy.random.uniform(0.0, 5.0, 250)

print(data)
```

```python
[3.12975676 0.03479117 0.53023482 0.8300111  2.13731369 3.69923588
 3.35252441 0.48922601 0.30700784 3.58235378 4.70492182 4.02098789
 2.8378238  3.88031088 3.70284812 3.75041396 4.8470219  3.89687566
 3.46789689 3.81458142 1.19827838 3.69261305 3.57159366 1.64822591
 2.93198168 2.01376081 0.52763868 1.69215708 3.00379235 4.03158086
 4.74880846 3.16402964 0.39800872 1.25738285 1.36509746 2.94272061
 3.8961089  1.35751968 4.83667425 4.94379315 4.29405709 0.90959564
 3.52267339 1.60916052 4.66981743 4.34590347 4.46661526 3.65627825
 4.77250465 0.70257518 1.7399764  2.95280355 0.20837485 4.87796254
 2.24767772 2.14549668 4.97276269 2.43620591 1.94316734 3.18750066
 0.16745034 2.0350957  2.5515838  4.97838967 1.06597971 1.09634826
 4.21224453 2.34604667 1.96585885 2.41541409 3.42823247 4.37762996
 1.59759894 1.57248052 0.30466896 0.48088325 3.72972431 3.38062195
 2.13629289 1.83856211 4.80313309 0.79116693 4.38203598 1.04804728
 2.59233951 0.43494167 4.9760058  1.673055   0.56359936 0.79430113
 4.33676836 4.16976616 2.17696719 4.4785446  0.30911726 0.35065305
 0.55986429 4.19276413 3.45596268 2.99583348 3.00319075 1.67254105
 3.69007753 0.76014571 4.62448817 1.58645691 0.1216174  0.45389406
 2.03492131 3.04248233 3.29356763 3.25599159 2.39221903 1.72957031
 3.61997767 1.73203548 0.31860489 0.43040619 1.29381391 4.47874457
 0.25196524 1.55010112 3.79682006 0.45139481 4.84325355 0.96199909
 3.89769143 3.11518889 2.23139332 0.11981311 2.42050381 2.74146798
 0.86815506 3.64534389 0.41910967 2.1149927  2.02967701 0.90493153
 2.01130144 4.53410439 4.37450409 4.13836133 1.79112377 0.68239952
 2.50497562 0.13941899 2.19730522 0.07771144 4.46299202 1.81976333
 1.69246214 3.75008137 3.77181157 0.68458982 4.92994447 1.99451827
 4.36768719 2.92734021 3.97189594 1.66542836 1.23639873 4.72345388
 4.93408526 1.5491949  0.85804618 0.09089385 1.38844351 1.6536271
 4.76022762 3.67459505 3.25396075 3.2820014  4.91281068 4.95361506
 0.75729466 1.10142875 1.69134819 0.63416654 2.9033216  0.40699424
 0.78572267 0.25243586 1.08699289 0.58880345 3.73890035 1.63771689
 1.35030082 3.00673565 0.5081551  2.37556166 1.73768989 4.48850889
 1.23028864 0.26277643 2.86912357 0.81016637 0.01507406 4.55712152
 4.732889   2.11390598 1.47757565 4.44558203 3.19828964 2.31824675
 2.90610229 0.77471272 1.60928317 0.30181887 0.63087323 2.36000662
 1.07231434 1.18949495 2.1550603  2.37678499 2.56723821 3.48661177
 1.2638908  2.81497175 4.22607161 3.69221947 2.4768084  1.85061294
 4.636665   0.89943891 3.59073523 0.79496456 3.9816039  3.00015399
 0.63738644 3.20398383 4.4994135  3.64324658 0.90021244 4.92565905
 0.14231009 1.84709858 3.87790009 3.90786556 0.49970498 2.61616263
 2.61358984 2.26062174 4.30260564 1.67856734 4.41873738 1.66058535
 3.31256252 0.71530374 0.50778431 0.06414489]
```

# Histograms

- To visualise the data set we can draw a histogram with the data we collected.
- We will use the Python module Matplotlib to draw a histogram.

```python
import numpy
import matplotlib.pyplot as plt

# Creates a data set of 250 floats from 0.0 to 5.0
data = numpy.random.uniform(0.0, 5.0, 250) 

plt.hist(data, 5) # Creates a histogram with 5 bars

plt.show() # Displays the histogram
```

![We use the array from the example above to draw a histogram with 5 bars. The first bar represents how many values in the array are between 0 and 1. The second bar represents how many values are between 1 and 2 and so on.](Subject-Notes/Computing/Working%20With%20Data/Untitled.png)

We use the array from the example above to draw a histogram with 5 bars. The first bar represents how many values in the array are between 0 and 1. The second bar represents how many values are between 1 and 2 and so on.

# Big Data Distributions

- An array containing 250 values is not considered very big, but now you know how to create a random set of values, and by changing the parameters, you can create the data set as big as you want.

```python
import numpy
import matplotlib.pyplot as plt

#creates data set of 100000 floats from 0.0 to 5.0
data = numpy.random.uniform(0.0, 5.0, 100000)

plt.hist(data, 100) #creates histogram with 100 bars

plt.show() #displays the histogram
```

![image.png](Subject-Notes/Computing/Working%20With%20Data/image.png)

# Normal Data Distributions

- The past ways of creating data was a completely random array, of a given size and between two given values.
- The next way of creating data is where the values are concentrated around a given value.
- In probability theory this kind of data distribution is known as the *normal data distribution*, or the *Gaussian data distribution*, after the mathematician Carl Friedrich Gauss who came up with the formula of this data distribution.

```python
import numpy
import matplotlib.pyplot as plt

# Creates data set of 100000 floats from 0.0 to 5.0
data = numpy.random.normal(5.0, 1.0, 100000) 

plt.hist(data, 100) #creates histogram with 100 bars

plt.show() #displays the histogram
```

![image.png](Subject-Notes/Computing/Working%20With%20Data/image%201.png)

- Using the array from the numpy.random.normal() method, with 100000 values, to draw a histogram with 100 bars. You specify the mean value is 5.0, and the standard deviation is 1.0.
- Which means that the values should be concentrated around 5.0, and rarely further away than 1.0 from the mean. As you can see from the histogram most values lie between 4.0 and 6.0.

# Scatter Plot

- A scatter plot is a diagram where each value in the data set is represented by a dot.

![image.png](Subject-Notes/Computing/Working%20With%20Data/image%202.png)

- The MatPlotLib module has a method for drawing scatter plots, it needs two arrays of the same length, one for the values of the x-axis, and one for the values of the y-axis:

```python
import matplotlib.pyplot as plt

age = [5,7,8,7,2,17,2,9,4,11,12,9,6]
speed = [99,86,87,88,111,86,103,87,94,78,77,85,86]

plt.scatter(x,y)
plt.show()
```

![image.png](Subject-Notes/Computing/Working%20With%20Data/image%203.png)

- The x-axis represents the ages and the y-axis represents the speeds.
- We can gather from the scatter plot that the two fastest cars were only 2 years old and the slowest car was 12 years old.

# Random Data Distributions

- In machine learning data sets can contain thousands or even millions of values. However you may not have real world data when you are testing an algorithm you might have to use randomly generated values.

```python
import matplotlib.pyplot as plt
import numpy

# Creates normal data distribution array with mean of 5.0 and a standard deviation of 1.0
x = numpy.random.normal(5.0, 1.0, 1000) 
y = numpy.random.normal(10.0, 2.0 , 1000)

plt.scatter(x, y)
plt.show()
```

![image.png](Subject-Notes/Computing/Working%20With%20Data/image%204.png)

- You can see that the dots are concentrated around the value 5 on the x-axis and 10 on the y-axis. You can also see that the spread is wider on the y-axis as it had a standard deviation of 2.0 compared to the x-axis which has a standard deviation of 1.0.