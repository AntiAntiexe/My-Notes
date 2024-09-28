# While Loops

# C++ While Loops

- The `while` loop loops through a block of code as long as a specified condition is true:

```cpp
while (condition) {
  // code block to be executed
}
```

## Example

```cpp
int i = 0;
while (i < 5) {
  cout << i << "\n";
  i++;
}
```

```cpp
0
1
2
3
4
```

# Do/While Loop

- The `do/while` loop is a variant of the while loop. The loop will execute the block once, before checking if the condition is true, then is will repeat the loop as long as the condition is true.

```cpp
do {
  // code block to be executed
}
while (condition);
```

## Example

```cpp
int i = 0;
do {
  cout << i << "\n";
  i++;
}
while (i < 5);
```

```cpp
0
1
2
3
4
```