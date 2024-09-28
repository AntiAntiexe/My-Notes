# For Loop

# C++ For Loop

- When you exactly how many times you want to loop through a block of code us the `for` loop:

```cpp
for (statement 1; statement 2; statement 3) {
  // code block to be executed
}
```

- **Statement 1** is executed (one time) before the execution of the code block.
- **Statement 2** defines the condition for executing the code block.
- **Statement 3** is executed (every time) after the code block has been executed.

## Example

```cpp
for (int i = 0; i < 5; i++) {
  cout << i << endl;
}
```

```cpp
0
1
2
3
4
```

# Nested loops

- It is possible to place a loop inside another loop. This is called a nested loop.
- The “inner loop” will be executed one time for each iteration of the “outer loop”.

```cpp
// Outer loop
for (int i = 1; i <= 2; ++i) {
  cout << "Outer: " << i << "\n"; // Executes 2 times

  // Inner loop
  for (int j = 1; j <= 3; ++j) {
    cout << " Inner: " << j << "\n"; // Executes 6 times (2 * 3)
  }
}
```

```cpp
Outer: 1
 Inner: 1
 Inner: 2
 Inner: 3
Outer: 2
 Inner: 1
 Inner: 2
 Inner: 3
```

# Foreach Loop

- The foreach loop allows you to iterate through elements in an array (or other data structures).

```cpp
for (type variableName : arrayName) {
	// code block to be executed
}
```

## Example

```cpp
int myNumbers[5] = {10, 20, 30, 40, 50};

for (int i : myNumbers) {
  cout << i << "\n";
}
```

```cpp
**10
20
30
40
50**
```

# Break

- We used the `break` statement to “jump” out of a `switch` statement.
- The `break` statement can also be used to jump out of a loop.

## Example

```cpp
for (int i = 0; i < 10; i++) {
  if (i == 4) {
    break;
  }
  cout << i << "\n";
}
```

```cpp
0
1
2
3
```

# Continue

- The `continue` statement breaks one iteration (in the loop), if a specific copndition occurs, and continues with the next iteration in the loop.

## Example

```cpp
for (int i = 0; i < 10; i++) {
  if (i == 4) {
    continue;
  }
  cout << i << "\n";
}
```

```cpp
0
1
2
3
5
6
7
8
9
```

# Break and continue in a while loop

- You can also use `break` and `continue` in while loops.

## Example break

```cpp
int i = 0;
while (i < 10) {
  cout << i << "\n";
  i++;
  if (i == 4) {
    break;
  }
}
```

```cpp
0
1
2
3
```

## Example Continue

```cpp
int i = 0;
while (i < 10) {
  if (i == 4) {
    i++;
    continue;
  }
  cout << i << "\n";
  i++;
}
```

```cpp
0
1
2
3
5
6
7
8
9
```