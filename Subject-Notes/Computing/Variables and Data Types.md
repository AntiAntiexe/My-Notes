# Variables and Data Types

# Assigning Variables

- In C++ there are many different **types** of variables (defined with different keywords):
    - `int` - stores integers (whole numbers without decimals)
    - `double` - stores floating point numbers, numbers with decimals. You can also assign floats with the keyword `float`.
    - `char` - stores single characters, and must be assigned using single quotes ‘ ‘ not “ “.
    - `string` - stores text, they are surrounded in double quotes.
    - `boo`l  - stores values with two states: true or false.
- When assigning variables is C++ there is a certain structure you must follow:

```cpp
type variableName = value;
```

- Example:

```cpp
int myNum = 15;
```

- You also don’t have to assign the variable straight away, and then assign it later.

```cpp
int myNum;
myNum = 15;
```

## Assigning Multiple Variables in One Statement

- To declare multiple variables we can use the same structure as before.

```cpp
int x = 5, y = 6, z = 50;

cout << x + y + z
```

```powershell
61
```

# Constants

- When you do not what others (or yourself) to change existing variable values, use the `const` keyword. This will make the variable a constant, which makes it unchangeable.

```cpp
const int myNum = 15;

myNum = 10;
```

```powershell
'myNum':you cannot assign a variable that is const
```

- Constants are mostly used when there are values that should never change such as gravity or pi.