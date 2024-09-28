# Mean, Median and Mode

- What can we learn from looking at a group of numbers?
- In Machine Learning (and in mathematics) there are often three values that interests us:
    - Mean - The average value
    - Median - The midpoint value
    - Mode - The most common value

# Mean in Python

- We can use NumPy to calculate the mean of a list.

```python
import numpy # You must import the package NumPy

speed = [90,38,80,90,70,76,100,95] # Data set of speeds

mean = numpy.mean(speed) # Use numpy to calculate mean

print(mean)
```

```python
79.875
```

# Median

- Median can also be calculated using NumPy.

```python
import numpy

speed = [90,38,80,90,70,76,100,95] # Data set of speeds
median = numpy.median(speed) # Use numpy to calculate median

print(median)
```

```python
85.0
```

# Mode

- Mode can be calculated using the package SciPy.

```python
from scipy import stats # Import the scipy package

speed = [90,38,80,90,70,76,100,95] # Data set of speeds
mode = stats.mode(speed) # Use SciPy to calculate mode

print(mode)
```

```python
ModeResult(mode=90, count=2)
```