# Percentiles

# What are percentiles?

- Percentiles are used in statistics to give you a number that describes the value that a given percent of the values are lower than.
- Example: Let's say we have an array of the ages of all the people that live in a street.

```python
Ages = [5,31,43,48,50,41,7,11,15,39,80,82,32,2,8,6,25,36,27,61,31]
```

- What is .75 percentile? The answer is 43, meaning that 75% of the people are 43 or younger.
- The NumPy module has a method for finding the specified percentile:

```python
import numpy

ages = [5,31,43,48,50,41,7,11,15,39,
				80,82,32,2,8,6,25,36,27,61,31]
percentile = numpy.percentile(ages, 75)

print(percentile)
```

```python
43.0
```