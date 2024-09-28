# Derivatives

# The Analytical Derivative

- In mathematics there are two ways of solving problems: **numerical** and **analytical methods.**
    - Numerical solution methods involve coming up with a number to find a solution. It is also an approximation
    - Analytical method offers the exact and much quicker way in terms of calculation.
- To learn how to compute complex derivatives of complex functions we must start with something simple:

$$
f(x) = 1 \rightarrow \frac{d}{dx}f(x) = \frac{d}{dx}= 0
$$

- When Calculating the derivative of a function, the derivative can be interpreted as a slope.
- In the example the result of this function is a horizontal line as the output value for any x is 1.
- The derivative equals 0 since there is no change from one value of x to any other value of x (i.e. there is no slope).

$$
f(x) = x \rightarrow \frac{d}{dx}f(x) = \frac{d}{dx}x = \frac{dx^{1}}{dx}= 1 \cdot x^{1-1} = 1 \cdot x^{0} = 1 \cdot 1 = 1
$$

- Try the same but with 2x:

$$
f(x) = 2x \rightarrow \frac{d}{dx}f(x) = \frac{d}{dx}2x = 2 \cdot \frac{dx^{1}}{dx}= 2 \cdot 1x^{1-1} = 2 \cdot 1x^{0} = 2 \cdot 1 = 2
$$

- It’s now easy to identify what the derivative is of a function. So if you had y = 2x you would know straight away that the derivative is 2.
- But it is not as easy with non-linear equations

## Notation Types

- Leibniz notation:
    
    $$
    f'(x)=\frac{d}{dx}f(x) = \frac{df}{dx}(x) = \frac{df(x)}{dx}
    $$
    
- Prime notation:

$$
f(x) = 1 \rightarrow f'(x) = 0
$$

# Derivative Summary

The derivative of a constant equals 0 (m is a constant in this case, it’s not a parameter that we are deriving with respect, which is x in this example):

$$
\frac{d}{dx}1 = 0
\\
\frac{d}{dx}m = 0
$$

The derivative of x equals 1:

$$
\frac{d}{dx}x = 1
$$

The derivative of linear function equals its slope:

$$
\frac{d}{dx}mx + b = m
$$

# Rules:

The derivative of a constant multiplied by the function equals the constant multiplied by the function’s derivative:

$$
\frac{d}{dx}[l \cdot f(x)] = k \cdot \frac{d}{dx}f(x)
$$

The derivative of a sum of functions equals the sum of their derivatives:

$$
\frac{d}{dx}[f(x) + g(x)] = \frac{d}{dx}f(x) + \frac{d}{dx}g(x) = f'(x) + g'(x)
$$

The same concept applies to subtraction:

$$
\frac{d}{dx}[f(x) - g(x)] = \frac{d}{dx}f(x) - \frac{d}{dx}g(x) = f'(x) - g'(x)
$$

The derivative of an exponentiation:

$$
\frac{d}{dx}x^{n}=n \cdot x^{n-1}
$$