# Multi-Dimensional Arrays

- A multi-dimensional array is an array of arrays.
- To declare a multi-dimensional array, define the variable type, specify the name of the array followed by square brackets which specify how many elements the main array has, followed by another set of square brackets which indicates how many elements the sub-arrays have:

```cpp
string letters[2][4];
```

- As with ordinary arrays, you can insert values with an array literal - a comma - separated list inside curly braces. In a multi-dimensional array, each element in an array literal is another array literal.

```cpp
string letters[2][4] = {
  { "A", "B", "C", "D" },
  { "E", "F", "G", "H" }
};
```

- Each set of square brackets in an array declaration adds another dimension to an array. An array like the one above is said to have two dimensions.
- Arrays can have any number of dimensions. The more dimensions an array has, the more complex the code becomes. The following array has three dimensions:

```cpp
 string letters[2][2][2] = {
  {
    { "A", "B" },
    { "C", "D" }
  },
  {
    { "E", "F" },
    { "G", "H" }
  }
};
```

# Access the Elements of a Multi-Dimensional Array