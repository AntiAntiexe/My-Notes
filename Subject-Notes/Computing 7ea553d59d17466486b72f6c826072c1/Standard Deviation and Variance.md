# Standard Deviation and Variance

- Standard deviation is a number that describes how spread out the values are.
- A low standard deviation means that most of the numbers are close to the mean (average) value.
- A high standard deviation means that the values are spread out over a wider range.

# Standard Deviation in Python

```python
import numpy

speed = [90,38,80,90,70,76,100,95] # Data set of speeds
std = numpy.std(speed) # Use numpy to calculate standard deviation

print(std)
```

```python
18.387750678100897
```

# Variance

- Variance is another number that indicates how spread out the values are.
- In fact, if you take the square root of the variance, you get the standard deviation.
- Or the other way around, if you multiply the standard deviation by itself, you get the variance.

# Variance in Python

```python
import numpy

speed = [90,38,80,90,70,76,100,95] # Data set of speeds
var = numpy.var(speed) # Use numpy to calculate variance

print(var)
```

```python
338.109375
```

## Symbols

- Standard deviation is often represented by the symbol Sigma: $\sigma$
- Variance is often represented by the symbol Sigma Squared: $\sigma^2$