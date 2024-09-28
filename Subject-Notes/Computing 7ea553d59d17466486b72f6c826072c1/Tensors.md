# Tensors

Tensors are one of the most important parts of neural networks, all data will be handled using tensors whether that is the input variables, weights and biases or the outputs. Luckily PyTorch has an easy way that we can use tensors in python.

```python
import torch

x = torch.empty(1)

print(x)
```

```python
tensor([0.])
```

We can change the amount of value in our Tensor by changing the value in between the parentheses.

```python
x = torch.empty(5)

print(x)
```

```python
tensor([4.3065e+21, 1.1286e+27, 7.2251e+28, 4.5789e+30, 1.9051e+31])
```

These have all been 1D tensors but we can easily change the dimension as well.

```python
x = torch.empty(2, 4)

print(x)
```

```python
tensor([[1.3553e-11, 1.8754e+28, 1.7701e+31, 1.3044e-11],
        [1.6852e+22, 1.3155e-11, 1.8319e+25, 4.0372e-08]])
```

# Assigning values to tensors

If we want to give our tensor values we can use the random function, this will give every value in a tensor a random value. This is useful when creating initial weights and biases.

```python
x = torch.rand(2, 2)

print(x)
```

```python
tensor([[0.7008, 0.8462],
        [0.3596, 0.1842]])
```

Similarly to NumPy if we want to only have zeros in our tensor we do:

```python
x = torch.zeros(2,2)

print(x)
```

```python
tensor([[0., 0.],
        [0., 0.]])
```

And if we want only one:

```python
x = torch.ones(2,2)

print(x)
```

```python
tensor([[1., 1.],
        [1., 1.]])
```

# Creating tensors from lists

PyTorch also allows us to create a tensor from a python list. This is useful when you have some values that you wish to use.

```python
x = torch.tensor([2.5, 0.1])
print(x)
```

```python
tensor([2.5000, 0.1000])
```

# Data Types

We can see the data types of the values within the tensors.

```python
x = torch.ones(2,2)
print(x.dtype)
```

```python
torch.float32
```

To assign a different data type we can change the `dtype` parameter when creating the tensor.

```python
x = torch.ones(2,2, dtype=torch.int)
print(x.dtype)
```

```python
torch.int32
```

# Size of Tensors

To find the size of a tensor we use the `size()` function.

```python
x = torch.ones(2,2)
print(x.size())
```

```python
torch.Size([2, 2])
```