# Functions

- In python functions are block of reusable code that perform specific tasks.
- They allow you to break down complex problems into smaller, more manageable parts, making you code easier to read and maintain.

if your variable is inside a function it called a local variable and outside is called a outside variable. Programmers avoid global variables as if it changes it will break the entire code.

## Return

The Python return statement **marks the end of a function and specifies the value or values to pass back from the function**. Return statements can return data of any type, including integers, floats, strings, lists, dictionaries, and even other functions.

example:

```python
def function_name(parameter1, parameter2,...)

```

example:

```python
def sum_of_two():
  func_total = x + y
  print(func_total)

x = int(input("Number 1: "))
y = int(input("Number 2: "))
sum_of_two()
```

```python
Number 1: #5
Number 2: #6
11
```

another:

```python
def greet():
  return f"Hello, {name}!"
name = input("name: ")
greet(name)
```