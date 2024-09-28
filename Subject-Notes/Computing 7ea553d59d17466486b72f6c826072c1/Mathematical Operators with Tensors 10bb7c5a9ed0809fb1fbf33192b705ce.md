# Mathematical Operators with Tensors

We can do regular mathematical operations with tensors, this can be done in two ways: regular python operators (e.g. +, -, *, / etc) or using PyTorch specific tensor operators. Each of these operator perform the operations p[er element, this is called **element wise**. For example, if you have two tensors `x` and `y`, the element in the i-th row and j-th column of the resulting tensor would be the sum of the element in the i-th row and j-th column of `x` and the element in the i-th row and j-th column of `y`.

If we were to add these two “tensors” together the sum would be:

| A | B |
| --- | --- |
| C | D |

| W | X |
| --- | --- |
| Y | Z |

Answer:

| A+W | B+X |
| --- | --- |
| C+Y | D+Z |

# Addition

```python
x = torch.rand(2,2)
y = torch.rand(2,2)

z = x + y
print(z)
```

```python
tensor([[0.3974, 1.4077],
        [0.4328, 1.0795]])
```

This can also be written as

```python
x = torch.rand(2,2)
y = torch.rand(2,2)

z = torch.add(x, y)
print(z)
```

```python
tensor([[0.9288, 0.6807],
        [1.5090, 1.5401]])
```

The last way to write an addition is using in place. The in place allows you to add the sum to to the existing tensor.

```python

x = torch.rand(2,2)
y = torch.rand(2,2)
print(y)
print(x)

y.add_(x)
print(y)
```

```python
# y tensor
tensor([[0.7389, 0.4585],
        [0.3704, 0.9191]])
# x tensor
tensor([[0.3627, 0.5371],
        [0.6106, 0.8793]])
# the sum of x and y added to y
tensor([[1.1015, 0.9956],
        [0.9810, 1.7984]])
```

# Subtraction

```python
x = torch.rand(2,2)
y = torch.rand(2,2)

z = x - y
print(z)
```

```python
tensor([[-0.4172,  0.5723],
        [-0.5629, -0.4246]])
```

Which can be done with tensor library

```python
x = torch.rand(2,2)
y = torch.rand(2,2)

z = torch.sub(x,y)
print(z)
```

And the in place version

```python
x = torch.rand(2,2)
y = torch.rand(2,2)

z = sub_(x, y)
print(z)
```

# Multiplication

```python
x = torch.rand(2,2)
y = torch.rand(2,2)

z = x * y
print(z)
```

```python
tensor([[0.2088, 0.3472],
        [0.0105, 0.0024]])
```

Using the PyTorch library

```python
x = torch.rand(2,2)
y = torch.rand(2,2)

z = torch.mul(x, y)
print(z)
```

And the in place version

```python
x = torch.rand(2,2)
y = torch.rand(2,2)

z = torch.mul_(x, y)
print(z)
```

# Division

```python
x = torch.rand(2,2)
y = torch.rand(2,2)

z = x / y
print(z)
```

```python
tensor([[2.5034, 0.8601],
        [0.6866, 1.0467]])
```

Using the PyTorch library

```python
x = torch.rand(2,2)
y = torch.rand(2,2)

z = torch.div(x, y)
print(z)
```

And the in place version

```python
x = torch.rand(2,2)
y = torch.rand(2,2)

z = torch.div_(x, y)
print(z)
```