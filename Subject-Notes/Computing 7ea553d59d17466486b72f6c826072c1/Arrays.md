# Arrays

- Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value.
- To declare an array, define the variable type, specify the name of the array followed by square brackets and specify the number of elements it should store.

```cpp
string cars[4];
```

- We have now declared a variable that holds an array of four strings. To insert values to it, we can use an array literal - place the values in a comma-separated list, inside curly braces.

```cpp
string cars[4] = {"Volvo", "BMW", "Ford", "Mazda"};
```

# Access the Elements of an Array

- You can access an element from an array by referring to the index number inside square brackets `[]`.

```cpp
string cars[4] = {"Volvo", "BMW", "Ford", "Mazda"};
cout << cars[0];
```

```cpp
Volvo
```

- Array indexes start with 0: `[0]` is the first element. `[1]` is the second element, etc.

# Change an Array Element

- To change the value of a specific element, refer to the index number:

## Example

```cpp
string cars[4] = {"Volvo", "BMW", "Ford", "Mazda"};
cars[0] = "Opel";
cout << cars[0];
```

```cpp
Opel
```

# Arrays and Loops

- You can loop through array elements with the `for` loop.

## Example

```cpp
// Create an array of strings
string cars[5] = {"Volvo", "BMW", "Ford", "Mazda", "Tesla"};

// Loop through strings
for (int i = 0; i < 5; i++) {
  cout << cars[i] << "\n";
}
```

```cpp
Volvo
BMW
Ford
Mazda
Tesla
```

# Foreach loop

- This can loops through elements in an array (and other data structures, like vectors and lists).

## Example

```cpp
// Create an array of integers
int myNumbers[5] = {10, 20, 30, 40, 50};

// Loop through integers
for (int i : myNumbers) {
  cout << i << "\n";
}
```

```cpp
10
20
30
40
50
```

# Array size

- You don’t have to write the array size when assigning an array. The compiler will know.

```cpp
string cars[] = {"Volvo", "BMW", "Ford"}; // Three array elements
```

# Get the Size of an Array

- Use the `sizeof()` operator:

```cpp
int myNumbers[5] = {10, 20, 30, 40, 50};
cout << sizeof(myNumbers);
```

```cpp
20
```

- You would expect it to output5 as there are 5 elements. However, the `sizeof()` operator returns the size type in bytes.
- The `int` type is usually 4 bytes, so from the example above, 4 x 5 (4 bytes x 5 elements) = 20 bytes.
- To find how many elements an array has, you have to divide the size of the array by the size of the data type it contains:

```cpp
int myNumbers[5] = {10, 20, 30, 40, 50};
int getArrayLength = sizeof(myNumbers) / sizeof(int);
cout << getArrayLength;
```

```cpp
5
```

# Loop Through an Array with `sizeof()`

- We can use the `sizeof()` to loop through an array with a specific amount.
- So instead of writing:

```cpp
int myNumbers[5] = {10, 20, 30, 40, 50};
for (int i = 0; i < 5; i++) {
  cout << myNumbers[i] << "\n";
}
```

- It is better to write:

```cpp
int myNumbers[5] = { 10, 20, 30, 40, 50 };

for (int i = 0; i < sizeof(myNumbers) / sizeof(int); i++) {
    cout << myNumbers[i] << '\n';
}
```

```cpp
10
20
30
40
50
```